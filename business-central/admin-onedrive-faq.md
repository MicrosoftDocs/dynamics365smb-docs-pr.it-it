---
title: OneDrive per il business FAQ
description: Ottieni risposte ad alcune domande tipiche sul lavoro con OneDrive for Business e Business Central.
author: brentholtorf
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'OneDrive, integration, share, browser'
ms.date: 09/09/2022
ms.author: bholtorf
---
# OneDrive per il business FAQ

[!INCLUDE [online_only](includes/online_only.md)]

Questo articolo risponde ad alcune delle domande che potreste avere sul lavoro con OneDrive e [!INCLUDE [prod_short](includes/prod_short.md)].

## Questo funziona con tutti i clienti di [!INCLUDE[prod_short](includes/prod_short.md)] ?

Sì. Puoi aprire i file in OneDrive dalle app mobili di [!INCLUDE[prod_short](includes/prod_short.md)], quando visualizzi i dettagli della carta in Microsoft Teams, o anche dall'add-in di Outlook.  

##  OneDrive è la stessa cosa di SharePoint per memorizzare i file?

Come parte del tuo abbonamento a Microsoft 365, la tua organizzazione ti fornisce OneDrive, il tuo spazio di archiviazione dei file nel cloud. OneDrive è privato per impostazione predefinita, dove organizzi i tuoi contenuti e scegli quali file o cartelle condividere e con chi. SharePoint d'altra parte, fornisce un archivio di file nel cloud che è condiviso con altri nella vostra organizzazione.  

##  [!INCLUDE[prod_short](includes/prod_short.md)] supporta il consumatore OneDrive?

No. Questa integrazione è destinata esclusivamente a OneDrive for Business e supporta solo il tuo account di lavoro. 

## Tutti i piani di OneDrive for Business sono supportati?

