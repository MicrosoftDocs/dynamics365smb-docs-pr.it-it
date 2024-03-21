---
title: Configurare le funzionalità di Copilot e IA
description: Questo articolo spiega come abilitare Copilot in un ambiente.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 10/29/2023
ms.custom: bap-template
ms.search.form: 7775
ms.collection:
  - bap-ai-copilot
---

# <a name="configure-copilot-and-ai-capabilities"></a>Configurare le funzionalità di Copilot e IA

<!--[!INCLUDE[ai-preview](includes/ai-preview.md)]-->

<!--This article explains how you can control the ability to create AI-powered item marketing text with Copilot for your organization. This task is done by an admin. There are two requirements that you must fulfill to make the feature available to users:-->

Questo articolo descrive come controllare Copilot e ad altre funzionalità di intelligenza artificiale in Business Central. Questa attività viene eseguita da un amministratore. Copilot è una funzionalità di sistema e parte integrante di Business Central. Come per la maggior parte delle funzionalità di sistema, non concedi l'accesso a singoli utenti né puoi attivare o disattivare Copilot. Tuttavia, Copilot offre controlli di governance dei dati e la possibilità di disattivare le singole funzionalità di Copilot e IA per ogni ambiente. Esistono diversi livelli di controllo dell'accesso alle funzionalità di IA, a seconda della funzionalità:

