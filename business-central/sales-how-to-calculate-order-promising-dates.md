---
title: Calcolare le date per la promessa ordine
description: La funzione promessa ordine consente di calcolare la prima data utile in cui l'articolo sarà disponibile per la spedizione.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/29/2021
ms.author: bholtorf
---
# <a name="calculate-order-promising-dates"></a>Calcolare le date per la promessa ordine

Una società deve essere in grado di comunicare ai rispettivi clienti le date di consegna dell'ordine. La pagina **Righe promessa ordine** consente di effettuare questa operazione dall'ordine di vendita.  

[!INCLUDE[prod_short](includes/prod_short.md)] calcola le date di disponibilità di spedizione e di consegna sulla base delle date di disponibilità note e previste di un articolo, che possono quindi essere promesse ai clienti.  

Se si specifica una data di consegna richiesta sulla riga dell'ordine di vendita, questa data verrà utilizzata come data di partenza per i calcoli successivi.  

- data di consegna richiesta - durata spedizione = data di spedizione pianificata  
- data di spedizione pianificata - tempo gest. uscita da whse. = data spedizione  

Se gli articoli sono disponibili per il prelievo alla data di spedizione, il processo di vendita può proseguire. Se non esistono articoli disponibili per il prelievo alla data di spedizione, verrà visualizzato un avviso di esaurimento delle scorte.  

Se nella riga dell'ordine di vendita non si specifica una data di consegna richiesta, o se la data richiesta non può essere rispettata, viene calcolata la prima data in cui gli articoli saranno disponibili. Questa data viene quindi immessa nel campo **Data spedizione** della riga e le date in cui si prevede di spedire gli articoli e in cui essi saranno consegnati al cliente vengono calcolate secondo i seguenti calcoli:  

- data spedizione + tempo gest. uscita da whse. = data di spedizione pianificata  
- data di spedizione pianificata + durata spedizione = data di consegna pianificata  

## <a name="about-order-promising"></a>Informazioni sulla promessa ordine

La funzionalità di promessa ordine consente di garantire la spedizione di un ordine in una determinata data. La data per la quale si garantisce la disponibilità dell'articolo e vengono create delle righe d'ordine per quella data che devono essere confermate dall'utente. La funzionalità consente di calcolare la prima data utile in cui l'articolo sarà disponibile per la spedizione. Vengono inoltre create righe di richiesta, nel caso gli articoli debbano essere prima acquistati o prodotti, per le date confermate dall'utente.

[!INCLUDE[prod_short](includes/prod_short.md)] utilizza due concetti fondamentali:  

- ATP (Available-to-Promise)  
- CTP (Capable-to-Promise)  

### <a name="available-to-promise"></a>ATP (Available-to-Promise)

Con ATP (Available-to-Promise) vengono calcolate le date sulla base del sistema di impegno. Viene eseguito un controllo di disponibilità delle quantità non impegnate in magazzino per quanto riguarda la produzione pianificata, gli acquisti, i trasferimenti e i resi di vendita. Sulla base di queste informazioni, [!INCLUDE[prod_short](includes/prod_short.md)] calcola la data di consegna dell'ordine del cliente perché gli articoli sono disponibili in magazzino o nei carichi pianificati.  

### <a name="capable-to-promise"></a>CTP (Capable-to-Promise)

CTP (Capable-to-Promise) presuppone uno scenario "what if", che si applica solo alle quantità di articoli che non sono in inventario o sugli ordini pianificati. In base a questo scenario, [!INCLUDE[prod_short](includes/prod_short.md)] calcola la prima data in cui l'articolo sarà disponibile se deve essere prodotto, acquistato oppure trasferito.

#### <a name="example"></a>Esempio

Se è presente un ordine per 10 pezzi e 6 pezzi sono disponibili in inventario o in ordini programmati, il calcolo CTP (Capable-to-Promise) sarà basato su 4 pezzi.

### <a name="calculations"></a>Calcoli

Quando in [!INCLUDE[prod_short](includes/prod_short.md)] viene calcolata la data di spedizione del cliente, vengono eseguiti due task:  

