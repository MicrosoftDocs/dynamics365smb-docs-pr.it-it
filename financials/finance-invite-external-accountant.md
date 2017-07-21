---
title: Aggiungere il contabile esterno a Financials | Documenti Microsoft
description: "Informazioni su come è possibile invitare un contabile esterno in Dynamics 365 for Financials."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting
ms.date: 06/23/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 1b9f88f02b198ae8da0f3359a3ce7799b9535739
ms.contentlocale: it-it
ms.lasthandoff: 07/07/2017


---
# <a name="invite-your-external-accountant-to-your-included365finincludesd365finmdmd"></a>Invitare il contabile esterno in [!INCLUDE[d365fin](includes/d365fin_md.md)]
Se viene utilizzato un contabile esterno per gestire i libri contabili e i rendiconti finanziari, è possibile invitarlo a [!INCLUDE[d365fin](includes/d365fin_md.md)] in modo che possa utilizzare i dati fiscali dell'azienda.

Dopo che il contabile ha eseguire l'accesso a [!INCLUDE[d365fin](includes/d365fin_md.md)], può utilizzare la Gestione ruolo utente **Contabile** che permette di accedere facilmente alle finestre più pertinenti al suo lavoro.  

> [!NOTE]  
>  Questa funzionalità richiede che l'esperienza sia impostata su **Suite**. Per ulteriori informazioni, vedere [Personalizzazione dell'esperienza utente di Financials](ui-experiences.md).  

## <a name="invite-your-accountant-to-your-included365finincludesd365finmdmd"></a>Invitare il contabile in [!INCLUDE[d365fin](includes/d365fin_md.md)]
Nella versione corrente di [!INCLUDE[d365fin](includes/d365fin_md.md)], per invitare un contabile esterno è necessario che un amministratore lo aggiunga al tenant di Active Directory. I passaggi da eseguire per questa operazione dipendono dal tipo di conto utilizzato per l'iscrizione a [!INCLUDE[d365fin](includes/d365fin_md.md)]. Questo argomento presuppone l'utilizzo di un account Office 365 che usa Microsoft Azure Active Directory.  

> [!TIP]  
>  È consigliabile contattare il partner [!INCLUDE[d365fin](includes/d365fin_md.md)] per assistenza.  

Se è stata attivata la sottoscrizione di [!INCLUDE[d365fin](includes/d365fin_md.md)] e non si utilizza più la società di valutazione, è disponibile un tenant di Azure Active Directory. L'amministratore o il partner [!INCLUDE[d365fin](includes/d365fin_md.md)] gestisce il tenant nel [portale di Azure](https://portal.azure.com). Nel portale è possibile aggiungere nuovi utenti e applicare o rimuovere le licenze. Per ulteriori informazioni, vedere [Panoramica del portale di Microsoft Azure](https://docs.microsoft.com/en-us/azure/azure-portal-overview).  

### <a name="separate-license"></a>Licenza separata
Uno dei tipi di licenza per [!INCLUDE[d365fin](includes/d365fin_md.md)] è la licenza *Contabile esterno*. Questo tipo di licenza è destinato a utenti quali i contabili esterni. In questo modo non è necessario acquistare una postazione aggiuntiva in Active Directory oppure utilizzare un account utente esistente [!INCLUDE[d365fin](includes/d365fin_md.md)] per il contabile esterno. Ad esempio, se la sottoscrizione corrente di Office 365 include 10 utenti per [!INCLUDE[d365fin](includes/d365fin_md.md)] e attualmente si utilizzano 10 licenze *Utente completo*, l'amministratore può semplicemente aggiungere il contabile esterno come utente guest nel portale di Azure e assegnare all'utente la licenza *Contabile esterno* senza alcun costo aggiuntivo. Tuttavia, è possibile avere un solo utente con la licenza *Contabile esterno*. Se si desidera aggiungere altri utenti, è necessario aggiornare di conseguenza la sottoscrizione di Office 365.  

## <a name="see-also"></a>Vedi anche
[Finanze](finance.md)  
[Esperienze contabile in Dynamics 365 for Financials](finance-accounting.md)  
[Financials per contabili in Microsoft.com](https://www.microsoft.com/en-us/dynamics365/financial-insights-for-accountants)  

