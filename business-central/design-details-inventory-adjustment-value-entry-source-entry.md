---
title: Data di registrazione nella registrazione del valore di aggiustamento rispetto alla registrazione di origine
description: Scopri di più sullo scenario "Data di registrazione sull'entrata del valore di aggiustamento rispetto alla data di registrazione sull'entrata che causa l'aggiustamento come la rivalutazione o l'addebito dell'articolo" quando si esegue il lavoro batch Rettifica costo movimenti articoli.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/17/2021
ms.author: edupont
---

# <a name="posting-date-on-adjustment-value-entry-compared-to-the-source-entry" />Data di registrazione nella registrazione del valore di aggiustamento rispetto alla registrazione di origine

Questo articolo confronta la data di registrazione sulla registrazione del valore di aggiustamento con la data di registrazione sulla registrazione che causa l'esecuzione del lavoro batch Rettifica costo movimenti articoli, in particolare uno scenario di rivalutazione e uno scenario di addebito dell'articolo.

Il lavoro batch **Rettifica costo movimenti articoli** elaborerà i vostri dati a seconda del vostro scenario e della configurazione di [!INCLUDE[prod_short](includes/prod_short.md)]. In questa sezione, descriviamo due processi separati, e per ognuno mostriamo il tipo di impatto che il lavoro batch Rettifica costo movimenti articoli ha sui dati.

## <a name="revaluation-scenario" />Scenario di rivalutazione

### <a name="prerequisites" />Prerequisiti

Inserite i seguenti valori:

**Impostazione dell'inventario**:  

- Registrazione automatica dei costi = Sì  

- Adeguamento automatico dei costi = Sempre  

- Calcolo del costo medio. Tipo = Articolo  

- Costo medio periodo = Giorno  

**Impostazione della contabilità generale**:  

- Consenti registraz. da = 1° gennaio 2021  

- Permettere di inviare a = Vuoto  

**Impostazione dell'utente**:  

- Consenti registraz. da = 1° dicembre 2020  

- Permettere di inviare a = Vuoto  

### <a name="to-test-the-scenario" />Per verificare lo scenario:

Testate questo scenario eseguendo i seguenti passi.

1. Creare un **elemento** chiamato TEST con i seguenti valori:  

     - Unità di misura base = PZ  

     - Metodo di costing = Media  

     - Selezionare categorie di registrazione facoltative.  

2. Aprire un **Giornale delle voci**, poi creare una nuova voce e inserire una riga come segue:  

     - Data di registrazione = 15 dicembre 2020  

     - Articolo = TEST  

     - Tipo movimento = Acquisto  

     - Quantità = 100  

     - Importo unitario = 10  

3. Aprire un **Giornale delle voci**, poi creare una nuova voce e inserire una riga come segue:  

     - Data = 20 dicembre 2020  

     - Articolo = TEST  

     - Tipo movimento = Rettifica negativa  

     - Quantità = 2  

4. Aprire un **Giornale delle voci**, poi creare una nuova voce e inserire una riga come segue:  

     - Data = 15 gennaio 2021  

     - Articolo = TEST  

     - Tipo di voce = Aggiustamento negativo  

     - Quantità = 3  

5. Aprire un **Giornale di rivalutazione delle voci**, poi creare una nuova voce e inserire una riga come segue:  

     - Articolo = TEST  

     - Collega-a movimento = selezionare il movimento di tipo Acquisto registrato nel passaggio 2. La data di registrazione della rivalutazione sarà la stessa del movimento che rettifica.  

     - Costo unitario (rivalutato) = 40  

I seguenti **movimenti contabili articoli** e **movimenti di valorizzazione** sono stati registrati:  

**Mov. Contabile Articoli - acquisto**  

|Numero movimento  |Nr. Articolo  |Data di registrazione  |Tipo movimento  |Nr. documento  |Quantità  |Importo costo (effettivo)  |Quantità residua  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|317     |TEST         |2020-12-15         |Acquisti         |T00001         |100         |4000         |95        |

**Mov. valorizzazione**  

