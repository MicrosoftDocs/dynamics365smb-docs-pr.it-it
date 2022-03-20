---
title: OneDrive per il business FAQ
description: Ottieni risposte ad alcune domande tipiche sul lavoro con OneDrive for Business e Business Central.
author: brentholtorf
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: OneDrive, integration, share, browser
ms.date: 05/19/2021
ms.author: bholtorf
ms.openlocfilehash: 2ab3005c7958e6ce7cd112c495ba6bb1d0ae2366
ms.sourcegitcommit: 5a02f8527faecdffcc54f9c5c70cefe8c4b3b3f4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2022
ms.locfileid: "8381969"
---
# <a name="onedrive-for-business-faq"></a>OneDrive per il business FAQ

[!INCLUDE [online_only](includes/online_only.md)]

Questo articolo risponde ad alcune delle domande che potreste avere sul lavoro con OneDrive e [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="does-this-work-with-all-prod_short-clients"></a>Questo funziona con tutti i clienti di [!INCLUDE[prod_short](includes/prod_short.md)] ?

Sì. Puoi aprire i file in OneDrive dalle app mobili di [!INCLUDE[prod_short](includes/prod_short.md)], quando visualizzi i dettagli della carta in Microsoft Teams, o anche dall'add-in di Outlook.  

## <a name="is-onedrive-the-same-as-sharepoint-for-storing-files"></a> OneDrive è la stessa cosa di SharePoint per memorizzare i file?

Come parte del tuo abbonamento a Microsoft 365, la tua organizzazione ti fornisce OneDrive, il tuo spazio di archiviazione dei file nel cloud. OneDrive è privato per impostazione predefinita, dove organizzi i tuoi contenuti e scegli quali file o cartelle condividere e con chi. SharePoint d'altra parte, fornisce un archivio di file nel cloud che è condiviso con altri nella vostra organizzazione.  

## <a name="does-prod_short-support-consumer-onedrive"></a> [!INCLUDE[prod_short](includes/prod_short.md)] supporta il consumatore OneDrive?

No. Questa integrazione è destinata esclusivamente a OneDrive for Business e supporta solo il tuo account di lavoro. 

## <a name="are-all-onedrive-for-business-plans-supported"></a>Tutti i piani di OneDrive for Business sono supportati?

[!INCLUDE[prod_short](includes/prod_short.md)] non supporta piani indipendenti per OneDrive for Business. OneDrive deve essere acquistato come parte di un piano Microsoft 365 business o enterprise. Per ulteriori informazioni, vedere [Confrontare i prezzi e i piani di Storage cloud di OneDrive ](https://www.microsoft.com/microsoft-365/onedrive/compare-onedrive-plans?market=af&activetab=tab:primaryr2).  

## <a name="where-can-i-see-onedrive-service-health"></a>Dove posso vedere OneDrive Service Health?

Gli amministratori possono accedere al dashboard sull'integrità del servizio come parte dell'interfaccia di amministrazione di Microsoft 365. Il dashboard include OneDrive's disponibilità del servizio. 
 
## <a name="is-onedrive-integration-available-to-prod_short-on-premises"></a>L'integrazione di OneDrive è disponibile per [!INCLUDE[prod_short](includes/prod_short.md)] on premises?

Sì, ma a differenza di [!INCLUDE[prod_short](includes/prod_short.md)] online, richiede una configurazione aggiuntiva. Per ulteriori informazioni, vedere [Configurazione di Business Central On-Premises](admin-onedrive-integration.md#configuring-business-central-on-premises).  

## <a name="does-prod_short-on-premises-connect-with-sharepoint-server"></a> [!INCLUDE[prod_short](includes/prod_short.md)] on premises si collega con SharePoint Server?

No. Questa combinazione di distribuzione non è supportata, anche se SharePoint Server ha abilitato My Sites.  

## <a name="does-prod_short-online-connect-with-sharepoint-server"></a> [!INCLUDE[prod_short](includes/prod_short.md)] online si collega con SharePoint Server?

No. Questa combinazione di distribuzione non è supportata, anche se SharePoint Server ha abilitato My Sites.  

## <a name="how-does-this-work-in-an-organization-with-multiple-environments"></a>Come funziona in un'organizzazione con più ambienti?

L'integrazione presuppone che i nomi delle aziende siano unici tra gli ambienti [!INCLUDE[prod_short](includes/prod_short.md)] . Quando i nomi delle società sono unici in tutta l'organizzazione, l'apertura di un file in OneDrive copierà il file in una cartella con il nome della società corrente. Se i nomi delle società non sono unici tra gli ambienti, i file possono da nomi di società identici saranno messi insieme nella stessa cartella.  

## <a name="weve-changed-company-name-what-happens-to-my-previous-files"></a>Abbiamo cambiato il nome dell'azienda. Cosa succede ai miei file precedenti?

[!INCLUDE[prod_short](includes/prod_short.md)] non migra automaticamente i file aperti in precedenza in OneDrive nella nuova cartella. Dopo aver rinominato l'azienda, l'azione Open in OneDrive copierà i file in una cartella che ha il nuovo nome dell'azienda.   

## <a name="when-attaching-files-to-prod_short-how-do-i-pick-a-file-from-onedrive"></a>Quando si allegano dei file a [!INCLUDE[prod_short](includes/prod_short.md)], come faccio a prendere un file da OneDrive? 
[!INCLUDE[prod_short](includes/prod_short.md)] non fornisce un selezionatore di file cloud. Devi scaricare il file da OneDrive sul tuo dispositivo, e poi caricarlo su [!INCLUDE[prod_short](includes/prod_short.md)]. 

## <a name="i-want-to-open-files-in-sharepoint-instead-how-do-i-do-this"></a>Voglio invece aprire i file in SharePoint . Come si fa?

[!INCLUDE[prod_short](includes/prod_short.md)] non fornisce funzioni per copiare i file su SharePoint e aprirli da una libreria SharePoint . Contatta il tuo partner Microsoft per capire le tue opzioni, o cerca le applicazioni su AppSource.  

## <a name="how-do-i-turn-off-integration-to-onedrive"></a>Come faccio a disattivare l'integrazione in OneDrive?

[!INCLUDE[prod_short](includes/prod_short.md)] online non fornisce un modo per abilitare o disabilitare l'integrazione con OneDrive.  

## <a name="should-i-use-the-sharepoint-connection-setup-page-to-connect-to-sharepoint"></a>Devo usare la pagina SharePoint Connection Setup per connettermi a SharePoint?

Questa è una funzione legacy in cui tutti i file [!INCLUDE[prod_short](includes/prod_short.md)] da tutti gli utenti sono inviati a una singola cartella SharePoint . Raccomandiamo di non configurare la FastTab dei documenti condivisi nella pagina SharePoint Connection Setup perché stiamo lavorando per deprecare questa caratteristica.  

## <a name="which-version-of-prod_short-supports-onedrive"></a>Quale versione di [!INCLUDE[prod_short](includes/prod_short.md)] supporta OneDrive?

L'integrazione con OneDrive è diventata disponibile nella versione 2021 wave 2.  

## <a name="will-microsoft-continue-to-improve-the-integration-to-onedrive"></a>Microsoft continuerà a migliorare l'integrazione con OneDrive?

In Microsoft, i feedback della nostra variegata comunità di utenti vengono costantemente monitorati e si agisce in base ai migliori suggerimenti. Per saperne di più sulle prossime integrazioni con le app di Microsoft 365, vedi il [piano di rilascio di Dynamics 365](/dynamics365-release-plan/2021wave1).  

Se vuoi partecipare al miglioramento dell'integrazione di OneDrive, o hai un'idea che migliorerebbe la condivisione di file e la collaborazione in [!INCLUDE[prod_short](includes/prod_short.md)], aggiungi un'idea o vota le idee esistenti su [https://aka.ms/BusinessCentralIdeas](https://aka.ms/BusinessCentralIdeas).

## <a name="troubleshooting"></a>Troubleshooting

Questa sezione fornisce informazioni su come identificare e risolvere i problemi che si possono verificare quando si usa OneDrive con [!INCLUDE[prod_short](includes/prod_short.md)].  

### <a name="i-have-to-sign-in-each-time-i-open-a-file"></a>Devo accedere ogni volta che apro un file

Mi dispiace, è un problema noto e ci stiamo lavorando. Ci aspettiamo di fornire un'esperienza più fluida in un prossimo aggiornamento.  

### <a name="business-central-cant-find-my-onedrive"></a>Business Central non riesce a trovare il mio OneDrive

Quando appare questo messaggio, "Impossibile determinare la posizione del tuo OneDrive for Business, contatta il tuo partner per configurarlo", controlla se l'utente ha avuto accesso al suo OneDrive almeno una volta. Se non l'hanno fatto, chiedi alla persona di andare su portal.office.com/onedrive per impostarlo. Questo può richiedere un po' di tempo. Se il messaggio viene ancora visualizzato dopo 24 ore, contatta il supporto.  
 

## <a name="see-also"></a>Vedere anche
[Business Central e OneDrive Integrazione](across-onedrive-overview.md)  
[Gestione dell'integrazione di OneDrive con Business Central](admin-onedrive-integration.md)  
[Apertura dei file di Business Central in OneDrive](across-share-onedrive.md)  
