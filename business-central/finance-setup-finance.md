---
title: Impostare i processi finanziari| Documenti Microsoft
description: Informazioni sulle attività per impostare i dati finanziari nella propria attività per adattarli alle esigenze di contabilità, controllo e gestione dei libri contabili.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accounting, auditing, bookkeeping
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: c64b58c036395764191c05f47f8327c6479a4c6f
ms.sourcegitcommit: dac212009aadf3227e54c99976c438f6e56f182a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/02/2019
ms.locfileid: "1447039"
---
# <a name="setting-up-finance"></a>Impostazione di dati finanziari
Per velocizzare l'inizio, [!INCLUDE[d365fin](includes/d365fin_md.md)] include le configurazioni di default della maggior parte dei processi finanziari. Se è necessario apportare modifiche alle configurazioni per adattarle alla propria attività, procedere subito. Ad esempio, nella Gestione ruolo utente, è possibile utilizzare la guida al setup assistito per configurare l'aliquota in base all'ubicazione.  

Tuttavia, esistono alcune opzioni che occorre impostare manualmente. Ad esempio, se si desidera utilizzare le dimensioni come base per la categoria di business intelligence.  

Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.

| Per | Vedere |
| --- | --- |
| Scegliere la modalità di pagamento dei fornitori. |[Definizione dei metodi di pagamento](finance-payment-methods.md) |
| Specificare le categorie di registrazione che associano entità come clienti, fornitori, articoli, risorse e documenti di vendita o di acquisto a conti di contabilità generale. |[Impostazione delle categorie di registrazione](finance-posting-groups.md)|
|Creare le situazioni contabili e definire le categorie di conti per definire il contenuto dei grafici e dei report finanziari, ad esempio i report di conto patrimoniale e conto economico.|[Preparare i rendiconti finanziari con le situazioni contabili e le categorie di conti](bi-how-work-account-schedule.md)|
|Impostare una tolleranza da cui il sistema chiude una fattura anche se il pagamento, incluso un eventuale sconto, non copre interamente l'importo della fattura.|[Utilizzare le tolleranze pagamento e le tolleranze sconto pagamento](finance-payment-tolerance-and-payment-discount-tolerance.md)|
| Impostare periodi fiscali. |[Aprire un nuovo anno fiscale](finance-how-open-new-fiscal-year.md) |
| Definire come dichiarare alle autorità fiscali gli importi dell'imposta sul valore aggiunto (IVA) raccolti per le vendite. |[Impostazione dei calcoli e registrazione dei metodi per l'IVA](finance-setup-vat.md)|
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

## <a name="see-also"></a>Vedi anche
[Finanze](finance.md)  
[Gestione di conti correnti bancari](bank-manage-bank-accounts.md)  
[Utilizzo delle dimensioni](finance-dimensions.md)  
[Importazione dei dati aziendali da altri sistemi contabili](across-import-data-configuration-packages.md)  
[Analizzare il flusso di cassa dell'azienda](finance-analyze-cash-flow.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
