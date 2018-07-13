---
title: Impostazione di gruppi mailing per i contatti| Documenti Microsoft
description: "È possibile usare i gruppi di mailing per identificare gruppi di contatti a cui inviare le stesse informazioni, ad esempio per una campagna marketing o promozionale."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, campaign, promo, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: e3917573a912a4e51416c4e926443c87513728fe
ms.openlocfilehash: b4ed119845ef460ac3235a2e56a18f99e5cc4ee3
ms.contentlocale: it-it
ms.lasthandoff: 06/01/2018

---
# <a name="set-up-mailing-groups-for-contacts"></a>Impostare i gruppi mailing per i contatti
È possibile utilizzare i gruppi mailing per identificare gruppi di contatti a cui inviare le stesse informazioni. È possibile, ad esempio, impostare un gruppo mailing relativo ai contatti a cui si desidera inviare una notifica di un cambio di ufficio o un altro gruppo per inviare gli auguri delle festività.

L'utilizzo dei gruppi mailing nei contatti è un processo a due passaggi. Innanzitutto, occorre definire il codice dei gruppi mailing. Questo passaggio deve essere eseguito una sola volta per ogni gruppo mailing. Dopo aver creato un codice di gruppo di mailing, è possibile iniziare ad assegnarlo alle società.

## <a name="to-define-mailing-group-codes"></a>Per definire i codici di gruppo di mailing
Il codice gruppo mailing definisce il tipo o la categoria del gruppo, ad esempio SPOSTAMENTO per lo spostamento dell'ufficio o AUGURI per gli auguri festivi. È possibile impostare più codici di settori industriali. Per definire i gruppi mailing, utilizzare la finestra **Gruppi mailing**.

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Gruppi mailing**, quindi scegliere il collegamento correlato.
2. Selezionare l'azione **Nuovo** e immettere un codice e una descrizione. Il codice può avere un massimo di 11 caratteri e può essere qualsiasi combinazione di numeri o lettere.

## <a name="AssignMailGroupContact"></a> Per assegnare gruppi di mailing a un contatto
1. Aprire il contatto.
2. Selezionare l'azione **Gruppi mailing**. Verrà visualizzata la finestra **Gruppi mailing contatto**.
3. Nel campo **Codice gruppi mailing** selezionare il gruppo mailing da assegnare.

Ripetere tali passaggi per assegnare altri gruppi mailing. È inoltre possibile assegnare altri gruppi di mailing dalla lista contatti seguendo la stessa procedura.

Il numero di gruppi di mailing assegnati al contatto viene visualizzato nel campo **Nr. di gruppi mailing** nella sezione **Segmentazione** della finestra **Contatto**.

Dopo avere assegnato i gruppi di mailing ai contatti, è possibile utilizzare queste informazioni per selezionare i contatti per i segmenti. Per ulteriori informazioni, vedere [Aggiungere contatti ai segmenti](marketing-add-contact-segment.md).

## <a name="see-also"></a>Vedi anche
[Creazione di società contatto](marketing-create-contact-companies.md)  
[Creazione di contatti](marketing-create-contact-persons.md)  
[Utilizzo di Business Central](ui-work-product.md)

