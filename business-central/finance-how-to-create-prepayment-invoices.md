---
title: Come creare fatture di pagamenti anticipati | Microsoft Docs
description: Informazioni su come gestire situazioni in cui un pagamento anticipato viene richiesto ai clienti o dal fornitore.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 96433274efa8ea8f5ec93248f4a7c992e456aa26
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/29/2019
ms.locfileid: "1243551"
---
# <a name="create-prepayment-invoices"></a>Creare fatture per i pagamenti anticipati
Se è necessario che i clienti inviino il pagamento prima della spedizione di un ordine, oppure se il fornitore richiede l'invio del pagamento prima di spedire l'ordine, è possibile utilizzare la funzionalità Pagamento anticipato.  

Dopo avere creato un ordine di vendita o di acquisto, è possibile creare una fattura pagamento anticipato. È possibile utilizzare le percentuali di default per ogni riga di vendita o di acquisto oppure rettificare l'importo come necessario. È ad esempio possibile specificare un importo totale per l'intero ordine.  

La procedura seguente descrive come fatturare un pagamento anticipato per un ordine di vendita. I passaggi sono simili per un ordine di acquisto.  

## <a name="to-create-a-prepayment-invoice"></a>Per creare una fattura di pagamento anticipato  
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ordini di vendita** e quindi scegliere il collegamento correlato.  
2. Creare un nuovo ordine di vendita. Per ulteriori informazioni, vedere [Vendere prodotti](sales-how-sell-products.md).  

    Nella Scheda dettaglio **Pagamento anticipato**, il campo **% pagamento anticipato** verrà compilato automaticamente se nella scheda cliente è impostata una percentuale pagamento anticipato di default. È possibile modificare il contenuto del campo. La percentuale pagamento anticipato viene copiata dalla testata solo nelle righe in cui non viene copiata la percentuale pagamento anticipato di default per l'articolo.  

    Se il campo **Comprimi pagamento anticipato** è selezionato, nella fattura le righe verranno combinate se:  
    - Le righe hanno lo stesso conto di contabilità generale per i pagamenti anticipati, come determinato in Setup registrazioni COGE.  
    - Le righe hanno le stesse dimensioni.  

    Lasciare vuoto il campo se si desidera specificare una fattura pagamento anticipato con una riga per ogni riga dell'ordine di vendita associata a una percentuale pagamento anticipato.  

3. Compilare le righe di vendita.  

    Se per gli articoli sono state impostate percentuali predefinite di pagamento anticipato, i valori vengono automaticamente copiati nel campo **% pagamento anticipato** nella riga. In caso contrario, la percentuale pagamento anticipato viene copiata dalla testata. È possibile modificare il contenuto del campo **% pagamento anticipato** nella riga.  
4. Se si desidera collegare una percentuale di pagamento anticipato all'intero ordine, modificare il campo **% pagamento anticipato** nella testata dopo avere compilato le righe.  
5. Per visualizzare l'importo del pagamento anticipato totale, scegliere l'azione **Statistiche**.

    Se si desidera rettificare l'importo del pagamento anticipato totale per l'ordine, è possibile modificare il contenuto del campo **Importo pagamento anticipato** nella pagina **Statistiche ordini vendita**.  

    Se il campo **Prezzi IVA inclusa** è selezionato, il campo **Importo pagam. ant. IVA incl.** è modificabile.  

    Se si modifica il contenuto del campo **Importo pagamento anticipato**, l'importo verrà distribuito proporzionalmente tra tutte le righe, ad eccezione di quelle in cui è presente il valore **0** nel campo **% pagamento anticipato**.  
6. Per stampare un report test prima di registrare una fattura pagamento anticipato, scegliere l'azione **Pagamento anticipato** e quindi scegliere l'azione **Report test pagamento anticipato**.  
7. Per registrare la fattura pagamento anticipato, scegliere l'azione **Pagamento anticipato** e quindi scegliere l'azione **Registra fattura pagamento anticipato**.  

    Per registrare e stampare la fattura pagamento anticipato, scegliere l'azione **Registra e stampa fattura pagam. ant.**  

È possibile emettere fatture pagamento anticipato aggiuntive per l'ordine. A tale scopo, aumentare l'importo pagamento anticipato in una o più righe, rettificare la data del documento, se necessario, e registrare la fattura pagamento anticipato. Verrà creata una nuova fattura per la differenza tra gli importi pagamento anticipato fatturati fino a quel momento e il nuovo importo pagamento anticipato.  

> [!NOTE]  
>  Se ci si trova in America del Nord, non è possibile modificare la percentuale di pagamento anticipato dopo che la fattura pagamento anticipato è stata registrata. Ciò è impedito nella versione nordamericana di [!INCLUDE[d365fin](includes/d365fin_md.md)] perché altrimenti il calcolo dell'imposta sulle vendite risulterebbe errato.  

 Quando si è pronti per registrare il resto della fattura, effettuare la registrazione come con qualsiasi fattura. L'importo pagamento anticipato verrà automaticamente dedotto dall'importo dovuto.  

## <a name="see-also"></a>Vedi anche  
[Fatturazione dei pagamenti anticipati](finance-invoice-prepayments.md)  
[Procedura dettagliata: impostazione e fatturazione dei pagamenti anticipati vendite](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Finanze](finance.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
