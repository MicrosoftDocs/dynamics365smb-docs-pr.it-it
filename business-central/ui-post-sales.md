---
title: Registrazione di documenti di vendita
description: Informazioni sulle diverse funzioni di registrazione per registrare documenti di vendita e sul modo in cui aggiornare documenti registrati.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.search.form: '130, 142, 1350'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="posting-sales"></a><a name="posting-sales"></a><a name="posting-sales"></a>Registrazione di vendite

Nel menu **Registrazione** in un documento di vendita, è possibile scegliere tra le seguenti funzioni di registrazione:

* **Registra**
* **Registra e nuovo**
* **Registra e invia**
* **Anteprima registrazione**
* **Registra batch**
* **Report test**

> [!NOTE]
> Per gli ordini vendita, è anche possibile visualizzare le opzioni relative alla funzionalità di pagamento anticipato. Per ulteriori informazioni, vedere [Fatturazione dei pagamenti anticipati](finance-invoice-prepayments.md).

Una volta completate le righe e immesse tutte le informazioni nell'ordine di vendita, è possibile registrarlo. Vengono create una spedizione e una fattura.

Quando un ordine di acquisto viene registrato, il conto del cliente, la contabilità generale e i movimenti contabili articoli vengono aggiornati.

Per ciascun ordine di vendita viene creato un movimento di vendita nella tabella **Movimenti C/G**. Vengono inoltre creati un movimento nel conto del cliente nella tabella **Mov. contabili clienti** e un movimento C/G nel relativo conto crediti. Infine, la registrazione dell'ordine potrebbe generare un movimento IVA e un movimento di contabilità generale relativi all'importo dello sconto. La registrazione di un movimento relativo allo sconto dipende dal contenuto del campo **Registrazione sconti** della pagina **Setup contabilità clienti**.

Per ciascuna riga dell'ordine di vendita, verrà creato un movimento contabile articolo nella tabella **Mov. contabili articoli** (se le righe di vendita contengono numeri di articolo) oppure un movimento C/G nella tabella **Movimenti C/G** (se le righe di vendita contengono un conto C/G). Inoltre, gli ordini vendita vengono sempre registrati nelle tabelle **Testate sped. vendita** e **Testate Fatt. Vendita**.

[!INCLUDE [order-ship-invoice](includes/order-ship-invoice.md)]

È possibile effettuare la registrazione oppure effettuare la registrazione e inviare. Se si sceglie di registrare e inviare, viene generato un file PDF che è possibile inviare. È inoltre possibile scegliere la funzione **Registra batch** che consente di registrare più ordini contemporaneamente. Per ulteriori informazioni, vedere [Pubblicare più documenti contemporaneamente](ui-batch-posting.md).

## <a name="viewing-ledger-entries"></a><a name="viewing-ledger-entries"></a><a name="viewing-ledger-entries"></a>Visualizzazione di movimenti contabili

Una volta completata la registrazione, le righe di vendita registrate vengono rimosse dall'ordine. Un messaggio avviserà l'utente che la registrazione è completata. Dopodiché sarà possibile visualizzare i movimenti registrati nelle varie pagine che contengono movimenti registrati, ad esempio le pagine **Mov. contabili clienti**, **Movimenti C/G**, **Mov. contabili articoli**, **Spedizioni vendite registrate** e **Fatture di vendita registrate**.  

Nella maggior parte dei casi, è possibile aprire i movimenti contabili dalla scheda o dal documento interessato. Ad esempio, nella pagina **Scheda cliente** scegliere l'azione **Movimenti contabili**.

## <a name="editing-ledger-entries"></a><a name="editing-ledger-entries"></a><a name="editing-ledger-entries"></a>Modifica di movimenti contabili

È possibile modificare determinati campi nei documenti di acquisto registrati, come ad esempio **Nr. identificazione collo** . Per ulteriori informazioni, vedere [Modificare i documenti registrati](across-edit-posted-document.md). Per i campi più critici che influiscono sulla traccia di controllo, è necessario stornare o annullare la registrazione. Per ulteriori informazioni, vedere [Stornare le registrazioni e annullare carichi/spedizioni errati](finance-how-reverse-journal-posting.md).

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Vedi il relativo [training Microsoft](/training/modules/ship-invoice-items-dynamics-365-business-central/index)

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Vedi anche

[Vendite](sales-manage-sales.md)  
[Registrare più documenti contemporaneamente](ui-batch-posting.md)  
[Modificare i documenti registrati](across-edit-posted-document.md)  
[Inviare documenti via e-mail](ui-how-send-documents-email.md)  
[Correggere o annullare le fatture di vendita non pagate](sales-how-correct-cancel-sales-invoice.md)  
[Individuare pagine e informazioni con la funzionalità delle informazioni](ui-search.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]  
