---
title: Gestisci le impostazioni e le preferenze dell'utente come amministratore
description: Gestire le impostazioni e le preferenze dell'utente in Dynamics 365 Business Central.
author: sorenfriisalexandersen
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.search.keywords: 'user settings, preferences, language, region, time zone, regional settings'
ms.search.form: '9204,'
ms.date: 04/01/2021
ms.author: soalex
---
# Gestire le impostazioni e le preferenze dell'utente

Come amministratore, è possibile configurare le impostazioni dell'utente in [!INCLUDE[prod_short](includes/prod_short.md)], in modo simile a come i singoli utenti possono gestire le proprie preferenze nella pagina **Impostazioni personali**.  

Ottieni una panoramica di tutti gli utenti nell'elenco **Utenti** e modifica le singole impostazioni scegliendo l'azione **Impostazioni utente** per l'utente pertinente.

> [!TIP]
> L'elenco **Impostazioni utente** mostra le impostazioni correnti per ogni utente. Per visualizzare o modificare singoli utenti, scegli l'azione **Visualizza** o **Modifica**.

La pagina **Scheda Impostazioni utente** è simile alla pagina **Le mie impostazioni** a cui ogni utente ha accesso ed è un potente strumento per te come amministratore per l'impostazione delle impostazioni predefinite e la cancellazione delle pagine personalizzate, ad esempio.  

## Tipi di impostazioni utente

Le *impostazioni utente* non sono il *setup dell'utente*, che riguarda l'utente come entità e l'accesso dell'utente nel sistema. Inoltre, le impostazioni dell'utente non hanno nulla a che fare con la personalizzazione di un utente, come lievi modifiche all'interfaccia utente. Le impostazioni dell'utente determinano le impostazioni predefinite per ciascun utente in vari aspetti del modo in cui l'applicazione si presenta all'utente. Il paragrafo seguente elenca i cinque tipi di impostazioni e preferenze dell'utente che possono essere impostate dall'utente o centralmente dall'amministratore:

* **Società**  

  Questa impostazione determina la società a cui accedere al successivo accesso. Un utente può avere accesso a più società e può essere attivo in diverse società.

* **Ruolo**  

  Il ruolo o il profilo descrive la funzione dell'utente nella società, come ad esempio *Direttore vendite*, *Addetto contabile* o *Addetto acquisti*. Il profilo determina quindi la gestione ruolo dell'utente, la home page che gli utenti vedranno quando effettuano l'accesso. Il profilo non influisce sui diritti di accesso alla funzionalità in [!INCLUDE[prod_short](includes/prod_short.md)].  

* **Lingua**  

  Definisce la lingua dell'applicazione che [!INCLUDE[prod_short](includes/prod_short.md)] usa per presentare testo, didascalie e messaggi di errore. Se gli utenti [!INCLUDE[prod_short](includes/prod_short.md)] sono sincronizzati da Microsoft 365 vengono utilizzate le impostazioni della lingua di Microsoft 365, presupponendo che l'utente desideri utilizzare le stesse impostazioni nei prodotti Office e [!INCLUDE[prod_short](includes/prod_short.md)]. L'amministratore può modificare l'impostazione predefinita e ogni utente può scegliere tra le lingue disponibili nella pagina Le mie impostazioni. Ma verranno reimpostati al valore di Microsoft 365 una volta eseguita la successiva sincronizzazione.

  Se l'impostazione della lingua di Microsoft 365 corrisponde a una lingua supportata in [!INCLUDE[prod_short](includes/prod_short.md)], questa lingua verrà scelta per l'utente.  

  > [!NOTE]
  > Potrebbe essere necessario installare un'app di lingua per [!INCLUDE[prod_short](includes/prod_short.md)] per visualizzare correttamente la lingua. Pertanto, è buona norma installare le app di lingua necessarie prima che qualsiasi utente acceda per la prima volta in modo che abbiano una buona esperienza fin dal primo giorno. Per ulteriori informazioni, consultare l'elenco delle [lingue supportate](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations).  
  
* **Area geografica**  

  Definisce come le date e i numeri sono presentati nel client [!INCLUDE[prod_short](includes/prod_short.md)], ad esempio se utilizzare i formati di data europei o americani o come visualizzare il segno decimale e i separatori delle migliaia negli importi. Se gli utenti [!INCLUDE[prod_short](includes/prod_short.md)] sono sincronizzati da Microsoft 365 vengono utilizzate le impostazioni regionali da Microsoft 365, presupponendo che l'utente desideri utilizzare le stesse impostazioni nei prodotti Office e [!INCLUDE[prod_short](includes/prod_short.md)]. Un amministratore o un utente può modificare queste impostazioni manualmente in [!INCLUDE[prod_short](includes/prod_short.md)], ma verranno reimpostate sul valore di Microsoft 365 una volta eseguita la sincronizzazione successiva.

* **Fuso orario**  

  Definisce il fuso orario dell'utente. Attualmente questo non è sincronizzato da Microsoft 365 e deve essere impostato manualmente.  

* **Suggerimenti didattici**

  [!INCLUDE [ua-teachingtips](includes/ua-teachingtips.md)] In qualità di amministratore, puoi disattivare i suggerimenti di insegnamento per tutti gli utenti, ad esempio se stai eseguendo l'onboarding di utenti che hanno già familiarità con [!INCLUDE [prod_short](includes/prod_short.md)].  

> [!NOTE]
> Se la sincronizzazione degli utenti di Microsoft 365 viene effettuata mentre gli utenti sono connessi a [!INCLUDE[prod_short](includes/prod_short.md)], questi utenti devono aggiornare il browser o disconnettersi e accedere nuovamente a [!INCLUDE[prod_short](includes/prod_short.md)] per vedere una potenziale lingua diversa impostata dall'azione di sincronizzazione.

## Panoramica di tutte le modifiche specifiche dell'utente

In qualità di amministratore, puoi ottenere una panoramica delle singole modifiche a [!INCLUDE [prod_short](includes/prod_short.md)] che ogni utente potrebbe aver apportato in varie pagine in [!INCLUDE [prod_short](includes/prod_short.md)]. Man mano che gli utenti apportano modifiche alla loro esperienza in [!INCLUDE [prod_short](includes/prod_short.md)], tali modifiche verranno riflesse nell'elenco **Personalizzazioni utente**. <!--Administrators can also set these settings for users before they log in the first time, so users do not have to do it themselves, providing them a better *getting started* experience.-->

<!-- >[!NOTE]
> User personalizations do not have anything to do with the *personal* lightweight changes a user can make to the user experience.-->

## Per rivedere o eliminare le personalizzazioni degli utenti

1. Scegli l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Icona Cerca pagina o report") immetti **Pagine personalizzate**, quindi scegli il collegamento correlato.
2. Viene visualizzato l'elenco degli utenti e le loro pagine personalizzate. Per cancellare la personalizzazione di un utente, fai clic sulla riga pertinente o scegli **Gestisci**, quindi scegli **Elimina**.

Ciò elimina la personalizzazione e l'esperienza dell'utente della pagina pertinente torna allo stato predefinito.

## Vedere anche

[Preparazione al business](ui-get-ready-business.md)  
[Disponibilità nazionale/regionale e lingue supportate](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations)  
[Modifica di lingua e impostazioni locali](about-locale-language.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
