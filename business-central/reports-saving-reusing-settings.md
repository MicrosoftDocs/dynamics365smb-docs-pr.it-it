---
title: Collegare e modificare le impostazioni salvate nei report | Documenti Microsoft
description: Descrive l'utilizzo delle opzioni predefinite e dei filtri per personalizzare un report e generare dati corretti.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customization, personalization
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: d9ae0f8e45c940d2a78d4d383a733ad378e90650
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3926349"
---
# <a name="manage-saved-settings-for-reports-and-batch-jobs"></a>Gestire impostazioni salvate per report e processi batch
Quando si eseguono report, gli utenti di norma vedono una pagina che consente loro di selezionare opzioni e impostare filtri per modificare i dati inclusi nel report generato. Questa pagina è denominata la pagina di richiesta. Un report può includere uno o più *impostazioni salvate* che gli utenti possono applicare al report dalla pagina di richiesta. Le *impostazioni salvate* sono fondamentalmente opzioni e filtri predefiniti. L'utilizzo delle impostazioni salvate è un metodo rapido e affidabile di generare coerentemente report contenenti dati corretti. Per ulteriori informazioni, vedere [Uso delle impostazioni salvate](ui-work-report.md#SavedSettings).

> [!NOTE]
> Questo argomento fa essenzialmente riferimento a “report" ma informazioni simili si applicano ai processi batch.

Se si dispone delle autorizzazioni appropriate, è possibile visualizzare, creare e modificare le impostazioni salvate per tutti i report di tutti gli utenti in una società. È possibile assegnare le impostazioni salvate per un report ai singoli utenti o a tutti gli utenti della società.

<!--
## Apply saved settings to a report
1. Open the report.

   The request page appears.    
2. In the **Saved Settings** section of the page, set the **Name** field  to the saved settings that you want to use.

   The **Saved Settings** section only appears if the report has been run before or if there are existing saved settings entries. The saved settings entry called **Last used options and filters** is always available. These settings are the option and filter values that were used the last time you ran the report.

-->

## <a name="to-create-and-modify-saved-settings-for-all-users"></a>Per creare e modificare impostazioni salvate per tutti gli utenti
È possibile gestire le impostazioni salvate nella pagina **Impostazioni report**. Sono disponibili due modi per aprire questa pagina:
-   Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Impostazioni report** e quindi scegliere il collegamento correlato.
-   Aprire un report, scegliere la funzionalità di ricerca nel campo **Utilizza valori predefiniti da:**, quindi scegliere l'azione **Seleziona da elenco completo**.

Nella pagina vengono visualizzate tutte le voci delle impostazioni salvate esistenti per tutti gli utenti. Se esiste un nome utente nel campo **Assegnato a**, solo tale utente può utilizzare le impostazioni salvate per il report associato. Se è presente un segno di spunta nel campo **Condiviso con tutti gli utenti**, tutti gli utenti possono utilizzare le impostazioni salvate per il report.

Nella pagina **Impostazioni report**, è possibile:
-   Scegliere l'azione **Nuovo** per creare da zero una nuova voce di impostazioni salvate.
-   Selezionare una voce di impostazioni salvate dall'elenco e scegliere l'azione **Copia** per creare una copia.
-   Selezionare una voce di impostazioni salvate dall'elenco e scegliere l'azione **Modifica** per modificare una voce di impostazioni salvate.

> [!Important]
> Tenere in considerazione il nome che viene assegnato a una voce di impostazioni salvate. Se si crea una voce di impostazioni salvate per tutti gli utenti e le si assegna lo stesso nome di una voce di impostazioni salvate esistente solo per un utente specifico, tale utente non potrà utilizzare la voce di impostazioni salvate assegnata a tutti gli utenti.  Nella sezione **Impostazioni salvate** nella pagina di richiesta, l'utente vedrà due voci di impostazioni salvate con lo stesso nome. Tuttavia, indipendentemente dall'opzione scelta, verrà usata la voce di impostazioni salvate specifica dell'utente.

> [!NOTE]
> La funzionalità Impostazioni salvate è disponibile solo nei report in cui la [proprietà SaveValues](/dynamics365/business-central/dev-itpro/developer/properties/devenv-savevalues-property) della pagina di richiesta del report è impostata su **Sì**. La proprietà **SaveValues** viene impostata nell'ambiente di sviluppo.  

## <a name="see-also"></a>Vedere anche
[Utilizzo di report, processi batch e XMLport](ui-work-report.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]