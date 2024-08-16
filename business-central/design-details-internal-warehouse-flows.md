---
title: 'Dettagli di progettazione: flussi per produzione, assemblaggio e progetti'
description: 'Scopri il flusso tra le collocazioni per il prelievo dei componenti e lo stoccaggio degli articoli finali per gli ordini di assemblaggio, produzione o progetto.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 08/12/2024
ms.custom: bap-template
---
# Flussi per produzione, assemblaggio e progetti

I flussi interni, come il prelievo dei componenti e lo stoccaggio degli articoli finali per ordini di assemblaggio, progetto e produzione, sono simili ai flussi in entrata o in uscita. Molti dei processi potrebbero sembrarti familiari. Questo articolo fornisce informazioni su come utilizzare i flussi di warehouse interni con vari livelli di complessità.

## Panoramica delle diverse opzioni di configurazione

È possibile configurare le funzionalità warehouse in vari modi. È importante che le opzioni che scegli migliorino i tuoi processi senza causare sovraccarico. Le seguenti tabelle descrivono le configurazioni tipiche per la gestione dei beni fisici per ordini di produzione, progetto e assemblaggio.

### Flusso in entrata (stoccaggio)

|Livello di complessità|Descrizione|Impostazioni|Codice collocazione|Flusso in entrata dell'ordine di produzione|Flusso in entrata dell'ordine di assemblaggio|Flusso in entrata di progetti|  
|---|----------------|----------|---------|------------------|------------------|------------------|
|Nessuna attività di warehouse dedicata.|Contabilizzazione di ordini e registrazioni.||Facoltativo. Controllato dall'interruttore **Il codice collocazione è obbligatorio**.|Registrazioni di produzione -> Registrazioni di output</br><br/> **NOTA**: puoi registrare l'output utilizzando **Registrazioni di produzione**.|Ordine di assemblaggio|Il riordino non è applicabile ai progetti|  
|Base|Ordine per ordine.|Produzione Output Movimentazione in magazzino: Stoccaggio inventario. </br><br/> **NOTA**: puoi comunque pubblicare l'output direttamente dai documenti di origine nelle posizioni in cui hai attivato queste impostazioni. |Facoltativo. Controllato dall'interruttore **Il codice collocazione è obbligatorio**.|Ordine di produzione -> Stoccaggio in magazzino|Ordine di assemblaggio|Il riordino non è applicabile ai progetti|
|Avanzata|Attività di stoccaggio consolidate per più documenti di origine.|Nessuna impostazione dedicata|Facoltativo. Controllato dall'interruttore **Il codice collocazione è obbligatorio**.|Ordini di produzione -> Registrazioni output|Ordini di assemblaggio -> Movimenti interni | Il riordino non è applicabile ai progetti|
|Avanzata|Come sopra più attività di prelievo/riordino guidate|Prelievo e stoccaggio diretti (gli interruttori dipendenti verranno abilitati automaticamente)|Obbligatorio|Come sopra|Come sopra| Il riordino non è applicabile ai progetti|

Alcune configurazioni non consentono di utilizzare documenti di magazzino dedicati per registrare gli stoccaggi. Tuttavia, se l'ubicazione utilizza le collocazioni, è possibile utilizzare i documenti di movimento generici per spostare gli articoli prodotti o assemblati nella warehouse. Per ulteriori informazioni vedi [Spostamento degli articoli](warehouse-move-items.md).

### Flusso in uscita (prelievo)

|Livello di complessità|Descrizione|Impostazioni|Codice collocazione|Flusso in uscita dell'ordine di produzione|Flusso in uscita dell'ordine di assemblaggio|Flusso in uscita di progetti|  
|---|----------------|----------|---------|------------------|------------------|------------------|
|Nessuna attività di warehouse dedicata.|Contabilizzazione di ordini e registrazioni.||Facoltativo. Controllato dall'interruttore **Il codice collocazione è obbligatorio**.|Registrazioni di produzione -> Registrazioni consumi </br><br/> **NOTA**: puoi registrare il consumo utilizzando **Registrazioni di produzione**.|Ordine di assemblaggio|Progetto -> Registrazione progetti|  
|Base|Ordine per ordine.|Produzione, assemblaggio, progetti: prelievo inventario, movimento inventario </br><br/> **NOTA**: puoi comunque registrare il consumo direttamente dai documenti di origine nelle posizioni in cui hai attivato queste impostazioni.|Facoltativo. Controllato dall'interruttore **Il codice collocazione è obbligatorio**.|Ordine di produzione -> Prelievo in magazzino|Ordine di assemblaggio -> Movimento di magazzino</br><br/>L'opzione **Movimento di magazzino** può essere utilizzata solo con le collocazioni.|Progetto -> Prelievi magazzino|
|Avanzata|Attività di prelievo consolidate per più documenti di origine.|Produzione, assemblaggio, progetti: prelievo magazzino|Facoltativo. Controllato dall'interruttore Il codice collocazione è obbligatorio|Ordini di produzione -> Prelievi warehouse -> Registrazioni consumi |Ordini di assemblaggio -> Prelievo warehouse| Progetti -> Prelievo warehouse -> Registrazione progetti |
|Avanzata|Come sopra + Attività di prelievo/stoccaggio diretti|Prelievo e stoccaggio diretti (gli interruttori dipendenti verranno abilitati automaticamente)|Obbligatorio|Come sopra|Come sopra| Il prelievo e lo stoccaggio diretti non sono supportati per i progetti|

