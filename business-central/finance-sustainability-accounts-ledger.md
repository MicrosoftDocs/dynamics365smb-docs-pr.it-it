---
title: Piano dei conti di sostenibilità e contabilità
description: 'Informazioni su come gestire il piano dei conti di sostenibilità (CoSA), le categorie e le sottocategorie, nonché i dettagli sui movimenti contabili relativi alla sostenibilità.'
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD, CoA, Chart, Account, Ledger'
ms.search.form: '6210, 6213, 6214, 6220'
ms.date: 05/07/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# Contabilità generale e piano dei conti di sostenibilità

## Piano dei conti di sostenibilità

Il piano dei conti di sostenibilità (CoSA) costituisce l'elenco strutturato fondamentale che viene utilizzato per registrare tutti i dati sulle emissioni. Funge da framework che classifica e organizza i conti di sostenibilità in base ai relativi attributi, come l'ambito o altri raggruppamenti. A ogni conto viene in genere assegnato un codice o un numero univoco per un facile riferimento e per facilitare il tracciamento. Presenta la stessa struttura di un piano dei conti tradizionale ma è personalizzato specificamente per monitorare i dati e le metriche correlati alla sostenibilità in un'organizzazione.

Gli utenti possono aggiungere categorie e sottocategorie di conti di sostenibilità per definire il comportamento del sistema. In questo modo, possono selezionare le emissioni dedicate da tracciare, i fattori di emissione, le formule e configurazioni simili.

> [!NOTE]
> In base agli standard relativi ai gas a effetto serra (GHG), esistono tre ambiti di emissione:
>
> - **Emissioni di ambito 1**: includono le emissioni da combustione mobile e stazionaria e da emissioni fuggitive involontarie.
> - **Emissioni di ambito 2**: includono le emissioni indirette derivanti dalla generazione di energia acquistata da fornitori di servizi pubblici.
> - **Emissioni di ambito 3**: includono un ampio spettro di emissioni, derivanti da beni e servizi acquistati e beni capitali, attività legate a combustibile ed energia, trasporti a monte e a valle, rifiuti generati, viaggi di lavoro e spostamenti dei dipendenti, ecc.

Il CoSA consente di eseguire le operazioni seguenti:

- Visualizzare i report che mostrano i movimenti e i saldi contabili di sostenibilità.
- Aprire la scheda del conto di sostenibilità per aggiungere o modificare le impostazioni.
- Visualizzare la categoria e la sottocategoria per il conto. 
- Visualizzare saldi separati per ogni emissione per un singolo conto.
- Aggiungere una o più dimensioni a ciascun conto e impostare i filtri dimensioni.

È possibile aggiungere, modificare o eliminare i conti di sostenibilità. Tuttavia, per evitare discrepanze, non è possibile eliminare un conto di sostenibilità se sono presenti uno o più movimenti contabili associati al conto.

### Aggiungere o cambiare conti

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi 3.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Piano dei conti di sostenibilità**, quindi seleziona il collegamento correlato.
2. Nella pagina **Piano dei conti di sostenibilità** puoi aprire ciascun conto di sostenibilità e aggiungere impostazioni o modificarle. Passa sul campo con il mouse per visualizzare una breve descrizione.

Per i conti di tipo **Totale** devi impostare il campo **Totale**.

Per i conti di tipo **Fine-Totale**, la funzione di impostazione del rientro imposta il campo **Totale** automaticamente. Dopo aver impostato tutti i conti, seleziona l'azione **Imposta rientri piano dei conti di sostenibilità** per eseguire la funzione di impostazione del rientro e impostare il campo **Totale**.

> [!IMPORTANT]
> La funzione di impostazione del rientro sovrascrive il valore di tutti i campi per i conti **Fine-Totale**. Pertanto, se hai immesso definizioni nel campo **Totale** per i conti **Fine-Totale** prima di eseguire la funzione di impostazione del rientro, dovrai inserirle di nuovo dopo aver eseguito la funzione.

### Eliminare conti

È possibile eliminare un conto di sostenibilità. Tuttavia, è necessario assicurarsi prima di tutto che non vi siano movimenti contabili associati. Business Central non consente di eliminare un conto di sostenibilità se sono presenti uno o più movimenti contabili associati al conto.

