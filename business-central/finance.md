---
title: Gestione finanziaria (video)
description: 'Scopri come Business Central supporta le esigenze di gestione finanziaria, contabilità, controllo e contabilità.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.search.keywords: 'accounting, auditing, bookkeeping'
ms.search.form: '1151, 1166, 9027, 9004'
ms.date: 02/01/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Gestione contabile

[!INCLUDE[prod_short](includes/prod_short.md)] include una configurazione standard per la maggior parte dei processi finanziari. Tuttavia, tale configurazione può essere adattata alle esigenze aziendali. Per ulteriori informazioni, vedi [Impostazione degli aspetti finanziari](finance-setup-finance.md).

La configurazione predefinita include un piano dei conti e le categorie di registrazione standard che consentono di rendere più efficiente il processo di assegnazione dei conti C/G predefiniti a clienti, fornitori e articoli.  

Nelle sezioni seguenti viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.  

## Guardare un video

Questo video presenta alcune delle funzionalità chiave per la gestione delle finanze. <br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE4Fss4?rel=0]

## Iniziare con le funzionalità finanziarie

Prima di poter iniziare a gestire la propria attività, è necessario specificare come si desidera gestire i processi finanziari dell'azienda.

|Per...| Vedere |
|---|---|
| Modificare la configurazione standard di [!INCLUDE[prod_short](includes/prod_short.md)] per la maggior parte dei processi finanziari in modo da adattarla alle proprie esigenze aziendali. | [Impostazione di dati finanziari](finance-setup-finance.md) | 
| Informazioni sulla contabilità generale e sul piano dei conti. |[Informazioni sulla contabilità generale e COA](finance-general-ledger.md) |

## Contabilità

In questa sezione vengono descritti alcuni degli strumenti contabili utilizzati per registrare le transazioni finanziarie in modo che soddisfino i requisiti di registrazione, creazione di report e finanza gestionale.

| Per... | Vedere |
| --- | --- |
| Aggiungere le dimensioni per Business Intelligence più dettagliata. |[Usare le dimensioni](finance-dimensions.md) |
|Imparare a utilizzare valute aggiuntive e ad aggiornare i tassi di cambio automaticamente. |[Aggiornare i tassi di cambio valuta](finance-how-update-currencies.md)|
| Alloca i ricavi e le spese a periodi diversi da quando sono state effettivamente registrate le transazioni. |[Rateizzare le entrate e le uscite](finance-how-defer-revenue-expenses.md)|
|Assegnare un movimento in una registrazione generale a più conti, quando tale registrazione viene contabilizzata. |[Allocazione di costi e ricavi](year-allocate-costs-income.md) |
| Assegna costi aggiuntivi, quali il trasporto e la gestione fisica sopportata durante il commercio, agli articoli interessati. In questo modo il costo si riflette nella valutazione dell'inventario. |[Usare gli addebiti articolo al conto per i costi aggiuntivi commerciali](payables-how-assign-item-charges.md) |
| Informazioni sulle opzioni disponibili per automatizzare il modo in cui si inviano le fatture di abbonamento ai clienti e registrare il ricavo periodico. |[Utilizzo del ricavo ricorrente](finance-recurring-invoicing.md)|
|Registra le spese dei dipendenti per attività legate al lavoro ed effettua rimborsi direttamente sui conti bancari dei dipendenti.|[Registrare e rimborsare le spese dei dipendenti](finance-how-record-reimburse-employee-expenses.md)|

## IVA e tasse

L'utilizzo dell'IVA in [!INCLUDE[prod_short](includes/prod_short.md)] è semplice e puoi utilizzare la configurazione manuale o automatica. Questi articoli forniscono informazioni su come soddisfare le normative specifiche del proprio paese/area geografica.

| Per... | Vedere |
| --- | --- |
|Calcola l'imposta sul valore aggiunto (VAT) sulle transazioni di vendita e acquisto in modo da segnalare gli importi alle autorità fiscali.|[Utilizzare l'IVA nelle vendite e negli acquisti](finance-work-with-vat.md)|
|Preparare un report che elenca l'IVA di vendita e inviare il report alle autorità fiscali in Unione Europea (UE). | [Dichiarare l'IVA all'autorità fiscale](finance-how-report-vat.md)|
|Convertire manualmente i contratti di servizio per modificare la loro aliquota VAT.|[Convertire i contratti di servizio che includono importi IVA](service-how-to-convert-service-contracts.md)|

## Gestire crediti e debiti

Il nucleo della finanza è incentrato sulla gestione dei crediti e dei debiti, sulla registrazione delle transazioni, sulla riconciliazione dei conti bancari, sul pagamento dei fornitori, sulla ricezione dei pagamenti dei clienti, sul rimborso delle spese ai dipendenti e così via. Questa sezione fornisce collegamenti ai concetti principali.

