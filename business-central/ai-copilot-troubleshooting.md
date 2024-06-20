---
title: Risoluzione dei problemi relativi alle funzionalità di Copilot e IA
description: Scopri come risolvere problemi comuni che potrebbero verificarsi durante l'utilizzo delle funzionalità di Copilot e di IA in Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: troubleshooting
ms.collection:
  - bap-ai-copilot
ms.date: 02/01/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="troubleshoot-copilot-and-ai-capabilities"></a>Risoluzione dei problemi relativi alle funzionalità di Copilot e IA

Copilot è una funzionalità basata sull'intelligenza artificiale in Business Central che assiste in varie attività come la stesura di testi di marketing e la riconciliazione di conti correnti bancari. In caso di problemi con funzionalità di Copilot o IA, questo articolo può aiutarti a identificare e risolvere problemi comuni.

## <a name="copilot-doesnt-appear-on-pages"></a>Copilot non appare nelle pagine

Se la funzionalità Copilot, come l'azione **Bozza con Copilot** per suggerimenti di testo di marketing o l'azione **Riconcilia con Copilot** per l'assistenza per la riconciliazione dei conti correnti bancari non viene visualizzata in una pagina come previsto, verifica quanto segue:

- Se la funzionalità è controllata in Gestione funzionalità, assicurati che sia abilitata. [Ulteriori informazioni su Gestione funzionalità](admin-feature-management.md).

- Assicurati che la funzionalità non sia nascosta dalla personalizzazione. [Scopri di più sulla personalizzazione](ui-personalization-user.md)

## <a name="copilot-appears-on-pages-but-you-get-an-error-that-its-not-activated"></a>Copilot appare nelle pagine, ma viene visualizzato un messaggio errore che indica che non è attivato

Se provi a utilizzare Copilot e viene visualizzato un errore simile a **Copilot non è attivato per \[funzionalità\]**, devi controllare un paio di cose:

- Innanzitutto, assicurati che la funzionalità sia attivata nella pagina **Funzionalità di Copilot e IA**. [Scopri di più sull'attivazione delle funzionalità di Copilot e IA](enable-ai.md#activate-features). 
- Successivamente, assicurati che l'informativa sulla privacy per l'integrazione di Azure OpenAI non sia impostata su **Non accetto per tutti**. Se lo è, impostala su **Accetto per tutti**. [Scopri di più sulle informative sulla privacy](privacy-notices-status.md).

## <a name="copilot-capabilities-from-microsoft-not-listed-on-copilot--ai-capabilities-page"></a>Funzionalità di Copilot di Microsoft non elencate nella pagina Copilot e funzionalità IA

Se nessuna delle funzionalità AI di Microsoft è mostrata nella pagina **Copilot e funzionalità IA**, è probabile che tu abbia una o più app incorporate installate nel tuo ambiente. Le app incorporate possono offrire le proprie funzionalità Copilot, ma le funzionalità pubblicate da Microsoft non sono compatibili con gli ambienti che dispongono di app incorporate.

## <a name="see-also"></a>Vedere anche

[Configurare le funzionalità di Copilot e IA](enable-ai.md)  
[Suggerimenti di testo di marketing con Copilot](ai-overview.md)  
[Riconciliare i conti correnti bancari con Copilot](bank-reconciliation-with-copilot.md)  
