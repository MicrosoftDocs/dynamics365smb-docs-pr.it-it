---
title: Sincronizzazione e integrazione dei dati | Microsoft Docs
description: La sincronizzazione copia i dati tra i movimenti di Dynamics 365 for Sales e i record di Business Central e mantiene i dati aggiornati in entrambi i sistemi.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: e52010384de83d95011cb29a88cad17a5eba817c
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/29/2019
ms.locfileid: "1247142"
---
# <a name="synchronizing-data-in-business-central-and-dynamics-365-for-sales"></a>Sincronizzazione di dati in Business Central e Dynamics 365 for Sales
Quando si integra [!INCLUDE[crm_md](includes/crm_md.md)] con [!INCLUDE[d365fin](includes/d365fin_md.md)], è possibile decidere se sincronizzare i dati nei campi selezionati di [!INCLUDE[d365fin](includes/d365fin_md.md)] (ad esempio clienti, contatti e agenti) con record equivalenti in [!INCLUDE[d365fin](includes/d365fin_md.md)] (come conti, contatti e utenti). A seconda del tipo di record, è possibile sincronizzare i dati da [!INCLUDE[crm_md](includes/crm_md.md)] a [!INCLUDE[d365fin](includes/d365fin_md.md)], o viceversa. Per ulteriori informazioni, vedere [Integrazione con Dynamics 365 for Sales](admin-prepare-dynamics-365-for-sales-for-integration.md).  

La sincronizzazione utilizza i seguenti elementi:

* Mapping di tabella di integrazione
* Mapping di campo di integrazione
* Regole di sincronizzazione
* Record associati

Quando la sincronizzazione è impostata è possibile associare i record di [!INCLUDE[d365fin](includes/d365fin_md.md)] ai record di [!INCLUDE[crm_md](includes/crm_md.md)] per sincronizzare i relativi dati. È possibile avviare una sincronizzazione manualmente o in base a una programmazione. La tabella seguente fornisce una panoramica dei modi in cui è possibile sincronizzare record.  

|  Tipo  |  Metodo  |  Vedere  |  
|--------|----------|-------|  
|Sincronizzazione manuale|Sincronizzare record per record.<br /><br /> È possibile sincronizzare singoli record in [!INCLUDE[d365fin](includes/d365fin_md.md)], ad esempio un cliente, con un record di [!INCLUDE[crm_md](includes/crm_md.md)] corrispondente, ad esempio un conto. Questo è in genere il modo in cui gli utenti utilizzano i dati di [!INCLUDE[crm_md](includes/crm_md.md)] in [!INCLUDE[d365fin](includes/d365fin_md.md)].|[Associare e sincronizzare i record manualmente](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
|  |Sincronizzare in base a un mapping di tabella.<br /><br /> È possibile sincronizzare tutti i record in una tabella di [!INCLUDE[d365fin](includes/d365fin_md.md)] con un'entità di [!INCLUDE[crm_md](includes/crm_md.md)].|[Sincronizzare singoli mapping di tabella](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
||Sincronizzazione di tutti i record modificati per tutti i mapping di tabella.<br /><br /> È possibile sincronizzare tutte record che sono stati modificati nelle tabelle di [!INCLUDE[d365fin](includes/d365fin_md.md)] dall'ultima sincronizzazione.|[Sincronizzazione di tutti i record modificati](admin-manual-synchronization-of-table-mappings.md#synchronizing-all-modified-records)|
||Sincronizzazione completa di tutti i dati per tutti i mapping di tabella.<br /><br /> È possibile sincronizzare tutti i dati nelle tabelle di [!INCLUDE[d365fin](includes/d365fin_md.md)] e le entità di [!INCLUDE[crm_md](includes/crm_md.md)] mappate e creare nuovi record nella soluzione di destinazione per record non associati nella soluzione di origine.<br /><br /> La sincronizzazione completa sincronizza tutti i dati e ignora l'associazione. In genere, si effettua una sincronizzazione completa quando si imposta l'integrazione e una sola delle soluzioni contiene dati. Una sincronizzazione completa può anche risultare utile in un ambiente dimostrativo.|[Eseguire una sincronizzazione completa](admin-manual-synchronization-of-table-mappings.md#run-a-full-synchronization)|  
|Sincronizzazione pianificata|Sincronizzare tutte le modifiche ai dati per tutti i mapping di tabella.<br /><br /> È possibile sincronizzare [!INCLUDE[d365fin](includes/d365fin_md.md)] con [!INCLUDE[crm_md](includes/crm_md.md)] a intervalli pianificati impostando i processi nella coda processi.|[Pianificare una sincronizzazione](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)|  

## <a name="standard-sales-entity-mapping-for-synchronization"></a>Mapping delle entità standard di Sales per la sincronizzazione
Le entità in [!INCLUDE[crm_md](includes/crm_md.md)], come i conti, vengono integrate con i tipi di entità equivalenti in [!INCLUDE[d365fin](includes/d365fin_md.md)], quali i clienti. Per utilizzare i dati di [!INCLUDE[crm_md](includes/crm_md.md)] si impostano collegamenti, denominati associazioni, tra le entità in [!INCLUDE[d365fin](includes/d365fin_md.md)] e [!INCLUDE[crm_md](includes/crm_md.md)].

Nella seguente tabella elenca il mapping standard tra le entità in [!INCLUDE[d365fin](includes/d365fin_md.md)] e [!INCLUDE[crm_md](includes/crm_md.md)] che [!INCLUDE[d365fin](includes/d365fin_md.md)] fornisce.

|[!INCLUDE[d365fin](includes/d365fin_md.md)]|[!INCLUDE[crm_md](includes/crm_md.md)]|Direzione della sincronizzazione|Filtro predefinito|
|-------------------------------------------|-----|-------------------------|--------------|
|Agenti/Addetti acq.|Utente|[!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|Filtro contatto di Sales: il campo **Stato** è impostato su **No**, **Con licenza utente** è impostato su **Sì**, Modalità utente integrazione è su **No**|
|Cliente|Conto|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] e [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|Filtro conto di Sales: il **Tipo di relazione** è **Cliente** e lo **Stato** è **Attivo**.|
|Contatto|Contatto|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] e [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|Filtro contatto di [!INCLUDE[d365fin](includes/d365fin_md.md)]: **Tipo** è **Persona** e il contatto viene assegnato a una società. Filtro contatto di Sales: il contatto è assegnati a una società e il tipo di cliente padre è **Conto**.|
|Valuta|Valuta transazione|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
|Unità di misura|Unità di vendita|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
|Articolo|Prodotto|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] e [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|Filtro contatto di Sales: il campo **Tipo prodotto** è **Inventario vendite**|
|Risorsa|Prodotto|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] e [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|Filtro contatto di Sales: il campo **Tipo prodotto** è **Servizi**|
|Gruppo prezzi cliente|Listino prezzi|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
|Prezzo vendita|Listino prezzi prodotto|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]|Filtro contatto di [!INCLUDE[d365fin](includes/d365fin_md.md)]: **Codice vendita** non è vuoto, **Tipo vendita** è **Gruppo prezzi cliente**|
|Opportunità|Opportunità|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] e [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]| |
|Testate Fatt. Vendita|Fattura|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
|Righe Fatt. Vendita|Prodotto di fatturazione|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
|Testate ordine cliente|Ordini Vendita|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]|Filtro Testate vendita di [!INCLUDE[d365fin](includes/d365fin_md.md)]: **Tipo di documento** è Ordine, **Stato** è Rilasciato|
|Note dell'ordine di vendita|Note dell'ordine di vendita|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] e [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]| |