|Numero movimento  |Nr. Articolo  |Data di registrazione  |Nr. movimento cont. articolo  |Tipo mov. articolo  |Tipo movimento  |Nr. documento  |Quantità num. mov. contabili art.  |Importo costo (effettivo)  |Costo registrato in C/G  |Rettifica  |Movimento collegato  |Codice origine  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|376     |TEST|   2020-12-15    |317         |Acquisti         |Costo diretto         |T00001         |100         |1 000,00          |1 000,00    |No         |0         |ITEMNL         |
|379     |TEST   |**12-2020-15**    |317         |Acquisti         |Rivalutazione         |T04002         |0         |3 000,00         |3 000,00         |No         |0         |REVALINL         |

**Mov. Contabile Articoli - rettifica negativa, passaggio 3**  

|Nr. movimento  |Nr. Articolo  |Data di registrazione  |Tipo movimento  |Nr. documento  |Quantità  |Importo costo (effettivo)  |Quantità residua  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|318     |TEST      |2020-12-20   |Rettifica negativa  |T00002         |-2         |-80         | 0        |

**Mov. valorizzazione**  

|Numero movimento  |Nr. Articolo  |Data di registrazione  |Nr. movimento cont. articolo  |Tipo mov. articolo  |Tipo movimento  |Nr. documento  |Quantità num. mov. contabili art.  |Importo costo (effettivo)  |Costo registrato in C/G  |Rettifica  |Movimento collegato  |Codice origine  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|377     |TEST|   2020-12-20    |318         |Rettifica negativa         |Costo diretto         |T00002         |-2         |-20          |-20    |No         |0         |ITEMNL         |
|380     |TEST   |**01-2021-01**    |318         |Rettifica negativa         |Costo diretto         |T04002         |0         |-60         |-60         |Sì         |377         |INVTADAMT         |

**Mov. Contabile Articoli - rettifica negativa, passaggio 4**  

|Nr. movimento  |Nr. Articolo  |Data di registrazione  |Tipo movimento  |Nr. documento  |Quantità  |Importo costo (effettivo)  |Quantità residua  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|319     |TEST      |2021-01-15   |Rettifica negativa  |T00003         |-3         |-120         | 0        |

**Mov. valorizzazione**  

|Numero movimento  |Nr. Articolo  |Data di registrazione  |Nr. movimento cont. articolo  |Tipo mov. articolo  |Tipo movimento  |Nr. documento  |Quantità num. mov. contabili art.  |Importo costo (effettivo)  |Costo registrato in C/G  |Rettifica  |Movimento collegato  |Codice origine  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|378     |TEST|   2021-01-15    |319         |Rettifica negativa         |Costo diretto         |T00003         |-3         |-30          |-30    |No         |0         |ITEMNL         |
|381     |TEST   |**01-2021-15**    |319         |Rettifica negativa         |Costo diretto         |T04003         |0         |-90         |-90         |Sì         |378         |INVTADAMT         |

Il lavoro batch **Rettifica costo movimenti articoli** ha riconosciuto un cambiamento nel costo e ha regolato gli aggiustamenti negativi.  

**Analisi delle date di registrazione dei movimenti di valorizzazione delle rettifiche creati:** la data di registrazione consentita più vicina a cui il processo batch Rettifica costo - Movimenti articoli deve fare riferimento è il 1° gennaio 2021 come indicato nel setup di contabilità generale.  

**Rettifica negativa nel passaggio 3:** la data di registrazione assegnata è il 1° gennaio, fornita dal setup di contabilità generale. La data di registrazione della registrazione del valore nell'ambito dell'adeguamento è il 20 dicembre 2020. Secondo il Setup contabilità generale, la data non è all'interno dell'intervallo di date di registrazione consentito. Di conseguenza, la data di registrazione indicata nel campo Consenti registraz. da nel setup di contabilità generale è assegnata al movimento di valorizzazione della rettifica.  

**Rettifica negativa nel passaggio 4:** la data di registrazione assegnata è il 15 gennaio. La data di registrazione del movimento di valorizzazione in relazione alla rettifica è il 15 gennaio, che rientra nell'intervallo di date di registrazione consentite secondo il setup di contabilità generale.  

