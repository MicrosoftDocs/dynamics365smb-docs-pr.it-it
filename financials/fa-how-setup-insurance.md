---
title: Impostare l'assicurazione cespiti| Documenti Microsoft
description: "Per gestire la copertura assicurativa del cespite è necessario impostare le informazioni generali sull'assicurazione e una scheda assicurazione."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: policy, coverage
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 8e88002c920e392cd61f2a899811fd0434d8cb4b
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-fixed-asset-insurance"></a>Procedura: Impostare l'assicurazione cespiti
Per gestire la copertura assicurativa del cespite, è prima necessario impostare alcune informazioni generali sull'assicurazione e una scheda assicurazione per ogni polizza.

## <a name="to-set-up-general-insurance-information"></a>Per impostare le informazioni generali delle assicurazioni
Per utilizzare le funzionalità dell'assicurazione in [!INCLUDE[d365fin](includes/d365fin_md.md)], occorre impostare alcune informazioni generali sull'assicurazione.  

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Setup cespiti**, quindi scegliere il collegamento correlato.  
2. Compilare i campi, se necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-set-up-insurance-types"></a>Per impostare i tipi di assicurazione
È possibile raggruppare le polizze assicurative in categorie, ad esempio assicurazione da furti o incendi. I tipi di assicurazione vengono utilizzati nella Scheda Assicurazione.

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Tipi di assicurazione**, quindi scegliere il collegamento correlato.  
2. Compilare i campi, se necessario.

## <a name="to-set-up-insurance-cards"></a>Per impostare le schede assicurazione
È possibile raggruppare informazioni relative ad ogni polizza assicurativa nella scheda di assicurazione.  

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Assicurazione**, quindi scegliere il collegamento correlato.  
2. Scegliere l'azione **Nuovo** nella finestra **Assicurazione** per creare una nuova scheda per l'assicurazione.  
3. Compilare i campi, se necessario.

## <a name="to-set-up-insurance-journal-templates"></a>Per impostare le definizioni registrazioni assicurazioni
Una definizione delle registrazioni assicurazioni viene creata automaticamente in [!INCLUDE[d365fin](includes/d365fin_md.md)] la prima volta che si apre la finestra **Registr. assicuraz.**. È tuttavia possibile impostare definizioni delle registrazioni aggiuntive. Per ulteriori informazioni, vedere [Utilizzo delle registrazioni COGE](ui-work-general-journals.md).  

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Def. reg. assicurazioni**, quindi scegliere il collegamento correlato.  
2. Compilare i campi, se necessario.

## <a name="to-set-up-insurance-journal-batches"></a>Per impostare i batch registrazioni assicurazioni
I batch possono essere impostati in una definizione registrazioni assicurazioni. I valori nel batch delle registrazioni vengono utilizzati come valori di default nel caso in cui i campi nelle righe delle registrazioni non siano compilati. Per ulteriori informazioni, vedere [Elaborazione delle registrazioni COGE](ui-work-general-journals.md)  

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Def. reg. assicurazioni**, quindi scegliere il collegamento correlato.  
2. Selezionare una definizione registrazioni assicurazione e quindi scegliere l'azione **Batch**.
3. Nella finestra **Batch registrazioni assicurazioni** compilare i campi in base alle esigenze.

> [!NOTE]  
>   I numeri hanno una funzione speciale nei nomi delle registrazioni. Se il nome definizione registrazioni o un nome batch registrazioni contiene un numero, quest'ultimo viene automaticamente incrementato di una unità ogni volta che le registrazioni vengono contabilizzate. Se ad esempio si immette HH1 nel campo **Nome**, il nome della registrazione verrà modificato in HH2 dopo la contabilizzazione della registrazione denominata HH1.

## <a name="see-also"></a>Vedi anche
[Impostazione di cespiti](fa-setup.md)  
[Cespiti](fa-manage.md)  
[Finanze](finance.md)  
[Benvenuto in [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

