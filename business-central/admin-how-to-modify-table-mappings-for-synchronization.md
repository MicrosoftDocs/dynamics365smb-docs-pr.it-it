---
title: Mapping delle tabelle e dei campi da sincronizzare | Microsoft Docs
description: Informazioni su come mappare tabelle e campi per la sincronizzazione dei dati tra Business Central e Common Data Service.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize, table mapping
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 382328e88c828afbf4316eb1f9bab73f6a2b7f95
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3911382"
---
# <a name="mapping-the-tables-and-fields-to-synchronize"></a>Mapping delle tabelle e dei campi da sincronizzare
La base della sincronizzazione dei dati in [!INCLUDE[d365fin](includes/d365fin_md.md)] con dati in [!INCLUDE[d365fin](includes/cds_long_md.md)] consiste nel mapping delle tabelle e dei campi che contengono i dati tra loro. Il mapping avviene tramite tabelle di integrazione. 

## <a name="mapping-integration-tables"></a>Mapping delle tabelle di integrazione
La tabella di integrazione è una tabella del database di [!INCLUDE[d365fin](includes/d365fin_md.md)] che rappresenta un'entità, ad esempio un account, in [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Le tabelle di integrazione includono i campi corrispondenti ai campi della tabella dell'entità [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Ad esempio, la tabella di integrazione dell'account si collega all'entità account in [!INCLUDE[cds_short_md](includes/cds_long_md.md)]. Per ogni entità di [!INCLUDE[cds_short_md](includes/cds_short_md.md)] che si desidera sincronizzare con i dati in [!INCLUDE[prodshort](includes/prodshort.md)], deve esserci un corrispondente mapping della tabella di integrazione.

Quando si crea la connessione tra le app, [!INCLUDE[d365fin](includes/d365fin_md.md)] imposta alcuni mapping di tabella e campi predefiniti. È possibile modificare i mapping di tabella se necessario. Per ulteriori informazioni, vedere [Mapping delle entità standard per la sincronizzazione](admin-synchronizing-business-central-and-sales.md#standard-entity-mapping-for-synchronization). Se sono stati modificati i mapping predefiniti e si desidera annullare le modifiche, nella pagina **Setup connessione di [!INCLUDE[d365fin](includes/cds_long_md.md)]**, scegliere **Utilizza setup di default per la sincronizzazione**.

> [!Note]
> Se si utilizza una versione locale di [!INCLUDE[d365fin](includes/d365fin_md.md)], i mapping della tabella di integrazione sono memorizzati nella tabella 5335 Mapping tabella integrazione e possono essere visualizzati e modificati dalla pagina 5335 Mapping tabella integrazione. La mappatura e regole complessi di sincronizzazione vengono definiti nella codeunit 5341. 

### <a name="synchronization-rules"></a>Regole di sincronizzazione
Un mapping della tabella di integrazione include anche le regole che controllano il modo in cui i processi di sincronizzazione dell'integrazione sincronizzano i record in una tabella [!INCLUDE[d365fin](includes/d365fin_md.md)] e un'entità in [!INCLUDE[d365fin](includes/cds_long_md.md)]. <!--For examples of rules for an integration with Sales, see [Synchronization Rules](admin-synchronizing-business-central-and-sales.md#synchronization-rules). need to verify link -->

### <a name="strategies-for-auto-resolving-conflicts"></a>Strategie per la risoluzione automatica dei conflitti
I conflitti di dati possono verificarsi facilmente quando le applicazioni aziendali scambiano dati su base continuativa. Ad esempio, qualcuno potrebbe eliminare o modificare un record in una delle applicazioni o in entrambe. Per ridurre il numero di conflitti da risolvere manualmente, è possibile specificare le strategie di risoluzione e [!INCLUDE[d365fin](includes/d365fin_md.md)] risolverà automaticamente i conflitti secondo le regole nelle strategie.

I mapping della tabella di integrazione includono regole che controllano il modo in cui i processi di sincronizzazione sincronizzano i record. Nella pagina **Mapping tabella integrazione**, nelle colonne **Risolvi conflitti di eliminazione** e **Risolvi conflitti di aggiornamento** è possibile specificare come [!INCLUDE[d365fin](includes/d365fin_md.md)] risolverà i conflitti che si verificano perché i record sono stati eliminati nelle tabelle in una o nell'altra applicazione aziendale o aggiornati in entrambe. 

Nella colonna **Risolvi conflitti di eliminazione** è possibile scegliere che [!INCLUDE[d365fin](includes/d365fin_md.md)] ripristini automaticamente i record eliminati, rimuova l'associazione tra i record o non esegua alcuna operazione. Se non si fa nulla, è necessario risolvere manualmente i conflitti. 

Nella colonna **Risolvi conflitti di aggiornamento** è possibile scegliere che [!INCLUDE[d365fin](includes/d365fin_md.md)] invii automaticamente un aggiornamento dei dati alla tabella di integrazione durante l'invio dei dati a [!INCLUDE[d365fin](includes/cds_long_md.md)] o ottenere un aggiornamento dei dati dalla tabella di integrazione quando si ottengono dati da [!INCLUDE[d365fin](includes/cds_long_md.md)] o non fare nulla. Se non si fa nulla, è necessario risolvere manualmente i conflitti.

Dopo aver specificato la strategia, nella pagina **Errori di sincronizzazione dati associati** è possibile scegliere l'azione **Riprova tutto** per risolvere automaticamente i conflitti. 

## <a name="mapping-integration-fields"></a>Mapping dei campi di integrazione
Il mapping delle tabelle è solo il primo passo. È necessario anche eseguire il mapping dei campi nelle tabelle. I mapping dei campi di integrazione collegano i campi nelle tabelle [!INCLUDE[d365fin](includes/d365fin_md.md)] con i campi corrispondenti in [!INCLUDE[d365fin](includes/cds_long_md.md)] e determinano se vengono sincronizzati i dati in ciascuna tabella. Il mapping della tabella standard fornita da [!INCLUDE[d365fin](includes/d365fin_md.md)] include i mapping dei campi, ma è possibile modificarli se necessario. Per ulteriori informazioni, vedere [Visualizzazione di mapping di entità](admin-synchronizing-business-central-and-sales.md#tip-for-admins-viewing-entity-mappings).

> [!Note]
> Se si utilizza una versione locale di [!INCLUDE[d365fin](includes/d365fin_md.md)], i mapping dei campi di integrazione sono definiti nella tabella 5336 Mapping campi integrazione.

### <a name="handling-differences-in-field-values"></a>Gestione delle differenze nei valori di campo
A volte i valori nei campi che si desidera mappare sono diversi. Ad esempio, in [!INCLUDE[crm_md](includes/crm_md.md)] il codice della lingua per gli Stati Uniti è "U.S.", ma in [!INCLUDE[d365fin](includes/d365fin_md.md)] è "US". Ciò significa che è necessario trasformare il valore quando si sincronizzano i dati. Ciò accade attraverso le regole di trasformazione definite per i campi. Si definiscono le regole di trasformazione sulla pagina **Mapping tabella integrazione** scegliendo **Mappatura** e poi **Campi**. Vengono fornite le regole predefinite, ma è possibile anche crearne di proprie. Per ulteriori informazioni, vedere [Regole di trasformazione](across-how-to-set-up-data-exchange-definitions.md#transformation-rules).

### <a name="handling-missing-option-values-in-mapping"></a>Gestione dei valori delle opzioni mancanti nella mappatura
[!INCLUDE[d365fin](includes/cds_long_md.md)] contiene solo tre campi di set di opzioni che forniscono valori su cui è possibile eseguire il mapping ai campi [!INCLUDE[d365fin](includes/d365fin_md.md)] di tipo **Opzione** per la sincronizzazione automatica. Durante la sincronizzazione, le opzioni non mappate vengono ignorate e le opzioni mancanti vengono aggiunte alla relativa tabella [!INCLUDE[d365fin](includes/d365fin_md.md)] e aggiunte alla tabella di sistema **Mappatura opzione CDS** da gestire manualmente in seguito. Ad esempio, aggiungendo le opzioni mancanti in entrambi i prodotti e quindi aggiornando la mappatura. Per ulteriori informazioni, vedere [Gestione dei valori delle opzioni mancanti](admin-cds-missing-option-values.md).

## <a name="coupling-records"></a>Associazione di record
Record dei collegamenti di associazione in [!INCLUDE[d365fin](includes/cds_long_md.md)] per registrare in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Ad esempio, gli account in [!INCLUDE[d365fin](includes/cds_long_md.md)] sono in genere associati ai clienti in [!INCLUDE[d365fin](includes/d365fin_md.md)]. I record di associazione offrono i seguenti vantaggi:

* Rendono possibile la sincronizzazione.
* Gli utenti possono aprire i record di un'app aziendale da un'altra. Ciò richiede che le app siano già integrate.

Le associazioni possono essere impostate automaticamente utilizzando i processi di sincronizzazione o manualmente modificando il record in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Per ulteriori informazioni, vedere [Sincronizzazione dei dati in [!INCLUDE[d365fin](includes/d365fin_md.md)] e [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-synchronizing-business-central-and-sales.md) e [Associare e sincronizzare i record manualmente](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings).

## <a name="filtering-records"></a>Filtro dei record  
Se non si desidera sincronizzare tutti i record per un'entità di [!INCLUDE[d365fin](includes/cds_long_md.md)] o una tabella di [!INCLUDE[d365fin](includes/d365fin_md.md)] specifica, è possibile impostare i filtri per limitare i record che vengono sincronizzati. I filtri vengono impostati nella pagina **Mapping tabella integrazione**.  

#### <a name="to-filter-records-for-synchronization"></a>Per filtrare record per la sincronizzazione  
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Mapping tabella integrazione** e quindi scegliere il collegamento correlato.

2.  Per filtrare i record di [!INCLUDE[d365fin](includes/d365fin_md.md)], impostare il campo **Filtro tabella**.  

3.  Per filtrare i record di [!INCLUDE[d365fin](includes/cds_long_md.md)], impostare il campo **Filtro tabella integrazione**.  

## <a name="creating-new-records"></a>Creazione di nuovi record  
Per impostazione predefinita, solo i record di [!INCLUDE[d365fin](includes/d365fin_md.md)]e [!INCLUDE[d365fin](includes/cds_long_md.md)] associati verranno sincronizzati dai processi di sincronizzazione di integrazione. È possibile impostare i mapping di tabella in modo che i nuovi record vengano creati nella destinazione (ad esempio [!INCLUDE[d365fin](includes/d365fin_md.md)]), per ogni record nell'origine (ad esempio [!INCLUDE[d365fin](includes/cds_long_md.md)]) non ancora associato.  

Ad esempio, il processo di sincronizzazione AGENTE - Dynamics 365 Sales utilizza il mapping di tabella AGENTE. Il processo di sincronizzazione copia i dati dai record utente in [!INCLUDE[d365fin](includes/cds_long_md.md)] nei record agente in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Se si imposta il mapping di tabella per creare nuovi record, per ogni utente di [!INCLUDE[d365fin](includes/cds_long_md.md)] non ancora associato a un agente di [!INCLUDE[d365fin](includes/d365fin_md.md)], viene creato un nuovo record agente in [!INCLUDE[d365fin](includes/d365fin_md.md)].  

#### <a name="to-create-new-records-during-synchronization"></a>Per creare nuovi record durante la sincronizzazione  
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Mapping tabella integrazione** e quindi scegliere il collegamento correlato.

2.  Nel movimento di mapping della tabella nell'elenco, deselezionare il campo **Sinc. solo record associati**.  

## <a name="using-configuration-templates-on-table-mappings"></a>Utilizzo dei modelli di configurazione sui mapping di tabella
È possibile assegnare i modelli di configurazione ai mapping di tabella da utilizzare per i nuovi record creati in [!INCLUDE[d365fin](includes/d365fin_md.md)] o [!INCLUDE[d365fin](includes/cds_long_md.md)]. Per ogni mapping di tabella, è possibile specificare un modello di configurazione da utilizzare per i nuovi record di [!INCLUDE[d365fin](includes/d365fin_md.md)] e un altro modello per utilizzare i nuovi record di [!INCLUDE[d365fin](includes/cds_long_md.md)].  

Se si installa il setup di sincronizzazione predefinito, la maggioranza delle volte i due modelli di configurazione verranno automaticamente creati e utilizzati nel mapping di tabella per i clienti di [!INCLUDE[d365fin](includes/d365fin_md.md)] e i conti di [!INCLUDE[crm_md](includes/crm_md.md)]: **CDSCUST** e **CDSACCOUNT**.  

-   **CDSCUST** viene utilizzato per creare e sincronizzare i nuovi clienti in [!INCLUDE[d365fin](includes/d365fin_md.md)] in base a un conto di [!INCLUDE[crm_md](includes/crm_md.md)].  

     Il modello viene creato copiando un modello di configurazione esistente per i clienti nell'applicazione. **CDSCUST** viene creato solo se esiste un modello di configurazione e il campo **Cod. valuta** nel modello è vuoto. Se un campo del modello di configurazione contiene un valore, questo valore viene utilizzato al posto del valore del campo mappato nel conto di [!INCLUDE[d365fin](includes/cds_long_md.md)]. Ad esempio, se il campo **Paese** in un conto di [!INCLUDE[d365fin](includes/cds_long_md.md)] include *Stati Uniti* e il campo **Paese** del modello di configurazione è *GB*, viene utilizzato *GB* come **Paese** nel cliente creato in [!INCLUDE[d365fin](includes/d365fin_md.md)].  

-   **CDSACCOUNT** crea e sincronizza nuovi conti in [!INCLUDE[d365fin](includes/cds_long_md.md)] in base a un conto di [!INCLUDE[d365fin](includes/d365fin_md.md)].  

#### <a name="to-specify-configuration-templates-on-a-table-mapping"></a>Per specificare i modelli di configurazione in un mapping di tabella  
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Mapping tabella integrazione** e quindi scegliere il collegamento correlato.

2.  Nel movimento mapping di tabella nell'elenco, nel campo **Codice modello di configurazione tabella** scegliere il modello di configurazione da utilizzare per nuovi record in [!INCLUDE[d365fin](includes/d365fin_md.md)].  

3.  Impostare il campo **Codice modello di configurazione tabella integrazione** nel modello di configurazione da utilizzare per i nuovi record di [!INCLUDE[d365fin](includes/cds_long_md.md)].

## <a name="see-also"></a>Vedere anche  
[Informazioni sull'integrazione di Dynamics 365 Business Central con [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md )   
[Sincronizzazione di Business Central e [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-synchronizing-business-central-and-sales.md)   
[Pianificare una sincronizzazione](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