La rettifica apportata per la rettifica negativa nel passaggio 3 è oggetto di discussione. La data di registrazione favorevole del movimento di valorizzazione della rettifica sarebbe stata il 20 dicembre o almeno in dicembre in quanto la rivalutazione che causa la modifica in COGS è stata registrata in dicembre.  

Per ottenere l'aggiustamento in dicembre dell'aggiustamento negativo al passo 3, il campo Setup contabilità generale, Consenti registrazione da, deve indicare una data in dicembre.  

### <a name="conclusion" />Conclusione

Con l'esperienza acquisita in questo scenario, quando si considera la configurazione più adatta per un intervallo di date di invio consentito per un'azienda, si potrebbe voler considerare quanto segue. Finché si permette che i cambiamenti nel valore dell'inventario siano registrati in un periodo, come dicembre in questo caso, la configurazione che l'azienda usa per gli intervalli di date di registrazione permessi dovrebbe essere allineata con questa decisione. Il campo Consenti registraz. da nel setup di contabilità generale, indicante il 1° dicembre, permetterebbe il trasferimento della rivalutazione effettuata a dicembre ai movimenti in uscita interessati nello stesso periodo.  

Per i gruppi di utenti a cui non è consentito registrare in dicembre ma a gennaio, condizione probabilmente determinata dal setup di contabilità generale in questo scenario, si deve utilizzare il setup utente.  

## <a name="item-charge-scenario" />Scenario di addebito dell'articolo

### <a name="prerequisites-1" />Prerequisiti

Inserite i seguenti valori:

**Impostazione dell'inventario**:  

- Registrazione automatica dei costi = Sì  

- Adeguamento automatico dei costi = Sempre  

- Calcolo del costo medio. Tipo = Articolo  

- Periodo di costo medio = giorno  

**Impostazione della contabilità generale**:  

- Consenti registraz. da = 1° dicembre 2020  

- Permettere di inviare a = Vuoto  

**Impostazione dell'utente**:  

- Consentire l'invio da = 1 dicembre 2020.  

- Consentire la pubblicazione di = vuoto  

### <a name="to-test-the-scenario-1" />Per testare lo scenario

Testate questo scenario eseguendo i seguenti passi:

1.  Creare un addebito **Elemento** con i seguenti valori:  

     - Unità di misura di base = PCS  

     - Metodo di calcolo dei costi = Media  

     - Seleziona i gruppi di pubblicazione opzionali.  

2.  Creare un nuovo **ordine di acquisto** con i seguenti valori:  

     - Acquistare da - Nr. for.: 10000  

     - Data di invio = 15 dicembre 2020

     - Nr. fattura fornitore: 1234  

     Nella linea dell'ordine di acquisto selezionare i seguenti valori:  

     - Articolo = ADDEBITO  

     - Quantità = 1  

     - Costo unitario diretto = 100  

     Per completare il passo, Pubblica il documento come Ricevuto e Fatturato.  

3.  Creare un nuovo **ordine di vendita** con i seguenti valori:  

     - Vendere a - Nr. cliente: 10000  

     - Data di registrazione = 16 dicembre 2020  

     Sulla linea dell'ordine di vendita:  

     - Articolo = ADDEBITO  

     - Quantità = 1  

     - Prezzo unitario = 135  

     Per completare il passo, Pubblica il documento come Ricevuto e Fatturato.  

4.  Inserire i valori per la pagina **Setup contabilità generale** :  

     - Permettere il distacco da = 1 gennaio 2021  

    -  Consenti registrazioni fino a = vuoto  

5.  Creare un nuovo **ordine di acquisto** con i seguenti valori:  

     - Acquista dal venditore No: 10000  

     - Data di registrazione = 2 gennaio 2021  

     - Nr. fattura fornitore: 2345  

     Sulla linea dell'ordine di acquisto:  

     - Addebito articolo = COM-SPEDIZ  

     - Quantità = 1  

     - Costo unitario diretto = 3  

     - Assegnare il costo dell'articolo alla ricevuta d'acquisto dal passo 2.  

     Per completare il passo, Pubblica il documento come Ricevuto e Fatturato.  


