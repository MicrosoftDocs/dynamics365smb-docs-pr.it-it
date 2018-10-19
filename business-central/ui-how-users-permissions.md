---
title: Assegnare o modificare autorizzazioni utente | Documenti di Microsoft
description: Descrive come aggiungere utenti di Office 365 a Business Central e quindi assegnare le autorizzazioni, i diritti di accesso e le impostazioni di protezione.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 58077ae917d7943e6dd2da06847dfbb0eef5defd
ms.contentlocale: it-it
ms.lasthandoff: 09/28/2018

---
# <a name="managing-users-and-permissions"></a>Gestione di utenti e autorizzazioni
Per aggiungere utenti in [!INCLUDE[d365fin](includes/d365fin_md.md)], l'amministratore di Office 365 della società deve innanzitutto creare gli utenti tramite l'interfaccia di amministrazione di Office 365. Per ulteriori informazioni, vedere [Aggiungere utenti a Office 365 per l'azienda](https://aka.ms/CreateOffice365Users).

Una volta che gli utenti vengono creati in Office 365, possono essere inclusi nella finestra **Utenti** in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Agli utenti vengono assegnati set di autorizzazioni in base al piano assegnato all'utente in Office 365. Per informazioni dettagliate sulle licenze, vedere [Guida alle licenze di Microsoft Dynamics 365 Business Central](https://aka.ms/BusinessCentralLicensing).

È quindi possibile continuare ad assegnare set di autorizzazioni agli utenti per definire a quali oggetti di database, e quindi quali elementi dell'interfaccia utente, tali utenti dispongono di accesso e in quali società. È possibile aggiungere gli utenti ai gruppi utente. Ciò facilita l'assegnazione degli stessi set di autorizzazioni a più utenti.

Un set di permessi è un raccolta di permessi per oggetti specifici del database. A tutti gli utenti devono essere assegnati uno o più set di autorizzazioni prima di poter accedere a [!INCLUDE[d365fin](includes/d365fin_md.md)].

Nella finestra **Scheda utente**, aprire la finestra **Autorizzazioni valide** per visualizzare di quali autorizzazioni l'utente dispone e tramite quali set di autorizzazioni vengono assegnate. È inoltre possibile modificare i dettagli di autorizzazione per i set di autorizzazioni di tipo **Personalizzato**. Per ulteriori informazioni, vedere la sezione "Per visualizzare o modificare le autorizzazioni di un utente".

Gli amministratori possono utilizzare la finestra **Setup utente** per definire i periodi di tempo in cui utenti specificati possono effettuare registrazioni e anche specificare se il sistema registra il periodo di tempo per cui gli utenti si sono connessi.

Un altro sistema per definire a cosa possono accedere gli utenti è l'impostazione Esperienza. Per ulteriori informazioni, vedere [Modifica delle funzionalità visualizzate](ui-experiences.md).

## <a name="to-add-a-user-in-business-central"></a>Per aggiungere un utente in Business Central
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Utenti** e quindi scegliere il collegamento correlato.
2. Scegliere l'azione **Ottieni utenti da Office 365**.

Ogni nuovo utente che è stato creato per la sottoscrizione a Office 365 verrà aggiunto nella finestra **Utenti**.

## <a name="to-group-users-in-a-user-group"></a>Per raggruppare gli utenti in un gruppo di utenti
È possibile impostare i gruppi di utenti per gestire facilmente i set di autorizzazioni per i gruppi di utenti della società.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Gruppi di utenti** e quindi scegliere il collegamento correlato.
2. In alternativa, nella finestra **Utenti** scegliere l'azione **Gruppi di utenti**.
3. Nella finestra **Gruppo di utenti**, scegliere l'azione **Membri gruppo di utenti**.
4. Nella finestra **Membri gruppo di utenti**, scegliere l'azione **Aggiungi utenti**.

Quando vengono creati utenti o gruppi di utenti, è necessario assegnare set di autorizzazioni a ciascuno per definire l'oggetto a cui un utente può accedere. Innanzitutto, è necessario organizzare le autorizzazioni pertinenti nei set di autorizzazioni. Per ulteriori informazioni, vedere la sezione "Per creare o modificare un set di autorizzazioni".

## <a name="to-copy-a-user-group-and-all-its-permission-sets"></a>Per copiare un gruppo di utenti e tutti i suoi set di autorizzazioni
Per definire rapidamente un nuovo gruppo di utenti, è possibile copiare tutti i set di autorizzazioni da un gruppo di utenti esistenti al nuovo gruppo di utenti.

I membri del gruppo di utenti non vengono copiati nel nuovo gruppo di utenti. Bisogna aggiungerli manualmente successivamente.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Gruppi di utenti** e quindi scegliere il collegamento correlato.
2. Selezionare il gruppo di utenti che si desidera copiare, quindi scegliere l'azione **Copia gruppo di utenti**.
3. Nel campo **Nuovo codice gruppo di utenti**, immettere un nome per il gruppo, quindi scegliere il pulsante **OK**.

Il nuovo gruppo di utenti viene aggiunto nella finestra **Gruppi di utenti**. Procedere con l'aggiunta di utenti. Per ulteriori informazioni, vedere la sezione “Per raggruppare gli utenti in gruppi di utenti".  

## <a name="to-set-up-user-time-constraints"></a>Per impostare i vincoli connessioni utenti
Gli amministratori possono definire i periodi di tempo in cui utenti specificati possono effettuare registrazioni e anche specificare se il sistema registra il periodo di tempo per cui gli utenti si sono connessi. Gli amministratori possono anche assegnare centri di responsabilità agli utenti. Per ulteriori informazioni, vedi [Utilizzare i centri di responsabilità](inventory-responsibility-centers.md).

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup utente** e quindi scegliere il collegamento correlato.
2. Nella finestra **Setup utenti** scegliere l'azione **Nuovo**.
3. Nel campo **ID utente**, immettere l'ID di un utente o scegliere il campo per visualizzare tutti gli utenti correnti di Windows nel sistema.
4. Compilare i campi come necessario.

## <a name="to-create-or-edit-a-permission-set"></a>Per creare o modificare un set di autorizzazioni
I set di autorizzazioni funzionano come contenitori di autorizzazioni, in modo da poter gestire facilmente più autorizzazioni in un record. Dopo avere creato un set di autorizzazioni, è necessario aggiungere le autorizzazioni effettive. Per ulteriori informazioni, vedere la sezione "Per creare o modificare un set di autorizzazioni".

> [!NOTE]  
> Una soluzione [!INCLUDE[d365fin](includes/d365fin_md.md)] contiene solitamente una serie di set di autorizzazioni predefiniti che vengono aggiunti da Microsoft o dal fornitore software. Tali set di autorizzazioni sono di tipo **Sistema** o **Estensione**. Non è possibile creare o modificare questi tipi di set di autorizzazioni o le autorizzazioni al loro interno. Tuttavia, è possibile copiarli per definire i propri set di autorizzazioni e autorizzazioni personalizzati. <br /><br />
I set di autorizzazioni creati dagli utenti, come nuovi o come copie, sono di tipo **Definito dall'utente** e possono essere modificati.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Set di autorizzazioni** e quindi scegliere il collegamento correlato.
2. Scegliere l'azione **Nuovo** per creare un nuovo set di autorizzazioni.
3. Nella nuova riga, compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="to-copy-a-permission-set"></a>Per copiare un set di autorizzazioni
Quando si creano nuovi set di autorizzazioni, è possibile utilizzare una funzione di copia per trasferire rapidamente tutte le autorizzazioni di un altro set di autorizzazioni a un nuovo set di autorizzazioni.

> [!NOTE]  
> Se viene modificato un set di autorizzazioni di sistema che era stato copiato, si riceve una notifica (a seconda della selezione), in modo che sia possibile verificare se le modifiche sono rilevanti per copiare o scrivere nel set di autorizzazioni definito dall'utente.

1. Nella finestra **Set di autorizzazioni**, selezionare la riga per un set di autorizzazioni che si desidera copiare, quindi selezionare l'azione **Copia set di autorizzazioni**.
2. Nella finestra **Copia set di autorizzazioni**, specificare il nome del nuovo set di autorizzazioni e quindi scegliere il pulsante **OK**.
3. Selezionare la casella di controllo **Notifica in caso di set di autorizzazioni modificato** se si desidera mantenere un collegamento tra il set di autorizzazioni originale e quello copiato. Il collegamento viene quindi utilizzato per notificare all'utente se il nome o il contenuto del set di autorizzazioni originale cambia in una versione futura a cui la soluzione viene aggiornata successivamente..

Il nuovo set di autorizzazioni, contenente tutte le autorizzazioni del set di autorizzazioni copiate, viene aggiunto come nuova riga nella finestra **Set di autorizzazioni**. Si noti che le linee sono ordinate alfabeticamente all'interno di ciascun tipo.

## <a name="to-create-or-edit-permissions"></a>Per creare o modificare autorizzazioni
1. Nella finestra **Set di autorizzazioni**, selezionare la riga per un set di autorizzazioni che si desidera copiare, quindi selezionare l'azione **Autorizzazioni**.
2. Nella finestra **Autorizzazioni**, creare una nuova riga o modificare i campi in una linea esistente.

In ognuno dei campi dei cinque tipi di accesso (**Autorizzazione di lettura**, **Autorizzazione di inserimento**, **Autorizzazione di modifica**, **Autorizzazione di eliminazione** e **Autorizzazione di esecuzione**) è possibile selezionare una delle tre opzioni seguenti:

|Opzione|Description|Classificazione|
|------|-----------|
|**Sì**|L'utente può eseguire l'azione per l'oggetto in questione.|Il più alto|
|**Indiretto**|L'utente può eseguire l'azione per l'oggetto in questione ma solo attraverso un altro oggetto correlato a cui l'utente ha accesso completo.|Il secondo più alto|
|**Vuoto**|L'utente non può eseguire l'azione per l'oggetto in questione.|Più basso|

> [!NOTE]  
> Quando si modifica un'autorizzazione e quindi il relativo set di autorizzazioni, le modifiche si applicano anche ad altri utenti a cui è stato assegnato il set di autorizzazioni.

## <a name="to-assign-permission-sets-to-users-or-user-groups"></a>Per assegnare i set di autorizzazioni agli utenti o ai gruppi utente
È possibile assegnare le autorizzazioni agli utenti in due modi:
- Definire i set di autorizzazioni nella scheda utente di un utente.
- Selezionare la casella di controllo per un utente, in una colonna, per un set di autorizzazioni correlato, in una riga, nella finestra **Set di autorizzazioni per utente**.
    Con questo metodo, è inoltre possibile assegnare i set di autorizzazioni ai gruppi di utenti.

### <a name="to-assign-a-permission-set-on-a-user-card"></a>Per assegnare un set di autorizzazioni in una scheda utente
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Utenti** e quindi scegliere il collegamento correlato.
2. Selezionare l'utente a cui si intende assegnare l'autorizzazione.
Tutti i set di autorizzazioni già assegnati all'utente vengono visualizzati nel Dettaglio informazioni **Set di autorizzazioni**.
3. Scegliere l'azione **Modifica** per aprire la finestra **Scheda utente**.
4. Nella Scheda dettaglio **Set di autorizzazioni utente** compilare i campi secondo le necessità su una nuova riga. Per ulteriori informazioni, vedere la sezione "Per creare o modificare un set di autorizzazioni".

### <a name="to-assign-a-permission-set-in-the-permission-set-by-user-window"></a>Per assegnare un set di autorizzazioni nella finestra **Set di autorizzazioni per utente**  
La seguente procedura illustra come assegnare i set di autorizzazioni a un utente nella finestra **Set di autorizzazioni per utente**. I passaggi sono simili a quelli della finestra **Set di autorizzazioni per gruppo di utenti**.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Utenti** e quindi scegliere il collegamento correlato.
2. Nella finestra **Utenti**, selezionare l'utente pertinente quindi scegliere l'azione **Set di autorizzazioni per utente**.
3. Nella finestra **Set di autorizzazioni per utente**, selezionare la casella di controllo **[nome utente]** in una riga per il set di autorizzazioni pertinente per assegnare il set all'utente.
4. Selezionare la casella di controllo **Tutti gli utenti** per assegnare il set di autorizzazioni a tutti gli utenti.

## <a name="to-view-or-edit-a-users-permissions"></a>Per visualizzare o modificare le autorizzazioni di un utente
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Utenti** e quindi scegliere il collegamento correlato.
2. Aprire la scheda dell'utente pertinente.
3. Scegliere l'azione **Autorizzazioni valide**.

    La parte **Autorizzazioni** elenca tutti gli oggetti del database a cui l'utente ha accesso. Non è possibile modificare questa sezione.

    La sezione **Per set di autorizzazioni** mostra i set di autorizzazioni assegnati attraverso i quali le autorizzazioni sono concesse all'utente, l'origine e il tipo del set di autorizzazioni e il livello per i diversi tipi di accesso.

    Per ogni riga selezionata nella sezione **Autorizzazioni**, la sezione **Per set di autorizzazioni** mostra tramite quali set di autorizzazioni è stata concessa l'autorizzazione. In questa sezione, è possibile modificare il valore in ciascuno dei cinque tipi di accesso disponibili: **Autorizzazione di lettura**, **Autorizzazione di inserimento**, **Autorizzazione di modifica**, **Autorizzazione di eliminazione** e **Autorizzazione di esecuzione**.   

    > [!NOTE]  
    > È possibile modificare solo i set di autorizzazioni di tipo **Definito dall'utente**.<br /><br />
    > Le righe di autorizzazione di origine derivano dal piano di sottoscrizione. I valori di autorizzazione di diritto annullano i valori in altri set di autorizzazioni se hanno una classificazione più alta. La presenza di un valore in un set di autorizzazioni senza diritti che ha una classificazione superiore rispetto al valore correlato nel diritto sarà racchiuso tra parentesi per indicare che non è valido in quanto è superato dal diritto esistente. Per una spiegazione della classificazione, vedere la sezione "Per creare o modificare un set di autorizzazioni".  

4. Per modificare un set di autorizzazioni, nella parte **Per set di autorizzazioni**, nella riga per un set di autorizzazioni pertinente di tipo **Definito dall'utente**, selezionare uno dei cinque campi del tipo di accesso e selezionare un valore diverso.

5. Per modificare le singole autorizzazioni all'interno del set di autorizzazioni, selezionare il valore nel campo **Set di autorizzazioni** per aprire la finestra **Autorizzazioni**. Seguire i passaggi descritti nella sezione "Per creare o modificare autorizzazioni".  

> [!NOTE]  
> Quando si modifica un set di autorizzazioni, le modifiche si applicano anche ad altri utenti a cui è stato assegnato il set di autorizzazioni.

## <a name="see-also"></a>Vedi anche
[Preparazione al business](ui-get-ready-business.md)  
[Modifica delle funzionalità visualizzate](ui-experiences.md)   
[Amministrazione](admin-setup-and-administration.md)  
[Aggiungere utenti a Office 365 per l'azienda](https://aka.ms/CreateOffice365Users)  
[Guida alle licenze di Microsoft Dynamics 365 Business Central](https://aka.ms/BusinessCentralLicensing)

