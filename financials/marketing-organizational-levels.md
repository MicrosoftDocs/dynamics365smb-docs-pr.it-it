---
title: Impostare i livelli organizzativi per i contatti| Documenti Microsoft
description: "È possibile definire un livello organizzativo e assegnarlo al contatto per indicare la posizione all'interno della rispettiva società, ad esempio alta dirigenza."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, client, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: d101076c8a51b1c7a79606d207f79a826c89bf29
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-organizational-levels-for-contact-persons"></a>Procedura: Configurare i livelli organizzativi per i contatti
È possibile usare i livelli organizzativi con i contatti per specificarne la posizione all'interno della società, ad esempio alta dirigenza. È possibile utilizzare queste informazioni quando si inseriscono informazioni sui contatti.

L'utilizzo dei livelli organizzativi nei contatti è un processo a due passaggi. Innanzitutto, occorre definire il codice livello organizzativo. Questo passaggio deve essere eseguito una sola volta per ogni livello organizzativo. Dopo aver creato un codice livello organizzativo, è possibile iniziare ad assegnarlo ai contatti.

## <a name="to-define-an-organizational-level-code"></a>Per definire un codice livello organizzativo
Il codice livello organizzativo definisce il tipo o la categoria di livello organizzativo, ad esempio CEO o CFO. È possibile impostare più codici di livello organizzativo. Per definire il livello organizzativo, utilizzare la finestra **Livelli organizzativi**.

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Livelli organizzativi**, quindi scegliere il collegamento correlato.
2. Selezionare l'azione **Nuovo** e immettere un codice e una descrizione. Il codice può avere un massimo di 11 caratteri e può essere qualsiasi combinazione di numeri o lettere.

## <a name="to-assign-organizational-levels-to-a-contact-person"></a>Per assegnare livelli organizzativi a un contatto
È possibile assegnare un livello organizzativo ai contatti costituiti da persone, non alle società contatto. È possibile assegnare un livello organizzativo a ciascun contatto.

1. Aprire il contatto.
2. Nel campo **Livelli organizzativi** scegliere il codice che si desidera assegnare.

Una volta assegnati livelli organizzativi ai contatti, è possibile utilizzare queste informazioni per la creazione di segmenti.

Dopo avere assegnato i ruoli professionali ai contatti, è possibile utilizzare queste informazioni per selezionare i contatti per i segmenti. Per ulteriori informazioni, vedere [Procedura: aggiungere contatti ai segmenti](marketing-add-contact-segment.md).

## <a name="see-also"></a>Vedi anche
[Creazione di società contatto](marketing-create-contact-companies.md)  
[Creazione di contatti](marketing-create-contact-persons.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

