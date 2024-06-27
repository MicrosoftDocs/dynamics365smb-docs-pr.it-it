---
title: Messaggio di errore "La data di invio non rientra nel tuo intervallo di date di invio consentite"
description: Risolvere l'errore dietro al messaggio "La data di registrazione non rientra nel tuo intervallo di date di registrazione consentite" quando si esegue il lavoro batch Regolare i costi - Voci voce.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: null
ms.date: 05/24/2024
ms.service: dynamics-365-business-central
---

# Messaggio di errore: "La data di invio non rientra nel tuo range di date di invio consentite..."

Quando si usa il processo batch **Rettifica costo movimenti articoli** si potrebbe incorrere nel seguente messaggio di errore:

**La data di invio non rientra nel tuo range di date di invio consentite**

Questo messaggio indica che non sei autorizzato a pubblicare movimenti per la data inserita. Puoi aggirare questo problema modificando la configurazione dell'utente.

## Cambiare l'impostazione dell'utente  

|ID utente  |Consenti registrazione da  | Consenti registrazione in  |
|---------|---------|--------|
|EUROPA  |  2020-09-11      |2020-09-30      |

In questo caso, puoi registrare nell'intervallo di date compreso tra l'11 settembre e il 30 settembre. Tuttavia, non è consentito registrare il movimento del valore di rettifica con data di registrazione il 10 settembre.  

### Panoramica della configurazione della data di registrazione

#### Periodi magazzino

|Data di fine  |Nome  |Chiuso  |
|---------|---------|---------|
|2020-01-31     |2020 gennaio      |  Sì    |
|2020-02-28     |Febbraio 2020     |  Sì    |
|2020-03-31     |Marzo 2020        |  Sì    |
|2020-04-30     |Aprile 2020        |  Sì    |
|2020-05-31     |Maggio 2020        |  Sì    |
|2020-06-30     |Giugno 2020       |  Sì    |
|2020-07-31     |Luglio 2020        |   Sì   |
|2020-08-31     |Agosto 2020     |   Sì   |
|2020-09-30     |Settembre 2020  |         |
|2020-10-31     |Ottobre 2020    |         |
|2020-11-30     |Novembre 2020   |         |
|2020-12-31     |Dicembre 2020   |         |  

#### Setup contabilità generale

|Campo|Valore|
|---------|---------|
|Consenti registraz. da:  |  2020-09-10      |
|Consenti registrazioni fino a:    |  2020-09-30      |
|Registra tempi:       |         |
|Formato indirizzo locale:|   CAP      |  

#### Impostazione dell'utente

|ID utente  |Consenti registraz. da  | Consenti registrazione in  |
|---------|---------|--------|
|USERNAME |  2020-09-10      |2020-09-30      |

Assegnando un intervallo di date più ampio dove consenti la registrazione nelle pagine **Periodo magazzino** o **Setup contabilità generale**, puoi evitare il conflitto che causa il messaggio di errore. Ad esempio, l'intervallo più ampio ti consente di registrare il movimento del valore di rettifica con data di registrazione il 10 settembre.
  
## Vedere anche  

[Dettagli di progettazione: data di registrazione del movimento di valorizzazione della rettifica](design-details-inventory-adjustment-value-entry-posting-date.md)  
[Dettagli di progettazione: Costing di magazzino](design-details-inventory-costing.md)  
[Dettagli di progettazione: Collegamento articoli](design-details-item-application.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
