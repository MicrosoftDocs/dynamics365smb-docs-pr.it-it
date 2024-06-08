---
title: Impostare le stampanti con indirizzo e-mail
description: Descrizione pratica
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 01/26/2023
ms.custom: bap-template
---
# Impostare le stampanti con indirizzo e-mail

Questo articolo spiega come configurare le stampanti con indirizzo e-mail in [!INCLUDE[prod_short](includes/prod_short.md)]. Con queste stampanti [!INCLUDE[prod_short](includes/prod_short.md)] invia i lavori di stampa alla stampante utilizzando l'indirizzo e-mail della stampante.

> [!TIP]
> Per conoscere altre possibilità della stampante, vai a [Panoramica della gestione delle stampanti](admin-printer-setup-overview.md). 

## Prerequisiti

- [!INCLUDE[prod_short](includes/prod_short.md)] 2020 primo ciclo di rilascio o successivi
- L'estensione **Invia a stampante e-mail** è installata

    Questa estensione è installata per impostazione di default. Per ulteriori informazioni sull'installazione delle estensioni, vedi [Installazione e disinstallazione delle estensioni in Business Central](ui-extensions-install-uninstall.md).
- La funzionalità e-mail è impostata.

   Per ulteriori informazioni, vedi [Configurazione e-mail](admin-how-setup-email.md).

## Aggiungi una stampante e-mail

La pagina **Gestione stampante** mostra le stampanti attualmente configurate. La pagina ti dà anche accesso alla pagina **Impostazioni** per ciascuna stampante per modificare una configurazione esistente o configurare una nuova stampante.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Gestione stampante**, quindi scegli il collegamento correlato.
2. Seleziona **Stampa e-mail**, quindi scegli **Aggiungi una stampante e-mail**.
3. Compila i campi nella pagina **Impostazioni stampante e-mail** in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > È necessario selezionare manualmente il formato carta appropriato per una stampante poiché non è possibile memorizzare alcuna stampante locale o impostazioni dell'utente.
    >
    > Assicurati che l'estensione Stampante e-mail non sia impostata sul formato carta **A4** per impostazione predefinita, che non è adatto in Nord America, ad esempio.

## Informativa sulla privacy

Se usi l'estensione Stampante e-mail, tutti o alcuni lavori di stampa vengono inviati all'indirizzo e-mail configurato per la stampante. Si consiglia vivamente di associare un ID e-mail univoco a un dispositivo stampante utilizzando solo i servizi ufficiali forniti dal produttore dell'hardware, come HP ePrint, KonicaMinolta EveryonePrint o Epson Email Print.

Prendi tutte le precauzioni sulla privacy necessarie, assicurati che la soluzione di stampa e-mail abbia le autorizzazioni, le impostazioni sulla privacy e i criteri di conservazione configurati correttamente. È responsabilità dell'utente fornire un indirizzo e-mail corretto, verificato e operativo. Per ulteriori informazioni, vedi [Informativa sulla privacy di Microsoft](https://privacy.microsoft.com/privacystatement).

## Passaggi successivi

[Configurazione delle stampanti predefinite](ui-specify-printer-selection-reports.md)

## Vedere anche

[Panoramica della gestione delle stampanti](admin-printer-setup-overview.md)  
[Configurazione delle stampanti di Stampa universale](admin-printer-setup-universal-print.md)
[Stampa di un report](ui-work-report.md#PrintReport)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Eseguire i processi batch](ui-how-run-batch-jobs.md)  
