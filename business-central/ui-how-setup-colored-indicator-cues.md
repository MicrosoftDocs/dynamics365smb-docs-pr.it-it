---
title: Personalizzare segnali visivi sull'attività di una pila | Documenti Microsoft
description: Impostare un indicatore colorato sulla sezione Pila per fornire un segnale visivo per personalizzato per l'attività di una pila.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: personalize, customize
ms.date: 04/01/2019
ms.author: solsen
redirect_url: admin-how-set-up-colored-indicator-on-cues
ms.openlocfilehash: f79f1a65ee17d8ca46a8ecf1cd9d49c5246bef63
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2019
ms.locfileid: "923440"
---
# <a name="set-up-a-colored-indicator-on-cues"></a>Impostare un indicatore colorato nelle pile
È possibile impostare le pile che vengono visualizzate in Gestione ruolo utente degli utenti in modo che includano un indicatore che cambia colore in base ai valori dei dati presenti nelle pile.

L'indicatore viene visualizzato come una barra colorata lungo il bordo superiore della pila. Fornisce un segnale visivo dello stato dell'attività della pila, che può indicare le condizioni favorevoli o sfavorevoli per spingere l'utente a intraprendere un'azione. Ad esempio, se una pila visualizza le fatture di vendita in corso, è possibile impostare l'indicatore in modo che appaia verde (favorevole) quando il totale delle fatture di vendita in corso è minore di 10 e rosso (sfavorevole) quando il totale è maggiore di 20.

Nella pagina **Setup pila**, si impostano gli indicatori di tutte le pile disponibili nel database della società.

Per impostare l'indicatore, specificare fino a due valori di soglia che definiscono tre intervalli dei valori dei dati (basso, medio e alto) e a cui è possibile applicare un colore diverso (o stile).

## <a name="to-set-up-colored-indicators-on-cues"></a>Per impostare indicatori colorati nelle pile
1. In **Attività**, nella pagina Gestione ruolo utente, scegliere **Imposta pile**.  
   Verrà visualizzata la pagina **Setup pila**. Nella pagina sono elencati gli indicatori attualmente impostati nelle pile.
2. Per modificare un indicatore, modificare i campi e modificare, ad esempio, i valori per le diverse soglie.  

Nella tabella seguente sono elencati i colori corrispondenti alle opzioni dei campi **Stile intervallo inferiore**, **Stile intervallo medio** e **Stile intervallo superiore**.

| Opzione | Colore |
| --- | --- |
| **Nessuno** |Nessun colore (lo stesso colore della sezione Pila)|
| **Favorevole** |Verde |
| **Sfavorevole** |Rosso |
| **Ambiguo** |Giallo |
| **Subordinato** |Grigio |

## <a name="see-also"></a>Vedi anche
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
