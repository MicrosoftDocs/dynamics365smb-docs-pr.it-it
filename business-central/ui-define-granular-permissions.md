---
title: Definire autorizzazioni granulari | Microsoft Docs
description: Descrive come concedere agli utenti l'accesso agli oggetti assegnando loro set di autorizzazioni.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c2b663208a1bed8522ea532efdb2dee0d519b646
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3912523"
---
# <a name="assign-permissions-to-users-and-groups"></a>Assegnare autorizzazioni a utenti e gruppi

Il sistema di sicurezza di [!INCLUDE[d365fin](includes/d365fin_md.md)] sicurezza consente di controllare gli oggetti a cui un utente può accedere all'interno di ciascun database o ambiente. Per ciascun utente è possibile specificare se si desidera consentire di leggere, modificare o inserire dati negli oggetti di database selezionati. Per informazioni dettagliate, vedere [Sicurezza dati ](/dynamics365/business-central/dev-itpro/security/data-security?tabs=object-level) in Guida per sviluppatori e professionisti IT per [!INCLUDE[d365fin](includes/d365fin_md.md)].

Prima di assegnare autorizzazioni a utenti e gruppi di utenti, è necessario definire chi può accedere a funzionalità specifiche creando utenti in base alla licenza come definito nell'interfaccia di amministrazione di Microsoft 365. Per ulteriori informazioni, vedere [Creare utenti in base alle licenze](ui-how-users-permissions.md).

In [!INCLUDE[d365fin](includes/d365fin_md.md)] esistono due livelli di autorizzazioni per gli oggetti di database:

- Autorizzazioni complete in base alla licenza, denominate anche diritti.
- Autorizzazioni più dettagliate assegnate da [!INCLUDE[d365fin](includes/d365fin_md.md)].

