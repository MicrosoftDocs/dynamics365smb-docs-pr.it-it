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
ms.date: 09/08/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 42deec3d94209a7963e596e7deb5584fccd6db7f
ms.openlocfilehash: adc15d5f80f4d7ab2a1ca5a8247588ec0aa9779a
ms.contentlocale: it-it
ms.lasthandoff: 07/19/2018

---
# <a name="managing-saved-settings-on-reports"></a>Gestione impostazioni salvate nei report
A seconda del report che viene eseguito, potrebbe apparire una pagina che consente di impostare determinate opzioni e filtri per variare i dati inclusi nel report generato. Questa pagina è nota come la pagina di richiesta report. Un report può includere uno o più *impostazioni salvate* che è possibile applicare al report dalla pagina di richiesta. Le *impostazioni salvate* sono fondamentalmente opzioni e filtri predefiniti. L'utilizzo delle impostazioni salvate è un metodo rapido e affidabile di generare coerentemente report contenenti dati corretti.

È possibile visualizzare le impostazioni salvate a disposizione dell'utente per un report nella sezione **Impostazioni salvate** della pagina di richiesta report.  

## <a name="apply-saved-settings-to-a-report"></a>Applicare le impostazioni salvate a un report
1. Aprire il report.

   Viene visualizzata la pagina di richiesta report.    
2. Nella sezione **Impostazioni salvate** della pagina impostare il campo **Nome** sulle impostazioni salvate che si desidera utilizzare.

   La sezione **Impostazioni salvate** viene visualizzata solo se il report è già stato eseguito in precedenza o se esistono movimenti salvati delle impostazioni. Esiste sempre una voce Impostazioni salvate, che viene chiamata **Filtri e opzioni utilizzati di recente**. Queste impostazioni sono i valori delle opzioni e dei filtri che sono stati utilizzati l'ultima volta che è stato eseguito il report.

## <a name="create-and-modify-saved-settings-for-all-users"></a>Creare e modificare le impostazioni salvate per tutti gli utenti
Se si dispone delle autorizzazioni appropriate, è possibile visualizzare, creare e modificare le impostazioni salvate per tutti i report di tutti gli utenti nella società. È possibile assegnare le impostazioni salvate per un report ai singoli utenti o a tutti gli utenti della società.

È possibile gestire le impostazioni salvate nella pagina 1560 **Impostazioni report**. Per aprire questa pagina, scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Impostazioni report**, quindi scegliere il collegamento correlato.

Nella pagina **Impostazioni report** è possibile creare impostazioni ex novo o duplicarle e modificare le impostazioni esistenti. Per modificare le opzioni e i filtri di un'impostazione, scegliere l'azione **Modifica**.

> [!NOTE]
> La funzionalità Impostazioni salvate nei report è rilevante solo quando la proprietà SaveValues della pagina di richiesta è impostata su Sì. La proprietà SaveValues è impostata nell'ambiente di sviluppo.  

> [!Important]
> Se si crea un articolo impostazioni salvato per tutti gli utenti con lo stesso nome di un'impostazione salvata esistente per un utente specifico, tale utente non potrà utilizzare le impostazioni salvate assegnata a tutti gli utenti.  Nel campo Impostazioni salvate nella pagina di richiesta del report, l'utente vedrà due opzioni delle impostazioni salvate con lo stesso nome. Tuttavia, indipendentemente dall'opzione che sceglie, verranno usate le impostazioni salvate specifiche dell'utente.

## <a name="see-also"></a>Vedi anche
[Utilizzo dei report](ui-work-report.md)  

