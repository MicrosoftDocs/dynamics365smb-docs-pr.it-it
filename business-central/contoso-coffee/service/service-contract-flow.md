---
title: Procedura dettagliata sui contratti di assistenza per articoli in assistenza
description: Questo articolo illustra vari scenari relativi ad articoli in assistenza e contratti di assistenza.
author: andreipanko
ms.author: andreipa
ms.topic: how-to
ms.date: 11/08/2023
ms.custom: bap-template
---

# <a name="walkthrough-of-service-contracts-for-service-items"></a>Procedura dettagliata sui contratti di assistenza per articoli in assistenza

Questa procedura dettagliata illustra diversi processi principali:

- Creazione di articoli in assistenza tramite vendite
- Creazione e fatturazione per un contratto di assistenza
- Creazione di un ordine di assistenza per un contratto di assistenza
- Assegnare una risorsa in base a competenza e zona
- Completare l'inserimento di ore per l'ordine di assistenza
- Registrare e fatturare l'ordine di assistenza del contratto

## <a name="creation-of-service-items"></a>Creazione di articoli in assistenza

### <a name="scenario"></a>Scenario

Susan, la responsabile degli ordini, registra un ordine di vendita vendendo un articolo configurato per generare un articolo in assistenza.  

### <a name="steps"></a>Passaggi

