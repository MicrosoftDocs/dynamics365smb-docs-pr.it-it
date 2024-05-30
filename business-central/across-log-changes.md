---
title: Revisione delle modifiche
description: È possibile attivare un registro utente in modo da disporre di uno storico di tutte le modifiche apportate ai dati delle tabelle tracciate. È anche possibile tenere traccia delle attività con determinati tipi di registri attività.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'user log, user activity, tracking'
ms.search.form: '592, 593, 594, 595, 710, 1366, 1367, 1368, 1369'
ms.date: 05/03/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="auditing-changes"></a>Revisione delle modifiche

Una sfida comune in molte applicazioni di gestione aziendale è evitare modifiche indesiderate nei dati. Potrebbe trattarsi di un numero di telefono errato del cliente o di una registrazione errata nella contabilità generale. Questo articolo descrive le funzionalità per scoprire cosa è cambiato, chi l'ha cambiato e quando è stato cambiato.

## <a name="about-the-change-log"></a>Informazioni sul log modifiche

Il log modifiche consente di tenere traccia di tutte le modifiche dirette apportate da un utente ai dati nel database. Si specifica ogni tabella e campo che si vuole che il sistema registri, e poi si attiva il registro delle modifiche. Il log modifiche è basato sulle modifiche apportate ai dati nelle tabelle che si traccia. Nella pagina **Movimenti log modifiche**, i movimenti vengono ordinati cronologicamente e mostrano tutte le modifiche apportate ai valori dei campi nelle tabelle specificate.

La tracciabilità delle modifiche può avere un impatto sulle prestazioni e quindi comportare costi in termini di tempo, nonché aumentare le dimensioni del database e quindi comportare costi in termini di denaro. Per ridurre questi costi, tenete a mente quanto segue:

- Prestare attenzione quando si scelgono le tabelle e le operazioni.
- Non aggiungere movimenti contabili e documenti registrati. Assegnare invece la priorità ai campi di sistema, ad esempio Creato da e Data di creazione.
- Non utilizzare il tipo di tracciabilità **Tutti i campi**. Scegliere invece **Alcuni campi** e tenere traccia solo dei campi più importanti.

> [!NOTE]
> Il registro delle modifiche non tiene traccia delle modifiche per i campi che utilizzano `autoIncrement property`. Un esempio di campo che utilizza la proprietà è il campo Intero nelle tabelle Messaggi di errore e Riga report IVA.

Anche per motivi di prestazioni, il registro delle modifiche viene disattivato durante il processo di aggiornamento [!INCLUDE [prod_short](includes/prod_short.md)] alla versione successiva. Oltre ad accelerare il processo di aggiornamento, la disattivazione del registro aiuta anche a ridurre il disordine nel registro delle probabilità. Non appena l'aggiornamento è completato, il registro riprende a tenere traccia delle modifiche.

> [!Important]
> Le modifiche vengono visualizzate in **Voci log modifiche** solo dopo il riavvio della sessione dell'utente, che avviene come segue:
>
> - La sessione è scaduta ed è stata aggiornata.
> - L'utente ha selezionato un'altra società o gestione ruolo utente.
> - L'utente è uscito e si è iscritto di nuovo.

## <a name="setting-up-the-change-log"></a>Configurazione del log delle modifiche

Nella pagina **Setup log modifiche** puoi attivare o disattivare il log delle modifiche. Quando lo fai, l'attività viene registrata, quindi puoi sempre vedere chi ha apportato la modifica.

Nella pagina **Setup log modifiche**, se scegli l'azione **Tabelle**, puoi specificare per quali tabelle vuoi tracciare le modifiche e quali modifiche tracciare. [!INCLUDE[prod_short](includes/prod_short.md)] traccia anche diverse tabelle di sistema.

> [!NOTE]
> È possibile monitorare campi specifici per le modifiche, come i campi che contengono dati sensibili, impostando il monitoraggio dei campi. In caso contrario, per evitare la ridondanza, la tabella che contiene il campo non sarà disponibile per l'impostazione del log delle modifiche. Per ulteriori informazioni, vedere [Monitoraggio di campi sensibili](across-log-changes.md#monitor-sensitive-fields).

