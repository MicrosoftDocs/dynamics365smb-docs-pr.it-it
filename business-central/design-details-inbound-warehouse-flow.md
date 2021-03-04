---
title: 'Dettagli di progettazione: Flusso warehouse in entrata | Microsoft Docs'
description: Il flusso in entrata in una warehouse inizia quando gli articoli arrivano nella warehouse dell'ubicazione della società, ricevuti dalle origini esterne o da un'altra ubicazione della società. Un impiegato registra gli articoli, in genere eseguendo la scansione di un codice a barre. Dal dock di ricezione, le attività di magazzino vengono eseguite a livelli diversi di complessità per introdurre gli articoli nell'area di immagazzinamento.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 6b86bf4be6a925913e3e2a0a70cf2066e8956681
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/17/2020
ms.locfileid: "4751557"
---
# <a name="design-details-inbound-warehouse-flow"></a>Dettagli di progettazione: Flusso warehouse in entrata
Il flusso in entrata in una warehouse inizia quando gli articoli arrivano nella warehouse dell'ubicazione della società, ricevuti dalle origini esterne o da un'altra ubicazione della società. Un impiegato registra gli articoli, in genere eseguendo la scansione di un codice a barre. Dal dock di ricezione, le attività di magazzino vengono eseguite a livelli diversi di complessità per introdurre gli articoli nell'area di immagazzinamento.  

 Ogni articolo viene identificato e corrisposto a un documento di origine in entrata corrispondente. Sono disponibili i seguenti documenti di origine in entrata:  

- Ordine di acquisto  
- Ordine di trasferimento in ingresso  
- Ord. reso di vendita  

Inoltre, sono presenti i seguenti documenti di origine interni che funzionano come origini in entrata:  

- Ordine di produzione con registrazione dell'output  
- Ordine di assemblaggio con registrazione dell'output  

Gli ultimi due rappresentano i flussi in entrata nella warehouse dalle aree operative interne. Per ulteriori informazioni sulla gestione del magazzino per i processi in entrata e in uscita interni, vedere [Dettagli di progettazione: Flussi warehouse interni](design-details-internal-warehouse-flows.md).  

I processi e i documenti dell'interfaccia utente nei flussi di warehouse in entrata sono diversi nelle configurazioni di base e avanzata della warehouse. La principale differenza consiste nel fatto che le attività sono eseguite ordine per ordine nelle configurazioni di base della warehouse e vengono consolidate per più ordini nelle configurazioni avanzate della warehouse. Per ulteriori informazioni sui diversi livelli di complessità della warehouse, vedere [Dettagli di progettazione: Panoramica warehouse](design-details-warehouse-setup.md).  

In [!INCLUDE[prod_short](includes/prod_short.md)], i processi in entrata per la ricezione e lo stoccaggio possono essere eseguiti in quattro modalità utilizzando diverse funzionalità a seconda del livello di complessità della warehouse.  

|Metodo|Processo in entrata|Collocazioni|Carichi|Stoccaggi|Livello di complessità (vedere [Dettagli di progettazione: Setup warehouse](design-details-warehouse-setup.md))|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Registrare il carico e lo stoccaggio dalla riga ordine|X|||2|  
|B|Registrare il carico e lo stoccaggio da un documento di stoccaggio magazzino|||X|3|  
|C|Registrare il carico e lo stoccaggio da un documento di carico warehouse||X||5/4/6|  
|D|Registrare il carico da un documento di carico warehouse e registrare lo stoccaggio da un documento di stoccaggio warehouse||X|X|5/4/6|  

La selezione di un approccio dipende dalle pratiche accettate della società e dal relativo livello di complessità organizzativa. In un ambiente warehouse ordine per ordine, dove la maggior parte degli addetti della warehouse lavora direttamente con i documenti di ordine, una società potrebbe decidere di utilizzare il metodo A. Una warehouse ordine per ordine con un processo di stoccaggio più complesso o dove del personale dedicato svolge le funzioni di gestione della warehouse, potrebbe decidere di separare le funzioni di stoccaggio dal documento di ordine, metodo B. Inoltre, le società che devono pianificare la gestione di molteplici ordini potrebbero trovare utile utilizzare documenti di carico della warehouse, metodi C e D.  

