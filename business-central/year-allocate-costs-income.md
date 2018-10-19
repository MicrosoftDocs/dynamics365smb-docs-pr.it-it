---
title: "Panoramica delle attività per l'allocazione di costi e ricavi | Documenti Microsoft"
description: "Descrive i task necessari per assegnare un movimento in una registrazione COGE a più conti diversi, quando tale registrazione viene contabilizzata."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 2291f45cda61f72cbabc8a39b2463903c641ad97
ms.contentlocale: it-it
ms.lasthandoff: 09/28/2018

---
# <a name="allocate-costs-and-income"></a>Allocazione di costi e ricavi
È possibile assegnare un movimento in una registrazione generale a più conti diversi, quando tale registrazione viene contabilizzata. L'assegnazione può essere effettuata in base a tre diversi metodi:

* Quantità
* Percentuale (%)
* Importo

Le funzionalità di assegnazione possono essere utilizzate per le registrazioni COGE periodiche e le registrazioni cespiti.
<!--You can also distribute the cost or revenue of a line to an intercompany partner when you post a sales or purchase document. When you post the document, a line will be posted in your general journal, and a corresponding line will be created in the intercompany outbox.-->

Di seguito viene descritto come preparare l'allocazione dei costi in una registrazione COGE periodica definendo le chiavi di allocazione. Quando le chiavi di allocazione sono definite, è possibile completare e contabilizzare le registrazioni come qualsiasi altra registrazione COGE periodica. Per ulteriori informazioni, vedere [Utilizzo delle registrazioni COGE](ui-work-general-journals.md).

## <a name="to-set-up-allocation-keys"></a>Per impostare le chiavi di allocazione
È possibile assegnare un movimento in una registrazione COGE periodica a più conti diversi, quando tale registrazione viene contabilizzata. L'allocazione può essere effettuata per quantità, percentuale o importo.
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Reg. periodiche generali** e quindi scegliere il collegamento correlato.
2. Scegliere il campo **Nome batch** per aprire la finestra **Batch registrazioni COGE**.
3. È possibile modificare le allocazioni in un batch esistente nell'elenco o creare un nuovo batch con le allocazioni.
   * Per creare un nuovo batch, scegliere l'azione **Nuovo** e andare al passaggio successivo.
   * Per modificare le allocazioni di registrazioni esistenti, selezionare le registrazioni e andare al passaggio 7.    
4. Nel campo **Nome** immettere un nome per il batch, ad esempio PULIZIE. Nel campo **Descrizione** immettere una descrizione, ad esempio Registrazioni spese pulizie.
5. Al termine, chiudere la finestra. Verrà visualizzata una nuova registrazione periodica vuota.
6. Compilare i campi nella riga.
7. Scegliere l'azione **Allocazioni**.
8. Aggiungere una riga per ciascuna allocazione. È necessario compilare il campo **Allocazione %**, **Quantità allocazione** o **Importo**. È necessario compilare anche il campo **Nr. conto** e, se si sta allocando la transazione tra dimensioni globali, anche i campi delle dimensioni globali.
9. Se in una riga è stata immessa una percentuale, il valore del campo **Importo** viene calcolato automaticamente. Questi importi hanno il segno opposto rispetto all'importo totale nel campo **Importo** delle registrazioni periodiche.
10. Dopo aver immesso le righe di allocazione, scegliere **OK** per tornare alla finestra **Reg. periodiche generali**. Il campo **Importo allocato (VL)** viene compilato e corrisponde al campo **Importo**.
11. Effettuare la registrazione.

## <a name="to-change-an-allocation-key-that-has-already-been-set-up"></a>Per modificare una chiave di allocazione già impostata
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Reg. periodiche generali** e quindi scegliere il collegamento correlato.
2. Nella finestra **Registrazioni periodiche generali** selezionare le registrazioni con l'allocazione.
3. Selezionare la riga con l'allocazione e scegliere l'azione **Allocazioni**.
4. Cambiare i campi pertinenti e quindi scegliere **OK**.

## <a name="see-also"></a>Vedi anche
[Chiusura di anni e periodi](year-close-years-periods.md)  
[Utilizzo delle registrazioni COGE](ui-work-general-journals.md)    
[Contabilizzazione dei documenti e delle registrazioni](ui-post-documents-journals.md)    
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

