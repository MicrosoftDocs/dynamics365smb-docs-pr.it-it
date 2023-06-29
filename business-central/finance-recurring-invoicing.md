---
title: Utilizzo del ricavo ricorrente
description: Informazioni sulle opzioni disponibili per automatizzare il modo in cui si inviano le fatture di abbonamento ai clienti e registrare il ricavo periodico.
author: AndreiPanko
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'recurring, invoicing, subscription, billing'
ms.search.form: 283
ms.reviewer: edupont
ms.date: 04/01/2021
ms.author: andreipa
---
# <a name="work-with-recurring-revenue-in-"></a><a name="work-with-recurring-revenue-in-"></a>Utilizzo del ricavo ricorrente in [!INCLUDE[prod_short](includes/prod_short.md)]

Molte aziende stanno passando da un modello di ricavo aziendale in cui i ricavi vengono effettuati dall'acquisto singolo di un cliente a un modello di abbonamento in cui i ricavi vengono effettuati su base ricorrente in cambio di un accesso coerente alla consegna di un bene o servizio.
[!INCLUDE[prod_short](includes/prod_short.md)] ha le seguenti opzioni per automatizzare il modo in cui si inviano le fatture di abbonamento ai clienti e registrare il ricavo periodico. 

## <a name="register-revenue-with-a-recurring-general-journal"></a><a name="register-revenue-with-a-recurring-general-journal"></a>Registrare il ricavo con un giornale generale di registrazione periodica

Una registrazione periodica è una registrazione generale con campi specifici per la gestione di transazioni registrate frequentemente con poche o nessuna modifica, come affitto, sottoscrizioni, elettricità o riscaldamento. Se si utilizzano questi campi per le transazioni ricorrenti, è possibile registrare sia gli importi fissi sia quelli variabili. Utilizzando registrazioni periodiche, è sufficiente immettere una sola volta i movimenti registrati regolarmente. Ciò significa che i conti, le dimensioni, i valori dimensioni e così via, immessi nei campi rimarranno nelle registrazioni dopo la contabilizzazione. Se sono necessarie rettifiche, è possibile eseguirle a ogni registrazione.

### <a name="why-use-this-option"></a><a name="why-use-this-option"></a>Perché usare questa opzione