### <a name="tip-for-admins-viewing-entity-mappings"></a>Suggerimento per amministratori: visualizzazione di mapping di entità
È possibile visualizzare il mapping tra le entità in [!INCLUDE[crm_md](includes/crm_md.md)] e le tabelle in [!INCLUDE[d365fin](includes/d365fin_md.md)] nella pagina **Mapping tabella integrazione**, dove è anche possibile applicare filtri. È possibile definire il mapping tra i campi nelle tabelle di [!INCLUDE[d365fin](includes/d365fin_md.md)] e i campi nelle entità di [!INCLUDE[crm_md](includes/crm_md.md)] nella pagina **Mapping campo integrazione**, in cui è possibile aggiungere ulteriori logica di mapping. Ad esempio, ciò può essere utile se è necessario risolvere problemi relativi alla sincronizzazione.

### <a name="tip-for-developers-mapping-fields-in-business-central-to-the-option-sets-in-sales"></a>Suggerimento per sviluppatori: mapping dei campi in Business Central agli insiemi di opzioni in Sales
Se si è un sviluppatore e si desidera aggiungere opzioni a insiemi di opzioni in [!INCLUDE[crm_md](includes/crm_md.md)], è necessario sapere quando segue. Vi sono tre tabelle in [!INCLUDE[d365fin](includes/d365fin_md.md)] che vengono mappate ai campi delle opzioni dell'entità **Conto** in [!INCLUDE[crm_md](includes/crm_md.md)]. I record nelle tabelle che non sono collegati alle opzioni in [!INCLUDE[crm_md](includes/crm_md.md)] non verranno sincronizzati. Ciò significa che il campo **Opzione** rimarrà vuoto in [!INCLUDE[crm_md](includes/crm_md.md)].

La seguente tabella mostra i mapping delle tabelle di [!INCLUDE[d365fin](includes/d365fin_md.md)] per il campo **Opzione** dell'entità **Conto** in [!INCLUDE[crm_md](includes/crm_md.md)].

|Tavolo|Campo Opzioni nell'entità Conto|
|----------------------|-------------------------------------------|
|Condizioni pagamento|Condizioni pagamento|
|Metodo di spedizione|Indirizzo 1: Termini di spedizione|
|Spedizioniere|Indirizzo 1: metodo di spedizione|

