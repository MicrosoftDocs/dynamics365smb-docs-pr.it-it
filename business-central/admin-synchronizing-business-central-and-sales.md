---
title: Sincronizzazione e integrazione dei dati | Microsoft Docs
description: La sincronizzazione copia i dati tra le entità di Common Data Service e i record di Business Central e mantiene i dati aggiornati in entrambi i sistemi.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 07/23/2020
ms.author: bholtorf
ms.openlocfilehash: 2c7b7c4175f4c17e01c114f76d0b14834e0409ae
ms.sourcegitcommit: 7b5c927ea9a59329daf1b60633b8290b552d6531
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/23/2020
ms.locfileid: "3617706"
---
# <a name="synchronizing-data-in-business-central-with-common-data-service"></a>Sincronizzazione di dati in Business Central con Common Data Service

Quando si integra [!INCLUDE[d365fin](includes/cds_long_md.md)] con [!INCLUDE[d365fin](includes/d365fin_md.md)], è possibile decidere se sincronizzare i dati nei campi selezionati di [!INCLUDE[d365fin](includes/d365fin_md.md)] (ad esempio clienti, contatti e agenti) con record equivalenti in [!INCLUDE[d365fin](includes/cds_long_md.md)] (come conti, contatti e utenti). A seconda del tipo di record, è possibile sincronizzare i dati da [!INCLUDE[d365fin](includes/cds_long_md.md)] a [!INCLUDE[d365fin](includes/d365fin_md.md)], o viceversa. Per ulteriori informazioni, vedere [Integrazione con Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md).  

La sincronizzazione utilizza i seguenti elementi:

* Mapping di tabella di integrazione
* Mapping di campo di integrazione
* Regole di sincronizzazione
* Record associati

Quando la sincronizzazione è impostata è possibile associare i record di [!INCLUDE[d365fin](includes/d365fin_md.md)] ai record di [!INCLUDE[d365fin](includes/cds_long_md.md)] per sincronizzare i relativi dati. È possibile avviare una sincronizzazione manualmente o in base a una programmazione. La tabella seguente fornisce una panoramica dei modi in cui è possibile sincronizzare record.  

