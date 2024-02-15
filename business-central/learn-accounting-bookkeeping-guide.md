---
title: Contabilità e tenuta dei libri
description: Questo articolo fornisce informazioni che ti aiuteranno a utilizzare Microsoft Dynamics 365 Business Central per eseguire correttamente la contabilità e la tenuta dei libri per la tua azienda.
author: altotovi
ms.topic: overview
ms.devlang: al
ms.search.keywords: 'accounting, bookkeeping'
ms.search.form: '16, 39, 108'
ms.date: 03/14/2023
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# <a name="accounting-and-bookkeeping"></a>Contabilità e tenuta dei libri

La contabilità è una funzione fondamentale in qualsiasi soluzione di pianificazione delle risorse aziendali (ERP) nonché nella maggior parte delle aziende. La contabilità rappresenta il processo di registrazione e catalogazione delle transazioni finanziarie di un'azienda e quindi il recupero, la misurazione, la sintesi e la presentazione dei risultati utilizzando differenti report spesso richiesti dalla legislazione locale. L'obiettivo principale di questo processo è aiutare la direzione dell'azienda a comprendere i dati finanziari della stessa e misurare i risultati delle attività economiche dell'azienda.

La tenuta dei libri è una parte del processo contabile e comporta di registrare regolarmente tutte le transazioni finanziarie in un'azienda. [!INCLUDE[prod_short](includes/prod_short.md)] è un sistema ERP che include strumenti integrati per semplificare la tenuta dei libri nel sistema. Molte azioni possono essere eseguite manualmente o automaticamente.

Questo articolo fornisce una panoramica dei processi di tenuta dei libri, comprese le regole, le procedure e altre linee guida in [!INCLUDE[prod_short](includes/prod_short.md)]. Il contenuto di questo articolo ha lo scopo di aiutare contabili e ragionieri a completare il loro lavoro quotidiano in questo sistema ERP. Per ulteriore assistenza, [!INCLUDE[prod_short](includes/prod_short.md)] include un assistente basato sul contesto. Questo assistente contiene collegamenti a informazioni correlate alla pagina corrente e istruzioni per utilizzare il processo pertinente. Per accedervi, seleziona il pulsante [**Guida**](product-help-and-support.md) nell'angolo in alto a destra per aprire il riquadro **Guida**. Utilizza quindi i collegamenti nelle sezioni **Informazioni sull'attività o sulla pagina** e **Risorse correlate di Microsoft Learn**.

Il video seguente presenta alcune delle funzionalità chiave per la contabilità e la tenuta dei libri.

