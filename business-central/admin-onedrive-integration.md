---
title: Gestione dell'integrazione di OneDrive con Business Central
description: Scopri le cose che puoi fare per gestire un'integrazione tra Business Central e OneDrive for Business.
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'OneDrive, share, browser'
ms.date: 06/13/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---
# Gestione dell'integrazione di OneDrive con Business Central

Questo articolo fornisce una panoramica di ciò che un amministratore può fare per controllare l'integrazione di OneDrive for Business con [!INCLUDE[prod_short](includes/prod_short.md)]. I clienti online [!INCLUDE[prod_short](includes/prod_short.md)] beneficiano di un'integrazione automatica, senza che sia necessaria una configurazione aggiuntiva per aprire e utilizzare queste funzioni OneDrive. Con la guida al setup assistito **Setup OneDrive** puoi dare agli utenti l'accesso ad altre funzionalità OneDrive, come l'apertura dei file Excel in OneDrive, o anche disattivare tutte le funzionalità.  

## Configurare OneDrive per l'integrazione con Business Central

Questa sezione discute i requisiti che devono essere soddisfatti in OneDrive for Business per configurare l'integrazione con Business Central e l'attività che è possibile eseguire per gestire l'integrazione.

### Requisiti minimi

* Ogni utente deve avere una licenza per [!INCLUDE[prod_short](includes/prod_short.md)] e OneDrive come parte di un piano Microsoft 365.
* OneDrive deve essere impostato per ogni utente.

### Gestione della privacy

> [!IMPORTANT]
> Se hai scelto di distribuire Business Central e OneDrive in diversi paesi o aree geografiche, i file generati da Business Central e inseriti in OneDrive possono attraversare i confini della residenza dei dati. Assicurati di confermare le politiche della tua organizzazione e i requisiti di conformità governativa per la residenza dei dati prima di abilitare la connessione a OneDrive.

