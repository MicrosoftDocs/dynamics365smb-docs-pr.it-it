---
title: Dettagli di progettazione - Modifica dei metodi di costing per gli articoli
description: Informazioni su come assegnare un diverso metodo di costing a un articolo sebbene si sia già utilizzato l'articolo nelle transazioni.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'costing methods, costing, item cost'
ms.search.form: 8645
ms.date: 06/08/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# <a name="design-details-change-the-costing-method-for-items"></a>Dettagli di progettazione: modifica dei metodi di costing per gli articoli

In [!INCLUDE[prod_short](includes/prod_short.md)], non è possibile modificare un metodo di costing per un articolo dopo aver incluso l'articolo in una transazione. Ad esempio, dopo aver acquistato o venduto l'articolo. Se è stato assegnato un metodo di costing errato per l'articolo o gli articoli, è possibile che il problema non venga rilevato fino a quando non si esegue la rendicontazione finanziaria.

Questo argomento descrive come risolvere questa situazione. L'approccio consigliato è quello di sostituire l'articolo con un metodo di costing errato con un nuovo articolo e utilizzare un ordine di assemblaggio per trasferire l'inventario dal vecchio articolo al nuovo.

> [!NOTE]
> L'utilizzo degli ordini di assemblaggio consente di continuare a far fluire i costi, anche se ci sono fatture di acquisto o spese di spedizione da registrare. Inoltre, consentono di annullare la conversione e di recuperare le quantità degli articoli originali, se necessario.

> [!TIP]
> Per familiarizzare con il processo, consigliamo di iniziare il processo di conversione con un singolo articolo o un piccolo set di articoli.

## <a name="about-costing-methods"></a>Informazioni sui metodi di costing

I metodi di costing controllano i calcoli dei costi quando le merci vengono acquistate, ricevute in inventario e vendute. I metodi di costing influenzano la tempistica degli importi registrati nel COGS che incidono sul profitto lordo. È questo flusso che calcola il COGS. Il costo delle merci vendute (COGS) e il ricavo sono utilizzati per determinare l'utile lordo, come segue:

*utile lordo* = *entrate - COGS*

Quando si impostano gli articoli di inventario, è necessario assegnare un metodo di costing. Il metodo può variare da azienda a azienda e da articolo a articolo, quindi è importante scegliere quello giusto. In [!INCLUDE[prod_short](includes/prod_short.md)] sono supportati i seguenti metodi di costing:

* Media
* FIFO
* LIFO
* Standard
* Specifico

Per ulteriori informazioni, vedere [Dettagli di progettazione: Metodi di costing](design-details-costing-methods.md).

## <a name="use-assembly-orders-to-change-costing-method-assignments"></a>Utilizzare gli ordini di assemblaggio per modificare le assegnazioni del metodo di costing

Questa sezione descrive i seguenti passaggi per modificare il metodo di costing assegnato a un articolo:

1. Definire il metodo di costing di default.
2. Identificare gli articoli per cui modificare il metodo di costing e rinumerarli.
3. Creare nuovi articoli con il vecchio schema di numerazione e copiare l'anagrafica in un batch.
4. Copiare manualmente l'anagrafica correlata dall'articolo esistente al nuovo articolo.
5. Determinare la quantità di inventario da convertire dall'articolo originale al nuovo articolo.
6. Trasferire l'inventario al nuovo articolo.
7. Gestire le quantità di inventario assegnate alla domanda.
8. Bloccare l'articolo originale da ulteriore utilizzo.  

### <a name="define-a-default-costing-method"></a>Definire il metodo di costing di default

Per evitare errori futuri, è possibile specificare un metodo di costing predefinito per i nuovi articoli. Ogni volta che qualcuno crea un nuovo oggetto, [!INCLUDE[prod_short](includes/prod_short.md)] suggerirà il metodo di costing predefinito. Si specifica il metodo predefinito nel campo **Metodo di costing di default** della pagina **Setup magazzino**. 

### <a name="identify-the-items-to-change-the-costing-method-for-and-renumber-them"></a>Identificare gli articoli per cui modificare il metodo di costing e rinumerarli

Si potrebbe voler dare ai nuovi articoli gli stessi numeri di quelli che stanno sostituendo. Per fare ciò, modificare i numeri degli articoli esistenti. Ad esempio, se il numero di articolo esistente è "P1000", è possibile modificarlo in "X-P1000". Questa è una modifica manuale che occorre apportare per ogni articolo.

