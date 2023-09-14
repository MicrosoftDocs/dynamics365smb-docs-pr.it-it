---
title: Stato ordine assistenza e stato riparazione
description: Lo stato dell'ordine assistenza corrisponde allo stato di riparazione degli articoli in assistenza nell'ordine assistenza.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: bholtorf
---
# Stato ordine assistenza e stato riparazione

Il campo **Stato** nella pagina **Ordine assistenza** e lo stato di riparazione dell'ordine assistenza, rappresentato dal campo **Codice stato riparazione** nella pagina **Ordine assistenza**, sono correlati in Gestione assistenza. Lo stato dell'ordine assistenza corrisponde allo stato di riparazione degli articoli in assistenza nell'ordine assistenza.  

> [!NOTE]  
> I due campi relativi allo stato non sono correlati al campo **Stato rilascio** nella testata dell'ordine assistenza, che determina la gestione della warehouse degli articoli in assistenza.  

Ogni volta che si modifica lo stato di riparazione di un articolo in assistenza in un ordine assistenza, lo stato dell'ordine viene aggiornato. Affinché lo stato visualizzato corrisponda allo stato generale di riparazione dei singoli articoli in assistenza, occorre specificare quanto segue:  

* lo stato dell'ordine assistenza a cui è collegata ogni stato di riparazione;  
* il livello di priorità di ogni opzione dell'ordine assistenza.  

Quando un'offerta di assistenza viene convertita in ordine assistenza, lo stato di riparazione di ogni articolo in assistenza viene convertito in **Iniziale** nell'ordine, mentre lo stato dell'ordine assistenza diventa **Non iniziato**.  

> [!NOTE]
> Prima di poter creare ordini assistenza, è necessario impostare gli stati di riparazione e le priorità dello stato di assistenza. Per ulteriori informazioni, vedere [Impostare gli stati per gli ordini di assistenza e le riparazioni](service-order-repair-status.md).

## Indicazione dello stato dell'ordine assistenza per lo stato di riparazione

Ogni stato di riparazione è collegato a un particolare stato dell'ordine assistenza. Le opzioni per lo stato dell'ordine assistenza sono le seguenti:

* **In sospeso**
* **In corso**
* **In sospeso**
* **Completato**

Le opzioni dello stato di riparazione sono:

* **Iniziale**
* **In corso**
* **Demandato**
* **Parzialmente assistito**
* **Offerta completata**
* **In attesa del cliente**
* **Pezzo di ricambio ordinato**
* **Pezzo di ricambio ricevuto**
* **Completato**  

### In sospeso

Lo stato dell'ordine assistenza **Non iniziato** indica che l'assistenza può iniziare o continuare in qualsiasi momento. Le opzioni dello stato di riparazione **Iniziale**, **Demandato**, **Parzialmente assistito** e **Pezzo di ricambio ricevuto** possono quindi essere collegate a questo stato dell'ordine assistenza.  

### In Corso

Lo stato dell'ordine assistenza **In corso** indica che l'assistenza è in atto. Le opzioni dello stato di riparazione **In corso** e **Pezzo di ricambio ordinato** possono quindi essere collegate a questo stato dell'ordine assistenza. Se lo stato **Pezzo di ricambio ordinato** viene collegato allo stato dell'ordine assistenza **In corso**, a questo stato occorre collegare anche lo stato **Pezzo di ricambio ricevuto**.  

### Fermo

Lo stato dell'ordine assistenza **In sospeso** indica che l'assistenza è temporaneamente interrotta perché si sta aspettando una risposta dal cliente o delle parti di ricambio per iniziare l'assistenza. Le opzioni dello stato di riparazione **Offerta completata**, **Pezzo di ricambio ordinato** e **In attesa del cliente** possono essere collegate a questo stato dell'ordine assistenza.  

### Completato

Lo stato dell'ordine assistenza **Completato** indica che l'assistenza è stata completata. Lo stato di riparazione **Completato** viene quindi collegato a questo stato.  

## Assegnazione di priorità allo stato dell'ordine assistenza

Quando lo stato di riparazione di un articolo in assistenza viene modificato, vengono individuate le opzioni di stato dell'ordine assistenza collegate alle diverse opzioni dello stato di riparazione di tutti gli articoli in assistenza nell'ordine. Se gli articoli in assistenza sono collegati a due o più opzioni di stato dell'ordine assistenza, viene selezionata l'opzione relativa allo stato dell'ordine con la priorità più alta.  

Occorre decidere quale stato contiene le informazioni più importanti per assegnargli quindi la priorità più alta, e così via.  

Quindi, quando si crea un nuovo ordine assistenza e si aggiungono articoli in assistenza, il campo **Priorità** nell'intestazione dell'ordine assistenza viene aggiornato in base alle priorità negli articoli in assistenza.  

### Esempio

Una tipica assegnazione del livello di priorità potrebbe essere:  

* In Corso - Alta  
* Non iniziato - Medio alta  
* In sospeso - Medio bassa  
* Completato - Bassa  

Se ad esempio un articolo in assistenza ha lo stato di riparazione **Iniziale**, collegato allo stato dell'ordine assistenza **Non iniziato**, un altro è **In corso**, collegato allo stato **In corso** e a un terzo corrisponde lo stato **Pezzo di ricambio ordinato**, collegato allo stato **In sospeso**, lo stato che ne risulterà sarà **In corso**, in quanto ha la priorità più alta.  

## Vedi anche

[Impostare gli stati per gli ordini di assistenza e le riparazioni](service-order-repair-status.md)  
[Impostazione della gestione assistenza](service-setup-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]