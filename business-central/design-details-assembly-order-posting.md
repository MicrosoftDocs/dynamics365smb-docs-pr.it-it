---
title: Dettagli di progettazione - Registrazione dell'ordine di assemblaggio
description: La registrazione dell'ordine di assemblaggio è basata sugli stessi principi della registrazione delle attività analoghe degli ordini di vendita e del consumo di produzione o dell'output.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/15/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="design-details-assembly-order-posting"></a>Dettagli di progettazione: Registrazione dell'ordine di assemblaggio
La registrazione dell'ordine di assemblaggio è basata sugli stessi principi della registrazione delle attività analoghe degli ordini di vendita e del consumo di produzione o dell'output. Tuttavia, i principi vengono combinati nel fatto che gli ordini di assemblaggio dispongono di una propria interfaccia utente di registrazione, quella per gli ordini di vendita, mentre l'effettiva registrazione dei movimenti si verifica in background come registrazioni dirette di risorse e articoli, come quella per il consumo di produzione, l'output e la capacità.  

Analogamente alla registrazione dell'ordine di produzione, i componenti consumati e le risorse utilizzate vengono convertiti e resi come articolo di assemblaggio una volta registrato l'ordine di assemblaggio. Per ulteriori informazioni, vedere [Dettagli di progettazione: Registrazione dell'ordine di produzione](design-details-production-order-posting.md). Tuttavia, il flusso dei costi per gli ordini di assemblaggio è meno complesso, soprattutto perché la registrazione dei costi di assemblaggio si verifica solo una volta e pertanto non genera magazzino WIP.  

Le seguenti registrazioni si verificano durante la registrazione dell'ordine di assemblaggio:  

-   Le registrazioni magazzino registrano movimenti contabili articoli positivi, che rappresentano l'uscita dell'articolo di assemblaggio, dall'intestazione dell'ordine di assemblaggio  
-   Le registrazioni magazzino registrano movimenti contabili articoli negativi, che rappresentano il consumo di componenti di assemblaggio, dalle righe ordine di assemblaggio.  
-   Le registrazioni risorse registrano l'utilizzo delle risorse di assemblaggio (unità di tempo), dalle righe ordine di assemblaggio.  
-   Le registrazioni capacità registrano movimenti di valorizzazione relativi all'utilizzo delle risorse, dalle righe ordine di assemblaggio.  

Nel seguente diagramma viene mostrata la struttura dei movimenti contabili risorse e articolo che derivano dalla registrazione dell'ordine di assemblaggio.  

![Movimenti contabili capacità, risorse e articolo che derivano dalla registrazione dell'ordine di assemblaggio.](media/design_details_assembly_posting_1.png "Movimenti contabili capacità, risorse e articolo che derivano dalla registrazione dell'ordine di assemblaggio")  

> [!NOTE]  
>  Le aree di lavoro e di produzione sono incluse per illustrare che i movimenti contabili capacità vengono creati sia dalla produzione che dall'assemblaggio.  

Nel seguente diagramma viene mostrato il flusso dei dati di assemblaggio nei movimenti contabili durante la registrazione:  

![Flusso dei movimenti correlati all'assemblaggio durante la registrazione.](media/design_details_assembly_posting_2.png "Flusso dei movimenti correlati all'assemblaggio durante la registrazione")  

## <a name="posting-sequence"></a>Sequenza di registrazione
La registrazione di un ordine di assemblaggio viene eseguita nel seguente ordine:  

1.  Le righe dell'ordine di assemblaggio vengono registrate.  
2.  L'intestazione dell'ordine di assemblaggio viene registrata.  

Nella seguente tabella viene illustrata la sequenza di azioni.  

|Azione|Description|  
|------------|-----------------|  
|Inizializzare la registrazione|1. Effettuare i controlli preliminari.<br />2. Aggiungere il numero di registrazione e modificare l'intestazione dell'ordine di assemblaggio.<br />3. Rilasciare l'ordine di assemblaggio.|  
|Spedizioni postali|<ol><li>Creare l'intestazione dell'ordine di assemblaggio registrato.</li><li>Copiare le righe commento.</li><li>Registrare le righe ordine di assemblaggio (consumo):<br /><br /> <ol><li>Creare una pagina di stato per calcolare il consumo in fase di assemblaggio.</li><li>Ottenere la quantità residua su cui verrà basata la riga del giornale di registrazione.</li><li>Reimpostare le quantità consumate e residue.</li><li>Per le righe dell'ordine di assemblaggio del tipo Articolo:<br /><br /> <ol><li>Compilare i campi nella riga di registrazione magazzino.</li><li>Trasferire gli impegni alla riga di registrazione magazzino.</li><li>Registrare la riga di registrazione magazzino per creare i movimenti contabili articoli.</li><li>Creare le righe di registrazione e registrarle.</li></ol></li><li>Per le righe dell'ordine di assemblaggio del tipo Risorsa:<br /><br /> <ol><li>Compilare i campi nella riga di registrazione magazzino.</li><li>Contabilizzare la riga di registrazione magazzino. Vengono creati così dei movimenti contabili capacità.</li><li>Creare e registrare la riga delle registrazioni risorse.</li></ol></li><li>Trasferire i valori del campo della riga ordine di assemblaggio in una nuova riga ordine di assemblaggio registrata.</li></ol></li><li>Registrare l'intestazione ordine di assemblaggio (output):<br /><br /> <ol><li>Compilare i campi nella riga di registrazione magazzino.</li><li>Trasferire gli impegni alla riga di registrazione magazzino.</li><li>Registrare la riga di registrazione magazzino per creare i movimenti contabili articoli.</li><li>Creare le righe di registrazione e registrarle.</li><li>Reimpostare le quantità di assemblaggio e le quantità residue.</li></ol></li></ol>|  

> [!IMPORTANT]  
>  A differenza dell'output di produzione, che viene registrato al costo previsto, l'output di assemblaggio viene registrato al costo effettivo.  

## <a name="cost-adjustment"></a>Rettifica costo
 Un volta registrato un ordine di assemblaggio, ovvero una volta che i componenti (materiale) e le risorse sono assemblati in un nuovo articolo, dovrebbe essere possibile determinare il costo effettivo di tale articolo di assemblaggio e il costo di magazzino effettivo dei componenti interessati. A tal fine vengono inoltrati i costi dai movimenti registrati dell'origine (i componenti e le risorse) ai movimenti registrati della destinazione (l'articolo di assemblaggio). L'inoltro di costi viene svolto calcolando e generando nuovi movimenti, chiamati movimenti di rettifica, che vengono associati ai movimenti di destinazione.  

 I costi di assemblaggio da inoltrare vengono rilevati attraverso il meccanismo di tracciabilità del livello di ordine. Per informazioni su altri meccanismi di rilevazione rettifica, vedere [Dettagli di progettazione: Rettifica costo](design-details-cost-adjustment.md).  

### <a name="detecting-the-adjustment"></a>Rilevazione della rettifica
La funzione di rilevamento del livello di ordine viene utilizzata in scenari di conversione, produzione e assemblaggio. Le funzioni della funzione sono le seguenti:  

-   La rettifica dei costi viene rilevata contrassegnando l'ordine ogni volta che una risorsa o un materiale viene registrato come utilizzato o consumato.  
-   Il costo viene inoltrato applicando i costi dalla risorsa o dal materiale ai movimenti di output associati allo stesso ordine.  

Nel seguente grafico viene visualizzata la struttura del movimento di rettifica e in che modo vengono rettificati i costi di assemblaggio.  

![Flusso dei movimenti correlati all'assemblaggio durante la rettifica costi.](media/design_details_assembly_posting_3.png "Flusso dei movimenti correlati all'assemblaggio durante la registrazione")  

### <a name="performing-the-adjustment"></a>Esecuzione della rettifica
La distribuzione delle rettifiche rilevate dai costi delle risorse e dei materiali nei movimenti di output assemblaggio viene eseguita dal processo batch **Rettifica costo - Movimenti articoli**. Contiene la funzione di rettifica multilivello, che è costituita dai seguenti due elementi:  

-   Rettifica ordine di assemblaggio, che inoltra il costo del materiale e dell'utilizzo delle risorse al movimento di output assemblaggio. Ciò è dovuto alle righe 5 e 6 dell'algoritmo riportato di seguito.  
-   Eseguire rettifiche a livello singolo, che inoltra i costi per i singoli articoli utilizzando il relativo metodo di costing. Ciò è dovuto alle righe 9 e 10 dell'algoritmo riportato di seguito.  

![Riepilogo dell'algoritmo di rettifica costo per la registrazione di assemblaggio.](media/design_details_assembly_posting_4.jpg "Riepilogo dell'algoritmo di rettifica costo per la registrazione di assemblaggio")  

> [!NOTE]  
>  L'elemento di creazione rettifiche WIP alle righe 7 e 8 è responsabile dell'inoltro del materiale di produzione e dell'utilizzo della capacità all'output di ordini di produzione non completati. Non viene utilizzato per la rettifica dei costi dell'ordine di assemblaggio in quanto il concetto di WIP non si applica all'assemblaggio.  

Per ulteriori informazioni su come i costi dall'assemblaggio e della produzione vengono registrati nella contabilità generale, vedere [Dettagli di progettazione: Registrazione di magazzino](design-details-inventory-posting.md).  

## <a name="assembly-costs-are-always-actual"></a>I costi di assemblaggio sono sempre effettivi
 Il concetto WIP (WIP) non si applica alla registrazione dell'ordine di assemblaggio. I costi di assemblaggio vengono registrati solo come costo effettivo, mai come costo previsto. Per ulteriori informazioni, vedere [Dettagli di progettazione: Registrazione costi previsti](design-details-expected-cost-posting.md).  

Ciò è possibile grazie alla seguente struttura dei dati.  

-   Nel campo **Tipo** nelle righe delle registrazioni magazzino, nelle tabelle **Movimento contabile capacità** e **Movimenti valorizzazione**, il parametro *Risorsa* viene utilizzato per identificare i movimenti di risorse di assemblaggio.  
-   Nel campo **Tipo mov. articolo** nelle righe delle registrazioni magazzino, nelle tabelle **Movimento contabile capacità** e **Movimenti valorizzazione**, vengono utilizzati i parametri *Output assemblaggio* e *Consumo assemblaggio* per identificare rispettivamente i movimenti di articoli di assemblaggio in uscita e i movimenti di componenti di assemblaggio consumati.  

Inoltre, i campi della categoria di registrazione nella testata ordine di assemblaggio e nelle righe ordine di assemblaggio vengono popolati per impostazione predefinita come indicato di seguito.  

|Entità|Tipo|Business IVA|Righe Cat. reg. art./serv.|  
|------------|----------|-------------------|------------------------------|  
|Testata ordine di assemblaggio|Articolo|Cat. reg. magazzino|Righe Cat. reg. art./serv.|  
|Riga ordine di assemblaggio|Articolo|Cat. reg. magazzino|Righe Cat. reg. art./serv.|  
|Riga ordine di assemblaggio|Risorsa||Righe Cat. reg. art./serv.|  

Di conseguenza, solo i costi effettivi vengono registrati nella contabilità generale e nessun conto provvisorio viene compilato dalla registrazione dell'ordine di assemblaggio. Per ulteriori informazioni, vedere [Dettagli di progettazione: Conti nella contabilità generale](design-details-accounts-in-the-general-ledger.md).  

## <a name="assemble-to-order"></a>Assemblaggio su ordine
Il movimento contabile articolo che risulta dalla registrazione di una vendita di assemblaggio su ordine è collegato in modo fisso al movimento contabile articolo correlato per l'output di assemblaggio. Di conseguenza, il costo di una vendita di assemblaggio su ordine è derivato dall'ordine di assemblaggio a cui è stato collegato.  

I movimenti contabili articoli di tipo Vendita che derivano dalla registrazione delle quantità di assemblaggio su ordine sono contrassegnati con **Sì** nel campo **Assemblaggio su ordine**.  

La registrazione di righe ordini di vendita in cui una parte è quantità di magazzino e un'ulteriore parte è quantità per l'assemblaggio su ordine dà come risultato movimenti contabili articoli separati, uno per la quantità di magazzino e uno per la quantità per l'assemblaggio su ordine.  

### <a name="posting-dates"></a>Date di registrazione

In generale, le date di registrazione vengono copiate da un ordine cliente nell'ordine di assemblaggio collegato. La data di registrazione nell'ordine di assemblaggio viene aggiornata automaticamente quando si modifica la data di registrazione nell'ordine cliente direttamente o indirettamente, ad esempio se modifichi la data di registrazione nella spedizione di magazzino, nel prelievo di magazzino o come parte di una registrazione in blocco.

Puoi modificare manualmente la data di registrazione nell'ordine di assemblaggio. Tuttavia, non può essere successiva alla data di registrazione nell'ordine cliente collegato. Il sistema manterrà questa data a meno che non aggiorni la data di registrazione nell'ordine cliente.


## <a name="see-also"></a>Vedi anche
 [Dettagli di progettazione: Costing di magazzino](design-details-inventory-costing.md)   
 [Dettagli di progettazione: Registrazione dell'ordine di produzione](design-details-production-order-posting.md)   
 [Dettagli di progettazione: Metodi di costing](design-details-costing-methods.md)  
 [Gestione dei costi di magazzino](finance-manage-inventory-costs.md)  
 [Finanze](finance.md)  
 [Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
