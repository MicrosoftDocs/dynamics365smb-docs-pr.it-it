---
title: Archiviare documenti di vendita e acquisto
description: Puoi archiviare ordini di acquisto e vendita, offerte, ordini di reso e ordini programmati in modo da poter utilizzare il documento archiviato per ricreare il documento da cui è stato archiviato.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 42, 49, 50, 459, 460, 5159, 5162, 5164, 5167, 6627, 6630, 6644, 9305, 9306, 9346, 9347, 9348, 9349
ms.date: 06/29/2021
ms.author: edupont
ms.openlocfilehash: dcb99e2c1231e95fca2eb9f8c36fc363a193cd82
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2022
ms.locfileid: "8141627"
---
# <a name="archive-documents"></a>Archiviare documenti
È possibile archiviare ordini di vendita e acquisto, offerte, ordini di reso e ordini programmati, ad esempio perché si desidera salvare una copia di un documento per il riutilizzo in seguito. È possibile archiviare documento di acquisto o vendita più di uno volta, salvando ogni volta una versione archiviata diversa.

Per i documenti di vendita archiviati di cui l'originale esiste ancora e non è registrato, puoi utilizzare la funzione **Ripristina** per sovrascrivere l'originale con la versione archiviata del documento. Ciò si rivela particolarmente utile se è necessario ripristinare il contenuto di un documento a uno stato precedente.

Per i documenti archiviati di cui l'originale è stato eliminato, è possibile riutilizzare il contenuto solo copiando i dati, ad esempio con la funzione **Copia da documento**.  

## <a name="to-set-up-automatic-document-archiving"></a>Per impostare l'archiviazione automatica dei documenti

È possibile impostare l'archiviazione automatica di documenti di vendita e di acquisto, offerte, ordini programmati e ordini di reso, prima di eliminarli.

La procedura seguente illustra come configurare l'archiviazione automatica di documenti di vendita. I passaggi sono simili per i documenti di acquisto.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup contabilità clienti**, quindi scegli il collegamento correlato.
2. Nella pagina **Setup contabilità clienti e vendite** compila i campi. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

In particolare per il campo **Archivia offerte**, la tabella seguente illustra la differenza tra le opzioni.

|Opzione|Descrizione|
|------|-----------|
|**Mai**| Non archiviare mai offerte di vendita quando vengono eliminate.|
|**Domanda**|Selezionare per chiedere all'utente di scegliere se archiviare le offerte di vendita quando vengono eliminate.|
|**Sempre**|Selezionare per archiviare automaticamente le offerte di vendita quando vengono eliminate.|

## <a name="to-archive-a-sales-order"></a>Per archiviare un ordine di vendita

Di seguito viene descritto come archiviare un ordine di vendita. I passaggi sono simili per tutti gli ordini, gli ordini programmati, gli ordini di reso e le offerte.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ordini vendita**, quindi seleziona il collegamento correlato.  
2. Aprire un ordine di vendita da archiviare.  
3. Scegliere l'azione **Archivia documento**.

L'ordine di vendita è archiviato. È possibile visualizzarlo nella pagina **Ordine vendite archiviato**.

## <a name="to-restore-a-non-posted-sales-order-from-the-archive"></a>Per ripristinare un ordine di vendita non registrato dall'archivio

Di seguito viene descritto come ripristinare il contenuto di un ordine di vendita archiviato nell'ordine di vendita originale. Questa operazione è possibile soltanto quando il documento originale non è stato registrato. I passaggi sono simili per tutti gli ordini, gli ordini programmati, gli ordini di reso e le offerte.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Archivi ordini vendita**, quindi seleziona il collegamento correlato.
2. Selezionare l'ordine di vendita archiviato, o una versione dello stesso, che si intende ripristinare, quindi scegliere **Ripristina**.  

Il contenuto dell'ordine di vendita originale viene sostituito con quello della versione archiviata selezionata.

## <a name="to-delete-archived-sales-orders"></a>Per eliminare ordini di vendita archiviati

Di seguito viene descritto come eliminare ordini di vendita archiviati. I passaggi sono simili per altri altri documenti di acquisto e vendita archiviati.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Archivi ordini vendita**, quindi seleziona il collegamento correlato.  
2. Scegli l'azione **Elimina versioni ordine vendita archiviate**, e poi, nella pagina **Elimina versioni ordine vendita archiviate**, seleziona i filtri appropriati.  
3. Scegliere il pulsante **OK**.

## <a name="see-also"></a>Vedi anche

[Tenere traccia delle righe dei documenti](across-how-to-track-document-lines.md)  
[Vendite](sales-manage-sales.md)  
[Funzionalità aziendali generali](ui-across-business-areas.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
