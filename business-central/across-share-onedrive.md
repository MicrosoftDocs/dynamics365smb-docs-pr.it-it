---
title: Apertura dei file di Business Central in OneDrive
description: Scopri come condividere i dati di Business Central tramite OneDrive for Business.
author: jswymer
ms.topic: conceptual
ms.workload: na
ms.search.keywords: null
ms.date: 08/03/2022
ms.author: jswymer
---
# <a name="opening-and-sharing-business-central-files-in-microsoft-onedrive"></a><a name="opening-and-sharing-business-central-files-in-microsoft-onedrive"></a><a name="opening-and-sharing-business-central-files-in-microsoft-onedrive"></a>Apertura e condivisione dei file di Business Central in Microsoft OneDrive

[!INCLUDE[prod_short](includes/prod_short.md)] rende facile archiviare, gestire e condividere i file con altre persone attraverso Microsoft OneDrive for Business. Nella maggior parte delle pagine con file disponibili, come Report elaborati o con file allegati ai record, troverai le azioni **Apri in OneDrive** e **Condividi**.


:::image type="content" source="media/onedrive-overview-report-inbox-w-outline.png" alt-text="Le azioni Apri in OneDrive e Condividi per i report":::


:::image type="content" source="media/one-drive-attachments-w-outline.png" alt-text="Le azioni Apri in OneDrive e Condividi per gli allegati":::


## <a name="open-in-onedrive"></a><a name="open-in-onedrive"></a><a name="open-in-onedrive"></a>Apri in OneDrive

L'azione **Apri in OneDrive** copia il file nel tuo OneDrive e apre il file nelle applicazioni online, come Microsoft Excel online, Microsoft Word online, o Microsoft PowerPoint online. 

<!--## Working with different types of files-->

Quando scegli **Apri in OneDrive**, [!INCLUDE[prod_short](includes/prod_short.md)] identifica i file Excel, Word e PowerPoint e li apre nelle loro applicazioni online, cioè Excel online, Word online e PowerPoint online. 

Utilizzando le versioni online di queste applicazioni, puoi annotare, modificare e collaborare con altri senza uscire dal browser.

Per altri tipi di file popolari, come PDF, file di testo e immagini, OneDrive fornisce visualizzatori di file che offrono funzioni per la stampa, la condivisione e altro. Se un file non può essere visualizzato in OneDrive, potrebbe essere richiesto di scaricarlo.

## <a name="share"></a><a name="share"></a><a name="share"></a>Condividi

L'azione **Condividi** copia il file nel tuo OneDrive così puoi vedere con chi l'hai già condiviso e condividere il file con altre persone. Quando selezioni l'azione **Condividi** si apre la pagina seguente.

:::image type="content" source="media/share-to-onedrive-dialog-v2.PNG" alt-text="Condividi file in OneDrive":::

Se hai familiarità con OneDrive, potresti riconoscere la pagina illustrata sopra. Vedrai due opzioni per condividere il file: **Invia collegamento** e **Copia collegamento**.

- **Invia collegamento** ti permette di condividere i file con persone specifiche. Le persone con cui condividi il file riceveranno un'e-mail con un collegamento al file. Il file apparirà anche nella sezione **Condiviso** di OneDrive. Inizia digitando gli indirizzi e-mail o i nomi dei contatti nel campo **nome, gruppo o indirizzo e-mail**. Includi un messaggio sotto il campo **nome, gruppo o e-mail**, se vuoi.

  > [!TIP]
  > Se vuoi comporre il tuo messaggio in Outlook, seleziona il pulsante **Outlook**. Il collegamento verrà inserito in una bozza di e-mail e tutti quelli con cui hai inserito per condividere saranno presenti nell'elenco **A**. Con questa opzione, puoi creare e-mail utilizzando tutte le funzionalità di Outlook, inclusa la formattazione del testo, l'aggiunta di altri allegati, l'inserimento di immagini o tabelle e l'aggiunta di destinatari CC o CCN.

- **Copia collegamento** copia un collegamento al file che puoi utilizzare per condividere il file tramite applicazioni come Facebook, Twitter o e-mail. 

Prima di inviare o copiare il collegamento di un file, imposta il livello di autorizzazione che desideri abbiano le persone. Puoi vedere l'impostazione corrente sotto **Invia collegamento** o **Copia collegamento**. Nella maggior parte dei casi, sarà **Chiunque abbia il collegamento può modificare**, a seconda delle impostazioni dell'amministratore. Per modificare i permessi, seleziona il collegamento e apporta le modifiche nella pagina **Impostazioni collegamento**.

