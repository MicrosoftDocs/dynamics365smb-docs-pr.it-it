---
title: Gestire utenti e ruoli
description: Informazioni su come gestire profili utente in Business Central.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 07/26/2024
ms.custom: bap-template
ms.search.form: '9171,'
---
# Gestire profili utente

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

## Personalizzazione delle pagine

È possibile personalizzare layout di pagina per un profilo di modo che tutti gli utenti assegnati al profilo possano vedere le pagine personalizzate. Come amministratore, si personalizzano le pagine utilizzando le stesse funzionalità utilizzate dagli utenti. Per ulteriori informazioni sulla personalizzazione dei layout di pagina, vedi [Personalizzare le pagine per i profili](ui-personalization-manage.md).

## Crea un profilo

Se non è possibile copiare un profilo esistente, è possibile crearne uno manualmente.

1. Seleziona la ![ricerca di pagina o report.](media/ui-search/search_small.png "Icona Cerca pagina o report") Icona, immettere **Profili (Ruoli)**, quindi Seleziona il relativo collegare.  
2. Nella pagina **Profili (Ruoli)**, Seleziona l'azione **Nuovo** .  
3. Compila i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Se desideri che un particolare profilo sia disponibile solo per utenti molto specifici, puoi impostare il campo **Descrizione** su `Navigation menu only.`. In questo modo il profilo viene escluso dall'elenco dei ruoli disponibili in **Impostazioni personali**.

## Copia di un profilo

Per risparmiare tempo, è possibile creare un nuovo profilo copiandone uno esistente. Copiarne uno con impostazioni simili a quello che si desidera creare.

Quando si copia un profilo, vengono copiate anche tutte le personalizzazioni delle pagine coinvolte, sia quelle create dall'utente sia quelle derivate dalle estensioni.

1. Nella pagina **Profili (Ruoli)**, Seleziona la riga per il profilo che vuoi copiare, quindi Seleziona l'azione **Copia profilo** .
2. Compila i campi  **ID profilo** e  **Nome visualizzato**, quindi Seleziona il pulsante  **OK** .
3. Nella pagina **Profili (ruoli)**, aprire la scheda profilo appena creata e quindi modificare altri campi come necessario.

## Modifica un profilo

È possibile modificare un profilo modificando i campi nella pagina **Profili (ruoli)**. Le modifiche non sono visibili all'utente a cui è assegnato il profilo solo dopo che tale utente avrà eseguito la disconnessione e quindi avrà eseguito di nuovo l'accesso.

> [!Caution]
> Non rinominare un profilo mentre gli utenti a cui è stato assegnato sono connessi, poiché potrebbero verificarsi blocchi del prodotto e il successivo riavvio.

## Assegna un profilo a un utente

Gli utenti possono assegnarsi un ruolo (che rappresenta un profilo) scegliendo il campo **Ruolo** nella pagina **Impostazioni personali**. Come amministratore, è possibile fare lo stesso tramite la pagina **Profili (ruoli)**.

1. Nella pagina  **Profili (Ruoli)**, Seleziona il profilo che vuoi assegnare, quindi Seleziona l'azione  **Elenco personalizzazione utente** .
2. Nella pagina **Impostazioni utente**, Seleziona l'utente a cui vuoi assegnare il profilo, quindi Seleziona l'azione **Modifica** .
3. Nel campo **ID profilo**, selezionare il profilo pertinente.

Se si assegna un altro profilo a un utente, tutte le personalizzazioni eseguite dall'utente con il profilo precedente vengono mantenute.

## Definire le impostazioni utente per un profilo

Nella pagina **Impostazioni personali**, gli utenti possono definire il comportamento di base del proprio account, come la Gestione ruolo utente, la lingua e le notifiche che ricevono. Per ulteriori informazioni sulle impostazioni utente, vedi [Modificare le impostazioni di base](ui-change-basic-settings.md).

In qualità di amministratore, puoi definire le impostazioni per un profilo. Le impostazioni verranno applicate a tutti gli utenti assegnati al ruolo.

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), Icona, immettere **Profili (Ruoli)**, quindi Seleziona il relativo collegare.
2. Seleziona la riga per il profilo per cui vuoi modificare le impostazioni utente, quindi Seleziona l'azione **Elenco personalizzazioni utente** .
3. Nella pagina **Personalizzazioni utente**, aprire la scheda per l'utente di cui si desidera modificare le impostazioni.
4. Nella pagina **Scheda personalizzazione utente** modificare i campi come necessario.

## Attiva un profilo

Quando crei un profilo, è possibile definire se, dove e come il profilo e le relative informazioni sono disponibili per gli utenti.

Nella pagina **Profili (ruoli)**, seleziona le seguenti caselle di controllo:

* **Abilitato** per specificare se il ruolo correlato è visibile nella pagina **Ruoli disponibili**.  
* **Usa come profilo predefinito** per specificare il profilo che si applica agli utenti a cui non è assegnato un ruolo specifico.
* **Disabilita personalizzazione** per specificare se gli utenti del ruolo correlato possono personalizzare la propria area di lavoro.
* **Mostra in Esplora ruoli** per specificare se le azioni per le funzionalità aziendali incluse nel profilo vengono visualizzate nella vista estesa di Esplora ruoli, una panoramica delle funzionalità. Per ulteriori informazioni su Esplora ruoli, vedi [Ricerca di pagine con Esplora ruoli](ui-role-explorer.md).

