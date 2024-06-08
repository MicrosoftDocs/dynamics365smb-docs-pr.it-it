---
title: Creare flussi di lavoro di approvazione per connettere le attività
description: Scopri come creare flussi di lavoro che collegano attività di processi aziendali eseguiti da utenti diversi nei processi aziendali.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 04/24/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="create-workflows-to-connect-tasks-in-business-processes"></a>Creare flussi di lavoro per connettere nei processi aziendali

Puoi creare flussi di lavoro che collegano attività nei processi aziendali eseguiti da utenti diversi. Puoi includere le attività di sistema, ad esempio la registrazione automatica, come passaggi nei flussi di lavoro e preceduti o seguiti da task degli utenti. La richiesta e la concessione dell'approvazione per creare nuovi record sono passaggi tipici del flusso di lavoro.  

Nella pagina **Workflow** crea un workflow elencando i passaggi nelle righe. Ogni passaggio è costituito da un trigger e una risposta:

* Un evento che specifica le condizioni che avvieranno il workflow.
* Una risposta del workflow che definisce cosa fa il workflow.

[!INCLUDE[workflow](includes/workflow.md)]

Quando si creano i flussi di lavoro, è possibile copiare i passaggi dai flussi di lavoro esistenti o dai modelli di flusso di lavoro. I modelli di workflow sono workflow non modificabili forniti da [!INCLUDE[prod_short](includes/prod_short.md)]. I codici identificativi dei workflow hanno il prefisso "MS-", ad esempio "MS-PIW". Ulteriori informazioni in [Creare workflow da modelli di workflow](across-how-to-create-workflows-from-workflow-templates.md).  

> [!NOTE]  
> Tutte le notifiche sui passaggi del flusso di lavoro vengono inviate tramite una coda processi. Assicurati che la coda dei lavori rifletta le tue esigenze aziendali. Per ulteriori informazioni, vedi [Utilizzare le code processi per pianificare le attività](admin-job-queues-schedule-tasks.md).  

:::image type="content" source="media/Workflows/workflow-example.png" alt-text="Illustrazione di un esempio di flusso di lavoro.":::

Un workflow è diviso in tre sezioni:

1. **Evento**  
   Qui è dove si seleziona il trigger.  
   Esempi di trigger:
   * Modifica di un record di dati anagrafici
   * Creazione di una riga di registrazione
   * Creazione o rilascio di un documento in entrata
   * Richiesta di approvazione di un documento
2. **Condizione**  
   Le **condizioni** sono correlate all'evento e consentono di creare filtri per decidere come continuare il flusso di lavoro.
3. **Risposta**  
   Le **risposte** specificano i passaggi successivi nel flusso di lavoro.

Le opzioni per gli eventi e per le risposte sono definite dal sistema. Per aggiungere nuove opzioni, dovrai sviluppare un'estensione.

## <a name="to-create-a-workflow"></a>Per creare un flusso di lavoro

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Flussi di lavoro**, quindi scegli il collegamento correlato.  
2. Scegli l'azione **Nuovo**. Verrà aperta la pagina **Workflow**.  
3. Nel campo **Codice** immettere un massimo di 20 caratteri che identifichino il workflow.  
4. Per creare il workflow da un modello di workflow, nella pagina **Workflow** scegli l'azione **Nuovo workflow da modello**. Ulteriori informazioni in [Creare workflow da modelli di workflow](across-how-to-create-workflows-from-workflow-templates.md).  
5. Nel campo  **Descrizione** descrivere il workflow.  
6. Nel campo **Categoria** specificare a quale categoria appartiene il flusso di lavoro.  
7. Nel campo **Evento** specificare l'evento che deve verificarsi per avviare la fase workflow.  

   Quando scegli il campo, viene visualizzata la pagina **Eventi workflow** con tutti gli eventi workflow disponibili.  
8. Nel campo **Condizione** specifica una o più condizioni che devono essere soddisfatte prima che si verifichi l'evento nel campo **Evento**.  

   Quando scegli il campo, la pagina **Condizioni evento** elenca i campi filtro che possono essere condizioni per l'evento. Puoi aggiungere nuovi campi filtro se lo desideri.  

   Se l'evento del flusso di lavoro è la modifica di un campo specifico di un record, la pagina **Condizioni evento** per selezionare il campo e il tipo di modifica.  

   1. Per specificare una modifica di campo per l'evento, nella pagina **Condizioni evento**, nel campo **Campo**, selezionare il campo che viene modificato.  
   2. Nel campo **Operatore**, selezionare **Diminuito**, **Aumentato** o **Modificato**.  
