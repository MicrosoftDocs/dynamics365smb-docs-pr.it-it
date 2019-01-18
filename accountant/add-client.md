---
title: "Coinvolgere i clienti nell'esperienza di contabilità in Dynamics 365 | Documenti Microsoft"
description: Informazioni su come aggiungere i clienti esistenti in Accountant Hub per Dynamics 365.
author: edupont04
ms.service: dynamics365-accountant
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 11/23/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: c7f0af8d3535f558567cd40c841909cd151ce313
ms.contentlocale: it-it
ms.lasthandoff: 11/26/2018

---
# <a name="add-clients-to-your-dashboard-in-include-d365acclongincludesd365acclongmdmd"></a>Aggiungere clienti al dashboard in [!INCLUDE [d365acc_long](includes/d365acc_long_md.md)]
[!INCLUDE [d365fin_early_release](includes/d365fin_early_release.md.md)]

È possibile aggiungere un client utilizzando la pagina **Client**, che è possibile aprire scegliendo l'azione **Gestione client** nella barra multifunzione. Scegliere **Nuovo** e compilare i campi.  

> [!div class="mx-imgBorder"]
> ![Aggiungere un cliente](./media/accountant-add-client/manage-client.png)

I dati della scheda per ciascun client sono specificati dall'utente e possono essere modificati secondo le necessità. Tuttavia, il campo **URL client** è fondamentale, indica come è possibile accedere a [!INCLUDE [d365fin](includes/d365fin_md.md)] di ogni client. Utilizzare l'azione **Convalida URL client** nella barra multifunzione per verificare che sia stato inserito il collegamento corretto. La URL che è necessario immettere indirizza alla soluzione [!INCLUDE [d365fin](includes/d365fin_md.md)] del client e include il relativo indirizzo di dominio. Ad esempio, se è stato specificato un dominio come MyBusiness.com, il collegamento alla soluzione [!INCLUDE [d365fin](includes/d365fin_md.md)] sarà *https://businesscentral.dynamics.com/mybusiness.com?redirectedfromsignup=1*.  

> [!NOTE]
>  Prima dell'aggiornamento di maggio 2018, l'URL specificato aveva un formato diverso con il nome dell'azienda del cliente all'inizio. Nella versione corrente di [!INCLUDE [d365fin](includes/d365fin_md.md)], il formato è ```https://businesscentral.dynamics.com/clientdomain?redirectedfromsignup=1```, dove ```clientdomain``` rappresenta il dominio del client.  

L'URL del client viene quindi utilizzato quando si sceglie la voce di menu **Vai a società** nel dashboard di [!INCLUDE [d365acc](includes/d365acc_md.md)].  

### <a name="get-invited-to-a-clients-include-d365finlongincludesd365finlongmdmd"></a>Ottenere l'invito per [!INCLUDE [d365fin_long](includes/d365fin_long_md.md)] in un client
Una società che utilizza [!INCLUDE [d365fin](includes/d365fin_md.md)] può invitare un utente a [!INCLUDE [d365fin](includes/d365fin_md.md)] come contabile esterno. Per ottenere l'invito, è necessario indirizzo e-mail utilizzato con [!INCLUDE [d365acc](includes/d365acc_md.md)], ad esempio <em>me@accountant.com</em>. L'amministratore del client può quindi aggiungere l'utente al sistema tramite la procedura guidata **Invita contabile esterno**.  

Si riceverà di conseguenza un messaggio di posta elettronica dal cliente contenente collegamenti a [!INCLUDE [d365fin](includes/d365fin_md.md)] Il primo collegamento è un invito all'accesso alla società. Apri il collegamento e accetta i passaggi per l'aggiunta a [!INCLUDE [d365fin](includes/d365fin_md.md)] del cliente. Il secondo collegamento è per l'aggiunta del cliente al dashboard in [!INCLUDE [d365acc](includes/d365acc_md.md)] come descritto sopra.  

Quando è stato accettato l'invito si è connessi ed è possibile accedere ai dati finanziari del cliente tramite la Gestione ruolo utente **Contabile**. Per ulteriori informazioni, vedere [Esperienze di contabile in [!INCLUDE[d365fin](includes/d365fin_md.md)]](/dynamics365/business-central/finance-accounting?toc=/dynamics365/accountants/toc.json).  

## <a name="see-also"></a>Vedi anche
[Introduzione a [!INCLUDE[d365acc](includes/d365acc_md.md)]](get-started.md)  
[Risoluzione dei problemi di [!INCLUDE[d365acc](includes/d365acc_md.md)]](troubleshooting.md)  

