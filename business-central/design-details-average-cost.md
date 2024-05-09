---
title: 'Dettagli di progettazione: costo medio'
description: Il costo medio di un articolo è calcolato con una media ponderata periodica.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: null
ms.search.form: '8645,'
ms.date: 04/26/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Dettagli di progettazione: costo medio

Il costo medio di un articolo è calcolato con una media ponderata periodica. La media si basa sul periodo di costo medio specificato in [!INCLUDE[prod_short](includes/prod_short.md)].  

La data di valutazione viene impostata automaticamente.  

## Impostazione del calcolo del costo medio

Nella seguente tabella vengono descritti i due campi della pagina **Setup magazzino** che devono essere compilati per abilitare il calcolo del costo medio.  

|Campo|Descrizione|  
|---------------------------------|---------------------------------------|  
|**Costo medio periodo**|Specifica il periodo di tempo in cui viene calcolato il costo medio. Sono disponibili le seguenti opzioni:<br /><br /> - **Giorno**<br />- **Settimana**<br />- **Mese**<br />- **Periodo contabile**<br /><br /> Le riduzioni di magazzino registrate nel costo medio del periodo viene assegnato il costo medio calcolato per tale periodo.|  
|**Tipo calcolo costo medio**|Specifica come viene calcolato il costo medio. Sono disponibili le seguenti opzioni:<br /><br /> - **Articolo**<br />- **Articolo, variante e ubicazione**<br /> Con questa opzione, il costo medio viene calcolato per ciascun articolo, per ciascuna collocazione e per ciascuna variante dell'articolo. Il costo medio di questo articolo dipende da dove lo immagazzini e dalla variante selezionata, ad esempio il colore.|  

> [!NOTE]  
> È possibile utilizzare solo un costo medio del periodo e un tipo di calcolo del costo medio in un anno fiscale.  
>
> Nella pagina **Periodi contabili** viene mostrato il costo medio del periodo e il tipo di calcolo del costo medio utilizzato per quel periodo, per ogni periodo contabile.  

## Calcolo del costo medio

 Quando si registra una transazione per un articolo per il quale viene utilizzato il metodo di costing medio, viene creato un movimento nella tabella **Rettifica costo medio cod. spedizioni Intrastat**. Il movimento contiene numero articolo, codice variante e codice ubicazione della transazione. Il movimento contiene inoltre il campo **Data valutazione**, che specifica l'ultima data del costo medio del periodo in cui è stata registrata la transazione.  

> [!NOTE]  
> Questo campo non deve essere confuso con il campo **Data valutazione** della tabella **Movimenti valorizzazione**, che mostra la data in cui ha effetto il valore e viene utilizzato per determinare il costo medio del periodo a cui appartiene il movimento di valorizzazione.  

 Il costo medio di una transazione viene calcolato quando il costo dell'articolo viene rettificato. Per ulteriori informazioni, vedere [Dettagli di progettazione: Rettifica costo](design-details-cost-adjustment.md). La rettifica dei costi utilizza i movimenti nella tabella **Rettifica costo medio cod. spedizioni Intrastat** per identificare gli articoli o gli articoli, le ubicazioni e le varianti per cui calcolare il costo medio. Per ogni movimento il cui costo non è ancora stato rettificato, la rettifica costo utilizza quanto segue per determinare il costo medio:  

- Determinazione del costo dell'articolo all'inizio del costo medio del periodo.  
- Aggiunge la somma dei costi in entrata registrati nel costo medio del periodo. Sono inclusi gli acquisti, i resi di vendita, le rettifiche positive e gli output di produzione e di assemblaggio.  
- Sottrazione della somma dei costi delle transazioni in uscita collegate in modo fisso ai carichi nel costo medio del periodo. In genere sono inclusi resi di acquisto e output negativi.  
- Divisione per la quantità di magazzino totale alla fine del costo medio del periodo. Esclude le riduzioni di magazzino che vengono valutate.  

 Il costo medio calcolato viene quindi collegato alle riduzioni di magazzino per l'articolo (o articolo, ubicazione e variante) con le date di registrazione nel costo medio del periodo. Per gli aumenti di magazzino collegati in modo fisso alle riduzioni di magazzino nel costo medio del periodo, [!INCLUDE [prod_short](includes/prod_short.md)] trasferisce il costo medio calcolato dall'aumento alla riduzione.  

### Esempio: costo medio del periodo = giorno

Nel seguente esempio viene illustrato l'effetto del calcolo del costo medio basato su un periodo di un giorno. Il campo **Tipo calcolo costo medio** della pagina **Setup magazzino** è impostato su **Articolo**.  