[!INCLUDE[prod_short](includes/prod_short.md)] non supporta piani indipendenti per OneDrive for Business. OneDrive deve essere acquistato come parte di un piano Microsoft 365 business o enterprise. Per ulteriori informazioni, vedere [Confrontare i prezzi e i piani di Storage cloud di OneDrive ](https://www.microsoft.com/microsoft-365/onedrive/compare-onedrive-plans?market=af&activetab=tab:primaryr2).  

## Dove posso vedere OneDrive Service Health?

Gli amministratori possono accedere al dashboard sull'integrità del servizio come parte dell'interfaccia di amministrazione di Microsoft 365. Il dashboard include OneDrive's disponibilità del servizio. Vai a [https://admin.microsoft.com/Adminportal/Home?#/servicehealth](https://admin.microsoft.com/Adminportal/Home?#/servicehealth).
 
## L'integrazione di OneDrive è disponibile per [!INCLUDE[prod_short](includes/prod_short.md)] on premises?

Sì, ma a differenza di [!INCLUDE[prod_short](includes/prod_short.md)] online, richiede una configurazione aggiuntiva. Per ulteriori informazioni, vedi [Configurazione di Business Central On-Premises](admin-onedrive-integration-onpremises.md).  

##  [!INCLUDE[prod_short](includes/prod_short.md)] on premises si collega con SharePoint Server?

Nr. Questa combinazione di distribuzione non è supportata, anche se SharePoint Server ha abilitato My Sites.  

##  [!INCLUDE[prod_short](includes/prod_short.md)] online si collega con SharePoint Server?

Nr. Questa combinazione di distribuzione non è supportata, anche se SharePoint Server ha abilitato My Sites.  

## Come funziona in un'organizzazione con più ambienti?

L'integrazione presuppone che i nomi delle aziende siano unici tra gli ambienti [!INCLUDE[prod_short](includes/prod_short.md)] . Quando i nomi delle società sono unici in tutta l'organizzazione, l'apertura di un file in OneDrive copierà il file in una cartella con il nome della società corrente. Se i nomi delle società non sono unici tra gli ambienti, i file possono da nomi di società identici saranno messi insieme nella stessa cartella.  

## Abbiamo cambiato il nome dell'azienda. Cosa succede ai miei file precedenti?

[!INCLUDE[prod_short](includes/prod_short.md)] non migra automaticamente i file aperti in precedenza in OneDrive nella nuova cartella. Dopo aver rinominato l'azienda, l'azione Open in OneDrive copierà i file in una cartella che ha il nuovo nome dell'azienda.   

## Quando si allegano dei file a [!INCLUDE[prod_short](includes/prod_short.md)], come faccio a prendere un file da OneDrive?

[!INCLUDE[prod_short](includes/prod_short.md)] non fornisce un selezionatore di file cloud. Devi scaricare il file da OneDrive sul tuo dispositivo, e poi caricarlo su [!INCLUDE[prod_short](includes/prod_short.md)]. 

## Voglio invece aprire i file in SharePoint . Come si fa?

[!INCLUDE[prod_short](includes/prod_short.md)] non fornisce funzioni per copiare i file su SharePoint e aprirli da una libreria SharePoint. Contatta il tuo partner Microsoft per capire le tue opzioni, o cerca le applicazioni su AppSource.  

## Come faccio a disattivare l'integrazione in OneDrive?

Esegui la guida al setup assistito **Setup OneDrive** e disattiva gli interruttori **Usa OneDrive per le funzionalità dell'app** e **Usa OneDrive per le funzionalità di sistema**. 

## Devo usare la pagina SharePoint Connection Setup per connettermi a SharePoint?

Questa è una funzione legacy in cui tutti i file [!INCLUDE[prod_short](includes/prod_short.md)] da tutti gli utenti sono inviati a una singola cartella SharePoint . Si consiglia di non configurare la Scheda dettaglio Documenti condivisi nella pagina **Setup connessione SharePoint** perché questa pagina è stata [deprecata](/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-w1#microsoft-sharepoint-connection-setup) e verrà rimossa nel secondo ciclo di rilascio del 2023, versione 23.0.  Ti consigliamo di utilizzare invece il **Setup OneDrive**.  

## Quale versione di [!INCLUDE[prod_short](includes/prod_short.md)] supporta OneDrive?

L'integrazione con OneDrive è diventata disponibile nella versione 2021 wave 2.  

## <a name="features"></a>Quali funzionalità sono interessate dall'integrazione OneDrive?

Nella guida al setup assistito **Setup OneDrive** per la configurazione dell'integrazione OneDrive, puoi attivare o disattivare le funzionalità per la gestione dei file di Business Central in OneDrive. Le funzionalità sono divise in due opzioni:

|Opzione|Descrizione|
|------|----------|
|**Usa OneDrive per le funzionalità dell'app**|Se attivi questa opzione, le azioni **Apri in OneDrive** e **Condividi** sono rese disponibili sui file in Business Central, come i file allegati ai documenti o in Report elaborati. Queste azioni consentono agli utenti di copiare, aprire e condividere file in OneDrive. Per ulteriori informazioni, vedi [Apertura e condivisione dei file di Business Central in OneDrive](across-share-onedrive.md).
|**Usa OneDrive per le funzionalità di sistema**|L'attivazione di questa opzione attiva le seguenti funzionalità:<ul><li> Le azioni **Apri in Excel** e **Modifica in Excel** nelle pagine elenco copieranno automaticamente il file Excel in OneDrive, quindi aprilo in Excel Online. Per ulteriori informazioni, vedi [Visualizzazione e modifica in Excel](across-work-with-excel.md).</li><li> L'invio di un report a un file Excel o Word copierà automaticamente il file in OneDrive, quindi aprilo in Excel o Word online. Per ulteriori informazioni, vedi [Salvataggio di un report in un file](ui-work-report.md#saving-a-report-to-a-file).|

## Microsoft continuerà a migliorare l'integrazione con OneDrive?

In Microsoft, i feedback della nostra variegata comunità di utenti vengono costantemente monitorati e si agisce in base ai migliori suggerimenti. Per saperne di più sulle prossime integrazioni con le app di Microsoft 365, vedi il [piano di rilascio di Dynamics 365](/dynamics365-release-plan/2021wave1).  

Se vuoi partecipare al miglioramento dell'integrazione di OneDrive, o hai un'idea che migliorerebbe la condivisione di file e la collaborazione in [!INCLUDE[prod_short](includes/prod_short.md)], aggiungi un'idea o vota le idee esistenti su [https://aka.ms/BusinessCentralIdeas](https://aka.ms/BusinessCentralIdeas).

## Troubleshooting

Questa sezione fornisce informazioni su come identificare e risolvere i problemi che si possono verificare quando si usa OneDrive con [!INCLUDE[prod_short](includes/prod_short.md)].  

### Business Central non riesce a trovare il mio OneDrive

Quando appare questo messaggio, "Impossibile determinare la posizione del tuo OneDrive for Business, contatta il tuo partner per configurarlo", controlla se l'utente ha avuto accesso al suo OneDrive almeno una volta. Se non l'hanno fatto, chiedi alla persona di andare su portal.office.com/onedrive per impostarlo. Questo può richiedere un po' di tempo. Se il messaggio viene ancora visualizzato dopo 24 ore, contatta il supporto.  
 
### Ho problemi con la condivisione da Outlook

Vedi [Impossibile condividere file OneDrive da Outlook.com](https://support.microsoft.com/en-us/office/can-t-share-onedrive-files-from-outlook-com-05d4cb21-40a2-40e3-b111-82cddb82d22f) nel supporto tecnico Microsoft.

### Le azioni Apri in OneDrive e Condividi mancano

Ci sono un paio di cose che puoi controllare:

- Verifica che le funzioni dell'applicazione per OneDrive siano attivate nella guida al setup assistito **Setup OneDrive**. Vedi [Configurare OneDrive usando Setup OneDrive](admin-onedrive-integration.md#configure-onedrive-using-onedrive-setup).
- Controlla che Microsoft OneDrive sia impostato su **Accetto** nella pagina **Stato informative sulla privacy**. Vedi [Stato informative sulla privacy](privacy-notices-status.md).

## Vedi anche

[Business Central e integrazione OneDrive](across-onedrive-overview.md)  
[Gestione dell'integrazione di OneDrive con Business Central](admin-onedrive-integration.md)  
[Apertura dei file di Business Central in OneDrive](across-share-onedrive.md)  
