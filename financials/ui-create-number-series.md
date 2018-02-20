---
title: Creazione di numerazioni | Documenti Microsoft
description: Informazioni su come impostare la numerazione per assegnare codici di identificazione univoci a conti e documenti in Finance and Operations, Business edition.
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: numbers, numbering
ms.date: 06/02/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 3f50bc1153ccd6b58bc502974c042626ce696078
ms.contentlocale: it-it
ms.lasthandoff: 01/30/2018

---
# <a name="create-number-series"></a>Creazione di numerazioni
Per ogni società impostata, è necessario assegnare codici di identificazione univoci a elementi quali i conti di contabilità generale, i conti clienti e i conti fornitori, le fatture e altri documenti. La numerazione è importante non solo ai fini dell'identificazione. Un sistema di numerazione progettato correttamente semplifica la gestione e l'analisi della società e può ridurre il numero di errori correlati all'immissione dei dati.

> [!NOTE]  
>   Si consiglia di utilizzare gli stessi codici di numerazione visualizzati nella finestra **Elenco nr. serie** nella società di esempio CRONUS. I codici come *P-INV+* potrebbero non avere significato immediato, ma [!INCLUDE[d365fin](includes/d365fin_md.md)] dispone di un numero di impostazioni predefinite che dipendono da tali codici di numerazione.

Per creare un sistema di numerazione, è necessario impostare uno o più codici per ogni tipo di anagrafica o documento. È possibile, ad esempio, impostare un codice per la numerazione dei clienti, un altro per la numerazione delle fatture di vendita e un altro ancora per la numerazione di documenti in registrazioni COGE. Dopo avere impostato un codice, è necessario impostare almeno una riga di numerazione. Tale riga contiene informazioni quali il primo e l'ultimo numero nella serie e la data di inizio. È possibile impostare più righe di numerazione per codice di numerazione, con una diversa data di inizio per ogni riga. Le numerazioni verranno utilizzate consecutivamente, avviando ciascuna alla rispettiva data di inizio.

In genere, si imposta la serie di numeri per inserire automaticamente il numero immediatamente successivo nelle nuove schede o documenti creati. Tuttavia, è anche possibile impostare una numerazione che consente l'immissione manuale del nuovo numero. A tale scopo selezionare la casella di controllo **Consenti num. manuale**.

Se si desidera utilizzare più codici di numerazione per un tipo di anagrafica, ad esempio per utilizzare una numerazione diversa per diverse categorie di articoli, è possibile utilizzare relazioni tra numerazioni.

## <a name="to-create-a-new-number-series"></a>Per creare nuove numerazioni
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Nr. serie**, quindi scegliere il collegamento correlato.
2. Scegliere l'azione **Nuovo**.
3. Nella nuova riga, compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

**SUGGERIMENTO**: Per consentire l'immissione manuale di un numero nelle nuove schede o documenti, deselezionare la casella di controllo **Proponi automaticamente** e selezionare la casella di controllo **Consenti num. manuale**.

Ora quando si crea una nuova scheda o un documento che è impostato per utilizzare la serie di numeri in questione, è possibile compilare manualmente il campo **Nr.** con qualsiasi valore.  

## <a name="to-set-up-where-a-number-series-is-used"></a>Per impostare le aree in cui la numerazione viene utilizzata
La seguente procedura illustra come impostare una numerazione per l'area delle vendite. I passaggi sono simili per altre aree.
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Contabilità clienti**, quindi scegliere il collegamento correlato.
2. Nella finestra **Contabilità clienti** nella Scheda dettaglio **Numerazioni**, selezionare la numerazione desiderata per ogni scheda di vendita o documento.

Il numero selezionato risulterà utilizzato per compilare il campo **Nr.** nella scheda o nel documento in questione, in base alle impostazioni effettuate nella serie di numerazione.

## <a name="to-create-relationships-between-number-series"></a>Per creare relazioni tra numerazioni
È possibile creare relazioni tra codici di numero di serie se ne sono stati impostati più di uno per lo stesso tipo di informazione o transazione di base. Questa funzione può essere utile per selezionare il codice corretto, al momento di utilizzare un numero.

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Nr. serie**, quindi scegliere il collegamento correlato.
2. Selezionare la riga contenente la numerazione per la quale si desidera creare delle relazioni, quindi scegliere **Relazioni**.
3. Nel campo **Codice serie** immettere il codice della numerazione che si desidera associare alla serie selezionata nel passaggio 2.
4. Aggiungere una riga per ogni codice che si desidera associare alla numerazione selezionata.
5. Chiudere la finestra.

Ogni volta che verrà impostato un elemento che richiede un numero, è ora possibile utilizzare le relazioni che sono state create per selezionare la numerazione corretta tra quelle poste in relazione.

## <a name="see-also"></a>Vedi anche
[Impostazione di [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