La tabella seguente mostra i movimenti contabili per l'articolo di esempio costo medio, ITEM1, prima di eseguire il processo batch **Rettifica costo - Movimenti articoli**.  

| **Data di registrazione** | **Tipo mov. articolo** | **Quantità** | **Importo costo (effettivo)** | **Nr. movimento** |
|--|--|--|--|--|
| 01-01-23 |   Acquisti | 1 | 20.00 | 1 |
| 01-01-23 |   Acquisti | 1 | 40.00 | 2 |
| 01-01-23 |   Vendita | -1 | -20,00 | 3 |
| 02-01-23 |   Vendita | -1 | -40,00 | 4 |
| 02-02-23 |   Acquisti | 1 | 100.00 | 5 |
| 02-03-23 |   Vendita | -1 | -100,00 | 6 |

> [!NOTE]  
> Poiché la rettifica dei costi non è ancora avvenuta, i valori nel campo **Importo costo (effettivo)** delle riduzioni di magazzino corrispondono agli aumenti di magazzino a cui sono applicati.  

 Nella seguente tabella vengono mostrati i movimenti nella tabella **Rettifica costo medio cod. spedizioni Intrastat** che si applicano ai movimenti di valorizzazione risultanti dai movimenti contabili articolo nella tabella precedente.  

| **Nr. Articolo** | **Cod. variante** | **Codice ubicazione** | **Data di valutazione** | **Costo rettificato** |
|--|--|--|--|--|
| ARTICOLO1 |  | BLU | 01-01-23 |   Nr. |
| ARTICOLO1 |  | BLU | 02-01-23 |   Nr. |
| ARTICOLO1 |  | BLU | 02-02-23 |   Nr. |
| ARTICOLO1 |  | BLU | 02-03-23 |   Nr. |

 Nella tabella seguente vengono mostrati gli stessi movimenti contabili dopo che hai eseguito il processo batch **Rettifica costo - Movimenti articoli**. Il costo medio giornaliero viene calcolato e applicato alle riduzioni del magazzino.  

| **Data di registrazione** | **Tipo mov. articolo** | **Quantità** | **Importo costo (effettivo)** | **Nr. movimento** |
|--|--|--|--|--|--|
| 01-01-23 |   Acquisti | 1 | 20.00 | 1 |
| 01-01-23 |   Acquisti | 1 | 40.00 | 2 |
| 01-01-23 |   Vendita | -1 | -30,00 | 3 |
| 02-01-23 |   Vendita | -1 | -30,00 | 4 |
| 02-02-23 |   Acquisti | 1 | 100.00 | 5 |
| 02-03-23 |   Vendita | -1 | -100,00 | 6 |

### Esempio: costo medio del periodo = mese

 In questo esempio viene illustrato l'effetto del calcolo del costo medio basato su un periodo di un mese. Il campo **Tipo calcolo costo medio** della pagina **Setup magazzino** è impostato su **Articolo**.  

 Se il costo medio è calcolato su un periodo di un mese, [!INCLUDE [prod_short](includes/prod_short.md)] crea solo un movimento per ogni combinazione di numero di articolo, codice variante, codice ubicazione e data di valutazione.  

 La tabella seguente mostra i movimenti contabili per l'articolo di esempio costo medio, ITEM1, prima di eseguire il processo batch **Rettifica costo - Movimenti articoli**.  

| **Data di registrazione** | **Tipo mov. articolo** | **Quantità** | **Importo costo (effettivo)** | **Nr. movimento** |
|--|--|--|--|--|
| 01-01-23 |   Acquisti | 1 | 20.00 | 1 |
| 01-01-23 |   Acquisti | 1 | 40.00 | 2 |
| 01-01-23 |   Vendita | -1 | -20,00 | 3 |
| 02-01-23 |   Vendita | -1 | -40,00 | 4 |
| 02-02-23 |   Acquisti | 1 | 100.00 | 5 |
| 02-03-23 |   Vendita | -1 | -100,00 | 6 |

> [!NOTE]  
> Poiché la rettifica dei costi non è ancora avvenuta, i valori nel campo **Importo costo (effettivo)** delle riduzioni di magazzino corrispondono agli aumenti di magazzino a cui sono applicati.  

Nella seguente tabella vengono mostrati i movimenti nella tabella **Rettifica costo medio cod. spedizioni Intrastat** che si applicano ai movimenti di valorizzazione risultanti dai movimenti contabili articolo nella tabella precedente.  

| **Nr. Articolo** | **Cod. variante** | **Codice ubicazione** | **Data di valutazione** | **Costo rettificato** |
|--|--|--|--|--|
| ARTICOLO1 |  | BLU | 01-31-23 |   Nr. |
| ARTICOLO1 |  | BLU | 02-28-23 |   Nr. |

