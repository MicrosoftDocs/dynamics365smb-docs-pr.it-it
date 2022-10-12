---
title: Utilizzare flussi di Power Automate in Business Central
description: Configurare e utilizzare flussi di Power Automate per creare o modificare i dati di Business Central.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, OData, Power App, SOAP, Power Automate,
ms.search.form: 1500,
ms.date: 09/13/2022
ms.author: edupont
ms.openlocfilehash: 5fe089c0330a8d2b7a71f4907212665722d27d38
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/30/2022
ms.locfileid: "9606523"
---
# <a name="use-power-automate-flows-in-prod_short"></a>Utilizzare i flussi di Power Automate in [!INCLUDE[prod_short](includes/prod_short.md)]

È possibile utilizzare i dati di [!INCLUDE[prod_short](includes/prod_short.md)] come parte di un flusso di lavoro in Microsoft Power Automate. Crea i tuoi flussi e connettiti ai tuoi dati da origini interni ed esterni con il connettore [!INCLUDE [prod_short](includes/prod_short.md)].

> [!NOTE]
> È necessario disporre di un account valido con [!INCLUDE[prod_short](includes/prod_short.md)] e con Power Automate.  

> [!TIP]
> Oltre a Power Automate, è possibile utilizzare i modelli di flusso di lavoro di approvazione in [!INCLUDE[prod_short](includes/prod_short.md)]. Sebbene siano presenti due sistemi del flusso di lavoro, qualsiasi modello di flusso di lavoro di approvazione creato con Power Automate viene aggiunta all'elenco dei workflow in [!INCLUDE[prod_short](includes/prod_short.md)]. Ulteriori informazioni in [Flussi di lavoro](across-workflow.md).

I flussi Power Automate sono attivati da eventi quali la creazione, la modifica o l'eliminazione di record e documenti (flussi automatizzati). I flussi possono anche essere eseguiti su una pianificazione definita dall'utente (flussi programmati) o su richiesta (flussi istantanei).

## <a name="power-automate-features-in-prod_short"></a>Funzionalità Power Automate in [!INCLUDE[prod_short](includes/prod_short.md)]

I flussi espandono le funzionalità dei flussi di lavoro di approvazione integrate disponibili in [!INCLUDE[prod_short](includes/prod_short.md)] senza richiedere conoscenze di codifica e può essere associato a un'ampia gamma di eventi e risposte, come modifiche ai record, aggiornamenti di file esterni, documenti pubblicati, nonché diversi servizi Microsoft e di terze parti ad esempio Microsoft Outlook, Microsoft Excel, Microsoft Dataverse, Microsoft Teams, Microsoft SharePoint, Microsoft Power Apps e altro ancora.

Ad esempio, una nuova fattura di vendita può attivare un flusso di lavoro per una richiesta di approvazione, che può avere eventi diversi impostati a seconda della risposta dell'approvatore. Una risposta negativa invia una notifica e un'e-mail al richiedente l'approvazione. Una risposta positiva aggiorna contemporaneamente un foglio di calcolo Excel che si trova in una cartella di SharePoint e invia un aggiornamento a una chat di Teams.

I flussi istantanei funzionano in modo simile ai collegamenti batch, eseguendo più passaggi lunghi con poche pressioni di pulsanti e vengono avviati da pagine o tabelle specifiche. Ad esempio, un flusso può aggiungere un pulsante al menu delle azioni nella pagina **Fornitori** per bloccare i pagamenti a un fornitore e, allo stesso tempo, inviare e-mail personalizzabili al contatto del fornitore e agli acquirenti della tua azienda, nonché aggiornare il contatto in Outlook.

## <a name="automated-workflows"></a>Flussi di lavoro automatizzati

Con Power Automate, puoi creare flussi aziendali direttamente internamente e affidarti agli sviluppatori non professionisti. I flussi di lavoro automatizzati possono essere avviati da eventi interni ed esterni in [!INCLUDE[prod_short](includes/prod_short.md)] ed essere anche impostati per l'esecuzione periodica. Scopri di più e ottieni istruzioni su come creare flussi di lavoro nell'articolo [Configurare flussi di lavoro automatizzati](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) nel contenuto per gli amministratori.

## <a name="instant-flows"></a>Flussi istantanei

