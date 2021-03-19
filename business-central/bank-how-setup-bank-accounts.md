---
title: Impostare i conti correnti bancari| Documenti Microsoft
description: È possibile riconciliare i conti correnti bancari con gli estratti conto della banca.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 6d61b235369a25fe04157b7af280f8756900d3f8
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5376664"
---
# <a name="set-up-bank-accounts"></a>Impostare i conti correnti bancari
I conti correnti bancari vengono utilizzati in [!INCLUDE[prod_short](includes/prod_short.md)] per tenere traccia delle transazioni bancarie. I conti possono essere denominati in valuta locale o estera. Dopo aver impostato i conti correnti bancari è possibile utilizzare l'opzione per la stampa di assegni.<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Vhpl?rel=0]

## <a name="to-set-up-bank-accounts"></a>Per impostare i conti correnti bancari
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Conti correnti bancari** e quindi scegliere il collegamento correlato.
2. Nella pagina **C/C bancari** scegliere l'azione **Nuovo**.
3. Compilare i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> Per compilare il campo **Saldo** con un saldo iniziale, è necessario registrare un movimento contabile del conto corrente bancario con la quantità in questione. È possibile effettuare questa operazione eseguendo un una riconciliazione bancaria. Per ulteriori informazioni, vedere [Riconciliare i conti correnti bancari](bank-how-reconcile-bank-accounts-separately.md). In alternativa, è possibile implementare il saldo iniziale come parte della creazione di dati generali in nuove aziende utilizzando la guida al setup assistito **Migra dati aziendali**. Per ulteriori informazioni, vedere [Introduzione](product-get-started.md).

## <a name="to-set-up-your-bank-account-for-import-or-export-of-bank-files"></a>Per impostare il conto corrente bancario per l'importazione o l'esportazione di file dei conti correnti bancari
I campi nella nella Scheda dettaglio **Trasferimento** della pagina **Scheda conto corrente bancario** sono correlati all'importazione e all'esportazione dei feed e dei file della banca. Per ulteriori informazioni, vedere [Utilizzo dell'estensione AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md) e [Impostare il servizio Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Conti correnti bancari** e quindi scegliere il collegamento correlato.
2. Aprire la scheda di un conto corrente bancario per il quale verranno esportati o importati i file dei conti correnti bancari.
3. Compilare i campi appropriati nella Scheda dettaglio **Trasferimento**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   I diversi servizi di esportazione file e i rispettivi formati richiedono valori di configurazione differenti nella pagina **Scheda conto corrente bancario**. Si verrà informati sui valori di setup mancanti o non corretti mentre si tenta di esportare il file. Leggere quindi con attenzione le brevi descrizioni dei campi o fare riferimento agli argomenti di procedura correlati. Ad esempio, esportare un file di pagamento per il trasferimento elettronico dei fondi (EFT) in Nord America richiede che sia il campo **Nr. ultimo avviso di rimessa** che il campo **Nr. transito** siano compilati. Per ulteriori informazioni, vedere [Esportare pagamenti in un file della banca](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

## <a name="to-set-up-vendor-bank-accounts-for-export-of-bank-files"></a>Per impostare i conti correnti fornitore per l'esportazione di file dei conti correnti bancari

I campi nella nella Scheda dettaglio **Trasferimento** della pagina **Scheda C/C bancari fornitori** sono correlati all'esportazione dei feed e dei file dei conti correnti bancari. Per ulteriori informazioni, vedere [Utilizzo dell'estensione AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md) ed [Esportare pagamenti in un file della banca](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Fornitori** e quindi scegliere il collegamento correlato.
2. Aprire la scheda di un conto corrente bancario fornitore nel quale verranno esportati i file di pagamento della banca.
3. Scegliere l'azione **C/C bancari**.
4. Dall'**elenco dei conti bancari del fornitore**, scegliere il conto bancario pertinente o aggiungere un nuovo conto bancario.  
5. Nella Scheda dettaglio **Trasferimenti** della pagina **Scheda C/C bancari fornitori** compilare i campi come richiesto. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a>Vedere anche

[Impostazione delle attività bancarie](bank-setup-banking.md)  
[Impostazione delle categorie di registrazione](finance-posting-groups.md)  
[Riconciliazione dei conti correnti bancari](bank-manage-bank-accounts.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]