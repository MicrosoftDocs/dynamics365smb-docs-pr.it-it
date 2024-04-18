---
title: Utilizzare documenti elettronici nel processo di acquisto
description: Scopri come utilizzare la funzionalità dei documenti elettronici correlata a fatture e ordini di acquisto.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'electronic document, electronic invoice, e-document, e-invoice, receive, purchase, matching, mapping, Copilot'
ms.search.form: '50, 51, 138, 6103, 6133, 6121, 6167, 9307, 9308'
ms.date: 04/03/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# <a name="use-e-documents-in-the-purchases-process"></a>Utilizzare documenti elettronici nel processo di acquisto

Puoi utilizzare documenti elettronici configurati con documenti di acquisto.

Puoi utilizzare i seguenti documenti di acquisto con la funzionalità dei documenti elettronici:  

- Fatture di acquisto
- Ordini di acquisto (dalla versione 24.0)
- Note di credito di acquisto
- Registrazioni COGE

> [!NOTE]
> Da [!INCLUDE[prod_short](includes/prod_short.md)] versione 24.0, è possibile connettere gli **Ordini di acquisto** con i **Documenti elettronici** ricevuti.  

## <a name="e-documents-in-purchases"></a>Documenti elettronici per gli acquisti

La ricezione dei documenti elettronici di acquisto in Dynamics 365 Business Central può essere effettuata come processo batch o manualmente.  

### <a name="how-to-set-up-vendors-to-work-with-different-purchase-documents"></a>Come impostare i fornitori per utilizzare documenti di acquisto differenti

Segui i passaggi per configurare i fornitori affinché siano utilizzati correttamente con le fatture elettroniche in entrata: 

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immetti **Fornitori**, quindi seleziona il collegamento correlato. 
2. Scegli il fornitore da configurare.   
3. Nella Scheda dettaglio **Carico**, trova il campo **Ricevi documento elettronico a** per specificare il documento di acquisto predefinito da generare dal documento elettronico ricevuto. 

> [!NOTE]
> Nel campo **Ricevi documento elettronico da**, gli utenti possono selezionare una **Fattura di acquisto** o un **Ordine di acquisto** in base a ciò che vorrebbero creare dalla fattura elettronica ricevuta. Questa selezione non influisce sulla creazione di documenti correttivi; in entrambi gli scenari il sistema genererà una **Nota di credito**.  

> [!NOTE]
> Se l'utente sceglie l'opzione **Ordine di acquisto** nel campo **Ricevi documento elettronico a** , il sistema tenterà di aggiornare uno degli ordini di acquisto esistenti, ma se l'ordine di acquisto per un fornitore nel **Documento elettronico** ricevuto non esiste, [!INCLUDE[prod_short](includes/prod_short.md)] creerà un nuovo **Ordine di acquisto**, utilizzando lo stesso approccio utilizzato per creare le nuove **Fatture di acquisto** descritte in questa pagina più avanti.  

4. Scegli una delle opzioni che desideri utilizzare per il fornitore selezionato. 
5. Chiudere la pagina.   

### <a name="to-work-with-purchase-invoices"></a>Per utilizzare fatture di acquisto

#### <a name="run-the-batch-job"></a>Eseguire il processo batch

> [!NOTE]
> Questo processo batch è usato per la raccolta automatizzata delle fatture in entrata. Può funzionare solo in un paese o in un'area geografica in cui esiste la funzionalità.  

Ogni volta che si seleziona una **Coda processi** da eseguire, se il servizio esterno ha fatture in entrata inviate dal fornitore, il sistema raccoglie e importa tali fatture. Per completare il processo, segui i passaggi seguenti. 

1. Al termine dell'esecuzione del processo batch, le fatture appena importate vengono elencate nella pagina **Documenti elettronici**, insieme alle informazioni dettagliate di base. 
2. Per visualizzare maggiori dettagli, aprire un documento elettronico specifico.   
3. Se non sono presenti errori o problemi nel documento elettronico, il campo **Record** esegue il mapping del numero di documento della fattura di acquisto, se questa è configurata nella pagina **Scheda fornitore** (creata automaticamente dal sistema). Seleziona il collegamento per aprire il documento.
 
> [!NOTE]
> Questo documento creato dal sistema non è il documento registrato. 

