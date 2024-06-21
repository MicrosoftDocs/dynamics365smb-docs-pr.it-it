---
title: Aggiungere testo esteso
description: 'È possibile aggiungere righe supplementari per estendere il testo standard che descrive un articolo, un conto C/G e altri dati.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '391, 30'
ms.date: 06/24/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="add-extended-text"></a>Aggiungere testo esteso

È possibile estendere la descrizione di articoli, unità di stockkeeping, conti di contabilità generale e risorse aggiungendo righe extra come testo esteso. È inoltre possibile impostare le condizioni per l'uso delle righe extra.  

La sezione seguente descrive come aggiungere testo esteso a una descrizione di un articolo. Gli stessi passaggi si applicano alle unità di stockkeeping, ai conti di contabilità generale e alle risorse.  

## <a name="to-define-extended-text-for-an-description"></a>Per definire il testo esteso per una descrizione

1. Aprire la scheda di un articolo al quale si desidera aggiungere il testo esteso, quindi scegliere l'azione **Testo esteso**.
2. Compilare i campi **Codice** e **Descrizione**.
3. Scegliere **Nuovo**.
4. Compilare il campo **Cod. lingua** o selezionare la casella di controllo **Tutti cod. lingua** se si utilizzano i codici lingua.
5. Compilare i campi **Data inizio** e **Data fine** se si desidera limitare il periodo in cui il testo esteso verrà utilizzato.
6. Nel campo **Testo** immettere il testo esteso.
7. Selezionare le relative caselle di controllo per i tipi di documento su cui si desidera stampare il testo esteso.
8. Chiudere la pagina.

È ora possibile aggiungere questo testo esteso ai documenti. La seguente procedura spiega come aggiungere testo esteso a un ordine cliente, ma gli stessi passaggi si applicano a qualsiasi altro documento specificato per il testo esteso.  

## <a name="to-add-an-extended-item-text-on-a-sales-order-line"></a>Per aggiungere testo esteso di articoli in una riga di un ordine di vendita

1. Aprire un ordine di vendita con una riga di vendita per un articolo che ha testo esteso definito. Per ulteriori informazioni, vedere [Vendere prodotti](sales-how-sell-products.md).
2. Selezionare la riga in questione e scegliere l'azione **Inserisci testo esteso**.

## <a name="see-also"></a>Vedere anche

[Impostazione del magazzino](inventory-setup-inventory.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