### <a name="create-new-items-with-the-old-numbering-scheme-and-copy-the-master-data-in-a-batch"></a>Creare nuovi articoli con il vecchio schema di numerazione e copiare l'anagrafica in un batch

Creare i nuovi articoli utilizzando lo schema numerico corrente. Con l'eccezione del campo **Metodo di costing**, i nuovi articoli dovrebbero contenere la stessa anagrafica degli articoli esistenti. Per trasferire l'anagrafica per l'articolo e i dati correlati da altre funzioni, utilizzare l'azione **Copia articolo** della pagina **Scheda articolo**. Per ulteriori informazioni, vedere [Copiare articoli esistenti per creare nuovi articoli](inventory-how-copy-items.md).

Dopo aver creato i nuovi articoli e trasferito l'anagrafica, assegnare il metodo di costing corretto.

### <a name="manually-copy-related-master-data-from-the-original-item-to-the-new-item"></a>Copiare manualmente l'anagrafica correlata dall'articolo originale al nuovo articolo

Per rendere completamente utili i nuovi articoli, è necessario copiare manualmente alcuni dati anagrafici da altre aree, come descritto nella tabella seguente.

|Area  |Cosa copiare  |Come copiarlo  |
|---------|---------|---------|
|Inventario |Unità di stockkeeping (SKU) |Controllare se è stato specificato una SKU per l'articolo originale. Se sono stati immessi parametri di pianificazione per ciascuna scheda SKU, è necessario creare manualmente la SKU per il nuovo articolo. Se i parametri non sono specificati, è possibile utilizzare il processo batch **Crea unità di stockkeeping** dalla pagina **Scheda articolo** per creare i dati.|
| |Articoli sostitutivi |Controllare se sono stati definiti articoli sostitutivi per l'articolo originale. Se presenti, trasferire tali dati nel nuovo articolo. Per visualizzare gli articoli sostitutivi, utilizzare l'azione **Sostituzioni** nella pagina **Scheda articolo**. |
| |Report di analisi |Esaminare i report Analisi articoli, Analisi vendite e Analisi acquisti. Se si fa riferimento agli articoli originali è possibile creare un nuovo report di analisi con un riferimento al nuovo articolo (mantenendo il report di analisi originale da utilizzare come cronologia) oppure modificare i report in modo che facciano riferimento al nuovo articolo. |
| |Registrazioni standard |Verificare se le registrazioni standard fanno riferimento all'articolo originale e trasferire tali dati al nuovo articolo quando necessario. Queste informazioni sono disponibili nelle registrazioni standard, che sono disponibili nella registrazione magazzino.  |
|Vendite |Percentuale pagamenti anticipati vendite | Controllare se sono state definite percentuali di pagamento anticipato vendite per l'articolo originale e trasferire tali dati nel nuovo articolo. Per visualizzare le percentuali di pagamento anticipato, nella pagina **Scheda articolo** scegliere **Vendite** e poi **Percentuali di pagamento anticipato**.|
|Acquisti |Percentuale pagamento anticipato acquisti |Controllare se sono state definite percentuali di pagamento anticipato acquisti per l'articolo originale e trasferire tali dati nel nuovo articolo. Per visualizzare le percentuali di pagamento anticipato, nella pagina **Scheda articolo** scegliere **Acquisti** e poi **Percentuali di pagamento anticipato**. |
|Warehouse |Contenuto collocazioni |Rivedere il contenuto collocazione definito per l'articolo originale. Se colonne come Q.tà min.,  Q.tà max.,  Predefinito e Dedicato sono state inserite individualmente, è necessario creare manualmente il contenuto della collocazione per il nuovo articolo. In caso contrario, non è richiesta alcuna azione. [!INCLUDE[prod_short](includes/prod_short.md)] manterrà i record quando si registrano documenti e registrazioni di magazzino.|
|Posizione |Costi commessa |Controllare se sono stati definiti costi progetto per l'articolo originale e trasferire tali dati nel nuovo articolo. Questa informazione è disponibile nella pagina **Scheda progetto** nella parte **Dettagli progetto - Nr. prezzi** nel **riquadro Dettaglio informazioni**. |
|Assistenza |Competenza risorsa in assistenza |Controllare se sono state definite le competenze risorsa in assistenza per l'articolo originale e trasferire tali dati nel nuovo articolo. Per visualizzare le competenze delle risorse, utilizzare l'azione **Competenze risorse** nella pagina **Scheda articolo**.  |
| |Componenti articolo in assistenza |Controllare se sono stati definiti i componenti per l'articolo in assistenza originale e trasferire tali dati nel nuovo articolo. Per visualizzare i componenti dell'articolo in assistenza, nella pagina **Scheda articolo** usare l'azione **Articolo in assistenza** per aprire l'elenco degli articoli in assistenza correlati, quindi selezionare l'azione **Componenti**.  |
|Produzione |Dist.base di produz. |Controllare se eventuali DB produzione contengono l'articolo originale e sostituirlo con il nuovo articolo. Per sostituire l'articolo originale, nella pagina **DB produzione**, scegliere l'azione **Scambio articolo DB produzione**. |
|Assemblaggio |DB assemblaggio |Controllare se eventuali DB assemblaggio contengono l'articolo originale e sostituirlo manualmente con il nuovo articolo. |

