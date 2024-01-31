---
title: Impostare l'IVA ad esigibilità differita
description: 'Se si utilizza contabilità basata su contanti, è possibile specificare come gestire l''IVA ad esigibilità differita per le vendite e acquisti.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'cash, VAT, unrealized, cash-based'
ms.search.form: '118, 472, 473'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# Setup dell'IVA ad esigibilità differita per la contabilità basata su contanti

Se si utilizzano metodi di contabilità basata su contanti, è possibile impostare [!INCLUDE[prod_short](includes/prod_short.md)] affinché gestisca l'IVA ad esigibilità differita.

## Per utilizzare conti C/G per l'IVA ad esigibilità differita

Gli importi IVA possono essere calcolati e registrati in un conto di contabilità generale temporaneo al momento della registrazione di una fattura, quindi registrati nel conto corretto e inclusi nelle dichiarazioni IVA al momento della registrazione del pagamento effettivo della fattura. Prima di effettuare questa operazione, è necessario completare l'[impostazione della registrazione dell'IVA](finance-setup-vat.md).

Per utilizzare conti per l'IVA ad esigibilità differita, procedere nel modo seguente:

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup contabilità generale**.
2. Nella pagina **Setup contabilità generale** selezionare la casella di controllo **IVA ad esigibilità differita**.
3. Scegli l'icona **Cerca pagina o report** ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") e immetti **Setup registrazione IVA**.
4. Nella pagina **Setup registrazioni IVA** selezionare la categoria di registrazione IVA, quindi scegliere l'azione **Modifica**.
5. Nel campo **Ripart. IVA ad esig. diff.** scegliere un'opzione per specificare come assegnare i pagamenti all'importo di una fattura (IVA esclusa) e all'importo stesso dell'IVA e come trasferire gli importi dell'IVA dal conto IVA ad esigibilità differita al conto realizzato. Nella seguente tabella vengono illustrate le opzioni.

| Opzione | Descrizione |
| --- | --- |
| Vuoto | Scegliere questa opzione se non si desidera utilizzare la funzione IVA ad esigibilità differita. |
| Percentuale | I pagamenti coprono sia l'IVA che l'importo della fattura, proporzionalmente alla percentuale di pagamento dell'importo totale della fattura. L'importo dell'IVA pagato viene trasferito dal conto IVA ad esigibilità differita al conto IVA realizzata. |
| Primo | I pagamenti coprono prima l'IVA e dopo gli importi delle fatture. In tal caso, l'importo trasferito dal conto dell'IVA ad esigibilità differita al conto dell'IVA sarà uguale all'importo del pagamento finché non verrà pagato l'importo totale dell'IVA. |
| Ultimo | I pagamenti coprono prima l'importo della fattura e dopo l'IVA. In tal caso, non verrà trasferito alcun importo dal conto dell'IVA ad esigibilità differita al conto dell'IVA finché non verrà pagato l'importo totale della fattura, esclusa l'IVA. |
| Primo (Interam. Pagato) | I pagamenti copriranno prima l'IVA (come con l'opzione _Primo_), ma non verrà trasferito alcun importo sul conto dell'IVA finché non verrà pagato l'importo totale dell'IVA. |
| Ultimo (Interam. Pagato) | I pagamenti copriranno prima l'importo della fattura (come con l'opzione _Ultimo_), ma non verrà trasferito alcun importo sul Conto IVA finché non verrà pagato l'importo totale dell'IVA. |

6. Nel campo **Conto IVA ven. ad esig. diff.** scegliere il conto per l'IVA di vendita ad esigibilità differita.

    > [!NOTE]  
    > L'importo dell'IVA verrà registrato su questo conto e vi rimarrà fino alla registrazione del pagamento effettuato dal cliente. L'importo viene quindi trasferito sul conto relativo all'IVA sulle vendite.
7. Nel campo **Conto IVA acq. ad esig. diff.** immettere il conto contabilità generale per l'IVA di acquisto ad esigibilità differita.

> [!NOTE]  
> L'importo dell'IVA verrà registrato su questo conto e vi rimarrà fino alla registrazione del pagamento effettuato dal cliente. L'importo viene quindi trasferito sul conto relativo all'IVA sugli acquisti.

## Vedere anche
[Setup dei calcoli e registrazione dei metodi per l'IVA](finance-setup-vat.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
