---
title: 'Eseguire la pianificazione completa, MPS o MRP'
description: Il sistema di pianificazione può calcolare la programmazione MPS o la pianificazione MRP su richiesta oppure entrambe contemporaneamente.
author: brentholtorf
ms.topic: conceptual
ms.search.form: '99000852, 99000860'
ms.date: 01/24/2024
ms.author: bholtorf
ms.reviewer: andreipa
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Eseguire la pianificazione completa, MPS o MRP

L'espressione "esecuzione del prospetto di pianificazione" o "esecuzione di MRP" si riferisce al calcolo della programmazione di produzione master e delle richieste di materiale. Il calcolo si basa sulla domanda effettiva e prevista. Il sistema di pianificazione può calcolare la programmazione MPS o la pianificazione MRP su richiesta oppure entrambe contemporaneamente.  

- Per MPS si intende il calcolo di una programmazione produzione master in base alla domanda effettiva e alla previsione della domanda. Il calcolo MPS viene utilizzato per articoli finali associati a una riga ordine di vendita o previsione. Tali articoli sono denominati articoli MPS e sono identificati dinamicamente all'inizio del calcolo.  
- Per MRP si intende il calcolo delle richieste di materiale in base alla domanda effettiva di componenti e alla previsione della domanda a livello di componente. La programmazione MRP viene calcolata solo per articoli diversi dagli articoli MPS. Lo scopo generale della pianificazione MRP consiste nel fornire piani formali rapportati alla scala cronologica, in base all'articolo, per fornire l'articolo corretto al momento giusto, nel luogo adatto e nella quantità appropriata.  

Gli algoritmi di pianificazione per MPS e MRP sono identici. Gli algoritmi di pianificazione riguardano il confronto. il riutilizzo di ordini di approvvigionamento esistenti e messaggi di azione. Il processo del sistema di pianificazione analizza cosa è necessario o sarà necessario (domanda) e cosa è disponibile o previsto (approvvigionamento). Quando tali quantità vengono confrontate, [!INCLUDE[prod_short](includes/prod_short.md)] fornisce messaggi di azione. I messaggi di azione sono suggerimenti relativi alla creazione di un nuovo ordine, alla modifica di un ordine (quantità o data) o all'annullamento di un ordine. Il termine "ordine" include ordini di acquisto, ordini di assemblaggio, ordini di produzione e ordini di trasferimento.

Puoi tenere traccia dei collegamenti creati dalla pianificazione tra domanda e approvvigionamento nella pagina **Tracciabilità ordine**. Per ulteriori informazioni, vedere [Tenere traccia delle relazioni tra domanda e approvvigionamento](production-how-track-demand-supply.md)

La correttezza dei risultati di pianificazione dipende dal setup di schede articolo, DB di assemblaggio, DB di produzione e cicli.  

## Metodi per la generazione di un piano  

- **Calcola piano - Rigenerativo:** consente di elaborare o rigenerare il piano del materiale. Il processo inizia con l'eliminazione di tutti gli ordini approvvigionamento attualmente caricati. Tutti gli articoli inclusi nel database vengono ripianificati.  
- **Calcola piano - Solo cambiamenti**: consente di elaborare un piano dei cambiamenti. In questo piano gli articoli vengono considerati come da due tipi di cambiamenti:  
   - **Cambiamenti relativi a domanda/approvvigionamento:** tali cambiamenti includono modifiche alle quantità negli ordini di vendita, nelle previsioni della domanda, negli ordini di assemblaggio, negli ordini di produzione o negli ordini di acquisto. Un cambiamento non pianificato a livello di magazzino viene anche considerato un cambiamento di quantità.  
   - **Cambiamenti relativi ai parametri di pianificazione:** tali cambiamenti includono modifiche alla scorta di sicurezza, al punto di riordino, al ciclo, alla distinta base e alle modifiche all'intervallo di tempo o al calcolo del lead time.  
- **Genera messaggi di azione:** funge da strumento di pianificazione a breve termine tramite l'emissione di messaggi di azione per avvisare l'utente di eventuali modifiche apportate dall'ultimo calcolo del piano rigenerativo o relativo ai cambiamenti.  

