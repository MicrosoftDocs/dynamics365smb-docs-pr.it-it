---
title: Creazione di budget C/G | Microsoft Docs
description: "Descrive come creare i budget C/G per prevedere diverse attività finanziarie e assegnare le dimensioni per scopi di business intelligence."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: postpone
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: dd3be77519075b67a942402bd01d5a2a562a1c32
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="create-gl-budgets"></a>Creare budget C/G
È possibile mantenere più budget per periodi di tempo identici creando budget con nomi separati. Innanzitutto è necessario impostare il nome del budget e immettere le relative cifre. Il nome del budget viene quindi inserito in tutti i movimenti di budget che vengono creati.  

 Quando si crea un budget, è possibile definire quattro dimensioni per ogni budget. Queste quattro dimensioni specifiche per un singolo budget sono definite dimensioni budget. Le dimensioni budget possono essere scelte tra le dimensioni impostate Le dimensioni budget possono essere utilizzate per applicare filtri ai budget oppure per aggiungere informazioni sulle dimensioni ai movimenti budget. Per ulteriori informazioni, vedere [Utilizzo delle dimensioni](finance-dimensions.md).

 I budget giocano un ruolo importante in business intelligence, ad esempio nel rendiconto finanziario definito in base alle situazioni contabili che includono movimenti budget oppure quando si analizzano gli importi a budget rispetto agli importi effettivi nel piano dei conti. Per ulteriori informazioni, vedere [Business Intelligence](bi.md).

 I budget giocano un ruolo importante in business intelligence, ad esempio nel rendiconto finanziario definito in base alle situazioni contabili che includono movimenti budget oppure quando si analizzano gli importi a budget rispetto agli importi effettivi nel piano dei conti. Per ulteriori informazioni, vedere [Business Intelligence](bi.md).

Nella contabilità industriale si utilizzano i budget costi in modo simile. Per altre informazioni, vedere [Creazione di budget di costi](finance-create-cost-budgets.md).    

## <a name="to-create-a-new-gl-budget"></a>Per creare un nuovo budget C/G  
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Budget C/G**, quindi scegliere il collegamento correlato.  
2. Scegliere l'azione **Modifica lista** e compilare i campi necessari. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Scegliere l'azione **Modifica budget**.
4. All'inizio della finestra **Budget**, compilare i campi secondo le necessità per definire cosa viene visualizzato.  

    Verranno visualizzati solo i movimenti che contengono il nome del budget indicato nel campo **Nome budget**. Poiché il nome budget è appena stato creato non ci saranno movimenti corrispondenti al filtro. Di conseguenza, la finestra sarà vuota.  
5. Per immettere un importo, selezionare la appropriata nella matrice. Verrà visualizzata la finestra **Movimenti budget C/G**.  
6. Creare una nuova riga e compilare il campo **Importo**. Chiudere la finestra **Movimenti budget C/G**.  
7. Ripetere i passaggi da 5 a 6 per immettere tutti gli importi del budget.  

> [!NOTE]  
>  Nella Scheda dettaglio **Filtri** è possibile filtrare le informazioni in base alle dimensioni di budget impostate per il nome del budget.   

## <a name="see-also"></a>Vedi anche
[Finanze](finance.md)  
[Business Intelligence](bi.md)  
[Impostazione di dati finanziari](finance-setup-finance.md)  
[Contabilità generale e piano dei conti](finance-general-ledger.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