## Categorie di conti

Gli utenti devono aggiungere una categoria di conti di sostenibilità per ciascun conto di sostenibilità per definire il comportamento del sistema. Possono selezionare gli ambiti delle emissioni, le emissioni dedicate da tracciare, le formule e configurazioni simili.

Per esaminare le categorie di conti di sostenibilità, segui i passaggi:

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi 3.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Categorie conti di sostenibilità**, quindi seleziona il collegamento correlato.
2. Nella pagina **Categorie conti di sostenibilità**, puoi modificare l'elenco esistente o creare una nuova categoria. Per creare una nuova categoria, seleziona l'azione **Nuova**.
3. Imposta i campi **Codice** e **Descrizione**.
4. Nel campo **Ambito emissioni** seleziona una delle opzioni di ambito.
5. Seleziona le emissioni di gas che desideri monitorare. Attualmente sono disponibili le opzioni seguenti: **CO2**, **CH4** e **N2O**. Puoi selezionare qualsiasi combinazione che desideri monitorare, ma devi selezionare almeno una emissione.
6. Nel campo **Base di calcolo** puoi selezionare la base per il calcolo, vale a dire la formula, da usare per i calcoli delle emissioni se non conosci la quantità di emissioni precisa. Puoi selezionare una delle opzioni seguenti: **Combustibile/elettricità**, **Distanza**, **Installazione** o **Personalizzata**.

    > [!NOTE]
    > Se il set di formule disponibili nel campo **Base di calcolo** non è sufficiente, puoi estendere il campo e aggiungere al sistema altri calcoli da usare nelle registrazioni di sostenibilità.

7. Se hai selezionato **Personalizzata** nel campo **Base di calcolo**, puoi configurare una descrizione personalizzata nel campo **Valore personalizzato**.

Se imposti il campo **Base di calcolo**, la tabella seguente spiega il modo in cui il sistema calcola le emissioni in base all'opzione che hai selezionato. In questa tabella, *EF* rappresenta il valore **Fattore di emissione** che è possibile configurare nella pagina **Sottocategoria conto di sostenibilità**.

| Tipo di emissioni | Base di calcolo | Formula | Commento |
|---------------|------------------------|---------|---------|
| **Ambito 1** | | | |
| Combustione stazionaria | Combustibile/Elettricità | *Emissione* = *Combustibile* &times; *EF* | *Combustibile* = Quantità di combustibile speso per scaldabagni, stufe, ossidatori termici, ecc. |
| Combustione mobile | Combustibile/Elettricità | *Emissione* = *Combustibile* &times; *EF* | *Combustibile* = Quantità di combustibile speso per veicoli stradali, non stradali, ferrovia, ecc. |
| | | *Emissione* = *Distanza* &times; *EF* | *Distanza* = Chilometraggio dei veicoli stradali, non stradali, ferrovia, ecc. |
| Emissioni fuggitive | Installazione | *Emissione* = *Moltiplicatore installazione* &times; *Importo personalizzato* &divide; 100 &times; *Fattore temporale* | *Importo personalizzato* = Perdite di assemblaggio, tasso di perdita annuale, ecc. |
| **Ambito 2** | | | |
| Fornitori di servizi | Combustibile/Elettricità | *Emissione* = *Elettricità* &times; *EF* | *Combustibile/elettricità* = Quantità di elettricità, quantità di vapore, unità di riscaldamento, ecc. |
| | Personalizzato | *Emissione* = *Importo personalizzato* &times; *EF* | *Importo personalizzato* = Unità termica, tonnellata all'ora, ecc. |
| **Ambito 3** | | | |
| Beni e servizi acquistati e beni capitali | Personalizzato | *Emissione* = *Importo personalizzato* &times; *EF* | *Importo personalizzato* = Costo (CoGe), ecc. |
| Trasporto e distribuzione upstream | Distanza | *Emissione* = *Distanza* &times; *EF* | |
| | Distanza | *Emissione* = *Distanza* &times; *Moltiplicatore* &times; *EF* | *Moltiplicatore* = Tonnellate di carico |
| Trasporto e distribuzione downstream | Distanza | *Emissione* = *Distanza* &times; *EF* | |
| | Distanza | *Emissione* = *Distanza* &times; *Moltiplicatore* &times; *EF* | *Moltiplicatore* = Tonnellate di carico |
| Rifiuti generati nelle operazioni e nel trattamento di fine vita dei prodotti venduti | Personalizzato | *Emissione* = *Importo personalizzato* &times; *EF* | *Importo personalizzato* = Rifiuti |
| Viaggi d'affari e spostamento dei dipendenti | Distanza | *Emissione* = *Distanza* &times; *EF* | *Distanza* = Chilometraggio di auto aziendale, auto a noleggio, treno, volo utilizzati, ecc. |
| | Personalizzato | *Emissione* = *Importo personalizzato* &times; *EF* | *Importo personalizzato* = Soggiorni in hotel |
| | Combustibile/Elettricità | *Emissione* = *Combustibile* &times; *EF* | *Combustibile* = Quantità di combustibile consumato con auto aziendale, auto a noleggio, ecc. |

