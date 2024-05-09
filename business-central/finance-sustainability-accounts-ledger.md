---
title: Contabilità generale e grafico dei conti di sostenibilità
description: 'Scopri come gestire il grafico dei conti di sostenibilità, le categorie e le sottocategorie nonché i dettagli sui movimenti contabili di sostenibilità.'
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD, CoA, Chart, Account, Ledger'
ms.search.form: '6210, 6213, 6214, 6220'
ms.date: 04/02/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# Contabilità generale e grafico dei conti di sostenibilità 

## Grafico dei conti di sostenibilità  

Il **grafico dei conti di sostenibilità** (CoSA) costituisce l'elenco strutturato fondamentale utilizzato per registrare tutti i dati sulle emissioni. Funziona come un framework che classifica e organizza i conti di sostenibilità in base ai relativi attributi, come l’ambito o altri raggruppamenti. A ogni conto viene generalmente assegnato un codice o numero univoco per facilitarne la consultazione e il monitoraggio, seguendo la stessa struttura di un tradizionale **Piano dei conti** ma personalizzato specificamente per il monitoraggio dei dati e delle metriche relativi alla sostenibilità all’interno di un’organizzazione. 
 
Gli utenti possono aggiungere **Categorie di account** e **Sottocategorie** per definire il comportamento del sistema, selezionando le emissioni dedicate per monitoraggio, fattori di emissione, formule e configurazioni simili.  

>[!NOTE]
>Per acquisire familiarità con gli ambiti, sulla base degli standard di gas a effetto serra, esistono tre ambiti di emissione:  
>- **Emissioni di ambito 1**: includono le emissioni emesse dalla combustione mobile e stazionaria e da emissioni fuggitive involontarie. 
>- **Emissioni di ambito 2**: includono le emissioni indirette derivanti dalla generazione di energia acquistata da fornitori di servizi pubblici. 
>- **Emissioni di ambito 3**: includono un ampio spettro di emissioni, derivanti da beni e servizi acquistati e beni capitali, attività legate a combustibile ed energia, trasporti a monte e a valle, rifiuti generati, viaggi di lavoro e spostamenti dei dipendenti, ecc. 

Tramite il **Grafico dei conti di sostenibilità** è possibile eseguire operazioni come:  

-   Visualizzare i report che mostrano i movimenti e i saldi contabili di sostenibilità. 
-   Aprire la **Scheda conto di sostenibilità** per aggiungere o modificare le impostazioni.  
-   Visualizzare la categoria e la sottocategoria per quel conto.   
-   Visualizzare saldi separati per ciascuna delle emissioni per un singolo conto. 
-   Aggiungere una o più **Dimensioni** a ciascuno dei conti e impostare il filtro dimensioni. 
    
È possibile aggiungere, modificare o eliminare **Conti di sostenibilità**. Tuttavia, per evitare discrepanze, non è possibile eliminare un **Conto di sostenibilità** se sono presenti uno o più movimenti contabili associati al conto.  

### Aggiungere o cambiare conti  

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi 3.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Grafico dei conti di sostenibilità**, quindi seleziona il collegamento correlato. 
2. Nella pagina **Grafico dei conti di sostenibilità**, è possibile aprire ogni **Conto di sostenibilità** e quindi aggiungere o modificare le impostazioni. Passare sul campo con il mouse per visualizzare una breve descrizione. 

Per i conti di tipo **Totale** compilare il campo **Totale**. Per i conti di tipo **Totale Finale** questo campo viene compilato automaticamente tramite la funzione di indentazione. A tale proposito, dopo aver impostato tutti i conti, scegli l'azione **Imposta rientri grafico dei conti di sostenibilità**.  

>[!IMPORTANT]
>Se le definizioni per i conti **Totale Finale** sono state immesse nei campi **Totale** prima di eseguire la funzione di indentazione, sarà necessario inserirle nuovamente in seguito poiché questa funzione sovrascrive i valori in tutti i campi **Totale finale**.  

### Eliminare conti  

È possibile eliminare un **Conto di sostenibilità**. Tuttavia, prima di eliminarlo, devi assicurarti che siano presenti uno o più movimenti contabili associati al conto, poiché Business Central impedirà l'eliminazione di un **Conto di sostenibilità** in questa situazione.  