> [!IMPORTANT]
> Se il nuovo metodo di costing è standard, è necessario immettere un valore nel campo **Costo standard** della pagina **Scheda articolo**. È possibile usare la pagina **Prospetto costo standard** per impostare il dettaglio costi di conseguenza. Per ulteriori informazioni, vedere [Aggiornare i costi standard](finance-how-to-update-standard-costs.md).

### <a name="determine-the-inventory-quantity-to-convert-from-the-original-item-to-the-new-item"></a>Determinare la quantità di inventario da convertire dall'articolo originale al nuovo articolo

> [!NOTE]
> Questo passaggio non considera le quantità incluse negli ordini non spediti. Per ulteriori informazioni, vedere [Gestire le quantità di magazzino allocate alla domanda](design-details-changing-costing-methods.md#handle-inventory-quantities-that-are-allocated-to-demand). 

Utilizzare una registrazione d'inventario fisico per produrre un elenco di quantità di magazzino. A seconda dell'impostazione della posizione del magazzino, utilizzare una delle seguenti opzioni:

* Registrazioni inventario fisico
* Registrazioni  inventario whse.

Entrambe le registrazioni possono calcolare la quantità di inventario dell'articolo, compresa la posizione, la variante, la collocazione e la posizione di stoccaggio. Per ulteriori informazioni, vedere [Conteggio, rettifica e riclassificazione dell'inventario utilizzando registrazioni ](inventory-how-count-adjust-reclassify.md).

### <a name="transfer-the-inventory-to-the-new-item"></a>Trasferire l'inventario al nuovo articolo

Creare e registrare ordini di assemblaggio per trasferire il costo e la quantità di magazzino dall'articolo originale al nuovo articolo. Gli ordini di assemblaggio possono convertire un articolo in un altro preservando i costi. Questo aiuta a garantire che i totali netti per il conto magazzino e il COGS non siano interessati (tranne quando il nuovo metodo di costing è standard, nel qual caso i costi possono essere distribuiti ai conti scostamento). Per ulteriori informazioni, vedere [Gestione assemblaggio](assembly-assemble-items.md).

Quando si creano ordini di assemblaggio, utilizzare le informazioni dalla Registrazioni inventario fisico o dalla  Registrazioni inventario whse. Le seguenti tabelle descrivono le informazioni nei report da inserire nell'intestazione e nelle righe nell'ordine di assemblaggio.

#### <a name="header"></a>Testata

|Campo  |Valore da immettere  |
|---------|---------|
|Nr. Articolo |Il numero del nuovo articolo. |
|Quantità |La quantità nella registrazione di inventario fisico.<br> **NOTA:** le quantità calcolate dalle registrazioni di inventario fisico non includono le quantità che si trovano su ordini non ancora spediti.  |
|Cod. variante |Lo stesso della registrazione di inventario fisico.  |
|Cod. ubicazione |Lo stesso della registrazione di inventario fisico. |
|Codice unità di misura |Lo stesso della registrazione di inventario fisico. |
|Codice collocazione |Lo stesso della registrazione di inventario fisico. |

#### <a name="lines"></a>Righe

|Campo  |Valore da immettere  |
|---------|---------|
|Tipo |Articolo |
|No. |Il numero dell'articolo originale. |
|Quantità per |1 |
|Cod. variante |Lo stesso della registrazione di inventario fisico. |
|Cod. ubicazione |Lo stesso della registrazione di inventario fisico. |
|Codice unità di misura |Lo stesso della registrazione di inventario fisico. |

> [!NOTE]
> Un ordine di assemblaggio può gestire una sola SKU di un articolo alla volta. È necessario creare un ordine di assemblaggio per ogni combinazione di SKU che ha una quantità in inventario.

