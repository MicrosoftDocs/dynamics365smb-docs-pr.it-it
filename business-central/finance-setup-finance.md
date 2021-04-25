---
title: Impostare i processi finanziari| Documenti Microsoft
description: Informazioni sulle attività per impostare i dati finanziari nella propria attività per adattarli alle esigenze di contabilità, controllo e gestione dei libri contabili.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accounting, auditing, bookkeeping
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: f93eaa38b07a5135aafa22b21253d1e99a8d0406
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788104"
---
# <a name="setting-up-finance"></a>Impostazione di dati finanziari
Prima di poter iniziare a gestire la propria attività, è necessario specificare le regole e i valori predefiniti per impostare come si desidera gestire i processi finanziari per quella società. Innanzitutto, impostare le basi dei record contabili della società, vale a dire il piano dei conti, dopodiché è necessario procedere all'impostazione delle categorie di registrazione che contribuiscono a rendere più efficiente il processo di assegnazione dei conti delle registrazioni della contabilità generale di default a clienti, fornitori e articoli.

Alcune impostazioni finanziarie possono essere eseguite automaticamente con le guide del setup assistita, mentre altre devono essere eseguite manualmente. Per ulteriori informazioni, vedere [Preparazione al business](ui-get-ready-business.md).

È possibile utilizzare dimensioni per aggiungere tipi diversi di informazioni a ogni transazione. È possibile impostare le dimensioni di base della società, ad esempio Progetti e Reparti. In seguito, sarà possibile aggiungere ulteriori dimensioni e impostare dimensioni temporanee da utilizzare in un periodo di tempo limitato, ad esempio in occasione di una campagna di vendita. Per ulteriori informazioni, vedere [Utilizzo delle dimensioni](finance-dimensions.md).

Molti dei task di impostazione devono essere completati prima di avviare la registrazione delle transazioni finanziarie, anche se molte impostazioni potranno essere modificate in un momento successivo. Alcuni dei task di impostazione sono facoltativi, ad esempio si imposteranno consolidamenti e registrazioni intercompany solo se si lavora con più società. Alcuni task di impostazione, ad esempio la definizione del periodo in cui è consentita la registrazione, è possibile che debbano essere ripetuti periodicamente.  

Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.

| A | Vedere |
| --- | --- |
| Specificare come si desidera essere pagato dai clienti e come pagare i fornitori. |[Impostare i metodi di pagamento](finance-payment-methods.md) |
| Specificare le condizioni pagamento per gestire le date di scadenza e per calcolare eventuali sconti pagamento.|[Impostare le condizioni pagamento](finance-payment-terms.md) |
| Specificare le categorie di registrazione che associano entità come clienti, fornitori, articoli, risorse e documenti di vendita o di acquisto a conti di contabilità generale. |[Impostazione delle categorie di registrazione](finance-posting-groups.md)|
|Creare le situazioni contabili e definire le categorie di conti per definire il contenuto dei grafici e dei report finanziari, ad esempio i report di conto patrimoniale e conto economico.|[Preparare i rendiconti finanziari con le situazioni contabili e le categorie di conti](bi-how-work-account-schedule.md)|
|Impostare una tolleranza da cui il sistema chiude una fattura anche se il pagamento, incluso un eventuale sconto, non copre interamente l'importo della fattura.|[Utilizzare le tolleranze pagamento e le tolleranze sconto pagamento](finance-payment-tolerance-and-payment-discount-tolerance.md)|
| Impostare periodi fiscali. |[Utilizzare periodi contabili e anni fiscali](finance-accounting-periods-and-fiscal-years.md) |
|Impostare termini di sollecito per riscuotere pagamenti in ritardo.|[Impostare i termini e i livelli di sollecito](finance-setup-reminders.md)|
| Definire come dichiarare alle autorità fiscali gli importi dell'imposta sul valore aggiunto (IVA) raccolti per le vendite. |[Impostare l'IVA (imposta sul valore aggiunto)](finance-setup-vat.md)|
|Preparare la gestione dell'IVA ad esigibilità differita in connessione con metodi di contabilità basata su contanti.|[Setup dell'IVA ad esigibilità differita per la contabilità basata su contanti](finance-setup-unrealized-vat.md)|
| Impostare le funzionalità Vendite e acquisti per gestire i pagamenti in valute estere.|[Abilitare il collegamento dei movimenti contabili fornitore in valute diverse](finance-how-enable-application-ledger-entries-different-currencies.md)
|Definire una o più valute aggiuntive in modo da indicare automaticamente gli importi sia nella valuta corrente sia nella seconda valuta in ogni movimento C/G e in altri movimenti.|[Impostare una valuta contabile addizionale](finance-how-setup-additional-currencies.md)|
|Rettificare periodicamente gli equivalenti della valuta addizionale per compensare tassi di cambio fluttuanti.|[Aggiornare i tassi di cambio valuta](finance-how-update-currencies.md)|
|Definire molteplici tassi di interesse da utilizzare in periodi differenti per pagamenti in ritardo nelle transazioni commerciali.|[Impostare più tassi d'interesse](finance-how-to-set-up-multiple-interest-rates.md)|
|Preparare l'arrotondamento automatico degli importi delle fatture quando si creano fatture.|[Impostare l'arrotondamento delle fatture](finance-set-up-invoice-rounding.md)|
| Aggiungere nuovi conti a un piano dei conti esistente. |[Impostazione del piano dei conti](finance-setup-chart-accounts.md) |
| Impostare i grafici di business intelligence (BI) per analizzare il flusso di cassa. |[Impostazione di un'analisi di un flusso di cassa](finance-setup-cash-flow-analyses.md) |
|Abilitazione della fatturazione di un cliente che non è impostato nel sistema.|[Impostare i clienti per vendite in contanti](finance-how-to-set-up-cash-customers.md)|
| Impostare la creazione di report Intrastat e inviare il report a un'autorità | [Impostare e registrare report Intrastat](finance-how-setup-report-intrastat.md)|
|Assicurarsi che un movimento in una registrazione generale sia allocato a più conti diversi quanto tale registrazione viene contabilizzata, in base alla quantità, alla percentuale o all'importo.|[Utilizzare le chiavi di allocazione nelle registrazioni COGE](ui-how-use-allocation-keys-general-journals.md)|
|Impostare i codici sorgente e le causali da utilizzare per tenere traccia degli audit trail.|[Impostazione di codici sorgente e causali per audit trail](finance-setup-trail-codes.md)|
|Specificare report predefiniti da utilizzare per diversi tipi di documenti.|[Selezione report in Business Central](across-report-selections.md)|

> [!TIP]
> A seconda della posizione geografica, alcune pagine possono contenere campi non descritti negli articoli qui elencati perché si applicano a funzionalità o personalizzazioni locali. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

## <a name="see-related-training-at-microsoft-learn"></a>Vedere le informazioni relative al training in [Microsoft Learn](/learn/paths/set-up-financial-management-dynamics-365-business-central/)

## <a name="see-also"></a>Vedere anche

[Finanze](finance.md)  
[Riconciliazione dei conti correnti bancari](bank-manage-bank-accounts.md)  
[Utilizzo delle dimensioni](finance-dimensions.md)  
[Importazione dei dati aziendali da altri sistemi contabili](across-import-data-configuration-packages.md)  
[Analizzare il flusso di cassa dell'azienda](finance-analyze-cash-flow.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]