Nei metodi A, B e C, le azioni di carico e di stoccaggio sono combinate in un unico passaggio quando si registrano i documenti corrispondenti come ricevuti. Nel metodo D, il carico viene registrato per primo per riconoscere l'aumento di magazzino e che gli articoli sono disponibili per la vendita. L'addetto warehouse registra quindi lo stoccaggio per rendere gli articoli disponibili al prelievo.  

## <a name="basic-warehouse-configurations"></a>Configurazioni di base della warehouse  
Nel diagramma seguente vengono illustrati i flussi warehouse in entrata per tipo di documento nelle configurazioni di base della warehouse. I numeri nel diagramma corrispondono ai passaggi indicati nelle sezioni che seguono il grafico.  

![Flusso in entrata nelle configurazioni di base della warehouse](media/design_details_warehouse_management_inbound_basic_flow.png "Flusso in entrata nelle configurazioni di base della warehouse")  

### <a name="1-release-source-document--create-inventory-put-away"></a>1: Rilasciare il documento di origine / Creare stoccaggio di inventario  
Quando gli articoli vengono caricati nella warehouse, l'utente responsabile della ricezione pubblica il documento di origine, ad esempio un ordine di acquisto o di trasferimento in entrata, per segnalare agli addetti alla warehouse che gli articoli caricati possono essere stoccati in magazzino. In alternativa, l'utente crea documenti di stoccaggio magazzino per le singole righe ordine, in modalità push, in base alle collocazioni specificate e le quantità da gestire.  

### <a name="2-create-inbound-request"></a>2: Crea Richiesta in entrata  
Quando il documento di origine in entrata viene rilasciato, viene creata automaticamente una richiesta warehouse in entrata. Contiene riferimenti al numero e al tipo di documento di origine e non è visibile all'utente.  

### <a name="3-create-inventory-put-away"></a>3: Crea un nuovo stoccaggio magazzino  
Nella pagina **Stoccaggio magazzino**, l'addetto alla warehouse recupera, in modalità pull, le righe del documento di origine in attesa in base alle richieste warehouse in entrata. In alternativa, le righe di stoccaggio di magazzino sono già create, in modalità push, dall'utente responsabile del documento di origine.  

### <a name="4-post-inventory-put-away"></a>4: Registra stoccaggio magazzino  
In ogni riga per gli articoli che sono stati stoccati, in parte o completamente, l'addetto alla warehouse compila il campo **Quantità**, quindi registra lo stoccaggio di magazzino. I documenti di origine che sono correlati allo stoccaggio di magazzino vengono registrati come ricevuti.  

Vengono creati i movimenti contabili articoli positivi e i movimenti warehouse e viene eliminata la richiesta di stoccaggio, se completamente gestita. Ad esempio, il campo **Quantità ricevuta** nella riga del documento di origine in entrata viene aggiornato. Viene creato un documento di carico registrato che corrisponde all'ordine di acquisto, ad esempio, e agli articoli ricevuti.  

## <a name="advanced-warehouse-configurations"></a>Configurazioni avanzate della warehouse  
Nel diagramma seguente viene illustrato il flusso warehouse in entrata per tipo di documento nelle configurazioni avanzate della warehouse. I numeri nel diagramma corrispondono ai passaggi indicati nelle sezioni che seguono il grafico.  

![Flusso in entrata nelle configurazioni avanzate della warehouse](media/design_details_warehouse_management_inbound_advanced_flow.png "Flusso in entrata nelle configurazioni avanzate della warehouse")  

### <a name="1-release-source-document"></a>1: Rilasciare documenti di origine  
Quando gli articoli vengono caricati nella warehouse, l'utente responsabile della ricezione pubblica il documento di origine, ad esempio un ordine di acquisto o di trasferimento in entrata, per segnalare agli addetti alla warehouse che gli articoli caricati possono essere stoccati in magazzino.  

### <a name="2-create-inbound-request"></a>2: Crea Richiesta in entrata  
Quando il documento di origine in entrata viene rilasciato, viene creata automaticamente una richiesta warehouse in entrata. Contiene riferimenti al numero e al tipo di documento di origine e non è visibile all'utente.  

