---
title: Revisione delle modifiche
description: È possibile attivare un registro utente in modo da disporre di uno storico di tutte le modifiche apportate ai dati delle tabelle tracciate. È anche possibile tenere traccia delle attività con determinati tipi di registri attività.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: null
ms.topic: conceptual
ms.search.keywords: 'user log, user activity, tracking'
ms.search.form: '592, 593, 594, 595, 710, 1366, 1367, 1368, 1369'
ms.date: 08/03/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Revisione delle modifiche in Business Central

Una sfida comune in molte applicazioni di gestione aziendale è evitare modifiche indesiderate nei dati. Potrebbe trattarsi di un numero di telefono errato del cliente o di una registrazione errata nella contabilità generale. Questo argomento descrive le funzionalità per scoprire cosa è cambiato, chi l'ha cambiato e quando è stato cambiato.

## Informazioni sul log modifiche

Il log modifiche consente di tenere traccia di tutte le modifiche dirette apportate da un utente ai dati nel database. Si specifica ogni tabella e campo che si vuole che il sistema registri, e poi si attiva il registro delle modifiche. Il log modifiche è basato sulle modifiche apportate ai dati nelle tabelle che si traccia. Nella pagina **Movimenti log modifiche**, i movimenti vengono ordinati cronologicamente e mostrano tutte le modifiche apportate ai valori dei campi nelle tabelle specificate. 

La tracciabilità delle modifiche può avere un impatto sulle prestazioni e quindi comportare costi in termini di tempo, nonché aumentare le dimensioni del database e quindi comportare costi in termini di denaro. Per ridurre questi costi, tenete a mente quanto segue:

- Prestare attenzione quando si scelgono le tabelle e le operazioni.
- Non aggiungere movimenti contabili e documenti registrati. Assegnare invece la priorità ai campi di sistema, ad esempio Creato da e Data di creazione.
- Non utilizzare il tipo di tracciabilità Tutti i campi. Scegliere invece Alcuni campi e tenere traccia solo dei campi più importanti.

Anche per motivi di prestazioni, il registro delle modifiche viene disattivato durante il processo di aggiornamento [!INCLUDE [prod_short](includes/prod_short.md)] alla versione successiva. Oltre ad accelerare il processo di aggiornamento, questo aiuta anche a ridurre il disordine nel registro delle probabilità. Non appena l'aggiornamento è completato, il registro riprende a tenere traccia delle modifiche.

> [!Important]
> Le modifiche vengono visualizzate in **Voci log modifiche** solo dopo il riavvio della sessione dell'utente, che avviene come segue:
>
> - La sessione è scaduta ed è stata aggiornata.
> - L'utente ha selezionato un'altra società o gestione ruolo utente.
> - L'utente è uscito e si è iscritto di nuovo.

### Utilizzare il log delle modifiche

Il log modifiche viene attivato e disattivato nella pagina **Setup log modifiche**. Quando un utente attiva o disattiva il log modifiche, questa attività viene registrata, in modo da poter visualizzare sempre quale utente ha disattivato o riattivato il log modifiche.

Nella pagina **Setup log modifiche**, se scegli l'azione **Tabelle**, puoi specificare per quali tabelle vuoi tracciare le modifiche e quali modifiche tracciare. [!INCLUDE[prod_short](includes/prod_short.md)] traccia anche diverse tabelle di sistema.

> [!NOTE]
> È possibile monitorare campi specifici per le modifiche, come i campi che contengono dati sensibili, impostando il monitoraggio dei campi. In caso contrario, per evitare la ridondanza, la tabella che contiene il campo non sarà disponibile per l'impostazione del log delle modifiche. Per ulteriori informazioni, vedere [Monitoraggio di campi sensibili](across-log-changes.md#monitor-sensitive-fields).

Dopo avere impostato e attivato il log modifiche e apportato una modifica ai dati, è possibile visualizzare e filtrare le modifiche nella pagina **Movimenti log modifiche**. Se desideri eliminare le voci, imposta un criterio di conservazione, in cui puoi impostare filtri in base a data e ora. Per altre informazioni sui criteri di conservazione, vai a [Definire i criteri di conservazione](admin-data-retention-policies.md).  

## Informazioni sui log attività

Da alcune pagine in [!INCLUDE [prod_short](includes/prod_short.md)], è possibile visualizzare un log attività che mostra lo stato e gli eventuali errori nei file esportati da o importati in [!INCLUDE [prod_short](includes/prod_short.md)].  

### Utilizzare i log attività

Le informazioni vengono visualizzate nella finestra **Log attività** in base alla pagina di contesto dalla quale viene aperta. Ad esempio, è possibile aprire la pagina dalle pagine **Setup servizio di scambio documenti**, **Documento in entrata**, **Fattura vendita registrata** e **Note cr. vendita registrate**. È possibile svuotare l'elenco dei movimenti del log o semplicemente cancellare l'elenco dei movimenti più vecchi di sette giorni.  

## Monitoraggio campi sensibili

