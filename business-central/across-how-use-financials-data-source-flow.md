---
title: Connettere i dati a Power Automate | Documenti Microsoft
description: È possibile rendere disponibili i dati di Business Central come origine dati e specificare un URL OData dei service Web per creare un workflow automatizzato.
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, OData, Power App, SOAP, Entity set not found, workflowWebhookSubscriptions
ms.date: 07/27/2021
ms.author: edupont
author: jswymer
ms.openlocfilehash: 62718df1c80cb419501b72bcbdb6d7a6f9f18402
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2022
ms.locfileid: "8518469"
---
# <a name="use-prod_short-in-an-automated-workflow"></a>Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)] in un flusso di lavoro automatizzato

È possibile utilizzare i dati di [!INCLUDE[prod_short](includes/prod_short.md)] come parte di un flusso di lavoro in Microsoft Power Automate.

> [!NOTE]
> Oltre a Power Automate, è possibile utilizzare la funzionalità Workflow in [!INCLUDE[prod_short](includes/prod_short.md)]. Si noti che sebbene siano presenti due sistemi del flusso di lavoro, qualsiasi modello di workflow creato con Power Automate viene aggiunta all'elenco dei workflow in [!INCLUDE[prod_short](includes/prod_short.md)]. Per ulteriori informazioni, vedere [Workflow](across-workflow.md).  

> [!NOTE]  
> È necessario disporre di un account valido con [!INCLUDE[prod_short](includes/prod_short.md)] e con Power Automate.  

## <a name="add-prod_short-as-a-data-source-in-power-automate"></a>Aggiungere [!INCLUDE[prod_short](includes/prod_short.md)] come origine dati in Power Automate

1. Nel browser passare a [flow.microsoft.com](https://flow.microsoft.com), quindi accedere.
2. Scegliere **I miei flussi** dalla barra nella parte superiore della pagina.
3. Sono disponibili 3 modi per creare un flusso: **Inizia da modello**, **Inizia da zero** e **Inizia da un connettore**. Un modello è un flusso predefinito che è stato creato per l'utente. Per utilizzare un modello, selezionarlo e creare una connessione per ogni servizio utilizzato dal modello. Con le opzioni **Inizia da zero** e **Inizia da un connettore**, è possibile creare un nuovo flusso da zero.
4. Per creare un flusso da zero, nella pagina **I miei flussi** selezionare le opzioni **Inizia da zero** e **Flusso automatizzato**.
5. Cercare il connettore **Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]**.
6. Definire un nome e scegliere il trigger da utilizzare per il flusso.
7. Selezionare uno dei trigger [!INCLUDE[prod_short](includes/prod_short.md)] disponibili dall'elenco dei trigger:  

    - *Quando viene richiesta l'approvazione del fornitore*  
    - *Quando viene richiesta un'approvazione riga registrazioni COGE* 
    - *Quando viene eliminato un record*
    - *Quando viene cambiato un record*
    - *Quando viene creato un record*
    - *Quando viene modificato un record*
    - *Quando viene richiesta l'approvazione batch giornale di registrazione generale* 
    - *Quando viene richiesta l'approvazione del cliente*
    - *Quando viene richiesta l'approvazione di un elemento*
    - *Quando viene richiesta l'approvazione di un documento di acquisto*
    - *Quando viene richiesta l'approvazione di un documento di vendita*

8. Power Automate richiederà di selezionare un ambiente e una società all'interno del tenant [!INCLUDE[prod_short](includes/prod_short.md)], oltre a tutti i termini nei dati che si desidera ascoltare.

    > [!NOTE]
    > Il connettore [!INCLUDE[prod_short](includes/prod_short.md)] per Power Automate supporta più ambienti di produzione e sandbox. Se non sono stati creati più ambienti di produzione o sandbox, **Produzione** è l'unica opzione disponibile che è possibile scegliere.  

    A questo punto, è stata stabilita correttamente la connessione ai dati di Business Central[!INCLUDE[prod_short](includes/prod_short.md)] e si è pronti per iniziare a creare il flusso.

9. Per creare da un modello, selezionare l'opzione **Inizia da modello**.
10. Cercare i modelli **Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]**.
11. Dall'elenco di modelli disponibili, selezionare uno dei modelli e scegliere **Crea**.  

    - *Richiesta di approvazione per ordine di vendita Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]*
    - *Richiesta di approvazione per offerta di vendita Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]*
    - *Richiesta di approvazione per fattura di vendita Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]*
    - *Richiesta di approvazione per nota di credito di vendita Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]*
    - *Richiesta di approvazione per cliente Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]*
    - *Richiesta di approvazione per acquisto Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]*
    - *Richiesta di approvazione per fattura d'acquisto Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]*
    - *Richiesta di approvazione per nota di credito di acquisto Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]*  
    - *Richiesta di approvazione per articolo Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]*
    - *Richiesta di approvazione per fornitore Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]*
    - *Richiesta di approvazione per batch registrazioni COGE Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]*  
    - *Richiesta di approvazione per righe registrazioni COGE Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]*
