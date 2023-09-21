---
title: Sincronizzazione e integrazione dei dati | Microsoft Docs
description: La sincronizzazione copia i dati tra le tabelle di Microsoft Dataverse e i record di Business Central e mantiene i dati aggiornati in entrambi i sistemi.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.date: 03/31/2023
ms.custom: bap-template
ms.search.keywords: 'Dataverse, integration, sync, synchronize, mapping'
---

# Sincronizzazione di dati in Business Central con Microsoft Dataverse

Quando si integra [!INCLUDE[prod_short](includes/cds_long_md.md)] con [!INCLUDE[prod_short](includes/prod_short.md)], è possibile decidere se sincronizzare i dati nei campi selezionati di [!INCLUDE[prod_short](includes/prod_short.md)] (ad esempio clienti, contatti e agenti) con righe equivalenti in [!INCLUDE[prod_short](includes/cds_long_md.md)] (come conti, contatti e utenti). A seconda del tipo di riga, è possibile sincronizzare i dati da [!INCLUDE[prod_short](includes/cds_long_md.md)] a [!INCLUDE[prod_short](includes/prod_short.md)], o viceversa. Per ulteriori informazioni, vedere [Integrazione con Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md).  

La sincronizzazione utilizza i seguenti elementi:

* Mapping di tabella di integrazione
* Mapping di campo di integrazione
* Regole di sincronizzazione
* Record associati

Quando la sincronizzazione è impostata è possibile associare i record di [!INCLUDE[prod_short](includes/prod_short.md)] alle righe di [!INCLUDE[prod_short](includes/cds_long_md.md)] per sincronizzare i relativi dati. È possibile avviare una sincronizzazione manualmente o in base a una programmazione. La tabella seguente fornisce una panoramica dei modi in cui è possibile eseguire la sincronizzazione.  

