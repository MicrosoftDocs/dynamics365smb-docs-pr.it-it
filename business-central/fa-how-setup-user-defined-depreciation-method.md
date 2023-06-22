---
title: Impostare un metodo di ammortamento del cespite definito dall'utente
description: 'In Business Central, è possibile applicare un metodo di ammortamento definito dall''utente per definire il metodo di ammortamento del cespite nella pagina Scheda cespite.'
author: jill-kotel-andersson
ms.reviewer: edupont
ms.topic: conceptual
ms.search.keywords: user-depreciation
ms.date: 07/05/2021
ms.author: edupont
---

# <a name="set-up-fixed-assets-with-user-defined-depreciation-methods" />Impostare i cespiti con metodi di ammortamento definiti dall'utente

Puoi usare [!INCLUDE[prod_short](includes/prod_short.md)] per impostare i metodi di ammortamento definiti dall'utente come descritto qui.

Per ogni metodo personalizzato, occorre inserire nella pagina **Tabelle Ammortamento** una percentuale di ammortamento per ogni periodo (mese, trimestre, anno o periodo contabile). Quando si assegna un registro beni ammortizzabili con un metodo definito dall'utente a un cespite, è necessario impostare i campi **Data iniz. amm. personalizzato** e **Data inizio ammortamento** sulla pagina **Registro beni amm. cespiti** per i cespiti specifici.  

La formula per il calcolo dell'importo di ammortamento è la seguente:  

*Importo di ammortamento = (% ammortamento x numero di giorni di ammortamento x base ammortizzabile) / (100 x 360)*


> [!NOTE]  
> Mentre la data nel campo **Data iniz. amm. personalizzato** viene utilizzato per determinare gli intervalli di tempo, è il campo **Data inizio ammortamento** che viene utilizzato per determinare il numero di giorni di ammortamento. Se il valore in **Data iniz. amm. personalizzato** è antecedente al valore di **Data inizio ammortamento**, la percentuale relativa al primo periodo nella tabella di ammortamento verrà utilizzata solo parzialmente quando viene calcolato il primo ammortamento. Ciò significa che il cespite non verrà ammortizzato completamente entro la fine dell'ultimo periodo.

## <a name="to-assign-a-depreciation-book-to-a-fixed-asset-with-a-user-defined-depreciation-method" />Per assegnare un registro beni ammortizzabili a un cespite con un metodo di ammortamento definito dall'utente

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Cespiti**, quindi scegli il collegamento correlato.
2. Selezionare il cespite per il quale si desidera impostare un registro beni ammortizzabili.
3. Scegli l'azione **Correlato** quindi scegli **Cespite**, poi **Registri beni ammortizzabili**. Questo apre la pagina **Registro beni amm. cespiti**.

   Per impostazione predefinita, alcuni dei campi che devono essere compilati secondo le istruzioni seguenti sono nascosti, quindi è necessario visualizzarli. Per fare ciò è necessario personalizzare la pagina. Per ulteriori informazioni, vedere [Per avviare la personalizzazione di una pagina tramite il banner Personalizzazione](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).
4. Nel campo **Metodo ammortamento**, selezione **Definito dall'utente**.
5. Nel campo **Cod. tabella ammortamento**, seleziona la **tabella di ammortamento** che vuoi usare.
6. Nel campo **Data inizio ammortamento**, seleziona la data di inizio per il calcolo dell'ammortamento.
7. Quando usi un metodo definito dall'utente, il campo **Data iniz. amm. personalizzato** deve essere impostato su una data uguale o precedente al campo **Data inizio ammortamento**. Se hai selezionato un valore nel campo **Periodo** nella tabella di ammortamento, la data contenuta nel campo **Data iniz. amm. personalizzato** deve essere la data iniziale di un periodo contabile.
8. Compila il campo **Nr. anni di ammortamento** o il campo **Data finale ammortamento**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] 

## <a name="to-set-up-user-defined-depreciation-methods" />Per impostare i metodi di ammortamento personalizzati