1. Verifica che per **Articolo** sia selezionato **Gruppo articoli in assistenza**.
   
    1. Scegli la ![lampadina che apre la funzione Dimmi.](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Articoli** e scegli il collegamento correlato.  
    2. Seleziona l'articolo *S-100* e aprilo.
    3. Controlla il valore nel campo **Gruppo articoli in assistenza**.
       
2. Registra l'**Ordine vendita** per creare l'articolo in assistenza per il cliente.  

    1. Scegli la ![lampadina che apre la funzione Dimmi.](../../media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ordini vendita**, quindi seleziona il collegamento correlato.  
    2. Seleziona l'ordine per il cliente 10000. Il numero dell'ordine esterno è *SVC-1*.
    3. Scegli l'azione **Registra** per spedire l'articolo al cliente.

### <a name="results"></a>Risultati

- Viene creato un articolo in assistenza per il cliente 10000

## <a name="invoicing-a-service-contract"></a>Fatturazione di un contratto di assistenza

### <a name="scenario-1"></a>Scenario

Charles, il responsabile dell'assistenza, crea quindi un contratto di assistenza per fatturare le visite di manutenzione periodiche.

3. Crea il **Contratto di assistenza** per il nuovo articolo in assistenza
    1. Scegli la ![lampadina che apre la funzione Dimmi.](../../media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Contratti assistenza**, quindi scegli il collegamento correlato.
    2. Scegli l'azione **Nuovo**.  
    3. Nella finestra di dialogo di conferma, scegli **Sì** per creare un contratto utilizzando il modello. 
    4. Seleziona *Contratto non prepagato - Mensile*.
    5. Nella Scheda dettaglio Assistenza, in **Tipo ordine assistenza**, immetti **MANUTEN**.
    6. Nelle righe immetti le seguenti informazioni:

    |Nr. articolo in assistenza|Valore riga|  
    |----------------|----------|  
    |SV000001|6000|

    7. Scegli l'azione **Firma contratto** e conferma la firma.
    8. Scegli **Sì** per confermare la creazione di una fattura di assistenza. Viene visualizzato un messaggio di conferma con il numero di fattura di assistenza.

3. Registra la fattura di assistenza
   1. Scegli la ![lampadina che apre la funzione Dimmi.](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Fatture assistenza**, quindi scegli il collegamento correlato.
   2. Trova la fattura di assistenza e scegli l'azione **Registra**.

### <a name="results-1"></a>Risultati

- Viene creato un contratto di assistenza firmato, con movimenti contabili
- Viene creata una fattura assistenza registrata

## <a name="create-a-service-order-for-a-service-contract-and-assign-resources"></a>Creare un ordine di assistenza per un contratto di assistenza e assegnare le risorse

### <a name="scenario-2"></a>Scenario

Charles, il responsabile dell'assistenza, crea gli ordini di assistenza per ordini di manutenzione periodici nell'ambito del contratto di assistenza, quindi esaminerà la pagina Quadro attività per assegnarli.

### <a name="steps-1"></a>Passaggi

1. Esegui gli ordini di assistenza che adempiono agli obblighi dei contratti di assistenza attivi.
   1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Crea ordini assistenza a contratto**, quindi seleziona il collegamento correlato.
   2. Immetti le date di inizio e fine del mese nei campi Data di inizio e Data di fine nella Scheda dettaglio Opzioni
   3. Scegli **OK** per confermare la creazione di ordini di assistenza. Viene visualizzato un messaggio di conferma con il numero di ordini di assistenza creati.

2. Esamina gli ordini in attesa di assegnazione nella pagina Quadro attività
   1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Quadro attività**, quindi scegli il collegamento correlato.
   2. Quadro attività mostra tutti gli ordini di assistenza aperti, insieme a **N. di assegnazioni** per mostrare se gli ordini di assistenza vengono assegnati a una risorsa.
   3. Scegli l'azione **Mostra documenti** per aprire un ordine di assistenza.  Il riquadro Dettaglio informazioni Righe articoli in assistenza mostra quali risorse dispongono delle competenze necessarie per l'articolo.

3. Assegna una risorsa all'ordine di assistenza
   1. In Ordine assistenza, scegli l'azione **Assegnazioni risorse**
   2. Immetti le seguenti informazioni per l'assegnazione della risorsa

    |Nr. articolo in assistenza|Nr. risorsa|Data allocazione|Ore assegnate|
    |----------------|------------|---------------|---------------|  
    |SV000001|RISORSA1|t|1|

    3. Lo stato dell'assegnazione diventa Attivo.
    4. Aggiornando la pagina Quadro attività mostra che il valore di **N. di assegnazioni** è passato da 0 a 1 per l'ordine di assistenza.

### <a name="results-2"></a>Risultati

- Vengono creati ordini di assistenza per i contratti di assistenza
- Gli ordini di assistenza vengono assegnati a una risorsa per completare il lavoro

## <a name="complete-the-time-entry-for-the-service-order-and-post-the-service-order"></a>Completare l'inserimento di ore per l'ordine di assistenza e registrare l'ordine di assistenza

### <a name="scenario-3"></a>Scenario

Il tecnico dell'assistenza registra il tempo speso direttamente nell'ordine di assistenza, quindi contrassegnerà l'ordine come completato.

> [!NOTE]
> L'inserimento delle ore per gli ordini di assistenza può essere eseguito tramite i fogli presenze. Per ulteriori informazioni, vedi [collegamento al foglio presenza se questa nota ha senso].

### <a name="steps-2"></a>Passaggi

1. Trova l'ordine di assistenza e immetti le ore nella riga dell'assistenza
   1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") , entrare in **Ordini di servizio**, e poi scegliere il link relativo.
   2. Individua l'ordine di assistenza per il quale immettere il tempo speso.
   3. Scegli l'azione **Riga assistenza**.
   4. Immetti le seguenti informazioni

    |Tipo|Nr.|Quantità|Qtà da consumare|
    |----|---|--------|--------|   
    |Risorsa|RISORSA1|2|2|

2. Registra il consumo nell'ordine di assistenza
   1. Scegli l'azione **Registra** per completare l'ordine di assistenza, seleziona l'azione **Spedisci e consuma**, quindi scegli il pulsante **OK**.

### <a name="results-3"></a>Risultati

- Vengono creati movimenti contabili di assistenza associati all'articolo in assistenza, al contratto di assistenza e alla risorsa

## <a name="see-also"></a>Vedere anche

[Introduzione ai dati demo Contoso Coffee](../../contoso-coffee/contoso-coffee-intro.md)  
[Informazioni sugli ordini di produzione](../../production-about-production-orders.md)
