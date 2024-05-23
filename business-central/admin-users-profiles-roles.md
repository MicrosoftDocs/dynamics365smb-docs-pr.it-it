---
title: Gestire utenti e ruoli
description: Informazioni su come gestire profili utente in Business Central.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 05/07/2024
ms.custom: bap-template
ms.search.form: '9171,'
---
# <a name="manage-user-profiles"></a>Gestire profili utente

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

Assegna tutti gli utenti a profili che riflettono:

* Il loro ruolo aziendale
* Il reparto in cui lavorano
* Un altro tipo di categorizzazione

I profili consentono agli amministratori di definire e gestire centralmente quali diversi tipi di utenti possono eseguire l'accesso a Business Central.

L'uso aziendale tipico di un profilo è un ruolo. Un profilo viene quindi denominato *Profilo (ruolo)* nell'interfaccia utente.

Gli amministratori creano e gestiscono i profili nella pagina **Profili (ruoli)**. Ciascun profilo ha una scheda in cui gestisci le impostazioni per il relativo ruolo. La scheda contiene le seguenti informazioni:

* Nome del ruolo
* Impostazioni utente
* La Gestione ruolo utente utilizzata dal profilo

Per ulteriori informazioni sulle impostazioni utente e sulle Gestioni ruolo utente, consultare [Modificare le impostazioni di base](ui-change-basic-settings.md).

Prima di poter amministrare i profili degli utenti, è necessario creare e aggiungere gli utenti tramite l'interfaccia di amministrazione di Microsoft 365. È quindi possibile assegnare autorizzazioni a ciascun utente o gruppo di utenti. Le autorizzazioni definiscono le funzionalità a cui gli utenti possono accedere. Per ulteriori informazioni sulle impostazioni delle autorizzazioni, vedi [Assegnare autorizzazioni a utenti e gruppi](ui-define-granular-permissions.md).

## <a name="page-customization"></a>Personalizzazione delle pagine

È possibile personalizzare layout di pagina per un profilo di modo che tutti gli utenti assegnati al profilo possano vedere le pagine personalizzate. Come amministratore, si personalizzano le pagine utilizzando le stesse funzionalità utilizzate dagli utenti. Per ulteriori informazioni sulla personalizzazione dei layout di pagina, vedi [Personalizzare le pagine per i profili](ui-personalization-manage.md).

## <a name="to-create-a-profile"></a>Per creare un profilo

Se non è possibile copiare un profilo esistente, è possibile crearne uno manualmente.

1. Scegli l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Icona Cerca pagina o report") immetti **Profili (ruoli)**, quindi scegli il collegamento correlato.  
2. Nella pagina **Profili (ruoli)** scegliere l'azione **Nuovo**.  
3. Compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Se desideri che un particolare profilo sia disponibile solo per utenti molto specifici, puoi impostare il campo **Descrizione** su `Navigation menu only.`. In questo modo il profilo viene escluso dall'elenco dei ruoli disponibili in **Impostazioni personali**.

## <a name="to-copy-a-profile"></a>Per copiare un profilo

Per risparmiare tempo, è possibile creare un nuovo profilo copiandone uno esistente. Copiarne uno con impostazioni simili a quello che si desidera creare.

Quando si copia un profilo, vengono copiate anche tutte le personalizzazioni delle pagine coinvolte, sia quelle create dall'utente sia quelle derivate dalle estensioni.

1. Nella pagina **Profili (ruoli)** selezionare la riga per il profilo che si desidera copiare, quindi scegliere l'azione **Copia profilo**.
2. Riempire i campi **ID profilo** e **Nome da visualizzato**, quindi selezionare il pulsante **OK**.
3. Nella pagina **Profili (ruoli)**, aprire la scheda profilo appena creata e quindi modificare altri campi come necessario.

## <a name="to-edit-a-profile"></a>Per modificare un profilo

È possibile modificare un profilo modificando i campi nella pagina **Profili (ruoli)**. Le modifiche non sono visibili all'utente a cui è assegnato il profilo solo dopo che tale utente avrà eseguito la disconnessione e quindi avrà eseguito di nuovo l'accesso.

