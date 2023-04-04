---
title: Impostare i calendari del reparto produzione
description: La creazione e l'abilitazione di un calendario dell'area di produzione comporta diverse attività tra cui l'impostazione dei calendari del reparto di produzione e la creazione di turni di lavoro.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '9291, 9293, 9295, 99000750, 99000751, 99000752, 99000753, 99000759, 99000769, 99000770, 99000771, 99000772, 99000920'
ms.date: 06/22/2021
ms.author: edupont
---
# Impostare i calendari del reparto produzione

In un calendario delle aree di produzione o dei centri di lavoro sono specificati i giorni e gli orari lavorativi, i turni, le ferie e le assenze che determinano la capacità lorda disponibile dell'area o del centro, misurata in tempo, sulla base dei valori definiti per l'efficienza e la capacità di tale area o centro.

Come base per il calcolo di un calendario specifico delle aree di produzione o dei centri di lavoro è prima di tutto necessario configurare uno o più calendari del reparto produzione generali. In un calendario del reparto produzione viene definita una settimana lavorativa standard in termini di ora di inizio e di fine di ogni giorno lavorativo e di relazione di turni lavorativi. In tale calendario sono inoltre disponibili le ferie fisse nel corso di un anno.  

Di seguito viene descritto come impostare i calendari delle aree di produzione. I passaggi sono gli stessi della procedura per l'impostazione dei calendari dei centri di lavoro.  

## Per creare turni lavorativi  
1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Turni lavorativi**, quindi scegli il collegamento correlato.  
2.  In una riga vuota immettere un numero nel campo **Codice** per identificare il turno lavorativo, ad esempio **1**.  
3.  Descrivere il turno lavorativo nel campo **Descrizione**, ad esempio **1mo Turno**.  
4.  Facoltativamente, compilare le righe relative a un secondo o terzo turno lavorativo.  

Anche se nelle aree di produzione specificate non vengono effettuati turni diversi, immettere almeno un codice di turno lavorativo.  

## Per impostare un calendario reparto prod.  
1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Calendari reparto prod.**, quindi scegli il collegamento correlato.  
2.  In una riga vuota immettere un numero nel campo **Codice** per identificare il calendario reparto prod.  
3.  Nel campo **Descrizione** immettere una descrizione del calendario.  
4.  Scegliere l'azione **Giorni lavorativi**.
5.  Nella pagina **Giorni lavorativi rep. prod.**, specificare una settimana lavorativa completa, con l'ora di inizio e di fine per ogni giorno.  

    Nel campo **Cod. turno lavorativo** , selezionare uno dei turni precedentemente definiti. Aggiungere una riga per ogni giorno lavorativo e ogni turno. Ad esempio:  

    Lunedì 07.00 15.00 1   
    Martedì 07.00 15.00 1  

    Se è necessario un calendario reparto prod. con due turni lavorativi, occorre compilarlo come illustrato nell'esempio seguente:  

    Lunedì 07.00 15.00 1   
    Lunedì 15.00 23.00 2  
    Martedì 07.00 15.00 1  
    Martedì 15.00 23.00 2  

    Eventuali giorni della settimana non definiti nel calendario reparto produz., ad esempio sabato e domenica, verranno semplicemente considerati giorni non lavorativi e la relativa capacità disponibile sarà pari a zero in un calendario aree di produzione.  

    Dopo avere definito tutti i giorni lavorativi di una settimana, è possibile chiudere la pagina **Giorni Lavorativi Rep. Prod.** e procedere all'immissione delle ferie:  

6.  Nella pagina **Calendari reparto prod.**, selezionare il calendario del reparto produzione, quindi scegliere l'azione **Ferie**.
7. Nella pagina **Cal. festività rep. prod.**, definire le ferie dell'anno specificando l'ora e la data di inizio e fine e la descrizione di ogni festività in righe distinte. Ad esempio:  

    04/07/14 0.00.00 23.59.00 Vacanze estive  
    05/07/14 0.00.00 23.59.00 Vacanze estive  
    06/07/14 0.00.00 23.59.00 Vacanze estive  

