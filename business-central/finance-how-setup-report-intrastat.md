---
title: Impostare il reporting Intrastat
description: Informazioni su come impostare le funzionalità di reporting Intrastat per segnalare le attività commerciali con società in altri paesi UE.
author: altotovi
ms.author: altotovi
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 12/20/2022
ms.custom: bap-template
ms.search.keywords: 'electronic document, Intrastat, trade, EU, European Union'
ms.search.form: '308, 309, 310, 311, 325, 326, 327, 328, 405, 406, 4810, 4811, 8451, 12202, 31077'
---
# Impostare il reporting Intrastat

Tutte le società dell'Unione Europea (UE) devono creare report relativi alle attività commerciali con altri paesi UE. Le società devono presentare ogni mese alle autorità statistiche del proprio paese/area geografica report relativi al movimento delle merci, che devono quindi essere inviati alle autorità fiscali. Intrastat è il sistema per la raccolta di statistiche commerciali di prodotti all'interno di questi paesi/aree geografiche. Usa **Report Intrastat** per completare il reporting Intrastat periodico (tipicamente mensile), la raccolta, la registrazione e i report degli scambi di prodotti secondo la legislazione locale.

Il reporting Intrastat si basa sui regolamenti di base dell'UE che si applicano a tutti i paesi, tuttavia, in pratica, vi sono alcune differenze all'interno dei singoli paesi. Ogni paese ha le sue regole su cosa e come dichiarare esattamente.

