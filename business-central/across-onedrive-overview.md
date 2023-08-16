---
title: Business Central e OneDrive per l'integrazione del business
description: 'Puoi usare OneDrive for Business per archiviare, gestire e condividere file, come rapporti o allegati. Anche se lo scrivi One Drive.'
author: jswymer
ms.topic: overview
ms.workload: na
ms.search.keywords: null
ms.date: 02/28/2022
ms.author: jswymer
---

# Business Central e OneDrive per l'integrazione del business

OneDrive for Business è un servizio di Storage cloud che è incluso in Microsoft 365. [!INCLUDE[prod_short](includes/prod_short.md)] rende facile l'archiviazione, la gestione e la condivisione di file con altre persone attraverso OneDrive. Quando un file è nel tuo OneDrive puoi approfittare delle ricche esperienze collaborative delle versioni online dei prodotti Microsoft, come Word, Excel e PowerPoint. Per esempio, puoi condividere un documento Word, e poi tu e i tuoi colleghi potete modificarlo insieme in tempo reale. OneDrive permette anche di aprire altri tipi di file, come i PDF. 

## Introduzione alle funzionalità di OneDrive

Se usi [!INCLUDE[prod_short](includes/prod_short.md)] online, abbiamo già creato la connessione tra [!INCLUDE[prod_short](includes/prod_short.md)] online e OneDrive, quindi è facile iniziare. L'unico requisito è che gli utenti abbiano aperto OneDrive almeno una volta. Con [!INCLUDE[prod_short](includes/prod_short.md)] in locale, un amministratore deve configurare la connessione prima di poter iniziare. Per ulteriori informazioni, vedi [Gestione dell'integrazione di OneDrive con Business Central](admin-onedrive-integration.md).

<!-- We've created the connection between [!INCLUDE[prod_short](includes/prod_short.md)] online and OneDrive, so it's easy to get started. The only requirement is that users have opened OneDrive at least one time. -->

### Aprire e condividere in OneDrive

Nella maggior parte delle pagine in cui i file sono disponibili, come Report elaborati o i file allegati ai record, troverai le azioni **Apri in OneDrive** e **Condividi**.

:::image type="content" source="media/onedrive-overview-report-inbox-w-outline.png" alt-text="Le azioni Apri in OneDrive e Condividi per i report":::


:::image type="content" source="media/one-drive-attachments-w-outline.png" alt-text="Le azioni Apri in OneDrive e Condividi per gli allegati":::

|Selezionare...|Per...|Ulteriori informazioni...|
|---------|-----|----------------|
|Apri in OneDrive|Copiare il file in una cartella di Business Central nel tuo OneDrive e aprire il file.|[Apri in OneDrive](across-share-onedrive.md#open-in-onedrive) |
|Quota|Copiare il file sul tuo OneDrive e condividerlo con altre persone.|[Condividi in OneDrive](across-share-onedrive.md#share) |

### Salvare le cartelle di lavoro di Excel e i file di report in OneDrive

Con l'impostazione dell'integrazione di OneDrive, un paio di altre funzionalità familiari utilizzeranno automaticamente OneDrive per salvare i file invece di salvare i file sul tuo dispositivo:

- Le azioni **Apri in Excel** e **Modifica in Excel** nelle pagine elenco copieranno automaticamente il file Excel in OneDrive, quindi aprilo in Excel Online. Per ulteriori informazioni, vedi [Visualizzazione e modifica in Excel](across-work-with-excel.md).
- L'invio di un report a un file Excel o Word copierà automaticamente il file in OneDrive, quindi aprilo in Excel o Word online. Per ulteriori informazioni, vedi [Salvataggio di un report in un file](ui-work-report.md#saving-a-report-to-a-file).

Queste funzionalità non sono attivate per impostazione predefinita. Ma come amministratore, puoi facilmente attivarle usando la guida al setup assistito **Setup OneDrive**.

<!--
When you use the **Open in OneDrive** action for the first time, [!INCLUDE[prod_short](includes/prod_short.md)] does the following in your OneDrive:

1. Creates a folder named [!INCLUDE[prod_short](includes/prod_short.md)]. 
2. In the [!INCLUDE[prod_short](includes/prod_short.md)] folder, it creates another folder with the same name as the company you're working in. If you work in more than one company, it will create a folder for the company you're working in when you use the **Open in OneDrive** action. 
3. Puts a copy of the file you selected in the folder, and then opens the file. The next time you use the action, it only copies and opens the file. 

The folder and its content are private until you decide to share them with others. For example, you might decide to share content with one or more of your coworkers, or even people outside of your organization. For more information, see [Share OneDrive files and folders](https://support.microsoft.com/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07) in the content for OneDrive.
-->

> [!NOTE]
> Potete anche collegare il vostro [!INCLUDE[prod_short](includes/prod_short.md)] on-premises a OneDrive. Tuttavia, ci sono alcune cose da fare per farlo funzionare. Per ulteriori informazioni, vedi [Configurazione di Business Central On-Premises](admin-onedrive-integration-onpremises.md).

## Vedere anche

[Gestione dell'integrazione di OneDrive con Business Central](admin-onedrive-integration.md)  
[Apertura dei file di Business Central in OneDrive](across-share-onedrive.md)  
[OneDrive FAQ](admin-onedrive-faq.md)  
