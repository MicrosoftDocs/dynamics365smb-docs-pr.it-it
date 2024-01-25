---
title: Impostare il reporting Intrastat
description: Questo articolo descrive come impostare il reporting Intrastat per dichiarare le attività commerciali con società in altri paesi/aree geografiche della UE.
author: altotovi
ms.author: altotovi
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 04/05/2023
ms.custom: bap-template
ms.search.keywords: 'electronic document, Intrastat, trade, EU, European Union'
ms.search.form: '308, 309, 310, 311, 325, 326, 327, 328, 405, 406, 4810, 4811, 8451, 12202, 31077'
---
# <a name="set-up-intrastat-reporting"></a>Impostare il reporting Intrastat

Tutte le società dell'Unione Europea (UE) devono creare report relativi alle attività commerciali con altri paesi UE. Le società devono presentare ogni mese alle autorità statistiche del proprio paese/area geografica report relativi al movimento delle merci, che devono quindi essere inviati alle autorità fiscali. Intrastat è il sistema usato per raccogliere statistiche commerciali su prodotti in tali paesi/aree geografiche. Usa il report Intrastat per completare il reporting Intrastat periodico mediante raccolta, registrazione e reporting degli scambi di prodotti secondo la legislazione locale.

Il reporting Intrastat si basa sulle normative UE standard che si applicano a tutti i paesi o aree geografiche. Tuttavia, vi sono differenze all'interno dei singoli paesi/aree geografiche. Ogni paese/area geografica ha le sue regole su cosa includere nei report e come.

