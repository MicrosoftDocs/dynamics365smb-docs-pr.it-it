---
title: Usare documenti elettronici nelle vendite
description: Scopri come utilizzare la funzionalità dei documenti elettronici correlata alle vendite.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'electronic document, electronic invoice, e-document, e-invoice, sales, deliver'
ms.search.form: '42, 43, 132, 6103, 6133, 6121, 9301, 9305'
ms.date: 03/29/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# Utilizzare documenti elettronici nel processo di vendita

Puoi utilizzare documenti elettronici configurati con documenti di vendita.

Puoi utilizzare i seguenti documenti di vendita con la funzionalità dei documenti elettronici:  

- Fatture di vendita
- Ordini di vendita
- Note di credito di vendita
- Fatture assistenza
- Note credito assistenza
- Note addebito interessi
- Solleciti

## Documenti elettronici per le vendite  

Per creare e inviare una fattura elettronica a un cliente, devi creare e registrare la fattura di vendita. Per ulteriori informazioni sul processo standard, consulta [Fatturare le vendite](sales-how-invoice-sales.md).

Dopo aver registrato il documento di vendita, apri la pagina **Fattura di vendita registrata** per accedere alla pagina  **Documento elettronico** correlata.

### Visualizzare documenti elettronici   

Per visualizzare i documenti elettronici esistenti, procedi come segue.

1. Nella pagina **Fattura di vendita registrata** seleziona **Documento elettronico** \> **Apri documento elettronico**.
2. Nella pagina **Documento elettronico**, nell'intestazione, puoi visualizzare le informazioni di base sulla fattura registrata.
3. Il campo **Record** mostra il numero del documento della fattura di vendita registrata. Seleziona il collegamento per aprire il documento.
4. Nel campo **Stato del documento elettronico** puoi visualizzare lo stato in tempo reale del documento e la relativa posizione nella pipeline del processo. Se il documento è stato registrato, lo stato è **Elaborato**.

### Log e stati dei documenti elettronici 

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

## Panoramica degli stati dei documenti elettronici

Per avere una migliore panoramica di tutti i documenti elettronici nella società, puoi selezionare la gestione ruolo utente **Contabile** dove esistono gli stati dei documenti elettronici. Qui puoi trovare le attività relative ai documenti elettronici che hanno i seguenti stati:

- **Documenti elettronici in uscita:**

    - Elaborato
    - In corso
    - Errore


## Vedere anche

[Come impostare documenti elettronici in Business Central](finance-how-setup-edocuments.md)  
[Come estendere documenti elettronici in Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments)  
[Gestione contabile](finance.md)  
[Fatturazione delle vendite](sales-how-invoice-sales.md)  
[Registrare gli acquisti con le fatture e gli ordini di acquisto](purchasing-how-record-purchases.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