> [!NOTE]
> Le informazioni Intrastat non si applicano alla circolazione di servizi tra paesi, ma solo a beni (articoli e cespiti). Se il governo locale richiede la registrazione della circolazione dei servizi tra paesi, è possibile farlo utilizzando la funzionalità **Dichiarazione di servizio**.
>
> Questa funzione si prevede sia disponibile da novembre 2022 come app in [AppSource](https://go.microsoft.com/fwlink/?linkid=2081646) quindi, se vuoi usarla, dovrai prima installarla nella pagina **Gestione estensioni**.

> [!IMPORTANT]
> Questo articolo illustra la nuova esperienza Intrastat disponibile da [!INCLUDE[prod_short](includes/prod_short.md)] versione 21. Contatta l'amministratore per sapere quale versione sta utilizzando la tua società e per abilitare la nuova funzionalità.
>
> Leggi l'articolo sulla configurazione e l'utilizzo di Intrastat della versione precedente in [Impostazione e report Intrastat](finance-how-setup-report-intrastat-v20.md).

## Abilitare la nuova esperienza Intrastat

Nel secondo ciclo di rilascio del 2022, [!INCLUDE[prod_short](includes/prod_short.md)] include un'esperienza Intrastat riprogettata con funzionalità estese. Se la nuova funzionalità Intrastat non è abilitata nel tuo ambiente, può essere abilitata manualmente da un amministratore nella pagina **Gestione funzionalità**.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Gestione funzionalità**, quindi scegli il collegamento correlato.
2. Nella pagina **Gestione funzionalità**, seleziona la riga **Aggiornamento funzionalità: sostituire la funzionalità Intrastat esistente con la nuova estensione Intrastat**. Per ulteriori informazioni sulla gestione funzionalità vedi [Abilitazione di funzionalità imminenti in anticipo](/dynamics365/business-central/dev-itpro/administration/feature-management) nel contenuto per amministratori.
3. Nella colonna **Abilita per** scegli **Tutti gli utenti**.
4. Leggi la spiegazione di come verrà aggiornato il sistema e scegli **sì** se sei d'accordo.
5. Seleziona **Avanti** e otterrai una configurazione di base per Intrastat. Per maggiori informazioni sulla configurazione Intrastat vedi la sezione [Configurazione Intrastat](#intrastat-configuration).
6. Dopo aver terminato la configurazione, scegli **Fine** per iniziare a utilizzare la nuova esperienza Intrastat.

> [!IMPORTANT]
> Tieni presente che non puoi utilizzare le vecchie e le nuove esperienze in parallelo. Prima di attivare l'estensione in un ambiente di produzione, ti consigliamo di abilitare e testare questa funzionalità in un ambiente sandbox con una copia dei dati di produzione. Dopo aver attivato una nuova esperienza utente nell'ambiente di produzione, non è possibile ripristinare la vecchia funzionalità Intrastat.

> [!NOTE]
> A seconda dell'ubicazione della società, sarà sufficiente abilitare la funzione sopra descritta. Per i paesi con funzionalità specifiche per i report Intrastat, è necessario abilitare l'app Intrastat specifica per paese oltre all'estensione principale.

## Configurazione Intrastat

Prima di poter utilizzare i report Intrastat, è necessario configurare diverse impostazioni.

### Setup reporting Intrastat

La pagina **Setup reporting Intrastat** consente di abilitare il reporting Intrastat e impostare i relativi valori predefiniti. È possibile specificare se è necessario creare report Intrastat da spedizioni (invii), entrate (arrivi) o entrambi a seconda delle soglie impostate in base alle normative locali. Puoi anche impostare tipi di transazioni di default per documenti normali e di reso, utilizzati per la natura del reporting delle transazioni.

Per impostare il reporting Intrastat:

1. Scegli l'icona a forma di ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Setup report Intrastat**, quindi scegli il collegamento correlato.
2. Apri la Scheda dettaglio **Generale** e compila i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] La tabella seguente descrive alcuni dei campi chiave:

   | Campo | Descrizione |
   | --- | --- |
   | **Dichiara ricevute** | Specifica che è necessario includere gli arrivi delle le merci ricevute nei report Intrastat. |
   | **Dichiara spedizioni** | Specifica che è necessario includere le spedizioni degli articoli inviati nei report Intrastat. |
   | **Spedizioni basate su**  | Specifica in base a quale codice paese vengono utilizzate le righe report Intrastat. Puoi scegliere una delle opzioni: **Vendere a - Paese**, **Fatturare a - Paese**, o **Spedire a - Paese**. |
   | **Partita IVA basata su** | Specifica in base a quale codice cliente/fornitore viene utilizzato il numero partita IVA per il report Intrastat. Puoi scegliere una delle opzioni: **Vendere a - IVA** o **Fatturare a - IVA**. |
   | **Partita IVA della società in archivio** | Specifica la modalità di esportazione del numero di partita IVA della società nel file Intrastat. Puoi scegliere una delle opzioni: Reg. IVA No., aggiungendo il prefisso UE come prefisso e rimuovendo il prefisso UE dalla Reg. IVA No. |
   | **Partita IVA del fornitore in archivio** | Specifica la modalità di esportazione del numero di partita IVA del fornitore nel file Intrastat. Puoi scegliere una delle opzioni: Reg. IVA No., aggiungendo il prefisso UE come prefisso e rimuovendo il prefisso UE dalla Reg. IVA No. |
   | **Partita IVA del cliente in archivio** | Specifica la modalità di esportazione del numero di partita IVA del cliente nel file Intrastat. Puoi scegliere una delle opzioni: Reg. IVA No., aggiungendo il prefisso UE come prefisso e rimuovendo il prefisso UE dalla Reg. IVA No. |
   | **Ottieni IVA partner** | Specifica da quale tipo di riga **Report Intrastat** viene aggiornato il numero di partita IVA del partner. A seconda dei requisiti locali, puoi scegliere solo per ricevuta, solo per spedizione o per entrambi i tipi di righe. |
3. Apri la Scheda dettaglio **Transazioni predefinite** e compila i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] La tabella seguente descrive alcuni dei campi chiave:

   | Campo | Descrizione |
   | --- | --- |
   | **Tipo di transazione predefinito** | Specifica il tipo di transazione predefinito per spedizioni vendite, spedizioni di assistenza e carichi di acquisti regolari. |
   | **Tipo di transazione predefinito - Resi** | Specifica il tipo di transazione predefinito per resi di vendita, resi di assistenza e resi di acquisto. |
   | **Partita IVA predefinita persona** | Specifica il numero di partita IVA predefinito del privato nel caso in cui il privato debba disporre di un numero di partita IVA dedicato nel report Intrastat. |
   | **Partita IVA predefinita commercio terze parti** | Specifica il numero di partita IVA commercio terze parti predefinito nel caso in cui non sia disponibile il relativo numero di partita IVA. |
   | **IVA predefinita per stato sconosciuto** | Specifica il numero di partita IVA predefinito per uno stato sconosciuto. |
   | **Codice paese/area geografica predefinito** | Specifica il codice paese di ricevimento predefinito. |
