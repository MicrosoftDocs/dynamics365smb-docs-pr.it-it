---
title: Gestire impostazioni salvate per report e processi batch
description: Descrive come l'amministratore può impostare opzioni e filtri predefiniti per un report e condividere tali impostazioni con uno o tutti gli utenti.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customization, personalization'
ms.date: 12/21/2021
ms.author: edupont
---
# <a name="manage-saved-settings-for-reports-and-batch-jobs" />Gestire impostazioni salvate per report e processi batch

Quando si eseguono report, gli utenti di norma vedono una pagina che consente loro di selezionare opzioni e impostare filtri per modificare i dati inclusi nel report generato. Questa pagina è denominata la *pagina di richiesta*. Un report può includere uno o più *impostazioni salvate* che gli utenti possono applicare al report dalla pagina di richiesta. Le *impostazioni salvate* sono fondamentalmente opzioni e filtri predefiniti. L'utilizzo delle impostazioni salvate è un metodo rapido e affidabile di generare coerentemente report contenenti dati corretti. Per ulteriori informazioni, vedi [Usare le impostazioni salvate](ui-work-report.md#SavedSettings).

> [!NOTE]
> Questo argomento fa riferimento a *report* ma informazioni simili si applicano ai *processi batch*.

Se si dispone delle autorizzazioni appropriate, è possibile visualizzare, creare e modificare le impostazioni salvate per tutti i report di tutti gli utenti in una società. È possibile assegnare le impostazioni salvate per un report ai singoli utenti o a tutti gli utenti della società.

## <a name="manage-saved-settings" />Gestire le impostazioni salvate

È possibile gestire le impostazioni salvate nella pagina **Impostazioni report**. Sono disponibili due modi per aprire questa pagina:

- Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Impostazioni report**, quindi scegli il collegamento correlato.
- Nella pagina del richiesta del report, scegli la funzionalità di ricerca nel campo **Utilizza valori predefiniti da:**, quindi scegli l'azione **Seleziona da elenco completo**.

    Questo campo è visibile solo se hai eseguito il report almeno una volta in precedenza. L'elenco mostrerà solo le impostazioni a tua disposizione, perché sono le tue impostazioni o perché sono condivise con te.

Nella pagina **Impostazioni report** vengono visualizzate tutte le voci delle impostazioni salvate esistenti per tutti gli utenti. Se esiste un nome utente nel campo **Assegnato a**, solo tale utente può utilizzare le impostazioni salvate per il report associato. Se è presente un segno di spunta nel campo **Condiviso con tutti gli utenti**, tutti gli utenti possono utilizzare le impostazioni salvate per il report.  

> [!TIP]
> Quando un utente ha eseguito un report che supporta le impostazioni condivise, le sue impostazioni vengono salvate e aggiunte a questo elenco. Nella maggior parte dei casi, l'amministratore può quindi modificare tali impostazioni e scegliere di condividere le impostazioni con tutti gli utenti.
>
> Tuttavia, in alcuni casi, le impostazioni non possono essere condivise e l'amministratore non può nemmeno modificarle. La maggior parte dei processi batch non supporta le impostazioni condivise.  

## <a name="create-or-modify-saved-settings-for-all-users" />Creare o modificare le impostazioni salvate per tutti gli utenti

Nella pagina **Impostazioni report**, è possibile:

- Scegliere l'azione **Nuovo** per creare da zero una nuova voce di impostazioni salvate.
- Selezionare una voce di impostazioni salvate dall'elenco e scegliere l'azione **Copia** per creare una copia.
- Selezionare una voce di impostazioni salvate dall'elenco e scegliere l'azione **Modifica** per modificare una voce di impostazioni salvate.

> [!Important]
> Tenere in considerazione il nome che viene assegnato a una voce di impostazioni salvate. Se si crea una voce di impostazioni salvate per tutti gli utenti e le si assegna lo stesso nome di una voce di impostazioni salvate esistente solo per un utente specifico, tale utente non potrà utilizzare la voce di impostazioni salvate assegnata a tutti gli utenti.  Nella sezione **Impostazioni salvate** nella pagina di richiesta, l'utente vedrà due voci di impostazioni salvate con lo stesso nome. Tuttavia, indipendentemente dall'opzione scelta, verrà usata la voce di impostazioni salvate specifica dell'utente.

> [!NOTE]
> La funzionalità per salvare le impostazioni è disponibile solo nei report in cui la [proprietà SaveValues](/dynamics365/business-central/dev-itpro/developer/properties/devenv-savevalues-property) della pagina di richiesta del report è impostata su **Sì**. La proprietà **SaveValues** viene impostata dallo sviluppatore.  

## <a name="see-also" />Vedere anche

[Utilizzare report, processi batch e XMLport](ui-work-report.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