| Per... | Vedere |
| --- | --- |
| Collegare i pagamenti in entrata, riconciliare i conti bancari durante il collegamento di pagamento e riscuotere i saldi inevasi. |[Gestione della contabilità clienti](receivables-manage-receivables.md) |
| Effettuare i pagamenti, collegare i pagamenti in uscita e utilizzare gli assegni. |[Gestione della contabilità fornitori](payables-manage-payables.md) |
|Chiedere ai clienti di pagare prima che venga spedita loro la merce o di pagare i fornitori prima che questi spediscano la merce.|[Fatturazione dei pagamenti anticipati](finance-invoice-prepayments.md)|
| Riconciliare e trasferire fondi tra conti bancari. |[Riconciliazione dei conti correnti bancari](bank-manage-bank-accounts.md) |

## Gestire più società

[!INCLUDE [prod_short](includes/prod_short.md)] offre alle piccole e medie imprese una soluzione di gestione aziendale facile da usare e da mantenere a un basso costo di proprietà.

| Per... | Vedere |
| --- | --- |
|Impostare i partner intercompany ed elaborare le transazioni, manualmente o automaticamente, tra le persone giuridiche all'interno della stessa società.|[Gestione delle transazioni Intercompany](intercompany-manage.md)|
|Combinare i movimenti di contabilità generale di più società in una "società consolidata“ virtuale per analisi finanziarie.|[Consolidare dati finanziari di molteplici società](finance-consolidated-company-reporting.md)|
| Lavora a stretto contatto con le aziende correlate a cui hai accesso e per ottenere informazioni sui dati dei punti di interesse chiave (KPI). | [Gestire il lavoro tra più aziende nell'hub aziendale](company-hub.md)|

## Creazione di report di fine periodo e attività correlate

Alla fine di ogni periodo contabile o alla fine dell'anno fiscale, ci sono una serie di attività amministrative da svolgere. Ad esempio, probabilmente vorrai assicurarti che tutti i documenti e i giornali di registrazione siano pubblicati, assicurarti che i dati sulla valuta siano aggiornati, chiudere i libri e così via. Le attività effettive dipenderanno dalla società.

| Per... | Vedere |
| --- | --- |
|Gestire i costi di magazzino e di produzione, creare report dei costi e riconciliare i costi con la contabilità generale.|[Gestione dei costi di magazzino](finance-manage-inventory-costs.md)|
| Importare le transazioni degli stipendi dal sistema di gestione delle retribuzioni nella contabilità generale. |[Importare transazioni retribuzioni](finance-how-import-payroll-transactions.md)|
|Informazioni su come utilizzare Gestione ruolo utente Contabile, invitare un contabile esterno e utilizzare l'hub aziendale per gestire i conti relativi a più client.|[Esperienze di contabile in Business Central](finance-accounting.md)| 

## Contabilità gestionale

In qualità di responsabile o controller aziendale, è importante che tu possa preparare e analizzare i dati aziendali necessari per prendere decisioni informate. Gli articoli nella tabella seguente aiutano a preparare i dati. Per ulteriori informazioni sull'analisi, vai a [Panoramica di Business Intelligence e creazione di report](reports-bi-reporting.md).

| Per... | Vedere |
| --- | --- |
|Analizzare i costi di gestione dell'azienda allocando i costi effettivi e a budget di operazioni, dipartimenti, prodotti e progetti a centri di costo.|[Contabilizzazione dei costi](finance-manage-cost-accounting.md)|
| Monitorare il flusso dei contanti in entrata e in uscita dell'azienda. |[Analizzare i flussi di cassa della società](finance-analyze-cash-flow.md) |
|Segui una procedura end-to-end sull'utilizzo dei report finanziari per fare previsioni sul flusso di cassa.|[Procedura dettagliata: Esecuzione di previsioni di flusso di cassa utilizzando i report finanziari](walkthrough-making-cash-flow-forecasts-by-using-account-schedules.md)|
| Utilizzare i rendiconti finanziari e le sintesi fornite in Microsoft Excel. |[Analisi dei rendiconti finanziari in Excel](finance-analyze-excel.md) |

## Moduli di e-learning gratuiti

Desideri ottenere altre informazioni su [!INCLUDE[prod_short](includes/prod_short.md)] al tuo ritmo? 

[!INCLUDE[footer-include](includes/footer-banner.md)]

## Vedere anche

[Impostazione di dati finanziari](finance-setup-finance.md)  
[Lavorare con il modulo Vendite](sales-manage-sales.md)  
[Lavorare con il modulo Acquisti](purchasing-manage-purchasing.md)  
[Chiusura di periodi fiscali](year-close-years-periods.md)  
[Gestione di progetti](projects-manage-projects.md)  
[Importazione dei dati aziendali da altri sistemi contabili](across-import-data-configuration-packages.md)  
[Utilizzo delle registrazioni COGE](ui-work-general-journals.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]