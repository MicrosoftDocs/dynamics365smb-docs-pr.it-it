---
title: Apertura dei file di Business Central in OneDrive
description: Scopri come condividere i dati di Business Central tramite OneDrive for Business.
author: jswymer
ms.topic: conceptual
ms.workload: na
ms.search.keywords: ''
ms.date: 02/28/2022
ms.author: jswymer
ms.openlocfilehash: 2e1cc04d265541c87244dcd6c13b14327f07cc2f
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2022
ms.locfileid: "8516423"
---
# <a name="opening-and-sharing-business-central-files-in-onedrive"></a>Apertura e condivisione dei file di Business Central in OneDrive

[!INCLUDE[prod_short](includes/prod_short.md)] rende facile archiviare, gestire e condividere i file con altre persone attraverso OneDrive for Business. Nella maggior parte delle pagine in cui i file sono disponibili, come Report elaborati o i file allegati ai record, troverai le azioni **Apri in OneDrive** e **Condividi**.


:::image type="content" source="media/onedrive-overview-report-inbox-w-outline.png" alt-text="Le azioni Apri in OneDrive e Condividi per i report":::


:::image type="content" source="media/one-drive-attachments-w-outline.png" alt-text="Le azioni Apri in OneDrive e Condividi per gli allegati":::

<!--
:::image type="content" source="media/Open in OneDrive.PNG" alt-text="The Open in OneDrive action":::

 
:::image type="content" source="media/OneDrive attachment.PNG" alt-text="Share file attachments in OneDrive":::
-->

## <a name="open-in-onedrive"></a>Apri in OneDrive

L'azione **Apri in OneDrive** copia il file nel tuo OneDrive e apre il file nelle applicazioni online, come Excel online, Word online e PowerPoint online. 

<!--## Working with Different Types of Files-->

Quando scegli **Apri in OneDrive**, [!INCLUDE[prod_short](includes/prod_short.md)] identifica i file Excel, Word e PowerPoint e li apre nelle loro applicazioni online, cioè Excel online, Word online e PowerPoint online. Puoi annotare, modificare e collaborare con gli altri senza lasciare il browser.

Per altri tipi di file popolari, come PDF, file di testo e immagini, OneDrive fornisce visualizzatori di file che offrono funzioni per la stampa, la condivisione e altro. Se un file non può essere visualizzato in OneDrive, potrebbe essere richiesto di scaricarlo.

## <a name="share"></a>Quota

L'azione **Condividi** copia il file nel tuo OneDrive e ti permette di condividere il file con altre persone e vedere con chi hai già condiviso il file. Quando selezioni l'azione **Condividi** si apre la pagina seguente.

:::image type="content" source="media/share-to-onedrive-dialog.PNG" alt-text="Condividi file in OneDrive":::

Se hai familiarità con OneDrive, potresti riconoscere la pagina. Hai due opzioni per condividere il file: **Invia collegamento** e **Copia collegamento**.

- **Invia collegamento** ti permette di condividere i file con persone specifiche. Le persone con cui condividi il file riceveranno un'e-mail con un collegamento al file. Il file apparirà anche nella sezione **Condiviso** di OneDrive. Inizia digitando gli indirizzi e-mail o i nomi dei contatti nel campo **nome, gruppo o indirizzo e-mail**.

- **Copia collegamento** copia un collegamento al file sul tuo OneDrive in modo che puoi usarlo in altri posti come Facebook, Twitter o e-mail. 

Prima di inviare o copiare il collegamento, imposta l'autorizzazione sul file che desideri condividere con le persone. Puoi vedere l'impostazione corrente sotto **Invia collegamento** e **Copia collegamento**. Nella maggior parte dei casi, sarà **Chiunque abbia il collegamento può modificare per aprire il collegamento**, a seconda delle impostazioni impostate dall'amministratore. Per modificare i permessi, seleziona il collegamento e apporta le modifiche nella pagina **Impostazioni collegamento**.

