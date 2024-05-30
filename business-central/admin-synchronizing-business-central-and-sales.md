---
title: Sincronizzazione e integrazione dei dati
description: La sincronizzazione copia i dati tra le tabelle di Microsoft Dataverse e i record di Business Central e mantiene i dati aggiornati in entrambi i sistemi.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 05/07/2024
ms.custom: bap-template
ms.search.keywords: 'Dataverse, integration, sync, synchronize, mapping'
ms.service: dynamics-365-business-central
---

# <a name="synchronizing-data-in-business-central-with-microsoft-dataverse"></a>Sincronizzazione dei dati in Business Central con Microsoft Dataverse

Quando si integra [!INCLUDE[prod_short](includes/cds_long_md.md)] con [!INCLUDE[prod_short](includes/prod_short.md)], è possibile decidere se sincronizzare i dati nei campi selezionati di [!INCLUDE[prod_short](includes/prod_short.md)] (ad esempio clienti, contatti e agenti) con righe equivalenti in [!INCLUDE[prod_short](includes/cds_long_md.md)] (come conti, contatti e utenti). A seconda del tipo di riga, è possibile sincronizzare i dati da [!INCLUDE[prod_short](includes/cds_long_md.md)] a [!INCLUDE[prod_short](includes/prod_short.md)], o viceversa. Per ulteriori informazioni, vedere [Integrazione con Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md).  

La sincronizzazione utilizza i seguenti elementi:

* Mapping della tabella di integrazione
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

## <a name="standard-table-mapping-for-synchronization"></a>Mapping delle tabelle standard per la sincronizzazione

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
> Le azioni **Dataverse** non saranno disponibili nelle pagine, ad esempio, la pagina Scheda cliente, per i record che non rispettano il filtro tabella sul mapping della tabella di integrazione.

### <a name="tip-for-admins-viewing-table-mappings"></a>Suggerimento per amministratori: visualizzazione dei mapping delle tabelle

È possibile visualizzare il mapping tra le tabelle in [!INCLUDE[prod_short](includes/cds_long_md.md)] e le tabelle in [!INCLUDE[prod_short](includes/prod_short.md)] nella pagina **Mapping tabella integrazione**, dove è anche possibile applicare filtri. È possibile definire il mapping tra i campi nelle tabelle di [!INCLUDE[prod_short](includes/prod_short.md)] e le colonne nelle tabelle di [!INCLUDE[prod_short](includes/cds_long_md.md)] nella pagina **Mapping campo integrazione**, in cui è possibile aggiungere ulteriori logica di mapping. Ad esempio, ciò può essere utile se è necessario risolvere problemi relativi alla sincronizzazione.

## <a name="use-virtual-tables-to-get-more-data"></a>Utilizzare tabelle virtuali per ottenere più dati

Quando configuri l'integrazione, puoi utilizzare le tabelle virtuali per rendere disponibili più dati in [!INCLUDE[prod_short](includes/cds_long_md.md)], senza l'aiuto di uno sviluppatore.

Una tabella virtuale è una tabella personalizzata con colonne e righe contenenti dati di un'origine dati esterna, come [!INCLUDE [prod_short](includes/prod_short.md)]. Le colonne e le righe in una tabella virtuale hanno l'aspetto di una tabella normale, tuttavia, i dati non vengono archiviati in una tabella fisica nel database [!INCLUDE[prod_short](includes/cds_long_md.md)]. In effetti, i dati vengono recuperati in fase di esecuzione.

> [!NOTE]
> [!INCLUDE [prod_short](includes/prod_short.md)] contiene oggetti denominati anche tabelle virtuali. Questi oggetti non sono correlati alle tabelle virtuali utilizzate con [!INCLUDE[prod_short](includes/cds_long_md.md)].

Per ulteriori informazioni sulle tabelle virtuali, consulta i seguenti articoli:

