---
title: Tabella delle voci di prenotazione - Funzionalità che aggiornano la tabella delle voci di prenotazione | Microsoft Docs
description: In questa sezione vengono fornite indicazioni utili per comprendere e risolvere i problemi di incoerenza dei dati nella tabella di immissione delle prenotazioni.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/26/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Tavolo di ingresso per le prenotazioni - Introduzione

Questo whitepaper tecnico fornisce indicazioni utili per comprendere e risolvere i problemi di incoerenza dei dati nella tabella  *Inserimento prenotazione* (Tabella 337) Microsoft Dynamics NAV. La prima parte è un'introduzione alle funzionalità che generano o modificano i dati in questa tabella. Copre anche diversi campi nella tabella  *Inserimento prenotazione* che vale la pena sottolineare in relazione a queste funzionalità. La seconda parte illustra attraverso esempi come le voci nella tabella  *Voci di prenotazione* vengono generate, eliminate o modificate quando vengono elaborati gli ordini di trasferimento o eseguite le funzionalità di pianificazione.

La tabella  *Inserimento prenotazione* viene utilizzata per gestire e memorizzare le informazioni relative alla prenotazione, al monitoraggio degli articoli e al monitoraggio degli ordini.

Quando si gestisce il monitoraggio degli articoli con registrazione parziale, la tabella funziona insieme alla tabella  *Specifiche di monitoraggio* (Tabella 336). I dati immessi dall'utente nella pagina  **Righe di tracciabilità articolo**  vengono creati in una versione temporanea della tabella 336 e salvati nella tabella 337 e nella tabella delle specifiche di tracciabilità quando la pagina viene chiusa.

In termini generali, i dati generati nella tabella  *Inserimento prenotazione* dipenderanno dalle funzionalità utilizzate e dai parametri selezionati nell'elemento scheda. Questi includono:

- Politica di monitoraggio degli ordini
- Politica di prenotazione
- Funzionalità di pianificazione eseguite
- Politica di riordino e produzione
- Parametri di pianificazione sull'articolo o sull'unità di stoccaggio scheda
- Codice tracciabilità articolo

## Funzionalità che aggiornano la tabella di inserimento delle prenotazioni

### Politica di monitoraggio degli ordini

Se il campo  **Criterio di tracciamento degli ordini** di un articolo è impostato su Nessuno, Microsoft Dynamics NAV non creerà mai voci di prenotazione nella tabella  *Voce di prenotazione*, a meno che non venga eseguito il Piano di modifica netta o il Piano rigenerativo, la Prenotazione o il Tracciamento articolo. Inoltre, se non è abilitato il monitoraggio degli ordini, è possibile avere voci di prenotazione quando si utilizzano le policy Produzione su ordinazione o Assemblaggio su ordinazione.

Puoi valutare di impostare la  **Politica di tracciamento degli ordini** su Nessuno se non hai bisogno di tracciare al volo una domanda rispetto a una fornitura o viceversa. Il monitoraggio dell'offerta rispetto alla domanda è gestito dalla funzionalità di monitoraggio degli ordini o dal motore di pianificazione. Ti sconsigliamo di utilizzare il monitoraggio degli ordini insieme alla funzionalità di pianificazione.

Quando imposti il campo  **Criterio di tracciamento dell'ordine** su Solo tracciamento, Microsoft Dynamics NAV verranno sempre create voci nella tabella 337 ogni volta che viene creato un ordine per l'articolo, ma lo  **Stato della prenotazione** nella tabella 337 non è sempre impostato rigorosamente su Tracciamento. Consideriamo il seguente scenario:

> [!NOTE]  
> Per tutti gli esempi la data di lavoro è impostata su 23/01/2014 (GG/MM/AAAA). 
  
1. Crea un articolo con il campo  **Criteri di tracciamento degli ordini** impostato su Solo tracciamento.  
1. Creare un ordine di acquisto. Microsoft Dynamics NAV creerà una voce di prenotazione con lo **stato di prenotazione** di Surplus, poiché l'ordine di acquisto non è ancora stato assegnato a una domanda.
1. Creare un ordine di vendita. Microsoft Dynamics NAV creerà ora un'altra voce di prenotazione con uno **stato di prenotazione** di monitoraggio.

Lo **stato di prenotazione** creato in passaggio 2 verrà aggiornato in Monitoraggio; questa operazione viene gestita Microsoft Dynamics NAV automaticamente. Questo concetto è chiamato Tracciamento Dinamico.
Impostando il campo  **Criterio di tracciamento dell'ordine** sull'articolo su Solo tracciamento, un utente finale può utilizzare la funzionalità di tracciamento dell'ordine per ottenere una panoramica della fornitura a cui è assegnata la domanda e viceversa.

> [!NOTE]  
> La funzionalità di monitoraggio non sostituisce la funzionalità di pianificazione, che considera tutti gli articoli, le richieste e le forniture insieme per fornire proposte di pianificazione ottimali per ottimizzare i livelli di servizio clienti e bilanciare i livelli di inventario.

### Politica di prenotazione

Una prenotazione è composta da una coppia di record nella tabella  *Voce di prenotazione* con uno  **Stato di prenotazione** di Prenotazione, che condivide lo stesso numero di voce. Un record ha il campo Positivo abilitato e punta alla fornitura. L'altro record ha il campo  **Positivo** non abilitato e punta alla domanda. I campi **Tipo di origine**, **N. rif. origine** e **ID origine** evidenziano la prenotazione collegare tra domanda e offerta.

Le informazioni nel campo  **Tipo di origine** sono la tabella a cui è correlato il campo  **Numero di voce di prenotazione** . Ad esempio, se si tratta di una voce di domanda (negativa), potrebbe essere la tabella  *Ordine di vendita* (Tabella 37) o il  *Componente di pianificazione* (Tabella 99000829).

Il campo  **ID sorgente** contiene l'ID del documento nella tabella a cui fa riferimento il Tipo sorgente.

Numero di riferimento della fonte. **·** Campo contiene un numero di riferimento per la linea, che la prenotazione **Numero di iscrizione**  è relazionato a. Se la voce è correlata a una riga di vendita o di acquisto, a una riga di giornale o a una riga di richiesta, le informazioni in questo campo vengono copiate dal **Numero di riga** . Se è correlato a una voce nella tabella  *Movimento contabile articolo* (Tabella 32), le informazioni in questo campo vengono copiate dal campo  **Numero voce** della tabella  *Movimento contabile articolo* .

