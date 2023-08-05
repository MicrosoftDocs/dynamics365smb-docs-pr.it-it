---
title: Impostare l'assegnazione delle risorse | Documenti Microsoft
description: Informazioni su come il sistema può aiutare a garantire che l'assegnazione venga fatta a chi ha le competenze necessarie per fornire a un servizio di assistenza.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'resource, skill, service, zones'
ms.date: 04/01/2021
ms.author: bholtorf
---

# Impostare l'assegnazione delle risorse
Per assicurarsi che un compito di assistenza sia eseguito correttamente, è importante trovare una risorsa qualificata per il lavoro. È possibile configurare [!INCLUDE[prod_short](includes/prod_short.md)] di modo che sia semplice assegnare una risorsa che disponga delle competenze necessarie per il compito. In [!INCLUDE[prod_short](includes/prod_short.md)] questa funzionalità è detta _assegnazione delle risorse_. È possibile assegnare le risorse in base alla loro competenza, disponibilità o se si trovano nella stessa zona di assistenza del cliente. 

Per utilizzare l'assegnazione delle risorse, è necessario impostare:  
  
* Le competenze necessarie per riparare e gestire gli articoli in assistenza. Queste devono essere assegnate agli articoli in assistenza e alle risorse.  
* Le aree geografiche, chiamate zone, definite per il proprio mercato. Ad esempio, Est, Ovest, Centro e così via. Queste devono essere assegnate ai clienti e alle risorse.  
* Scegliere se visualizzare le zone e le competenze delle risorse e se visualizzare un avviso quando qualcuno sceglie una risorsa non qualificata o che non si trova nella zona cliente.  

## Per impostare le competenze
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Competenze**, quindi scegli il collegamento correlato.  
2. Compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## Per assegnare le competenze agli articoli in assistenza e alle risorse
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Articoli in assistenza** o **Risorse**, quindi scegli il collegamento correlato.  
2. Aprire la scheda relativa all'articolo in assistenza o alla risorsa, quindi scegliere una delle seguenti opzioni:  
  
    * Per gli articoli in assistenza, scegliere **Competenze risorse**.  
    * Per le risorse, scegliere **Competenze**.  

## Per impostare le zone
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Zone**, quindi scegli il collegamento correlato.  
2. Compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## Per assegnare le zone ai clienti e alle risorse 
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Clienti** o **Risorse**, quindi scegli il collegamento correlato.  
2. Aprire la scheda relativa all'articolo in assistenza o alla risorsa, quindi scegliere una delle seguenti opzioni:  
  
    * Per i clienti, scegliere una zona nel campo **Codice zona di assistenza**.  
    * Per le risorse, scegliere l'azione **Zone assistenza**.  

## Per specificare il contenuto da visualizzare quando si sceglie una risorsa
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup gestione assistenza**, quindi scegli il collegamento correlato. 
2. Nel campo **Opzione competenze risorse** scegliere una delle opzioni descritte nella seguente tabella.  
  
    |**Opzione**|**Description**|  
    |------------|-------------|  
    |Mostra codice | Viene visualizzato solo il codice.|  
    |Warning visualizzato | Le informazioni vengono visualizzate e appare un avviso se si sceglie una risorsa che non è qualificata.|  
    |Non usato | Le informazioni non vengono visualizzate.|  

## Per aggiornare la capacità della risorsa  
Potrebbe essere necessario modificare la capacità delle risorse.  
  
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Capacità risorsa**, quindi scegli il collegamento correlato.  
2. Scegliere la risorsa, quindi scegliere l'azione **Imposta capacità**.  
3. Apportare le modifiche, quindi scegliere **Aggiorna capacità**.  

## Per aggiornare le competenze per gli articoli, gli articoli in assistenza o i gruppi di articoli in assistenza
Se si desidera modificare i codici competenza assegnati agli articoli, ad esempio da **PC** a **PCS**, è possibile effettuare questa operazione per un articolo, un articolo in assistenza o per tutti gli articoli in un gruppo di articoli in assistenza.  
  
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Articoli**, **Articoli in assistenza** o **Gruppo articoli in assistenza**, quindi scegli il collegamento correlato.  
2. Scegliere l'entità da aggiornare, quindi scegliere l'azione **Competenze risorse**.  
3. Sulla riga contenente il codice da modificare, nel campo **Codice competenza**, scegliere il codice competenza appropriato.  
4.  Se all'articolo sono associati articoli in assistenza, verrà visualizzata una finestra di dialogo con le due opzioni seguenti:  
  
    * Modificare i codici competenze nel valore selezionato: selezionare questa opzione per sostituire il vecchio codice con il nuovo in tutti gli articoli in assistenza correlati.  
    * Eliminare i codici competenze o aggiornarne la relazione: selezionare questa opzione se si desidera modificare il codice competenza solo per l'articolo selezionato. Il codice competenza degli articoli in assistenza correlati verrà riassegnato, ovvero, il campo **Assegnato da** verrà aggiornato.  
  
## Vedi anche
[Assegnare risorse](service-how-to-allocate-resources.md)  
[Impostare le ore di lavoro e le ore di assistenza](service-how-setup-work-service-hours.md)  
[Impostare il reporting dei guasti](service-how-setup-fault-reporting.md)  
[Impostare codici per servizi standard](service-how-setup-service-coding.md)  
 



[!INCLUDE[footer-include](includes/footer-banner.md)]