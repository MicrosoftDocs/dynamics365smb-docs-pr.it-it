---
title: Importare transazioni retribuzioni| Documenti Microsoft
description: "Per gestire lo stipendio, importare e registrare le transazioni finanziarie dal provider di retribuzioni nella contabilità generale, utilizzando un'estensione di retribuzione quale Ceridian o Quickbooks."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Ceridian, Quickbooks, salary
ms.date: 06/16/2017
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 52ed67b2f2e08cbb2f4104c2b0c26f662212a9f4
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="import-payroll-transactions"></a>Importa transazioni retribuzioni
Per indicare i pagamenti di stipendio e le transazioni correlate, è necessario importare e registrare in contabilità generale le transazioni finanziarie trasformate dal provider di retribuzioni. A tale scopo, è necessario innanzitutto importare un file che si riceve dal provider di retribuzioni nella finestra **Contabilità generale**. Successivamente si esegue il mapping tra i conti esterni nel file retribuzioni e i conti C/G pertinenti. Infine, si registrano le transazioni retribuzioni in base alla mappatura dei conti.

> [!NOTE]  
>   Per utilizzare questa funzione, è necessario installare e abilitare un'estensione per l'importazione delle retribuzioni. Il Registro paga di Ceridian e le estensioni per l'importazione del file retribuzioni di Quickbooks sono preinstallati in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Per maggiori informazioni, vedere [Personalizzazione di [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzando le estensioni](ui-extensions.md).

## <a name="to-import-a-payroll-file"></a>Per importare un file delle retribuzioni
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Registrazioni COGE**, quindi scegliere il collegamento correlato.
2. Nel batch registrazioni COGE appropriato scegliere l'azione **Importa transazioni retribuzioni**. Si apre una guida al setup assistito.
3. Seguire i passaggi indicati nella finestra **Importa transazioni retribuzioni**.

    > [!TIP]  
    >   Nel passaggio relativo alla mappatura dei record di retribuzione esterni ai conti C/G, i mapping eseguiti verranno ricordati che la successiva importazione degli stessi record. In questo modo si risparmia tempo in quando non occorre compilare manualmente il campo **Nr. conto** nelle registrazioni COGE ogni volta che si importano transazioni retribuzioni periodiche.   

    Se si sceglie il pulsante **OK** nella guida al setup assistito, la finestra **Contabilità generale** viene popolata con le righe che rappresentano le transazioni che contiene il file retribuzioni e con i conti appropriati già precompilati nei campi **Conto C/G** in base ai mapping effettuati nella guida.
4. Modificare o registrare le righe delle registrazioni relative a tutte le altre le transazioni della contabilità generale. Per ulteriori informazioni, vedere [Registrare le transazioni direttamente nella contabilità generale](finance-how-post-transactions-directly.md).   

## <a name="see-also"></a>Vedi anche
[Finanze](finance.md)  
[Personalizzazione di [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzando le estensioni](ui-extensions.md)  
[Utilizzo delle registrazioni COGE](ui-work-general-journals.md)  

