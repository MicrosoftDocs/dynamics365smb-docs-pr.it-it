---
title: Impostare gli utenti per l'approvazione
description: 'Prima di creare workflow che coinvolgono passaggi di approvazione, devi impostare gli utenti del workflow coinvolti nei processi di approvazione.'
author: brentholtorf
ms.topic: how-to
ms.devlang: al
ms.search.form: '663,'
ms.date: 05/31/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Impostare gli utenti per l'approvazione

Prima di creare workflow che coinvolgono passaggi di approvazione, devi impostare gli utenti coinvolti nei processi di approvazione nella pagina **Setup utente approvazione**. Puoi anche impostare limiti di importo per diversi tipi di richieste, definire responsabili dell'approvazione sostitutivi e impostare notifiche.  

Una volta impostati gli utenti per l'approvazione, puoi creare le risposte del workflow per i workflow di approvazione. Ulteriori informazioni in [Creare workflow di approvazione](across-how-to-create-workflows.md).  

> [!TIP]
> Puoi richiedere che più responsabili dell'approvazione reagiscano a una richiesta di approvazione creando un gruppo di responsabili dell'approvazione nella pagina **Gruppo di utenti del workflow**. Per ulteriori informazioni, vedi [Impostare gruppi utenti del workflow](across-how-to-set-up-workflow-users.md).  

## Per impostare un utente per l'approvazione

[!INCLUDE [workflow-requestor-approver](includes/workflow-requestor-approver.md)]

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup utente approvazione**, quindi scegli il collegamento correlato.  
2. Nella pagina **Setup utente approvazione** creare una nuova riga e compilare i campi come descritto nella tabella seguente.  

   |Campo|Descrizione|
   |-----|-----------|
   |**ID utente**|Seleziona l'ID utente della persona coinvolta nel processo di approvazione.|
   |**Codice agente/addetto acquisti**|Specifica il codice del venditore o dell'acquirente che si applica all'utente.<br /><br /> In genere compili il campo **Codice agente/addetto acquisti** se l'agente o l'addetto acquisti che è responsabile del cliente o de fornitore è anche la persona che deve approvare la richiesta di vendite o di acquisto in questione.|
   |**ID resp. approvazione**|Seleziona l'ID utente della persona che deve approvare le richieste effettuate dalla persona specificata nel campo **ID utente**.|
   |**Limite importo approvazione ordine**|Specifica l'importo di vendita massimo in valuta locale (VL) che la persona selezionata nel campo **ID utente** può approvare.|
   |**Approvazione vendite illimitate**|Specificare che la persona identificata nel campo **ID utente** può approvare tutte le richieste di vendita indipendentemente dall'importo.<br /><br /> Se selezioni questa casella di controllo, non è possibile compilare il campo **Limite di approvazione importo vendita**.|
   |**Limite approvazione importo acquisto**|Specifica l'importo massimo di acquisto in valuta locale che la persona identificata nel campo **ID utente** può approvare.|
   |**Approvazione acquisti illimitati**|Specifica che la persona identificata nel campo **ID utente** può approvare tutte le richieste di acquisto indipendentemente dall'importo.<br /><br /> Se selezioni questa casella di controllo, non è possibile compilare il campo **Limite di approvazione importo acquisto**.|
   |**Limite importo approvazione richiesta**|Specificare l'importo massimo in valuta locale che la persona identificata nel campo **ID utente**  può approvare per le offerte di acquisto.<br /><br /> Per utilizzare questo campo, è necessario selezionare l'opzione **Catena responsabili approvazione** nel campo **Tipo di limite responsabile approvazione** della pagina **Risposta workflow**.|
   |**Approvazione richieste illimitate**|Specifica che la persona identificata nel campo **ID utente** può approvare tutte le richieste di offerta indipendentemente dall'importo.<br /><br /> Se selezioni questa casella di controllo, non è possibile compilare il campo **Limite importo approvazione richiesta**.|
   |**Sostituto**|Seleziona l'ID utente che approverà le richieste effettuate dalla persona nel campo **ID utente** se l'utente nel campo **ID resp. approvazione** non è disponibile. <br /><br />**Nota:** Il sostituto può essere l'utente nel campo **Sostituto**, il responsabile approvazione diretto o l'amministratore approvazioni, in tale ordine di priorità. Ulteriori informazioni in [Utilizzare i workflow di approvazione](across-how-use-approval-workflows.md).|
   |**Indirizzo e-mail**|Specificare l'indirizzo e-mail della persona nel campo **ID utente**.|
   |**Amministratore approvazioni**|Specifica l'utente che dispone dei diritti per sbloccare i workflow di approvazione delegando le richieste di approvazione a nuovi responsabili sostitutivi o eliminando le richieste di approvazione scadute.<br /><br />**Nota** Solo una persona può svolgere il ruolo di amministratore di approvazioni.|

3. Per testare l'impostazione degli utenti per l'approvazione, scegliere l'azione **Test Setup utente approvazione**.  
4. Ripetere i passaggi 2 e 3 per ogni persona che si desidera impostare come utente di approvazione.  

Il passaggio successivo consiste nello specificare come si desidera [!INCLUDE [prod_short](includes/prod_short.md)] notificare alle persone che una richiesta è in attesa della loro attenzione. Per ulteriori informazioni, vedi [Impostazione delle notifiche del workflow](across-setting-up-workflow-notifications.md).

## Vedere anche

[Impostare gli utenti del flusso di lavoro](across-how-to-set-up-workflow-users.md)  
[Impostazione delle notifiche del workflow](across-setting-up-workflow-notifications.md)  
[Creare workflow di approvazione](across-how-to-create-workflows.md)  
[Configurare i workflow di approvazione](across-set-up-workflows.md)  
[Procedura dettagliata: Impostazione e utilizzo di un workflow di approvazione di acquisto](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Workflow](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
