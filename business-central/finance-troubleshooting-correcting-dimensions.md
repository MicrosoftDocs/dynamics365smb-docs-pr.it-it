---
title: Risoluzione dei problemi e correzione delle dimensioni
description: Scopri come risolvere i tipici errori di dimensione e come correggere le dimensioni dopo che sono state utilizzate nelle transazioni registrate.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'dimension, correction, correct, business intelligence'
ms.search.form: '116, 540, 2588'
ms.date: 04/26/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Risoluzione dei problemi e correzione delle dimensioni

Le visualizzazioni analisi e i report finanziari spesso si basano sui dati delle dimensioni. Nonostante le misure di sicurezza disponibili, a volte accade un errore che può portare a imprecisioni. Questo articolo descrive alcuni degli errori tipici e descrive come correggere le assegnazioni di dimensioni sulle transazioni registrate in modo che i report finanziari siano accurati.

## Risoluzione degli errori relativi alle dimensioni

Quando registri documenti o righe di registrazione che contengono dimensioni, potrebbero verificarsi diversi errori. Tuttavia, in genere sono correlati a un'impostazione o un'assegnazione di dimensione errata.

> [!NOTE]
> Nell'elenco di potenziali messaggi di errore seguente, i codici *%X* sono segnaposti per le variabili di dati che il messaggio effettivo conterrà nell'interfaccia utente a seconda del contesto. Ad esempio, *%1 %2 bloccata.* potrebbe essere visualizzato nell'interfaccia utente come “Codice dimensione AREA bloccato".  

|Problema|Messaggio di errore|Soluzione possibile|
|-----|-------------|-----------------|
|Dimensione bloccata|%1 %2 è bloccato.|-Trovare documenti non registrati che contengono il set di dimensioni con la dimensione bloccata e sbloccarla.<br />- Rimuovere la riga del set di dimensioni per la dimensione bloccata.|
|Dimensione eliminata|Impossibile trovare %1 %2.|- Ripristinare la dimensione mancante.<br />-Trovare documenti non registrati che contengono il set di dimensioni con la dimensione mancante e aggiungerla.<br />- Rimuovere la riga del set di dimensioni per la dimensione mancante.|
|Valore di dimensione bloccato|%1 %2 - %3 bloccato.|-Trovare documenti non registrati che contengono il set di dimensioni con il valore di dimensione bloccato e sbloccarlo.<br />- Rimuovere la riga del set di dimensioni per il valore di dimensione bloccato.|
|Valore di dimensione eliminato|    %1 per %2 mancante.|- Ripristinare il valore di dimensione mancante.<br />-Trovare documenti non registrati che contengono il set di dimensioni con il valore di dimensione mancante e aggiungerlo.<br />- Rimuovere la riga del set di dimensioni per il valore di dimensione mancante.|
|Valore di dimensione non consentito|Il tipo di valore di dimensione per %1 %2 - %3 non deve essere %4.|- Impostare il campo **Tipo valori dimensioni** nella pagina **Valori dimensioni** su **Standard** o **Inizio-Totale**.<br />- Rimuovere la riga del set di dimensioni per il valore di dimensione bloccato.|
|Combinazione di dimensioni bloccata|Le dimensioni %1 e %2 non possono essere utilizzate contemporaneamente.|-Trovare documenti non registrati che contengono il set di dimensioni con la combinazione di dimensioni bloccata e sbloccarla.<br />-Modificare una delle righe del set di autorizzazioni in conflitto per la combinazione di dimensioni.|
|Combinazione di valori di dimensioni bloccata|Le combinazioni di dimensioni %1 - %2 e %3 - %4 non possono essere usare contemporaneamente.|-Trovare documenti non registrati che contengono il set di dimensioni con la combinazione di valori di dimensioni bloccata e sbloccarla.<br />-Modificare una delle righe del set di autorizzazioni in conflitto per la combinazione di valori di dimensioni.|
|Codice del valore di dimensione vuoto per la dimensione di default in cui il campo **Registrazione valore** contiene **Codice obbligatorio**|- Selezionare un %1 per %2 %3.<br />- Selezionare un %1 per i %2 %3 per %4 %5.|- Modificare il campo **Registrazione valore** nella pagina **Dimensione di default**.<br />-Immettere un valore di dimensione non vuoto per la dimensione in conflitto nel set di dimensioni.|
|Codice del valore di dimensione errato per la dimensione di default in cui il campo **Registrazione valore** contiene **Stesso Cod.**|- Selezionare %1 %2 per i %3 %4.<br />- Selezionare %1 %2 per i %3 %4 per %5 %6.|- Modificare il campo **Registrazione valore** nella pagina **Dimensione di default**.<br />- Immettere il valore di dimensione richiesto per la dimensione in conflitto nel set di dimensioni.|
|Codice del valore di dimensione non vuoto per la dimensione di default vuota in cui il campo **Registrazione valore** contiene **Stesso Cod.**|-%1 %2 deve essere vuoto.<br />-%1 %2 deve essere vuoto per %3 %4.|- Modificare il campo **Registrazione valore** nella pagina **Dimensione di default**.<br />- Immettere un codice del valore di dimensione vuoto per la dimensione in conflitto nel set di dimensioni.|
|Valore di dimensione non previsto per la dimensione di default in cui il campo **Registrazione valore** contiene **Nessun Cod.**|-%1 %2 non deve essere nominato.<br />-%1 %2 non deve essere nominato per %3 %4.|- Modificare il campo **Registrazione valore** nella pagina **Dimensione di default**.<br />- Rimuovere la riga in conflitto dal set di dimensioni.|
|Una correzione dimensionale non viene completata correttamente.||-Scegli **Ripristina** per riportare la correzione allo stato di bozza. Ciò ripristina le modifiche e puoi eseguire nuovamente la correzione.|

