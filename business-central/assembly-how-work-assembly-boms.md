---
title: Utilizzare le distinte base di assemblaggio
description: Crei una distinta base di assemblaggio per specificare i componenti richiesti per un l'articolo che la distinta rappresenta.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'assembly bom, bills of material,'
ms.search.form: '36, 5870, 5872, 5874'
ms.date: 09/26/2022
ms.author: edupont
---
# <a name="work-with-assembly-boms" />Utilizzare le distinte base di assemblaggio

Utilizza le distinte base (DB) di assemblaggio per strutturare gli articoli padre che devono essere assemblati dai componenti con poco o nessun uso di risorse. Una DB di assemblaggio può essere utilizzata, ad esempio, per vendere un articolo padre come kit comprendente articoli componenti.

Utilizzare gli ordini di assemblaggio per la creazione di articoli finali dai componenti in un semplice processo che può essere svolto da una o più risorse di base, che non sono centri di lavoro o aree di produzione, né privi di risorse. Ad esempio, un processo di assemblaggio potrebbe consistere nel prelevare due bottiglie di vino e un pacchetto di caffè, quindi di imballarli come articolo da regalo.  

Una DB di assemblaggio contiene i dati master che definiscono gli articoli componenti che costituiscono un articolo finale assemblato e le risorse che vengono utilizzate per assemblare l'articolo di assemblaggio. Immettendo un articolo di assemblaggio e una quantità nella testata di un nuovo ordine di assemblaggio, le righe ordine di assemblaggio vengono automaticamente immesse in base alla DB di assemblaggio con una riga ordine di assemblaggio per ogni componente o risorsa. Per ulteriori informazioni, vedi [Gestione assemblaggio](assembly-assemble-items.md).

[!INCLUDE[prod_short](includes/prod_short.md)] supporta anche le DB di produzione. Le DB di produzione differiscono dalle DB di assemblaggio in quanto implicano procedure più complesse, tra cui l'utilizzo delle risorse, il ciclo di produzione e i centri di lavoro o produzione. Per ulteriori informazioni sulle differenze vedi [Utilizzare le distinte base](inventory-how-work-BOMs.md) e [Creare le distinte base di produzione](production-how-to-create-production-boms.md).

## <a name="to-create-an-assembly-bom" />Per creare una DB di assemblaggio

Per definire un articolo padre composto da altri articoli e potenzialmente da risorse richieste per l'assemblaggio, è necessario creare una DB di assemblaggio.  

Le DB di assemblaggio in genere contengono articoli ma possono anche contenere una o più risorse richieste per l'assemblaggio dell'articolo.

Le DB di assemblaggio possono essere multilivello, cioè un componente della DB di assemblaggio può essere un articolo di assemblaggio esso stesso. In tal caso, il campo **DB assemblaggio** nella riga della DB di assemblaggio contiene il valore **Sì**.

