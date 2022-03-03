---
title: Dettagli di progettazione - Flusso warehouse in uscita
description: In questo argomento viene illustrata la sequenza del flusso di warehouse in uscita dai documenti di origine rilasciati agli articoli pronti per la spedizione.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/15/2021
ms.author: edupont
ms.openlocfilehash: 282c6533d7ac8b769c1ec74c42d4808ebc5da380
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2022
ms.locfileid: "8139705"
---
# <a name="design-details-outbound-warehouse-flow"></a>Dettagli di progettazione: Flusso warehouse in uscita

Il flusso in uscita nella warehouse inizia con una richiesta da documenti di origine rilasciati di prelevare gli articoli dall'ubicazione della warehouse, per spedirli a una parte esterna o un'altra ubicazione della società. Dall'area di immagazzinamento, le attività di magazzino vengono eseguite a livelli diversi di complessità per portare gli articoli fuori dai dock di immagazzinamento.  

 Ogni articolo viene identificato e corrisposto a un documento di origine in entrata corrispondente. Sono disponibili i seguenti documenti di origine in uscita:  

- Ordine di vendita  
- Ordine di trasferimento in uscita  
- Ord. reso di acquisto  
- Ordine assistenza  

Inoltre, sono presenti i seguenti documenti di origine interni che funzionano come origini in uscita:  

- Ordine di produzione con componenti necessari  
- Ordine di assemblaggio con componenti necessari  

 Gli ultimi due documenti rappresentano i flussi in uscita dalla warehouse alle aree operative interne. Per ulteriori informazioni sulla gestione del magazzino per i processi in entrata e in uscita interni, vedere [Dettagli di progettazione: Flussi warehouse interni](design-details-internal-warehouse-flows.md).  

 I processi e i documenti dell'interfaccia utente nei flussi di warehouse in uscita sono diversi nelle configurazioni di base e avanzata della warehouse. La principale differenza consiste nel fatto che le attività sono eseguite ordine per ordine nelle configurazioni di base della warehouse e vengono consolidate per più ordini nelle configurazioni avanzate della warehouse. Per ulteriori informazioni sui diversi livelli di complessità della warehouse, vedere [Dettagli di progettazione: Panoramica warehouse](design-details-warehouse-setup.md).  

 In [!INCLUDE[prod_short](includes/prod_short.md)], i processi in uscita per il prelievo e la spedizione possono essere eseguiti in quattro modalità utilizzando diverse funzionalità a seconda del livello di complessità della warehouse.  

|Metodo|Processo in uscita|Collocazioni|Prelievi|Spedizioni|Livello di complessità (vedere [Dettagli di progettazione: Setup warehouse](design-details-warehouse-setup.md))|  
|------|----------------|----|-----|---------|-------------------------------------------------------------------------------------|  
|A|Registra prelievo e spedizione dalla riga ordine|X|||2|  
|B|Registra prelievo e spedizione da un documento di prelievo magazzino||X||3|  
|C|Registra prelievo e spedizione da un documento di spedizione warehouse|||X|5/4/6|  
|D|Registra il prelievo da un documento di prelievo warehouse e la spedizione da un documento di spedizione warehouse||X|X|5/4/6|  

 La selezione di un approccio dipende dalle pratiche accettate della società e dal relativo livello di complessità organizzativa. In un ambiente di ordine per ordine con processi chiari e una struttura di collocazione semplice, il metodo A, il prelievo e la spedizione dalla riga ordine è appropriato. In altre società ordine per ordine dove gli articoli per una riga ordine potrebbero provenire da più collocazioni o dove gli addetti alla warehouse non possono utilizzare i documenti di ordine, l'utilizzo di documenti di prelievo separati è il metodo appropriato, B. Laddove i processi di prelievo e di spedizione di una società includono la gestione di molteplici ordini e pertanto richiedono un controllo maggiore e una sintesi più precisa, la società potrebbe scegliere di utilizzare un documento di spedizione warehouse e un documento di prelievo warehouse per separare le attività di spedizione e di prelievo, i metodi C e D.  

 Nei metodi A, B e C, le azioni di prelievo e di spedizione sono combinate in un unico passaggio quando si registra il documento corrispondente come spedito. Nel metodo D, il prelievo viene registrato per primo e la spedizione viene registrata in un momento successivo da un documento diverso.  

