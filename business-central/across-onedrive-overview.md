---
title: Business Central e OneDrive per l'integrazione del business
description: Puoi usare OneDrive for Business per archiviare, gestire e condividere file, come rapporti o allegati.
author: jswymer
ms.topic: overview
ms.workload: na
ms.search.keywords: ''
ms.date: 02/28/2022
ms.author: jswymer
ms.openlocfilehash: 371c090e321992ec2fdc0ee7cb218feaa6b16d9a
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2022
ms.locfileid: "8521230"
---
# <a name="business-central-and-onedrive-for-business-integration"></a>Business Central e OneDrive per l'integrazione del business

OneDrive for Business è un servizio di Storage cloud che è incluso in Microsoft 365. [!INCLUDE[prod_short](includes/prod_short.md)] rende facile l'archiviazione, la gestione e la condivisione di file con altre persone attraverso OneDrive. Quando un file è nel tuo OneDrive puoi godere delle ricche esperienze collaborative delle versioni online dei prodotti Microsoft, come Word, Excel e PowerPoint. Per esempio, puoi condividere un documento Word, e poi tu e i tuoi colleghi potete modificarlo insieme in tempo reale. OneDrive permette anche di aprire altri tipi di file, come i PDF. 

## <a name="getting-started"></a>Introduzione

Abbiamo creato la connessione tra [!INCLUDE[prod_short](includes/prod_short.md)] online e OneDrive, quindi è facile iniziare. L'unico requisito è che gli utenti abbiano aperto OneDrive almeno una volta. 

Nella maggior parte delle pagine in cui i file sono disponibili, come Report elaborati o i file allegati ai record, troverai le azioni **Apri in OneDrive** e **Condividi**.

:::image type="content" source="media/onedrive-overview-report-inbox-w-outline.png" alt-text="Le azioni Apri in OneDrive e Condividi per i report":::


:::image type="content" source="media/one-drive-attachments-w-outline.png" alt-text="Le azioni Apri in OneDrive e Condividi per gli allegati":::

|Selezionare...|Per...|Ulteriori informazioni...|
|---------|-----|----------------|
|Apri in OneDrive|Copiare il file in una cartella di Business Central nel tuo OneDrive e aprire il file.|[Apri in OneDrive](across-share-onedrive.md#open-in-onedrive) |
|Quota|Copiare il file sul tuo OneDrive e condividerlo con altre persone.|[Condividi in OneDrive](across-share-onedrive.md#share) |

<!--
When you use the **Open in OneDrive** action for the first time, [!INCLUDE[prod_short](includes/prod_short.md)] does the following in your OneDrive:

1. Creates a folder named [!INCLUDE[prod_short](includes/prod_short.md)]. 
2. In the [!INCLUDE[prod_short](includes/prod_short.md)] folder, it creates another folder with the same name as the company you're working in. If you work in more than one company, it will create a folder for the company you're working in when you use the **Open in OneDrive** action. 
3. Puts a copy of the file you selected in the folder, and then opens the file. The next time you use the action, it only copies and opens the file. 

The folder and its content are private until you decide to share them with others. For example, you might decide to share content with one or more of your coworkers, or even people outside of your organization. For more information, see [Share OneDrive files and folders](https://support.microsoft.com/en-us/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07).
-->

> [!NOTE]
> Potete anche collegare il vostro [!INCLUDE[prod_short](includes/prod_short.md)] on-premises a OneDrive. Tuttavia, ci sono alcune cose da fare per farlo funzionare. Per ulteriori informazioni, vedere [Configurazione di Business Central On-Premises](admin-onedrive-integration.md#configuring-business-central-on-premises).

## <a name="see-also"></a>Vedere anche
[Gestione dell'integrazione di OneDrive con Business Central](admin-onedrive-integration.md)  
[Apertura dei file di Business Central in OneDrive](across-share-onedrive.md)  
[OneDrive FAQ](admin-onedrive-faq.md)