**Stato Mov. Contabile Articoli dell'acquisto passaggio 2**:  
  
|Numero movimento  |Nr. Articolo  |Data di registrazione  |Tipo movimento  |Nr. documento  |Quantità  |Importo costo (effettivo)  |Quantità residua  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|324     |ADDEBITO         |2020-12-15         |Acquisti         |107030         |1         |105         |0        |

**Mov. valorizzazione**  

|Numero movimento |Nr. Articolo  |Data di registrazione  |Nr. movimento cont. articolo  |Tipo mov. articolo  |Tipo movimento  |Nr. documento  | Nr. addebito articolo    |  Quantità mov. contabili art.   |Importo costo (effettivo)     |Costo registrato in C/G |Rettifica |Movimento Collegato |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|397      |ADDEBITO|   2020-12-15    |324         |Acquisti         |Costo diretto         |108029         |         |1          |100    |100         |NO         |0         |
|399      |ADDEBITO   |2021-01-02    |324         |Acquisti         |Costo diretto         |108009         |JBFREIGHT         |0         |3         |3         |NO         |0         |

**Stato Mov. Contabile Articoli vendita**:  
  
|Nr. movimento  |Nr. Articolo  |Data di registrazione  |Tipo movimento  |Nr. documento  |Quantità  |Importo costo (effettivo)  |Quantità residua  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|325     |ADDEBITO         |2020-12-16         |Vendite         |102035         |-1         |-105         |0        |

**Mov. valorizzazione**  

|Numero movimento |Nr. Articolo  |Data di registrazione  |Nr. movimento cont. articolo  |Tipo mov. articolo  |Tipo movimento  |Nr. documento  | Nr. addebito articolo    |  Quantità mov. contabili art.   |Importo costo (effettivo)     |Costo registrato in C/G |Rettifica |Movimento Collegato |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|398      |ADDEBITO|   2020-12-16    |325         |Vendite         |Costo diretto         |109024         |         |-1          |-100    |-100         |NO         |0         |
|400      |ADDEBITO   |2021-01-01    |325         |Vendite         |Costo diretto         |109024         |         |0         |-3         |-3         |Sì         |398         |

6.  Il 3 gennaio, data di lavoro, arriva una fattura d'acquisto che contiene un costo aggiuntivo all'acquisto fatto nel passo 2. Questa fattura ha data di documento 30 dicembre, ed è quindi registrata con Posting Date 30 dicembre 2020.  

     Creare un nuovo **ordine di acquisto** con i seguenti valori:  

     - Acquista dal venditore No: 10000  

     - Data di registrazione = 30 dicembre 2020  

     - Nr. fattura fornitore: 3456  

     Nella linea dell'ordine di acquisto selezionare i seguenti valori:  

     - Costo dell'articolo = JB-FREIGHT  

     - Quantità = 1  

     - Costo unitario diretto = 2  

     Assegnare il costo dell'articolo alla ricevuta d'acquisto del passo 2  

     Per completare il passo, Pubblica il documento come Ricevuto e Fatturato.  


**Stato Mov. Contabile Articoli dell'acquisto**:  

|Numero movimento  |Nr. Articolo  |Data di registrazione  |Tipo movimento  |Nr. documento  |Quantità  |Importo costo (effettivo)  |Quantità residua  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|324     |ADDEBITO         |2020-12-15         |Acquisti         |107030         |1         |105         |0        |

**Mov. valorizzazione**  