> [!NOTE]
> Per una posizione di magazzino, potrebbe essere necessario creare prelievi prima di poter registrare l'ordine di assemblaggio. Per indagare su ciò, rivedere il setup per il prelievo nella pagina **Scheda ubicazione**. Per ulteriori informazioni vedere [Impostare articoli e ubicazioni per gli stoccaggi e i prelievi guidati](warehouse-how-to-set-up-items-for-directed-put-away-and-pick.md).

### <a name="handle-inventory-quantities-that-are-allocated-to-demand"></a>Gestire le quantità di inventario assegnate alla domanda

Idealmente, l'inventario per l'articolo originale dovrebbe essere a zero dopo aver trasferito le quantità di magazzino. Tuttavia, possono esserci ordini, prospetti e registrazioni in sospeso (vedere la tabella seguente) che richiedono ancora una quantità dell'articolo originale. La quantità potrebbe anche essere bloccata da una prenotazione o dalla tracciabilità articolo.

**Esempio** Ci sono 1000 pezzi in inventario e 20 pezzi sono riservati per un ordine di vendita non ancora spedito. In tal caso, si potrebbe decidere di conservare i 20 pezzi nel vecchio articolo in modo da poter evadere l'ordine in sospeso.

> [!NOTE]
> Esistono aree funzionali che possono influire sulla quantità, come elencato nella tabella seguente, quindi può essere complicato trovare la quantità corretta. Per sicurezza, usando l'esempio sopra, è possibile scegliere di conservare 100 pezzi e trasferire i restanti 900 pezzi come alternativa. Un altro modo per farlo sarebbe quello di elaborare i documenti e le registrazioni in modo che ne rimangano solo pochi gestibili. Un'altra alternativa è quella di trasferire l'intera quantità al nuovo articolo e quindi trasferirne una parte indietro nell'articolo originale usando l'ordine di assemblaggio.

La tabella seguente elenca le aree funzionali in cui potrebbero esserci quantità in sospeso.

|Area  |Dove cercare quantità in sospeso  |
|---------|---------|
|Vendite |Documenti di vendita, inclusi ordini, ordini di reso, fatture, offerte, ordini programmati e note di credito |
|Inventario |Registrazioni magazzino, prenotazioni, tracciabilità articoli e prospetto costi standard |
|Acquisti |Documenti di acquisto, inclusi ordini, ordini di reso, fatture, offerte, ordini programmati e note di credito |
|Pianificazione |Richiesta di approvvigionamento, prospetto di pianificazione e pianificazione degli ordini |
|Warehouse |Ordini di trasferimento, spedizioni warehouse, registrazioni di warehouse e prelievi warehouse, stoccaggi e movimenti, prelievi e stoccaggi interni e prospetti di creazione collocazione |
|Assemblaggio |Documenti di assemblaggio, inclusi ordini, ordini di reso e ordini programmati |
|Commesse |Righe di pianificazione progetto e righe di registrazione progetto |
|Assistenza |Documenti di assistenza e contratti di assistenza |
|Produzione |Ordini di produzione (pianificati, confermati e rilasciati) |

### <a name="block-the-original-item-from-further-use"></a>Bloccare l'articolo originale da ulteriore utilizzo

Quando l'inventario per l'articolo originale è zero, è possibile bloccare l'articolo per impedirne l'utilizzo in nuove transazioni. Per bloccare l'articolo, nella pagina **Scheda articolo** attivare l'interruttore **Bloccato**. Per ulteriori informazioni, vedere [Bloccare gli articoli per la vendita o l'acquisto](inventory-how-block-items.md).

## <a name="summary"></a>Riepilogo

La modifica del metodo di costing per gli articoli che sono stati utilizzati nelle transazioni è un processo e non un'azione standard in [!INCLUDE[prod_short](includes/prod_short.md)]. È possibile utilizzare i passaggi descritti in questo argomento come modello per il processo.

Il processo può richiedere molto tempo perché ci sono diversi passaggi manuali. Tuttavia, dedicare del tempo per completarlo riduce l'impatto degli errori sulla contabilità generale.

Si consiglia quanto segue:

1. Valutare la fattibilità del processo prendendo uno, o forse alcuni, articoli rappresentativi durante l'intero processo.
2. Prendere in considerazione di contattare un partner esperto che può aiutare nel processo.

## <a name="see-also"></a>Vedere anche

[Dettagli di progettazione: Metodi di costing](design-details-costing-methods.md)  
[Sintesi](design-details-inventory-costing.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
