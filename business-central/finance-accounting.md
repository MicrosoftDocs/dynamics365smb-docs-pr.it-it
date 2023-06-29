---
title: Esperienze contabili in Business Central (video)
description: Informazioni sulla Gestione ruolo utente Contabile e sull'hub aziendale che supportano i contabili interni ed esterni nella società client.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'accountant, accounting, financial report'
ms.search.form: '100, 1156, 1157, 1314, 1315, 1316, 9027'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="accountant-experiences-in-"></a><a name="accountant-experiences-in-"></a>Esperienze di contabile in [!INCLUDE[prod_long](includes/prod_long.md)]

Qualsiasi attività deve avere i suoi libri e firmare la contabilità. Alcuni aziende hanno un contabile esterno e altre hanno un contabile interno. Senza tenere conto del tipo di contabile in questione, è possibile utilizzare la Gestione ruolo utente **Contabile** come Home page in [!INCLUDE[prod_short](includes/prod_short.md)]. Da questa pagina, è possibile accedere a tutte le pagine necessarie per lavorare.  

## <a name="accountant-role-center"></a><a name="accountant-role-center"></a>Gestione ruolo utente Contabile

La Gestione ruolo utente è un dashboard con riquadri di attività che indicano le informazioni di base in tempo reale e consentono di accedere rapidamente ai dati. La barra multifunzione nella parte superiore della pagina consente di accedere a più azioni, ad esempio l'apertura in Excel di report e rendiconti finanziari di uso più comune. Nella barra di spostamento superiore, è possibile passare rapidamente tra le liste che si utilizzano con maggiore frequenza. Qui vengono visualizzate altre aree, ad esempio **Documenti registrati** con i diversi tipi di documenti registrati dalla società.  

Se non si ha familiarità con [!INCLUDE[prod_short](includes/prod_short.md)], è possibile guardare una serie di video direttamente dalla Gestione ruolo utente. È inoltre possibile avviare una **Introduzione** che illustra i punti chiave.  

## <a name="company-hub"></a><a name="company-hub"></a>Hub aziendale

