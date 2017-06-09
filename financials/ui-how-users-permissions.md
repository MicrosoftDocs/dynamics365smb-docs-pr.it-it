---
title: 'Procedura: Gestire gli utenti e le autorizzazioni | Documenti Microsoft'
description: Gestire i set di autorizzazioni per gli utenti dopo avere creato gli utenti in Office 365.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: d1a973b864a654e2047c5a89271519da04f55c08
ms.contentlocale: it-it
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-manage-users-and-permissions"></a>Procedura: Gestire gli utenti e le autorizzazioni
Per aggiungere utenti in [!INCLUDE[d365fin](includes/d365fin_md.md)], l'amministratore di Office 365 della società deve innanzitutto creare gli utenti tramite l'interfaccia di amministrazione di Office 365. Per ulteriori informazioni, vedere [Aggiungere utenti a Office 365 per l'azienda](https://support.office.com/en-us/article/Add-users-to-Office-365-for-business-435ccec3-09dd-4587-9ebd-2f3cad6bc2bc)

Una volta creati gli utenti in Office 365, è possibile importarli nella finestra **Utenti** utilizzando l'azione **Ottieni utenti da Office 365**. Agli utenti vengono assegnati set di autorizzazioni in base al piano assegnato all'utente in Office 365.

È quindi possibile continuare ad assegnare set di autorizzazioni agli utenti per definire a quali oggetti di database, e quindi quali elementi dell'interfaccia utente, tali utenti dispongono di accesso e in quali società.

**Importante**: se il database include più società, almeno un utente deve essere configurato come membro del gruppo di utenti SUPER in tutte le società.

Un set di permessi è un raccolta di permessi per oggetti specifici del database. A tutti gli utenti devono essere assegnati uno o più set di autorizzazioni prima di poter accedere a [!INCLUDE[d365fin](includes/d365fin_md.md)]. Alcuni set di autorizzazioni predefiniti vengono forniti per default. È possibile utilizzare questi set di permessi già definiti, modificarli o creare ulteriori set di permessi.

È possibile aggiungere gli utenti ai gruppi utente. Ciò facilita l'assegnazione degli stessi set di autorizzazioni a più utenti.

**Nota**: questa funzionalità richiede che l'esperienza sia impostata su Suite. Per ulteriori informazioni, vedere [Personalizzazione dell'esperienza di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md).

## <a name="to-assign-permissions-to-a-user"></a>Assegnare autorizzazioni a un utente
1. Nell'angolo superiore destro, scegliere l'icona Cerca pagina o report, immettere **Utenti**, quindi scegliere il collegamento correlato.
2. Selezionare l'utente a cui si intende assegnare l'autorizzazione.
Tutti i set di autorizzazioni già assegnati all'utente vengono visualizzati nel Dettaglio informazioni **Set di autorizzazioni**.
3. Scegliere l'azione **Modifica** per aprire la finestra **Scheda utente**.
4. Nella Scheda dettaglio **Set di autorizzazioni utente** compilare i campi secondo le necessità su una nuova riga. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-group-users-in-user-groups"></a>Per raggruppare gli utenti in gruppi di utenti
È possibile impostare i gruppi di utenti per gestire facilmente i set di autorizzazioni per i gruppi di utenti della società. È possibile utilizzare una funzione che consente di copiare tutti i set di autorizzazioni da un gruppo di utenti esistenti al nuovo gruppo di utenti. I membri del gruppo di utenti non vengono copiati.

1. Nell'angolo superiore destro, scegliere l'icona Cerca pagina o report, immettere **Gruppi di utenti**, quindi scegliere il collegamento correlato.
2. In alternativa, nella finestra **Utenti** scegliere l'azione **Gruppi di utenti**.
3. Nella finestra **Gruppi di utenti** selezionare un gruppo di utenti esistenti che si desidera copiare quindi scegliere l'azione **Copia gruppo di utenti**.
4. Nel campo **Nuovo codice gruppo di utenti** specificare il nome del nuovo gruppo di utenti quindi scegliere il pulsante **OK**.

    Come alternativa alla copia, è possibile scegliere l'azione Nuovo per creare una nuova riga per un gruppo di utenti vuoto, che quindi viene compilato manualmente.
5. Per aggiungere nuovi o ulteriori utenti, nella finestra **Gruppo di utenti** selezionare l'azione **Membri gruppo di utenti**.
6. Nella finestra **Membri gruppo di utenti**, in una nuova riga, compilare tutti i campi come necessario selezionando dagli utenti esistenti.
7. Per aggiungere nuove o ulteriori autorizzazioni, nella finestra **Gruppo di utenti** selezionare l'azione **Set di autorizzazioni gruppo di utenti**.
8. Nella finestra **Set di autorizzazioni gruppo di utenti**, in una nuova riga, compilare tutti campi come necessario selezionando dai set di autorizzazioni.

## <a name="to-create-or-modify-permission-sets"></a>Per creare o modificare i set di autorizzazioni
Se i set di autorizzazioni di default forniti con [!INCLUDE[d365fin](includes/d365fin_md.md)] non sono sufficienti o non appropriati per la propria organizzazione, è possibile creare nuovi set di autorizzazioni. Se le singole autorizzazioni oggetto che definiscono un set di autorizzazioni non sono appropriate, è possibile modificare un set di autorizzazioni. È possibile creare manualmente un set di autorizzazioni oppure utilizzare una funzione di registrazione per le azioni mentre gli utenti effettuano spostamenti in uno scenario e quindi generare il set di autorizzazioni richiesto.

