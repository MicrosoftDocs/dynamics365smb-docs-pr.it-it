---
title: 'Procedura: Importare transazioni retribuzioni | Documenti Microsoft'
description: "Viene descritto come importare i pagamenti di stipendio e le transazioni correlate dal provider di retribuzioni nella contabilità generale."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Ceridian, Quickbooks, salary
ms.date: 03/24/2017
ms.author: SorenGP
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 8d7ee87a80b4de2bc90086c188e5a53291c52683
ms.contentlocale: it-it
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-import-payroll-transactions"></a>Procedura: Importare transazioni retributive 
Per indicare i pagamenti di stipendio e le transazioni correlate, è necessario importare e registrare in contabilità generale le transazioni finanziarie trasformate dal provider di retribuzioni. A tale scopo, è necessario innanzitutto importare un file che si riceve dal provider di retribuzioni nella finestra **Contabilità generale**. Successivamente si esegue il mapping tra i conti esterni nel file retribuzioni e i conti C/G pertinenti. Infine, si registrano le transazioni retribuzioni in base alla mappatura dei conti.

**Nota**: per utilizzare questa funzione, è necessario installare e abilitare un'estensione per l'importazione delle retribuzioni. Il Registro paga di Ceridian e le estensioni per l'importazione del file retribuzioni di Quickbooks sono preinstallati in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Per ulteriori informazioni, consultare [Personalizzazione di [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzando le estensioni](ui-extensions.md).

## <a name="to-import-a-payroll-file"></a>Per importare un file delle retribuzioni
1. Nell'angolo superiore destro scegliere l'icona **Cerca pagina o report** ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), inserire **Registrazioni COGE**, quindi scegliere il collegamento correlato.
2. Nel batch registrazioni COGE appropriato scegliere l'azione **Importa transazioni retribuzioni**. Si apre una guida al setup assistito.
3. Seguire i passaggi indicati nella finestra **Importa transazioni retribuzioni**.

    **Suggerimento**: nel passaggio relativo alla mappatura dei record di retribuzione esterni ai conti C/G, i mapping eseguiti verranno ricordati che la successiva importazione degli stessi record. In questo modo, sarà possibile risparmiare tempo perché non è necessario compilare manualmente il campo **Nr. conto** nelle registrazioni COGE ogni volta che si importano transazioni retribuzioni periodiche.   

    Se si sceglie il pulsante **OK** nella guida al setup assistito, la finestra **Contabilità generale** viene popolata con le righe che rappresentano le transazioni che contiene il file retribuzioni e con i conti appropriati già precompilati nei campi **Conto C/G** in base ai mapping effettuati nella guida.
4. Modificare o registrare le righe delle registrazioni relative a tutte le altre le transazioni della contabilità generale. Per ulteriori informazioni, vedere [Procedura: Elaborazione delle registrazioni COGE](ui-work-general-journals.md).   

## <a name="see-also"></a>Vedi anche
[Finanza](finance.md)  
[Personalizzazione di [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzando le estensioni](ui-extensions.md)  
[Procedura: Utilizzare le registrazioni di contabilità generale](ui-work-general-journals.md)  