|  Tipo  |  Metodo  |  Vedere  |  
|--------|----------|-------|  
|Sincronizzazione manuale|Sincronizzare record per record.<br /><br /> È possibile sincronizzare singoli record in [!INCLUDE[d365fin](includes/d365fin_md.md)], ad esempio un cliente, con un record di [!INCLUDE[d365fin](includes/cds_long_md.md)] corrispondente, ad esempio un conto. Questo è in genere il modo in cui gli utenti utilizzano i dati di [!INCLUDE[d365fin](includes/cds_long_md.md)] in [!INCLUDE[d365fin](includes/d365fin_md.md)].|[Associare e sincronizzare i record manualmente](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
|  |Sincronizzare in base a un mapping di tabella.<br /><br /> È possibile sincronizzare tutti i record in una tabella di [!INCLUDE[d365fin](includes/d365fin_md.md)] con un'entità di [!INCLUDE[d365fin](includes/cds_long_md.md)].|[Sincronizzare singoli mapping di tabella](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
||Sincronizzazione di tutti i record modificati per tutti i mapping di tabella.<br /><br /> È possibile sincronizzare tutte record che sono stati modificati nelle tabelle di [!INCLUDE[d365fin](includes/d365fin_md.md)] dall'ultima sincronizzazione.|[Sincronizzazione di tutti i record modificati](admin-manual-synchronization-of-table-mappings.md#synchronizing-all-modified-records)|
||Sincronizzazione completa di tutti i dati per tutti i mapping di tabella.<br /><br /> È possibile sincronizzare tutti i dati nelle tabelle di [!INCLUDE[d365fin](includes/d365fin_md.md)] e le entità di [!INCLUDE[d365fin](includes/cds_long_md.md)] mappate e creare nuovi record nella soluzione di destinazione per record non associati nella soluzione di origine.<br /><br /> La sincronizzazione completa sincronizza tutti i dati e ignora l'associazione. In genere, si effettua una sincronizzazione completa quando si imposta l'integrazione e una sola delle soluzioni contiene dati. Una sincronizzazione completa può anche risultare utile in un ambiente dimostrativo.|[Eseguire una sincronizzazione completa](admin-manual-synchronization-of-table-mappings.md#run-a-full-synchronization)|  
|Sincronizzazione pianificata|Sincronizzare tutte le modifiche ai dati per tutti i mapping di tabella.<br /><br /> È possibile sincronizzare [!INCLUDE[d365fin](includes/d365fin_md.md)] con [!INCLUDE[d365fin](includes/cds_long_md.md)] a intervalli pianificati impostando i processi nella coda processi.|[Pianificare una sincronizzazione](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)|  

## <a name="standard-entity-mapping-for-synchronization"></a>Mapping delle entità standard per la sincronizzazione
Le entità in [!INCLUDE[d365fin](includes/cds_long_md.md)], come i conti, vengono integrate con i tipi di entità equivalenti in [!INCLUDE[d365fin](includes/d365fin_md.md)], quali i clienti. Per utilizzare i dati di [!INCLUDE[d365fin](includes/cds_long_md.md)] si impostano collegamenti, denominati associazioni, tra le entità in [!INCLUDE[d365fin](includes/d365fin_md.md)] e [!INCLUDE[d365fin](includes/cds_long_md.md)].

Nella seguente tabella elenca il mapping standard tra le entità in [!INCLUDE[d365fin](includes/d365fin_md.md)] e [!INCLUDE[d365fin](includes/cds_long_md.md)] che [!INCLUDE[d365fin](includes/d365fin_md.md)] fornisce.

| [!INCLUDE[d365fin](includes/d365fin_md.md)] | [!INCLUDE[d365fin](includes/cds_long_md.md)] | Direzione della sincronizzazione | Filtro predefinito |
|---------------------------------------------|----------------------------------------------|---------------------------|----------------|
| Agenti/Addetti acq. | Utente | [!INCLUDE[d365fin](includes/cds_long_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)] | Filtro contatto di [!INCLUDE[d365fin](includes/cds_long_md.md)] : il campo **Stato** è impostato su **No**, **Con licenza utente** è impostato su **Sì**, Modalità utente integrazione è su **No** |
| Cliente | Conto | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[d365fin](includes/cds_long_md.md)] e [!INCLUDE[d365fin](includes/cds_long_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)] | Filtro conto di [!INCLUDE[d365fin](includes/cds_long_md.md)]: il **Tipo di relazione** è **Cliente** e **Stato** è **Attivo**. Filtro di [!INCLUDE[d365fin](includes/d365fin_md.md)]: **Bloccato** è vuoto (il cliente non è bloccato). |
| Fornitore | Conto | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[d365fin](includes/cds_long_md.md)] e [!INCLUDE[d365fin](includes/cds_long_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)] | Filtro conto di [!INCLUDE[d365fin](includes/cds_long_md.md)]: il **Tipo di relazione** è **Fornitore** e **Stato** è **Attivo**. Filtro di [!INCLUDE[d365fin](includes/d365fin_md.md)]: **Bloccato** è vuoto (il fornitore non è bloccato). |
| Contatto | Contatto | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[d365fin](includes/cds_long_md.md)] e [!INCLUDE[d365fin](includes/cds_long_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)] | Filtro contatto di [!INCLUDE[d365fin](includes/d365fin_md.md)]: il campo **Tipo** è **Persona** e il contatto viene assegnato a una società. Filtro contatto di [!INCLUDE[d365fin](includes/cds_long_md.md)]: il contatto è assegnati a una società e il tipo di cliente padre è **Conto** |
| Valuta | Valuta transazione | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[d365fin](includes/cds_long_md.md)] |  |


### <a name="tip-for-admins-viewing-entity-mappings"></a>Suggerimento per amministratori: visualizzazione di mapping di entità
È possibile visualizzare il mapping tra le entità in [!INCLUDE[d365fin](includes/cds_long_md.md)] e le tabelle in [!INCLUDE[d365fin](includes/d365fin_md.md)] nella pagina **Mapping tabella integrazione**, dove è anche possibile applicare filtri. È possibile definire il mapping tra i campi nelle tabelle di [!INCLUDE[d365fin](includes/d365fin_md.md)] e i campi nelle entità di [!INCLUDE[d365fin](includes/cds_long_md.md)] nella pagina **Mapping campo integrazione**, in cui è possibile aggiungere ulteriori logica di mapping. Ad esempio, ciò può essere utile se è necessario risolvere problemi relativi alla sincronizzazione.

## <a name="see-also"></a>Vedere anche  
[Associare e sincronizzare i record manualmente](admin-how-to-couple-and-synchronize-records-manually.md)   
[Pianificare una sincronizzazione](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)   
[Integrazione con Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)
