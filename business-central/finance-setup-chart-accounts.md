---
title: Impostazione di un piano dei conti
description: È possibile modificare i conti predefiniti nel piano dei conti ed è possibile aggiungere nuovi conti.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: COA, cha of acc
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: b20c4680393fa13b260beca366c7e4ba04abb291
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/17/2020
ms.locfileid: "4750382"
---
# <a name="setting-up-or-changing-the-chart-of-accounts"></a>Impostazione o modifica del piano dei conti
Il piano dei conti mostra i conti di contabilità che memorizzano i dati finanziari. [!INCLUDE[prod_short](includes/prod_short.md)] include un piano dei conti standard pronto per supportare l'azienda.
Tuttavia, è possibile modificare i conti predefiniti ed è possibile aggiungere nuovi conti.
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE43KO9?rel=0]


## <a name="adding-or-changing-accounts"></a>Aggiungere o modificare i conti
Nel piano dei conti, è possibile aprire ogni conto C/G e aggiungere o modificare le impostazioni.

> [!NOTE]  
>   È possibile eliminare un conto di contabilità generale. Tuttavia, prima che venga eliminato, è necessario soddisfare le seguenti condizioni:  
>  
>   * Il saldo nel conto deve essere pari a zero.  
>   * Nel campo **Consenti Eliminaz. Conti C/G Anteriori a** della pagina **Setup Contabilità Generale** deve essere impostata una data ed è necessario che il conto non includa movimenti contabili in tale data o dopo tale data.  
>   * Se il campo **Verifica Uso Conti C/G** della pagina **Setup Contabilità Generale** è selezionato, il conto non deve essere utilizzato in tutte le categorie di registrazione o impostazioni delle registrazioni.  

[!INCLUDE[prod_short](includes/prod_short.md)] impedirà di eliminare un conto di contabilità generale che memorizza i dati necessari per il piano dei conti.  

## <a name="see-related-training-at-microsoft-learn"></a>Vedere le informazioni relative al training in [Microsoft Learn](/learn/modules/chart-accounts-dynamics-365-business-central/index)

## <a name="see-also"></a>Vedere anche
[Contabilità generale e piano dei conti](finance-general-ledger.md)  
[Riconciliazione dei conti correnti bancari](bank-manage-bank-accounts.md)  
[Utilizzo delle dimensioni](finance-dimensions.md)  
[Importazione dei dati aziendali da altri sistemi contabili](across-import-data-configuration-packages.md)  
[Utilizzare le situazioni contabili](bi-how-work-account-schedule.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]