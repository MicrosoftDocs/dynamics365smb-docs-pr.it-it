---
title: Gestire la sincronizzazione dei dati master
description: Scopri come gestire la sincronizzazione dei dati master.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 01/25/2023
ms.custom: bap-template
ms.search.form: '7230, 7233, 5338, 7236, 672, 7234'
---
# <a name="manage-master-data-synchronization"></a>Gestire la sincronizzazione dei dati master

Dopo aver impostato la sincronizzazione dei dati master e la esegui per la prima volta, i record nelle tabelle selezionate vengono accoppiati e per ciascuna tabella viene creata un movimento coda processi ricorrente. I movimenti coda processi sincronizzano automaticamente i dati nelle società filiali quando qualcuno apporta una modifica nella società di origine. Altrimenti, non devi fare nulla.

> [!NOTE]
> Per impostazione predefinita, i movimenti coda processi vengono pianificati ogni minuto e non è possibile modificare la pianificazione.

Tuttavia, a volte le cose vanno male e potrebbero esserci situazioni che devi gestire o indagare. Ad esempio, se le persone modificano lo stesso record sia nella società di origine che in una filiale, la sincronizzazione avrà esito negativo in modo da poter specificare la modifica corretta. Oppure, la società di origine potrebbe installare un'estensione che modifica lo schema di una delle tabelle che stai sincronizzando aggiungendo uno o due campi. Se vuoi sincronizzare i nuovi campi nelle filiali, dovrai installare le stesse estensioni e aggiornare gli schemi delle tabelle nel loro setup.

Questo articolo descrive gli strumenti che puoi utilizzare per mantenere la sincronizzazione senza problemi.

## <a name="investigate-the-status-of-synchronization"></a>Investigare lo stato della sincronizzazione

Ci sono due azioni sulla pagina **Tabelle di sincronizzazione** che possono aiutarti a monitorare la tua sincronizzazione:

* **Processi di sincronizzazione integrazione**
* **Movimenti coda processi**

Nella seguente tabella vengono illustrate le azioni.

|Pagina  |Descrizione  |
|---------|---------|
|**Processi di sincronizzazione integrazione**     | Apri la pagina **Processi di sincronizzazione dell'integrazione** per indagare su cosa è successo ogni volta che è stata eseguita un movimento coda processi. Per approfondire i dettagli sui nuovi record che sono stati aggiunti o esplorare il motivo per cui un record non è stato sincronizzato, scegli i numeri nelle colonne **Inserito** o **Non riuscito**. Puoi anche utilizzare questa pagina per ripulire i record meno recenti di cui potresti non aver bisogno. Per ulteriori informazioni sulla pulizia, vai a [Pulire i vecchi movimenti](#clean-up-old-entries).        |
|**Movimenti coda processi**     | Accedi ai dettagli sul movimento coda processi che sincronizza i dati per una tabella selezionata. Ad esempio, utilizza questa pagina per gestire lo stato del movimento coda dei processi. Per ulteriori informazioni sui movimenti coda processi, vai a [Utilizzare le code processi per pianificare le attività](admin-job-queues-schedule-tasks.md).     |

> [!NOTE]
> Se trovi un errore nella pagina **Processi di sincronizzazione integrazione** che non puoi risolvere da solo, se contatti il tuo partner o Microsoft per il supporto, è utile fornire il messaggio di errore e informazioni sullo stack di chiamate.

## <a name="synchronize-modified-records"></a>Sincronizzare i record modificati

Se si modifica un'impostazione per una tabella o un campo in una filiale, è necessario aggiornare la sincronizzazione. Ad esempio, se decidi di selezionare la casella di controllo **Sovrascrivi modifica locale** su un campo per consentire ai dati della società di origine di sovrascrivere le modifiche locali. Per aggiornare la sincronizzazione, utilizza l'azione **Sincronizza record modificati** nella pagina **Tabelle di sincronizzazione**.

## <a name="update-table-schemas"></a>Aggiornare gli schemi delle tabelle

Se la società di origine modifica una tabella, ad esempio aggiungendo un campo che vuoi sincronizzare, le filiali devono aggiornare le mappature dei campi. Nella pagina **Campi di sincronizzazione** utilizza l'azione **Aggiorna campi**. 

## <a name="enable-or-disable-couplings-between-records"></a>Abilitare o disabilitare gli accoppiamenti tra i record

Per avviare o interrompere l'accoppiamento di record specifici in una tabella, nella pagina **Campi di sincronizzazione** scegli i campi, quindi utilizza l'azione **Abilita** o **Disabilita**. 

> [!TIP]
> Un modo rapido per abilitare o disabilitare più campi contemporaneamente è selezionarli nell'elenco, quindi utilizzare le azioni **Abilita** o **Disabilita**.

## <a name="adding-extensions"></a>Aggiunta di estensioni

Se la società di origine installa una nuova estensione, anche la filiale deve installarla se vuoi sincronizzare i dati. La filiale può utilizzare l'azione **Aggiorna campi** nella pagina **Campi di sincronizzazione** per aggiungere le tabelle dall'estensione all'elenco.

> [!NOTE]
> Alcune tabelle ottengono i dati da tabelle correlate. Se aggiungi un'estensione che non include le tabelle correlate, i campi di tali tabelle non saranno disponibili. Verifica di aver aggiunto tutte le tabelle correlate.

## <a name="clean-up-old-entries"></a>Pulire i vecchi movimenti

Nel corso del tempo, il numero di movimenti nel registro di sincronizzazione aumenterà, quindi potresti voler fare un po' di pulizia per rimuovere i movimenti non necessari. Per semplificare la pulizia dei vecchi movimenti, la pagina **Processi di sincronizzazione integrazione** offre le seguenti azioni:

* **Elimina movimenti risalenti a più di 7 giorni precedenti**
* **Elimina tutti i movimenti**

<!--
## <a name="recreate-a-deleted-job-queue-entry"></a>Recreate a deleted job queue entry

If the recurring job queue entry is deleted for a table, you can quickly recreate it. On the **Synchronization Tables** page, choose the **Use Default Synchronization Setup** action.
-->

## <a name="see-also"></a>Vedere anche

[Prepararsi a sincronizzare i dati master](admin-set-up-data-sync.md)