Con ogni metodo pianificato, [!INCLUDE[prod_short](includes/prod_short.md)] genera movimenti di prospetto in cui si presuppone una capacità infinita. La capacità del centro di lavoro e dell'area di produzione non viene presa in considerazione durante lo sviluppo delle pianificazioni.  

> [!IMPORTANT]  
> La funzione Calcola piano - Rigenerativo rappresenta il processo utilizzato più comunemente. Le funzioni Calcola piano e Esegui messaggi di azione, tuttavia, possono essere utilizzate per eseguire il processo Calcola Piano - Solo Cambiamenti.  
>
> È possibile eseguire il piano Ottieni messaggi di azione tra le esecuzioni della pianificazione delle modifiche nette e rigenerative per ottenere una visualizzazione immediata dell'effetto delle modifiche alla pianificazione. Tuttavia, non è destinato a sostituire l'intero processo rigenerativo o di pianificazione del cambiamento netto.  

## Per calcolare il prospetto pianificazione
  
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Prospetti pianificazione**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Calcola piano - Rigenerativo** per aprire la pagina **Calcola piano**.  
3. Nella Scheda dettaglio **Opzioni** compilare i campi come descritto nella tabella riportata di seguito.  

    |Campo|Descrizione|  
    |---------------------------------|---------------------------------------|  
    |**MPS**|Calcolare un programma di produzione principale. Gli articoli con ordini di vendita aperti e/o previsioni della domanda vengono inclusi nell'esecuzione. <br/>Se per tali articoli esistono anche altri fabbisogni, ad esempio scorte di sicurezza, punti di riordino o linee di componenti di produzione aperte, tali fabbisogni vengono inclusi nel calcolo MPS per garantire che il sistema di pianificazione gestisca il profilo scorte completo.  |  
    |**MRP**|Programmazione del fabbisogno di materiali calcolate. Gli articoli con richieste dipendenti vengono inclusi nell'esecuzione. In genere, MPS e MRP sono eseguiti contemporaneamente. Per eseguire MPS e MRP simultaneamente, nella pagina **Manufacturing Setup**, nella scheda dettaglio **Pianificazione**, seleziona il campo **Calcolo combinato MPS/MRP**.|  
    |**Data Inizio**|Calcola disponibilità magazzino. Se la quantità disponibile di un articolo è inferiore al punto di riordino, nel sistema viene eseguita una programmazione in avanti di un ordine di rifornimento da questa data. Se un articolo è inferiore alla relativa scorta di sicurezza (alla data di inizio), nel sistema viene eseguita una programmazione a ritroso di un ordine di rifornimento con scadenza alla data di inizio della pianificazione.|  
    |**Data Fine**|Data di fine dell'orizzonte di pianificazione. Dopo questa data non viene considerato alcun approvvigionamento o alcuna domanda. Se il ciclo di riordino per un articolo si protrae oltre la data di fine, l'orizzonte di pianificazione effettivo per l'articolo equivale a Data ordine più Ciclo riordino.<br/><br/> L'orizzonte di pianificazione è il tempo per cui si protrae il piano. Se l'orizzonte è troppo ridotto, gli articoli con un lead time maggiore non vengono ordinati in tempo. Se l'orizzonte è troppo esteso, viene impiegata un'eccessiva quantità di tempo nell'esaminare ed elaborare le informazioni soggette a probabili modifiche prima del necessario. È possibile impostare un orizzonte di pianificazione per la produzione e uno più esteso per gli acquisti. È consigliabile impostare un orizzonte di pianificazione e uno per gli acquisti per coprire il lead time totale per i componenti.|  
    |**Interrompi e mostra primo errore**|Seleziona questa opzione se si desidera che l'esecuzione della pianificazione si interrompa non appena viene rilevato un errore. Viene visualizzato un messaggio contenente le informazioni sull'errore. Se è presente un errore, nel prospetto pianificazione verranno presentate solo le righe di pianificazione create prima dell'individuazione dell'errore. Se questo campo non è selezionato, il processo batch **Calcola piano** continuerà fino a completamento. Gli errori non interrompono il processo batch. Se sono presenti uno o più errori, dopo il completamento viene visualizzato un messaggio con informazioni sugli articoli interessati. Verrà quindi visualizzata la pagina **Log errori pianificazione**, in cui saranno disponibili ulteriori dettagli sull'errore e i collegamenti alle schede articolo interessate.|  
    |**Usa previsione**|Seleziona una previsione da includere come domanda durante l'esecuzione del processo batch di pianificazione. La previsione predefinita è impostata nella Scheda dettaglio **Pianificazione** della pagina **Setup manufacturing**.|  
    |**Escludi previsione prima**|Specifica la quantità della previsione selezionata da includere nell'esecuzione della pianificazione immettendo una data prima della quale la domanda di previsione non viene inclusa.|  
    |**Rispetta parametri di pianificazione per avvisi di eccezione**|Questo campo è selezionato di default.<br/><br/> L'approvvigionamento nelle righe di pianificazione con avvisi in genere non viene modificato in base ai parametri di pianificazione. Al contrario, il sistema di pianificazione suggerisce solo un approvvigionamento per coprire la quantità di domanda esatta. Tuttavia, è possibile definire alcuni parametri di pianificazione per le righe di pianificazione da rispettare con determinati avvisi.<br/><br/>|  

