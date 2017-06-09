---
title: 'Procedura: Gestire i budget delle commesse | Documenti Microsoft'
description: Viene descritto come gestire il budget per le commesse.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project budget, forecast
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 9a351b581e0312d21b04db43a85243b8a5afb0e3
ms.contentlocale: it-it
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-manage-job-budgets"></a>Procedura: Gestire i budget delle commesse
È possibile impostare un budget per ogni commessa. Il budget viene utilizzato per pianificare le risorse allocate a una commessa. Il budget può essere generale con pochi movimenti oppure può contenere più movimenti divisi in livelli di attività. È quindi possibile confrontare gli importi previsti con l'utilizzo effettivo come registrato nelle registrazioni commesse. Monitorando le differenze tra l'utilizzo effettivo e quello a budget, è possibile controllare un progetto in corso e migliorare la qualità di commesse future riducendo il rischio di sottovalutazione dei costi.

Di seguito viene descritto come stimare i costi a budget durante la pianificazione. Per informazioni su come registrare i prezzi e i costi di commesse a budget rispetto a quelli effettivi, vedere [Procedura: Registrare l'utilizzo nelle commesse](projects-how-record-job-usage.md).  

## <a name="JobBudgetCosts"></a> Per stimare i costi a budget per una commessa
Quando un cliente desidera conoscere il prezzo di una commessa che verrà fatturata in base all'utilizzo, è necessario determinare i costi a budget per la commessa. A tale scopo, utilizzare la finestra **Righe task commessa**.

1. Nell'angolo superiore destro scegliere l'icona **Cerca pagina o report** ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), inserire **Commesse**, quindi scegliere il collegamento correlato.  
2. Aprire una commessa appropriata.
3. Selezionare una riga di task di tipo Registrazione quindi scegliere l'azione **Righe pianificazione commessa**.
4. In una nuova riga, compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]   

Per il campo **Tipo riga** fare riferimento alle seguenti informazioni.  

| Tipo riga | Descrizione |
| --- | --- |
| **Sia Budget sia fatturabile** |Gli importi relativi a costi e prezzo immessi nella riga di pianificazione sono i costi a budget per la riga di pianificazione specifica. L'importo dei prezzi verrà fatturato. |
| **Budget** |Al cliente non viene addebitato l'utilizzo. L'utilizzo non è trasferito in una fattura ma verrà comunque utilizzato nel calcolo di WIP. |
| **Fatturabile** |Al cliente viene addebitato l'utilizzo. L'utilizzo viene trasferito nella fattura, in base alla quantità specificata nel campo Qtà da trasferire nel campo Fattura. |

**Nota**: il campo **Data pianificazione** per la riga di pianificazione contiene la data in cui è previsto il completamento dell'utilizzo correlato alla riga di pianificazione. È inoltre la data in cui la riga di pianificazione può essere trasferita a una fattura vendita ed essere registrata.  

**Nota**: quando si compila il campo **Quantità**, tutte le informazioni sul prezzo totale e i costi totali saranno calcolate e immesse per quella riga di registrazione. È possibile modificarle in qualsiasi momento.

Nella finestra **Scheda commessa**, è possibile ora vedere un riepilogo dei costi a budget totali, del prezzo a budget, del costo e del prezzo fatturabili per ciascun task.

Per informazioni su come registrare i prezzi e i costi di commesse a budget rispetto a quelli effettivi, vedere [Procedura: Registrare l'utilizzo nelle commesse](projects-how-record-job-usage.md).

## <a name="see-also"></a>Vedi anche
[Gestione progetti](projects-manage-projects.md)  
[Finanza](finance.md)  
[Acquisti](purchasing-manage-purchasing.md)         
[Vendite](sales-manage-sales.md)      
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

