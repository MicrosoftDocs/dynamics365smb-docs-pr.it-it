---
title: Ottenere una panoramica della disponibilità
description: 'Informazioni su come visualizzare la disponibilità di articoli o scorte tra le ubicazioni, per eventi di vendita o di acquisto, in base a un periodo di tempo e altro.'
documentationcenter: ''
author: brentholtorf
ms.topic: overview
ms.devlang: al
ms.search.keywords: stock
ms.search.form: '908, 909, 925, 926, 504, 501, 500, 499, 99000896, 342, 515, 5417, 5415, 5871, 5530, 492, 157, 5540, 5416, 5414, 1872, 1873, 99000902, 353, 491, 9231, 5390'
ms.date: 04/08/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Visualizzare la disponibilità di articoli

Dal contesto di un task di business, è possibile ottenere informazioni avanzate relative al momento e all'ubicazione in cui un articolo è disponibile, ad esempio quando si parla con un cliente per proporre una data di consegna.

È possibile visualizzare la disponibilità di tutti gli articoli per ubicazione ed è possibile visualizzare la disponibilità di ciascun articolo per evento o periodo. Per evento si intende qualsiasi transazione articolo pianificata, ad esempio una spedizione o un carico di trasferimento in entrata.

> [!NOTE]  
>   Le visualizzazioni di disponibilità per ubicazione richiedono che si disponga di un magazzino presso più di un'ubicazione. Per ulteriori informazioni, vedere [Impostare le ubicazioni](inventory-how-setup-locations.md).

Se si utilizza la funzionalità di gestione warehouse, la disponibilità varia in base alle allocazioni a livello di collocazione quando si verificano le attività di warehouse ad esempio i prelievi e i movimenti e quando il sistema di impegno magazzino impone limitazioni da soddisfare. Un algoritmo piuttosto complesso verifica che tutte le condizioni siano soddisfatte prima di assegnare le quantità ai prelievi per i flussi in uscita. Per ulteriori informazioni, vedi [Dettagli di progettazione: Disponibilità nella warehouse](design-details-availability-in-the-warehouse.md).

In [!INCLUDE[prod_short](includes/prod_short.md)], i dati relativi alla disponibilità vengono in genere visualizzati in due campi diversi, ognuno con una diversa definizione:

* Il campo **Giacenza**, in alcuni casi denominato **Inventario**, mostra l'effettiva quantità in base ai movimenti contabili articoli registrati.
* Nel campo **Disponibilità calcolata** viene calcolato e viene visualizzata la giacenza più i carichi programmati e meno il fabbisogno lordo. (In [!INCLUDE[prod_short](includes/prod_short.md)], i carichi programmati includono le quantità degli ordini di acquisto e degli ordini di trasferimento in entrata. Il fabbisogno lordo include le quantità degli ordini di vendita e degli ordini di trasferimento in uscita.)

> [!TIP]  
>   La disponibilità calcolata è particolarmente importante per visualizzare le pagine **Disponibilità art. per periodi** e **Disponibilità articolo per evento** poiché contengono le dimensioni per data.  

> [!NOTE]  
>   Di seguito viene descritto come visualizzare le informazioni avanzate sulla disponibilità per articolo dall'elenco articoli e dalla scheda articolo. È inoltre possibile accedere alle informazioni contenute nelle righe dei documenti di vendita, per l'articolo nella riga. Per ulteriori informazioni, vedere [Vendere prodotti](sales-how-sell-products.md).

## Per visualizzare la disponibilità di un articolo secondo quando verrà ricevuto o spedito

Si visualizza la disponibilità di un articolo secondo le transazioni pianificate dell'articolo nella pagina **Disponibilità articolo per evento**.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Articoli**, quindi scegli il collegamento correlato.
2. Apri la scheda di un articolo per cui vuoi visualizzare la disponibilità.
3. Scegliere l'azione **Disponibilità articolo per** quindi scegliere l'azione **Evento**.

    La pagina **Disponibilità articolo per evento** mostra come le quantità di magazzino dell'articolo si svilupperanno nel tempo in base agli eventi programmati per carico e spedizione. La pagina fornisce una visualizzazione ridotta che mostra una riga di informazioni accumulate per intervallo di tempo in cui le quantità di magazzino cambiano. Gli intervalli di tempo in cui non si è verificato alcun evento non sono visualizzati. È possibile espandere ogni riga per mostrare i dettagli sull'evento o gli eventi che hanno generato la quantità accumulata sulla riga.
4. Selezionare il valore nel campo **Disponibilità calcolata** per visualizzare i movimenti articoli o documenti aperti che compongono il valore.

## Per visualizzare la disponibilità di un articolo in diversi periodi di tempo