### <a name="3-create-warehouse-receipt"></a>3: Creare il carico warehouse  
Nella pagina **Carico warehouse**, l'utente responsabile della ricezione degli articoli recupera le righe del documento di origine in attesa in base alla richiesta warehouse in entrata. Più righe del documento di origine possono essere combinate in un unico documento di carico warehouse.  

L'utente compila il campo **Qtà da gestire** e, se necessario, seleziona la collocazione e l'area ricevimento.  

### <a name="4-post-warehouse-receipt"></a>4: Registra Carico warehouse  
L'utente registra il carico warehouse. Vengono creati movimenti contabili articoli positivi. Ad esempio, il campo **Quantità ricevuta** nella riga del documento di origine in entrata viene aggiornato.  

### <a name="5-create-warehouse-internal-put-away"></a>5: Crea Stoccaggio interno warehouse  
L'utente responsabile dello stoccaggio a partire da operazioni interne crea uno stoccaggio warehouse interno per gli articoli che devono essere stoccati nella warehouse, ad esempio l'output di produzione o di assemblaggio. L'utente specifica la quantità, la zona e la collocazione da cui gli articoli devono essere stoccati, potenzialmente tramite la funzione **Prendi contenuto collocazione**. L'utente rilascia lo stoccaggio interno della warehouse, che crea una richiesta warehouse in entrata in modo che l'attività possa essere recuperata nei documenti di stoccaggio warehouse o nel prospetto di stoccaggio.  

### <a name="6-create-put-away-request"></a>6: Crea Richiesta stoccaggio  
Quando il documento di origine in entrata viene registrato, viene creata automaticamente una richiesta di stoccaggio warehouse. Contiene riferimenti al numero e al tipo di documento di origine e non è visibile all'utente. In base al setup, l'output da un ordine di produzione crea inoltre una richiesta di stoccaggio per stoccare gli articoli finiti in magazzino.  

### <a name="7-generate-put-away-worksheet-lines-optional"></a>7: Generare le righe del prospetto di stoccaggio (facoltativo)  
L'utente responsabile del coordinamento degli stoccaggi recupera le righe di stoccaggio warehouse nel **Prospetto stoccaggi** basato su carichi warehouse registrati o operazioni interne con output. L'utente seleziona le righe da stoccare e prepara gli stoccaggi specificando le collocazioni da cui prelevare, quelle in cui inserire e il numero di unità da gestire. Le collocazioni possono essere definite anticipatamente dall'impostazione dell'ubicazione warehouse o della risorsa operativa.  

Una volta che tutti gli stoccaggi sono pianificati e assegnati agli addetti warehouse, l'utente genera i documenti di stoccaggio warehouse. Le righe degli stoccaggi completamente assegnati vengono eliminate dal **Prospetto stoccaggi**.  

> [!NOTE]  
>  Se il campo **Usa prospetto stoccaggi** non è selezionato nella scheda ubicazione, i documenti di stoccaggio warehouse vengono creati direttamente in base a carichi warehouse registrati. In questo caso, il passaggio 7 è omesso.  

### <a name="8-create-warehouse-put-away-document"></a>8: Creare documento di stoccaggio warehouse  
L'addetto warehouse che esegue gli stoccaggi crea un documento di stoccaggio warehouse in modalità pull, in base al carico warehouse registrato. In alternativa, il documento di stoccaggio magazzino viene creato e assegnato a un lavoratore del magazzino in modalità push.  

### <a name="9-register-warehouse-put-away"></a>9: Registra Stoccaggio warehouse  
In ogni riga per gli articoli che sono stati stoccati, in parte o completamente, l'addetto alla warehouse compila il campo **Quantità** della pagina **Stoccaggio warehouse**, quindi registra lo stoccaggio nella warehouse.  

I movimenti warehouse vengono creati e le righe di stoccaggio warehouse vengono eliminate, se completamente gestite. Il documento di stoccaggio warehouse rimane aperto fino a quando la quantità completa del carico warehouse registrato correlato non viene registrata. Il campo **Qtà stoccata** nelle righe dell'ordine di carico warehouse viene aggiornato.  

## <a name="see-also"></a>Vedere anche  
[Dettagli di progettazione: Gestione warehouse](design-details-warehouse-management.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]