---
title: Definire codici di relazioni d'affari per i contatti| Documenti Microsoft
description: Utilizzare le relazioni d'affari in Business Central per supportare il marketing e per indicare il tipo di relazione commerciale che intercorre con prospetti e clienti, ad esempio, una banca o un fornitore di servizi.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, prospect, contact, client, customer
ms.date: 10/01/2018
ms.author: jswymer
redirect_url: marketing-setup-marketing
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 33743655f682aae9e02393aa68d04dffd334357b
ms.contentlocale: it-it
ms.lasthandoff: 11/26/2018

---
# <a name="setting-up-business-relations-on-contact-companies"></a>Impostazione delle relazioni d'affari nelle società contatto
È possibile utilizzare le relazioni d'affari vengono utilizzate per indicare il tipo di relazione commerciale che intercorre con i contatti, ad esempio potenziale cliente, banca, consulente e fornitore di servizi e così via.

L'utilizzo delle relazioni d'affari nei contatti è un processo a due passaggi. Innanzitutto, occorre definire il codice relazioni d'affari. Questo passaggio deve essere eseguito una sola volta per ogni relazione d'affari. Dopo aver creato un codice di relazione d'affari, è possibile iniziare ad assegnarlo alle società.

> [!NOTE]  
>   Per sincronizzare i contatti con fornitori, clienti o conti correnti bancari in altre sezioni dell'applicazione, è consigliabile impostare una relazione d'affari.

## <a name="to-define-a-business-relation-code"></a>Per definire un codice relazioni d'affari
Il codice relazione d'affari definisce una categoria o un tipo della relazione d'affari, ad esempio BANCA o Legge. È possibile impostare più codici di relazione d'affari. Per definire la relazione d'affari, utilizzare la pagina **Relazioni d'affari**.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Relazioni d'affari** e quindi scegliere il collegamento correlato.
2. Selezionare l'azione **Nuovo** e immettere un codice e una descrizione. Il codice può avere un massimo di 11 caratteri e può essere qualsiasi combinazione di numeri o lettere.

## <a name="AssignBusRelContact"></a> Per assegnare relazioni d'affari a un contatto
Non è possibile assegnare relazioni d'affari a un contatto, ma solo alle società.

1. Aprire il contatto.
2. Scegliere l'azione **Società**, quindi l'azione **Relazioni d'affari**.

    Verrà aperta la pagina **Relazioni d'affari contatto**.
3. Nel campo **Codice relazione d'affari** selezionare la relazione d'affari da assegnare.

Ripetere questi passaggi per assegnare altre relazioni d'affari. È inoltre possibile assegnare altre relazioni d'affari dalla lista Contatti seguendo la stessa procedura.

Il numero di relazioni d'affari assegnate al contatto viene visualizzato nel campo **Nr. relazione d'affari** nella sezione **Segmentazione** nella pagina **Contatto**.

Una volta assegnate le relazioni d'affari ai contatti, è possibile utilizzare queste informazioni per selezionare i contatti per i segmenti. Per ulteriori informazioni, vedere [Aggiungere contatti ai segmenti](marketing-add-contact-segment.md).

## <a name="see-also"></a>Vedi anche
[Creazione di società contatto](marketing-create-contact-companies.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

