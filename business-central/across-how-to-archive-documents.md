---
title: Archiviare documenti di vendita e acquisto
description: 'Puoi archiviare ordini di vendita e di acquisto, offerte, ordini di reso e ordini programmati e ripristinare gli originali se necessario.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 06/02/2023
ms.custom: bap-template
ms.search.form: '42, 49, 50, 459, 460, 5159, 5162, 5164, 5167, 6627, 6630, 6644, 9305, 9306, 9346, 9347, 9348, 9349'
---
# <a name="archive-documents"></a>Archiviare documenti

È possibile archiviare ordini di vendita e di acquisto, offerte, ordini di reso e ordini programmati. L'archiviazione dei documenti consente di ripristinare l'originale, se necessario. È possibile archiviare documento di acquisto o vendita più di uno volta, salvando ogni volta una versione archiviata diversa.

Per i documenti di vendita archiviati di cui l'originale esiste ancora e non è registrato, puoi utilizzare l'azione **Ripristina** per sovrascrivere il documento corrente con la versione archiviata.

Per i documenti archiviati di cui l'originale è stato eliminato, è possibile riutilizzare il contenuto solo copiando i dati, ad esempio con l'azione **Copia da documento**.  

## <a name="to-set-up-automatic-document-archiving"></a>Per impostare l'archiviazione automatica dei documenti

È possibile impostare l'archiviazione automatica di documenti di vendita e di acquisto, offerte, ordini programmati e ordini di reso. Quando l'archiviazione automatica è attiva, viene creata una nuova versione del documento archiviato quando qualcuno esegue le seguenti operazioni:

* Modifica o elimina un documento.
* Stampa, scarica o invia un documento tramite e-mail.
* Converte un'offerta in un ordine o fattura.
* Registra un ordine.

La procedura seguente illustra come configurare l'archiviazione automatica di documenti di vendita. I passaggi sono simili per i documenti di acquisto.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup contabilità clienti**, quindi scegli il collegamento correlato.
2. Sulla scheda dettaglio **Archiviazione** specifica se attivare l'archiviazione automatica per le varie tipologie di documenti di vendita. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

Nella seguente tabella vengono illustrate le opzioni per il campo **Archivia offerte**.

|Opzione|Descrizione|
|------|-----------|
|**Mai**| Non archiviare mai offerte di vendita quando vengono eliminate.|
|**Domanda**|Chiedi all'utente di scegliere se archiviare le offerte di vendita quando vengono eliminate.|
|**Sempre**|Archivia automaticamente le offerte di vendita quando vengono eliminate.|

## <a name="to-manually-archive-a-sales-order"></a>Per archiviare manualmente un ordine di vendita

Di seguito viene descritto come archiviare manualmente un ordine di vendita. I passaggi sono simili per tutti gli ordini, gli ordini programmati, gli ordini di reso e le offerte.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ordini vendita**, quindi seleziona il collegamento correlato.  
2. Aprire un ordine di vendita da archiviare.  
3. Scegliere l'azione **Archivia documento**.

L'ordine di vendita è archiviato. È possibile visualizzarlo nella pagina **Ordine vendite archiviato**.

## <a name="to-restore-a-non-posted-sales-order-from-the-archive"></a>Per ripristinare un ordine di vendita non registrato dall'archivio

Di seguito viene descritto come ripristinare un ordine di vendita archiviato nell'ordine di vendita originale. Il ripristino di un documento è possibile soltanto quando il documento originale non è stato registrato. I passaggi sono simili per tutti gli ordini, gli ordini programmati, gli ordini di reso e le offerte.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Archivi ordini vendita**, quindi seleziona il collegamento correlato.
2. Selezionare l'ordine di vendita archiviato, o una versione dello stesso, che si intende ripristinare, quindi scegliere **Ripristina**.  

Il contenuto dell'ordine di vendita originale viene sostituito con quello della versione archiviata.

## <a name="to-delete-archived-sales-orders"></a>Per eliminare ordini di vendita archiviati

Utilizza criteri di conservazione per pulire i documenti archiviati di cui non hai più bisogno. I criteri di conservazione consentono agli amministratori di definire per quanto tempo desiderano archiviare i dati. Ad esempio, possono impostare un criterio che elimina i dati dopo una data di scadenza. Per ulteriori informazioni, vedere [Definire i criteri di conservazione](admin-data-retention-policies.md).

Ci sono alcune cose da prendere in considerazione in relazione alla creazione di criteri di conservazione per documenti archiviati:

* *Se il documento originale non è stato eliminato, Business Central non eliminerà le versioni archiviate. Le versioni archiviate non scadranno finché esiste l'originale.
* Quando configuri i criteri di conservazione, puoi specificare che vuoi che il criterio elimini tutte le versioni archiviate di un documento tranne la più recente. Ad esempio, potresti avere 10 versioni di un documento e voler conservare una copia dell'ultima. 
* Business Central calcola la data di scadenza dei documenti in base alla data della versione archiviata più recente.

## <a name="see-also"></a>Vedi anche

[Tracciare le righe documento](across-how-to-track-document-lines.md)  
[Vendite](sales-manage-sales.md)  
[Funzionalità aziendali generali](ui-across-business-areas.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
