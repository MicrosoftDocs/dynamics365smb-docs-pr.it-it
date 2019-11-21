---
title: Connettere i dati a Flow| Documenti Microsoft
description: È possibile rendere disponibili i dati di Business Central come origine dati e specificare un URL OData dei service Web per creare un workflow automatizzato.
documentationcenter: ''
author: bmeier90
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 10/01/2019
ms.author: bmeier
ms.openlocfilehash: a46692503b19ddad57c4a68d0f29b588d84f5c9e
ms.sourcegitcommit: cd5d3d288feee76d058d325720135275f4c8ad85
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/08/2019
ms.locfileid: "2775453"
---
# <a name="using-included365finincludesd365fin_mdmd-in-an-automated-workflow"></a>Uso di [!INCLUDE[d365fin](includes/d365fin_md.md)] in un workflow automatizzato
È possibile utilizzare i dati di [!INCLUDE[d365fin](includes/d365fin_md.md)] come parte di un flusso di lavoro in Microsoft Flow.

> [!NOTE]
> Oltre a Microsoft Flow, è possibile utilizzare la funzionalità Workflow in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Si noti che sebbene siano presenti due sistemi del flusso di lavoro, qualsiasi modello di flusso creato con Microsoft Flow viene aggiunta all'elenco dei flussi di lavoro in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Per ulteriori informazioni, vedere [Workflow](across-workflow.md).  

> [!NOTE]  
> È necessario disporre di un account valido con [!INCLUDE[d365fin](includes/d365fin_md.md)] e con Flow.  

## <a name="to-add-included365finincludesd365fin_mdmd-as-a-data-source-in-flow"></a>Per aggiungere [!INCLUDE[d365fin](includes/d365fin_md.md)] come origine dati in Flow
1. Nel browser passare a [flow.microsoft.com](https://flow.microsoft.com/en-us/), quindi accedere.
2. Scegliere **I miei flussi** dalla barra nella parte superiore della pagina.
3. Sono disponibili 3 modi per creare un flusso: **Inizia da modello**, **Inizia da zero** e **Inizia da un connettore**. Un modello è un flusso predefinito che è stato creato per l'utente. Per utilizzare un modello, selezionarlo semplicemente e creare una connessione per ogni servizio utilizato dal modello. Con le opzioni **Inizia da zero** e **Inizia da un connettore**, è possibile creare un nuovo flusso da zero.
4. Per creare un flusso da zero, nella pagina **I miei flussi** selezionare le opzioni **Inizia da zero** e **Flusso automatizzato**.
5. Cercare il connettore **Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]**.
6. Definire un nome e scegliere il trigger da utilizzare per il flusso.
7. Selezionare uno dei trigger [!INCLUDE[d365fin](includes/d365fin_md.md)] disponibili dall'elenco dei trigger:  
    
    *Quando viene richiesta l'approvazione del fornitore*,    
    *Approvazione riga registrazioni COGE necessaria*,    
    *Quando viene modificato un record*,    
    *Quando viene modificato un record*,    
    *Quando un record viene creato*,    
    *Quando viene modificato un record*,    
    *Quando viene richiesta l'approvazione batch giornale di registrazione generale*,   
    *Quando viene richiesta l'approvazione del cliente*,   
    *Quando viene richiesta l'approvazione di un elemento*,    
    *Quando viene richiesta l'approvazione di un documento di acquisto* oppure     
     *Quando viene richiesta l'approvazione di un documento di vendita*.
     
8. Il flusso richiederà di selezionare un ambiente e una società all'interno del tenant [!INCLUDE[d365fin](includes/d365fin_md.md)], nonché tutti i termini nei dati che si desidera ascoltare.

> [!NOTE]  
>   Il connettore [!INCLUDE[d365fin](includes/d365fin_md.md)] per Microsoft Flow supporta più ambienti di produzione e sandbox. Se non sono stati creati più ambienti di produzione o sandbox, **Produzione** è l'unica opzione disponibile che è possibile scegliere. 

A questo punto, è stata stabilita correttamente la connessione ai dati di Business Central e si è pronti per iniziare a creare il flusso.

9. Per creare da un modello, selezionare l'opzione **Inizia da modello**.
10. Cercare i modelli **Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]**.
11. Dall'elenco di modelli disponibili, selezionare uno dei modelli e scegliere **Crea**.  

    *Richiesta di approvazione per ordine di vendita Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]*,  
    *Richiesta di approvazione per offerta di vendita Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]*,  
    *Richiesta di approvazione per fattura di vendita Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]*,  
    *Richiesta di approvazione per nota di credito di vendita Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]*,  
    *Richiesta di approvazione per cliente Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]*,  
    *Richiesta di approvazione per acquisto Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]*,  
    *Richiesta di approvazione per fattura d'acquisto Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]*,  
    *Richiesta di approvazione per nota di credito di acquisto Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]*,  
    *Richiesta di approvazione per articolo Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]*,  
    *Richiesta di approvazione per fornitore Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]*,  
    *Richiesta di approvazione per batch registrazioni COGE Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]* oppure    
    *Richiesta di approvazione per righe registrazioni COGE Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]*,  
12. Flow visualizzerà un elenco di servizi utilizzati nel modello Flow e tenterà di connettersi automaticamente a tali servizi. Se non si è precedentemente connessi a un servizio, verrà richiesto di accedere a ciascuno dei servizi a cui è necessario connettersi. Un segno di spunta verde verrà visualizzato accanto a ciascun servizio una volta stabilita correttamente una connessione. Selezionare **Continua**.
13. Flow richiederà la selezione di un ambiente e di una società nel tenant [!INCLUDE[d365fin_md](includes/d365fin_md.md)]. Poiché ogni fase del flusso è indipendente dalla successiva, è possibile che sia necessario definire l'ambiente e la società più volte quando si utilizza un modello di flusso di [!INCLUDE[d365fin_md](includes/d365fin_md.md)].

Per ulteriori informazioni, vedere la [Documentazione di Flow](/flow/getting-started).

## <a name="see-also"></a>Vedere anche
[Introduzione](product-get-started.md)  
[Workflow](across-workflow.md)  
[Importazione dei dati aziendali da altri sistemi contabili](across-import-data-configuration-packages.md)  
[Assegnare autorizzazioni a utenti e gruppi](ui-define-granular-permissions.md)   
[Gestire flussi di lavoro [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](across-use-workflows.md)  
[Setup utente approvazione](across-how-to-set-up-approval-users.md)  
[Impostazione di [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finanze](finance.md)  