> [!NOTE]  
> La data di valutazione è impostata sull'ultimo giorno del costo medio del periodo, che in questo caso è l'ultimo giorno del mese.  

Nella tabella seguente vengono mostrati gli stessi movimenti contabili dopo che hai eseguito il processo batch **Rettifica costo - Movimenti articoli**. Il costo medio mensile viene calcolato e applicato alle riduzioni di magazzino.  

|**Data di registrazione** | **Tipo mov. articolo** | **Quantità** | **Importo costo (effettivo)** | **Nr. movimento** |
|--|--|--|--|--|
| 01-01-23 | Acquisti | 1 | 20.00 | 1 |
| 01-01-23 | Acquisti | 1 | 40.00 | 2 |
| 01-01-23 | Vendita | -1 | -30,00 | 3 |
| 02-01-23 | Vendita | -1 | -65,00 | 4 |
| 02-02-23 | Acquisti | 1 | 100.00 | 5 |
| 02-03-23 | Vendita | -1 | -65,00 | 6 |

Il costo medio della voce numero 3 è calcolato nel periodo di costo medio di gennaio. Il costo medio per le voci 4 e 6 è calcolato nel periodo di costo medio di febbraio.  

Per ottenere il costo medio per febbraio, [!INCLUDE [prod_short](includes/prod_short.md)] aggiunge il costo medio di un articolo ricevuto in magazzino (100,00) al costo medio all'inizio del periodo (30,00). La somma (130,00) viene quindi divisa per la quantità totale in magazzino (2). Questo calcolo fornisce il costo medio risultante dell'articolo nel periodo di febbraio (65,00). Tale costo medio viene assegnato alle uscite da magazzino nel periodo (movimenti 4 e 6).  

## Impostazione della data di valutazione

 Il campo **Data valutazione** della tabella **Movimenti valorizzazione** determina il costo medio del periodo al quale la voce di dimuzione inventario appartiene. Questa impostazione si applica anche al magazzino dei semilavorati (WIP).  

 Nella seguente tabella vengono mostrati i criteri utilizzati per impostare la data di valutazione.  

| Scenario | Data di registrazione | Quantità valorizzata | Rivalutazione | Data di valutazione |
|--|--|--|--|--|
| 1 |  | Positivo | No | Data di registrazione del movimento contabile articolo |
| 2 | Successivo all'ultima data di valutazione dei movimenti di valorizzazione collegati | Negativo | No | Data di registrazione del movimento contabile articolo |
| 3 | Precedentemente all'ultima data di valutazione dei movimenti di valorizzazione collegati | Positivo | No | Ultima data di valutazione dei movimenti di valorizzazione collegati |
| 4 |  | Negativo | Sì | Data di registrazione del movimento di rivalorizzazione |

### Esempio

Nella seguente tabella di movimenti di valorizzazione vengono illustrati differenti scenari.  

| Scenario | Data di registrazione | Tipo mov. articolo | Data di valutazione | Quantità valorizzata | Importo costo (effettivo) | Nr. movimento cont. articolo | Nr. movimento |
|--|--|--|--|--|--|--|--|
| 1 | 01-01-20 | Acquisto | 01-01-20 | 2 | 20.00 | 1 | 1 |
| 2 | 01-15-20 | (Addebito articolo) | 01-01-20 | 2 | 8.00 | 1 | 2 |
| 3 | 02-01-20 | Vendite | 02-01-20 | -1 | -14,00 | 2 | 3 |
| 4 | 03-01-20 | (Rivalutazione) | 03-01-20 | 1 | -.4,00 | 1 | 4 |
| 5 | 02-01-20 | Vendite | 03-01-20 | -1 | -10,00 | 3 | 5 |

> [!NOTE]  
> Nel movimento numero 5 nella tabella precedente, l'utente ha immesso un ordine di vendita con una data di registrazione (20-01-02) antecedente all'ultima data di valutazione dei movimenti di valorizzazione collegati (20-01-03). Se il valore corrispondente nel campo **Importo costo (effettivo)** per questa data (01-02-20) viene utilizzato per questo movimento, sarà 14,00. Ciò fornirebbe una situazione in cui la quantità in magazzino è pari a zero, ma il valore di magazzino è 4,00.  
>
> Per evitare una tale mancanza di corrispondenza tra quantità e valore, la data di valutazione è impostata in modo da essere uguale alla data di valutazione più recente dei movimenti di valorizzazione collegati (20-01-03). Il valore nel campo **Importo costo (effettivo)** diventa 10,00 dopo la rivalutazione, che significa che la quantità di magazzino è pari a zero e anche il valore di magazzino è pari a zero.  