Per semplificare la gestione delle autorizzazioni per più utenti, è possibile organizzarle in gruppi di utenti e quindi assegnare o modificare un set di autorizzazioni per molti utenti in una sola azione. Per ulteriori informazioni, vedere [Per gestire le autorizzazioni tramite gruppo di utenti](ui-define-granular-permissions.md#to-manage-permissions-through-user-groups).

> [!NOTE]
> Un ulteriore metodo per definire le funzionalità a cui un utente ha accesso consiste nell'impostare il campo **Esperienza** nella pagina **Informazioni società**. Per ulteriori informazioni, vedere [Modifica delle funzionalità visualizzate](ui-experiences.md).
>
> È anche possibile definire ciò che gli utenti vedono nell'interfaccia utente e come interagiscono con le funzionalità consentite attraverso le pagine. A questo proposito si utilizzano i profili, che vengono assegnati a diversi tipi di utenti in base al ruolo e al reparto. Per ulteriori informazioni, vedere [Gestire i profili](admin-users-profiles-roles.md) e [Personalizzazione di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-customizing-overview.md).

## <a name="to-assign-permission-sets-to-users"></a>Per assegnare set di autorizzazioni agli utenti

Un set di autorizzazioni è una raccolta di autorizzazioni per oggetti di database specifici. A tutti gli utenti devono essere assegnati uno o più set di autorizzazioni prima di poter accedere a [!INCLUDE[d365fin](includes/d365fin_md.md)].

Una soluzione [!INCLUDE[d365fin](includes/d365fin_md.md)] contiene solitamente una serie di set di autorizzazioni predefiniti che vengono aggiunti da Microsoft o dal proprio provider di soluzioni. È inoltre possibile aggiungere nuovi set di autorizzazioni personalizzati in base alle esigenze della propria organizzazione. Per ulteriori informazioni, vedere [Per creare o modificare un set di autorizzazioni](ui-define-granular-permissions.md#to-create-or-modify-a-permission-set).

> [!NOTE]
> Se non si desidera limitare l'accesso di un utente più di quanto già definito dalla licenza, è possibile assegnare all'utente un set di autorizzazioni speciale chiamato SUPER. Questo set di autorizzazioni garantisce che l'utente possa accedere a tutti gli oggetti specificati nella licenza.
>
> Un utente con la licenza Essential e il set di autorizzazioni SUPER ha accesso a più funzionalità rispetto agli utenti con la licenza Team Member e il set di autorizzazioni SUPER.

È possibile assegnare i set di autorizzazioni agli utenti in due modi:

- Nella pagina **Scheda Utente** selezionando i set di autorizzazioni da assegnare all'utente.
- Nella pagina **Set di autorizzazioni per utente** selezionando gli utenti a cui è assegnato un set di autorizzazioni.

### <a name="to-assign-a-permission-set-on-a-user-card"></a>Per assegnare un set di autorizzazioni in una scheda utente

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Utenti** e quindi scegliere il collegamento correlato.
2. Selezionare l'utente a cui si intende assegnare l'autorizzazione.
Tutti i set di autorizzazioni già assegnati all'utente vengono visualizzati nel Dettaglio informazioni **Set di autorizzazioni**.
3. Scegliere l'azione **Modifica** per aprire la pagina **Scheda utente**.
4. Nella Scheda dettaglio **Set di autorizzazioni utente** compilare i campi secondo le necessità su una nuova riga. Per ulteriori informazioni, vedere [Per creare o modificare un set di autorizzazioni](ui-define-granular-permissions.md#to-create-or-modify-a-permission-set).

### <a name="to-assign-a-permission-set-on-the-permission-set-by-user-page"></a>Per assegnare un set di autorizzazioni nella pagina Set di autorizzazioni per utente

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Utenti** e quindi scegliere il collegamento correlato.
2. Nella pagina **Utenti**, selezionare l'utente pertinente quindi scegliere l'azione **Set di autorizzazioni per utente**.
3. Nella pagina **Set di autorizzazioni per utente**, selezionare la casella di controllo **[nome utente]** in una riga per il set di autorizzazioni pertinente per assegnare il set all'utente.
4. Selezionare la casella di controllo **Tutti gli utenti** per assegnare il set di autorizzazioni a tutti gli utenti.

## <a name="to-get-an-overview-of-a-users-permissions"></a>Per ottenere una sintesi delle autorizzazioni di un utente:

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Utenti** e quindi scegliere il collegamento correlato.
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
    > Per una spiegazione della classificazione, vedere [Per creare o modificare le autorizzazioni manualmente](ui-define-granular-permissions.md#to-create-or-modify-permissions-manually).  

4. Per modificare un set di autorizzazioni, nella parte **Per set di autorizzazioni**, nella riga per un set di autorizzazioni pertinente di tipo **Definito dall'utente**, selezionare uno dei cinque campi del tipo di accesso e selezionare un valore diverso.

5. Per modificare le singole autorizzazioni all'interno del set di autorizzazioni, selezionare il valore nel campo **Set di autorizzazioni** per aprire la pagina **Autorizzazioni**. Seguire i passaggi descritti in [Per creare o modificare autorizzazioni](ui-define-granular-permissions.md#to-create-or-modify-permissions-manually).  

> [!NOTE]  
> Quando si modifica un set di autorizzazioni, le modifiche si applicano anche ad altri utenti a cui è stato assegnato il set di autorizzazioni.

## <a name="to-create-or-modify-a-permission-set"></a>Per creare o modificare un set di autorizzazioni

I set di autorizzazioni funzionano come contenitori di autorizzazioni, in modo da poter gestire facilmente più autorizzazioni in un record.

> [!NOTE]  
> Una soluzione [!INCLUDE[d365fin](includes/d365fin_md.md)] contiene solitamente una serie di set di autorizzazioni predefiniti che vengono aggiunti da Microsoft o dal fornitore software. Tali set di autorizzazioni sono di tipo **Sistema** o **Estensione**. Non è possibile creare o modificare questi tipi di set di autorizzazioni o le autorizzazioni al loro interno. Tuttavia, è possibile copiarli per definire i propri set di autorizzazioni e autorizzazioni personalizzati.
>
> I set di autorizzazioni creati dagli utenti, come nuovi o come copie, sono di tipo **Definito dall'utente** e possono essere modificati.

### <a name="to-create-new-permission-set-from-scratch"></a>Per creare un nuovo set di autorizzazioni da zero

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Set di autorizzazioni** e quindi scegliere il collegamento correlato.
2. Scegliere l'azione **Nuovo** per creare un nuovo set di autorizzazioni.
3. Nella nuova riga, compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Dopo avere creato un set di autorizzazioni, è necessario aggiungere le autorizzazioni effettive. Per ulteriori informazioni, vedere [Per creare o modificare le autorizzazioni manualmente](ui-define-granular-permissions.md#to-create-or-modify-permissions-manually).

### <a name="to-copy-a-permission-set"></a>Per copiare un set di autorizzazioni

È anche possibile utilizzare una funzione di copia per trasferire rapidamente tutte le autorizzazioni di un altro set di autorizzazioni a un nuovo set di autorizzazioni.

> [!NOTE]  
> Se viene modificato un set di autorizzazioni di sistema che era stato copiato, si riceve una notifica (a seconda della selezione), in modo che sia possibile verificare se le modifiche sono rilevanti per copiare o scrivere nel set di autorizzazioni definito dall'utente.

1. Nella pagina **Set di autorizzazioni**, selezionare la riga per un set di autorizzazioni che si desidera copiare, quindi selezionare l'azione **Copia set di autorizzazioni**.
2. Nella pagina **Copia set di autorizzazioni**, specificare il nome del nuovo set di autorizzazioni e quindi scegliere il pulsante **OK**.
3. Selezionare la casella di controllo **Notifica in caso di set di autorizzazioni modificato** se si desidera mantenere un collegamento tra il set di autorizzazioni originale e quello copiato. Il collegamento viene quindi utilizzato per notificare all'utente se il nome o il contenuto del set di autorizzazioni originale cambia in una versione futura a cui la soluzione viene aggiornata successivamente..

Il nuovo set di autorizzazioni, contenente tutte le autorizzazioni del set di autorizzazioni copiate, viene aggiunto come nuova riga nella pagina **Set di autorizzazioni**. È ora possibile modificare le autorizzazioni nel nuovo set di autorizzazioni. Si noti che le linee sono ordinate alfabeticamente all'interno di ciascun tipo.

### <a name="to-export-and-import-a-permission-set"></a>Per esportare e importare un set di autorizzazioni

Per impostare rapidamente le autorizzazioni, è possibile importare set di autorizzazioni che sono state esportate da un altro tenant [!INCLUDE[d365fin](includes/d365fin_md.md)].

In ambienti multitenant, un set di autorizzazioni verrà importato in un tenant specifico, ossia l'ambito dell'importazione è "Tenant".

1. Nella pagina **Set di autorizzazioni** nel tenant 1, selezionare la riga o le tighe per i set di autorizzazioni, quindi selezionare l'azione **Esporta set di autorizzazioni**.

    Un file XML viene creato nella cartella di download sul computer. Per impostazione predefinita, si chiama "Export Permission Sets.xml"

2. Nella pagina **Set di autorizzazioni** nel tenant 2, selezionare l'azione **Importa set di autorizzazioni**.
3. Nella finestra di dialogo **Importa set di autorizzazioni**, valutare se si desidera unire i set di autorizzazioni esistenti con eventuali nuovi set di autorizzazioni nel file XML.

    Se si seleziona la casella di controllo **Aggiorna autorizzazioni esistenti**, i set di autorizzazioni esistenti con lo stesso nome di quelli esistenti nel file XML verranno uniti ai set di autorizzazioni importati.

    Se non si seleziona la casella di controllo **Aggiorna autorizzazioni esistenti**, i set di autorizzazioni esistenti con lo stesso nome di quelli esistenti nel file XML verranno ignorati durante l'importazione. In tal caso, si riceve una notifica relativa ai set di autorizzazioni ignorati.

4. Dalla finestra di dialogo **Importa**, trovare e selezionare il file XML da importare, quindi scegliere l'azione **Apri**.

I set di autorizzazioni vengono importati.

## <a name="to-create-or-modify-permissions-manually"></a>Per creare o modificare le autorizzazioni manualmente

In questa procedura verrà illustrato come aggiungere o modificare autorizzazioni manualmente. Le autorizzazioni possono anche essere create automaticamente a partire dalle proprie azioni nell'interfaccia utente. Per ulteriori informazioni, vedere [Per creare o modificare le autorizzazioni registrando le azioni](ui-define-granular-permissions.md#to-create-or-modify-permissions-by-recording-your-actions).

> [!NOTE]
> Quando si modifica un'autorizzazione e quindi il relativo set di autorizzazioni, le modifiche si applicano anche ad altri utenti a cui è stato assegnato il set di autorizzazioni.

1. Nella pagina **Set di autorizzazioni**, selezionare la riga per un set di autorizzazioni che si desidera copiare, quindi selezionare l'azione **Autorizzazioni**.
2. Nella pagina **Autorizzazioni**, creare una nuova riga o modificare i campi in una linea esistente.

In ognuno dei campi dei cinque tipi di accesso (**Autorizzazione di lettura**, **Autorizzazione di inserimento**, **Autorizzazione di modifica**, **Autorizzazione di eliminazione** e **Autorizzazione di esecuzione**) è possibile selezionare una delle tre opzioni seguenti:

|Opzione|Description|Classificazione|
|------|-----------|-------|
|**Sì**|L'utente può eseguire l'azione per l'oggetto in questione.|Il più alto|
|**Indiretto**|L'utente può eseguire l'azione per l'oggetto in questione ma solo attraverso un altro oggetto correlato a cui l'utente ha accesso completo. Per ulteriori informazioni sulle autorizzazioni indirette, vedere [Proprietà delle autorizzazioni](/dynamics365/business-central/dev-itpro/developer/properties/devenv-permissions-property) nella Guida per sviluppatori e professionisti IT|Il secondo più alto|
|**Vuoto**|L'utente non può eseguire l'azione per l'oggetto in questione.|Più basso|

### <a name="example---indirect-permission"></a>Esempio - Autorizzazione indiretta

È possibile assegnare un'autorizzazione indiretta per utilizzare un oggetto solo attraverso un altro oggetto.
Ad esempio, un utente può disporre del permesso di eseguire la codeunit 80, Vendite-Registra. La codeunit Vendite-Registra esegue molti task, tra cui la modifica della tabella 37, Riga vendite. Quando l'utente registra un documento di vendita, la codeunit Vendite-Registra, [!INCLUDE[d365fin](includes/d365fin_md.md)] verifica se l'utente dispone delle autorizzazioni per modificare la tabella Righe vendite. In caso di risposta negativa, la codeunit non può completare i relativi task e l'utente riceve un messaggio di errore. In caso di risposta affermativa, la codeunit viene eseguita correttamente.

Tuttavia, per l'utente non è necessario avere accesso completo alla tabella Righe vendite per eseguire la codeunit. Se l'utente possiede un'autorizzazione indiretta per la tabella Righe vendite, la codeunit Vendite-Registra viene eseguita correttamente. Quando un utente possiede un'autorizzazione indiretta, tale utente può solo modificare la tabella Riga vendite eseguendo la codeunit di Vendite-Registra o un altro oggetto per cui possiede l'autorizzazione per modificare la tabella Righe vendite. L'utente può solo modificare la tabella Righe vendite quando esegue questa operazione da aree di applicazione supportate. L'utente non può eseguire inavvertitamente o intenzionalmente la funzionalità con altri metodi.

## <a name="to-create-or-modify-permissions-by-recording-your-actions"></a>Per creare o modificare le autorizzazioni registrando le azioni

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Set di autorizzazioni** e quindi scegliere il collegamento correlato.
2. In alternativa, nella pagina **Utenti** scegliere l'azione **Set di autorizzazioni**.
3. Nella pagina **Set di autorizzazioni** scegliere l'azione **Nuovo**.
4. In una nuova riga, compilare i campi in base alle esigenze.
5. Scegliere l'azione **Autorizzazioni**.
6. Nella pagina **Autorizzazioni**, scegliere l'azione **Registra autorizzazioni**, quindi selezionare l'azione **Avvia**.

    Viene avviato un processo di registrazione che acquisisce tutte le azioni nell'interfaccia utente.
7. Passare alle diverse pagine e attività di [!INCLUDE[d365fin](includes/d365fin_md.md)] a cui si desidera che gli utenti con questo set di autorizzazioni possano accedere. È necessario eseguire i task per cui si desidera registrare le autorizzazioni.
8. Quando si desidera terminare la registrazione, tornare alla pagina **Autorizzazioni** e scegliere l'azione **Arresta**.
9. Scegliere il pulsante **Sì** per aggiungere le autorizzazioni registrate nel nuovo set di autorizzazioni.
10. Per ogni oggetto nella lista registrata, specificare se gli utenti possono immettere, modificare o eliminare, i record nelle tabelle registrate.

## <a name="security-filters---to-limit-a-users-access-to-specific-records-in-a-table"></a>Filtri di protezione - Per limitare l'accesso di un utente a record specifici in una tabella

Per la protezione a livello di record in [!INCLUDE[d365fin](includes/d365fin_md.md)], si utilizzano filtri di protezione per limitare l'accesso dell'utente ai dati in una tabella. I filtri di protezione sono creati sui dati della tabella. Un filtro di protezione descrive un set di record in una tabella che un utente è autorizzato a accedere. È possibile specificare, ad esempio, che un utente può leggere solo i record che contengono informazioni su un determinato cliente. Ciò significa che l'utente non può accedere ai record che contengono informazioni su altri clienti. Per ulteriori informazioni, vedere [Utilizzo di filtri di protezione](/dynamics365/business-central/dev-itpro/security/security-filters) in Guida per sviluppatori e professionisti IT.

## <a name="to-manage-permissions-through-user-groups"></a>Per gestire le autorizzazioni tramite gruppi di utenti

È possibile impostare i gruppi di utenti per gestire facilmente i set di autorizzazioni per i gruppi di utenti della società.

Si inizia creando un gruppo di utenti. Quindi assegnare i set di autorizzazioni al gruppo per definire a quale oggetto possono accedere gli utenti del gruppo. Quando si aggiunge l'utente al gruppo, i set di autorizzazioni definiti per il gruppo verranno applicati all'utente.

I set di autorizzazioni assegnati a un utente tramite un gruppo di utenti rimangono sincronizzati in modo tale che una modifica alle autorizzazioni del gruppo di utenti venga automaticamente propagata all'utente. Se si rimuove un utente da un gruppo di utenti, le autorizzazioni interessate vengono automaticamente revocate.

### <a name="to-group-users-in-user-groups"></a>Per raggruppare gli utenti in gruppi di utenti

La seguente procedura spiega come creare manualmente gruppi di utenti. Per creare automaticamente gruppi di utenti, vedere [Per copiare un gruppo di utenti e tutti i suoi set di autorizzazioni](ui-define-granular-permissions.md#to-copy-a-user-group-and-all-its-permission-sets).

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Gruppi di utenti** e quindi scegliere il collegamento correlato.
2. In alternativa, nella pagina **Utenti** scegliere l'azione **Gruppi di utenti**.
3. Nella pagina **Gruppo di utenti**, scegliere l'azione **Membri gruppo di utenti**.
4. Nella pagina **Gruppo di utenti**, scegliere l'azione **Aggiungi utenti**.

### <a name="to-copy-a-user-group-and-all-its-permission-sets"></a>Per copiare un gruppo di utenti e tutti i suoi set di autorizzazioni

Per definire rapidamente un nuovo gruppo di utenti, è possibile copiare tutti i set di autorizzazioni da un gruppo di utenti esistenti al nuovo gruppo di utenti.

> [!NOTE]
> I membri del gruppo di utenti non vengono copiati nel nuovo gruppo di utenti. Bisogna aggiungerli manualmente successivamente. Per ulteriori informazioni, vedere [Per raggruppare gli utenti in gruppi di utenti](ui-define-granular-permissions.md#to-group-users-in-user-groups).

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Gruppi di utenti** e quindi scegliere il collegamento correlato.
2. Selezionare il gruppo di utenti che si desidera copiare, quindi scegliere l'azione **Copia gruppo di utenti**.
3. Nel campo **Nuovo codice gruppo di utenti**, immettere un nome per il gruppo, quindi scegliere il pulsante **OK**.

Il nuovo gruppo di utenti viene aggiunto nella pagina **Gruppi di utenti**. Procedere con l'aggiunta di utenti. Per ulteriori informazioni, vedere [Per raggruppare gli utenti in gruppi di utenti](ui-define-granular-permissions.md#to-group-users-in-user-groups).  

### <a name="to-assign-permission-sets-to-user-groups"></a>Per assegnare i set di autorizzazioni a gruppi utente

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Gruppi di utenti** e quindi scegliere il collegamento correlato.
2. Selezionare il gruppo di utenti a cui si intende assegnare l'autorizzazione.
Tutti i set di autorizzazioni già assegnati all'utente vengono visualizzati nel Dettaglio informazioni **Set di autorizzazioni**.
3. Scegliere l'azione **Set di autorizzazioni utente** per aprire la pagina **Set di autorizzazioni utente**.
4. Nella pagina **Set di autorizzazioni utente** compilare i campi secondo le necessità su una nuova riga.

### <a name="to-assign-a-permission-set-on-the-permission-set-by-user-group-page"></a>Per assegnare un set di autorizzazioni nella pagina **Set di autorizzazioni per gruppo di utenti**

La seguente procedura illustra come assegnare i set di autorizzazioni a un gruppo di utenti nella pagina **Set di autorizzazioni per gruppo di utenti**.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Utenti** e quindi scegliere il collegamento correlato.
2. Nella pagina **Utenti** selezionare l'utente pertinente quindi scegliere l'azione **Set di autorizzazioni per gruppo di utenti**.
3. Nella pagina **Set di autorizzazioni per gruppo di utenti** selezionare la casella di controllo **[nome gruppo di utenti]** in una riga per il set di autorizzazioni pertinente per assegnare il set al gruppo di utenti.
4. Selezionare la casella di controllo **Tutti i gruppi di utenti** per assegnare il set di autorizzazioni a tutti i gruppi di utenti.

## <a name="to-remove-obsolete-permissions-from-all-permission-sets"></a>Per rimuovere le autorizzazioni obsolete da tutti i set di autorizzazioni

1. Nella pagina **Set di autorizzazioni**, scegliere l'azione **Rimuovi autorizzazioni obsolete**.

## <a name="to-set-up-user-time-constraints"></a>Per impostare i vincoli connessioni utenti

Gli amministratori possono definire i periodi di tempo in cui utenti specificati possono effettuare registrazioni e anche specificare se il sistema registra il periodo di tempo per cui gli utenti si sono connessi. Gli amministratori possono anche assegnare centri di responsabilità agli utenti. Per ulteriori informazioni, vedi [Utilizzare i centri di responsabilità](inventory-responsibility-centers.md).

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup utente** e quindi scegliere il collegamento correlato.
2. Nella pagina **Setup utenti** scegliere l'azione **Nuovo**.
3. Nel campo **ID utente**, immettere l'ID di un utente o scegliere il campo per visualizzare tutti gli utenti correnti di Windows nel sistema.
4. Compilare i campi in base alle esigenze.

## <a name="see-also"></a>Vedere anche

[Creare utenti in base alle licenze](ui-how-users-permissions.md)  
[Gestire profili](admin-users-profiles-roles.md)  
[Modifica delle funzionalità visualizzate](ui-experiences.md)  
[Personalizzazione di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-customizing-overview.md)  
[Preparazione al business](ui-get-ready-business.md)  
[Amministrazione](admin-setup-and-administration.md)  
[Aggiungere utenti a Microsoft 365 per le aziende](https://aka.ms/CreateOffice365Users)  
[Sicurezza e protezione in Business Central](/dynamics365/business-central/dev-itpro/security/security-and-protection) nella Guida per sviluppatori e professionisti IT
