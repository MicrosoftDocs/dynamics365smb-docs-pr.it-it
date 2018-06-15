---
title: Utilizzare il processo batch Suggerisci pagamenti fornitore| Documenti Microsoft
description: "È possibile specificare le impostazioni di pagamento dei fornitori per ottenere suggerimenti o proposte per pagamenti in scadenza oppure per cui è disponibile uno sconto."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 05/15/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ad1b888d475c0523c5a905e804a3f89ab4531b28
ms.openlocfilehash: 02f063daf5afeea85832c8a322183b3db120d8d2
ms.contentlocale: it-it
ms.lasthandoff: 05/17/2018

---
# <a name="suggest-vendor-payments"></a>Sugg. pagamenti fornitore
Nella finestra **Registraz. pagamenti** è possibile utilizzare il processo batch **Sugg. pagamenti fornitore** per suggerire le righe di pagamento. Le righe per i pagamenti che scadono presto oppure i pagamenti dove è disponibile uno sconto sul pagamento vengono suggerite in base alle impostazioni.

Per trarre completamente vantaggio dai pagamenti suggeriti, è prima necessario assegnare una priorità ai fornitori. Per ulteriori informazioni, vedere [Attribuire un ordine di priorità ai fornitori](purchasing-how-prioritize-vendors.md).  

> [!NOTE]  
> I movimenti contabili fornitore con stato **In sospeso** non sono inclusi nel processo batch.  

> [!IMPORTANT]  
>   Per trarre vantaggio dagli sconti sui pagamenti, se si è immesso un importo disponibile, l'importo verrà utilizzato per:  

* Movimenti fornitori scaduti con priorità innanzitutto in ordine di priorità.  
* Movimenti fornitori scaduti senza priorità.  
* Movimenti fornitori che vengono qualificati per gli sconti sui pagamenti, sistemati in base al numero di fornitori.  

## <a name="to-use-the-suggest-vendor-payments-function"></a>Per utilizzare la funzione di suggerimento pagamenti fornitori
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Registrazioni pagamenti**, quindi scegliere il collegamento correlato.  
2. Aprire le registrazioni rilevanti e scegliere l'azione **Sugg. pagamenti fornitore**.  
3. Compilare i campi, se necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Scegliere il pulsante **OK**.  

## <a name="to-insert-the-due-date-as-posting-date-on-payment-journal-lines"></a>Per inserire la data di scadenza come data di registrazione nelle righe di registrazione pagamenti
Quando si esegue il processo batch **Sugg. pagamenti fornitore** per creare righe di pagamento per i fornitori, è possibile compilare due campi speciali per assicurarsi che le righe generate utilizzino la data di scadenza per calcolare la data di registrazione. Questi campi sono **Calcola data di registrazione da Collega a - Scadenza doc.** e **Offset Collega a - Scadenza doc.**  

> [!IMPORTANT]  
>   Non è possibile utilizzare il campo **Calcola data di registrazione da Collega a - Scadenza doc** insieme al campo **Trova sconti pagamenti** o al campo **Raggruppa per fornitore**. Se la data di registrazione è basata sulla data di scadenza, gli sconti sui pagamenti potrebbero non essere calcolati correttamente, in quanto la data di registrazione potrebbe essere successiva alla data dello sconto sul pagamento.  

Inoltre, se la data di registrazione calcolata è già trascorsa, la data di registrazione viene spostata alla data di lavoro e viene visualizzato un avviso.  

In alternativa, è possibile creare manualmente le righe di pagamento utilizzando la data di scadenza per calcolare la data di registrazione. Dopo che si collegano movimenti contabili fornitori, è possibile utilizzare l'azione **Calcola data registrazione** per aggiornare la data di registrazione nella riga di registrazione con la data di scadenza della fattura relativa di acquisto. Per ulteriori informazioni, vedere [Collegare manualmente le transazioni di acquisto](payables-how-apply-purchase-transactions-manually.md).  

> [!NOTE]  
>   Se la fattura di acquisto è scaduta, la data di registrazione viene impostata sulla data di lavoro e il carattere nella riga diventa di colore rosso.  

## <a name="see-also"></a>Vedi anche
[Gestione della contabilità fornitori](payables-manage-payables.md)  
[Effettuare i pagamenti](payables-make-payments.md)  
[Utilizzo delle registrazioni COGE](ui-work-general-journals.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