La pagina **Tabella ammortamento** consente di impostare metodi di ammortamento personalizzati. Ad esempio, è possibile impostare l'ammortamento in base al numero di unità.  

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Tabelle ammortamento**, quindi scegli il collegamento correlato.  
2. Nella pagina **Lista tabelle ammortamento** scegliere l'azione **Nuovo**.  
3. Nella pagina **Scheda tabella ammortamento** compila i campi secondo le necessità. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

> [!TIP]
> Utilizzare la funzione **Crea tabella somma cifre** per definire una tabella di ammortamento basata sul metodo *Somma di cifre*.

Con il metodo *Somma di cifre*, se i cespiti vengono ammortizzati in 4 anni, l'ammortamento per ogni anno viene calcolato nel modo seguente:

Somma di cifre = 1 + 2 + 3 + 4 = 10 Ammortamento:

* Anno 1 = 4/10  
* Anno 2 = 3/10  
* Anno 3 = 2/10  
* Anno 4 = 1/10  

### <a name="depreciation-based-on-number-of-units" />Ammortamento in base al numero di unità

Il metodo personalizzato può essere utilizzato anche per effettuare l'ammortamento in base al numero di unità, ad esempio nel caso di produzione di macchinari con una determinata durata totale di funzionamento. Nella pagina **Tabelle Ammortamento** è possibile immettere il numero di unità che possono essere prodotte in ogni periodo (mese, trimestre, anno o periodo contabile).  

### <a name="example---user-defined-depreciation" />Esempio - ammortamento definito dall'utente

Ai fini del calcolo dell'imposta sul reddito, l'utilizzo di un determinato metodo di ammortamento consente di ammortizzare i cespiti più velocemente.  

A fini fiscali, per un cespite della durata utile di tre anni si utilizzerebbero i seguenti tassi di ammortamento:  

* Anno 1: 25%  
* Anno 2: 38%  
* Anno 3: 37%  

Il costo di acquisto è VL 100.000 e la durata dell'ammortamento è di 5 anni. L'ammortamento viene calcolato annualmente.  

| Date | Tipo reg. cespite | Giorni | Importo | Valore contabile |
| --- | --- | --- | --- | --- |
| 01/01/20 |Costo di acquisto |Data inizio ammortamento |100,000.00 |100,000.00 |
| 31/12/20 |Deprezzamento |360 |-25.000,00 |75,000.00 |
| 31/12/21 |Deprezzamento |360 |-38.000,00 |37,000.00 |
| 31/12/22 |Deprezzamento |360 |-37.000,00 |0 |
| 31/12/23 |Deprezzamento |Nessuno |Nessuno |0 |
| 31/12/24 |Deprezzamento |Nessuno |Nessuno |0 |

Nell'esempio precedente, entrambi i campi **Data iniz. amm. personalizzato** e **Data inizio ammortamento** sarebbero impostati su 01/01/20 nella pagina **Registro beni amm. cespiti** per i cespiti specifici. Se invece nel campo **Data iniz. amm. personalizzato** fosse indicata la data 01/01/20 e nel campo **Data inizio ammortamento** la data riportata fosse 01/04/20, il risultato sarebbe:  

| Date | Tipo reg. cespite | Giorni | Importo | Valore contabile |
| --- | --- | --- | --- | --- |
| 01/01/20 |Costo di acquisto |Data inizio ammortamento |100,000.00 |100,000.00 |
| 31/12/20 |Deprezzamento |270 |-18.750,00 |81,250.00 |
| 31/12/21 |Deprezzamento |360 |-38.000,00 |42,250.00 |
| 31/12/22 |Deprezzamento |360 |-37.000,00 |6,250.00 |
| 31/12/23 |Deprezzamento |90 |-6.250,00 |0 |
| 31/12/24 |Deprezzamento |Nessuno |Nessuno |0 |


## <a name="see-also" />Vedere anche
[Impostazione di cespiti](fa-setup.md)  
[Cespiti](fa-manage.md)  
[Impostare l'ammortamento dei cespiti](fa-how-setup-depreciation.md)  
[Metodi ammortamento per cespiti](fa-depreciation-methods.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
