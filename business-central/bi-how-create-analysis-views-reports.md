---
title: Creare report di analisi
description: 'Descrive come creare nuovi report di analisi per vendite, acquisti e magazzino e impostare modelli di analisi.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '555, 556, 557, 558, 9372, 9370, 9371'
ms.date: 09/22/2022
ms.author: edupont
---
# <a name="create-analysis-reports" />Creare report di analisi

I direttori vendite devono analizzare il turnover, il margine lordo e altri indicatori di prestazioni vendite principali periodicamente. Gli addetti agli acquisti sono più interessati alle dinamiche dei volumi di acquisto, alle prestazioni dei fornitori e ai prezzi di acquisto. Mentre i responsabili di logistica e magazzino necessitano informazioni sull'indice di rotazione delle giacenze, l'analisi dei movimenti di magazzino e le statistiche sul valore di magazzino. Quindi non esiste un report di analisi valido per tutti.

Puoi personalizzare i report di analisi in base ai record delle transazioni registrate, ad esempio vendite, acquisti, trasferimenti e rettifiche magazzino. In un report personalizzabile i dati di origine, derivati dai movimenti contabili degli articoli a cui sono associati movimenti di valorizzazione, possono essere combinati, confrontati e presentati nel formato più appropriato definito dall'utente. Da questo punto di vista, il report Analisi è molto simile a un report tabella pivot di Microsoft Excel.  

Quindi, ad esempio, puoi creare un report personalizzato che si concentra sui tuoi conti chiave in termini di fatturato totale del prodotto in importi e quantità vendute, profitto lordo e percentuale di profitto lordo durante il mese corrente. Quindi puoi far confrontare queste cifre con i risultati dei mesi precedenti o dello stesso mese dell'anno precedente e calcolare le deviazioni. Tutte queste operazioni possono essere effettuate nella stessa visualizzazione, che ti consente di visualizzare le cause di aree problematiche identificate e anche scegliere il pulsante a discesa per accedere ai dettagli a livello delle singole transazioni.  

Il report di analisi è costituito dagli oggetti che si desidera analizzare, ad esempio clienti, categorie clienti, agenti e così via, sotto forma di righe e dai parametri di analisi, ovvero dalla modalità desiderata per l'analisi degli oggetti, sotto forma di colonne, ad esempio calcoli del margine, confronti periodici tra importi e volumi di vendita oppure confronti periodici tra valori effettivi e previsti. 

Oltre ai report di analisi, puoi creare e visualizzare informazioni simili nelle visualizzazioni di analisi, che sono basate sulle dimensioni. Per ulteriori informazioni, vedi [Analizzare i dati per dimensioni](bi-how-analyze-data-dimension.md).

## <a name="example" />Esempio

Puoi impostare queste righe (oggetti che vuoi analizzare):  

- Computer  
- Monitor  
- Ricambi  

Quindi puoi impostare queste colonne (come vuoi che gli oggetti vengano analizzati):  

- Vendite mese corrente  
- Vendite mese precedente  
- Percentuale vendite mese precedente  

## <a name="setting-up-line-and-column-layouts" />Impostazione dei layout di riga e di colonna

Nella pagina **Report analisi**, è possibile visualizzare layout di riga e colonna diversi che hai impostato:

* Nella pagina **Modelli righe analisi** dove è possibile definire il nome del report e gli oggetti che si desidera visualizzare nelle righe del report e
* Nella pagina **Modelli colonne analisi** dove è possibile definire il nome del modello colonna e i parametri di analisi che vuoi visualizzare nel report come colonne. Ogni riga in questa pagina rappresenta una colonna nel report. 

Si noti che le righe analisi e le colonne analisi sono indipendenti tra loro.  

In base alle righe e alle colonne impostate, il risultato del report viene aggregato da [!INCLUDE[prod_short](includes/prod_short.md)] nella pagina **Report analisi** come nella tabella seguente.  

|- |Vendite mese corrente|Vendite mese precedente|Percentuale vendite mese precedente|  
|-|-|-|-|  
|Computer| | | |  
|Monitor| | | |  
|Pezzi di ricambio| | | |  
|Totale| | | |  

È ad esempio possibile impostare un gruppo di layout di riga e svariati gruppi di layout di colonna per visualizzare rispettivamente i report mensili e i report annuali.

## <a name="set-up-analysis-column-templates" />Impostare modelli colonne analisi

La seguente procedura è basata sulle visualizzazioni di analisi per le vendite. I passaggi sono simili a quelli delle visualizzazioni di analisi di magazzino e di acquisto.

