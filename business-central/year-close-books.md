---
title: Panoramica delle attività di chiusura dei registri
description: Informazioni sul processo di chiusura dei registri contabili per un anno fiscale o un periodo e su cosa accade dopo la chiusura di un anno.
author: jswymer
ms.topic: overview
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'year closing, close accounting period, close fiscal year, bank account detailed trial balance'
m.search.form: 100
ms.date: 04/01/2021
ms.author: jswymer
---
# <a name="closing-the-books" />Chiusura dei registri
Dopo avere verificato che tutti i conti sono aggiornati e assegnato costi ed entrate, è possibile chiudere i registri per un anno fiscale o un periodo.

Non è obbligatorio chiudere un anno, ma se si esegue questa operazione è più semplice lavorare con il programma in quanto è possibile utilizzare le comode opzioni di filtro fornite. Non è inoltre necessario preoccuparsi di perdere i dettagli relativi alle transazioni, in quanto tali dettagli vengono conservati anche dopo la chiusura dell'anno.

## <a name="closing-book-process" />Processo di chiusura dei libri
Il processo di chiusura dei libri include le seguenti attività principali:

1. Chiusura del periodo contabile.

    Un anno fiscale è definito come uno o più periodi aperti definiti nella pagina **Periodi contabili**. Un tipico anno fiscale contiene 12 periodi di un mese, tuttavia è possibile scegliere un altro metodo per definire un anno.

    Per ulteriori informazioni, vedere [Chiudere i periodi contabili](year-close-account-periods.md).
2. Registrazione dei movimenti dell'anno precedente.

    Quando si chiude un anno fiscale, è necessario immettere un numero di transazioni amministrative, ad esempio articoli prepagati e sospesi. Tali transazioni sono dette movimenti di rettifica. Non vi sono regole speciali per la registrazione di questi movimenti e, come altri movimenti, se vengono registrati in una data di un anno fiscale chiuso, contengono un segno di spunta nel campo **Mov. anno prec.** Anche se l'anno fiscale è stato chiuso, è possibile registrarvi dei movimenti C/G.
3. Trasferimento dei saldi dai conti economici al conto patrimoniale.

    Dopo la chiusura di un anno fiscale e la registrazione di tutti i movimenti dell'anno precedente, è necessario chiudere i conti economici e trasferire il fatturato netto dell'anno in un conto come capitale netto nello stato patrimoniale. A questo scopo utilizzare il processo batch Chiudi conto economico. Il processo batch elabora tutti i conti di contabilità generale di tipo Conto economico e crea movimenti che stornano i saldi. Tali movimenti vengono inseriti in una registrazione da cui possono essere contabilizzati. I movimenti non vengono contabilizzati automaticamente dal processo batch, eccetto quando viene utilizzata una valuta addizionale. In questo caso la contabilizzazione viene effettuata direttamente nella contabilità generale.

    Per ulteriori informazioni, vedere [Chiudere il conto economico](year-close-income-statement.md).
4. Registrazione del movimento di chiusura di fine anno insieme alla compensazione dei movimenti conti patrimonio netto.

    Una volta completato il processo batch di chiusura del conto economico, registrare i movimenti generati dal processo. Se non è stato specificato un conto profitti/perdite nel processo batch, immettere una riga con un movimento di contropartita che registra il fatturato netto nel conto di contabilità generale corretto nello stato patrimoniale. Contabilizzare infine le registrazioni.

    Per ulteriori informazioni, vedere [Registrare il movimento di chiusura di fine anno](year-how-post-year-end-close-entry.md).

## <a name="what-happens-when-you-close" />Cosa accade alla chiusura
Quando si effettua la chiusura alla fine dell'anno, gli utili calcolati vengono spostati in un conto profitti/perdite. L'anno fiscale viene inoltre contrassegnato come "chiuso," e tutti i movimenti successivi per l'anno chiuso vengono contrassegnati come "movimenti dell'anno precedente".

Viene quindi generato un movimento di chiusura, che non viene però registrato automaticamente. È possibile creare il movimento o i movimenti conti patrimonio netto di compensazione, per stabilire come assegnare il movimento di chiusura. Se, ad esempio, nella società sono presenti più divisioni, è possibile fare in modo che venga generato un singolo movimento di chiusura per tutte le divisioni, quindi creare un movimento di compensazione per il conto patrimonio netto di ogni divisione.

È possibile effettuare registrazioni in un anno fiscale precedente, anche dopo la chiusura dei conti economici, se, successivamente, si esegue di nuovo il processo batch Chiudi conto economico.

## <a name="see-also" />Vedere anche

[Utilizzare periodi contabili e anni fiscali](finance-accounting-periods-and-fiscal-years.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
