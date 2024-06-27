---
title: Usare le distinte base assemblaggio
description: Crei una distinta base di assemblaggio per specificare i componenti richiesti per un l'articolo che la distinta rappresenta.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'assembly bom, bills of material,'
ms.search.form: '36, 5870, 5872, 5874'
ms.date: 06/13/2024
ms.service: dynamics-365-business-central
---
# Usare le distinte base assemblaggio

Utilizza le distinte base (DB) di assemblaggio per strutturare gli articoli padre che devono essere assemblati dai componenti con poco o nessun uso di risorse. Una DB di assemblaggio può essere utilizzata, ad esempio, per vendere un articolo padre come kit comprendente articoli componenti.

Utilizza gli ordini di assemblaggio per creare articoli finiti da componenti in un processo che può essere svolto da una o più risorse di base, che non sono centri di lavoro o aree di produzione, né privi di risorse. Ad esempio, un processo di assemblaggio potrebbe consistere nel prelevare due bottiglie di vino e un pacchetto di caffè e di imballarli come articolo da regalo.  

Una DB di assemblaggio contiene i dati master che definiscono gli articoli componenti che costituiscono un articolo finale assemblato e le risorse che vengono utilizzate per assemblare l'articolo di assemblaggio. Quando inserisci un articolo di assemblaggio e una quantità in un ordine di assemblaggio, le righe dell'ordine di assemblaggio vengono compilate in base alla distinta base di assemblaggio. L'ordine dispone di una riga di ordine di assemblaggio per componente o risorsa. Per ulteriori informazioni, vedi [Gestione assemblaggio](assembly-assemble-items.md).

[!INCLUDE[prod_short](includes/prod_short.md)] supporta anche le DB di produzione. Le distinte base di produzione differiscono da quelle di assemblaggio in quanto implicano procedure più complesse, come l'utilizzo di risorse, ciclo di produzione e aree di produzione o centri di lavoro. Per ulteriori informazioni sulle differenze vedi [Utilizzare le distinte base](inventory-how-work-BOMs.md) e [Creare le distinte base di produzione](production-how-to-create-production-boms.md).

## Per creare una DB di assemblaggio

Per definire un articolo composto da altri articoli e potenzialmente da risorse che assemblano l'articolo, devi creare una distinta base di assemblaggio.  

Le DB di assemblaggio possono essere multilivello, cioè un componente della DB di assemblaggio può essere un articolo di assemblaggio esso stesso. In tal caso, il campo **DB assemblaggio** nella riga della DB di assemblaggio contiene il valore **Sì**.