> [!Caution]
> Non rinominare un profilo mentre gli utenti a cui è stato assegnato sono connessi, poiché potrebbero verificarsi blocchi del prodotto e il successivo riavvio.

## <a name="to-assign-a-profile-to-a-user"></a>Per assegnare un profilo a un utente

Gli utenti possono assegnarsi un ruolo (che rappresenta un profilo) scegliendo il campo **Ruolo** nella pagina **Impostazioni personali**. Come amministratore, è possibile fare lo stesso tramite la pagina **Profili (ruoli)**.

1. Nella pagina **Profili (ruoli)**, selezionare il profilo che si desidera assegnare, quindi scegliere l'azione **Elenco personalizzazioni utente**.
2. Nella pagina **Personalizzazioni utente**, selezionare l'utente a cui si desidera assegnare il profilo, quindi scegliere l'azione **Modifica**.
3. Nel campo **ID profilo**, selezionare il profilo pertinente.

Se si assegna un altro profilo a un utente, tutte le personalizzazioni eseguite dall'utente con il profilo precedente vengono mantenute.

## <a name="to-define-user-settings-for-a-profile"></a>Per definire le impostazioni utente per un profilo

Nella pagina **Impostazioni personali**, gli utenti possono definire il comportamento di base del proprio account, come la Gestione ruolo utente, la lingua e le notifiche che ricevono. Per ulteriori informazioni sulle impostazioni utente, vedi [Modificare le impostazioni di base](ui-change-basic-settings.md).

In qualità di amministratore, puoi definire le impostazioni per un profilo. Le impostazioni verranno applicate a tutti gli utenti assegnati al ruolo.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Profili (ruoli)**, quindi scegli il collegamento correlato.
2. Selezionare la riga per il profilo per il quale si desidera modificare le impostazioni utente e scegliere l'azione **Elenco personalizzazioni utente**.
3. Nella pagina **Personalizzazioni utente**, aprire la scheda per l'utente di cui si desidera modificare le impostazioni.
4. Nella pagina **Scheda personalizzazione utente** modificare i campi come necessario.

## <a name="to-activate-a-profile"></a>Per attivare un profilo

Quando crei un profilo, è possibile definire se, dove e come il profilo e le relative informazioni sono disponibili per gli utenti.

Nella pagina **Profili (ruoli)**, seleziona le seguenti caselle di controllo:

* **Abilitato** per specificare se il ruolo correlato è visibile nella pagina **Ruoli disponibili**.  
* **Usa come profilo predefinito** per specificare il profilo che si applica agli utenti a cui non è assegnato un ruolo specifico.
* **Disabilita personalizzazione** per specificare se gli utenti del ruolo correlato possono personalizzare la propria area di lavoro.
* **Mostra in Esplora ruoli** per specificare se le azioni per le funzionalità aziendali incluse nel profilo vengono visualizzate nella vista estesa di Esplora ruoli, una panoramica delle funzionalità. Per ulteriori informazioni su Esplora ruoli, vedi [Ricerca di pagine con Esplora ruoli](ui-role-explorer.md).

## <a name="to-export-profiles"></a>Per esportare profili

Puoi esportare i profili da [!INCLUDE[prod_short](includes/prod_short.md)] e riutilizzarli in un altro tenant. I profili vengono esportati in un file zip che contiene file Lingua applicazione (AL). Puoi riutilizzare i file AL per sviluppare estensioni. Per ulteriori informazioni sull'esportazione di profili, vedi [Utilizzare il client per creare profili e personalizzazioni di pagine](/dynamics365/business-central/dev-itpro/developer/devenv-design-profiles-using-client).

* Nella pagina **Profili (ruoli)**, scegliere l'azione **Esporta profili**.

    Questa azione esporta un file zip che contiene file AL per tutti i profili.

## <a name="to-import-profiles"></a>Per importare profili

Puoi importare i profili che sono stati esportati da Business Central. I passaggi sono più o meno l'opposto dei passaggi per esportare i profili.

1. Nella pagina **Profili (ruoli)**, scegliere l'azione **Importa profili**.
1. Segui i passaggi della procedura guidata **Importa profili**.

    Se si desidera importare solo i profili selezionati, utilizzare la casella di controllo **Selezionato** per indicare quale importare.
