---
title: Impostazione delle dimensioni | Documenti Microsoft
description: "È possibile definire le dimensioni e i valori di dimensione da utilizzare per classificare le registrazioni e i documenti, ad esempio ordini di vendita e di acquisto."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 03/28/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 0da77c5be3b49f715384752ad61fc072aea8525c
ms.contentlocale: it-it
ms.lasthandoff: 05/04/2017


---
# <a name="setting-up-dimensions"></a>Setup delle dimensioni
È possibile definire le dimensioni e i valori di dimensione da utilizzare per classificare le registrazioni e i documenti, ad esempio ordini di vendita e di acquisto. Impostare le dimensioni nella finestra **Dimensioni** in cui si crea una riga per ogni dimensione, ad esempio *Progetto*, *Reparto*, *Area* e *Agente*.

Vengono inoltre impostati i valori delle dimensioni. Ad esempio, i valori potrebbero essere i reparti della società. I valori di dimensione possono essere impostati in una struttura gerarchica simile al piano dei conti, in modo che i dati possano essere suddivisi in vari livelli di granularità e i sottoinsiemi dei valori di dimensione sommati. In base alle necessità, è possibile impostare un numero illimitato di dimensioni e di valori dimensioni che possono essere utilizzati da tutti gli utenti nella società.

È inoltre possibile impostare alcune dimensioni globali e dimensioni a collegamento rapido:  

* **Dimensioni globali** utilizzate come filtro, ad esempio, per report e processi batch. È possibile utilizzare solo due dimensioni globali, scegliere pertanto le dimensioni che verranno utilizzate più spesso.
* Le **dimensioni a collegamento rapido** sono disponibili come campi nelle righe di registrazioni e documenti. È possibile creare fino a sei dimensioni a collegamento rapido.  

**Nota**: questa funzionalità richiede che l'esperienza sia impostata su ***** Suite *****. Per ulteriori informazioni, vedere [Personalizzazione dell'esperienza di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md).

## <a name="set-up-default-dimensions-for-customers-vendors-and-other-accounts"></a>Impostare le dimensioni di default per clienti, fornitori e altri conti
È possibile assegnare una dimensione di default per un conto specifico. La dimensione verrà copiata nelle registrazioni o nel documento quando si immette il numero di conto in una riga, ma è possibile eliminare o modificare il codice nella riga se il dato non è appropriato. È inoltre possibile impostare una dimensione richiesta per la registrazione del movimento con un tipo di conto specifico.  

## <a name="translate-the-names-of-dimensions"></a>Tradurre i nomi delle dimensioni
Quando si crea una dimensione e, particolarmente una dimensione di collegamento, l'elemento che si sta effettivamente creando è un campo personalizzato o un'intestazione di colonna. Se l'attività è internazionale, è possibile inserire le traduzioni per il nome della dimensione. I documenti che includono la dimensione utilizzeranno il nome tradotto, quando applicabile.   

## <a name="example"></a>Esempio
Supponiamo che la società desideri tenere traccia delle transazioni in base alla struttura organizzativa e alle posizioni geografiche. A tale scopo, è possibile impostare due dimensioni nella finestra **Dimensioni** :

* **AREA**  
* **REPARTO**  

| Codice | Name | Didascalia codice | Didascalia filtro |
| --- | --- | --- | --- |
| AREA |Area |Codice area |Filtro area |
| REPARTO |Reparto |Codice reparto |Filtro per reparto |

Per **AREA**, è possibile aggiungere i seguenti valori dimensioni:

| Codice | Name | Tipo valori dimensioni |
| --- | --- | --- |
| 10 |America |Inizio-Totale |
| 2.0 |Nord America |Standard |
| 30 |Pacifico |Standard |
| 40 |Sud America |Standard |
| 50 |America, totale |Fine-Totale |
| 60 |Europa |Inizio-Totale |
| 70 |UE |Standard |
| 80 |Extracomunitaria |Standard |
| 90 |Europa, totale |Fine-Totale |

Per le zone due are geografiche principali, Europa e America,, si aggiungono sottocategorie per regioni tramite l'indentazione dei valori di dimensione. In questo modo sarà possibile ottenere report per vendite o spese nelle varie regioni e i totali per le aree geografiche più grandi. È anche possibile scegliere di utilizzare paesi o regioni come valori di dimensione, province o città, a seconda della propria attività.  
**Nota**: per impostare una gerarchia, i codici devono essere in ordine alfabetico. Inclusi quelli dei valori dimensioni che forniti in [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Per **REPARTO**, è possibile aggiungere i seguenti valori dimensioni:

| Codice | Name | Tipo valori dimensioni |
| --- | --- | --- |
| AMMIN |Setup |Standard |
| PROD |Produzione |Standard |
| VENDITE |Vendite |Standard |

Con questa impostazione, si aggiungono le due dimensioni come dimensioni globali nella finestra **Setup contabilità generale**. Ciò significa che è possibile utilizzare AREA e REPARTO come filtri per i movimenti di contabilità generale, nonché per tutti i report e le situazioni contabili. Le dimensioni globali sono inoltre disponibili automaticamente come dimensioni a collegamento rapido nelle righe di registrazione e nelle testate dei documenti.  

Con questa impostazione, è possibile iniziare ad aggiungere le dimensioni a documenti e alle registrazioni. Per ulteriori informazioni, vedere [Dimensioni](finance-dimensions.md).  

## <a name="see-also"></a>Vedi anche
[Dimensioni](finance-dimensions.md)  
[Impostazione di dati finanziari](finance-setup-finance.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

