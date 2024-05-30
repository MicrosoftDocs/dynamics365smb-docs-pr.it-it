---
author: brentholtorf
ms.topic: include
ms.date: 04/23/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

Aumenta l'efficienza del tuo warehouse con informazioni accurate e in tempo reale sui fattori che possono influenzare le quantità disponibili. Ad esempio: 

* Livelli di magazzino
* Ubicazioni
* Fasi di lavorazione
* Articoli in quarantena
* Prenotazioni

Puoi accedere a informazioni sulla disponibilità degli articoli dai seguenti documenti di origine:

* Ordini vendita
* Ordini di produzione
* Ordini di assemblaggio
* Commesse

Le informazioni rispettano anche altri fattori che influenzano la disponibilità. Ad esempio, collocazioni dedicate, collocazioni bloccate e articoli non disponibili per il prelievo. Ad esempio, gli articoli potrebbero essere impegnati oppure delle operazioni di stoccaggio o spedizione potrebbero essere in sospeso. La pagina **Riepilogo prelievi** ti consente di esaminare gli articoli che [!INCLUDE [prod_short](prod_short.md)] non ha incluso nei documenti di prelievo e di intraprendere le azioni necessarie.

> [!NOTE]
> Questa funzionalità richiede l'attivazione dell'interruttore **Stoccaggi e prelievi guidati** per le posizioni che utilizzi nel processo di prelievo.

### <a name="set-up-previews"></a>Configurare le anteprime

Per ottenere dettagli su cosa viene prelevato e cosa no, attiva l'interruttore **Mostra riepilogo (stoccaggi e prelievi guidati)** nella pagina di richiesta **Whse.- Origine - Crea documento** o **Whse.- Spediz. - Crea prelievo**.

### <a name="determine-the-quantity-you-can-pick"></a>Determinare la quantità che è possibile prelevare

Nelle righe della pagina **Crea riepilogo prelievi warehouse** il campo **Qtà da gestire (base)** mostra quali e quanti articoli [!INCLUDE [prod_short](prod_short.md)] ha provato a prelevare. Il Dettaglio informazioni **Riepilogo** fornisce maggiori dettagli.

Per semplici analisi, la **Qtà prelevabile** potrebbe fornirti informazioni sufficienti. Il campo mostra quanti articoli sono disponibili. Se la quantità prelevabile è inferiore al previsto, esplora il contenuto della collocazione.

La **Qtà prelevabile** è la quantità massima che [!INCLUDE [prod_short](prod_short.md)] può prendere in considerazione per il prelievo. Questa quantità è composta da articoli in collocazioni prelevabili. La quantità esclude le quantità presenti in collocazioni bloccate o dedicate oppure gli articoli prelevati nei documenti di prelievo warehouse. Se l'articolo che vuoi prelevare richiede la tracciabilità articolo, i numeri di lotto o di serie bloccati archiviati nelle collocazioni prelevabili sono esclusi dalla quantità prelevabile.

Se la quantità prelevabile differisce dalla quantità nelle collocazioni prelevabili, potrebbe esserci un problema. Esplora il contenuto delle collocazioni per trovare collocazioni o quantità bloccate in documenti attivi.

Il campo **Quantità in warehouse** mostra la quantità totale che troverai nel warehouse se effettui un conteggio fisico. Da questo campo puoi eseguire il drill-down dei movimenti contabili di warehouse. Se il campo mostra una quantità inferiore alla quantità nel campo **Quantità in collocazioni prelevabili**, c'è un disallineamento tra le quantità di warehouse e quelle di inventario. In tal caso, utilizza l'azione **Calcola rettifica warehouse** nella pagina **Registrazioni articoli** e quindi crea di nuovo il prelievo warehouse.

L'immagine seguente illustra la quantità massima presa in considerazione per il prelievo.

:::image type="content" source="../media/pickable-qty.png" alt-text="Quantità massima presa in considerazione per il prelievo.":::

**Legenda**

