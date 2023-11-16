---
title: Utilizzare documenti elettronici in vendite e acquisti
description: Scopri come utilizzare la funzionalità dei documenti elettronici correlata a fatture di vendita e di acquisto.
author: altotovi
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, electronic invoice, e-document, e-invoice, sales, purchase'
ms.search.form: '42, 43, 51, 6103, 6133, 6121, 9301, 9305, 9308'
ms.date: 10/03/2023
ms.author: altotovi
---

# <a name="use-e-documents-in-sales-and-purchases"></a>Utilizzare documenti elettronici in vendite e acquisti

Puoi utilizzare documenti elettronici configurati con documenti di vendita e di acquisto.

Attualmente puoi utilizzare i seguenti documenti per i documenti elettronici:

- Fatture di vendita
- Ordini di vendita
- Note di credito di vendita
- Fatture di acquisto
- Ordini acquisto
- Note di credito di acquisto
- Registrazioni COGE

Attualmente, un ordine di acquisto può essere utilizzato solo quando crei il documento dal documento elettronico del tuo fornitore. Tuttavia, non puoi aggiornare il documento esistente con le righe ricevute dal tuo fornitore.

## <a name="e-documents-in-sales"></a>Documenti elettronici per le vendite

Per creare e inviare una fattura elettronica a un cliente, devi creare e registrare la fattura di vendita. Per ulteriori informazioni sul processo standard, consulta [Fatturare le vendite](sales-how-invoice-sales.md).

Dopo aver registrato il documento di vendita, apri la pagina **Fattura di vendita registrata** per accedere alla pagina  **Documento elettronico** correlata.

### <a name="view-e-documents"></a>Visualizzare documenti elettronici

Per visualizzare i documenti elettronici esistenti, procedi come segue.

1. Nella pagina **Fattura di vendita registrata** seleziona **Documento elettronico** \> **Apri documento elettronico**.
2. Nella pagina **Documento elettronico**, nell'intestazione, puoi visualizzare le informazioni di base sulla fattura registrata.
3. Il campo **Record** mostra il numero del documento della fattura di vendita registrata. Seleziona il collegamento per aprire il documento.
4. Nel campo **Stato del documento elettronico** puoi visualizzare lo stato in tempo reale del documento e la relativa posizione nella pipeline del processo. Se il documento è stato registrato, lo stato è **Elaborato**.

### <a name="e-document-statuses-and-logs"></a>Log e stati dei documenti elettronici

Per dettagli sul livello di stato del servizio del documento elettronico, consulta la Scheda dettaglio **Stato del servizio documenti elettronici**. Nelle righe il sistema mostra uno o più servizi utilizzati dal documento. Nello scenario più comune, ogni documento utilizza un solo servizio. Tuttavia, un documento può utilizzare più servizi.

- Controlla il campo **Codice servizio documenti elettronici** per determinare quale servizio è stato utilizzato.
- Controlla il campo **Stato del documento elettronico** per determinare lo stato del servizio corrente per questo documento.
- Se desideri maggiori dettagli seleziona il campo **Log** del servizio nella pagina **Log documenti elettronici**. Viene visualizzata una panoramica cronologica dei diversi stati del documento.
- Controlla i campi **Nr. movimento** e **Data/Ora di creazione** e altre informazioni nella pagina **Log documenti elettronici**. Nel campo **Stato del documento elettronico**, il primo stato è **Esportato**, che indica che il file del documento elettronico è stato creato. Lo stato successivo è **Inviato**, che indica che il documento è stato inviato al provider di servizi, se configurato.

Per ulteriori informazioni dettagliate, seleziona il movimento con lo stato **Esportato**, quindi esegui una delle seguenti azioni:

- **Apri log di mapping** – Ottieni una panoramica di tutti i campi esportati dalle tabelle di origine nel campo **Valore originale**. Se hai utilizzato regole di trasformazione nel processo di esportazione, puoi anche ottenere il valore finale nel campo **Nuovo valore**.
- **Esporta file** – Esporta il file XML per la revisione manuale.

Per visualizzare la comunicazione tra te e il servizio a cui stai inviando il documento, utilizza il campo **Log di comunicazione**. Apri la pagina **Log comunicazioni dei documenti elettronici** per visualizzare i dettagli sulla richiesta e i motivi del messaggio con quel servizio.

Se c'è un problema con il provider del servizio e il documento non può essere inviato, cerca i seguenti indicatori nella pagina **Documento elettronico**:

- Il campo **Stato del documento elettronico** nell'intestazione mostra lo stato **Errore**.
- Il campo **Stato del documento elettronico** nella Scheda dettagli **Stato del servizio documenti elettronici** mostra lo stato **Errore di invio**.
- La Scheda dettaglio **Errori e avvisi** contiene uno o più messaggi che forniscono la causa del problema.

Una volta risolto il problema, esegui manualmente le azioni **Invia documento**. Se hai bisogno di azioni diverse, come ad esempio **Documento ricreato**, **Annulla documento**, o **Ottieni approvazione**, puoi eseguirle.