Un modello colonne analisi contiene un set di righe, che rappresentano una colonna di analisi nel report di analisi. Per definire una colonna, è necessario assegnare un codice di tipo di analisi a una riga. Questo codice tipo analisi determina il tipo di dati di origine nei movimenti contabili articoli su cui sarà basata l'analisi. I dati di origine possono includere costo, importo vendita o quantità e i relativi movimenti di valorizzazione associati. Puoi impostare il numero di modelli di colonna desiderato, quindi utilizzarli per creare nuovi report di analisi.    

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Modelli colonne vendite**, quindi scegli il collegamento correlato.  
2. Seleziona la prima riga vuota e compila i campi necessari.
3. Scegliere l'azione **Colonne**.  
4. Nella pagina **Colonne Analisi** compila i campi per specificare le colonne da includere nel report analisi.  

    > [!NOTE]  
    > Per definire una colonna, è necessario compilare il campo **Codice tipo analisi** per tutti i tipi di colonna ad eccezione di **Formula**. La pagina **Tipi di analisi** consente di impostare i codici di tipo di analisi.  
    
    Inoltre, se si seleziona **Mov. articoli** nel campo **Tipo mov. contabile**, i valori effettivi verranno copiati dai movimenti contabili articoli. Se si seleziona **Movimenti budget articoli**, i valori previsti verranno copiati dal budget.  
5. Scegli **OK** per salvare le modifiche.  

## <a name="set-up-analysis-line-templates" />Impostare modelli di righe di analisi

La seguente procedura è basata sui report di analisi per le vendite. I passaggi sono simili a quelli dei report di analisi di magazzino e di acquisto.

Un modello righe analisi contiene un set di righe, che rappresentano una riga di analisi nel report di analisi. In una riga è possibile specificare un articolo o un insieme di articoli, clienti, fornitori o gruppi. È inoltre possibile creare una formula in una riga per calcolare la somma delle altre righe. Puoi impostare il numero desiderato di modelli di righe e utilizzarli per creare nuovi report di analisi.   

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Modelli righe vendite**, quindi scegli il collegamento correlato.  
2. Seleziona la prima riga vuota e compila i campi necessari.
3. Scegliere l'azione **Righe**.  
4. Nella pagina **Righe Analisi** creare le righe relative agli articoli, ai clienti, ai fornitori o agli agenti di cui si desidera visualizzare i valori nel report analisi. È necessario compilare i campi **Tipo**, **Range** e **Descrizione**.  

> [!NOTE]  
> In alternativa, per creare più righe distinte per ogni articolo, cliente e così via, puoi selezionare il punto di inserimento appropriato e consentire il completamento dei campi necessari della riga. Se necessario, è possibile modificare manualmente le righe. Per inserire righe, scegli l'azione **Inserisci articoli** o **Inserisci gruppi articoli**.  

## <a name="create-a-new-sales-analysis-report" />Creare un nuovo report di analisi delle vendite

La seguente procedura è basata sui report di analisi per le vendite. I passaggi sono simili a quelli dei report di analisi di magazzino e di acquisto.

Con i report di analisi puoi valutare in dettaglio la dinamica delle vendite in base a determinati indicatori chiave delle performance di vendita, quali ad esempio turnover di vendita sia in importi che in quantità, margine lordo di contribuzione, stato delle vendite effettive confrontato con il budget. I report di analisi possono inoltre essere utilizzati per analizzare i prezzi di vendita medi e per valutare le performance della forza di vendita.  

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Report analisi vendite**, quindi scegli il collegamento correlato.  
2. Nella pagina **Report analisi vendite** scegliere l'azione **Nuovo**.
3. Compila i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Scegliere l'azione **Modifica report analisi**.
5. Nella pagina **Report analisi vendite** scegliere l'azione **Mostra matrice**.  

> [!NOTE]  
> La creazione di combinazioni di modelli di righe e colonne per i report di analisi e l'assegnazione di nomi univoci sono facoltative. In tal caso, non è necessario selezionare modelli di riga e colonna nella pagina **Report Analisi Vendite**. Dopo aver scelto un nome per il report, è possibile modificare i modelli di righe e colonne in modo indipendente e quindi tornare a selezionare nuovamente il nome del report per ripristinare la combinazione originale.

## <a name="see-also" />Vedere anche

[Business Intelligence finanziario](bi.md)  
[Finanze](finance.md)  
[Impostazione di dati finanziari](finance-setup-finance.md)  
[Contabilità generale e piano dei conti](finance-general-ledger.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
