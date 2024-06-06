---
title: Messaggio di errore "La data di invio non rientra nel tuo intervallo di date di invio consentite"
description: Risolvere l'errore dietro al messaggio "La data di registrazione non rientra nel tuo intervallo di date di registrazione consentite" quando si esegue il lavoro batch Regolare i costi - Voci voce.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 09/17/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# <a name="error-message-posting-date-is-not-within-your-range-of-allowed-posting-dates"></a>Messaggio di errore: "La data di invio non rientra nel tuo range di date di invio consentite..."

Quando si usa il lavoro batch **Rettifica costo movimenti articoli** si può incorrere nel seguente messaggio di errore:

**La data di invio non rientra nel tuo range di date di invio consentite**

Questo messaggio di errore indica che l'utente non è autorizzato a pubblicare voci per la data in questione, e questo può essere rimediato cambiando la configurazione dell'utente.

## <a name="change-the-user-setup"></a>Cambiare l'impostazione dell'utente

|ID utente  |Consenti registraz. da  | Consenti registrazioni fino a  |
|---------|---------|--------|
|EUROPA  |  2020-09-11      |2020-09-30      |

L'utente in questo caso ha un intervallo di date di registrazione consentito dall'11 settembre al 30 settembre e quindi non è autorizzato a registrare la registrazione del valore di aggiustamento con data di registrazione 10 settembre.  

### <a name="overview-of-the-posting-date-setup"></a>Panoramica della configurazione della data di registrazione coinvolta

#### <a name="inventory-periods"></a>Periodi di inventario

|Data fine  |Name  |Chiuso  |
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

#### <a name="general-ledger-setup"></a>Setup contabilità generale

|Campo|Valore|
|---------|---------|
|Consenti registraz. da:  |  2020-09-10      |
|Consenti registrazioni fino a:    |  2020-09-30      |
|Registra tempi:       |         |
|Formato indirizzo locale:|   CAP      |  

#### <a name="user-setup"></a>Impostazione dell'utente

|ID utente  |Consenti registraz. da  | Consenti registrazioni fino a  |
|---------|---------|--------|
|USERNAME |  2020-09-10      |2020-09-30      |

Assegnando un intervallo di date di registrazione più ampio, come in Inventory Period o Setup contabilità generale, è possibile evitare il conflitto che causa il messaggio di errore. Il movimento di valorizzazione della rettifica con data di registrazione 10 settembre verrà registrato correttamente con questo setup.
  
## <a name="see-also"></a>Vedere anche

[Dettagli del design: Data di registrazione del valore di aggiustamento](design-details-inventory-adjustment-value-entry-posting-date.md)  
[Dettagli di progettazione: Costing di magazzino](design-details-inventory-costing.md)  
[Dettagli di progettazione: Collegamento articoli](design-details-item-application.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