## <a name="e-documents-in-purchases"></a>Documenti elettronici per gli acquisti

La ricezione delle fatture elettroniche di acquisto in Dynamics 365 Business Central può essere effettuata come processo batch o manualmente.

### <a name="run-the-batch-job"></a>Eseguire il processo batch

> [!NOTE]
> Questo processo batch è usato per la raccolta automatizzata delle fatture in entrata. Può funzionare solo in un paese o in un'area in cui esiste la funzionalità.

Ogni volta che viene eseguita una coda di processi, se il servizio esterno ha fatture in entrata inviate dal fornitore, il sistema raccoglie e importa tali fatture. Per completare il processo, segui i passaggi seguenti.

1. Al termine dell'esecuzione del processo batch, le fatture appena importate vengono elencate nella pagina **Documenti elettronici**, insieme alle informazioni dettagliate di base.
2. Per visualizzare maggiori dettagli, aprire un documento elettronico specifico.
3. Se non sono presenti errori o problemi nel documento elettronico e nel relativo mapping, il campo **Record** mostra il numero di documento della fattura di acquisto creata automaticamente dal sistema. Seleziona il collegamento per aprire il documento. Questo documento creato dal sistema non è il documento registrato.
4. Per accedere direttamente al documento di acquisto, seleziona il campo **Record**. Dopo aver aperto la pagina **Fattura di acquisto**, controlla il documento. Quindi, se tutto è corretto, registra il documento.
5. Quando registri il documento di acquisto, il campo **Record** nel **Documento elettronico** viene aggiornato da **Fattura** a **Fattura di acquisto** e il numero del documento di acquisto registrato è disponibile. Puoi selezionare il numero per aprire la fattura di acquisto registrata.

I dettagli sui log sono gli stessi del processo di vendita dei documenti elettronici.

Poiché gli errori nel processo di vendita sono per lo più correlati alla disponibilità del servizio, il documento in entrata può contenere molteplici ragioni. Il motivo più comune di un errore è che il sistema non riesce a riconoscere le righe del documento elettronico ricevuto dal fornitore. Pertanto, non puoi immettere righe nella fattura di acquisto.

Vi sono due errori comuni:

- Se vuoi utilizzare questa riga specifica della fattura fornitore registrata direttamente nel conto di contabilità generale (C/G), devi aver configurato correttamente il valore **Mapping testo**. Per ignorare questo errore se desideri utilizzare conti C/G, seleziona **Mappa testo a conto** per creare un mapping specifico del valore **Mapping testo** con il valore **N. conto dare** che vuoi utilizzare.
- Se vuoi tenere traccia dell'inventario e utilizzare le righe della fattura fornitore per compilare gli articoli nelle righe del documento, devi aver configurato correttamente il valore **Nr. riferimento articolo** . Per ignorare questo errore, mappa l'articolo esterno ai tuoi numeri di articolo utilizzando la lista dei riferimenti agli articoli. Per maggiori informazioni, vedi [Usare i riferimenti agli articoli](inventory-how-use-item-cross-refs.md).

Dopo aver corretto gli errori e gli avvisi, puoi specificare manualmente quando il sistema deve creare una fattura di acquisto in base alla tua impostazione selezionando **Crea documento**.

### <a name="manually-import-invoices"></a>Importare manualmente le fatture

Per importare manualmente documenti elettronici esterni, procedi come segue.

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immetti **Servizio documenti elettronici**, quindi seleziona il collegamento correlato.
2. Nella pagina **Servizio documenti elettronici** seleziona il servizio attivo. 
3. Seleziona **Ricevi** e carica il file del documento elettronico che hai ricevuto dal fornitore.
4. Se viene visualizzato un messaggio di errore, apri il documento elettronico per risolvere i problemi.
5. Una volta risolti i problemi, nel gruppo **Importa manualmente**, seleziona **Crea documento**.
6. Dopo aver creato il documento in Business Central, puoi visualizzarlo esattamente come se si utilizzasse un processo batch.

## <a name="overview-of-e-document-statuses"></a>Panoramica degli stati dei documenti elettronici

Per avere una migliore panoramica di tutti i documenti elettronici nella società, puoi selezionare la gestione ruolo utente **Contabile** dove esistono gli stati dei documenti elettronici. Qui puoi trovare le attività relative ai documenti elettronici che hanno i seguenti stati:

- **Documenti elettronici in uscita:**

    - Elaborato
    - In corso
    - Errore

- **Documenti elettronici in entrata:**

    - Elaborato
    - In corso
    - Errore

## <a name="see-also"></a>Vedere anche

[Come impostare documenti elettronici in Business Central](finance-how-setup-edocuments.md)  
[Come estendere documenti elettronici in Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments)  
[Gestione contabile](finance.md)  
[Fatturazione delle vendite](sales-how-invoice-sales.md)  
[Registrare gli acquisti con le fatture e gli ordini di acquisto](purchasing-how-record-purchases.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