1. Per accedere direttamente al documento di acquisto, seleziona il campo **Record**. Dopo aver aperto la pagina **Fattura di acquisto**, controlla il documento. Quindi, se tutto è corretto, registra il documento.  
1. Quando registri il documento di acquisto, il campo **Record** nel **Documento elettronico** viene aggiornato da **Fattura** a **Fattura di acquisto** e il numero del documento di acquisto registrato è disponibile. Puoi selezionare il numero per aprire la fattura di acquisto registrata. 

I dettagli sui log sono gli stessi del processo di vendita dei documenti elettronici.  

Poiché gli errori nel processo di vendita sono per lo più correlati alla disponibilità del servizio, il documento in entrata può contenere molteplici ragioni. Il motivo più comune di un errore è che il sistema non riesce a riconoscere le righe del documento elettronico ricevuto dal fornitore. Pertanto, non puoi immettere righe nella fattura di acquisto. 

Vi sono due errori comuni:  

- Se vuoi utilizzare questa riga specifica della fattura fornitore registrata direttamente nel conto di contabilità generale (C/G), devi aver configurato correttamente il valore **Mapping testo**. Per ignorare questo errore se desideri utilizzare conti C/G, seleziona **Mappa testo a conto** per creare un mapping specifico del valore **Mapping testo** con il valore **N. conto dare** che vuoi utilizzare. 
- Se vuoi tenere traccia dell'inventario e utilizzare le righe della fattura fornitore per compilare gli articoli nelle righe del documento, devi aver configurato correttamente il valore **Nr. riferimento articolo** . Per ignorare questo errore, mappa l'articolo esterno ai tuoi numeri di articolo utilizzando la lista dei riferimenti agli articoli. Per maggiori informazioni, vedi [Usare i riferimenti agli articoli](inventory-how-use-item-cross-refs.md). 

Dopo aver corretto gli errori e gli avvisi, puoi specificare manualmente quando il sistema deve creare una fattura di acquisto in base alla tua impostazione selezionando **Crea documento**.   

#### <a name="manually-import-invoices"></a>Importare manualmente le fatture

Per importare manualmente documenti elettronici esterni, procedi come segue:

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](media/ui-search/search_small.png "Dimmi cosa vuoi fare"), immetti **Servizio documenti elettronici**, quindi seleziona il collegamento correlato. 
2. Nella pagina **Servizio documenti elettronici** seleziona il servizio attivo.   
3. Seleziona **Ricevi** e carica il file del documento elettronico che hai ricevuto dal fornitore. 
4. Se viene visualizzato un messaggio di errore, apri il documento elettronico per risolvere i problemi. 
5. Una volta risolti i problemi, nel gruppo **Importa manualmente**, seleziona **Crea documento**.  
6. Dopo che il documento è stato creato in [!INCLUDE[prod_short](includes/prod_short.md)], l'utilizzo di un processo batch non modifica il modo in cui lo visualizzi. 

### <a name="e-documents-with-purchase-orders"></a>Domande elettronici con ordini di acquisto

#### <a name="to-link-purchase-orders-with-the-received-e-documents"></a>Per collegare ordini di acquisto con i documenti elettronici ricevuti

Se il tuo **Fornitore** ha configurato il campo **Ricevi documento elettronico a** per l'utilizzo con **Ordini di acquisto**, una volta creato il documento elettronico in [!INCLUDE[prod_short](includes/prod_short.md)] (manualmente o da un punto finale esterno), [!INCLUDE[prod_short](includes/prod_short.md)] effettuerà quanto segue:  

