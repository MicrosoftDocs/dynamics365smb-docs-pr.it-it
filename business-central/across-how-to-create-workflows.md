---
title: Come creare workflow | Microsoft Docs
description: È possibile creare flussi di lavoro che collegano task di processi aziendali eseguiti da utenti diversi. I task di sistema, ad esempio la registrazione automatica, possono essere inclusi come passaggi nei flussi di lavoro e preceduti o seguiti da task degli utenti. La richiesta e la concessione dell'approvazione per creare nuovi record sono passaggi tipici del workflow.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 61493e1c98f54c37ba729fd53ad42336c2fc3d35
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/29/2019
ms.locfileid: "1245503"
---
# <a name="create-workflows"></a>Creare i workflow
È possibile creare workflow che collegano task di processi aziendali eseguiti da utenti diversi. I task di sistema, ad esempio la registrazione automatica, possono essere inclusi come passaggi nei flussi di lavoro e preceduti o seguiti da task degli utenti. La richiesta e la concessione dell'approvazione per creare nuovi record sono passaggi tipici del workflow.  

Nella pagina **Workflow** creare un workflow elencando le fasi interessate nelle righe. Ogni passaggio consiste in un evento del flusso di lavoro, moderato dalle condizioni di evento, e in una risposta del flusso di lavoro con le opzioni di risposta. È possibile definire le fasi workflow compilando i campi delle righe del workflow in base a elenchi fissi di valori di evento e di risposta che rappresentano gli scenari supportati dal codice dell'applicazione.  

Quando si creano i flussi di lavoro, è possibile copiare i passaggi dai flussi di lavoro esistenti o dai modelli di flusso di lavoro. I modelli di flusso di lavoro rappresentano flussi di lavoro non modificabili presenti nella versione generica di [!INCLUDE[d365fin](includes/d365fin_md.md)]. Il codice dei modelli di flusso di lavoro che vengono aggiunti da Microsoft hanno il prefisso "MS-", ad esempio "MS-PIW". Per ulteriori informazioni, vedere [Creare workflow da modelli di workflow](across-how-to-create-workflows-from-workflow-templates.md).  

Se uno scenario aziendale richiede eventi o risposte del flusso di lavoro non supportati, il partner Microsoft deve implementarli tramite la personalizzazione del codice dell'applicazione.  
  
> [!NOTE]  
>  Tutte le notifiche sui passaggi del flusso di lavoro vengono inviate tramite una coda processi. Assicurarsi che la coda processi nella propria installazione sia impostata in modo da gestire le notifiche del workflow e che la casella di controllo **Avvia automaticamente da NAS** sia selezionata. Per ulteriori informazioni, vedere [Utilizzare le code processi per pianificare i task](admin-job-queues-schedule-tasks.md).  

## <a name="to-create-a-workflow"></a>Per creare un flusso di lavoro  
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Workflow** e quindi scegliere il collegamento correlato.  
2. Scegliere l'azione **Nuovo**. Verrà aperta la pagina **Workflow**.  
3. Nel campo **Codice** immettere un massimo di 20 caratteri che identifichino il workflow.  
4. Per creare il workflow da un modello di workflow, nella pagina **Workflow** scegliere l'azione **Crea flusso di lavoro da modello**. Per ulteriori informazioni, vedere [Creare workflow da modelli di workflow](across-how-to-create-workflows-from-workflow-templates.md).  
5. Nel campo  **Descrizione** descrivere il workflow.  
6. Nel campo **Categoria** specificare a quale categoria appartiene il flusso di lavoro.  
7. Nel campo **Evento** specificare l'evento che deve verificarsi per avviare la fase workflow.  

    Quando si sceglie il campo, viene visualizzata la pagina **Eventi workflow** nella quale è possibile scegliere un evento da tutti gli eventi workflow esistenti.  
