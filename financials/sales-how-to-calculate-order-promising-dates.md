---
title: 'Procedura: Calcolare le date per la promessa ordine | Documenti Microsoft'
description: "La funzione promessa ordine consente di calcolare la prima data utile in cui l'articolo sarà disponibile per la spedizione. Consente inoltre di creare delle righe di richiesta per le date confermate dall'utente."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 01/19/2019
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: b31ba087798c3f54e54403ed418019c82ce3091c
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="calculate-order-promising-dates"></a>Calcolare le date per la promessa ordine
Una società deve essere in grado di comunicare ai rispettivi clienti le date di consegna dell'ordine. La finestra **Righe promessa ordine** consente di effettuare questa operazione da una riga di ordine di vendita.  

Sulla base delle date di disponibilità note e previste di un articolo, [!INCLUDE[d365fin](includes/d365fin_md.md)] calcola immediatamente le date di spedizione e di consegna, che possono quindi essere promesse al cliente.  

Se si specifica una data di consegna richiesta sulla riga dell'ordine di vendita, questa data verrà utilizzata come data di partenza per i calcoli successivi.  

- data di consegna richiesta - durata spedizione = data di spedizione pianificata  
- data di spedizione pianificata - tempo gest. uscita da whse. = data spedizione  

Se gli articoli sono disponibili per il prelievo alla data di spedizione, il processo di vendita può proseguire. Se non esistono articoli disponibili per il prelievo alla data di spedizione, verrà visualizzato un avviso di esaurimento delle scorte.  

Se nella riga dell'ordine di vendita non si specifica una data di consegna richiesta, o se la data richiesta non può essere rispettata, viene calcolata la prima data in cui gli articoli saranno disponibili. Questa data viene quindi immessa nel campo **Data spedizione** della riga e le date in cui si prevede di spedire gli articoli e in cui essi saranno consegnati al cliente vengono calcolate secondo i seguenti calcoli:  

- data spedizione + tempo gest. uscita da whse. = data di spedizione pianificata  
- data di spedizione pianificata + durata spedizione = data di consegna pianificata  

## <a name="about-order-promising"></a>Informazioni sulla promessa ordine
La funzionalità di promessa ordine consente di garantire la spedizione di un ordine in una determinata data. La data per la quale si garantisce la disponibilità dell'articolo e vengono create delle righe d'ordine per quella data che devono essere confermate dall'utente. La funzionalità consente di calcolare la prima data utile in cui l'articolo sarà disponibile per la spedizione. Vengono inoltre create righe di richiesta, nel caso gli articoli debbano essere prima acquistati, per le date confermate dall'utente.

[!INCLUDE[d365fin](includes/d365fin_md.md)] utilizza due concetti fondamentali:  

- ATP (Available-to-Promise)  
- CTP (Capable-to-Promise)  

### <a name="available-to-promise"></a>ATP (Available-to-Promise)  
Con ATP (Available-to-Promise) vengono calcolate le date sulla base del sistema di impegno. Viene eseguito un controllo di disponibilità delle quantità non impegnate in magazzino per quanto riguarda la produzione pianificata, gli acquisti, i trasferimenti e i resi di vendita. Sulla base di queste informazioni, [!INCLUDE[d365fin](includes/d365fin_md.md)] calcola automaticamente la data di consegna dell'ordine del cliente perché gli articoli sono disponibili, in magazzino o nei carichi pianificati.  

### <a name="capable-to-promise"></a>CTP (Capable-to-Promise)  
CTP (Capable-to-Promise) presuppone uno scenario "what if", che si applica solo alle quantità di articoli che non sono in inventario o sugli ordini pianificati. In base a questo scenario, [!INCLUDE[d365fin](includes/d365fin_md.md)] calcola la prima data in cui l'articolo sarà disponibile se deve essere prodotto, acquistato oppure trasferito.

#### <a name="example"></a>Esempio
Se è presente un ordine per 10 pezzi e 6 pezzi sono disponibili in inventario o in ordini programmati, il calcolo CTP (Capable-to-Promise) sarà basato su 4 pezzi.

### <a name="calculations"></a>Calcoli  
Quando in [!INCLUDE[d365fin](includes/d365fin_md.md)] viene calcolata la data di spedizione del cliente, vengono eseguiti due task:  

