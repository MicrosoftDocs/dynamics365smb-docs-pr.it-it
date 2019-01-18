---
title: 'Procedura: Utilizzare le distinte base per gestire i componenti | Documenti Microsoft'
description: Si crea una distinta base di assemblaggio o di produzione per specificare i componenti o le risorse richieste per un l'articolo che la distinta rappresenta.
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 587817f68dd731c1ea3e23617e405d0c9493fdd6
ms.contentlocale: it-it
ms.lasthandoff: 11/26/2018

---
# <a name="work-with-bills-of-material"></a>Utilizzare le distinte base
Utilizzare le distinte base (DB) per strutturare gli articoli padre che devono essere assemblati o prodotti dalle risorse o dai centri di lavoro a partire dai componenti. Una DB di assemblaggio può essere utilizzata anche per vendere un articolo padre come kit comprendente i relativi componenti.

## <a name="assembly-boms-or-production-boms"></a>DB di assemblaggio o DB di produzione
Utilizzare gli ordini di assemblaggio per la creazione di articoli finali dai componenti in un semplice processo che può essere svolto da una o più risorse di base, che non sono centri di lavoro o aree di produzione, né privi di risorse. Ad esempio, un processo di assemblaggio potrebbe consistere nel prelevare due bottiglie di vino e un pacchetto di caffè, quindi di imballarli come articolo da regalo.  

Una DB di assemblaggio contiene i dati master che definiscono gli articoli componenti che costituiscono un articolo finale assemblato e le risorse che vengono utilizzate per assemblare l'articolo di assemblaggio. Immettendo un articolo di assemblaggio e una quantità nella testata di un nuovo ordine di assemblaggio, le righe ordine di assemblaggio vengono automaticamente immesse in base alla DB di assemblaggio con una riga ordine di assemblaggio per ogni componente o risorsa. Per ulteriori informazioni, vedere [Gestione assemblaggio](assembly-assemble-items.md).

Le DB di assemblaggio sono descritte in questo argomento.

Utilizzare gli ordini di produzione per la creazione dio articoli finali dai componenti in una processo complesso che richiede un ciclo di produzione e centri di lavoro o aree di produzione che rappresentano le capacità di produzione. Ad esempio, un processo di produzione potrebbe consistere nel tagliare piastre di acciaio in un'unica operazione, saldarle nell'operazione successiva e verniciare l'articolo finale nell'ultima operazione. Per ulteriori informazioni, vedere [Manufacturing](production-manage-manufacturing.md).  

La distinta base di produzione corrisponde ai dati master che definiscono un articolo di produzione e ai componenti che lo costituiscono. Per gli articoli di assemblaggio, la distinta base di produzione deve essere certificata e assegnata all'articolo di produzione prima che possa essere utilizzata in un ordine di produzione. Immettendo l'articolo di produzione in una riga ordine di produzione, manualmente o aggiornando l'ordine, i contenuti della DB di produzione diventano i componenti dell'ordine di produzione. Per ulteriori informazioni, vedere [Creare distinte base di produzione](production-how-to-create-production-boms.md).  

Il concetto di risorse in produzione è molto più avanzato rispetto alla gestione assemblaggio. Le aree di produzione e centri di lavoro funzionano come risorse e i passaggi di produzione sono rappresentati dalle operazioni assegnate alle risorse nei cicli di produzione. Per ulteriori informazioni, vedere [Creare cicli](production-how-to-create-routings.md).

Gli ordini di assemblaggio e gli ordini di produzione possono essere collegati direttamente agli ordini di vendita. Tuttavia, è possibile utilizzare soltanto gli ordini di assemblaggio per personalizzare direttamente l'articolo finale per una richiesta cliente con l'ordine di vendita.

## <a name="to-create-an-assembly-bom"></a>Per creare una DB di assemblaggio
Per definire un articolo padre composto da altri articoli e potenzialmente da risorse richieste per l'assemblaggio, è necessario creare una DB di assemblaggio.  

Le DB di assemblaggio in genere contengono articoli ma possono anche contenere una o più risorse richieste per l'assemblaggio dell'articolo.

Le DB di assemblaggio possono essere multilivello, cioè un componente della DB di assemblaggio può essere un articolo di assemblaggio esso stesso. In tal caso, il campo **DB assemblaggio** nella riga della DB di assemblaggio contiene il valore **Sì**.

Requisiti speciali si applicano agli articoli nelle DB di assemblaggio correlati alla disponibilità. Per ulteriori informazioni, vedere la sezione "Per visualizzare la disponibilità di un articolo per l'utilizzo in DB di assemblaggio" in [Visualizzare la disponibilità di articoli](inventory-how-availability-overview.md).

Esistono due passaggi per creare una DB di assemblaggio:
- Impostazione di un nuovo articolo
- Definizione della struttura della distinta base dell'articolo di assemblaggio.

1. Impostare un nuovo articolo. Per ulteriori informazioni, vedere [Registrare nuovi articoli](inventory-how-register-new-items.md).

    Continuare a inserire componenti o risorse nella distinta base di assemblaggio.  
