---
title: 'Dettagli di progettazione - Flussi per produzione, assemblaggio e commesse'
description: 'Scopri il flusso tra le collocazioni per il prelievo dei componenti e lo stoccaggio degli articoli finali per gli ordini di assemblaggio, produzione o commessa.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 12/16/2022
ms.custom: bap-template
---
# <a name="flows-for-production-assembly-and-jobs" />Flussi per produzione, assemblaggio e commesse

I flussi interni, come il prelievo dei componenti e lo stoccaggio degli articoli finali per ordini di assemblaggio, commesse e di produzione, sono simili ai flussi in entrata o in uscita. Quindi, molti dei processi potrebbero sembrare familiari. Questo articolo fornisce informazioni su come utilizzare i flussi di warehouse interni con vari livelli di complessità.

## <a name="overview-of-different-configuration-options" />Panoramica delle diverse opzioni di configurazione

È possibile configurare le funzionalità warehouse in vari modi. È importante che le opzioni che scegli migliorino i tuoi processi senza causare sovraccarico. Le seguenti tabelle descrivono le configurazioni tipiche per la gestione dei beni fisici per ordini di produzione, commesse e assemblaggio.

### <a name="inbound-flow-put-away" />Flusso in entrata (stoccaggio)

|Livello di complessità|Descrizione|Impostazioni|Codice collocazione|Flusso in entrata dell'ordine di produzione|Flusso in entrata dell'ordine di assemblaggio|Flusso in entrata delle commesse|  
|---|----------------|----------|---------|------------------|------------------|------------------|
|Nessuna attività di warehouse dedicata.|Contabilizzazione di ordini e registrazioni.||Facoltativo. Controllato dall'interruttore **Il codice collocazione è obbligatorio**.|Registrazioni di produzione -> Registrazioni di output</br><br/> **NOTA**: puoi registrare l'output utilizzando **Registrazioni di produzione**.|Ordine di assemblaggio|Lo stoccaggio non è applicabile per le commesse|  
|Di base|Ordine per ordine.|Richiesto stoccaggio. </br><br/> **NOTA**: Anche se l'impostazione è chiamata **Richiesto stoccaggio**, puoi ancora registrare l'output dai documenti di origine nelle ubicazioni in cui selezioni questa casella di controllo. |Facoltativo. Controllato dall'interruttore **Il codice collocazione è obbligatorio**.|Ordine di produzione -> Stoccaggio in magazzino|Ordine di assemblaggio|Lo stoccaggio non è applicabile per le commesse|
|Avanzate|Attività di stoccaggio consolidate per più documenti di origine.|Richiesto carico + Richiesto stoccaggio|Facoltativo. Controllato dall'interruttore **Il codice collocazione è obbligatorio**.|Ordini di produzione -> Registrazioni output|Ordini di assemblaggio -> Movimenti interni | Lo stoccaggio non è applicabile per le commesse|
|Avanzate|Come sopra + Attività di prelievo/stoccaggio diretti|Prelievo e stoccaggio diretti (gli interruttori dipendenti verranno abilitati automaticamente)|Obbligatorio|Come sopra.|Come sopra.| Lo stoccaggio non è applicabile per le commesse|

Alcune configurazioni non consentono di utilizzare documenti di warehouse dedicati per registrare gli stoccaggi. Tuttavia, se l'ubicazione utilizza le collocazioni, è possibile utilizzare i documenti di movimento generici per spostare gli articoli prodotti o assemblati nella warehouse. Per ulteriori informazioni vedi [Spostare gli articoli internamente nelle configurazioni warehouse di base](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).

### <a name="outbound-flow-pick" />Flusso in uscita (prelievo)

|Livello di complessità|Descrizione|Impostazioni|Codice collocazione|Flusso in uscita dell'ordine di produzione|Flusso in uscita dell'ordine di assemblaggio|Flusso in uscita delle commesse|  
|---|----------------|----------|---------|------------------|------------------|------------------|
|Nessuna attività di warehouse dedicata.|Contabilizzazione di ordini e registrazioni.||Facoltativo. Controllato dall'interruttore **Il codice collocazione è obbligatorio**.|Registrazioni di produzione -> Registrazioni consumi </br><br/> **NOTA**: puoi registrare il consumo utilizzando **Registrazioni di produzione**.|Ordine di assemblaggio|Commessa -> Registrazioni commesse|  
|Di base|Ordine per ordine.|Richiesto prelievo. </br><br/> **NOTA**: Anche se l'impostazione è chiamata **Richiesto prelievo**, puoi ancora registrare l'output dai documenti di origine nelle ubicazioni in cui selezioni questa casella di controllo. <!-- ToDo Test prod output-->|Facoltativo. Controllato dall'interruttore **Il codice collocazione è obbligatorio**.|Ordine di produzione -> Prelievo in magazzino|Ordine di assemblaggio -> Movimento di magazzino</br><br/>L'opzione **Movimento di magazzino** può essere utilizzata solo con le collocazioni.|Commessa -> Prelievi magazzino|
|Avanzate|Attività di prelievo consolidate per più documenti di origine.|Richiesta spedizione + Richiesto prelievo|Facoltativo. Controllato dall'interruttore Il codice collocazione è obbligatorio|Ordini di produzione -> Prelievi warehouse -> Registrazioni consumi |Ordini di assemblaggio -> Prelievo warehouse| Commesse -> Prelievo warehouse -> Registrazioni commesse |
|Avanzate|Come sopra + Attività di prelievo/stoccaggio diretti|Prelievo e stoccaggio diretti (gli interruttori dipendenti verranno abilitati automaticamente)|Obbligatorio|Come sopra.|Come sopra.| Lo stoccaggio e il prelievo diretti non sono supportati per le commesse|

