---
title: Utilizzo dei workflow
description: È possibile impostare e utilizzare i flussi di lavoro che collegano task di processi aziendali eseguiti da utenti diversi. Informazioni sui differenti passaggi da eseguire per iniziare a utilizzare i flussi di lavoro.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 92b32957bb7b20dda304be8a99bb17c5c5947498
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787009"
---
# <a name="using-workflows"></a>Utilizzo dei workflow
È possibile impostare e utilizzare i flussi di lavoro che collegano task di processi aziendali eseguiti da utenti diversi. I task di sistema, ad esempio la registrazione automatica, possono essere inclusi come passaggi nei flussi di lavoro e preceduti o seguiti da task degli utenti. La richiesta e la concessione dell'approvazione per creare nuovi record sono passaggi tipici del flusso di lavoro.  

 Prima di poter iniziare a utilizzare i flussi di lavoro, è necessario impostare gli utenti del flusso di lavoro, creare i flussi di lavoro, potenzialmente preceduti dalla personalizzazione del codice, e specificare la modalità di ricezione delle notifiche da parte degli utenti. Per ulteriori informazioni, vedere [Impostazione dei workflow](across-set-up-workflows.md).  

> [!NOTE]  
>  I passaggi di un flusso di lavoro tipici riguardano gli utenti che richiedono l'approvazione di attività e i responsabili dell'approvazione che accettano o rifiutano le richieste. Di conseguenza, molti argomenti che trattano l'utilizzo dei workflow fanno riferimento alle approvazioni.  

 Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.  

|**Task**|**Vedere**|  
|------------|-------------|  
|Impostare un flusso di lavoro per iniziare quando si verifica la prima spedizione Intrastat.|[Abilitare i workflow](across-how-to-enable-workflows.md)|  
|Richiedere l'approvazione di un task, come responsabile approvazione, accettare, declinare o delegare le approvazioni e inviare o visualizzare le notifiche di approvazione.|[Utilizzare i workflow di approvazione](across-how-use-approval-workflows.md)|  
|Creare le fasi del flusso di lavoro che limitano l'utilizzo di un certo tipo di record prima del verificarsi di un determinato evento, ad esempio l'approvazione del record.|[Limitare e consentire l'utilizzo di un record](across-how-to-restrict-and-allow-usage-of-a-record.md)|  
|Visualizzare istanze dei passaggi del flusso di lavoro con lo stato Completato.|[Visualizzare le istanze di fase workflow archiviate](across-how-to-view-archived-workflow-step-instances.md)|  
|Eliminare un flusso di lavoro che sicuramente non verrà più utilizzato.|[Eliminare i workflow](across-how-to-delete-workflows.md)|  

## <a name="see-also"></a>Vedi anche  
[Impostazione dei workflow](across-set-up-workflows.md)   
[Workflow](across-workflow.md)   
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]