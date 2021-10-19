---
title: Business Central e OneDrive per l'integrazione del business
description: Puoi usare OneDrive for Business per archiviare, gestire e condividere file, come rapporti o allegati.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: bholtorf
ms.openlocfilehash: 669f3272099057809dcb364d9fc47c0e69b57a4e
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2021
ms.locfileid: "7589463"
---
# <a name="business-central-and-onedrive-for-business-integration"></a>Business Central e OneDrive per l'integrazione del business
OneDrive for Business è un servizio di Storage cloud che è incluso in Microsoft 365. [!INCLUDE[prod_short](includes/prod_short.md)] rende facile l'archiviazione, la gestione e la condivisione di file con altre persone attraverso OneDrive. Quando un file è nel tuo OneDrive puoi godere delle ricche esperienze collaborative delle versioni online dei prodotti Microsoft, come Word, Excel e PowerPoint. Per esempio, puoi condividere un documento Word, e poi tu e i tuoi colleghi potete modificarlo insieme in tempo reale. OneDrive permette anche di aprire altri tipi di file, come i PDF. 

## <a name="getting-started"></a>Introduzione
Abbiamo creato la connessione tra [!INCLUDE[prod_short](includes/prod_short.md)] online e OneDrive, quindi è facile iniziare. L'unico requisito è che gli utenti abbiano aperto OneDrive almeno una volta. 

Nella maggior parte delle pagine in cui i file sono disponibili, come la Report Inbox o i file allegati ai record, troverai un'azione **Apri in OneDrive** .

:::image type="content" source="media/Open in OneDrive.PNG" alt-text="L'azione Apri in OneDrive":::

 
:::image type="content" source="media/OneDrive attachment.PNG" alt-text="Condividere gli allegati dei file in OneDrive":::

Quando usi l'azione **Apri in OneDrive** per la prima volta, [!INCLUDE[prod_short](includes/prod_short.md)] fai quanto segue in OneDrive:

1. Crea una cartella chiamata [!INCLUDE[prod_short](includes/prod_short.md)]. 
2. Nella cartella [!INCLUDE[prod_short](includes/prod_short.md)], crea un'altra cartella con lo stesso nome della società in cui stai lavorando. Se lavori in più di un'azienda, verrà creata una cartella per l'azienda in cui stai lavorando quando usi l'azione **Apri in OneDrive** . 
3. Mette una copia del file selezionato nella cartella e poi apre il file. La prossima volta che usi l'azione, questa copia e apre solo il file. 

La cartella e il suo contenuto sono privati finché non si decide di condividerli con altri. Per esempio, potresti decidere di condividere il contenuto con uno o più dei tuoi colleghi, o anche con persone al di fuori della tua organizzazione. Per maggiori informazioni, vedi [Condividere file e cartelle OneDrive ](https://support.microsoft.com/en-us/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07).

> [!NOTE]
> Potete anche collegare il vostro [!INCLUDE[prod_short](includes/prod_short.md)] on-premises a OneDrive. Tuttavia, ci sono alcune cose da fare per farlo funzionare. Per ulteriori informazioni, vedere [Configurazione di Business Central On-Premises](admin-onedrive-integration.md#configuring-business-central-on-premises).

## <a name="see-also"></a>Vedere anche
[Gestione dell'integrazione di OneDrive con Business Central](admin-onedrive-integration.md)  
[Apertura dei file di Business Central in OneDrive](across-share-onedrive.md)  
[OneDrive FAQ](admin-onedrive-faq.md)