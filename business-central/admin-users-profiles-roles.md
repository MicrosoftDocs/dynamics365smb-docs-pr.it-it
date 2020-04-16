---
title: Gestire utenti e ruoli | Microsoft Docs
description: Informazioni su come gestire utenti e Gestioni ruolo utente in Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: profiles, users
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 50a67bf5d64cbf932801738d60b4477a7e3d9fde
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2020
ms.locfileid: "3186502"
---
# <a name="manage-profiles"></a>Gestire profili
A tutti gli utenti di [!INCLUDE[d365fin](includes/d365fin_md.md)] viene assegnato un profilo che ne riflette il ruolo aziendale, il reparto in cui lavorano o un'altra categorizzazione. I profili consentono agli amministratori di definire e gestire centralmente ciò che i vari tipi di utenti possono vedere e fare nell'interfaccia utente in modo da poter eseguire le proprie attività aziendali in modo efficiente.

> [!NOTE]
> L'uso aziendale tipico di un profilo è un ruolo. Un profilo viene quindi denominato *Profilo (ruolo)* nell'interfaccia utente.

Gli amministratori creano e gestiscono i profili nella pagina **Profili (ruoli)**. Ogni profilo presenta una scheda in cui è possibile gestire varie impostazioni per il ruolo correlato, come il nome del ruolo, le impostazioni utente e la Gestione ruolo utente che il profilo utilizza. Per ulteriori informazioni sulle impostazioni utente e sulle Gestioni ruolo utente, consultare [Modificare le impostazioni di base](ui-change-basic-settings.md).

Prima di poter amministrare i profili degli utenti, è necessario creare e aggiungere gli utenti tramite l'interfaccia di amministrazione di Microsoft 365. È quindi possibile assegnare autorizzazioni a ciascun utente o gruppo di utenti per definire quali funzionalità sono autorizzati a visualizzare e/o modificare. Per ulteriori informazioni, vedere [Assegnare autorizzazioni a utenti e gruppi](ui-define-granular-permissions.md).

## <a name="page-customization"></a>Personalizzazione delle pagine
È possibile personalizzare layout di pagina per un profilo di modo che tutti gli utenti assegnati al profilo possano vedere le pagine personalizzate. Come amministratore, si personalizzano le pagine utilizzando le stesse funzionalità utilizzate dagli utenti. Per ulteriori informazioni, vedere [Personalizzare pagine per profili](ui-personalization-manage.md).

## <a name="to-create-a-profile"></a>Per creare un profilo
Se non è possibile copiare un profilo esistente, è possibile crearne uno manualmente.

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Icona Cerca pagina o report"), immettere **Profili (ruoli)** e quindi scegliere il collegamento correlato.  
2. Nella pagina **Profili (ruoli)** scegliere l'azione **Nuovo**.  
3. Compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-copy-a-profile"></a>Per copiare un profilo
Per risparmiare tempo, è possibile creare un nuovo profilo copiandone uno esistente. Copiarne uno con impostazioni simili a quello che si desidera creare.

> [!NOTE]
> Quando si copia un profilo, vengono copiate anche tutte le personalizzazioni delle pagine coinvolte, sia quelle create dall'utente sia quelle derivate dalle estensioni.

1. Nella pagina **Profili (ruoli)** selezionare la riga per il profilo che si desidera copiare, quindi scegliere l'azione **Copia profilo**.
2. Riempire i campi **ID profilo** e **Nome da visualizzato**, quindi selezionare il pulsante **OK**.
3. Nella pagina **Profili (ruoli)**, aprire la scheda profilo appena creata e quindi modificare altri campi come necessario.

## <a name="to-edit-a-profile"></a>Per modificare un profilo
È possibile modificare un profilo modificando i campi nella pagina **Profilo (ruolo)**. Le modifiche saranno tuttavia visibili all'utente a cui è assegnato il profilo solo dopo che tale utente avrà eseguito la disconnessione e quindi avrà eseguito di nuovo l'accesso.

> [!Caution]
> Non rinominare un profilo mentre gli utenti a cui è stato assegnato sono connessi, poiché potrebbero verificarsi blocchi del prodotto e il successivo riavvio.