* [Creare e modificare tabelle virtuali che contengono dati di un'origine dati esterna](/power-apps/maker/data-platform/create-edit-virtual-entities) (documentazione di Power Apps)
* [Riferimento per amministratori di Business Central Virtual Table per Microsoft Dataverse](/dynamics365/business-central/dev-itpro/powerplatform/powerplat-admin-reference) (documentazione di [!INCLUDE [prod_short](includes/prod_short.md)])

Per utilizzare le tabelle virtuali, devi installare l'app **Business Central Virtual Entity** da [AppSource](https://appsource.microsoft.com/en-US/product/dynamics-365/microsoftdynsmb.businesscentral_virtualentity). 

Dopo aver installato l'app, puoi abilitare le tabelle virtuali da una delle seguenti pagine in [!INCLUDE [prod_short](includes/prod_short.md)]:

* Quando esegui la guida al setup assistito **Imposta connessione a Dataverse**, puoi utilizzare la pagina **Tabelle virtuali disponibili in Dataverse** per selezionare più tabelle virtuali. Successivamente, le tabelle sono disponibili in [!INCLUDE[prod_short](includes/cds_long_md.md)] e in PowerApps Maker Portal. 
* Dalle pagine **Imposta connessione a Dataverse**, **Tabelle virtuali** e **Tabelle virtuali disponibili**.  
* Da Power App Maker Portal.

## <a name="synchronize-data-from-multiple-companies-or-environments"></a>Sincronizzare i dati di più società o ambienti

Puoi sincronizzare i dati di più società o ambienti [!INCLUDE [prod_short](includes/prod_short.md)] con un ambiente [!INCLUDE[prod_short](includes/cds_long_md.md)]. Negli scenari di sincronizzazione di più società, ci sono diversi aspetti da considerare.

### <a name="set-company-ids"></a>Impostare ID società

Quando sincronizzi i record, impostiamo un ID società sull'entità [!INCLUDE[prod_short](includes/cds_long_md.md)] per chiarire la società [!INCLUDE [prod_short](includes/prod_short.md)] da cui provengono i record. I mapping della tabella di integrazione dispongono di campi filtro della tabella di integrazione che tengono conto dell'ID società. Per includere un mapping di tabella in una configurazione di più società, nella pagina **Mapping tabelle integrazione**, scegli la casella di controllo **Sincronizzazione di più società abilitata**. L'impostazione ottimizza il modo in cui i campi filtro della tabella di integrazione filtrano gli ID società in una configurazione di più società.

Per i mapping della tabella di integrazione che sincronizzano documenti, come ordini, preventivi e opportunità, se scegli la casella di controllo **Sincronizzazione di più società abilitata** l'integrazione considera solo le entità che hanno l'ID società della società [!INCLUDE [prod_short](includes/prod_short.md)] corrente. Per sincronizzare i documenti, ad esempio, tra Business Central e Sales, gli utenti in Sales devono specificare l'ID società nei documenti. In caso contrario, i documenti non verranno sincronizzati.  

Per tutti gli altri mapping della tabella di integrazione, scegliendo la casella di controllo **Sincronizzazione di più società abilitata** si rimuove il filtro sull'ID società. La sincronizzazione prenderà in considerazione entità correlate, indipendentemente dal relativo ID società.

### <a name="specify-the-synchronization-direction"></a>Specificare la direzione della sincronizzazione

Se abiliti il ​​supporto per più società in un mapping della tabella di integrazione, ti consigliamo di impostare la direzione del mapping su **FromIntegration**. Se imposti la direzione su **ToIntegration** o **Bidirectional**, è buona idea usare **Filtro tabella**  e **Filtro tabella integrazione**  per controllare quali entità si sincronizzano con quale società. È una buona idea anche utilizzare l'associazione basata su corrispondenza per evitare la creazione di record duplicati. Per saperne di più sull'associazione basata su corrispondenza, vedi [Personalizzare l'associazione basata su corrispondenza](/dynamics365/business-central/admin-how-to-set-up-a-dynamics-crm-connection#customize-the-match-based-coupling).

### <a name="use-unique-numbers"></a>Utilizzare numeri univoci

Se la serie numerica non garantisce che i valori della chiave primaria siano univoci per ogni società, ti consigliamo di utilizzare i prefissi. Per iniziare a utilizzare i prefissi, crea una regola di trasformazione nel mapping dei campi di integrazione. Per ulteriori informazioni sulle regole di trasformazione, vedi [Gestire le differenze nei valori di campi](admin-how-to-modify-table-mappings-for-synchronization.md#handle-differences-in-field-values).

## <a name="see-also"></a>Vedere anche

[Associare e sincronizzare i record manualmente](admin-how-to-couple-and-synchronize-records-manually.md)   
[Programmare una sincronizzazione](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
[Integrazione con Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
