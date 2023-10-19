---
title: Gestire il lavoro tra più aziende nell'hub aziendale
description: Informazioni sull'hub aziendale in Dynamics 365 Business Central che si utilizza per gestire il lavoro in più società.
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'accountant, accounting, financial report'
ms.search.form: '1151, 1154, 1165, 1166'
ms.date: 09/28/2023
ms.author: bholtorf
ms.custom: bap-template
---

# <a name="manage-work-across-multiple-companies-in-the-company-hub"></a>Gestire il lavoro tra più aziende nell'hub aziendale

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Alcune persone lavorano in più società in [!INCLUDE [prod_short](includes/prod_short.md)] e alcuni lavorano anche in più di un'organizzazione, come contabili esterni o dipendenti e manager di società con più filiali. Per questi utenti e molti altri, l'hub aziendale funge da pagina di destinazione che offre una panoramica finanziaria di società e ambienti. Fornisce agli utenti uno strumento per la gestione del lavoro nei vari ambienti in cui lavorano, tra società, ambienti e aree.  

È possibile accedere all'hub aziendale passando al ruolo **Hub aziendale** in Impostazioni personali o aprendo la pagina **Hub aziendale** direttamente. È possibile eseguire lo stesso lavoro in entrambi i posti, ma le azioni sono posizionate in modo leggermente diverso nei menu.  

