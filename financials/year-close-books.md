---
title: "Panoramica delle attività di chiusura dei registri | Documenti Microsoft"
description: Informazioni sul processo di chiusura dei registri contabili per un anno fiscale o un periodo e su cosa accade dopo la chiusura di un anno.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 03/29/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 870f1c6a7f93195e0308a646402d642f6cadd219
ms.contentlocale: it-it
ms.lasthandoff: 07/07/2017


---
# <a name="closing-the-books"></a>Chiusura dei registri
Dopo avere verificato che tutti i conti sono aggiornati e assegnato costi ed entrate, è possibile chiudere i registri per un anno fiscale o un periodo.

Non è obbligatorio chiudere un anno, ma se si esegue questa operazione è più semplice lavorare con il programma in quanto è possibile utilizzare le comode opzioni di filtro fornite. Non è inoltre necessario preoccuparsi di perdere i dettagli relativi alle transazioni, in quanto tali dettagli vengono conservati anche dopo la chiusura dell'anno.

## <a name="closing-book-process"></a>Processo di chiusura dei libri
Il processo di chiusura dei libri include le seguenti attività principali:

1. Chiusura del periodo contabile.

    Una anno fiscale viene definito come uno o più periodi indicati nella finestra **Periodi contabili**. Un tipico anno fiscale contiene 12 periodi di un mese, tuttavia è possibile scegliere un altro metodo per definire un anno.

    Per ulteriori informazioni, vedere [Procedura: Chiudere i periodi contabili](year-close-account-periods.md).
2. Registrazione dei movimenti dell'anno precedente.

    Quando si chiude un anno fiscale, è necessario immettere un numero di transazioni amministrative, ad esempio articoli prepagati e sospesi. Tali transazioni sono dette movimenti di rettifica. Non vi sono regole speciali per la registrazione di questi movimenti e, come altri movimenti, se vengono registrati in una data di un anno fiscale chiuso, contengono un segno di spunta nel campo **Mov. anno prec.** Anche se l'anno fiscale è stato chiuso, è possibile registrarvi dei movimenti C/G.
3. Trasferimento dei saldi dai conti economici al conto patrimoniale.

    Dopo la chiusura di un anno fiscale e la registrazione di tutti i movimenti dell'anno precedente, è necessario chiudere i conti economici e trasferire il fatturato netto dell'anno in un conto come capitale netto nello stato patrimoniale. A questo scopo utilizzare il processo batch Chiudi conto economico. Il processo batch elabora tutti i conti di contabilità generale di tipo Conto economico e crea movimenti che stornano i saldi. Tali movimenti vengono inseriti in una registrazione da cui possono essere contabilizzati. I movimenti non vengono contabilizzati automaticamente dal processo batch, eccetto quando viene utilizzata una valuta addizionale. In questo caso la contabilizzazione viene effettuata direttamente nella contabilità generale.

    Per ulteriori informazioni, vedere [Chiudere il conto economico](year-close-income-statement.md).
4. Registrazione del movimento di chiusura di fine anno insieme alla compensazione dei movimenti conti patrimonio netto.

    Una volta completato il processo batch di chiusura del conto economico, registrare i movimenti generati dal processo. Se non è stato specificato un conto profitti/perdite nel processo batch, immettere una riga con un movimento di contropartita che registra il fatturato netto nel conto di contabilità generale corretto nello stato patrimoniale. Contabilizzare infine le registrazioni.

    Per ulteriori informazioni, vedere [Procedura: registrare il movimento di chiusura di fine anno](year-how-post-year-end-close-entry.md).

## <a name="what-happens-when-you-close"></a>Cosa accade alla chiusura
Quando si effettua la chiusura alla fine dell'anno, gli utili calcolati vengono spostati in un conto profitti/perdite. L'anno fiscale viene inoltre contrassegnato come "chiuso," e tutti i movimenti successivi per l'anno chiuso vengono contrassegnati come "movimenti dell'anno precedente".

Viene quindi generato un movimento di chiusura, che non viene però registrato automaticamente. È possibile creare il movimento o i movimenti conti patrimonio netto di compensazione, per stabilire come assegnare il movimento di chiusura. Se, ad esempio, nella società sono presenti più divisioni, è possibile fare in modo che venga generato un singolo movimento di chiusura per tutte le divisioni, quindi creare un movimento di compensazione per il conto patrimonio netto di ogni divisione.

È possibile effettuare registrazioni in un anno fiscale precedente, anche dopo la chiusura dei conti economici, se, successivamente, si esegue di nuovo il processo batch Chiudi conto economico.

## <a name="see-also"></a>Vedi anche
[Procedura: aprire un nuovo anno fiscale](finance-how-open-new-fiscal-year.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