Analogamente al flusso in entrata, alcune configurazioni non consentono di utilizzare documenti di warehouse dedicati per registrare gli stoccaggi. Se l'ubicazione utilizza le collocazioni, è possibile utilizzare i documenti di movimento generici per spostare gli articoli prodotti o assemblati. Per ulteriori informazioni vedi [Spostamento degli articoli](warehouse-move-items.md).

## <a name="warehouses-without-dedicated-warehouse-activity" />Warehouse senza attività di warehouse dedicata

Anche se non hai attività di warehouse dedicate, probabilmente vorrai comunque tenere traccia di cose come il consumo e la produzione. I seguenti articoli forniscono informazioni su come elaborare le ricevute per i documenti di origine.

* [Registrare i consumi e l'output relativi a una singola riga dell'ordine di produzione rilasciato](production-how-to-register-consumption-and-output.md)
* [Assemblare articoli](assembly-how-to-assemble-items.md)
* [Registrare il consumo o l'uso per i lavori](projects-how-record-job-usage.md)

## <a name="basic-warehouse-configuration" />Configurazione warehouse di base

I flussi in entrata e in uscita in una configurazione warehouse di base comportano le seguenti impostazioni nella pagina **Scheda ubicazione** per l'ubicazione:

* Per il flusso in entrata (stoccaggio), attiva l'interruttore **Richiesto stoccaggio** ma disattiva l'interruttore **Richiesto carico**.
* Per il flusso in uscita (prelievo), attiva l'interruttore **Richiesto prelievo** ma disattiva l'interruttore **Richiesta spedizione**.

### <a name="flows-to-and-from-production-in-a-basic-warehouse-configuration" />I flussi da e verso la produzione in una configurazione warehouse di base

Utilizza i documenti **prelievo magazzino** per prelevare i componenti di produzione nel flusso verso la produzione. Per stoccare i prodotti che produci, usa i documenti **Stoccaggio in magazzino**.

Per le ubicazioni che utilizzano le collocazioni, i documenti di movimento magazzino sono particolarmente utili per la consuntivazione dei componenti. Per ulteriori informazioni su come il consumo del componente è consuntivato dalla collocazione articoli per produzione o produzione aperta, vedi [Consuntivazione componenti di produzione nel magazzino](warehouse-how-to-pick-for-production.md#flushing-production-components-in-a-basic-warehouse-configuration).

   > [!NOTE]
   > I movimenti di inventario sono documenti importanti se utilizzi i metodi di consuntivazione **Prelievo + Avanti** o **Prelievo + indietro**. Per ulteriori informazioni vedi [Metodi di consuntivazione](production-how-to-flush-components-according-to-operation-output.md#flushing-methods).

* I campi **Cod. coll. art. per produzione**, **Cod. coll. art. da produzione** e **Codice coll. produzione aperta** nell'ubicazione o nel centro di lavoro/area di produzione definiscono i flussi predefiniti da e verso le aree di produzione.
* Gestisci il movimento degli articoli prodotti nella pagina **Movimento interno** senza una relazione con un ordine di produzione.

### <a name="flows-to-and-from-assembly-in-a-basic-warehouse-configuration" />I flussi da e verso l'assemblaggio in una configurazione warehouse di base

Registra l'output e il consumo dell'assemblaggio direttamente da un ordine di assemblaggio.

> [!NOTE]
> I documenti **Prelievo di magazzino** e **Stoccaggio di magazzino** non sono supportati per gli ordini di assemblaggio.

Per le ubicazioni che usano le collocazioni:

* Utilizza i documenti **Movimento magazzino** per spostare i componenti dell'assemblaggio nell'area di assemblaggio.
* I campi **Cod. coll. art. per assembl.** e **Cod. coll. art. da assembl.** nella scheda ubicazione definiscono i flussi predefiniti da e verso le aree di assemblaggio.
* Gestisci il movimento degli articoli assemblati nella pagina **Movimento interno** senza una relazione con un ordine di assemblaggio.

[!INCLUDE [prod_short](includes/prod_short.md)] supporta i flussi assemblaggio su ordine e assemblaggio per magazzino. Per ulteriori informazioni vedi [Assemblaggio su ordine e assemblaggio per magazzino](assembly-assemble-to-order-or-assemble-to-stock.md#understanding-assemble-to-order-and-assemble-to-stock). In relazione alla gestione della warehouse, l'assemblaggio per magazzino fa parte del flusso warehouse interno e l'assemblaggio su ordine è nel flusso warehouse in uscita. Ulteriori informazioni in [Gestione di articoli da assemblare su ordine con prelievi magazzino](warehouse-how-to-pick-items-with-inventory-picks.md#handling-assemble-to-order-items-with-inventory-picks).

### <a name="flows-for-project-management-in-a-basic-warehouse-configuration" />Flussi per la gestione dei progetti in una configurazione warehouse di base

Utilizza i documenti **prelievo magazzino** per il prelievo dei componenti di commessa nel flusso verso la gestione progetti.

Per un'ubicazione che utilizza le collocazioni, il campo **A commessa - Codice collocazione** nell'ubicazione definisce i flussi predefiniti per la gestione dei progetti.

## <a name="advanced-warehouse-configurations" />Configurazioni avanzate della warehouse

I flussi in entrata e in uscita in una configurazione warehouse avanzata comportano le seguenti impostazioni nella pagina **Scheda ubicazione** per l'ubicazione:

* Per il flusso in entrata (stoccaggio), attiva gli interruttori **Richiesto carico** e **Richiesto stoccaggio**.
* Per il flusso in uscita (prelievo), attiva gli interruttori **Richiesta spedizione** e **Richiesto carico**.

### <a name="flows-to-and-from-production-in-advanced-warehouse-configurations" />I flussi da e verso la produzione in una configurazione warehouse avanzata

Utilizza i documenti **Prelievo warehouse** e la pagina **Prospetto prelievi** per prelevare i componenti per la produzione.

Per le ubicazioni che usano le collocazioni:

* I documenti **Movimento warehouse** e la pagina **Prospetti movimenti** sono particolarmente utili per la consuntivazione dei componenti. Per ulteriori informazioni vedi [Consuntivazione componenti di produzione nel magazzino](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md#flushing-production-components-in-a-advanced-warehouse-configuration).
* I campi **Cod. coll. art. per produzione**, **Cod. coll. art. da produzione** e **Codice coll. produzione aperta** nell'ubicazione o nel centro di lavoro/area di produzione definiscono i flussi predefiniti da e verso le aree di produzione. 
* Gestisci il movimento degli articoli prodotti nelle pagine **Prospetto movimenti** o **Stoccaggio interno whse.** senza una relazione con un ordine di produzione.

### <a name="flows-to-and-from-assembly-in-advanced-warehouse-configurations" />I flussi da e verso l'assemblaggio in una configurazione warehouse avanzata

Utilizza i documenti **Prelievo warehouse** e la pagina **Prospetto prelievi** per prelevare i componenti per l'assemblaggio.

Per le ubicazioni che usano le collocazioni:

* I campi **Cod. coll. art. per assembl.** e **Cod. coll. art. da assembl.** nell'ubicazione definiscono i flussi predefiniti da e verso le aree di assemblaggio.
* Gestisci il movimento degli articoli assemblaggio nelle pagine **Prospetto movimenti** o **Stoccaggio interno whse.** senza una relazione con un ordine di assemblaggio.

[!INCLUDE [prod_short](includes/prod_short.md)] supporta i flussi assemblaggio su ordine e assemblaggio per magazzino. Per ulteriori informazioni vedi [Assemblaggio su ordine e assemblaggio per magazzino](assembly-assemble-to-order-or-assemble-to-stock.md#understanding-assemble-to-order-and-assemble-to-stock). 

L'assemblaggio per magazzino fa parte del flusso warehouse interno e l'assemblaggio su ordine è nel flusso warehouse in uscita. Per ulteriori informazioni vedi [Gestione di articoli di assemblaggio su ordine in spedizioni warehouse](warehouse-how-ship-items.md#handling-assemble-to-order-items-in-warehouse-shipments).

### <a name="flows-to-project-management-in-advanced-warehouse-configurations" />Flussi per la gestione dei progetti in una configurazione warehouse avanzata

Utilizza i documenti **Prelievo warehouse** e la pagina **Prospetto prelievi** per prelevare i componenti nel flusso per la gestione dei progetti.

Per le ubicazioni che utilizzano le collocazioni, il campo **A commessa - Codice collocazione** nell'ubicazione definisce i flussi predefiniti per l'area dei progetti.

## <a name="see-also" />Vedere anche

[Panoramica gestione del magazzino](design-details-warehouse-management.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
