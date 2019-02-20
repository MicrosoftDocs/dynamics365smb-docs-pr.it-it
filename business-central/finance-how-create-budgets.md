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
ms.date: 01/07/2019
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: a98027c3ef3171491f84197897f93cbed4e288c2
ms.openlocfilehash: ca0648c3c3ccbfb02c910a063e6ac199e7b4b6d4
ms.contentlocale: it-it
ms.lasthandoff: 01/07/2019

---
# <a name="create-gl-budgets"></a>Creare budget C/G
È possibile mantenere più budget per periodi di tempo identici creando budget con nomi separati. Innanzitutto è necessario impostare il nome del budget e immettere le relative cifre. Il nome del budget viene quindi inserito in tutti i movimenti di budget che vengono creati.  

 Quando si crea un budget, è possibile definire quattro dimensioni per ogni budget. Queste quattro dimensioni specifiche per un singolo budget sono definite dimensioni budget. Le dimensioni budget possono essere scelte tra le dimensioni impostate Le dimensioni budget possono essere utilizzate per applicare filtri ai budget oppure per aggiungere informazioni sulle dimensioni ai movimenti budget. Per ulteriori informazioni, vedere [Utilizzo delle dimensioni](finance-dimensions.md).

 I budget giocano un ruolo importante in business intelligence, ad esempio nel rendiconto finanziario definito in base alle situazioni contabili che includono movimenti budget oppure quando si analizzano gli importi a budget rispetto agli importi effettivi nel piano dei conti. Per ulteriori informazioni, vedere [Business Intelligence](bi.md).

 I budget giocano un ruolo importante in business intelligence, ad esempio nel rendiconto finanziario definito in base alle situazioni contabili che includono movimenti budget oppure quando si analizzano gli importi a budget rispetto agli importi effettivi nel piano dei conti. Per ulteriori informazioni, vedere [Business Intelligence](bi.md).

Nella contabilità industriale si utilizzano i budget costi in modo simile. Per altre informazioni, vedere [Creazione di budget di costi](finance-create-cost-budgets.md).    

## <a name="to-create-a-new-gl-budget"></a>Per creare un nuovo budget C/G  
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Budget C/G** e quindi scegliere il collegamento correlato.  
2. Scegliere l'azione **Modifica lista** e compilare i campi necessari. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Scegliere l'azione **Modifica budget**.
4. All'inizio della pagina **Budget**, compilare i campi secondo le necessità per definire cosa viene visualizzato.  

    Verranno visualizzati solo i movimenti che contengono il nome del budget indicato nel campo **Nome budget**. Poiché il nome budget è appena stato creato non ci saranno movimenti corrispondenti al filtro. Di conseguenza, la pagina sarà vuota.  
5. Per immettere un importo, selezionare la appropriata nella matrice. Verrà visualizzata la pagina **Movimenti budget C/G**.  
6. Creare una nuova riga e compilare il campo **Importo**. Chiudere la pagina **Movimenti budget C/G**.  
7. Ripetere i passaggi da 5 a 6 per immettere tutti gli importi del budget.  

> [!NOTE]  
>  Nella Scheda dettaglio **Filtri** è possibile filtrare le informazioni in base alle dimensioni di budget impostate per il nome del budget.

## <a name="exporting-and-importing-gl-budgets-with-excel"></a>Esportazione e importazione di budget C/G con Excel
Per praticamente tutte le altre pagine, è possibile esportare dati nelle pagine del budget in Excel per una successiva elaborazione o analisi. Per ulteriori informazioni, vedere [Esportazione dei dati aziendali in Excel](about-export-data.md).

> [!NOTE]
> Il piano dei conti su cui i budget C/G sono basati include righe di tipo di conto Testata contenenti il totale delle righe sottostanti. Quando si esporta un budget C/G, i dati in tutte le righe vengono esportati indipendentemente dal tipo di conto. Tuttavia, solo i dati nelle righe del tipo di conto Analitico possono essere reimportate. Di conseguenza: <br /><br /> **Quando si importa un budget C/G, tutti i valori presenti nelle righe Testata verranno eliminati.** <br /><br /> Questo per evitare totali non corretti dopo l'importazione di dati creati o modificati in Excel.<br /><br /> **Scenario**: il nuovo costo degli stipendi a budget sarà di 1.200.000 VL. Si desidera lasciare il budget del reparto Stipendi per le tre righe specifiche (di tipo di conto Analitico) per gli impiegati a tempo pieno, gli impiegati part-time e gli aiutanti temporanei. Le tre righe sono raggruppate sotto una riga di intestazione Stipendi.<br /><br />Si immette 1.200.000 nella riga di intestazione, si esporta il budget in Excel e quindi lo si invia al reparto Stipendi, indicando di distribuire 1.200.000 VL.<br /><br /> Il reparto Stipendi distribuisce la somma su tre conti di registrazione. Quando si reimporta nel budget C/G, i tre conti vengono compilati con i nuovi dati Excel, con totale 1.200.000 VL, e la riga di intestazione è vuota.

## <a name="see-also"></a>Vedi anche
[Esportazione dei dati aziendali in Excel](about-export-data.md)  
[Finanze](finance.md)  
[Business Intelligence](bi.md)  
[Impostazione di dati finanziari](finance-setup-finance.md)  
[Contabilità generale e piano dei conti](finance-general-ledger.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