4. Apri la Scheda dettaglio **Reporting** e compila i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] La tabella seguente descrive alcuni dei campi chiave:

   | Campo | Descrizione |
   | --- | --- |
   | **Codice definizione di scambio dati** | Specifica il codice della definizione di scambio dati per generare il file Intrastat. Funziona solo se il campo **Suddividi file ricevute/spedizioni** è impostato su **No**. |
   | **Suddividi file ricevute/spedizioni** | Specifica se le ricevute e le spedizioni devono essere dichiarate in due file distinti. |
   | **File Zip (-s)** | Specifica se il file di report (-s) deve essere aggiunto al file .zip. |
   | **Codice definizione di scambio dati - Ricevuta** | Specifica il codice della definizione di scambio dati per generare il file Intrastat per le merci ricevute. Funziona solo se il campo **Suddividi file ricevute/spedizioni** è impostato su **Sì**. |
   | **Codice definizione di scambio dati - Spedizione** | Specifica il codice della definizione di scambio dati per generare il file Intrastat per le merci spedite. Funziona solo se il campo **Suddividi file ricevute/spedizioni** è impostato su **Sì**. |
5. Apri la scheda dettaglio **Numerazione** per configurare **Nr. Intrastat**.

### Impostare un file di report

1. Scegli l'icona a forma di ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti le **definizioni di scambio dati**, e scegli il collegamento correlato.
2. Scegli l'azione **Nuovo**.
3. Nella Scheda dettaglio **Generale** descrivi la definizione dello scambio di dati, il tipo di file di dati, il separatore di colonna, le codeunit correlate, XMLport e altri campi compilando i campi.
4. Sulla scheda dettaglio **Definizioni riga** descrivi la formattazione delle righe nel file di dati compilando i campi in base al campo **Tipo di riga** e a dove è necessario definire il numero di colonne per questa riga.
5. Sulla scheda dettaglio **Definizioni colonna** compila la riga per ogni colonna pianificata. È possibile definire i nomi delle colonne, i tipi di dati (*Testo*, *Data*, o *Decimale*), la lunghezza della riga a larghezza fissa che contiene la colonna se il file è di tipo Testo fisso e alcuni altri parametri.
6. Scegli l'azione **Mapping dei campi** nella scheda dettaglio **Definizioni riga** per aprire la pagina **Mapping dei campi**.
7. Crea la nuova voce e nella scheda dettaglio **Generale** scegli l'**ID tabella** corretto (per **Riga report Intrastat**, scegli 4812), quindi compila più campi:
   1. Specifica l'indice della chiave per ordinare i record di origine prima dell'esportazione nel campo **Indice chiave**.
   2. Seleziona la **Codeunit mapping** corretta.
8. Sulla scheda dettaglio **Mapping dei campi** aggiungi le colonne che hai precedentemente configurato nella scheda dettaglio **Definizioni colonna** quindi aggiungi quanto segue:
   1. Specifica l'**ID campo** per ciascuna delle colonne.
   2. Specifica la **Regola di trasformazione** per ogni colonna di cui hai bisogno. Specifica la regola che trasforma il testo importato in un valore supportato prima di poterne eseguire il mapping a un campo specificato in [!INCLUDE[prod_short](includes/prod_short.md)]. Quando scegli un valore in questo campo, lo stesso valore viene inserito nel campo **Regola di trasformazione** nella tabella **Buf. mapping campo scambio dati** e viceversa.
9. Se è necessario raggruppare le voci in base ad alcune colonne, nella scheda dettaglio **Raggruppamento campi** scegli i campi che desideri utilizzare per il raggruppamento.

> [!NOTE]
> [!INCLUDE[prod_long](includes/prod_long.md)] viene fornito con la definizione di scambio dati preconfigurata per Intrastat per tutti i paesi localizzati. Per informazioni sulla creazione di una nuova definizione di scambio dati, vedi l'articolo [Impostare le definizioni di scambio dati](across-how-to-set-up-data-exchange-definitions.md).

### Impostare i campi obbligatori con l'elenco di controllo del report Intrastat