8. Nel campo **Condizione** specificare una o più condizioni che devono essere soddisfatte prima che si verifichi l'evento nel campo **Evento**.  

    Quando si sceglie il campo, viene visualizzata la pagina **Condizioni evento** in cui è possibile scegliere da un elenco di campi di filtro pertinenti come condizioni dell'evento in questione. È possibile aggiungere nuovi campi filtro da utilizzare come condizioni di evento. I filtri di condizione di evento si impostano come i filtri delle pagine di richiesta report.  

    Se l'evento del flusso di lavoro è la modifica di un campo specifico di un record, la pagina **Condizioni evento** viene visualizzata con le opzioni per selezionare il campo e il tipo di modifica.  

    1.  Per specificare una modifica di campo per l'evento, nella pagina **Condizioni evento**, nel campo **Campo**, selezionare il campo che viene modificato.  
    2.  Nel campo **Operatore**, selezionare **Diminuito**, **Aumentato** o **Modificato**.  
9. Nel campo **Risposta** specificare la risposta che seguirà quando si verificherà l'evento workflow.  

     Quando si sceglie il campo, viene aperta la pagina **Risposte workflow** in cui è possibile effettuare una scelta tra tutte le risposte workflow esistenti e impostare le opzioni per la risposta selezionata.  
10. Nella scheda dettaglio **Opzioni per risposta selezionata**, specificare le opzioni per la risposta del flusso di lavoro selezionando i valori nei diversi campi che vengono visualizzati, come segue:  

    1.  Per specificare le opzioni per una risposta del flusso di lavoro che includa l'invio di una notifica, compilare i campi come descritto nella tabella seguente.  

        |Campo|Description|  
        |----------------------------------|---------------------------------------|  
        |**ID utente destinatario**|Specificare l'utente a cui deve essere inviata la notifica. Nota: questa opzione è disponibile solo per le risposte workflow con un segnaposto per un utente specifico. Per le risposte del flusso di lavoro senza segnaposto per gli utenti, il destinatario della notifica in genere è definito dall'impostazione dell'utente approvazione.|  
        |**Pagina destinazione collegamento**|Specificare un'altra pagina in [!INCLUDE[d365fin](includes/d365fin_md.md)] che viene aperta dal collegamento nella notifica al posto della pagina predefinita.|  
        |**Collegamento personalizzato**|Specificare l'URL di un collegamento che viene aggiunto alla notifica insieme al collegamento di una pagina in [!INCLUDE[d365fin](includes/d365fin_md.md)].|  
    2.  Per specificare le opzioni per una risposta del flusso di lavoro che includa la creazione di una richiesta di approvazione, compilare i campi come descritto nella tabella seguente.  

        |Campo|Description|  
        |----------------------------------|---------------------------------------|  
        |**Formula data di scadenza**|Specificare in quanti giorni è necessario risolvere la richiesta di approvazione a partire dalla data di invio.|  
        |**Delega dopo**|Specificare se e quando una richiesta di approvazione verrà automaticamente delegata al sostituto pertinente. È possibile selezionare di delegare automaticamente uno, due o cinque giorni dopo la data in cui l'approvazione è stata richiesta.|  
        |**Tipo di responsabile approvazione**|Specificare chi è il responsabile approvazione, in base al setup degli utenti approvazione e degli utenti del flusso di lavoro.<br /><br /> Sono disponibili le seguenti opzioni:<br /><br /> -   **Agenti/Addetti acq.** specifica che l'utente impostato nel campo **Codice agente/addetto acquisti** nella pagina **Setup utente approvazione** determina il responsabile approvazione. I movimenti di richiesta approvazione verranno quindi creati in base al valore del campo **Tipo di limite responsabile approvazione**.<br />     Per ulteriori informazioni, vedere [Impostare utenti per l'approvazione](across-how-to-set-up-workflow-users.md).|  
        |**Mostra messaggio di conferma**|Specificare se un messaggio di conferma viene visualizzato agli utenti quando richiedono un'approvazione.|  
        |**Tipo di limite responsabile approvazione**|Specificare l'influenza dei limiti di approvazione dei responsabili quando vengono creati movimenti di richiesta di approvazione. Un responsabile approvazione qualificato è un responsabile il cui limite di approvazione è superiore al valore nella richiesta effettuata.<br /><br /> Sono disponibili le seguenti opzioni:<br /><br /> 1.  **Catena responsabili approvazione** specifica che i movimenti di richiesta di approvazione vengono creati per tutti i responsabili dei richiedenti, incluso il primo responsabile approvazione qualificato.<br />2.  **Responsabile approvazione diretto** specifica che un movimento di richiesta di approvazione viene creato solo per il responsabile approvazione immediato del richiedente, indipendentemente dal limite di approvazione del responsabile.<br />3.  **Primo responsabile approvazione qualificato** specifica che un movimento di richiesta di approvazione viene creato solo per il primo responsabile approvazione del richiedente.<br />|  
    3.  Per specificare le opzioni per una risposta del flusso di lavoro che includa la creazione delle righe di registrazione, compilare i campi come descritto nella tabella seguente.  

        |Campo|Description|  
        |----------------------------------|---------------------------------------|  
        |**Nome definizione registrazioni COGE**|Specificare il nome del modello di registrazioni CoGe in cui vengono create le righe di registrazione specificate.|  
        |**Nome batch registrazioni COGE**|Specificare il nome del batch di registrazioni CoGe in cui vengono create le righe di registrazione specificate.|  

