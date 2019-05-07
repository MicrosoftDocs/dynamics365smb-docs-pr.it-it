---
title: Ricezione e stoccaggio nella gestione avanzata della warehouse | Documenti Microsoft
description: In Business Central, i processi in entrata per la ricezione e lo stoccaggio possono essere eseguiti in quattro modalità utilizzando diverse funzionalità a seconda del livello di complessità della warehouse.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 533d3b3c755294e07ca921df028f7742a388fad1
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2019
ms.locfileid: "932881"
---
# <a name="walkthrough-receiving-and-putting-away-in-advanced-warehouse-configurations"></a>Procedura dettagliata - Ricezione e stoccaggio nelle configurazioni di warehouse avanzate

**Nota**: questa procedura dettagliata deve essere eseguita in una società demo con l'opzione **Valutazione completa - Completo dati di esempio**, che è disponibile nell'ambiente sandbox. Per ulteriori informazioni, vedere [Creare un ambiente sandbox](across-how-create-sandbox-environment.md).

In [!INCLUDE[d365fin](includes/d365fin_md.md)], i processi in entrata per la ricezione e lo stoccaggio possono essere eseguiti in quattro modalità utilizzando diverse funzionalità a seconda del livello di complessità della warehouse.  

|Metodo|Processo in entrata|Collocazioni|Carichi|Stoccaggi|Livello di complessità (vedere [Dettagli di progettazione: Setup warehouse](design-details-warehouse-setup.md))|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Registrare il carico e lo stoccaggio dalla riga ordine|X|||2|  
|B|Registrare il carico e lo stoccaggio da un documento di stoccaggio magazzino|||X|3|  
|C|Registrare il carico e lo stoccaggio da un documento di carico warehouse||X||5/4/6|  
|D|Registrare il carico da un documento di carico warehouse e registrare lo stoccaggio da un documento di stoccaggio warehouse||X|X|5/4/6|  

Per ulteriori informazioni, vedere [Dettagli di progettazione: Flusso warehouse in entrata](design-details-inbound-warehouse-flow.md).  

Nella seguente procedura dettagliata viene dimostrato il metodo D nella tabella precedente.  

## <a name="about-this-walkthrough"></a>Informazioni sulla procedura dettagliata  
Nelle configurazioni di warehouse avanzate in cui un'ubicazione è impostata in modo da richiedere l'elaborazione di carichi oltre all'elaborazione di stoccaggi, utilizzare la pagina **Carico warehouse** per registrare e contabilizzare il carico di articoli su più ordini in entrata. Quando il carico warehouse è registrato, viene creato uno o più documenti di stoccaggio warehouse per istruire gli addetti warehouse sulla ricezione e lo stoccaggio dell'articolo ricevuto nelle aree definite in base alla collocazione stabilita o in altre collocazioni. L'ubicazione specifica degli articoli viene registrata quando viene registrato lo stoccaggio warehouse. Il documento di origine in entrata può essere un ordine di acquisto, un ordine di reso da vendita, un ordine di trasferimento in entrata, un assemblaggio o un ordine di produzione il cui output è pronto per lo stoccaggio. Se il carico viene creato per un ordine in entrata, più di un documento di origine in entrata può essere recuperato per il carico. Utilizzando questo metodo è possibile registrare più articoli in arrivo da ordini in entrata diversi con un carico.  

In questa procedura dettagliata sono illustrati i task seguenti.  

-   Impostazione dell'ubicazione BIANCA per la ricezione e lo stoccaggio.  
-   Creazione e rilascio di due ordini di acquisto per una gestione warehouse completa.  
-   Creazione e registrazione di un documento di carico warehouse per più righe di ordini di acquisto da fornitori specifici.  
-   Registrazione dello stoccaggio warehouse per gli articoli ricevuti.  

## <a name="roles"></a>Ruoli  
Questa procedura dettagliata comprende task svolti dai ruoli utente seguenti:  

-   Manager warehouse  
-   Rivenditore  
-   Personale di ricezione  
-   Lavoro warehouse  

## <a name="prerequisites"></a>Prerequisiti  
Per completare questa procedura dettagliata, sarà necessario:  

-   CRONUS International Ltd. installato.  
-   Per diventare un impiegato warehouse presso l'ubicazione BIANCA effettuando i seguenti passaggi:  

1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Impiegati warehouse** e quindi scegliere il collegamento correlato.  
2.  Selezionare il campo **ID utente** , quindi il proprio account utente nella pagina **Utenti**.  
3.  Nel campo **Codice ubicazione** immettere BIANCO:  
4.  Selezionare il campo **Default**.  

