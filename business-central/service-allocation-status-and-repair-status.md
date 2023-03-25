---
title: Stato di assegnazione e stato di riparazione | Documenti Microsoft
description: Informazioni sulla relazione tra lo stato di riparazione degli articoli in assistenza e lo stato di assegnazione dei relativi movimenti.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'resources, allocation, status, repairs'
ms.date: 04/01/2021
ms.author: bholtorf
---
# Stato di assegnazione e stato di riparazione degli articoli in assistenza
Lo stato di riparazione degli articoli in assistenza e lo stato di assegnazione dei movimenti di assegnazione degli articoli in assistenza sono correlati in Gestione assistenza. Lo stato di assegnazione cambia quando lo stato di riparazione dell'articolo in assistenza viene modificato in **Completato** o **Parzialmente Assistito** e quando un'offerta di assistenza viene convertita in ordine di assistenza. Lo stato di riparazione dell'articolo in assistenza cambia quando l'assegnazione dell'articolo in assistenza viene eliminata o quando l'articolo in assistenza viene riassegnato ad un'altra risorsa. Lo stato di riparazione degli articoli in assistenza può essere visualizzato nella pagina **Compiti di Assistenza** e aggiornato nel campo **Codice Stato Riparazione** della pagina **Prospetto Art. in Assist.** È possibile visualizzare lo stato di assegnazione nel campo **Stato** della pagina **Assegnazioni Risorse**.  
  
## Modifica dello stato di riparazione  
Quando lo stato di riparazione di un articolo in assistenza viene modificato in una riga di articoli in assistenza, viene ricercato un movimento di assegnazione corrispondente per questo articolo in assistenza con stato **Attivo**. Se tale movimento viene individuato, lo stato viene aggiornato in uno dei seguenti modi:  
  
* Se lo stato di riparazione viene modificato in **Completato**, lo stato di assegnazione passerà da **Attivo** a **Completato**.  
* Se lo stato di riparazione viene modificato in **Parzialmente assistito**, ovvero parte dell'assistenza è stata completata, o in **Demandato**, ovvero non è stata prestata alcuna assistenza, lo stato di assegnazione passerà da **Attivo** a **Riassegnazione necessaria**.  
* Quando si crea un movimento di assegnazione di un ordine di assistenza, in cui si indica che non è stata assegnata alcuna risorsa, il campo **Stato** della pagina **Assegnazioni risorse** viene impostato su **Non attivo**.  
* Lo stato del movimento di assegnazione viene impostato su **Annullato** quando si riassegna l'articolo in assistenza demandato nel movimento di assegnazione dell'ordine di assistenza, indicando che la risorsa o il gruppo di risorse assegnato non ha eseguito il compito di assistenza.  
  
Lo stato di assegnazione indica quando termina l'assistenza o quando è richiesta un'altra risorsa per completare l'assistenza dell'articolo.  
  
## Conversione delle offerte di assistenza in ordini di assistenza  
Quando un'offerta di assistenza viene convertita in ordine di assistenza, l'ordine e gli articoli in assistenza dell'ordine con i relativi movimenti di assegnazione vengono aggiornati come segue:  
  
* Lo stato di riparazione degli articoli in assistenza passa a **Iniziale**.  
* Lo stato dell'ordine di assistenza passa a **In sospeso**.  
* Vengono ricercati i movimenti di assegnazione per tutti gli articoli in assistenza dell'ordine di assistenza che presentano stato **Attivo**. Se tali movimenti di assegnazione vengono trovati, lo stato di assegnazione passerà da **Attivo** a **Riassegnazione necessaria**.  
  
## Eliminazione delle assegnazioni  
Quando viene eliminata l'assegnazione di un articolo in assistenza, [!INCLUDE[prod_short](includes/prod_short.md)] aggiorna lo stato di assegnazione del movimento di assegnazione corrispondente da **Attivo** a **Riassegnazione necessaria**.

Lo stato di riparazione dell'articolo in assistenza nel movimento di assegnazione verrà aggiornato come segue:  
  
* Se lo stato di riparazione è **Iniziale**, passerà a **Demandato** (l'assistenza non è ancora iniziata);  
* Se lo stato di riparazione è **In corso**, passerà a **Parzialmente assistito** (parte dell'assistenza è conclusa).  
  
## Riassegnazione di un movimento di assegnazione attivo  
Durante la riassegnazione di un articolo in assistenza in un movimento di assegnazione con stato **Attivo**, il movimento di assegnazione viene aggiornato come segue:  
  
* Se l'assistenza è iniziata quando l'assegnazione aveva stato **Attivo**, ovvero se lo stato di riparazione dell'articolo in assistenza nel movimento è diventato **In corso**, lo stato di assegnazione passerà da **Attivo** a **Completato**.  
* Se l'assistenza non è iniziata quando l'assegnazione aveva stato **Attivo**, lo stato di assegnazione passerà da **Attivo** ad **Annullato**.  
  
Lo stato di riparazione dell'articolo in assistenza nel movimento di assegnazione viene aggiornato nello stesso modo in cui è stata annullata l'assegnazione:  
  
* Se lo stato di riparazione è **Iniziale**, passerà a **Demandato** (l'assistenza non è ancora iniziata);  
* Se lo stato di riparazione è **In corso**, passerà a **Parzialmente assistito** (parte dell'assistenza è conclusa).  
  
Viene creato un nuovo movimento di assegnazione con stato **Attivo** contenente la nuova risorsa.  
  
## Riassegnazione di un articolo in assistenza  
Durante la riassegnazione di un articolo in assistenza in un movimento di assegnazione con stato **Riassegnazione necessaria**, il movimento di assegnazione viene aggiornato come segue:  
  
* Se l'assistenza è iniziata quando l'assegnazione aveva stato **Attivo**, ovvero se lo stato di riparazione dell'articolo in assistenza nel movimento è diventato **In corso**, lo stato di assegnazione passerà da **Riassegnazione necessaria** a **Completato**.  
* Se l'assistenza non è iniziata quando l'assegnazione aveva stato **Attivo**, lo stato di assegnazione passerà da **Riassegnazione necessaria** ad **Annullato**.  
  
Viene creato un nuovo movimento di assegnazione con stato **Attivo** contenente la nuova risorsa.  
  
## Vedi anche  
[Impostare l'assegnazione delle risorse](service-how-setup-resource-allocation.md)  
[Assegnare risorse](service-how-to-allocate-resources.md)  



[!INCLUDE[footer-include](includes/footer-banner.md)]