> [!Video https://www.microsoft.com/videoplayer/embed/RE4Fss4?rel=0]

La tabella seguente descrive una sequenza di attività e fornisce collegamenti agli articoli che le descrivono.

| Attività | Articolo |
|------|---------|
| Visualizzare o modificare i conti CoGe in cui sono registrati tutti i movimenti di contabilità generale. | [Impostare o modificare il piano dei conti](finance-setup-chart-accounts.md) |
| Specificare la modalità di pagamento dei clienti e quella dei fornitori. | [Impostare i metodi di pagamento](finance-payment-methods.md) |
| Specificare le condizioni pagamento per gestire le date di scadenza e per calcolare eventuali sconti pagamento. | [Impostare le condizioni pagamento](finance-payment-terms.md) |
| Specificare le categorie di registrazione che associano entità (come clienti, fornitori, articoli, risorse e documenti di vendita o di acquisto) a conti di contabilità generale. | [Configurazione delle categorie di registrazione](finance-posting-groups.md)|
| Creare report finanziari e definire le categorie di conti per determinare il contenuto dei grafici e dei report finanziari, ad esempio i report **Conto patrimoniale** e **Conto economico**. | [Preparare il reporting finanziario con i dati finanziari e le categorie di conti](bi-how-work-account-schedule.md)|
| Impostare una tolleranza con cui il sistema chiude una fattura anche se il pagamento, incluso un eventuale sconto, non copre interamente l'importo della fattura. | [Usare le tolleranze pagamento e le tolleranze sconto pagamento](finance-payment-tolerance-and-payment-discount-tolerance.md) |
| Impostare periodi fiscali. | [Utilizzare periodi contabili e anni fiscali](finance-accounting-periods-and-fiscal-years.md) |
| Impostare i termini di fatturazione che ricordano ai tuoi clienti di effettuare i pagamenti. | [Impostare i termini e i livelli di sollecito](finance-setup-reminders.md)|
| Definire come dichiarare alle autorità fiscali gli importi dell'imposta sul valore aggiunto (IVA) raccolti per le vendite. | [Impostare l'IVA (imposta sul valore aggiunto)](finance-setup-vat.md) |
| Determinare la gestione dell'IVA ad esigibilità differita in connessione con metodi di contabilità basata su contanti. | [Impostare l'IVA ad esigibilità differita per la contabilità basata su contanti](finance-setup-unrealized-vat.md) |
| Definire le valute estere in cui fai trading o crei i report per le transazioni. | [Impostare le valute](finance-set-up-currencies.md) |
| Impostare le funzionalità di vendite e acquisti per gestire i pagamenti in valute estere. | [Abilitare il collegamento dei movimenti contabili fornitore in valute diverse](finance-how-enable-application-ledger-entries-different-currencies.md) |
| Definire una o più valute aggiuntive in modo da indicare automaticamente gli importi sia nella valuta locale (VL) che in una valuta di dichiarazione addizionale in ogni movimento di contabilità generale e in altri movimenti. | [Impostare una valuta di dichiarazione addizionale](finance-how-setup-additional-currencies.md) |
| Rettificare periodicamente gli equivalenti della valuta addizionale per compensare tassi di cambio fluttuanti. | [Aggiornare i tassi di cambio valuta](finance-how-update-currencies.md)|
| Definire molteplici tassi di interesse per periodi differenti correlati a pagamenti in ritardo nelle transazioni commerciali. | [Impostare più tassi d'interesse](finance-how-to-set-up-multiple-interest-rates.md) |
| Fare in modo che gli importi vengano arrotondati automaticamente durante la creazione delle fatture. | [Impostare l'arrotondamento delle fatture](finance-set-up-invoice-rounding.md) |
| Aggiungere nuovi conti a un piano dei conti esistente (COA). | [Impostazione del piano dei conti](finance-setup-chart-accounts.md) |
| Impostare i grafici di business intelligence (BI) per analizzare il flusso di cassa. | [Impostazione di un'analisi di un flusso di cassa](finance-setup-cash-flow-analyses.md) |
| Abilitare la fatturazione ai clienti che non sono impostati nel sistema. | [Impostare i clienti per vendite in contanti](finance-how-to-set-up-cash-customers.md) |
| Impostare il reporting Intrastat e inviare il report a un'autorità. | [Impostare e registrare report Intrastat](finance-how-setup-report-intrastat.md) |
| Assicurarsi che un movimento contabile sia allocato tra conti diversi, ad esempio quantità, percentuale o importo, quando viene registrato nel giornale di registrazione. | [Usare le chiavi di allocazione nelle registrazioni COGE](ui-how-use-allocation-keys-general-journals.md) |
| Impostare codici origine e causali per tenere traccia degli audit trail. | [Impostazione di codici sorgente e causali per audit trail](finance-setup-trail-codes.md) |
| Specificare i report predefiniti utilizzati per diversi tipi di documenti. | [Selezione report in Business Central](across-report-selections.md) |
| Collegare i pagamenti in entrata, riconciliare i conti bancari durante il collegamento di pagamento e riscuotere i saldi inevasi. | [Gestione della contabilità clienti](receivables-manage-receivables.md) |
| Effettuare i pagamenti, collegare i pagamenti in uscita e utilizzare gli assegni. | [Gestione della contabilità fornitori](payables-manage-payables.md) |
| Chiedere ai clienti di pagare prima che venga spedita loro la merce o di pagare i fornitori prima che questi spediscano la merce. | [Fatturazione dei pagamenti anticipati](finance-invoice-prepayments.md) |
| Riconciliare e trasferire fondi tra conti bancari. | [Riconciliazione dei conti correnti bancari](bank-manage-bank-accounts.md) |
| Impostare partner intercompany ed elaborare transazioni manualmente o automaticamente tra le persone giuridiche nella stessa azienda. | [Gestione delle transazioni Intercompany](intercompany-manage.md) |
| Analizzare i costi di gestione dell'azienda allocando i costi effettivi e a budget di operazioni, dipartimenti, prodotti e progetti a centri di costo. | [Contabilizzazione dei costi](finance-manage-cost-accounting.md) |
| Gestire i costi di magazzino e di produzione, creare report dei costi e riconciliare i costi con la contabilità generale. | [Gestione dei costi di magazzino](finance-manage-inventory-costs.md) |
| Gestire e segnalare flussi di cassa in entrata e in uscita. | [Panoramica del flusso di cassa]( finance-cash-flow-overview.md) |
| Monitorare il flusso dei contanti in entrata e in uscita dell'azienda. | [Analizzare i flussi di cassa della società](finance-analyze-cash-flow.md) |
| Seguire una procedura end-to-end che utilizza report finanziari per fare previsioni sul flusso di cassa. | [Esecuzione di previsioni di flusso di cassa utilizzando i report finanziari](walkthrough-making-cash-flow-forecasts-by-using-account-schedules.md) |
| Ottenere informazioni sulla contabilità generale e sul COA. | [Informazioni sulla contabilità generale e COA](finance-general-ledger.md) |
| Combinare i movimenti di contabilità generale di più società in una "società consolidata“ virtuale per analisi finanziarie. | [Consolidare dati finanziari di molteplici società](finance-consolidated-company-reporting.md)|
| Aggiungere le dimensioni per Business Intelligence più dettagliata. | [Usare le dimensioni](finance-dimensions.md) |
| Creare budget di contabilità generale per prevedere differenti attività finanziarie e assegnare le dimensioni per scopi di business intelligence. | [Creare budget C/G](finance-how-create-budgets.md) |
| Registrare le entrate o le spese direttamente nella contabilità generale senza registrare documenti aziendali dedicati. | [Registrare le transazioni direttamente nella contabilità generale](finance-how-post-transactions-directly.md) |
| Registrare i movimenti di pareggio per annullare le registrazioni dei valori nelle registrazioni o le registrazioni delle quantità sui documenti di vendita e di acquisto. | [Stornare le registrazioni e annullare carichi/spedizioni errati.](finance-how-reverse-journal-posting.md) |
| Assegnare un movimento in una registrazione generale a più conti, quando tale registrazione viene contabilizzata. | [Allocazione di costi e ricavi](year-allocate-costs-income.md) |
| Assegnare costi aggiuntivi, quali trasporto e gestione fisica sopportata durante il commercio, agli articoli interessati. Il costo viene quindi riflesso nella valutazione del magazzino. | [Usare gli addebiti articolo al conto per i costi aggiuntivi commerciali](payables-how-assign-item-charges.md) |
| Registrare le spese dei dipendenti per attività legate al lavoro ed effettuare rimborsi direttamente sui conti bancari dei dipendenti. | [Registrare e rimborsare le spese dei dipendenti](finance-how-record-reimburse-employee-expenses.md) |
| Allocare ricavi e spese a periodi diversi dai periodi in cui sono state effettivamente registrate le transazioni. | [Rateizzare le entrate e le uscite](finance-how-defer-revenue-expenses.md) |
| Ottenere informazioni sulle opzioni disponibili per inviare automaticamente fatture di abbonamento ai clienti e registrare il ricavo periodico. | [Utilizzo del ricavo ricorrente](finance-recurring-invoicing.md) |
| Usare valute aggiuntive e aggiornare i tassi di cambio automaticamente. | [Aggiornare i tassi di cambio valuta](finance-how-update-currencies.md) |
| Importare le transazioni degli stipendi dal sistema di gestione delle retribuzioni nella contabilità generale. | [Importare transazioni retribuzioni](finance-how-import-payroll-transactions.md) |
| Calcolare l'imposta sul valore aggiunto (VAT) sulle transazioni di vendita e acquisto in modo da segnalare gli importi alle autorità fiscali. | [Usare l'IVA nelle vendite e negli acquisti](finance-work-with-vat.md) |
| Preparare un report che elenca l'IVA di vendita e inviare il report alle autorità fiscali in Unione Europea (UE). | [Dichiarare l'IVA all'autorità fiscale](finance-how-report-vat.md) |
| Convertire manualmente i contratti di servizio per modificare la loro aliquota VAT. | [Convertire i contratti di servizio che includono importi IVA](service-how-to-convert-service-contracts.md) |
| Utilizzare i rendiconti finanziari e le sintesi fornite in Microsoft Excel. | [Analisi dei rendiconti finanziari in Excel](finance-analyze-excel.md) |
| Usare Gestione ruolo utente Contabile, invitare un contabile esterno e utilizzare l'hub aziendale per gestire i conti relativi a più client. | [Esperienze di contabile in Business Central](finance-accounting.md) |
| Impostare il reporting Intrastat per fornire scambi con altri membri dell'UE in base alla legislazione locale. | [Impostare il reporting Intrastat]( finance-how-setup-report-intrastat.md) |
| Compilare, convalidare e inviare il report Intrastat. | [Usare il reporting Intrastat]( finance-how-report-intrastat.md) |
| Impostare, compilare, convalidare e inviare il report sulla dichiarazione di servizio per i servizi commerciali in tutta l'UE. | [ Impostare e usare la Dichiarazione di servizio]( finance-how-setup-use-service-declaration.md) |
| Creare cespiti, assegnare di metodi di ammortamento, registrare acquisti e valori di realizzo e stampare liste di cespiti. | [Acquisire i cespiti](fa-how-acquire.md) |
| Registrare le visite di assistenza, pubblicare e monitorare i costi di manutenzione. | [Gestione di cespiti](fa-how-maintain.md) |
| Aggiornare informazioni di assicurazione, registrare costi di acquisto in polizze assicurative, modificare la copertura assicurativa, visualizzare le statistiche di assicurazione e creare liste delle polizze assicurative. | [Assicurazione di cespiti](fa-how-insure.md) |
| Riclassificare i cespiti, trasferire i cespiti in ubicazioni diverse e suddividere o raggruppare i cespiti. | [Trasferimento, divisione o combinazione di cespiti](fa-how-trans-split-combine.md) |
| Rettificare il valore dei cespiti, registrare l'ammortamento e transazioni di svalutazione. | [Rivalutazione dei cespiti](fa-how-revalue.md) |
| Calcolare e registrare l'ammortamento e analizzare l'ammortamento nei report sui cespiti. | [Ammortamento dei cespiti](fa-how-depreciate-amortize.md) |
| Registrare transazioni di cessione, visualizzare movimenti contabili di cessione e registrare cessioni parziali. | [Smaltimento o ritiro dei cespiti](fa-how-dispose-retire.md) |
| Gestire budget per cespiti, costi di acquisto previsti, previsioni di cessione dei cespiti e previsioni di ammortamento. | [Gestione dei budget per i cespiti](fa-how-manage-budgets.md) |
| Impostare gli utenti del workflow di approvazione, specificare la modalità di notifica per gli utenti e creare nuovi flussi di lavoro. Per creare i nuovi flussi di lavoro per gli scenari non sostenuti, implementare gli elementi necessari del flusso di lavoro personalizzando il codice dell'applicazione. | [Impostare i flussi di lavoro di approvazione](across-set-up-workflows.md) |
| Abilitare i workflow di approvazione, intervenire sulle relative notifiche (ad esempio, richiedendo e approvando la fase del flusso di lavoro) e archivare ed eliminare i flussi di lavoro. | [Usare workflow di approvazione](across-use-workflows.md) |
| Visualizzare gli importi effettivi rispetto agli importi previsti per tutti i conti e per diversi periodi. | [Analisi degli importi effettivi e degli importi di budget](bi-how-analyze-actual-versus-budget.md) |
| Creare nuovi report finanziari per definire i rendiconti finanziari per il reporting o la visualizzazione in grafici. | [Preparare i report finanziari con i dati finanziari e le categorie di conti](bi-how-work-account-schedule.md) |
| Analizzare le prestazioni finanziarie impostando indicatori di prestazioni chiave (KPI) basati su report finanziari e pubblicare i KPI come servizi Web. Gli indicatori KPI dei report finanziari pubblicati possono essere visualizzati in un sito Web o essere importati in Excel utilizzando i servizi Web OData. | [Impostare e pubblicare servizi Web indicatore di prestazioni chiave (KPI) basati sui report finanziari](bi-how-to-set-up-and-publish-kpi-web-services-based-on-account-schedules.md) |
| Impostare le visualizzazioni per analizzare i dati utilizzando le dimensioni. | [Analizzare i dati per dimensioni](bi-how-analyze-data-dimension.md) |
| Creare nuovi report di analisi per vendite, acquisti e magazzino e impostare modelli di analisi. | [Creare report di analisi](bi-how-create-analysis-views-reports.md) |
| Abilitare il reporting finanziario globale per organizzazioni contabili internazionali utilizzando lo standard eXtensible Business Reporting Language (XBRL). | [Creare report con XBRL](bi-create-reports-with-xbrl.md) |
| Modificare l'intento di accesso al database in report, pagine di tipo API e query per ridurre il carico e migliorare le prestazioni. | [Gestire l'intento di accesso al database](admin-data-access-intent.md) |

## <a name="see-also"></a>Vedere anche

[Impostazione di dati finanziari](finance-setup-finance.md)  
[Vendite](sales-manage-sales.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Chiusura di periodi fiscali](year-close-years-periods.md)  
[Gestione di progetti](projects-manage-projects.md)  
[Importazione dei dati aziendali da altri sistemi contabili](across-import-data-configuration-packages.md)  
[Utilizzare le registrazioni COGE](ui-work-general-journals.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]

[!INCLUDE[footer-include](includes/footer-banner.md)]
