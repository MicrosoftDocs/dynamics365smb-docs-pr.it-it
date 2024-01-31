---
title: Utilizzare i flussi di lavoro di approvazione
description: È possibile impostare e utilizzare flussi di lavoro che collegano le attività dei processi aziendali come la pubblicazione automatica o la richiesta e la concessione dell'approvazione per nuovi record.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: '1500, 1501, 1503, 1504, 1505'
ms.date: 09/13/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Utilizzare i workflow di approvazione

Un flusso di lavoro è una sequenza di attività attivate da un'azione, una condizione o una regola. I flussi di lavoro vengono solitamente implementati per integrare la logica aziendale in un'organizzazione, come la separazione dei compiti, l'unificazione dei processi o l'applicazione delle procedure consigliate.

I flussi di lavoro sono progettati per creare richieste di approvazione di una modifica del campo dei record mantenendo i vecchi dati nel caso in cui la richiesta non venga approvata. Il nuovo valore non verrà implementato fino all'approvazione dell'ultima richiesta.

La logica aziendale potrebbe essere l'approvazione di:

- Nuovi dati master come conti C/G, clienti, fornitori o articoli.
- Modifiche ai campi nei record esistenti contenenti informazioni sensibili, come ad esempio **Nr. conto corrente fornitore** o **Limite di credito cliente**.
- Modifiche ai campi nei record esistenti contenenti informazioni aziendali critiche, come ad esempio **Prezzi di vendita degli articoli**.
- Nuovi utenti o modifiche alle autorizzazioni utente.
- Documenti di acquisto.
- Documenti di vendita.
- Documenti in entrata.
- Giornali di registrazione finanziari prima della pubblicazione.

L'illustrazione seguente mostra un esempio di flusso di lavoro con approvazione sequenziale attivata da un utente. Attivando il flusso di lavoro, viene creata una richiesta di approvazione per il primo responsabile approvazione.  

![Illustrazione di un flusso di lavoro con approvazione sequenziale.](media/Workflows/approval-flow.png)

Nell'illustrazione di seguito, la richiesta deve essere approvata dal primo responsabile approvazione prima di essere inviata al successivo responsabile approvazione. Se la richiesta non viene approvata dal primo responsabile approvazione, la richiesta non passerà mai al successivo responsabile approvazione.

Il percorso seguito dall'attivazione iniziale del flusso di lavoro può variare a seconda della natura dell'approvazione.  

L'illustrazione seguente mostra un'approvazione parallela attivata dall'utente. Viene inviata una richiesta di approvazione parallela a tutti i responsabili approvazione contemporaneamente.  

![Illustrazione di un flusso di lavoro con approvazione parallela.](media/Workflows/approval-flow-2.png)

Tuttavia, il flusso di lavoro non viene conclusa finché tutte le richieste non sono state approvate, come mostrato nella figura seguente:  

![Illustrazione di un flusso di lavoro rifiutato con approvazione parallela.](media/Workflows/approval-flow-3.png)

> [!NOTE]  
> Per un flusso di lavoro con più approvatori, tutti gli approvatori devono approvare ogni passaggio prima che il flusso di lavoro possa passare all'evento successivo. L'approvazione di un solo responsabile dell'approvazione non farà avanzare il flusso di lavoro.

È possibile impostare e utilizzare i flussi di lavoro che collegano task di processi aziendali eseguiti da utenti diversi. È anche possibile creare lo stesso flusso di lavoro più di una volta. Ogni flusso di lavoro può essere attivato da un evento tramite filtri diversi. Ciò è utile se una richiesta di approvazione in un reparto deve essere approvata da un responsabile approvazione, mentre le richieste di approvazione in altri reparti devono essere approvate da un altro responsabile approvazione. I task di sistema, ad esempio la registrazione automatica, possono essere inclusi come passaggi nei flussi di lavoro e preceduti o seguiti da task degli utenti. La richiesta e la concessione dell'approvazione per creare nuovi record sono passaggi tipici del flusso di lavoro.  

Prima di poter iniziare a utilizzare i flussi di lavoro, è necessario impostare gli utenti del flusso di lavoro, creare i flussi di lavoro, potenzialmente preceduti dalla personalizzazione del codice, e specificare la modalità di ricezione delle notifiche da parte degli utenti. Ulteriori informazioni in [Impostazione flussi di lavoro](across-set-up-workflows.md).

> [!NOTE]  
> I passaggi di un flusso di lavoro tipici riguardano gli utenti che richiedono l'approvazione di attività e i responsabili dell'approvazione che accettano o rifiutano le richieste. Di conseguenza, molti argomenti che trattano l'utilizzo dei workflow fanno riferimento alle approvazioni.  

 Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli articoli che li descrivono.  

| **Per** | **Vedere** |
|--|--|
| Impostare un workflow di approvazione per iniziare quando si verifica la prima spedizione Intrastat. | [Abilitare i workflow di approvazione](across-how-to-enable-workflows.md) |
| Richiedere l'approvazione di un task, come responsabile approvazione, accettare, declinare o delegare le approvazioni e inviare o visualizzare le notifiche di approvazione. | [Procedura: Utilizzare i workflow di approvazione](across-how-use-approval-workflows.md) |
| Creare le fasi del flusso di lavoro che limitano l'utilizzo di un certo tipo di record prima del verificarsi di un determinato evento, ad esempio l'approvazione del record. | [Limitare e consentire l'utilizzo di un record](across-how-to-restrict-and-allow-usage-of-a-record.md) |
| Visualizzare istanze dei passaggi del flusso di lavoro con lo stato **Completato**. | [Visualizzare le istanze di fase workflow archiviate](across-how-to-view-archived-workflow-step-instances.md) |
| Eliminare un workflow di approvazione che non verrà più utilizzato. | [Eliminare workflow di approvazione](across-how-to-delete-workflows.md) |

## Vedere anche

[Configurare i workflow di approvazione](across-set-up-workflows.md)  
[Workflow](across-workflow.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