> [!NOTE]
> Le informazioni Intrastat non si applicano alla circolazione di servizi tra paesi/aree geografiche. Tali informazioni si applicano solo a beni come articoli e cespiti. Se nel tuo paese è richiesta la registrazione della circolazione dei servizi tra paesi/aree geografiche, usa la funzionalità **Dichiarazione di servizio**.
>
> Questa funzionalità è disponibile come app scaricabile da [AppSource](https://go.microsoft.com/fwlink/?linkid=2081646). Per usare questa funzionalità, installala nella pagina **Gestione estensioni**.

> [!IMPORTANT]
> Questo articolo illustra la nuova esperienza Intrastat disponibile in [!INCLUDE[prod_short](includes/prod_short.md)] versione 21. Contatta il tuo amministratore per sapere quale versione sta utilizzando la tua società e se devi abilitare la nuova funzionalità.
>
> Leggi l'articolo sulla configurazione e sull'utilizzo di Intrastat della versione precedente in [Impostare e registrare report Intrastat](finance-how-setup-report-intrastat-v20.md).

## <a name="enable-the-new-intrastat-experience"></a>Abilitare la nuova esperienza Intrastat

Nel secondo ciclo di rilascio del 2022, [!INCLUDE[prod_short](includes/prod_short.md)] include un'esperienza Intrastat riprogettata che fornisce funzionalità estese. Se la nuova funzionalità Intrastat non è abilitata nel tuo ambiente, un amministratore può abilitarla manualmente nella pagina **Gestione funzionalità**.

> [!IMPORTANT]
> Non puoi utilizzare le vecchie e le nuove esperienze in parallelo. Prima di attivare l'estensione in un ambiente di produzione, ti consigliamo di testarla in un ambiente sandbox usando una copia dei dati di produzione. Dopo aver attivato una nuova esperienza utente nell'ambiente di produzione, non puoi ripristinare la vecchia funzionalità Intrastat.

1. Seleziona l'icona :::image type="icon" source="media/ui-search/search_small.png" border="false":::, immetti **Gestione funzionalità**, quindi seleziona il collegamento correlato.
2. Nella pagina **Gestione funzionalità**, seleziona la riga per **Aggiornamento funzionalità: sostituire la funzionalità Intrastat esistente con la nuova estensione Intrastat**. Per ulteriori informazioni sulla gestione delle funzionalità, vedi [Abilitazione anticipata delle funzionalità future](/dynamics365/business-central/dev-itpro/administration/feature-management).
3. Nella colonna **Abilita per** seleziona **Tutti gli utenti**.
4. Leggi la spiegazione su come verrà aggiornato il sistema e seleziona **Sì** se sei d'accordo.
5. Selezionare **Avanti**. Otterrai una configurazione di base per Intrastat. Per maggiori informazioni sulla configurazione Intrastat, vedi la sezione [Configurazione Intrastat](#intrastat-configuration) più avanti in questo articolo.
6. Dopo aver terminato la configurazione, seleziona **Fine** per utilizzare la nuova esperienza Intrastat.

    > [!NOTE]
    > A seconda dell'ubicazione della società, sarà sufficiente abilitare la funzionalità sopra descritta. Per i paesi/aree geografiche con funzionalità specifiche per il reporting Intrastat, abilita l'app Intrastat specifica del paese o dell'area geografica oltre all'estensione principale.

## <a name="intrastat-configuration"></a>Configurazione Intrastat

Prima di poter utilizzare i report Intrastat, è necessario configurare diverse impostazioni.

### <a name="intrastat-reporting-setup"></a>Setup reporting Intrastat

Usa la pagina **Setup reporting Intrastat** per abilitare e impostare il comportamento predefinito per il reporting Intrastat. Puoi specificare se è necessario creare report Intrastat da spedizioni (invii), entrate (arrivi) o entrambi a seconda delle soglie impostate in base alle normative locali. Puoi anche impostare tipi di transazioni predefiniti per documenti normali e di reso utilizzati per il reporting delle transazioni.

Per impostare il reporting Intrastat, esegui la procedura seguente:

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](media/ui-search/search_small.png "Dimmi cosa vuoi fare"), immetti **Setup report Intrastat**, quindi seleziona il collegamento correlato.
2. Nella Scheda dettaglio **Generale** seleziona o immetti le informazioni sul campo come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] La tabella seguente descrive alcuni dei campi chiave.

   | Campo | Descrizione |
   | --- | --- |
   | **Dichiara ricevute** | Specifica che è necessario includere gli arrivi delle le merci ricevute nei report Intrastat. |
   | **Dichiara spedizioni** | Specifica che è necessario includere le spedizioni degli articoli inviati nei report Intrastat. |
   | **Includi spedizioni dirette** | Specifica se le transazioni di spedizione diretta sono incluse nei report Intrastat. Per ulteriori informazioni, vedi [Utilizzo dei report Intrastat](finance-how-report-intrastat.md).  |  
   | **Spedizioni basate su**  | Specifica il codice paese in base a quale vengono utilizzate le righe report Intrastat.  |
   | **Partita IVA basata su** | Specifica il codice cliente/fornitore in base al quale viene utilizzato il numero partita IVA per il report Intrastat.  |
   | **Partita IVA della società in archivio** | Specifica la modalità di esportazione del numero di partita IVA della società nel file Intrastat.  |
   | **Partita IVA del fornitore in archivio** | Specifica la modalità di esportazione del numero di partita IVA del fornitore nel file Intrastat.  |
   | **Partita IVA del cliente in archivio** | Specifica la modalità di esportazione del numero di partita IVA del cliente nel file Intrastat.  |
   | **Ottieni IVA partner** | Specifica da quale tipo di riga del report Intrastat viene aggiornato il numero di partita IVA del partner. A seconda dei requisiti locali, puoi scegliere solo righe per ricevuta, solo righe per spedizione o entrambi i tipi di righe. |

4. Nella Scheda dettaglio **Transazioni predefinite** seleziona o immetti le informazioni sul campo come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] La tabella seguente descrive alcuni dei campi chiave.

   | Campo | Descrizione |
   | --- | --- |
   | **Tipo di transazione predefinito** | Specifica il tipo di transazione predefinito per spedizioni vendite, spedizioni di assistenza e carichi di acquisti regolari. |
   | **Tipo di transazione predefinito - Resi** | Specifica il tipo di transazione predefinito per resi di vendita, resi di assistenza e resi di acquisto. |
   | **Partita IVA predefinita persona** | Specifica il numero di partita IVA predefinito del privato se il privato deve disporre di un numero di partita IVA dedicato nel report Intrastat. |
   | **Partita IVA predefinita commercio terze parti** | Specifica il numero di partita IVA commercio terze parti predefinito nel caso in cui non sia disponibile il relativo numero di partita IVA. |
   | **IVA predefinita per stato sconosciuto** | Specifica il numero di partita IVA predefinito per uno stato sconosciuto. |
   | **Codice paese/area geografica predefinito** | Specifica il codice paese di ricevimento predefinito. |