È possibile visualizzare la disponibilità di un articolo nel tempo per periodi specificati nella pagina **Disponibilità art. per periodi**.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Articoli**, quindi scegli il collegamento correlato.
2. Apri la scheda di un articolo per cui vuoi visualizzare la disponibilità.
3. Scegliere l'azione **Disponibilità articolo per** quindi scegliere l'azione **Periodo**.

    La pagina **Disponibilità articolo per periodo** mostra come le quantità di magazzino dell'articolo si svilupperanno nel tempo in base al periodo selezionato, ad esempio giorno, settimana oppure trimestre.
4. Selezionare il valore nel campo **Disponibilità calcolata** per visualizzare i movimenti articoli o documenti aperti che compongono il valore.

## Per visualizzare la disponibilità di un articolo nelle ubicazioni dove è immagazzinato

È possibile visualizzare la disponibilità di un articolo presso i luoghi diversi dove viene immagazzinato nella pagina **Disp. art. per ubicazione**.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Articoli**, quindi scegli il collegamento correlato.
2. Apri la scheda di un articolo per cui vuoi visualizzare la disponibilità.
3. Scegliere l'azione **Disponibilità articolo per** quindi scegliere l'azione **Ubicazione**.

    La pagina **Disponibilità articolo per ubicazione** mostra come le quantità di magazzino dell'articolo si svilupperanno nel futuro in ogni ubicazione in cui è immagazzinato.
4. Selezionare il valore nel campo **Giacenza disponibile** per visualizzare i movimenti articoli che compongono il valore.
5. Selezionare il valore nel campo **Disponibilità calcolata** per visualizzare i movimenti articoli o documenti aperti che compongono il valore.

## Per visualizzare la disponibilità di tutti gli articoli in base all'ubicazione in cui sono immagazzinati

È possibile visualizzare la disponibilità di tutti gli articoli in tutte le ubicazioni nella pagina **Articoli per ubicazione**.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Articoli**, quindi scegli il collegamento correlato.
2. Scegliere l'azione **Articoli per ubicazione**.

    La pagina **Articoli per ubicazione** mostra per tutti gli articoli le quantità disponibili in ogni ubicazione.
3. Selezionare il valore nel campo **Giacenza disponibile** per visualizzare i movimenti articoli che compongono il valore.

## Per visualizzare la disponibilità di un articolo in base al relativo utilizzo nelle DB di assemblaggio o di produzione

Se un articolo è parte delle DB di assemblaggio o di produzione, come articolo principale o come componente, è possibile visualizzare il numero di unità che sono necessarie nella pagina **Disponibilità articolo per livello DB**. Nella pagina viene visualizzato il numero delle unità di un articolo padre che è possibile effettuare in base alla disponibilità di articoli figlio nelle righe sottostanti. Ogni articolo che ha una DB di assemblaggio o di produzione è visibile nella pagina come riga comprimibile. È possibile espandere la riga per visualizzare i componenti sottostanti i sottoassemblaggi di livello inferiore con le proprie DB.

Ad esempio, è possibile utilizzare la pagina per stabilire se è possibile soddisfare un ordine di vendita per un articolo nella data stabilita osservando la disponibilità corrente e le quantità che possono essere fornite dai componenti. È inoltre possibile utilizzare la pagina per identificare i colli di bottiglia nelle DB correlate.

In ogni riga della pagina per gli articoli padre e gli articoli figlio, i seguenti campi chiave specificano le cifre sulla disponibilità. È possibile utilizzare tali cifre per promettere il numero di unità di un articolo padre che è possibile fornire se si inizia il processo assemblaggio correlato.

|Campo|Descrizione|
|------|-----------|
|**Produzione possibile - Padre**|Mostra quante unità di un sottoassemblaggio nell'articolo principale è possibile preparare. Questo campo specifica quante unità dell'articolo padre immediate possono essere assemblate. Il valore è basato sulla disponibilità dell'articolo nella riga.|
|**Produzione possibile - Articolo principale**|Mostra quante unità dell'articolo principale è possibile preparare. Questo campo specifica quante unità dell'articolo DB nella prima riga possono essere assemblate. Il valore è basato sulla disponibilità dell'articolo nella riga.|

### Per visualizzare la disponibilità di un articolo in base alla domanda per il relativo articolo principale

Nella pagina **Disponibilità articolo per livello DB** vengono visualizzate le informazioni relative all'articolo sulla scheda o la riga del documento per il quale viene aperta la pagina. L'articolo viene indicato sempre nella prima riga. È possibile visualizzare informazioni per altri articoli o per tutti gli articoli modificando il valore nel campo **Filtro articolo**.

> [!NOTE]  
>   Per default, le cifre sulla disponibilità nelle righe mostrano la disponibilità totale di tutti gli articoli sotto l'articolo principale. Le cifre vengono visualizzate nel campo **Quantità disponibile** e lo stato attivo è sull'articolo principale. Tuttavia, le informazioni relative al numero di sottoassemblaggi che è possibile preparare potrebbero essere distorte. Per ottenere un'indicazione vera di quanti dei sottoassemblaggi mostrati è possibile preparare, è necessario cancellare il campo **Mostra disponibilità totale**, quindi visualizzare la cifra nel campo **Produzione possibile - Padre**.

