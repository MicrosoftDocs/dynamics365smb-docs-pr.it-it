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
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: 79ed5e1b7200a668be2aa078531fd68e0131b6ff
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2019
ms.locfileid: "2302597"
---
# <a name="accountant-experiences-in-included365fin_longincludesd365fin_long_mdmd"></a>Esperienze di contabile in [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]
Qualsiasi attività deve avere i suoi libri e firmare la contabilità. Alcuni aziende hanno un contabile esterno e altre hanno un contabile interno. Senza tenere conto del tipo di contabile in questione, è possibile utilizzare la Gestione ruolo utente **Contabile** come Home page in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Da questa pagina, è possibile accedere a tutte le pagine necessarie per lavorare.  

## <a name="accountant-role-center"></a>Gestione ruolo utente Contabile
La Gestione ruolo utente è un dashboard con riquadri di attività che indicano le informazioni di base in tempo reale e consentono di accedere rapidamente ai dati. La barra multifunzione nella parte superiore della pagina consente di accedere a più azioni, ad esempio l'apertura in Excel di report e rendiconti finanziari di uso più comune. Nella barra di spostamento superiore, è possibile passare rapidamente tra le liste che si utilizzano con maggiore frequenza. Qui vengono visualizzate altre aree, ad esempio **Documenti registrati** con i diversi tipi di documenti registrati dalla società.  

Se non si ha familiarità con [!INCLUDE[d365fin](includes/d365fin_md.md)], è possibile guardare una serie di video direttamente dalla Gestione ruolo utente. È inoltre possibile avviare una **Introduzione** che illustra i punti chiave.  

## <a name="accountant-hub"></a>Accountant Hub
Se si è un contabile con vari clienti, è possibile utilizzare [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)] per avere una panoramica più precisa dei client. Dal portale, è possibile accedere al tenant di ogni client in [!INCLUDE[d365fin](includes/d365fin_md.md)] e utilizzare la Gestione ruolo utente Contabile come descritto sopra. Per ulteriori informazioni, vedi [Benvenuto in [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]](/dynamics365/accountants/index).  

> [!NOTE]
> [!INCLUDE [d365acc_long_md](includes/d365acc_long_md.md)] è attualmente è in versione di anteprima pubblica in un numero limitato di mercati.

## <a name="inviting-your-external-accountant-to-your-included365finincludesd365fin_mdmd"></a>Invitare il contabile esterno in [!INCLUDE[d365fin](includes/d365fin_md.md)]
Se viene utilizzato un contabile esterno per gestire i libri contabili e i rendiconti finanziari, è possibile invitarlo a [!INCLUDE[d365fin](includes/d365fin_md.md)] in modo che possa utilizzare i dati fiscali dell'azienda.

Dopo che il contabile ha eseguire l'accesso a [!INCLUDE[d365fin](includes/d365fin_md.md)], può utilizzare la Gestione ruolo utente **Contabile** che permette di accedere facilmente alle pagine più pertinenti al suo lavoro.  

È stata semplificata la procedura per invitare il contabile esterno. Aprire semplicemente la pagina **Utenti** e scegliere l'azione **Invita contabile esterno** nella barra multifunzione. Viene presentato un messaggio di posta elettronica nel quale è sufficiente aggiungere l'indirizzo di posta elettronica del contabile e inviare l'invito.  

![Invitare il contabile](./media/finance-invite-accountant/invite-accountant.png)

> [!TIP]  
> È necessario avere impostato il sistema di posta elettronica SMTP. Questa operazione può essere svolta autonomamente oppure è possibile rivolgersi al proprio partner [!INCLUDE[d365fin](includes/d365fin_md.md)]. È inoltre necessario essere connessi a [!INCLUDE[d365fin](includes/d365fin_md.md)] come amministratore utente, non come imprenditore o altri utenti. Infine, è necessario aver lasciato la società di prova in modo da avere un amministratore di Azure Active Directory.  

> [!IMPORTANT]  
> L'indirizzo e-mail del contabile deve essere un indirizzo di lavoro che si basa su Azure Active Directory. Se il contabile utilizza un altro tipo di posta elettronica, l'invito non può essere inviato.  

### <a name="separate-license"></a>Licenza separata
Dietro le quinte, il contabile viene aggiunto al tenant di Active Directory in uso. L'amministratore può verificare che il contabile accetti l'invito e gli sia assegnato la licenza corretta. I passaggi da eseguire per questa operazione dipendono dal tipo di conto utilizzato per l'iscrizione a [!INCLUDE[d365fin](includes/d365fin_md.md)]. Questo argomento presuppone l'utilizzo di un account Office 365 che usa Microsoft Azure Active Directory.  

Se è stata attivata la sottoscrizione di [!INCLUDE[d365fin](includes/d365fin_md.md)] e non si utilizza più la società di valutazione, è disponibile un tenant di Azure Active Directory. L'amministratore o il partner [!INCLUDE[d365fin](includes/d365fin_md.md)] gestisce il tenant nel [portale di Azure](https://portal.azure.com). Nel portale è possibile aggiungere nuovi utenti e applicare o rimuovere le licenze. Per ulteriori informazioni, vedere [Panoramica del portale di Microsoft Azure](https://docs.microsoft.com/en-us/azure/azure-portal-overview).  

Uno dei tipi di licenza per [!INCLUDE[d365fin](includes/d365fin_md.md)] è la licenza *Contabile esterno*. Questo tipo di licenza è destinato a utenti quali i contabili esterni. In questo modo non è necessario acquistare una postazione aggiuntiva in Active Directory oppure utilizzare un account utente esistente [!INCLUDE[d365fin](includes/d365fin_md.md)] per il contabile esterno. Ad esempio, se la sottoscrizione corrente di Office 365 include 10 utenti per [!INCLUDE[d365fin](includes/d365fin_md.md)] e attualmente si utilizzano 10 licenze *Utente completo*, l'amministratore può semplicemente aggiungere il contabile esterno come utente guest nel portale di Azure e assegnargli la licenza *Contabile esterno* senza alcun costo aggiuntivo. Tuttavia, è possibile avere un solo utente con la licenza *Contabile esterno*. Se si desidera aggiungere altri utenti, è necessario aggiornare di conseguenza la sottoscrizione di Office 365.

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
[Dynamics 365 - Accountant Hub su Microsoft.com](https://www.microsoft.com/en-us/dynamics365/financial-insights-for-accountants)  