1. Scegli il pulsante **Importa selezionato**.

    Questa azione importa un file zip che contiene file AL per i profili selezionati.

## <a name="to-delete-a-profile"></a>Per eliminare un profilo

È possibile eliminare un profilo selezionando l'azione **Elimina** nella pagina **Profili (ruoli)**. Tuttavia, si applicano le seguenti limitazioni:

* Non è possibile eliminare un profilo assegnato a un utente o a un gruppo di utenti.
* Non è possibile eliminare profili originati dalle estensioni. L'estensione deve essere prima disinstallata.
* È possibile eliminare un solo profilo alla volta.

## <a name="to-delete-all-personalizations-made-by-a-user"></a>Per eliminare tutte le personalizzazioni effettuate da un utente

È possibile eliminare tutte le modifiche che un utente ha apportato alle pagine. L'eliminazione delle modifiche può essere utile, ad esempio, se un dipendente ha cambiato ruolo e non ne ha più bisogno. Il profilo definisce il layout della pagina e le eliminazioni lo ripristinano a quella definizione.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Personalizzazioni utente**, quindi scegli il collegamento correlato.

    Nella pagina **Personalizzazioni utente** sono elencati tutti gli utenti che hanno eseguito personalizzazioni.

2. Aprire la scheda dell'utente di cui si desidera eliminare le personalizzazioni.
3. Nella pagina **Scheda personalizzazione utente**, scegliere l'azione **Cancella pagine personalizzate**, quindi accettare il messaggio visualizzato.

L'utente visualizzerà le modifiche all'accesso successivo.

È anche possibile eliminare tutte le personalizzazioni di pagine per un profilo. Per ulteriori informazioni, vedere [Per eliminare tutte le personalizzazioni per un profilo](ui-personalization-manage.md#delete-all-customizations-for-a-profile).

## <a name="to-delete-personalizations-for-specific-pages"></a>Per eliminare le personalizzazioni per pagine specifiche

È possibile eliminare le personalizzazioni eseguite da uno o più utenti in pagine specifiche. L'eliminazione delle personalizzazioni può essere utile, ad esempio, se un processo aziendale modificato implica che una personalizzazione non deve più essere utilizzata. Le eliminazioni ripristinano il layout di pagina definito dal profilo.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Personalizzazioni pagine utente**, quindi scegli il collegamento correlato.

    La pagina **Personalizzazioni pagine utente** elenca tutte le pagine che sono state personalizzate e l'utente a cui appartengono.

    Un segno di spunta nel campo **Personalizzazione legacy** indica che la personalizzazione è stata effettuata in una versione precedente di [!INCLUDE[prod_short](includes/prod_short.md)] che gestiva la personalizzazione in modo diverso. Gli utenti che provano a personalizzare queste pagine vengono bloccati a meno che non scelgano di sbloccare la pagina.

2. Selezionare la riga per la personalizzazione da eliminare, quindi scegliere l'azione **Elimina**.

L'utente visualizzerà le modifiche dopo l'accesso successivo.  

È anche possibile eliminare singole personalizzazioni di pagina per un profilo. Per ulteriori informazioni, vedere [Per eliminare la personalizzazione di specifiche pagine per un profilo](ui-personalization-manage.md#delete-customization-for-specific-pages-for-a-profile).

## <a name="managing-user-sessions"></a>Gestione delle sessioni utente

Come amministratore di [!INCLUDE[prod_short](includes/prod_short.md)] online, è possibile gestire le sessioni utente nell'interfaccia di amministrazione. Per ulteriori informazioni, vedere [Gestione delle sessioni][def] nel contenuto amministrativo.  

Per [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, è possibile gestire le sessioni utilizzando, ad esempio, SQL Server Management Studio. Per ulteriori informazioni, vedere [Documentazione tecnica su SQL Server](/sql/sql-server).  

## <a name="see-also"></a>Vedere anche

[Assegnare autorizzazioni a utenti e gruppi](ui-define-granular-permissions.md)  
[Personalizzare le pagine per profili](ui-personalization-manage.md)  
[Personalizzare l'area di lavoro](ui-personalization-user.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

[def]: /dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-sessions
