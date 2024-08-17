---
title: Chiudere i libri
description: Informazioni sul processo di chiusura dei registri contabili per un anno fiscale o un periodo e su cosa accade dopo la chiusura di un anno.
author: jswymer
ms.topic: overview
ms.devlang: al
ms.search.keywords: 'year closing, close accounting period, close fiscal year, bank account detailed trial balance'
m.search.form: 100
ms.date: 08/05/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---

# <a name="closing-the-books"></a>Chiudere i libri
Dopo avere verificato che tutti i conti sono aggiornati e assegnato costi ed entrate, è possibile chiudere i registri per un anno fiscale o un periodo.

Non è obbligatorio Chiudi per un anno, ma farlo renderà più semplice lavorare nel sistema perché potrai sfruttare le comode opzioni di filtro fornite. Non è inoltre necessario preoccuparsi di perdere i dettagli relativi alle transazioni, in quanto tali dettagli vengono conservati anche dopo la chiusura dell'anno.

## <a name="closing-book-process"></a>Procedura di chiusura del libro
Il processo di chiusura dei libri include le seguenti attività principali:

1. Chiusura del periodo contabile.

    Un anno fiscale è definito come uno o più periodi aperti definiti nella pagina **Periodi contabili**. Un tipico anno fiscale contiene 12 periodi di un mese, tuttavia è possibile scegliere un altro metodo per definire un anno.

    Per ulteriori informazioni, vedere [Chiudere i periodi contabili](year-close-account-periods.md).
2. Registrazione dei movimenti dell'anno precedente.

    Quando si chiude un anno fiscale, è necessario immettere un numero di transazioni amministrative, ad esempio articoli prepagati e sospesi. Tali transazioni sono dette movimenti di rettifica. Non ci sono regole particolari per la registrazione di queste voci e, come altre voci, contengono un segno di spunta nel campo  **Voce dell'anno precedente** se vengono registrate in una data di un anno fiscale chiuso. Anche se l'anno fiscale è stato chiuso, è possibile registrarvi dei movimenti C/G.
3. Trasferimento dei saldi dai conti economici al conto patrimoniale.

    Dopo la chiusura di un anno fiscale e la registrazione di tutti i movimenti dell'anno precedente, è necessario chiudere i conti economici e trasferire il fatturato netto dell'anno in un conto come capitale netto nello stato patrimoniale. A questo scopo utilizzare il processo batch Chiudi conto economico. Il processo batch elabora tutti i conti di contabilità generale di tipo Conto economico e crea movimenti che stornano i saldi. Tali movimenti vengono inseriti in una registrazione da cui possono essere contabilizzati. Il batch job non li registra automaticamente, tranne quando viene utilizzata una valuta di rendicontazione aggiuntiva. In questo caso la contabilizzazione viene effettuata direttamente nella contabilità generale.

    Per ulteriori informazioni, vedere [Chiudere il conto economico](year-close-income-statement.md).
4. Registrazione del movimento di chiusura di fine anno insieme alla compensazione dei movimenti conti patrimonio netto.

    Una volta completato il processo batch di chiusura del conto economico, registrare i movimenti generati dal processo. Se non hai specificato un conto utili non distribuiti nel batch job, inserisci una riga con una registrazione di compensazione che registri l'utile netto nel conto contabilità generale corretto sotto il patrimonio netto nel bilancio. Contabilizzare infine le registrazioni.

    Per ulteriori informazioni, vedere [Registrare il movimento di chiusura di fine anno](year-how-post-year-end-close-entry.md).

## <a name="what-happens-when-you-close"></a>Cosa succede quando si effettua la chiusura

Quando si effettua la chiusura alla fine dell'anno, gli utili calcolati vengono spostati in un conto profitti/perdite. L'anno fiscale viene inoltre contrassegnato come "chiuso," e tutti i movimenti successivi per l'anno chiuso vengono contrassegnati come "movimenti dell'anno precedente".

Il sistema genera quindi una registrazione di chiusura, ma non la registra automaticamente. Ti viene data la possibilità di effettuare la registrazione o le registrazioni di compensazione del conto patrimoniale, il che ti consente di decidere come allocare la tua registrazione di chiusura. Se, ad esempio, nella società sono presenti più divisioni, è possibile fare in modo che venga generato un singolo movimento di chiusura per tutte le divisioni, quindi creare un movimento di compensazione per il conto patrimonio netto di ogni divisione.

È possibile effettuare registrazioni in un anno fiscale precedente, anche dopo la chiusura dei conti economici, se, successivamente, si esegue di nuovo il processo batch Chiudi conto economico.

## <a name="see-also"></a>Vedere anche

[Lavorare con periodi contabili e anni fiscali](finance-accounting-periods-and-fiscal-years.md)    
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    


[!INCLUDE[footer-include](includes/footer-banner.md)]
