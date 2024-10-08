---
title: Configurazione delle funzionalità di Copilot e dell'IA
description: Questo articolo spiega come abilitare Copilot in un ambiente.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 06/28/2024
ms.custom: bap-template
ms.collection:
  - bap-ai-copilot
ms.search.form: '7771,7772_Primary,7775_Primary'
---

# <a name="configure-copilot-and-ai-capabilities"></a>Configurare le funzionalità di Copilot e IA

<!--[!INCLUDE[ai-preview](includes/ai-preview.md)]-->

<!--This article explains how you can control the ability to create AI-powered item marketing text with Copilot for your organization. This task is done by an admin. There are two requirements that you must fulfill to make the feature available to users:-->

Questo articolo descrive come controllare Microsoft Copilot e ad altre funzionalità di intelligenza artificiale in Dynamics 365 Business Central. Un amministratore deve completare queste attività.

Copilot è una funzionalità di sistema e parte integrante di Business Central. Come per la maggior parte delle funzionalità di sistema, non concedi l'accesso a singoli utenti e non puoi attivare o disattivare Copilot. Tuttavia, Copilot offre controlli di governance dei dati e la possibilità di disattivare le singole funzionalità di Copilot e IA per ogni ambiente. Esistono diversi livelli di controllo dell'accesso per le funzionalità di IA, a seconda della funzionalità:

- Consentire lo spostamento dei dati tra aree geografiche.

    Questa attività è necessaria solo se l'ambiente Business Central si trova in un'area geografica diversa rispetto a quella del servizio OpenAI di Azure che utilizza. [Ulteriori informazioni su questa attività](#allow-data-movement-across-geographies)

- Attiva la funzionalità nella pagina **Funzionalità di Copilot e IA**. [Ulteriori informazioni su questa attività](#activate-features).

<!-- For 2024 there are no AI features governed by **Feature Management**, so this section is not shown
- Enable the specific feature if it's governed by **Feature Management**.

  Check whether  of 2024 release wave 1, chat with Copilot, marketing text suggestions, and bank account reconciliation assist features are included under **Feature Management**. [Learn more](#enable-feature-in-feature-management)
<!-- 
- Enable the specific feature, if it's still governed by **Feature Management**.

  In 2023 release wave 2, both the marketing text suggestions and bank account reconciliation assist features are included under **Feature Management**. [Learn more](#enable-feature-in-feature-management)-->

Se uno qualsiasi di questi requisiti non viene soddisfatto, la funzionalità non è disponibile per l'uso.

## <a name="prerequisites"></a>Prerequisiti

- Stai utilizzando Business Central Online.
- Sei un [amministratore](#requirements-for-being-an-administrator) in Business Central.

## <a name="allow-data-movement-across-geographies"></a>Consentire lo spostamento di dati tra aree geografiche

Questa attività si applica solo se l'opzione **Consenti spostamento dati** viene visualizzata accanto alla parte superiore della pagina **Funzionalità di Copilot e IA**. Se il collegamento **Come è possibile gestire i propri dati del copilota?** viene visualizzato al posto dell'opzione **Consenti spostamento dati**, salta questa attività.

![Screenshot che mostra l'opzione Consenti spostamento dati nella pagina Funzionalità di Copilot e IA.](media/allow-data-movement-v2.png)

La presenza dell'opzione **Consenti spostamento dati** indica che la posizione dell'ambiente Business Central, ovvero l'area geografica in cui i dati vengono elaborati e archiviati, non è la stessa del servizio OpenAI di Azure usata da Copilot. Per abilitare Copilot, devi consentire lo spostamento dei dati tra aree geografiche. [Altre informazioni sullo spostamento di dati](ai-copilot-data-movement.md)

Per consentire lo spostamento dei dati al di fuori della tua area geografica, procedi come segue:

1. In Business Central, cerca e apri la pagina **Funzionalità di Copilot e IA**.
1. Attiva l'opzione **Consenti spostamento dati**.

    > [!NOTE]
    > Per gli ambienti nelle aree di Azure dell'Europa occidentale e dell'Europa settentrionale, l'opzione **Consenti spostamento dati** è attivata per impostazione predefinita.

Per rifiutare esplicitamente lo spostamento dei dati, disattiva l'opzione **Consenti spostamento dati**.

Una volta che un servizio OpenAI di Azure diventa disponibile nell'area geografica del tuo ambiente Business Central, l'ambiente viene automaticamente connesso ad esso. A quel punto, l'opzione **Consenti spostamento dati** non è più visibile nella pagina **Funzionalità di Copilot e IA**.

<!-- Don't review
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

Tutte le funzionalità di Copilot e IA sono attive per impostazione predefinita quando vengono rese disponibili in anteprima o diventano disponibili a livello generale. Nella pagina **Funzionalità di Copilot e IA** puoi disattivare o riattivare singole funzionalità per tutti gli utenti.

1. In Business Central, cerca e apri la pagina **Funzionalità di Copilot e IA**.
1. La pagina elenca tutte le funzionalità di Copilot e IA disponibili e il relativo stato corrente (lo stato può essere *Attivo* o *Inattivo*). Le funzionalità sono divise in due sezioni: una per le funzionalità in anteprima e un'altra per le funzionalità generalmente disponibili.

    - Per attivare una funzionalità, selezionala nell'elenco, quindi seleziona l'azione **Attiva**.
    - Per disattivare una funzionalità, selezionala nell'elenco e quindi seleziona **Disattiva**.

    [![Screenshot che mostra i pulsanti Attiva e Disattiva per gli elenchi di funzionalità nella pagina Funzionalità di Copilot e AI.](media/copilot-and-ai-capabilties-page.svg)](media/copilot-and-ai-capabilties-page.svg#lightbox)

<!-- don't review 

<!-- For 2024 there are no AI features governed by **Feature Management**, so this section is not shown
## <a name="enable-feature-in-feature-management"></a>Enable feature in Feature Management

When individual Copilot capabilities are released in Business Central minor updates, these capabilities are optional until the next major update. **Feature Management** is used to turn on or off features that are in preview, like bank reconciliation, and some features that are generally available, like marketing text suggestions. [Learn more about feature management](/dynamics365/business-central/dev-itpro/administration/feature-management).

1. In Business Central, search for and open the **Feature Management** page.
2. To enable a feature, set the **Enabled for** column to **All users**. To disable a feature, set the **Enabled for** column to **None**. Use the following table to help you determine the switch that applies to the Copilot and AI capability you want to enable:

   - **Feature Preview: Bank account reconciliation with Copilot** enables the bank account reconciliation assist feature.
   - **Feature Preview: Chat with Copilot** enables the chat with Copilot feature.
   - **Feature preview: Create AI-powered product descriptions with Copilot** enables the marketing text suggestions feature.

   For more information about feature management in general, go to [Feature Management](/dynamics365/business-central/dev-itpro/administration/feature-management).-->

## <a name="granting-user-access"></a>Concedere l'accesso degli utenti

Le funzionalità di Copilot e IA possono offrire funzionalità destinate a qualsiasi utente dell'organizzazione o a ruoli utente specifici. La maggior parte delle funzionalità di Copilot e IA offre il controllo dell'accesso tramite autorizzazioni e set di autorizzazioni nel sistema di gestione delle autorizzazioni di Business Central. [Scopri di più su autorizzazioni e insiemi di autorizzazioni](ui-define-granular-permissions.md).

Nella tabella seguente sono elencate le autorizzazioni necessarie per utilizzare le funzionalità di Copilot fornite da Business Central.

| Funzionalità di Copilot | Autorizzazioni richieste |
|---|---|
| Assistenza all'analisi | Il set di autorizzazioni **DATA ANALYSIS - EXEC** o l'autorizzazione di esecuzione sull'oggetto di sistema 9640 **Consenti modalità di analisi dati**. Si tratta delle stesse autorizzazioni necessarie per accedere alla modalità di analisi. |
| Assistenza per la riconciliazione dei conti correnti bancari | Autorizzazione per la pagina 7250 **Proposta IA riconciliazione conto corrente bancario** e la pagina 7252 **Proposta IA trans. a conto C/G**. |
| Chat | Non esistono autorizzazioni o set di autorizzazioni che controllano l'accesso alla chat in base all'utente. Se la chat è attivata, è disponibile per tutti gli utenti. |
| Esegui mapping documenti elettronici | Autorizzazione per la pagina 6.166 **Prop Copilot PO docum. elettr.**. |
| Suggerimenti di testo di marketing | Autorizzazione per la pagina 5836 **Testo marketing Copilot**. |
| Suggerimenti riga di vendita | Autorizzazione per la pagina 7.275 **Suggerimenti IA per la riga di vendita** e la pagina 7.276 **Suggerimenti IA riga vendita sec**. |

Per concedere o negare l'accesso a specifiche funzionalità di IA e non di Microsoft Copilot, consulta la documentazione o l'editore della documentazione delle funzionalità in questione per identificare le autorizzazioni necessarie.

## <a name="requirements-for-being-an-administrator"></a>Requisiti per essere amministratore

Devi disporre delle autorizzazioni SUPER nel tuo account utente Business Central o di una delle seguenti licenze Business Central:

- Agente amministratore delegato - Partner
- Agente Helpdesk Delegato - Partner
- Amministratore interno
- Amministratore interno BC
- Amministratore di Dynamics 365

Business Central non offre ancora autorizzazioni granulari a livello di oggetto in modo che solo amministratori specifici possano configurare Copilot.

## <a name="next-steps"></a>Passaggi successivi

Dopo aver abilitato e fornito il consenso per le funzionalità, sei pronto per provarle. Vedi i seguenti articoli:

- [Aggiungere testo di marketing agli articoli con Copilot](item-marketing-text.md)
- [Analizzare i dati degli elenchi con l'aiuto di Copilot](analysis-assist.md)
- [Chat con Copilot](chat-with-copilot.md)
- [Mappare documenti elettronici per acquistare righe di ordini di acquisto con Copilot](map-edocuments-with-copilot.md)
- [Riconciliare i conti correnti bancari con Copilot](bank-reconciliation-with-copilot.md)
- [Suggerire righe in ordini vendita con Copilot](sales-suggest-sales-lines-with-copilot.md)

## <a name="see-also"></a>Vedere anche

[Risolvere i problemi relativi alle funzionalità di Copilot e IA](ai-copilot-troubleshooting.md)  
[Domande frequenti sull'assistenza all'analisi](faqs-analysis-assist.md)  
[Domande frequenti sull'assistenza per la riconciliazione dei conti correnti bancari](faqs-bank-reconciliation.md)  
[Domande frequenti su Chat con Copilot](faqs-chat-with-copilot.md)  
[Domande frequenti sul mapping di documenti elettronici con ordini di acquisto](faqs-map-edocuments.md)  
[Domande frequenti sui suggerimenti di testo di marketing](faqs-marketing-text.md)  
[Domande frequenti per i suggerimenti della riga di vendita](faq-sales-suggest-sales-lines-with-copilot.md)  
[Panoramica dei suggerimenti di testo di marketing](ai-overview.md)
