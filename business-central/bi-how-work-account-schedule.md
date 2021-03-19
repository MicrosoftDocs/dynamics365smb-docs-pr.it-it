---
title: Generare report finanziari con le situazioni contabili
description: Descrive come utilizzare le situazioni contabili per creare le visualizzazioni e i report per analizzare i dati finanziari.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 584a3aa295ab3ec59a6f6a1e34017d0f9a67bc5c
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5389226"
---
# <a name="prepare-financial-reporting-with-account-schedules-and-account-categories"></a>Preparare i rendiconti finanziari con le situazioni contabili e le categorie di conti

Utilizzare le situazioni contabili per ottenere informazioni dettagliate sui dati finanziari memorizzati nel piano dei conti. Le situazioni contabili analizzano le cifre nei conti di contabilità generale e confrontano i movimenti di contabilità generale con i movimenti budget di contabilità generale. La visualizzazione dei risultati nei grafici nella Gestione ruolo utente, quali il piano del flusso di cassa e nei report, ad esempio i report Conto economico e Conto patrimoniale,

È possibile accedere a questi due report, ad esempio, con l'azione **Rendiconti finanziari** nella Gestione ruolo utente di Manager aziendale e Contabile.  

[!INCLUDE[prod_short](includes/prod_short.md)] fornisce alcune situazioni contabili di esempio che è possibile utilizzare immediatamente oppure è possibile impostare le proprie righe e colonne per specificare le cifre da confrontare. È ad esempio possibile creare piani dei conti per calcolare i margini di profitto in dimensioni quali reparti o gruppi di clienti. È possibile creare quanti rendiconti finanziari personalizzati si desidera.  

L'impostazione delle situazioni contabili richiede una comprensione dei dati finanziari nel piano dei conti. Per esempio, è possibile visualizzare i movimenti C/G come percentuali di movimenti budget. Tale operazione richiede che i budget siano creati. Per ulteriori informazioni, vedere [Creare budget C/G](finance-how-create-budgets.md).

## <a name="account-schedules"></a>Situazioni contabili

Le situazioni contabili sono utilizzate per organizzare i conti elencati nel piano dei conti in modi appropriati alla presentazione delle informazioni su tali conti. È possibile impostare vari layout per definire le informazioni che si desidera estrarre dal piano dei conti. Una delle principali funzioni dei piani dei conti consiste nel rendere disponibile un'area per i calcoli che non possono essere eseguiti direttamente nel piano dei conti, ad esempio creare subtotali per gruppi di conti in modo da poterli includere in nuovi totali e utilizzarli in altri totali. Gli utenti possono ad esempio creare piani dei conti per calcolare i margini di profitto in dimensioni quali reparti o gruppi di clienti. Inoltre è possibile filtrare movimenti di contabilità generale e movimenti budget di contabilità generale in base, ad esempio, al saldo periodo o all'importo dare.

È inoltre possibile confrontare due o più situazioni contabili e layout di colonna utilizzando le formule. Questo tipo di confronto consente di effettuare le seguenti operazioni:

* Creare report finanziari personalizzati.
* Creare tutte le situazioni contabili necessarie, ognuna con un nome univoco.
* Impostare vari layout di report e stampare i report con le cifre correnti.

## <a name="gl-account-categories"></a>Categorie conto C/G

Le categorie di conto C/G consentono di modificare il layout dei rendiconti finanziari. Dopo aver impostato le categorie di conto nella pagina **Categorie conto C/G** e aver scelto l'azione **Genera situazioni contabili**, le situazioni contabili sottostanti i report finanziari principali vengono aggiornate. Alla successiva esecuzione di uno dei report, ad esempio il report **Conto patrimoniale**, nuovi totali e voci secondarie vengono aggiunte, in base alle modifiche.