Dopo avere impostato e attivato il log modifiche e apportato una modifica ai dati, è possibile visualizzare e filtrare le modifiche nella pagina **Movimenti log modifiche**. Se desideri eliminare le voci, imposta un criterio di conservazione, in cui puoi impostare filtri in base a data e ora. Per altre informazioni sui criteri di conservazione, vai a [Definire i criteri di conservazione](admin-data-retention-policies.md).  

## <a name="analyze-data-in-the-change-log"></a>Analizzare i dati nel log delle modifiche

Puoi utilizzare la funzionalità **Analisi dei dati** per analizzare i dati nel registro delle modifiche dalla pagina [Voci log modifiche](https://businesscentral.dynamics.com/?page=595) . Non è necessario eseguire un report o aprire un'altra applicazione, come Excel. La funzionalità fornisce un modo interattivo e versatile per calcolare, riassumere ed esaminare i dati. Invece di eseguire i report utilizzando opzioni e filtri, puoi aggiungere più schede che rappresentano attività o viste diverse sui dati. Alcuni esempi sono "Chi ha modificato quali dati e quando" oppure "I dati cambiano per tabella/campo" o qualsiasi altra visualizzazione immaginabile. Per ulteriori informazioni su come utilizzare la funzionalità **Analisi dei dati**, vai a [Analizzare dati di elenco e query con la modalità di analisi](analysis-mode.md).

### <a name="change-log-ad-hoc-analysis-scenarios"></a>Scenari di analisi ad hoc per i log delle modifiche

Le sezioni seguenti forniscono esempi di scenari in cui l'analisi del log delle modifiche può aiutare a monitorare e controllare modifiche importanti.

| Ad area | Per... | Apri questa pagina in modalità di analisi | Utilizzando questi campi |
| ---- | ----- | ------------------------------- |------------------- |
| [Chi ha modificato quali dati e quando](#example-who-changed-what-data-and-when) | Vedi chi ha modificato quali dati. | [Movimenti log modifiche](https://businesscentral.dynamics.com/?page=595) | **ID utente**, **Data e ora**, **Didascalia tabella**, **Didascalia campo**, **Valore chiave primaria 2**, **Valore chiave primaria 3**, **Tipo di modifica**, **Vecchio valore** e **Nuovo valore**. |
| [I dati cambiano per tabella/campo](#example-data-changes-by-tablefield) | Visualizza le modifiche ai dati per tabella/campo e chi ha apportato la modifica. | [Movimenti log modifiche](https://businesscentral.dynamics.com/?page=595) | **Didascalia tabella**, **Didascalia campo**, **ID utente**, **Data e ora**, **Valore chiave primaria 2**, **Valore chiave primaria 3**, **Tipo di modifica**, **Vecchio valore** e **Nuovo valore**. |

### <a name="example-who-changed-what-data-and-when"></a>Esempio: chi ha modificato quali dati e quando

Per analizzare chi ha modificato quali dati e quando, segui questa procedura:

1. Apri l'elenco [Voci log modifiche](https://businesscentral.dynamics.com/?page=595) e scegli l'icona :::image type="content" source="media/analysis-mode-icon.png" alt-text="Entra in modalità analisi"::: per attivare la modalità di analisi.
1. Nel menu **Colonne**, rimuovi tutte le colonne (seleziona la casella accanto al campo **Ricerca** sulla destra).
1. Trascina il campo **ID utente** (chi l'ha fatto) nell'area **Gruppi di righe**.
1. Ora scegli i seguenti campi:
   - Per mostrare quando è successo, scegli **Data e ora**.
   - Per mostrare la tabella dove è successo, scegli **Didascalia tabella**. 
   - Per mostrare quale campo, scegli **Didascalia campo**.
   - Per mostrare il codice di campo, scegli **Valore della chiave primaria 2**. 
   - Per mostrare il nome dell'azienda, scegli **Valore della chiave primaria 3**.
   - Per mostrare se la modifica è stata un'azione di inserimento, aggiornamento o eliminazione, scegli **Tipo di modifica**.
   - Per mostrare la modifica, scegli **Vecchio valore** e **Nuovo valore**.
1. Rinomina la scheda di analisi in **Chi ha modificato quali dati e quando** o qualcosa che descriva questa analisi.

L'immagine seguente mostra il risultato di questi passaggi.

:::image type="content" source=" media/data-analysis-change-log-entries-Who-changed-What-data-When.png" alt-text="Esempio di come eseguire l'analisi dei dati nella pagina Voci log modifiche (Chi ha modificato quali dati e quando)." lightbox="media/data-analysis-change-log-entries-Who-changed-What-data-When.png":::

### <a name="example-data-changes-by-tablefield"></a>Esempio: i dati cambiano per tabella/campo

Per analizzare le modifiche ai dati per tabella/campo, segui questa procedura:

1. Apri l'elenco [Voci log modifiche](https://businesscentral.dynamics.com/?page=595) e scegli l'icona :::image type="content" source="media/analysis-mode-icon.png" alt-text="Entra in modalità analisi"::: per attivare la modalità di analisi.
1. Nel menu **Colonne**, rimuovi tutte le colonne (seleziona la casella accanto al campo **Ricerca** sulla destra).
1. Trascina i campi **Didascalia tabella** (su quale tabella) e **Didascalia campo** (su quale campo) nell'area **Gruppi di righe**.
1. Ora scegli i seguenti campi:
   - Per mostrare quando è successo, scegli **Data e ora**
   - Per mostrare chi ha apportato la modifica, scegli **ID utente**.
   - Per mostrare il codice del campo, scegli **Valore della chiave primaria 2**.
   - Per mostrare il nome dell'azienda, scegli **Valore della chiave primaria 3** (in genere il nome dell'azienda). 
   - Per mostrare se la modifica è stata un'azione di inserimento, aggiornamento o eliminazione, scegli **Tipo di modifica**.
   - Per mostrare la modifica, scegli **Vecchio valore** e **Nuovo valore**.
1. Rinomina la scheda di analisi in **I dati cambiano per tabella/campo** o qualcosa che descriva questa analisi.

L'immagine seguente mostra il risultato di questi passaggi.

:::image type="content" source=" media/data-analysis-change-log-entries-data-changes-by-table-field.png" alt-text="Esempio di come eseguire l'analisi dei dati nella pagina Voci log modifiche (modifiche dei dati per tabella/campo)." lightbox="media/data-analysis-change-log-entries-data-changes-by-table-field.png":::

## <a name="about-activity-logs"></a>Informazioni sui log attività

Da alcune pagine in [!INCLUDE [prod_short](includes/prod_short.md)], è possibile visualizzare un log attività che mostra lo stato e gli eventuali errori nei file esportati da o importati in [!INCLUDE [prod_short](includes/prod_short.md)].  

### <a name="work-with-activity-logs"></a>Utilizzare i log attività

Le informazioni vengono visualizzate nella finestra **Log attività** in base alla pagina di contesto dalla quale viene aperta. Ad esempio, è possibile aprire la pagina dalle pagine **Setup servizio di scambio documenti**, **Documento in entrata**, **Fattura vendita registrata** e **Note cr. vendita registrate**. È possibile svuotare l'elenco dei movimenti del log o semplicemente cancellare l'elenco dei movimenti più vecchi di sette giorni.  

## <a name="monitor-sensitive-fields"></a>Monitoraggio campi sensibili

Mantenere i dati sensibili protetti e privati è una preoccupazione fondamentale per la maggior parte delle aziende. Per aggiungere un livello di sicurezza, è possibile monitorare i campi importanti e ricevere un messaggio e-mail quando qualcuno modifica un valore. Ad esempio, è possibile essere avvisati se qualcuno cambia il numero IBAN della tua azienda.

> [!NOTE]
> L'invio di notifiche tramite e-mail richiede la configurazione della funzione e-mail in [!INCLUDE[prod_short](includes/prod_short.md)]. Per ulteriori informazioni, vedere [Configurare la posta elettronica](admin-how-setup-email.md).

### <a name="set-up-field-monitoring"></a>Impostazione monitoraggio campi

Usare la guida al setup assistito **Setup monitoraggio modifiche campi** per specificare i campi che si desidera monitorare in base a criteri di filtro, come la classificazione dei dati riservati per i campi. Per ulteriori informazioni, vedere [Classificazione di dati riservati](admin-classifying-data-sensitivity.md). La guida consente inoltre di specificare la persona che riceve la notifica e-mail quando si verifica una modifica e l'account e-mail che invia la notifica. Specifica sia l'utente da notificare che l'account da cui inviare la notifica. Al termine della guida, è possibile gestire le impostazioni per il monitoraggio dei campi nella pagina **Setup monitoraggio campi**.

> [!NOTE]
> Quando specifichi l'account di posta elettronica da cui inviare le notifiche, devi aggiungere i tipi di account **Microsoft 365** o **SMTP**. Le notifiche dovrebbero essere inviate da un account che non è associato a un utente reale. Pertanto non è possibile scegliere il tipo di account **Utente attuale** . Se lo fai, le notifiche non saranno inviate.

Nel tempo, l'elenco delle voci nella pagina **Voci del log dei campi monitorati** cresce. Per ridurre il numero di voci, è possibile creare una politica di conservazione che elimina le voci dopo un determinato periodo di tempo. Per ulteriori informazioni, vedere [Definire i criteri di conservazione](admin-data-retention-policies.md).

Quando si imposta il monitoraggio dei campi o si cambia qualcosa nella configurazione, vengono create voci per le modifiche. È possibile specificare se visualizzare le voci relative alla configurazione del monitoraggio mostrandole o nascondendole.

È possibile gestire le impostazioni per il monitoraggio dei campi, ad esempio se inviare una notifica e-mail o semplicemente registrare la modifica, per ogni campo nella pagina **Foglio di lavoro dei campi monitorati**. Nella pagina è anche possibile aggiungere o rimuovere i campi da monitorare.

> [!NOTE]
> Dopo aver aggiunto uno o più campi e avviato il monitoraggio, è necessario disconnettersi da [!INCLUDE[prod_short](includes/prod_short.md)] e accedere di nuovo per applicare le tue impostazioni.

### <a name="work-with-field-monitoring"></a>Utilizzare il monitoraggio campi

Le voci per tutti i valori modificati per i campi monitorati sono disponibili nella pagina **Voci del log dei campi monitorati**. Per esempio, le voci contengono le seguenti informazioni:

- Il campo in cui il valore è stato modificato.
- I valori originali e nuovi.
- Chi ha fatto il cambiamento e quando l'ha fatto.

Per esaminare ulteriormente una modifica, scegliere un valore per aprire la pagina in cui è stata apportata. Per visualizzare un elenco di tutte le voci, scegliere **Movimenti modifica campo**.

### <a name="view-field-monitoring-telemetry"></a>Visualizzare la telemetria di monitoraggio dei campi

È possibile configurare [!INCLUDE[prod_short](includes/prod_short.md)] per inviare attività di monitoraggio dei campi a una risorsa Application Insights in Microsoft Azure. Quindi, utilizzando Monitoraggio di Azure, si creano report e si configurano avvisi sui dati raccolti. Per ulteriori informazioni, vedere i seguenti articoli nella Guida per sviluppatori e professionisti IT di [!INCLUDE[prod_short](includes/prod_short.md)].

- [Monitoraggio e analisi della telemetria - Abilitazione di Application Insights](/dynamics365/business-central/dev-itpro/administration/telemetry-overview?toc=/dynamics365/business-central/toc.json#enable)
- [Analizzare la telemetria di monitoraggio dei campi](/dynamics365/business-central/dev-itpro/administration/telemetry-field-monitoring-trace?toc=/dynamics365/business-central/toc.json)

## <a name="define-retention-policies"></a>Definire i criteri di conservazione

È possibile creare criteri di conservazione per eliminare i dati non necessari nei log dopo un periodo di tempo specificato. Ad esempio, nel tempo il numero di voci in un log può aumentare. Eliminando le vecchie voci è possibile concentrarsi più facilmente sulle voci più recenti e probabilmente più rilevanti. Per altre informazioni sui criteri di conservazione, vai a [Definire i criteri di conservazione](admin-data-retention-policies.md).

## <a name="see-also"></a>Vedi anche

[Monitoraggio campi sensibili](across-log-changes.md#monitor-sensitive-fields)  
[Analizzare la telemetria di monitoraggio dei campi](/dynamics365/business-central/dev-itpro/administration/telemetry-field-monitoring-trace?toc=/dynamics365/business-central/toc.json)  
[Definire i criteri di conservazione](admin-data-retention-policies.md)  
[Modificare le impostazioni di base](ui-change-basic-settings.md)  
[Ricerca, filtro e ordinamento](ui-enter-criteria-filters.md)  
[Individuare pagine e informazioni con la funzionalità delle informazioni](ui-search.md)  
[Assegnare autorizzazioni a utenti e gruppi](ui-define-granular-permissions.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
