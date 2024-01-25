---
title: Impostare giustificativi digitali
description: Questo articolo descrive come impostare e utilizzare i voucher digitali imposti in Microsoft Dynamics 365 Business Central.
author: altotovi
ms.author: altotovi
ms.reviewer: null
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.search.keywords: 'digital voucher, voucher, attachment, setup'
ms.search.form: '5579, 5582, 5587'
ms.date: 11/17/2023
ms.custom: bap-template
---

# Impostare giustificativi digitali

Gli amministratori possono utilizzare la funzionalità dei voucher digitali per richiedere che i documenti siano allegati a transazioni specifiche quando vengono registrati. Pertanto, questa funzionalità consente un approccio basato sull'origine e fornisce un migliore audit trail. A questo scopo è possibile configurare diversi tipi di imposizione, a seconda dei documenti o dei tipi di registrazione.

Il termine *giustificativo digitale* si riferisce alla forma digitale o elettronica di un giustificativo tradizionale in contabilità. Un giustificativo è un documento utilizzato per supportare e autorizzare transazioni finanziarie. In contabilità, un giustificativo serve solitamente come prova di una spesa o di una ricevuta di fondi. Il giustificativo potrebbe includere dettagli come la data della transazione, una descrizione, l'importo ed eventuali firme di autorizzazione.

> [!IMPORTANT]
> In alcuni paesi e aree geografiche potrebbe non essere possibile configurare alcune opzioni perché configurazioni specifiche potrebbero essere imposte da requisiti legali. Se riscontri tali restrizioni, cerca una spiegazione dettagliata nella pagina della documentazione per il tuo Paese o area geografica.

## Abilitare giustificativi digitali

Segui questi passaggi per abilitare la funzionalità dei giustificativi digitali.

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi 3.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Impostazione giustificativi digitali**, quindi seleziona il collegamento correlato.
2. Seleziona la casella di controllo **Abilitato**.

## Impostare giustificativi digitali

Puoi utilizzare diverse impostazioni per i seguenti documenti e registrazioni.

| Tipo movimento | Descrizione |
|------------|-------------|
| Documento di vendita | Specifica le registrazioni completate dai documenti di vendita. |
| Documento di acquisto | Specifica le registrazioni completate dai documenti di acquisto. |
| Registrazione COGE | Specifica le registrazioni completate dalle registrazioni COGE per tutti i tipi di conto ad eccezione di quelli correlati al cliente e al fornitore. Se selezioni uno di questi tipi di conto, cambi il controllo del processo di registrazione. Se selezioni **Cliente** come tipo di conto, il sistema controlla l'impostazione correlata alla registrazione delle vendite. Se selezioni **Fornitore** come tipo di conto, il sistema controlla l'impostazione correlata alla registrazione degli acquisti. |
| Registraz. vendite | Specifica le registrazioni completate dalle registrazioni delle vendite e dalle registrazioni COGE dove **Cliente** è selezionato come tipo di conto. |
| Registraz. acquisti | Specifica le registrazioni completate dalle registrazioni degli acquisti e dalle registrazioni COGE dove **Fornitore** è selezionato come tipo di conto. |

Segui questi passaggi per definire il modo in cui la tua organizzazione utilizza i giustificativi digitali imposti.

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi 3.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Impostazione movimento giustificativi digitali**, quindi seleziona il collegamento correlato. In alternativa, nella pagina **Impostazione giustificativo digitale**, seleziona **Impostazione movimento**.
2. Nella colonna **Tipo movimento**, seleziona un'opzione.
3. Nella colonna **Tipo assegno**, seleziona un'opzione di imposizione. Se selezioni **Nessuno**, puoi registrare il tipo di movimento selezionato senza giustificativo digitale. Se selezioni **Allegato**, il movimento deve includere un allegato. Se selezioni **Allegato o nota**, puoi includere un allegato o una nota per il movimento. 
4. Seleziona la casella di controllo **Genera automaticamente** per generare automaticamente il giustificativo digitale. Ad esempio, se non desideri aggiungere manualmente una fattura di vendita alla transazione, seleziona questa casella di controllo. Quindi non ti resta che registrare il documento. Il sistema crea automaticamente il documento, in base al layout del report, e lo allega alla transazione.
5. Seleziona la casella di controllo **Ignora se aggiunto manualmente** se non desideri aggiungere un giustificativo digitale generato automaticamente se l'utente ha già aggiunto un allegato manuale.

### Utilizzare codici origine per l'impostazione

Per utilizzare l'imposizione per le registrazioni, ma non per tutti i tipi di transazione, connetti il codice origine specifico per identificare il tipo di movimento: registrazione COGE, registrazione delle vendite o registrazione degli acquisti.

Segui questi passaggi per impostare codici origine specifici pe giustificativi digitali.

1. Nella pagina **Impostazione movimento giustificativo digitale**, seleziona **Codici origine**.
2. Nella pagina **Codici origine movimento giustificativo**, seleziona i codici origine che desideri configurare.
3. Chiudere la pagina.

## Usare la funzionalità

Apri un documento di acquisto o di vendita e immetti le informazioni nei campi obbligatori. Prima di registrare il documento, devi seguire questi passaggi per allegare un giustificativo digitale.

1. Nel riquadro Dettaglio informazioni **File di documento in entrata**, seleziona **Allega file**.
2. Trascina un file direttamente nella pagina **Inserisci file** o accedi al file da questa pagina.

Il documento viene allegato al riquadro Dettaglio informazioni **File di documento in entrata**. Per ogni riga puoi trovare il nome e il tipo del documento.

Se alleghi accidentalmente un giustificativo sbagliato, segui questi passaggi per eliminarlo prima di registrare il documento.

1. Nel riquadro Dettaglio informazioni **File di documento in entrata**, nella riga del documento, seleziona **Documento in entrata**.
2. Nella pagina **Documento in entrata**, seleziona **Elimina**.

> [!NOTE]
> Se l'allegato di un giustificativo digitale è configurato come obbligatorio e tenti di registrare documenti o registrazioni senza allegare un giustificativo, il sistema impedisce la registrazione. Viene visualizzato il seguente messaggio di errore: "Impossibile effettuare la registrazione senza allegare il giustificativo digitale."

### Trovare giustificati allegati nelle transazioni

Puoi trovare il giustificativo allegato nel documento registrato o nella pagina **Movimenti C/G** cercando nel riquadro Dettaglio informazioni **File di documento in entrata**.

Non puoi eliminare un documento allegato una volta completata la registrazione. Tuttavia, puoi aggiungere altri allegati una volta completata la registrazione.

## Vedere anche

[Gestione contabile](finance.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