Con questa opzione, è possibile definire periodi di fatturazione flessibili con le [formule della data](ui-enter-date-ranges.md#use-date-formulas).

Tuttavia, con questa opzione, non è possibile stampare e inviare fatture nella versione predefinita di [!INCLUDE[prod_short](includes/prod_short.md)].  

Per ulteriori informazioni, vedi [Utilizzare le registrazioni periodiche](ui-work-general-journals.md#work-with-recurring-journals).  

## <a name="create-multiple-invoices-based-on-a-recurring-job-journal"></a><a name="create-multiple-invoices-based-on-a-recurring-job-journal"></a>Creare più fatture basate su un giornale di registrazione commesse periodico

Il giornale di registrazione commesse periodico è un'alternativa più avanzata al giornale di registrazione generale. Si definiscono articoli, risorse e conti Co.Ge., che devono essere ripetuti per ciascuna commessa e si specifica la frequenza di ricorrenza.  

Dopo aver pubblicato un giornale di registrazione commesse periodico, è possibile creare più fatture con l'attività **Crea fattura vendita per commessa**. È possibile rivedere e pubblicare le fatture create nella pagina **Fatture vendita**.

### <a name="why-use-this-option-1"></a><a name="why-use-this-option-1"></a>Perché usare questa opzione

Con questa opzione, seguire la procedura di fatturazione standard con tutti i vantaggi, inclusi layout standard e cliente per le preferenze di comunicazione. È inoltre possibile definire i prezzi per ciascuna commessa individualmente.

Tuttavia, per ogni nuovo cliente, è necessario creare una nuova commessa e aggiungere righe al giornale periodico. 

Per ulteriori informazioni, vedere [Creare righe del giornale di registrazione commesse](projects-how-record-job-usage.md#to-create-job-journal-lines-manually) e [Creare più fatture di vendita commesse](projects-how-invoice-jobs.md#to-create-multiple-job-sales-invoices).

## <a name="create-multiple-invoices-based-on-recurring-sales-lines"></a><a name="create-multiple-invoices-based-on-recurring-sales-lines"></a>Creare più fatture basate sulle righe di vendita ricorrenti

Se è spesso necessario creare righe di vendita e acquisto con informazioni simili, è possibile impostare righe di vendita ricorrenti da inserire nei documenti di vendita e di acquisto ricorrenti, ad esempio, per ordini di approvvigionamento ricorrenti. Utilizzare il processo batch **Crea fatture di vendita periodica** per creare fatture di vendita in base alle righe di vendita ricorrenti assegnate ai clienti e con date di registrazione comprese nell'intervallo di date valide specificato nelle righe di vendita ricorrenti.  

### <a name="why-use-this-option-2"></a><a name="why-use-this-option-2"></a>Perché usare questa opzione

Con questa opzione, è possibile assegnare le stesse righe ricorrenti a più clienti. È possibile definire un periodo di validità per le righe di vendita ricorrenti per un cliente specifico. È possibile assegnare più righe ricorrenti allo stesso cliente e tutte saranno incluse nella fattura.

Tuttavia, non è possibile impostare prezzi fissi per gli articoli perché [!INCLUDE[prod_short](includes/prod_short.md)] utilizzerà i prezzi effettivi e gli sconti validi alla data del documento, cercando di trovare la migliore combinazione per il prezzo più basso.  

Per altre informazioni, vedere [Creare righe di vendite e acquisti ricorrenti](sales-how-work-standard-lines.md).

## <a name="recurring-invoices-with-service-contract"></a><a name="recurring-invoices-with-service-contract"></a>Fatture ricorrenti con contratto di assistenza

Un contratto di assistenza contiene gli accordi di contratto di assistenza tra i clienti e l'azienda. Un contratto comprende sia gli accordi a livello di assistenza che gli articoli per i quali si presta assistenza a fronte del contratto.  

È possibile definire la data di inizio del contratto, il periodo della fattura, se il contratto è prepagato o meno, le specifiche di aggiornamento dei prezzi se si prevede di modificare i prezzi mentre il contratto è attivo. È possibile utilizzare sia gli articoli di assistenza sia gli articoli nelle righe del contratto di assistenza.
È possibile creare modelli dei contratti per definire il modo in cui creare determinati tipi di contratti.  

### <a name="why-use-this-option-3"></a><a name="why-use-this-option-3"></a>Perché usare questa opzione

Con questa opzione, si utilizza una parte della funzionalità avanzata di gestione dei servizi che non si limita all'emissione di fatture ricorrenti, ma supporta le operazioni di riparazione e assistenza sul campo.

Tuttavia, questa opzione richiede la licenza Premium. Impostare la gestione del servizio e mantenerlo potrebbe non offrire enormi vantaggi in scenari di abbonamento più semplici.  

Per ulteriori informazioni, vedere [Utilizzare contratti e offerte di contratto di assistenza](service-how-to-create-service-contracts-and-service-contract-quotes.md) e [Fatturare diversi contratti di assistenza](service-how-create-invoices.md#to-invoice-several-service-contracts).

## <a name="related-features"></a><a name="related-features"></a>Funzionalità correlate
Ci sono diverse funzionalità correlate in [!INCLUDE[prod_short](includes/prod_short.md)].

### <a name="blanket-sales-orders"></a><a name="blanket-sales-orders"></a>Ordini vendita programmati

Un ordine di vendita programmato rappresenta la struttura di un accordo a lungo termine tra la società e il cliente.
Un ordine programmato viene in genere creato quando un cliente si impegna ad acquistare grandi quantità che verranno consegnate con diverse spedizioni più piccole effettuate in un determinato periodo di tempo. Gli ordini programmati riguardano spesso un solo articolo con date di consegna predefinite. Il motivo principale dell'utilizzo di un ordine programmato anziché di un ordine di vendita consiste nel fatto che le quantità immesse in un ordine programmato non hanno influenza sulla disponibilità dell'articolo e pertanto tali ordini possono essere utilizzati come prospetto per il monitoraggio, le previsioni e le pianificazioni.

#### <a name="why-use-this-option-4"></a><a name="why-use-this-option-4"></a>Perché usare questa opzione

Con questa opzione, si utilizza la domanda prevista, pertanto le informazioni vengono prese in considerazione durante le normali procedure di pianificazione. Per ulteriori informazioni, vedere [Previsioni della domanda e ordini programmati](design-details-central-concepts-of-the-planning-system.md#demand-forecasts-and-blanket-orders).  

Tuttavia, la versione predefinita non offre la possibilità immediata di elaborare più ordini programmati in blocco.

Per ulteriori informazioni, vedere [Utilizzare ordini vendita programmati](sales-how-to-create-blanket-sales-orders.md).

### <a name="recurring-orders-norway"></a><a name="recurring-orders-norway"></a>Ordini ricorrenti (Norvegia)

È possibile utilizzare gli ordini ricorrenti per creare modelli di ordine programmato in modo che gli ordini di vendita possano essere creati in base agli intervalli di date definiti. Ad esempio, se si consegna lo stesso ordine cliente ogni due settimane, è possibile utilizzare un ordine cliente programmato e creare ordini ricorrenti.
È possibile utilizzare le categorie ricorrenti per definire un intervallo di parametri che mostrano come effettuare gli ordini. Queste categorie sono assegnate ad ordini programmati che devono essere creati regolarmente. Per creare gli ordini ricorrenti, sarà necessario eseguire periodicamente il processo di creazione degli ordini ricorrenti. 

#### <a name="why-use-this-option-5"></a><a name="why-use-this-option-5"></a>Perché usare questa opzione

Con questa opzione, è possibile scegliere tra prezzi fissi e "migliori".

L'opzione è disponibile solo in Norvegia. Il periodo di validità può essere definito a livello di categoria ricorrente.

Per ulteriori informazioni, vedere [Ordini ricorrenti](LocalFunctionality/Norway/recurring-orders.md).

### <a name="recurring-revenue-and-subscription-billing-by-other-providers"></a><a name="recurring-revenue-and-subscription-billing-by-other-providers"></a>Ricavo ricorrente e fatturazione in abbonamento da parte di altri fornitori

In [AppSource.microsoft.com](https://appsource.microsoft.com/), è possibile ottenere estensioni per Business Central. Alcune estensioni sono fornite da Microsoft, altre sono fornite da altre società. La lista delle estensioni di altre società aumenta ogni mese. Seguire gli aggiornamenti sulla disponibilità delle estensioni tramite il sito Web [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646) e scaricare app per semplificare il proprio lavoro in Business Central.  

## <a name="see-also"></a><a name="see-also"></a>Vedere anche

[Formule per la data](ui-enter-date-ranges.md#use-date-formulas)  
[Utilizzare le registrazioni periodiche](ui-work-general-journals.md#work-with-recurring-journals)  
[Creare righe di registrazione commesse](projects-how-record-job-usage.md#to-create-job-journal-lines-manually)  
[Creare più fatture di vendita commesse](projects-how-invoice-jobs.md#to-create-multiple-job-sales-invoices)  
[Creare righe di vendite e acquisti ricorrenti](sales-how-work-standard-lines.md)  
[Utilizzare contratti e offerte di contratto di assistenza](service-how-to-create-service-contracts-and-service-contract-quotes.md)  
[Fatturare più contratti di assistenza](service-how-create-invoices.md#to-invoice-several-service-contracts)  
[Previsioni della domanda e ordini programmati](design-details-central-concepts-of-the-planning-system.md#demand-forecasts-and-blanket-orders)  
[Utilizzare gli ordini di vendita programmati](sales-how-to-create-blanket-sales-orders.md)  
[Ordini ricorrenti (Norvegia)](LocalFunctionality/Norway/recurring-orders.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
