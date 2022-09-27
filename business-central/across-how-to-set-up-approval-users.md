---
title: Impostare gli utenti per l'approvazione
description: Prima di creare flussi di lavoro che coinvolgono passaggi di approvazione, è necessario impostare gli utenti del flusso di lavoro coinvolti nei processi di approvazione nella pagina Setup utente approvazione.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 663
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 464212d90ba43648bcb5d2852f5d3fec0c23ca41
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/19/2022
ms.locfileid: "9530785"
---
# <a name="set-up-approval-users"></a>Impostare gli utenti per l'approvazione

Prima di creare workflow che coinvolgono passaggi di approvazione, è necessario impostare gli utenti del workflow coinvolti nei processi di approvazione. Nella pagina **Setup utente approvazione** è possibile anche impostare i limiti quantitativi per specifici tipi di richiesta e definire i responsabili di approvazione sostitutivi ai quali vengono delegate le richieste di approvazione in assenza del responsabile originale.  

> [!NOTE]  
> Gli utenti dell'approvazione, sia i richiedenti sia i responsabili dell'approvazione, devono innanzitutto essere impostati come utenti del workflow nella pagina **Gruppo di utenti del workflow**. Per ulteriori informazioni, vedere [Impostare gli utenti del workflow](across-how-to-set-up-workflow-users.md).  

 Una volta impostati questi utenti, è possibile utilizzare l'impostazione per creare le risposte del flusso di lavoro per i flussi di lavoro di approvazione. Per ulteriori informazioni, vedere il passaggio 9 in [Creare workflow](across-how-to-create-workflows.md).  

> [!NOTE]  
> Per definire che una richiesta di approvazione non venga approvata fino a che non venga approvata da più responsabili di una catena di approvazione, impostare i responsabili di approvazione in una gerarchia. Per il tipo **Responsabile approvazione**, impostare i responsabili approvazione nella pagina **Setup utente approvazione**. Per il tipo **Gruppo di utenti del workflow**, impostare i responsabili di approvazione nella pagina **Gruppi di utenti del workflow** e definire la gerarchia assegnando numeri incrementali a ogni responsabile nel campo **Nr. sequenza**   Per ulteriori informazioni, vedere questo argomento e [Impostare gli utenti del workflow](across-how-to-set-up-workflow-users.md).  

## <a name="to-set-up-an-approval-user"></a>Per impostare un utente per l'approvazione

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup utente approvazione**, quindi scegli il collegamento correlato.  
2. Nella pagina **Setup utente approvazione** creare una nuova riga e compilare i campi come descritto nella tabella seguente.  

    |Campo|Description|  
    |---------------------------------|---------------------------------------|  
    |**ID utente**|Selezionare l'ID utente dell'utente coinvolto nel processo di approvazione.|  
    |**Codice agente/addetto acquisti**|Specificare il codice dell'agente o dell'addetto acquisti valido per l'utente nel campo **Codice agente/addetto acquisti**.<br /><br /> In genere si compila il campo **Codice agente/addetto acquisti** se l'agente o l'addetto acquisti che è responsabile del cliente o de fornitore è anche la persone che deve approvare la richiesta di vendite o di acquisto in questione.|  
    |**ID resp. approvazione**|Selezionare l'ID dell'utente che deve approvare le richieste effettuate dall'utente nel campo **ID utente** .|  
    |**Limite importo approvazione ordine**|Specificare l'importo di vendita massimo in valuta locale che l'utente nel campo  **ID utente** può approvare.|  
    |**Approvazione vendite illimitate**|Specificare che l'utente nel campo **ID utente** può approvare tutte le richieste di vendita indipendentemente dall'importo.<br /><br /> Se selezioni questa casella di controllo, non è possibile compilare il campo **Limite importo approvazione ordine**.|  
    |**Limite approvazione importo acquisto**|Specificare l'importo di acquisto massimo in valuta locale che l'utente nel campo  **ID utente** può approvare.|  
    |**Approvazione acquisti illimitati**|Specificare che l'utente nel campo **ID utente** può approvare tutte le richieste di acquisto indipendentemente dall'importo.<br /><br /> Se selezioni questa casella di controllo, non è possibile compilare il campo **Limite importo approvazione ordine**.|  
    |**Limite importo approvazione richiesta**|Specificare l'importo massimo in valuta locale che l'utente nel campo **ID utente**  può approvare per le offerte di acquisto.<br /><br /> Per utilizzare questo campo, è necessario selezionare l'opzione **Catena responsabili approvazione** nel campo **Tipo di limite responsabile approvazione** della pagina **Risposta workflow**.|  
    |**Approvazione richieste illimitate**|Specificare che l'utente nel campo **ID utente** può approvare tutte le offerte di acquisto indipendentemente dall'importo.<br /><br /> Se selezioni questa casella di controllo, non è possibile compilare il campo **Limite importo approvazione richiesta**.|  
    |**Sostituto**|Seleziona l'ID dell'utente che deve approvare le richieste effettuate dall'utente nel campo **ID utente** se l'utente nel campo **ID resp. approvazione** non è disponibile. <br /><br />**Nota:** Il sostituto può essere l'utente nel campo **Sostituto**, il responsabile approvazione diretto o l'amministratore approvazioni, in tale ordine di priorità. Per ulteriori informazioni, vedere [Utilizzare i workflow di approvazione](across-how-use-approval-workflows.md).|  
    |**Indirizzo e-mail**|Specificare l'indirizzo e-mail dell'utente nel campo **ID utente**.|  
    |**Amministratore approvazioni**|Specifica l'utente che dispone dei diritti per sbloccare il workflow di approvazione. Ad esempio, delegando le richieste di approvazione a nuovi responsabili sostitutivi ed eliminando le richieste di approvazione scadute.|

    > [!Note]
    > Solo una persona può svolgere il ruolo di amministratore di approvazioni.

3. Per testare l'impostazione degli utenti per l'approvazione, scegliere l'azione **Test Setup utente approvazione**.  
4. Ripetere i passaggi 2 e 3 per ogni utente che si desidera impostare come utente di approvazione.  

## <a name="see-related-microsoft-training"></a>Vedi il relativo [training Microsoft](/training/modules/create-workflows/)

## <a name="see-also"></a>Vedere anche

[Impostare gli utenti del workflow](across-how-to-set-up-workflow-users.md)  
[Impostazione delle notifiche del workflow](across-setting-up-workflow-notifications.md)  
[Creare i workflow](across-how-to-create-workflows.md)  
[Impostazione dei workflow](across-set-up-workflows.md)  
[Procedura dettagliata: Impostazione e utilizzo di un workflow di approvazione di acquisto](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Workflow](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
