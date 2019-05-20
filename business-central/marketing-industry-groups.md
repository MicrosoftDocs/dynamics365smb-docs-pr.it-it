---
title: Impostazione di settori industriali per le società contatto| Documenti Microsoft
description: Descrive come definire un settore industriale e assegnarlo a una società contatto, ad esempio il settore del commercio al dettaglio o dell'industria automobilistica.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 04/01/2019
ms.author: jswymer
redirect_url: marketing-setup-contacts
ms.openlocfilehash: 6f4fd9ef35c9a5287b01740861ad0b835c319ff4
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/29/2019
ms.locfileid: "1239185"
---
# <a name="set-up-industry-groups-for-contact-companies"></a>Impostare settori industriali per le società contatto
I gruppi industriali vengono utilizzati per indicare il tipo di settore industriale a cui appartengono i contatti, ad esempio il settore del commercio al dettaglio o l'industria automobilistica.

L'utilizzo dei settori industriali nei contatti è un processo a due passaggi. Innanzitutto, occorre definire il codice dei settori industriali. Questo passaggio deve essere eseguito una sola volta per ogni settore industriale. Dopo aver creato un codice di settore industriale, è possibile iniziare ad assegnarlo alle società.

> [!NOTE]  
>   Per sincronizzare i contatti con fornitori, clienti o conti correnti bancari in altre sezioni dell'applicazione, è consigliabile impostare una relazione d'affari.

## <a name="to-define-an-industry-group-code"></a>Per definire un codice di settore industriale
Il codice settore industriale definisce il tipo o la categoria del gruppo, ad esempio ANNUNCIO per la pubblicità o STAMPA per la TV e la radio. È possibile impostare più codici di settori industriali. Per definire i gruppi mailing, utilizzare la pagina **Settori industriali**.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Settori industriali** e quindi scegliere il collegamento correlato.
2. Selezionare l'azione **Nuovo** e immettere un codice e una descrizione. Il codice può avere un massimo di 11 caratteri e può essere qualsiasi combinazione di numeri o lettere.

## <a name="AssignIndustryGroupContact"></a> Per assegnare settori industriali a un contatto
Non è possibile assegnare i settori industriali a un contatto, ma solo alle società.

1. Aprire il contatto.
2. Scegliere l'azione **Società**, quindi l'azione **Settori industriali**. Verrà visualizzata la pagina **Settori industriali contatto**.
3. Nel campo **Codice settore industriale** selezionare il settore industriale da assegnare.

Ripetere tali passaggi per assegnare altri settori industriali. È inoltre possibile assegnare settori industriali nella finestra Lista Contatti seguendo la stessa procedura.

Il numero di settori industriali assegnati al contatto è visibile nel campo **Nr. settori industriali** della sezione **Segmentazione** della pagina **Contatto**.

Una volta assegnati i settori industriali ai contatti, è possibile utilizzare queste informazioni per selezionare i contatti per i segmenti. Per ulteriori informazioni, vedere [Aggiungere contatti ai segmenti](marketing-add-contact-segment.md).

## <a name="see-also"></a>Vedi anche
[Creazione di contatti](marketing-create-contact-companies.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