4. Nella Scheda dettaglio **Articolo** è impostare i filtri ed eseguire la pianificazione in base ad articolo, descrizione articolo o ubicazione.  
5. Scegli il pulsante **OK**. Verrà eseguito il processo batch, quindi nel prospetto di pianificazione verranno inserite le righe di pianificazione.  

## Per eseguire i messaggi di azione
  
1. Nella pagina **Prospetto pianificazione** scegliere l'azione **Esegui messaggi di azione**.  
2. Nella Scheda dettaglio **Opzioni** specificare come creare gli approvvigionamenti. Compilare i campi come indicato nella tabella seguente.  

    |Campo|Descrizione|  
    |---------------------------------|---------------------------------------|  
    |**Ordine di produzione**|Specifica come creare ordini di produzione. A tale scopo, è possibile utilizzare direttamente le proposte delle righe di pianificazione. È possibile creare ordini di produzione pianificati o confermati.|  
    |**Ordine di assemblaggio**|Specifica il modo in cui creare gli ordini di assemblaggio. A tale scopo, è possibile utilizzare direttamente le proposte delle righe di pianificazione.|  
    |**Ordine di acquisto**|Specifica come creare gli ordini di acquisto. A tale scopo, è possibile utilizzare direttamente le proposte delle righe di pianificazione.<br/><br/> Se si è scelto di copiare le proposte delle righe di pianificazione per gli ordini di acquisto nelle richieste di approvvigionamento, selezionare la definizione e il nome del prospetto.|  
    |**Ordine di trasferimento**|Specifica il modo in cui si desidera creare gli ordini di trasferimento. A tale scopo, è possibile utilizzare direttamente le proposte delle righe di pianificazione.<br/><br/> Se si è scelto di copiare le proposte delle righe di pianificazione per gli ordini di trasferimento nelle richieste di approvvigionamento, selezionare la definizione e il nome del prospetto.|  
    |**Combina ordini di trasferimento**|Selezionare se si desidera combinare gli ordini di trasferimento.|  
    |**Interrompi e mostra primo errore**|Seleziona questa opzione se si desidera che il processo batch **Pianificaz. - Esegui mess. azione** si interrompa appena viene rilevato un errore. Viene visualizzato un messaggio contenente le informazioni sull'errore. Se si verifica un errore, solo le righe di pianificazione elaborate prima dell'errore creeranno gli ordini di approvvigionamento.|  

3. Nella Scheda dettaglio **Riga pianificazione** è possibile impostare filtri per limitare l'esecuzione dei messaggi di azione.  
4. Scegliere il pulsante **OK**.  

Al termine dell'esecuzione del messaggio di azione, tramite il processo batch vengono eliminate le righe nel prospetto di pianificazione. Le righe meno recenti vengono mantenute nel prospetto di pianificazione fino a quando non vengono accettate in una data successiva o eliminate. È anche possibile eliminare le righe manualmente.  

## Messaggi di azione
  
I messaggi azione vengono generati dal sistema di tracciabilità degli ordini quando non è possibile raggiungere il saldo all'interno della rete di ordini esistente. I messaggi possono essere visualizzati come suggerimento per l'elaborazione delle modifiche che consentano di ristabilire l'equilibrio tra approvvigionamento e domanda.  

