---
title: Definire autorizzazioni granulari
description: Questo articolo descrive come definire autorizzazioni granulari e assegnare a ogni utente i set di autorizzazioni necessari per svolgere il proprio lavoro.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'access, right, security'
ms.search.form: '1, 119, 8930, 9800, 9807, 9808, 9830, 9831, 9802, 9855, 9862'
ms.date: 02/08/2023
---

# <a name="assign-permissions-to-users-and-groups"></a>Assegnare autorizzazioni a utenti e gruppi

[!INCLUDE [2023rw1-sec-group-long](includes/2023rw1-sec-group-long.md)]

Il sistema di sicurezza [!INCLUDE[prod_short](includes/prod_short.md)] controlla a quali oggetti un utente può accedere all'interno di ogni database o ambiente, in combinazione con le licenze dell'utente. Per ciascun utente puoi specificare se possono leggere, modificare o inserire dati negli oggetti di database. Per altre informazioni, vedi [Sicurezza dei dati](/dynamics365/business-central/dev-itpro/security/data-security?tabs=object-level) nel contenuto per sviluppatori e amministratori per [!INCLUDE[prod_short](includes/prod_short.md)].

Prima di assegnare autorizzazioni a utenti e gruppi di utenti, è necessario definire chi può accedere a funzionalità specifiche creando utenti in base alla licenza come definito nella loro licenza. Per ulteriori informazioni, vedere [Creare utenti in base alle licenze](ui-how-users-permissions.md).

In [!INCLUDE[prod_short](includes/prod_short.md)] esistono due livelli di autorizzazioni per gli oggetti di database:

