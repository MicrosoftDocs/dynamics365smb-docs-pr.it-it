---
title: Setup categorie di registrazione | Documenti Microsoft
description: Fornisce una panoramica delle categorie di registrazione
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: posting setup, initialize
ms.date: 03/24/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 79018546484ff3bb8965089a3554d69bec219304
ms.contentlocale: it-it
ms.lasthandoff: 05/04/2017


---
# <a name="posting-group-setups"></a>Setup categorie di registrazione
Le categorie di registrazione associano entità come clienti, fornitori, articoli, risorse e documenti di vendita o di acquisto a conti di contabilità generale. Consentono di risparmiare tempo e contribuiscono a evitare errori quando si registrano transazioni. I valori di transazione verranno registrati nei conti specificati nella categoria di registrazione per tale particolare entità. L'unico requisito consiste nella presenza di un piano dei conti. Per ulteriori informazioni, vedere [Impostare il piano dei conti](finance-setup-chart-accounts.md).  

Le categorie di registrazione possono essere di tre tipi:  

* Generale: specificare a quali clienti si vende o da quali fornitori si compra e gli articoli/servizi elementi o acquistati. È inoltre possibile combinare le categorie per specificare le operazioni come i conti economici in cui effettuare la registrazione oppure utilizzare le categorie per filtrare i report.  
* Specifica: consente, ad esempio, di utilizzare i documenti di vendita anziché effettuare la registrazione direttamente nella contabilità generale. Quando vengono creati movimenti contabili nel registro clienti , le categorie di registrazione garantiscono che nella contabilità generale vengano creati i movimenti corrispondenti.  
* IVA: consente di definire le aliquote dell'imposta e i tipi di calcolo da applicare a clienti o fornitori e agli articoli venduti o acquistati.

Nelle tabelle che seguono sono indicate le categorie di registrazione che rientrano in ciascun tipo.  

| Categorie di registrazione generali | Descrizione |
| --- | --- |
| Categorie di registrazione business |Assegnare il gruppo a clienti e fornitori per specificare a chi si vende e da chi si acquista. Impostare questi valori nella finestra **Cat. reg. business**. Durante l'impostazione, pensare a quante categorie saranno necessarie per suddividere vendite e acquisti. Ad esempio, le categorie di clienti e fornitori per aree geografiche o per tipo di attività. |
| Categorie di registrazione articoli/servizi |Assegnare questa categoria ad articoli e risorse per specificare gli articoli venduti o acquistati. Impostare questi valori nella finestra **Cat. reg. articoli/servizi**. Durante l'impostazione, pensare al numero di categorie che sarà necessario per ripartire le vendite per prodotto (articoli e risorse) e gli acquisti per articolo. Ad esempio, suddivide queste categorie per materie prime, vendita al dettaglio, risorse, capacità e così via. |
| Setup Registrazioni Generali |Combinare le categorie di registrazione business e le categorie di registrazione articoli/servizi e scegliere i conti per effettuare la registrazione. A ogni combinazione di categorie di registrazione business e articoli/servizi, è possibile assegnare un insieme di conti C/G. È possibile, ad esempio, registrare la vendita dello stesso articolo in conti vendite diversi nella contabilità generale se ai clienti sono assegnate categorie di registrazione business diverse. Impostare questi valori nella finestra **Setup registrazioni COGE**. |