|  Tipo  |  Metodo  |  Vedere  |  
|--------|----------|-------|  
|Sincronizzazione manuale|Sincronizzare riga per riga.<br /><br /> È possibile sincronizzare singoli record in [!INCLUDE[prod_short](includes/prod_short.md)], ad esempio un cliente, con una riga di [!INCLUDE[prod_short](includes/cds_long_md.md)] corrispondente, ad esempio un conto. Questo è in genere il modo in cui gli utenti utilizzano i dati di [!INCLUDE[prod_short](includes/cds_long_md.md)] in [!INCLUDE[prod_short](includes/prod_short.md)].|[Associare e sincronizzare i record manualmente](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
|  |Sincronizzare in base a un mapping di tabella.<br /><br /> È possibile sincronizzare tutti i record in una tabella di [!INCLUDE[prod_short](includes/prod_short.md)] con una tabella di [!INCLUDE[prod_short](includes/cds_long_md.md)].|[Sincronizzare singoli mapping di tabella](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
||Sincronizzazione di tutti i record modificati per tutti i mapping di tabella.<br /><br /> È possibile sincronizzare tutte record che sono stati modificati nelle tabelle di [!INCLUDE[prod_short](includes/prod_short.md)] dall'ultima sincronizzazione.|[Sincronizzazione di tutti i record modificati](admin-manual-synchronization-of-table-mappings.md#synchronizing-all-modified-records)|
||Sincronizzazione completa di tutti i dati per tutti i mapping di tabella.<br /><br /> È possibile sincronizzare tutti i dati nelle tabelle di [!INCLUDE[prod_short](includes/prod_short.md)] e [!INCLUDE[prod_short](includes/cds_long_md.md)] mappate e creare nuovi record o righe nella soluzione di destinazione per record non associati nella soluzione di origine.<br /><br /> La sincronizzazione completa sincronizza tutti i dati e ignora l'associazione. In genere, si effettua una sincronizzazione completa quando si imposta l'integrazione e una sola delle soluzioni contiene dati. Una sincronizzazione completa può anche risultare utile in un ambiente dimostrativo.|[Eseguire una sincronizzazione completa](admin-manual-synchronization-of-table-mappings.md#run-a-full-synchronization)|  
|Sincronizzazione pianificata|Sincronizzare tutte le modifiche ai dati per tutti i mapping di tabella.<br /><br /> È possibile sincronizzare [!INCLUDE[prod_short](includes/prod_short.md)] con [!INCLUDE[prod_short](includes/cds_long_md.md)] a intervalli pianificati impostando i processi nella coda processi.|[Pianificare una sincronizzazione](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)|  

> [!NOTE]
> La sincronizzazione tra [!INCLUDE[prod_short](includes/cds_long_md.md)] e [!INCLUDE[prod_short](includes/prod_short.md)] si basa sull'esecuzione pianificata delle voci della coda dei lavori e non garantisce la coerenza dei dati in tempo reale tra due servizi. Per la coerenza dei dati in tempo reale vai a [Tabelle virtuali di Business Central](/dynamics365/business-central/dev-itpro/powerplatform/powerplat-overview) o API di Business Central.   


## Mapping delle tabelle standard per la sincronizzazione
Le tabelle in [!INCLUDE[prod_short](includes/cds_long_md.md)], come i conti, vengono integrate con i tipi di tabelle equivalenti in [!INCLUDE[prod_short](includes/prod_short.md)], quali i clienti. Per utilizzare i dati di [!INCLUDE[prod_short](includes/cds_long_md.md)] si impostano collegamenti, denominati associazioni, tra le tabelle in [!INCLUDE[prod_short](includes/prod_short.md)] e [!INCLUDE[prod_short](includes/cds_long_md.md)].

Nella seguente tabella è elencato il mapping standard tra le tabelle in [!INCLUDE[prod_short](includes/prod_short.md)] e [!INCLUDE[prod_short](includes/cds_long_md.md)].

> [!TIP]
> È possibile ripristinare le modifiche di configurazione apportate alla tabella di integrazione e ai mapping dei campi sulle impostazioni predefinite selezionando i mapping e quindi scegliendo **Utilizza setup sincronizzazione predefinito**.

| [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[prod_short](includes/cds_long_md.md)] | Direzione della sincronizzazione | Filtro predefinito |
|---------------------------------------------|----------------------------------------------|---------------------------|----------------|
| Agenti/Addetti acq. | Utente | [!INCLUDE[prod_short](includes/cds_long_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | Filtro contatto di [!INCLUDE[prod_short](includes/cds_long_md.md)] : il campo **Stato** è impostato su **No**, **Con licenza utente** è impostato su **Sì**, Modalità utente integrazione è su **No** |
| Cliente | Conto | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] e [!INCLUDE[prod_short](includes/cds_long_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | Filtro conto di [!INCLUDE[prod_short](includes/cds_long_md.md)]: il **Tipo di relazione** è **Cliente** e **Stato** è **Attivo**. Filtro di [!INCLUDE[prod_short](includes/prod_short.md)]: **Bloccato** è vuoto (il cliente non è bloccato). |
| Fornitore | Conto | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] e [!INCLUDE[prod_short](includes/cds_long_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | Filtro conto di [!INCLUDE[prod_short](includes/cds_long_md.md)]: il **Tipo di relazione** è **Fornitore** e **Stato** è **Attivo**. Filtro di [!INCLUDE[prod_short](includes/prod_short.md)]: **Bloccato** è vuoto (il fornitore non è bloccato). |
| Contatto | Contatto | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] e [!INCLUDE[prod_short](includes/cds_long_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | Filtro contatto di [!INCLUDE[prod_short](includes/prod_short.md)]: il campo **Tipo** è **Persona** e il contatto viene assegnato a una società. Filtro contatto [!INCLUDE[prod_short](includes/cds_long_md.md)]: il contatto è assegnato a una società e il tipo di cliente padre è **Cliente**. |
| Valuta | Valuta transazione | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] |  |

> [!NOTE]
> Le azioni **Dataverse** non saranno disponibili nelle pagine, ad esempio, la pagina Scheda cliente, per i record che non rispettano il filtro tabella sul mapping di tabelle di integrazione.

### Suggerimento per amministratori: visualizzazione di mapping di tabelle
È possibile visualizzare il mapping tra le tabelle in [!INCLUDE[prod_short](includes/cds_long_md.md)] e le tabelle in [!INCLUDE[prod_short](includes/prod_short.md)] nella pagina **Mapping tabella integrazione**, dove è anche possibile applicare filtri. È possibile definire il mapping tra i campi nelle tabelle di [!INCLUDE[prod_short](includes/prod_short.md)] e le colonne nelle tabelle di [!INCLUDE[prod_short](includes/cds_long_md.md)] nella pagina **Mapping campo integrazione**, in cui è possibile aggiungere ulteriori logica di mapping. Ad esempio, ciò può essere utile se è necessario risolvere problemi relativi alla sincronizzazione.

## Vedere anche  
[Associare e sincronizzare i record manualmente](admin-how-to-couple-and-synchronize-records-manually.md)   
[Pianificare una sincronizzazione](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)   
[Integrazione con Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
