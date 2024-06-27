---
title: Spedire articoli
description: Questo articolo descrive come spedire gli articoli dalla warehouse.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 06/10/2024
ms.custom: bap-template
ms.search.form: '7335, 7337, 7339, 7340, 7341, 7362, 9008'
ms.service: dynamics-365-business-central
---

# <a name="ship-items-with-a-warehouse-shipment"></a>Spedire gli articoli con una spedizione warehouse

In [!INCLUDE[prod_short](includes/prod_short.md)], il prelievo e la spedizione degli articoli avvengono utilizzando uno dei quattro metodi, come descritto nella tabella seguente.

|Metodo|Processo in uscita|Richiesto prelievo|Richiesta spedizione|Livello di complessità (ulteriori informazioni in [Panoramica di Warehouse Management](design-details-warehouse-management.md))|  
|------|----------------|-----|---------|-------------------------------------------------------------------------------------|  
|A|Registra il prelievo e la spedizione dalla riga ordine|||Nessuna attività di warehouse dedicata.|  
|B|Registra il prelievo e la spedizione da un documento di prelievo magazzino|Attivato||Di base: ordine per ordine.|  
|C|Registra il prelievo e la spedizione da un documento di spedizione warehouse||Attivato|Di base: registrazione di ricezione e spedizione consolidata per più ordini.|  
|G|Registra il prelievo da un documento di prelievo warehouse e la spedizione da un documento di spedizione warehouse|Attivato|Attivato|Avanzate|  

Per ulteriori informazioni sulla spedizione degli articoli, vai a [Flusso warehouse in uscita](design-details-outbound-warehouse-flow.md).

Questo articolo fa riferimento ai metodi C e D nella tabella. In entrambi i metodi inizi creando un documento di spedizione da un documento di origine aziendale. Selezionare gli articoli specificati per la spedizione.

Quando un'ubicazione richiede spedizioni warehouse, puoi spedire gli articoli in base ai documenti di origine rilasciati al warehouse. Il rilascio dei documenti di origine rende gli articoli pronti per essere movimentati nella warehouse. I seguenti sono esempi di documenti di origine:

* Ordini vendita
* Ordini di reso acquisto
* Ordini di trasferimento
* Ordini assistenza

Puoi creare una spedizione warehouse in uno di due modi:

* In modalità push, quando il lavoro viene svolto ordine per ordine. Scegli l'azione **Crea spedizione warehouse** nel documento di origine per creare una spedizione warehouse per il documento.
* In modalità pull, in cui si utilizza l'azione **Rilascia** nel documento di origine per rilasciarlo alla warehouse. Un dipendente della warehouse crea una **Spedizione warehouse** per uno o più documenti di origine rilasciati. La procedura seguente descrive come creare la spedizione warehouse nella modalità pull.

## <a name="to-ship-items-using-a-warehouse-shipment-document"></a>Per spedire gli articoli usando un documento spedizione warehouse

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Spedizioni warehouse**, quindi scegli il collegamento correlato.  
2. Selezionare **Nuovo**.  
3. Nel campo **Nr.** Scegli la numerazione da utilizzare per creare un ID per la spedizione.  
4. Nel campo **Codice ubicazione**, scegli l'ubicazione da cui effettui la spedizione. 

    Quando si recuperano le righe dei documenti di origine, alcune informazioni dell'ubicazione vengono copiate in ciascuna riga.  
