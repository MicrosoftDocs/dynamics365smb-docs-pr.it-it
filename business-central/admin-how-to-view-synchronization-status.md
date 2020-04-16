---
title: Visualizzare lo stato dei processi di sincronizzazione | Microsoft Docs
description: Informazioni su come visualizzare lo stato dopo la sincronizzazione di record associati.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: 2371c61c36a17df93ccc1a24c588b12613f5c380
ms.sourcegitcommit: d67328e1992c9a754b14c7267ab11312c80c38dd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196617"
---
# <a name="view-the-status-of-synchronization-jobs"></a>Visualizzare lo stato dei processi d sincronizzazione
Utilizzare la pagina **Errori di sincronizzazione dati associati** per visualizzare lo stato dei lavori di sincronizzazione che sono stati eseguiti per i record associati in un'integrazione di Common Data Service o [!INCLUDE[crm_md](includes/crm_md.md)]. Ciò include i processi eseguiti dalla coda processi e i processi di sincronizzazione manuale eseguiti sui record di [!INCLUDE[d365fin](includes/d365fin_md.md)]. Ad esempio, la visualizzazione del relativo stato è utile per risolvere problemi in quanto consente di accedere ai dettagli degli errori relativi ai record associati. In genere, questi tipi di errori sono causati da azioni dell'utente, ad esempio, quando:  

* Due persone hanno apportato una modifica allo stesso record in entrambe le app aziendali.
* Qualcuno ha cancellato un record in una delle app, ma non entrambe.

> [!Note]
> La pagina **Errori di sincronizzazione dati associati**mostra informazioni sui processi relativi ai record associati. Se si risolvono tutti gli errori ma i record continuano a non essere sincronizzati, è possibile che il problema sia dovuto all'impostazione per l'integrazione. In genere, l'amministratore dovrà risolvere questi tipi di errori.   

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098171]

## <a name="to-view-and-resolve-synchronization-errors-for-coupled-records"></a>Per visualizzare e risolvere gli errori di sincronizzazione per record associati
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Errori di sincronizzazione dati associati** e quindi scegliere il collegamento correlato.
2. Nella pagina **Errori di sincronizzazione dati associati** vengono visualizzati i problemi verificatisi durante la sincronizzazione di record associati. La seguente tabella include le azioni che è possibile utilizzare per risolvere i problemi singolarmente:

|Azione|Descrizione|
|----|----|
|**Rimuovi associazione**|Elimina l'associazione dei record, che non verranno più sincronizzati. Per riprendere la sincronizzazione dei record, è necessario associarli nuovamente.|
|**Riprova**|Per ogni record in cui viene rilevato un errore, la sincronizzazione viene saltata a meno che non si risolva il problema manualmente. Riprova includerà il record nella prossima sincronizzazione.|
|**Sincronizza**|L'app proverà a risolvere un conflitto in cui un record è stato modificato in entrambe le app aziendali. È possibile scegliere la versione del record da utilizzare in entrambe le app.|
|**Ripristina record**ed **Elimina record**|Sono utili quando un record è stato eliminato in una delle app aziendali. Elimina record elimina il record nell'app in cui è ancora presente. Ripristina record ricrea il record nell'app aziendale in cui è stato eliminato.|

## <a name="to-view-the-synchronization-log-for-a-specific-manually-synchronized-record"></a>Per visualizzare il registro di sincronizzazione per uno specifico record (sincronizzato manualmente)
1. Aprire, ad esempio, un cliente, un articolo o qualunque altro record che esegue la sincronizzazione dei dati tra [!INCLUDE[d365fin](includes/d365fin_md.md)] e Common Data Service o [!INCLUDE[crm_md](includes/crm_md.md)].
2. Scegliere l'azione **Registro sincronizzazione** per visualizzare il registro di sincronizzazione per un record selezionato. Ad esempio, un cliente specifico sincronizzato manualmente.

## <a name="see-also"></a>Vedere anche  
[Impostazione di account utente per l'integrazione con Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md)  
[Utilizzo di Dynamics 365 Sales da Business Central](marketing-integrate-dynamicscrm.md)
