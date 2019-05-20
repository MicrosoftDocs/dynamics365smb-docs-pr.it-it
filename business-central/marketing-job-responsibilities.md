---
title: Impostazioni di ruoli professionali per i contatti| Documenti Microsoft
description: È possibile definire un codice ruolo professionale e assegnarlo a un contatto per indicare i task per cui il contatto è responsabile nella propria società, ad esempio IT o produzione.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, to-do, relationship, prospect
ms.date: 04/01/2019
ms.author: jswymer
redirect_url: marketing-setup-contacts
ms.openlocfilehash: d9c6b19d49ea9423762b0b4b5cf61eae0e325034
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/29/2019
ms.locfileid: "1242217"
---
# <a name="set-up-job-responsibilities-for-contact-persons"></a>Impostare i ruoli professionali per i contatti
È possibile aggiungere informazioni sui ruoli professionali che indicano il ruolo svolto dal contatto all'interno della propria società, ad esempio IT, gestione o produzione. È possibile utilizzare queste informazioni quando si inseriscono informazioni sui contatti.

L'utilizzo dei ruoli professionali nei contatti è un processo a due passaggi. Innanzitutto, occorre definire il codice ruolo professionale. Questo passaggio deve essere eseguito una sola volta per ogni ruolo professionale. Dopo aver creato un codice ruolo professionale, è possibile iniziare ad assegnarlo ai contatti.

## <a name="to-define-a-job-responsibility-code"></a>Per definire un codice ruolo professionale
Il codice ruolo professionale definisce il tipo o la categoria di processo, ad esempio MARKETING o ACQUISTO. È possibile impostare più codici di ruoli professionali. Per definire il ruolo professionale, utilizzare la pagina **Ruoli professionali**.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ruoli professionali** e quindi scegliere il collegamento correlato.
2. Selezionare l'azione **Nuovo** e immettere un codice e una descrizione. Il codice può avere un massimo di 11 caratteri e può essere qualsiasi combinazione di numeri o lettere.

## <a name="to-assign-job-responsibilities-to-a-contact-person"></a>Per assegnare ruoli professionali a un contatto
Non è possibile assegnare ruoli professionali alle società contatto.

1. Aprire il contatto.
2. Scegliere l'azione **Persona**, quindi l'azione **Ruoli professionali**. Verrà visualizzata la pagina **Ruolo professionale contatto**.
3. Nel campo **Cod. ruolo professionale** selezionare il ruolo professionale da assegnare.

Ripetere tali passaggi per assegnare altri ruoli professionali. È inoltre possibile assegnare ruoli professionali dalla lista Contatti seguendo la stessa procedura.

Il numero di ruoli professionali assegnati al contatto viene visualizzato nella pagina **Contatto**, sezione **Segmentazione**, in corrispondenza del campo **Nr. ruoli professionali**.

Dopo avere assegnato i ruoli professionali ai contatti, è possibile utilizzare queste informazioni per selezionare i contatti per i segmenti. Per ulteriori informazioni, vedere [Aggiungere contatti ai segmenti](marketing-add-contact-segment.md).

## <a name="see-also"></a>Vedi anche
[Creazione di contatti](marketing-create-contact-companies.md)  
[Utilizzo di Business Central](ui-work-product.md)