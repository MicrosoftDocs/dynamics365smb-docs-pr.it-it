---
title: Mapping delle tabelle e dei campi da sincronizzare
description: Informazioni su come mappare tabelle e campi per la sincronizzazione dei dati tra Business Central e Microsoft Dataverse.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.date: 03/31/2023
ms.custom: bap-template
ms.search.keywords: 'sales, crm, integration, sync, synchronize, table mapping'
---
# <a name="mapping-the-tables-and-fields-to-synchronize"></a><a name="mapping-the-tables-and-fields-to-synchronize"></a><a name="mapping-the-tables-and-fields-to-synchronize"></a>Mapping delle tabelle e dei campi da sincronizzare

La base della sincronizzazione dei dati consiste nel mapping delle tabelle e dei campi in [!INCLUDE[prod_short](includes/prod_short.md)] con tabelle e colonne in [!INCLUDE[prod_short](includes/cds_long_md.md)], di modo che possano scambiarsi i dati. Il mapping avviene tramite tabelle di integrazione.

## <a name="mapping-integration-tables"></a><a name="mapping-integration-tables"></a><a name="mapping-integration-tables"></a>Mapping delle tabelle di integrazione

La tabella di integrazione è una tabella del database di [!INCLUDE[prod_short](includes/prod_short.md)] che rappresenta una tabella, ad esempio un account, in [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Le tabelle di integrazione includono i campi corrispondenti alle colonne della tabella [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Ad esempio, la tabella di integrazione dell'account si collega alla tabella Account in [!INCLUDE[cds_short_md](includes/cds_long_md.md)]. Per ogni tabella di [!INCLUDE[cds_short_md](includes/cds_short_md.md)] che si desidera sincronizzare con i dati in [!INCLUDE[prod_short](includes/prod_short.md)], deve esserci un corrispondente mapping della tabella di integrazione.

Quando si crea la connessione tra le app, [!INCLUDE[prod_short](includes/prod_short.md)] imposta alcuni mapping predefiniti. È possibile modificare i mapping di tabella se necessario. Per ulteriori informazioni, vedere [Mapping delle tabelle standard per la sincronizzazione](admin-synchronizing-business-central-and-sales.md#standard-table-mapping-for-synchronization). Se sono stati modificati i mapping predefiniti e si desidera annullare le modifiche, nella pagina **Mapping tabella integrazione**, scegliere **Utilizza setup di default per la sincronizzazione**.

> [!Note]
> Se si utilizza una versione locale di [!INCLUDE[prod_short](includes/prod_short.md)], i mapping della tabella di integrazione sono memorizzati nella tabella 5335 Mapping tabella integrazione dove è possibile visualizzarli e modificarli. La mappatura e regole complessi di sincronizzazione vengono definiti nella codeunit 5341.

> [!TIP]
> Quando un record accoppiato cambia, [!INCLUDE [prod_short](includes/prod_short.md)] sincronizza automaticamente i dati con Dataverse. La sincronizzazione automatica è ottima nella maggior parte dei casi. Tuttavia, le frequenti modifiche a grandi quantità di record accoppiati in una tabella possono rallentare la sincronizzazione dei dati.
>
> Per evitare un rallentamento delle prestazioni, nella pagina **Mapping tabelle di integrazione**, puoi abilitare o disabilitare la sincronizzazione dei dati basata sugli eventi per qualsiasi tabella. Per impostazione predefinita, la sincronizzazione basata sugli eventi è attivata in modo che le integrazioni esistenti non siano interessate. L'amministratore può attivarla o disattivarla per tabelle specifiche.

### <a name="additional-mappings"></a><a name="additional-mappings"></a><a name="additional-mappings"></a>Mapping aggiuntivi

I termini di pagamento, i metodi di spedizione e gli agenti di spedizione possono cambiare e può essere importante poterli adeguare. Se abiliti la funzionalità **Aggiornamento della funzionalità: mapping all'opzione impostata in Dataverse senza codice** nella pagina [Gestione delle funzionalità](https://businesscentral.dynamics.com/?page=2610), è possibile aggiungere manualmente le mappature della tabella di integrazione per i termini di pagamento (TERMINI DI PAGAMENTO), i metodi di spedizione (METODO DI SPEDIZIONE) e gli agenti di spedizione (AGENTE DI SPEDIZIONE). Questa mappatura può aiutare a garantire che le tue politiche siano le stesse per queste configurazioni in [!INCLUDE[prod_short](includes/cds_long_md.md)] e [!INCLUDE[cds_long_md](includes/cds_long_md.md)].

### <a name="synchronization-rules"></a><a name="synchronization-rules"></a><a name="synchronization-rules"></a>Regole di sincronizzazione

Un mapping della tabella di integrazione include anche le regole che controllano il modo in cui i processi di sincronizzazione dell'integrazione sincronizzano i record in una tabella [!INCLUDE[prod_short](includes/prod_short.md)] e una tabella in [!INCLUDE[prod_short](includes/cds_long_md.md)]. Per esempi di regole per un'integrazione con Sales, vai a [Regole di sincronizzazione](#synchronization-rules).

### <a name="strategies-for-auto-resolving-conflicts"></a><a name="strategies-for-auto-resolving-conflicts"></a><a name="strategies-for-auto-resolving-conflicts"></a>Strategie per la risoluzione automatica dei conflitti

I conflitti di dati possono verificarsi facilmente quando le applicazioni aziendali scambiano dati su base continuativa. Ad esempio, qualcuno potrebbe eliminare o modificare una riga in una delle applicazioni o in entrambe. Per ridurre il numero di conflitti da risolvere manualmente, è possibile specificare le strategie di risoluzione e [!INCLUDE[prod_short](includes/prod_short.md)] risolverà automaticamente i conflitti secondo le regole nelle strategie.

I mapping della tabella di integrazione includono regole che controllano il modo in cui i processi di sincronizzazione sincronizzano i record. Nella pagina **Mapping tabella integrazione**, nelle colonne **Risolvi conflitti di eliminazione** e **Risolvi conflitti di aggiornamento** è possibile specificare come [!INCLUDE[prod_short](includes/prod_short.md)] risolverà i conflitti che si verificano perché i record sono stati eliminati nelle tabelle in una o nell'altra applicazione aziendale o aggiornati in entrambe. 

Nella colonna **Risolvi conflitti di eliminazione** è possibile scegliere che [!INCLUDE[prod_short](includes/prod_short.md)] ripristini automaticamente i record eliminati, rimuova l'associazione tra i record o non esegua alcuna operazione. Se non si fa nulla, è necessario risolvere manualmente i conflitti. 

Nella colonna **Risolvi conflitti di aggiornamento** è possibile scegliere che [!INCLUDE[prod_short](includes/prod_short.md)] invii automaticamente un aggiornamento dei dati alla tabella di integrazione durante l'invio dei dati a [!INCLUDE[prod_short](includes/cds_long_md.md)] o ottenere un aggiornamento dei dati dalla tabella di integrazione quando si ottengono dati da [!INCLUDE[prod_short](includes/cds_long_md.md)] o non fare nulla. Se non si fa nulla, è necessario risolvere manualmente i conflitti.

Dopo aver specificato la strategia, nella pagina **Errori di sincronizzazione dati associati** è possibile scegliere l'azione **Riprova tutto** per risolvere automaticamente i conflitti.

## <a name="mapping-integration-fields"></a><a name="mapping-integration-fields"></a><a name="mapping-integration-fields"></a>Mapping dei campi di integrazione

Il mapping delle tabelle è solo il primo passo. È necessario anche eseguire il mapping dei campi nelle tabelle. I mapping dei campi di integrazione collegano i campi nelle tabelle [!INCLUDE[prod_short](includes/prod_short.md)] con le colonne corrispondenti in [!INCLUDE[prod_short](includes/cds_long_md.md)] e determinano se vengono sincronizzati i dati in ciascuna tabella. Il mapping della tabella standard fornita da [!INCLUDE[prod_short](includes/prod_short.md)] include i mapping dei campi, ma è possibile modificarli se necessario. Per ulteriori informazioni, vedere [Visualizzazione di mapping di tabella](admin-synchronizing-business-central-and-sales.md#tip-for-admins-viewing-table-mappings).

> [!Note]
> Se si utilizza una versione on-premises di [!INCLUDE[prod_short](includes/prod_short.md)], le mappature dei campi di integrazione sono definite nella tabella 5336 Integration Field Mapping.

Puoi mappare manualmente i campi, o puoi automatizzare il processo mappando più campi allo stesso tempo in base a criteri di corrispondenza dei loro valori. Per maggiori informazioni, vedi [Per accoppiare più record basati sulla corrispondenza dei valori dei campi](admin-how-to-couple-and-synchronize-records-manually.md).

### <a name="handle-differences-in-field-values"></a><a name="handle-differences-in-field-values"></a><a name="handle-differences-in-field-values"></a>Gestione delle differenze nei valori di campo

A volte i valori nei campi che si desidera mappare sono diversi. Ad esempio, in [!INCLUDE[crm_md](includes/crm_md.md)] il codice della lingua per gli Stati Uniti è "U.S.", ma in [!INCLUDE[prod_short](includes/prod_short.md)] è "US". Ciò significa che è necessario trasformare il valore quando si sincronizzano i dati. Ciò accade attraverso le regole di trasformazione definite per i campi. Si definiscono le regole di trasformazione sulla pagina **Mapping tabella integrazione** scegliendo **Mappatura** e poi **Campi**. Vengono fornite le regole predefinite, ma è possibile anche crearne di proprie. Per ulteriori informazioni, vedere [Regole di trasformazione](across-how-to-set-up-data-exchange-definitions.md#transformation-rules).

### <a name="handle-missing-option-values"></a><a name="handle-missing-option-values"></a><a name="handle-missing-option-values"></a>Gestione dei valori delle opzioni mancanti

[!INCLUDE[prod_short](includes/cds_long_md.md)] contiene solo tre colonne di set di opzioni che forniscono valori su cui è possibile eseguire il mapping ai campi [!INCLUDE[prod_short](includes/prod_short.md)] di tipo **Opzione** per la sincronizzazione automatica. Durante la sincronizzazione, le opzioni non mappate vengono ignorate e le opzioni mancanti vengono aggiunte alla relativa tabella [!INCLUDE[prod_short](includes/prod_short.md)] e aggiunte alla tabella di sistema **Mappatura opzione CDS** da gestire manualmente in seguito. Ad esempio, aggiungendo le opzioni mancanti in entrambi i prodotti e quindi aggiornando la mappatura. Per ulteriori informazioni, vedere [Gestione dei valori delle opzioni mancanti](admin-cds-missing-option-values.md).

## <a name="couple-records"></a><a name="couple-records"></a><a name="couple-records"></a>Associare i record

Righe dei collegamenti di associazione in [!INCLUDE[prod_short](includes/cds_long_md.md)] per registrare in [!INCLUDE[prod_short](includes/prod_short.md)]. Ad esempio, gli account in [!INCLUDE[prod_short](includes/cds_long_md.md)] sono in genere associati ai clienti in [!INCLUDE[prod_short](includes/prod_short.md)]. I record di associazione offrono i seguenti vantaggi:

* Rendono possibile la sincronizzazione.
* Gli utenti possono aprire i record o le righe di un'app aziendale da un'altra. Ciò richiede che le app siano già integrate.

Le associazioni possono essere impostate automaticamente utilizzando i processi di sincronizzazione o manualmente modificando il record in [!INCLUDE[prod_short](includes/prod_short.md)]. Per ulteriori informazioni, vedere [Sincronizzazione dei dati in [!INCLUDE[prod_short](includes/prod_short.md)] e [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-synchronizing-business-central-and-sales.md) e [Associare e sincronizzare i record manualmente](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings).

## <a name="filter-records-and-rows"></a><a name="filter-records-and-rows"></a><a name="filter-records-and-rows"></a>Filtro di record e righe

Se non vuoi sincronizzare tutte le righe di una tabella di [!INCLUDE[prod_short](includes/cds_long_md.md)] o di [!INCLUDE[prod_short](includes/prod_short.md)] specifica, è possibile impostare i filtri per limitare i dati che vengono sincronizzati. I filtri vengono impostati nella pagina **Mapping tabella integrazione**.  

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Mapping tabella integrazione**, quindi scegli il collegamento correlato.
2. Per filtrare i record di [!INCLUDE[prod_short](includes/prod_short.md)], impostare il campo **Filtro tabella**.  
3. Per filtrare le righe di [!INCLUDE[prod_short](includes/cds_long_md.md)], impostare il campo **Filtro tabella integrazione**.  

## <a name="create-new-records"></a><a name="create-new-records"></a><a name="create-new-records"></a>Creare nuovi record

Per impostazione predefinita, solo i record di [!INCLUDE[prod_short](includes/prod_short.md)] e le righe di [!INCLUDE[prod_short](includes/cds_long_md.md)] associati verranno sincronizzati dai processi di sincronizzazione di integrazione. È possibile impostare i mapping di tabella o riga in modo che i nuovi record vengano creati nella destinazione (ad esempio [!INCLUDE[prod_short](includes/prod_short.md)]), per ogni riga nell'origine (ad esempio [!INCLUDE[prod_short](includes/cds_long_md.md)]) non ancora associata.  

Ad esempio, il processo di sincronizzazione AGENTE - Dynamics 365 Sales utilizza il mapping di tabella AGENTE. Il processo di sincronizzazione copia i dati dagli utenti in [!INCLUDE[prod_short](includes/cds_long_md.md)] negli agenti in [!INCLUDE[prod_short](includes/prod_short.md)]. Se si imposta il mapping di tabella per creare nuovi record, per ogni utente di [!INCLUDE[prod_short](includes/cds_long_md.md)] non ancora associato a un agente di [!INCLUDE[prod_short](includes/prod_short.md)], viene creata una nuova riga agente in [!INCLUDE[prod_short](includes/prod_short.md)].  

### <a name="to-create-new-records-during-synchronization"></a><a name="to-create-new-records-during-synchronization"></a><a name="to-create-new-records-during-synchronization"></a>Per creare nuovi record durante la sincronizzazione

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Mapping tabella integrazione**, quindi scegli il collegamento correlato.
2. Nel movimento di mapping della tabella nell'elenco, deselezionare il campo **Sinc. solo record associati**.  

## <a name="use-configuration-templates-on-table-mappings"></a><a name="use-configuration-templates-on-table-mappings"></a><a name="use-configuration-templates-on-table-mappings"></a>Utilizzare i modelli di configurazione sui mapping di tabella

È possibile assegnare i modelli di configurazione ai mapping di tabella da utilizzare per nuovi record o righe creati in [!INCLUDE[prod_short](includes/prod_short.md)] o [!INCLUDE[prod_short](includes/cds_long_md.md)]. Per ogni mapping di tabella, è possibile specificare un modello di configurazione da utilizzare per i nuovi record di [!INCLUDE[prod_short](includes/prod_short.md)] e un altro modello per utilizzare le nuove righe di [!INCLUDE[prod_short](includes/cds_long_md.md)].  

Se si installa il setup di sincronizzazione predefinito, la maggioranza delle volte i due modelli di configurazione verranno automaticamente creati e utilizzati nel mapping di tabella per i clienti di [!INCLUDE[prod_short](includes/prod_short.md)] e i conti di [!INCLUDE[crm_md](includes/crm_md.md)]: **CDSCUST** e **CDSACCOUNT**.  

* **CDSCUST** crea e sincronizza nuovi clienti in [!INCLUDE[prod_short](includes/prod_short.md)] in base ai conti di [!INCLUDE[crm_md](includes/crm_md.md)].  

     Crea questo modello copiando un modello di configurazione esistente per i clienti. **CDSCUST** viene creato solo se esiste un modello di configurazione e il campo **Cod. valuta** nel modello è vuoto. Se un campo del modello di configurazione contiene un valore, questo valore viene utilizzato al posto del valore della colonna mappata nel conto di [!INCLUDE[prod_short](includes/cds_long_md.md)]. Ad esempio, se la colonna **Paese** in un conto di [!INCLUDE[prod_short](includes/cds_long_md.md)] include *Stati Uniti* e il campo **Paese** del modello di configurazione è **GB**, viene utilizzato **GB** come **Paese** nel cliente creato in [!INCLUDE[prod_short](includes/prod_short.md)].  

* **CDSACCOUNT** crea e sincronizza nuovi conti in [!INCLUDE[prod_short](includes/cds_long_md.md)] in base a un conto di [!INCLUDE[prod_short](includes/prod_short.md)].  

### <a name="to-specify-configuration-templates-on-a-table-mapping"></a><a name="to-specify-configuration-templates-on-a-table-mapping"></a><a name="to-specify-configuration-templates-on-a-table-mapping"></a>Per specificare i modelli di configurazione in un mapping di tabella

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Mapping tabella integrazione**, quindi scegli il collegamento correlato.
2. Nel movimento mapping di tabella nell'elenco, nel campo **Codice modello di configurazione tabella** scegliere il modello di configurazione da utilizzare per nuovi record in [!INCLUDE[prod_short](includes/prod_short.md)].  
3. Impostare il campo **Codice modello di configurazione tabella integrazione** nel modello di configurazione da utilizzare per i nuovi record di [!INCLUDE[prod_short](includes/cds_long_md.md)].

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Vedere anche

[Informazioni sull'integrazione di Dynamics 365 Business Central con [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md )  
[Sincronizzazione di Business Central e [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-synchronizing-business-central-and-sales.md)  
[Pianificare una sincronizzazione](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