9. Nel campo **Risposta** specificare la risposta che seguirà quando si verificherà l'evento workflow.  

   Quando scegli il campo, viene visualizzata la pagina **Risposte workflow** con tutte le risposte eventi workflow e le opzioni di risposta disponibili.  
10. Nella scheda dettaglio **Opzioni per risposta selezionata**, specifica le opzioni per la risposta del flusso di lavoro selezionando i valori nei diversi campi che vengono visualizzati, come segue:  

    1. Per specificare le opzioni per una risposta del flusso di lavoro che includa l'invio di una notifica, compilare i campi come descritto nella tabella seguente.  

    > [!NOTE]
    > Questi campi variano a seconda della risposta che hai scelto.

       |Campo|Descrizione|
       |-----|-----------|
       |**Notifica mittente**|Specifica se desideri inviare una notifica al richiedente dell'approvazione anziché al destinatario della richiesta di approvazione. Se selezioni la casella di controllo, il campo **ID utente destinatario** viene disabilitato poiché la notifica sarà invece inviata al richiedente dell'approvazione, ovvero il mittente. Il nome della risposta workflow cambia di conseguenza in **Crea notifica per &lt;Mittente &gt;**. Se la casella di controllo non è selezionata, il nome della risposta workflow è **Crea notifica per &lt;Utente &gt;**.|
       |**ID utente destinatario**|Specificare l'utente a cui deve essere inviata la notifica. **Nota**: questa opzione è disponibile solo per le risposte del flusso di lavoro con un segnaposto per un utente specifico. Per le risposte del flusso di lavoro senza segnaposto per gli utenti, il destinatario della notifica in genere è definito dal **Setup utente approvazione**.|
       |**Tipo movimento notifica**|Specifica un trigger per la notifica del workflow. Il trigger può essere una modifica del record, una richiesta di approvazione o una data di scadenza superata.|
       |**Pagina destinazione collegamento**|Specifica la pagina che apre il collegamento nella notifica. La pagina deve avere la stessa tabella di origine del record interessato.|
       |**Collegamento personalizzato**|Specifica l'URL di un collegamento che viene incluso nella notifica insieme al collegamento della pagina.|

    2. Per specificare le opzioni per una risposta del flusso di lavoro che includa la creazione di una richiesta di approvazione, compilare i campi come descritto nella tabella seguente.  

       |Campo|Descrizione|  
       |-----|-----------|  
       |**Formula data di scadenza**|Specifica il numero di giorni a disposizione del responsabile dell'approvazione per risolvere la richiesta. Il periodo decorre dall'invio della richiesta.|
       |**Delega dopo**|Specifica se e quando una richiesta di approvazione viene automaticamente delegata al sostituto. È possibile selezionare di delegare automaticamente uno, due o cinque giorni dopo la data in cui l'approvazione è stata richiesta.|
       |**Tipo di responsabile approvazione**|Specificare chi è il responsabile approvazione, in base al setup degli utenti approvazione e degli utenti del flusso di lavoro. Il campo è impostato su **Agenti/Addetti acq.**, l'utente specificato nel campo **Codice agente/addetto acquisti** nella pagina **Setup utente approvazione** determina il responsabile dell'approvazione. I movimenti di richiesta approvazione verranno quindi creati in base al valore del campo **Tipo di limite responsabile approvazione**. Ulteriori informazioni in [Impostare utenti per l'approvazione](across-how-to-set-up-workflow-users.md).|
       |**Mostra messaggio di conferma**|Specificare se un messaggio di conferma viene visualizzato agli utenti quando richiedono un'approvazione.|
       |**Tipo di limite responsabile approvazione**|Specifica l'effetto dei limiti per i responsabili dell'approvazione. Il limite di approvazione di un responsabile dell'approvazione deve essere superiore al valore della richiesta. Sono disponibili le seguenti opzioni: <ol><li>**Catena responsabili approvazione** specifica che i movimenti di richiesta di approvazione vengono creati per tutti i responsabili dei richiedenti, incluso il primo responsabile approvazione qualificato</li><li>**Responsabile approvazione diretto** specifica che un movimento di richiesta di approvazione viene creato solo per il responsabile approvazione immediato del richiedente, indipendentemente dal limite di approvazione del responsabile.</li><li>**Primo responsabile dell'approvazione qualificato** specifica che un movimento di richiesta di approvazione viene creato solo per il primo responsabile dell'approvazione del richiedente.</li><li>**Responsabile dell'approvazione specifico** specifica che si notifica all'utente scelto nel campo **ID resp. approvazione**.</li></ol>|

    3. Per specificare le opzioni per una risposta del flusso di lavoro che includa la creazione delle righe di registrazione, compilare i campi come descritto nella tabella seguente.  

       |Campo|Descrizione|  
       |-----|-----------|  
       |**Nome definizione registrazioni COGE**|Specificare il nome del modello di registrazioni CoGe in cui vengono create le righe di registrazione specificate.|  
       |**Nome batch registrazioni COGE**|Specificare il nome del batch di registrazioni CoGe in cui vengono create le righe di registrazione specificate.|  

11. Scegli i pulsanti **Aumenta rientro** e **Riduci rientro** per far rientrare il nome dell'evento nel campo **Quando** per definire la posizione della fase nel flusso di lavoro.  

    1. Fai rientrare l'evento sotto il nome del passaggio precedente per indicare che si tratta del passaggio successivo.  
    2. Specificare che il passaggio fa parte di un gruppo di diversi passaggi alternativi che possono iniziare a seconda della relativa condizione posizionando il nome dell'evento in corrispondenza dello stesso rientro degli altri passaggi alternativi. Ordinare questi passaggi facoltativi in base alla priorità posizionando per primo il passaggio più importante.  

    > [!NOTE]  
    >  È possibile modificare solo il rientro di un passaggio a cui non è associato un passaggio successivo.  

12. Ripeti i passaggi da 7 a 11 per aggiungere altre fasi del flusso di lavoro, prima o dopo la fase appena creata.  
13. Attiva la casella di controllo **Abilitato** per specificare che il workflow comincerà non appena si verifica l'evento nel primo passaggio di tipo **Punto di ingresso**. Ulteriori informazioni in [Utilizzare i flussi di lavoro](across-use-workflows.md).  

> [!NOTE]  
> Non abilitare un workflow finché non sei sicuro che sia pronto.  

> [!TIP]  
> Per esplorare le relazioni tra le tabelle utilizzate nei workflow, scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") e immetti **Workflow - Relazioni tabella**.  

## <a name="example-of-creating-a-new-workflow-using-existing-events"></a>Esempio di creazione di un nuovo flusso di lavoro utilizzando eventi esistenti

Nell'esempio seguente viene creato un nuovo workflow per approvare una modifica al nome di un fornitore:

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Flussi di lavoro**, quindi scegli il collegamento correlato.  
2. Scegli l'azione **Nuovo**. Verrà aperta la pagina **Workflow**.
3. Nella sezione flusso di lavoro, compila i campi come descritto nella tabella riportata di seguito.

    |Campo  |Valore  |
    |---------|---------|
    |**Codice**|**VENDAPN-01**|
    |**descrizione**|**Approvazione della modifica del nome del fornitore** |
    |**Categoria**|**ACQ**|

4. Per creare il primo passaggio del flusso di lavoro, segui questi passaggi.

    1. Nel campo **Evento** specifica *Record fornitore cambiato*.  
    2. Nel campo **Condizione**, scegli la parola **Sempre**. Poi, nella pagina **Condizioni evento** scegli il collegamento **Aggiungere una condizione in caso di modifica di un valore campo**, quindi seleziona il campo **Nome**. Il risultato di questo passaggio è che la condizione viene letta come *Il nome è cambiato*.  
    3. Nel campo **Risposta**, scegli il collegamento **Seleziona risposta**. Quindi, nella pagina **Risposte workflow**, nel campo **Seleziona risposta**, scegli la risposta **Ripristinare il valore del campo \<Field\> sul record e salvare la risposta modificata**. Poi, nella sezione **Opzioni per la risposta selezionata**, specifica il campo **Nome**.  
    4. Scegli il collegamento **Aggiungi più risposte**, quindi aggiungi una voce per la risposta **Creare una richiesta di approvazione per il record utilizzando il tipo di responsabile approvazione <%1> e <%2>**.  
    5. Nella sezione **Opzioni per la risposta selezionata** per la nuova risposta, modifica il campo **Tipo di responsabile approvazione** in **Gruppo utenti workflow**. Quindi, nel campo **Gruppo utenti workflow**, specifica il gruppo utenti. Ulteriori informazioni in [Impostare utenti per l'approvazione](across-how-to-set-up-approval-users.md).  
    6. Aggiungi una terza risposta e scegli **Inviare la richiesta di approvazione per il record e creare una notifica**.  
    7. Aggiungi una quarta risposta, **Mostra messaggio "%1"**. Quindi, nella sezione **Opzioni per la risposta selezionata**, nel campo **Messaggio**, specifica **È stata inviata una richiesta di approvazione**.  
    8. Scegli **OK** per tornare al passaggio del flusso di lavoro.  

5. Nella riga successiva, aggiungi un nuovo passaggio del flusso di lavoro per l'evento **Richiesta approvazione approvata**.

    1. Nel campo **Evento** specifica **Richiesta approvazione approvata**.  
    2. Scegli il menu della riga, quindi scegli **Aumenta rientro**.  
    3. Nel campo **Condizione**, scegli **Sempre**. Quindi, nel campo **In attesa di approvazione**, specifica **0**. La condizione si legge come **In attesa di approvazione: 0** per indicare che la richeista non richiede altri responsabili dell'approvazione.  
    4. Nel campo **Risposta**, scegli il collegamento **Seleziona risposta**. Nella pagina **Risposte workflow**, nel campo **Seleziona risposta**, scegli la risposta **Inviare la richiesta di approvazione per il record e creare una notifica**.  
    5. Selezionare **OK**.  
6. Nella riga successiva, aggiungi un secondo passaggio del flusso di lavoro per l'evento **Richiesta approvazione approvata**.  

    1. Nel campo **Evento** specifica **Richiesta approvazione approvata**.
    2. Nel campo **Condizione**, scegli **Sempre**. Quindi, nel campo **In attesa di approvazione**, specifica **>0**. La condizione si legge come **In attesa di approvazione: >0** per indicare che questo non è l'ultimo responsabile dell'approvazione.  
    3. Nel campo **Risposta**, scegli il collegamento **Seleziona risposta**. Nella pagina **Risposte workflow**, nel campo **Seleziona risposta**, scegli la risposta **Inviare la richiesta di approvazione per il record e creare una notifica**.  
    4. Selezionare **OK**.  
7. Nella riga successiva, aggiungi un passaggio del flusso di lavoro per l'evento **Richiesta approvazione delegata**.  

    1. Nel campo **Evento** specifica **Richiesta approvazione delegata**.  
    2. Nel campo **Condizione** lascia il valore come **Sempre**.  
    3. Nel campo **Risposta**, scegli il collegamento **Seleziona risposta**. Nella pagina **Risposte workflow**, nel campo **Seleziona risposta**, scegli la risposta **Inviare la richiesta di approvazione per il record e creare una notifica**.  
    4. Selezionare **OK**.  
8. Nella riga successiva, aggiungi un secondo passaggio del flusso di lavoro per l'evento **Richiesta approvazione rifiutata**.  

    1. Nel campo **Evento** specifica **Richiesta approvazione rifiutata**.  
    2. Nel campo **Condizione** lascia il valore come **Sempre**.  
    3. Nel campo **Risposta**, scegli il collegamento **Seleziona risposta**. Nella pagina **Risposte workflow**, nel campo **Seleziona risposta**, scegli la risposta **Ignorare i nuovi valori**.  
    4. Scegli il collegamento **Aggiungi più risposte**, quindi aggiungi una voce per la risposta **Rifiutare la richiesta di approvazione per il record e creare una notifica**
    5. Selezionare **OK**.  
9. Per abilitare il flusso di lavoro attiva l'interruttore **Abilitato**.  

La seguente illustrazione fornisce una panoramica del risultato di questa procedura.  

:::image type="content" source="media/Workflows/workflow-example-2.png" alt-text="Illustrazione del flusso di lavoro di approvazione del nome del fornitore.":::

Successivamente, dovrai testare il flusso di lavoro aprendo una scheda fornitore esistente e modificando il nome. Verifica che venga inviata una richiesta di approvazione dopo la modifica del nome del fornitore.

## <a name="see-also"></a>Vedere anche

[Creare flussi di lavoro da modelli di flussi di lavoro](across-how-to-create-workflows-from-workflow-templates.md)  
[Impostare gli utenti per l'approvazione](across-how-to-set-up-approval-users.md)  
[Impostazione delle notifiche del workflow di approvazione](across-setting-up-workflow-notifications.md)  
[Visualizzare le istanze di fase workflow archiviate](across-how-to-view-archived-workflow-step-instances.md)  
[Eliminare i workflow di approvazione](across-how-to-delete-workflows.md)  
[Procedura dettagliata: Impostazione e utilizzo di un workflow di approvazione di acquisto](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Configurare i flussi di lavoro di approvazione](across-set-up-workflows.md)  
[Utilizzare i workflow di approvazione](across-use-workflows.md)  
[Workflow](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
