---
title: Gestire le impostazioni e le preferenze dell'utente in Dynamics 365 Business Central
description: Gestire le impostazioni e le preferenze dell'utente in Dynamics 365 Business Central.
author: sorenfriisalexandersen
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user settings, preferences, language, region, time zone, regional settings
ms.date: 06/17/2020
ms.author: soalex
ms.openlocfilehash: 633a0872a878843f26d627dcd76e69d1c851ef8a
ms.sourcegitcommit: 3945f16d6d9c9853651e6291ce1465a44fd71fc8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/17/2020
ms.locfileid: "3460422"
---
# <a name="manage-user-settings-and-preferences"></a>Gestire le impostazioni e le preferenze dell'utente

Come amministratore, è possibile accedere alle impostazioni dell'utente in [!INCLUDE[d365fin](includes/d365fin_md.md)], in modo simile a come i singoli utenti possono gestire le proprie preferenze nella pagina **Impostazioni personali**.  

## <a name="types-of-user-settings"></a>Tipi di impostazioni utente

Le *impostazioni utente* non sono il *setup dell'utente*, che riguarda l'utente come entità e l'accesso dell'utente nel sistema. Inoltre, le impostazioni dell'utente non hanno nulla a che fare con la personalizzazione di un utente, come lievi modifiche all'interfaccia utente. Le impostazioni dell'utente determinano le preferenze dell'utente in vari aspetti del modo in cui l'applicazione si presenta all'utente. Il paragrafo seguente elenca i cinque tipi di impostazioni e preferenze dell'utente che possono essere impostate dall'utente o centralmente dall'amministratore:

- **Società**  

  Questa impostazione determina la società a cui accedere al successivo accesso. Un utente può avere accesso a più società e può essere attivo in diverse società.

- **Profilo (ruoli)**  

  Il profilo descrive la funzione dell'utente nella società, come ad esempio *Direttore vendite*, *Addetto contabile* o *Addetto acquisti*. Il profilo determina quindi la gestione ruolo dell'utente, la home page che gli utenti vedranno quando effettuano l'accesso. Il profilo non influisce sui diritti di accesso alla funzionalità in [!INCLUDE[d365fin](includes/d365fin_md.md)].  

- **ID impostazioni locali (impostazioni regionali)**  

  Definisce come le date e i numeri sono presentati nel client [!INCLUDE[d365fin](includes/d365fin_md.md)], ad esempio se utilizzare i formati di data europei o americani o come visualizzare il segno decimale e i separatori delle migliaia negli importi. Se gli utenti [!INCLUDE[d365fin](includes/d365fin_md.md)] sono sincronizzati da Office 365, le impostazioni regionali da Office 365 vengono utilizzate, presupponendo che l'utente desideri utilizzare le stesse impostazioni nei prodotti Office e [!INCLUDE[d365fin](includes/d365fin_md.md)]. Un amministratore o un utente può modificare queste impostazioni manualmente in [!INCLUDE[d365fin](includes/d365fin_md.md)], ma verranno reimpostate sul valore di Office 365 una volta eseguita la sincronizzazione successiva.

- **Lingua**  

  Definisce la lingua dell'applicazione che [!INCLUDE[d365fin](includes/d365fin_md.md)] usa per presentare testo, didascalie e messaggi di errore. Se gli utenti [!INCLUDE[d365fin](includes/d365fin_md.md)] sono sincronizzati da Office 365, le impostazioni di lingua da Office 365 vengono utilizzate, presupponendo che l'utente desideri utilizzare le stesse impostazioni nei prodotti Office e [!INCLUDE[d365fin](includes/d365fin_md.md)]. Un amministratore o un utente può modificare queste impostazioni manualmente in [!INCLUDE[d365fin](includes/d365fin_md.md)], ma verranno reimpostate sul valore di Office 365 una volta eseguita la sincronizzazione successiva.

  Se l'impostazione della lingua di Office 365 corrisponde a una lingua supportata in [!INCLUDE[d365fin](includes/d365fin_md.md)], questa lingua verrà scelta per l'utente.  

  > [!NOTE]
  > Potrebbe essere necessario installare un'app di lingua per [!INCLUDE[d365fin](includes/d365fin_md.md)] per visualizzare correttamente la lingua. Pertanto, è buona norma installare le app di lingua necessarie prima che qualsiasi utente acceda per la prima volta in modo che abbiano una buona esperienza fin dal primo giorno. Per ulteriori informazioni, consultare l'elenco delle [lingue supportate](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations).  
  
- **Fuso orario**  

  Definisce il fuso orario dell'utente. Attualmente questo non è sincronizzato da Office 365 e deve essere impostato manualmente.  

> [!NOTE]
> Se la sincronizzazione degli utenti di Office 365 viene effettuata mentre gli utenti sono connessi a [!INCLUDE[d365fin](includes/d365fin_md.md)], questi utenti devono aggiornare il browser o disconnettersi e accedere nuovamente a [!INCLUDE[d365fin](includes/d365fin_md.md)] per vedere una potenziale lingua diversa impostata dall'azione di sincronizzazione.

## <a name="overview-of-all-user-settings"></a>Panoramica di tutte le impostazioni dell'utente

Gli amministratori hanno la possibilità di impostare o modificare queste impostazioni per gli utenti di ciascuna società. Queste operazioni vengono eseguite nella pagina **Personalizzazioni utente**. I record in questa pagina rifletteranno le scelte del singolo utente per le impostazioni di cui sopra, un record per utente. Quando gli utenti apportano modifiche alle proprie impostazioni nella pagina **Impostazioni personali**, queste modifiche si rifletteranno nell'elenco **Personalizzazioni utente**. Gli amministratori possono anche configurare queste impostazioni per gli utenti prima che accedano per la prima volta, quindi gli utenti non devono farlo autonomamente, fornendo loro una migliore esperienza di *inizio*.

> [!NOTE]
> Le Personalizzazioni utente non hanno nulla a che fare con le leggere modifiche *personali* che un utente può apportare all'esperienza utente.

## <a name="to-review-or-make-changes-to-user-settings"></a>Per rivedere o apportare modifiche alle impostazioni dell'utente

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Icona Cerca pagina o report"), immettere **Personalizzazioni utente** e quindi scegliere il collegamento correlato.
2. Viene visualizzato l'elenco degli utenti e le loro impostazioni. Per modificare le impostazioni di un utente, fare clic su **ID utente** o scegliere **Gestisci** e poi **Modifica**.
3. Viene visualizzata la scheda **Personalizzazione utente** per le impostazioni dell'utente specifico e possono essere apportate le modifiche desiderate.  

## <a name="see-also"></a>Vedere anche

[Introduzione](product-get-started.md)  
[Disponibilità nazionale/regionale e lingue supportate](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations)  
[Modifica di lingua e impostazioni locali](about-locale-language.md)  
