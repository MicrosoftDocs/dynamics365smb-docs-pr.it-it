---
title: Come dichiarare operazioni commerciali con clienti e fornitori in paesi inclusi nella blacklist
description: È necessario inviare un report periodico delle transazioni con clienti e fornitori in paesi che il governo italiano ha incluso in una blacklist.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: c68b6cb0668e5d5cb20071ecf4c1cc0cc3fff961
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/29/2019
ms.locfileid: "1241808"
---
# <a name="report-trade-with-customers-and-vendors-in-blacklist-countries-regions"></a>Dichiarare operazioni commerciali con clienti e fornitori in paesi inclusi nella blacklist
È necessario inviare un report periodico delle transazioni con clienti e fornitori in paesi che il governo italiano ha incluso in una blacklist. Il report comunicazioni blacklist deve essere inviato all'agenzia delle entrate italiana per impedire frodi relative all'IVA. Le transazioni che sono incluse nel report comunicazioni blacklist sono:  

- Acquisti di prodotti o servizi  
- Vendite di prodotti o servizi  

Ogni mese o trimestre, è necessario generare un report comunicazioni blacklist per le transazioni con paesi che hanno regimi fiscali privilegiati e inviarlo all'agenzia delle entrate italiana. L'agenzia delle entrate italiana decide quali paesi sono inclusi nella blacklist. È possibile visualizzare o modificare i paesi nella blacklist mediante la pagina **Paesi**. Il report periodico include solo le transazioni con un importo superiore a una determinata soglia. Il calcolo dell'importo di soglia viene applicato al livello del documento. Per ulteriori informazioni, vedere [Agenzia delle entrate italiana](https://go.microsoft.com/fwlink/?LinkId=396483).  

Prima di inviare il report periodico, è necessario impostare [!INCLUDE[d365fin](../../includes/d365fin_md.md)].  

## <a name="to-update-the-relevant-countriesregions"></a>Per aggiornare i paesi rilevanti  

1.  Scegliere l'icona ![Cerca pagina o report](../../media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Paesi**, quindi scegliere il collegamento correlato.  
2.  Scegliere il paese rilevante e selezionare la casella di controllo **In blacklist**.  

    > [!NOTE]  
    >  È possibile che il campo **In blacklist** non sia visualizzato. In tal caso, è necessario aggiungerlo alla visualizzazione.  

3.  Immettere il **Codice paese straniero** per il paese nella blacklist.  

