---
title: Assemblare articoli
description: Informazioni sui processi di assemblaggio su ordine e assemblaggio per magazzino in Business Central.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 11/23/2022
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
ms.custom: bap-template
---
# <a name="assemble-items"></a>Assemblare articoli

Se nel campo **Sistema di rifornimento** nella scheda articolo è indicato **Assemblaggio**, il metodo predefinito per l'approvvigionamento dell'articolo è l'assemblaggio in base a un assemblaggio BOM e potenzialmente in base a una risorsa specifica. Per ulteriori informazioni, vedi [Utilizzo delle DB assemblaggio](assembly-how-work-assembly-boms.md). Per ulteriori informazioni sull'impostazione di un articolo di assemblaggio, vedi [Assemblaggio su ordine e assemblaggio per magazzino](assembly-assemble-to-order-or-assemble-to-stock.md).

Puoi impostare gli articoli assemblaggio per due processi di assemblaggio.

|Processo  |Descrizione  |
|---------|---------|
|Assemblaggio per magazzino     | Articoli che assembli e immagazzini per vendite future. Ad esempio, i kit per una prossima campagna di vendita. Gli articoli non sono correlati a un ordine di vendita, almeno non ancora. Generalmente, questi articoli non sono personalizzati per le richieste dei clienti.        |
|Assemblaggio su ordine     | Articoli che non vuoi immagazzinare. Ad esempio, perché sono personalizzati in base agli ordini dei clienti o per ridurre il costo delle scorte disponibili. |
  
Questo articolo descrive le impostazioni standard per l'assemblaggio per magazzino. Tuttavia, potrebbero esserci altri modi più adatti alla tua attività. Per ulteriori informazioni, vedi [Vendere gli articoli di magazzino nei flussi assemblaggio su ordine](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md) e [Vedere insieme articoli assemblaggio su ordine e articoli in magazzino](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).

> [!NOTE]  
> I componenti di assemblaggio sono gestiti in modo speciale in configurazioni di warehouse di base. Ulteriori informazioni in [Gestione di articoli da assemblare su ordine con prelievi magazzino](warehouse-how-to-pick-items-with-inventory-picks.md#handling-assemble-to-order-items-with-inventory-picks).

## <a name="to-assemble-an-item-to-stock"></a>Per assemblare un articolo per magazzino

Segui i passaggi di questa procedura per assemblare un articolo per magazzino. Per informazioni sull'assemblaggio su ordine, vai a [Vendere articoli assemblati su ordine](assembly-how-to-sell-items-assembled-to-order.md).

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ordini di assemblaggio**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Nuovo**. Verrà visualizzata la pagina **Nuovo ordine di assemblaggio**.  
3. Compila i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Nel campo **Nr. articolo** seleziona l'articolo di assemblaggio da assemblare. Puoi selezionare articoli impostati per l'assemblaggio e con una distinta base di assemblaggio o articoli senza una distinta base di assemblaggio. Quest'ultima è utile per assemblaggi o scenari non pianificati quando si desidera usare la riclassificazione degli articoli e tenere traccia dei costi.  
5. Nel campo **Quantità** immettere il numero di unità dell'articolo che si desidera assemblare.  

    > [!NOTE]  
    >  Se uno o più componenti non sono disponibili per evadere la quantità alla data di scadenza, si apre la pagina **Disponibilità assemblaggio**. La pagina mostra quanti articoli di assemblaggio possono essere assemblati in base alla disponibilità dei componenti. Per ulteriori informazioni vedi [Visualizzare la disponibilità di articoli](inventory-how-availability-overview.md). Quando si chiude la pagina, l'ordine di assemblaggio viene creato con avvisi di disponibilità nelle righe per i componenti interessati.  

    Le righe contengono il contenuto della distinta base dell'assieme e le quantità specificate.  

    > [!NOTE]  
    >  Se la pagina **Disponibilità assemblaggio** è stata aperta al momento della compilazione della testata dell'ordine di assemblaggio, ogni riga dell'ordine di assemblaggio interessata contiene **Sì** nel campo **Avviso di disponibilità** con un collegamento alle informazioni dettagliate sulla disponibilità. <!--check whether this field help is useful For more information, see Check Availability.--> Puoi risolvere una disponibilità dei componente:

    > * Posticipare la data di inizio.
    > * Sostituzione del componente con un altro articolo.
    > * Selezione di una sostituzione disponibile, se definita.  

6. Nel campo **Quantità da assemblare** immettere il numero di unità dell'articolo di assemblaggio che si desidera registrare come output alla successiva registrazione dell'ordine di assemblaggio. Questa quantità può essere inferiore al valore nel campo **Quantità** per riflettere una registrazione di output parziale.  

    > [!NOTE]  
    >  Per garantire che la registrazione del consumo di componenti corrisponda alla registrazione di output dell'articolo di assemblaggio, i campi relativi alla quantità nelle righe dell'ordine di assemblaggio verranno rettificati automaticamente in base al valore immesso nel campo **Quantità da assemblare**.  
7. Nelle righe ordine di assemblaggio di tipo **Articolo** o **Risorsa**, nel campo **Quantità da consumare** immettere il numero di unità che si desidera registrare come consumate alla successiva registrazione dell'ordine di assemblaggio.
8. Quando si è pronti per registrare parzialmente o completamente, scegliere l'azione **Registra**.  

    > [!NOTE]  
    >  Se gli avvisi sono ancora presenti in una riga ordini di assemblaggio, non puoi registrare l'ordine. Viene visualizzato un messaggio sul componente o sui componenti non presenti in magazzino.  

Una volta effettuata la registrazione, l'articolo di assemblaggio viene registrato come output nel codice ubicazione e nel codice collocazione potenziale definiti nell'ordine di assemblaggio. Per gli ordini di assemblaggio creati manualmente, l'ubicazione può essere copiata dal campo di setup **Ubicazione di default per gli ordini**. Per i flussi di assemblaggio su ordine, il codice ubicazione può essere copiato dalla riga ordine di vendita.  

## <a name="see-also"></a>Vedere anche

[Gestione assemblaggio](assembly-assemble-items.md)  
[Usare le distinte base assemblaggio](assembly-how-work-assembly-boms.md)  
[Inventario](inventory-manage-inventory.md)  
[Panoramica di Warehouse Management](design-details-warehouse-management.md)
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