La funzionalità di condivisione in Business Central si basa su OneDrive. Quindi, per ulteriori informazioni sulla condivisione e sulle autorizzazioni, vedi [Condividere file e cartelle OneDrive](https://support.microsoft.com/en-us/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07).

> [!NOTE]
> L'azione **Condividi** non è disponibile nell'app Business Central per dispositivi mobili.

## <a name="first-time-sign-in-from-business-central"></a>Primo accesso da Business Central

Quando usi l'azione **Apri in OneDrive** o **Condividi** per la prima volta, [!INCLUDE[prod_short](includes/prod_short.md)] effettua le seguenti operazioni:

1. Apre la pagina **Esaminare le condizioni**. Leggi la pagina e, se sei d'accordo con le condizioni, seleziona **Accetto** e continua.
2. Apre la pagina **Scegli un account**, seleziona il tuo account o **usa un altro account** se non vedi il tuo, quindi inserisci il nome utente e la password quando richiesto.
3. Crea una cartella chiamata [!INCLUDE[prod_short](includes/prod_short.md)] in OneDrive. 
4. Nella cartella [!INCLUDE[prod_short](includes/prod_short.md)], crea un'altra cartella con lo stesso nome della società in cui stai lavorando. Se lavori in più di un'azienda, verrà creata una cartella per l'azienda in cui stai lavorando quando usi le azioni **Apri in OneDrive** e **Condividi**. 
5. Mette una copia del file selezionato nella cartella e poi apre il file. La prossima volta che usi l'azione, questa copia e apre solo il file. 

## <a name="managing-multiple-copies-of-a-file"></a>Gestione di più copie di un file

Quando scegli **Apri in OneDrive** o **Condividi**, il file viene copiato da [!INCLUDE[prod_short](includes/prod_short.md)] nella cartella in OneDrive. Se si modifica il file in OneDrive, le copie del file saranno diverse. Per aggiornare [!INCLUDE[prod_short](includes/prod_short.md)] con il file più recente, rimuovere il file esistente da [!INCLUDE[prod_short](includes/prod_short.md)] e poi caricare la copia più recente.

Inoltre, quando esiste già un file con lo stesso nome in OneDrive, [!INCLUDE[prod_short](includes/prod_short.md)] fornirà la possibilità di sostituire il file o di conservare entrambi i file. Se scegli di conservare entrambi i file, il nuovo file viene copiato in OneDrive con un nome file con suffisso di numero, come "Items (2).xlsx". Il file originale non viene modificato. 

Se scegli di sostituire il file, il nuovo file viene aggiunto alla cronologia delle versioni per quel file. Il file originale non viene perso, ed è possibile visualizzare o ripristinare le versioni precedenti del file. 

## <a name="about-your-business-central-folder-on-onedrive"></a>Informazioni sulla cartella Business Central in OneDrive

La cartella e il suo contenuto sono privati finché non si decide di condividerli con altri. Per esempio, potresti decidere di condividere il contenuto con uno o più dei tuoi colleghi, o anche con persone al di fuori della tua organizzazione. Puoi accedere al tuo OneDrive dalla pagina **Le mie impostazioni** scegliendo il link nel campo **Storage cloud** . Per maggiori informazioni, vedi [Condividere file e cartelle OneDrive ](https://support.microsoft.com/en-us/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07).

:::image type="content" source="media/my-settings-cloud-storage.PNG" alt-text="Il campo Storage cloud in Le mie impostazioni":::

<!--## Extending the Connection to OneDrive
You can create an extension and connect it to... For more information, see...-->

## <a name="see-also"></a>Vedere anche
[Business Central e OneDrive Integrazione](across-onedrive-overview.md)  
[Gestione dell'integrazione di OneDrive con Business Central](admin-onedrive-integration.md)  
[OneDrive FAQ](admin-onedrive-faq.md)