- Viene calcolata la prima data di consegna utile quando il cliente non ha richiesto una data di consegna specifica.  
- Viene verificato se la data di consegna richiesta dal cliente o promessa al cliente è realistica.  

Se il cliente non richiede una data di consegna specifica, la data di spedizione viene impostata in modo da corrispondere alla data di lavoro e la disponibilità viene quindi basata su tale data. Se l'articolo è in magazzino, in [!INCLUDE[prod_short](includes/prod_short.md)] viene calcolato un periodo avanti nel tempo per determinare quando è possibile consegnare l'ordine. Ciò avviene tramite le seguenti formule:  

- Data di spedizione pianificata + Tempo di uscita dalla warehouse = Data di spedizione pianificata  
- Data di Spedizione Pianificata + Tempo Spedizione = Data di Consegna Pianificata  

[!INCLUDE[prod_short](includes/prod_short.md)] verifica quindi se la data di consegna calcolata è realistica calcolando un periodo indietro nel tempo per determinare quando l'articolo deve essere disponibile per soddisfare la data promessa. Ciò avviene tramite le seguenti formule:  

- Data di consegna pianificata - Durata spedizione = Data di spedizione pianificata  
- Data di spedizione pianificata - Gestione uscita da warehouse = Data spedizione  

La data di spedizione viene utilizzata per eseguire il controllo di disponibilità. Se l'articolo è disponibile in questa data, [!INCLUDE[prod_short](includes/prod_short.md)] conferma che la consegna richiesta/promessa può essere soddisfatta impostando la data di consegna pianificata affinché corrisponda alla data di consegna richiesta/promessa. Se l'articolo non è disponibile, restituisce una data vuota e il gestore ordini può quindi utilizzare la funzionalità CTP.  

In base alle nuove date e ore, tutte le date correlate sono calcolate in base alle formule elencate in precedenza in questa sezione. Il calcolo CTP richiede più tempo, ma fornisce una data accurata in cui è prevista la consegna dell'articolo al cliente. Le date che vengono calcolate dalla funzionalità CTP sono contenute nei campi **Data di consegna pianificata** e **Prima data spedizione** nella pagina **Righe promessa ordine**.  

Il gestore ordini completa il processo CTP accettando le date. Ciò significa che vengono create una riga di pianificazione e un movimento di impegno per l'articolo prima delle date calcolate per garantire che l'ordine venga soddisfatto.  

Oltre alle promesse d'ordine esterne che è possibile eseguire nella pagina **Righe promessa ordine**, è possibile promettere date di consegna interne o esterne per gli articoli della distinta base. Per altre informazioni, vedere [Visualizzare la disponibilità di articoli](inventory-how-availability-overview.md).

## <a name="to-set-up-order-promising"></a>Per impostare le promesse ordine

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup promessa ordine**, quindi scegli il collegamento correlato.  
2. Immettere nel campo **Offset (Tempo)** un numero e un codice dell'unità di tempo. Selezionare uno dei seguenti codici:  

    |Codice|Descrizione|  
    |----------|-----------------|  
    |**d**|Giorno di calendario|  
    |**w**|Settimana|  
    |**m**|Mese|  
    |**q**|Trimestre|  
    |**y**|Anno|  

    L'espressione "3s", ad esempio, indica che il tempo di offset è di tre settimane. Per indicare il periodo corrente, utilizzare il prefisso "c" davanti a ognuno di questi codici. Se, ad esempio, il tempo di offset corrisponde al mese corrente, immettere **cm**.  
3. Inserire un numero di serie nel campo **Nr. promessa ordine** scegliendo una riga dalla lista riportata nella pagina **Nr. Serie**.  
4. Immettere un modello di promessa dell'ordine nel campo **Modello Promessa Ordine** selezionando una riga dall'elenco visualizzato nella pagina **Lista Mod. Rich. Approvv.**.  
5. Immettere nel campo **Prospetto Promessa Ordine** una richiesta di approvvigionamento selezionando una riga dalla lista contenuta nella pagina **Descr. Ric. Approvvig.**.

### <a name="inbound-and-outbound-warehouse-handling-times-in-order-promising"></a>Tempo di gestione della warehouse in entrata e in uscita nella promessa ordine