## Warehouse senza attività di warehouse dedicata

Anche se non si utilizzano attività di magazzino dedicate, potrebbe essere opportuno monitorare aspetti quali consumi e produzione. I seguenti articoli forniscono informazioni su come elaborare le ricevute per i documenti di origine.

* [Registrare i consumi e l'output relativi a una singola riga dell'ordine di produzione rilasciato](production-how-to-register-consumption-and-output.md)
* [Assemblare articoli](assembly-how-to-assemble-items.md)
* [Registrare il consumo o l'uso per i progetti](projects-how-record-job-usage.md)

## Configurazione warehouse di base

### I flussi da e verso la produzione in una configurazione warehouse di base  

I flussi in entrata e in uscita in una configurazione warehouse di base comportano le seguenti impostazioni nella pagina **Scheda ubicazione** per l'ubicazione:

* Per il flusso in entrata (stoccaggio), nel campo  **Prod. Output Whse. Handling**, Seleziona **Stoccaggio inventario**.
* Per il flusso in uscita (prelievo), nel campo  **Prod. Consumo Whse. Movimentazione**, Seleziona **Prelievo/Movimento inventario**.

Utilizza i documenti **prelievo magazzino** per prelevare i componenti di produzione nel flusso verso la produzione. Per stoccare i prodotti che produci, usa i documenti **Stoccaggio in magazzino**.

Per le ubicazioni che utilizzano le collocazioni, i documenti di movimento magazzino sono particolarmente utili per la consuntivazione dei componenti. Per ulteriori informazioni su come il consumo del componente è consuntivato dalla collocazione articoli per produzione o produzione aperta, vedi [Consuntivazione componenti di produzione nel magazzino](warehouse-how-to-pick-for-production.md#flushing-production-components-in-a-basic-warehouse-configuration).

   > [!NOTE]
   > I movimenti di inventario sono documenti importanti se utilizzi i metodi di consuntivazione **Prelievo + Avanti** o **Prelievo + indietro**. Per ulteriori informazioni vedi [Metodi di consuntivazione](production-how-to-flush-components-according-to-operation-output.md#flushing-methods).

* I campi **Cod. coll. art. per produzione**, **Cod. coll. art. da produzione** e **Codice coll. produzione aperta** nell'ubicazione o nel centro di lavoro/area di produzione definiscono i flussi predefiniti da e verso le aree di produzione.
* Gestisci il movimento degli articoli prodotti nella pagina **Movimento interno** senza una relazione con un ordine di produzione.

### I flussi da e verso l'assemblaggio in una configurazione warehouse di base  

Il flusso in uscita in una configurazione di magazzino di base prevede le seguenti impostazioni nella pagina  **Posizione scheda** per la posizione:

* Per il flusso in uscita (prelievo), nel campo  **Asm. Consumo Whse. Movimentazione**, Seleziona **Movimento inventario**.

Utilizzare i documenti  **Movimento inventario** per selezionare i componenti dell'assemblaggio nel flusso di assemblaggio. Registra l'output e il consumo dell'assemblaggio direttamente da un ordine di assemblaggio.

> [!NOTE]
> I documenti **Prelievo di magazzino** e **Stoccaggio di magazzino** non sono supportati per gli ordini di assemblaggio.

Per le ubicazioni che usano le collocazioni:

* Utilizza i documenti **Movimento magazzino** per spostare i componenti dell'assemblaggio nell'area di assemblaggio.
* I campi **Cod. coll. art. per assembl.** e **Cod. coll. art. da assembl.** nella scheda ubicazione definiscono i flussi predefiniti da e verso le aree di assemblaggio.
* Gestisci il movimento degli articoli assemblati nella pagina **Movimento interno** senza una relazione con un ordine di assemblaggio.

[!INCLUDE [prod_short](includes/prod_short.md)] supporta i flussi assemblaggio su ordine e assemblaggio per magazzino. Per ulteriori informazioni vedi [Assemblaggio su ordine e assemblaggio per magazzino](assembly-assemble-to-order-or-assemble-to-stock.md#understanding-assemble-to-order-and-assemble-to-stock). In relazione alla gestione della warehouse, l'assemblaggio per magazzino fa parte del flusso warehouse interno e l'assemblaggio su ordine è nel flusso warehouse in uscita. Ulteriori informazioni in [Gestione di articoli da assemblare su ordine con prelievi magazzino](warehouse-how-to-pick-items-with-inventory-picks.md#handling-assemble-to-order-items-with-inventory-picks).

### Flussi per la gestione dei progetti in una configurazione warehouse di base

Il flusso in uscita in una configurazione di magazzino di base prevede le seguenti impostazioni nella pagina  **Posizione scheda** per la posizione:

* Per il flusso in uscita (prelievo), nel campo  **Consumo progetto Gestione magazzino**, Seleziona **Prelievo inventario**.

Utilizza i documenti **prelievo magazzino** per il prelievo dei componenti di progetto nel flusso verso la gestione progetti.

Per un'ubicazione che utilizza le collocazioni, il campo **A progetto - Codice collocazione** nell'ubicazione definisce i flussi predefiniti per la gestione dei progetti.

## Configurazioni avanzate della warehouse  

### I flussi da e verso la produzione in una configurazione warehouse avanzata

Il flusso in uscita in una configurazione di magazzino avanzata prevede le seguenti impostazioni nella pagina  **Posizione scheda** per la posizione:

* Per il flusso in uscita (prelievo), nel campo  **Prod. Consumo Movimentazione magazzino**, Seleziona **Prelievo magazzino (facoltativo)** o **Prelievo magazzino (obbligatorio)**.

Utilizza i documenti **Prelievo warehouse** e la pagina **Prospetto prelievi** per prelevare i componenti per la produzione.

> [!NOTE]
> **I documenti di stoccaggio in magazzino non sono supportati per l'output di produzione.** 

Per le ubicazioni che usano le collocazioni:

* I documenti **Movimento warehouse** e la pagina **Prospetti movimenti** sono particolarmente utili per la consuntivazione dei componenti. Per ulteriori informazioni vedi [Consuntivazione componenti di produzione nel magazzino](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md#flushing-production-components-in-an-advanced-warehouse-configuration).
* I campi **Cod. coll. art. per produzione**, **Cod. coll. art. da produzione** e **Codice coll. produzione aperta** nell'ubicazione o nel centro di lavoro/area di produzione definiscono i flussi predefiniti da e verso le aree di produzione. 
* Gestisci il movimento degli articoli prodotti nelle pagine **Prospetto movimenti** o **Stoccaggio interno whse.** senza una relazione con un ordine di produzione.

### I flussi da e verso l'assemblaggio in una configurazione warehouse avanzata

Il flusso in uscita in una configurazione di magazzino avanzata prevede le seguenti impostazioni nella pagina  **Posizione scheda** per la posizione:

* Per il flusso in uscita (prelievo), nel campo  **Asm. Consumo Movimentazione Magazzino**, Seleziona **Prelievo Magazzino (facoltativo)** o **Prelievo Magazzino (obbligatorio)**. 

Utilizza i documenti **Prelievo warehouse** e la pagina **Prospetto prelievi** per prelevare i componenti per l'assemblaggio.

> [!NOTE]
> **Il documento di stoccaggio in magazzino non è supportato per gli ordini di assemblaggio.** 

Per le ubicazioni che usano le collocazioni:

* I campi **Cod. coll. art. per assembl.** e **Cod. coll. art. da assembl.** nell'ubicazione definiscono i flussi predefiniti da e verso le aree di assemblaggio.
* Gestisci il movimento degli articoli assemblaggio nelle pagine **Prospetto movimenti** o **Stoccaggio interno whse.** senza una relazione con un ordine di assemblaggio.

[!INCLUDE [prod_short](includes/prod_short.md)] supporta i flussi assemblaggio su ordine e assemblaggio per magazzino. Per ulteriori informazioni vedi [Assemblaggio su ordine e assemblaggio per magazzino](assembly-assemble-to-order-or-assemble-to-stock.md#understanding-assemble-to-order-and-assemble-to-stock). 

L'assemblaggio per magazzino fa parte del flusso warehouse interno e l'assemblaggio su ordine è nel flusso warehouse in uscita. Per ulteriori informazioni vedi [Gestione di articoli di assemblaggio su ordine in spedizioni warehouse](warehouse-how-ship-items.md#handling-assemble-to-order-items-in-warehouse-shipments).

### Flussi per la gestione dei progetti in una configurazione warehouse avanzata

Il flusso in uscita in una configurazione di magazzino avanzata prevede le seguenti impostazioni nella pagina  **Posizione scheda** per la posizione:

* Per il flusso in uscita (prelievo), nel campo  **Consumo progetto Gestione magazzino**, Seleziona **Prelievo magazzino (facoltativo)** o **Prelievo magazzino (obbligatorio)**.

Utilizza i documenti **Prelievo warehouse** e la pagina **Prospetto prelievi** per prelevare i componenti nel flusso per la gestione dei progetti.

Per le ubicazioni che utilizzano le collocazioni, il campo **A progetto - Codice collocazione** nell'ubicazione definisce i flussi predefiniti per l'area dei progetti.

## Vedere anche  

[Panoramica della gestione warehouse](design-details-warehouse-management.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