> [!NOTE]
> Le categorie di conto di livello superiore, come ad esempio il nodo **Passività** sono fisse e non è possibile aggiungere. Tuttavia, è possibile eliminare e aggiungere categorie di conto ai livelli inferiori e modificarne la struttura per definire la modalità di visualizzazione della situazione contabile correlata nei report.
>
> Si consiglia di creare e strutturare da zero le proprie categorie di conto C/G di livello inferiore, se necessario in una gerarchia, anziché tentare di riorganizzare quelle esistenti. Ad esempio, è possibile ristrutturare il nodo **Passività** per contenere un nuovo nodo **Equità** seguito dai nodi **Passività correnti** e **Debiti a lungo termine**.

## <a name="to-create-a-new-account-schedule"></a>Per creare una nuova situazione contabile

Utilizzare situazioni contabili per analizzare le cifre nei conti di contabilità generale o confrontare i movimenti di contabilità generale con i movimenti budget di contabilità generale. Per esempio, è possibile visualizzare i movimenti C/G come percentuali dei movimenti budget.

Le situazioni contabili nella versione standard di [!INCLUDE[prod_short](includes/prod_short.md)] sono la base dei report finanziari standard, che potrebbero non essere adatti alle esigenze dell'azienda. Per creare rapidamente i propri report finanziari, è possibile iniziare copiando una situazione contabile esistente. Vedere il passaggio 3 di seguito.

Nella pagina **Sintesi situaz. contabile** è possibile visualizzare un'anteprima del report finanziario definito dalla situazione contabile. Nella procedura seguente, è importante comprendere che le righe e le colonne della situazione contabile configurate possono essere visualizzate e convalidate solo nella pagina **Sintesi situaz. contabile**, a cui si accede da una situazione contabile scegliendo l'azione **Sintesi**. La pagina **Situazione contabile** è soltanto un'area di configurazione.  

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Situazioni contabili** e quindi scegliere il collegamento correlato.  
2. Nella pagina **Situazioni contabili** scegliere l'azione **Nuovo** per creare una nuova situazione contabile.
3. In alternativa, scegliere l'azione **Copia situazione contabile**, compilare i due campi, quindi scegliere **OK**.
4. Compilare i campi come necessario. Nel campo **Default layout colonna**, selezionare un layout esistente. Se necessario, è possibile modificarlo in seguito.

    I layout di colonna sono utilizzati per definire colonne per differenti parametri utilizzati per visualizzare i dati finanziari nelle righe. Ad esempio, è possibile creare un layout di colonna che compara saldo e saldo periodo per lo stesso periodo dell'anno in corso e di quello precedente, con quattro colonne. Per ulteriori informazioni, vedere [Per modificare un layout di colonna](bi-how-work-account-schedule.md#to-edit-a-column-layout).

5. Scegliere l'azione **Modifica situazione contabile**.
6. Creare una riga per ciascun elemento finanziario da visualizzare nel report, ad esempio una riga per i cespiti correnti e un'ulteriore riga per i cespiti. Per avere un'idea, vedere le situazioni contabili esistenti nella società di esempio CRONUS.
7. Scegliere l'azione **Sintesi** per visualizzare il report finanziario risultante.
8. Nella pagina **Sintesi situaz. contabile**, nel campo **Nome Layout colonna**, selezionare un altro layout di colonna per visualizzare i dati finanziari mediante altri parametri.
9. Scegliere il pulsante **OK**.

A questo punto, si è definita la base della situazione contabile, le righe dei dati finanziari da visualizzare e un layout esistente delle colonne per visualizzare i dati nelle righe per differenti parametri. Se il layout di colonna predefinito selezionato nel passaggio 4 non è adatto allo scopo, attenersi alla procedura seguente.

### <a name="to-edit-a-column-layout"></a>Per modificare un layout di colonna

I layout di colonna sono utilizzati per definire le colonne da includere nel report risultante. Ad esempio, è possibile creare un layout che metta a confronto saldo e saldo periodo per lo stesso periodo dell'anno in corso e di quello precedente.

> [!NOTE]
> In una versione stampata/visualizzata in anteprima/salvata di una situazione contabile è possibile visualizzare al massimo cinque colonne. Se la situazione contabile è utilizzata solo per l'analisi nella pagina **Sintesi situaz. contabile**, è possibile creare tutte le colonne necessarie.

