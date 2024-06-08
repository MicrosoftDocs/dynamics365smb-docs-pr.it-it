---
title: Archiviare documenti di vendita e acquisto
description: 'È possibile archiviare ordini di vendita e di acquisto, offerte, ordini di reso e ordini programmati.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 02/26/2024
ms.custom: bap-template
ms.search.form: '42, 49, 50, 459, 460, 5159, 5162, 5164, 5167, 6627, 6630, 6644, 9305, 9306, 9346, 9347, 9348, 9349'
ms.service: dynamics-365-business-central
---
# <a name="archive-documents"></a>Archiviare i documenti

È possibile archiviare ordini di vendita e di acquisto, offerte, ordini di reso e ordini programmati. Se utilizzi le funzionalità di Gestione progetti, puoi anche archiviare i tuoi progetti. Puoi archiviare documenti e progetti più volte e ogni volta viene salvata una versione archiviata diversa.

Per i documenti di vendita, se l'originale esiste ancora e non è registrato, puoi utilizzare l'azione **Ripristina** per sovrascriverlo con una versione archiviata. 

> [!NOTE]
> Puoi ripristinare solo documenti e progetti di vendita. L'azione non è disponibile per i documenti di acquisto archiviati.

Per i documenti archiviati di cui l'originale è stato eliminato, puoi riutilizzare il contenuto copiando i dati, ad esempio con l'azione **Copia da documento**.  

## <a name="to-set-up-automatic-document-archiving"></a>Per impostare l'archiviazione automatica dei documenti

Puoi automatizzare l'archiviazione per creare una nuova versione del documento archiviato quando qualcuno esegue le seguenti operazioni:

* Modifica o elimina un documento o un progetto.
* Stampa, scarica o invia un documento tramite e-mail.
* Converte un'offerta in un ordine o fattura.
* Registra un ordine.

I passaggi seguenti descrivono come impostare l'archiviazione automatica dei documenti di vendita dalla pagina **Setup contabilità clienti**. I passaggi sono simili per i progetti e i documenti di acquisto. Per i documenti di acquisto, utilizza la pagina **Contabilità fornitori e acquisti**. Per i progetti, utilizza la pagina **Setup progetto**.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup contabilità clienti**, quindi scegli il collegamento correlato.
2. Sulla scheda dettaglio **Archiviazione** specifica se attivare l'archiviazione automatica per le varie tipologie di documenti di vendita. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

Nella seguente tabella vengono illustrate le opzioni per il campo **Archivia offerte**.

|Opzione|Descrizione|
|------|-----------|
|**Mai**| Non archiviare mai offerte di vendita quando vengono eliminate.|
|**Domanda**|Chiedi all'utente di scegliere se archiviare le offerte di vendita quando vengono eliminate.|
|**Sempre**|Archivia automaticamente le offerte di vendita quando vengono eliminate.|

## <a name="to-manually-archive-a-sales-order"></a>Per archiviare manualmente un ordine di vendita

Di seguito viene descritto come archiviare manualmente un ordine di vendita. I passaggi sono simili per tutti i documenti e i progetti che puoi archiviare.

1. Scegli l'icona ![lampadina che apre la funzionalità Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ordini vendita**, quindi seleziona il collegamento correlato.  
2. Aprire un ordine di vendita da archiviare.  
3. Scegliere l'azione **Archivia documento**.

L'ordine di vendita è archiviato. È possibile visualizzarlo nella pagina **Ordine vendite archiviato**.

## <a name="to-restore-a-non-posted-sales-document-or-a-project-from-the-archive"></a>Per ripristinare un progetto o un documento di vendita non registrato dall'archivio

Di seguito viene descritto come ripristinare un ordine di vendita archiviato nell'ordine di vendita originale. Il ripristino di un documento è possibile soltanto quando il documento originale non è registrato. I passaggi sono simili per tutti gli ordini, gli ordini programmati, gli ordini di reso e le offerte, nonché i progetti.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Archivi ordini vendita**, quindi seleziona il collegamento correlato.
2. Selezionare l'ordine di vendita archiviato, o una versione dello stesso, che si intende ripristinare, quindi scegliere **Ripristina**.  

Il contenuto dell'ordine di vendita originale o del progetto viene sostituito con la versione archiviata.

## <a name="to-delete-archived-versions"></a>Per eliminare le versioni archiviate

Utilizza criteri di conservazione per pulire le versioni archiviate di cui non hai più bisogno. I criteri di conservazione consentono agli amministratori di definire per quanto tempo desiderano archiviare i dati. Ad esempio, possono impostare un criterio che elimina i dati dopo una data di scadenza. Per altre informazioni, vedi [Definire i criteri di conservazione](admin-data-retention-policies.md).

Ci sono alcune cose da prendere in considerazione in relazione alla creazione di criteri di conservazione per progetti e documenti archiviati:

* Se il documento originale non è stato eliminato, [!INCLUDE [prod_short](includes/prod_short.md)] non eliminerà le versioni archiviate. Le versioni archiviate non scadranno finché esiste l'originale.
* Quando configuri i criteri di conservazione, puoi specificare che vuoi che i criteri eliminino tutte le versioni archiviate tranne la più recente. Ad esempio, potresti avere 10 versioni e voler conservare una copia dell'ultima. 
* [!INCLUDE [prod_short](includes/prod_short.md)] calcola la data di scadenza dei documenti in base alla data della versione archiviata più recente.

## <a name="see-also"></a>Vedi anche

[Tracciare le righe documento](across-how-to-track-document-lines.md)  
[Vendite](sales-manage-sales.md)  
[Funzionalità aziendali generali](ui-across-business-areas.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