In alcuni paesi, le autorità richiedono che i report Intrastat includano, ad esempio, il metodo di spedizione per gli acquisti o altri valori quando le vendite superano una certa soglia.

Per impostare campi e/o valori obbligatori nella pagina **Report Intrastat**:

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup report Intrastat**, quindi scegli il collegamento correlato.
2. Scegliere l'azione **Elenco di controllo report Intrastat**.
3. Aggiungi le righe necessarie per il controllo utilizzando le seguenti istruzioni:
   1. Imposta il campo **Nr. campo** su un campo che deve essere verificato per un valore non vuoto.
   2. Compila il campo **Espressione filtro** se necessario, in base alle seguenti regole:
      1. Quando apri la **Pagina filtro**, scegli il **Filtro** che vuoi utilizzare per il controllo.
      2. Nel passaggio successivo, scegli un valore correlato al **Filtro** usato.
      3. Se hai più filtri da compilare per questo campo specifico, puoi aggiungere un altro filtro seguendo gli stessi passaggi.
      4. Quando hai finito di inserire i filtri per il campo scelto, scegli **OK**.
   3. Seleziona il campo **Espressione di filtro stornata** per specificare che il controllo dei campi viene eseguito solo nelle righe che non corrispondono all'espressione di filtro. Se la riga non viene filtrata, il campo viene ignorato.

> [!NOTE]
> Quando apri la **Pagina filtro** dalla riga **Espressione filtro** puoi utilizzare tutte le espressioni di filtro standard relative al campo specifico che desideri filtrare.
>
> Fai attenzione quando imposti le regole di convalida. Possono differire da paese a paese.

## Utilizzare codeunit personalizzate nei report Intrastat

Se vuoi modificare il funzionamento di Intrastat e la configurazione predefinita non è sufficiente, è possibile personalizzare il sistema estendendo le funzionalità standard. Se è necessario modificare ulteriormente il comportamento di Intrastat, è possibile sviluppare le proprie codeunit. Quando crei le codeunit, tuttavia, devi apportare ulteriori modifiche per utilizzarle. Per configurare il sistema per utilizzare i propri oggetti:

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Configurazione report IVA**, quindi scegli il collegamento correlato.
2. Nella pagina **Configurazione report IVA**, aggiungi una nuova riga.
3. Sul campo **Tipo di report IVA** scegli l'opzione **Report Intrastat**.
4. Sul campo **Versione report IVA** specifica la versione del report.
5. Successivamente, puoi aggiungere le tue codeunit per le seguenti opzioni: a. Nel campo **ID codeunit righe suggerite**, specifica la nuova codeunit per suggerire le righe nelle righe del report Intrastat.
   b. Nel campo **ID codeunit contenuto** specifica la nuova codeunit per esportare i dati come file utilizzando una definizione di scambio dati.
   c. Nel campo **Convalida ID codeunit**, specifica le nuove codeunit per convalidare i risultati nelle righe del report Intrastat.

> [!IMPORTANT]
>
> Questa riga deve essere vuota se si utilizzano le codeunit standard. Dovresti creare una riga e configurarla solo se hai sviluppato codeunit personalizzate.

## Altre configurazione Intrastat

> [!IMPORTANT]
> Le schede cliente e le schede fornitore includono un campo, **Tipo di partner Intrastat**, che ha gli stessi valori di opzione del campo **Tipo di partner:** "" (vuoto), *Società*, e *Persona*. Il campo **Tipo di partner Intrastat** ha sostituito il campo **Tipo di partner** nel report Intrastat. Il campo **Tipo di partner** viene utilizzato nell'area SEPA (Single Euro Payments Area) per definire lo schema di addebito diretto SEPA (core o B2B). Il campo **Tipo di partner Intrastat** viene utilizzato solo per i report Intrastat. In questo modo, puoi specificare valori diversi per i due campi, se necessario.
>
> Se il campo **Tipo di partner Intrastat** viene lasciato vuoto, il valore del campo **Tipo di partner** viene utilizzato per i report Intrastat.

Eccetto per **Setup report Intrastat**, **Definizioni di scambio di dati**, ed **Elenco di controllo report Intrastat**, devi anche configurare altre impostazioni:

| Pagina | Descrizione |
| ---- | ----------- |
| **Paesi/Aree geografiche** | Prima di iniziare a utilizzare i report Intrastat, è necessario anche impostare la pagina **Paesi/Aree geografiche**. In questa pagina devi aggiungere il **Codice Paese/Area geografica UE** e il **Codice Intrastat** per specificare un codice per il paese/area geografica con cui stai operando, poiché verrà utilizzato nei report Intrastat. |
| **Nomenclatura combinata** | In molti paesi, le autorità doganali e fiscali hanno stabilito dei codici a otto cifre per i vari articoli. Affinché i movimenti articoli contengano le informazioni necessarie quando vengono importati nella riga di registrazione Intrastat, è necessario immettere il codice articolo nella pagina **Nomenclatura combinata**. È necessario trovare i codici degli articoli di cui si occupa la propria società e immetterli nella pagina **Nomenclatura combinata**. |
| **Metodi di trasporto** | Sono disponibili sette codici di una cifra per i metodi di trasporto Intrastat. **1** via mare, **2** via ferrovia, **3** su strada, **4** via area, **5** per posta, **7** per installazioni fisse e **9** con proprio mezzo (ad esempio il trasporto con la propria auto). [!INCLUDE[prod_short](includes/prod_short.md)] non richiede tali codici specifici, tuttavia, si consiglia di inserire le descrizioni con un significato simile a questi codici. |
| **Natura transazione** | I paesi e le aree hanno codici differenti per la natura delle transazioni Intrastat, ad esempio acquisto o vendita ordinaria, cambio di merce resa e sostituzione di merce non resa. Imposta tutti codici che si applicano al tuo paese/area geografica. Questi codici vengono quindi usati nella Scheda dettaglio **Commercio estero** nei documenti di vendita e di acquisto e quando si elaborano i resi. |
| **Specifiche transazione** | Imposta i codici per integrare le descrizioni del tipo di transazione. |
  > [!NOTE]
  > A partire da gennaio 2022, Intrastat richiede un codice di natura transazione diverso per le spedizioni a privati o imprese senza partita IVA e imprese con partita IVA. Per soddisfare questo requisito, ti consigliamo di rivedere e/o aggiungere nuovi codici di natura della transazione nella pagina **Tipi di transazione** in base ai requisiti nel tuo paese. Dovresti anche controllare e aggiornare il campo **Tipo di partner Intrastat** su *Persona* per i clienti privati o aziende senza partita IVA nella relativa pagina **Cliente**. Se non sei sicuro del tipo di partner Intrastat o del tipo di transazione corretto da utilizzare, ti consigliamo di rivolgerti a un esperto nel tuo paese o nella tua regione.

| **Campo** | **descrizione** |
| --------- | --------------- |
| **Peso netto** | Il peso è una delle configurazioni di base relative al report Intrastat come il **Peso totale** è obbligatorio per il report. Per essere pronto a questo requisito, devi anche compilare il campo **Peso netto** nella scheda articolo o cespite. |
| **Cod. paese di origine** | Utilizza i codici alfa ISO di due lettere per la scheda articolo o cespite per il paese in cui il bene è stato ottenuto o prodotto. Se il bene è stato prodotto in più paesi, il paese di origine è l'ultimo paese in cui è stato elaborato in modo significativo. |
| **Numero di identificazione IVA dell'operatore partner nello Stato membro di importazione** | Questo è il numero di identificazione IVA dell'operatore partner nello Stato membro di importazione. La partita IVA viene utilizzata anche nello scambio di dati di esportazione intra-UE tra gli Stati Membri e consente agli Stati Membri di allocare i dati ricevuti alla società importatrice nel proprio paese. Le unità di creazione dei report devono riportare la partita IVA della società che ha dichiarato l'acquisto intra Unione di beni nello Stato membro di importazione. |

Facoltativamente è anche possibile impostare le opzioni seguenti:

* **Codici voce doganale**: le autorità doganali e fiscali hanno stabilito codici numerici che classificano gli articoli e i servizi. Specificare questi codici negli articoli.
* **Aree**: completamento delle informazioni sui paesi e le aree geografiche.
* **Cod. spedizione Intrastat**: specifica le ubicazioni da cui si spediscono o si ricevono gli articoli da o verso altri paesi. Un esempio di codice di spedizione Intrastat è un aeroporto. I codici di spedizione Intrastat possono essere immessi nei documenti di vendita e di acquisto nella Scheda dettaglio **Commercio estero**. Queste informazioni vengono inoltre copiate dai movimenti articoli creati per le registrazioni Intrastat.
* **Unità di misura supplementare**: la quantità di merci per il report Intrastat può essere il peso netto (in chilogrammi) o un'unità supplementare. Se sono necessarie unità supplementari, è necessario configurarle per articoli e cespiti.

#### Impostare i metodi di trasporto

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Metodi di trasporto**, quindi scegli il collegamento correlato.
2. Compila i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

#### Impostare il codici della natura delle transazioni

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Tipi di transazione**, quindi scegli il collegamento correlato.
2. Compila i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### Altre configurazioni correlate

Prima di utilizzare la funzionalità di report Intrastat è necessario configurare alcuni campi sulle schede articolo, cespite, cliente e fornitore.

#### Schede articolo

Per impostare tutte le informazioni necessarie relative a Intrastat sulle schede articolo:

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") , inserisci **Elemento** e scegli il link relativo.
2. Seleziona l'articolo da configurare.
3. Nella scheda dettaglio **Costi e registrazione** compila i campi **Nomenclatura combinata**, **Unità di misura supplementare**, e **Cod. paese/area geografica di origine**.
4. Espandi la scheda dettaglio **Inventario** e immetti il valore decimale nel campo **Peso netto**.

> [!NOTE]
> Puoi utilizzare diverse unità di misura come unità di misura supplementare. Se non sono uguali all'**Unità di misura di base**, è necessario configurare questa unità di misura sulla pagina **Unità di misura articolo**.

#### Schede cespite

Per impostare tutte le informazioni necessarie relative a Intrastat sulle schede cespite:

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Cespiti**, quindi scegli il collegamento correlato.
2. Seleziona il cespite che vuoi configurare.
3. Espandi la scheda dettaglio **Intrastat** e compila i campi **Nomenclatura combinata**, **Peso netto** e **Unità di misura supplementare**.

> [!NOTE]
> Puoi utilizzare diverse unità di misura come unità di misura supplementare. Qualsiasi **Codice unità di misura** scegli, la sua **Quantità** nei report Intrastat sarà sempre 1.

#### Schede fornitore

Prima di utilizzare un fornitore nei report Intrastat, è necessario specificare un **Codice Paese/Area geografica** e **Partita IVA** per ciascuno di essi, oltre ad ulteriori informazioni sulla pagina **Scheda fornitore**:

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Fornitori**, quindi scegli il collegamento correlato.
2. Seleziona il fornitore da configurare.
3. Sulla scheda dettaglio **Intrastat** puoi impostare valori predefiniti per i campi **Tipo di transazione predefinito**, **Tipo di transazione predefinito - Resi**, e **Metodo di trasporto predefinito**.
4. Espandi la scheda dettaglio **Pagamenti** e scegli l'opzione nel campo **Tipo di partner Intrastat** per specificare se il fornitore è una persona o una società nel report Intrastat.

#### Schede cliente

Prima di utilizzare un cliente nei report Intrastat, è necessario specificare un **Codice Paese/Area geografica** e **Partita IVA** per ciascuno di essi, oltre ad ulteriori informazioni sulla pagina **Scheda cliente**:

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Clienti**, quindi scegli il collegamento correlato.
2. Seleziona il cliente da configurare.
3. Sulla scheda dettaglio **Intrastat** puoi impostare valori predefiniti per i campi **Tipo di transazione predefinito**, **Tipo di transazione predefinito - Resi**, e **Metodo di trasporto predefinito**.
4. Espandi la scheda dettaglio **Pagamenti** e scegli l'opzione nel campo **Tipo di partner Intrastat** per specificare se il fornitore è una persona o una società nel report Intrastat.

#### Escludere articoli e cespiti dal report Intrastat

Se c'è un motivo per cui un articolo o un cespite specifico deve essere escluso dai report Intrastat, è necessario modificare un'opzione sulla scheda.