11. Scegliere i pulsanti **Aumenta rientro** e **Riduci rientro** per far rientrare il nome dell'evento nel campo **Quando** per definire la posizione della fase nel workflow.  
    1.  Specificare che la fase è la successiva nella sequenza del flusso di lavoro, impostando un rientro per il nome dell'evento sotto il nome dell'evento della fase precedente.  
    2.  Specificare che il passaggio fa parte di un gruppo di diversi passaggi alternativi che possono iniziare a seconda della relativa condizione posizionando il nome dell'evento in corrispondenza dello stesso rientro degli altri passaggi alternativi. Ordinare questi passaggi facoltativi in base alla priorità posizionando per primo il passaggio più importante.  

    > [!NOTE]  
    >  È possibile modificare solo il rientro di un passaggio a cui non è associato un passaggio successivo.  

12. Ripetere i passaggi da 7 a 11 per aggiungere altre fasi del flusso di lavoro, prima o dopo la fase appena creata.  
13. Selezionare la casella di controllo **Abilitato** per specificare che il workflow comincerà non appena si verifica l'evento nel primo passaggio di tipo **Punto di ingresso**. Per ulteriori informazioni, vedere [Utilizzo dei workflow](across-use-workflows.md).  

> [!NOTE]  
>  Non abilitare un flusso di lavoro finché non si è sicuri che quest'ultimo sia completo e che i relativi passaggi interessati possano iniziare.  

> [!TIP]  
>  Per visualizzare le relazioni tra le tabelle utilizzate nei workflow, scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") e quindi immettere **Workflow - Relazione tabella**.  

## <a name="see-also"></a>Vedi anche  
[Creare flussi di lavoro da modelli di flusso di lavoro](across-how-to-create-workflows-from-workflow-templates.md)   
[Impostare gli utenti per l'approvazione](across-how-to-set-up-approval-users.md)   
[Impostazione delle notifiche del workflow](across-setting-up-workflow-notifications.md)   
[Visualizzare le istanze di fase workflow archiviate](across-how-to-view-archived-workflow-step-instances.md)   
[Eliminare i workflow](across-how-to-delete-workflows.md)   
[Procedura dettagliata: Impostazione e utilizzo di un workflow di approvazione di acquisto](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
[Impostazione dei workflow](across-set-up-workflows.md)   
[Utilizzo dei workflow](across-use-workflows.md)   
[Workflow](across-workflow.md)      

