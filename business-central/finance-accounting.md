---
title: Esperienza di contabile in Business Central | Documenti Microsoft
description: Informazioni sul portale per contabili per Business Central e la Gestione ruolo utente Contabile che supporta i contabili interni ed esterni nella società client.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 2c99b8bef9bff22edd2d27856e703b41c6ec6441
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2020
ms.locfileid: "3184030"
---
# <a name="accountant-experiences-in-d365fin_long"></a>Esperienze di contabile in [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]
Qualsiasi attività deve avere i suoi libri e firmare la contabilità. Alcuni aziende hanno un contabile esterno e altre hanno un contabile interno. Senza tenere conto del tipo di contabile in questione, è possibile utilizzare la Gestione ruolo utente **Contabile** come Home page in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Da questa pagina, è possibile accedere a tutte le pagine necessarie per lavorare.  

## <a name="accountant-role-center"></a>Gestione ruolo utente Contabile
La Gestione ruolo utente è un dashboard con riquadri di attività che indicano le informazioni di base in tempo reale e consentono di accedere rapidamente ai dati. La barra multifunzione nella parte superiore della pagina consente di accedere a più azioni, ad esempio l'apertura in Excel di report e rendiconti finanziari di uso più comune. Nella barra di spostamento superiore, è possibile passare rapidamente tra le liste che si utilizzano con maggiore frequenza. Qui vengono visualizzate altre aree, ad esempio **Documenti registrati** con i diversi tipi di documenti registrati dalla società.  

Se non si ha familiarità con [!INCLUDE[d365fin](includes/d365fin_md.md)], è possibile guardare una serie di video direttamente dalla Gestione ruolo utente. È inoltre possibile avviare una **Introduzione** che illustra i punti chiave.  

