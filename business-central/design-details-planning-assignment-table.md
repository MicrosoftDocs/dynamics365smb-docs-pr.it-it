---
title: Dettagli di progettazione - Tabella Compiti di pianificazione
description: Questo argomento fornisce informazioni su cosa succede quando una modifica nei modelli di domanda o offerta richiede il calcolo della modalità di pianificazione di un articolo.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/15/2021
ms.author: edupont
---
# <a name="design-details-planning-assignment-table"></a>Dettagli di progettazione: Tabella Assegnazione pianificazione
Tutti gli articoli devono essere pianificati, tuttavia, non esiste motivo per calcolare un piano per un articolo a meno che non ci sia stato una modifica nella domanda o nel modello di approvvigionamento dall'ultima volta in cui è stato calcolato un piano.  

Se l'utente ha immesso un nuovo ordine di vendita o ne ha cambiato uno esistente, esiste motivo per ricalcolare il piano. Altri motivi includono una modifica nella previsione o la scorta di sicurezza desiderata. Modificare una distinta base aggiungendo o rimuovendo un componente che molto probabilmente indicherebbe una modifica, ma solo per l'articolo del componente.  

Per più ubicazioni, l'assegnazione avviene a livello di articolo per ogni combinazione di ubicazione. Se, ad esempio, un ordine di vendita è stato creato solo in un'ubicazione, l'applicazione assegnerà l'articolo a tale specifica ubicazione per la pianificazione.  

Il motivo per selezionare gli articoli per la pianificazione è una questione di prestazioni del sistema. Se non viene apportata alcuna modifica nel modello domanda-approvvigionamento di un articolo, il sistema di pianificazione non suggerirà alcuna azione da intraprendere. Senza l'assegnazione di pianificazione, il sistema deve eseguire i calcoli per tutti gli articoli per determinare cosa pianificare e cosa sfrutta maggiormente le risorse di sistema.  

Nella tabella **Pianificazione assegnazione** vengono monitorati gli eventi di domanda e approvvigionamento e assegnati gli articoli appropriati per la pianificazione. I seguenti eventi vengono monitorati:  

* Un nuovo ordine di vendita, previsione, componente, ordine acquisto, ordine di produzione, ordine di assemblaggio o ordine di trasferimento.  
* Modifica di un elemento, quantità, ubicazione, variante o data in un nuovo ordine di vendita, previsione, componente, ordine acquisto, ordine di produzione, ordine di assemblaggio o ordine di trasferimento.  
* Annullamento di un nuovo ordine di vendita, previsione, componente, ordine acquisto, ordine di produzione, ordine di assemblaggio o ordine di trasferimento.  
* Consumo di articoli diversi da quelli pianificati.  
* Output di articoli diversi da quelli pianificati.  
* Modifiche non pianificate in magazzino.  

Per questi spostamenti di domanda-approvvigionamento, il sistema di tracciabilità ordine e di messaggistica di azioni gestisce la tabella Compiti di pianificazione e stabilisce un motivo di pianificazione come messaggio di azione.  

Le seguenti modifiche nell'anagrafica possono causare uno sbilanciamento nella pianificazione:  

* Modifica dello stato in Certificato nella testata della DB di produzione (per tutti gli articoli che utilizzano tale testata).  
* Riga eliminata (articolo figlio).  
* Modifica dello stato in Certificato nella testata ciclo (per tutti gli articoli che utilizzano tale ciclo).  
* Le modifiche ai seguenti campi della scheda articolo.  
* Scorta di sicurezza o Lead time di sicurezza.  
* Calcolo lead time.  
* Punto riordino.  
* Nr. DB produzione (e tutti i figli del riferimento alla DB obsoleta).  
* Nr. ciclo  
* Metodo di riordino.  

In questi casi, una nuova funzione, gestione delle assegnazioni della pianificazione, gestisce la tabella e determina il motivo della pianificazione come Saldo periodo.  

Le seguenti modifiche non causano un'assegnazione di pianificazione:  

* Calendari  
* Altri parametri di pianificazione nella scheda articolo  

Nel calcolo di un MPS o un MRP si applicano le seguenti restrizioni:  

* MPS: il sistema di pianificazione controlla che l'articolo includa una previsione di domanda o un ordine di vendita. In caso contrario, l'articolo non viene incluso nel piano.  
* MRP: se il sistema di pianificazione rileva che l'articolo sta per essere rifornito da una riga di pianificazione MPS o da un ordine di approvvigionamento MPS, l'articolo verrà escluso dalla pianificazione. Tuttavia, è inclusa qualsiasi domanda dai componenti pertinenti.  

## <a name="see-also"></a>Vedi anche
[Dettagli di progettazione: Bilanciamento domanda e approvvigionamento](design-details-balancing-demand-and-supply.md)   
[Dettagli di progettazione: Gestione dei metodi di riordino](design-details-handling-reordering-policies.md)   
[Dettagli di progettazione: Trasferimenti nella pianificazione](design-details-transfers-in-planning.md)   
[Dettagli di progettazione: Parametri di pianificazione](design-details-planning-parameters.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
