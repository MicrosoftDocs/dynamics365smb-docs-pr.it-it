---
title: 'Impostare la tracciabilità articolo con numeri di serie, di lotto e di collo'
description: 'Configura la tracciabilità di articoli con numeri di serie, di lotto e di pacco'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/06/2024
ms.service: dynamics-365-business-central
---
# <a name="set-up-item-tracking-with-serial-lot-and-package-numbers"></a>Impostare la tracciabilità articolo con numeri di serie, di lotto e di collo

Tieni traccia degli articoli di magazzino anche in configurazioni di magazzino complesse con numeri specifici per ogni articolo, sia come singolo oggetto, come lotto o come pacchetto. Con la tracciabilità degli articoli, è possibile tracciare gli articoli nei movimenti del magazzino interno e nei documenti in uscita e in entrata.

Gli articoli con numeri seriali e di lotto che possono essere analizzati sia in avanti che indietro nella catena di catena di approvvigionamento. Ciò risulta utile per un controllo della qualità generale e per la restituzione dei prodotti. Per ulteriori informazioni, vedere [Analizzare articoli tracciati](inventory-how-to-trace-item-tracked-items.md).  

## <a name="numbers-and-item-tracking"></a>Numeri e tracciabilità degli articoli

Come parte dei processi di magazzino, puoi raggruppare le scorte in pacchi, scatole, contenitori e così via. Ma per tenere traccia degli articoli, assegni numeri univoci come identificazione. Ad esempio, produci e vendi una sedia con il numero articolo *1.900-S*. Ogni singola sedia ha un numero di serie, *1.001*, ma raccogli anche quattro sedie in un lotto, *LOT0001* e spedisci le sedie in un contenitore con il numero del pacco *CONTENITORE010* che include anche altri elementi, come *LOT0100* con tavolini e *LOTTO200* con lampade.  

A seconda della configurazione, utilizzi questi numeri diversi per tenere traccia del magazzino in [!INCLUDE [prod_short](includes/prod_short.md)] nelle varie fasi di acquisto, vendita, operazioni di magazzino e così via.

## <a name="to-set-up-item-tracking-codes"></a>Per impostare i codici di tracciabilità articolo

Un codice di tracciabilità articolo riflette i diversi criteri che una società può seguire nell'uso dei numeri seriali e di lotto degli articoli spostati all'interno di un magazzino.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Codici tracciabilità articolo**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Nuovo**.
3. Compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Sul **Numero di serie**, **Numero di lotto** e **Numero pacchetto** Definire i criteri di tracciabilità degli articoli rispettivamente in base al numero seriale, di lotto e di pacchetto.  

> [!NOTE]  
> Per tenere traccia degli articoli specifici o i lotti specifici durante il ciclo di vita, scegliere i campi **Tracciabilità NS specifico**, **Tracciab. lotto specifico** e **Tracciabilità specifica del collo** rispettivamente. Di conseguenza nella gestione di un'unità in uscita di un articolo con il codice di tracciabilità articolo, è necessario specificare sempre quale numero seriale esistente o numero di lotto esistente gestire. Ciò significa che, durante la vendita di un'unità dell'articolo, è necessario collegare tale unità a uno specifico gruppo di numeri seriali o numero di lotto in magazzino. In altri termini, è necessario che un numero seriale, di lotto o di collo assegnato a un articolo durante l'inserimento in magazzino resti sempre collegato a quel tipo di articolo anche al di fuori del magazzino.

Poiché questi campi di setup coprono tutte le possibili transazioni con l'articolo, i singoli campi In entrata/In uscita vengono selezionati. Tuttavia, i singoli campi in entrata/uscita non hanno nulla a che fare con l'applicazione nell'inventario. Questi definiscono soprattutto il flusso aziendale della società relativo all'assegnazione dei numeri di tracciabilità articolo.  

> [!NOTE]  
> Per assegnare i numeri di tracciabilità articolo nelle attività di warehouse, i campi **Tracciab. NS in warehouse** e **Tracciab. lotto in warehouse** devono essere selezionate nella scheda del codice di tracciabilità articolo.  

## <a name="to-set-up-expiration-rules-for-serial-or-lot-numbers"></a>Per impostare le regole di scadenza per i numeri seriali e di lotto

Per alcuni articoli potrebbe essere necessario impostare date e regole di scadenza specifiche nel codice di tracciabilità articolo. Questa funzionalità consente di tenere traccia della scadenza di determinati numeri seriali e di lotto.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Codici tracciabilità articolo**, quindi scegli il collegamento correlato.
2. Selezionare un codice di tracciabilità articolo esistente quindi scegliere l'azione **Modifica**.  
3. Nella Scheda dettaglio **Varie** selezionare i seguenti campi:  

    |Campo|Descrizione|  
    |---------------------------------|---------------------------------------|  
    |**Registrazione scadenza vincolante**|Specifica che una data di scadenza assegnata al numero di tracciabilità articolo al momento dell'inserimento in magazzino deve essere rispettata all'uscita dal magazzino.|  
    |**Richiedi inserimento data di scadenza**|Specifica che è necessario immettere una data di scadenza nella riga di tracciabilità articolo.|  
    |**Usa date di scadenza**|Specifica che si intendono calcolare date di scadenza. |  

## <a name="to-set-up-warranties-for-serial-or-lot-numbers"></a>Per impostare le garanzie per i numeri seriali o di lotto

