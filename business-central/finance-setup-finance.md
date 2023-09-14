---
title: Impostare i processi finanziari
description: 'Informazioni sulle attività necessarie per impostare i dati finanziari nella propria attività per adattarli alle esigenze di contabilità, controllo e gestione dei libri contabili.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'accounting, auditing, bookkeeping'
ms.date: 08/19/2022
ms.author: bholtorf
---
# Impostazione di dati finanziari

Prima di poter iniziare a gestire la propria attività, è necessario specificare come si desidera gestire i processi finanziari. Innanzitutto, imposta le basi dei record contabili della società, vale a dire il piano dei conti. Dopodiché è necessario procedere all'impostazione delle categorie di registrazione che contribuiscono a rendere più efficiente il processo di assegnazione dei conti delle registrazioni della contabilità generale di default a clienti, fornitori e articoli.

Alcune impostazioni finanziarie possono essere eseguite automaticamente con le guide del setup assistita, mentre altre devono essere eseguite manualmente. Ulteriori informazioni in [Prepararsi a fare affari](ui-get-ready-business.md). La pagina **Setup contabilità generale** specifica la modalità di gestione dei diversi processi contabili della società. Utilizza ad esempio questa pagina per specificare i dettagli relativi all'arrotondamento delle fatture, il codice valuta per la valuta locale, il formato degli indirizzi e se vuoi o meno utilizzare una valuta contabile addizionale. Per ulteriori informazioni, vedi [Informazioni sulla contabilità generale e sul piano dei conti](finance-general-ledger.md).  

È possibile utilizzare dimensioni per aggiungere tipi diversi di informazioni a ogni transazione. È possibile impostare le dimensioni di base della società, ad esempio *Progetti* e *Reparti*. In seguito, aggiungi più dimensioni quando ne hai bisogno. Ad esempio, puoi impostare dimensioni temporanee da utilizzare per un periodo di tempo limitato, ad esempio durante una campagna di vendita. Per ulteriori informazioni, vedi [Utilizzare le dimensioni](finance-dimensions.md).

Molti dei task di impostazione devono essere completati prima di avviare la registrazione delle transazioni finanziarie, ma molte impostazioni possono essere modificate come necessario. Detto questo, ci sono anche task di configurazione facoltativi. Ad esempio, è necessario impostare registrazioni e consolidamenti interaziendali solo se si lavora con più società. E altri task di impostazione, ad esempio la definizione del periodo in cui è consentita la registrazione, è possibile che debbano essere ripetuti periodicamente.  

Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.