1. Nella pagina **Situazioni contabili**, selezionare la situazione contabile pertinente, quindi scegliere l'azione **Modifica setup layout colonna**.
2. Nella pagina **Layout colonne**, creare una riga per ogni colonna utilizzata per visualizzare i dati finanziari nel report finanziario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Scegliere il pulsante **OK**.
4. Aprire la pagina **Sintesi situaz. contabile** di tanto in tanto per verificare che il nuovo layout di colonna funzioni come previsto.

> [!NOTE]
> Le colonne definite in ciascuna riga rappresentano la colonna 3 e le colonne successive nella pagina **Sintesi situaz. contabile**. Le prime due colonne, **Nr. riga** e **Descrizione**, sono fisse.  

### <a name="to-create-a-column-that-calculates-percentages"></a>Per creare una colonna per il calcolo delle percentuali

A volte, potrebbe essere necessario includere in una situazione contabile una colonna per il calcolo delle percentuali di un totale. Se, ad esempio, vi sono alcune righe in cui è prevista la suddivisione delle vendite per dimensioni, è possibile inserire una colonna per indicare la percentuale delle vendite totale rappresentata da ogni riga.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Situazioni contabili** e quindi scegliere il collegamento correlato.
2. Nella pagina **Descr. situazioni contabili** selezionare una situazione contabile.  
3. Selezionare l'azione **Modifica situazione contabile** per impostare una riga della situazione contabile per calcolare il totale su cui saranno basate le percentuali.  
4. Inserire una riga immediatamente sopra la prima riga per la quale si desidera visualizzare una percentuale.  
5. Compilare i campi della riga nel modo seguente: Nel campo **Tipo totale** immettere **Imposta base per percentuale**. Nel campo **Totale** immettere una formula del totale su cui sarà basata la percentuale. Ad esempio, se il totale vendite è incluso nella riga 11 immettere **11**.  
6. Scegliere l'azione **Modifica setup layout colonna** per impostare una colonna.  
7. Compilare i campi della riga nel modo seguente: nel campo **Tipo colonna** selezionare **Formula**. Nel campo **Formula** immettere una formula per l'importo per il quale si desidera calcolare la percentuale, seguita dalla percentuale (%). Ad esempio, se il numero di colonna N contiene il saldo periodo, immettere **N%**.  
8. Ripetere i passaggi da 4 a 7 per ogni gruppo di righe che di desidera suddividere per percentuale.

## <a name="to-set-up-account-schedules-with-overviews"></a>Per impostare situazioni contabili con sintesi

È possibile utilizzare una situazione contabile per creare un rendiconto in cui vengono confrontate le cifre C/G con le cifre del budget C/G.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Situazioni contabili** e quindi scegliere il collegamento correlato.
2. Nella pagina **Descr. situazioni contabili** selezionare una situazione contabile.  
3. Scegliere l'azione **Modifica situazione contabile**  
4. Nella pagina **Situazione contabile** selezionare il nome della situazione contabile di default nel campo **Nome**.
5. Scegliere l'azione **Inserisci conti**.  
6. Selezionare i conti che si intendono includere nella dichiarazione e selezionare il pulsante **OK**.

    I conti sono stati inseriti nella situazione contabile. È inoltre possibile modificare il layout colonna.  
7. Scegliere l'azione **Sintesi**.  
8. Nella pagina **Sintesi situaz. contabile**, nella scheda dettaglio **Filtri dimensione**, impostare il filtro budget con il nome di filtro desiderato.  
9. Scegliere il pulsante **OK**.  

Ora è possibile copiare e incollare la dichiarazione di budget in un foglio elettronico.  

## <a name="comparing-accounting-periods-using-period-formulas"></a>Confronto dei periodi contabili con le formule periodo