5. Se l'ubicazione richiede collocazioni, compila il campo **Codice collocazione**. A seconda della tua configurazione, [!INCLUDE[prod_short](includes/prod_short.md)]] può aggiungere il codice collocazione automaticamente. Per ulteriori informazioni vedi [Codici zona e collocazione](warehouse-how-ship-items.md#zone-and-bin-codes).  
6. Puoi ottenere il documento di origine in due modi:

    * Scegli l'azione **Prendi documenti origine**. Viene visualizzata la pagina **Documenti origine - In uscita**. Qui è possibile selezionare uno o più documenti di origine rilasciati alla warehouse che richiedono la spedizione.
    * Scegliere l'azione **Usa filtri per richiamare doc. orig.**. Si apre la pagina **Filtri per ottenere documenti di origine**. Puoi selezionare il filtro del documento di origine e applicarlo. Tutte le righe del documento origine rilasciato che soddisfano i criteri di filtro vengono aggiunte alla pagina **Spedizione warehouse**. Per ulteriori informazioni vedi [Procedura: Utilizzare i filtri per ottenere i documenti di origine](warehouse-how-ship-items.md#how-to-use-filters-to-get-source-documents).

    > [!NOTE]
    > Se l'ubicazione prevede cross-docking e collocazioni per ogni riga, è possibile esaminare la quantità di articoli inseriti nelle collocazioni di cross-dock. [!INCLUDE [prod_short](includes/prod_short.md)] calcola le quantità ogni volta che i campi della spedizione vengono aggiornati. Se sono articoli della spedizione che stai preparando, puoi creare un prelievo per tutti gli articoli e completare la spedizione. Ulteriori informazioni in [Sottoporre gli articoli a cross-dock](warehouse-how-to-cross-dock-items.md).

7. Crea un prelievo warehouse. Se l'ubicazione richiede il prelievo, è possibile creare attività di prelievo per le spedizioni warehouse in uno dei due seguenti modi:

    * In modalità push, dove utilizzi l'azione **Crea prelievo**. Seleziona le righe da prelevare e specifica le informazioni sui prelievi. Ad esempio, da quali collocazioni prelevare e inserire e quante unità gestire. Le collocazioni possono essere predefinite per l'ubicazione o la risorsa warehouse.
    * In modalità pull, dove utilizzi l'azione **Rilascia**. Nella pagina **Prospetto prelievi**, usa l'azione **Prendi documenti warehouse** per ottenere i prelievi assegnati. Una volta registrati i prelievi della warehouse, le righe nel **Prospetto prelievi** vengono eliminate. Per ulteriori informazioni vedi [Prelevare articoli per la spedizione warehouse](warehouse-how-to-pick-items-for-warehouse-shipment.md).

    > [!TIP]
    > Per un'ubicazione che non richiede il prelievo, è possibile stampare la spedizione warehouse e utilizzarla come lista prelievo.

8. Specifica la quantità da spedire.  

    Per un'ubicazione che richiede il prelievo, il campo **Qtà. da spedire** viene aggiornato automaticamente quando il prelievo viene registrato. In caso contrario, il campo **Qtà da spedire** viene compilato con la quantità inevasa per ciascuna riga quando viene creata la riga spedizione warehouse.

    Puoi modificare la quantità, ma non puoi spedire più articoli rispetto al numero nel campo **Qtà. in sospeso** nella riga del documento di origine o nel campo **Qtà. prelevata** se è richiesto il prelievo.

    Per impostare il valore nel campo **Qtà da spedire** in tutte le righe su zero, scegli l'azione **Elimina qtà da spedire**. Ad esempio, l'impostazione delle quantità su zero è utile se utilizzi uno scanner di codici a barre per aggiornare le quantità di spedizione. Per aggiungere la quantità disponibile per la spedizione, scegli l'azione **Autocompilazione qtà da spedire**.

9. Registrare la spedizione.

    [!INCLUDE [preview-posting-shipment](includes/preview-posting-shipment.md)]

## <a name="how-to-use-filters-to-get-source-documents"></a>Come utilizzare i filtri per ottenere i documenti di origine

Da una spedizione warehouse, è possibile utilizzare la pagina **Filtri per ottenere documenti origine** per recuperare le righe del documento di origine rilasciato che definiscono quali articoli spedire.

1. Nella spedizione warehouse, scegli l'azione **Usa filtri per richiamare doc. orig.**. 
2. Per impostare un nuovo filtro, immetti un codice descrittivo nel campo **Codice**, quindi scegli l'azione **Modifica**.

    Viene visualizzata la pagina **Scheda filtro documento origine - In uscita**.

3. Utilizza i filtri per definire il tipo di righe del documento di origine da recuperare. Ad esempio, è possibile selezionare i tipi di documenti di origine, come gli ordini di vendita o di trasferimento.
4. Scegli **Esegui**.  