## <a name="story"></a>Scenario  
Ellen, responsabile warehouse presso CRONUS International Ltd., crea due ordini di acquisto per articoli relativi agli accessori dai fornitori 10000 e 20000 che devono essere consegnati al magazzino BIANCO. Quando le consegne giungono alla warehouse, Sammy, responsabile della ricezione degli articoli dai fornitori 10000 e 20000, utilizza un filtro per creare righe di carico per gli ordini di acquisto che arrivano dai due fornitori. Sammy registra gli articoli ricevuti nel magazzino in un carico warehouse e li mette a disposizione per la vendita o altre richieste. John, il lavoratore warehouse, prende gli articoli dalla collocazione di ricevimento e li stocca. Stocca tutte le unità nelle proprie collocazioni di default, eccetto 40 su 100 cerniere ricevute durante lo stoccaggio nel reparto di assemblaggio suddividendo la riga di stoccaggio. Quando John registra lo stoccaggio, il contenuto delle collocazioni viene aggiornato e gli articoli vengono resi disponibili per il prelievo dalla warehouse.  

## <a name="reviewing-the-white-location-setup"></a>Verifica dell'impostazione dell'ubicazione BIANCA  
L'impostazione della pagina **Scheda Ubicazione** definisce i flussi della warehouse della società.  

### <a name="to-review-the-location-setup"></a>Per rivedere l'impostazione dell'ubicazione  

1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ubicazioni** e quindi scegliere il collegamento correlato.  
2.  Aprire la scheda ubicazione BIANCA.  
3.  Notare che nella Scheda dettaglio **Warehouse** la casella di controllo **Stoccaggi e prelievi guidati** è selezionata.  

    Ciò significa che l'ubicazione è impostata per il livello massimo di complessità, riflesso dal fatto che tutte le caselle di controllo di gestione della warehouse nella Scheda dettaglio sono selezionate.  

4.  Notare che nella Scheda dettaglio **Collocazioni** le collocazioni sono specificate nei campi **Codice collocazione carichi** e **Codice collocazione spedizione**.  

Ciò significa che quando si crea un carico warehouse, il codice collocazione viene copiato nell'intestazione del documento di carico warehouse per impostazione di default e nelle righe degli stoccaggi warehouse risultanti.  

## <a name="creating-the-purchase-orders"></a>Creazione degli ordini di acquisto  
Gli ordini di acquisto sono il tipo più comune di documenti origine in entrata.  

### <a name="to-create-the-purchase-orders"></a>Per creare gli ordini di acquisto  

1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ordini acquisto** e selezionare il collegamento correlato.  
2.  Scegliere l'azione **Nuovo**.  
3.  Creare un ordine di acquisto per il fornitore 10000 alla data di lavoro (23 gennaio) con le righe di ordine di acquisto seguenti.  

    |Articolo|Cod. ubicazione|Quantità|  
    |----------|-------------------|--------------|  
    |70200|BIANCO|100 PZ|  
    |70201|BIANCO|50 PZ|  

    Comunicare alla warehouse che l'ordine di acquisto è pronto per la gestione warehouse al momento della consegna.  

4.  Scegliere l'azione **Rilascia**.  

    Procedere alla creazione del secondo ordine di acquisto.  

5.  Scegliere l'azione **Nuovo**.  
6.  Creare un ordine di acquisto per il fornitore 20000 alla data di lavoro con le righe di ordine di acquisto seguenti.  

    |Articolo|Cod. ubicazione|Quantità|  
    |----------|-------------------|--------------|  
    |70100|BIANCO|10 CAN|  
    |70101|BIANCO|12 CAN|  

    Scegliere l'azione **Rilascia**.  

    Le consegne degli articoli dai fornitori 10000 e 20000 sono arrivate alla warehouse BIANCO e Sammy inizia per elaborare le ricezioni di acquisto.  

## <a name="receiving-the-items"></a>Ricezione degli articoli  
Nella pagina **Carico warehouse** è possibile gestire più ordini in entrata per i documenti di origine, ad esempio un ordine di acquisto.  