## <a name="to-assign-a-profile-to-a-user"></a>Per assegnare un profilo a un utente
Gli utenti possono assegnarsi un ruolo (che rappresenta un profilo) scegliendo il campo **Ruolo** nella pagina **Impostazioni personali**. Come amministratore, è possibile fare lo stesso tramite la pagina **Profili (ruoli)**.

1. Nella pagina **Profili (ruoli)**, selezionare il profilo che si desidera assegnare, quindi scegliere l'azione **Elenco personalizzazioni utente**.
2. Nella pagina **Personalizzazioni utente**, selezionare l'utente a cui si desidera assegnare il profilo, quindi scegliere l'azione **Modifica**.
3. Nel campo **ID profilo**, selezionare il profilo pertinente.

> [!NOTE]
> Se si assegna un altro profilo a un utente, tutte le personalizzazioni eseguite dall'utente con il profilo precedente vengono mantenute.

## <a name="to-define-user-settings-for-a-profile"></a>Per definire le impostazioni utente per un profilo
Nella pagina **Impostazioni personali**, gli utenti possono definire il comportamento di base del proprio account, come la Gestione ruolo utente, la lingua e le notifiche che ricevono. Per ulteriori informazioni, vedere [Modificare le impostazioni di base](ui-change-basic-settings.md).

Come amministratore, è possibile definire queste impostazioni per un profilo e quindi applicarle a tutti gli utenti del ruolo correlato.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Profili (Ruoli)** e quindi scegliere il collegamento correlato.
2. Selezionare la riga per il profilo per il quale si desidera modificare le impostazioni utente, selezionare l'azione **Naviga**, quindi scegliere l'azione **Personalizzazioni utente**.
3. Nella pagina **Personalizzazioni utente**, aprire la scheda per l'utente di cui si desidera modificare le impostazioni.
4. Nella pagina **Scheda personalizzazione utente** modificare i campi come necessario.

## <a name="to-activate-a-profile"></a>Per attivare un profilo
Quando si crea un profilo, è possibile selezionare diverse caselle di controllo che definiscono se, dove e come il profilo e le relative informazioni sono disponibili per gli utenti.

* Nella pagina **Profilo (ruolo)** selezionare le seguenti caselle di controllo:
    - **Abilitato** per specificare se il ruolo correlato è visibile nella pagina **Ruoli disponibili**.  
    - **Usa come profilo predefinito** per specificare il profilo che si applica agli utenti a cui non è assegnato un ruolo specifico.
    - **Disabilita personalizzazione** per specificare se gli utenti del ruolo correlato possono personalizzare la propria area di lavoro.
    - **Mostra in Esplora ruoli** per specificare se le azioni per le funzionalità aziendali incluse nel profilo vengono visualizzate nella vista estesa di Esplora ruoli, una panoramica delle funzionalità. Per ulteriori informazioni, vedere [Ricerca di pagine con Esplora ruoli](ui-role-explorer.md).

## <a name="to-export-profiles"></a>Per esportare profili
Puoi esportare i profili da [!INCLUDE[d365fin](includes/d365fin_md.md)], ad esempio per riutilizzarli in un altro tenant. I profili vengono esportati in un file zip contenente file .al che possono essere riutilizzati per sviluppare estensioni. Per ulteriori informazioni, vedere [Utilizzo del client per creare profili e personalizzazioni di pagine](/dynamics365/business-central/dev-itpro/developer/devenv-design-profiles-using-client).

* Nella pagina **Profili (ruoli)**, scegliere l'azione **Esporta profili**.

Viene esportato un file zip con i file .al per tutti i profili.

## <a name="to-import-profiles"></a>Per importare profili
Puoi importare i profili che sono stati esportati da [!INCLUDE[d365fin](includes/d365fin_md.md)]. I passaggi sono più o meno l'opposto dei passaggi per esportare i profili. Per ulteriori informazioni, vedere [Per esportare profili](admin-users-profiles-roles.md#to-export-profiles).