## Modifica delle assegnazioni delle dimensioni dopo la registrazione

Se scopri una dimensione errata nei movimenti di contabilità generale (C/G) registrati, puoi correggere i valori delle dimensioni e aggiornare le visualizzazioni analisi. La correzione contribuisce a mantenere accurati i report e le analisi finanziarie.

> [!IMPORTANT]
> Le funzioni per la correzione delle dimensioni hanno il solo scopo di contribuire a rendere accurato il reporting finanziario. Le correzioni delle dimensioni si applicano solo alle voci C/G. Non modificano le dimensioni assegnate alle voci in altri libri mastri per la stessa transazione. Ci sarà una mancata corrispondenza tra le dimensioni assegnate nella contabilità generale e nei movimenti inventario secondari.

### Configurazione delle correzioni delle dimensioni

Ci sono due cose da considerare quando si impostano le correzioni delle dimensioni:

* Ci sono dimensioni che non vuoi che siano modificate da altri utenti? Nella pagina **Impostazioni correzione quota**, specifica le dimensioni che desideri bloccare per le modifiche.
* Chi può modificare le dimensioni? Per consentire alle persone di apportare modifiche, assegna l'autorizzazione **CORREZIONE DIM D365** agli utenti. Le autorizzazioni consentono loro di creare correzioni delle dimensioni, eseguirle e annullarle se necessario. Possono anche specificare le dimensioni bloccate. Per ulteriori informazioni, vedere [Assegnare autorizzazioni a utenti e gruppi](ui-define-granular-permissions.md). 

### Correzione di una dimensione

È possibile selezionare manualmente uno o più movimenti di contabilità generale oppure utilizzare i filtri per selezionare gruppi di movimenti. Se necessario, puoi anche aggiungere o eliminare dimensioni. 

1. Per avviare una correzione dimensionale, utilizzare una delle seguenti pagine:

    * Nella pagina **Registro/CG**, selezionando un registro, quindi scegliendo l'azione **Dimensioni corrette**. Questa azione avvia una correzione per i movimenti nel registro selezionato.
    * Nella pagina **Movimenti C/G**, scegliendo l'azione **Correzione dimensionale**. 

2. Nel campo **Descrizione** immettere le informazioni relative alla modifica. Altre persone potrebbero utilizzare queste informazioni in seguito per capire cosa è stato fatto.
3. Nella Scheda dettaglio **Movimenti contabili selezionati**, seleziona le voci pertinenti.

    > [!IMPORTANT]
    > Quando modifichi una selezione, i valori nella Scheda dettaglio **Modifiche alla correzione delle dimensioni** vengono ripristinati. Pertanto, selezionare sempre le voci prima di specificare le modifiche al valore della dimensione.

   Nella seguente tabella vengono illustrate le opzioni.

   |Opzione  |Descrizione  |
   |---------|---------|
   |Aggiungi movimenti correlati     |Aggiungi voci C/G che si trovano nello stesso registro C/G.|   
   |Aggiungi per filtro     |Utilizza i criteri dei filtri quando aggiungi voci C/G.|
   |Selezione manuale     |Seleziona voci C/G specifiche.         |
   |Aggiungi per dimensioni     |Filtra le voci C/G in base alle dimensioni.         |
   |Rimuovi movimenti     |Deseleziona voci C/G.         |
   |Gestisci criteri di selezione     |Tieni traccia del processo di selezione e, se necessario, annulla le selezioni.         |

