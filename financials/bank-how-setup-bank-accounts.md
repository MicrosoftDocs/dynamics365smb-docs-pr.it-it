---
title: 'Procedura: Impostare i conti correnti bancari | Documenti Microsoft'
description: 'Procedura: impostare i conti correnti bancari'
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream
ms.date: 03/23/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 665c07a7242796718cfb01a1eb901d4df04ef8c9
ms.contentlocale: it-it
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-set-up-bank-accounts"></a>Procedura: impostare i conti correnti bancari
I conti correnti bancari vengono utilizzati in [!INCLUDE[d365fin](includes/d365fin_md.md)] per tenere traccia delle transazioni bancarie. I conti possono essere denominati in valuta locale o estera. Dopo aver impostato i conti correnti bancari è possibile utilizzare l'opzione per la stampa di assegni.

## <a name="to-set-up-bank-accounts"></a>Per impostare i conti correnti bancari
1. Nell'angolo superiore destro scegliere l'icona **Cerca pagina o report** ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), inserire **Conti Correnti Bancari**, quindi scegliere il collegamento correlato.
2. Nella finestra **C/C bancari** scegliere l'azione **Nuovo**.
3. Compilare i campi, se necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-your-bank-account-for-import-or-export-of-bank-files"></a>Per impostare il conto corrente bancario per l'importazione o l'esportazione di file dei conti correnti bancari
I campi nella nella Scheda dettaglio **Trasferimento** della finestra **Scheda conto corrente bancario** sono correlati all'importazione e all'esportazione dei feed e dei file della banca. Per ulteriori informazioni, vedere [Procedura: Impostare il servizio di conversione di dati bancari](bank-how-setup-bank-data-conversion-service.md) e [Procedura: Impostare il servizio Feed bancari di Envestnet Yodlee](bank-how-setup-bank-statement-service.md).

1. Nell'angolo superiore destro scegliere l'icona **Cerca pagina o report** ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), inserire **Conti Correnti Bancari**, quindi scegliere il collegamento correlato.
2. Aprire la scheda di un conto corrente bancario per il quale verranno esportati o importati i file dei conti correnti bancari.
3. Compilare i campi appropriati nella Scheda dettaglio **Trasferimento**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

**Nota**: servizi di esportazione file diversi e i rispettivi formati richiedono valori di configurazione differenti nella finestra **Scheda conto corrente bancario**. Si verrà informati sui valori di setup mancanti o non corretti mentre si tenta di esportare il file. Leggere quindi con attenzione le brevi descrizioni dei campi o fare riferimento agli argomenti di procedura correlati. Ad esempio, esportare un file di pagamento per il trasferimento elettronico dei fondi (EFT) in Nord America richiede che sia il campo **Nr. ultimo avviso di rimessa** e il campo **Nr. transito** siano compilati. Per ulteriori informazioni, vedere [Procedura: Esportare pagamenti in un file della banca](payables-how-export-payments-bank-file.md).

## <a name="to-set-up-vendor-bank-accounts-for-export-of-bank-files"></a>Per impostare i conti correnti fornitore per l'esportazione di file dei conti correnti bancari
I campi nella nella Scheda dettaglio **Trasferimento** della finestra **Scheda C/C bancari fornitori** sono correlati all'esportazione dei feed e dei file dei conti correnti bancari. Per ulteriori informazioni, vedere [Procedura: Impostare il servizio di conversione di dati bancari](bank-how-setup-bank-data-conversion-service.md) e [Procedura: Esportare pagamenti in un file della banca](payables-how-export-payments-bank-file.md).

1. Nell'angolo superiore destro scegliere l'icona **Cerca pagina o report** ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), inserire **Fornitori**, quindi scegliere il collegamento correlato.
2. Aprire la scheda di un conto corrente bancario fornitore nel quale verranno esportati i file di pagamento della banca.
3. Scegliere l'azione **C/C bancari**.
3. Nella Scheda dettaglio **Trasferimenti** della finestra **Scheda C/C bancari fornitori** compilare i campi come richiesto. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a>Vedi anche
[Impostazione delle attività bancarie](bank-setup-banking.md)  
[Gestione di conti correnti bancari](bank-manage-bank-accounts.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