|Nr. movimento |Nr. Articolo  |Data di registrazione  |Nr. movimento cont. articolo  |Tipo mov. articolo  |Tipo movimento  |Nr. documento  | Nr. addebito articolo    |  Quantità mov. contabili art.   |Importo costo (effettivo)     |Costo registrato in C/G |Rettifica |Movimento Collegato |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|397      |ADDEBITO   |2020-12-15    |324         |Acquisti         |Costo diretto         |108029         |            |1         |100    |100         |No         |0         |
|399      |ADDEBITO   |2021-01-02    |324         |Acquisti         |Costo diretto         |108030         |JBFREIGHT   |0         |3         |3         |No         |0         |
|401      |ADDEBITO   |**12-2020-30**    |324         |Acquisti         |Costo diretto         |108031         |JBFREIGHT   |0         |2         |2         |No         |0         |

**Stato Mov. Contabile Articoli vendita**:  
  
|Numero movimento  |Nr. Articolo  |Data di registrazione  |Tipo movimento  |Nr. documento  |Quantità  |Importo costo (effettivo)  |Quantità residua  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|325     |ADDEBITO         |2020-12-16         |Vendite         |102035         |-1         |-105         |0        |

**Mov. valorizzazione**  

|Nr. movimento |Nr. Articolo  |Data di registrazione  |Nr. movimento cont. articolo  |Tipo mov. articolo  |Tipo movimento  |Nr. documento  | Nr. addebito articolo    |  Quantità mov. contabili art.   |Importo costo (effettivo)     |Costo registrato in C/G |Rettifica |Movimento Collegato |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|398      |ADDEBITO   |2020-12-16        |325         |Vendite         |Costo diretto         |103024         |            |-1         |-100       |-100         |No         |0         |
|400      |ADDEBITO   |2021-01-01        |325         |Vendite         |Costo diretto         |103024         |            |0          |-3         |-3         |Sì         |398         |
|402      |ADDEBITO   |**01-2021-01**    |325         |Vendite         |Costo diretto         |103024         |            |0          |-2         |-2         |Sì         |398         |

Il report Valutazione magazzino viene stampato in data 31 dicembre 2020

![Contenuto del rapporto di valutazione dell'inventario.](media/helene/TechArticleAdjustcost13.png "Contenuto del report di valutazione magazzino")

**Riepilogo dello scenario:**  

Lo scenario descritto termina con un report Valutazione magazzino che indica Quantità = 0 quando Valore = 2. L'addebito articolo registrato nel passaggio 6 fa parte del valore Aumento di magazzino di dicembre mentre la riduzione di magazzino dello stesso periodo non è influenzata.  

La data 1° gennaio indicata nel campo Consenti registraz. da del setup di contabilità generale era ideale per il primo addebito articolo. I costi dell'aumento e della riduzione di magazzino sono stati registrati nello stesso periodo. Per il secondo addebito articolo tuttavia, il setup di contabilità generale posiziona la modifica in COGS nel periodo successivo.  

**Conclusione:**  

È una sfida ottenere il rapporto Valutazione dell'inventario per dimostrare Quantità = 0 mentre il Valore <> 0. In questo caso è anche più difficile esprimere le impostazioni ottimali, avendo fatture di acquisto che arrivano lo stesso giorno ma che si rivolgono a periodi diversi o addirittura ad anni fiscali. Passare a un nuovo anno fiscale di solito richiede una certa pianificazione e come parte di questo l'intuizione di regolare il processo di voci di costo, riconoscendo il COGS, deve essere considerato.  

Come alternativa in questo scenario si sarebbe potuto avere una data in dicembre di un paio di giorni in più nel campo Consenti registraz. da del setup di contabilità generale e differire la registrazione del primo addebito articolo per consentire il riconoscimento di tutti i costi relativi al periodo/anno fiscale per il periodo a cui appartengono inizialmente, quindi eseguire il processo batch Rettifica costo - Movimenti articoli e infine spostare la data di registrazione consentita al nuovo periodo\/anno fiscale. Si sarebbe quindi potuto registrare il primo addebito con la data 2 gennaio.  

## <a name="see-also" />Vedere anche

[Dettagli del design: Data di registrazione del valore di aggiustamento](design-details-inventory-adjustment-value-entry-posting-date.md)  
[Dettagli del design: Inventario dei costi](design-details-inventory-costing.md)  
[Dettagli del design: Applicazione dell'articolo](design-details-item-application.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