## Categorie di conti   

Gli utenti devono aggiungere la **Categoria conto di sostenibilità** a ciascuno dei **Conti di sostenibilità**, per definire come si comporta il sistema, selezionando ambiti di emissione, emissioni dedicate per il monitoraggio, formule e configurazioni simili.  

Per esaminare **Categorie conti di sostenibilità**, segui i passaggi: 

1.  Seleziona l'icona ![lampadina che apre la funzionalità Dimmi 3.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Categorie conti di sostenibilità**, quindi seleziona il collegamento correlato. 
2.  Nella pagina **Categorie conti di sostenibilità**, puoi modificare l'elenco esistente o creare una nuova categoria. Per creare una nuova categoria, seleziona l'azione **Nuova**.  
3.  Compilare i campi **Codice** e **Descrizione**.   
4.  Imposta il campo **Ambito di emissione**, scegliendo una delle opzioni di ambito.  
5.  Seleziona le emissioni di gas che desideri monitorare. Attualmente puoi utilizzare una delle opzioni: **CO2**, **CH4** o **N2O**. Puoi scegliere qualsiasi combinazione che desideri monitorare, ma devi avere almeno un'emissione per il monitoraggio.  
6.  Nel campo **Base di calcolo**, puoi scegliere una qualsiasi delle formule che desideri utilizzare, nel caso in cui non conosci la quantità esatta di emissioni. Qui puoi specificare la base di calcolo (formula) per il calcolo delle emissioni. Puoi scegliere una delle seguenti opzioni: **Combustibile/Elettricità**, **Distanza**, **Installazione** o **Personalizzata**. 
7.  Se scegli la formula **Personalizzata**, puoi configurare la descrizione personalizzata nel campo **Valore personalizzato**.  

>[!NOTE]
>Se questo insieme di formule offerte nel campo **Base di calcolo** non è sufficiente, puoi estendere questo campo e aggiungere più calcoli al sistema da utilizzare nelle **Registrazioni di sostenibilità**.  

Se usi la **Base di calcolo** (formule), c'è una spiegazione su come il sistema eseguirà il calcolo in base all'opzione scelta (**EF** è il **Fattore di emissione** che puoi configurare nella pagina **Sottocategoria conto di sostenibilità**): 

|  Tipo di emissioni  |  Base di calcolo  |  Formula         | Commento      |
|------------|--------------|------------------------------|---------------------------------|
| **AMBITO 1**  |
| Combustione stazionaria | Combustibile/Elettricità | Emissioni = Combustibile * EF | _ovvero Combustibile = Quantità di combustibile speso per caldaie, riscaldatori, ossidatori termici..._ |
| Combustione mobile | Combustibile/Elettricità | Emissioni = Combustibile * EF | _ovvero Combustibile = Quantità di combustibile speso per veicoli stradali o non stradali, ferroviari..._ |
|  |  |  Emissioni = Distanza * EF | _ovvero Distanza = Chilometraggio di veicoli stradali o non stradali, ferroviari..._ |
| Emissioni fuggitive | Installazione | Emissione = Moltiplicatore di installazione * Importo personalizzato / 100 * Fattore temporale | _ovvero Importo personalizzato = Perdite di assemblaggio, tasso di perdita annuale..._ |
| **AMBITO 2**  |
| Fornitori di servizi | Combustibile/Elettricità | Emissioni = Elettricità * EF | _ovvero Combustibile/elettricità = Quantità di elettricità, quantità di vapore, unità di riscaldamento..._ |
|  | Personalizzato | Emissione = Importo personalizzato * EF | _ovvero Importo personalizzato = Unità termica, Tonnellata-ora..._ |
| **AMBITO 3**  |
| Beni e servizi acquistati e beni capitali | Personalizzato | Emissione = Importo personalizzato * EF | _ovvero Importo personalizzato = Costo (GL)..._ |
| Trasporto e distribuzione upstream | Distanza | Emissioni = Distanza * EF |  |
|  | Distanza | Emissioni = Distanza * Moltiplicatore * EF | _Moltiplicatore = Tonnellate di carico_ |
| Trasporto e distribuzione downstream | Distanza | Emissioni = Distanza * EF |  |
|  | Distanza | Emissioni = Distanza * Moltiplicatore * EF | _Moltiplicatore = Tonnellate di carico_ |
| Rifiuti generati nelle operazioni e nel trattamento di fine vita dei prodotti venduti | Personalizzato | Emissione = Importo personalizzato * EF | _ovvero Importo personalizzato = Rifiuti..._ |
| Viaggi d'affari e spostamento dei dipendenti | Distanza | Emissioni = Distanza * EF | _ovvero Distanza = Chilometraggio di auto aziendale usata, auto a noleggio, treno, volo..._ |
|  | Personalizzato | Emissione = Importo personalizzato * EF | _ovvero Importo personalizzato = Soggiorni in hotel..._ |
|  | Combustibile/Elettricità | Emissioni = Combustibile * EF | _ovvero Combustibile = Quantità di combustibile spesa nell'auto aziendale, nell'auto a noleggio..._ |

