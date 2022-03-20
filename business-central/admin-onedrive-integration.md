---
title: Gestione dell'integrazione di OneDrive con Business Central
description: Scopri le cose che puoi fare per gestire un'integrazione tra Business Central e OneDrive for Business.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: OneDrive, share, browser
ms.date: 05/12/2021
ms.author: bholtorf
ms.openlocfilehash: 5debd01f9d26e5e1dc1abc1a0123073d0f7ee234
ms.sourcegitcommit: 5a02f8527faecdffcc54f9c5c70cefe8c4b3b3f4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2022
ms.locfileid: "8382873"
---
# <a name="managing-onedrive-integration-with-business-central"></a>Gestione dell'integrazione di OneDrive con Business Central 
Questo articolo fornisce una panoramica di ciò che un amministratore può fare per controllare l'integrazione di OneDrive for Business con [!INCLUDE[prod_short](includes/prod_short.md)]. [!INCLUDE[prod_short](includes/prod_short.md)] i clienti online beneficiano di un'integrazione automatica, senza che sia necessaria una configurazione aggiuntiva per utilizzare queste funzioni. 

## <a name="minimum-requirements"></a>Requisiti minimi

* Ogni utente deve avere una licenza per [!INCLUDE[prod_short](includes/prod_short.md)] e OneDrive come parte di un piano Microsoft 365.
* OneDrive deve essere impostato per ogni utente.

## <a name="governance"></a>Governance
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

