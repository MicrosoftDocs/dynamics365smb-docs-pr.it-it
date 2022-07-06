---
title: Utilizzare Business Central nei flussi Power Automate
description: Configurare e utilizzare flussi Power Automate che creano o modificano i dati di Business Central.
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, OData, Power App, SOAP, Entity set not found, workflowWebhookSubscriptions
ms.date: 05/12/2022
ms.author: edupont
author: jswymer
ms.openlocfilehash: f1128a9fb4e9643286e4305695e1d40719d86301
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/29/2022
ms.locfileid: "9079326"
---
# <a name="use-prod_short-in-power-automate-flows"></a>Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)] nei flussi Power Automate

È possibile utilizzare i dati di [!INCLUDE[prod_short](includes/prod_short.md)] come parte di un flusso di lavoro in Microsoft Power Automate. Crea i tuoi flussi e connettiti ai tuoi dati con il connettore [!INCLUDE [prod_short](includes/prod_short.md)].  

> [!NOTE]  
> È necessario disporre di un account valido con [!INCLUDE[prod_short](includes/prod_short.md)] e con Power Automate.  

> [!TIP]
> Oltre a Power Automate, è possibile utilizzare i modelli di flusso di lavoro di approvazione in [!INCLUDE[prod_short](includes/prod_short.md)]. Sebbene siano presenti due sistemi del flusso di lavoro, qualsiasi modello di flusso di lavoro di approvazione creato con Power Automate viene aggiunta all'elenco dei workflow in [!INCLUDE[prod_short](includes/prod_short.md)]. Per ulteriori informazioni, vedere [Flussi di lavoro](across-workflow.md).  

## <a name="automated-workflows"></a>Flussi di lavoro automatizzati

Con Power Automate, puoi creare flussi aziendali direttamente internamente e affidarti agli sviluppatori non professionisti. Per ulteriori informazioni, vedere [Configurare flussi di lavoro automatizzati](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) nel contenuto amministrativo.  

## <a name="manual-instant-flows"></a>Flussi istantanei manuali

A partire da maggio 2022, un amministratore di [!INCLUDE [prod_short](includes/prod_short.md)] online può [attivare una funzionalità ](admin-feature-management.md) per consentire l'esecuzione di un flusso Power Automate dalla maggior parte delle pagine. Per ulteriori informazioni, vedere [Configurare flussi di lavoro automatizzati](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) nel contenuto amministrativo.  

Una volta che l'amministratore ha connesso [!INCLUDE [prod_short](includes/prod_short.md)] aPower Automate, vedrai tutti i flussi che la tua organizzazione ha aggiunto quando scegli l'azione **Automatizza** nelle pagine pertinenti. Esegui i flussi senza uscire [!INCLUDE [prod_short](includes/prod_short.md)].  

Questi flussi di lavoro automatizzati si aprono in un riquadro all'interno di [!INCLUDE [prod_short](includes/prod_short.md)] online in modo da rimanere nel contesto del processo aziendale in cui eri nel mezzo. In alcune pagine, l'azione **Automatizza** si nasconde nel menu **Altre opzioni**, ma trovalo, scegli la voce di menu **Power Automate**, quindi scegli il collegamento pertinente per attivare il flusso di lavoro. La connessione a Power Automate è già configurata automaticamente.  

La maggior parte dei flussi richiede la compilazione di uno o due campi prima di scegliere l'azione **Esegui flusso**.  

> [!TIP]
> Se non vedi un'azione **Automatizza**, il tuo[!INCLUDE [prod_short](includes/prod_short.md)] non è stato ancora probabilmente impostato per l'uso Power Automate. Per ulteriori informazioni, chiedi all'amministratore.

## <a name="add-more-automated-flows-and-manual-instant-flows"></a>Aggiungere più flussi automatizzati e flussi istantanei manuali

Puoi creare flussi nel sito Web [powerautomate.microsoft.com](https://powerautomate.microsoft.com). Tuttavia, se l'amministratore ha attivato la funzionalità per l'esecuzione dei flussi Power Automate dall'interno di [!INCLUDE [prod_short](includes/prod_short.md)] online, puoi avviare il processo di creazione di un flusso dall'azione **Automatizza** nelle pagine pertinenti. In alcune pagine, l'azione **Automatizza** si nasconde nel menu **Altre opzioni**, ma trovalo, scegli la voce di menu **Power Automate**, quindi scegli l'azione **Crea un flusso**. Power Automate si apre quindi in una nuova scheda del browser e puoi accedere automaticamente.

## <a name="manage-workflows"></a>Gestire flussi di lavoro

Puoi avere una panoramica di tutti i flussi di lavoro a cui hai accesso scegliendo l'azione **Gestisci flussi di lavoro** nel menu **Power Automate**. L'elenco si apre quindi in una nuova scheda del browser e puoi accedere automaticamente Power Automate . Qui puoi vedere quando ogni flusso è stato eseguito più di recente.  

## <a name="see-related-training-at-microsoft-learn"></a>Vedi le informazioni relative al training in [Microsoft Learn](/learn/modules/use-power-automate/)

## <a name="see-also"></a>Vedere anche

[Risolvere i problemi dei flussi di lavoro automatizzati di [!INCLUDE[prod_short](includes/prod_short.md)]](across-flow-troubleshoot.md)  
[Preparazione al business](ui-get-ready-business.md)  
[Flussi di lavoro](across-workflow.md)  
[Importazione dei dati aziendali da altri sistemi contabili](across-import-data-configuration-packages.md)  
[Assegnare autorizzazioni a utenti e gruppi](ui-define-granular-permissions.md)  
[Configurare [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Finanze](finance.md)  
[Configurare flussi di lavoro automatizzati](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows)  

[!INCLUDE[footer-include](includes/footer-banner.md)]