[![Mostra la pagina dell'hub aziendale che elenca tutte le società.](media/company-hub.png)](media/company-hub.png#lightbox)  

> [!NOTE]
> Puoi collegare l'hub aziendale a tutte le società di cui hai bisogno. Tuttavia, puoi connettere l'hub aziendale solo alle società ospitate in [!INCLUDE [prod_short](includes/prod_short.md)] Online.

## <a name="company-hub-home-page"></a>Home page dell'hub aziendale

Se si utilizza il ruolo **Hub aziendale**, la home page mostra un elenco di società a cui si ha accesso, comprese le informazioni sui dati dei punti di interesse chiave (KPI) e i collegamenti per aprire ciascuna società. <!--You can customize the dashboard to show the data points that you want to see by adding or removing columns. For example, you might want to see taxes that are due, how many open sales documents each company has, or the number of purchase invoices that are due next week. You can configure the view to suit your needs. If you have added many companies, you can use filters to sort your view.--> Scegliere l'azione **Hub aziendale** per aprire l'hub aziendale, dove è possibile lavorare a più stretto contatto con ciascuna società.  

> [!TIP]
> Per accedere a una società specifica in [!INCLUDE [prod_short](includes/prod_short.md)], scegliere il nome della società o scegliere la voce di menu **Vai alla società** con cui si accede automaticamente in una nuova scheda del browser.

:::image type="content" source="media/company-hub-company-list-actions.png" alt-text="Azioni per una società elencata nell'hub aziendale.":::

È possibile aggiungere nuove società, ad esempio quando si ottiene un nuovo cliente o quando l'azienda aggiunge una nuova filiale. Per ulteriori informazioni, vedere [Aggiungere società all'hub aziendale](company-hub-add-company.md).  

> [!TIP]
> Per aggiornare i dati nell'hub aziendale, è necessario avere accesso ai dati nelle società da cui provengono i dati.

<!--## Company details

In the **Company Hub** page, you can see more information about each company by choosing the name of the company that you want to learn more about. This opens the **Company Details** pane, where you can see additional information, such as the following:  

* Cash account balances  
* Cash flow forecast  
* Overdue purchase invoices  
* Overdue sales invoices  

> [!TIP]
> You can launch predefined Excel workbooks from the **Reports** tab in the ribbon. These Excel workbooks are designed as ready-to-print key financial statements and reports, but you can also modify them to fit your needs. For more information, see [Analyzing Financial Statements in Microsoft Excel](finance-analyze-excel.md).  

Otherwise, close the details pane and continue to the next company.  -->

## <a name="assigned-tasks"></a>Task assegnati

In [!INCLUDE [prod_short](includes/prod_short.md)], è possibile assegnare task a se stessi e ad altri, altri utenti possono assegnate task a te. L'hub aziendale offre una panoramica dei task assegnati per ogni società ed è inoltre possibile accedere a una lista di tutti i task assegnati scegliendo nella pagina **Task personali dell'utente** nella **home page**.  

<!--In the client company, you also have cues that call out tasks assigned to you in this particular client.  -->

### <a name="my-user-tasks"></a>Task personali dell'utente

L'elenco **Task personali dell'utente** consente di assegnare la priorità al giorno mostrando ulteriori informazioni sui task assegnati per tutte le società.  

È possibile ordinare per data di scadenza, ad esempio, o per qualsiasi altro tipo di dati che consente di assegnare priorità per la giornata. Per impostazione predefinita, nell'elenco sono visualizzati tutti i task allocati a te, ma puoi impostare i filtri per visualizzare solo i task prioritari, ad esempio.  

Per selezionare un task, sceglilo dall'elenco dei task in sospeso dell'utente. Nella barra multifunzione, il collegamento **Vai a elemento task** apre la pagina in cui è possibile svolgere l'attività.  

Una volta completato il task, contrassegnalo come completato.  

Per ulteriori informazioni su società e ambienti, vedere [Collegamenti ambiente](company-hub-add-company.md#environment-links).  

## <a name="access-the-company-hub"></a>Accesso all'hub aziendale

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

Per accedere all'hub aziendale, è necessario accedere tramite il gruppo di utenti *Hub aziendale Dynamics 365* o tramite il set di autorizzazioni *Hub aziendale Dynamics 365*. È necessario inoltre disporre dell'accesso alle società elencate nell'hub aziendale, il che significa che è necessario essere un utente in quelle società. Per ulteriori informazioni, vedere [Creare utenti in base alle licenze](ui-how-users-permissions.md).  

> [!IMPORTANT]
> L'hub aziendale è un elenco a livello aziendale, quindi qualsiasi utente a cui viene concesso l'accesso all'hub aziendale sarà in grado di vedere tutte le società nel tenant [!INCLUDE [prod_short](includes/prod_short.md)] e tutti i KPI per le società a cui ha accesso.

Se non si riesce a trovare l'hub aziendale ed è stato concesso l'accesso, verificare con l'amministratore se l'hub aziendale è elencato nella pagina **Gestione delle estensioni**. Per ulteriori informazioni, vedere [Personalizzazione di Business Central usando le estensioni](ui-extensions.md).  

## <a name="set-up-the-company-hub"></a>Impostazione dell'hub aziendale

Per iniziare a utilizzare l'hub aziendale, è necessario aggiungere una o più società alla dashboard. Per ulteriori informazioni, vedere [Aggiungere società all'hub aziendale](company-hub-add-company.md).  

Tuttavia per aggiungere una società, è necessario che sia stato concesso l'accesso a una o più istanze di [!INCLUDE [prod_short](includes/prod_short.md)] oltre alla società in cui si utilizza l'hub aziendale.  

Ad esempio, in qualità di contabile, i clienti possono invitare l'utente in [!INCLUDE [prod_short](includes/prod_short.md)]. Per ulteriori informazioni, vedere [Invitare il contabile esterno in Business Central](finance-accounting.md#inviteaccountant).  

Gli amministratori possono utilizzare la stessa guida setup assistito per aggiungere l'utente a [!INCLUDE [prod_short](includes/prod_short.md)] oppure possono aggiungere l'utente all'account Microsoft Entra nell'interfaccia di amministrazione di Microsoft 365. Per ulteriori informazioni, vedere [Gestire gli utenti e i gruppi](/microsoft-365/admin/add-users/?view=o365-worldwide&preserve-view=true).  

## <a name="see-also"></a>Vedere anche

[Aggiungere società all'hub aziendale](company-hub-add-company.md)  
[Esperienze contabile in Business Central](finance-accounting.md)  
[Hub aziendale per l'estensione Business Central](ui-extensions-company-hub.md)  
[Modificare le impostazioni di base](ui-change-basic-settings.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