## <a name="managing-privacy"></a>Gestione della privacy
Gli amministratori e gli utenti finali controllano il contenuto memorizzato in OneDrive, e questi dati sono di proprietà esclusiva della tua organizzazione. Per ulteriori informazioni, vedi [Come SharePoint e OneDrive proteggono i tuoi dati nel cloud](/sharepoint/safeguarding-your-data). Puoi anche visitare la nostra [dichiarazione sulla privacy di Microsoft](https://privacy.microsoft.com/en-us/privacystatement), che spiega i dati che Microsoft tratta, come Microsoft li tratta e per quali scopi.

## <a name="restoring-onedrive-and-prod_short"></a>Ripristinare OneDrive e [!INCLUDE[prod_short](includes/prod_short.md)]
Come parte di un esercizio di disaster recovery, gli amministratori potrebbero aver bisogno di ripristinare un ambiente [!INCLUDE[prod_short](includes/prod_short.md)] su un backup da un momento nel passato, e sincronizzare lo storage OneDrive a quello stesso punto nel tempo. OneDrive fornisce vari strumenti per questo, come il ripristino di OneDrive di un utente ad un tempo precedente, il ripristino di una versione precedente di un singolo file, o il ripristino di file cancellati. Per ulteriori informazioni, vedere i seguenti articoli:

* Per [!INCLUDE[prod_short](includes/prod_short.md)], vedere [Ripristino di un ambiente nell'Admin Center](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-backup-restore).
* Per OneDrive, vedere [Ripristino OneDrive](https://support.microsoft.com/en-us/office/restore-your-onedrive-fa231298-759d-41cf-bcd0-25ac53eb8a15?ui=en-us&rs=en-us&ad=us)

## <a name="configuring-business-central-on-premises"></a>Configurazione di Business Central On-Premises

Un amministratore deve impostare la connessione tra [!INCLUDE[prod_short](includes/prod_short.md)] on premises e OneDrive. A differenza di [!INCLUDE[prod_short](includes/prod_short.md)] online, la connessione non è automatica. Se la connessione non è configurata, gli utenti non possono usare le funzioni di OneDrive. 

[!INCLUDE[prod_short](includes/prod_short.md)] on-premises può essere collegato solo a OneDrive ospitato da Microsoft nel cloud. La connessione di [!INCLUDE[prod_short](includes/prod_short.md)] on premises al repository My Sites di SharePoint Server non è supportata.

> [!IMPORTANT]
> Configurando questa funzione, si abilitano anche le funzioni legacy che inviano file a OneDrive.  
>
>* La funzione Apri in Excel copierà automaticamente il file Excel su OneDrive, quindi lo aprirà in Excel Online. 
>* Esportando qualsiasi rapporto in un file, il file verrà automaticamente copiato in OneDrive, quindi aperto in Excel Online, Word Online o OneDrive. 
>* Altre funzioni possono anche aprirsi automaticamente in OneDrive.

### <a name="to-prepare-prod_short-on-premises-for-connecting-to-onedrive"></a>Per preparare [!INCLUDE[prod_short](includes/prod_short.md)] on-premises per la connessione a OneDrive

<!-- 
1. For the best experience Configure Azure Active Directory (AD) authentication.

   For more information, see [Authenticating Business Central Users with Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-azure-active-directory)-->

Aggiungi un'applicazione registrata per Business Central nel tenant Azure AD del tuo piano Microsoft 365. Come altri servizi Azure che lavorano con Business Central, OneDrive richiede una registrazione dell'app in Azure Active Directory (Azure AD). La registrazione dell'app fornisce servizi di autenticazione e autorizzazione tra Business Central e SharePoint, utilizzato da OneDrive.

Configurare l'applicazione registrata con le seguenti autorizzazioni delegate all'API SharePoint :

- TuttiSiti.Write
- Scrivere i miei file
- Utente.Read.All 

Si fa questo lavoro nel portale Azure. Assicuratevi di copiare l'Application (client) ID e il Segreto client utilizzati dall'applicazione registrata. Avrai bisogno di queste informazioni nel prossimo compito.

Per maggiori informazioni sulla registrazione di un'applicazione e la configurazione dei permessi, vedi [Registrare un'applicazione in Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory) nell'aiuto per sviluppatori e IT pro.

> [!TIP]
> Se hai già registrato un'applicazione come parte di un'integrazione con un altro prodotto Microsoft, come Power BI, allora puoi riutilizzare la registrazione dell'applicazione. In questo caso, dovrete solo impostare i permessi di SharePoint .

### <a name="to-set-up-the-connection-in-prod_short-on-premises"></a>Per impostare la connessione in [!INCLUDE[prod_short](includes/prod_short.md)] on-premises

<!--
> [!NOTE]
> This requires the following types of authentication credentials:
>
> * Windows
> * NavUserPassword
> * Azure Active Directory
-->
1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") , entrare in **Microsoft SharePoint - Configurazione connessione**, e poi scegliere il link relativo.
2. Nel campo **Descrizione**, inserisci una descrizione per la connessione, come **OneDrive**.
3. Nel campo **Cartella**, inserisci **Business Central**.
4. Nel campo **Posizione**, inserisci l'URL del tuo OneDrive.

    L'URL di un OneDrive è di solito nel seguente formato: `https://<tenant name>-my.sharepoint.com`. Per maggiori informazioni, vedi [OneDrive URL per gli utenti della tua organizzazione](/onedrive/list-onedrive-urls) nella documentazione di OneDrive .
5. Nel campo **ID** cliente, inserisci l'ID cliente dalla registrazione dell'applicazione.
6. Nel campo **Segreto client**, inserisci il segreto della tua registrazione dell'applicazione. 
   <!-- 
   For information about how to find the URLs, see the following:
   * [How to find your SharePoint server URL]
   * [How to find your OneDrive URL]-->

> [!IMPORTANT]
> La pagina SharePoint Connection Setup è usata per configurare diverse funzioni legacy. La sezione **Generale** configura la connessione a OneDrive, e la sezione **Documenti condivisi** reindirizza invece i file a SharePoint . La funzione legacy SharePoint sarà deprecata nel prossimo futuro. Si consiglia di non configurare la sezione **Documenti condivisi** .

## <a name="see-also"></a>Vedere anche
[Business Central e OneDrive per l'integrazione del business](across-onedrive-overview.md)  
[Apertura dei file di Business Central in OneDrive](across-share-onedrive.md)  
[OneDrive FAQ](admin-onedrive-faq.md)