| Categorie di registrazione specifiche | Descrizione |
| --- | --- |
| Cat. reg. clienti |Definire i conti da utilizzare quando si registrano transazioni clienti. Se si utilizzano il magazzino insieme alla contabilità clienti, la categoria di registrazione business assegnata al cliente e categoria di registrazione articoli/servizi assegnata all'articolo di magazzino determina i conti in cui registrare i movimenti delle righe dell'ordine di vendita. Impostare questi valori nella finestra **Cat. reg. clienti**. |
| Cat. reg. fornitori |Definire dove registrare le transazioni relative a conti fornitori, conti di addebito assistenza e conti sconto pagamento. Questo è simile alle categorie di registrazione clienti. Impostare questi valori nella finestra **Cat. reg. fornitori**. |
| Cat. reg. magazzino |Definire i conti giacenza magazzino patrimoniali. Le categorie di registrazione magazzino rappresentano inoltre un metodo valido per organizzare il magazzino. Quando si generano report, è possibile separare gli articoli in base alle relative categorie di registrazione. Impostare questi valori nella finestra **Cat. reg. magazzino**. |
| Cat. reg. C/C bancari |Definire i conti per i conti bancari. Ad esempio, è possibile semplificare i processi di tracciamento delle transazioni e di riconciliazione dei conti correnti bancari. Impostare questi valori nella finestra **Cat. reg. C/C bancari**. |
| Categorie di registrazione cespiti |È possibile definire diversi tipi di spese e costi, come conti per costi di acquisto, importi di fondo ammortamento, costi di acquisto di cessione, fondo ammortamento di cessione, guadagni su cessione, perdite su cessione, spese di manutenzione e spese di ammortamento. Impostare questi valori nella finestra **Cat. reg. cespiti**. |

| Categoria registrazione IVA | Descrizione |
| --- | --- |
| Categorie reg. business IVA |Stabilire come calcolare e registrare l'IVA per clienti e fornitori. Impostare questi valori nella finestra **Cat. reg. business IVA**. Durante l'impostazione, pensare a quante categorie saranno necessarie. Ad esempio, questo può dipendere da diversi fattori, quali la legislazione locale e il fatto che l'azienda svolga un'attività commerciale sia a livello nazionale che internazionale. |
| Cat. reg. articoli/servizi IVA |Specificare i calcoli IVA necessari per i tipi di articoli o risorse acquistati o venduti. |
| Setup registrazioni IVA |Combinare le categorie di registrazione business IVA e di categorie di registrazione articoli/servizi IVA. Quando si compila una riga di registrazioni COGE, di acquisto o di vendita, si esamina la combinazione per identificare i conti da utilizzare. |

## <a name="example-of-linking-posting-groups"></a>Esempio di collegamento di categorie di registrazione
Ecco uno scenario.  

Le categorie di registrazione vengono selezionati in una scheda cliente:  

* Categoria di registrazione business
* Cat. reg. cliente  

Le categorie di registrazione vengono selezionate in una scheda articolo:  

* Categorie di registrazione articoli/servizi:  
* Cat. reg. magazzino  

Quando viene creato un documento di vendita, le informazioni della scheda cliente vengono utilizzate nella testata di vendita e quelle della scheda articolo nelle righe di vendita.  

* La registrazione dei ricavi (conto economico) è determinata dalla combinazione di categoria di registrazione business e categoria di registrazione articoli/servizi.  
* La registrazione dei crediti v/clienti (conto patrimoniale) è determinata dalla categoria di registrazione cliente.  
* La registrazione di magazzino (conto patrimoniale) è determinata dalla categoria di registrazione magazzino.  
* La registrazione del costo delle merci vendute (COGS, Cost of Goods Sold) è determinata dalla combinazione di categoria di registrazione business e categoria di registrazione articoli/servizi.  

Il setup determina quando avviene la registrazione. Ad esempio, la sincronizzazione è influenzata da quando si eseguono le attività periodiche, come la registrazione dei costi di magazzino o la rettifica dei movimenti di costo articoli.

## <a name="copying-posting-setup-lines"></a>Copia di righe di setup registrazione
Maggiore è il numero di categorie di registrazione articoli/servizi e business, maggiore sarà la quantità di righe visualizzate nella finestra Setup registrazioni COGE. Questo significa che per il setup delle registrazioni COGE per la società è necessario immettere una grande quantità di dati. Sebbene possano esserci numerose combinazioni diverse di categorie di registrazione business e articoli/servizi, le diverse combinazioni possono comportare la registrazione negli stessi conti C/G. Per limitare la quantità di dati da immettere manualmente, copiare i conti C/G da una riga esistente nella finestra **Setup registrazioni COGE**.

## <a name="see-also"></a>Vedere anche
[Contabilità generale e piano dei conti](finance-general-ledger.md)  
[Impostazione di dati finanziari](finance-setup-finance.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

