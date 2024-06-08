---
title: Data di registrazione dei movimenti di valorizzazione
description: Informazioni su come il processo batch Rettifica costo - Movimenti articoli identifica e assegna una data di registrazione ai movimenti di valorizzazione che il processo batch crea.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 09/17/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Dettagli di progettazione: Data di registrazione del movimento di valorizzazione della rettifica

Questo articolo fornisce una guida per gli utenti della funzionalità Inventory Costing in [!INCLUDE[prod_short](includes/prod_short.md)], e in particolare per come il lavoro batch **Rettifica costo movimenti articoli** identifica e assegna una data di registrazione alle voci di valore che il lavoro batch sta per creare.

## Come vengono assegnate le date di distacco

Il processo batch **Rettifica costo - Movimenti articoli** assegna una data di registrazione al movimento valorizzazione da creare mediante la seguente procedura:  

1. Inizialmente la data di registrazione del movimento da creare è la stessa data del movimento che viene rettificato.  

2. La data di registrazione viene convalidata in base ai periodi di magazzino e/o al setup di contabilità generale.  

3. Assegnazione della data di registrazione; se la data di registrazione iniziale non rientra nell'intervallo di date di registrazione consentite, il processo batch assegnerà una data di registrazione consentita in base al periodo di magazzino o al setup di contabilità generale. Se i periodi di magazzino e le date di registrazione consentite nel setup di contabilità generale sono definiti, la data più lontana delle due verrà assegnata al movimento di valorizzazione della rettifica.  

Esaminiamo questo processo con un esempio pratico. Supponiamo di avere un movimento contabile articolo di vendita. L'articolo è stato spedito il 5 settembre 2020 ed è stato fatturato il giorno dopo.  

#### Mov. Contabile Articoli

|Nr. movimento  |Nr. Articolo  |Data di registrazione  |Tipo movimento  | Nr. documento |Cod. ubicazione  |Quantità  |Importo costo (effettivo)  |Quantità fatturata  |Quantità residua  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|319     |A         |2020-09-05     |  Vendite       |102033     |  Blu       | -1    |    -11     |-1     |    0     |

Di seguito sono riportate le voci di valore correlate:

- La**registrazione n. 379** rappresenta la spedizione e ha la stessa data di registrazione della registrazione del libro mastro della voce madre.  
- La**voce n. 381** rappresenta la fattura.  
- La**registrazione n. 391** è un aggiustamento della registrazione del valore di fatturazione (registrazione n. 381 di cui sopra).  

|Nr. movimento  |Nr. Articolo  |Data di registrazione  |Tipo mov. articolo  |Tipo movimento  |Nr. documento  |Nr. movimento cont. articolo  |Cod. ubicazione  |Quantità mov. contabili art.  |Quantità fatturata  |Importo costo (effettivo)  |Importo costo (previsto)  |Rettifica  |Movimento Collegato  |Codice origine  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|--------|---------|---------|---------|---------|
|379     |  A       |    2020-09-05     |    Vendite     | Costo diretto   | 102033        |319     | Blu        | -1       |0         |  0       |     -10   |No   |0    |Vendite          |
|381     |  A       |    2020-09-06     |    Vendite     | Costo diretto   | 103022        |319     | Blu        |  0       |-1        |-10       |    10     | No  |0      |       Vendite   |
|391     |  A       |    2020-09-10     |    Vendite     | Costo diretto   | 103022        |319     | Blu        |  0       |0         |-1        |    0     |Sì   |    181   | INVTADJMT   |

Per assegnare la data di registrazione per la **voce n. 391** sono stati applicati i seguenti passi:

1. Alla **registrazione del valore di aggiustamento** da creare **(registrazione n. 391**) viene assegnata la stessa **data di registrazione** della registrazione che aggiusta.

2. Il processo batch **Rettifica costo - Movimenti articoli** determina se la data di registrazione iniziale del movimento di valorizzazione della rettifica rientra nell'intervallo di date consentite basato sui periodi di magazzino e/o sul setup di contabilità generale.  

Esaminiamo la vendita menzionata in precedenza aggiungendo il setup dell'intervallo di date di registrazione consentite.  
  
