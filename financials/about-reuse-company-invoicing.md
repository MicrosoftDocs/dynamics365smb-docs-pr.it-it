---
title: Utilizzare Invoicing e Finance and Operations, Business edition | Documenti Microsoft
description: Soluzione alternativa per l'accesso a Microsoft Invoicing dopo aver effettuato l'iscrizione a Dynamics 365 for Finance and Operations, Business edition.
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/22/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: 803569ed99f00b9055c5a6ec6e4ffae67d9df2bd
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="using-the-same-office-365-account-in-included365finincludesd365finlongmdmd-and-microsoft-invoicing"></a>Utilizzo dello stesso account di Office 365 in [!INCLUDE[d365fin](includes/d365fin_long_md.md)] e Microsoft Invoicing
Quando si effettua l'iscrizione per una versione di prova con [!INCLUDE[d365fin](includes/d365fin_md.md)], è possibile passare a una fase di valutazione di 30 giorni, effettuare una sottoscrizione oppure interrompere l'utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]. In tutti i casi, se si accede al portale di Office, è possibile che venga visualizzata una sezione denominata **Business Center** selezionabile con un clic. Questo elemento fa parte della sottoscrizione a Office 365 Business Premium, quindi non tutti gli utenti visualizzeranno tale sezione nel portale di Office.  

Se si accede al Business Center, verrà visualizzata una sezione denominata **Fatturazione**. Se si accede a tale sezione, verrà visualizzato un messaggio nel quale viene comunicato che non è possibile accedere a Microsoft Invoicing perché l'account è utilizzato in [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Un messaggio simile viene visualizzato se si installa l'app mobile per Invoicing.  

## <a name="workaround"></a>Soluzione alternativa
Invoicing e [!INCLUDE[d365fin](includes/d365fin_md.md)] dispongono di una piattaforma condivisa. Di conseguenza, quando l'utente fa clic su Invoicing nel Business Center, viene riconosciuto come un utente esistente di [!INCLUDE[d365fin](includes/d365fin_md.md)]. Ciò si verifica perché Invoicing non può utilizzare la stessa società in uso in [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Sarà necessario accedere a [!INCLUDE[d365fin](includes/d365fin_md.md)], rinominare la società esistente, quindi creare una nuova società che potrà essere utilizzata in Invoicing. Nessun dato viene spostato né sovrascritto durante questa soluzione alternativa.

### <a name="to-rename-your-company"></a>Per rinominare la società
1.  Accedere a [!INCLUDE[d365fin](includes/d365fin_md.md)].  
2.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Società**, quindi scegliere il collegamento correlato.  
3.  Nella finestra **Società**, scegliere il pulsante **Modifica lista**.  
4.  Modificare il nome dell'elemento *La mia società* inserendo una denominazione diversa.  

    Attendere alcuni minuti. Apporteremo alcune modifiche nel database sottostante e tale operazione richiede del tempo.
5.  Quando il sistema è nuovamente pronto all'uso, scegliere il pulsante **Crea nuova società**.  
6.  Nella finestra di dialogo visualizzata, specificare il nome come *La mia società*, quindi scegliere l'opzione **Produzione - Solo dati setup**.  

Anche tale operazione richiede alcuni minuti. Al completamento del processo, sarà possibile accedere a Invoicing come parte dell'esperienza Office 365 Business Premium.  

### <a name="what-about-my-data"></a>Quali modifiche vengono apportate ai miei dati?
Quando si rinomina l'elemento originale in La mia società, le tabelle del database in cui sono memorizzati i dati [!INCLUDE[d365fin](includes/d365fin_md.md)] esistenti vengono rinominate, ma i dati stessi non subiscono alcuna modifica.  

Se si utilizza sia Invoicing che [!INCLUDE[d365fin](includes/d365fin_md.md)], i dati vengono memorizzati in due contenitori diversi (le due società). Nessun elemento viene condiviso, quindi sarà necessario gestire i clienti e gli articoli in entrambe le società.  

## <a name="see-also"></a>Vedi anche
[Domande frequenti](across-faq.md)  
[Setup e amministrazione](admin-setup-and-administration.md)  