- Viene calcolata la prima data di consegna utile quando il cliente non ha richiesto una data di consegna specifica.  
- Viene verificato se la data di consegna richiesta dal cliente o promessa al cliente è realistica.  

Se il cliente non richiede una data di consegna specifica, la data di spedizione viene impostata in modo da corrispondere alla data di lavoro e la disponibilità viene quindi basata su tale data. Se l'articolo è in magazzino, in [!INCLUDE[d365fin](includes/d365fin_md.md)] viene calcolato un periodo avanti nel tempo per determinare quando è possibile consegnare l'ordine. Ciò avviene tramite le seguenti formule:  

- Data spedizione + Warehouse in uscita + Spedizione pianificata + Tempo di gestione = Data  
- Data di spedizione pianificata + Durata spedizione = Data di consegna pianificata  

[!INCLUDE[d365fin](includes/d365fin_md.md)] verifica quindi se la data di consegna calcolata è realistica calcolando un periodo indietro nel tempo per determinare quando l'articolo deve essere disponibile per soddisfare la data promessa. Ciò avviene tramite le seguenti formule:  

- Data di consegna pianificata - Durata spedizione = Data di spedizione pianificata  
- Data di spedizione pianificata - Gestione uscita da warehouse = Data spedizione  

La data di spedizione viene utilizzata per eseguire il controllo di disponibilità. Se l'articolo è disponibile in questa data, [!INCLUDE[d365fin](includes/d365fin_md.md)] conferma che la consegna richiesta/promessa può essere soddisfatta impostando la data di consegna pianificata affinché corrisponda alla data di consegna richiesta/promessa. Se l'articolo non è disponibile, restituisce una data vuota e il gestore ordini può quindi utilizzare la funzionalità CTP.  

In base alle nuove date e ore, tutte le date correlate sono calcolate in base alle formule elencate in precedenza in questa sezione. Il calcolo CTP richiede più tempo, ma fornisce una data accurata in cui è prevista la consegna dell'articolo al cliente. Le date che vengono calcolate dalla funzionalità CTP sono contenute nei campi **Data di consegna pianificata** e **Prima data spedizione** nella finestra **Righe promessa ordine**.  

Il gestore ordini completa il processo CTP accettando le date. Ciò significa che vengono create una riga di pianificazione e un movimento di impegno per l'articolo prima delle date calcolate per garantire che l'ordine venga soddisfatto.  

Oltre alle promesse d'ordine esterne che è possibile eseguire nella finestra **Righe promessa ordine**, è possibile promettere date di consegna interne o esterne per gli articoli della distinta base. Per altre informazioni, vedere [Visualizzare la disponibilità di articoli](inventory-how-availability-overview.md).

## <a name="to-set-up-order-promising"></a>Per impostare le promesse ordine  
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Setup promessa ordine**, quindi scegliere il collegamento correlato.  
2. Immettere nel campo **Offset (Tempo)** un numero e un codice dell'unità di tempo. Selezionare uno dei seguenti codici:  

    |Codice|Descrizione|  
    |----------|-----------------|  
    |**d**|Giorno di calendario|  
    |**w**|Settimana|  
    |**m**|Mese|  
    |**q**|Trimestre|  
    |**y**|Anno|  

    L'espressione "3s", ad esempio, indica che il tempo di offset è di tre settimane. Per indicare il periodo corrente, utilizzare il prefisso "c" davanti a ognuno di questi codici. Se, ad esempio, il tempo di offset corrisponde al mese corrente, immettere **cm**.  
3. Inserire un numero di serie nel campo **Nr. promessa ordine** scegliendo una riga dalla lista riportata nella finestra **Nr. Serie**.  
4. Immettere un modello di promessa dell'ordine nel campo **Modello Promessa Ordine** selezionando una riga dall'elenco visualizzato nella finestra  **Lista Mod. Rich. Approvv.**.  
5. Immettere nel campo **Prospetto Promessa Ordine** una richiesta di approvvigionamento selezionando una riga dalla lista contenuta nella finestra **Descr. Ric. Approvvig.**.

### <a name="to-enter-inbound-warehouse-handling-time-in-the-inventory-setup-window"></a>Per immettere il tempo di gestione warehouse nella finestra Setup magazzino  
Se si intende includere il tempo di gestione warehouse nel calcolo della promessa d'ordine nella riga di acquisto, è possibile impostarlo come valore di default per il magazzino e l'ubicazione.    
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Setup magazzino**, quindi scegliere il collegamento correlato.  
2. Nella Scheda dettaglio **Generale**, nel campo **Tempo gest. entrata in whse** inserire il numero di giorni che si intende comprendere nel calcolo promessa d'ordine.  

