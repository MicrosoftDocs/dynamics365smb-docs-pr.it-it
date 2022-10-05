---
title: Workflow in Dynamics 365 Business Central
description: Usa le funzionalità di flusso di lavoro integrate per impostare flussi di lavoro di approvazione per integrare i flussi di lavoro automatizzati basati su Power Automate. È possibile impostare passaggi per assegnare attività a persone diverse nell'ambito delle diverse attività dei processi aziendali.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 09/13/2022
ms.author: edupont
ms.openlocfilehash: ecaaf9bbb56e1c1b47f9f617319b32f32a2920fd
ms.sourcegitcommit: 9049f75c86dea374e5bfe297304caa32f579f6e4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/23/2022
ms.locfileid: "9585623"
---
# <a name="workflows-in-dynamics-365-business-central"></a>Workflow in Dynamics 365 Business Central

È possibile impostare e utilizzare i flussi di lavoro che collegano task di processi aziendali eseguiti da utenti diversi. I task di sistema, ad esempio la registrazione automatica, possono essere inclusi come passaggi nei flussi di lavoro e preceduti o seguiti da task degli utenti. La richiesta e la concessione dell'approvazione per creare nuovi record sono passaggi tipici del flusso di lavoro.

La versione predefinita di [!INCLUDE [prod_short](includes/prod_short.md)] supporta tre tipi di flussi di lavoro:

* Flussi di lavoro di approvazione basati su modelli di flusso di lavoro integrati

  Nella pagina **Modelli di flusso di lavoro**, puoi vedere tutti i flussi di lavoro disponibili. La versione di valutazione di [!INCLUDE[prod_short](includes/prod_short.md)] include molti workflow preconfigurati, rappresentati da modelli di workflow che si possono copiare per crearne di nuovi. Quando apri un modello dalla pagina **Modelli di flusso di lavoro** e il nome del flusso di lavoro inizia con *MS-*, il modello viene aggiunto da Microsoft.
  
* Flussi di Power Automate che hai impostato tu stesso

  Qualsiasi modello di workflow creato con Microsoft Power Automate viene aggiunto all'elenco dei modelli di workflow in [!INCLUDE[prod_short](includes/prod_short.md)]. Ulteriori informazioni in [Utilizza [!INCLUDE[prod_short](includes/prod_short.md)] in Flussi di Power Automate](across-how-use-financials-data-source-flow.md). 
  
* Flussi istantanei attivati manualmente dall'azione **Automatizza** (solo [!INCLUDE [prod_short](includes/prod_short.md)] online).

  Creare e attivare manualmente un flusso di Power Automate su un record [!INCLUDE[prod_short](includes/prod_short.md)], come un cliente, un articolo o un ordine di vendita, con opzioni per manipolare le informazioni sia internamente che esternamente (utilizzando strumenti integrati). Ulteriori informazioni nella sezione [Flussi istantanei](across-how-use-financials-data-source-flow.md#instant-flows).

## <a name="power-automate-flows"></a>Flussi di Power Automate

Usando [!INCLUDE [prod_short](includes/prod_short.md)] online, puoi iscriverti a Power Automate per creare potenti flussi di lavoro automatizzati. Puoi eseguire quei flussi di lavoro da [!INCLUDE [prod_short](includes/prod_short.md)], collegando fonti interne ed esterne di dati e strumenti, senza conoscenze di codifica.

I flussi Power Automate possono essere attivati da eventi (come creazione, modifica o eliminazione di record o documenti) ed essere eseguiti in base a una pianificazione definita dall'utente o su richiesta (nota come **Flusso istantaneo**).

## <a name="approval-workflows"></a>Workflow di approvazione

Puoi creare un flusso di lavoro di approvazione elencando le fasi interessate nelle righe. Ogni fase consiste in un evento del workflow, moderato dalle condizioni di evento, e in una risposta del workflow, moderata dalle opzioni di risposta. È possibile definire le fasi del flusso di lavoro compilando i campi delle righe del flusso di lavoro in base a elenchi fissi di valori di evento e di risposta che rappresentano gli scenari supportati dal codice dell'applicazione.<!--What are the "values"? Can we give an example?-->

Esempi di eventi dei workflow di approvazione includono, tra l'altro, la creazione di ordini/preventivi/fatture di vendita o acquisto, modifiche dei prezzi e modifiche del fornitore o del cliente.

[!INCLUDE[workflow](includes/workflow.md)]

| **Per** | **Vedere** |
|--|--|
| Imposta gli utenti del workflow di approvazione, specifica la modalità di notifica per gli utenti e crea nuovi flussi di lavoro. Per creare i nuovi flussi di lavoro per gli scenari non sostenuti, implementare gli elementi necessari del flusso di lavoro personalizzando il codice dell'applicazione. | [Configurare i flussi di lavoro di approvazione](across-set-up-workflows.md) |
| Abilita i workflow di approvazione, intervieni sulle relative notifiche, incluse le richieste e le approvazioni di una fase del workflow. Archiviare ed eliminare i flussi di lavoro. | [Utilizzare i workflow di approvazione](across-use-workflows.md) |
| Integra i dati aziendali con flussi di lavoro di Power Automate, utilizzando fonti ed eventi interni ed esterni per creare e automatizzare attività o flussi di lavoro. | [Utilizzare i flussi Power Automate in [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-financials-data-source-flow.md) |

## <a name="see-related-microsoft-training"></a>Vedi il relativo [training Microsoft](/training/modules/create-workflows/)

## <a name="see-also"></a>Vedere anche

[Vendite](sales-manage-sales.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Gestione di progetti](projects-manage-projects.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Risolvere i problemi dei flussi di lavoro automatizzati di [!INCLUDE[prod_short](includes/prod_short.md)]](across-flow-troubleshoot.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
