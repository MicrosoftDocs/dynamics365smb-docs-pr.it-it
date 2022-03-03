---
title: Pagamenti automatici ed effetti automatici [IT]
description: Il seguente argomento spiega come impostare le informazioni rilevanti in Business Central per gestire pagamenti ed effetti automatici.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.form: 12203, 12204
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: f33d0066a0e45b606c5d6579ce904e12117deb74
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2022
ms.locfileid: "8138134"
---
# <a name="set-up-automatic-payments-and-automatic-bills-in-the-italian-version"></a>Impostare i pagamenti automatici e gli effetti automatici nella versione italiana
In [!INCLUDE[prod_short](../../includes/prod_short.md)], è possibile gestire i pagamenti e gli effetti automatici.  

Per utilizzare i pagamenti e gli effetti automatici, è necessario impostare le informazioni pertinenti.  

## <a name="to-add-bank-information-for-your-company"></a>Per aggiungere le informazioni relative alla banca della società  

1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Informazioni società**, quindi scegli il collegamento correlato.  
2.  Nella Scheda dettaglio **Pagamenti** compilare i campi chiave come indicato nella tabella seguente.  

|Campo|Description|  
|------------------------------------|---------------------------------------|  
|**Metodo di pagamento**|Selezionare il metodo di pagamento per il tipo dei pagamenti effettuati dal o al conto corrente bancario. Ad esempio, per il conto corrente bancario da utilizzare per i pagamenti automatici effettuati da clienti, selezionare un metodo di pagamento per bonifici bancari.|  
|**Conto effetti all'Incasso**|Specificare il conto C/G sul quale verranno accreditati gli effetti per la riscossione.|  
|**Conto effetti allo sconto**|Specificare i conti di contabilità generale in cui verranno addebitati gli sconti di effetti.|  
|**Conto effetti salvo buon fine**|Specificare il conto C/G sul quale verranno accreditati gli effetti soggetti alla riscossione.|  
|**Conto spesa effetti**|Specificare i conti di contabilità generale in cui verranno registrate le spese per le ricevute bancarie.|  

5.  Scegliere il pulsante **OK**.  

> [!IMPORTANT]  
>  Prima di esportare un effetto fornitore, è necessario selezionare il formato di pagamento nel campo **Formato esportazione pagamento** nella pagina **Scheda conto corrente bancario**.  
>   
>  Prima di esportare un effetto cliente, è necessario selezionare il formato di pagamento nel campo **Formato esport. addebito dir. SEPA** nella pagina **Scheda conto corrente bancario**.  

Di seguito viene descritto come impostare gli effetti automatici per vendite e incassi, ma gli stessi passaggi sono applicabili per l'impostazione di acquisti e debiti per l'utilizzo dei pagamenti automatici.  

## <a name="to-set-up-automatic-bills-for-sales-and-receivables"></a>Per impostare gli effetti automatici per vendite e incassi  

1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup contabilità clienti**, quindi scegli il collegamento correlato.  
2.  Nella Scheda dettaglio **Effetti**, nel campo **Nr. temp. distinta effetto** selezionare il numero temporaneo della distinta effetti. Compilare i campi come indicato nella tabella seguente.  

|Campo|Description|  
|---------------------------------|---------------------------------------|  
|**Nr. temp. distinta effetto**|Selezionare la numerazione che sarà utilizzata le distinte effetti temporanee.|  
|**Richiamo effetti - Descrizione**|Specificare il testo descrittivo che verrà utilizzato per gli effetti richiamati.|  
|**Periodo rischio RIBA**|Specificare una formula di data per il calcolo del periodo di rischio in giorni, ad esempio **20G**.<br /><br /> Questo sarà un riferimento per la chiusura ricevute bancarie. Gli effetti del cliente verranno chiusi solo alla fine del periodo di rischio specificato qui.|  

3.  Scegliere il pulsante **OK**.  

 A questo punto, è necessario specificare i codici effetto per i metodi di pagamento utilizzati per i pagamenti automatici e gli effetti automatici.  

## <a name="to-specify-bill-codes-for-a-payment-method"></a>Per specificare i codici effetto per un metodo di pagamento  

1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Metodi di pagamento**, quindi scegli il collegamento correlato.  
2.  Selezionare il metodo di pagamento utilizzato per i trasferimenti bancari ai fornitori, quindi nel campo **Cod. effetto**, selezionare un codice effetto.  

1.  Per creare un codice effetto, nel campo **Cod. effetto**, scegliere il campo quindi scegliere l'azione **Nuovo**.  
2.  Compilare i campi della pagina **Effetto**.

A questo punto, è possibile elaborare gli effetti cliente e fornitore in modo che vengano gestiti automaticamente.  

## <a name="see-also"></a>Vedere anche  
 [Definizione dei metodi di pagamento](../../finance-payment-methods.md) [Funzionalità locale per l'Italia](italy-local-functionality.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]