#### Periodi di inventario

|Data fine  |Name  |Chiuso  |
|---------|---------|---------|
|2020-01-31     |2020 gennaio      |  Sì    |
|2020-02-28     |Febbraio 2020     |  Sì    |
|2020-03-31     |Marzo 2020        |  Sì    |
|2020-04-30     |Aprile 2020        |  Sì    |
|2020-05-31     |Maggio 2020        |  Sì    |
|2020-06-30     |Giugno 2020       |  Sì    |
|2020-07-31     |Luglio 2020        |  Sì    |
|2020-08-31     |Agosto 2020     |  Sì    |
|2020-09-30     |Settembre 2020  |         |
|2020-10-31     |Ottobre 2020    |         |
|2020-11-30     |Novembre 2020   |         |
|2020-12-31     |Dicembre 2020   |         |

La prima data di pubblicazione consentita è il primo giorno del primo periodo aperto, che è il 1° settembre 2020.  

#### Setup contabilità generale

|Campo|Valore  |
|---------|---------|
|Consenti registraz. da:  |  2020-09-10      |
|Consenti registrazioni fino a:    |  2020-09-30      |
|Registra tempi:       |         |
|Formato indirizzo locale:|   CAP      |  

La prima data di registrazione consentita è la data indicata nel campo **Allow Posting From**: 10 settembre 2020. Se sono definiti entrambi i periodi di inventario e le date di registrazione consentite in **Setup contabilità generale**, la data più recente delle due definirà l'intervallo di date di registrazione consentito.  

**Assegnazione di una data di distacco consentita**  

La data di registrazione assegnata iniziale era il 6 settembre come illustrato nel passaggio 1. Tuttavia, nel secondo passo il lavoro batch Rettifica costo movimenti articoli identifica che la prima data di registrazione consentita è il 10 settembre e quindi assegna il 10 settembre alla voce Adjustment Value Entry **(Entry No. 391**), sotto.  


|Nr. movimento  |Nr. Articolo  |Data di registrazione  |Tipo di voce del libro mastro  |Tipo movimento  |Nr. documento  |Nr. movimento cont. articolo  |Cod. ubicazione  |Quantità mov. contabili art.  |Quantità fatturata  |Importo costo (effettivo)  |Importo costo (previsto)  |Rettifica  |Movimento Collegato  |Codice origine  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|379     |  A       |    2020-09-05     |    Vendite     | Costo diretto   | 102033        |319     | Blu        | -1       |0         |  0       |     -10   |No   |0    |Vendite          |
|381     |  A       |    2020-09-06     |    Vendite     | Costo diretto   | 103022        |319     | Blu        |  0       |-1        |-10       |    10     | No  |0      |       Vendite   |
|391     |  A       |    **09-2020-10**     |    Vendite     | Costo diretto   | 103022        |319     | Blu        |  0       |0         |-1        |    0     |Sì   |    181   | INVTADJMT   |

## Problemi comuni con il lavoro batch "Regolare i costi - voci di articolo"

Ci sono due scenari che il team di supporto incontra abbastanza frequentemente da giustificare i propri articoli sulla risoluzione dei problemi.

### Messaggio di errore: "La data di invio non rientra nel tuo range di date di invio consentite..."

Se incontri questo errore, devi modificare le date per le quali l'utente è autorizzato a pubblicare voci. Per saperne di più, vedi [Messaggio di errore "Posting Date is not within your range of allowed posting dates"](design-details-inventory-adjustment-value-entry-allowed-posting-dates.md).

### Data di registrazione sulla registrazione del valore di aggiustamento rispetto alla data di registrazione sulla registrazione che causa l'aggiustamento, come la rivalutazione o l'addebito di una voce

Per saperne di più, vedere [Data di registrazione sulla registrazione del valore di aggiustamento rispetto alla registrazione di origine](design-details-inventory-adjustment-value-entry-source-entry.md).

## Vedere anche  

[Dettagli del design: Inventario dei costi](design-details-inventory-costing.md)  
[Dettagli del design: Applicazione dell'articolo](design-details-item-application.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