1. Se l'**Ordine di acquisto** per questo particolare fornitore esiste e c'è un numero di ordine di acquisto nel file di ricezione di **Documenti elettronici**, [!INCLUDE[prod_short](includes/prod_short.md)] collegherà automaticamente questo **Documento elettronico** con l'**Ordine di acquisto** menzionato e lo **Stato del documento** di questo **Documento elettronico** sarà **In corso** e lo **Stato del documento elettronico** nella pagina secondaria **Stato servizio** sarà **Ordine collegato**. Questo collegamento sarà visibile nel campo **Documento** in questo specifico **Documento elettronico**. Se devi modificare l' **Ordine di acquisto** collegato automaticamente, puoi farlo utilizzando l'azione **Aggiorna collegamento ordine di acquisto** e scegli manualmente uno degli ordini di acquisto esistenti per questo fornitore. Puoi farlo solo prima di abbinare le righe tra il **Documento elettronico** e l'**Ordine di acquisto**.  
2. Se l'**Ordine di acquisto** per questo particolare fornitore esiste ma non è presente un numero di ordine di acquisto nel file di ricezione di **Documenti elettronici**, [!INCLUDE[prod_short](includes/prod_short.md)] offrirà la possibilità di scegliere uno degli ordini di acquisto esistenti quando e se hai caricato manualmente questo documento, aprendo l'elenco **Ordini di acquisto** con solo ordini per il fornitore con il **Documento elettronico**, dove devi selezionare l'**Ordine di acquisto** che desideri e selezionare **OK**. Se non hai selezionato l **Ordine di acquisto** corretto o hai ricevuto il **Documento elettronico** automaticamente dall'endpoint esterno utilizzando la **Coda processi**, il nuovo **Documento elettronico** non sarà collegato ad alcun documento di acquisto e lo **Stato del documento** sarà **Errore** e lo **Stato del documento elettronico** nella pagina secondaria **Stato servizio** sarà **Errore di elaborazione documenti importati**. Per completare il collegamento con l'**Ordine di acquisto**, seleziona l'azione **Aggiorna collegamento ordine di acquisto** e scegli uno degli ordini di acquisto esistenti per questo fornitore. 
3. Se l'**Ordine d'acquisto** per questo particolare fornitore non esiste al momento della creazione del nuovo **Documento elettronico**, [!INCLUDE[prod_short](includes/prod_short.md)] creerà un nuovo **Ordine di acquisto**, utilizzando lo stesso modello di creazione già esistente per le nuove **Fatture di acquisto**. Lo **Stato del documento** di questo **Documento elettronico** sarà **Elaborato**, e lo **Stato del documento elettronico** nella pagina secondaria **Stato del servizio** sarà **Documento importato creato**. Questo collegamento sarà visibile nel campo **Documento** in questo specifico **Documento elettronico**.   

#### <a name="matching-lines-from-received-e-document-with-purchase-order"></a>Righe corrispondenti del documento elettronico ricevuto con ordine di acquisto

Puoi abbinare i documenti elettronici ricevuti alle righe degli ordini di acquisto da due aree diverse, ovvero la pagina **Documento elettronico** o la pagina **Ordine di acquisto**. Il modo più semplice di individuare l'**Ordine di acquisto** collegato è usare il riquadro **Ordini di acquisto collegati** come parte di **Attività documento elettronico**. Tutti i documenti non collegati possono essere trovati utilizzando il riquadro **Attesa di fatture elettroniche di acquisto** dove hai un elenco di **Documenti elettronici** che devi rivedere.  

> [!NOTE]
> L'**Attività documento elettronico** con questi due riquadri si trova nelle **Gestioni ruolo utente** seguenti: Valutazione manager aziendale, Manager aziendale, Contabile, Gestione inventario e Spedizione e carico.  

> [!NOTE]
> Se la percentuale di IVA è diversa tra il documento in entrata e la percentuale IVA della società, i documenti corrispondenti non possono essere utilizzati in un ambiente per più paesi.  

##### <a name="matching-lines-from-purchase-order"></a>Righe corrispondenti nell'ordine di acquisto

Puoi abbinare le righe dell'elenco **Ordini di acquisto** o di uno degli **Ordini di acquisto** aperti. Per iniziare, utilizza i seguenti passaggi:  

1. Seleziona il riquadro **Ordini di acquisto collegati** nella tua Gestione ruolo utente se è presente un numero. 
2. Poiché vi sono due opzioni per l'abbinamento, scegline una: 

    1. Se vuoi abbinare le righe dell'elenco **Ordini di acquisto**, seleziona la riga **Ordine di acquisto** che vuoi abbinare e scegli l'azione **Mappa righe documento elettronico**.  
    2. Se vuoi prima aprire l'**Ordine di acquisto**, apri il documento e quindi scegli l'azione **Mappa righe documento elettronico**. 