5. Nella Scheda dettaglio **Reporting** seleziona o immetti le informazioni sul campo come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] La tabella seguente descrive alcuni dei campi chiave.

   | Campo | Descrizione |
   | --- | --- |
   | **Codice definizione di scambio dati** | Specifica il codice della definizione di scambio dati per generare il file Intrastat. Questa campo è disponibile solo se il campo **Suddividi file ricevute/spedizioni** è impostato su **No**. |
   | **Suddividi file ricevute/spedizioni** | Specifica se le ricevute e le spedizioni devono essere dichiarate in due file distinti. |
   | **File Zip (-s)** | Specifica se i file di report devono essere aggiunti al file zip. |
   | **Codice definizione di scambio dati - Ricevuta** | Specifica il codice della definizione di scambio dati per generare il file Intrastat per le merci ricevute. Questa campo è disponibile solo se il campo **Suddividi file ricevute/spedizioni** è impostato su **Sì**. |
   | **Codice definizione di scambio dati - Spedizione** | Specifica il codice della definizione di scambio dati per generare il file Intrastat per le merci spedite. Questa campo è disponibile solo se il campo **Suddividi file ricevute/spedizioni** è impostato su **Sì**. |

6. Nella scheda dettaglio **Numerazione** immetti un valore nel campo **Nr. Intrastat** .

### <a name="set-up-a-reporting-file"></a>Impostare un file di reporting

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](media/ui-search/search_small.png "Dimmi cosa vuoi fare"), immetti le **definizioni di scambio dati** e seleziona il collegamento correlato.
2. Seleziona **Nuovo** e nella Scheda dettaglio **Generale** immetti le informazioni sulla definizione dello scambio di dati, il tipo di file di dati, il separatore di colonna, le codeunit correlate, XMLport e altri campi come necessario.
3. Nella Scheda dettaglio **Definizioni riga** immetti un valore nel campo **Tipo di riga** per descrivere la formattazione delle righe nel file di dati e dove è necessario definire il numero di colonne per questa riga.
4. Sulla scheda dettaglio **Definizioni colonna** compila la riga per ogni colonna pianificata. Puoi definire i nomi delle colonne, i tipi di dati (come testo, data o decimale), la lunghezza della riga a larghezza fissa che contiene la colonna se il file è di tipo *Testo fisso* e altri parametri.
5. Nella Scheda dettaglio **Definizioni righe** seleziona **Mapping campi**.
6. Nella pagina **Mapping campi** crea una nuova voce. 
7. Nella Scheda dettaglio **Generale** seleziona il valore **ID tabella** (per **Riga report Intrastat**, scegli **4812**) e immetti le seguenti informazioni sul campo:

   1. Nel campo **Indice chiave** specifica l'indice della chiave per ordinare i record di origine prima dell'esportazione.
   2. Seleziona un valore nel campo **Codeunit mapping**.

8. Nella Scheda dettaglio **Mapping campi** aggiungi le colonne che hai precedentemente configurato nella Scheda dettaglio **Definizioni colonna** quindi aggiungi le seguenti informazioni sul campo:

   1. Specifica il valore **ID campo** per ciascuna delle colonne.
   2. Specifica il valore **Regola di trasformazione** per ciascuna colonna come necessario. Il valore specifica la regola che trasforma il testo importato in un valore supportato prima di poterne eseguire il mapping a un campo specificato in [!INCLUDE[prod_short](includes/prod_short.md)]. Quando scegli un valore in questo campo, lo stesso valore viene inserito nel campo **Regola di trasformazione** nella tabella **Buf. mapping campo scambio dati** . Al contrario, quando immetti un valore esatto nel campo **Regola di trasformazione** nella tabella **Buf. mapping campo scambio dati**, un valore viene scelto in questo campo.

