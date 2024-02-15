---
title: Come limitare e consentire l'utilizzo di un record
description: 'Se vuoi limitare l''utilizzo di un record, puoi includere due risposte in un flusso di lavoro che controlla l''utilizzo del record.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 09/08/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Limitare e consentire l'utilizzo di un record

Se si desidera limitare l'utilizzo di un record in determinate attività, ad esempio, fino all'approvazione del record, è possibile includere due risposte in un flusso di lavoro che controlla l'utilizzo del record. Una risposta del workflow limita l'utilizzo del record come definito dall'evento e dalle condizioni del flusso di lavoro. L'altra risposta del workflow consente l'utilizzo del record come definito dall'evento e dalle condizioni del workflow. Esistono due risposte nella versione predefinita di [!INCLUDE[prod_short](includes/prod_short.md)] per questo scopo: **Aggiungere limitazione record** e **Rimuovere limitazione record**.

> [!NOTE]  
> La versione predefinita di [!INCLUDE[prod_short](includes/prod_short.md)] offre il supporto per limitare la registrazione di un record, l'esportazione come pagamento e la stampa come controllo. Per supportare altre restrizioni, è necessario che un partner Microsoft personalizzi il codice dell'applicazione.  

> [!NOTE]  
> La funzionalità del flusso di lavoro per limitare e consentire l'utilizzo dei record non è correlata alla funzionalità per bloccare la registrazione di record relativi a fornitori, clienti e articoli.

Nella procedura riportata di seguito viene descritto come limitare la registrazione degli ordini di acquisto fino all'approvazione. Il nuovo flusso di lavoro si baserà sul modello esistente del *flusso di lavoro di approvazione della fattura di acquisto*.  

## Creare una fase del flusso di lavoro che limiti la registrazione degli ordini di acquisto non approvati

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Flussi di lavoro**, quindi scegli il collegamento correlato.  
2. Nella pagina **Workflow** scegliere l'azione **Nuovo workflow da modello**. Ulteriori informazioni in [Creare workflow da modelli di workflow](across-how-to-create-workflows-from-workflow-templates.md).
3. Nella pagina **Modelli del workflow**, seleziona il modello *Flusso di lavoro approvazione ordine acquisto*.  

   Nota che le prime due fasi del flusso di lavoro sono relative alla limitazione e all'autorizzazione dell'utilizzo delle fatture di acquisto. Modifica la condizione di evento nella prima fase del nuovo flusso di lavoro per specificare che si applica agli ordini di acquisto.  
4. Nella Scheda dettaglio **Fasi workflow** scegli il campo **Condizione** per il primo passaggio e per il filtro **Tipo di documento** scegli **Ordine**.  
5. Continuare per modificare, eliminare o aggiungere altre fasi del flusso di lavoro per creare un processo aziendale che inizia limitando la registrazione degli ordini di acquisto non approvati.  

## Vedere anche

[Utilizzare i workflow di approvazione](across-use-workflows.md)  
[Creare workflow di approvazione](across-how-to-create-workflows.md)  
[Workflow](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
