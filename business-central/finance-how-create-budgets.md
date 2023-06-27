---
title: Creazione di budget C/G
description: Descrive come creare i budget C/G per prevedere diverse attività finanziarie e assegnare le dimensioni per scopi di business intelligence.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: postpone
ms.search.form: '113, 120, 121, 154, 350, 422, 7132, 7133, 7138, 7139, 9203, 9219, 9239, 9373, 9374'
ms.date: 08/24/2022
ms.author: edupont
---
# <a name="create-gl-budgets"></a>Creare budget C/G

È possibile mantenere più budget per periodi di tempo identici creando budget con nomi separati. Innanzitutto è necessario impostare il nome del budget e immettere le relative cifre. Il nome del budget viene quindi inserito in tutti i movimenti di budget che vengono creati.  

Quando crei un budget, puoi definire quattro dimensioni specifiche del budget, denominate dimensioni budget, per ogni budget. Seleziona le dimensioni del budget per ogni budget tra quelle che hai già impostato. Le dimensioni budget possono essere utilizzate per applicare filtri ai budget oppure per aggiungere informazioni sulle dimensioni ai movimenti budget. Per ulteriori informazioni, vedi [Utilizzare le dimensioni](finance-dimensions.md).

I budget svolgono un ruolo importante nella business intelligence. Gli esempi includono un rendiconto finanziario basato su report finanziari che includono movimenti di budget o quando si analizzano gli importi a budget rispetto a quelli effettivi nel piano dei conti. Per ulteriori informazioni vedi [Business Intelligence](bi.md).

Nella contabilità industriale si utilizzano i budget costi in modo simile. Per ulteriori informazioni, vedi [Creazione di budget di costi](finance-create-cost-budgets.md).  

## <a name="to-create-a-new-gl-budget"></a>Per creare un nuovo budget C/G

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Budget C/G**, quindi scegli il collegamento correlato.  
2. Scegli l'azione **Modifica lista** e compila i campi necessari. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Scegliere l'azione **Modifica budget**.
4. All'inizio della pagina **Budget**, compilare i campi secondo le necessità per definire cosa viene visualizzato.  

    Verranno visualizzati solo i movimenti che contengono il nome del budget indicato nel campo **Nome budget**. Poiché il nome budget è appena stato creato, non ci saranno movimenti corrispondenti al filtro. Di conseguenza, la pagina sarà vuota.  
5. Per immettere un importo, selezionare la appropriata nella matrice. Verrà visualizzata la pagina **Movimenti budget C/G**.  
6. Creare una nuova riga e compilare il campo **Importo**. Chiudere la pagina **Movimenti budget C/G**.  
7. Ripeti i passaggi da 5 a 6 per immettere tutti gli importi del budget.  

> [!NOTE]  
> Nella Scheda dettaglio **Filtri** è possibile filtrare le informazioni in base alle dimensioni di budget impostate per il nome del budget.

## <a name="exporting-and-importing-gl-budgets-with-excel"></a>Esportazione e importazione di budget C/G con Excel

Per praticamente tutte le altre pagine, è possibile esportare dati nelle pagine del budget in Microsoft Excel per una successiva elaborazione o analisi. Per ulteriori informazioni vedi [Esportazione dei dati aziendali in Excel](about-export-data.md).

> [!NOTE]
> Il piano dei conti, su cui si basano i budget di contabilità generale (C/G), ha righe di tipo di conto Testata che contengono il totale delle righe sottostanti. Quando si esporta un budget C/G, i dati in tutte le righe vengono esportati indipendentemente dal tipo di conto. Tuttavia, solo i dati nelle righe del tipo di conto Analitico possono essere reimportate. 

Di conseguenza, quando importi un budget C/G, tutti i valori presenti nelle righe Testata vengono eliminati. Questo per evitare totali non corretti dopo l'importazione di dati creati o modificati in Excel.

### <a name="scenario"></a>Scenario

Il nuovo costo degli stipendi a budget sarà di 1.200.000 in valuta locale. Vuoi consentire al reparto Stipendi di definire il budget per le tre righe specifiche (di tipo di conto Analitico) per i dipendenti a tempo pieno, i dipendenti part-time e gli aiutanti temporanei. Le tre righe sono raggruppate sotto una riga di intestazione Stipendi.

Immetti 1.200.000 nella riga di intestazione, esporti il budget in Excel e quindi lo invii al reparto Stipendi, indicando di distribuire 1.200.000 VL.

Il reparto Stipendi distribuisce la somma su tre conti di registrazione. Quando si reimporta nel budget C/G, i tre conti vengono compilati con i nuovi dati Excel, con totale 1.200.000 VL, e la riga di intestazione è vuota.

## <a name="see-related-microsoft-training"></a>Vedi il relativo [training Microsoft](/training/modules/budgets-exchange-rates-dynamics-365-business-central/index)

## <a name="see-also"></a>Vedere anche

[Esportazione dei dati aziendali in Excel](about-export-data.md)  
[Finanze](finance.md)  
[Business Intelligence](bi.md)  
[Impostazione di dati finanziari](finance-setup-finance.md)  
[Contabilità generale e piano dei conti](finance-general-ledger.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
