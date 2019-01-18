---
title: Collegare e modificare le impostazioni salvate nei report | Documenti Microsoft
description: Descrive l'utilizzo delle opzioni predefinite e dei filtri per personalizzare un report e generare dati corretti.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customization, personalization
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: 9fd086831c0d145570d87c33c62a003c166aca87
ms.contentlocale: it-it
ms.lasthandoff: 11/22/2018

---
# <a name="managing-saved-settings-on-reports"></a>Gestione impostazioni salvate nei report
Quando si esegue un report, gli utenti di norma vedono una pagina che consente loro di impostare determinate opzioni e filtri per variare i dati inclusi nel report generato. Questa pagina è chiamata la pagina di richiesta report. Un report può includere uno o più *impostazioni salvate* che gli utenti possono applicare al report dalla pagina di richiesta. Le *impostazioni salvate* sono fondamentalmente opzioni e filtri predefiniti. L'utilizzo delle impostazioni salvate è un metodo rapido e affidabile di generare coerentemente report contenenti dati corretti. Per ulteriori informazioni su come utilizzare le impostazioni salvate, vedere [Uso delle impostazioni salvate](ui-work-report.md#SavedSettings).

Se si dispone delle autorizzazioni appropriate, è possibile visualizzare, creare e modificare le impostazioni salvate per tutti i report di tutti gli utenti nella società. È possibile assegnare le impostazioni salvate per un report ai singoli utenti o a tutti gli utenti della società.

<!-- 
## Apply saved settings to a report
1. Open the report.

   The report request page appears.    
2. In the **Saved Settings** section of the page, set the **Name** field  to the saved settings that you want to use.

   The **Saved Settings** section only appears if the report has been run before or if there are existing saved settings entries. The saved settings entry called **Last used options and filters** is always available. These settings are the option and filter values that were used the last time you ran the report.

-->

## <a name="create-and-modify-saved-settings-for-all-users"></a>Creare e modificare le impostazioni salvate per tutti gli utenti
È possibile gestire le impostazioni salvate nella pagina **1560 Impostazioni report**. Sono disponibili due modi per aprire questa pagina:
-   Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Impostazioni report** e quindi scegliere il collegamento correlato.
-   Aprire un report, scegliere la funzionalità di ricerca accanto alla casella **Utilizza valori predefiniti da:**, scegliere **Seleziona da elenco completo**.

Nella pagina vengono visualizzate tutte le voci delle impostazioni salvate esistenti per tutti gli utenti. Se esiste un nome utente nella colonna **Assegnato a**, solo tale utente può utilizzare le impostazioni salvate per il report associato. Se è presente un segno di spunta nella colonna **Condiviso con tutti gli utenti**, tutti gli utenti possono utilizzare le impostazioni salvate per il report.

Nella pagina **Impostazioni report**, è possibile:
-   Scegliere **Nuovo** per creare da zero una nuova voce di impostazioni salvate.
-   Selezionare una voce di impostazioni salvate dall'elenco e scegliere **Copia** per creare una copia.
-   Selezionare una voce di impostazioni salvate dall'elenco e scegliere **Modifica** per modificare una voce di impostazioni salvate.


> [!Important]
> Tenere in considerazione il nome che viene assegnato a una voce di impostazioni salvate. Se si crea una voce di impostazioni salvate per tutti gli utenti e le si assegna lo stesso nome di una voce di impostazioni salvate esistente solo per un utente specifico, tale utente non potrà utilizzare la voce di impostazioni salvate assegnata a tutti gli utenti.  Nel campo **Impostazioni salvate** nella pagina di richiesta del report, l'utente vedrà due voci di impostazioni salvate con lo stesso nome. Tuttavia, indipendentemente dall'opzione che sceglie, verrà usata la voce di impostazioni salvate specifica dell'utente.

> [!NOTE]
> La funzionalità delle impostazioni salvate è disponibile solo nei report in cui la [proprietà SaveValues](https://docs.microsoft.com/en-us/dynamics-nav/savevalues-property) della pagina di richiesta del report è impostata su `Yes`. La proprietà **SaveValues** viene impostata nell'ambiente di sviluppo.  

## <a name="see-also"></a>Vedi anche
[Utilizzo dei report](ui-work-report.md)  

