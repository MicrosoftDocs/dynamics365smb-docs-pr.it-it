---
title: Creare una scheda progetto per un progetto e specificare le attività
description: 'Per un nuovo progetto, è possibile creare una scheda progetto contenente le attività progetto e le righe di pianificazione, per semplificare la gestione dell''avanzamento e del budget.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.search.keywords: 'project management, task'
ms.search.form: '88, 275, 276, 1001, 1002, 1003, 1004, 1005, 1006, 1007, 1020'
ms.date: 02/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="create-projects"></a>Creare progetti

Quando si inizia un nuovo progetto, è necessario creare una scheda progetto con le attività di progetto e le righe di pianificazione progetto integrate. La scheda è strutturata su due livelli.  

Il primo livello è costituito da attività di progetto. Occorre creare almeno un'attività di progetto per progetto perché tutte le operazioni di registrazione fanno riferimento a un'attività di progetto. La presenza di almeno un'attività nel progetto consente di impostare le righe di pianificazione progetto e di registrare il consumo nel progetto.

Il secondo livello è costituito dalle righe di pianificazione progetto, che consentono di specificare l'utilizzo dettagliato delle risorse, degli articoli e di diverse spese di contabilità generale.

La struttura a livelli consente di dividere il progetto in attività meno complesse e pertanto di dettagliare maggiormente le fasi di definizione del budget, dell'offerta e della registrazione. Inoltre, consente di ottenere informazioni dettagliate sullo stato di avanzamento di un progetto. Ad esempio, è possibile verificare se si stanno soddisfacendo le attività cardine definite o se si stanno rispettano le previsioni di budget.

> [!TIP]
> Scegliere l'azione **Nuovo progetto** in Gestione ruolo utente **Manager progetto** per avviare una guida al setup assistito che consente di creare un progetto con attività e righe di pianificazione integrati. Di seguito viene descritto come eseguire i passaggi manualmente. <!-- For an example of how to create a project manually, go to [Video: How to create a project in Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw).-->

## <a name="invoice-one-or-more-customers-for-project-tasks"></a>Fatturare a uno o più clienti per attività di progetto

A volte la parte a cui è rivolto un servizio è diversa dalla parte che pagherà la fattura. Inoltre, a volte potrebbe essere necessario fatturare a più clienti per le attività nel progetto. Nella pagina **Scheda progetto**, utilizza il campo **Metodo di fatturazione delle attività** per specificare se stai fatturando a un cliente o a più clienti.

Se anche il cliente che riceve il servizio pagherà la fattura, nei campi **Fatturazione** e **Spedizione**, scegliere **Predefinito (Cliente)** e **Predefinito (Indirizzo di vendita)**.

Se stai fatturando a più clienti, puoi specificare il cliente che riceverà il servizio e il cliente a cui fatturare ogni attività nel progetto. È inoltre possibile fornire le seguenti informazioni:

* Dove avverrà il processo selezionando da un elenco di indirizzi di spedizione per il cliente.
* Aggiungi informazioni su riferimenti esterni per semplificare la comunicazione sul progetto.
* Sovrascrivi i termini finanziari standard del progetto.

## <a name="invoice-one-customer-for-multiple-project-tasks"></a>Fatturare a un cliente per molteplici attività di progetto

Puoi semplificare il processo di fatturazione inviando una fattura a un cliente per più progetti. Aggiungi righe di pianificazione progetto da più progetti a una fattura di vendita in una volta sola. Questo processo è simile alla creazione di una fattura di vendita da una riga di pianificazione progetto e all'immissione di un valore nel campo **Aggiungi a nr. fattura vendita**.

Di seguito è riportata una panoramica del processo.

1. Crea una nuova fattura di vendita e compila il campo **Nr. cliente di vendita** . Se necessario, compila anche i campi **Nr. cliente di fatturazione** e **Codice valuta**.
2. Nella Scheda dettaglio **Righe** scegli l'azione **Ottieni righe di pianificazione progetto**. La pagina **Ottieni righe di pianificazione progetto** mostra le righe di pianificazione progetto fatturabili dai progetti per il cliente a cui vendere, il cliente a cui fatturare e la valuta di fatturazione in cui la quantità da fatturare è maggiore di zero. 
3. Scegli le righe che vuoi aggiungere alla fattura, quindi scegli **OK**.

Ripeti questi passaggi se vuoi aggiungere un altro set di righe di pianificazione progetto. Puoi anche eliminare la fattura o le relative righe e ricominciare da capo.

> [!NOTE]
> Ci sono un paio di limitazioni:
>
> * L'azione **Ottieni righe di pianificazione progetto** non è disponibile negli ordini cliente o nelle offerte di vendita.
> * Non puoi filtrare in base ai campi **Codice di spedizione** o **Nr. contatto** .

