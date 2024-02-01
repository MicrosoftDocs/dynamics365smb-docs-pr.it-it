---
title: Definizione e allocazione dei costi
description: 'Con le allocazioni costi è possibile spostare i costi e i ricavi tra i tipi di costo, i centri di costo e gli oggetti di costo. È possibile definire tutte le allocazioni necessarie.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '1102, 1105, 1106, 1107, 1109, 1114'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="defining-and-allocating-costs"></a>Definizione e allocazione dei costi

Con le allocazioni costi è possibile spostare i costi e i ricavi tra i tipi di costo, i centri di costo e gli oggetti di costo. È possibile definire tutte le allocazioni necessarie. Ogni allocazione è costituita da:  

- Un'origine allocazione.  
- Uno o più destinazioni di allocazione.  

L'origine dell'allocazione stabilisce quali costi devono essere assegnati, mentre le destinazioni di allocazione determinano dove i costi devono essere allocati. Ad esempio, i costi per il tipo di costo Elettricità e riscaldamento sono un'origine di allocazione. Allocare tutti i costi del riscaldamento e dell'elettricità a tre centri di costo: Workshop, Produzione e Vendite. Questi centri di costi sono le destinazioni di allocazione.  

Per ogni origine di allocazione, è possibile definire un livello di allocazione, un periodo di validità e una variante come identificatore di gruppo. È possibile utilizzare un processo batch per impostare i filtri per selezionare le definizioni di allocazione e quindi eseguire le allocazioni costi automaticamente.  

Per ogni destinazione di allocazione, è possibile definire una base di allocazione. La base di allocazione può essere statica o dinamica.  

- Le basi di allocazioni statiche sono basate su un valore definito, come la superficie o un rapporto di allocazione stabilito, ad esempio 5:2:4.  
- Le basi di allocazioni dinamiche dipendono da valori variabili, quali il numero di impiegati in un centro di costo o i ricavi di vendite di un oggetto di costo in un determinato periodo di tempo.  

Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.

## <a name="setting-up-allocation-source-and-targets"></a>Impostare origini e destinazioni dell'allocazione

Ogni allocazione è costituita da un'origine di allocazione e da una o più destinazioni di allocazione. L'origine di allocazione definisce i costi che verranno allocati. Le destinazioni di allocazione determinano dove i costi verranno allocati.  

### <a name="to-set-up-cost-allocations"></a>Per impostare le allocazioni costi

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Allocazione costi**, quindi scegli il collegamento correlato.  
2. Nella pagina **Allocazione costi** scegliere l'azione **Modifica**.  
3. Immettere un ID dell'origine allocazione nel campo **ID**.  
4. Definire un livello come numero compreso tra 1 e 99 nel campo **Livello**. La registrazione di allocazione seguirà l'ordine dei livelli.  
5. Immettere un tipo di costo per definire quali di questi verranno allocati nel campo **Intervallo tipi di costo**. Se tutti i costi per un tipo di costo sono allocati, non viene definito alcun intervallo.  
6. Immettere un centro di costo insieme ai costi da allocare nel campo **Codice centro di costo**.  
7. Immettere un oggetto di costo insieme ai costi da allocare nel campo **Codice oggetto di costo**. Molto spesso questo campo rimane vuoto poiché gli oggetti di costo sono raramente allocati ad altri relativi oggetti.  
8. Immettere un tipo di costo nel campo **Importo dare in tipo di costo**. I costi allocati verranno accreditati al tipo di costo di origine. La registrazione di accredito verrà immessa nel tipo di costo specificato in questo punto.  
9. Definire i target di allocazione nella Scheda dettaglio **Righe**. Nel campo **Tipo di costo di destinazione** della prima riga immettere un tipo di costo. Esso consente di definire a quale tipo di costo viene addebitata l'allocazione.  
10. Nella prima riga immettere la prima destinazione di allocazione nel campo **Centro di costo di destinazione** o **Oggetto di costo di destinazione**. Questi due campi consentono di definire a quale centro di costo o oggetto di costo viene addebitata l'allocazione. È possibile compilare uno di questi campi, ma non entrambi.  
11. Ripetere gli stessi passaggi nella seconda riga per impostare destinazioni di allocazione aggiuntive.  
12. Dopo aver impostato le origini e le destinazioni delle allocazioni, scegliere **Calcola chiave di allocazione** per calcolare i valori delle quote totali.  

> [!NOTE]  
> Selezionare la casella di controllo **Bloccato** per disattivare l'impostazione dell'allocazione.

## <a name="setting-filters-for-dynamic-allocation-bases"></a>Impostazione di filtri per le basi di allocazione dinamica

