---
title: Risolvere i problemi dei flussi di lavoro automatizzati
description: Scopri come risolvere i problemi di connessione tra Business Central e Power Automate quando crei un flusso di lavoro automatizzato.
author: jswymer
ms.topic: conceptual
ms.search.keywords: 'workflow, OData, Power App, SOAP, Entity set not found, workflowWebhookSubscriptions, Power Automate,'
ms.date: 07/03/2023
ms.author: jswymer
ms.reviewer: jswymer
---

# <a name="troubleshoot-your--automated-workflows"></a>Risolvere i problemi dei[!INCLUDE[prod_short](includes/prod_short.md)] flussi di lavoro auomatizzati

Quando ti connetti a[!INCLUDE [prod_short](includes/prod_short.md)] insieme aPower Automate per creare flussi di lavoro automatizzati, potrebbero essere visualizzati messaggi di errore. Questo articolo fornisce soluzioni suggerite per problemi ricorrenti.

## <a name="flow-doesnt-run-on-all-records-created-or-changed"></a>Il flusso non viene eseguito su tutti i record creati o modificati

### <a name="problem"></a>Problema

Se un evento crea o modifica molti record, il flusso non viene eseguito su alcuni o tutti i record.

### <a name="possible-cause"></a>Causa possibile

Attualmente esiste un limite al numero di record che un flusso può elaborare. Se vengono creati o modificati più di 1000 record entro 30 secondi, il flusso non viene attivato.

> [!NOTE]
> Per gli sviluppatori, l'attivazione del flusso viene eseguita tramite notifiche webhook e questa limitazione è dovuta al modo in cui il connettore Business Central gestisce le notifiche `collection`. Per ulteriori informazioni, vedi [Utilizzo dei webhook in Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/api-reference/v2.0/dynamics-subscriptions#notes-for-power-automate-flows) nella Guida per sviluppatori e amministratori.

## <a name="the-response-from-the-business-central-service-is-too-large-error"></a>Errore "La risposta dal servizio Business Central è troppo grande"

### <a name="problem-1"></a>Problema

Quando si utilizza un'azione che interagisce con i record (come *Crea record (V3)* e *Ottieni record (V3)*), Power Automate potrebbe visualizzare un errore simile a questo:

`The response from the Business Central service is too large`

### <a name="possible-cause-1"></a>Causa possibile

Anche se Business Central non ha limiti prefissati per le dimensioni dei record restituiti dalle API, il connettore Dynamics 365 Business Central per Power Automate può gestire solo record fino a 8 MB.

Tutte le API di Business Central fornite da Microsoft restituiscono record al di sotto di questo limite, ma le API fornite dai partner potrebbero non esserlo. Se visualizzi un errore "La risposta dal servizio Business Central è troppo grande", contatta il partner che ha creato l'API che stai utilizzando.

## <a name="entity-set-not-found-error"></a>Errore "Set di entità non trovato"

### <a name="problem-2"></a>Problema

Quando si crea un nuovo flusso Power Automate usando un trigger di approvazione [!INCLUDE[prod_short](includes/prod_short.md)], ad esempio *Quando viene richiesta l'approvazione di un documento di acquisto*, si potrebbe ricevere un messaggio di errore simile al seguente:

`Entity set not found: \<name\>`

Il segnaposto, `\<name\>` è il nome del servizio Web mancante, come *workflowWebhookSubscriptions* o *workflowPurchaseDocumentLines*.

### <a name="possible-cause-2"></a>Causa possibile

L'utilizzo di Power Automate per le approvazioni richiede che determinati oggetti pagina e codeunit objects vengano pubblicati come servizi Web. Per impostazione predefinita, la maggior parte degli oggetti richiesti viene pubblicata come servizi Web. In alcuni casi, tuttavia, l'ambiente potrebbe essere stato personalizzato in modo che questi oggetti non vengano più pubblicati.

### <a name="fix"></a>Correggi

Accedere alla pagina **Servizi Web** e assicurarsi che i seguenti oggetti vengano pubblicati come servizi Web. Dovrebbe esserci una voce nell'elenco per ogni oggetto, con la casella di controllo **Pubblicato** selezionata.  

| Tipo oggetto | ID oggetto | Nome oggetto | Nome servizio |
|--|--|--|--|
| Codeunit | 1544 | WorkflowWebhookSubscription | WorkflowActionResponse |
| Pagina | 6408 | workflowCustomers | workflowCustomers |
| Pagina | 6406 | workflowGenJournalBatches | workflowGenJournalBatches |
| Pagina | 6407 | workflowGenJournalLines | workflowGenJournalLines |
| Pagina | 6409 | workflowItems | workflowItems |
| Pagina | 6405 | Entità riga documento di acquisto | workflowPurchaseDocumentLines |
| Pagina | 6404 | workflowPurchaseDocuments | workflowPurchaseDocuments |
| Pagina | 6403 | Entità riga documento di vendita | workflowSalesDocumentLines |
| Pagina | 6402 | workflowSalesDocuments | workflowSalesDocuments |
| Pagina | 6410 | workflowVendors | workflowVendors |
| Pagina | 831 | workflowWebhookSubscriptions | workflowWebhookSubscriptions |

> [!NOTE]
> Il valore **Nome servizio** deve essere esattamente quello mostrato nella tabella. Non modificare o tradurre il nome del servizio.

Per ulteriori informazioni sulla pubblicazione di servizi Web, vedi [Pubblicare un servizio Web](across-how-publish-web-service.md).

## <a name="see-related-training-at-microsoft-learn"></a>Vedi le informazioni relative al training in [Microsoft Learn](/learn/modules/use-power-automate/).

## <a name="see-also"></a>Vedere anche

[Utilizzare i flussi Power Automate in [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-financials-data-source-flow.md)  
[Workflow](across-workflow.md)  
[Configurare flussi di lavoro automatizzati](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows)  
[Attivare flussi istantanei](/dynamics365/business-central/dev-itpro/powerplatform/instant-flows)  
[Gestire flussi di Power Automate](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