La generazione dei messaggi di azione si verifica a un livello per volta, considerando il codice di ultimo livello di ciascun articolo. In questo modo, verranno sicuramente presi in considerazione tutti gli articoli soggetti a modifiche relative all'approvvigionamento o alla domanda.  

Per evitare la visualizzazione di messaggi di azione non significativi, superflui o non pertinenti, l'utente può stabilire smorzamenti, che consentono di ridurre la generazione dei messaggi di azione solo alle modifiche che superano la quantità o il numero di giorni specificati.  

Dopo avere esaminato i messaggi di azione e avere determinato se accettare alcune o tutte le modifiche suggerite, selezionare il campo **Accetta messaggio azione**. Successivamente, aggiorna le programmazioni di conseguenza.  

> [!NOTE]  
> Un messaggio azione è un suggerimento relativo alla creazione di un nuovo ordine, all'annullamento di un ordine o alla modifica della quantità o della data di un ordine. L'ordine può essere di acquisto, di trasferimento o di produzione.  

In risposta a qualsiasi mancato saldo tra approvvigionamento e domanda, vengono generati i seguenti messaggi di azione  

|Messaggio di azione|Descrizione|  
|--------------------|---------------------------------------|  
|**Nuovo**|Se non è possibile soddisfare una domanda tramite i messaggi di azione in **Modifica qtà**, **Riprogramma** o **Riprogr. e mod. qtà** per gli ordini esistenti, viene generato il messaggio azione **Nuovo**, in cui viene suggerito un nuovo ordine. Viene generato un messaggio **Nuovo** anche se non sono presenti ordini di approvvigionamento esistenti nel ciclo di riordino dell'articolo. Questa opzione determina il numero di periodi in avanti e a ritroso nel profilo di disponibilità durante la ricerca di un ordine da ripianificare.|  
|**Modifica qtà**|Quando la domanda tracciata in uno o più ordini di approvvigionamento è soggetta a una modifica della quantità, viene generato il messaggio di azione **Modifica qtà**. Il messaggio indica che è necessario modificare l'approvvigionamento correlato in base alla modifica verificatasi nella domanda. Se viene rilevata una nuova domanda, in [!INCLUDE[prod_short](includes/prod_short.md)] viene eseguita la ricerca del più vicino ordine di approvvigionamento non impegnato esistente nel ciclo di riordino e per tale ordine viene generato un messaggio di azione di modifica.|  
|**Riprogramma**|Quando in un ordine di approvvigionamento o domanda si verifica una modifica alla data che provoca un mancato saldo nella rete di ordini, viene generato il messaggio azione **Riprogramma**. Se tra la domanda e l'approvvigionamento vi è una relazione uno a uno, viene generato un messaggio di azione che suggerisce lo spostamento dell'ordine di approvvigionamento. Se l'ordine di approvvigionamento riguarda una domanda da più ordini di vendita, l'ordine di approvvigionamento viene riprogrammato in base alla data della prima domanda.|  
|**Riprogr. e mod. qtà.**|Se sono state modificate sia le date sia le quantità di un ordine, è necessario modificare i piani relativamente a entrambe le situazioni. Le due azioni vengono riunite in un unico messaggio, **Riprogr. e mod. qtà.**, per garantire il ripristino del saldo nella rete di ordini.|  
|**Annulla**|Se una domanda, trattata su base ordine-a-ordine, viene eliminata, viene generato un messaggio di azione per annullare gli ordini di approvvigionamento correlati. Se la relazione non è di tipo ordine-a-ordine, viene generato un messaggio di azione per ridurre l'approvvigionamento. Se a causa di altri fattori, ad esempio le rettifiche del magazzino, non è necessario alcun ordine di approvvigionamento nel momento in cui i messaggi di azione vengono generati, viene generato da [!INCLUDE[prod_short](includes/prod_short.md)] un messaggio di azione **Annulla**.|  

## Vedere anche  

[Pianif.](production-planning.md)  
[Impostazione della produzione](production-configure-production-processes.md)  
[Produzione](production-manage-manufacturing.md)    
[Inventario](inventory-manage-inventory.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Dettagli di progettazione: Pianificazione approvvigionamento](design-details-supply-planning.md)   
[Impostare le procedure ottimali: Pianificazione forniture](setup-best-practices-supply-planning.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