La situazione contabile consente di confrontare i risultati di diversi periodi contabili, ad esempio mese corrente rispetto allo stesso mese dell'anno precedente. Per eseguire questa operazione, aprire la pagina **Layout colonna** e personalizzala aggiungendo il campo **Formula confronto periodo** come colonna. Per ulteriori informazioni, vedere [Personalizzare l'area di lavoro](ui-personalization-user.md). È quindi possibile impostare quel campo su una formula del periodo.  

Un periodo contabile non deve corrispondere esattamente al calendario, ma ogni anno fiscale deve avere lo stesso numero di periodi contabili, che possono tuttavia avere una durata distinta.  

[!INCLUDE[prod_short](includes/prod_short.md)] usa la formula periodo per calcolare l'importo dal periodo di confronto in relazione al periodo rappresentato dal filtro data nella richiesta del report. Il periodo di confronto si basa sul periodo indicato dalla data di inizio del filtro data. Le abbreviazioni per l'indicazione dei periodi sono:

| Abbreviazione | Descrizione                                                                           |
| ------------ | ------------------------------------------------------------------------------------- |
| P            | Periodo                                                                                |
| UP           | Ultimo periodo di un trimestre, semestre o anno fiscale.                                   |
| CP           | Periodo corrente di un trimestre, semestre o anno fiscale. Usare CP nelle formule per impostare il periodo che inizia o finisce la formula. Ad esempio, FY\[1..CP\] indica il tempo dall'inizio dell'anno fiscale corrente al periodo corrente.|
| AF           | Anno fiscale. Ad esempio, FY\[1..3\] indica il primo trimestre dall'anno fiscale corrente |

Esempi di formule

| Formula         | Descrizione                                                                                     |
| --------------- | ----------------------------------------------------------------------------------------------- |
| \<Blank\>       | Periodo corrente                                                                                  |
| \-1P            | Periodo precedente                                                                                 |
| \-1FY\[1..LP\]  | Intero anno fiscale precedente                                                                     |
| \-1FY           | Periodo corrente nel precedente anno fiscale                                                          |
| \-1FY\[1..3\]   | Primo trimestre dell'anno fiscale trascorso                                                           |
| \-1FY\[1..CP\]  | Dall'inizio dell'anno fiscale trascorso al periodo corrente dell'anno fiscale trascorso, compresi entrambi i periodi |
| \-1FY\[CP..LP\] | Dal periodo corrente dell'anno fiscale trascorso all'ultimo periodo dell'anno fiscale trascorso, compresi entrambi i periodi   |

Se si desidera eseguire i calcoli in base a periodi di tempo regolari, è necessario invece immettere una formula nel campo **Formula confronto data**. Ad esempio, se il campo è impostato su -1A, in [!INCLUDE [prod_short](includes/prod_short.md)] viene effettuato il confronto con lo stesso periodo di un anno prima.

> [!NOTE]
> Non è sempre trasparente quali periodi si stanno confrontando perché è possibile impostare un filtro per data su un report che si estende su date diverse rispetto ai periodi contabili che si riflettono nei dati nel piano dei conti. Ad esempio, si crea una situazione contabile in cui si desidera confrontare il periodo corrente con lo stesso periodo dell'anno precedente, quindi si imposta il campo **Formula confronto data** su *-1AF*. Quindi, si esegue il report il 28 febbraio e si imposta il filtro della data su gennaio e febbraio. Di conseguenza, la situazione contabile confronta gennaio e febbraio di quest'anno con gennaio dell'anno scorso, che è l'unico periodo contabile completato dei due per l'anno prima.  

Per ulteriori informazioni sulle formule di data, vedere [Lavorare con le date e gli orari del calendario ](ui-enter-date-ranges.md).  

## <a name="see-related-training-at-microsoft-learn"></a>Vedere le informazioni relative al training in [Microsoft Learn](/learn/modules/configure-financial-reports-dynamics-365-business-central/index)

## <a name="see-also"></a>Vedere anche

[Business Intelligence](bi.md)  
[Finanze](finance.md)  
[Impostazione di dati finanziari](finance-setup-finance.md)  
[Contabilità generale e piano dei conti](finance-general-ledger.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]