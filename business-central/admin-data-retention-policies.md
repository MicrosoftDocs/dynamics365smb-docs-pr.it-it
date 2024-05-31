---
title: Pulisci i dati con i criteri di conservazione
description: È possibile specificare la frequenza con cui si desidera eliminare determinati tipi di dati.
author: brentholtorf
ms.topic: conceptual
ms.author: bholtorf
ms.search.keywords: 'delete, data, retention, policy, policies'
ms.search.form: '3903, 3901'
ms.date: 12/15/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Definire i criteri di conservazione

Questo articolo illustra in che modo gli amministratori possono definire i criteri di conservazione per specificare la frequenza con cui desiderano che  elimini i dati obsoleti nelle tabelle che contengono voci di log e record archiviati. Ad esempio, la pulizia delle voci di log può semplificare il lavoro con i dati più rilevanti. I criteri possono eliminare i dati in base a una data di scadenza oppure puoi aggiungere filtri per includere solo determinati dati scaduti.

## Configurazioni e autorizzazioni obbligatorie

Prima di poter creare criteri di conservazione, è necessario impostare le tabelle da includere e i periodi di tempo in cui conservare i dati.

|Installazione  |Descrizione  |
|---------|---------|
|**Tabelle consentite**     |Viene fornito un elenco delle tabelle che puoi includere nei criteri di conservazione. Se desideri aggiungere tabelle da un'estensione a un criterio di conservazione, uno sviluppatore deve aggiungere le proprie tabelle all'elenco. Per ulteriori informazioni, vai a [Includere l'estensione in un criterio di conservazione](admin-data-retention-policies.md#include-your-extension-in-a-retention-policy-requires-help-from-a-developer).          |
|**Periodi di conservazione**     |Specificare i periodi di tempo per conservare i dati nelle tabelle in un criterio. I periodi determinano la frequenza con cui i dati vengono eliminati.         |

Inoltre, è necessario disporre delle autorizzazioni utente con privilegi **avanzati** o del set di autorizzazioni **Setup criteri di conservazione**. Gli utenti che dispongono del set di autorizzazioni Impostazione criteri di conservazione possono definire criteri di conservazione per le tabelle. Questo è vero, anche se non dispongono delle autorizzazioni di lettura ed eliminazione per le tabelle. Il movimento coda processi deve essere eseguito come utente con autorizzazioni per leggere ed eliminare i dati. Non concedere il set di autorizzazioni Setup criteri di conservazione agli utenti a cui non è consentito eliminare i dati.

> [!NOTE]
> Se si utilizza [!INCLUDE[prod_short](includes/prod_short.md)] in locale e si desidera provare i criteri di conservazione nel database dimostrativo di Cronus, è necessario eseguire alcune operazioni. La società di dimostrazione non contiene tabelle che è possibile utilizzare con i criteri di conservazione, quindi è necessario aggiungerle. A tale scopo, creare una nuova società vuota nel database dimostrativo. Nella nuova società, importare il pacchetto di configurazione RapidStart per il proprio paese/area geografica che corrisponde al pacchetto NAV17.0.W1.ENU.STANDARD.rapidstart standard. I dati di setup per i criteri di conservazione saranno disponibili nella nuova società.

### Creare periodi di conservazione

I periodi di conservazione possono essere lunghi o brevi come si desidera. Per creare periodi di conservazione, nella pagina **Criteri di conservazione** usare l'azione **Periodo di conservazione**. I periodi definiti sono disponibili per tutte i criteri.

> [!NOTE]
> Per motivi di conformità, è stato definito un periodo di conservazione minimo per alcune tabelle. Se si imposta un periodo di conservazione inferiore al minimo richiesto, un messaggio visualizzerà il periodo obbligatorio.

### Impostare i criteri di conservazione

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Criteri di conservazione**, quindi scegli il collegamento correlato.
2. Nel campo **ID tabella**, scegliere la tabella che si desidera includere nel criterio.
3. Nel campo **Periodo di conservazione** specificare il periodo di tempo per il quale conservare i dati nella tabella.
4. Facoltativo: è possibile applicare i criteri a dati specifici in una tabella, anziché a tutti i record, filtrando i dati per ogni riga. I criteri verranno applicati solo ai record restituiti dai filtri. Per specificare i criteri di filtro, disattiva l'interruttore **Applica a tutti i record**. Viene visualizzata la Scheda dettaglio **Criteri di conservazione dei record** in cui è possibile impostare i criteri di filtro. Per ulteriori informazioni sui filtri, vai a [Filtri](ui-enter-criteria-filters.md#filtering).

   > [!NOTE]
   > Ogni riga ha il proprio periodo di conservazione. Se si specificano periodi di conservazione diversi per gli stessi dati, verrà utilizzato il periodo più lungo. Inoltre, alcune tabelle contengono filtri che non è possibile modificare o rimuovere. Per identificare con chiarezza questi filtri, vengono visualizzati con un carattere di colore più chiaro.

#### Guida video

Questo video fornisce un esempio di come configurare un criterio di conservazione.

>[!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RW1fLeJ]

## Applicazione criteri di conservazione

È possibile utilizzare un movimento coda processi per applicare i criteri di conservazione per eliminare automaticamente i dati oppure applicare manualmente i criteri.

Per applicare automaticamente un criterio di conservazione, è sufficiente creare e abilitare un criterio. Quando si abilita un criterio, [!INCLUDE [prod_short](includes/prod_short.md)] crea un movimento coda processi che applicherà i criteri di conservazione in base al periodo di conservazione specificato. Tutti i criteri di conservazione utilizzeranno lo stesso movimento coda processi. Per impostazione predefinita, il movimento coda processi applica il criterio ogni giorno alle 02.00. È possibile modificare l'impostazione predefinita, ma in tal caso è consigliabile eseguirla al di fuori dell'orario di lavoro. Per ulteriori informazioni, vai a [Utilizzare le code processi per pianificare le attività](admin-job-queues-schedule-tasks.md). 

È possibile applicare manualmente un criterio utilizzando l'azione **Applica manualmente** nella pagina **Criteri di conservazione**. Per applicare sempre un criterio manualmente, attivare l'interruttore **Manuale**. Il movimento coda processi ignorerà il criterio quando viene eseguito.

## Visualizzazione delle voci di log dei criteri di conservazione

È possibile visualizzare l'attività relativa ai criteri di conservazione nella pagina **Log criteri di conservazione**. Ad esempio, le voci vengono create quando viene applicato un criterio o se si sono verificati errori.

## Includi l'estensione in un criterio di conservazione (richiede l'aiuto di uno sviluppatore)

Per impostazione predefinita, i criteri di conservazione coprono solo [!INCLUDE[prod_short](includes/prod_short.md)] l'elenco che forniamo. È possibile rimuovere le tabelle predefinite dall'elenco e aggiungere le tabelle di proprietà dell'utente. Cioè, non è possibile aggiungere una tabella che è stata creata personalmente. Ad esempio, non è possibile aggiungere altre tabelle da [!INCLUDE[prod_short](includes/prod_short.md)] o da un'estensione acquistata.

Per aggiungere le tue tabelle all'elenco delle tabelle consentite, uno sviluppatore deve aggiungere del codice. Ad esempio, alla codeunit dell'installatore per l'interno (una codeunit con il sottotipo  *install* ).

Quando uno sviluppatore aggiunge una tabella, può specificare filtri obbligatori e predefiniti. I filtri obbligatori non possono essere rimossi o modificati successivamente quando si aggiungono tabelle per definire un criterio di conservazione. I filtri predefiniti sono solo suggerimenti.

Di seguito sono riportati esempi di come aggiungere una tabella all'elenco di tabelle consentite con e senza filtri obbligatori o predefiniti. Per un esempio più complesso, vedere codeunit 3999 "Reten. Pol. Installa - BaseApp".

```al
 trigger OnInstallAppPerCompany()
    var
        RetenPolAllowedTables: Codeunit "Reten. Pol. Allowed Tables";
    begin
        RetenPolAllowedTables.AddAllowedTable(Database::"Retention Policy Log Entry");
    end;
```

L'esempio seguente include un filtro obbligatorio.

```al
 trigger OnInstallAppPerCompany()
    var
        ChangeLogEntry: Record "Change Log Entry";
        RetenPolAllowedTables: Codeunit "Reten. Pol. Allowed Tables";
        RetentionPeriod: Enum "Retention Period Enum";
        RecRef: RecordRef;
        TableFilters: JsonArray;
        Enabled: Boolean;
        Mandatory: Boolean;
    begin
        ChangeLogEntry.Reset();
        ChangeLogEntry.SetFilter("Field Log Entry Feature", '%1|%2', ChangeLogEntry."Field Log Entry Feature"::"Monitor Sensitive Fields", ChangeLogEntry."Field Log Entry Feature"::All);
        RecRef.GetTable(ChangeLogEntry);
        Enabled := true;
        Mandatory := true;
        RetenPolAllowedTables.AddTableFilterToJsonArray(TableFilters, RetentionPeriod::"28 Days", ChangeLogEntry.FieldNo(SystemCreatedAt), Enabled, Mandatory, RecRef);
        RetenPolAllowedTables.AddAllowedTable(Database::"Change Log Entry", ChangeLogEntry.FieldNo(SystemCreatedAt), TableFilters);
    end;
```

Dopo che uno sviluppatore ha aggiunto le tabelle all'elenco, un amministratore può includerle in un criterio di conservazione. 

## Vedere anche

[Analisi della telemetria della traccia dei criteri di conservazione](/dynamics365/business-central/dev-itpro/administration/telemetry-retention-policy-trace)  
[Revisione delle modifiche in Business Central](across-log-changes.md)  
[Filtri](ui-enter-criteria-filters.md#filtering)  
[Utilizzare le code processi per pianificare le attività](admin-job-queues-schedule-tasks.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]