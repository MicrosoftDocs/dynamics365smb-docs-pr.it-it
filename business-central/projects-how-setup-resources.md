---
title: "Impostare costi, prezzi e capacità per le risorse| Documenti Microsoft"
description: "Per utilizzare le risorse e semplificare la gestione dei progetti, specificare i costi e i prezzi per le singole risorse o i gruppi di risorse e impostare la capacità della risorsa."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 362f335fa313dce9a4e75c962ef6f5a2f01ec5fd
ms.contentlocale: it-it
ms.lasthandoff: 11/26/2018

---
# <a name="set-up-resources"></a>Impostare risorse
Per gestire correttamente le attività delle risorse, è necessario impostare le risorse, nonché i costi e i prezzi correlati. I prezzi, gli sconti e le regole dei fattori di costi correlati a una commessa vengono impostati nella scheda commessa. È possibile specificare i costi e i prezzi per singole risorse, gruppi di risorse oppure per tutte le risorse disponibili della società.

Quando le risorse vengono utilizzate o vendute nell'ambito di una commessa, i prezzi e i costi ad esse associati vengono recuperati dalle informazioni impostate.

L'importo orario di default viene specificato durante la creazione della risorsa. Se, ad esempio, si utilizza per cinque ore un macchinario per l'esecuzione di una commessa, quest'ultima verrà calcolata sulla base dell'importo orario.

## <a name="to-set-up-a-resource"></a>Per impostare una risorsa
Creare una scheda per ogni risorsa che si desidera utilizzare nei progetti.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Risorse** e quindi scegliere il collegamento correlato.
2. Scegliere l'azione **Nuovo**.
3. Compilare i campi, se necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-set-up-a-resource-group"></a>Per impostare un gruppo di risorse
È possibile unire diverse risorse in uno stesso gruppo di risorse. Le capacità e i budget di un gruppo di risorse sono il risultato della somma delle capacità e dei budget delle singole risorse. È possibile immettere le capacità dei gruppi di risorse indipendentemente dai valori accumulati oppure in aggiunta a questi.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Gruppi di risorse** e quindi scegliere il collegamento correlato.
2. Scegliere l'azione **Nuovo**.
3. Compilare i campi, se necessario.

## <a name="to-set-capacity-for-a-resource"></a>Per impostare la capacità per una risorsa
Per calcolare quanto tempo una risorsa può dedicare alle commesse, la relativa capacità deve essere prima impostata come tempo disponibile per periodo nel calendario di produzione. Questa impostazione è utilizzata quando si compilano le righe di pianificazione commessa che contengono la risorsa. Per ulteriori informazioni, vedere [Creare le commesse](projects-how-create-jobs.md).

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Risorse** e quindi scegliere il collegamento correlato.
2. Aprire la scheda risorsa interessata e scegliere l'azione **Capacità risorsa**.
3. Nella pagina **Capacità risorsa** nel campo **Visualizza per** specificare la durata del periodo, ad esempio **giorno**, che viene visualizzato nelle colonne della Scheda dettaglio **Matrice capacità risorse**.
4. Per ogni risorsa di una riga, specificare per ogni periodo nelle colonne il numero di ore per cui la risorsa è disponibile.
5. In alternativa, per dettagliare la capacità settimanale della risorsa con una data di inizio e una data di fine, scegliere l'azione **Imposta capacità**.
6. Nella pagina **Impostazioni capacità risorse** compilare i campi in una riga in base alle esigenze.
7. Scegliere l'azione **Aggiorna capacità**. La pagina **Capacità risorsa** viene aggiornata con la capacità immessa.
8. Chiudere la pagina.

## <a name="to-set-up-alternate-resource-costs"></a>Per impostare costi di risorsa alternativi
Oltre al costo specificato nella scheda risorsa, è possibile impostare dei costi alternativi per ogni risorsa. Se ad esempio un lavoratore percepisce una paga oraria maggiore per il lavoro straordinario, si può impostare un costo risorsa per lo straordinario. Il costo alternativo impostato per la risorsa sovrascriverà il costo nella scheda della risorsa, quando si utilizzerà la risorsa nelle registrazioni risorse.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Risorse** e quindi scegliere il collegamento correlato.  
2. Selezionare la risorsa per la quale si desidera impostare uno o più costi alternativi, quindi scegliere l'azione **Costi**.  
3. Nella pagina **Costi risorse** compilare i campi in una riga in base alle esigenze.  
4. Ripetere il passaggio 3 per ogni costo di risorsa alternativo che si desidera impostare.

**Nota**. Per impostare i costi risorse da applicare a tutte le risorse e ai gruppi di risorse, aprire la pagina **Costi risorse** e compilare i campi.

## <a name="to-set-up-alternate-resource-prices"></a>Per impostare prezzi di risorsa alternativi
Oltre al prezzo specificato nella scheda risorsa, è possibile impostare dei prezzi alternativi per ogni risorsa. Questi prezzi alternativi possono essere condizionali. Possono dipendere dal fatto che la risorsa sia utilizzata con un tipo di lavoro o una commessa specifica.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Risorse** e quindi scegliere il collegamento correlato.
2. Selezionare la risorsa per la quale si desidera impostare uno o più prezzi alternativi, quindi scegliere l'azione **Prezzi**.
3. Nella pagina **Prezzi risorse** compilare i campi in una riga in base alle esigenze.
4. Ripetere il passaggio 3 per ogni prezzo di risorsa alternativo che si desidera impostare.

## <a name="see-also"></a>Vedi anche
[Impostazione della Gestione progetti](projects-setup-projects.md)  
[Gestione progetti](projects-manage-projects.md)  
[Finanze](finance.md)  
[Acquisti](purchasing-manage-purchasing.md)         
[Vendite](sales-manage-sales.md)      
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

