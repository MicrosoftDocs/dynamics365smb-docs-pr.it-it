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
ms.date: 03/08/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 602c429733104a792a49f4a7f38e2a3090420c9d
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="manage-users-and-permissions"></a>Gestire utenti e autorizzazioni
Per aggiungere utenti in [!INCLUDE[d365fin](includes/d365fin_md.md)], l'amministratore di Office 365 della società deve innanzitutto creare gli utenti tramite l'interfaccia di amministrazione di Office 365. Per ulteriori informazioni, vedere [Aggiungere utenti a Office 365 per l'azienda](https://support.office.com/en-us/article/Add-users-to-Office-365-for-business-435ccec3-09dd-4587-9ebd-2f3cad6bc2bc)

Una volta creati gli utenti in Office 365, è possibile importarli nella finestra **Utenti** utilizzando l'azione **Ottieni utenti da Office 365**. Agli utenti vengono assegnati set di autorizzazioni in base al piano assegnato all'utente in Office 365.

È quindi possibile continuare ad assegnare set di autorizzazioni agli utenti per definire a quali oggetti di database, e quindi quali elementi dell'interfaccia utente, tali utenti dispongono di accesso e in quali società. È possibile aggiungere gli utenti ai gruppi utente. Ciò facilita l'assegnazione degli stessi set di autorizzazioni a più utenti.

Un set di permessi è un raccolta di permessi per oggetti specifici del database. A tutti gli utenti devono essere assegnati uno o più set di autorizzazioni prima di poter accedere a [!INCLUDE[d365fin](includes/d365fin_md.md)]. Alcuni set di autorizzazioni di default vengono forniti per default. È possibile utilizzare questi set di permessi già definiti, modificarli o creare ulteriori set di permessi.

Gli amministratori possono utilizzare la finestra **Setup utente** per definire i periodi di tempo in cui utenti specificati possono effettuare registrazioni e anche specificare se il sistema registra il periodo di tempo per cui gli utenti si sono connessi.

## <a name="to-assign-permissions-to-a-user"></a>Assegnare autorizzazioni a un utente
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Utenti**, quindi scegliere il collegamento correlato.
2. Selezionare l'utente a cui si intende assegnare l'autorizzazione.
Tutti i set di autorizzazioni già assegnati all'utente vengono visualizzati nel Dettaglio informazioni **Set di autorizzazioni**.
3. Scegliere l'azione **Modifica** per aprire la finestra **Scheda utente**.
4. Nella Scheda dettaglio **Set di autorizzazioni utente** compilare i campi secondo le necessità su una nuova riga. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-group-users-in-user-groups"></a>Per raggruppare gli utenti in gruppi di utenti
È possibile impostare i gruppi di utenti per gestire facilmente i set di autorizzazioni per i gruppi di utenti della società. È possibile utilizzare una funzione che consente di copiare tutti i set di autorizzazioni da un gruppo di utenti esistenti al nuovo gruppo di utenti. I membri del gruppo di utenti non vengono copiati.

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Gruppi di utenti**, quindi scegliere il collegamento correlato.
2. In alternativa, nella finestra **Utenti** scegliere l'azione **Gruppi di utenti**.
3. Nella finestra **Gruppo di utenti**, scegliere l'azione **Membri gruppo di utenti**.
6. Nella finestra **Membri gruppo di utenti**, scegliere l'azione **Aggiungi utenti**.
7. Per aggiungere nuove o ulteriori set di autorizzazioni, nella finestra **Gruppo di utenti** selezionare l'azione **Set di autorizzazioni gruppo di utenti**.
8. Nella finestra **Set di autorizzazioni gruppo di utenti**, in una nuova riga, compilare tutti campi come necessario selezionando dai set di autorizzazioni.

## <a name="to-set-up-user-time-constraints"></a>Per impostare i vincoli connessioni utenti
Gli amministratori possono definire i periodi di tempo in cui utenti specificati possono effettuare registrazioni e anche specificare se il sistema registra il periodo di tempo per cui gli utenti si sono connessi. Gli amministratori possono anche assegnare centri di responsabilità agli utenti. Per ulteriori informazioni, vedi [Utilizzare i centri di responsabilità](inventory-responsibility-centers.md).

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Setup utente**, quindi scegliere il collegamento correlato.
2. Nella finestra **Setup utenti** scegliere l'azione **Nuovo**.
3. Nel campo **ID utente**, immettere l'ID di un utente o scegliere il campo per visualizzare tutti gli utenti correnti di Windows nel sistema.
4. Compilare i campi come necessario.

## <a name="see-also"></a>Vedi anche
[Preparazione al business](ui-get-ready-business.md)  
[Impostazione e amministrazione in [!INCLUDE[d365fin](includes/d365fin_md.md)]](admin-setup-and-administration.md)  
[Benvenuto in [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

