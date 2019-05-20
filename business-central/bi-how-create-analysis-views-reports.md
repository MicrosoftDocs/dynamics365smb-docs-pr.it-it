---
title: Creare report di analisi| Documenti Microsoft
description: Descrive come creare nuovi report di analisi per vendite, acquisti e magazzino e impostare modelli di analisi.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: e8744455f41897f00315968cc10f12f18bf042b9
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/29/2019
ms.locfileid: "1245260"
---
#  <a name="create-analysis-reports"></a>Creare report di analisi
I direttori vendite devono analizzare il turnover, il margine lordo e altri indicatori di prestazioni vendite principali periodicamente. Gli addetti agli acquisti sono più interessati alle dinamiche dei volumi di acquisto, alle prestazioni dei fornitori e ai prezzi di acquisto. Mentre i responsabili di logistica e magazzino necessitano informazioni sull'indice di rotazione delle giacenze, l'analisi dei movimenti di magazzino e le statistiche sul valore di magazzino.  

I report Analisi consentono di creare report personalizzati, basati sui record delle transazioni registrate, ad esempio vendite, acquisti, trasferimenti e rettifiche magazzino. In un report personalizzabile i dati di origine, derivati dai movimenti contabili degli articoli a cui sono associati movimenti di valorizzazione, possono essere combinati, confrontati e presentati nel formato più appropriato definito dall'utente. Da questo punto di vista, il report Analisi è molto simile a un report tabella pivot di Microsoft Excel.  

È possibile creare un report personalizzato, incentrato sui conti principali in termini di turnover totale a livello di importi e quantità vendute, margine lordo e percentuale di margine lordo nel corso del mese corrente, quindi confrontare i valori ottenuti con i risultati dei mesi precedenti o dello stesso mese nell'anno precedente e infine calcolare le deviazioni. Tutte queste operazioni possono essere effettuate nella stessa visualizzazione, che consente di visualizzare le cause di aree problematiche identificate scegliendo il pulsante a discesa per accedere ai dettagli a livello delle singole transazioni.  

Il report Analisi è costituito dagli oggetti che si desidera analizzare, ad esempio clienti, categorie clienti, agenti e così via, sotto forma di righe e dai parametri di analisi, ovvero dalla modalità desiderata per l'analisi degli oggetti, sotto forma di colonne, ad esempio calcoli del margine, confronti periodici tra importi e volumi di vendita oppure confronti periodici tra valori effettivi e previsti.

Oltre ai report di analisi, è possibile creare e visualizzare informazioni simili nelle visualizzazioni di analisi, che sono basate sulle dimensioni. Per ulteriori informazioni, vedere [Analizzare i dati per dimensioni](bi-how-analyze-data-dimension.md).

## <a name="example"></a>Esempio  
È possibile configurare righe analoghe alle seguenti:  
- Computer  
- Monitor  
- Pezzi di ricambio  

Si possono quindi configurare colonne analoghe alle seguenti:  

- Vendite mese corrente  
- Vendite mese precedente  
- Percentuale vendite mese precedente  

## <a name="setting-up-line-and-column-layouts"></a>Impostazione dei layout di riga e di colonna  
 Nella pagina **Report analisi**, è possibile visualizzare layout di riga e colonna diversi a seconda di ciò che è stato impostato. Le righe o i modelli righe devono essere impostati nella pagina **Modelli righe analisi**. In questa pagina è possibile definire il nome del report e gli oggetti che si desidera visualizzare nelle righe del report. Le colonne devono essere impostate nella pagina **Modelli colonne analisi**. In questa pagina è possibile definire il nome del modello colonna e i parametri di analisi che si desidera visualizzare nel report come colonne. Nella pagina **Modelli colonne analisi** ogni riga rappresenta una colonna nel report. Si noti che le righe analisi e le colonne analisi sono indipendenti tra loro.  

In base alle righe e alle colonne impostate, il risultato del report viene aggregato automaticamente nella pagina della matrice **Report Analisi**, come nel seguente esempio:  

| |Vendite mese corrente|Vendite mese precedente|Percentuale vendite mese precedente|  
|-|-|-|-|  
|Computer| | | |  
|Monitor| | | |  
|Pezzi di ricambio| | | |  
|Totale| | | |  

 È ad esempio possibile impostare un insieme di layout di riga e svariati insiemi di layout di colonna per visualizzare rispettivamente i report mensili e i report annuali.

 ## <a name="to-set-up-analysis-column-templates"></a>Per impostare modelli colonne analisi
La seguente procedura è basata sulle visualizzazioni di analisi per le vendite. I passaggi sono simili a quelli delle visualizzazioni di analisi di magazzino e di acquisto.

I parametri di analisi vengono visualizzati sotto forma di colonne di un report di analisi. L'impostazione di modelli di colonne di analisi consente di definire le colonne da includere nel report di analisi.  