La capacità disponibile per le ferie definite sarà pari a zero in un calendario delle aree di produzione.  

È ora possibile assegnare il calendario reparto prod. a un'area di produzione per calcolare il calendario reparto prod. su cui sarà basata la pianificazione di tutte le operazioni in tale area di produzione.  

## Per calcolare un calendario aree di produzione  

1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Aree di produzione**, quindi scegli il collegamento correlato.
2. Aprire l'area di produzione che si desidera aggiornare.  
3. Nel campo **Cod. calendario reparto prod.**, selezionare il calendario del reparto produzione da utilizzare come base per un calendario delle aree di produzione.  
4. Scegliere l'azione **Calendario**.  
5. Nella pagina **Calendario aree di prod.**, scegliere l'azione **Mostra matrice**.  

    Nel lato sinistro della pagina della matrice sono elencate le aree di produzione configurate. Nella parte destra è disponibile un calendario, in cui vengono visualizzati i valori relativi alla capacità disponibile per giorno lavorativo nell'unità di misura specificata, ad esempio **480** minuti. Ogni riga rappresenta il calendario relativo a un'area di produzione.  

    > [!NOTE]  
    >  È anche possibile selezionare i valori di capacità per ogni settimana o mese cambiando l'opzione del campo **Visualizza per** nella pagina **Calendario aree di prod.**.  

    Per riflettere il nuovo calendario di reparto come riga dell'area di produzione selezionata, è necessario prima calcolarlo.  

6.  Scegliere l'azione **Calcola**.  
7.  Nella Scheda dettaglio **Area di produzione** è possibile impostare un filtro per eseguire il calcolo solo per un'area di produzione. Se non si imposta alcun filtro, verranno calcolati tutti i calendari delle aree di produzione esistenti.  
8.  Definire la data di inizio e di fine del periodo di calendario da calcolare, ad esempio un anno, dal giorno 01/01/14 al 31/12/14.
9. Scegliere **OK** per calcolare la capacità.  

Vengono ora creati o aggiornati i movimenti di calendario, in cui viene visualizzata la capacità disponibile per ogni periodo sulla base dei tre gruppi seguenti di dati master:  

- Giorni e turni lavorativi definiti nel calendario reparto prod. assegnato.  
- Valore specificato nel campo **Capacità** della scheda area di produzione.  
- Valore specificato nel campo **Efficienza** della scheda dell'area di produzione.  

Il calendario calcolato dell'area di produzione definirà ora quando e quanta capacità è disponibile in quest'area di produzione. Ciò controlla la pianificazione dettagliata delle operazioni eseguite nell'area di produzione.  

## Per registrare un'assenza dell'area di produzione  
1.  Nella pagina **Calendario aree di prod.**, scegliere l'azione **Mostra matrice**.
2. Nella pagina **Matrice calendario aree di prod.** selezionare l'area di produzione e il giornio di calendario in cui registrare l'orario di assenza, quindi scegliere l'azione **Assenze**.  
3.  Nella pagina **Assenze** definire l'ora di inizio, l'ora di fine e la descrizione dell'assenza relativa al giorno specificato. Ad esempio:  

    25/01/01 08.00 10.00 Manutenzione  

4.  Scegliere l'azione **Aggiorna** e chiudere la pagina **Assenze**.  

La capacità del giorno selezionato risulta ora diminuita in base al tempo di assenza registrato.  

## Vedi anche  
[Impostare i calendari di base](across-how-to-assign-base-calendars.md)  
[Impostare aree di produzione e centri di lavoro](production-how-to-set-up-work-and-machine-centers.md)  
[Impostazione della produzione](production-configure-production-processes.md)  
[Manufacturing](production-manage-manufacturing.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]