Requisiti speciali si applicano agli articoli nelle DB di assemblaggio in relazione alla disponibilità. Per ulteriori informazioni, vedi [Per visualizzare la disponibilità di un articolo per l'utilizzo in DB di assemblaggio](inventory-how-availability-overview.md#to-view-the-availability-of-an-item-by-its-use-in-assembly-or-production-boms).

Esistono due passaggi per creare una DB di assemblaggio:

- Impostazione di un nuovo articolo.
- Definizione della struttura della distinta base dell'articolo di assemblaggio.

1. Impostare un nuovo articolo. Ulteriori informazioni in [Registrare nuovi articoli](inventory-how-register-new-items.md).

   Continuare a inserire componenti o risorse nella distinta base di assemblaggio.  
2. Nella pagina **Scheda articolo** per un articolo di assemblaggio, scegli l'azione **Assembla** quindi l'azione **DB assemblaggio**.
3. Nella pagina **DB assemblaggio** compilare i campi secondo le proprie necessità. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Gli articolo di assemblaggio possono avere varianti, come qualsiasi altro articolo, che ti aiutano a mantenere contenuto l'elenco dei prodotti disponibili. Per ulteriori informazioni sulla funzionalità, vedi [Gestire le varianti di prodotto](inventory-item-variants.md).

## Per modificare le DB di assemblaggio

È possibile modificare le righe di una distinta base di assemblaggio in qualsiasi momento. Tuttavia, la distinta base potrebbe essere utilizzata dalle vendite in corso o dagli assemblaggi dell'articolo padre. La modifica della distinta base potrebbe influire su tali attività. Scegli l'azione **Dove-usato** per esplorare gli articoli che la utilizzano e se gli ordini di vendita o di assemblaggio possono essere interessati.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") , inserisci **Elemento** e scegli il link relativo.
2. Scegliere il valore **Sì** nella colonna **DB assemblaggio**.
3. Nella pagina **DB assemblaggio**, scegli l'azione **Modifica elenco**, quindi modifica i campi secondo necessità.

## Per visualizzare i componenti e le risorse con indentazione in base alla struttura DB

Nella pagina **DB assemblaggio**, è possibile aprire una pagina distinta in cui vengono visualizzati i componenti e tutte le risorse indentate in base alla posizione nella distinta base dell'articolo di assemblaggio.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") , inserisci **Elemento** e scegli il link relativo.
2. Aprire la scheda per l'articolo di assemblaggio. (Il campo **DB assemblaggio** nella pagina **Articoli** contiene il valore **Sì**.)
3. Nella pagina **Scheda articolo** scegli l'azione **Assembla** quindi l'azione **DB assemblaggio**.
4. Nella pagina **DB assemblaggio** selezionare l'azione **Mostra DB**.

## Per sostituire l'articolo di assemblaggio con i suoi componenti nelle righe del documento

Da un documento di vendita e di acquisto contenente un articolo di assemblaggio è possibile utilizzare un'azione speciale per sostituire la riga per l'articolo di assemblaggio con nuove righe per i componenti. Questa azione è utile, ad esempio, se si intende vendere i componenti come kit che rappresenta l'articolo di assemblaggio.

L'azione **Esplodi DB** è anche disponibile nella pagina **DB assemblaggio** come metodo per visualizzare gli articoli di sottoassemblaggi in una DB di assemblaggio.

> [!CAUTION]  
> Una volta utilizzata l'azione **Esplodi DB**, non è possibile annullarla facilmente. È necessario eliminare le righe di ordine di vendita per i componenti e registrare nuovamente una riga ordine di vendita per l'articolo di assemblaggio.

La seguente procedura è basata su fattura di vendita. La stessa procedura si applica ad altri documenti di vendita e a tutti i documenti di acquisto.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Fatture vendite**, quindi seleziona il collegamento correlato.
2. Aprire una fattura di vendita che contiene una riga per un articolo di assemblaggio.
3. Scegli la riga per un articolo di assemblaggio quindi l'azione riga **Esplodi DB**.

Tutti i campi nella riga della fattura di vendita per l'articolo di assemblaggio vengono cancellati ad eccezione dei campi **Descrizione** e **Articolo**. Le righe intere della fattura di vendita vengono immesse per i componenti e le risorse possibili che costituiscono l'articolo di assemblaggio.

> [!NOTE]
> Il report **Lista prelievo per ordine** viene inoltre modificato per mostrare solo i componenti. Ciò significa che un lavoratore warehouse che preleva l'articolo principale, l'articolo di assemblaggio non lo vedrà nella lista prelievo. Per ulteriori informazioni, vedi [Stampare la lista prelievo](sales-how-print-picking-list.md).

## Per calcolare il costo standard di un articolo di assemblaggio

Si calcola il costo unitario di un articolo di assemblaggio eseguendo il ricalcolo del costo unitario di ciascun componente e risorsa nella DB di assemblaggio dell'articolo.

È inoltre possibile calcolare e aggiornare il costo standard di un o più articoli nella pagina **Prospetto costo standard**. Per ulteriori informazioni, vedi [Aggiornare i costi standard](finance-how-to-update-standard-costs.md).  

Il costo unitario di una DB di assemblaggio è sempre uguale al totale dei costi unitari dei suoi componenti, comprese le DB di assemblaggio ed eventuali risorse.  

> [!NOTE]
> [!INCLUDE [bom-standard-cost](includes/bom-standard-cost.md)]

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") , inserisci **Elemento** e scegli il link relativo.
2. Aprire la scheda per l'articolo di assemblaggio. (Il campo **DB assemblaggio** nella pagina **Articoli** contiene il valore **Sì**.)
3. Nella pagina **Scheda articolo** scegli l'azione **DB assemblaggio**.
4. Nella pagina **DB assemblaggio**, selezionare l'azione **Calc. costo standard**.
5. Seleziona una delle seguenti opzioni e scegli il pulsante **OK**.

|Opzione |Descrizione |
|-------|------------|
|**Livello principale**|Calcola il costo standard dell'articolo di assemblaggio come costo totale di tutti gli articoli acquistati o assemblati in tale DB di assemblaggio indipendentemente dalle DB di assemblaggio sottostanti.|
|**Tutti i Livelli**|Calcola il costo standard dell'articolo dell'assemblaggio come somma di:</br></br>* Costo calcolato di tutte le distinte base di assemblaggio sottostanti nella distinta base di assemblaggio.</br>* Il costo di tutti gli articoli acquistati nella distinta base di assemblaggio.|

I costi degli articoli che compongono la DB di assemblaggio vengono copiate dalle schede articoli componenti. Il costo di ogni articolo viene moltiplicato per la quantità e il costo totale viene mostrato nel campo **Costo unitario** nella scheda articolo.

## Vedere anche

[Registrare nuovi articoli](inventory-how-register-new-items.md)  
[Gestire le varianti di prodotto](inventory-item-variants.md)  
[Visualizzare la disponibilità di articoli](inventory-how-availability-overview.md)  
[Magazzino](inventory-manage-inventory.md)  
[Utilizzare le distinte base](inventory-how-work-BOMs.md)  
[Creare le distinte base di produzione](production-how-to-create-production-boms.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