- Consentire lo spostamento dei dati tra aree geografiche

  Questa attività è necessaria solo se l'ambiente Business Central si trova in un'area geografica diversa rispetto a quella del servizio OpenAI di Azure. [Ulteriori informazioni](#allow-data-movement-across-geographies)

- Attiva la funzionalità nella pagina **Funzionalità di Copilot & IA**. [Ulteriori informazioni](#activate-features)

- Abilita la funzionalità specifica, se è ancora regolata da **Gestione funzionalità**.

  Nel secondo ciclo di rilascio del 2023, le funzionalità per i suggerimenti di testo di marketing e per l'assistenza per la riconciliazione dei conti correnti bancari sono entrambe incluse in **Gestione funzionalità**. [Ulteriori informazioni](#enable-feature-in-feature-management)

Se uno qualsiasi di questi requisiti non viene soddisfatto, la funzionalità non è disponibile per l'uso.

## <a name="prerequisites"></a>Prerequisiti

- Utilizzi Business Central Online, versione 23.1 o successiva. <!--[preview version](ai-preview-getstarted.md) of Business Central that's enabled for Copilot.-->
- Disponi di autorizzazioni di amministratore o super in Business Central.  <!--For more information, go to [Configure AI-powered item marketing text with Copilot](enable-ai.md).-->

## <a name="allow-data-movement-across-geographies"></a>Consentire lo spostamento di dati tra aree geografiche

Questa attività si applica solo se l'interruttore **Consenti spostamento dati** viene visualizzato accanto alla parte superiore della pagina **Funzionalità di Copilot & IA**. Se viene visualizzato il collegamento **Come è possibile gestire i propri dati di Copilot?** al posto dell'interruttore **Consenti spostamento dati**, salta questo passaggio.

![Mostra uno screenshot dell'interruttore Consenti spostamento dati nella pagina Funzionalità di Copilot e IA.](media/allow-data-movement-v2.png)

L'interruttore **Consenti spostamento dati** indica che la posizione dell'ambiente Business Central, ovvero l'area geografica in cui i dati vengono elaborati e archiviati, non è la stessa del servizio OpenAI di Azure usata da Copilot. Se vuoi abilitare Copilot, devi consentire lo spostamento dei dati tra aree geografiche. Per ulteriori informazioni sullo spostamento di dati, vedi [Spostamento dei dati di Copilot tra aree geografiche](ai-copilot-data-movement.md). 

Per consentire lo spostamento dei dati al di fuori della tua area geografica, completa i seguenti passaggi:

1. In Business Central, cerca e apri la pagina **Funzionalità di Copilot e IA**.
1. Attiva l'interruttore **Consenti spostamento dati**.

   L'opzione **Consenti spostamento dati** è attivata per impostazione predefinita per gli ambienti nelle aree di Azure dell'Europa occidentale e dell'Europa settentrionale.

Puoi rifiutare esplicitamente lo spostamento dei deati disattivando l'opzione **Consenti spostamento dati**. Una volta che un servizio OpenAI di Azure diventa disponibile nell'area geografica dell'ambiente Business Central, l'ambiente viene automaticamente connesso ad esso e l'interruttore non è più disponibile.
<!--
| Australia, United Kingdom, United States | Within the respective geographical region |
| Europe, France, Germany, Norway, Switzerland  | Sweden or Switzerland |
| Asia Pacific, Brazil, Canada, India, Japan, Singapore, South Africa, South Korea, United Arab Emirates  | United States |-->



<!--Note

If your environment is hosted in North America, Copilot will use an Azure OpenAI endpoint in North America to process your data.
If your environment is hosted in Europe, Copilot will use an Azure OpenAI endpoint in Europe to process your data.
If your environment is hosted anywhere else, Copilot will use an Azure OpenAI endpoint outside of the region in which the environment is hosted.
To opt in 

Copilot and other AI capabilities use Azure OpenAI Service.  and are provided by default to only those customers with environments that have United States as their geography for data processing and storage. While the Azure OpenAI Service is available in multiple geographies including Australia, Canada, United States, France, Japan and UK, Copilot does not follow the same regional rollout schedule.

Meanwhile, customers with environments outside the United States can use Copilot AI features by opting in to share relevant data with the Azure OpenAI Service in United States or Switzerland.

The information in the following table outlines the Azure OpenAI service that's used by the Copilot services based on the geography of their Dynamics 365 environment when they opt-in to share data.-->
## <a name="activate-features"></a>Attivare le funzionalità

Tutte le funzionalità di Copilot e IA sono attive per impostazione predefinita quando vengono rese disponibili in anteprima o diventano disponibili a livello generale. Puoi disattivare o riattivare singole funzionalità per tutti gli utenti mediante la pagina **Funzionalità di Copilot e IA**.

1. In Business Central, cerca e apri la pagina **Funzionalità di Copilot e IA**.

1. La pagina elenca tutte le funzionalità di Copilot e IA disponibili e il relativo stato corrente, che può essere Attivo o Inattivo. Le funzionalità sono divise in due sezioni: una sezione per le funzionalità in anteprima e un'altra per le funzionalità generalmente disponibili. 

   [![Gestione ruolo utente di Business Central e l'elenco di controllo per Copilot](media/copilot-and-ai-capabilties-page.svg)](media/copilot-and-ai-capabilties-page.svg#lightbox)

   - Per attivare una funzionalità, selezionala nell'elenco, quindi seleziona l'azione **Attiva**.
   - Per disattivare una funzionalità, selezionala e quindi seleziona l'azione **Disattiva**. 


## <a name="enable-feature-in-feature-management"></a>Abilitare la funzionalità in Gestione funzionalità

Quando singole funzionalità di Copilot vengono rilasciate negli aggiornamenti minori di Business Central, tali funzionalità sono facoltative fino al successivo aggiornamento principale. **Gestione funzionalità** è utilizzata per attivare o disattivare le funzionalità in anteprima, come la riconciliazione bancaria, e alcune funzionalità generalmente disponibili, come i suggerimenti di testo per il marketing. [Ulteriori informazioni su Gestione funzionalità](/dynamics365/business-central/dev-itpro/administration/feature-management).

1. In Business Central, cerca e apri la pagina **Gestione funzionalità**.
2. Per abilitare una funzionalità, imposta la colonna **Abilitata per** su **Tutti gli utenti**. Per disabilitare una funzionalità, imposta la colonna **Abilitata per** su **Nessuno**. Utilizza la tabella seguente per determinare l'interruttore che si applica alle funzionalità di Copilot e IA che intendi abilitare:

   - **Anteprima funzionalità: riconciliazione dei conti correnti bancari con Copilot** abilita la funzionalità per l'assistenza per la riconciliazione dei conti correnti bancari.
   - **Anteprima della funzionalità: crea descrizioni del prodotto basate sull'intelligenza artificiale con Copilot** abilita la funzionalità per i suggerimenti di testo di marketing.

   Per ulteriori informazioni sulla gestione delle funzionalità in generale, vai a [Gestione delle funzionalità](/dynamics365/business-central/dev-itpro/administration/feature-management).

## <a name="granting-user-access"></a>Concedere l'accesso degli utenti

Le funzionalità di Copilot e IA possono offrire funzionalità destinate a qualsiasi utente dell'organizzazione o a ruoli utente specifici. La maggior parte delle funzionalità di Copilot e IA offre il controllo dell'accesso utilizzando autorizzazioni e set di autorizzazioni nel sistema di gestione delle autorizzazioni di Business Central. [Scopri di più su autorizzazioni e insiemi di autorizzazioni](ui-define-granular-permissions.md).

Per concedere o negare l'accesso a specifiche funzionalità di Copilot e IA, consulta la documentazione o l'editore della funzionalità in questione per identificare quali autorizzazioni sono necessarie. 

## <a name="next-steps"></a>Passaggi successivi

Dopo aver abilitato e acconsentito alle funzionalità, sei pronto per provarle. Vedi:

- [Aggiungere del testo di marketing agli articoli](item-marketing-text.md) 
- [Riconciliare mediante l'assistenza per la riconciliazione dei conti correnti bancari](bank-reconciliation-with-copilot.md) 

## <a name="see-also"></a>Vedere anche

[Risoluzione dei problemi relativi alle funzionalità di Copilot e IA](ai-copilot-troubleshooting.md)  
[Panoramica dei suggerimenti di testo di marketing](ai-overview.md)   
[Domande frequenti sui suggerimenti di testo di marketing](faqs-marketing-text.md)  
