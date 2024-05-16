---
title: Automatizzare i solleciti nelle riscossioni
description: 'Risparmia tempo nelle riscossioni automatizzando i processi di creazione, emissione e invio di solleciti ai clienti.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.search.keywords: 'collection, remindes'
ms.search.form: null
ms.date: 03/12/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Automatizzare i solleciti nelle riscossioni

Rendi le tue riscossioni più efficaci automatizzando i processi di creazione, emissione e invio di solleciti ai tuoi clienti. L'automazione può ridurre significativamente il tempo che dedicherai alle riscossioni, fornire una migliore panoramica del processo e darti il ​​pieno controllo su ogni passaggio.

Nella pagina **Automazione sollecito** definisci le singole azioni (passaggi). Puoi combinare i passaggi per creare, emettere e inviare solleciti oppure puoi creare un'automazione separata per ogni passaggio se è meglio per i tuoi processi di riscossione. Le automazioni si basano sui termini e sui livelli di sollecito. Per ulteriori informazioni, vai a [Impostare i termini e i livelli di sollecito](finance-setup-reminders.md). Puoi impostare filtri per i termini di sollecito per un'automazione nel suo complesso e impostare filtri per ciascuna azione nell'automazione. Puoi anche associare fatture inevase a e-mail come file PDF.

L'automazione avviene tramite un movimento della coda di processi. Quando imposti un'automazione, utilizza il campo **Cadenza** per specificare come e quando viene eseguita. Se scegli **Manuale**, l'automazione viene eseguita una volta quando utilizzi l'azione **Avvia**. Puoi anche scegliere **Settimanale**, **Mensile** o scegliere **Personalizzato** per impostare una cadenza più dettagliata. Se scegli **Personalizzato**, devi immettere una formula di data. Per ulteriori informazioni sull'inserimento di una formula per la data, vedi [Uare le formule data](ui-enter-date-ranges.md#use-date-formulas). Quando scegli un'opzione diversa da **Manuale**, l'automazione viene eseguita finché non la metti in attesa. Se vuoi essere ancora più specifico su quando viene eseguita, utilizza l'azione **Movimenti coda processi** per aprire l'azione **Movimenti coda processi** e modificare la ricorrenza, ad esempio su giornaliera o su un giorno della settimana specifico.

## Automatizzare il flusso di solleciti

Le sezioni seguenti descrivono come impostare solleciti da creare, emettere e inviare automaticamente.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Automazione solleciti**, quindi scegli il collegamento correlato.
1. Scegli **Nuovo** e quindi compila i campi nella Scheda dettaglio **Generale**.
1. Nel campo **Filtro Termini di sollecito**, scegli il termine o i termini del sollecito per cui utilizzare questa automazione.
1. Nel campo **Cadenza** scegli la frequenza con cui viene eseguita l'automazione.
1. Nella Scheda dettaglio **Azioni**, scegli **Nuovo**, quindi scegli se l'automazione crea, emette o invia solleciti. Selezionare **OK**.
1. A seconda del tipo di azione eseguita dall'automazione, compila i campi come necessario nella pagina di impostazione. Per ulteriori informazioni sulle impostazioni, vedi [Impostazioni per azioni di solleciti](#settings-for-reminder-actions).
1. Dopo aver impostato le azioni per l'automazione, puoi utilizzare le azioni **Sposta su** e **Sposta giù** per modificare l'ordine in cui vengono eseguite.

## Impostazioni per le azioni di sollecito

Le impostazioni di configurazione differiscono per le azioni Crea, Emetti e Invia sollecito. Nelle sezioni successive viene descritto come utilizzarle.

### Crea

* Imposta il livello più alto su tutte le righe del sollecito.  
* Crea solleciti per movimenti in sospeso. Ad esempio, questa impostazione è utile se è in corso una controversia con un cliente e desideri che veda il quadro generale.
* Crea solleciti per tutte le fatture non pagate e non solo per quelle scadute. Il report visualizza le fatture scadute e quelle semplicemente non pagate ma non scadute in sezioni separate.
* Imposta i filtri per rendere il sollecito più specifico.

### Emetti

Quando emetti un sollecito, crei movimenti nella contabilità clienti che contengono la data di registrazione e la data fiscale. Utilizza le impostazioni nella pagina **Impostazione Emetti solleciti** per specificare se sostituire le informazioni sul sollecito emesso con le informazioni del sollecito creato. Ad esempio, se hai creato il sollecito ieri e lo emetti oggi, la data di scadenza viene spostata di un giorno.

### Invia

> [!NOTE]
> L'automazione Invia richiede che tu abbia configurato la posta elettronica in [!INCLUDE [prod_short](includes/prod_short.md)]. Per ulteriori informazioni sull'impostazione della posta elettronica, vai a [Imposta posta elettronica](admin-how-setup-email.md).

Il contenuto della posta elettronica, come i testi degli allegati, i testi del corpo delle e-mail e la lingua, derivano dall'impostazione del termine del sollecito. Per ulteriori informazioni sulle impostazioni della posta elettronica, vai a [Impostare i termini e i livelli di sollecito](finance-setup-reminders.md).

Utilizza le impostazioni nella pagina **Impostazione Invia solleciti** controlla quanto segue:

* Impostazioni generali, come la descrizione e quante volte invierai lo stesso sollecito.
* Impostazioni su cosa includere nel sollecito.
* Impostazioni per tenere traccia dei solleciti che invii creando interazioni, se stampi o invii il sollecito tramite posta elettronica e se desideri allegare solo le fatture scadute, tutte le fatture o nessuna fattura. 

## Accedere alla cronologia di un sollecito

[!INCLUDE [prod_short](includes/prod_short.md)] tiene traccia di ogni volta che viene eseguita un'automazione. Puoi accedere alla cronologia scegliendo l'azione **Movimenti log**. Puoi anche usare l'azione **Solleciti emessi** per accedere all'elenco dei solleciti che hai emesso.

## Gestire gli errori

Nella Scheda dettaglio **Azioni**, per ogni azione puoi specificare se desideri che l'automazione si interrompa se l'azione presenta un errore. Se lo fai, l'automazione non elaborerà le azioni successive. Per attivare o disattivare questa funzionalità, utilizza le azioni **Imposta arresto in caso di errore** o **Cancella arresto in caso di errore**.

## Modificare le impostazioni delle azioni per un'automazione

Puoi modificare le impostazioni per un'automazione in qualsiasi momento. Nella Scheda dettaglio **Azioni**, scegli **Imposta**, quindi apporta le modifiche.

## Vedere anche

[Impostare i termini e i livelli di sollecito](finance-setup-reminders.md)  
[Inviare promemoria per saldi inevasi](receivables-send-reminders.md)  