Quando si utilizza l'opzione di politica di prenotazione Always in combinazione con il tracciamento dell'ordine, entrambi sono normalmente sincronizzati. Tuttavia, quando la prenotazione viene rimossa o la data di ricezione della fornitura viene spostata in avanti oltre la data di scadenza della domanda, il tracciamento dell'ordine verrà rimosso. Potrebbe anche essere visualizzato un messaggio di errore in cui viene chiesto cosa fare con le prenotazioni esistenti. Microsoft Dynamics NAV  Questo scenario è illustrato nel seguente esempio:

1. Crea un nuovo elemento chiamato COMP. Impostare i seguenti campi:
  - **Sistema di rifornimento**: Acquisto
  - **Politica di monitoraggio degli ordini**: solo monitoraggio
  - **Riserva**: Sempre
2. Crea un secondo elemento chiamato FG. Impostare i seguenti campi:
  - **Sistema di rifornimento**: Ordine di produzione
  - **Politica di monitoraggio degli ordini**: solo monitoraggio
  - **Riserva**: Sempre
3. Crea un secondo elemento chiamato FG. Impostare i seguenti campi:
  - **Oggetto**: COMP
  - **Quantità per**: 1
4. Certificare il numero della distinta base di produzione BOM FG e assegnarlo all'articolo FG.
5. Creare un ordine di acquisto. Impostare i seguenti campi:
  - **Oggetto**: COMP
  - **Quantità**: 10
  - **Codice posizione**: BLU
  - **Data di ricezione prevista**: 24/01/2014
6. Creare un ordine di vendita. Impostare i seguenti campi:
  - **Data di spedizione**: 14/02/2014
  - **Codice posizione**: BLU
  - **Articolo**: COMP
  - **Quantità**: 10

> [!NOTE]  
> È stata eseguita la prenotazione automatica tra l'ordine di acquisto e quello di vendita. Inoltre, è stato creato un sistema di tracciamento degli ordini tra gli ordini di acquisto e quelli di vendita.

7. Creare un ordine di produzione rilasciato manualmente. Impostare i seguenti campi:
  - **Articolo**: 14/02/2014
  - **Quantità**: 10
  - **Posizione**: BLU
  - **Data di scadenza**: 02/01/2014
8. Nella scheda **Home**, nel gruppo Processo, seleziona **Aggiorna ordine di produzione**.
9. Aprire l'elenco dei componenti e cercare l'articolo COMP.

> [!NOTE]  
>  Microsoft Dynamics NAV non crea alcuna prenotazione o tracciamento degli ordini. Il motivo è che esiste già una prenotazione per l'ordine di vendita creato in passaggio 6.

Supponiamo che, per motivi aziendali, l'articolo sia necessario con maggiore urgenza nell'ordine di produzione rilasciato creato in passaggio 7. Quindi, nei passaggi successivi, Annulla la prenotazione dall'ordine di vendita creato in passaggio 6 e notiamo come viene gestito il monitoraggio dell'ordine.

10. Cercare l'ordine di vendita per l'articolo COMP da passaggio 6 e Annulla la prenotazione.
11. Aprire l'ordine di acquisto da passaggio 5 e notare che ora è stato creato il tracciamento dell'ordine tra l'ordine di acquisto e il componente necessario dall'ordine di produzione rilasciato.
12. Ricreare la prenotazione tra il componente necessario dall'ordine di produzione rilasciato e la fornitura dall'ordine di acquisto in passaggio 5.

> [!NOTE]  
> La prenotazione non viene ricreata, è necessario Fatto manualmente.

13. Modificare il campo  **Data di ricezione prevista** nell'intestazione dell'ordine di acquisto in passaggio 5 da 24/01/2014 a 05/02/2014.

Microsoft Dynamics NAV verrà visualizzato il seguente messaggio di avviso:

   Esistono delle riserve per questo Ordine. Tali prenotazioni verranno annullate qualora la modifica dovesse causare un conflitto di dati. Continuare?

14. Seleziona Sì. Cercare le voci di prenotazione e di tracciamento dell'ordine dall'ordine di acquisto.

> [!NOTE]  
> La prenotazione esistente è stata annullata e dovrà essere ricreata manualmente. L'ordine, tuttavia, è dinamico ed è stato ricreato da Microsoft Dynamics NAV per esistere tra l'ordine di acquisto e l'ordine di vendita. Il motivo è che la richiesta dell'ordine di produzione rilasciato (02/01/2014) è precedente alla data prevista di ricezione della fornitura.

Si conclude così la dimostrazione dell'interazione tra l'utilizzo delle prenotazioni automatiche e il monitoraggio degli ordini. Gli esempi mostrano anche cosa succede quando si modificano le date di scadenza e il messaggio di errore che viene visualizzato quando si verifica un conflitto di prenotazione.

### Pianificazione calcolata

La pianificazione Fatto mediante la pianificazione degli ordini, il foglio di lavoro delle richieste o il foglio di lavoro di pianificazione genererà voci nella tabella  *Voce di prenotazione* con il campo  **Stato della prenotazione** impostato su Tracciamento, Prenotazione o Surplus. Dovrebbe sempre esserci una coppia corrispondente con lo stesso numero di voce di valore positivo e negativo nel campo  **Quantità (base)** quando lo stato è Tracciamento o Prenotazione. Il campo  **Tipo di origine**  sarà il tipo di domanda, ovvero la tabella 37 per la quantità negativa e una tabella di pianificazione, ad esempio la tabella 246, per la quantità positiva. Il campo  **ID sorgente** sarà PIANIFICAZIONE.

In caso di domanda o offerta non assegnata, Microsoft Dynamics NAV il campo **Stato della prenotazione** verrà impostato su Surplus. Ad esempio, è possibile avere uno stato di prenotazione Surplus quando l'inventario esistente è al di sotto della quantità di scorta di sicurezza o la domanda è collegata alla previsione.

La tabella  *Elemento di pianificazione non tracciato* (Tabella 99000855) contiene informazioni sulle quantità non tracciate visualizzate quando l'utente esegue una ricerca dalla pagina di tracciamento dell'ordine per visualizzare le quantità non tracciate o sceglie un'icona di avviso nel foglio di lavoro di pianificazione. La tabella contiene voci che rappresentano una quantità in eccesso non tracciata nella rete di tracciamento degli ordini.