Gli amministratori e gli utenti finali controllano il contenuto memorizzato in OneDrive, e questi dati sono di proprietà esclusiva della tua organizzazione. Per ulteriori informazioni, vedi [Come SharePoint e OneDrive proteggono i tuoi dati nel cloud](/sharepoint/safeguarding-your-data). Puoi anche visitare la nostra [dichiarazione sulla privacy di Microsoft](https://privacy.microsoft.com/en-us/privacystatement), che spiega i dati che Microsoft tratta, come Microsoft li tratta e per quali scopi.

Abilitando la connessione al servizio, accetti:

(a) condividere i dati da Dynamics 365 Business Central con il provider di servizi, che li utilizzerà secondo le condizioni e l'informativa sulla privacy; (b) i livelli di conformità del provider di servizi possono essere diversi da Dynamics 365 Business Central e (c) Microsoft può condividere le informazioni di contatto con il provider di servizi, se necessario, per consentirgli di gestire e risolvere i problemi relativi al servizio.

## Configura Business Central

Con Business Central online, la connessione tra Business Central e OneDrive è configurata automaticamente, e le funzionalità OneDrive sono prontamente disponibili per gli utenti per impostazione predefinita. Se desideri disattivare alcune o tutte le funzionalità, puoi utilizzare la guida al setup assistito **Setup OneDrive** nel client Business Central.

La configurazione di Business Central in locale è diversa perché la connessione tra Business Central e OneDrive non è configurata automaticamente. È necessario eseguirla manualmente. Per ulteriori informazioni, vedi [Configurazione dell'integrazione OneDrive con Business Central in locale](admin-onedrive-integration-onpremises.md).

### Informazioni sugli ambienti multipli

L'integrazione OneDrive è configurata in base all'ambiente, ovvero le impostazioni verranno applicate a tutte le società in quell'ambiente. Se la tua organizzazione ha più di un ambiente, dovrai configurare l'integrazione OneDrive per ciascuno di essi.

### Prerequisiti

- Autorizzazione indiretta, modifica ed eliminazione (imd) sulla tabella **Scenario di servizio documenti** come minimo

### Configurare OneDrive usando Setup OneDrive

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Setup OneDrive**, quindi scegli il collegamento correlato. 
2. La prima volta che esegui il setup assistito, vedrai il collegamento **Privacy**. Leggi le informazioni della pagina e, se sei d'accordo con le condizioni, seleziona **Accetto** e continua.
3. Nella pagina **Configura gestione file OneDrive** sono presenti le seguenti opzioni tra cui scegliere:

   [!INCLUDE[onedrive-feature-options](includes/onedrive-feature-options.md)]
4. Seleziona **Avanti**>**Fatto**.

### Passaggio alla nuova integrazione OneDrive dopo l'aggiornamento

Il setup assistito **Setup OneDrive** è stata introdotto nel secondo ciclo di rilascio del 2022, versione 21.0. In precedenza, l'integrazione OneDrive utilizzava **Setup connessione SharePoint**, che è stato deprecato e verrà rimosso nel secondo ciclo di rilascio del 2023, versione 23.0. Dopo aver eseguito l'aggiornamento alla versione 21, OneDrive funzionerà ancora come prima. Ma ti consigliamo di passare alla nuova integrazione OneDrive. Fare questo passaggio ora renderà le cose più facili quando il **Setup connessione SharePoint** viene infine rimosso. Inoltre, ti consentirà di utilizzare la guida al setup assistito **Setup OneDrive** per gestire le funzionalità OneDrive accessibili agli utenti. Il setup assistito **Setup OneDrive** effettua il passaggio dal setup SharePoint legacy facilmente e semplicemente.

Per passare, basta aprire ed eseguire il setup assistito **Setup OneDrive** direttamente o aprire la pagina **Setup connessione SharePoint** e scegliere **Vai al nuovo setup OneDrive** nella notifica nella parte superiore della pagina. Seguire la guida al setup come descritto nella sezione precedente.

## Ripristinare OneDrive e [!INCLUDE[prod_short](includes/prod_short.md)]

Come parte di un esercizio di disaster recovery, gli amministratori potrebbero aver bisogno di ripristinare un ambiente [!INCLUDE[prod_short](includes/prod_short.md)] online su un backup da un momento nel passato, e sincronizzare lo storage OneDrive a quello stesso punto nel tempo. OneDrive fornisce vari strumenti di ripristino, come il ripristino di OneDrive di un utente ad un tempo precedente, il ripristino di una versione precedente di un singolo file, o il ripristino di file cancellati. Per ulteriori informazioni, vedere i seguenti articoli:

* Per [!INCLUDE[prod_short](includes/prod_short.md)], vedere [Ripristino di un ambiente nell'Admin Center](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-backup-restore).
* Per OneDrive, vedere [Ripristino OneDrive](https://support.microsoft.com/en-us/office/restore-your-onedrive-fa231298-759d-41cf-bcd0-25ac53eb8a15?ui=en-us&rs=en-us&ad=us)

## Governance

Il centro amministrativo di SharePoint fornisce un ampio controllo sulle politiche che regolano l'uso di OneDrive in tutta l'organizzazione. Gli amministratori globali, o gli utenti che hanno il ruolo SharePoint Admin, possono impostare le politiche che determinano chi può accedere a OneDrive, dove risiedono i dati, il ciclo di vita dei contenuti e molto altro. I seguenti collegamenti forniscono informazioni sulle caratteristiche e le impostazioni usate spesso che possono migliorare l'integrazione con [!INCLUDE[prod_short](includes/prod_short.md)]. 

* [Gestire le impostazioni di condivisione](/sharepoint/turn-external-sharing-on-or-off)
* [Utilizzare le barriere informative con SharePoint](/sharepoint/information-barriers)
* [Conoscere la prevenzione della perdita di dati](/microsoft-365/compliance/dlp-learn-about-dlp)
* [Imposta lo spazio di archiviazione predefinito per gli utenti di OneDrive ](/onedrive/set-default-storage-space)
* [Aggiungere e rimuovere amministratori per un utente OneDrive](/sharepoint/manage-user-profiles#add-and-remove-admins-for-a-users-onedrive)
* [Disattivare la creazione di OneDrive per alcuni utenti](/sharepoint/manage-user-profiles#disable-onedrive-creation-for-some-users)
* [Capacità Multi-Geo in OneDrive e SharePoint Online](/microsoft-365/enterprise/multi-geo-capabilities-in-onedrive-and-sharepoint-online-in-microsoft-365)

> [!NOTE]
> Alcune caratteristiche possono essere disponibili solo per piani specifici.

## Vedere anche

[Business Central e OneDrive per l'integrazione del business](across-onedrive-overview.md)  
[Apertura dei file di Business Central in OneDrive](across-share-onedrive.md)  
[OneDrive FAQ](admin-onedrive-faq.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