## Sottocategorie di conti  

Gli utenti devono aggiungere la **Sottocategoria conto di sostenibilità** a ciascuno dei **Conti di sostenibilità** per definire i fattori di emissione che verranno utilizzati nelle formule, ma si basa sulla scelta del monitoraggio delle emissioni nella **Categoria conto di sostenibilità**.  

Per esaminare le **Sottocategorie conti di sostenibilità**, procedi come segue:  

1.  Seleziona l'icona ![lampadina che apre la funzionalità Dimmi 3.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Sottocategorie conti di sostenibilità**, quindi seleziona il collegamento correlato. 
2.  Nella pagina **Sottocategorie conti di sostenibilità**, puoi modificare l'elenco esistente o creare una nuova categoria. Per creare una nuova categoria, seleziona l'azione **Nuova**.  
3.  Compilare i campi **Codice** e **Descrizione**.   
4.  In base alle emissioni di gas che desideri monitorare nella **Categoria conto di sostenibilità** e a cui vuoi collegare questa sottocategoria, puoi anche popolare uno o più fattori di emissione: 

   - **Fattore di emissione CO2**: specifica il fattore di emissioni per le emissioni CO2.  
   - **Fattore di emissione CH4**: specifica il fattore di emissioni per le emissioni CH4. 
   - **Fattore di emissione N2O**: specifica il fattore di emissioni per le emissioni N2O.  

5.  Se questa sottocategoria è correlata alle energie rinnovabili, seleziona il campo **Energie rinnovabili**.   

>[!NOTE]
>I campi **Importa dati** e **Importa da** sono destinati alla potenziale integrazione con sistemi esterni utilizzati per la raccolta dei fattori di emissione, ma nel **Prima ciclo di rilascio del 2024** non possono essere utilizzati come funzionalità per impostazione predefinita.  

## Movimenti contabili sostenibilità  

Nel **Registro della sostenibilità** è memorizzata la cronologia di tutte le transazioni di sostenibilità registrate, con tutti i dati sulle emissioni organizzati secondo il **Grafico dei conti di sostenibilità**. Quando un utente registra la **Registrazione sostenibilità**, tutti i dati cruciali verranno registrati lì. Tutti i report attivi vengono generati in base a **Movimenti contabili sostenibilità**.   

L'utente può aprire questo registro per un conto specifico utilizzando l'azione **Movimenti contabili** nella pagina **Grafico dei conti di sostenibilità** oppure, per aprire tutti i movimenti del registro, seleziona l'icona ![lampadina che apre la funzionalità Dimmi 3.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Movimenti contabili sostenibilità**, quindi seleziona il collegamento correlato. Passa sul campo con il mouse per visualizzare una breve descrizione.  

>[!IMPORTANT]
>Una volta registrati i dati nel Registro della sostenibilità, non è possibile eliminarli. In caso di errore puoi registrare la transazione di storno utilizzando gli stessi dettagli, ma utilizzando il segno negativo per l'importo.  

## Vedere anche  
[Finanze](finance.md)    
[Panoramica sulla gestione della sostenibilità](finance-manage-sustainability.md)
[Setup sostenibilità](finance-sustainability-setup.md)
[Come registrare le emissioni](finance-sustainability-journal.md)
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