Il metodo di allocazione dinamica si basa su valori variabili. Ad esempio, il numero di dipendenti in un centro di costo o gli articoli venduti di un oggetto di costo in un determinato intervallo di tempo specifico. Esistono nove basi di allocazione predefinite e dodici intervalli di date dinamici. Si impostano filtri diversi a seconda della base di allocazione.  

### <a name="setting-filters"></a>Impostazione filtri

Nella tabella seguente vengono indicati i filtri possibili per le diverse basi di allocazione e i valori validi nei campi **Filtro nr.** e **Filtro gruppo**. Seleziona <kbd>F1</kbd> nel campo **Codice filtro data** per leggere le descrizioni dettagliate.  

|**Base**|**Filtro nr.**|**Codice filtro data**|**Filtro centro di costo**|**Filtro oggetto di costo**|**Filtro gruppo**|  
|--------------|----------------------------------------|----------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------|  
|Movimenti C/G|Conto C/G|Sì|Sì|Sì|N/D|  
|Movimenti budget C/G|Conto C/G|Sì|Sì|Sì|Nome budget C/G|  
|Movimenti del tipo di costo|Tipo Costo|Sì|Sì|Sì|N/D|  
|Movimenti budget costi|Tipo Costo|Sì|Sì|Sì|Nome Budget|  
|Nr. di impiegati|N/D|Sì|Sì|Sì|N/D|  
|Articoli venduti (qtà)|Nr. Articolo|Sì|Sì|Sì|Cat. reg. magazzino|  
|Articoli acquistati (qtà)|Nr. Articolo|Sì|Sì|Sì|Cat. reg. magazzino|  
|Articoli venduti (importo)|Nr. Articolo|Sì|Sì|Sì|Cat. reg. magazzino|  
|Articoli acquistati (importo)|Nr. articolo|Sì|Sì|Sì|Gruppo registrazione magazzino|

## <a name="scenario-1-defining-static-allocations-based-on-allocation-ratio"></a>Scenario 1: definizione della allocazioni statiche in base al rapporto di allocazione

Il metodo di allocazione statica è basato su un valore definito, ad esempio i metri quadri utilizzati, o su un rapporto di allocazione stabilito, quale 5:2:4.  

In questo argomento viene descritto come definire i tre nuovi oggetti di costo di destinazione di allocazione per il centro di costo PROD di origine di allocazione utilizzando il rapporto di allocazione stabilito 5:2:4. I tre oggetti di costo di destinazione sono ACCESSORI, VERNICE e ARREDI.  

> [!NOTE]  
> Nell'esempio vengono utilizzati i dati di esempio di [!INCLUDE[prod_short](includes/prod_short.md)].  

### <a name="to-define-the-allocation-source-prod-cost-center-on-the-general-fasttab"></a>Per definire il centro di costo PROD di origine di allocazione nella Scheda dettaglio Generale

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Allocazione costi**, quindi scegli il collegamento correlato.  
2. Nella pagina **Allocazione costi** scegliere l'azione **Nuovo**.  
3. Nel campo **ID** seleziona <kbd>INVIO</kbd> o immetti un ID.  
4. Nel campo **Livello** immettere **1**.  
5. Nei campi **Data di inizio validità** e **Data di fine validità**, immettere le date appropriate.  
6. Nel campo **Codice centro di costo** immettere **PROD**.  
7. Nel campo **Importo dare in tipo di costo** immettere il tipo di costo **9903**.  

### <a name="to-define-the-allocation-target-cost-objects-on-the-lines-fasttab"></a>Per definire gli oggetti di costo di destinazione di allocazione nella Scheda dettaglio Righe

1. Nel campo **Tipo di costo di destinazione** della prima riga immettere **9903**.  
2. Nel campo **Oggetto di costo di destinazione** della prima riga selezionare **ACCESSO**.  
3. Nella prima riga nel campo **Tipo di destinazione allocazione** selezionare **Tutti i costi** per definire la modalità di allocazione di tutti i costi sospesi.  
4. Nella prima riga nel campo **Base** selezionare **Statica** per utilizzare il metodo di allocazione statica.  
5. Nella prima riga nel campo **Quota** immettere il rapporto di allocazione **5**.  
6. Nel campo **Tipo di costo di destinazione** della seconda riga immettere **9903**.  
7. Nel campo **Oggetto di costo di destinazione** della seconda riga selezionare **VERNICE**.  
8. Nella seconda riga nel campo **Tipo di destinazione allocazione** selezionare **Tutti i costi** per definire la modalità di allocazione di tutti i costi sospesi.  
9. Nella seconda riga nel campo **Base** selezionare **Statica** per utilizzare il metodo di allocazione statica.  
10. Nella seconda riga nel campo **Quota** immettere il rapporto di allocazione **2**.  
11. Nel campo **Tipo di costo di destinazione** della terza riga immettere **9903**.  
12. Nel campo **Oggetto di costo di destinazione** della terza riga selezionare **ARREDI**.  
13. Nella terza riga nel campo **Tipo di destinazione allocazione** selezionare **Tutti i costi** per definire la modalità di allocazione di tutti i costi sospesi.  
14. Nella terza riga nel campo **Base** selezionare **Statica** per utilizzare il metodo di allocazione statica.  
15. Nella terza riga nel campo **Quota** immettere il rapporto di allocazione **4**.  