### <a name="to-receive-the-items"></a>Per ricevere gli articoli  
1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Carichi warehouse** e quindi scegliere il collegamento correlato.  
2.  Scegliere l'azione **Nuovo**.  
3.  Nel campo **Codice ubicazione** immettere BIANCO:  
4.  Scegliere l'azione **Usa filtri per richiamare doc. orig.**.  
5.  Nel campo **Codice** immettere **ACCESSORIO**.  
6.  Nel campo **Descrizione** immettere **Fornitori 10000 e 20000**.  
7.  Scegliere l'azione **Modifica**.  
8.  Nella Scheda dettaglio **Acquisto**, nel campo **Filtro Acquistare-da Nr. forn.**, immettere **10000&#124;20000**.  
9. Scegliere l'azione **Esegui**. Il carico warehouse viene compilato con quattro righe che rappresentano le righe ordine di acquisto per i fornitori specificati. Il campo **Qtà da ricevere** è compilato in quanto non è stata selezionata la casella di controllo **Non compilare Qtà da gestire** nella pagina **Filtri per ottenere documenti origine**.  
10. In alternativa, se si desidera utilizzare un filtro come descritto in precedenza in questa sezione, scegliere l'azione **Prendi documento origine**, quindi selezionare gli ordini di acquisto dai fornitori in questione.  
11. Scegliere l'azione **Registra carico**, quindi scegliere il pulsante **Sì**.  

    I movimenti contabili articoli positivi vengono creati sulla base delle ricezioni acquisti registrate di accessori da fornitori 10000 e 20000 e gli articoli sono pronti per lo stoccaggio nella warehouse dalla collocazione di carico.  

## <a name="putting-the-items-away"></a>Stoccaggio di articoli  
Nella pagina **Stoccaggio warehouse** è possibile gestire gli stoccaggi per uno specifico documento warehouse di carico che copre più documenti di origine. Come in tutti i documenti di attività di warehouse, ogni articolo nello stoccaggio nella warehouse è rappresentato da una riga Prendere e da una riga Mettere. Nella procedura riportata di seguito, il codice di collocazione nelle righe Prendere è la collocazione di ricevimento di default presso l'ubicazione BIANCA, W-08-0001.  

### <a name="to-put-the-items-away"></a>Per stoccare gli articoli  
1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Stoccaggi** e quindi scegliere il collegamento correlato.  
2.  Selezionare l'unico documento di stoccaggio warehouse nell'elenco e nella scheda **Pagina iniziale**, nel gruppo **Gestisci**, scegliere **Modifica**.  

    Il documento di stoccaggio warehouse verrà visualizzato con un totale di otto righe Prendere o Mettere per le quattro righe ordine di acquisto.

    Al lavoratore warehouse viene detto che il reparto di assemblaggio necessita di 40 cerniere. Inizia così a dividere la singola riga Mettere per specificare una seconda riga Mettere per la collocazione W-02-0001 nel reparto di assemblaggio in cui colloca quella parte di cerniere ricevute.  

3.  Selezionare la seconda riga nella pagina **Stoccaggio warehouse**, la riga Mettere per l'articolo 70200.  
4.  Nel campo **Qtà da gestire** modificare il valore da 100 a 60.  
5.  Nella Scheda dettaglio **Righe** scegliere **Funzioni**, quindi **Dividi riga**. Una nuova riga viene inserita per l'articolo 70200 con 40 nel campo **Qtà da gestire**.  
6.  Nel campo **Codice collocazione** immettere W-02-0001. Il campo **Codice zona** viene compilato automaticamente.  

    Procedere con la registrazione dello stoccaggio.  

7.  Scegliere l'azione **Registra stoccaggio**, quindi scegliere il pulsante **Sì**.  

    Gli accessori ricevuti vengono a questo punto stoccati nelle collocazioni di default degli articoli e 40 cerniere vengono collocate nel reparto di assemblaggio. Gli articoli ricevuti sono ora disponibili per essere prelevati a seconda delle richieste interne, ad esempio gli ordini di assemblaggio, o delle richieste esterne, ad esempio le spedizioni vendite.  

## <a name="see-also"></a>Vedi anche  
 [Eseguire lo stoccaggio con Stoccaggi warehouse:](warehouse-how-to-put-items-away-with-warehouse-put-aways.md)   
 [Spostare articoli in configurazioni di warehouse avanzate](warehouse-how-to-move-items-in-advanced-warehousing.md)   
 [Dettagli di progettazione: Flusso warehouse in entrata](design-details-inbound-warehouse-flow.md)   
 [Procedura dettagliata: ricezione e stoccaggio nelle configurazioni di warehouse di base](walkthrough-receiving-and-putting-away-in-basic-warehousing.md)   
 [Procedure dettagliate per i processi aziendali](walkthrough-business-process-walkthroughs.md)
