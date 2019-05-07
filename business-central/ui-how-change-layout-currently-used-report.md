---
title: Modificare l'aspetto di un report selezionando un layout diverso | Documenti Microsoft
description: È possibile utilizzare diversi layout per un report e passate tra i layout per modificare l'aspetto di un report.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: f24f1cd24a31ddbd0b455b876821ae0173a677c3
ms.sourcegitcommit: addfb47612cc2e4e98dfd7e338b6f41cde405d5c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2019
ms.locfileid: "969811"
---
# <a name="change-which-layout-is-currently-used-on-a-report"></a>Modificare il layout attualmente utilizzato in un report
Un report può essere impostato con diversi layout di report, che è possibile alternare a seconda delle necessità.

In base ai layout disponibili per un report, è possibile scegliere di utilizzare un layout di report RDLC o Word predefinito o un layout personalizzato. Per ulteriori informazioni sui layout di report RDLC e Word, sui layout personalizzati integrati e altro ancora, vedere [Gestire i layout dei report](ui-manage-report-layouts.md).

> [!TIP]  
> I report documento (non elenchi) che utilizzano un layout report Word sono in genere più rapidi di quelli che utilizzano un layout report RDLC. Quindi, se si ha la possibilità di scegliere tra un layout report Word o RDLC per un report documento, utilizzare il report layout Word per ottenere le migliori prestazioni.  

## <a name="to-change-the-layout-that-is-used-on-a-report"></a>Per modificare il layout utilizzato in un report
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Selezione layout report** e quindi scegliere il collegamento correlato.  
   Nella pagina **Selezione layout report** sono elencati tutti i report disponibili per la società che è specificata nel campo Società nella parte superiore della pagina. Il campo Layout selezionato specifica il layout che attualmente è utilizzato nel report.
2. Impostare il campo **Società** nella parte superiore della pagina alla società che include il report.
3. Per modificare il layout utilizzato da un report, nella riga del report nell'elenco, impostare il campo **Layout selezionato** su una delle seguenti opzioni:
   * RDLC (predefinito) utilizza nel report il layout di report RDLC integrato.
   * Word (predefinito) utilizza nel report il layout di report Word integrato.
   * Personalizzato utilizza nel report un layout personalizzato.  
     È possibile visualizzare i layout personalizzati disponibili per il report nel Dettaglio informazioni Parte di layout report. Se non esistono layout personalizzati per il report, è necessario innanzitutto creare uno. Se si seleziona questa opzione, andare alla procedura descritta di seguito per specificare il layout personalizzato da utilizzare.

    > [!NOTE]  
    >   Se si sceglie **RDLC (predefinito)** o **Word (predefinito)** e si visualizza un messaggio di errore che indica che il report non dispone di un layout del tipo specificato, è necessario selezionare un'altra opzione di layout o creare un layout di report personalizzato del tipo che si desidera utilizzare.

Se è stato selezionato un layout di report RDLC o Word predefinito, non sono necessarie ulteriori azioni e il layout verrà utilizzato alla successiva esecuzione del report.

## <a name="to-specify-a-custom-layout-on-a-report"></a>Per specificare un layout personalizzato in un report
1. Specificare quale layout personalizzato utilizzare nel report dalla pagina **Layout report personalizzati**. Se la pagina **Layout report personalizzati** non è aperta, nel campo **Descrizione layout report** scegliere il pulsante di ricerca.
2. Nella pagina **Layout report personalizzati** selezionare la riga di layout personalizzato che si desidera utilizzare, quindi chiudere la finestra.

Verrà visualizzata nuovamente la pagina **Selezione layout report**. Il nome del layout personalizzato selezionato viene visualizzato nel campo **Descrizione layout personalizzato**. Il layout personalizzato verrà utilizzato la volta successiva che si esegue il report.

## <a name="see-also"></a>Vedi anche
[Gestione dei layout di report](ui-manage-report-layouts.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
