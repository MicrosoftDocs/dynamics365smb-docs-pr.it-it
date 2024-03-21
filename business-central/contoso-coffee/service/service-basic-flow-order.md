---
title: Procedura dettagliata sugli ordini di assistenza per articoli in assistenza
description: Questo articolo illustra diversi processi principali relativi ad ordini di assistenza e articoli in assistenza.
author: andreipa
ms.author: andreipa
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 05/31/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# <a name="walkthrough-of-service-orders-for-service-items"></a>Procedura dettagliata sugli ordini di assistenza per articoli in assistenza

Questa procedura dettagliata illustra diversi processi principali:

- Creare un ordine di assistenza ad hoc e registrare la riparazione dell'articolo
- Fornire un articolo in prestito al cliente per il periodo della riparazione
- Registrare e fatturare l'ordine di assistenza
    
## <a name="creating-a-service-order"></a>Creazione di un ordine di assistenza

### <a name="scenario"></a>Scenario

Charles, il responsabile dell'assistenza, crea un ordine di assistenza per uno scenario di riparazione e presta un articolo al cliente per il periodo della riparazione.

### <a name="steps"></a>Passaggi

1. Crea manualmente l'ordine di assistenza per l'articolo da riparare.
   1. Scegli la ![lampadina che apre la funzione Dimmi.](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") e immetti **Ordini di assistenza**
   2. Scegli l'azione **Nuovo**.
   3. Immetti **10000** nel campo Nr. cliente
   4. Seleziona **RIPARAZIONE** nel campo **Tipo ordine assistenza**.
   5. Nelle righe, seleziona **S-100** come **Nr. articolo**.
2. Facoltativo
   1. Scegli l'azione **Risoluzione dei problemi** per verificare le possibili soluzioni.
   2. Scegli l'azione **Relazioni codici guasto/risoluzione**
   3. Seleziona *RUMORE* come **Codice indizio**
   4. Seleziona *5-2 Rumore forte durante la macinazione* come **Codice guasto** e chiudi la pagina. Il codice del guasto e quello della risoluzione vengono aggiornati nelle righe.
3. Presta un articolo sostitutivo durante il periodo della riparazione
   1. Nelle righe, seleziona **MUTUANTE1** come Nr. articolo in prestito. Conferma l'emissione dell'articolo in prestito selezionando **Sì** per prestare l'articolo sostitutivo. 
   2. Scegli l'azione Funzioni **Ottieni codici servizio std.**, seleziona il codice standard associato al gruppo di assistenza e seleziona **OK**.
   
### <a name="results"></a>Risultati

- Viene creato un ordine di assistenza per l'articolo
- Il log dei documenti di assistenza dell'ordine di assistenza mostra le attività relative all'articolo in prestito.
- L'articolo in prestito ha un movimento contabile per riflettere il prestito.
   

## <a name="register-performed-work-mark-loaner-as-returned"></a>Registra il lavoro eseguito e contrassegna l'articolo in prestito come restituito

### <a name="scenario-1"></a>Scenario

Il tecnico dell'assistenza contrassegna l'articolo in prestito come restituito e registra il lavoro eseguito.

### <a name="steps-1"></a>Passaggi

1. Individua l'attività di assistenza e registra il tempo speso 
   1. Scegli la ![lampadina che apre la funzione Dimmi.](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") , entrare in **Attività di servizio**, e poi scegliere il link relativo.
   2. Individua l'ordine di assistenza per il quale immettere il tempo speso.
   3. Scegli l'azione **Prospetto interv. articolo**.
   4. Immetti le seguenti informazioni

    |Tipo|Nr.|Quantità|
    |----|---|--------|  
    |Articolo|SER102|2|

   4. Seleziona *FINITO* nel campo **Codice stato riparazione**
    
2. Contrassegna l'articolo in prestito come restituito
   1. Scegli la ![lampadina che apre la funzione Dimmi.](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Articoli in prestito**, quindi scegli il collegamento correlato.
   2. Individua l'articolo in prestito da contrassegnare come restituito.
   3. Scegli l'azione **Ricevi** 
   4. Conferma la restituzione dell'articolo in prestito selezionando **Sì**.
      
### <a name="results-1"></a>Risultati

- Il **log dei documenti di assistenza** dell'ordine di assistenza mostra le attività relative all'articolo in prestito.
- L'articolo in prestito ha un movimento contabile per riflettere la ricezione.


### <a name="scenario-2"></a>Scenario

Charles, il responsabile dell'assistenza, registra l'ordine di assistenza finito.

1. Individua l'ordine di assistenza 
   1. Scegli la ![lampadina che apre la funzione Dimmi.](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") , entrare in **Ordini di servizio**, e poi scegliere il link relativo.
   2. Trova l'ordine di assistenza che vuoi registrare.

2. Registra la fattura nell'ordine di assistenza
   1. Scegli l'azione **Registra** per completare l'ordine di assistenza, seleziona l'azione **Spedisci e fattura**, quindi scegli il pulsante **OK**.
   2. Conferma l'apertura della fattura registrata selezionando **Sì**. 
### <a name="results-2"></a>Risultati

- Verrà creata una **Fattura assistenza registrata**.
- Vengono creati i **Movimenti contabili assistenza** associati all'articolo e alla risorsa

## <a name="see-also"></a>Vedere anche
[Procedura dettagliata sui contratti di assistenza per articoli in assistenza](service-contract-flow.md)  
[Assistenza](../../service-service.md)
