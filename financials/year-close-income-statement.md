---
title: 'Procedura: Chiudere il conto economico | Documenti Microsoft'
description: Viene spiegato come chiudere un conto economico.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 03/29/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: dde7b93c6a3dcf78173494f1c6fa09a38207e676
ms.contentlocale: it-it
ms.lasthandoff: 05/04/2017


---
# <a name="close-income-statement"></a>Chiudi conto economico
Al termine di un anno fiscale, è necessario chiudere i periodi di cui è costituito. In questo caso, eseguire il processo batch **Chiudi conto economico**. Il processo trasferisce i risultati dell'anno in un conto nel conto patrimoniale e chiude i conti economici. A tale scopo creare righe di registrazioni che in seguito sarà possibile contabilizzare.

## <a name="to-run-the-close-income-statement-batch-job"></a>Per eseguire il processo batch di chiusura del conto economico
1. Chiudere l'anno fiscale. È necessario chiudere l'anno fiscale prima di eseguire il processo batch. Per ulteriori informazioni, vedere [Procedura: Chiudere i periodi contabili](year-close-account-periods.md).
2. Nell'angolo superiore destro scegliere l'icona **Cerca pagina o report** ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Chiudi conto economico**, quindi scegliere il collegamento correlato.
3. Scegliere **OK** per eseguire il processo batch.

## <a name="about-the-close-income-statement-batch-job"></a>Processo batch di chiusura del conto economico
Il processo batch elabora tutti i conti del tipo conto economico e crea movimenti che eliminano i rispettivi saldi. Ogni movimento è la somma di tutti i movimenti C/G sul conto nell'anno fiscale. Questi nuovi movimenti vengono inseriti in registrazioni in cui sarà necessario specificare una contropartita e un conto utili non distribuito, nel bilancio patrimoniale prima della registrazione. Dopo la registrazione, in ogni conto economico viene registrato un movimento in modo che il relativo saldo sia uguale a zero e allo stesso tempo il risultato dell'anno viene trasferito al conto patrimoniale.

Le registrazioni devono essere contabilizzate manualmente. I movimenti non vengono contabilizzati automaticamente dal processo batch, eccetto quando viene utilizzata una valuta contabile addizionale. In questo caso la contabilizzazione viene effettuata direttamente nella contabilità generale.

La data nelle righe che il processo batch inserisce nelle registrazioni è sempre la data di chiusura dell'anno fiscale. La data di chiusura è una data fittizia compresa tra l'ultimo giorno del vecchio anno fiscale e il primo giorno del nuovo. Il vantaggio di registrare in una data di chiusura è che vengono mantenuti i saldi corretti per le date ordinarie dell'anno fiscale.

Il processo batch **Chiudi conto economico** può essere utilizzato più di una volta. Se in seguito alla chiusura dei conti economici il processo batch viene nuovamente eseguito, sarà possibile effettuare registrazioni in un anno fiscale precedente.

## <a name="see-also"></a>Vedi anche
[Chiusura registri](year-close-books.md)  
[Procedura: Registrare il movimento di chiusura di fine anno](year-how-post-year-end-close-entry.md)  
[Procedura: aprire un nuovo anno fiscale](finance-how-open-new-fiscal-year.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

