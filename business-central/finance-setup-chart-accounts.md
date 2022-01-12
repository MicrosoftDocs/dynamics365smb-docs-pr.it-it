---
title: Impostare il piano dei conti (video)
description: Il piano dei conti mostra i conti di contabilità che memorizzano i dati finanziari. Puoi modificare i conti predefiniti nel piano dei conti e aggiungere nuovi conti.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: COA, cha of acc
ms.date: 06/22/2021
ms.author: edupont
ms.openlocfilehash: 0ef1a35805413619c6da19654a8f501525997d35
ms.sourcegitcommit: 4c97f38fc53c1c1ec534054a4a100d8cfb73175b
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/20/2021
ms.locfileid: "7940553"
---
# <a name="setting-up-or-changing-the-chart-of-accounts"></a>Impostazione o modifica del piano dei conti

Il piano dei conti mostra i conti di contabilità che memorizzano i dati finanziari. [!INCLUDE[prod_short](includes/prod_short.md)] include un piano dei conti standard pronto per supportare l'azienda.
Tuttavia, è possibile modificare i conti predefiniti ed è possibile aggiungere nuovi conti.
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE43KO9?rel=0]

## <a name="adding-or-changing-accounts"></a>Aggiungere o modificare i conti

Nel piano dei conti, è possibile aprire ogni conto C/G e aggiungere o modificare le impostazioni. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

In caso di necessità è possibile utilizzare più di una riga per il nome di un conto C/G. Nella pagina **Scheda conto C/G** nel gruppo **Conto** scegli **Testi estesi**, quindi compila una o più righe con il testo da copiare e il nome dell'account.  

Per i conti di tipo **Totale** compila il campo **Totale**. Per i conti di tipo **Totale finale** questo campo viene compilato automaticamente tramite la funzione di indentazione. Dopo aver impostato tutti gli account, scegli l'azione **Elabora**, quindi scegli **Indenta piano dei conti**.  

> [!IMPORTANT]
> Se le definizioni per i conti **Totale Finale** sono state immesse nei campi **Totale** prima di eseguire la funzione di indentazione, sarà necessario inserirle nuovamente in seguito poiché questa funzione sovrascrive i valori in tutti i campi **Totale finale**.

## <a name="deleting-accounts"></a>Eliminazione di conti

È possibile eliminare un conto di contabilità generale. Tuttavia, prima che venga eliminato, è necessario soddisfare le seguenti condizioni:  

* Il saldo nel conto deve essere pari a zero.  
* Nel campo **Consenti Eliminaz. Conti C/G Anteriori a** della pagina **Setup Contabilità Generale** deve essere impostata una data ed è necessario che il conto non includa movimenti contabili in tale data o dopo tale data.  
* Se il campo **Verifica Uso Conti C/G** della pagina **Setup Contabilità Generale** è selezionato, il conto non deve essere utilizzato in tutte le categorie di registrazione o impostazioni delle registrazioni.  

[!INCLUDE[prod_short](includes/prod_short.md)] impedirà di eliminare un conto di contabilità generale che memorizza i dati necessari per il piano dei conti.  

## <a name="see-related-training-at-microsoft-learn"></a>Vedere le informazioni relative al training in [Microsoft Learn](/learn/modules/chart-accounts-dynamics-365-business-central/index)

## <a name="see-also"></a>Vedere anche

[Contabilità generale e piano dei conti](finance-general-ledger.md)  
[Riconciliazione dei conti correnti bancari](bank-manage-bank-accounts.md)  
[Utilizzo delle dimensioni](finance-dimensions.md)  
[Importazione dei dati aziendali da altri sistemi contabili](across-import-data-configuration-packages.md)  
[Utilizzare le situazioni contabili](bi-how-work-account-schedule.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Chiudere i conti del conto economico nella versione francese](LocalFunctionality/France/how-to-close-income-statement-accounts.md)  
[Stampare il conto economico nella versione australiana](LocalFunctionality/Australia/how-to-print-income-statements.md)  
[Stampare il conto economico nella versione della Nuova Zelanda](LocalFunctionality/NewZealand/how-to-print-income-statements.md)  
[Impostare e chiudere i saldi di conto economico nella versione spagnola](LocalFunctionality/Spain/how-to-set-up-and-close-income-statement-balances.md)  
[Indentare e convalidare il piano dei conti nella versione spagnola](LocalFunctionality/Spain/how-to-indent-and-validate-chart-of-accounts.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]