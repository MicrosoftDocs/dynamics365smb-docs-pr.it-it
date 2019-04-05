---
title: Creazione di numerazioni | Documenti Microsoft
description: Informazioni su come impostare la numerazione per assegnare codici di identificazione univoci a conti e documenti in Business Central.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: numbers, numbering
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 46131d6ad5f77a02ffe33d24f1210a226c3041c1
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/08/2019
ms.locfileid: "801221"
---
# <a name="create-number-series"></a>Creazione di numerazioni
Per ogni società impostata, è necessario assegnare codici di identificazione univoci a elementi quali i conti di contabilità generale, i conti clienti e i conti fornitori, le fatture e altri documenti. La numerazione è importante non solo ai fini dell'identificazione. Un sistema di numerazione progettato correttamente semplifica la gestione e l'analisi della società e può ridurre il numero di errori correlati all'immissione dei dati.

> [!NOTE]  
>   Si consiglia di utilizzare gli stessi codici di numerazione visualizzati nella pagina **Elenco nr. serie** nella società di esempio CRONUS. I codici come *P-INV+* potrebbero non avere significato immediato, ma [!INCLUDE[d365fin](includes/d365fin_md.md)] dispone di un numero di impostazioni predefinite che dipendono da tali codici di numerazione.

Per creare un sistema di numerazione, è necessario impostare uno o più codici per ogni tipo di anagrafica o documento. È possibile, ad esempio, impostare un codice per la numerazione dei clienti, un altro per la numerazione delle fatture di vendita e un altro ancora per la numerazione di documenti in registrazioni COGE. Dopo avere impostato un codice, è necessario impostare almeno una riga di numerazione. Tale riga contiene informazioni quali il primo e l'ultimo numero nella serie e la data di inizio. È possibile impostare più righe di numerazione per codice di numerazione, con una diversa data di inizio per ogni riga. Le numerazioni verranno utilizzate consecutivamente, avviando ciascuna alla rispettiva data di inizio.

In genere, si imposta la serie di numeri per inserire automaticamente il numero immediatamente successivo nelle nuove schede o documenti creati. Tuttavia, è anche possibile impostare una numerazione che consente l'immissione manuale del nuovo numero. A tale scopo selezionare la casella di controllo **Consenti num. manuale**.

Se si desidera utilizzare più codici di numerazione per un tipo di anagrafica, ad esempio per utilizzare una numerazione diversa per diverse categorie di articoli, è possibile utilizzare relazioni tra numerazioni.

## <a name="behavior-of-the-no-field-on-documents-and-cards"></a>Comportamento del campo Nr. in documenti e schede
Nella vendita, acquisto e trasferimento di documenti e su tutte le schede, il campo **Nr.** può essere compilato automaticamente da una serie di numeri o manualmente e può essere impostato per essere invisibile.

Il campo **Nr.** può essere compilato in tre modi:

1. Se esiste solo una numerazione per il tipo di documento o scheda dove la casella di controllo **Proponi automaticamente** è selezionata e la casella di controllo **Consenti num. manuale** non è selezionata, il campo viene compilato automaticamente con il numero successivo della numerazione e il campo **Nr.** non sarà visibile.

    > [!NOTE]  
    > Se la serie di numeri non funziona, ad esempio perché ha esaurito i numeri, il campo **Nr.** risulterà visibile e sarà possibile immettere manualmente un numero o risolvere il problema nella pagina **Elenco nr. serie**.

2. Se esiste più di una numerazione per il tipo di documento o scheda e la casella di controllo **Proponi automaticamente** non è selezionata per la numerazione attualmente assegnata, il campo **Nr.** è visibile ed è possibile cercare la pagina **Elenco nr. serie** e selezionare la numerazione che si desidera utilizzare. Il numero successivo della serie viene quindi inserito nel campo **Nr.**.  

3. Se per il tipo di documento o scheda non è stata impostata alcuna numerazione o se è selezionato il campo **Consenti num. manuale** per la numerazione, il campo **Nr.** è visibile ed è necessario inserire qualsiasi numero manualmente. È possibile immettere un massimo di 20 caratteri, tra numeri e lettere.

Quando si apre un nuovo documento o scheda per cui esiste una numerazione, si apre la relativa pagina **Setup numerazione** in modo da poter impostare una numerazione per il tipo di documento o scheda prima di procedere con un'altra immissione di dati.

> [!NOTE]  
> Se è necessario attivare la numerazione manuale, ad esempio su nuove schede articolo create con un processo di migrazione di dati che ha nascosto il campo **Nr.** per impostazione predefinita, passare alla pagina **Setup magazzino** e scegliere il campo **Nr. articoli** per aprire e impostare la relativa numerazione su **Consenti num. manuale**.

## <a name="to-create-a-new-number-series"></a>Per creare nuove numerazioni
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Nr. serie** e quindi scegliere il collegamento correlato.
2. Scegliere l'azione **Nuovo**.
3. Nella nuova riga, compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-where-a-number-series-is-used"></a>Per impostare le aree in cui la numerazione viene utilizzata
La seguente procedura illustra come impostare una numerazione per l'area delle vendite. I passaggi sono simili per altre aree.
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Contabilità clienti** e quindi scegliere il collegamento correlato.
2. Nella pagina **Contabilità clienti** nella Scheda dettaglio **Numerazioni**, selezionare la numerazione desiderata per ogni scheda di vendita o documento.

Il numero selezionato risulterà utilizzato per compilare il campo **Nr.** nella scheda o nel documento in questione, in base alle impostazioni effettuate nella serie di numerazione.

## <a name="to-create-relationships-between-number-series"></a>Per creare relazioni tra numerazioni
È possibile creare relazioni tra codici di numero di serie se ne sono stati impostati più di uno per lo stesso tipo di informazione o transazione di base. Questa funzione può essere utile per selezionare il codice corretto, al momento di utilizzare un numero.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Nr. serie** e quindi scegliere il collegamento correlato.
2. Selezionare la riga contenente la numerazione per la quale si desidera creare delle relazioni, quindi scegliere **Relazioni**.
3. Nel campo **Codice serie** immettere il codice della numerazione che si desidera associare alla serie selezionata nel passaggio 2.
4. Aggiungere una riga per ogni codice che si desidera associare alla numerazione selezionata.
5. Chiudere la pagina.

Ogni volta che verrà impostato un elemento che richiede un numero, è ora possibile utilizzare le relazioni che sono state create per selezionare la numerazione corretta tra quelle poste in relazione.

## <a name="see-also"></a>Vedi anche
[Impostazione di [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