12. Power Automate visualizzerà un elenco di servizi utilizzati nel modello di flusso e tenterà di connettersi automaticamente a tali servizi. Se non si è precedentemente connessi a un servizio, verrà richiesto di accedere a ciascuno dei servizi a cui è necessario connettersi. Un segno di spunta verde verrà visualizzato accanto a ciascun servizio una volta stabilita correttamente una connessione. Selezionare **Continua**.
13. Power Automate richiederà la selezione di un ambiente e di una società nel tenant [!INCLUDE[prod_short](includes/prod_short.md)]. Poiché ogni fase del flusso è indipendente dalla successiva, è possibile che sia necessario definire l'ambiente e la società più volte quando si utilizza un modello di flusso di [!INCLUDE[prod_short](includes/prod_short.md)] Power Automate.

Per ulteriori informazioni, vedere [Documentazione di Power Automate](/power-automate/getting-started).

## <a name="troubleshooting"></a>Troubleshooting

### <a name="entity-set-not-found-error"></a>Errore "Set di entità non trovato"

#### <a name="problem"></a>Problema

Quando si crea un nuovo flusso Power Automate usando un trigger di approvazione [!INCLUDE[prod_short](includes/prod_short.md)], ad esempio *Quando viene richiesta l'approvazione di un documento di acquisto*, si riceve un messaggio di errore simile al seguente:

**Set di entità non trovato: \<name\>**

dove **\<name\>** è il nome del servizio Web mancante, come **workflowWebhookSubscriptions** o **workflowPurchaseDocumentLines**.

#### <a name="possible-cause"></a>Causa possibile

Quando si usa Power Automate come integrazione a [!INCLUDE[prod_short](includes/prod_short.md)], le approvazioni richiedono che determinati oggetti pagina e codeunit objects vengano pubblicati come servizi Web. Per impostazione predefinita, la maggior parte degli oggetti richiesti viene pubblicata come servizi Web. In alcuni casi, tuttavia, l'ambiente potrebbe essere stato personalizzato in modo che questi oggetti non vengano più pubblicati.

#### <a name="fix"></a>Correzione

Accedere alla pagina **Servizi Web** e assicurarsi che i seguenti oggetti vengano pubblicati come servizi Web. Dovrebbe esserci una voce nell'elenco per ogni oggetto, con la casella di controllo **Pubblicato** selezionata. 

|Tipo oggetto|ID oggetto|Nome oggetto|Nome servizio|
|-----------|---------|-----------|------------|
|Codeunit|  1544    |WorkflowWebhookSubscription|WorkflowActionResponse|
|Pagina|  6408|   workflowCustomers|  workflowCustomers|
|Pagina   |6406   |workflowGenJournalBatches| workflowGenJournalBatches|
|Pagina   |6407   |workflowGenJournalLines|workflowGenJournalLines|
|Pagina   |6409   |workflowItems| workflowItems|
|Pagina   |6405   |Entità riga documento di acquisto|workflowPurchaseDocumentLines|
|Pagina|  6404    |workflowPurchaseDocuments| workflowPurchaseDocuments|
|Pagina|  6403    |Entità riga documento di vendita |workflowSalesDocumentLines|
|Pagina|  6402|   workflowSalesDocuments| workflowSalesDocuments|
|Pagina|  6410    |workflowVendors|   workflowVendors|
|Pagina|  831 |workflowWebhookSubscriptions|  workflowWebhookSubscriptions|

> [!NOTE]
> Il valore **Nome servizio** deve essere esattamente quello mostrato nella tabella. Non modificare o tradurre il nome del servizio.

Per ulteriori informazioni sulla pubblicazione di servizi Web, vedere [Pubblicare un servizio Web](across-how-publish-web-service.md).

## <a name="see-also"></a>Vedere anche

[Preparazione al business](ui-get-ready-business.md)  
[Workflow](across-workflow.md)  
[Importazione dei dati aziendali da altri sistemi contabili](across-import-data-configuration-packages.md)  
[Assegnare autorizzazioni a utenti e gruppi](ui-define-granular-permissions.md)  
[Gestire flussi di lavoro [!INCLUDE[prod_long](includes/prod_long.md)]](across-use-workflows.md)  
[Setup utente approvazione](across-how-to-set-up-approval-users.md)  
[Impostazione di [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Finanze](finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]