1. Nella pagina **Profili (ruoli)**, scegliere l'azione **Importa profili**.
2. Segui i passaggi della procedura guidata **Importa profili**.

    Se si desidera importare solo i profili selezionati, utilizzare la casella di controllo **Selezionato** per indicare quale importare.
3. Scegli il pulsante **Importa selezionato**.

Viene esportato un file zip con i file .al per i profili selezionati.

## <a name="to-delete-a-profile"></a>Per eliminare un profilo
È possibile eliminare un profilo selezionando l'azione **Elimina** nella pagina **Profili (ruoli)**. Tuttavia, si applicano le seguenti limitazioni:

- Non è possibile eliminare un profilo assegnato a un utente o a un gruppo di utenti.
- Non è possibile eliminare profili originati dalle estensioni. L'estensione deve essere prima disinstallata.
- È possibile eliminare un solo profilo alla volta.

## <a name="to-delete-all-personalizations-made-by-a-user"></a>Per eliminare tutte le personalizzazioni effettuate da un utente
È possibile eliminare tutte le modifiche che un utente ha apportato alle pagine che compongono la sua area di lavoro. Ciò può essere utile, ad esempio, se un dipendente ha cambiato ruolo e non ha più bisogno delle personalizzazioni. L'eliminazione delle personalizzazioni degli utenti ripristina il layout di pagina definito dal profilo.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Personalizzazioni utente** e quindi scegliere il collegamento correlato.

    Nella pagina **Personalizzazioni utente** sono elencati tutti gli utenti che hanno eseguito personalizzazioni.

2. Aprire la scheda dell'utente di cui si desidera eliminare le personalizzazioni.
3. Nella pagina **Scheda personalizzazione utente**, scegliere l'azione **Cancella pagine personalizzate**, quindi accettare il messaggio visualizzato.

L'utente visualizzerà le modifiche all'accesso successivo.

È anche possibile eliminare tutte le personalizzazioni di pagine per un profilo. Per ulteriori informazioni, vedere [Per eliminare tutte le personalizzazioni per un profilo](ui-personalization-manage.md#to-delete-all-customizations-for-a-profile).

## <a name="to-delete-personalizations-for-specific-pages"></a>Per eliminare le personalizzazioni per pagine specifiche
È possibile eliminare le personalizzazioni eseguite da uno o più utenti in pagine specifiche che compongono la relativa area di lavoro. Ciò può essere utile, ad esempio, se un processo aziendale modificato implica che una personalizzazione non deve più essere utilizzata dagli utenti. L'eliminazione delle personalizzazioni degli utenti ripristina il layout di pagina definito dal profilo.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Personalizzazioni pagine utente** e quindi scegliere il collegamento correlato.

    La pagina **Personalizzazioni pagine utente** elenca tutte le pagine che sono state personalizzate e l'utente a cui appartengono.

    > [!Note]
    > Un segno di spunta nel campo **Personalizzazione legacy** indica che la personalizzazione è stata effettuata in una versione precedente di [!INCLUDE[d365fin](includes/d365fin_md.md)] che gestiva la personalizzazione in modo diverso. Gli utenti che provano a personalizzare queste pagine vengono bloccati a meno che non scelgano di sbloccare la pagina. Per ulteriori informazioni, vedere [Perché la personalizzazione di una pagina è bloccata](ui-personalization-locked.md).

2. Selezionare la riga per la personalizzazione da eliminare, quindi scegliere l'azione **Elimina**.

L'utente visualizzerà le modifiche dopo l'accesso successivo.    

È anche possibile eliminare singole personalizzazioni di pagina per un profilo. Per ulteriori informazioni, vedere [Per eliminare la personalizzazione di specifiche pagine per un profilo](ui-personalization-manage.md#to-delete-customization-for-specific-pages-for-a-profile).

## <a name="see-also"></a>Vedere anche  
[Assegnare autorizzazioni a utenti e gruppi](ui-define-granular-permissions.md)  
[Personalizzare pagine per profili](ui-personalization-manage.md)  
[Personalizzare l'area di lavoro](ui-personalization-user.md)  