Tutte le righe del documento origine rilasciato che soddisfano i criteri di filtro vengono aggiunte nella pagina **Spedizione warehouse** in cui hai impostato i filtri.

È possibile creare un numero indefinito di combinazioni di filtri. I filtri vengono salvati nella pagina **Filtri per ottenere documenti origine** e sono disponibili in momento successivo. È possibile modificare i criteri in qualsiasi momento scegliendo l'azione **Modifica**.

## <a name="zone-and-bin-codes"></a>Codici zona e collocazione

Se le collocazioni sono obbligatorie nell'ubicazione, [!INCLUDE [prod_short](includes/prod_short.md)] suggerisce una zona e un codice collocazione sul documento di spedizione warehouse.

* Per le configurazioni avanzate in cui un'ubicazione utilizza stoccaggio e prelievo diretti, [!INCLUDE [prod_short](includes/prod_short.md)] usa la collocazione specificata nel campo **Codice collocazione spedizione** nella **Scheda ubicazione**. Se il **Codice collocazione spedizione** non è specificato, il campo è vuoto. Se l'articolo e la collocazione spedizione non corrispondono, [!INCLUDE [prod_short](includes/prod_short.md)] lascia vuota la collocazione spedizione.
* Negli altri casi, [!INCLUDE [prod_short](includes/prod_short.md)] utilizza sempre la collocazione specificata nel campo **Codice collocazione spedizione** nella **Scheda ubicazione**. Se non è specificato un codice collocazione spedizione, [!INCLUDE [prod_short](includes/prod_short.md)] utilizza il codice collocazione del documento di origine.

## <a name="handling-assemble-to-order-items-in-warehouse-shipments"></a>Gestione di articoli da assemblare su ordine in spedizioni warehouse

Negli scenari di assemblaggio su ordine, usa il campo **Qtà da spedire** sulle righe spedizione warehouse per registrare il numero di unità assemblate. La quantità viene registrata come output assemblaggio quando registri la spedizione warehouse. Per altre righe spedizione warehouse, il valore del campo **Qtà da spedire** è uguale a zero.

Quando completano l'assemblaggio delle parti o di tutta la quantità assemblaggio su ordine, i lavoratori registrano la quantità nel campo **Qtà da spedire** sulla riga spedizione warehouse. Quindi scelgono l'azione **Registra spedizione**. L'output dell'assemblaggio viene registrato, incluso il consumo dei componenti. Una spedizione di vendita per la quantità viene registrata per l'ordine di vendita.

Nell'ordine di assemblaggio è possibile scegliere **Riga spediz. whse. assem. su ordine** per accedere alla riga spedizione warehouse.

Dopo che la spedizione warehouse è stata registrata, i vari campi della riga ordine di vendita vengono aggiornati per mostrare lo stato di avanzamento nella warehouse. I seguenti campi vengono inoltre aggiornati per mostrare le quantità rimanente da assemblare su ordine e spedire:

* **Qtà inevasa whse. per assemblaggio su ordine**
* **Qtà inevasa whse. per assemblaggio su ordine (base)**

> [!NOTE]
> Negli scenari di combinazione, in cui una parte della quantità deve essere assemblata e un'altra deve essere spedita dal magazzino, vengono create due righe spedizione warehouse. Una riga corrisponde alla quantità da assemblare su ordine, mentre l'altra corrisponde alla quantità di magazzino.
>
> La quantità assemblaggio su ordine viene gestita come descritto in questo articolo. La quantità di magazzino viene gestita come una normale riga di spedizione warehouse. Per informazioni sugli scenari di combinazione, vedi [Assemblaggio su ordine e assemblaggio per magazzino](assembly-assemble-to-order-or-assemble-to-stock.md).

## <a name="see-also"></a>Vedere anche

[Inventario](inventory-manage-inventory.md)  
[Impostazione Warehouse Management](warehouse-setup-warehouse.md)  
[Gestione assemblaggio](assembly-assemble-items.md)  
[Panoramica di Warehouse Management](design-details-warehouse-management.md)
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