> [!CAUTION]  
> Poiché il report **Valutazione magazzino** è basato sulla data di registrazione, il report rifletterà tutte le non corrispondenze quantità-valore negli scenari come nell'esempio di cui sopra. Per ulteriori informazioni, vedere [Dettagli di progettazione: Valutazione magazzino](design-details-inventory-valuation.md).  

Se la quantità in magazzino è inferiore a zero dopo la registrazione della riduzione di magazzino, la data di valutazione viene prima impostata sulla data di registrazione della riduzione di magazzino. La data può essere modificata quando viene applicato l'aumento di magazzino, in base alle regole precedentemente descritte nella nota in questa sezione.  

## Ricalcolo del costo medio

La valutazione delle diminuzioni delle scorte come media ponderata sarebbe semplice in diversi scenari:

- Gli acquisti vengono sempre fatturati prima della vendita.
- I post non sono mai retrodatati.
- Non hai mai commesso errori.

Tuttavia, la realtà è diversa.  

Come illustrato negli esempi in questo articolo, la data di valutazione è definita come data a partire dalla quale il movimento di valorizzazione viene inclusa nel calcolo del costo medio. Questa impostazione consente di eseguire diverse operazioni per gli articoli con il metodo di costing medio:  

- Fatturare la vendita di un articolo prima che l'acquisto dell'articolo sia stato fatturato.  
- Retrodatare una registrazione.  
- Recuperare una registrazione errata.  

> [!NOTE]  
> Un altro motivo per questa flessibilità è il collegamento fisso. Per ulteriori informazioni sul collegamento fisso, vedere [Dettagli di progettazione: Collegamento articoli](design-details-item-application.md).  

A causa di questa flessibilità, potrebbe essere necessario ricalcolare il costo medio dopo la registrazione. Ad esempio, se si registra un aumento o una riduzione di magazzino con una data di valutazione antecedente a una riduzione di magazzino. Il ricalcolo del costo medio avviene automaticamente quando si esegue il processo batch **Rettifica costo - Movimenti articoli**, manualmente o automaticamente.  

Puoi modificare la base di valutazione del magazzino in un periodo contabile modificando i valori nei campi **Costo medio periodo** e **Tipo calcolo costo medio**. Tuttavia, ti consigliamo di usare cautela e di consultare il tuo revisore.  

### Esempio di costo medio ricalcolato

Questo esempio mostra come [!INCLUDE [prod_short](includes/prod_short.md)] ricalcola il costo medio quando pubblichi in una data precedente a una diminuzione dell'inventario. L'esempio si basa su un periodo del costo medio impostato su **Giorno**.  

Nella seguente tabella vengono mostrati i movimenti di valorizzazione presenti per l'articolo dopo l'immissione della registrazione.  

| Data di valutazione | Quantità | Importo costo (effettivo) | Nr. movimento |
|--|--|--|--|
| 01-01-20 | 1 | 10.00 | 1 |
| 01-02-20 | 1 | 20.00 | 2 |
| 02-15-20 | -1 | -15,00 | 3 |
| 02-16-20 | -1 | -15,00 | 4 |

L'utente registra un aumento di magazzino (movimento numero 5) con una data di valutazione (20-03-01) prima di una riduzione di magazzino. Per pareggiare il magazzino, il costo medio deve essere ricalcolato e rettificato a 17,00.  

Nella seguente tabella vengono mostrati i movimenti di valorizzazione presenti per l'articolo dopo l'immissione del movimento numero 5.  

| Data di valutazione | Quantità | Importo costo (effettivo) | Nr. movimento |
|--|--|--|--|
| 01-01-20 | 1 | 10.00 | 1 |
| 01-02-20 | 1 | 20.00 | 2 |
| 01-03-20 | 1 | 21.00 | 5 |
| 02-15-20 | -1 | -17,00 | 3 |
| 02-16-20 | -1 | -17,00 | 4 |

## Vedi anche

[Dettagli di progettazione: determinazione dei costi di magazzino](design-details-inventory-costing.md)  
[Dettagli di progettazione: metodi di determinazione dei costi](design-details-costing-methods.md)  
[Dettagli di progettazione: rettifica costo](design-details-cost-adjustment.md)  
[Dettagli di progettazione: collegamento articoli](design-details-item-application.md)  
[Gestione dei costi di magazzino](finance-manage-inventory-costs.md)  
[Dati finanziari](finance.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Glossario dei termini nei processi aziendali di Dynamics 365](/dynamics365/guidance/business-processes/glossary)  
[Processo aziendale per la determinazione dei costi dei prodotti e relazione con altri processi con Dynamics 365](/dynamics365/guidance/business-processes/design-to-retire-define-product-costing-overview)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