| A | Vedere |
| --- | --- |
|Visualizzare o modificare i conti di contabilità generale in cui tutti i movimenti di contabilità generale sono registrati|[Impostare o modificare il piano dei conti](finance-setup-chart-accounts.md)|
| Specificare come si desidera essere pagato dai clienti e come pagare i fornitori. |[Impostare i metodi di pagamento](finance-payment-methods.md) |
| Specifica le condizioni pagamento per gestire le date di scadenza e per calcolare eventuali sconti pagamento.|[Impostare le condizioni pagamento](finance-payment-terms.md) |
| Specificare le categorie di registrazione che associano entità come clienti, fornitori, articoli, risorse e documenti di vendita o di acquisto a conti di contabilità generale. |[Configurazione delle categorie di registrazione](finance-posting-groups.md)|
|Crea report finanziari e definisci le categorie di conti per determinare il contenuto dei grafici e dei report finanziari, ad esempio i report di conto patrimoniale e conto economico.|[Preparare Financial Reporting con i dati finanziari e le categorie di conti](bi-how-work-account-schedule.md)|
|Imposta una tolleranza con cui il sistema chiude una fattura anche se il pagamento, incluso un eventuale sconto, non copre interamente l'importo della fattura.|[Utilizzare le tolleranze pagamento e le tolleranze sconto pagamento](finance-payment-tolerance-and-payment-discount-tolerance.md)|
| Impostare periodi fiscali. |[Utilizzare periodi contabili e anni fiscali](finance-accounting-periods-and-fiscal-years.md) |
|Imposta i termini di fatturazione che ricordano ai tuoi clienti di effettuare il pagamento.|[Impostare i termini e i livelli di sollecito](finance-setup-reminders.md)|
| Definisci come dichiarare alle autorità fiscali gli importi dell'imposta sul valore aggiunto (IVA) raccolti per le vendite. |[Impostare l'IVA (imposta sul valore aggiunto)](finance-setup-vat.md)|
|Preparare la gestione dell'IVA ad esigibilità differita in connessione con metodi di contabilità basata su contanti.|[Setup dell'IVA ad esigibilità differita per la contabilità basata su contanti](finance-setup-unrealized-vat.md)|
|Definisci le valute estere in cui fai trading o crei i report per le transazioni.|[Impostare le valute](finance-set-up-currencies.md)|
| Imposta le funzionalità Vendite e acquisti per gestire i pagamenti in valute estere.|[Abilitare il collegamento dei movimenti contabili fornitore in valute diverse](finance-how-enable-application-ledger-entries-different-currencies.md)
|Definisci una o più valute aggiuntive in modo da indicare automaticamente gli importi sia nella valuta locale (VL) sia nella seconda valuta in ogni movimento di contabilità generale (C/G) e in altri movimenti.|[Impostare una valuta contabile addizionale](finance-how-setup-additional-currencies.md)|
|Rettificare periodicamente gli equivalenti della valuta addizionale per compensare tassi di cambio fluttuanti.|[Aggiornare i tassi di cambio valuta](finance-how-update-currencies.md)|
|Definisci molteplici tassi di interesse da utilizzare in periodi differenti per pagamenti in ritardo nelle transazioni commerciali.|[Impostare più tassi d'interesse](finance-how-to-set-up-multiple-interest-rates.md)|
|Fai in modo che gli importi vengano arrotondati automaticamente durante la creazione delle fatture.|[Impostare l'arrotondamento delle fatture](finance-set-up-invoice-rounding.md)|
| Aggiungere nuovi conti a un piano dei conti esistente. |[Impostazione del piano dei conti](finance-setup-chart-accounts.md) |
| Impostare i grafici di business intelligence (BI) per analizzare il flusso di cassa. |[Impostazione di un'analisi di un flusso di cassa](finance-setup-cash-flow-analyses.md) |
|Abilita la fatturazione di un cliente che non è impostato nel sistema.|[Impostare i clienti per vendite in contanti](finance-how-to-set-up-cash-customers.md)|
| Imposta la creazione di report Intrastat e invia il report a un'autorità. | [Impostare e registrare report Intrastat](finance-how-setup-report-intrastat.md)|
|Assicurati che un movimento contabile sia allocato tra conti diversi, ad esempio quantità, percentuale o importo, quando lo registri nel giornale di registrazione.|[Utilizzare le chiavi di allocazione nelle registrazioni COGE](ui-how-use-allocation-keys-general-journals.md)|
|Imposta i codici origine e le causali per tenere traccia degli audit trail.|[Impostazione di codici sorgente e causali per audit trail](finance-setup-trail-codes.md)|
|Specificare report predefiniti da utilizzare per diversi tipi di documenti.|[Selezione report in Business Central](across-report-selections.md)|

> [!TIP]
> A seconda della posizione geografica, alcune pagine di Business Central possono contenere campi non descritti negli articoli qui elencati perché si applicano a funzionalità o personalizzazioni locali. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

## Vedi il relativo [training Microsoft](/training/paths/set-up-financial-management-dynamics-365-business-central/)

## Vedere anche

[Finanze](finance.md)  
[Riconciliazione dei conti correnti bancari](bank-manage-bank-accounts.md)  
[Utilizzare le dimensioni](finance-dimensions.md)  
[Importazione dei dati aziendali da altri sistemi contabili](across-import-data-configuration-packages.md)  
[Analizzare il flusso di cassa dell'azienda](finance-analyze-cash-flow.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
