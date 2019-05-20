---
title: Utilizzare Invoicing e Business Central | Microsoft Docs
description: Soluzione alternativa per l'accesso a Microsoft Invoicing dopo aver effettuato l'iscrizione a Dynamics 365 Business Central.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Invoicing, Office 365
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 0173d64e140cfea91bf7f08d821c2d30cf0eb7b3
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/29/2019
ms.locfileid: "1241486"
---
# <a name="using-the-same-office-365-account-in-included365finincludesd365finlongmdmd-and-microsoft-invoicing"></a>Utilizzo dello stesso account di Office 365 in [!INCLUDE[d365fin](includes/d365fin_long_md.md)] e Microsoft Invoicing
Quando si effettua l'iscrizione per una versione di valutazione con [!INCLUDE[d365fin](includes/d365fin_md.md)], è possibile passare a una fase di valutazione di 30 giorni, effettuare una sottoscrizione oppure interrompere l'utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]. In tutti i casi, se si accede al portale di Office, è possibile che venga visualizzata una sezione denominata **Microsoft Invoicing** selezionabile con un clic. Questo elemento fa parte della sottoscrizione a Office 365 Business Premium, quindi non tutti gli utenti visualizzeranno tale sezione nel portale di Office.  

Se si accede a Microsoft Invoicing, verrà visualizzato un messaggio nel quale viene comunicato che non è possibile accedere a Microsoft Invoicing perché l'account è utilizzato in [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Un messaggio simile viene visualizzato se si installa l'app mobile per Invoicing.  

## <a name="workaround"></a>Soluzione alternativa
Invoicing e [!INCLUDE[d365fin](includes/d365fin_md.md)] dispongono di una piattaforma condivisa. Di conseguenza, quando l'utente fa clic su Invoicing nel portale di Office, viene riconosciuto come un utente esistente di [!INCLUDE[d365fin](includes/d365fin_md.md)]. Ciò si verifica perché Invoicing non può utilizzare la stessa società in uso in [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Sarà necessario accedere a [!INCLUDE[d365fin](includes/d365fin_md.md)], rinominare la società esistente, quindi creare una nuova società che potrà essere utilizzata in Invoicing. Nessun dato viene spostato né sovrascritto durante questa soluzione alternativa.

### <a name="to-rename-your-company"></a>Per rinominare la società
1. Accedi a [!INCLUDE[d365fin](includes/d365fin_md.md)].
2. Nell'angolo superiore destro scegliere l'icona **Impostazioni** ![Impostazioni](media/ui-experience/settings_icon_small.png "icona Impostazioni per Gestione ruolo utente"), quindi scegliere **Impostazioni personali**.
3. Nel campo **Società**, scegliere un'altra società.
4. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Società** e quindi scegliere il collegamento correlato.  
5. Nella pagina **Società**, scegliere **Modifica lista**.  
6. Modificare il nome dell'elemento *La mia società* inserendo una denominazione diversa.  

    Attendere alcuni minuti. Apporteremo alcune modifiche nel database sottostante e tale operazione richiede del tempo.
7.  Quando il sistema è nuovamente pronto all'uso, scegliere il pulsante **Crea nuova società**.  
8.  Nella finestra di dialogo visualizzata, specificare il nome come *La mia società*, quindi scegliere l'opzione **Produzione - Solo dati setup**.  

Anche tale operazione richiede alcuni minuti. Al completamento del processo, sarà possibile accedere a Invoicing come parte dell'esperienza Office 365 Business Premium.  

### <a name="what-about-my-data"></a>Quali modifiche vengono apportate ai miei dati?
Quando si rinomina l'elemento originale in La mia società, le tabelle del database in cui sono memorizzati i dati [!INCLUDE[d365fin](includes/d365fin_md.md)] esistenti vengono rinominate, ma i dati stessi non subiscono alcuna modifica.  

Se si utilizza sia Invoicing che [!INCLUDE[d365fin](includes/d365fin_md.md)], i dati vengono memorizzati in due contenitori diversi (le due società). Nessun elemento viene condiviso, quindi sarà necessario gestire i clienti e gli articoli in entrambe le società.  

## <a name="see-also"></a>Vedi anche
[Domande frequenti](across-faq.md)  
[Amministrazione](admin-setup-and-administration.md)  