Se si lavora in più società [!INCLUDE [prod_short](includes/prod_short.md)] è possibile utilizzare la pagina **Hub aziendale** per tenere traccia del lavoro.  Per ulteriori informazioni, vedere [Gestire il lavoro tra più aziende nell'hub aziendale](company-hub.md).  

## <a name="inviting-your-external-accountant-to-your-"></a><a name="inviting-your-external-accountant-to-your-"></a><a name="inviteaccountant"></a>Invitare il contabile esterno in [!INCLUDE[prod_short](includes/prod_short.md)]

Se viene utilizzato un contabile esterno per gestire i libri contabili e i rendiconti finanziari, l'amministratore può invitarlo a [!INCLUDE[prod_short](includes/prod_short.md)] in modo che possa utilizzare i dati fiscali dell'azienda. [!INCLUDE[prod_short](includes/prod_short.md)] include tre licenze di tipo Contabile esterno. Per ulteriori informazioni sulle licenze, vedere [Guida alle licenze di Microsoft Dynamics 365 Business Central](https://go.microsoft.com/fwlink/?LinkId=871590).

Dopo che il contabile ha eseguire l'accesso a [!INCLUDE[prod_short](includes/prod_short.md)], può utilizzare la Gestione ruolo utente **Contabile** che permette di accedere facilmente alle pagine più pertinenti al suo lavoro. Possono anche utilizzare l'hub aziendale nel proprio [!INCLUDE [prod_short](includes/prod_short.md)] per gestire il lavoro. Per ulteriori informazioni, vedere [Gestire il lavoro tra più aziende nell'hub aziendale](company-hub.md).  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4Fnyw?rel=0]

È stata semplificata la procedura per invitare il contabile esterno. Aprire semplicemente la pagina **Utenti** e scegliere l'azione **Invita contabile esterno** nella barra multifunzione. Viene presentato un messaggio di posta elettronica nel quale è sufficiente aggiungere l'indirizzo di posta elettronica del contabile e inviare l'invito.  

> [!Note]  
> È necessario avere impostato il sistema di posta elettronica SMTP. Per ulteriori informazioni, vedere [Configurare la posta elettronica](admin-how-setup-email.md).  

<!-- ![Invite your accountant.](./media/finance-invite-accountant/invite-accountant.png)-->

> [!IMPORTANT]  
> L'indirizzo e-mail del contabile deve essere un indirizzo di lavoro che si basa su Azure Active Directory. Se il contabile utilizza un altro tipo di posta elettronica, l'invito non può essere inviato.
>
> Questo task richiede l'accesso alla gestione di utenti e licenze in Azure Active Directory. All'utente che invia questo invito deve essere assegnato il ruolo **Amministratore globale** o **Amministratore utente** nell'interfaccia di amministrazione di Microsoft 365. Per ulteriori informazioni, vedere [Informazioni sui ruoli di amministratore](/microsoft-365/admin/add-users/about-admin-roles) nell'interfaccia di amministrazione di Microsoft 365.  

### <a name="adding-your-accountant-to-your-microsoft-365-in-the-azure-portal"></a><a name="adding-your-accountant-to-your-microsoft-365-in-the-azure-portal"></a>Aggiunta del contabile a Microsoft 365 nel portale di Azure

Se l'amministratore o il partner di rivendita non desidera utilizzare la guida **Invita un contabile esterno**, possono aggiungere un utente esterno nel portale di Azure e assegnare a questo utente la licenza di *contabile esterno*. Per ulteriori informazioni, vedere [Avvio rapido: aggiunta di utenti guest alla directory nel portale di Azure](/azure/active-directory/b2b/b2b-quickstart-add-guest-users-portal).

#### <a name="to-add-your-accountant-as-a-guest-user"></a><a name="to-add-your-accountant-as-a-guest-user"></a>Per aggiungere il contabile come utente guest

1. Aprire il [Portale di Azure](https://portal.azure.com/).
2. Nel riquadro a sinistra selezionare **Azure Active Directory**.
3. In **Gestione**, selezionare **Utenti**.
4. Selezionare **Nuovo utente guest**.
5. Nella pagina **Nuovo utente**, selezionare **Invita utente** e aggiungere le informazioni sul contabile esterno.  

   Facoltativamente, includere un messaggio di benvenuto personale per il contabile per fargli sapere che lo stai aggiungendo a [!INCLUDE[prod_short](includes/prod_short.md)].

6. Selezionare **Invita** per inviare automaticamente l'invito. Viene visualizzata una notifica in alto a destra con il messaggio **L'utente è stato invitato**. 
7. Dopo aver inviato l'invito, l'account utente viene automaticamente aggiunto alla directory come guest.

Successivamente, è necessario assegnare una licenza al nuovo utente guest per [!INCLUDE[prod_short](includes/prod_short.md)].

#### <a name="to-give-your-accountant-access-to-your-"></a><a name="to-give-your-accountant-access-to-your-"></a>Per concedere al contabile l'accesso a [!INCLUDE[prod_short](includes/prod_short.md)]

1. Nel portale di Azure, per l'utente appena aggiunto, selezionare **Profilo** e quindi scegliere **Modifica**
2. Aggiornare il campo **Posizione di utilizzo** con il paese pertinente, quindi selezionare **Salva**.
3. Scegliere **Licenze** e quindi aprire **Assegnazioni**.
4. Scegliere la licenza **Dynamics 365 Business Central - Contabile esterno**.  
    
    Se questa licenza non è disponibile, contattare il partner rivenditore per aggiungere la licenza alla sottoscrizione.

    In particolare per scopi di valutazione in un tenant di prova, è invece possibile utilizzare una licenza **Dynamics 365 Business Central per IWs**. Tuttavia, non è possibile utilizzare questo tipo di licenza se [!INCLUDE[prod_short](includes/prod_short.md)] è già stato acquistato. 
5. Salvare l'assegnazione.

Se l'operazione viene completata, la licenza viene assegnata all'utente guest e viene creato l'account guest.

### <a name="importing-the-new-user-into-"></a><a name="importing-the-new-user-into-"></a>Importazione del nuovo utente in [!INCLUDE[prod_short](includes/prod_short.md)]

Il contabile riceverà un messaggio e-mail che lo informa che gli è stato concesso l'accesso ad Active Directory. Successivamente, è necessario assegnare l'accesso alla società giusta in [!INCLUDE[prod_short](includes/prod_short.md)].

#### <a name="to-add-the-accountant-to-the-right-company"></a><a name="to-add-the-accountant-to-the-right-company"></a>Per aggiungere il contabile alla società giusta

1. Aprire la società [!INCLUDE[prod_short](includes/prod_short.md)] a cui si desidera che il contabile acceda all'indirizzo [https://businesscentral.dynamics.com](https://businesscentral.dynamics.com).
2. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Utenti**, quindi scegli il collegamento correlato.  
3. Scegliere l'azione **Ottieni nuovi utenti da Microsoft 365**.

In tal modo l'account utente creato nel portale di Azure viene importato nella società. Per ulteriori informazioni, vedere [Per aggiungere un utente in Business Central](ui-how-users-permissions.md#adduser).  

Se si desidera consentire l'accesso a più società, è necessario accedere a ciascuna società e ripetere questo processo. In alternativa, è possibile aggiornare i gruppi di autorizzazioni per il profilo utente del contabile in [!INCLUDE[prod_short](includes/prod_short.md)], ad esempio assegnando il gruppo di utenti *D365 Bus Premium*. Per ulteriori informazioni, vedere [Assegnare autorizzazioni a utenti e gruppi](ui-define-granular-permissions.md).  

## <a name="see-also"></a><a name="see-also"></a>Vedere anche

[Finanze](finance.md)  
[Impostazione di dati finanziari](finance-setup-finance.md)  
[Contabilità generale e piano dei conti](finance-general-ledger.md)  
[Chiusura di anni e periodi](year-close-years-periods.md)  
[Utilizzare le dimensioni](finance-dimensions.md)  
[Analisi dei rendiconti finanziari in Excel](finance-analyze-excel.md)  
[Gestire il lavoro tra più aziende nell'hub aziendale](company-hub.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Impostazione di un'analisi di un flusso di cassa](finance-setup-cash-flow-analyses.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