## <a name="to-create-a-project-card"></a>Per creare una scheda progetto

Crea una scheda progetto e quindi righe di attività di progetto e le relative righe di pianificazione progetto.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Progetti**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Nuovo** e compilare i campi necessari. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Per basare il progetto sulle informazioni di un altro progetto, scegli l'azione **Copia progetto**, compila i campi come necessario, quindi scegli il pulsante **OK**.

> [!NOTE]  
> Se con il progetto si stanno utilizzando dei fogli presenze, è necessario designare un responsabile. Questa persona può approvare i fogli presenze per le attività degli impiegati associate al progetto. Per maggiori informazioni, vedere [Impostare i fogli di presenza](projects-how-setup-time-sheets.md).

Facoltativamente, contrassegna le azioni sul progetto come bloccate utilizzando il campo **Bloccato**. la seguente tabella descrive gli effetti delle opzioni per questo campo.

|Opzione  |Descrizione  |
|---------|---------|
|Vuoto |Sono consentite tutte le azioni.|
|Registrazione    |È possibile utilizzare le righe di pianificazione, ma il progetto è bloccato ai fini della registrazione. Se si sceglie questa opzione, non è possibile registrare alcun utilizzo o vendita nel progetto.|
|Tutto  |Sono bloccate tutte le azioni.|

## <a name="to-create-tasks-for-a-project"></a>Per creare attività per un progetto

Una parte fondamentale nella creazione di un progetto consiste nello specificare le varie attività implicate nel progetto. Specifica le attività creando una riga per attività nella Scheda dettaglio **Attività** della pagina **Scheda progetto**. Ogni progetto deve avere almeno un'attività.

1. Scegli l'icona ![lampadina che apre la funzionalità Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Progetti**, quindi scegli il collegamento correlato.
2. Aprire la scheda progetto per un progetto pertinente.
3. Nella Scheda dettaglio **Attività** compilare i campi secondo le necessità su una nuova riga.
4. Per indentare le attività e creare una gerarchia, scegliere l'azione **Attività**, quindi l'azione **Indenta attività di progetto**.
5. Ripetere i passaggi 3 e 4 per le attività necessarie per il progetto.
6. Per specificare le attività di progetto con informazioni di altri attività di progetto, scegliere l'azione **Copia attività di progetto da**, compilare i campi necessari, quindi scegliere il pulsante **OK**.

## <a name="to-create-planning-lines-for-a-project"></a>Per creare righe di pianificazione per un progetto

È possibile perfezionare le nuove attività di progetto nelle righe di pianificazione progetto. Una riga di pianificazione può acquisire le informazioni di cui si desidera tenere traccia per un progetto. Ad esempio, puoi tenere traccia delle risorse richieste dal processo o degli articoli necessari. Ad esempio, disponi di un'attività affinché un cliente approvi un progetto. È possibile associare l'attività alle righe di pianificazione per articoli quali la riunione con il cliente e l'assegnazione di una risorsa.  

Una riga di pianificazione progetto può avere uno dei seguenti tipi.  

| Tipo | Descrizione |
| --- | --- |
| **Budget** |Fornisce le stime di utilizzo e di costo per il processo, generalmente in un tipo di progetto Time and Material. Le righe di pianificazione di questo tipo non possono essere fatturate. |
| **Fatturabile** |Fornisce le stime di fatturazione per il cliente, in genere in un progetto a prezzo fisso. |
| **Sia Budget sia fatturabile** |Fornisce un utilizzo a budget pari a ciò che si desidera fatturare. |

> [!NOTE]
> Mentre si immettono le informazioni nelle righe di pianificazione progetto, i dati sui costi vengono inseriti automaticamente. Ad esempio, il costo, il prezzo e lo sconto per le risorse e gli articoli si basano inizialmente sulle informazioni dalla risorsa e dell'articolo.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Progetti**, quindi scegli il collegamento correlato.
2. Apri una scheda progetto pertinente.
3. Selezionare un'attività di progetto per il quale il campo **Tipo di attività di progetto** contiene **Registrazione**, quindi scegliere l'azione **Righe di pianificazione progetto**.  
4. Nella pagina **Righe di pianificazione progetto**, in una nuova riga compila i campi come necessario.
5. Ripetere i passaggi 3 e 4 per tutte le righe di pianificazione necessarie per l'attività di progetto.

## <a name="see-also"></a>Vedere anche

[Gestione progetti](projects-manage-projects.md)  
[Video: Come creare un progetto in Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw)  
[Dati finanziari](finance.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Vendite](sales-manage-sales.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