Un modello contiene un insieme di righe, che rappresentano le colonne di analisi visualizzate nel report di analisi. Per definire una colonna, è necessario assegnare un codice di tipo di analisi a una riga. Questo codice tipo analisi determina il tipo di dati di origine nei movimenti contabili articoli su cui sarà basata l'analisi. I dati di origine comprendono costo, importo vendita o quantità e i relativi movimenti di valorizzazione associati. È possibile impostare il numero di modelli di colonna desiderato, quindi utilizzarli per creare nuovi report di analisi.    

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Modelli colonne vendite** e quindi scegliere il collegamento correlato.  
2. Selezionare la prima riga vuota e compilare i campi necessari.
3. Scegliere l'azione **Colonne**.  
4. Nella pagina **Colonne Analisi** compilare i campi per specificare le colonne da includere nel report analisi.  

    > [!NOTE]  
    >   Per definire una colonna, è necessario compilare il campo **Codice tipo analisi** per tutti i tipi di colonna ad eccezione di **Formula**. La pagina **Tipi di analisi** consente di impostare i codici di tipo di analisi.  
    Inoltre, se si seleziona **Mov. articoli** nel campo **Tipo mov. contabile**, i valori effettivi verranno copiati dai movimenti contabili articoli. Se si seleziona **Movimenti budget articoli**, i valori previsti verranno copiati dal budget.  
5.  Scegliere il pulsante **OK** per salvare le modifiche.  

## <a name="to-set-up-analysis-line-templates"></a>Per impostare modelli di righe di analisi  
La seguente procedura è basata sui report di analisi per le vendite. I passaggi sono simili a quelli dei report di analisi di magazzino e di acquisto.

Gli oggetti vengono visualizzati nelle righe di un report di analisi. L'impostazione di modelli di righe di analisi consente di definire le righe da includere nel report di analisi.  

Un modello contiene un insieme di righe, che rappresentano le righe di analisi visualizzate nel report di analisi. In una riga è possibile specificare un articolo o un insieme di articoli, clienti, fornitori o gruppi. È inoltre possibile creare una formula in una riga per calcolare la somma delle altre righe. È possibile impostare il numero desiderato di modelli di righe e utilizzarli per creare nuovi report di analisi.    

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Modelli righe vendite** e quindi scegliere il collegamento correlato.  
2. Selezionare la prima riga vuota e compilare i campi necessari.
3. Scegliere l'azione **Righe**.  
4. Nella pagina **Righe Analisi** creare le righe relative agli articoli, ai clienti, ai fornitori o agli agenti di cui si desidera visualizzare i valori nel report analisi. È necessario compilare i campi **Tipo**, **Range** e **Descrizione**.  

> [!NOTE]  
>   In alternativa, per creare più righe distinte per ogni articolo, cliente e così via, è possibile selezionare il punto di inserimento appropriato e consentire il completamento dei campi necessari della riga. Se necessario, è possibile modificare manualmente le righe. Per inserire righe, scegliere l'azione **Inserisci articoli** o **Inserisci gruppi articoli**.  

## <a name="to-create-a-new-sales-analysis-report"></a>Per creare un nuovo report di analisi delle vendite
La seguente procedura è basata sui report di analisi per le vendite. I passaggi sono simili a quelli dei report di analisi di magazzino e di acquisto.

I report di analisi consentono di valutare in dettaglio la dinamica delle vendite in base a determinati indicatori chiave delle performance di vendita, quali ad esempio turnover di vendita sia in importi che in quantità, margine lordo di contribuzione o stato delle vendite effettive confrontato con il budget. Il report può inoltre essere utilizzato per analizzare i prezzi di vendita medi e per valutare le performance della forza di vendita.  

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Report analisi vendite** e quindi scegliere il collegamento correlato.  
2. Nella pagina **Report analisi vendite** scegliere l'azione **Nuovo**.
3. Compilare i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Scegliere l'azione **Modifica report analisi**.
5. Nella pagina **Report analisi vendite** scegliere l'azione **Mostra matrice**.  

> [!NOTE]  
>   La creazione di combinazioni di modelli di righe e colonne per i report di analisi e l'assegnazione di nomi univoci sono facoltative. La scelta di un nome per il report rende superfluo selezionare modelli di riga e colonna nella pagina **Report Analisi Vendite**. Dopo aver scelto un nome per il report, è possibile modificare i modelli di righe e colonne in modo indipendente e quindi tornare a selezionare nuovamente il nome del report per ripristinare la combinazione originale.

## <a name="see-also"></a>Vedi anche
[Business Intelligence](bi.md)  
[Finanze](finance.md)  
[Impostazione di dati finanziari](finance-setup-finance.md)  
[Contabilità generale e piano dei conti](finance-general-ledger.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
