---
title: Creazione di budget C/G
description: Descrive come creare i budget C/G per prevedere diverse attività finanziarie e assegnare le dimensioni per scopi di business intelligence.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: postpone
ms.search.form: '113, 120, 121, 154, 350, 422, 7132, 7133, 7138, 7139, 9203, 9219, 9239, 9373, 9374'
ms.date: 06/10/2024
ms.service: dynamics-365-business-central
---
# <a name="create-gl-budgets"></a>Creare budget C/G

È possibile mantenere più budget per periodi di tempo identici creando budget con nomi separati. Innanzitutto è necessario impostare il nome del budget e immettere le relative cifre. Il nome del budget viene quindi inserito in tutti i movimenti di budget che vengono creati.  

Quando crei un budget, puoi assegnargli dimensioni specifiche del budget, denominate dimensioni budget. Puoi usare dimensioni budget per applicare filtri sui budget e per aggiungere informazioni sulle dimensioni ai movimenti budget. Per ulteriori informazioni, vedi [Utilizzare le dimensioni](finance-dimensions.md).

I budget svolgono un ruolo importante nella business intelligence. Gli esempi includono un rendiconto finanziario basato su report finanziari che includono movimenti di budget o quando si analizzano gli importi a budget rispetto a quelli effettivi nel piano dei conti. Per ulteriori informazioni vedi [Business Intelligence](bi.md).

Nella contabilità industriale si utilizzano i budget costi in modo simile. Per ulteriori informazioni, vedi [Creazione di budget di costi](finance-create-cost-budgets.md).  

## <a name="to-create-a-new-gl-budget"></a>Per creare un nuovo budget C/G

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Budget C/G**, quindi scegli il collegamento correlato.  
2. Scegli l'azione **Modifica lista** e compila i campi necessari. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Scegliere l'azione **Modifica budget**.
4. All'inizio della pagina **Budget**, compilare i campi secondo le necessità per definire cosa viene visualizzato.  

   La pagina mostra solo i movimenti che contengono il nome del budget indicato nel campo **Nome budget**. Poiché il nome budget è appena stato creato, non ci saranno movimenti corrispondenti al filtro. Di conseguenza, la pagina sarà vuota.  
5. Per immettere un importo, selezionare la appropriata nella matrice. Verrà visualizzata la pagina **Movimenti budget C/G**.  
6. Creare una nuova riga e compilare il campo **Importo**. Chiudere la pagina **Movimenti budget C/G**.  
7. Ripeti i passaggi 5 e 6 per tutti gli importi nel budget.  

> [!NOTE]  
> Nella Scheda dettaglio **Filtri** è possibile filtrare le informazioni in base alle dimensioni di budget impostate per il nome del budget.

## <a name="exporting-and-importing-gl-budgets-with-excel"></a>Esportazione e importazione di budget C/G con Excel

Per praticamente tutte le altre pagine, è possibile esportare dati nelle pagine del budget in Microsoft Excel per una successiva elaborazione o analisi. Per ulteriori informazioni vedi [Esportazione dei dati aziendali in Excel](about-export-data.md).

> [!NOTE]
> Il piano dei conti, su cui si basano i budget della contabilità generale (C/G), presenta righe del tipo di conto Intestazione. Queste righe contengono il totale delle righe sottostanti. Quando si esporta un budget C/G, si esportano dati in tutte le righe indipendentemente dal tipo di conto. Tuttavia, solo i dati nelle righe del tipo di conto Analitico possono essere importati.

Analogamente, quando importi un budget C/G, tutti i valori nelle righe Intestazione vengono eliminati. Vengono eliminati per evitare totali errati dopo l'importazione di dati creati o modificati in Excel.

### <a name="scenario"></a>Scenario

Il nuovo costo degli stipendi a budget sarà di 1.200.000 in valuta locale. Vuoi consentire al reparto Stipendi di definire il budget per le tre righe specifiche (di tipo di conto Analitico) per i dipendenti a tempo pieno, i dipendenti part-time e gli aiutanti temporanei. Le tre righe sono raggruppate sotto una riga di intestazione Stipendi.

Immetti 1.200.000 nella riga di intestazione, esporti il budget in Excel e quindi lo invii al reparto Stipendi, indicando di distribuire 1.200.000 in VL.

Il reparto Stipendi distribuisce la somma su tre conti di registrazione. Quando si reimporta nel budget C/G, i tre conti vengono compilati con i nuovi dati Excel, con totale 1.200.000 VL, e la riga di intestazione è vuota.

## <a name="see-also"></a>Vedere anche

[Esportazione dei dati aziendali in Excel](about-export-data.md)  
[Dati finanziari](finance.md)  
[Business Intelligence](bi.md)  
[Impostazione di dati finanziari](finance-setup-finance.md)  
[Contabilità generale e piano dei conti](finance-general-ledger.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
