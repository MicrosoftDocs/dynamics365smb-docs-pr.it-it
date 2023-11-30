---
title: Spostamento dei dati di Copilot tra aree geografiche
description: Scopri come i dati utilizzati nelle funzionalità copilota in Dynamics 365 Business Central vengono spostati tra aree geografiche in cui il servizio OpenAI di Azure non è disponibile per impostazione predefinita.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: conceptual
ms.collection: null
ms.date: 11/15/2023
ms.custom: bap-template
---

# <a name="copilot-data-movement-across-geographies"></a>Spostamento dei dati di Copilot tra aree geografiche

Copilot è disponibile in tutte le [aree geografiche/paesi di Business Central](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations) supportati. Tuttavia, Copilot utilizza il servizio OpenAI di Microsoft Azure, attualmente disponibile per Business Central solo in alcune aree geografiche, ovvero Stati Uniti e Svizzera. Ciò significa che se il tuo ambiente si trova altrove, i dati delle funzionalità di Copilot e dell'IA generativa devono essere trasmessi al di fuori della tua area geografica e potrebbero essere elaborati e archiviati al di fuori dei limiti di conformità. I dati includono le richieste di IA e i dati aziendali utilizzati o generati da Copilot. In questo caso, devi fornire il consenso esplicito per spostare i dati in un servizio OpenAI di Azure in un'altra area geografica. <!--For a list of geographies, refer to the [Azure OpenAI Service geographies](#azure-openai-service-geographies) section that follows.-->

> [!IMPORTANT]
> Se il tuo ambiente si trova nella stessa area geografica Azure del servizio OpenAI di Azure, si connette automaticamente al servizio OpenAI di Azure. Non è necessaria alcuna opzione e configurazione. 

> [!NOTE]
> Singole funzionalità di Copilot e dell'IA generativa potrebbero non essere disponibili in tutte le aree geografiche/paesi dell'ambiente Business Central. Consulta l'editore di ogni funzionalità per informazioni sulla disponibilità.
> 
> Ogni funzionalità di Copilot e dell'intelligenza artificiale generativa di editori non Microsoft, come quelle originate da personalizzazioni o app AppSource installate, definisce le proprie aree geografiche specifiche del servizio OpenAI di Azure. Consulta l'editore dell'estensione per sapere quali servizi regionali di Azure sono usati dall'estensione. 

### <a name="azure-openai-service-geographies"></a>Aree geografiche del servizio OpenAI di Azure

La tabella seguente mostra le aree geografiche del servizio OpenAI di Azure usate da Copilot, in base all'area geografica di un ambiente Business Central. Queste informazioni sono importanti quando si decide se acconsentire esplicitamente o meno allo spostamento dei dati tra aree geografiche. Puoi identificare l'area geografica di Azure per il tuo ambiente nell'interfaccia di amministrazione di Business Central, (vedi [Gestione di ambienti nell'interfaccia di amministrazione](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)).

| Area geografica di Azure per l'ambiente| Area geografica del servizio OpenAI di Azure|Azione amministrativa necessaria per sbloccare Copilot| 
| - | - | - |
|Asia (orientale, sud-orientale) |Stati Uniti|Sì|
|Australia (sud-orientale)| Stati Uniti |Sì, fino all'aggiornamento 23.2 |
|Brasile (meridionale) |Stati Uniti|Sì|
|Canada (centrale, orientale)|Stati Uniti|Sì|
|Europa (occidentale, settentrionale)| Svezia o Svizzera |Sì|
|Francia (centrale, meridionale)| Svezia o Svizzera |Sì|
|Germania (settentrionale, centro-occidentale)| Svezia o Svizzera |Sì|
|India (centrale, meridionale)|Stati Uniti|Sì|
|Giappone (orientale, occidentale)|Stati Uniti|Sì|
|Corea del Sud (centrale, meridionale)|Stati Uniti|Sì|
|Norvegia (orientale, occidentale)|Svezia o Svizzera |Sì|
|Sudafrica (settentrionale, occidentale)|Stati Uniti|Sì|
|Svizzera (settentrionale, occidentale) |Svezia o Svizzera |Sì|
|Emirati Arabi Uniti (settentrionali, occidentali)|Stati Uniti|Sì|
|Regno Unito (meridionale, occidentale)|Regno Unito|Sì, fino all'aggiornamento 23.2|
|Stati Uniti (centrali, orientali, centro-settentrionali, centro-meridionali, occidentali) |Stati Uniti|No|

> [!NOTE]
> Quando il servizio OpenAI di Azure diventa disponibile nell'area geografica di Business Central, il tuo ambiente inizierà a usare automaticamente il servizio OpenAI di Azure e il consenso esplicito non sarà più necessario e nemmeno possibile.  
<!--

BC geos base on https://dynamics.microsoft.com/en-us/availability-reports/georeport/
case "AUSTRALIAEAST":
            case "AUSTRALIASOUTHEAST":
                return new CapiRegion("au", 2);
            case "BRAZILSOUTH":
                return new CapiRegion("br", 2);
            case "CANADACENTRAL":
            case "CANADAEAST":
                return new CapiRegion("ca", 2);
            case "CENTRALINDIA":
            case "SOUTHINDIA":
                return new CapiRegion("in", 1);
            case "EASTASIA":
                return new CapiRegion("as", 2);
            case "EASTUS":
            case "EASTUS2":
            case "SOUTHCENTRALUS":
            case "CENTRALUS":
            case "NORTHCENTRALUS":
            case "WESTUS":
            case "US":
                return new CapiRegion("us", 9, HasGpt4InGeo: true, HasTurboInGeo: true);
            case "FRANCECENTRAL":
            case "FRANCESOUTH":
                return new CapiRegion("fr", 1);
            case "GERMANYNORTH":
            case "GERMANYWESTCENTRAL":
                return new CapiRegion("de", 1);
            case "JAPANEAST":
            case "JAPANWEST":
                return new CapiRegion("jp", 1);
            case "KOREACENTRAL":
            case "KOREASOUTH":
                return new CapiRegion("kr", 1);
            case "NORWAYEAST":
            case "NORWAYWEST":
                return new CapiRegion("no", 1);
            case "SOUTHAFRICANORTH":
            case "SOUTHWESTAFRICA":
                return new CapiRegion("za", 1);
            case "SOUTHEASTASIA":
                return new CapiRegion("sg", 1);
            case "SWITZERLANDNORTH":
            case "SWITZERLANDWEST":
                return new CapiRegion("ch", 1, HasTurboInGeo: true);
            case "UKSOUTH":
            case "UKWEST":
                return new CapiRegion("uk", 2);
            case "NORTHEUROPE":
            case "WESTEUROPE":
                return new CapiRegion("eu", 10);
            case "UAENORTH":
            case "UAECENTRAL":
                return new CapiRegion("ae", 1);

-->

## <a name="next-steps"></a>Passaggi successivi

Il consenso esplicito allo spostamento dei dati tra aree geografiche viene fornito nella pagina [Funzionalità di Copilot e IA](https://businesscentral.dynamics.com/?page=7775). Per ulteriori informazioni, vedi [Consentire lo spostamento di dati tra aree geografiche](enable-ai.md#allow-data-movement-across-geographies).
