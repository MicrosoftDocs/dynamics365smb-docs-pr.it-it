---
title: "Impostazione di settori industriali nelle società contatto | Documenti Microsoft"
description: Viene descritto l&quot;utilizzo dei settori industriali con contatti in Financials
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 03/28/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 34b81ec1e92eea67af13c7a2dfe03bdb97c8c59c
ms.contentlocale: it-it
ms.lasthandoff: 05/04/2017


---
# <a name="setting-up-industry-groups-for-contact-companies"></a>Impostazione di settori industriali per le società contatto
I gruppi industriali vengono utilizzati per indicare il tipo di settore industriale a cui appartengono i contatti, ad esempio il settore del commercio al dettaglio o l'industria automobilistica.

L'utilizzo dei settori industriali nei contatti è un processo a due passaggi. Innanzitutto, occorre definire il codice dei settori industriali. Questo passaggio deve essere eseguito una sola volta per ogni settore industriale. Dopo aver creato un codice di settore industriale, è possibile iniziare ad assegnarlo alle società.

**Nota**: se si prevede di sincronizzare i contatti con fornitori, clienti o conti correnti bancari in altre sezioni dell'applicazione, è consigliabile impostare una relazione d'affari.

## <a name="to-define-an-industry-group-code"></a>Per definire un codice di settore industriale
Il codice settore industriale definisce il tipo o la categoria del gruppo, ad esempio ANNUNCIO per la pubblicità o STAMPA per la TV e la radio. È possibile impostare più codici di settori industriali. Per definire i settori industriali, utilizzare la finestra **Settori industriali**.

1. Nell'angolo superiore destro scegliere l'icona **Cerca pagina o report** ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), inserire **Settori industriali**, quindi scegliere il collegamento correlato.
2. Selezionare l'azione **Nuovo** e immettere un codice e una descrizione. Il codice può avere un massimo di 11 caratteri e può essere qualsiasi combinazione di numeri o lettere.

## <a name="AssignIndustryGroupContact"></a> Per assegnare settori industriali a un contatto
Non è possibile assegnare i settori industriali a un contatto, ma solo alle società.

1. Aprire il contatto.
2. Scegliere l'azione **Società**, quindi l'azione **Settori industriali**. Verrà visualizzata la finestra **Settori industriali contatto**.
3. Nel campo **Codice settore industriale** selezionare il settore industriale da assegnare.

Ripetere tali passaggi per assegnare altri settori industriali. È inoltre possibile assegnare settori industriali nella finestra Lista Contatti seguendo la stessa procedura.

Il numero di settori industriali assegnati al contatto è visibile nel campo **Nr. settori industriali** della sezione **Segmentazione** della finestra **Contatto**.

Una volta assegnati i settori industriali ai contatti, è possibile utilizzare queste informazioni per selezionare i contatti per i segmenti. Per ulteriori informazioni, vedere [Procedura: aggiungere contatti ai segmenti](marketing-add-contact-segment.md).

## <a name="see-also"></a>Vedi anche
[Creazione di società contatto](marketing-create-contact-companies.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