9. Se è necessario raggruppare le voci in base ad alcune colonne, nella scheda dettaglio **Raggruppamento campi** seleziona i campi che desideri utilizzare per il raggruppamento.

> [!NOTE]
> [!INCLUDE[prod_long](includes/prod_long.md)] viene fornito con la definizione di scambio dati preconfigurata per Intrastat per tutti i paesi o le aree geografiche localizzati. Per informazioni su come creare una nuova definizione di scambio dati, vedi [Impostare le definizioni di scambio dati](across-how-to-set-up-data-exchange-definitions.md).

### <a name="set-mandatory-fields-with-the-intrastat-report-checklist"></a>Impostare i campi obbligatori con l'elenco di controllo del report Intrastat

In alcuni paesi/aree geografiche, le autorità richiedono che i report Intrastat includano, ad esempio, il metodo di spedizione per gli acquisti o altri valori quando le vendite superano una certa soglia.

Per impostare campi e/o valori obbligatori nella pagina **Report Intrastat**, procedi come segue:

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](media/ui-search/search_small.png "Dimmi cosa vuoi fare"), immetti **Setup report Intrastat**, quindi seleziona il collegamento correlato.
2. Seleziona Report **Elenco di controllo report Intrastat**.
3. Segui questi passaggi per aggiungere le righe necessarie per il controllo:
   1. Imposta il campo **Nr. campo** su un campo che deve essere verificato per un valore non vuoto.
   2. Immetti un valore nel campo **Espressione filtro** se necessario, in base alle seguenti regole:

        1. Quando apri la **Pagina filtro**, seleziona il filtro che vuoi utilizzare per il controllo.
        2. Seleziona un valore correlato al filtro selezionato.
        3. Se devi riempire più filtri per il campo scelto, ripeti i due passaggi precedenti per aggiungere un altro filtro.
        4. Quando hai finito di immettere i filtri per il campo scelto, seleziona **OK**.

   3. Seleziona la casella di controllo **Espressione di filtro stornata** per specificare che il controllo dei campi viene eseguito solo nelle righe che non corrispondono all'espressione di filtro. Se la riga non viene filtrata, il campo viene ignorato.

> [!NOTE]
> Quando apri la **Pagina filtro** dalla riga **Espressione filtro** puoi utilizzare tutte le espressioni di filtro standard relative al campo specifico che desideri filtrare.
>
> Fai attenzione quando imposti le regole di convalida poiché possono differire da un paese o area geografica all'altro.

## <a name="use-custom-codeunits-in-intrastat-reporting"></a>Utilizzare codeunit personalizzate nel reporting Intrastat

Se vuoi modificare il funzionamento di Intrastat e la configurazione predefinita non è sufficiente, puoi personalizzare il sistema estendendo le funzionalità standard. Se è necessario modificare ulteriormente il comportamento di Intrastat, è possibile sviluppare le proprie codeunit. Quando crei codeunit, devi apportare ulteriori modifiche per utilizzarle. Per configurare il sistema per utilizzare i tuoi oggetti, procedi come segue.

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immetti **Configurazione report IVA**, quindi seleziona il collegamento correlato.
2. Nella pagina **Configurazione report IVA**, aggiungi una nuova riga.
3. Nel campo **Tipo report IVA**, selezionare **Report Intrastat**.
4. Nel campo **Versione report IVA** specifica la versione del report.
5. Aggiungi le tue codeunit per le seguenti opzioni:
   1. Nel campo **ID codeunit righe suggerite**, specifica la nuova codeunit per suggerire le righe nelle righe del report Intrastat.
   2. Nel campo **ID codeunit contenuto** specifica la nuova codeunit per esportare i dati come file utilizzando una definizione di scambio dati.
   3. Nel campo **Convalida ID codeunit**, specifica le nuove codeunit per convalidare i risultati nelle righe del report Intrastat.

> [!IMPORTANT]
> Questa riga deve essere vuota se si utilizzano le codeunit standard. Dovresti creare una riga e configurarla solo se hai sviluppato codeunit personalizzate.

## <a name="other-intrastat-configurations"></a>Altre configurazione Intrastat

Le schede cliente e fornitore includono il campo **Tipo di partner Intrastat**, che ha gli stessi valori di opzione del campo **Tipo di partner**: 