Per una lista dei codici e dei paesi rilevanti, vedere [Agenzia delle entrate italiana](https://go.microsoft.com/fwlink/?LinkID=206524).  

## <a name="to-specify-the-current-threshold-amount"></a>Per specificare l'importo di soglia corrente  

1.  Scegliere l'icona ![Cerca pagina o report](../../media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Cat. reg. business IVA** e scegliere il collegamento correlato.  
2.  Nella pagina **Setup registrazioni IVA**, scegliere l'azione **Importo per comunicazioni blacklist**.  
3.  Nella pagina **Importi per comunicazioni blacklist**, compilare i campi come indicato nella tabella riportata di seguito.  

    |Campo|Description|  
    |------------------------------------|---------------------------------------|  
    |**Nome**|Specifica il nome del modello, **Blacklist**.|  
    |**Description**|Specifica una descrizione del modello, Comunicazione blacklist.|  
    |**ID Form**|Specifica la pagina in cui impostare la lista delle transazioni per le comunicazioni blacklist, **12110**.|  
    |**ID report dichiarazione IVA**|Specifica il report che stampa la lista delle transazioni per le comunicazioni blacklist, **12128**.|  
    |**ID report esportazione statistiche IVA**|Specifica il report che esporta la lista delle transazioni per le comunicazioni blacklist, **12129**.|  

3.  Facoltativo. Selezionare il modello Dichiarazione IVA e quindi scegliere l'azione **Nomi dichiarazione**. È possibile specificare il modello con un nome e una descrizione. In caso contrario, il modello avrà il nome Default quando si accede allo stesso nella pagina **Comunicazione blacklist**.  

## <a name="creating-the-list-of-transactions"></a>Creazione della lista delle transazioni  
In base alle dimensioni e al tipo di società, è necessario generare e inviare un report delle transazioni con i fornitori di paesi nella blacklist ogni mese o trimeste. Un mappatura delle transazioni ai conti [!INCLUDE[d365fin](../../includes/d365fin_md.md)] viene fornita nella procedura riportata di seguito, in base allo Spesometro 2013.  

### <a name="to-set-up-the-template-to-create-the-list-of-blacklist-transactions"></a>Per impostare il modello per creare la lista di transazioni nella blacklist  

1.  Scegliere l'icona ![Cerca pagina o report](../../media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Comunicazione blacklist**, quindi scegliere il collegamento correlato.  
2.  Nel campo **Nome** selezionare il nome della dichiarazione IVA appropriata.  
3.  Compilare le righe con le informazioni pertinenti come indicato nella tabella seguente.  

    |Campo|Description|**Tipo di dati**|  
    |--------------------------------------|---------------------------------------|-------------------|  
    |**Nr. riga**|Specificare un numero di riga. Per abilitare il filtro corretto, si raccomanda di numerare le righe nel modo seguente: 1001...1006 e così via.|Codice|  
    |**Description**|Immettere una descrizione della riga. È possibile immettere fino a un massimo di 50 caratteri.<br /><br /> I tipi di transazioni che è obbligatorio inserire nel report includono le vendite e gli acquisti di prodotti e servizi. Queste transazioni possono essere imponibili, non imponibili o esenti da imposta. Devono essere dichiarate anche le fatture per transazioni non soggette a IVA,<br /><br /> nonché le informazioni per le transazioni nota di accredito.|Testo|  
    |**Tipo**|Specificare il tipo del conto che sarà incluso nel report blacklist, ad esempio, Totale movimenti IVA.|Opzione|  
    |**Transazione paese blacklist**|Selezionare la casella di controllo per includere informazioni dei movimenti IVA relativi a una persona o a un'organizzazione con residenza in un paese incluso nella blacklist. In genere, selezionare la casella di controllo solo quando il tipo di riga è Totale movimenti IVA.<br /><br /> Se la casella di controllo non è selezionata, [!INCLUDE[d365fin](../../includes/d365fin_md.md)] estrae solo gli articoli non inclusi nella blacklist.|Boolean|  
    |**Tipo reg. gen.**|Selezionare un tipo di registrazione. Per il report comunicazioni blacklist, è possibile scegliere qualsiasi opzione, ma in genere si utilizza una delle seguenti opzioni:<br /><br /> Vendita<br /><br /> Acquisto<br /><br /> Se si lascia vuoto il campo, [!INCLUDE[d365fin](../../includes/d365fin_md.md)] restituirà solo le righe della dichiarazione IVA in cui questo campo è vuoto.<br /><br /> Se si sceglie il tipo Totale movimenti IVA, in questo campo è possibile scegliere solo tra Acquisto, Vendita e Liquidazione.|Opzione|  
    |**Assistenza UE**|Specificare se il totale dei movimenti rappresenta vendite di servizi in altri paesi UE.|Boolean|  
    |**Tipo di documento**|Specificare un tipo di documento. È possibile scegliere qualsiasi opzione, ma in genere si utilizza una delle seguenti opzioni:<br /><br /> Fattura<br /><br /> Nota credito<br /><br /> Se si lascia vuoto il campo, [!INCLUDE[d365fin](../../includes/d365fin_md.md)] restituisce tutti i tipi di documenti.|Opzione|  
    |**Riferito a periodo**|Specificare il periodo a cui i documenti sono correlati. Quando si esportano i dati e non è stata specificata una data, l'impostazione in questo campo viene ignorata.<br /><br /> Se si lascia vuoto il campo, [!INCLUDE[d365fin](../../includes/d365fin_md.md)] restituisce i movimenti in cui questo campo è vuoto. Inoltre, restituisce i movimenti senza storno di vendite per il totale movimenti IVA.|Opzione|  
    |**Cat. Reg. Business IVA**|Specificare una categoria di registrazione business IVA. Compilare questo campo quando il tipo di riga è Totale movimenti IVA.<br /><br /> Se si lascia vuoto questo campo, [!INCLUDE[d365fin](../../includes/d365fin_md.md)] restituisce i movimenti con qualsiasi gruppo specificato.|Codice|  
    |**Cat. reg. art./serv. IVA**|Specificare una categoria di registrazione di articoli/servizi IVA. Compilare questo campo quando il tipo di riga è Totale movimenti IVA.<br /><br /> Se si lascia vuoto questo campo, [!INCLUDE[d365fin](../../includes/d365fin_md.md)] restituisce i movimenti con qualsiasi gruppo specificato.|Codice|  
    |**Tipo importo**|Specificare il tipo di importo da dichiarare. Di seguito sono elencate le opzioni disponibili:<br /><br /> Base<br /><br /> Importo<br /><br /> Se si lascia vuoto questo campo, [!INCLUDE[d365fin](../../includes/d365fin_md.md)] non restituisce alcuna informazione.|Opzione|  
    |**Totale Riga**|Specificare le righe da includere nel calcolo del totale. Ad esempio, è possibile immettere 1001...1006 per includere tali righe.|Testo|  
    |**Fattore arrotondamento**|Specificare il fattore di arrotondamento utilizzato per arrotondare gli importi dei movimenti IVA.|Opzione|  
    |**Calcola con**|Specificare se calcolare l'importo con un segno o con quello opposto.|Opzione|  
    |**Stampa**|Specificare se stampare informazioni dalla riga.|Boolean|  
    |**Stampa con**|Specificare se includere il segno dell'importo nella stampa.|Opzione|  
    |**Campo per com. in blacklist**|Specificare il campo a cui mappare il totale IVA nel file da esportare. Le opzioni valide sono quelle definite nello Spesometro 2013: BL003001 – BL008002. **Importante:**  il campo **Com. in blacklist** può contenere solo i nomi dei campi correntemente necessari specificati dallo Spesometro. Se si specifica un altro nome di campo, ad esempio i campi dei conti di [!INCLUDE[d365fin](../../includes/d365fin_md.md)] con lo stesso valore di Campo per com. in blacklist, l'esportazione dei dati sarà la somma di quelle righe. La stampa elencherà ogni riga.|Codice|  
    |**Nuova pagina**|Specificare se si desidera inserire una nuova pagina dopo la riga quando si stampano le informazioni.|Boolean|  

Il report stampato include tutte le transazioni che soddisfano i requisiti di soglia. Non include le transazioni che non soddisfano quei requisiti.  

### <a name="to-create-and-print-the-list-of-transactions"></a>Per creare e stampare la lista delle transazioni  

1.  Scegliere l'icona ![Cerca pagina o report](../../media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Comunicazione blacklist**, quindi scegliere il collegamento correlato.  
2.  Nel campo **Nome** selezionare il nome della dichiarazione IVA appropriata.  
3.  Immettere le informazioni appropriate nelle righe. Vedere la procedura per l'impostazione del modello di blacklist.  
4.  Scegliere l'azione **Stampa**.  
5.  Nella Scheda dettaglio **Righe dichiarazione IVA**, impostare eventualmente i filtri appropriati.  
6.  Nella Scheda dettaglio **Opzioni** compilare i campi come descritto nella tabella riportata di seguito.  

    |Campo|Description|  
    |---------------------------------|---------------------------------------|  
    |**Data Inizio**|Facoltativo. Immettere la data di inizio per il report blacklist, che è basata sulla data in cui le operazioni sono state eseguite.|  
    |**Data Fine**|Immettere la data di fine per il report blacklist.|  
    |**Includi movimenti IVA**|Specificare se la lista delle transazioni deve contenere i movimenti IVA aperti o chiusi o entrambi.|  
    |**Includi movimenti IVA**|Specificare se la lista delle transazioni deve contenere i movimenti IVA nel periodo IVA specificato oppure anche quelli dei periodi precedenti.|  
    |**Periodo IVA**|Immettere il periodo di tempo che definisce il periodo IVA per il report blacklist.|  
    |**Tipo Origine**|Facoltativo. Immettere il tipo di origine delle transazioni nella blacklist. Le opzioni includono **Cliente** e **Fornitore**. Se non si effettua alcuna selezione, sono incluse entrambe le categorie.|  
    |**Nr. Origine**|Se si sceglie **Tipo Origine**, immettere il numero di identificazione della transazione di origine. Se non si immettono dati, vengono inclusi tutti i clienti o fornitori.|  
    |**Nome**|Sola lettura. Specifica il nome dell'organizzazione.|  

7.  Scegliere il pulsante **Stampa** per stampare il report oppure scegliere il pulsante **Anteprima** per visualizzare i risultati.  

    > [!NOTE]  
    >  Il report stampato include tutte le transazioni che soddisfano i requisiti di soglia. Non include le transazioni che non soddisfano quei requisiti.  

### <a name="to-preview-and-export-the-list-of-transactions"></a>Per visualizzare un'anteprima della lista delle transazioni e esportarla  

1.  Scegliere l'icona ![Cerca pagina o report](../../media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Comunicazione blacklist**, quindi scegliere il collegamento correlato.  
2.  Nel campo **Nome** selezionare il nome della dichiarazione IVA appropriata.  
3.  Immettere le informazioni appropriate nelle righe. Vedere la procedura per l'impostazione del modello di blacklist.  
4.  Nella scheda **Naviga**, scegliere l'azione **Anteprima**. È possibile esaminare le informazioni per assicurarsi che le mappature abbiano fornito quelle previste.
5. Scegliere il pulsante **OK** per chiudere la pagina.  
6.  Scegliere l'azione **Esporta**.  
7.  Nella Scheda dettaglio **Righe dichiarazione IVA**, impostare eventualmente i filtri appropriati.  
8.  Nella Scheda dettaglio **Opzioni** compilare i campi come descritto nella tabella riportata di seguito.  

    |Campo|Description|  
    |---------------------------------|---------------------------------------|  
    |**Data Inizio**|Immettere la data di inizio per il report blacklist.|  
    |**Data Fine**|Immettere la data di fine per il report blacklist.|  
    |**Includi movimenti IVA**|Specificare se la lista delle transazioni deve contenere i movimenti IVA aperti o chiusi o entrambi.|  
    |**Includi movimenti IVA**|Specificare se la lista delle transazioni deve contenere i movimenti IVA nel periodo IVA specificato oppure anche quelli dei periodi precedenti.|  
    |**Periodo IVA**|Immettere il periodo di tempo che definisce il periodo IVA per il report blacklist.|  
    |**Tipo di comunicazione**|Immettere il tipo di comunicazione per l'esportazione della blacklist. Le opzioni includono <blank>, **Correttiva** e **Annullamento**.<br /><br /> Se si immette **Correttiva**, un report completo viene generato per il periodo specificato, ma è possibile scegliere di sovrascrivere un report inviato in precedenza.<br /><br /> Se si immette **Annullamento**, è necessario immettere i valori del report creato in precedenza e verrà generato un nuovo report.<br /><br /> Le informazioni sull'azione di annullamento o correttiva vengono immesse nel gruppo **Dati sostitutivi**. Compilare i campi seguenti, utilizzando le informazioni fornite dall'agenzia delle entrate italiana (IVA) quando il report blacklist è stato inviato per la prima volta:<br /><br /> -   **Nr. report sostituzione**<br />-   **Nr. documento sostituzione**|  
    |**Tipo periodo**|Specificare se il report ha cadenza mensile o trimestrale.|  

8.  Scegliere il pulsante **OK**.  

    > [!NOTE]  
    >  Il file esportato include le transazioni che sono superiori all'importo di soglia corrente.  

È ora possibile inviare la lista delle transazioni all'agenzia delle entrate italiana. Se si hanno più di 1500 record, verranno esportati più file.  

## <a name="see-also"></a>Vedi anche  
 [IVA italiana](italian-vat.md)