[!INCLUDE [prod_short](includes/prod_short.md)] può eseguire un flusso Power Automate dalla maggior parte delle pagine di elenchi, schede e documenti. Una volta che l'amministratore ha connesso [!INCLUDE [prod_short](includes/prod_short.md)] a Power Automate, vedrai tutti i flussi che la tua organizzazione ha aggiunto quando scegli l'azione **Automatizza** nelle pagine pertinenti. I flussi istantanei vengono eseguito senza uscire da [!INCLUDE [prod_short](includes/prod_short.md)]. Per ulteriori informazioni, vedi l'articolo [Configurare flussi di lavoro automatizzati](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) nel contenuto per gli amministratori.

Questi flussi di lavoro istantanei aprono una pagina all'interno di [!INCLUDE [prod_short](includes/prod_short.md)] online in modo da rimanere nel contesto del processo aziendale in cui eri nel mezzo. Scegli l'azione **Automatizza**, in alcune pagine nel menu **Altre opzioni**, scegli la voce di menu **Power Automate**, quindi scegli il collegamento pertinente per attivare il flusso di lavoro. La connessione a Power Automate è già configurata automaticamente.

La maggior parte dei flussi richiede la compilazione di uno o due campi prima di scegliere l'azione **Esegui flusso**.

> [!TIP]
> Se non vedi un'azione **Automatizza**, il tuo[!INCLUDE [prod_short](includes/prod_short.md)] non è stato ancora probabilmente impostato per l'uso Power Automate. Ulteriori informazioni dal tuo amministratore.

## <a name="add-more-automated-flows-and-instant-flows"></a>Aggiungere più flussi automatizzati e flussi istantanei

Puoi creare flussi nel sito Web [powerautomate.microsoft.com](https://powerautomate.microsoft.com). Tuttavia, se l'amministratore ha attivato la funzionalità per l'esecuzione di flussi Power Automate da [!INCLUDE [prod_short](includes/prod_short.md)] online, puoi avviare il processo di creazione di un flusso dall'azione **Automatizza** nelle relative pagine, che si trovano nel menu **Altre opzioni** a seconda della pagina. Quindi scegli la voce di menu di **Power Automate** e l'azione **Crea un flusso**. Power Automate si apre quindi in una nuova scheda del browser e puoi accedere automaticamente.

Puoi trovare modelli di esempio da adattare alla tua azienda e tutti gli eventi trigger disponibili, utilizzando [!INCLUDE [prod_short](includes/prod_short.md)] e strumenti esterni, scegliendo il menu **Connettori** nel sito Web Power Automate. Ulteriori informazioni sui trigger e i modelli disponibili nell'articolo [Configurare flussi di lavoro automatizzati](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) nel contenuto per gli amministratori.

## <a name="manage-automated-workflows"></a>Gestire flussi di lavoro automatizzati

Puoi creare nuovi flussi o gestire i flussi di Power Automate esistenti in [!INCLUDE [prod_short](includes/prod_short.md)] nella pagina **Gestisci flussi Power Automate**. Ulteriori informazioni nell'articolo [Gestire i flussi di Power Automate](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows) nel contenuto per gli amministratori.

Puoi anche gestire i flussi di lavoro di Power Automate disponibili nella pagina **Flussi di lavoro** in [!INCLUDE[prod_short](includes/prod_short.md)]. La pagina elenca sia l'approvazione integrata che i flussi di lavoro di Power Automate, con l'opzione di abilitare/disabilitare, eliminare e visualizzare il flusso di lavoro nel sito Web di Power Automate.

## <a name="see-related-microsoft-training"></a>Vedi il relativo [training Microsoft](/training/modules/use-power-automate/)

## <a name="see-also"></a>Vedere anche

[Risolvere i problemi dei flussi di lavoro automatizzati di [!INCLUDE[prod_short](includes/prod_short.md)]](across-flow-troubleshoot.md)  
[Preparazione al business](ui-get-ready-business.md)  
[Flussi di lavoro](across-workflow.md)  
[Importazione dei dati aziendali da altri sistemi contabili](across-import-data-configuration-packages.md)  
[Assegnare autorizzazioni a utenti e gruppi](ui-define-granular-permissions.md)  
[Configurare [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Finanze](finance.md)  
[Gestire flussi di Power Automate](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows)  
[Configurare flussi di lavoro automatizzati](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows)  
[Attivare flussi istantanei](/dynamics365/business-central/dev-itpro/powerplatform/instant-flows)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
