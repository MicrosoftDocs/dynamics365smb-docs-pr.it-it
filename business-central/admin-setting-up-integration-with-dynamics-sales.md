---
title: Impostazione di account utente per l'integrazione con Dynamics 365 for Sales | Microsoft Docs
description: Ottenere informazioni su come impostare account utente che le app utilizzano per scambiare dati e che le persone utilizzano per accedere ai dati nelle app e per sincronizzarli.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: c318346c62b7776a550a77a2947173e33d5f17c0
ms.sourcegitcommit: addfb47612cc2e4e98dfd7e338b6f41cde405d5c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2019
ms.locfileid: "940252"
---
# <a name="setting-up-user-accounts-for-integrating-with-dynamics-365-for-sales"></a>Impostazione di account utente per l'integrazione con Dynamics 365 for Sales
In questo articolo viene fornita una panoramica su come impostare account utente necessari per integrare [!INCLUDE[crm_md](includes/crm_md.md)] con [!INCLUDE[d365fin](includes/d365fin_md.md)].  

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2085500]

## <a name="setting-up-the-admininstrator-user-account-in-sales"></a>Impostazione dell'account utente amministratore in Sales
È necessario aggiungere l'account utente amministratore per [!INCLUDE[d365fin](includes/d365fin_md.md)] come utente in [!INCLUDE[crm_md](includes/crm_md.md)] e quindi promuovere l'utente ad amministratore in [!INCLUDE[crm_md](includes/crm_md.md)]. L'account utente amministratore deve anche avere il ruolo Addetto personalizzazione sistema e almeno un altro ruolo utente non amministrativo, ad esempio Manager vendite, in [!INCLUDE[crm_md](includes/crm_md.md)].

## <a name="setting-up-the-user-account-for-the-integration"></a>Impostazione dell'account utente per l'integrazione
È necessario creare un account utente dedicato nella sottoscrizione di Office 365 che [!INCLUDE[d365fin](includes/d365fin_md.md)] e [!INCLUDE[crm_md](includes/crm_md.md)] possono utilizzare per sincronizzare i dati. Questo account utente deve poter accedere a [!INCLUDE[crm_md](includes/crm_md.md)], il che significa che tale utente deve disporre di una licenza per [!INCLUDE[crm_md](includes/crm_md.md)]. Questo account deve inoltre essere un account non interattivo in [!INCLUDE[crm_md](includes/crm_md.md)]. Per ulteriori informazioni su come creare utenti in [!INCLUDE[crm_md](includes/crm_md.md)], vedere [Gestire la sicurezza, utenti e team](http://go.microsoft.com/fwlink/?LinkID=616518). Dopo che la connessione è impostata, [!INCLUDE[d365fin](includes/d365fin_md.md)] assegnerà all'account utente i ruoli di sicurezza di cui necessita in [!INCLUDE[d365fin](includes/d365fin_md.md)].

![Guida al setup assistito che mostra dove immettere le credenziali utente per la sincronizzazione](media/sync-user-setup.png "Visualizzazione della pagina della guida al setup assistito che mostra dove immettere le credenziali utente per la sincronizzazione")

> [!IMPORTANT]  
> Non utilizzare l'account amministratore per [!INCLUDE[crm_md](includes/crm_md.md)] per la sincronizzazione. In caso contrario, la sincronizzazione verrà interrotta.
> Inoltre, per evitare una sincronizzazione costante, le modifiche ai dati eseguite dall'account utente di integrazione non vengono sincronizzate. <!--What changes would this account make?--> Dopo la connessione, si consiglia di impostare la modalità di accesso per l'account utente per l'integrazione sulla modalità non interattiva in [!INCLUDE[crm_md](includes/crm_md.md)]. Per ulteriori informazioni, vedere [Creare un account utente non interattivo](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#create-a-non-interactive-user-account).

## <a name="setting-up-accounts-for-sales-people"></a>Impostazione di account per agenti
È necessario creare account utente in [!INCLUDE[crm_md](includes/crm_md.md)] per gli agenti da [!INCLUDE[d365fin](includes/d365fin_md.md)]. Per semplificare tale operazione, l'interfaccia di amministrazione di Microsoft 365 offre un modello di Excel che è possibile utilizzare. Nella pagina **Utenti attivi** scegliere **Altro**, quindi **Importa più utenti**. Scegliere **Scarica un file CSV solo con le intestazioni** e quindi immettere le informazioni per gli agenti. Per visualizzare un esempio, scegliere **Scarica un file CSV con le intestazioni ed esempi di informazioni degli utenti**. Dopo l'immissione delle informazioni relative agli utenti, il passaggio successivo nel processo di importazione consiste nell'assegnare licenze per il piano Dynamics 365 Customer Engagement agli utenti.  

Dopo aver importato gli utenti e assegnato loro le licenze per Dynamics 365 Customer Engagement, è necessario assegnare gli utenti al ruolo **Agente** in [!INCLUDE[crm_md](includes/crm_md.md)].

![Associazione di agenti e utenti in Dynamics 365 for Sales](media/couple-salespeople.png "Visualizzazione dell'associazione di agenti e utenti in Dynamics 365 for Sales")

## <a name="see-also"></a>Vedere anche  
[Integrazione con Dynamics 365 for Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