Questi movimenti vengono generati durante l'esecuzione della pianificazione e indicano la provenienza di tale quantità presente nelle righe di tracciabilità dell'ordine. Il surplus non tracciato può derivare dai seguenti elementi:

- Previsione di produzione
- Ordini programmati
- Scorta di sicurezza
- Punto di riordino
- Giacenza massima
- Quantità di riordino
- Quantità massima dell'ordine
- Quantità minima dell'ordine
- Molteplicità dell'ordine
- Smorzamento (percentuale di dimensione del lotto)

Nella tabella *Inserimento prenotazione*, come negli ordini di acquisto, trasferimento e produzione, è presente un campo **Flessibilità di pianificazione** . Questo campo opzione definisce se la fornitura rappresentata da questi ordini di fornitura viene presa in considerazione dal sistema di pianificazione durante il calcolo dei messaggi di azione. Se il campo contiene l'opzione Illimitato, il sistema di pianificazione include la riga nel calcolo dei messaggi di azione. Se il campo contiene l'opzione Nessuno, la riga è fissa e immodificabile e il sistema di pianificazione non include la riga nel calcolo dei messaggi di azione. La funzionalità è gestita nella tabella *Inserimento prenotazione* dal campo con lo stesso nome.

### Politica di riordino e produzione

Se viene eseguita una funzionalità di pianificazione per un set di articoli con la Politica di riordino impostata su Ordine, Microsoft Dynamics NAV verranno create voci nella tabella *Voce di prenotazione* con lo stato di prenotazione di tipo Prenotazione anziché Tracciamento.

I campi  **Tipo di origine** e  **ID origine** avranno lo stesso trattamento di altre policy di riordino. Tuttavia, nel campo  **Legatura** nella tabella  *Inserimento prenotazione*, Microsoft Dynamics NAV verrà inserito Ordine su ordine.

Il campo  **Legatura** viene compilato per controllare gli ordini di fornitura vincolati a una domanda specifica, ad esempio gli ordini di produzione creati direttamente da un ordine di vendita. Il campo visualizza Ordine su ordine quando la voce è specificamente collegata a una domanda o a un'offerta (prenotazione automatica). La domanda può essere correlata alle vendite o alla necessità di componenti.

### Tracciamento degli articoli e inserimento delle prenotazioni dei potenziali clienti

Lo stato di prenotazione del potenziale cliente può essere creato nella tabella  Microsoft Dynamics NAV Inserimento prenotazione *quando non si utilizza alcuna entità di rete degli ordini, ovvero Monitoraggio ordini.*  Ad esempio, in una riga del registro dei consumi si assegna la tracciabilità dell'articolo al componente. Tuttavia, se l'articolo è già tracciato, Microsoft Dynamics NAV potrebbero essere create più voci di prenotazione Prospect. Ciò è dimostrato nell'ESEMPIO 2 relativo agli ordini di trasferimento nella seconda parte di questo documento.

Quando si visualizza o si modifica la pagina  **Righe di tracciamento articolo**, il contenuto collettivo della tabella  *Specifiche di tracciamento* (Tabella 336) e della tabella  *Inserimento prenotazione* viene presentato in una versione temporanea della tabella 336. In questo modo si garantisce l'accesso unico ai dati di tracciabilità articolo attivi e storici.

Le prenotazioni rientrano in due categorie: prenotazioni non specifiche, in cui i numeri di lotto e di serie non sono specificati al momento della prenotazione, e prenotazioni specifiche, in cui si prenotano numeri di lotto o di serie specifici dall'inventario.

In una prenotazione non specifica, il campo  **N. lotto** o **N. di serie** è vuoto nel campo  **N. voce** della tabella 337 che indica la domanda (ad esempio, la vendita). A causa della struttura della logica di prenotazione in Microsoft Dynamics NAV, quando si inserisce una prenotazione non specifica su un articolo tracciato nell'inventario, Microsoft Dynamics NAV è comunque necessario Seleziona effettuare la prenotazione specificando le voci del registro articoli.

Poiché le registrazioni contabili degli articoli contengono le informazioni di tracciamento degli articoli, la prenotazione riserva indirettamente numeri di lotto o di serie specifici, anche se l'utente non lo desiderava. Tuttavia, con la rilegatura tardiva, Microsoft Dynamics NAV le riserve restano per voci specifiche, ma poi viene utilizzato un meccanismo di riordino in Microsoft Dynamics NAV quando si pubblica.

Per ulteriori informazioni, consultare i whitepaper tecnici elencati nelle risorse aggiuntive alla fine del presente documento. Microsoft Dynamics NAV 

### Campi Sottotipo sorgente, Messaggio azione soppresso, Adeguamento messaggio azione e Annullamento non consentito

In questa sezione vengono descritti i campi  **Sottotipo sorgente**,  **Messaggio azione soppresso**,  **Regolazione messaggio azione** e  **Non consentire annullamento** nella tabella  *Inserimento prenotazione* . Vengono forniti scenari per dimostrare l'utilizzo dei campi  **Messaggio di azione soppresso**,  **Regolazione messaggio di azione** e  **Non consentire annullamento** . Il campo  **Regolazione messaggio azione** viene utilizzato per la funzionalità della politica di monitoraggio degli ordini Messaggio di monitoraggio e azione. Il campo  **Non consentire annullamento** viene utilizzato per la funzionalità Assemblaggio su ordinazione nel Microsoft Dynamics NAV 2013.

#### Sottotipo origine

Il campo  **Sottotipo di origine** indica a quale sottotipo di origine è correlata la voce di prenotazione. Se la voce è correlata a una riga di acquisto o di vendita, il campo viene copiato dal campo  **Tipo di documento** sulla riga. Se è correlato a una riga di giornale, il campo viene copiato dal campo  **Tipo di voce** sulla riga di giornale.

#### Mess. azione eliminato

Il campo  **Messaggio azione soppressa**  registra quando una fornitura esistente è già stata parzialmente elaborata, ad esempio quando un ordine di acquisto è già stato parzialmente ricevuto o un ordine di produzione ha consumi registrati.

Quando si esegue la pianificazione, Microsoft Dynamics NAV contrassegna questo campo e imposta il campo **Stato di inserimento prenotazione** su *Surplus8. Il seguente esempio serve come illustrazione:

1. Aprire la voce 80001. Impostare i seguenti campi:
  - **Politica di riordino**: lotto per lotto
  - **Riserva**: Facoltativo
  - **Politica di monitoraggio degli ordini**: Nessuna
2. Creare un ordine di vendita. Impostare i seguenti campi:
  - **Articolo**: 80001
  - **Posizione**: Vuoto/Nessuno
  - **Quantità**: 10
  - **Data di spedizione**: 15/02/2014
3. Aprire i  **Fogli di lavoro di richiesta** ed eseguire il batch job  **Calcola piano** per l'articolo 80001.
  - **Data di inizio**: 23/01/2014
  - **Data di fine**: 03/01/2014
4. Viene suggerito di pianificare il rifornimento di una quantità pari a 10 con un nuovo ordine di acquisto e **data di scadenza** 15/02/2014.
5. Nella scheda  **Azioni**, nel gruppo Funzioni, seleziona  **Esegui azione** Messaggio per creare un ordine di acquisto con  **Data di ricezione prevista** 15/02/2014.
6. Aprire l'ordine di acquisto da passaggio 5 e impostare  **Qtà da ricevere** su 2 e registrare solo la ricevuta.
7. Aprire l'ordine di vendita da passaggio 2 e modificare **Data di spedizione** in 02/10/2014.
8. Apri i  **Fogli di lavoro di richiesta** ed esegui  **Calcola piano** per l'articolo 80001
  - **Data di inizio**: 23/01/2014
  - **Data di fine**: 03/01/2014
9. Viene suggerito di pianificare il rifornimento della quantità di 8 con un nuovo ordine di acquisto e **data di scadenza** 02/10/2014.

Le informazioni sullo stato nella tabella 337 sono mostrate nella seguente illustrazione.

La voce n. 28 nella tabella 337 ha lo stato di prenotazione Tracciamento per abbinare l'inventario esistente registrato nella voce contabile articolo 318 per 2 unità e la domanda in sospeso nella tabella 37 dell'ordine di vendita. Anche la successiva voce n. 29 ha lo stato di prenotazione Tracking e collega la quantità rimanente di 8 unità tra la domanda nella tabella 37 dell'ordine di vendita e la fornitura suggerita nella tabella 246 della riga di richiesta.

La voce n. 30 è l'ordine di acquisto esistente che è stato ricevuto parzialmente con quantità 2. Di conseguenza, il campo  **Stato della prenotazione**  è Surplus e Microsoft Dynamics NAV imposta il campo  **Quantità (base)** su *8* (saldo rimanente) e il campo  **Messaggio di azione soppresso** è abilitato.

#### Rettif. messaggio di azione

Il campo  **Regolazione messaggio azione** mostra la modifica nel lato fornitura del monitoraggio dell'ordine che si verifica quando si accettano i messaggi azione correlati. Un valore viene visualizzato qui solo quando sono attive le funzionalità per il monitoraggio degli ordini e i messaggi di azione (criterio di monitoraggio degli ordini impostato su Monitoraggio e messaggio di azione). Il valore viene calcolato in base ai dati nella tabella  *Voce messaggio azione* (Tabella 99000849). Il seguente esempio serve come illustrazione:
1. Aprire la voce 80002. Imposta il seguente campo:
 - **Politica di monitoraggio degli ordini**: messaggio di monitoraggio e azione.
2. Creare un ordine di vendita. Impostare i seguenti campi:
  - **Articolo**: 80002
  - **Posizione**: BLU
  - **Quantità**: 100
3. Aprire la pagina  **Pianificazione ordine** ed eseguire il processo batch  **Calcola piano** .
4. Seleziona l'ordine di vendita da passaggio 2 ed eseguire il batch job  **Crea ordini** .
5. Nell'ordine di vendita da passaggio 2, modificare il campo  **Quantità** da 100 a 105.
Le informazioni sullo stato nella tabella 337 sono mostrate nella seguente illustrazione.
6. Nella voce n. 34 il campo  **Adeguamento messaggio azione** nella tabella 337 è abilitato per 5 unità con stato di prenotazione Surplus. Poiché l'ordine di vendita è aumentato di passaggio 5, è stata creata questa prenotazione perché è richiesta una maggiore fornitura. Microsoft Dynamics NAV 
7. Aprire la pagina **Fogli di lavoro di pianificazione** e nella scheda **Home**, nel gruppo **Processo**, scegliere **Ottieni messaggi di azione**. Microsoft Dynamics NAV suggerirà di aumentare la quantità dell'ordine di acquisto da 100 a 105.

#### Non consentire annullamento

Il campo  **Non consentire annullamento** indica che la voce di prenotazione rappresenta l'collegare tra una riga di ordine di vendita e un ordine di assemblaggio. Non è possibile eliminare questa prenotazione perché è necessaria per mantenere la sincronizzazione che si verifica quando un articolo viene assemblato su ordinazione. Il seguente esempio serve come illustrazione:

1. Creare un ordine di acquisto. Impostare i seguenti campi:
  - **Unità di misura di base**: PCS
  - Qualsiasi gruppo di pubblicazione predefinito
  - **Sistema di rifornimento**: Assemblaggio
  - **Politica di assemblaggio**: assemblaggio su ordinazione
  - **Politica di monitoraggio degli ordini**: solo monitoraggio
2. Crea un nuovo elemento chiamato Assemble COMP. Impostare i seguenti campi:
  - **Unità di misura di base**: PCS
  - Qualsiasi gruppo di pubblicazione predefinito
  - **Sistema di rifornimento**: Acquisto
  - **Politica di monitoraggio degli ordini**: solo monitoraggio
3. Aprire l'elemento Assembla FG e nella scheda  **Naviga**, nel gruppo  **Assemblaggio/Produzione**, scegliere  **Assemblaggio**, quindi scegliere  **BOM assemblaggio**. Nella distinta base dell'assemblaggio, impostare i seguenti campi:
  - **Tipo**: Articolo
  - **No.**: Assembla COMP
  - **Quantità per**: 1 Selezionare il pulsante **OK** .
4. Aprire un giornale di registrazione degli articoli e aumentare l'inventario di Assemble COMP alla quantità 10 rispetto alla posizione BLU e registrare la riga del giornale.
5. Creare un ordine di vendita. Impostare i seguenti campi:
  - **Oggetto**: Assembla FG
  - **Posizione**: BLU
  - **Quantità**: 1 Le informazioni sullo stato nella tabella 337 sono mostrate nella seguente illustrazione.