4. Nella Scheda dettaglio **Modifiche alla correzione delle dimensioni**, scegli la dimensione che desideri modificare nel campo **Codice dimensione** e il nuovo valore nel campo **Nuovo codice valore dimensione**.
5. Per convalidare la correzione, scegli **Convalida le modifiche alle dimensioni**. Per ulteriori informazioni, vedi [Convalida delle correzioni delle dimensioni](finance-troubleshooting-correcting-dimensions.md#validating-dimension-corrections).
6. Scegli **Esegui**.

### Convalida delle correzioni delle dimensioni

Prima di eseguire una correzione, è una buona idea convalidarla. La convalida controlla le restrizioni sulla registrazione del valore per i conti C/G, le restrizioni per le dimensioni e se i valori delle dimensioni sono bloccati. Durante la convalida, lo stato della correzione è impostato su **Convalida in corso**. Dopo aver convalidato una correzione, il risultato viene visualizzato nel campo **Stato di convalida**. Se sono stati rilevati errori, è possibile utilizzare l'azione **Visualizza errori** per indagare su di loro. Dopo aver corretto un errore, è necessario utilizzare l'azione **Riapri** per eseguire la correzione o una nuova convalida.

Puoi eseguire una correzione immediatamente o programmarne l'esecuzione in un secondo momento. Se stai eseguendo correzioni su un set di dati di grandi dimensioni, ti consigliamo di pianificarne l'esecuzione al di fuori dell'orario di lavoro. Per ulteriori informazioni, vedi [Correzioni delle dimensioni su set di dati di grandi dimensioni](finance-troubleshooting-correcting-dimensions.md#dimension-corrections-on-large-data-sets).

### Annullamento di una correzione

Dopo aver corretto una dimensione, se non ti piace quello che vedi puoi usare l'azione **Annulla** per ripristinare il valore precedente. Tuttavia, puoi annullare solo la correzione più recente. Prima di annullare una correzione, puoi convalidare le modifiche risultanti dall'azione di annullamento. Ad esempio, la convalida è utile se le restrizioni sulle dimensioni sono cambiate dopo la correzione.

Se l'azione Annulla non è disponibile, ad esempio perché ci sono molte correzioni, è possibile utilizzare l'azione **Copia in bozza** per avviare una nuova correzione per le stesse voci.

### Correzioni delle dimensioni in set di dati di grandi dimensioni

Prestare attenzione quando si correggono set di voci di grandi dimensioni, ad esempio set che includono più di 10.000 voci. Se puoi, ti consigliamo di utilizzare i filtri per eseguire le correzioni su set di dati di dimensioni più piccole. È anche una buona idea eseguire le correzioni al di fuori del normale orario lavorativo. 

### Utilizzare le visualizzazioni analisi con correzioni delle dimensioni

Se **Aggiorna in registrazione** è abilitata per una visualizzazione analisi, [!INCLUDE[prod_short](includes/prod_short.md)] può aggiornare la visualizzazione quando vengono registrati documenti e giornali. Puoi inoltre aggiornare le viste con questa impostazione abilitata con i risultati delle correzioni delle dimensioni. A tale scopo, attivare il toggle **Aggiorna visualizzazione analisi**. L'aggiornamento delle visualizzazioni delle analisi può influire sulle prestazioni, soprattutto per set di dati di grandi dimensioni, quindi si consiglia di aggiornare le visualizzazioni di analisi solo per set di dati di piccole dimensioni.  

### Visualizzazione delle correzioni delle dimensioni storiche

Se un movimento di contabilità generale è stato corretto, è possibile esaminare la modifica utilizzando l'azione **Cronologia delle correzioni dimensionali**.

### Gestione di correzioni incomplete

Se una correzione non viene completata, viene visualizzato un avviso nella scheda della correzione. In tal caso, puoi utilizzare l'azione **Ripristina** per riportare la correzione allo stato di bozza e annullare le modifiche. È quindi possibile eseguire nuovamente la correzione.

> [!NOTE]
> La reimpostazione di una correzione incompleta non influirà sugli aggiornamenti alle visualizzazioni dell'analisi perché questi si verificano alla fine del processo di correzione.

### Utilizzare la contabilità industriale con movimenti C/G corretti

Dopo aver corretto le dimensioni, i dati per la contabilità dei costi non sono sincronizzati. La contabilità industriale utilizza le dimensioni per aggregare gli importi per centri di costo e oggetti di costo e per eseguire le allocazioni dei costi. La modifica delle dimensioni per i movimenti C/G comporta probabilmente una nuova esecuzione dei modelli di contabilità industriale. A seconda dei dati aggiornati e di come sono impostate le funzionalità di contabilità industriale, potrebbe essere necessario:

* Eliminare solo alcuni registri dei costi ed eseguire nuovamente le allocazioni.
* Eliminare tutto ed eseguire nuovamente tutti i modelli.

Devi identificare manualmente dove le correzioni delle dimensioni hanno un impatto sulla contabilità dei costi e dove sono necessari aggiornamenti. [!INCLUDE[prod_short](includes/prod_short.md)] non fornisce attualmente un modo automatizzato per farlo.

## Vedere anche

[Usare le dimensioni](finance-dimensions.md)  
[Analizzare i dati per dimensioni](bi-how-analyze-data-dimension.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
