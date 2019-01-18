---
title: 'Procedura: Convertire i contratti di assistenza | Documenti Microsoft'
description: "Dal momento che lo strumento di modifica dell'aliquota IVA non può convertire i contratti di assistenza, tali contratti devono essere convertiti manualmente. In questo argomento vengono descritti diversi metodi alternativi che è possibile utilizzare per la conversione del contratto di assistenza."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 3c34f2b456df88b043b7b90a739f363b892dd48d
ms.contentlocale: it-it
ms.lasthandoff: 11/26/2018

---
# <a name="convert-service-contracts-that-include-vat-amounts"></a>Convertire i contratti di assistenza che includono importi IVA
Dal momento che lo strumento di modifica dell'aliquota IVA non può convertire i contratti di assistenza, tali contratti devono essere convertiti manualmente. In questo argomento vengono descritti diversi metodi alternativi che è possibile utilizzare per la conversione del contratto di assistenza.  

> [!NOTE]  
>  In questo argomento viene fornito un flusso di lavoro dettagliato.  

 Nella procedura riportata di seguito viene descritto come correggere una fattura per un contratto di assistenza prepagato creato un anno prima.  

> [!NOTE]  
>  Per questo esempio, è necessario modificare la data di lavoro in 01.01.2017.  

### <a name="to-correct-an-invoice-for-a-prepaid-service-contract"></a>Per correggere una fattura per un contratto di assistenza prepagato  
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Gestione contratti** e quindi scegliere il collegamento correlato.  
2. In **Liste** selezionare **Contratti assistenza**.  
3. Creare un nuovo contratto di assistenza prepagato. Immettere una data di inizio **01.01.2017** e un anno del periodo di fatturazione per il cliente **20000**.  
4. Questo contratto deve essere firmato. Nel gruppo **Processo** della scheda **Pagina iniziale** scegliere **Firma contratto**.  
5. Creare una fattura assistenza.
6. La fattura viene elencata come fattura di assistenza non registrata. Per visualizzare la fattura di assistenza, fare clic su **Assistenza**, selezionare **Gestione contratti**, quindi scegliere **Fatture assistenza**.  
7. Registrare la fattura di assistenza.  

> [!NOTE]  
>  Non modificare la fattura di assistenza non registrata. Poiché i movimenti di assistenza vengono generati quando la fattura viene creata, una modifica della fattura non registrata non influenzerà i movimenti contabili di assistenza già creati. Tuttavia, i movimenti IVA vengono creati quando la fattura viene registrata. In questo modo è possibile modificare la categoria di registrazione articoli/servizi e la categoria di registrazione articoli/servizi del sistema di preferenze generalizzate nella fattura di assistenza non registrata.  

### <a name="to-create-a-credit-memo-for-vat-difference"></a>Per creare una nota di credito per la differenza IVA  
Nella procedura riportata di seguito viene descritto come creare una nota di credito che includa solo la differenza IVA per un periodo già fatturato a partire da **01.07.2017**. Nell'esempio l'importo IVA viene registrato solo nel modulo Gestione contabile, non in quello Gestione assistenza. I movimenti IVA collegati al movimento assistenza non verranno corretti.  

1. Creare un nuovo conto di contabilità generale per la differenza IVA. Questo conto verrà utilizzato per la registrazione diretta della correzione IVA.  
2. Aggiungere una nuova riga all'impostazione per le registrazioni IVA.  

### <a name="to-create-contract-expiration-dates-in-contract-lines"></a>Per creare le date di scadenza del contratto nelle righe di contratto  
Nella procedura riportata di seguito viene descritto come creare nuovi contratti utilizzando le date di scadenza del contratto nelle righe del contratto di assistenza.  

1. Nella pagina **Contratto assistenza** impostare la data di scadenza del contratto su **30.06.2017**.  
2. Scegliere l'azione **Crea nota credito** per creare automaticamente una nota di credito per il periodo compreso tra luglio 2017 e dicembre 2017.  
3. Dal momento che il contratto è scaduto, è necessario creare un nuovo contratto con la nuova aliquota IVA per il periodo compreso tra il 1° luglio 2017 e 31 dicembre 2017.  

### <a name="to-create-a-new-credit-memo"></a>Per creare una nuova nota di credito.  
Nella procedura riportata di seguito viene descritto come creare una nuova nota di credito mediante il processo batch **Prendi mov. contr. prepagati**. I movimenti che non si desidera correggere da gennaio 2017 a giugno 2017 verranno eliminati.  

1. Eseguire lo strumento per la modifica dell'aliquota IVA il 1° luglio 2017. La categoria di registrazione articoli/servizi o la categoria di registrazione articoli/servizi IVA è cambiata. Per ulteriori informazioni, vedere [Utilizzare l'IVA nelle vendite e negli acquisti](finance-work-with-vat.md).  
2. Dopo aver eseguito lo strumento di modifica aliquota IVA, immettere una data di scadenza del contratto per il contratto di assistenza. È ora possibile eliminare la riga del contratto di assistenza e creare una nuova riga identica a quella precedente.  
3. Creare una nuova fattura per il periodo compreso tra gennaio 2017 e dicembre 2012 utilizzando la nuova aliquota IVA.  
4. Per creare un'altra nota di credito, selezionare **Nuovo** nella pagina **Note credito assistenza**.  
5. Scegliere l'azione **Prendi mov. contr. prepagati**.  
6. Dopo aver completato la conversione, l'IVA e i movimenti contabili verranno corretti.  

## <a name="see-also"></a>Vedi anche  
[Utilizzare contratti e offerte di contratto di assistenza](service-how-to-create-service-contracts-and-service-contract-quotes.md)  
[Finanze](finance.md)  
[Dichiarare l'IVA all'autorità fiscale](finance-how-report-vat.md)  
[Utilizzare l'IVA nelle vendite e negli acquisti](finance-work-with-vat.md)  