3. Poiché entrambe le opzioni hanno lo stesso processo, aprirai la pagina **Corrispondenza ordine di acquisto** con il seguente contenuto: 

    1. Nell'intestazione puoi trovare le seguenti informazioni, che possono aiutarti a mappare più facilmente le righe: 

    |Nome campo |Descrizione |
    |--------|-----------------|
    |Nome fornitore |Specifica il nome del fornitore nel documento elettronico. |
    |Nr. documento elettronico |Specifica il numero di documento elettronico collegato. |
    |Data documento elettronico |Specifica la data del documento elettronico collegato.  |
    |Importo documento elettronico |Specifica l'importo totale del documento elettronico collegato, IVA inclusa. |

    2. Nelle righe puoi trovare quelle importate dal file di **Documenti elettronici** sul lato sinistro e le righe dell'**Ordine di acquisto** esistente sul lato destro.  
    3. Tutte le righe su entrambi i lati hanno numeri e descrizioni di articoli, insieme al **Costo unitario diretto** e alla **% sconto riga**.  
    4. Sul lato **Righe importate**, puoi anche individuare il campo **Quantità** come quantità totale dalla fattura elettronica e il campo **Quantità corrispondente** che specifica la quantità già abbinata alle righe dell'ordine di acquisto. 
    5. Sul lato **Righe di ordini di acquisto**, puoi anche trovare la **Quantità disponibile** come quantità che può essere abbinata a questa riga (quantità ricevuta, ma non fatturata) e **Qtà da fatturare**, specificando la quantità già abbinata a questa riga. 
    6. Per abbinare le righe, seleziona le righe su entrambi i lati che desideri abbinare e scegli l'azione **Corrispondenza manuale**. Le righe abbinate verranno contrassegnate in verde. 
    7. È possibile eseguire l'abbinamento uno a uno, ma anche molti a uno o uno a molti, selezionando più righe su un lato o sull'altro lato prima di scegliere l'azione **Corrispondenza manuale**. 
    8. Puoi anche scegliere l'azione **Corrispondenza automatica** per abbinare automaticamente tutte le righe con lo stesso **Tipo**, **N.**, **Prezzo unitario**, **Sconto** e **Unità di misura**. 
    9. Se commetti un errore, puoi scegliere l'azione **Rimuovi corrispondenza** per rimuovere le righe abbinate sul lato dell'ordine di acquisto o scegli l'azione **Ripristina corrispondenza** per ripristinare tutto ciò che è abbinato. 
    10. Se il tuo **Documento elettronico** ha molte righe, durante il processo di abbinamento puoi scegliere l'azione **Mostra righe in sospeso** per rimuovere tutte le righe del documento elettronico se sono già completamente abbinate. Se hai bisogno di vedere tutte le righe, puoi sempre scegliere l'azione **Mostra tutte le righe** . 

4. Una volta terminato l'abbinamento, devi scegliere l'azione **Applica all'ordine di acquisto**.   
5. Una volta applicato l'abbinamento all'**Ordine di acquisto**, [!INCLUDE[prod_short](includes/prod_short.md)] aggiornerà i seguenti campi:

    1. **Nr. fattura fornitore** e **Data documento** nell'intestazione del documento verranno aggiornati con i valori del documento elettronico che hai ricevuto e collegato. 
    2. La **Qtà. da fatturare** nelle righe verrà aggiornata con i valori della colonna **Qtà da fatturare** nella pagina **Corrispondenza ordine di acquisto** in base alla corrispondenza trovata. 
    3. Ora puoi registrare il documento, scegliendo l'azione **Registra**.  
    4. Una volta registrato il documento, il campo **Documento** nella pagina **Documento elettronico** cambierà il valore e sarà correlato alla **Fattura di acquisto registrata**. 
    5. Chiudere la pagina.  

> [!IMPORTANT]
> Per impostazione predefinita, puoi abbinare solo le righe con lo stesso importo totale in entrambi i documenti. Ciò significa che il **Costo unitario diretto** insieme alla riga applicata **% di sconto** devono essere gli stessi, in quanto in un documento puoi avere un importo senza sconto ed un altro con sconto.  

Se desideri aggiungere un po' di tolleranza e consentire la differenza tra le righe in **Fattura elettronica** e **Ordine di acquisto**, segui i passi:   

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](media/ui-search/search_small.png "Dimmi cosa vuoi fare"), immetti **Setup contabilità fornitori**, quindi seleziona il collegamento correlato.  
2. Desideri consentire la tolleranza nel campo **% differenza corrispondenza documento elettronico**, specificando la percentuale massima consentita della differenza di costo durante l'abbinamento del **Documento elettronico** in entrata e la riga dell'**Ordine di acquisto**. 
3. Questa impostazione verrà applicata a tutte le righe corrispondenti, ma ancora una volta considerando la tolleranza per l'importo totale, come per il **Costo unitario diretto** insieme alla **% sconto riga** applicata.  
4. Chiudere la pagina.   

##### <a name="to-match-lines-from-e-document"></a>Per abbinare righe del documento elettronico