## <a name="basic-warehouse-configurations"></a>Configurazioni di base della warehouse

 Nel diagramma seguente vengono illustrati i flussi warehouse in uscita per tipo di documento nelle configurazioni di base della warehouse. I numeri nel diagramma corrispondono ai passaggi indicati nelle sezioni che seguono il grafico.  

 ![Flusso in uscita nelle configurazioni di base della warehouse.](media/design_details_warehouse_management_outbound_basic_flow.png "Flusso in uscita nelle configurazioni di base della warehouse")  

### <a name="1-release-source-document--create-inventory-pick-or-movement"></a>1: Rilasciare il documento di origine o creare il prelievo di magazzino o il movimento

 Quando un utente responsabile dei documenti di origine, ad esempio un gestore ordini di vendita o un responsabile della pianificazione della produzione, è pronto per le attività di warehouse in uscita, pubblica il documento di origine in modo da segnalare agli addetti warehouse che gli articoli o i componenti venduti possono essere prelevati e posizionati nelle collocazioni specificate. In alternativa, l'utente crea documenti di movimentazione o di prelievo magazzino per le singole righe ordine, in modalità push, in base alle collocazioni e alle quantità specificate da gestire.  

> [!NOTE]  
> I movimenti di magazzino vengono utilizzati per spostare gli articoli nelle aree operative interne nelle configurazioni di base della warehouse, in base ai documenti di origine o su una base ad hoc.  

### <a name="2-create-outbound-request"></a>2: Crea Richiesta in uscita

 Quando il documento di origine in uscita viene rilasciato, viene creata automaticamente una richiesta warehouse in uscita. Contiene riferimenti al numero e al tipo di documento di origine e non è visibile all'utente.  

### <a name="3-create-inventory-pick-or-movement"></a>3: Creare il prelievo magazzino o il movimento

 Nella pagina **Prelievo magazzino** o **Movimento di magazzino**, l'addetto alla warehouse recupera, in modalità pull, le righe del documento di origine in attesa in base alle richieste warehouse in entrata. In alternativa, le righe di prelievo magazzino sono già create, in modalità push, dall'utente responsabile del documento di origine.  

### <a name="4-post-inventory-pick-or-register-inventory-movement"></a>4: Registrare prelievo di magazzino o Registrare movimento di magazzino

 In ogni riga per gli articoli che sono stati prelevati o spostati, in parte o completamente, l'addetto alla warehouse compila il campo **Quantità**, quindi registra il prelievo o il movimento di magazzino. I documenti di origine correlati al prelievo magazzino vengono registrati come spediti o consumati. I documenti di origine correlati ai movimenti di magazzino non vengono registrati.  

 Per i prelievi di magazzino vengono creati i movimenti contabili articoli negativi e i movimenti warehouse e viene eliminata la richiesta di prelievo, se completamente gestita. Ad esempio, il campo **Quantità spedita** nella riga del documento di origine in entrata viene aggiornato. Viene creato un documento di spedizione registrato che corrisponde all'ordine di vendita, ad esempio, e agli articoli spediti.  

## <a name="advanced-warehouse-configurations"></a>Configurazioni avanzate della warehouse

 Nel diagramma seguente viene illustrato il flusso warehouse in uscita per tipo di documento nelle configurazioni avanzate della warehouse. I numeri nel diagramma corrispondono ai passaggi indicati nelle sezioni che seguono il grafico.  

 ![Flusso in uscita nelle configurazioni avanzate della warehouse.](media/design_details_warehouse_management_outbound_advanced_flow.png "Flusso in uscita nelle configurazioni avanzate della warehouse")  

### <a name="1-release-source-document"></a>1: Rilasciare documenti di origine

 Quando un utente responsabile dei documenti di origine, ad esempio un gestore ordini di vendita o un responsabile della pianificazione della produzione, è pronto per le attività di warehouse in uscita, pubblica il documento di origine in modo da segnalare agli addetti alla warehouse che gli articoli o i componenti venduti possono essere prelevati e posizionati nelle collocazioni specificate.  

### <a name="2-create-outbound-request-2"></a>2: Creare la richiesta in uscita (2)

 Quando il documento di origine in uscita viene rilasciato, viene creata automaticamente una richiesta warehouse in uscita. Contiene riferimenti al numero e al tipo di documento di origine e non è visibile all'utente.  

