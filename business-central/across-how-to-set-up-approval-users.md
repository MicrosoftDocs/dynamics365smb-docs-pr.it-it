---
title: Impostare gli utenti per l'approvazione
description: 'Prima di creare flussi di lavoro che coinvolgono passaggi di approvazione, è necessario impostare gli utenti del flusso di lavoro coinvolti nei processi di approvazione nella pagina Setup utente approvazione.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 663
ms.date: 09/08/2022
ms.author: edupont
---
# Impostare gli utenti per l'approvazione

Prima di creare workflow che coinvolgono passaggi di approvazione, è necessario impostare gli utenti del workflow coinvolti nei processi di approvazione. Nella pagina **Setup utente approvazione** è possibile anche impostare i limiti quantitativi per specifici tipi di richiesta e definire i responsabili di approvazione sostitutivi ai quali vengono delegate le richieste di approvazione in assenza del responsabile originale.  

> [!NOTE]  
> I richiedenti e i responsabili dell'approvazione, devono innanzitutto essere impostati come utenti del workflow nella pagina **Gruppo di utenti del workflow**. Ulteriori informazioni in [Impostare gli utenti del workflow](across-how-to-set-up-workflow-users.md).  

Una volta impostati questi utenti, è possibile creare le risposte del flusso di lavoro per i flussi di lavoro di approvazione. Ulteriori informazioni dal passaggio 9 in [Creare workflow di approvazione](across-how-to-create-workflows.md).  

> [!NOTE]  
> Per definire che una richiesta di approvazione non venga approvata finché più utenti non la approvano, impostare i responsabili di approvazione in una gerarchia. Per il tipo **Responsabile approvazione**, impostare i responsabili approvazione nella pagina **Setup utente approvazione**. Per il tipo **Gruppo di utenti del workflow**, impostare i responsabili di approvazione nella pagina **Gruppi di utenti del workflow** e definire la gerarchia assegnando numeri incrementali a ogni responsabile nel campo **Nr. sequenza** . Ulteriori informazioni di seguito e in [Impostare gli utenti del workflow](across-how-to-set-up-workflow-users.md).  

## Per impostare un utente per l'approvazione

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup utente approvazione**, quindi scegli il collegamento correlato.  
2. Nella pagina **Setup utente approvazione** creare una nuova riga e compilare i campi come descritto nella tabella seguente.  

   |Campo|Descrizione|
   |-----|-----------|
   |**ID utente**|Seleziona l'ID utente della persona coinvolta nel processo di approvazione.|
   |**Codice agente/addetto acquisti**|Specifica il codice del venditore o dell'acquirente che si applica all'utente.<br /><br /> In genere si compila il campo **Codice agente/addetto acquisti** se l'agente o l'addetto acquisti che è responsabile del cliente o de fornitore è anche la persone che deve approvare la richiesta di vendite o di acquisto in questione.|
   |**ID resp. approvazione**|Selezionare l'ID dell'utente della persona che deve approvare le richieste effettuate dalla persona identificata nel campo **ID utente**.|
   |**Limite importo approvazione ordine**|Specifica l'importo di vendita massimo in valuta locale (VL) che la persona identificata nel campo **ID utente** può approvare.|
   |**Approvazione vendite illimitate**|Specificare che la persona identificata nel campo **ID utente** può approvare tutte le richieste di vendita indipendentemente dall'importo.<br /><br /> Se selezioni questa casella di controllo, non è possibile compilare il campo **Limite di approvazione importo vendita**.|
   |**Limite approvazione importo acquisto**|Specifica l'importo massimo di acquisto in valuta locale che la persona identificata nel campo **ID utente** può approvare.|
   |**Approvazione acquisti illimitati**|Specifica che la persona identificata nel campo **ID utente** può approvare tutte le richieste di acquisto indipendentemente dall'importo.<br /><br /> Se selezioni questa casella di controllo, non è possibile compilare il campo **Limite di approvazione importo acquisto**.|
   |**Limite importo approvazione richiesta**|Specificare l'importo massimo in valuta locale che la persona identificata nel campo **ID utente**  può approvare per le offerte di acquisto.<br /><br /> Per utilizzare questo campo, è necessario selezionare l'opzione **Catena responsabili approvazione** nel campo **Tipo di limite responsabile approvazione** della pagina **Risposta workflow**.|
   |**Approvazione richieste illimitate**|Specifica che la persona identificata nel campo **ID utente** può approvare tutte le richieste di offerta indipendentemente dall'importo.<br /><br /> Se selezioni questa casella di controllo, non è possibile compilare il campo **Limite importo approvazione richiesta**.|
   |**Sostituto**|Seleziona l'ID della persona che approverà le richieste effettuate dalla persona nel campo **ID utente** se l'utente nel campo **ID resp. approvazione** non è disponibile. <br /><br />**Nota:** Il sostituto può essere l'utente nel campo **Sostituto**, il responsabile approvazione diretto o l'amministratore approvazioni, in tale ordine di priorità. Ulteriori informazioni in [Utilizzare i workflow di approvazione](across-how-use-approval-workflows.md).|
   |**Indirizzo e-mail**|Specificare l'indirizzo e-mail della persona nel campo **ID utente**.|
   |**Amministratore approvazioni**|Specifica l'utente che dispone dei diritti per sbloccare i workflow di approvazione delegando le richieste di approvazione a nuovi responsabili sostitutivi o eliminando le richieste di approvazione scadute.|

   > [!NOTE]
   > Solo una persona può svolgere il ruolo di amministratore di approvazioni.

3. Per testare l'impostazione degli utenti per l'approvazione, scegliere l'azione **Test Setup utente approvazione**.  
4. Ripetere i passaggi 2 e 3 per ogni persona che si desidera impostare come utente di approvazione.  

## Vedi il relativo [training Microsoft](/training/modules/create-workflows/)

## Vedere anche

[Impostare gli utenti del workflow](across-how-to-set-up-workflow-users.md)  
[Impostazione delle notifiche del workflow](across-setting-up-workflow-notifications.md)  
[Creare workflow di approvazione](across-how-to-create-workflows.md)  
[Configurare i flussi di lavoro di approvazione](across-set-up-workflows.md)  
[Procedura dettagliata: Impostazione e utilizzo di un workflow di approvazione di acquisto](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Workflow](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