La voce n. 82 ha un surplus di stato di prenotazione pari a 9 unità di Assemble Comp in inventario e non ha domanda. La voce n. 84 tiene traccia delle registrazioni di prenotazione tra la domanda sulla tabella 901 della linea di assemblaggio e la sua offerta nella voce contabile articolo 346. *·* 

La voce n. 86 presenta un ordine vincolante con stato di prenotazione. Inoltre, il campo  **Non consentire annullamento** è abilitato poiché il criterio di assemblaggio è impostato su Assemblaggio su ordine per l'articolo Assemblaggio FG. Infine, il campo  **Flessibilità di pianificazione** è impostato su Nessuno, poiché Microsoft Dynamics NAV non consente alla logica di pianificazione di eliminare la prenotazione.

#### Quantità disponibile per il ritiro e prenotazioni

Il campo  **Prelievo riservato e quantità di spedizione** nella tabella 337, presente nelle versioni precedenti al  Microsoft Dynamics NAV 2013, controlla la disponibilità degli articoli all'interno di un magazzino gestito. In qualsiasi installazione di gestione del magazzino, le quantità degli articoli esistono sia come voci di magazzino che come voci del registro degli articoli. Microsoft Dynamics NAV  Questi due tipi di voce contengono informazioni diverse su dove si trovano gli articoli e se sono disponibili. I movimenti warehouse definiscono la disponibilità di un articolo per collocazione e per tipo di collocazione, che è denominato anche contenuto collocazione. I movimenti contabili articoli definiscono la disponibilità di un articolo in base al relativo impegno verso i documenti in uscita. Nell'algoritmo di prelievo è presente una funzionalità speciale per calcolare la quantità disponibile per il prelievo quando il contenuto del contenitore è abbinato alle prenotazioni. L'algoritmo di prelievo sottrae le quantità riservate per altri documenti in uscita, le quantità presenti sui documenti di prelievo esistenti e le quantità prelevate ma non ancora spedite o consumate. Il risultato viene visualizzato nel campo  **Quantità disponibile da prelevare** nella pagina  **Foglio di lavoro di prelievo**, dove il campo viene calcolato dinamicamente. Il valore viene calcolato anche quando un utente crea prelievi di magazzino direttamente da documenti in uscita quali ordini di vendita, consumi di produzione o trasferimenti in uscita.

*Quantità disponibile per il prelievo = quantità nei contenitori di prelievo - quantità nei prelievi e nei movimenti (quantità riservata nei contenitori di prelievo + quantità riservata nei prelievi e nei movimenti).*

L'esempio seguente illustra come viene calcolato il valore della quantità disponibile per il prelievo in Microsoft Dynamics NAV:

1. Crea un nuovo articolo denominato Articolo magazzino. Impostare i seguenti campi:
  - **Unità di misura di base**: PCS
  - Qualsiasi gruppo di pubblicazione predefinito
  - **Sistema di rifornimento**: Acquisto
  - **Politica di riserva**: sempre
  - **Politica di monitoraggio degli ordini**: solo monitoraggio
2. Creare un ordine di acquisto per il fornitore 60000. Impostare i seguenti campi:
  - **Articolo**: Articolo di magazzino
  - **Posizione**: BIANCO
  - **Quantità**: 100
3. Rilasciare l'ordine di acquisto e creare la ricevuta di magazzino.
4. Registrare la ricevuta di magazzino e lo stoccaggio in magazzino per la quantità 100.
5. Creare un secondo ordine di acquisto per il fornitore 60000. Impostare i seguenti campi:
  - **Articolo**: Articolo di magazzino
  - **Posizione**: BIANCO
  - **Quantità**: 10
6. Rilasciare l'ordine di acquisto e creare la ricevuta di magazzino.
7. Inviare SOLO la ricevuta del magazzino. Non registrare lo stoccaggio in magazzino.
8. Creare un ordine di vendita. Impostare i seguenti campi:
  - **Articolo**: Articolo di magazzino
  - **Posizione**: BIANCO
  - **Quantità**: 10 La quantità riservata viene impostata automaticamente su 10 poiché la politica di riserva è impostata su Sempre.
9. Creare un ordine di vendita. Impostare i seguenti campi:
  - **Articolo**: Articolo di magazzino
  - **Posizione**: BIANCO
  - **Quantità**: 100 La quantità riservata viene impostata automaticamente su 100 poiché la politica di riserva è impostata su Sempre.
10. Rilascia il primo ordine di vendita da passaggio 8 e crea una spedizione in magazzino.
11. Rilascia la spedizione del magazzino e nella scheda  **Azioni** scegli **Crea prelievo**.
Viene visualizzato il seguente messaggio di errore: *Niente da gestire.*
  Il motivo è che la quantità disponibile da prelevare è pari a zero. Questo viene calcolato come segue: Quantità in inventario = 110 Quantità disponibile per il prelievo = 100

> [!NOTE]  
> La quantità in deposito o nel contenitore di ricezione non è disponibile per il prelievo.
   
   Totale riservato per ordini di vendita: 110 Quantità disponibile per il prelievo = 100 – 110 = zero.

Quando lo stoccaggio in magazzino viene registrato in passaggio 7, ciò consente la creazione del prelievo in magazzino in passaggio 11. Nelle versioni precedenti alla Microsoft Dynamics NAV 2013, il campo  **Preleva e spedisci quantità riservata**  nella tabella 337 viene compilato in base alla prenotazione per la quantità 10.

La seguente illustrazione è tratta da  Microsoft Dynamics NAV 2009 R2.

## Illustrazioni che utilizzano ordini di trasferimento e pianificazione

### Ordini di trasferimento

Quando si utilizzano ordini di trasferimento e l'articolo viene spedito ma non completamente ricevuto, nella tabella  *Inserimento prenotazione* si ottiene uno stato di prenotazione Surplus. Il codice posizione sarà la posizione di trasferimento.

Numero di riferimento della fonte. **·** Il campo viene calcolato in base all'ultimo numero di riga + numero di riga dell'articolo nella spedizione di trasferimento registrata.

