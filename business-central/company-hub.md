---
title: Gestire il lavoro tra più aziende nell'hub aziendale
description: Informazioni sull'hub aziendale in Dynamics 365 Business Central che si utilizza per gestire il lavoro in più società.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: accountant, accounting, financial report
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 7ed69f86a941a216ef948488d3756c06f298549d
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3927694"
---
# <a name="manage-work-across-multiple-companies-in-the-company-hub"></a>Gestire il lavoro tra più aziende nell'hub aziendale

Alcune persone lavorano in più società in [!INCLUDE [prodshort](includes/prodshort.md)] e alcuni lavorano anche in più di un'organizzazione, come contabili esterni o dipendenti e manager di società con più filiali. Per questi utenti e molti altri, l'hub aziendale funge da pagina di destinazione per la gestione del lavoro nei vari ambienti in cui lavorano, tra aziende, ambienti e regioni.  

È possibile accedere all'hub aziendale passando al ruolo **Hub aziendale** in Impostazioni personali o aprendo la pagina **Hub aziendale** direttamente. È possibile eseguire lo stesso lavoro in entrambi i posti, ma le azioni sono posizionate in modo leggermente diverso nei menu.  

## <a name="company-hub-home-page"></a>Home page dell'hub aziendale

Se si utilizza il ruolo **Hub aziendale**, la home page mostra un elenco di società a cui si ha accesso, comprese le informazioni sui dati dei punti di interesse chiave (KPI) e i collegamenti per aprire ciascuna società. È possibile personalizzare il dashboard per indicare le informazioni sui dati che si desidera visualizzare aggiungendo o rimovendo le colonne. Ad esempio, è possibile visualizzare le imposte in scadenza, il numero di documenti di vendita aperti in ogni società o il numero delle fatture di acquisto che sono in scadenza la settimana prossima. È possibile configurare la visualizzazione in base alle proprie esigenze. Se si dispone di molte società, è possibile utilizzare i filtri per ordinare la visualizzazione.  

Scegliere l'azione **Hub aziendale** per aprire l'hub aziendale, dove è possibile lavorare a più stretto contatto con ciascuna società.  

> [!TIP]
> Per accedere a una società specifica in [!INCLUDE [prodshort](includes/prodshort.md)], scegliere il nome della società o scegliere la voce di menu **Vai alla società** con cui si accede automaticamente in una nuova scheda del browser.

:::image type="content" source="media/company-hub-company-list-actions.png" alt-text="Azioni per una società elencata nell'hub aziendale":::

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

In [!INCLUDE [prodshort](includes/prodshort.md)], è possibile assegnare task a se stessi e ad altri, altri utenti possono assegnate task a te. L'hub aziendale offre una panoramica dei task assegnati per ogni società ed è inoltre possibile accedere a una lista di tutti i task assegnati scegliendo nella pagina **Task personali dell'utente** nella **home page**.  

<!--In the client company, you also have cues that call out tasks assigned to you in this particular client.  -->

### <a name="my-user-tasks"></a>Task personali dell'utente

L'elenco **Task personali dell'utente** consente di assegnare la priorità al giorno mostrando ulteriori informazioni sui task assegnati per tutte le società.  

È possibile ordinare per data di scadenza, ad esempio, o per qualsiasi altro tipo di dati che consente di assegnare priorità per la giornata. Per impostazione predefinita, nell'elenco sono visualizzati tutti i task allocati a te, ma puoi impostare i filtri per visualizzare solo i task prioritari, ad esempio.  

Per selezionare un task, sceglierlo dall'elenco dei task in sospeso dell'utente. Nella barra multifunzione, il collegamento **Vai a elemento task** apre la pagina in cui è possibile svolgere l'attività.  

Una volta completato il task, contrassegnarlo come completato.  

Per ulteriori informazioni su società e ambienti, vedere [Collegamenti ambiente](company-hub-add-company.md#environment-links).  

## <a name="access-the-company-hub"></a>Accesso all'hub aziendale

Per accedere all'hub aziendale, è necessario accedere tramite il gruppo di utenti *Hub aziendale Dynamics 365* o tramite il set di autorizzazioni *Hub aziendale Dynamics 365*. È necessario inoltre disporre dell'accesso alle società elencate nell'hub aziendale, il che significa che è necessario essere un utente in quelle società. Per ulteriori informazioni, vedere [Creare utenti in base alle licenze](ui-how-users-permissions.md).  

> [!IMPORTANT]
> L'hub aziendale è un elenco a livello aziendale, quindi qualsiasi utente a cui viene concesso l'accesso all'hub aziendale sarà in grado di vedere tutte le società nel tenant [!INCLUDE [prodshort](includes/prodshort.md)] e tutti i KPI per le società a cui ha accesso.

Se non si riesce a trovare l'hub aziendale ed è stato concesso l'accesso, verificare con l'amministratore se l'hub aziendale è elencato nella pagina **Gestione delle estensioni**. Per ulteriori informazioni, vedere [Personalizzazione di Business Central usando le estensioni](ui-extensions.md).  

## <a name="set-up-the-company-hub"></a>Impostazione dell'hub aziendale

Per iniziare a utilizzare l'hub aziendale, è necessario aggiungere una o più società alla dashboard. Per ulteriori informazioni, vedere [Aggiungere società all'hub aziendale](company-hub-add-company.md).  

Tuttavia per aggiungere una società, è necessario che sia stato concesso l'accesso a una o più istanze di [!INCLUDE [prodshort](includes/prodshort.md)] oltre alla società in cui si utilizza l'hub aziendale.  

Ad esempio, in qualità di contabile, i clienti possono invitare l'utente in [!INCLUDE [prodshort](includes/prodshort.md)]. Per ulteriori informazioni, vedere [Invitare il contabile esterno in Business Central](finance-accounting.md#inviteaccountant).  

Gli amministratori possono utilizzare la stessa guida setup assistito per aggiungere l'utente a [!INCLUDE [prodshort](includes/prodshort.md)] oppure possono aggiungere l'utente all'account Azure AD nell'interfaccia di amministrazione di Microsoft 365. Per ulteriori informazioni, vedere [Gestire gli utenti e i gruppi](/microsoft-365/admin/add-users/?view=o365-worldwide&preserve-view=true).  

## <a name="see-also"></a>Vedere anche

[Aggiungere società all'hub aziendale](company-hub-add-company.md)  
[Esperienze contabile in Business Central](finance-accounting.md)  
[Hub aziendale per l'estensione Business Central](ui-extensions-company-hub.md)  
[Modificare le impostazioni di base](ui-change-basic-settings.md)  