Se desideri includere il tempo di gestione della warehouse nel calcolo della promessa ordine nella riga di acquisto, nella pagina **Setup magazzino** è possibile specificare un tempo di gestione predefinito da utilizzare nei documenti di vendita e acquisto. Puoi anche inserire orari specifici per ciascuna delle tue ubicazioni nella pagina **Scheda ubicazione**. 

#### <a name="to-enter-default-inbound-and-outbound-warehouse-handling-times-for-sales-and-purchase-documents"></a>Per immettere il tempo di gestione della warehouse in entrata e in uscita predefinito per i documenti di vendita e acquisto

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Setup magazzino**, quindi scegli il collegamento correlato.  
2. Nella Scheda dettaglio **Generale** nei campi **Tempo gest. entrata in whse.** e **Tempo gest. uscita da whse.** finserire il numero di giorni che vuoi includere nei calcoli della promessa ordine.  

#### <a name="to-enter-inbound-and-outbound-warehouse-handling-times-on-locations"></a>Per immettere i tempi di gestione warehouse in entrata e in uscita nelle ubicazioni

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ubicazione**, quindi scegli il collegamento correlato.  
2.  Aprire la scheda ubicazione pertinente.  
3.  Nella Scheda dettaglio **Warehouse** nei campi **Tempo gest. entrata in whse.** e **Tempo gest. uscita da whse.** finserire il numero di giorni che vuoi includere nei calcoli della promessa ordine.  

> [!NOTE]  
>  Quando crei un ordine di acquisto, se scegli **Ubicazione** nel campo **Spedire a** della scheda dettaglio **Spedizione e pagamento**, e quindi scegli un'ubicazione nel campo **Codice ubicazione** campo, i campi **Tempo gest. uscita da whse.** e **Tempo gest. entrata in whse.** utilizzeranno il tempo di gestione specificato per l'ubicazione. Per gli ordini cliente, lo stesso vale se scegli un'ubicazione nel campo **Codice ubicazione**. Se non viene specificato alcun tempo di gestione per l'ubicazione, i campi **Tempo gest. uscita da whse.** e **Tempo gest. entrata in whse.** saranno vuoti. Se lasci vuoto il campo **Codice ubicazione** nei documenti di vendita e acquisto, il calcolo utilizza il tempo di gestione specificato nella pagina **Setup magazzino**.

## <a name="to-make-an-item-critical"></a>Per identificare un articolo come critico

Prima che un articolo possa essere incluso nel calcolo della promessa d'ordine, deve essere contrassegnato come critico. Questa impostazione garantisce che gli articoli non critici non causino calcoli di promesse d'ordine irrilevanti.   
1.  Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Articoli**, quindi scegli il collegamento correlato.  
2.  Aprire la scheda articolo desiderata.  
3.  Nella Scheda dettaglio **Pianificazione** selezionare il campo **Critico** .  

## <a name="to-calculate-an-order-promising-date"></a>Per calcolare una data per la promessa ordine

1.  Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ordine vendita**, quindi seleziona il collegamento correlato.  
2.  Aprire l'ordine di vendita appropriato e selezionare la riga o le righe da calcolare automaticamente.  
3.  Scegliere l'azione **Promessa ordine** quindi scegliere l'azione **Righe promessa ordine**.  
4.  Selezionare una riga e quindi selezionare una delle seguenti opzioni:  

    - Selezionare **ATP (Available-To-Promise)** per calcolare la prima data possibile in cui l'articolo sarà disponibile tenendo in considerazione le giacenze, i carichi programmati e il fabbisogno lordo.  
    - Selezionare **CTP (Capable-To-Promise)** se l'articolo attualmente è esaurito e se si desidera calcolare la prima data in cui può essere disponibile emettendo delle nuove richieste di rifornimento.  
5.  Selezionare il pulsante **Accetta** per confermare la prima data di spedizione disponibile.  

## <a name="see-also"></a>Vedere anche

[Vendite](sales-manage-sales.md)  
[Calcolo della data per gli acquisti](purchasing-date-calculation-for-purchases.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
