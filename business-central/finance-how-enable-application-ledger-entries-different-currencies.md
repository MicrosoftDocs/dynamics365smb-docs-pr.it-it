---
title: Collegare i movimenti in diverse valute
description: 'Se si effettua una vendita in una valuta e si riceve il pagamento in un''altra, è possibile collegare il movimento contabile in più valute.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'multiple currencies, payment, reconcile'
ms.search.form: '148, 460, 25'
ms.date: 04/01/2021
ms.author: bholtorf
---
# Abilitare il collegamento dei movimenti contabili fornitore in valute diverse

Se si acquista da un fornitore con una valuta e si paga con un'altra valuta, è possibile collegare il pagamento all'acquisto.

In modo analogo, se si effettua una vendita a un cliente in una valuta e si riceve il pagamento in un'altra, è possibile collegare il pagamento alla fattura di vendita.

Nella procedura riportata di seguito viene descritto come configurare questa impostazione per i movimenti contabili fornitori nella pagina **Setup contabilità fornitori e acquisti**. L'impostazione è simile per i movimenti contabili clienti nella pagina **Setup contabilità clienti e vendite**.

## Per abilitare il collegamento dei movimenti contabili fornitore in valute diverse

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Setup contabilità fornitori**, quindi scegli il collegamento correlato.
2. Nel campo **Collegamenti tra valute** selezionare una delle seguenti opzioni:

| Opzione | Descrizione |
| --- | --- |
| Nessuno |Collegamento fra valute non consentito. |
| UE |Collegamento fra valute UE consentito |
| Tutto |Collegamento fra tutte le valute consentito |

## Per impostare i conti C/G per le differenze di arrotondamento di applicazione delle valute

Se movimenti in diverse valute vengono collegati, è necessario impostare il conto di contabilità generale in cui verranno registrate le differenze di arrotondamento.  

> [!NOTE]  
> È necessario impostare i conti di contabilità generale prima di completare il task. Per ulteriori informazioni, vedere [Contabilità generale e piano dei conti](finance-general-ledger.md).

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Cat. reg. clienti**, quindi scegli il collegamento correlato.  
2. Nei campi **Conto dare arrot. coll. val.** e **Conto avere arrot. coll. val.** immettere i conti di contabilità generale pertinenti per registrare le differenze di arrotondamento.  
3. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Cat. reg. fornitori**, quindi scegli il collegamento correlato.  
4. Nei campi **Conto dare arrot. coll. val.** e **Conto avere arrot. coll. val.** immettere i conti di contabilità generale pertinenti per registrare le differenze di arrotondamento.  

## Vedi il relativo [training Microsoft](/training/modules/process-foreign-currency-payments-dynamics-365-business-central/)

## Vedere anche

[Gestione della contabilità fornitori](payables-manage-payables.md)  
[Gestione della contabilità clienti](receivables-manage-receivables.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