Puoi abbinare le righe nella pagina **Documento elettronico**. Per iniziare, utilizza i seguenti passaggi:  

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immetti **Servizi documenti elettronici**, quindi seleziona il collegamento correlato. 
2. Seleziona il **Documento elettronico** che vuoi abbinare.   
3. Scegli l'azione **Abbina ordine d'acquisto** per aprire la pagina **Corrispondenza ordine di acquisto**.  
4. Ripeti gli stessi passaggi che hai utilizzato quando hai iniziato ad eseguire l'abbinamento negli ordini di acquisto.

### <a name="e-document-matching-assistance-copilot"></a>Copilota Assistenza per la corrispondenza dei documenti elettronici

> [!NOTE]
> Attualmente, il copilota **Assistenza per la corrispondenza dei documenti elettronici** è nello stato di anteprima pronto per la produzione ed è disponibile a livello globale tranne che nel Canada. Tuttavia, funziona solo con la lingua inglese. 

> [!NOTE]
> Copilot è il assistente basato sull'intelligenza artificiale che aiuta le persone all'interno dell'organizzazione a liberare la propria creatività e ad automatizzare le attività noiose. Il copilota **Assistenza per la corrispondenza dei documenti elettronici** aiuta gli utenti ad abbinare facilmente le fatture elettroniche ricevute e le righe degli ordini di acquisto esistenti, utilizzando il modello LLM per trovare righe corrispondenti tra due documenti diversi. 

#### <a name="to-activate-the-copilot"></a>Per attivare il copilota

Nel caso in cui non hai attivato il copilota **Assistenza per la corrispondenza dei documenti elettronici**, devi farlo manualmente. Per abilitare il copilota **Assistenza per la corrispondenza dei documenti elettronici**, segui i passaggi: 

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immetti **Funzionalità di Copilot e IA**, quindi seleziona il collegamento correlato. 
2. Nell'elenco delle funzionalità, seleziona **Assistenza per la corrispondenza dei documenti elettronici** e modifica lo stato in **Attivo**.  

Una volta attivato il copilota, puoi iniziare a usarlo.

#### <a name="use-the-e-document-matching-assistance-copilot"></a>Utilizzare il copilota Assistenza per la corrispondenza dei documenti elettronici

Se il copilota è attivato, le azioni esistenti **Mappa righe documento elettronico** negli ordini acquistati e **Abbina ordine di acquisto** nella pagina **Documento elettronico** avranno icone diverse, che simboleggiano la funzionalità dell'intelligenza artificiale. Puoi eseguire queste azioni (assolutamente identiche a quelle degli esempi precedenti dall'elenco degli ordini di acquisto) da uno degli **Ordini d'acquisto** o dal **Documento elettronico**. Tutti i passaggi per l'esecuzione sono uguali, ma quando esegui questa azione, il risultato sarà diverso e dovrai seguire i passaggi:  