Quando il monitoraggio degli ordini è attivato e non c'è domanda (ordine di vendita o consumo), Microsoft Dynamics NAV crea due voci nella tabella 337 con stato di riserva Surplus. Uno è nella tabella 5741 della riga di trasferimento e l'altro è nella tabella 32 della registrazione contabile dell'articolo. *·* 

Ciò è dimostrato nel primo esempio.

#### Esempio 1

1. Aprire gli elementi 80003 e 80004 e impostare il campo **Criterio di tracciamento** su *Solo tracciamento*. Lasciare gli altri campi come predefiniti.
2. Aprire un giornale di registrazione articoli e aumentare l'inventario di questi articoli alla quantità 10 ciascuno per la posizione ROSSA e registrare le righe del giornale.
3. Creare un ordine di trasferimento dalla posizione ROSSA a BLU per questi due articoli: Articolo 80003 sulla riga dell'ordine di trasferimento 10000 e Articolo 80004 sulla seconda riga 20000, entrambi per 10 unità.
4. Registrare solo la parte relativa alla spedizione dell'ordine di trasferimento, senza alcuna funzionalità di magazzino.
La spedizione di trasferimento registrata è illustrata nella seguente illustrazione.
Le informazioni sullo stato nella tabella 337 sono mostrate nella seguente illustrazione.
5. Confrontare i risultati della spedizione di trasferimento registrata con le voci della tabella 337.

Nella tabella seguente viene descritto cosa accade in determinati campi per la voce di prenotazione 40.

|Campo|Descrizione|  
|---------------------------------|---------------------------------------|  
|**Stato della prenotazione**|Surplus come Articolo 80003 è impostato con tracciamento ordine ma non esiste alcuna domanda.|  
|**Codice ubicazione**|Codice di trasferimento in posizione BLU.|  
|**Tipo Origine**|Tabella della linea di trasferimento 5741.|  
|**ID sorgente**|Numero del documento dell'ordine di trasferimento 1011.|
|**Riferimento sorgente n.**|Numero totale di righe 20000 + Numero di riga 10000 contro la voce 80003 = 30000.|

Di seguito è riportata la spiegazione dei campi seguenti per la voce di prenotazione 43.

|Campo|Descrizione|  
|---------------------------------|---------------------------------------|  
|**Stato della prenotazione**|Surplus come Articolo 80003 è impostato con tracciamento ordine ma non esiste alcuna domanda.|  
|**Codice ubicazione**|Ubicazione in transito Il REGISTRO PROPRIO è l'ubicazione in cui si trova l'articolo.|  
|**Tipo Origine**|Tabella 32 delle registrazioni contabili degli articoli.|  
|**Riferimento sorgente n.**|Numero di registrazione contabile aperta 322.|

#### Esempio 2

L'esempio seguente illustra cosa accade quando un componente viene trasferito tra sedi diverse, ma allo stesso tempo viene monitorato tra una domanda necessaria e una fornitura disponibile. I componenti verranno trasferiti dalla posizione ROSSA a quella BLU, per essere consumati in base a un ordine di produzione rilasciato. Il componente utilizza il monitoraggio degli ordini, la pianificazione degli ordini e il monitoraggio degli articoli.

L'esempio evidenzia il flusso rilevato nella tabella 337 in relazione ai campi **Stato prenotazione**, **Codice posizione**, **Tipo origine**, **ID origine**, **N. rif. origine** e tipo di **Legame**.

1. Nella pagina  **Impostazione produzione**, imposta il campo  **Componenti nella posizione**  su ROSSO.
2. Crea un nuovo componente articolo. Impostare i seguenti campi:
  - **Unità di misura di base**: PCS
  - Qualsiasi gruppo di pubblicazione predefinito
  - **Sistema di rifornimento**: Acquisto
  - **Politica di produzione**: produzione su ordinazione
  - **Politica di monitoraggio degli ordini**: solo monitoraggio
  - **Codice di tracciamento dell'articolo**: LOTALL
3. Utilizzando il registro degli articoli, aumenta l'inventario per il componente dell'articolo nella posizione ROSSA a 100 unità. Impostare i seguenti numeri di lotto:
  - Numero lotto Lotto A, Quantità 30
  - Numero lotto Lotto B, Quantità 70
4. Crea un nuovo elemento Prodotto. Impostare i seguenti campi:
  - **Unità di misura di base**: PCS
  - Qualsiasi gruppo di pubblicazione predefinito
  - **Sistema di rifornimento**: Produzione
  - **Politica di produzione**: produzione su ordinazione
  - **Politica di monitoraggio degli ordini**: solo monitoraggio
5. Crea **BOM di produzione** con 1 quantità per componente dell'articolo.
6. Assegnare la distinta base di produzione all'articolo prodotto.
7. Creare un ordine di vendita. Impostare i seguenti campi:
  - **Articolo**: Prodotto
  - **Posizione**: BLU
  - **Quantità**: 100
8. Nella scheda  **Azioni** dell'ordine di vendita, nel gruppo  **Pianificazione**, scegliere  **Pianificazione** per creare un ordine di produzione rilasciato collegato all'ordine di vendita.
9. Aprire l'ordine di produzione rilasciato/necessità di componenti e notare che la posizione è impostata come ROSSO.
Il motivo è che i **Componenti in posizione** sono ROSSI in **Configurazione di produzione** scheda.
L'articolo prodotto otterrà l'output nella posizione BLU.

Le informazioni sullo stato nella tabella 337 sono mostrate nella seguente illustrazione.

##### Voci di prenotazione con numeri 55 e 56

Per il componente necessario per il lotto A e il lotto B, rispettivamente, vengono creati collegamenti di tracciamento dell'ordine dalla domanda nella tabella 5407, Componente ordine di produzione, alla fornitura nella tabella 32, Registrazione contabile articolo. IL **Stato della prenotazione**  il campo contiene il monitoraggio per tutte e quattro le voci per indicare che questi collegamenti di monitoraggio dinamico degli ordini sono tra domanda e offerta.

La domanda nella tabella 5407, Componente ordine di produzione, è collegata all'ID origine dell'ordine di produzione rilasciato 101006. La fornitura nella tabella 32, Registrazione contabile articolo, è collegata al numero di riferimento sorgente. Essendo i numeri di registrazione contabile 325 e 326 in cui esistono le unità.

> [!NOTE]  
> Il campo **Nr. lotto** è vuoto nelle righe della domanda, in quanto i numeri di lotto non sono specificati nelle righe componenti dell'ordine di produzione rilasciato.

