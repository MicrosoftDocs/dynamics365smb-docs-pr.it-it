---
title: Chiudi conti del conto economico
description: 'Alla chiusura dell''anno, è necessario eseguire il processo batch Chiudi conto economico per chiudere i periodi contabili che costituiscono l''anno fiscale.'
author: jswymer
ms.topic: conceptual
ms.search.keywords: 'year closing, close accounting period, close fiscal year, bank account detailed trial balance'
ms.date: 08/05/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---

# <a name="close-income-statement-accounts"></a>Chiudi conti del conto economico

Al termine di un anno fiscale, è necessario chiudere i periodi di cui è costituito. In questo caso, eseguire il processo batch **Chiudi conto economico**. Il processo trasferisce i risultati dell'anno in un conto nel conto patrimoniale e chiude i conti economici. A tale scopo creare righe di registrazioni che in seguito sarà possibile contabilizzare.

## <a name="to-run-the-close-income-statement-batch-job"></a>Per eseguire il processo batch di chiusura del conto economico

1. Chiudere l'anno fiscale. È necessario chiudere l'anno fiscale prima di eseguire il processo batch. Per ulteriori informazioni, vedere [Chiudere i periodi contabili](year-close-account-periods.md).
2. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Chiudi conto economico**, quindi scegli il collegamento correlato.
3. Scegliere **OK** per eseguire il processo batch.

## <a name="about-the-close-income-statement-batch-job"></a>Processo batch di chiusura del conto economico

Il processo batch elabora tutti i conti del tipo conto economico e crea movimenti che eliminano i rispettivi saldi. Ogni movimento è la somma di tutti i movimenti C/G sul conto nell'anno fiscale. Questi nuovi movimenti vengono inseriti in registrazioni in cui sarà necessario specificare una contropartita e un conto utili non distribuito, nel bilancio patrimoniale prima della registrazione. Dopo la registrazione, in ogni conto economico viene registrato un movimento in modo che il relativo saldo sia uguale a zero e allo stesso tempo il risultato dell'anno viene trasferito al conto patrimoniale.

Le registrazioni devono essere contabilizzate manualmente. Il processo batch non registra automaticamente le voci, tranne quando viene utilizzata una valuta di rendicontazione aggiuntiva. In questo caso la contabilizzazione viene effettuata direttamente nella contabilità generale.

La data nelle righe che il processo batch inserisce nelle registrazioni è sempre la data di chiusura dell'anno fiscale. La data di chiusura è una data fittizia compresa tra l'ultimo giorno del vecchio anno fiscale e il primo giorno del nuovo. Il vantaggio di registrare in una data di chiusura è che vengono mantenuti i saldi corretti per le date ordinarie dell'anno fiscale.

Il processo batch **Chiudi conto economico** può essere utilizzato più di una volta. Se in seguito alla chiusura dei conti economici il processo batch viene nuovamente eseguito, sarà possibile effettuare registrazioni in un anno fiscale precedente.

## <a name="see-also"></a>Vedere anche

[Chiudere i libri](year-close-books.md)    
[Pubblicare la registrazione di chiusura di fine anno](year-how-post-year-end-close-entry.md)    
[Lavorare con periodi contabili e anni fiscali](finance-accounting-periods-and-fiscal-years.md)    
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
