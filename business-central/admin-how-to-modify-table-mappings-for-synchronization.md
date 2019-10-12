---
title: Modificare i mapping di tabella per la sincronizzazione | Microsoft Docs
description: Ottenere informazioni su come modificare i mapping di tabella che vengono utilizzati quando si sincronizzano dati tra Business Central e Dynamics 365 Sales.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize, table mapping
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 505c1427c63a0a6f9e68980ea0ff05c93918ea60
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2019
ms.locfileid: "2308077"
---
# <a name="modify-table-mappings-for-synchronization"></a>Modificare i mapping di tabella per la sincronizzazione
Un mapping di tabella di integrazione collega una tabella di [!INCLUDE[d365fin](includes/d365fin_md.md)] a un tabella di integrazione per l'entità di [!INCLUDE[crm_md](includes/crm_md.md)]. Per ogni entità di [!INCLUDE[crm_md](includes/crm_md.md)] che si desidera sincronizzare con i dati corrispondenti in [!INCLUDE[d365fin](includes/d365fin_md.md)], deve esserci un corrispondente mapping di tabella di integrazione. Un mapping di tabella di integrazione comprende diverse impostazioni che consentono di verificare come i record nella tabella di [!INCLUDE[d365fin](includes/d365fin_md.md)] e un'entità di [!INCLUDE[crm_md](includes/crm_md.md)] vengono sincronizzati dai processi di sincronizzazione di integrazione corrispondenti.  

## <a name="filtering-records"></a>Filtro dei record  
 Se non si desidera sincronizzare tutti i record per un'entità di [!INCLUDE[crm_md](includes/crm_md.md)] o una tabella di [!INCLUDE[d365fin](includes/d365fin_md.md)] specifica, è possibile impostare i filtri per limitare i record che vengono sincronizzati. I filtri vengono impostati nella pagina **Mapping tabella integrazione**.  

#### <a name="to-filter-records-for-synchronization"></a>Per filtrare record per la sincronizzazione  
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Mapping tabella integrazione** e quindi scegliere il collegamento correlato.

2.  Per filtrare i record di [!INCLUDE[d365fin](includes/d365fin_md.md)], impostare il campo **Filtro tabella**.  

3.  Per filtrare i record di [!INCLUDE[crm_md](includes/crm_md.md)], impostare il campo **Filtro tabella integrazione**.  

## <a name="creating-new-records"></a>Creazione di nuovi record  
 Per impostazione predefinita, solo i record di [!INCLUDE[d365fin](includes/d365fin_md.md)]e [!INCLUDE[crm_md](includes/crm_md.md)] associati verranno sincronizzati dai processi di sincronizzazione di integrazione. È possibile impostare i mapping di tabella in modo che i nuovi record vengano creati nella destinazione (ad esempio [!INCLUDE[d365fin](includes/d365fin_md.md)]), per ogni record nell'origine (ad esempio [!INCLUDE[crm_md](includes/crm_md.md)]) non ancora associato.  

 Ad esempio, il processo di sincronizzazione AGENTE - Dynamics 365 Sales utilizza il mapping di tabella AGENTE. Il processo di sincronizzazione copia i dati dai record utente in [!INCLUDE[crm_md](includes/crm_md.md)] nei record agente in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Se si imposta il mapping di tabella per creare nuovi record, per ogni utente di [!INCLUDE[crm_md](includes/crm_md.md)] non ancora associato a un agente di [!INCLUDE[d365fin](includes/d365fin_md.md)], viene creato un nuovo record agente in [!INCLUDE[d365fin](includes/d365fin_md.md)].  

#### <a name="to-create-new-records-during-synchronization"></a>Per creare nuovi record durante la sincronizzazione  
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Mapping tabella integrazione** e quindi scegliere il collegamento correlato.

2.  Nel movimento di mapping della tabella nell'elenco, deselezionare il campo **Sinc. solo record associati**.  

## <a name="using-configuration-templates-on-table-mappings"></a>Utilizzo dei modelli di configurazione sui mapping di tabella
È possibile assegnare i modelli di configurazione ai mapping di tabella da utilizzare per i nuovi record creati in [!INCLUDE[d365fin](includes/d365fin_md.md)] o [!INCLUDE[crm_md](includes/crm_md.md)]. Per ogni mapping di tabella, è possibile specificare un modello di configurazione da utilizzare per i nuovi record di [!INCLUDE[d365fin](includes/d365fin_md.md)] e un altro modello per utilizzare i nuovi record di [!INCLUDE[crm_md](includes/crm_md.md)].  

Se si installa il setup di sincronizzazione predefinito, la maggioranza delle volte i due modelli di configurazione verranno automaticamente creati e utilizzati nel mapping di tabella per i clienti di [!INCLUDE[d365fin](includes/d365fin_md.md)] e i conti di [!INCLUDE[crm_md](includes/crm_md.md)]: **CRMCUST** e **CRMACCOUNT**.  

-   **CRMCUST** viene utilizzato per creare e sincronizzare i nuovi clienti in [!INCLUDE[d365fin](includes/d365fin_md.md)] in base a un conto di [!INCLUDE[crm_md](includes/crm_md.md)].  

     Il modello viene creato copiando un modello di configurazione esistente per i clienti nell'applicazione. **CRMCUST** viene creato solo se esiste un modello di configurazione e il campo **Cod. valuta** nel modello è vuoto. Se un campo del modello di configurazione contiene un valore, questo valore viene utilizzato al posto del valore del campo mappato nel conto di [!INCLUDE[crm_md](includes/crm_md.md)]. Ad esempio, se il campo **Paese** in un conto di [!INCLUDE[crm_md](includes/crm_md.md)] include *Stati Uniti* e il campo **Paese** del modello di configurazione è *GB*, viene utilizzato *GB* come **Paese** nel cliente creato in [!INCLUDE[d365fin](includes/d365fin_md.md)].  

-   **CRMACCOUNT** crea e sincronizza nuovi conti in [!INCLUDE[crm_md](includes/crm_md.md)] in base a un conto di [!INCLUDE[d365fin](includes/d365fin_md.md)].  

#### <a name="to-specify-configuration-templates-on-a-table-mapping"></a>Per specificare i modelli di configurazione in un mapping di tabella  
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Mapping tabella integrazione** e quindi scegliere il collegamento correlato.

2.  Nel movimento mapping di tabella nell'elenco, nel campo **Codice modello di configurazione tabella** scegliere il modello di configurazione da utilizzare per nuovi record in [!INCLUDE[d365fin](includes/d365fin_md.md)].  

3.  Impostare il campo **Codice modello di configurazione tabella integrazione** nel modello di configurazione da utilizzare per i nuovi record di [!INCLUDE[crm_md](includes/crm_md.md)].

## <a name="see-also"></a>Vedere anche  
[Informazioni sull'integrazione di Dynamics 365 Business Central con Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md )   
[Sincronizzazione di Business Central e Dynamics 365 Sales](admin-synchronizing-business-central-and-sales.md)   
[Pianificare una sincronizzazione](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