> [!IMPORTANT]  
> In [!INCLUDE[prod_short](includes/prod_short.md)] il campo **Percentuale** viene calcolato automaticamente utilizzando un tasso percentuale che dipende da tutti e tre i rapporti di allocazione immessi nel campo **Quota**  per tutte e tre le righe.

## <a name="scenario-2-defining-dynamic-allocations-based-on-items-sold"></a>Scenario 2: definizione delle allocazioni dinamiche in base agli articoli venduti

In questo argomento viene visualizzato un esempio su come definire le allocazioni utilizzando il metodo di allocazione dinamica. Nell'esempio è possibile modificare l'assegnazione dinamica dei costi per il centro di costo VENDITE per supportare il nuovo oggetto di costo ATTREZZATURA IT. I numeri degli articoli dei colli di ATTREZZATURA IT sono inclusi nell'intervallo compreso tra 8904-W e 8924-W. Utilizzare le cifre di vendita dell'anno precedente per calcolare la quota. L'allocazione viene registrata nel tipo di costo di supporto 9903.  

> [!NOTE]  
> Nell'esempio vengono utilizzati i dati di esempio di [!INCLUDE[prod_short](includes/prod_short.md)].  

### <a name="to-define-dynamic-allocations-based-on-items-sold-in-the-previous-year"></a>Per definire le allocazioni dinamiche in base agli articoli venduti nell'anno precedente

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Allocazioni costi**, quindi scegli il collegamento correlato.  
2. Nella pagina **Allocazione costi** scegliere l'azione **Nuovo**.  
3. Nel campo **ID** seleziona <kbd>INVIO</kbd> o immetti un ID.  
4. Nel campo **Livello** immettere **1**.  
5. Nei campi **Data di inizio validità** e **Data di fine validità**, immettere le date appropriate.  
6. Nel campo **Codice centro di costo** immettere **VENDITE**.  
7. Nel campo **Importo dare in tipo di costo** immettere il tipo di costo **9903**.  
8. Nel campo **Tipo di costo di destinazione** immettere il tipo di costo **9903**.  
9. Nel campo **Oggetto di costo di destinazione** selezionare **Nuovo** per creare un nuovo oggetto di costo ATTREZZATURA IT e compilare i campi in base alle esigenze. Selezionare **ATTREZZATURA IT**. Lasciare vuoto il campo **Centro di costo di destinazione**.  
10. Nel campo **Tipo di destinazione allocazione** selezionare **Tutti i costi** per definire la modalità di allocazione di tutti i costi accumulati.  
11. Nel campo **Base** selezionare la base di allocazione **Articoli venduti (importo)**.  
12. Nel campo **Filtro nr.** immettere **8904-W..8924-W**.  
13. Nel campo **Codice filtro data**, immettere **Anno Precedente**.  
14. Per calcolare la quota, scegliere l'azione **Calcola chiave di allocazione**.  

> [!IMPORTANT]  
> In [!INCLUDE[prod_short](includes/prod_short.md)] vengono utilizzate le cifre di vendita degli anni precedenti per calcolare una quota di 1.596,50 VL con il 100% dei colli di ATTREZZATURA IT. Pertanto, tutti gli articoli venduti nell'ultimo anno verranno assegnati all'oggetto di costo ATTREZZATURA IT.

## <a name="see-also"></a>Vedere anche

 [Impostazione della contabilità industriale](finance-set-up-cost-accounting.md)  
 [Trasferimento e registrazione di movimenti di costi](finance-transfer-and-post-cost-entries.md)  
 [Contabilizzazione dei costi](finance-manage-cost-accounting.md)  
 [Terminologia della contabilità industriale](finance-terminology-in-cost-accounting.md)  
 [Informazioni sulla contabilità industriale](finance-about-cost-accounting.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