Mantenere i dati sensibili protetti e privati è una preoccupazione fondamentale per la maggior parte delle aziende. Per aggiungere un livello di sicurezza, è possibile monitorare i campi importanti ed essere avvisati tramite e-mail quando qualcuno modifica un valore. Ad esempio, è possibile essere avvisati se qualcuno cambia il numero IBAN della tua azienda.

> [!NOTE]
> L'invio di notifiche tramite e-mail richiede la configurazione della funzione e-mail in [!INCLUDE[prod_short](includes/prod_short.md)]. Per ulteriori informazioni, vedere [Configurare la posta elettronica](admin-how-setup-email.md).

### Impostazione monitoraggio campi

Usare la guida al setup assistito **Setup monitoraggio modifiche campi** per specificare i campi che si desidera monitorare in base a criteri di filtro, come la classificazione dei dati riservati per i campi. Per ulteriori informazioni, vedere [Classificazione di dati riservati](admin-classifying-data-sensitivity.md). La guida consente inoltre di specificare la persona che riceverà la notifica e-mail quando si verifica una modifica e l'account e-mail che invierà l'e-mail di notifica. Specifica sia l'utente da notificare che l'account da cui inviare la notifica. Al termine della guida, è possibile gestire le impostazioni per il monitoraggio dei campi nella pagina **Setup monitoraggio campi**. 

> [!NOTE]
> Quando specifichi l'account di posta elettronica da cui inviare le notifiche, devi aggiungere i tipi di account **Microsoft 365** o **SMTP**. Le notifiche dovrebbero essere inviate da un account che non è associato a un utente reale. Pertanto non è possibile scegliere il tipo di account **Utente attuale** . Se lo fai, le notifiche non saranno inviate. 

Nel tempo, l'elenco delle voci nella pagina **Voci del log dei campi monitorati** cresce. Per ridurre il numero di voci, è possibile creare una politica di conservazione che elimina le voci dopo un determinato periodo di tempo. Per ulteriori informazioni, vedere [Definire i criteri di conservazione](admin-data-retention-policies.md).

Quando si imposta il monitoraggio dei campi o si cambia qualcosa nella configurazione, vengono create voci per le modifiche. È possibile specificare se visualizzare le voci relative alla configurazione del monitoraggio mostrandole o nascondendole. 

È possibile gestire le impostazioni per il monitoraggio dei campi, ad esempio se inviare una notifica e-mail o semplicemente registrare la modifica, per ogni campo nella pagina **Foglio di lavoro dei campi monitorati**. Nella pagina è anche possibile aggiungere o rimuovere i campi da monitorare.

> [!NOTE]
> Dopo aver aggiunto uno o più campi e avviato il monitoraggio, è necessario disconnettersi da [!INCLUDE[prod_short](includes/prod_short.md)] e accedere di nuovo per applicare le tue impostazioni.

### Utilizzare il monitoraggio campi

Le voci per tutti i valori modificati per i campi monitorati sono disponibili nella pagina **Voci del log dei campi monitorati**. Per esempio, le voci contengono le seguenti informazioni:

- Il campo per il quale il valore è stato cambiato.
- I valori originali e nuovi.
- Chi ha fatto il cambiamento e quando l'ha fatto.

Per esaminare ulteriormente una modifica, scegliere un valore per aprire la pagina in cui è stata apportata. Per visualizzare un elenco di tutte le voci, scegliere **Movimenti modifica campo**.

### Visualizzare la telemetria di monitoraggio dei campi 

È possibile configurare [!INCLUDE[prod_short](includes/prod_short.md)] per inviare attività di monitoraggio dei campi a una risorsa Application Insights in Microsoft Azure. Quindi, utilizzando Monitoraggio di Azure, si creano report e si configurano avvisi sui dati raccolti. Per ulteriori informazioni, vedere i seguenti articoli nella Guida per sviluppatori e professionisti IT di [!INCLUDE[prod_short](includes/prod_short.md)].

- [Monitoraggio e analisi della telemetria - Abilitazione di Application Insights](/dynamics365/business-central/dev-itpro/administration/telemetry-overview#enable)
- [Analizzare la telemetria di monitoraggio dei campi](/dynamics365/business-central/dev-itpro/administration/telemetry-field-monitoring-trace)

## Definire i criteri di conservazione

È possibile creare criteri di conservazione per eliminare i dati non necessari nei log dopo un periodo di tempo specificato. Ad esempio, nel tempo il numero di voci in un log può aumentare. Eliminando le vecchie voci è possibile concentrarsi più facilmente sulle voci più recenti e probabilmente più rilevanti. Per altre informazioni sui criteri di conservazione, vai a [Definire i criteri di conservazione](admin-data-retention-policies.md).

## Vedi anche

[Modificare le impostazioni di base](ui-change-basic-settings.md)  
[Ricerca, filtro e ordinamento](ui-enter-criteria-filters.md)  
[Individuare pagine e informazioni con la funzionalità delle informazioni](ui-search.md)  
[Assegnare autorizzazioni a utenti e gruppi](ui-define-granular-permissions.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Definire i criteri di conservazione](admin-data-retention-policies.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