- "" (vuoto)
- *Società*
- *Persona*
    
Il campo **Tipo di partner Intrastat** ha sostituito il campo **Tipo di partner** nel reporting Intrastat. Il campo **Tipo di partner** viene utilizzato nell'area SEPA (Single Euro Payments Area) per definire lo schema di addebito diretto SEPA (core o B2B). Il campo **Tipo di partner Intrastat** viene utilizzato solo per il reporting Intrastat. Quindi, puoi specificare valori diversi per i due campi, se necessario.

Se il campo **Tipo di partner Intrastat** viene lasciato vuoto, il valore del campo **Tipo di partner** viene utilizzato per il reporting Intrastat.

Oltre a **Setup report Intrastat**, **Definizioni di scambio di dati** ed **Elenco di controllo report Intrastat**, devi anche configurare le seguenti impostazioni:

| Pagina | Descrizione |
| ---- | ----------- |
| **Paesi/Aree geografiche** | Nella pagina **Paesi/Aree geografiche**, aggiungi le infomazioni **Codice Paese/Area geografica UE** e il **Codice Intrastat** per specificare un codice per il paese/l'area geografica con cui stai operando. Queste informazioni saranno utilizzate nel reporting Intrastat. |
| **Nomenclatura combinata** | In molti paesi/aree geografiche, le autorità doganali e fiscali hanno stabilito dei codici a otto cifre per i vari articoli. Per abilitare i movimenti articoli affinché contengano le informazioni necessarie quando vengono importati nella riga di registrazione Intrastat, immetti il codice articolo nella pagina **Nomenclatura combinata**. Trova i codici degli articoli di cui si occupa la tua società e immettili nella pagina **Nomenclatura combinata**. |
| **Metodi di trasporto** | Sono disponibili sette codici di una cifra per i metodi di trasporto Intrastat: **1** via mare, **2** via ferrovia, **3** su strada, **4** via area, **5** per posta, **7** per installazioni fisse e **9** con proprio mezzo (ad esempio il trasporto con la propria auto). [!INCLUDE[prod_short](includes/prod_short.md)] non richiede questi codici specifici. Tuttavia, si consiglia di inserire descrizioni con un significato simile a questi codici. |
| **Natura transazione** | I paesi e le aree hanno codici differenti per la natura delle transazioni Intrastat, ad esempio acquisto o vendita ordinaria, cambio di merce resa e sostituzione di merce non resa. Imposta tutti codici che si applicano al tuo paese/area geografica. Questi codici vengono quindi usati nella Scheda dettaglio **Commercio estero** nei documenti di vendita e di acquisto e quando si elaborano i resi. |
| **Specifiche transazione** | Imposta i codici per integrare le descrizioni del tipo di transazione. |
  
> [!NOTE]
> A partire da gennaio 2022, Intrastat richiede un codice di natura transazione diverso per le spedizioni a privati o imprese senza partita IVA e imprese con partita IVA. Per soddisfare questo requisito, ti consigliamo di rivedere o aggiungere nuovi codici di natura della transazione nella pagina **Tipi di transazione** in base ai requisiti nel tuo paese. Dovresti anche controllare e aggiornare il campo **Tipo di partner Intrastat** su *Persona* per i clienti privati o aziende senza partita IVA nella relativa pagina **Cliente**. Se non sei sicuro del tipo di partner Intrastat o del tipo di transazione corretto da utilizzare, ti consigliamo di rivolgerti a un esperto nel tuo paese o nella tua regione.

|   Campo   |   Descrizione   |
| --------- | --------------- |
| **Peso netto** | Il peso è una delle configurazioni di base relative al reporting Intrastat poiché il peso totale è obbligatorio per il reporting. Per essere pronto per questo requisito, immetti un valore nel campo **Peso netto** nella scheda dell'articolo o del cespite. |
| **Cod. paese di origine** | Utilizza i codici alfa ISO di due lettere per la scheda articolo o cespite per il paese o l'area geografica in cui il bene è stato ottenuto o prodotto. Se il bene è stato prodotto in più paesi, il paese o l'area geografica di origine è l'ultimo paese o area geografica in cui è stato elaborato in modo significativo. |
| **Numero di identificazione IVA dell'operatore partner nello Stato membro di importazione** | Questo è il numero di identificazione IVA dell'operatore partner nello Stato membro di importazione. La partita IVA viene utilizzata anche nello scambio di dati di esportazione intra-UE tra gli Stati Membri e consente agli Stati Membri di allocare i dati ricevuti alla società importatrice nel proprio paese/area geografica. Le unità di reporting devono riportare la partita IVA della società che ha dichiarato l'acquisto intra Unione di beni nello Stato membro di importazione. |

