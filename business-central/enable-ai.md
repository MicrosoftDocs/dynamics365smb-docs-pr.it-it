---
title: Configurare un testo di marketing dell'articolo basato su intelligenza artificiale (anteprima) con Copilot
description: Questo articolo spiega come ottenere una versione di valutazione di Copilot di Business Central e abilitare Copilot in un ambiente.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 03/22/2023
ms.custom: bap-template
---

# <a name="configure-ai-powered-item-marketing-text-preview-with-copilot"></a><a name="configure-ai-powered-item-marketing-text-preview-with-copilot"></a><a name="configure-ai-powered-item-marketing-text-preview-with-copilot"></a>Configurare un testo di marketing dell'articolo basato su intelligenza artificiale (anteprima) con Copilot

[!INCLUDE[ai-preview](includes/ai-preview.md)]

Questo articolo spiega come puoi controllare la possibilità di creare un testo di marketing basato sull'intelligenza artificiale con Copilot per la tua organizzazione. Questa operazione viene eseguita da un amministratore. Ci sono due requisiti che devi soddisfare per rendere la funzione disponibile per gli utenti:

- Abilita la funzionalità **Crea descrizioni del prodotto basate sull'intelligenza artificiale con Copilot**.
- Accetta le condizioni dell'[anteprima](https://dynamics.microsoft.com/legaldocs/supp-dynamics365-preview/) e dell'[Informativa sulla privacy di Microsoft](https://go.microsoft.com/fwlink/?LinkId=521839) per conto dell'organizzazione.

Se uno di questi requisiti non viene soddisfatto, la funzione non sarà disponibile per l'uso.

## <a name="prerequisites"></a><a name="prerequisites"></a><a name="prerequisites"></a>Prerequisiti

Stai utilizzando una [versione di anteprima](ai-preview-getstarted.md) di Business Central abilitata per Copilot. L'abilitazione di Copilot viene eseguita da un amministratore. Per ulteriori informazioni, vai a [Configurare il testo di marketing degli articoli basato sull'intelligenza artificiale con Copilot](enable-ai.md).

## <a name="enable-or-disable-create-ai-powered-product-descriptions-with-copilot"></a><a name="enable-or-disable-create-ai-powered-product-descriptions-with-copilot"></a><a name="enable-or-disable-create-ai-powered-product-descriptions-with-copilot"></a>Abilita o disabilita Crea descrizioni del prodotto basate sull'intelligenza artificiale con Copilot

1. In Business Central, cerca e apri la pagina **Gestione funzionalità**.
2. Imposta la colonna **Abilitato per** di **Anteprima della funzionalità: crea descrizioni del prodotto basate sull'intelligenza artificiale con Copilot** su **Tutti gli utenti** per abilitare la funzione o su **Nessuno** per disabilitarla.

   Per ulteriori informazioni sulla gestione delle funzionalità in generale, vai a [Gestione delle funzionalità](/dynamics365/business-central/dev-itpro/administration/feature-management).

## <a name="consent-to-or-reject-preview-and-privacy-terms-and-conditions-for-all-users"></a><a name="consent-to-or-reject-preview-and-privacy-terms-and-conditions-for-all-users"></a><a name="consent-to-or-reject-preview-and-privacy-terms-and-conditions-for-all-users"></a>Accettare o rifiutare l'anteprima e le condizioni sulla privacy per tutti gli utenti

1. In Business Central, cerca e apri la pagina **Stato avvisi sulla privacy**.
2. Nella colonna **Nome integrazione** seleziona **Azure OpenAI**, quindi leggi le condizioni che vengono presentati.
3. Nella riga **Azure OpenAI** seleziona la casella di controllo **Accetto per tutti** per consentire o la casella di spunta **Non sono d'accordo per tutti** per rifiutare.

## <a name="next-steps"></a><a name="next-steps"></a><a name="next-steps"></a>Passaggi successivi

Dopo aver abilitato e acconsentito alla funzione, si è pronti per provare Copilot sugli articoli in Business Central. Vai ad [Aggiungere del testo di marketing agli articoli](item-marketing-text.md).  

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Vedere anche

[Panoramica del testo di marketing dell'articolo basato su intelligenza artificiale con Copilot](ai-overview.md)  
[Creare un testo di marketing per gli articoli utilizzando Copilot](item-marketing-text.md)  
[Domande frequenti sul testo di marketing per l'articolo basato sull'intelligenza artificiale con Copilot](ai-faq.md)  
