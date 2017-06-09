---
title: Dimensioni | Documenti Microsoft
description: Utilizzo delle dimensioni per analizzare i dati.
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 03/24/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 7552ee2b3398c203a7f3295f3203c83914fbb15f
ms.contentlocale: it-it
ms.lasthandoff: 05/04/2017


---
# <a name="dimensions"></a>Dimensioni
Per rendere più semplice eseguire analisi sui documenti, quali ordini di vendita, è possibile utilizzare le dimensioni. Le dimensioni sono attributi e valori che categorizzano i movimenti in modo da poterli seguire e analizzare. Ad esempio, le dimensioni possono indicare il progetto o il reparto da cui un movimento proviene.  

For example, anziché impostare conti di contabilità generale distinti per ogni reparto e progetto, è possibile utilizzare le dimensioni. Ciò dà un'opportunità ricca per l'analisi, senza creare un piano dei conti complesso.  

Un altro esempio consiste nell'impostare una dimensione denominata *Reparto* e nell'utilizzare tale dimensione al momento della registrazione dei documenti di vendita. In questo modo sarà possibile utilizzare strumenti di business intelligence per vedere quale reparto ha venduto quali articoli.
Più dimensioni si utilizzano, più dettagliati sono i report su cui è possibile basare le decisioni aziendali. Ad esempio, un singolo movimento di vendita può includere le informazioni di più dimensioni, quali:  

* Il conto in cui è stata registrata la vendita dell'articolo  
* Dove l'articolo è stato venduto
* Chi lo ha venduto
* Il tipo di cliente che lo ha acquistato  

È possibile creare tutte le dimensioni con tutti i valori che si desiderano.  

**Nota**: questa funzionalità richiede che l'esperienza sia impostata su ***** Suite *****. Per ulteriori informazioni, vedere [Personalizzazione dell'esperienza di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md).

## <a name="using-dimensions"></a>Utilizzo delle dimensioni
In un documento come un ordine di vendita, è possibile aggiungere le informazioni sulle dimensioni sia per una singola riga del documento che l'intero documento. Ad esempio, nella finestra **Ordine di vendita** è possibile immettere i valori dimensioni per le prime due dimensioni a collegamento rapido nelle singole righe vendita e aggiungere altre informazioni sulle dimensioni selezionando il pulsante **Dimensioni**.  

Se si lavora nelle registrazioni invece, è possibile aggiungere informazioni sulle dimensioni a un movimento nello stesso modo, se le dimensioni a collegamento rapido sono state impostate come campi direttamente sulle righe di registrazione.  

È possibile impostare le dimensioni di default per i conti o i tipi di conto, in modo che le dimensioni e i valori dimensioni vengano compilati automaticamente.  

## <a name="dimension-sets"></a>Set di dimensioni
Un set di dimensioni è una combinazione univoca di valori dimensioni. Viene archiviato come movimenti set di dimensioni nel database. Ogni movimento set di dimensioni rappresenta un valore dimensioni singolo. Il set di dimensioni è identificato da un ID set di dimensioni comune assegnato a ogni movimento set di dimensioni che appartiene al set di dimensioni.  

Quando si crea una riga di registrazione, una testata del documento o una riga documento, è possibile specificare una combinazione di valori dimensioni. Anziché archiviare esplicitamente ogni valore dimensioni nel database, viene assegnato un ID set di dimensioni alla riga di registrazione, alla testata del documento o alla riga del documento per specificare il set di dimensioni.  

## <a name="see-also"></a>Vedi anche
[Finanza](finance.md)  
[Setup delle dimensioni](finance-setup-dimensions.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

