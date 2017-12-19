---
title: Impostazioni di ruoli professionali per i contatti| Documenti Microsoft
description: "È possibile definire un codice ruolo professionale e assegnarlo a un contatto per indicare i task per cui il contatto è responsabile nella propria società, ad esempio IT o produzione."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, to-do, relationship, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: aa56764b5f3210229ad21eae6891fb201462209c
ms.openlocfilehash: f0a4000a3f12a23b1d732ab9671e7cb5938eb887
ms.contentlocale: it-it
ms.lasthandoff: 12/14/2017

---
# <a name="how-to-set-up-job-responsibilities-for-contact-persons"></a>Procedura: Impostare i ruoli professionali per i contatti
È possibile aggiungere informazioni sui ruoli professionali che indicano il ruolo svolto dal contatto all'interno della propria società, ad esempio IT, gestione o produzione. È possibile utilizzare queste informazioni quando si inseriscono informazioni sui contatti.

L'utilizzo dei ruoli professionali nei contatti è un processo a due passaggi. Innanzitutto, occorre definire il codice ruolo professionale. Questo passaggio deve essere eseguito una sola volta per ogni ruolo professionale. Dopo aver creato un codice ruolo professionale, è possibile iniziare ad assegnarlo ai contatti.

## <a name="to-define-a-job-responsibility-code"></a>Per definire un codice ruolo professionale
Il codice ruolo professionale definisce il tipo o la categoria di processo, ad esempio MARKETING o ACQUISTO. È possibile impostare più codici di ruoli professionali. Per definire il ruolo professionale, utilizzare la finestra **Ruoli professionali**.

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Ruoli professionali**, quindi scegliere il collegamento correlato.
2. Selezionare l'azione **Nuovo** e immettere un codice e una descrizione. Il codice può avere un massimo di 11 caratteri e può essere qualsiasi combinazione di numeri o lettere.

## <a name="to-assign-job-responsibilities-to-a-contact-person"></a>Per assegnare ruoli professionali a un contatto
Non è possibile assegnare ruoli professionali alle società contatto.

1. Aprire il contatto.
2. Scegliere l'azione **Persona**, quindi l'azione **Ruoli professionali**. Verrà visualizzata la finestra **Ruolo professionale contatto**.
3. Nel campo **Cod. ruolo professionale** selezionare il ruolo professionale da assegnare.

Ripetere tali passaggi per assegnare altri ruoli professionali. È inoltre possibile assegnare ruoli professionali dalla lista Contatti seguendo la stessa procedura.

Il numero di ruoli professionali assegnati al contatto viene visualizzato nella finestra **Contatto**, sezione **Segmentazione**, in corrispondenza del campo **Nr. ruoli professionali**.

Dopo avere assegnato i ruoli professionali ai contatti, è possibile utilizzare queste informazioni per selezionare i contatti per i segmenti. Per ulteriori informazioni, vedere [Procedura: aggiungere contatti ai segmenti](marketing-add-contact-segment.md).

## <a name="see-also"></a>Vedi anche
[Creazione di contatti](marketing-create-contact-persons.md)  
[Creazione di società contatto](marketing-create-contact-companies.md)  
[Utilizzo di Financials](ui-work-product.md)