Il campo **Collo di bottiglia** specifica quale articolo nella struttura di DB limita la possibilità di produrre una quantità maggiore di quella indicata nel campo **Produzione possibile - Articolo principale**. Ad esempio, l'articolo collo di bottiglia può essere un componente acquistato con una data di carico prevista troppo in ritardo per creare unità aggiuntive dell'articolo principale entro la data presente nel campo **Disponibile entro**.

## Per visualizzare la disponibilità di un articolo in base alle unità di misura

La pagina **Disponibilità articolo per unità di misura** mostra la disponibilità di un articolo nelle unità di misura in cui è memorizzata.

> [!NOTE]  
> Per mantenere accurate queste informazioni, è necessario convertire le unità di misura degli articoli. Ad esempio, se si acquista un articolo in un'unità di misura, ad esempio scatole, e si vendono articoli in un'altra unità di misura, ad esempio pezzi, è necessario utilizzare una registrazione magazzino per convertire le unità di misura o articoli "da disimballare". È possibile utilizzare una riga di registrazione magazzino con rettifica negativa per ridurre il livello di magazzino nell'unità di misura di acquisto, ad esempio scatole, e una rettifica positiva per aumentare il livello di magazzino nell'unità di misura di vendita, ad esempio pezzi. 

## Per visualizzare la disponibilità di un articolo in base alle varianti

La pagina **Disponibilità articolo per variante** mostra la disponibilità effettiva e prevista di un articolo raggruppato in base al codice variante.

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Articoli** e scegli il collegamento correlato.
2. Apri la scheda di un articolo per cui vuoi visualizzare la disponibilità.
3. Scegli l'azione **Disponibilità articolo per** quindi scegli l'azione **Variante**.

    La pagina **Disponibilità articolo per variante** mostra la disponibilità per ogni variante esistente per l'articolo. La pagina è vuota se non esistono varianti per l'articolo.

4. Nel campo **Visualizza per** seleziona la lunghezza del periodo desiderato.
5. Visualizza le cifre sulla disponibilità nei diversi campi quantità per ogni riga.

[!INCLUDE [inventory_variant-availability](includes/inventory_variant-availability.md)]

## Pagina Disponibilità assemblaggio

Nella pagina **Disponibilità assemblaggio** sono visualizzate le informazioni dettagliate sulla disponibilità per l'articolo di assemblaggio. La finestra viene aperta:

- Automaticamente da una riga ordine di vendita in scenari di assemblaggio su ordine quando si immette una quantità che provoca un problema di disponibilità dei componenti.
- Automaticamente da una testata ordine di assemblaggio quando si immette un valore nel campo Quantità che provoca un problema di disponibilità dei componenti.
- Manualmente quando la si apre da un ordine di assemblaggio. Nel gruppo Funzioni della scheda Azioni seleziona Mostra disponibilità.

Nella Scheda dettaglio **Dettagli** sono visualizzate le informazioni dettagliate sulla disponibilità per l'articolo di assemblaggio, inclusa la quantità dell'ordine di assemblaggio che è possibile assemblare entro la data di scadenza in base alla disponibilità dei componenti necessari. Sono visualizzate nel campo In grado di assemblare nella Scheda Dettaglio Dettagli.

Il valore nel campo **In grado di assemblare** viene visualizzato con un carattere rosso se la quantità è inferiore alla quantità nel campo **Quantità residua**, per indicare che non sono disponibili componenti sufficienti per assemblare la quantità completa.

Nella Scheda dettaglio **Righe** vengono visualizzate le informazioni dettagliate sulla disponibilità per i componenti di assemblaggio.

Se uno o più componenti di assemblaggio non sono disponibili, queste informazioni vengono riflesse nel campo **In grado di assemblare** nella riga in questione come quantità minore della quantità nel campo **Quantità residua** nella Scheda Dettaglio **Dettagli**.

## Vedere anche

[Gestire i costi del magazzino](inventory-manage-inventory.md)  
[Gestione assemblaggio](assembly-assemble-items.md)  
[Utilizzare le distinte base](inventory-how-work-BOMs.md)  
[Utilizzare le distinte base assemblaggio](assembly-how-work-assembly-boms.md)  
[Creare le distinte base di produzione](production-how-to-create-production-boms.md)  
[Impostare le ubicazioni](inventory-how-setup-locations.md)  
[Trasferire il magazzino tra le ubicazioni](inventory-how-transfer-between-locations.md)  
[Vendere prodotti](sales-how-sell-products.md)  
[Funzionalità aziendali generali](ui-across-business-areas.md)  
[Utilizzare Business Central](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