## <a name="inviting-your-external-accountant-to-your-d365fin"></a><a name="inviteaccountant"></a>Invitare il contabile esterno in [!INCLUDE[d365fin](includes/d365fin_md.md)]
Se viene utilizzato un contabile esterno per gestire i libri contabili e i rendiconti finanziari, l'amministratore può invitarlo a [!INCLUDE[d365fin](includes/d365fin_md.md)] in modo che possa utilizzare i dati fiscali dell'azienda. [!INCLUDE[d365fin](includes/d365fin_md.md)] include tre licenze di tipo Contabile esterno. Per ulteriori informazioni sulle licenze, vedere [Guida alle licenze di Microsoft Dynamics 365 Business Central](https://go.microsoft.com/fwlink/?LinkId=871590).

Dopo che il contabile ha eseguire l'accesso a [!INCLUDE[d365fin](includes/d365fin_md.md)], può utilizzare la Gestione ruolo utente **Contabile** che permette di accedere facilmente alle pagine più pertinenti al suo lavoro.  

È stata semplificata la procedura per invitare il contabile esterno. Aprire semplicemente la pagina **Utenti** e scegliere l'azione **Invita contabile esterno** nella barra multifunzione. Viene presentato un messaggio di posta elettronica nel quale è sufficiente aggiungere l'indirizzo di posta elettronica del contabile e inviare l'invito.  

> [!Note]  
> È necessario avere impostato il sistema di posta elettronica SMTP. Per ulteriori informazioni, vedere [Imposta indirizzo e-mail](admin-how-setup-email.md).   

<!-- ![Invite your accountant](./media/finance-invite-accountant/invite-accountant.png)-->

> [!IMPORTANT]  
> L'indirizzo e-mail del contabile deve essere un indirizzo di lavoro che si basa su Azure Active Directory. Se il contabile utilizza un altro tipo di posta elettronica, l'invito non può essere inviato. 
> 
> Poiché questa attività richiede l'accesso alla gestione di utenti e licenze in Azure Active Directory, all'utente che invia questo invito deve essere assegnato il ruolo **Amministratore globale** o **Amministratore utente** nell'interfaccia di amministrazione di Office 365. Per ulteriori informazioni, vedere [Informazioni sui ruoli di amministratore](/office365/admin/add-users/about-admin-roles) nell'interfaccia di amministrazione di Office 365.  

### <a name="adding-your-accountant-to-your-office-365-via-azure-portal"></a>Aggiunta del contabile a Office 365 tramite il portale di Azure

Se l'amministratore o il partner di rivendita non desidera utilizzare la guida **Invita un contabile esterno**, possono aggiungere un utente esterno nel portale di Azure e assegnare a questo utente la licenza di contabile esterno. Per ulteriori informazioni, vedere [Avvio rapido: aggiunta di utenti guest alla directory nel portale di Azure](/azure/active-directory/b2b/b2b-quickstart-add-guest-users-portal).

#### <a name="to-add-your-accountant-as-a-guest-user"></a>Per aggiungere il contabile come utente guest

1. Aprire il [Portale di Azure](https://portal.azure.com/).
2. Nel riquadro a sinistra selezionare **Azure Active Directory**.
3. In **Gestione**, selezionare **Utenti**.
4. Selezionare **Nuovo utente guest**.
5. Nella pagina **Nuovo utente**, selezionare **Invita utente** e aggiungere le informazioni sul contabile esterno.  

   Facoltativamente, includere un messaggio di benvenuto personale per il contabile per fargli sapere che lo stai aggiungendo a [!INCLUDE [prodshort](includes/prodshort.md)].

6. Selezionare **Invita** per inviare automaticamente l'invito. Viene visualizzata una notifica in alto a destra con il messaggio **L'utente è stato invitato**. 
7. Dopo aver inviato l'invito, l'account utente viene automaticamente aggiunto alla directory come guest.

Successivamente, è necessario assegnare una licenza al nuovo utente guest per [!INCLUDE [prodshort](includes/prodshort.md)].

#### <a name="to-give-your-accountant-access-to-your-prodshort"></a>Per concedere al contabile l'accesso a [!INCLUDE [prodshort](includes/prodshort.md)]

1. Nel portale di Azure, per l'utente appena aggiunto, selezionare **Profilo** e quindi scegliere **Modifica**
2. Aggiornare il campo **Posizione di utilizzo** con il paese pertinente, quindi selezionare **Salva**.
3. Scegliere **Licenze** e quindi aprire **Assegnazioni**.
4. Scegliere la licenza **Dynamics 365 Business Central - Contabile esterno**.  

    Se questa licenza non è disponibile, è necessario utilizzare una licenza **Dynamics 365 Business Central for IWs** disponibile.
5. Salvare l'assegnazione.

Se l'operazione viene completata, la licenza viene assegnata all'utente guest e viene creato l'account guest.

### <a name="importing-the-new-user-into-prodshort"></a>Importazione del nuovo utente in [!INCLUDE [prodshort](includes/prodshort.md)]

Il contabile riceverà un messaggio e-mail che lo informa che gli è stato concesso l'accesso ad Active Directory. Successivamente, è necessario assegnare l'accesso alla società giusta in [!INCLUDE [prodshort](includes/prodshort.md)].

#### <a name="to-add-the-accountant-to-the-right-company"></a>Per aggiungere il contabile alla società giusta

1. Aprire la società [!INCLUDE [prodshort](includes/prodshort.md)] a cui si desidera che il contabile acceda all'indirizzo [https://businesscentral.dynamics.com](https://businesscentral.dynamics.com).
2. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Utenti** e quindi scegliere il collegamento correlato.  
3. Scegliere l'azione **Ottieni nuovi utenti da Office 365**.

In tal modo l'account utente creato nel portale di Azure viene importato nella società. Per ulteriori informazioni, vedere [Per aggiungere un utente in Business Central](ui-how-users-permissions.md#adduser).  

Se si desidera consentire l'accesso a più società, è necessario accedere a ciascuna società e ripetere questo processo. In alternativa, è possibile aggiornare i gruppi di autorizzazioni per il profilo utente del contabile in [!INCLUDE [prodshort](includes/prodshort.md)], ad esempio assegnando il gruppo di utenti *D365 Bus Premium*. Per ulteriori informazioni, vedere [Assegnare autorizzazioni a utenti e gruppi](ui-define-granular-permissions.md).  

## <a name="accountant-hub"></a>Accountant Hub

Se si è un contabile con vari clienti, è possibile utilizzare [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)] per avere una panoramica più precisa dei client. Dal portale, è possibile accedere al tenant di ogni client in [!INCLUDE[d365fin](includes/d365fin_md.md)] e utilizzare la Gestione ruolo utente Contabile come descritto sopra. Per ulteriori informazioni, vedi [Benvenuto in [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]](/dynamics365/accountants/index).  

> [!NOTE]
> [!INCLUDE [d365acc_long_md](includes/d365acc_long_md.md)] è attualmente è in versione di anteprima pubblica in un numero limitato di mercati.

## <a name="see-also"></a>Vedere anche

[Finanze](finance.md)  
[Impostazione di dati finanziari](finance-setup-finance.md)  
[Contabilità generale e piano dei conti](finance-general-ledger.md)  
[Chiusura di anni e periodi](year-close-years-periods.md)  
[Utilizzo delle dimensioni](finance-dimensions.md)  
[Analisi dei rendiconti finanziari in Excel](finance-analyze-excel.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Impostazione di un'analisi di un flusso di cassa](finance-setup-cash-flow-analyses.md)  
[Benvenuto in [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]](/dynamics365/accountants/index)  
[Dynamics 365 - Accountant Hub su Microsoft.com](https://www.microsoft.com/dynamics365/financial-insights-for-accountants)  