Per alcuni articoli potrebbe essere necessario impostare garanzie specifiche nel codice di tracciabilità articolo. Questa funzionalità consente di tenere traccia della scadenza delle garanzie per determinati numeri seriali o di lotto presenti in magazzino.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Codici tracciabilità articolo**, quindi scegli il collegamento correlato.  
2. Selezionare un codice di tracciabilità articolo esistente quindi scegliere l'azione **Modifica**.  
3. Nella Scheda dettaglio **Varie** compilare il campo **Formula data garanzia** e selezionare i campi come indicato di seguito:  

    |Campo|Descrizione|  
    |---------------------------------|---------------------------------------|  
    |**Formula data garanzia**|Specifica l'ultimo giorno di garanzia per l'articolo.|  
    |**Richiedi inserimento data garanzia**|Specifica che è necessario immettere manualmente una data di garanzia nella riga di tracciabilità articolo.|  

## <a name="to-set-up-items-for-tracking-with-the-correct-item-tracking-codes"></a>Per impostare gli articoli per la tracciabilità con i codici di tracciabilità articolo corretti

Per abilitare la tracciabilità degli articoli devi prima assegnare i codici di tracciabilità articolo a un articolo. Esistono due modi per aggiungere codici di tracciabilità articolo: selezionando il codice in un elenco predefinito o assegnando un nuovo codice univoco. Passa con il mouse sui campi per visualizzare una breve descrizione.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Articolo**, quindi scegli il collegamento correlato.
2. Seleziona un articolo esistente nell'elenco e apri la pagina **Scheda articolo**.  
3. Nella Scheda dettaglio **Tracciabilità articolo**, assegna i codici di tracciabilità articolo appropriati e specifica dei valori nei campi **Codice tracciabilità articolo**, **Nr. seriali** e **Nr. lotti**.
    1. In alternativa puoi anche creare un nuovo codice di tracciabilità articolo selezionando l'azione **Nuovo**.

## <a name="to-specify-opening-balances-for-the-items-you-track"></a>Per specificare i saldi di apertura per gli articoli di cui si tiene traccia

Puoi creare saldi iniziali per gli articoli che monitori. Poiché puoi scegliere diverse configurazioni di magazzino, ci sono due opzioni:

* Abilita batch specifici nella pagina **Reg. Magazzino** per consentire alle persone di inserire i dati di serie, lotto e confezione direttamente nelle righe del giornale di registrazione.
* Per i luoghi in cui l'interruttore **Stoccaggi e prelievi guidati** è attivato, utilizza la pagina **Giornale inventario fisico magazzino** per rendere disponibili tutti i campi di tracciabilità dell'articolo. I campi disponibili includono i campi **Data garanzia** e **Data di scadenza**.

### <a name="item-journals"></a>Registrazioni articoli

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registrazioni articoli**, quindi scegli il collegamento correlato.
2. Scegli il campo **Nome** per aprire un elenco di batch registrazioni magazzino.
3. Scegli **Nuovo** per creare un nuovo batch, quindi attiva l'interruttore **Righe tracciabilità articolo**.
4. Scegli **OK** per selezionare il batch creato.
5. Compila i campi nella riga di registrazione magazzino in base alle esigenze. Nota che i campi **Lotto n.**, **Numero di serie**, **Data di scadenza**, **Data garanzia** e **N. pacchetto** sono disponibili (se la funzione è abilitata).
6. Scegli l'azione **Registra** per regolare il magazzino.

> [!NOTE] 
> [!INCLUDE [prod_short](includes/prod_short.md)] esegue alcune convalide minori quando si immettono o si importano dati. Un controllo più completo si verifica quando si registrano o si trasferiscono dati dalle righe del giornale di registrazione alla pagina **Codici tracciabilità articolo**. Quest'ultimo avviene automaticamente quando si apre la pagina **Tracciabilità articolo** dalla riga del registro magazzino o se si sceglie l'azione **Aggiorna righe tracciabilità articolo**.

### <a name="warehouse-physical-inventory-journal-for-locations-where-directed-pick-and-put-away-is-turned-on"></a>Registrazione dell'inventario fisico warehouse nelle ubicazioni che prevedono l'uso di prelievi e stoccaggi guidati

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registrazione dell'inventario fisico warehouse**, quindi scegli il collegamento correlato.
2. Compila i campi nella riga di registrazione magazzino in base alle esigenze. Nota che i campi **Lotto n.**, **Numero di serie**, **Data di scadenza**, **Data garanzia** e **N. pacchetto** sono disponibili (se la funzione è abilitata).
3. Scegli l'azione **Registra** per procedere con le rettifiche di magazzino. Ricordati che per sincronizzare i movimenti warehouse rettificati con i movimenti contabili articoli correlati. Per saperne di più, vai a [Sincronizzare i movimenti warehouse rettificati](/dynamics365/business-central/inventory-how-count-adjust-reclassify#to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries).

Per le importazioni in blocco, utilizzare i pacchetti di configurazione per importare i dati nei giornali.

> [!NOTE]
> Non puoi utilizzare **Modifica in Excel** per creare righe di registrazione con informazioni di tracciabilità.

## <a name="see-also"></a>Vedere anche

[Utilizzare i numeri di serie e di lotto](inventory-how-work-item-tracking.md)  
[Tracciare gli articoli tracciati](inventory-how-to-trace-item-tracked-items.md)  
[Magazzino](inventory-manage-inventory.md)  
[Dettagli di progettazione: Tracciabilità articolo](design-details-item-tracking.md)  
[Dettagli di progettazione: Tracciabilità articolo e impegni](design-details-item-tracking-and-reservations.md)  
[Prenotare articoli](inventory-how-to-reserve-items.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
