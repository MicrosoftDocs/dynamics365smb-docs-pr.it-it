---
title: Utilizzare i profili per classificare i contatti
description: Informazioni su come impostare i questionari del profilo per aiutarti a classificare i profili dei tuoi contatti commerciali.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'contacts, profiles'
ms.search.form: '5109, 5110'
ms.author: bholtorf
ms.date: 05/20/2022
---

# Utilizzare i questionari profilo per classificare i contatti business

Puoi assegnare valutazioni ai potenziali clienti in modo da identificare quelli ideali e rivolgere loro la campagna di vendita. È possibile impostare questionari profilo da utilizzare durante l'immissione di informazioni sul profilo dei contatti. In ogni questionario, è possibile impostare le diverse domande da porre ai contatti. In questo modo, puoi raggruppare i contatti in modo che le tue campagne abbiano maggiori probabilità di rivolgersi alle persone giuste in base ai criteri che definisci con i questionari.  

Con i questionari corretti, puoi valutare i potenziali clienti e raggrupparli in categorie. È possibile utilizzare le domande e risposte esistenti, nonché combinarle con nuove domande e risposte per creare una base di valutazione. A ciascuna risposta nella valutazione è assegnato un valore del punto e, a seconda dell'intervallo impostato per le categorie, indicato dai campi *Da valore* e *A valore*, il sistema di valutazione raggrupperà i contatti nelle categorie definite. Ad esempio clienti *ABC*, fornitori ad *alta e bassa fedeltà* o potenziali clienti *Platino/Oro/Argento*.  

È inoltre possibile eseguire il questionario per rispondere automaticamente ad alcune domande sulla base dei dati di contatto, cliente o fornitore.  

## Per aggiungere un questionario profilo

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup questionario**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Nuovo**.  
3. Compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## Per aggiungere domande a un questionario profilo

1. Scegliere il questionario profilo pertinente e quindi scegliere l'azione **Modifica setup questionario**.  
2. Sulla prima riga vuota, nel campo **Tipo**, scegliere **Domanda** e digitare la domanda desiderata nel campo **Descrizione**. Compilare gli altri campi della riga.  

    Facoltativamente, aggiungi i dettagli alla domanda.

    1. Scegli la riga con la domanda, quindi scegli il menu **Riga** quindi scegli **Dettagli della domanda**.  

    2. Nella Scheda dettaglio **Classificazione** della pagina **Dettagli domande profilo** seleziona il campo **Classificazione auto contatto**.  

    3. Nel campo **Campo class. contatto** seleziona l'opzione **Valutazione**.  

    4. Compila il campo **% min. domande con risposta**. Il valore predefinito è **0**.  

        Questo specifica il numero di domande, espresso in percentuale, a cui occorre rispondere per il calcolo della valutazione.

    5. Nel gruppo **Pagina** della scheda **Azioni** scegli **Punti di risposta**. Immetti i punti che vuoi assegnare a ciascuna risposta elencata nella pagina **Punti di risposta**.

        Se vuoi avere una panoramica dei punti che hai assegnato a ciascuna risposta, scegli l'azione **Punti di risposta**.

    6. Per eseguire un aggiornamento, torna alla pagina **Setup questionario profilo**. Nel menu **Funzioni** della scheda **Azioni** scegli **Aggiornare classificazione**.

    Nella pagina **Setup questionario profilo** il numero di contatti che soddisfa questi criteri viene visualizzato nel campo **Nr. di contatti**, nonché nella **Scheda contatto** di ogni contatto.

3. Sulla prima riga vuota successiva nel campo **Tipo**, scegliere **Risposta** e digitare la risposta desiderata nel campo **Descrizione**.  
4. Nel campo **Priorità** selezionare la priorità. Nei campi **Da valore** e **A valore** definire un intervallo di punti. I contatti che ricevono punti entro l'intervallo stabilito otterranno la risposta.  

Ripetere tali passaggi per immettere tutte le domande e le risposte nel questionario profilo.

Dopo avere creato un questionario, puoi usarlo per valutare e classificare i contatti. È inoltre possibile impostare le domande classificate automaticamente in base alle informazioni presenti nella scheda contatto.  

> [!NOTE]
> Se immetti una domanda con risposta automatica, seleziona **Riga** e quindi **Dettagli domanda** per immettere i criteri da utilizzare per fornire la risposta automatica.

## Applicare i questionari ai contatti

Puoi applicare i tuoi questionari ai contatti manualmente. Apri la scheda conatto appropriata, quindi scegli l'azione **Profilo**. Quindi, una volta applicati i questionari che desideri applicare, puoi iniziare a utilizzare le categorie nelle tue campagne.  

## Classificazione automatica dei contatti

È possibile classificare automaticamente i contatti in base alle informazioni relative a cliente, fornitore e contatto, mediante una serie di domande sul profilo con risposta automatica nella pagina **Setup questionario profilo**.  

> [!NOTE]
> È possibile assegnare una classificazione basata sui dati dei clienti solo ai contatti registrati come clienti e una classificazione basata sui dati dei fornitori solo ai contatti registrati come fornitori. La classificazione automatica non viene aggiornata automaticamente. Si consiglia pertanto di aggiornare i questionari profilo una volta effettuato l'aggiornamento dei dati relativi a clienti, fornitori o contatti su cui tali questionari si basano.  

Dopo avere impostato le domande relative al profilo, se si assegna il questionario profilo a un contatto, le risposte corrette relative a tale contatto vengono assegnate automaticamente da [!INCLUDE[prod_short](includes/prod_short.md)].  

## Esempio

È possibile classificare i contatti in base al volume di acquisti da essi effettuati:

|Risposta|Si applica a|
|--- |--- |
|A|contatti che hanno effettuato acquisti per 500.000 VL o più|
|B|contatti che hanno effettuato acquisti per un importo compreso tra 100.000 e 499.999 VL|
|C|contatti che hanno effettuato acquisti per 99.999 VL o meno|

Per effettuare questa operazione, completare la pagina **Setup questionario profilo** nel modo seguente:

| Tipo     | Descrizione        | Classificazione automatica     | Da Valore | Al valore |
|----------|--------------------|------------------------------|------------|----------|
| Domanda | Classificazione di ABC | Fare clic per inserire un segno di spunta |            |          |
| Risposta   | A                  |                              | 500.000    |          |
| Risposta   | B                  |                              | 100,000    | 499,999  |
| Risposta   | C                  |                              |            | 99,999   |

Compilare la pagina **Dettagli domande profilo** nel modo seguente:

| Campo                         | Valore         |
|-------------------------------|---------------|
| Campo di classificazione del cliente | Vendite (LCY)   |
| Metodo di classificazione         | Valore definito |

Quando si assegna il questionario profilo contenente questa domanda a un contatto, la risposta pertinente al contatto viene automaticamente inserita nelle righe profilo della scheda del contatto.

## Vedere anche

[Creazione di contatti](marketing-create-contact-companies.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]