---
title: Panoramica della configurazione e della gestione delle stampanti
description: Scopri quali sono le diverse opportunità di stampa in Business Central
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics-365-business-central
ms.topic: overview
ms.date: 09/28/2023
ms.custom: bap-template
---

# Panoramica della configurazione e della gestione delle stampanti

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

La stampa di documenti e report da [!INCLUDE[prod_short](includes/prod_short.md)] è un compito importante per gli utenti aziendali. Gli utenti vogliono in genere inviare i lavori di stampa direttamente a una delle stampanti dell'organizzazione, indipendentemente dal client o dall'app [!INCLUDE[prod_short](includes/prod_short.md)] che stanno utilizzando. Poiché [!INCLUDE[prod_short](includes/prod_short.md)] online è un servizio cloud, non può raggiungere direttamente le stampanti locali collegate ai dispositivi degli utenti, ma puoi connetterlo a stampanti abilitate per il cloud.

## Quali sono le possibilità per la stampante in Business Central?

Per supportare le tue esigenze di stampa, [!INCLUDE[prod_short](includes/prod_short.md)] offre le seguenti caratteristiche:

|Funzionalità|Descrizione|Client Web| App per dispositivi mobili|App per Teams|
|-------|-----------|----------|-----------|--------------|
|Stampa universale|Stampa universale è una soluzione di gestione della stampante disponibile come servizio cloud di Microsoft. Con questa funzione, puoi configurare le tue stampanti in Stampa universale, quindi registrarle per l'uso in [!INCLUDE[prod_short](includes/prod_short.md)]. Questa funzione richiede un abbonamento a Stampa universale e l'estensione **Integrazione di Stampa universale**.|![disponibile online.](media/check.png)|![disponibile online.](media/check.png)|![funziona online](media/check.png)|
|Stampa con indirizzo e-mail|Questa funzione consente di configurare stampanti abilitate per la posta elettronica. [!INCLUDE[prod_short](includes/prod_short.md)] quindi invia i lavori di stampa a una stampante utilizzando l'indirizzo e-mail della stampante. Questa funzione richiede stampanti abilitate per la posta elettronica e l'estensione **Invia a stampante e-mail**.|![disponibile online.](media/check.png)|![funziona online](media/check.png)|![funziona online](media/check.png)|
|Stampa tramite browser|I lavori di stampa sono gestiti dalla funzionalità di stampa del browser dell'utente. Se una stampante cloud non è installata e configurata, o se una stampante installata non funziona, la stampa imposterà automaticamente le opzioni di stampa per il browser. Il campo **Stampante** verrà visualizzato nella pagina di richiesta del report *(Gestita dal browser)*.|![funziona online](media/check.png)|||

La maggior parte del lavoro per l'impostazione delle stampanti può essere eseguita dalla pagina **Gestione stampanti** in [!INCLUDE[prod_short](includes/prod_short.md)]. Sebbene con le stampanti di Stampa universale potresti anche dover lavorare nell'interfaccia di amministrazione di Microsoft 365 o nel portale di Azure.

> [!IMPORTANT]
> Per Business Central locale, Stampa universale e Stampa e-mail richiedono l'utilizzo dell'autenticazione Microsoft Entra ID o NavUserPassword.

## Estensioni di stampante personalizzate

[!INCLUDE[prod_short](includes/prod_short.md)] supporta altre estensioni stampante personalizzate che aggiungono ancora più funzioni di stampa. Pertanto, se sono installate estensioni della stampante personalizzate, la tua applicazione potrebbe includere funzionalità di stampa non descritte in questo articolo.

Se sei uno sviluppatore AL e vuoi sapere come creare estensioni per stampanti, vai a [Sviluppo di estensioni per stampanti in Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-reports-printing).

## Passaggi successivi

- [Impostare le stampanti di Stampa universale](admin-printer-setup-universal-print.md)  
- [Impostare le stampanti con indirizzo e-mail](admin-printer-setup-email.md)  
- [Configurazione delle stampanti predefinite](ui-specify-printer-selection-reports.md)