### <a name="to-create-or-modify-permission-sets-manually"></a>Per creare o modificare i set di autorizzazioni manualmente
1. Nell'angolo superiore destro, scegliere l'icona Cerca pagina o report, immettere **Utenti**, quindi scegliere il collegamento correlato.
2. Nella finestra **Utenti** scegliere l'azione **Set di autorizzazioni**.
3. Nella finestra **Set di autorizzazioni** scegliere l'azione **Nuovo**.
4. In una nuova riga, compilare i campi in base alle esigenze.
5. Scegliere l'azione **Autorizzazioni**.
6. Nella finestra **Autorizzazioni** compilare i campi nell'intestazione in base alle esigenze.
7. In una nuova riga, compilare i cinque campi per i vari tipi di autorizzazione come descritto nella tabella seguente.

    |Opzione|Descrizione|
    |------|-----------|
    |Vuoto|Specifica che il tipo di autorizzazione non è concesso per l'oggetto.|
    |**Sì**|Specifica che il tipo di autorizzazione è concesso con accesso diretto all'oggetto.|
    |**Indiretto**|Specifica che il tipo di autorizzazione è concesso con accesso indiretto all'oggetto.|

    L'autorizzazione indiretta per una tabella significa che non è possibile aprire la tabella e leggere da essa, ma è possibile visualizzare i dati della tabella mediante un altro oggetto, ad esempio una pagina, con autorizzazione diretta all'accesso. Per ulteriori informazioni, vedere la sezione "Esempio - Autorizzazione indiretta" in questo argomento.

8. Nel campo **Filtro protezione** immettere un filtro da applicare all'autorizzazione selezionando il campo per cui si desidera limitare l'accesso dell'utente.

    Ad esempio, se si desidera creare un filtro di protezione in modo che l'utente visualizzi solo le vendite con uno specifico codice agente, si può scegliere il numero di campo per il campo **Codice agente**. Quindi, nel campo **Filtro campo**, immettere il valore di che si desidera utilizzare per limitare l'accesso. Ad esempio, per limitare l'accesso di un utente solo alle vendite di Annette Hill, immettere AH.
9. Ripetere i passaggi 7 e 8 per aggiungere le autorizzazioni per gli oggetti aggiuntivi al set di autorizzazioni.

### <a name="to-create-or-modify-permission-sets-by-recording-your-actions"></a>Per creare o modificare i set di autorizzazioni registrando le azioni
1. Nell'angolo superiore destro, scegliere l'icona Cerca pagina o report, immettere **Utenti**, quindi scegliere il collegamento correlato.
2. Nella finestra **Utenti** scegliere l'azione **Set di autorizzazioni**.
3. Nella finestra **Set di autorizzazioni** scegliere l'azione **Nuovo**.
4. In una nuova riga, compilare i campi in base alle esigenze.
5. Scegliere l'azione **Autorizzazioni**.
6. Nella finestra **Autorizzazioni** scegliere l'azione **Avvia**.

    Un processo di registrazione inizia ad acquisire tutte le azioni nell'interfaccia utente.
7. Passare alle diverse finestre e attività di [!INCLUDE[d365fin](includes/d365fin_md.md)] a cui si desidera che gli utenti con questo set di autorizzazioni possano accedere. È necessario eseguire i task per cui si desidera registrare le autorizzazioni.
8. Quando si desidera terminare la registrazione, tornare alla finestra **Autorizzazioni** e scegliere l'azione **Arresta**.
9. Scegliere il pulsante **Sì** per aggiungere le autorizzazioni registrate nel nuovo set di autorizzazioni.
10. Per ogni oggetto nella lista registrata, specificare se gli utenti possono immettere, modificare o eliminare, i record nelle tabelle registrate. Vedere il passaggio 7 della sezione "Per creare o modificare i set di autorizzazioni manualmente".

### <a name="example---indirect-permission"></a>Esempio - Autorizzazione indiretta
È possibile assegnare un'autorizzazione indiretta per utilizzare un oggetto solo attraverso un altro oggetto.
Ad esempio, un utente può disporre dell'autorizzazione per eseguire la codeunit 80, **Vendite-Registra**. La codeunit **Vendite-Registra** esegue molti task, tra cui la modifica della tabella 37, **Riga vendite**. Quando l'utente registra un documento di vendita, la codeunit **Vendite-Registra**, [!INCLUDE[d365fin](includes/d365fin_md.md)] verifica se l'utente dispone delle autorizzazioni per modificare la tabella **Righe vendite**. In caso di risposta negativa, la codeunit non può completare i relativi task e l'utente riceve un messaggio di errore. In caso di risposta affermativa, la codeunit viene eseguita correttamente.

Tuttavia, per l'utente non è necessario avere accesso completo alla tabella **Righe vendite** per eseguire la codeunit. Se l'utente possiede un'autorizzazione indiretta per la tabella **Righe vendite**, la codeunit **Vendite-Registra** viene eseguita correttamente. Quando un utente possiede un'autorizzazione indiretta, tale utente può solo modificare la tabella **Riga vendite** eseguendo la codeunit di **Vendite-Registra** o un altro oggetto per cui possiede l'autorizzazione per modificare la tabella **Righe vendite**. L'utente può solo modificare la tabella **Righe vendite** quando esegue questa operazione da aree di applicazione supportate. L'utente non può eseguire inavvertitamente o intenzionalmente la funzionalità con altri metodi.

## <a name="see-also"></a>Vedi anche
[Preparazione al business](ui-get-ready-business.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]](index.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

