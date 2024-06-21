---
title: Impostazione del browser
description: Descrizione su come configurare i browser per utilizzare Business Central e i prodotti che include.
author: jswymer
ms.topic: get-started
ms.devlang: al
ms.search.keywords: 'Teams, web client, troubleshooting, errors'
ms.date: 12/04/2023
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---
# <a name="setting-up-and-troubleshooting-your-browser-to-work-with-business-central-web-client"></a>Configurazione e risoluzione dei problemi relativi al browser per utilizzare il client Web Business Central

In questo articolo viene descritto come configurare il browser di modo che [!INCLUDE[web_client](includes/web_client.md)] e tutte le relative funzionalità funzionino correttamente. Leggi questo articolo se hai problemi ad aprire [!INCLUDE[web_client](includes/web_client.md)], le impostazioni del tuo browser possono essere la causa di alcuni problemi.

L'articolo fornisce dettagli per la configurazione di Microsoft Edge, ma i requisiti per JavaScript, cookie e popup sono gli stessi per tutti i browser supportati. Per altri browser, fai riferimento alle istruzioni fornite dal produttore.  

## <a name="use-a-supported-browser"></a>Utilizzare un browser supportato

Assicurati di utilizzare uno dei browser supportati. Vedi [Requisiti minimi per l'utilizzo di Business Central](product-requirements.md#browsers).

Ti consigliamo di utilizzare una versione del canale stabile di un browser Web poiché è la versione più affidabile e stabile che è stata sottoposta a test approfonditi e correzione di bug. Ciò ti garantisce la migliore esperienza e avrai meno probabilità di riscontrare problemi durante l'utilizzo del client Web.  

## <a name="allow-javascript-from-business-central"></a>Consentire JavaScript in Business Central

*Problema:*

Se il browser non consente JavaScript, vedi **NotSupported/DisabledJavaScript** nella barra degli indirizzi e un messaggio **Errore HTTP 404.0 - Non trovato** quando tenti di aprire [!INCLUDE[prod_short](includes/prod_short.md)] e la 

<!-- http://localhost:8080/NotSupported/DisabledJavaScript HTTP Error 404.0 - Not Found
The resource you are looking for has been removed, had its name changed, or is temporarily unavailable. -->

*Correzione:*

1. In Microsoft Edge, vai a **Impostazioni** > **Cookie e autorizzazioni sito** > **JavaScript**.
2. Effettua uno dei seguenti passaggi. Scegli il passaggio consigliato dall'organizzazione:

    - Sposta l'interruttore **Consentito** a sinistra (Off). Quindi seleziona **Aggiungi** e digita l'indirizzo (URL) per [!INCLUDE[prod_short](includes/prod_short.md)] nella casella **Sito**. Al termine, seleziona **Aggiungi**.
    - Sposta l'interruttore **Consentito** a destra (On).

## <a name="allow-cookies-from-business-central"></a>Consentire i cookie in Business Central

*Problema:*

Se il browser non consente i cookie, verrà visualizzato il seguente errore:

**Impossibile trovare la pagina. Verificare l'indirizzo e riprovare.** 

*Correzione:*

1. In Microsoft Edge, vai a **Impostazioni** > **Cookie e autorizzazioni del sito** > **Cookie e dati del sito**.
2. Sposta l'interruttore **Consenti ai siti di salvare e leggere i dati dei cookie** a destra (On).  

## <a name="allow-pop-ups-from-business-central"></a><a name="popup"></a>Consentire popup in Business Central

[!INCLUDE[prod_short](includes/prod_short.md)] si integra con diversi prodotti. In alcuni casi, come con Microsoft Teams, vengono visualizzati [!INCLUDE[prod_short](includes/prod_short.md)] o "popup", nel prodotto. Per questa funzionalità il browser deve consentire i popup in [!INCLUDE[prod_short](includes/prod_short.md)].

*Problema:*

Se i popup per [!INCLUDE[prod_short](includes/prod_short.md)] sono bloccati, viene visualizzato un messaggio simile al seguente:

**Si è verificato un errore. Il browser potrebbe bloccare i popup necessari per Business Central.**

<!--
Something went wrong
Your browser may be blocking pop-ups needed by Business Central.

Change your browser settings to allow pop-ups or allow this for trusted domains, then try again.
If these settings are managed for your organization, you should contact your administrator for assistance.

Try again
-->
*Correzione:*

1. In Microsoft Edge, vai a **Impostazioni** > **Cookie e autorizzazioni del sito** > **Popup e reindirizzamenti**.
2. Sposta l'interruttore **Bloccato** a destra (On).
3. Seleziona **Aggiungi**. Nella casella **Sito**, digita `https://businesscentral.dynamics.com`, quindi seleziona **Aggiungi**.

## <a name="see-also"></a>Vedere anche

[Risoluzione dei problemi relativi a Teams](admin-teams-troubleshooting.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
