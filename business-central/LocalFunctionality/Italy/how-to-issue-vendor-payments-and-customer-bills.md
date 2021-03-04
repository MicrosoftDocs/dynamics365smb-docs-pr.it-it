---
title: 'Procedura: Emettere pagamenti fornitori ed effetti clienti'
description: La funzionalità di pagamento degli effetti cliente e fornitore supporta i formati SEPA oltre ai formati di file italiani.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 208b860fe5b59032c5814e3cfee084edc43e56ea
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3919989"
---
# <a name="issue-vendor-payments-and-customer-bills"></a>Emettere pagamenti fornitori ed effetti clienti

La funzionalità di pagamento degli effetti cliente e fornitore supporta i formati SEPA oltre ai formati di file italiani. È possibile pagare i fornitori in base al bonifico SEPA standard e riscuotere i pagamenti dai clienti in base al metodo di addebito diretto SEPA standard. Di seguito viene descritto il processo per l'invio del pagamento a un fornitore con bonifico SEPA. I passaggi sono simili per la riscossione del pagamento da un cliente.  

Prima di avviare la seguente procedura, controllare che le informazioni sulla banca della società siano state immesse nella pagina **Scheda conto corrente bancario**. Nella scheda. includere le informazioni per i seguenti campi:  

- IBAN  
- Codice SWIFT (facoltativo)  
- Formato esportazione pagamento  
- Nr serie ID msg CT SEPA Serie  

Inoltre, occorre inserire una fattura di acquisito registrata e con cui è possibile inviare un pagamento.  

## <a name="to-issue-payment-to-a-vendor"></a>Per emettere il pagamento per un fornitore  

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Fornitori** e quindi scegliere il collegamento correlato.  
2. Selezionare il fornitore al quale si desidera inviare il pagamento. Nella Scheda dettaglio **Pagamento**, nel campo **Codice metodo di pagamento** scegliere l'opzione **TRASFBANC**.
3. Scegliere l'azione **C/C bancari**.  
4. In **Lista C/C bancari fornitori**, selezionare il conto C/C bancari del fornitore e scegliere l'azione **Modifica**.
5. Nella Scheda dettaglio **Trasferimento**, specificare le informazioni relative al campo **IBAN**.  
6. Scegliere il pulsante **OK**.  
7. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Distinta fornitore** e quindi scegliere il collegamento correlato.  
8. Scegliere l'azione **Nuovo**.  
9. Nella Scheda dettaglio **Generale**, immettere le informazioni nei seguenti campi: **Nr. conto bancario** del fornitore e **Codice metodo di pagamento**.  
10. Scegliere l'azione **Suggerisci Pagamenti**.
11. Impostare i filtri appropriati e scegliere il pulsante **OK** per eseguire il processo batch.  
12. Scegliere l'azione **Crea Distinta**.
13. Scegliere il pulsante **Sì** per inviare il pagamento dell'effetto.  
14. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Distinta effetti fornitore emessa** e quindi scegliere il collegamento correlato.
15. Selezionare l'utente dall'elenco quindi scegliere l'azione **Modifica**. Verrà aperta la pagina **Distinta effetti forn. emessa**.  
16. Per esportare le informazioni sui pagamenti, scegliere l'azione **Esporta distinta effetti su file**. È possibile visualizzare il file XML inviato.  

    1. Esportare nel file (per file in formato SEPA standard)  
    2. Esporta distinta effetti su file  

È possibile visualizzare il file XML prima di inviarlo. Per esaminare e correggere gli errori, è possibile fare riferimento al riquadro Dettaglio informazioni **Errori esportazione file**.  

## <a name="see-also"></a>Vedi anche

[Creare movimenti riscossione addebiti diretti SEPA ed esportarli in un file della banca](../../finance-collect-payments-with-sepa-direct-debit.md#creating-sepa-direct-debit-collection-entries-and-export-to-a-bank-file)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]