Facoltativamente è anche possibile impostare le opzioni seguenti:

* **Codici voce doganale**: le autorità doganali e fiscali hanno stabilito codici numerici che classificano gli articoli e i servizi. Puoi specificare questi codici negli articoli.
* **Aree**: completamento delle informazioni sui paesi e le aree geografiche.
* **Cod. spedizione Intrastat**: specifica le ubicazioni da cui si spediscono o si ricevono gli articoli da o verso altri paesi/aree geografiche. Un esempio di codice di spedizione Intrastat è un aeroporto. I codici di spedizione Intrastat possono essere immessi nei documenti di vendita e di acquisto nella Scheda dettaglio **Commercio estero**. Queste informazioni vengono copiate dai movimenti articoli creati per le registrazioni Intrastat.
* **Unità di misura supplementare**: la quantità di merci per il reporting Intrastat può essere il peso netto (in chilogrammi) o un'unità supplementare. Se sono necessarie unità supplementari, è necessario configurarle per articoli e cespiti.

#### <a name="set-up-transport-methods"></a>Impostare i metodi di trasporto

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immetti **Metodi di trasporto**, quindi seleziona il collegamento correlato.
2. Compila i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

#### <a name="set-up-transaction-nature-codes"></a>Impostare il codici della natura delle transazioni

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immetti **Tipi di transazione di servizio**, quindi seleziona il collegamento correlato.
2. Compila i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="other-related-configurations"></a>Altre configurazioni correlate

Prima di utilizzare la funzionalità di reporting Intrastat, devi definire dei campi nelle schede articolo, cespite, cliente e fornitore.

#### <a name="item-cards"></a>Schede articolo

Segui questi passaggi per impostare tutte le informazioni necessarie relative a Intrastat nelle schede articolo.

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immetti **Articoli** e seleziona il collegamento correlato.
2. Seleziona l'articolo da configurare.
3. Nella scheda dettaglio **Costi e registrazione** e compila i campi **Nomenclatura combinata**, **Unità di misura supplementare**, e **Cod. paese/area geografica di origine**, immetti un valore.

    > [!NOTE]
    > Per usare un'unità di misura per integrare l'unità di misura di base, configura l'unità di misura supplementare nella pagina **Unità di misura articolo**.

4. Nella Scheda dettaglio **Inventario** nel campo **Peso netto** immetti un valore in formato decimale.

> [!NOTE]
> Quando aggiungi la nomenclatura combinata a un'unità di misura definita per l'articolo, [!INCLUDE [prod_short](includes/prod_short.md)] compila automaticamente il campo **Unità di misura supplementare**, in base alla configurazione della nomenclatura combinata. Puoi cambiare il campo **Unità di misura supplementare** come necessario.

#### <a name="set-up-fixed-assets-for-intrastat"></a>Impostare cespiti per Intrastat

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immetti **Cespiti**, quindi seleziona il collegamento correlato.
2. Seleziona il cespite che vuoi configurare.
3. Nella Scheda dettaglio **Intrastat** e compila i campi **Nomenclatura combinata**, **Peso netto** e **Unità di misura supplementare**, immetti un valore.

> [!NOTE]
> Puoi utilizzare diverse unità di misura come unità di misura supplementare. Qualsiasi **Codice unità di misura** scegli, la sua **Quantità** nei report Intrastat sarà sempre 1.

#### <a name="set-up-vendors-for-intrastat"></a>Impostare fornitori per Intrastat