Requisiti speciali si applicano agli articoli nelle DB di assemblaggio in relazione alla disponibilità. Per ulteriori informazioni, vedi [Per visualizzare la disponibilità di un articolo per l'utilizzo in DB di assemblaggio](inventory-how-availability-overview.md#to-view-the-availability-of-an-item-by-its-use-in-assembly-or-production-boms).

Esistono due passaggi per creare una DB di assemblaggio:

- Impostazione di un nuovo articolo
- Definizione della struttura della distinta base dell'articolo di assemblaggio.

1. Impostare un nuovo articolo. Ulteriori informazioni in [Registrare nuovi articoli](inventory-how-register-new-items.md).

   Continuare a inserire componenti o risorse nella distinta base di assemblaggio.  
2. Nella pagina **Scheda articolo** per un articolo di assemblaggio, scegli l'azione **Assembla** quindi l'azione **DB assemblaggio**.
3. Nella pagina **DB assemblaggio** compilare i campi secondo le proprie necessità. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Gli articolo di assemblaggio possono avere diverse varianti impostate in [!INCLUDE[prod_short](includes/prod_short.md)] proprio come qualsiasi altro articolo, aiutandoti a mantenere contenuto l'elenco dei prodotti disponibili. Per ulteriori informazioni sulla funzionalità, vedi [Gestire le varianti di prodotto](inventory-item-variants.md).

## <a name="to-edit-assembly-boms" />Per modificare le DB di assemblaggio

È possibile modificare le righe di una distinta base di assemblaggio in qualsiasi momento. Tuttavia, tenere presente che la distinta base potrebbe essere in uso nelle vendite o negli assemblaggi dell'elemento padre, che potrebbero essere influenzati dalla modifica. Scegliere l'azione **Dove-usato** per vedere in quali articoli viene utilizzato e quindi se gli ordini di vendita o di assemblaggio possono essere interessati.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") , inserisci **Elemento** e scegli il link relativo.
2. Scegliere il valore **Sì** nella colonna **DB assemblaggio**.
3. Nella pagina **DB assemblaggio**, scegli l'azione **Modifica elenco**, quindi modifica i campi secondo necessità.

## <a name="to-view-components-and-resources-indented-according-to-the-bom-structure" />Per visualizzare i componenti e le risorse con indentazione in base alla struttura DB

Nella pagina **DB assemblaggio**, è possibile aprire una pagina distinta in cui vengono visualizzati i componenti e tutte le risorse indentate in base alla posizione nella distinta base dell'articolo di assemblaggio.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") , inserisci **Elemento** e scegli il link relativo.
2. Aprire la scheda per l'articolo di assemblaggio. (Il campo **DB assemblaggio** nella pagina **Articoli** contiene il valore **Sì**.)
3. Nella pagina **Scheda articolo** scegli l'azione **Assembla** quindi l'azione **DB assemblaggio**.
4. Nella pagina **DB assemblaggio** selezionare l'azione **Mostra DB**.

## <a name="to-replace-the-assembly-item-with-its-components-on-document-lines" />Per sostituire l'articolo di assemblaggio con i suoi componenti nelle righe del documento

Da un documento di vendita e di acquisto contenente un articolo di assemblaggio è possibile utilizzare una funzione speciale per sostituire la riga per l'articolo di assemblaggio con nuove righe per i componenti. Questa funzione è utile, ad esempio, se si intende vendere i componenti come kit che rappresenta l'articolo di assemblaggio.

L'azione **Esplodi DB** è anche disponibile nella pagina **DB assemblaggio** come metodo per visualizzare gli articoli di sottoassemblaggi in una DB di assemblaggio.

> [!CAUTION]  
> Una volta utilizzata la funzione **Esplodi DB**, non è possibile annullare l'operazione facilmente. È necessario eliminare le righe ordine di vendita che rappresentano i componenti e registrare nuovamente una riga ordine di vendita per l'articolo di assemblaggio.

La seguente procedura è basata su fattura di vendita. La stessa procedura si applica ad altri documenti di vendita e a tutti i documenti di acquisto.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Fatture vendite**, quindi seleziona il collegamento correlato.
2. Aprire una fattura di vendita che contiene una riga per un articolo di assemblaggio.
3. Scegli la riga per un articolo di assemblaggio quindi l'azione riga **Esplodi DB**.

Tutti i campi nella riga della fattura di vendita per l'articolo di assemblaggio vengono cancellati ad eccezione dei campi **Descrizione** e **Articolo**. Le righe intere della fattura di vendita vengono immesse per i componenti e le risorse possibili che costituiscono l'articolo di assemblaggio.

> [!NOTE]
> Il report **Lista prelievo per ordine** viene inoltre modificato per mostrare solo i componenti. Ciò significa che un lavoratore warehouse che preleva l'articolo principale, l'articolo di assemblaggio non lo vedrà nella lista prelievo. Per ulteriori informazioni, vedi [Stampare la lista prelievo](sales-how-print-picking-list.md).

## <a name="to-calculate-the-standard-cost-of-an-assembly-item" />Per calcolare il costo standard di un articolo di assemblaggio

Si calcola il costo unitario di un articolo di assemblaggio eseguendo il ricalcolo del costo unitario di ciascun componente e risorsa nella DB di assemblaggio dell'articolo.

È inoltre possibile calcolare e aggiornare il costo standard di un o più articoli nella pagina **Prospetto costo standard**. Per ulteriori informazioni, vedi [Aggiornare i costi standard](finance-how-to-update-standard-costs.md).  

Il costo unitario di una DB di assemblaggio è sempre uguale al totale dei costi unitari dei suoi componenti, comprese le DB di assemblaggio ed eventuali risorse.  

> [!NOTE]
> [!INCLUDE [bom-standard-cost](includes/bom-standard-cost.md)]

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") , inserisci **Elemento** e scegli il link relativo.
2. Aprire la scheda per l'articolo di assemblaggio. (Il campo **DB assemblaggio** nella pagina **Articoli** contiene il valore **Sì**.)
3. Nella pagina **Scheda articolo** scegli l'azione **Assembla** quindi l'azione **DB assemblaggio**.
4. Nella pagina **DB assemblaggio**, selezionare l'azione **Calc. costo standard**.
5. Seleziona una delle seguenti opzioni e scegli il pulsante **OK**.

|Opzione |Descrizione |
|-------|------------|
|**Livello principale**|Calcola il costo standard dell'articolo di assemblaggio come costo totale di tutti gli articoli acquistati o assemblati in tale DB di assemblaggio indipendentemente dalle DB di assemblaggio sottostanti.|
|**Tutti i Livelli**|Viene calcolato il costo standard dell'articolo di assemblaggio come somma dei seguenti elementi: 1) Il costo calcolato di tutte le distinte base di assemblaggio sottostanti della distinta base di assemblaggio. 2) Il costo di tutti gli articoli acquistati nella DB di assemblaggio.|

I costi degli articoli che compongono la DB di assemblaggio vengono copiate dalle schede articoli componenti. Il costo di ogni articolo viene moltiplicato per la quantità e il costo totale viene mostrato nel campo **Costo unitario** nella scheda articolo.

## <a name="see-related-microsoft-trainingtrainingmodulesset-up-assembly-items-dynamics-365-business-central" />Vedi il relativo [training Microsoft](/training/modules/set-up-assembly-items-dynamics-365-business-central/).

## <a name="see-also" />Vedere anche

[Registrare nuovi articoli](inventory-how-register-new-items.md)  
[Gestire le varianti di prodotto](inventory-item-variants.md)  
[Visualizzare la disponibilità di articoli](inventory-how-availability-overview.md)  
[Magazzino](inventory-manage-inventory.md)  
[Utilizzare le distinte base](inventory-how-work-BOMs.md)  
[Creare le distinte base di produzione](production-how-to-create-production-boms.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