### <a name="synchronization-rules"></a>Regole di sincronizzazione
Nella seguente tabella vengono illustrate le regole che controllano la sincronizzazione tra app.

> [!NOTE]  
> Le modifiche ai dati di [!INCLUDE[crm_md](includes/crm_md.md)] effettuate dall'account utente per la connessione di [!INCLUDE[crm_md](includes/crm_md.md)] non vengono sincronizzate. Di conseguenza, si consiglia di non modificare i dati quando si utilizza quell'account Per ulteriori informazioni, vedere [Impostazione dell'integrazione con Dynamics 365 for Sales](admin-setting-up-integration-with-dynamics-sales.md).

|Tavolo|Regola|
|-----|----|
|Clienti|Prima che un cliente possa essere sincronizzato con un conto, l'agente assegnato al cliente deve essere associato a un utente di [!INCLUDE[crm_md](includes/crm_md.md)]. Di conseguenza, quando viene eseguito il processo di sincronizzazione per CLIENTI - Dynamics 365 for Sales e lo si imposta per creare nuovi record, assicurarsi di sincronizzare l'agente con gli utenti di [!INCLUDE[crm_md](includes/crm_md.md)] prima di sincronizzare i clienti con i conti di [!INCLUDE[crm_md](includes/crm_md.md)]. <br /> <br />Il processo di sincronizzazione per CLIENTI di Dynamics 365 for Sales sincronizza solo i conti di Sales con il tipo di relazione Cliente.|
|Contatti|Solo i contatti di [!INCLUDE[crm_md](includes/crm_md.md)] associati a un conto verranno creati in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Il valore Codice agente indica il proprietario dell'entità associata in [!INCLUDE[crm_md](includes/crm_md.md)].|
|Valute|Le valute vengono associate alle valute di transazione in [!INCLUDE[crm_md](includes/crm_md.md)] in base ai codici ISO. Solo le valute con un codice dello standard ISO verranno associate e sincronizzate con le valute di transazione.|
|Unità di misura|Le unità di misura vengono sincronizzate con le unità di vendita in [!INCLUDE[crm_md](includes/crm_md.md)]. Può essere definita solo un'unità di misura nell'unità di vendita.|
|Articoli|Quando si sincronizzano gli articoli con i prodotti di [!INCLUDE[crm_md](includes/crm_md.md)], [!INCLUDE[d365fin](includes/d365fin_md.md)] crea automaticamente un listino prezzi in [!INCLUDE[crm_md](includes/crm_md.md)]. Per evitare errori di sincronizzazione, è consigliabile non modificare il listino prezzi manualmente.|
|Agenti|Gli agenti vengono associati agli utenti di sistema in [!INCLUDE[crm_md](includes/crm_md.md)]. L'utente deve essere abilitato e disporre di licenza e non deve essere l'utente di integrazione. Si noti che questa è la prima tabella che deve essere sincronizzata perché viene utilizzata nei clienti, nei contatti, nelle opportunità e nelle fatture di vendita.|
|Risorse|Le risorse vengono sincronizzate con i prodotti di [!INCLUDE[crm_md](includes/crm_md.md)] con tipo di prodotto Assistenza.|
|Gruppi prezzi cliente|Per Gruppi prezzi cliente viene eseguita la sincronizzazione con i listini prezzi di Sales.|
|Prezzi vendita|I prezzi di vendita con tipo di vendita Gruppo prezzi cliente e un codice di vendita definito vengono sincronizzati con le righe del listino prezzi di [!INCLUDE[crm_md](includes/crm_md.md)].|
|Opportunità|Le opportunità vengono sincronizzate con le opportunità di [!INCLUDE[crm_md](includes/crm_md.md)]. Il valore Codice agente indica il proprietario dell'entità associata in [!INCLUDE[crm_md](includes/crm_md.md)].|
|Fatture di vendita registrate|Le fatture di vendita registrate vengono sincronizzate con le fatture di Sales. Prima di poter sincronizzare una fattura, è meglio sincronizzare tutte le altre entità che possono essere incluse nella fattura, dai venditori ai listini prezzi. Il valore Codice agente nella testata della fattura indica il proprietario dell'entità associata in Sales.|
|Ordini vendita|Gli ordine di vendita (testate) rilasciati sono sincronizzati con gli ordini di vendita. Prima di poter sincronizzare un ordine, è meglio sincronizzare tutte le altre entità che possono essere incluse nell'ordine, dagli agenti ai listini prezzi. Il valore Codice agente nella testa dell'ordine indica il proprietario dell'entità associata in Sales.|  

## <a name="see-also"></a>Vedere anche  
[Associare e sincronizzare i record manualmente](admin-how-to-couple-and-synchronize-records-manually.md)   
[Pianificare una sincronizzazione](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)   
[Integrazione con Dynamics 365 for Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)
