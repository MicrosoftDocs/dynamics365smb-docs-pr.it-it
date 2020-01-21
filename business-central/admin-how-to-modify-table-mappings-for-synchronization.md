---
title: Mapping delle tabelle e dei campi da sincronizzare | Microsoft Docs
description: Informazioni su come mappare tabelle e campi per la sincronizzazione dei dati tra Business Central e Dynamics 365 Sales.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize, table mapping
ms.date: 12/18/2019
ms.author: bholtorf
ms.openlocfilehash: 371bd80c04917495ea1b35f214d10d716ed5f9ad
ms.sourcegitcommit: b570997f93d1f7141bc9539c93a67a91226660a8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2020
ms.locfileid: "2943115"
---
# <a name="mapping-the-tables-and-fields-to-synchronize"></a>Mapping delle tabelle e dei campi da sincronizzare
La base della sincronizzazione dei dati in [!INCLUDE[d365fin](includes/d365fin_md.md)] con dati in [!INCLUDE[crm_md](includes/crm_md.md)] consiste nel mapping delle tabelle e dei campi che contengono i dati tra loro. Il mapping avviene tramite tabelle di integrazione. 

## <a name="mapping-integration-tables"></a>Mapping delle tabelle di integrazione
La tabella di integrazione è una tabella del database di [!INCLUDE[d365fin](includes/d365fin_md.md)] che rappresenta un'entità, ad esempio un account, in [!INCLUDE[crm_md](includes/crm_md.md)]. Le tabelle di integrazione includono i campi corrispondenti ai campi della tabella dell'entità [!INCLUDE[crm_md](includes/crm_md.md)]. Ad esempio, la tabella di integrazione dell'account si collega all'entità account in [!INCLUDE[crm_md](includes/crm_md.md)]. Per ogni entità di [!INCLUDE[crm_md](includes/crm_md.md)] che si desidera sincronizzare con i dati in [!INCLUDE[d365fin](includes/d365fin_md.md)], deve esserci un corrispondente mapping della tabella di integrazione.

Quando si crea la connessione tra le app, [!INCLUDE[d365fin](includes/d365fin_md.md)] imposta alcuni mapping di tabella e campi predefiniti. È possibile modificare i mapping di tabella se necessario. Per ulteriori informazioni, vedere [Mapping delle entità standard di Sales per la sincronizzazione](admin-synchronizing-business-central-and-sales.md#standard-sales-entity-mapping-for-synchronization). Se sono stati modificati i mapping predefiniti e si desidera annullare le modifiche, nella pagina **Setup connessione di Dynamics 365**, scegliere **Utilizza setup di default per la sincronizzazione**.

> [!Note]
> Se si utilizza una versione locale di [!INCLUDE[d365fin](includes/d365fin_md.md)], i mapping della tabella di integrazione sono memorizzati nella tabella 5335 Mapping tabella integrazione e possono essere visualizzati e modificati dalla pagina 5335 Mapping tabella integrazione. La mappatura e regole complessi di sincronizzazione vengono definiti nella codeunit 5341. 

### <a name="synchronization-rules"></a>Regole di sincronizzazione
Un mapping della tabella di integrazione include anche le regole che controllano il modo in cui i processi di sincronizzazione dell'integrazione sincronizzano i record in una tabella [!INCLUDE[d365fin](includes/d365fin_md.md)] e un'entità in [!INCLUDE[crm_md](includes/crm_md.md)]. Per ulteriori informazioni, vedere [Regole di sincronizzazione](admin-synchronizing-business-central-and-sales.md#synchronization-rules). 

## <a name="mapping-integration-fields"></a>Mapping dei campi di integrazione
Il mapping delle tabelle è solo il primo passo. È necessario anche eseguire il mapping dei campi nelle tabelle. I mapping dei campi di integrazione collegano i campi nelle tabelle [!INCLUDE[d365fin](includes/d365fin_md.md)] con i campi corrispondenti in [!INCLUDE[crm_md](includes/crm_md.md)] e determinano se vengono sincronizzati i dati in ciascuna tabella. Il mapping della tabella standard fornita da [!INCLUDE[d365fin](includes/d365fin_md.md)] include i mapping dei campi, ma è possibile modificarli se necessario. Per ulteriori informazioni, vedere [Visualizzazione di mapping di entità](admin-synchronizing-business-central-and-sales.md#tip-for-admins-viewing-entity-mappings).

> [!Note]
> Se si utilizza una versione locale di [!INCLUDE[d365fin](includes/d365fin_md.md)], i mapping dei campi di integrazione sono definiti nella tabella 5336 Mapping campi integrazione.

## <a name="coupling-records"></a>Associazione di record
Record dei collegamenti di associazione in [!INCLUDE[crm_md](includes/crm_md.md)] per registrare in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Ad esempio, gli account in [!INCLUDE[crm_md](includes/crm_md.md)] sono in genere associati ai clienti in [!INCLUDE[d365fin](includes/d365fin_md.md)]. I record di associazione offrono i seguenti vantaggi:

* Rendono possibile la sincronizzazione.
* Gli utenti possono aprire i record di un'app aziendale da un'altra. Questo richiede che la soluzione di integrazione [!INCLUDE[d365fin](includes/d365fin_md.md)] sia installata in [!INCLUDE[crm_md](includes/crm_md.md)].

Le associazioni possono essere impostate automaticamente utilizzando i processi di sincronizzazione o manualmente modificando il record in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Per ulteriori informazioni, vedere [Sincronizzazione dei dati in [!INCLUDE[d365fin](includes/d365fin_md.md)] e [!INCLUDE[crm_md](includes/crm_md.md)]](admin-synchronizing-business-central-and-sales.md) e [Associare e sincronizzare i record manualmente](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings).

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
