---
title: Visualizzare lo stato di una sincronizzazione | Microsoft Docs
description: Ottenere informazioni su come visualizzare lo stato di un singolo processo di sincronizzazione.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 11e29674c2d12031fdf4e7f66e767be4fcc74795
ms.sourcegitcommit: 04581558f6c5488c705a7ac392cf297be10b5f4f
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/06/2019
ms.locfileid: "1620886"
---
# <a name="view-the-status-of-a-synchronization"></a>Visualizzare lo stato di una sincronizzazione
È possibile visualizzare lo stato dei singoli processi di sincronizzazione che sono stati eseguiti per l'integrazione di [!INCLUDE[crm_md](includes/crm_md.md)]. Ciò include i processi di sincronizzazione che sono stati eseguiti dai processi di sincronizzazione manuale e della coda processi sui record del client [!INCLUDE[d365fin](includes/d365fin_md.md)]. Ciò risulta utile per risolvere problemi di sincronizzazione perché consente di accedere ai dettagli degli errori specifici.

### <a name="to-view-synchronization-issues-for-coupled-records"></a>Per visualizzare problemi di sincronizzazione relativi a record associati
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Errori di sincronizzazione dati associati** e quindi scegliere il collegamento correlato.
2. Nella pagina **Errori di sincronizzazione dati associati** vengono visualizzati i problemi verificatisi durante la sincronizzazione di record associati. È possibile filtrare e ordinare record ed eseguire azioni come **Ripristina** o **Elimina record** per risolvere i problemi singolarmente.

### <a name="to-view-synchronization-log-for-specific-manually-synchronized-record"></a>Per visualizzare il registro di sincronizzazione per specifici record (sincronizzati manualmente)
1. Aprire, ad esempio, un cliente, un articolo o qualunque altro record che esegue la sincronizzazione tra [!INCLUDE[d365fin](includes/d365fin_md.md)] e Sales
2. Scegliere l'azione **Registro sincronizzazione** per visualizzare il registro di sincronizzazione per un record selezionato. Ad esempio, un cliente specifico sincronizzato manualmente.

## <a name="see-also"></a>Vedere anche  
[Configurare l'integrazione di Dynamics 365 for Sales in Business Central](admin-setting-up-integration-with-dynamics-sales.md)  
[Utilizzo di Dynamics 365 for Sales da Business Central](marketing-integrate-dynamicscrm.md)