La funzionalità di condivisione in Business Central si basa su OneDrive. Per ulteriori informazioni sulla condivisione e sulle autorizzazioni di OneDrive, vedi [Condividere file e cartelle OneDrive](https://support.microsoft.com/en-us/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07).

> [!NOTE]
> L'azione **Condividi** non è disponibile nell'app Business Central per dispositivi mobili.

## <a name="first-time-sign-in-from-business-central"></a><a name="first-time-sign-in-from-business-central"></a><a name="first-time-sign-in-from-business-central"></a>Primo accesso da Business Central

Quando usi l'azione **Apri in OneDrive** o **Condividi** per la prima volta, [!INCLUDE[prod_short](includes/prod_short.md)] effettua le seguenti operazioni:

1. Apre la pagina **Esaminare le condizioni**. Leggi la pagina e, se sei d'accordo con le condizioni, seleziona **Accetto** e continua.
2. Crea una cartella chiamata [!INCLUDE[prod_short](includes/prod_short.md)] in OneDrive. 
3. Nella cartella [!INCLUDE[prod_short](includes/prod_short.md)], crea una cartella con lo stesso nome della società in cui stai lavorando. Se lavori in più di un'azienda, [!INCLUDE[prod_short](includes/prod_short.md)] crea una cartella per ogni azienda in cui stai lavorando quando usi le azioni **Apri in OneDrive** o **Condividi**. 
4. Mette una copia del file selezionato nella cartella con il nome della società e poi apre il file. 

La prossima volta che usi l'azione **Apri in OneDrive** o **Condividi**, [!INCLUDE[prod_short](includes/prod_short.md)] copia e apre solo il file. 

## <a name="managing-multiple-copies-of-a-file"></a><a name="managing-multiple-copies-of-a-file"></a><a name="managing-multiple-copies-of-a-file"></a>Gestione di più copie di un file

Quando scegli **Apri in OneDrive** o **Condividi**, il file viene copiato da [!INCLUDE[prod_short](includes/prod_short.md)] nella cartella in OneDrive. Se modifichi il file in OneDrive, questo file sarà diverso dal file [!INCLUDE[prod_short](includes/prod_short.md)]. Per aggiornare [!INCLUDE[prod_short](includes/prod_short.md)] con la versione più recente del file, rimuovi il file esistente da [!INCLUDE[prod_short](includes/prod_short.md)] e poi carica la copia più recente.

Se esiste già un file con lo stesso nome in OneDrive, ti verranno offerte le seguenti scelte:

- **Utilizza esistente**

  Questa opzione apre o condivide il file che è già archiviato in OneDrive, invece di copiare il file da Business Central.
  
- **Sostituisci**
  
  Questa opzione sostituisce il file esistente in OneDrive con il file selezionato da Business Central. Il file originale non va perso, puoi vederlo e ripristinarlo usando la cronologia delle versioni in OneDrive. Per ulteriori informazioni, vedi [Ripristinare una versione precedente di un file archiviato in OneDrive](https://support.microsoft.com/office/restore-a-previous-version-of-a-file-stored-in-onedrive).

- **Mantieni entrambi**
 
  Questa opzione mantiene il file esistente così com'è e salva il file selezionato da Business Central con un nome diverso. Il nuovo nome è simile al nome esistente, tranne che con un numero di suffisso come "Elementi (2).xlsx".

## <a name="about-your-business-central-folder-on-onedrive"></a><a name="about-your-business-central-folder-on-onedrive"></a><a name="about-your-business-central-folder-on-onedrive"></a>Informazioni sulla cartella Business Central in OneDrive

La cartella e il suo contenuto sono privati finché non si decide di condividerli con altri. Potresti decidere di condividere il contenuto con uno o più dei tuoi colleghi, o anche con persone al di fuori della tua organizzazione. 

Puoi accedere al tuo OneDrive dalla pagina **Le mie impostazioni** scegliendo il link nel campo **Storage cloud** . Per ulteriori informazioni, vedi [Condividere file e cartelle OneDrive](https://support.microsoft.com/en-us/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07).

:::image type="content" source="media/my-settings-cloud-storage.PNG" alt-text="Il campo Storage cloud in Le mie impostazioni":::

<!--## Extending the Connection to OneDrive
You can create an extension and connect it to... For more information, see...-->

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Vedere anche

[Business Central e integrazione OneDrive](across-onedrive-overview.md)  
[Gestione dell'integrazione di OneDrive con Business Central](admin-onedrive-integration.md)  
[OneDrive FAQ](admin-onedrive-faq.md)