1. Scegli l'azione **Mappa righe documento elettronico** o **Abbina ordine di acquisto** per i documenti già collegati.  
2. Puoi notare che il prompt **Abbina righe dell'ordine del documento elettronico con Copilot** funziona e hai la pagina **Corrispondenza ordine di acquisto** in background. Ciò significa che è in esecuzione lo stesso processo ma con il supporto automatico di **Copilot**, che esegue il processo di abbinamento al posto tuo. 
3. Dopo alcuni secondi, **Abbina righe dell'ordine del documento elettronico con Copilot** suggerirà le righe da abbinare con alcuni dettagli aggiuntivi: 

    1. Nell'intestazione del prompt puoi trovare le seguenti informazioni: 

    |Nome campo |Descrizione |
    |--------|-----------------|
    |Corrispondenza automatica | Specifica il numero di corrispondenze proposte automaticamente. Ciò si basa su un confronto di stringhe e se si verifica una sovrapposizione dell'80% o più delle descrizioni, il sistema abbinerà automaticamente queste descrizioni senza utilizzare le funzionalità GPT. |
    |Corrispondenze di Copilot | Specifica il numero di corrispondenze proposte da Copilot utilizzando sia il confronto delle stringhe che quello semantico. |
    |Nr. documento elettronico | Specifica il numero di documento elettronico collegato. |
    |Importo totale fattura, IVA esclusa | Specifica l'importo totale della fattura IVA esclusa. |
    |Corrispondenza importo totale IVA inclusa | Specifica l'importo corrispondente, IVA esclusa. |
    
    2. Se tutte le righe corrispondono, vedrai il testo verde nell'angolo in alto a destra: **Tutte le righe (100%) corrispondono. Esaminare le corrispondenze proposte**.  
    3. Nelle righe **Proposta corrispondente** puoi trovare le seguenti informazioni:  

    |Nome campo |Descrizione |
    |--------|-----------------|
    |Nr. righe documento elettronico | Specifica il numero di riga del documento elettronico (presente nel file del documento elettronico originale). |
    |Descrizione riga documento elettronico | Specifica la descrizione della riga del documento elettronico (presente nel file del documento elettronico originale). |
    |Quantità corrispondente | Specifica la quantità che verrà applicata alla riga dell'ordine di acquisto. |
    |Proposta | Specifica l'azione proposta dall'IA e queste azioni suggerite sono correlate alla corrispondenza delle righe dell'ordine di acquisto. |

    4. Tutte le righe completamente suggerite e corrispondenti sono contrassegnate in verde. Se c'è qualche problema, ad esempio un prezzo diverso, ma nell'intervallo di prezzo consentito, questa riga sarà in giallo e se c'è qualche similarità tra i campi della descrizione ma la differenza di prezzo è maggiore del consentito, sarà in rosso. 
    5. Se non sei soddisfatto di alcuni suggerimenti, puoi eliminarli utilizzando l'azione **Elimina riga**.  
    6. Se desideri visualizzare le corrispondenze delle proposte, puoi selezionare il collegamento nella colonna **Proposta** per aprire la pagina **Dettagli della corrispondenza del documento elettronico**. 
    7. Nella pagina **Dettagli della corrispondenza del documento elettronico** puoi confrontare i dettagli del **Documento elettronico** e dell'**Ordine di acquisto**, per essere sicuro dell'abbinamento suggerito prima di confermarlo. 
    8. Dopo la revisione, chiudi la pagina.   

4. Se non sei soddisfatto della maggior parte dei suggerimenti o se non desideri utilizzare la funzionalità **Abbina righe dell'ordine del documento elettronico con Copilot**, seleziona **Ignora** e puoi continuare con l'abbinamento manuale come spiegato in precedenza.  
5. Se vuoi conservare i suggerimenti, scegli il pulsante **Mantieni** e il sistema salverà tutti i suggerimenti forniti da **Copilot**.  
6. [!INCLUDE[prod_short](includes/prod_short.md)] chiuderà il prompt di Copilot e le righe nella pagina **Corrispondenza ordine di acquisto** verranno contrassegnate in verde, poiché sono già abbinate.  
7. Da questo momento, puoi continuare a lavorare mentre esegui l'abbinamento manuale, e ciò significa che puoi rimuovere corrispondenze e corrispondenze manuali, ripristinare la corrispondenza o, se non ci sono modifiche che desideri apportare, scegliere l'azione **Applica all'ordine di acquisto** e continuare a lavorare con l'**Ordine di acquisto**. 

> [!NOTE]
> Se lo desideri, puoi scegliere di nuovo l'azione **Confronta con Copilot** nella pagina **Corrispondenza ordine di acquisto**, ma in questa In questo caso, ti verrà chiesto se desideri sovrascrivere le corrispondenze esistenti, poiché tutte le righe sono già state abbinate.  

> [!NOTE]
> L'analisi dei prezzi/costi e il controllo della quantità disponibile fanno parte dell'attività di pre-elaborazione.   

## <a name="overview-of-e-document-statuses"></a>Panoramica degli stati dei documenti elettronici

Per avere una migliore panoramica di tutti i documenti elettronici nella società, puoi selezionare la gestione ruolo utente **Contabile** dove esistono gli stati dei documenti elettronici. Lì puoi trovare le attività relative ai documenti elettronici che hanno i seguenti stati:

- **Documenti elettronici in entrata:**

    - Elaborato
    - In corso
    - Errore


## <a name="see-also"></a>Vedere anche

[Come impostare documenti elettronici in [!INCLUDE[prod_short](includes/prod_short.md)]](finance-how-setup-edocuments.md)    
[Come utilizzare il documento elettronico nel processo di vendita](finance-how-use-edocuments.md)   
[Come estendere documenti elettronici in [!INCLUDE[prod_short](includes/prod_short.md)]](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments)    
[Gestione contabile](finance.md)    
[Fatturare le vendite](sales-how-invoice-sales.md)    
[Registrare gli acquisti con le fatture e gli ordini di acquisto](purchasing-how-record-purchases.md)    
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