### <a name="3-create-warehouse-shipment"></a>3: Crea una nuova spedizione warehouse

 Nella pagina **Spedizione warehouse**, il responsabile della spedizione recupera le righe del documento di origine in attesa in base alla richiesta warehouse in uscita. Più righe del documento di origine possono essere combinate in un unico documento di spedizione warehouse.  

### <a name="4-release-shipment--create-warehouse-pick"></a>4: Rilasciare la spedizione o Creare il prelievo warehouse

 Il responsabile della spedizione rilascia la spedizione warehouse, in modo che gli addetti alla warehouse possano creare o coordinare i prelievi warehouse per la spedizione in questione.  

 In alternativa, l'utente crea documenti di prelievo magazzino per le singole righe di spedizione, in modalità push, in base alle collocazioni specificate e le quantità da gestire.  

### <a name="5-release-internal-operation--create-warehouse-pick"></a>5: Rilasciare l'operazione interna o Creare il prelievo warehouse

 L'utente responsabile delle operazioni interne pubblica un documento di origine interno, ad esempio un ordine di produzione e di assemblaggio, in modo che gli addetti warehouse possano creare o coordinare i prelievi warehouse per l'operazione interna in questione.  

 In alternativa, l'utente crea documenti di prelievo magazzino per il singolo ordine di produzione o di assemblaggio, in modalità push, in base alle collocazioni specificate e alle quantità da gestire.  

### <a name="6-create-pick-request"></a>6: Creare richiesta prelievo

 Quando il documento di origine in uscita viene rilasciato, viene creata automaticamente una richiesta di prelievo della warehouse. Contiene riferimenti al numero e al tipo di documento di origine e non è visibile all'utente. In base all'impostazione, il consumo da un ordine di produzione e di assemblaggio crea inoltre una richiesta di prelievo per prelevare i componenti necessari dal magazzino.  

### <a name="7-generate-pick-worksheet-lines"></a>7: Generare le righe del prospetto prelievi

 L'utente responsabile del coordinamento dei prelievi recupera le righe di prelievo warehouse nel **Prospetto prelievi** basato sulle richieste di prelievo da spedizioni warehouse o da operazioni interne con consumo di componenti. L'utente seleziona le righe da prelevare e prepara i prelievi specificando le collocazioni da cui prelevare, quelle in cui inserire e il numero di unità da gestire. Le collocazioni possono essere definite anticipatamente dall'impostazione dell'ubicazione warehouse o della risorsa operativa.  

 L'utente specifica i metodi di prelievo per la gestione ottimizzata della warehouse quindi utilizza una funzione per creare i documenti di prelievo warehouse corrispondenti, che vengono assegnati a differenti addetti warehouse che eseguono i prelievi warehouse. Una volta assegnati i prelievi della warehouse, le righe nel **Prospetto prelievi** vengono eliminate.  

### <a name="8-create-warehouse-pick-documents"></a>8: Creare documenti di prelievo warehouse

 L'addetto warehouse che esegue i prelievi crea un documento di prelievo warehouse, in modalità pull, in base al documento di origine rilasciato. In alternativa, il documento di prelievo magazzino viene creato e assegnato al lavoratore del magazzino in modalità push.  

### <a name="9-register-warehouse-pick"></a>9: Registrare prelievo di warehouse

 In ogni riga per gli articoli che sono stati prelevati, in parte o completamente, l'addetto alla warehouse compila il campo **Quantità** nella pagina **Prospetto prelievi**, quindi registra il prelievo della warehouse.  

 I movimenti warehouse vengono creati e le righe di prelievo warehouse vengono eliminate, se completamente gestite. Il documento di prelievo warehouse rimane aperto fino a quando la quantità completa della spedizione warehouse correlata non viene registrata. Il campo **Qtà prelevata** nelle righe di spedizione warehouse viene aggiornato di conseguenza.  

### <a name="10-post-warehouse-shipment"></a>10: Registrare spedizioni warehouse

 Una volta che tutti gli articoli nel documento di spedizione warehouse sono registrati come prelevati nelle collocazioni di spedizione specificate, il responsabile spedizioni registra la spedizione warehouse. Vengono creati movimenti contabili articoli negativi. Ad esempio, il campo **Quantità spedita** nella riga del documento di origine in entrata viene aggiornato.  

## <a name="see-also"></a>Vedere anche

[Dettagli di progettazione: Gestione warehouse](design-details-warehouse-management.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]