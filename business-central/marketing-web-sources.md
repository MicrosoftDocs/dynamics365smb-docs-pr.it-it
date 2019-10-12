---
title: Impostare le origini Web per le società contatto| Documenti Microsoft
description: È possibile definire origini Web o Internet e assegnarle a una società contatto per consentire l'identificazione delle modalità di ricerca delle informazioni sui contatti.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: internet
ms.date: 10/01/2019
ms.author: jswymer
redirect_url: marketing-setup-contacts
ms.openlocfilehash: 8e9defda4f5ff25d5ac90a308549880e454bc637
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2019
ms.locfileid: "2308673"
---
# <a name="set-up-web-sources-for-contact-companies"></a>Impostare le origini Web per le società contatto
È possibile utilizzare le origini Web con le società contatto per identificare, ad esempio, motori di ricerca e siti Web dove effettuare la ricerca di informazioni sui contatti. Quando si assegna un'origine Web, specificare il motore di ricerca e la parola di ricerca che saranno utilizzati per individuare le informazioni richieste.

L'utilizzo delle origini Web nei contatti è un processo a due passaggi. Innanzitutto, occorre definire il codice origine Web. Questo passaggio deve essere eseguito una sola volta per ogni origine Web. Dopo aver creato un codice origine Web, è possibile iniziare ad assegnarlo ai contatti.

## <a name="to-define-a-web-source-code"></a>Per definire un codice origine Web
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Origini Web** e quindi scegliere il collegamento correlato.
2. Scegliere l'azione **Nuovo**.
3. Compilare i campi **Codice**, **Descrizione** e **URL**.

    Nel campo **URL** immettere %1 per inserire un segnaposto per una parola di ricerca nell'URL. Quando si apre l'origine Web da un contatto, %1 verrà automaticamente sostituito con la parola da ricercare (ad esempio il nome della società) inserita nella pagina **Origini Web contatto**.

Ripetere tali passaggi per impostare altre origini Web.

## <a name="to-assign-web-sources-to-a-contact-company"></a>Per assegnare origini Web a una società contatto
Quando si assegna un'origine Web, specificare il motore di ricerca e la parola di ricerca che saranno utilizzati per individuare le informazioni richieste.

1. Aprire il contatto.
2. Scegliere l'azione **Società**, quindi l'azione **Origini Web**. Verrà visualizzata la pagina **Origine Web contatto**.
3. Nel campo **Codice origine Web** scegliere l'origine Web che si desidera assegnare.
4. Nel campo **Parola ricerca** inserire la parola ricerca che verrà utilizzata per individuare le informazioni.

Ripetere tali passaggi per assegnare altre origini Web.

È inoltre possibile assegnare l'origine Web dalla pagina **Lista Contatti** seguendo la stessa procedura.

## <a name="see-also"></a>Vedi anche
[Creazione di contatti](marketing-create-contact-companies.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
