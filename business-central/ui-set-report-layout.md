---
title: Impostazione del layout di report
description: Scopri come impostare il layout utilizzato in un report durante l'anteprima e la stampa.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.search.form: 9652, 9650
ms.date: 03/07/2022
ms.author: jswymer
ms.openlocfilehash: 9cc827630c5acfeba2efc860d8baf67cd31bb404
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2022
ms.locfileid: "8525091"
---
# <a name="setting-the-layout-used-by-a-report"></a>Impostare il layout utilizzato da un report

> **SI APPLICA A:** Business Central Online, primo ciclo di rilascio del 2022 Business Central locale e successivi. Per le versioni precedenti, vai [qui](ui-how-change-layout-currently-used-report.md).

Un layout di report determina l'aspetto di un report. Controlla quali campi di dati di un set di dati del report vengono visualizzati, come sono organizzati, definiti e altro ancora. Un report può avere più layout, che è possibile alternare a seconda delle necessità.

Quando nell'applicazione sono presenti più società, i layout vengono impostati per società. Quindi lo stesso report in una società può avere un layout diverso in un'altra società.

## <a name="get-started"></a>Inizia

Esistono due modi per impostare il layout utilizzato da un report. Un modo è dalla pagina **Selezione layout report**. L'altro modo è dalla pagina **Layout report**. Ogni pagina ha dei vantaggi, ad esempio: 

- La pagina **Selezione layout report** visualizza un elenco di tutti i report.

  Questa pagina indica qual è il layout corrente di un report. Inoltre, puoi impostare layout in diverse società, senza dover cambiare la società con cui lavori.

- La pagina **Layout report** visualizza tutti i layout disponibili per ogni report nella società corrente.

  È facile trovare un layout specifico ordinando o filtrando l'elenco. Una volta trovato il layout, puoi impostarlo per un report con un'unica selezione.

  > [!NOTE]
  > Non puoi usare la pagina **Layout report** per i layout di Word e RDLC creati utilizzando la funzionalità legacy **Layout personalizzati**. In effetti, non vedrai questi layout personalizzati elencati nella pagina **Layout report**. Per questi layout, puoi impostarli solo utilizzando la pagina **Selezione layout report**.

## <a name="set-the-layout-from-the-report-layouts-page"></a>Impostare il layout dalla pagina Layout report

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Trova il layout nell'elenco, selezionalo, quindi seleziona l'azione **Imposta predefinito** nella parte superiore della pagina.

## <a name="set-the-layout-from-report-layout-selection-page"></a>Impostare il layout dalla pagina Selezione layout report

1. Scegli la ![lampadina che apre la funzione Dimmi 1](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"). immetti **Selezione layout report**, quindi scegli il collegamento correlato.
  
   Nella pagina sono elencati tutti i report disponibili per la società che è specificata nel campo **Società** nella parte superiore della pagina. Il campo **Descrizione layout** specifica il layout che attualmente è utilizzato dal report.
2. Imposta il campo **Società** nella parte superiore della pagina sulla società che include il report.
3. Trova e seleziona il report nell'elenco, quindi esegui una delle seguenti operazioni:

   - Se il layout a cui vuoi passare non è il layout corrente, seleziona il campo **Tipo di layout** quindi scegli il tipo di layout che desideri impostare sul report. 
   - Se il layout che a cui desideri passare è dello stesso tipo del layout corrente, seleziona l'azione **Seleziona layout** in alto.

4. Nella pagina **Layout report** seleziona il layout, quindi seleziona **OK**.

## <a name="revert-to-the-original-default-layout"></a>Ripristinare il layout predefinito originale

I report sono progettati per utilizzare un layout per impostazione predefinita. È possibile tornare al layout predefinito originale dalla pagina **Selezione layout report**. Basta selezionare il report, quindi selezionare l'azione **Ripristina selezione predefinita** nella parte superiore della pagina.

## <a name="see-related-training-at-microsoft-learn"></a>Vedere le informazioni relative al training in [Microsoft Learn](/learn/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Vedere anche

[Gestione dei layout di report](ui-manage-report-layouts.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]