##### Registrazione della prenotazione con numero 57

Dalla domanda di vendita nella tabella 37, Riga di vendita, viene creato un tracciamento dell'ordine collegare per la fornitura nella tabella 5406, Riga ordine di produzione. Il campo  **Stato prenotazione** contiene Prenotazione e il campo  **Legatura** contiene Da ordine a ordine. Ciò avviene perché l'ordine di produzione rilasciato è stato generato specificatamente per l'ordine di vendita e deve rimanere collegato, a differenza dei collegamenti di tracciamento degli ordini con stato di prenotazione di Tracciamento, che vengono creati e modificati dinamicamente.

> [!NOTE]  
> Il campo  **Binding** può contenere anche  *Order-to-Order* quando si utilizza Make-to-Order come politica di produzione e/o Order come politica di riordino.

10. In questo puntare nello scenario, le 100 unità del componente vengono trasferite dalla posizione ROSSA alla posizione BLU utilizzando un ordine di trasferimento.

Seleziona Lotto A e lotto B per la spedizione.

Inserire la quantità totale in sospeso SOLO come Spedito.

> [!NOTE]  
> I componenti possono essere consumati nella posizione ROSSA, ma per illustrare l'esempio del flusso delle voci di prenotazione, le unità vengono trasferite manualmente nella posizione BLU.

Le informazioni sullo stato nella tabella 337 sono mostrate nella seguente illustrazione.

##### Voci di prenotazione con numero 55 e 56

Le voci di tracciamento degli ordini per i due lotti del componente che riflettono la domanda nella tabella 5407 vengono modificate dallo stato di prenotazione Tracciamento a Surplus. Il motivo è che gli approvvigionamenti a cui erano collegati prima, nella tabella 32, sono stati utilizzati dalla spedizione dell'ordine di trasferimento. Il surplus genuino, come n questo caso, riflette un approvvigionamento o una domanda effettiva eccedente che non viene tracciata. È un'indicazione di squilibrio nella rete degli ordini che, a meno che non venga risolto dinamicamente, genererà un messaggio di azione da parte del sistema di pianificazione.

##### Numeri di prenotazione da 59 a 63

Poiché i due lotti del componente vengono registrati nell'ordine di trasferimento come spediti ma non ricevuti, tutte le voci di tracciamento ordine positive correlate sono di tipo di riserva Surplus, a indicare che non sono assegnate ad alcuna domanda. Per ogni numero di lotto, una voce si riferisce alla tabella 5741, Riga di trasferimento, e una voce si riferisce alla registrazione contabile dell'articolo nella posizione di transito in cui si trovano ora gli articoli.

La tabella 5741, **Linea di trasferimento**, è il tipo di origine. **L'ID sorgente** è il numero del documento di ordine di trasferimento 1012 e **numero di riferimento sorgente.** è 20000 = 10000 + 10000 come dettagliato nell'esempio 1. La posizione è impostata come BLU per il codice della posizione di trasferimento.

Le due voci rimanenti con  **Stato di prenotazione** Surplus hanno la tabella 32,  **Movimento contabile articolo**, come Tipo di origine e  **N. rif. origine.** 328 e 330, inclusi i rispettivi numeri di lotto attualmente presenti nel REGISTRO IN TRASPORTO.

11. Registrare l'ordine di trasferimento in sospeso come Ricevuto.

Le informazioni sullo stato nella tabella 337 sono mostrate nella seguente illustrazione.

Le voci di tracciamento degli ordini sono ora simili al primo puntare nello scenario, prima che l'ordine di trasferimento venisse registrato come solo spedito, ad eccezione delle voci per il componente che ora hanno lo stato di prenotazione Surplus anziché Tracciamento. Ciò avviene perché il componente necessario è ancora nella posizione ROSSA, il che riflette il fatto che il campo  **Codice posizione** nella riga del componente dell'ordine di produzione contiene ROSSO come impostato nel campo di impostazione  **Componenti nella posizione** .

La fornitura precedentemente assegnata a questa domanda era stata trasferita alla posizione BLU e ora non può essere completamente tracciata a meno che la necessità del componente sulla riga dell'ordine di produzione non venga modificata nella posizione BLU. Ciò viene registrato nelle ultime due voci di prenotazione con i numeri di lotto compilati, il campo  **Tipo di origine** è la Tabella 32 e il campo Rif. origine **N. rif.** Campo costituito dalle voci contabili 333 e 334.

12. Nell'elenco dei componenti assegnato all'ordine di produzione rilasciato, modificare la posizione del componente in BLU.

12. Aprire il  **Giornale dei consumi** ed eseguire il processo batch  **Calcola consumi** .
Assegnare al lotto A la quantità 30 e al lotto B la quantità 70.

Chiudi il modulo di tracciamento degli articoli.

Le informazioni sullo stato nella tabella 337 sono mostrate nella seguente illustrazione.

##### Voci di prenotazione con numeri 68 e 69

Poiché la necessità del componente è stata modificata nella posizione BLU e la fornitura è disponibile come voci del registro articoli nella posizione BLU, tutte le voci di tracciamento degli ordini per i due numeri di lotto sono ora completamente tracciate, come indicato dallo stato di prenotazione di Tracciamento. I numeri di lotto non vengono inseriti nel campo  **N. lotto** rispetto alla domanda nella tabella 5406,  **Riga ordine produzione**, poiché non abbiamo specificato i numeri di lotto per il componente nell'ordine di produzione rilasciato.

##### Voci di prenotazione con numeri 70 e 71

Le voci con stato di prenotazione Prospect vengono generate nella tabella 337. Il motivo è che entrambi i numeri di lotto sono assegnati al componente nel giornale di consumo, ma il giornale non è stato registrato.

Questa è la sezione in cui viene descritta la modalità in cui le voci di tracciamento degli ordini nella tabella  **Voce di prenotazione** vengono generate, modificate ed eliminate quando si utilizzano più funzionalità in combinazione con gli ordini di trasferimento.

### Pianificazione calcolata

