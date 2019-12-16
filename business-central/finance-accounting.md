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
ms.date: 12/02/2019
ms.author: edupont
ms.openlocfilehash: c575c0e482ebe4d34c9b699b22747486651efe04
ms.sourcegitcommit: b6e506a45a1cd632294bafa1c959746cc3a144f6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/06/2019
ms.locfileid: "2896135"
---
# <a name="accountant-experiences-in-included365fin_longincludesd365fin_long_mdmd"></a>Esperienze di contabile in [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]
Qualsiasi attività deve avere i suoi libri e firmare la contabilità. Alcuni aziende hanno un contabile esterno e altre hanno un contabile interno. Senza tenere conto del tipo di contabile in questione, è possibile utilizzare la Gestione ruolo utente **Contabile** come Home page in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Da questa pagina, è possibile accedere a tutte le pagine necessarie per lavorare.  

## <a name="accountant-role-center"></a>Gestione ruolo utente Contabile
La Gestione ruolo utente è un dashboard con riquadri di attività che indicano le informazioni di base in tempo reale e consentono di accedere rapidamente ai dati. La barra multifunzione nella parte superiore della pagina consente di accedere a più azioni, ad esempio l'apertura in Excel di report e rendiconti finanziari di uso più comune. Nella barra di spostamento superiore, è possibile passare rapidamente tra le liste che si utilizzano con maggiore frequenza. Qui vengono visualizzate altre aree, ad esempio **Documenti registrati** con i diversi tipi di documenti registrati dalla società.  

Se non si ha familiarità con [!INCLUDE[d365fin](includes/d365fin_md.md)], è possibile guardare una serie di video direttamente dalla Gestione ruolo utente. È inoltre possibile avviare una **Introduzione** che illustra i punti chiave.  

## <a name="inviteaccountant"></a>Invitare il contabile esterno in [!INCLUDE[d365fin](includes/d365fin_md.md)]
Se viene utilizzato un contabile esterno per gestire i libri contabili e i rendiconti finanziari, è possibile invitarlo a [!INCLUDE[d365fin](includes/d365fin_md.md)] in modo che possa utilizzare i dati fiscali dell'azienda.

Dopo che il contabile ha eseguire l'accesso a [!INCLUDE[d365fin](includes/d365fin_md.md)], può utilizzare la Gestione ruolo utente **Contabile** che permette di accedere facilmente alle pagine più pertinenti al suo lavoro.  

È stata semplificata la procedura per invitare il contabile esterno. Aprire semplicemente la pagina **Utenti** e scegliere l'azione **Invita contabile esterno** nella barra multifunzione. Viene presentato un messaggio di posta elettronica nel quale è sufficiente aggiungere l'indirizzo di posta elettronica del contabile e inviare l'invito.  
> [!Note]  
> È necessario avere impostato il sistema di posta elettronica SMTP. Per ulteriori informazioni, vedere [Imposta indirizzo e-mail](admin-how-setup-email.md).   

![Invitare il contabile](./media/finance-invite-accountant/invite-accountant.png)

> [!IMPORTANT]  
> L'indirizzo e-mail del contabile deve essere un indirizzo di lavoro che si basa su Azure Active Directory. Se il contabile utilizza un altro tipo di posta elettronica, l'invito non può essere inviato.  

### <a name="behind-the-scenes"></a>Dietro le quinte
[!INCLUDE[d365fin](includes/d365fin_md.md)] include tre licenze di tipo Contabile esterno. Se la società utilizza un contabile esterno, è possibile consentire l'accesso a [!INCLUDE[d365fin](includes/d365fin_md.md)] assegnandogli tale licenza. Per ulteriori informazioni sulle licenze, consultare la [Guida alle licenze di Microsoft Dynamics 365 Busincess Central](https://go.microsoft.com/fwlink/?LinkId=871590). 

Se la sottoscrizione ha ancora una licenza disponibile, l'amministratore o il partner rivenditore può aggiungere un utente esterno tramite il portale di Azure e assegnare a questo utente la licenza Contabile esterno. Per ulteriori informazioni, vedere [Aggiungere gli utenti della collaborazione B2B di Azure Active Directory nel portale di Azure ](/azure/active-directory/b2b/add-users-administrator).

È quindi possibile invitare il contabile da [!INCLUDE[d365fin](includes/d365fin_md.md)] usando la guida al setup assistito **Invita contabile esterno**. Tuttavia, poiché questa attività richiede l'accesso alla gestione di utenti e licenze in Azure Active Directory, all'utente che invia questo invito deve essere assegnato il ruolo **Amministratore globale** o **Amministratore utente** nell'interfaccia di amministrazione di Office 365. Per ulteriori informazioni, vedere [Informazioni sui ruoli di amministratore](/office365/admin/add-users/about-admin-roles) nell'interfaccia di amministrazione di Office 365. 

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
