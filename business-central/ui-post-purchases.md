---
title: Informazioni sulle modalità di registrazione dei documenti di acquisto | Documenti Microsoft
description: Informazioni sulle diverse funzioni di registrazione per registrare documenti di acquisto e sul modo in cui aggiornare documenti registrati.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: bd22d29f82c1cfe1ac5e998f131c20cc2e288085
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "3781256"
---
# <a name="posting-purchases"></a>Registrazione di acquisti
In un documento di acquisto, è possibile scegliere tra le seguenti azioni di registrazione:

* **Registra**
* **Anteprima registrazione**
* **Registra e stampa**
* **Report test**
* **Registra batch**

Quando un documento di acquisto viene registrato, il conto del fornitore, la contabilità generale e i movimenti contabili risorse vengono aggiornati.

Per ciascun documento di acquisto viene creato un movimento di acquisto nella tabella **Movimenti C/G**. Vengono inoltre creati un movimento nel conto del fornitore nella tabella **Mov. contabili fornitori** e un movimento C/G nel relativo conto passività verso il fornitore. Infine, la registrazione dell'acquisto potrebbe generare un movimento IVA e un movimento C/G relativi all'importo dello sconto. La registrazione di un movimento relativo allo sconto dipende dal contenuto del campo **Registrazione Sconti** nella pagina **Setup contabilità fornitori**.

Per ogni riga di acquisto, verranno create le seguenti voci:
- Una voce nella tabella **Movimento contabile articolo** se la riga di acquisto è di tipo **Articolo**.
- Una voce nella tabella **Movimento C/G** se le righe di acquisto sono di tipo **Conto G/C**.
- Una voce nella tabella **Movimento contabile risorsa** se la riga di acquisto è di tipo **Risorsa**.

Inoltre, i documenti di acquisto vengono sempre registrati nelle tabelle **Testata carico acq.** e **Testate fatt. acq**.

Prima di avviare la registrazione, è possibile stampare un report di test in cui sono indicate tutte le informazioni contenute nell'ordine di acquisto, insieme a eventuali errori. Per stampare il report, scegliere **Registrazione**, quindi **Report test**.

> [!IMPORTANT]  
>   Quando si registra un ordine acquisto per gli articoli, è possibile creare sia un carico che una fattura. Ciò può avvenire in modo simultaneo oppure indipendente. Prima di effettuare la registrazione, è inoltre possibile creare una ricevuta parziale e una fattura parziale immettendo le necessarie informazioni nei campi **Qtà da ricevere** e **Qtà da fatturare** delle singole righe dell'ordine di acquisto. Si tenga presente che non è possibile creare una fattura per un articolo che non è stato ricevuto. Questo significa che è necessario registrare una ricezione prima di emettere una fattura oppure la ricezione e la fattura devono essere contemporanee.

È possibile effettuare la registrazione oppure effettuare la registrazione e stampare. Quando si seleziona Registra e stampa, viene stampato un report al momento della registrazione dell'ordine. È inoltre possibile scegliere la funzione **Registra batch** che consente di registrare più ordini contemporaneamente. Per ulteriori informazioni, vedere [Pubblicare più documenti contemporaneamente](ui-batch-posting.md).

## <a name="viewing-ledger-entries"></a>Visualizzazione di movimenti contabili
Una volta completata la registrazione, le righe di acquisto registrate vengono rimosse dall'ordine. Un messaggio avviserà l'utente che la registrazione è completata. Dopodiché sarà possibile visualizzare i movimenti registrati nelle varie pagine che contengono movimenti registrati, come ad esempio le pagine **Movimenti contabili fornitori**, **Movimenti C/G**, **Mov. contabili articoli**, **Movimenti contabili risorse**, **Ricezioni acquisti** e **Fatture acquisto registrate**.

Nella maggior parte dei casi, è possibile aprire i movimenti contabili dalla scheda o dal documento interessato. Ad esempio, nella pagina **Scheda fornitore** scegliere l'azione **Movimenti**.

## <a name="editing-ledger-entries"></a>Modifica di movimenti contabili
È possibile modificare determinati campi nei documenti di acquisto registrati, come ad esempio **Riferimento pagamento**. Per ulteriori informazioni, vedere [Modificare i documenti registrati](across-edit-posted-document.md). Per i campi più critici che influiscono sulla traccia di controllo, è necessario stornare o annullare la registrazione. Per ulteriori informazioni, vedere [Stornare le registrazioni e annullare carichi/spedizioni errati](finance-how-reverse-journal-posting.md).

## <a name="see-related-training-at-microsoft-learn"></a>Vedere le informazioni relative al training in [Microsoft Learn](/learn/modules/receive-invoice-dynamics-d365-business-central/index)

## <a name="see-also"></a>Vedere anche
[Modificare i documenti registrati](across-edit-posted-document.md)  
[Registrare più documenti contemporaneamente](ui-batch-posting.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Contabilizzazione dei documenti e delle registrazioni](ui-post-documents-journals.md)  
[Correggere o annullare le fatture di acquisto non pagate](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Individuare pagine e informazioni con la funzionalità delle informazioni](ui-search.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