2. Nella pagina **Scheda articolo** per un articolo di assemblaggio, scegliere l'azione **Assembla** quindi l'azione **DB assemblaggio**.
3. Nella pagina **DB assemblaggio** compilare i campi secondo le proprie necessità. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-view-the-components-of-an-assembly-item-indented-according-to-the-bom-structure"></a>Per visualizzare i componenti di un articolo di assemblaggio con indentazione in base alla struttura DB
Nella pagina **DB assemblaggio**, è possibile aprire una pagina distinta in cui vengono visualizzati i componenti e tutte le risorse indentate in base alla posizione nella distinta base dell'articolo di assemblaggio.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Articoli** e quindi scegliere il collegamento correlato.
2. Aprire la scheda per l'articolo di assemblaggio. (Il campo **DB assemblaggio** nella pagina **Articoli** contiene il valore **Sì**.)
3. Nella pagina **Scheda articolo** scegliere l'azione **Assembla** quindi l'azione **DB assemblaggio**.
4. Nella pagina **DB assemblaggio** selezionare l'azione **Mostra DB**.

## <a name="to-replace-the-assembly-item-with-its-components-on-document-lines"></a>Per sostituire l'articolo di assemblaggio con i suoi componenti nelle righe del documento
Da un documento di vendita e di acquisto contenente un articolo di assemblaggio è possibile utilizzare una funzione speciale per sostituire la riga per l'articolo di assemblaggio con nuove righe per i componenti. Questa funzione è utile, ad esempio, se si intende vendere i componenti come kit che rappresenta l'articolo di assemblaggio.

**Attenzione**: una volta utilizzata la funzione **Esplodi DB**, non è possibile annullare l'operazione facilmente. È necessario eliminare le righe ordine di vendita che rappresentano i componenti e registrare nuovamente una riga ordine di vendita per l'articolo di assemblaggio.

La seguente procedura è basata su fattura di vendita. La stessa procedura si applica ad altri documenti di vendita e a tutti i documenti di acquisto.

1. Nell'angolo superiore destro scegliere l'icona **Cerca pagina o report**, immettere **Fatture vendite**, quindi scegliere il collegamento correlato.
2. Aprire una fattura di vendita che contiene una riga per un articolo di assemblaggio.
3. Scegliere la riga per un articolo di assemblaggio quindi l'azione riga **Esplodi DB**.

Tutti i campi nella riga della fattura di vendita per l'articolo di assemblaggio vengono cancellati ad eccezione dei campi **Descrizione** e **Articolo**. Le righe intere della fattura di vendita vengono immesse per i componenti e le risorse possibili che costituiscono l'articolo di assemblaggio.

**Nota**: la funzione Esplodi DB è anche disponibile nella pagina **DB assemblaggio**.

## <a name="to-calculate-the-standard-cost-of-an-assembly-item"></a>Per calcolare il costo standard di un articolo di assemblaggio
Si calcola il costo unitario di un articolo di assemblaggio eseguendo il ricalcolo del costo unitario di ciascun componente e risorsa nella DB di assemblaggio dell'articolo.

È inoltre possibile calcolare e aggiornare il costo standard di un o più articoli nella pagina **Prospetto costo standard**. Per ulteriori informazioni, vedere [Aggiornare i costi standard](finance-how-to-update-standard-costs.md).  

Il costo unitario di una DB di assemblaggio è sempre uguale al totale dei costi unitari dei suoi componenti, comprese le DB di assemblaggio ed eventuali risorse.

1. Nell'angolo superiore destro, scegliere l'icona **Cerca pagina o report**, immettere **Articoli**, quindi scegliere il collegamento correlato.
2. Aprire la scheda per l'articolo di assemblaggio. (Il campo **DB assemblaggio** nella pagina **Articoli** contiene il valore **Sì**.)
3. Nella pagina **Scheda articolo** scegliere l'azione **Assembla** quindi l'azione **DB assemblaggio**.
4. Nella pagina **DB assemblaggio**, selezionare l'azione **Calc. costo standard**.
5. Selezionare una delle seguenti opzioni e scegliere il pulsante **OK**.

|Opzione |Description |
|-------|------------|
|**Livello principale**|Calcola il costo standard dell'articolo di assemblaggio come costo totale di tutti gli articoli acquistati o assemblati in tale DB di assemblaggio indipendentemente dalle DB di assemblaggio sottostanti.|
|**Tutti i Livelli**|Viene calcolato il costo standard dell'articolo di assemblaggio come somma dei seguenti elementi: 1) Il costo calcolato di tutte le distinte base di assemblaggio sottostanti della distinta base di assemblaggio. 2) Il costo di tutti gli articoli acquistati nella DB di assemblaggio.|



I costi degli articoli che compongono la DB di assemblaggio vengono copiate dalle schede articoli componenti. Il costo di ogni articolo viene moltiplicato per la quantità e il costo totale viene mostrato nel campo **Costo unitario** nella scheda articolo.

## <a name="see-also"></a>Vedi anche
[Registrare nuovi articoli](inventory-how-register-new-items.md)  
[Visualizzare la disponibilità di articoli](inventory-how-availability-overview.md)     
[Magazzino](inventory-manage-inventory.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