|Lettera  |Descrizione  |
|---------|---------|
|P     |Collocazioni con contenuto di tipo Prelievo         |
|D     |Collocazioni con contenuto di tipo Prelievo contrassegnate come collocazioni dedicate        |
|A     |Collocazioni con contenuto di tipo Prelievo nei documenti attivi (come altro prelievo)       |
|T     |Collocazioni con contenuto di tipo Prelievo con articoli con tracciabilità bloccata         |
|B     |Collocazioni con contenuto di tipo Prelievo con articoli con movimentazione in uscita bloccata         |
|O     |Altre collocazioni         |

### <a name="reservations"></a>Prenotazioni

Se sono presenti impegni per l'articolo da prelevare, il calcolo continua. L'idea è che la domanda impegnata abbia una priorità più alta rispetto a quella non impegnata, il che significa che il prelievo per la domanda non impegnata non dovrebbe impedire il prelievo per la domanda impegnata in seguito.

Per verificare che la quantità possa coprire una domanda, confronta il valore **Qtà prelevabile** nel Dettaglio informazioni **Riepilogo** con il valore del campo **Qtà. da gestire (base)** nelle righe.

Puoi trovare gli impegni nel campo **Qtà totale impegnata in warehouse**. Le quantità impegnate già prelevate e pronte per la spedizione, l'utilizzo o il consumo non influiscono sulla disponibilità. Il campo **Qtà impegnata nei contenitori di prelievo/spedizione** mostra questa quantità.

Il campo **Qtà disponibile escluso il contenitore di spedizione** mostra la quantità disponibile, escluse le quantità per le quali è vero quanto segue:

* Sono già prelevate per le spedizioni.
* Si trovano in numeri di serie o lotti di articoli bloccati.
* Sono in collocazioni bloccate.
* Sono in collocazioni dedicate.

Queste quantità potrebbero essere disponibili, ma è possibile che non tu non sia ancora in grado di prelevarle. Potrebbero trovarsi ancora nelle aree di carico, stoccaggio o controllo qualità. Puoi spostarle nell'area di prelievo elaborando un prospetto di stoccaggio o movimentazione.

La differenza tra la quantità in **Qtà disponibile escluso il contenitore di spedizione** e la quantità impegnata in warehouse è la quantità disponibile per il prelievo senza incidere sullo stock impegnato.

L'immagine seguente illustra l'allocazione della quantità disponibile per la quantità impegnata.

:::image type="content" source="../media/Warehouse_Reservation_Pick.png" alt-text="Quantità massima considerata per il prelievo al momento della prenotazione.":::

**Legenda**

|Lettera  |Descrizione  |
|---------|---------|
|P     |Quantità da prelevare         |
|TR    |Qtà totale impegnata in warehouse.         |
|RS    |Le quantità impegnate già prelevate e pronte per la spedizione, l'utilizzo o il consumo       |
|A     |Qtà disponibile escluso il contenitore di spedizione         |
|B     |Quantità in collocazioni dedicate o bloccate, lotti di articoli bloccati o numeri di serie         |

Sebbene nella warehouse sia disponibile una quantità sufficiente per soddisfare completamente il prelievo, ciò porterà al fatto che la quantità totale impegnata verrà allocata rispetto alle quantità nelle collocazioni dedicate o bloccate, impedendo il prelievo per questa domanda. Poiché la domanda impegnata ha una priorità più alta, [!INCLUDE [prod_short](prod_short.md)] riduce la quantità da prelevare per evitare un impatto negativo, come l'impossibilità di prelevare, sulla domanda impegnata.

### <a name="other-details"></a>Altri dettagli

Se gli articoli richiedono la tracciabilità articolo, puoi anche trovare la quantità in lotti o numeri di serie bloccati, il che comporta le seguenti riduzioni:

* La quantità prelevabile
* La quantità disponibile, esclusa la collocazione spedizione
* La quantità impegnata in warehouse 

Se prelevi lo stesso articolo per più documenti o righe di origine, come nel caso in cui si prelevano numeri di serie, vengono visualizzate anche le informazioni sui prelievi per altre righe poiché riducono la quantità prelevabile.