- Autorizzazioni complete in base alla licenza, denominate anche diritti.

  Le licenze includono set di autorizzazioni predefiniti. A partire dal primo ciclo di rilascio del 2022, gli amministratori possono personalizzare queste autorizzazioni predefinite per i tipi di licenza pertinenti. Per ulteriori informazioni, vedi [Configurare le autorizzazioni in base alle licenze](ui-how-users-permissions.md#licensespermissions).  

- Autorizzazioni dettagliate che assegni in [!INCLUDE[prod_short](includes/prod_short.md)].

Questo articolo descrive come definire, usare e applicare le autorizzazioni in [!INCLUDE [prod_short](includes/prod_short.md)] per modificare la configurazione predefinita.  

[!INCLUDE [admin-gdap-users](includes/admin-gdap-users.md)]  
Per ulteriori informazioni, vedi [Accesso dell'amministratore con delega a Business Central Online](/dynamics365/business-central/dev-itpro/administration/delegated-admin).  

[!INCLUDE [prod_short](includes/prod_short.md)] online include gruppi di utenti predefiniti che vengono assegnati automaticamente agli utenti in base alla loro licenza. Puoi modificare la configurazione predefinita modificando o aggiungendo gruppi di sicurezza, set di autorizzazioni e autorizzazioni. La tabella seguente illustra gli scenari chiave per la modifica delle autorizzazioni predefinite.  

|A  |Vedere  |
|---------|---------|
|Per semplificare la gestione delle autorizzazioni per più utenti, è possibile organizzarle in gruppi di sicurezza e quindi assegnare o modificare un set di autorizzazioni per molti utenti in una sola azione.| [Per gestire le autorizzazioni tramite gruppi di utenti](#to-manage-permissions-through-user-groups) |
|Per gestire i set di autorizzazioni per utenti specifici | [Per assegnare set di autorizzazioni agli utenti](#to-assign-permission-sets-to-users) |
|Per informazioni su come definire un set di autorizzazioni|[Per creare un set di autorizzazioni](#to-create-a-permission-set)|
|Per visualizzare o risolvere i problemi delle autorizzazioni di un utente|[Per ottenere una sintesi delle autorizzazioni di un utente](#to-get-an-overview-of-a-users-permissions)|
|Per informazioni sulla sicurezza a livello di record|[Filtri di sicurezza per limitare l'accesso di un utente a record specifici in una tabella](#security-filters-limit-a-users-access-to-specific-records-in-a-table)|

> [!NOTE]
> Un metodo più ampio per definire le funzionalità a cui un utente ha accesso consiste nell'impostare il campo **Esperienza** nella pagina **Informazioni società**. Per ulteriori informazioni, vedi [Modifica delle funzionalità visualizzate](ui-experiences.md).
>
> È inoltre possibile definire le funzionalità disponibili per gli utenti nell'interfaccia utente e il modo in cui si interagisce nelle pagine. A questo proposito si utilizzano i profili, che vengono assegnati a diversi tipi di utenti in base al ruolo e al reparto. Per ulteriori informazioni, vedere [Gestire i profili](admin-users-profiles-roles.md) e [Personalizzazione di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md).

## <a name="to-create-a-permission-set"></a>Per creare un set di autorizzazioni

> [!NOTE]
> Nel secondo ciclo di rilascio del 2022 abbiamo semplificato l'aggiunta di autorizzazioni ai set di autorizzazioni. Anziché aggiungere le autorizzazioni singolarmente, puoi aggiungere interi set di autorizzazioni. Se necessario, puoi quindi escludere singole autorizzazioni al loro interno. Per ulteriori informazioni, vedi [Per aggiungere altri set di autorizzazioni](#to-add-other-permission-sets). Per renderlo possibile, abbiamo sostituito la pagina Set di autorizzazioni con una nuova. Le differenze principali sono i nuovi riquadri **Set di autorizzazioni** e **Risultati** e la scheda dettaglio **Autorizzazioni incluse**. Per continuare a usare la pagina Autorizzazioni sostituite, nella pagina **Set di autorizzazioni**, scegli l'azione **Autorizzazioni (legacy)**.

Anche la manutenzione è più facile. Quando aggiungi un'autorizzazione di sistema, il tuo set di autorizzazioni definito dall'utente verrà aggiornato automaticamente con tutte le modifiche apportate da Microsoft a tali autorizzazioni.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Set di autorizzazioni**, quindi scegli il collegamento correlato.
2. Scegli l'azione **Nuovo**.
3. Nella nuova riga, compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Scegliere l'azione **Autorizzazioni**.
5. Sulla pagina **Set di autorizzazioni** nel campo **Tipo** includi o escludi le autorizzazioni per l'oggetto come segue:

  Per includere l'autorizzazione, scegli **Includi**, e quindi scegli il livello di accesso da fornire nei campi **Autorizzazione di lettura**, **Autorizzazione di inserimento**, **Autorizzazione di modifica**, **Autorizzazione di eliminazione**, e **Autorizzazione di esecuzione**. Nella seguente tabella vengono illustrate le opzioni.

  |Opzione|Descrizione|Valutazione|
  |------|-----------|-------|
  |**Vuoto**|L'utente non può eseguire l'azione per l'oggetto.|Più basso|  
  |**Sì**|L'utente non può eseguire l'azione per l'oggetto.|Il più alto|
  |**Indiretto**|L'utente può eseguire l'azione per l'oggetto ma solo attraverso un altro oggetto correlato a cui l'utente ha accesso completo. Per ulteriori informazioni, vedi [Esempio - Autorizzazione indiretta](#example---indirect-permission) in questo articolo e [Proprietà delle autorizzazioni](/dynamics365/business-central/dev-itpro/developer/properties/devenv-permissions-property#example---indirect-permission) nella Guida per sviluppatori e professionisti IT.|Il secondo più alto|
  
  Per escludere l'autorizzazione o uno o più livelli di accesso, scegli **Escludi**, quindi scegli il livello di accesso desiderato. Nella seguente tabella vengono illustrate le opzioni.

  |Opzione|Descrizione|
  |------|-----------|-------|
  |**Vuoto**|Utilizza il livello di accesso in base alla gerarchia delle autorizzazioni nel set.  |
  |**Escludi**|Rimuovi il livello di accesso specifico per l'oggetto.|
  |**Riduci su indiretto**|Modifica il livello di accesso su Indiretto se qualsiasi set di autorizzazioni concede l'accesso diretto all'oggetto. Ad esempio, scegli questa opzione se il set di autorizzazioni fornisce l'accesso diretto alle voci CoGe, ma non vuoi che gli utenti abbiano accesso completo alle voci.|
  
  > [!NOTE]
  > Se un'autorizzazione si trova in un set di autorizzazioni incluso e si trova anche in un set di autorizzazioni escluso, l'autorizzazione verrà esclusa.

6. Utilizza i campi **Tipo di oggetto** e **ID oggetto** per specificare l'oggetto a cui stai concedendo l'accesso.

  > [!TIP]
  > Le nuove righe mostrano i valori predefiniti. Ad esempio, il campo **Tipo di oggetto** contiene **Dati tabella**, e il campo **ID oggetto** contiene **0**. I valori predefiniti sono solo segnaposto e non vengono utilizzati. Devi scegliere un tipo di oggetto e un oggetto nel campo **ID oggetto** prima di poter creare un'altra nuova riga.

7. Facoltativo: se stai definendo le autorizzazioni per un tipo di oggetto Dati tabella, nel campo **Filtro sicurezza** è possibile filtrare i dati a cui un utente può accedere nei campi della tabella selezionata. Ad esempio, potresti voler consentire a un utente di accedere solo ai record che contengono informazioni su un particolare cliente. Per ulteriori informazioni, vedi [I filtri di sicurezza limitano l'accesso di un utente a record specifici in una tabella](#security-filters-limit-a-users-access-to-specific-records-in-a-table) e [Utilizzo dei filtri di sicurezza](/dynamics365/business-central/dev-itpro/security/security-filters).
8. Opzionale: nel riquadro **Set di autorizzazioni** aggiungi uno o più set di autorizzazioni. Per ulteriori informazioni, vedi [Per aggiungere altri set di autorizzazioni](#to-add-other-permission-sets).

> [!IMPORTANT]
> Usa cautela quando assegni **Permesso inserimento** o **Permesso modifica** alla tabella **9001 Membro gruppo utenti** o **9003 Set autorizzazioni gruppo utenti** . Qualsiasi utente assegnato al set di permessi potrebbe potenzialmente assegnarsi ad altri gruppi di utenti, che a loro volta potrebbero dare permessi non voluti.

### <a name="example---indirect-permission"></a>Esempio - Autorizzazione indiretta

Puoi assegnare un'autorizzazione indiretta per consentire a un utente di usare un oggetto, ma solo attraverso un altro oggetto. Ad esempio, un utente ha l'autorizzazione per eseguire la codeunit 80, Vendite-Registra. La codeunit Vendite-Registra esegue molti task, tra cui la modifica della tabella 37, Riga vendite. Quando l'utente registra un documento di vendita usando la codeunit Vendite-Registra, [!INCLUDE[prod_short](includes/prod_short.md)] verifica se l'utente dispone delle autorizzazioni per modificare la tabella Righe vendite. In caso di risposta negativa, la codeunit non può completare i relativi task e l'utente riceve un messaggio di errore. In caso di risposta affermativa, la codeunit viene eseguita correttamente.

Tuttavia, per l'utente non è necessario avere accesso completo alla tabella Righe vendite per eseguire la codeunit. Se l'utente possiede un'autorizzazione indiretta per la tabella Righe vendite, la codeunit Vendite-Registra viene eseguita correttamente. Quando un utente possiede un'autorizzazione indiretta, può solo modificare la tabella Riga vendite eseguendo la codeunit di Vendite-Registra o un altro oggetto per cui possiede l'autorizzazione per modificare la tabella Righe vendite. L'utente può solo modificare la tabella Righe vendite quando esegue questa operazione da aree di applicazione supportate. L'utente non può eseguire inavvertitamente o intenzionalmente la funzionalità con altri metodi.

### <a name="to-add-other-permission-sets"></a>Per aggiungere altri set di autorizzazioni

Espandi un set di autorizzazioni aggiungendovi altri set di autorizzazioni. Successivamente, puoi includere o escludere autorizzazioni specifiche o interi set di autorizzazioni in ogni set che aggiungi. Ciò include le autorizzazioni nei set di autorizzazioni di tipo Estensione e Sistema, che altrimenti non sono consentite. Le esclusioni si applicano solo al set di autorizzazioni che stai espandendo. Il set originale non viene modificato.

Sulla pagina **Set di autorizzazioni** aggiungi un set di autorizzazioni nel riquadro **Set di autorizzazioni**. Il riquadro **Risultato** elenca tutti i set di autorizzazioni aggiunti. Per esplorare le autorizzazioni incluse in un set che hai aggiunto, scegli il set nel riquadro Risultato e la scheda dettaglio **Autorizzazioni incluse** mostrerà le autorizzazioni.

Sul riquadro **Risultato** utilizza il campo **Stato inclusione** per identificare i set di autorizzazioni in cui hai escluso autorizzazioni o set di autorizzazioni. Se qualcosa è stato escluso, lo stato lo sarà **Parziale**.

Per una visualizzazione generale delle autorizzazioni nel set di autorizzazioni, scegli l'azione **Visualizza tutte le autorizzazioni**. La pagina **Autorizzazioni estese** mostra tutte le autorizzazioni che erano già state assegnate al set di autorizzazioni e le autorizzazioni nei set di autorizzazioni aggiunti.

Per escludere completamente tutte le autorizzazioni di un set di autorizzazioni, nel riquadro **Risultato** seleziona la riga, scegli **Mostra altre opzioni**, quindi scegli **Escludi**. Quando si esclude un set di autorizzazioni, viene creata una riga nel riquadro **Set di autorizzazioni** di tipo Escluso. Se hai escluso un set di autorizzazioni, ma desideri includerlo di nuovo, elimina la riga nel riquadro **Set di autorizzazioni**.

Per escludere completamente o parzialmente un'autorizzazione specifica in un set che hai aggiunto, in **Autorizzazioni**, crea una riga per l'oggetto. I campi del livello di accesso, Inserisci autorizzazione, Modifica autorizzazione e così via, conterranno tutti **Escludi**. Per consentire un certo livello di accesso, scegli l'opzione appropriata.

L'esclusione di un set di autorizzazioni esclude tutte le autorizzazioni nel set. [!INCLUDE [prod_short](includes/prod_short.md)] calcola le autorizzazioni come segue:

1. Calcola l'elenco completo delle autorizzazioni incluse
2. Calcola l'elenco completo delle autorizzazioni escluse
3. Rimuovi le autorizzazioni escluse dall'elenco delle autorizzazioni incluse (la rimozione di un'autorizzazione indiretta equivale a Riduci su indiretto)

## <a name="to-copy-a-permission-set"></a>Per copiare un set di autorizzazioni

Crea un nuovo set di autorizzazioni copiandone un altro. Il nuovo set includerà tutte le autorizzazioni e i set di autorizzazioni del set copiato. Il modo in cui le autorizzazioni e i set di autorizzazioni sono organizzati nel nuovo set di autorizzazioni varia a seconda della scelta effettuata nel campo **Operazione di copia**. Nella seguente tabella vengono illustrate le opzioni.

|Opzione  |Descrizione  |
|---------|---------|
|**Copia per riferimento**     | Il set di autorizzazioni originale e tutti i set di autorizzazioni che sono stati aggiunti sono elencati nel riquadro **Risultati**.       |
|**Copia autorizzazione semplice**  | Tutte le autorizzazioni di tutti i set di autorizzazioni sono incluse in un elenco semplice nel **riquadro delle autorizzazioni**. Le autorizzazioni non sono organizzate per set di autorizzazioni.        |
|**Clona**     | Crea una copia esatta del set di autorizzazioni originale.        |

1. Nella pagina **Set di autorizzazioni**, selezionare la riga per un set di autorizzazioni che si desidera copiare, quindi selezionare l'azione **Copia set di autorizzazioni**.
2. Nella pagina **Copia set di autorizzazioni**, specifica il nome del nuovo set di autorizzazioni.
3. Nel campo **Operazione di copia** specifica come disporre l'autorizzazione nel nuovo set di autorizzazioni.
4. Facoltativo: se stai aggiungendo un set di autorizzazioni di sistema, potresti voler essere avvisato se il nome o il contenuto del set di autorizzazioni originale cambia in una versione futura. Ciò consente di valutare se aggiornare il set di autorizzazioni definito dall'utente. Per ricevere una notifica, attiva l'interruttore **Notifica in caso di set di autorizzazioni modificato**.

> [!NOTE]
> La notifica richiede che la notifica **Set di autorizzazioni di sistema originale modificato** sia abilitata nella pagina **Notifiche personali**.

## <a name="to-create-or-modify-permissions-by-recording-your-actions"></a>Per creare o modificare le autorizzazioni registrando le azioni

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Set di autorizzazioni**, quindi scegli il collegamento correlato.

    In alternativa, nella pagina **Utenti** scegliere l'azione **Set di autorizzazioni**.
2. Nella pagina **Set di autorizzazioni** scegliere l'azione **Nuovo**.
3. In una nuova riga, compilare i campi in base alle esigenze.
4. Scegliere l'azione **Autorizzazioni**.
5. Nella pagina **Autorizzazioni**, scegliere l'azione **Registra autorizzazioni**, quindi selezionare l'azione **Avvia**.  
    La registrazione deve essere eseguita utilizzando la funzione **Apri questa pagina in una nuova finestra** (pop-out) per avere la finestra di registrazione **Autorizzazioni** affiancata o lavorando all'interno della stessa scheda.  
    Viene ora avviato un processo di registrazione che acquisisce tutte le azioni nell'interfaccia utente.
6. Passare alle diverse pagine e attività di [!INCLUDE[prod_short](includes/prod_short.md)] a cui si desidera che gli utenti con questo set di autorizzazioni possano accedere. È necessario eseguire i task per cui si desidera registrare le autorizzazioni.
7. Quando si desidera terminare la registrazione, tornare alla pagina **Autorizzazioni** e scegliere l'azione **Arresta**.
8. Scegliere il pulsante **Sì** per aggiungere le autorizzazioni registrate nel nuovo set di autorizzazioni.
9. Per ogni oggetto nella lista registrata, specifica se gli utenti possono immettere, modificare o eliminare, i record nelle tabelle registrate.

### <a name="to-export-and-import-a-permission-set"></a>Per esportare e importare un set di autorizzazioni

Per impostare rapidamente le autorizzazioni, è possibile importare set di autorizzazioni che sono state esportate da un altro tenant [!INCLUDE[prod_short](includes/prod_short.md)].

In ambienti multitenant, un set di autorizzazioni verrà importato in un tenant specifico. In altre parole, l'ambito dell'importazione è *Tenant*.

1. Nella pagina **Set di autorizzazioni** nel tenant 1, selezionare la riga o le tighe per i set di autorizzazioni, quindi selezionare l'azione **Esporta set di autorizzazioni**.

    Un file XML viene creato nella cartella di download sul computer. Per impostazione predefinita, il nome è *"Export Permission Sets.xml*

2. Nella pagina **Set di autorizzazioni** nel tenant 2, selezionare l'azione **Importa set di autorizzazioni**.
3. Nella finestra di dialogo **Importa set di autorizzazioni**, valutare se si desidera unire i set di autorizzazioni esistenti con eventuali nuovi set di autorizzazioni nel file XML.

    Se selezioni la casella di controllo **Aggiorna autorizzazioni esistenti**, i set di autorizzazioni esistenti con lo stesso nome nel file XML verranno uniti ai set di autorizzazioni importati.

    Se non selezioni la casella di controllo **Aggiorna autorizzazioni esistenti**, i set di autorizzazioni con lo stesso nome di quelli esistenti nel file XML verranno ignorati durante l'importazione. In tal caso, si riceve una notifica relativa ai set di autorizzazioni ignorati.

4. Dalla finestra di dialogo **Importa**, trovare e selezionare il file XML da importare, quindi scegliere l'azione **Apri**.

I set di autorizzazioni vengono importati.

## <a name="to-remove-obsolete-permissions-from-all-permission-sets"></a>Per rimuovere le autorizzazioni obsolete da tutti i set di autorizzazioni

Nella pagina **Set di autorizzazioni**, scegliere l'azione **Rimuovi autorizzazioni obsolete**.

## <a name="to-set-up-time-constraints-for-users"></a>Per impostare i vincoli di tempo per gli utenti

Gli amministratori possono definire periodi di tempo durante i quali gli utenti specificati possono pubblicare. Gli amministratori possono anche specificare se il sistema registra per quanto tempo gli utenti sono connessi. Gli amministratori possono anche assegnare centri di responsabilità agli utenti. Per ulteriori informazioni, vedi [Usare i centri di responsabilità](inventory-responsibility-centers.md).

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Setup utente**, quindi scegli il collegamento correlato.
2. Nella pagina **Setup utenti** scegliere l'azione **Nuovo**.
3. Nel campo **ID utente**, immettere l'ID di un utente o scegliere il campo per visualizzare tutti gli utenti correnti di Windows nel sistema.
4. Compilare i campi in base alle esigenze.

## <a name="to-manage-permissions-through-user-groups"></a>Per gestire le autorizzazioni tramite gruppi di utenti

I gruppi di utenti ti aiutano a gestire i set di autorizzazioni all'interno dell'azienda. [!INCLUDE [prod_short](includes/prod_short.md)] online include gruppi di utenti predefiniti che vengono assegnati automaticamente agli utenti in base alla loro licenza. Puoi aggiungere utenti manualmente a un gruppo di utenti e creare nuovi gruppi di utenti come copie di quelli esistenti.  

Si inizia creando un gruppo di utenti. Quindi assegnare i set di autorizzazioni al gruppo per definire a quale oggetto possono accedere gli utenti del gruppo. Quando si aggiunge l'utente al gruppo, i set di autorizzazioni definiti per il gruppo verranno applicati all'utente.

I set di autorizzazioni assegnati a un utente tramite un gruppo di utenti rimangono sincronizzati. Una modifica alle autorizzazioni del gruppo di utenti viene propagata automaticamente agli utenti. Se si rimuove un utente da un gruppo di utenti, le autorizzazioni interessate vengono automaticamente revocate.

### <a name="to-add-users-to-a-user-group"></a>Per aggiungere utenti a un gruppo di utenti

La seguente procedura spiega come creare manualmente gruppi di utenti. Per creare automaticamente gruppi di utenti, vedi [Per copiare un gruppo di utenti e tutti i suoi set di autorizzazioni](#to-copy-a-user-group-and-all-its-permission-sets).

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Gruppi di utenti**, quindi scegli il collegamento correlato.

    1. In alternativa, nella pagina **Utenti** scegliere l'azione **Gruppi di utenti**.
2. Nella pagina **Gruppo di utenti**, scegliere l'azione **Membri gruppo di utenti**.
3. Nella pagina **Gruppo di utenti**, scegliere l'azione **Aggiungi utenti**.

### <a name="to-copy-a-user-group-and-all-its-permission-sets"></a>Per copiare un gruppo di utenti e tutti i suoi set di autorizzazioni

Per definire rapidamente un nuovo gruppo di utenti, è possibile copiare tutti i set di autorizzazioni da un gruppo di utenti esistenti al nuovo gruppo di utenti.

> [!NOTE]
> I membri del gruppo di utenti non vengono copiati nel nuovo gruppo di utenti. Bisogna aggiungerli manualmente successivamente. Per ulteriori informazioni, vedi la sezione [Per aggiungere utenti a un gruppo di utenti](#to-add-users-to-a-user-group).

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Gruppi di utenti**, quindi scegli il collegamento correlato.
2. Selezionare il gruppo di utenti che si desidera copiare, quindi scegliere l'azione **Copia gruppo di utenti**.
3. Nel campo **Nuovo codice gruppo di utenti**, immettere un nome per il gruppo, quindi scegliere il pulsante **OK**.

Il nuovo gruppo di utenti viene aggiunto nella pagina **Gruppi di utenti**. Procedere con l'aggiunta di utenti. Per ulteriori informazioni, vedi la sezione [Per aggiungere utenti a un gruppo di utenti](#to-add-users-to-a-user-group).  

> [!IMPORTANT]
> Riceverai un errore di convalida se stai tentando di assegnare un gruppo di utenti all'utente che fa riferimento a un set di autorizzazioni che è stato definito in un'estensione disinstallata. È perché l'ID app dell'estensione viene convalidato ogni volta che viene indicato come riferimento. Per assegnare quel gruppo di utenti a un utente, puoi reinstallare l'estensione, rimuovere il riferimento dell'estensione disinstallata dal set delle autorizzazioni o rimuovere quel set di autorizzazioni dal gruppo di utenti.

### <a name="to-assign-permission-sets-to-user-groups"></a>Per assegnare i set di autorizzazioni a gruppi utente

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Gruppi di utenti**, quindi scegli il collegamento correlato.
2. Selezionare il gruppo di utenti a cui si intende assegnare l'autorizzazione.  

    Tutti i set di autorizzazioni già assegnati all'utente vengono visualizzati nel Dettaglio informazioni **Set di autorizzazioni**.
3. Scegliere l'azione **Set di autorizzazioni utente** per aprire la pagina **Set di autorizzazioni utente**.
4. Nella pagina **Set di autorizzazioni utente** compilare i campi secondo le necessità su una nuova riga.

### <a name="to-assign-a-permission-set-on-the-permission-set-by-user-group-page"></a>Per assegnare un set di autorizzazioni nella pagina **Set di autorizzazioni per gruppo di utenti**

La seguente procedura illustra come assegnare i set di autorizzazioni a un gruppo di utenti nella pagina **Set di autorizzazioni per gruppo di utenti**.

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Utenti**, quindi scegli il collegamento correlato.
2. Nella pagina **Utenti** selezionare l'utente pertinente quindi scegliere l'azione **Set di autorizzazioni per gruppo di utenti**.
3. Nella pagina **Set di autorizzazioni per gruppo di utenti** selezionare il campo **[nome gruppo di utenti]** in una riga per il set di autorizzazioni pertinente per assegnare il set al gruppo di utenti.
4. Seleziona la casella di controllo **Tutti i gruppi di utenti** per assegnare il set di autorizzazioni a tutti i gruppi di utenti.

È anche possibile assegnare i set di autorizzazioni direttamente a un utente.

## <a name="to-assign-permission-sets-to-users"></a>Per assegnare set di autorizzazioni agli utenti

Un set di autorizzazioni è una raccolta di autorizzazioni per oggetti di database specifici. A tutti gli utenti devono essere assegnati uno o più set di autorizzazioni prima di poter accedere a [!INCLUDE[prod_short](includes/prod_short.md)].  

Una soluzione [!INCLUDE[prod_short](includes/prod_short.md)] contiene solitamente un set di autorizzazioni predefiniti che vengono aggiunti da Microsoft o dal proprio provider di soluzioni. È inoltre possibile aggiungere nuovi set di autorizzazioni personalizzati in base alle esigenze della propria organizzazione. Per ulteriori informazioni, vedi la sezione [Per creare un set di autorizzazioni](#to-create-a-permission-set).

> [!NOTE]
> Se non si desidera limitare l'accesso di un utente più di quanto già definito dalla licenza, è possibile assegnare all'utente un set di autorizzazioni speciale chiamato SUPER. Questo set di autorizzazioni garantisce che l'utente possa accedere a tutti gli oggetti specificati nella licenza.
>
> Un utente con la licenza Essential e il set di autorizzazioni SUPER ha accesso a più funzionalità rispetto agli utenti con la licenza Team Member e il set di autorizzazioni SUPER.

È possibile assegnare i set di autorizzazioni agli utenti in due modi:

- Nella pagina **Scheda Utente** selezionando i set di autorizzazioni da assegnare all'utente.
- Nella pagina **Set di autorizzazioni per utente** selezionando gli utenti a cui è assegnato un set di autorizzazioni.

### <a name="to-assign-a-permission-set-on-a-user-card"></a>Per assegnare un set di autorizzazioni in una scheda utente

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Utenti**, quindi scegli il collegamento correlato.
2. Selezionare l'utente a cui si intende assegnare l'autorizzazione.
Tutti i set di autorizzazioni già assegnati all'utente vengono visualizzati nel Dettaglio informazioni **Set di autorizzazioni**.
3. Scegliere l'azione **Modifica** per aprire la pagina **Scheda utente**.
4. Nella Scheda dettaglio **Set di autorizzazioni utente** compilare i campi secondo le necessità su una nuova riga. Per ulteriori informazioni, vedi [Per creare o modificare un set di autorizzazioni](ui-define-granular-permissions.md#to-create-a-permission-set).

### <a name="to-assign-a-permission-set-on-the-permission-set-by-user-page"></a>Per assegnare un set di autorizzazioni nella pagina Set di autorizzazioni per utente

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Utenti**, quindi scegli il collegamento correlato.
2. Nella pagina **Utenti** scegli l'azione **Set di autorizzazioni per utente**.
3. Nella pagina **Set di autorizzazioni per utente**, seleziona la casella di controllo **[nome utente]** in una riga per il set di autorizzazioni pertinente per assegnare il set all'utente.

    Seleziona la casella di controllo **Tutti gli utenti** per assegnare il set di autorizzazioni a tutti gli utenti.

## <a name="to-get-an-overview-of-a-users-permissions"></a>Per ottenere una sintesi delle autorizzazioni di un utente:

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Utenti**, quindi scegli il collegamento correlato.
2. Aprire la scheda dell'utente pertinente.
3. Scegliere l'azione **Autorizzazioni valide**.

    La parte **Autorizzazioni** elenca tutti gli oggetti del database a cui l'utente ha accesso. Non è possibile modificare questa sezione.

    La sezione **Per set di autorizzazioni** mostra i set di autorizzazioni assegnati attraverso i quali le autorizzazioni sono concesse all'utente, l'origine e il tipo del set di autorizzazioni e il livello per i diversi tipi di accesso.

    Per ogni riga selezionata nella sezione **Autorizzazioni**, la sezione **Per set di autorizzazioni** mostra tramite quali set di autorizzazioni è stata concessa l'autorizzazione. In questa sezione, è possibile modificare il valore in ciascuno dei cinque tipi di accesso disponibili: **Autorizzazione di lettura**, **Autorizzazione di inserimento**, **Autorizzazione di modifica**, **Autorizzazione di eliminazione** e **Autorizzazione di esecuzione**.

    > [!NOTE]  
    > È possibile modificare solo i set di autorizzazioni di tipo **Definito dall'utente**.
    >
    > Le righe di diritto di origine derivano dalla licenza di sottoscrizione. I valori di autorizzazione di diritto annullano i valori in altri set di autorizzazioni se hanno una classificazione più alta. La presenza di un valore in un set di autorizzazioni senza diritti che ha una classificazione superiore rispetto al valore correlato nel diritto sarà racchiuso tra parentesi per indicare che non è valido in quanto è superato dal diritto esistente.
    >
    > Per una spiegazione della classificazione, vedi [Per creare un set di autorizzazioni](ui-define-granular-permissions.md#to-create-a-permission-set).  

4. Per modificare un set di autorizzazioni, nella parte **Per set di autorizzazioni**, nella riga per un set di autorizzazioni pertinente di tipo **Definito dall'utente**, selezionare uno dei cinque campi del tipo di accesso e selezionare un valore diverso.

5. Per modificare le singole autorizzazioni all'interno del set di autorizzazioni, selezionare il valore nel campo **Set di autorizzazioni** per aprire la pagina **Autorizzazioni**.

> [!NOTE]  
> Quando si modifica un set di autorizzazioni, le modifiche si applicano anche ad altri utenti a cui è stato assegnato il set di autorizzazioni.

### <a name="security-filters-limit-a-users-access-to-specific-records-in-a-table"></a>Filtri di sicurezza per limitare l'accesso di un utente a record specifici in una tabella

Per la protezione a livello di record in [!INCLUDE[prod_short](includes/prod_short.md)], usa i filtri di protezione per limitare l'accesso dell'utente ai dati in una tabella. I filtri di protezione sono creati sui dati della tabella. Un filtro di protezione descrive un set di record in una tabella che un utente è autorizzato a accedere. È possibile specificare, ad esempio, che un utente può leggere solo i record che contengono informazioni su un determinato cliente. Ciò significa che l'utente non può accedere ai record che contengono informazioni su altri clienti. Per ulteriori informazioni, vedere [Uso dei filtri di sicurezza](/dynamics365/business-central/dev-itpro/security/security-filters) nel contenuto amministrativo.

## <a name="viewing-permission-changes-telemetry"></a>Visualizzazione della telemetria sulle modifiche delle autorizzazioni

È possibile configurare [!INCLUDE[prod_short](includes/prod_short.md)] per inviare le modifiche applicate a un'autorizzazione a una risorsa Application Insights in Microsoft Azure. Quindi, utilizzando Monitoraggio di Azure, si creano report e si configurano avvisi sui dati raccolti. Per ulteriori informazioni, vedere i seguenti articoli nella Guida per sviluppatori e amministratori di [!INCLUDE[prod_short](includes/prod_short.md)].

- [Monitoraggio e analisi della telemetria - Abilitazione di Application Insights](/dynamics365/business-central/dev-itpro/administration/telemetry-overview#enable)
- [Analizzare la telemetria di monitoraggio dei campi](/dynamics365/business-central/dev-itpro/administration/telemetry-permission-changes-trace)

## <a name="delegated-admin-users"></a>Utenti amministratori con delega

[!INCLUDE [admin-gdap-users](includes/admin-gdap-users.md)]

## <a name="see-also"></a>Vedi anche

[Creare utenti in base alle licenze](ui-how-users-permissions.md)  
[Gestire profili](admin-users-profiles-roles.md)  
[Modifica delle funzionalità visualizzate](ui-experiences.md)  
[Personalizzazione di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md)  
[Preparazione al business](ui-get-ready-business.md)  
[Amministrazione](admin-setup-and-administration.md)  
[Aggiungere utenti a Microsoft 365 per le aziende](/microsoft-365/admin/add-users/add-users)  
[Sicurezza e protezione in Business Central](/dynamics365/business-central/dev-itpro/security/security-and-protection) nella Guida per sviluppatori e professionisti IT  
[Assegnare un ID telemetria agli utenti](/dynamics365/business-central/dev-itpro/administration/telemetry-enable-application-insights#assign-a-telemetry-id-to-users)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