Prima di poter includere un fornitore nel reporting Intrastat, immetti le relative informazioni nella pagina **Scheda fornitore**. Ad esempio, specifica un valore **Codice paese/area geografica** e un valore **Partita IVA**.

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immetti **Fornitori**, quindi seleziona il collegamento correlato.
2. Seleziona il fornitore da configurare.
3. Nella Scheda dettaglio **Intrastat** nei campi **Tipo di transazione predefinito**, **Tipo di transazione predefinito - Resi** e **Metodo di trasporto predefinito**, imposta un valore predefinito per ogni campo.
4. Espandi la scheda dettaglio **Pagamenti** e scegli l'opzione nel campo **Tipo di partner Intrastat** per specificare se il fornitore è una persona o una società nel report Intrastat.

#### <a name="set-up-customers-for-intrastat"></a>Impostare clienti per Intrastat

Prima di poter includere un cliente nel reporting Intrastat, immetti le relative informazioni nella pagina **Scheda cliente**. Ad esempio, devi specificare un valore **Codice paese/area geografica** e un valore **Partita IVA**.

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immetti **Clienti**, quindi seleziona il collegamento correlato.
2. Seleziona il cliente da configurare.
3. Nella Scheda dettaglio **Intrastat** nei campi **Tipo di transazione predefinito**, **Tipo di transazione predefinito - Resi** e **Metodo di trasporto predefinito**, imposta un valore predefinito per ogni campo.
4. Espandi la scheda dettaglio **Pagamenti** e scegli l'opzione nel campo **Tipo di partner Intrastat** per specificare se il fornitore è una persona o una società nel report Intrastat.

#### <a name="exclude-items-and-fixed-assets-from-intrastat-reporting"></a>Escludere articoli e cespiti dal reporting Intrastat

Se c'è un motivo per escludere un articolo o un cespite specifico dal reporting Intrastat, modifica l'opzione nella relativa scheda contrassegnando il campo **Escludi da report Intrastat**. Utilizzare questo campo nella scheda **Modello articolo** per creare più articoli esclusi dal reporting Intrastat. 

##### <a name="exclude-an-item-from-intrastat-reporting"></a>Escludere un articolo dal reporting Intrastat

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immetti **Articoli** e seleziona il collegamento correlato.
2. Seleziona l'elemento che desideri configurare, quindi nella Scheda dettaglio  **Costo e registrazione**, seleziona la casella di controllo **Escludi da report Intrastat** .

##### <a name="exclude-a-fixed-asset-from-intrastat-reporting"></a>Escludere un cespite dal reporting Intrastat

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immetti **Cespiti**, quindi seleziona il collegamento correlato.
2. Seleziona il cespite che vuoi configurare.
3. Nella Scheda dettaglio **Intrastat** seleziona la casella di controllo **Escludi da report Intrastat**.

#### <a name="set-up-tariff-numbers"></a>Impostare nomenclature combinate

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immetti **Nomenclatura combinata**, quindi scegli il collegamento correlato.  
2. Nella pagina **Nomenclatura combinata** immetti le informazioni nei campi come descritto nella tabella riportata di seguito.

    | Campo | Descrizione |  
    |-------|-------------|
    | **Nr.** | Specifica la nomenclatura combinata. |
    | **Descrizione** | Specifica una descrizione della nomenclatura combinata correlata. |
    | **Unità supplementari** | Specifica se le autorità doganali e fiscali richiedono informazioni circa la quantità e l'unità di misura dell'articolo. |
    | **Fattore di conversione** | Specifica il fattore di conversione per la nomenclatura combinata. |
    | **Unità di misura** | Specifica l'unità di misura per la nomenclatura combinata. |

> [!NOTE]
> Se aggiungi un'unità di misura supplementare, [!INCLUDE [prod_short](includes/prod_short.md)] chiede se desideri aggiornare gli articoli correlati. Se scegli di aggiornare gli articoli correlati, il valore **Unità di misura** nella pagina **Unità di misura articoli** viene aggiornato per tutti gli articoli che hanno la stessa nomenclatura combinata.
> 
> Quando aggiungi una nomenclatura che ha un valore **Unità di misura** definito per l'articolo,  [!INCLUDE [prod_short](includes/prod_short.md)] aggiunge automaticamente una nuova unità di misura al valore **Unità di misura articoli** per l'articolo. Il valore **Quantità per unità di misura** si basa sul campo **Precisione arrotondamento quantità**.

