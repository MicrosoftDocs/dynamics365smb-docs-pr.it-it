---
title: Gestire le assenze di un dipendente | Microsoft Docs
description: Descrive come registrare le assenze dei dipendenti e analizzare le statistiche sulle assenze.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 89f164207b78a9b1845ed7add0b6dea7c4b6efbc
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5782140"
---
# <a name="manage-employee-absence"></a>Gestire le assenze di un impiegato
Per gestire le assenze di un impiegato, è necessario registrare l'assenza nella pagina **Registrazione assenza**. Le informazioni possono quindi essere visualizzate in diversi modi per esigenze di analisi e creazione report.

Le assenze degli impiegati possono essere visualizzate in due pagine diverse:

* Nella pagina **Registrazioni assenze**, che consente di registrare tutte le assenze degli impiegati, un'assenza per riga.
* Nella pagina **Assenze Impiegato** dove vengono visualizzate le assenze di un solo impiegato. Si tratta delle informazioni immesse nella pagina **Registrazioni assenze**, ma filtrate in base a un determinato impiegato.

Per ottenere statistiche significative, per le registrazioni delle assenze degli impiegati è consigliabile utilizzare sempre la stessa unità di misura, giorno oppure ora.

## <a name="to-register-employee-absence"></a>Per registrare le assenze di un impiegato
È possibile registrare le assenze degli impiegati su base giornaliera o in base a un altro intervallo rispondente alle proprie esigenze organizzative.

1. Nell'angolo superiore destro, scegliere l'icona **Cerca pagina o report**, immettere **Registrazione assenza**, quindi scegliere il collegamento correlato.
2. Scegliere l'azione **Nuovo**.
3. Ripetere la procedura per ciascun assenza impiegato che si desidera registrare.
4. Chiudere la pagina.

    > [!Tip]
    > Per ottenere statistiche significative utilizzare sempre la stessa unità di misura, cioè giorno oppure ora, per le registrazioni delle assenze.

## <a name="to-view-an-individual-employees-absence"></a>Per visualizzare l'assenza di un singolo impiegato
1. Nell'angolo superiore destro, scegliere l'icona **Cerca pagina o report**, immettere **Impiegati**, quindi scegliere il collegamento correlato.
2. Selezionare l'impiegato di interesse e quindi scegliere l'azione **Assenza**.

    Si apre la pagina **Assenze impiegato** e vengono visualizzate le assenze e le date in cui hanno avuto inizio e termine.

## <a name="to-view-an-employees-absence-by-categories"></a>Per visualizzare le assenze di un impiegato per categorie
1. Nell'angolo superiore destro, scegliere l'icona **Cerca pagina o report**, immettere **Impiegati**, quindi scegliere il collegamento correlato.
2. Selezionare l'impiegato di interesse e quindi scegliere l'azione **Assenze per categoria**.
3. Nella pagina **Assenze impieg. per categorie**, compilare i campi filtro come necessario e quindi scegliere l'azione **Mostra matrice**.

    La pagina **Assenze imp. per matrice cat.** si apre e mostra tutte le assenze, suddivise per cause di assenza.

## <a name="to-view-all-employee-absences-by-category"></a>Per visualizzare tutte le assenze degli impiegati per categoria
1. Nell'angolo superiore destro, scegliere l'icona **Cerca pagina o report**, immettere **Registrazione assenza**, quindi scegliere il collegamento correlato.
2. Nella pagina **Registrazione assenza** scegliere l'azione **Per categorie**.
3. Nella pagina **Sintesi assenze per categorie** impostare un filtro in **Filtro nr. impiegato** per visualizzare le assenze di un singolo impiegato o di un gruppo definito di impiegati.
4. Scegliere l'azione **Mostra matrice**.

    La pagina **Matrice sintesi assenze per categorie** si apre e visualizza le assenze di tutti gli impiegati suddivise secondo le varie cause di assenza.

## <a name="to-view-all-employee-absences-by-period"></a>Per visualizzare tutte le assenze degli impiegati per periodo
1. Nell'angolo superiore destro, scegliere l'icona **Cerca pagina o report**, immettere **Registrazione assenza**, quindi scegliere il collegamento correlato.
   Nella pagina **Registrazione assenza** scegliere l'azione **Per periodi**.
2. Nella pagina **Sintesi assenze per periodo** impostare un filtro nel campo **Filtro cause di assenza** per visualizzare le assenze degli impiegati per cause specifiche.
3. Scegliere l'azione **Mostra matrice**.

    La pagina **Matrice sintesi assenze per periodo** si apre e visualizza le assenze suddivise per periodo.

## <a name="see-also"></a>Vedere anche
[Gestione personale](hr-manage-human-resources.md)  
[Finanze](finance.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Modifica delle funzionalità visualizzate](ui-experiences.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]