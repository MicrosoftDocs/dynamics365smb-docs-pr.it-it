---
title: Impostare i fogli presenze e la relativa approvazione| Documenti Microsoft
description: Si possono impostare i fogli presenze per tenere traccia del tempo utilizzato per le commesse e l'utilizzo delle risorse, per semplificare la gestione dei progetti, i processi relativi al personale e la gestione della capacità.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff, resource
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: d2efe0d6d630f3548a41e164f0d71cb98fe09240
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2019
ms.locfileid: "915169"
---
# <a name="set-up-time-sheets"></a>Impostare fogli presenze
I fogli presenze di [!INCLUDE[d365fin](includes/d365fin_md.md)] consentono di gestire la registrazione del tempo in incrementi settimanali di sette giorni. Questi fogli possono essere usati per tenere traccia del tempo utilizzato nelle commesse e per registrare la semplice registrazione del tempo risorsa. Prima di poter utilizzare i fogli presenze, è necessario specificare come si desidera impostarli e configurarli.

Dopo aver impostato la modalità con cui l'organizzazione utilizzerà i fogli presenze, è possibile specificare se e come approvarli. In base alle esigenze dell'organizzazione, è possibile indicare:

* Uno o più utenti come amministratore dei fogli presenze e come responsabile approvazione di tutti i fogli presenze.
* Un responsabile approvazione del foglio presenze di ogni risorsa.

Una volta impostati dei fogli presenze, è possibile creare fogli presenze per le risorse, assegnarli alle righe di pianificazione commessa e registrare le righe dei fogli presenze. Per ulteriori informazioni, vedere [Utilizzare i fogli presenze](projects-how-use-time-sheets.md).

## <a name="to-set-up-general-information-for-time-sheets"></a>Per impostare le informazioni generali relative ai fogli presenze
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup risorse** e quindi scegliere il collegamento correlato.  
2. Compilare i campi, se necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Per il campo **Foglio presenze per approvazione commesse** selezionare una delle opzioni indicate di seguito.

| Opzione | Descrizione |
| --- | --- |
| **Mai** |Il foglio presenze viene approvato dall'utente indicato nel campo **ID utente resp. approvazione foglio presenze** nella scheda risorsa. |
| **Sempre** |Il foglio presenze viene approvato dall'utente indicato nel campo **Persona responsabile** nella scheda commessa. |
| **Solo macchina** |Se il foglio presenze della macchina è collegato a una commessa, il foglio presenze viene approvato dall'utente indicato nel campo **Persona responsabile** della scheda commessa. Se il foglio presenze della macchina è collegato a una risorsa, il foglio presenze viene approvato dall'utente indicato nel campo **ID utente resp. approvazione foglio presenze** della scheda risorsa. |

## <a name="to-assign-a-time-sheet-administrator"></a>Per assegnare un amministratore per il foglio presenze
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup utente** e quindi scegliere il collegamento correlato.  
2. Aggiungere un nuovo utente se la lista degli utenti non include la persona che si desidera nominare come amministratore del foglio presenze. Per ulteriori informazioni, vedere [Gestione di utenti e autorizzazioni](ui-how-users-permissions.md).
3. Selezionare un utente come amministratore del foglio presenze, quindi selezionare la casella di controllo **Amministratore foglio presenze**.  

> [!TIP]  
>   Si consiglia di designare un solo utente come amministratore del foglio presenze di un'azienda. Nella procedura riportata di seguito, si impostano un proprietario e un responsabile approvazione del foglio presenze dove il responsabile approvazione è assegnato a ciascuna risorsa.  

## <a name="to-assign-a-time-sheets-owner-and-approver"></a>Per assegnare un proprietario e un responsabile approvazione dei fogli presenze
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Risorse** e quindi scegliere il collegamento correlato.
2. Selezionare la risorsa per cui si desidera impostare la possibilità di utilizzare i fogli presenze, quindi selezionare la casella di controllo **Usa foglio presenze**.  
3. Nel campo **ID utente proprietario foglio presenze** immettere l'ID del proprietario del foglio presenze. Il proprietario può immettere l'utilizzo del tempo in un foglio presenze e inviarlo per l'approvazione. In generale quando la risorsa è una persona, è anche il proprietario.  
4. Nel campo **ID utente resp. approvazione foglio presenze** immettere l'ID del responsabile approvazione del foglio presenze. Il responsabile approvazione può approvare, rifiutare o riaprire un foglio presenze.  

> [!NOTE]  
>   Non è possibile modificare l'ID del responsabile approvazione del foglio presenze in caso di fogli presenze non ancora elaborati e con lo stato **Inviato** o **Aperto**.

## <a name="see-also"></a>Vedi anche
[Impostazione della Gestione progetti](projects-setup-projects.md)  
[Gestione progetti](projects-manage-projects.md)  
[Finanze](finance.md)  
[Acquisti](purchasing-manage-purchasing.md)         
[Vendite](sales-manage-sales.md)      
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
