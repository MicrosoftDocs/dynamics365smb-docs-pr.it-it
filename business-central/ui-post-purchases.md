---
title: Informazioni sulle modalità di registrazione dei documenti di acquisto | Documenti Microsoft
description: Informazioni sulle diverse funzioni di registrazione per i documenti di acquisto.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2019
ms.author: solsen
ms.openlocfilehash: cc3d2e5b0f3425c329e5567e7d00908cb7f5c7d5
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2019
ms.locfileid: "922817"
---
# <a name="posting-purchases"></a>Registrazione di acquisti
Nella **Categoria registrazione** in un documento di acquisto, è possibile scegliere tra le seguenti funzioni di registrazione:

* **Registra**
* **Anteprima registrazione**
* **Registra e stampa**
* **Report test**
* **Registra batch**

Una volta completate le righe e immesse tutte le informazioni nell'ordine di acquisto, è possibile registrarlo, ovvero creare una ricezione e una fattura.

Quando un ordine di acquisto viene registrato, il conto del fornitore, la contabilità generale e i movimenti contabili articoli vengono aggiornati.

Per ciascun ordine di acquisto viene creato un movimento di acquisto nella tabella **Movimenti C/G**. Vengono inoltre creati un movimento nel conto del fornitore nella tabella **Mov. contabili fornitori** e un movimento C/G nel relativo conto passività verso il fornitore. Infine, la registrazione dell'ordine potrebbe generare un movimento IVA e un movimento C/G relativi all'importo dello sconto. La registrazione di un movimento relativo allo sconto dipende dal contenuto del campo **Registrazione Sconti** nella pagina **Setup contabilità fornitori**.

Per ciascuna riga dell'ordine di acquisto, verrà creato un movimento contabile articolo nella tabella **Mov. contabili articoli** (se le righe di acquisto contengono numeri di articoli) o verrà creato un movimento C/G nella tabella **Movimento C/G** (se le righe di acquisto contengono un conto C/G). Inoltre, gli ordini di acquisto vengono sempre registrati nelle tabelle **Testata carico acq.** e **Testate fatt. acq**.

Prima di avviare la registrazione, è possibile stampare un report di test in cui sono indicate tutte le informazioni contenute nell'ordine di acquisto, insieme a eventuali errori. Per stampare il report, scegliere **Registrazione**, quindi **Report test**.

> [!IMPORTANT]  
>   Quando si registra un ordine, è possibile creare sia un carico che una fattura. Ciò può avvenire in modo simultaneo oppure indipendente. Prima di effettuare la registrazione, è inoltre possibile creare una ricevuta parziale e una fattura parziale immettendo le necessarie informazioni nei campi **Qtà da ricevere** e **Qtà da fatturare** delle singole righe dell'ordine di acquisto. Si tenga presente che non è possibile creare una fattura per un articolo che non è stato ricevuto. Questo significa che è necessario registrare una ricezione prima di emettere una fattura oppure la ricezione e la fattura devono essere contemporanee.

È possibile effettuare la registrazione oppure effettuare la registrazione e stampare. Quando si seleziona Registra e stampa, viene stampato un report al momento della registrazione dell'ordine. È inoltre possibile scegliere la funzione **Registra batch** che consente di registrare più ordini contemporaneamente.

Una volta completata la registrazione, le righe di acquisto registrate vengono rimosse dall'ordine. Un messaggio avviserà l'utente che la registrazione è completata. Dopodiché sarà possibile visualizzare i movimenti registrati nelle varie pagine che contengono movimenti registrati, come ad esempio le pagine **Movimenti contabili fornitori**, **Movimenti C/G**, **Mov. contabili articoli**, **Ricezioni acquisti** e **Fatture acquisto registrate**.

## <a name="see-also"></a>Vedi anche
[Acquisti](purchasing-manage-purchasing.md)  
[Contabilizzare documenti e registrazioni](ui-post-documents-journals.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