> [!NOTE]  
>  Se il campo **Tempo gest. entrata in whse** nella **Scheda Ubicazione** è stato compilato per l'ubicazione, il contenuto di questo campo verrà utilizzato come tempo gestione entrata in warehouse di default.  

### <a name="to-enter-inbound-warehouse-handling-time-on-location-cards"></a>Per immettere il tempo di gestione entrata in warehouse nelle schede ubicazione  
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Ubicazioni**, quindi scegliere il collegamento correlato.  
2.  Aprire la scheda ubicazione pertinente.  
3.  Nella Scheda dettaglio **Warehouse**, nel campo **Tempo gest. entrata in whse** inserire il numero di giorni che si intende includere nel calcolo promessa d'ordine.  

> [!NOTE]  
>  Se si lascia vuoto il campo **Tempo gest. entrata in whse.**, il calcolo utilizza il valore nella finestra **Setup magazzino**.

### <a name="to-enter-outbound-warehouse-handling-time-in-the-inventory-setup-window"></a>Per immettere il tempo di gestione warehouse in uscita nella finestra Setup magazzino  
Se si intende impostare l'inclusione del tempo di uscita dalla warehouse nel calcolo della promessa d'ordine nella riga di vendita, è possibile impostarlo come valore di default per l'inventario.

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Setup magazzino**, quindi scegliere il collegamento correlato.  
2. Nella Scheda dettaglio **Generale**, nel campo **Tempo gest. uscita da whse** inserire il numero di giorni che si intende comprendere nel calcolo promessa d'ordine.  

> [!NOTE]  
>  Se il campo **Tempo gest. uscita da whse** nella scheda Ubicazione è stato compilato per l'ubicazione, il contenuto di questo campo verrà utilizzato come tempo gestione uscita da warehouse di default.  

### <a name="to-enter-outbound-warehouse-handling-time-on-location-cards"></a>Per immettere il tempo gestione uscita da warehouse nelle schede ubicazione  
1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Ubicazioni**, quindi scegliere il collegamento correlato.  
2.  Aprire la scheda ubicazione pertinente.  
3.  Nella Scheda dettaglio **Warehouse**, nel campo **Tempo gest. uscita da whse** inserire il numero di giorni che si intende includere nel calcolo promessa ordine.  

> [!NOTE]  
>  Se si lascia vuoto il campo **Tempo gest. uscita da whse.**, il calcolo utilizza il valore nella finestra **Setup magazzino**.

## <a name="to-make-an-item-critical"></a>Per identificare un articolo come critico  
Prima che un articolo possa essere incluso nel calcolo della promessa d'ordine, deve essere contrassegnato come critico. Questa impostazione garantisce che gli articoli non critici non causino calcoli di promesse d'ordine irrilevanti.   
1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Articoli**, quindi scegliere il collegamento correlato.  
2.  Aprire la scheda articolo desiderata.  
3.  Nella Scheda dettaglio **Pianificazione** selezionare il campo **Critico** .  

## <a name="to-calculate-an-order-promising-date"></a>Per calcolare una data per la promessa ordine  
1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Ordine di vendita**, quindi scegliere il collegamento correlato.  
2.  Aprire l'ordine di vendita appropriato e selezionare la riga o le righe da calcolare automaticamente.  
3.  Scegliere l'azione **Promessa ordine** quindi scegliere l'azione **Righe promessa ordine**.  
4.  Selezionare una riga e quindi selezionare una delle seguenti opzioni:  

    - Selezionare **ATP (Available-To-Promise)** per calcolare la prima data possibile in cui l'articolo sarà disponibile tenendo in considerazione le giacenze, i carichi programmati e il fabbisogno lordo.  
    - Selezionare **CTP (Capable-To-Promise)** se l'articolo attualmente è esaurito e se si desidera calcolare la prima data in cui può essere disponibile emettendo delle nuove richieste di rifornimento.  
5.  Selezionare il pulsante **Accetta** per confermare la prima data di spedizione disponibile.  

## <a name="see-also"></a>Vedi anche  
[Vendite](sales-manage-sales.md)  
[Calcolo della data per gli acquisti](purchasing-date-calculation-for-purchases.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

