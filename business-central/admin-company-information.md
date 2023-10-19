---
title: Panoramica delle informazioni sulla società
description: 'La pagina Informazioni sulla società specifica le informazioni di base per un''entità aziendale, come nome, indirizzi e informazioni sulla spedizione.'
author: jswymer
ms.topic: conceptual
ms.search.form: 1
ms.date: 09/24/2023
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.custom: bap-template
---

# Panoramica delle informazioni sulla società

[!INCLUDE[prod_short](includes/prod_short.md)] organizza le entità aziendali in *società*. Per ogni società, è necessario compilare alcuni dei dettagli aziendali di base e le informazioni pertinenti nella pagina **Informazioni società**. Le informazioni nella pagina [**Informazioni società**](https://businesscentral.dynamics.com/?page=1) sono usate nei documenti, come le testate delle fatture. È possibile impostare più di una società, per esempio, una società madre e una consociata.  

Se la warehouse e la sede dell'azienda hanno indirizzi differenti è possibile completare i vari campi relativi alle spedizioni e il campo **Codice ubicazione** nella Scheda dettaglio **Spedizione**. Le informazioni contenute in questi campi vengono poi stampate sugli ordini di acquisto in modo che i fornitori possano spedire le merci all'ubicazione corretta.  

Per ogni società impostata è necessario completare la pagina **Informazioni società** e la pagina **Setup contabilità generale**. Devi anche impostare ogni area in [!INCLUDE [prod_short](includes/prod_short.md)], come la pagina **Setup contabilità clienti**, per ogni società. Per ulteriori informazioni, vedi [Panoramica dei task per impostare [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md).  

La pagina **Informazioni società** contiene diversi campi e Schede dettaglio, a seconda del tuo paese/area geografica. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] La tabella seguente descrive le Schede dettaglio più comuni.

[!INCLUDE [admin-company-info-fasttabs](includes/admin-company-info-fasttabs.md)]

Una volta completata la compilazione delle informazioni puoi chiudere la pagina.  

## Lavorare con più società

Se [!INCLUDE [prod_short](includes/prod_short.md)] include più società, i tuoi utenti potrebbero voler utilizzare i *badge società* per sapere velocemente con quale azienda stanno attualmente lavorando. Per ulteriori informazioni, vedi [Visualizzare un badge società](#badge).

Ci sono alcune funzioni che puoi utilizzare per passare da una società all'altra mentre lavori, come il selettore società (<kbd>CTRL</kbd>+<kbd>O</kbd>). Per ulteriori informazioni, vedi [Passare a un'altra società o ambiente](ui-organization-switch.md).

## <a name="badge"></a>Visualizzare un badge società

Quando c'è più di una società o un ambiente, vedrai il selettore società nella parte in alto a destra della barra dell'app, vicino all'icona di ricerca nella barra dell'app. Per impostazione predefinita, il selettore società utilizza un'icona di società standard, come ![icona di avvio della società.](media/ui-experience/company-icon.png "Visualizza l'icona del selettore società utilizzata quando è presente un unico ambiente") e ![company-icon-mult-env](media/ui-experience/company-icon-multi-env.png "Visualizza l'icona del selettore società utilizzata quando sono presenti più ambienti").

:::image type="content" source="media/ui-experience/company-switch-2.png" alt-text="Mostra l'icona del selettore società nell'intestazione del client Business Central.":::  

A partire dal secondo ciclo di rilascio del 2023, versione 23, il badge società viene visualizzato nella scheda del browser quando si utilizza il client Web. È incluso anche nei collegamenti alle pagine che [copi e incolli](across-share-data-features.md#copying-a-link) negli editor di testo RTF, come Word, Outlook e Teams.
 
### Impostare il badge società

Usando la pagina **Informazioni società** puoi sostituire l'icona società standard con un badge personalizzato per la società se il badge società consente agli utenti di identificare più facilmente la società in cui lavorano.

1. Nella Scheda dettaglio **Badge società** compilare i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
2. Al termine, aggiorna il browser (seleziona <kbd>CTRL</kbd>+<kbd>F5</kbd>) per aggiornare il badge nel client.  

> [!NOTE]
> Il selettore di società è stato introdotto nel secondo ciclo di rilascio del 2022, versione 21. Nelle versioni precedenti, il badge società non viene utilizzato per cambiare società. Viene visualizzato nell'angolo in alto a destra della maggior parte delle pagine, anche quando è presente una sola società. Selezionandolo verranno visualizzati il nome completo della società e il nome dell'ambiente.

## Cambiare il nome visualizzato della società

Il nome della società viene sempre visualizzato nell'angolo in alto a sinistra e funziona come un'azione che è possibile scegliere per tornare a Gestione ruolo utente. Questo nome può essere modificato nella pagina **Informazioni società**.

1. Scegli l'icona ![Icona ingranaggio per aprire il menu Impostazioni.](media/ui-experience/settings_icon_small.png) e quindi scegli l'azione **Informazioni società**.
2. Nel campo **Nome** immettere il nuovo nome della società.
3. Chiudere la pagina. Il sistema si riavvia e visualizza la nuova società nell'angolo superiore sinistro.

## Esperienza

L'esperienza utente predefinita in una versione di prova di [!INCLUDE [prod_short](includes/prod_short.md)] non rivela tutte le capacità. Puoi attivare l'esperienza completa nella pagina **Informazioni sulla società**. Per ulteriori informazioni, vedi [Modifica delle funzionalità visualizzate](ui-experiences.md).  

## Vedere anche

[Panoramica delle attività per impostare [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Informazioni società - Inizio rapido](quick-start-company-information.md)  
[Impostazione di informazioni sulla società in Italia](LocalFunctionality/Italy/how-to-set-up-company-information.md)  
[Modificare le impostazioni di base](ui-change-basic-settings.md)  
[Modifica delle funzionalità visualizzate](ui-experiences.md)  
[Creazione di nuove società](about-new-company.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