## Esporta profili

Puoi esportare i profili da [!INCLUDE[prod_short](includes/prod_short.md)] e riutilizzarli in un altro tenant. I profili vengono esportati in un file zip che contiene file Lingua applicazione (AL). Puoi riutilizzare i file AL per sviluppare estensioni. Per ulteriori informazioni sull'esportazione di profili, vedi [Utilizzare il client per creare profili e personalizzazioni di pagine](/dynamics365/business-central/dev-itpro/developer/devenv-design-profiles-using-client).

* Nella pagina **Profili (Ruoli)**, Seleziona l'azione **Esporta profili** .

    Questa azione esporta un file zip che contiene file AL per tutti i profili.

## Importa profili

Puoi importare i profili che sono stati esportati da Business Central. I passaggi sono più o meno l'opposto dei passaggi per esportare i profili.

1. Nella pagina **Profili (Ruoli)**, Seleziona l'azione **Importa profili** .
1. Segui i passaggi della procedura guidata **Importa profili**.

    Se si desidera importare solo i profili selezionati, utilizzare la casella di controllo **Selezionato** per indicare quale importare.
1. Seleziona il pulsante **Importa selezione** .

    Questa azione importa un file zip che contiene file AL per i profili selezionati.

## Elimina un profilo

È possibile eliminare un profilo selezionando l'azione **Elimina** nella pagina **Profili (ruoli)**. Tuttavia, si applicano le seguenti limitazioni:

* Non è possibile eliminare un profilo assegnato a un utente o a un gruppo di utenti.
* Non è possibile eliminare profili originati dalle estensioni. L'estensione deve essere prima disinstallata.
* È possibile eliminare un solo profilo alla volta.

## Elimina personalizzazioni

### Elimina tutte le personalizzazioni effettuate da un utente specifico

Puoi eliminare tutte le modifiche apportate da un utente a una qualsiasi pagina, ripristinando così la versione originale delle pagine area di disposizione. Le personalizzazioni non sono associate a un profilo (ruolo). Se un utente personalizza una pagina, sperimenterà le personalizzazioni sulla pagina indipendentemente dal ruolo che sta ricoprendo.<!--Deleting changes can be useful, for example, if an employee changes role and no longer needs them. The profile defines the page layout and deletions restore it back to that definition.--> 

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), Icona, inserisci **Impostazioni utente**, quindi Seleziona il relativo collegare.

    La pagina  **Impostazioni utente** elenca tutti gli utenti<!--who make personalizations-->.

2. Seleziona l'utente di cui vuoi eliminare le personalizzazioni.
3. Nella pagina **Impostazioni utente** scheda, Seleziona l'azione **Cancella pagine personalizzate**, quindi accetta il messaggio visualizzato.

L'utente vedrà le modifiche al successivo accesso.

È anche possibile eliminare tutte le personalizzazioni di pagine per un profilo. Per ulteriori informazioni, vedere [Per eliminare tutte le personalizzazioni per un profilo](ui-personalization-manage.md#delete-all-customizations-for-a-profile).

### Elimina le personalizzazioni per pagine specifiche

È possibile eliminare le personalizzazioni eseguite da uno o più utenti in pagine specifiche. L'eliminazione delle personalizzazioni può essere utile, ad esempio, se un processo aziendale modificato implica che una personalizzazione non deve più essere utilizzata. Le eliminazioni ripristinano il layout di pagina definito dal profilo.

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), Icona, inserisci **Pagine personalizzate**, quindi Seleziona il relativo collegare.

    Nella pagina  **Pagine personalizzate** sono elencate tutte le pagine personalizzate e l'utente a cui appartengono.

    <!--A checkmark in the **Legacy Personalization** field indicates that the personalization was done in an older version of [!INCLUDE[prod_short](includes/prod_short.md)], which handled personalization differently. Users who try to personalize these pages are locked from doing so unless they choose to unlock the page.-->

2. Seleziona la riga per la personalizzazione della pagina che vuoi eliminare, quindi Seleziona l'azione **Elimina** .

L'utente visualizzerà le modifiche dopo l'accesso successivo.  

È anche possibile eliminare singole personalizzazioni di pagina per un profilo. Per ulteriori informazioni, vedere [Per eliminare la personalizzazione di specifiche pagine per un profilo](ui-personalization-manage.md#delete-customization-for-specific-pages-for-a-profile).

## Gestione delle sessioni utente

Come amministratore di [!INCLUDE[prod_short](includes/prod_short.md)] online, è possibile gestire le sessioni utente nell'interfaccia di amministrazione. Per ulteriori informazioni, vedere [Gestione delle sessioni][def] nel contenuto amministrativo.  

Per [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, è possibile gestire le sessioni utilizzando, ad esempio, SQL Server Management Studio. Per ulteriori informazioni, vedere [Documentazione tecnica su SQL Server](/sql/sql-server).  

## Vedere anche

[Assegnare autorizzazioni a utenti e gruppi](ui-define-granular-permissions.md)  
[Personalizzare le pagine per profili](ui-personalization-manage.md)  
[Personalizzare l'area di lavoro](ui-personalization-user.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

[def]: /dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-sessions