## <a name="enter-countryregion-intrastat-settings"></a>Immettere impostazioni Intrastat specifiche per paese/area geografica

I requisiti Intrastat sono simili in tutti gli stati membri dell'UE, sebbene vi siano importanti eccezioni. In teoria, le regole dovrebbero essere applicate uniformemente in tutti gli Stati membri. Tuttavia, esistono differenze nelle implementazioni perché alcuni Stati membri forniscono linee guida su come applicare i principi in situazioni specifiche (ad esempio, campioni commerciali e resi di merci). Queste linee guida possono produrre risultati diversi per varie situazioni. Pertanto, le informazioni che i paesi/aree geografiche devono immettere possono differire, così come il formato di file che devono utilizzare per il reporting.

### <a name="austria"></a>Austria

Il reporting Intrastat in Austria richiede due file diversi per i ricevimenti e le spedizioni. Per verificare che la configurazione sia corretta, procedi nel seguente modo.

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immetti **Setup report Intrastat**, quindi seleziona il collegamento correlato.  
2. Nella Scheda dettaglio **Reporting**, controlla se l'opzione **Suddividi file ricevute/spedizioni** è selezionata. Se lo è, troverai due valori **Codice definizione di scambio dati** distinti configurati. 
3. Verifica che il campo **File zip** è selezionato, anche per garantire che i file di report vengano aggiunti al file zip.

Il processo di utilizzo dei report Intrastat è lo stesso della funzionalità globale.

<!-- ### Belgium-->

### <a name="czech-republic"></a>Repubblica Ceca

La nuova esperienza di report Intrastat per la Repubblica Ceca sarà disponibile nel primo ciclo di rilascio del 2023. Nel frattempo, continua a utilizzare la funzionalità **Registrazione Intrastat**.

### <a name="finland"></a>Finlandia

In Finlandia, ci sono alcuni passaggi aggiuntivi per configurare Intrastat. Il reporting Intrastat in Finlandia richiede due file diversi per i ricevimenti e le spedizioni. Puoi notare che vi sono anche due valori **Codice definizione di scambio dati** distinti configurati.

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immetti **Setup report Intrastat**, quindi seleziona il collegamento correlato.  
2. Nella pagina **Setup report Intrastat**, nella Scheda dettaglio **Setup file** immetti le informazioni dei campi come descritto nella tabella seguente.

    |                 Campo              |            Descrizione                |  
    |------------------------------------|---------------------------------------|
    | **Codice personalizzato** | Specifica un codice personalizzato per le informazioni di configurazione del file Intrastat. |
    | **Nr. seriale società** | Specifica un numero di serie aziendale per le informazioni di configurazione del file Intrastat. |

3. Nella Scheda dettaglio **Reporting**, controlla se l'opzione **Suddividi file ricevute/spedizioni** è selezionata.

Il processo di utilizzo dei report Intrastat è lo stesso della funzionalità globale.

<!-- ### Germany-->

### <a name="italy"></a>Italia

Un nuova esperienza di report Intrastat per l'Italia sarà disponibile a partire da febbraio 2023. Nel frattempo, continua a utilizzare la funzionalità **Registrazione Intrastat**.

<!-- ### France-->

### <a name="sweden"></a>Svezia

Il reporting Intrastat in Svezia richiede due file diversi per i ricevimenti e le spedizioni. Per verificare che la configurazione sia corretta, procedi nel seguente modo.

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immetti **Setup report Intrastat**, quindi seleziona il collegamento correlato.  
2. Nella Scheda dettaglio **Reporting**, verifica che l'opzione **Suddividi file ricevute/spedizioni** è selezionata. Se lo è, troverai due valori **Codice definizione di scambio dati** distinti configurati.

Il processo di utilizzo dei report Intrastat è lo stesso della funzionalità globale.

<!-- ### United Kingdom-->

## <a name="see-also"></a>Vedere anche

[Reporting Intrastat in Business Central](finance-how-report-intrastat.md)  
[Gestione contabile](finance.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
