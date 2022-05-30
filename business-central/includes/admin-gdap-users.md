---
author: edupont04
ms.topic: include
ms.date: 05/09/2022
ms.author: edupont
ms.openlocfilehash: f002086780e694ad80f2b5c80e942ab411de1948
ms.sourcegitcommit: 2fa712d0aabe4287ebd4454c28d142d6baf045a0
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/09/2022
ms.locfileid: "8732965"
---
Potresti vedere altri utenti nell'elenco **Utenti** a parte quelli della propria azienda. Quando un amministratore con delega di una società partner di rivendita accede a un ambiente [!INCLUDE [prod_short](prod_short.md)] per conto del proprio cliente, vengono automaticamente creati come utenti all'interno di [!INCLUDE [prod_short](prod_short.md)]. In questo modo, le azioni eseguite da un amministratore con delega vengono registrate in [!INCLUDE [prod_short](prod_short.md)], come la pubblicazione di documenti e associati al loro ID utente.  

Con i *privilegi di amministratore delegato granulare (GDAP)*, l'utente viene visualizzato nell'elenco **Utenti** e può ricevere qualsiasi autorizzazione. Non vengono mostrati con il nome e altre informazioni personali ma con il nome della società e un ID univoco. Sia gli amministratori interni che quelli esterni possono vedere questi utenti nell'elenco **Utenti** e hanno piena trasparenza su ciò che questi utenti fanno attraverso il [registro delle modifiche](../across-log-changes.md), ad esempio. Ma non possono vedere il nome reale di questi utenti. Gli utenti GDAP sono elencati con i nomi utente nel seguente formato: `User123456@partnerdomain.com`. Potrebbero avere un nome utente che riflette il nome dell'azienda del partner e l'indirizzo e-mail non è l'indirizzo e-mail effettivo della persona. In questo modo, gli account utente GDAP non rivelano informazioni personali. Se hai bisogno di scoprire chi è la persona dietro un tale pseudonimo, dovrai contattare l'azienda per cui questo utente lavora o ha lavorato.  