##### Escludere un articolo dal report Intrastat

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") , inserisci **Elemento** e scegli il link relativo.
2. Seleziona l'articolo da configurare.
3. Nella scheda dettaglio **Costo e registrazione** seleziona il campo **Escludi da report Intrastat**.

##### Escludere un cespite dal report Intrastat

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Cespiti**, quindi scegli il collegamento correlato.
2. Seleziona il cespite che vuoi configurare.
3. Espandi la scheda dettaglio **Intrastat**, quindi seleziona il campo **Escludi da report Intrastat**.

## Impostazione Intrastat specifica per paese

I requisiti Intrastat sono simili in tutti gli stati membri dell'UE, sebbene vi siano importanti eccezioni. In teoria, le regole dovrebbero essere applicate uniformemente in tutti gli Stati membri. Tuttavia, esistono differenze nell'attuazione perché alcuni Stati membri forniscono linee guida su come applicare i principi generali del regolamento in situazioni specifiche. Ad esempio, campioni commerciali, restituzione di merci e così via. Queste linee guida possono produrre risultati diversi per varie situazioni negli Stati membri dell'UE. Per questo motivo, alcuni paesi hanno alcune informazioni specifiche extra separate da altri paesi. Usano anche un formato di file diverso per i report.

### Austria

I report Intrastat in Austria richiedono due file diversi per i ricevimenti e le spedizioni. Per verificare che la configurazione sia corretta, procedi nel seguente modo:

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup report Intrastat**, quindi scegli il collegamento correlato.  
2. Nella Scheda dettaglio **Reporting**, controlla se l'opzione **Suddividi file ricevute/spedizioni** è selezionata. In relazione a ciò, troverai due **Codici definizione di scambio dati** configurati. Il campo **File zip** è selezionato anche per garantire che i file di report vengano aggiunti al file zip.

Il processo di utilizzo dei report Intrastat è lo stesso della funzionalità globale.

<!-- ### Belgium-->

### Repubblica Ceca

La nuova esperienza del report Intrastat per la Repubblica Ceca sarà disponibile a partire dalla prima ondata di rilascio del 2023. Nel frattempo, puoi continuare a utilizzare la funzionalità **Registrazione Intrastat**.

### Finlandia

In Finlandia, ci sono alcuni passaggi aggiuntivi per configurare Intrastat. I report Intrastat in Finlandia richiedono due file diversi per i ricevimenti e le spedizioni. In relazione a ciò, troverai due **Codici definizione di scambio dati** configurati.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup report Intrastat**, quindi scegli il collegamento correlato.  
2. Nella pagina **Setup report Intrastat**, nella Scheda dettaglio **Setup file** compilare i campi come descritto nella tabella seguente.

    |Campo|Descrizione|  
    |------------------------------------|---------------------------------------|
    | **Codice personalizzato**|Specifica un codice personalizzato per le informazioni di configurazione del file Intrastat. |
    | **Nr. seriale società**|Specifica un numero di serie aziendale per le informazioni di configurazione del file Intrastat. |

3. Nella Scheda dettaglio **Reporting**, controlla se l'opzione **Suddividi file ricevute/spedizioni** è selezionata.

Il processo di utilizzo dei report Intrastat è lo stesso della funzionalità globale.

<!-- ### Germany-->

### Italia

La nuova esperienza del report Intrastat per l'Italia sarà disponibile da febbraio 2023. Nel frattempo, puoi continuare a utilizzare la funzionalità **Registrazione Intrastat**.

<!-- ### France-->

### Svezia

I report Intrastat in Svezia richiedono due file diversi per i ricevimenti e le spedizioni. Per verificare che la configurazione sia corretta, procedi nel seguente modo:

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup report Intrastat**, quindi scegli il collegamento correlato.  
2. Nella Scheda dettaglio **Reporting**, controlla se l'opzione **Suddividi file ricevute/spedizioni** è selezionata. In relazione a ciò, troverai due **Codici definizione di scambio dati** configurati.

Il processo di utilizzo dei report Intrastat è lo stesso della funzionalità globale.

<!-- ### United Kingdom-->

## Vedi le informazioni relative al training in [Microsoft Learn](/learn/modules/process-intrastat-dynamics-365-business-central/index).

## Vedere anche

[Report Intrastat in Business Central](finance-how-report-intrastat.md)  
[Gestione contabile](finance.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