## Sottocategorie di conti

Gli utenti devono aggiungere una categoria di conti di sostenibilità per ciascun conto di sostenibilità. Questa sottocategoria definisce i fattori di emissione che vengono utilizzati nelle formule, in base alla scelta di tracciamento delle emissioni nella categoria del conto di sostenibilità.

Per esaminare le sottocategorie di conti di sostenibilità, segui questi passaggi:

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi 3.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Sottocategorie conti di sostenibilità**, quindi seleziona il collegamento correlato. 
2. Nella pagina **Sottocategorie conti di sostenibilità**, puoi modificare l'elenco esistente o creare una nuova categoria. Per creare una nuova categoria, seleziona l'azione **Nuova**.
3. Imposta i campi **Codice** e **Descrizione**.
4. In base alle emissioni di gas che desideri monitorare nella categoria del conto di sostenibilità e a cui vuoi collegare questa sottocategoria, puoi anche impostare uno o più fattori di emissione: 

    - **Fattore di emissione CO2**: il fattore di emissione per l'emissione di anidride carbonica (CO<sub>2</sub>).
    - **Fattore di emissione CH4**: il fattore di emissione per l'emissione di metano (CH<sub>4</sub>).
    - **Fattore di emissione N2O**: il fattore di emissione per l'emissione di ossido di azoto (N<sub>2</sub>O).

5. Se la sottocategoria è correlata a energie rinnovabili, seleziona il campo **Energie rinnovabili**.

> [!NOTE]
> I campi **Importa dati** e **Importa da** sono destinati all'integrazione potenziale con i sistemi esterni che vengono usati per raccogliere i fattori di emissione. Tuttavia, nel **primo ciclo di rilascio del 2024**, questi campi non possono essere utilizzati come funzionalità per impostazione predefinita.

## Movimenti contabili sostenibilità

Il registro della sostenibilità memorizza la cronologia di tutte le transazioni di sostenibilità registrate e organizza tutti i dati sulle emissioni in base al CoSA. Quando un utente registra il giornale di registrazione della sostenibilità, tutti i dati cruciali vengono registrati lì. Tutti i report attivi vengono generati in base ai movimenti contabili sostenibilità.

Per aprire questo registro per un conto specifico, utilizza l'azione **Movimenti contabili** nella pagina **Piano del conto di sostenibilità**. Per aprire tutti i movimenti contabili, seleziona l'![icona lampadina che apre la funzione Dimmi 3.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Movimenti contabili sostenibilità**, quindi seleziona il collegamento correlato. Passa sul campo con il mouse per visualizzare una breve descrizione.

> [!IMPORTANT]
> Dopo che hai registrato i dati nel registro della sostenibilità, non puoi eliminarli. In caso di errore puoi registrare la transazione di storno con gli stessi dettagli, ma con il segno negativo per l'importo.

## Vedere anche

[Dati finanziari](finance.md)  
[Panoramica della gestione della sostenibilità](finance-manage-sustainability.md)  
[Setup sostenibilità](finance-sustainability-setup.md)  
[Come registrare le emissioni](finance-sustainability-journal.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