Quando si utilizzano le funzionalità di pianificazione, ovvero il  **Foglio di lavoro di richiesta**, il  **Foglio di lavoro di pianificazione** o la  **Pianificazione degli ordini**, le voci di prenotazione nella tabella 337  **Voce di prenotazione**  potrebbero essere modificate o aggiunte a seconda del suggerimento di pianificazione fornito dalla logica in Microsoft Dynamics NAV. L'esempio 3 verrà utilizzato **Politica di riordino**  Ordina con **Politica di produzione**  Realizzazione su ordinazione di un articolo prodotto. Il componente verrà utilizzato **Politica di riordino**  Quantità di riordino fissa.

#### Esempio 3

1. Nel **Impostazione della produzione**  scheda, **Componente in posizione**  è ROSSO dall'esempio precedente.
2. Crea un nuovo elemento padre 70061. Impostare i seguenti campi:
  - **Unità di misura di base**: PCS
  - Qualsiasi gruppo di pubblicazione predefinito
  - **Sistema di rifornimento**: Ordine di produzione
  - **Politica di produzione** : Realizzazione su ordinazione
  - **Politica di riordino** : Ordine
  - **Politica di riserva** : Opzionale
  - **Tracciamento dell'ordine** : Nessuno
3. Crea nuovo elemento componente 70062. Impostare i seguenti campi:
  - **Unità di misura di base**: PCS
  - Qualsiasi gruppo di pubblicazione predefinito
  - **Sistema di rifornimento** : Acquistare
  - **Politica di riordino** : Quantità di riordino fissa
  - **Politica di riserva** : Opzionale
  - **Politica di monitoraggio degli ordini**: Nessuna
  - **Quantità di scorta di sicurezza**: 10
  - **Riordina puntare**: 25
  - **Quantità di riordino**: 50
4. Creare una nuova distinta base di produzione e specificare l'articolo componente 70062 con quantità per 1.
Assegnare la distinta base di produzione all'articolo padre 70061.
5. Creare un ordine di vendita. Impostare i seguenti campi:
  - **Articolo**: Quantità di riordino fissa
  - **Posizione**: ROSSO
  - **Quantità**: 40
  - **Data di spedizione**: 15/02/2014
6. Aprire la pagina **Fogli di lavoro di pianificazione** ed eseguire il processo batch **Calcola piano rigenerativo** .
  - **MPS/MRP**: abilitato
  - **Data di inizio**: 23/01/2014
  - **Data di fine**: 03/01/2014
  - Filtra per gli articoli 70061 e 70062
  - Nessuna previsione

Di seguito vengono forniti i seguenti suggerimenti di pianificazione.

Il primo suggerimento di pianificazione è quello di creare un nuovo ordine di produzione pianificato per soddisfare la domanda in sospeso dell'ordine di vendita per la quantità 40 dell'articolo padre 70061. Controlla il monitoraggio dell'ordine e Microsoft Dynamics NAV verrà visualizzato l'ordine di vendita in sospeso. Il tracciamento degli ordini viene attivato non appena vengono generati dal motore di pianificazione.

La seconda riga serve per portare l'inventario sopra Reorder puntare (25). Pertanto, tenendo conto della quantità di riordino (50), la logica di pianificazione suggerisce una quantità di 50 unità. La terza linea è quella di portare l'inventario al livello di scorta di sicurezza (10).

La quarta linea serve a rifornire l'inventario quando l'ordine di vendita viene spedito. In quel momento, l'inventario è 20 e quindi sotto Riordina puntare. Di conseguenza, il motore di pianificazione propone di acquistare 50 componenti aggiuntivi tenendo conto della quantità di riordino. Questa è una quantità non tracciata, quindi nella tabella  *Inserimento prenotazione*  337 questa sarà contrassegnata con lo stato di prenotazione Surplus.

Le informazioni sullo stato nella tabella 337 sono mostrate nella seguente illustrazione.

Il campo  **Stato della prenotazione**  è Prenotazione e viene creato un vincolo ordine-ordine. Il motivo è che la politica di produzione degli articoli è impostata su "Produci su ordinazione" e la politica di riordino è impostata su "Ordine". Se uno dei due è impostato su Ordine, lo stato della prenotazione sarà Prenotazione anziché Tracciamento e il Vincolo sarà impostato su Ordine-Ordine.

La domanda di 40 unità rispetto al campo **ID origine** è il numero dell'ordine di vendita 1005 e il tipo di origine è *Riga di vendita* tabella 37. L'inserimento della prenotazione è allineato con la proposta di pianificazione, Riferimento sorgente n. 10000, l'ID sorgente è PIANIFICAZIONE e il tipo sorgente è  *Riga di richiesta* tabella 246. Esiste quindi un equilibrio tra la domanda derivante dall'ordine di vendita e l'offerta suggerita dal motore di pianificazione.

##### Numeri di prenotazione 73 e 74

Eseguendo il batch job Calcola piano, le quattro voci successive vengono generate con uno stato di prenotazione Tracciamento dovuto all'impostazione della politica di riordino Quantità di riordino fissa per il componente. La fornitura richiesta per il componente Articolo 70062 viene ripristinata in base ai suggerimenti di pianificazione forniti, Riferimento Fonte n. 20000 e 30000, con ID sorgente impostato su PIANIFICAZIONE e Tipo sorgente dalla tabella 246 *Riga di richiesta* . Il componente necessario viene creato per soddisfare la domanda dell'articolo padre 70061 per una quantità totale (base) di 40. Come risultato di questa richiesta, il campo  **Riga ordine produzione origine** è 10000, con Tipo origine nella tabella  *Fabbisogno componenti* 99000829.

Lo stato della prenotazione non è Surplus, poiché esiste un tracciamento dell'ordine tra la domanda dell'articolo padre 70061 e la fornitura dell'articolo componente 70062.

##### Numeri di prenotazione 75 e 76

Le ultime due voci hanno uno stato di prenotazione Surplus, in quanto si tratta di Quantità non tracciate generate sul foglio di lavoro di pianificazione relative ai parametri di riordino Riordina puntare e Quantità di riordino.

## Vedere anche  
[Dettagli di progettazione: progettazione della tracciabilità articolo](design-details-item-tracking-design.md)  
[Dettagli di progettazione: bilanciamento di domanda e offerta](design-details-balancing-demand-and-supply.md)  
[Dettagli di progettazione: Impegno, tracciabilità dell'ordine e messaggistica di azioni](design-details-reservation-order-tracking-and-action-messaging.md)   
[Dettagli di progettazione: Pianificazione approvvigionamento](design-details-supply-planning.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]