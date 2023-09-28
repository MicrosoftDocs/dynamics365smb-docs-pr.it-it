---
title: Impostare e registrare report Intrastat
description: Informazioni su come impostare le funzionalità di reporting Intrastat e come segnalare le attività commerciali con società in altri paesi/aree geografiche.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, Intrastat, trade, EU, European Union'
ms.search.form: '308, 309, 310, 311, 325, 326, 327, 328, 405, 406, 8451, 12202, 31077'
ms.date: 05/23/2022
ms.author: bholtorf
---
# <a name="set-up-and-report-intrastat"></a>Impostare e registrare report Intrastat

Tutte le società dell'Unione Europea devono creare report relativi alle attività commerciali con altri paesi UE. È necessario presentare ogni mese alle autorità statistiche del proprio paese report relativi al movimento delle merci, che devono quindi essere inviati alle autorità fiscali. Questa operazione è detta reporting Intrastat. Per compilare i report Intrastat periodici si utilizza la pagina **Registrazioni Intrastat**.

[!INCLUDE[intrastat-2022w2](includes/intrastat-2022w2.md)]

## <a name="required-and-optional-setups"></a>Configurazioni obbligatorie e facoltative

> [!IMPORTANT]
> Le carte cliente e le carte fornitore includono un campo, **Tipo di partner Intrastat**, che ha gli stessi valori di opzione del campo **Tipo di partner**: *"" (vuoto)*, *Azienda*, e *Persona*. Il campo **Tipo di partner Intrastat** ha sostituito il campo **Tipo di partner** nel report Intrastat. **Tipo di partner** viene utilizzato in SEPA per definire lo schema di addebito diretto SEPA (Core o B2B). **Tipo di partner Intrastat** viene utilizzato solo per i report Intrastat. In questo modo, puoi specificare valori diversi per i due campi, se necessario.
>
> Tuttavia, se il campo **Tipo di partner Intrastat** viene lasciato vuoto, il valore del campo **Tipo di partner** viene utilizzato per i report Intrastat.

Prima di poter usare la registrazione Intrastat per dichiarare le informazioni Intrastat, è necessario impostare varie opzioni:  

* **Setup Intrastat**: la pagina Setup Intrastat consente di abilitare il reporting Intrastat e impostare i relativi valori predefiniti. È possibile specificare se è necessario creare report Intrastat da spedizioni (invii), entrate (arrivi) o entrambi a seconda delle soglie impostate in base alle normative locali. È anche possibile impostare tipi di transazioni di default per documenti normali e di reso, utilizzati per la natura del reporting delle transazioni.
* **Definizioni di registrazioni Intrastat**: è necessario impostare le definizioni di registrazioni Intrastat e i batch che verranno utilizzati. Poiché il report Intrastat viene creato mensilmente, è necessario creare 12 batch di registrazioni Intrastat basati sulla stessa definizione.  
* **Codici voce doganale**: le autorità doganali e fiscali hanno stabilito codici numerici che classificano gli articoli e i servizi. Specificare questi codici negli articoli.
* **Codici natura transazione**: i paesi e le aree hanno codici differenti per la natura delle transazioni Intrastat, ad esempio acquisto o vendita ordinaria, cambio di merce resa e sostituzione di merce non resa. Impostare tutti codici che si applicano al proprio paese. È possibile utilizzare questi codici nella Scheda dettaglio **Commercio estero** nei documenti di vendita e di acquisto e quando si elaborano i resi.

    > [!NOTE]
    > A partire da gennaio 2022, Intrastat richiede un codice di natura transazione diverso per le spedizioni a privati o imprese senza partita IVA e imprese con partita IVA. Per soddisfare questo requisito, ti consigliamo di rivedere e/o aggiungere nuovi codici di natura della transazione nella pagina **Tipi di transazione** in base ai requisiti nel tuo paese. Dovresti anche rivedere e aggiornare il campo **Tipo di partner Intrastat** su *Persona* per i clienti privati o aziende senza partita IVA nella relativa pagina **Cliente**. Se non sei sicuro del tipo di partner Intrastat o del tipo di transazione corretto da utilizzare, ti consigliamo di rivolgerti a un esperto nel tuo paese o nella tua regione.

* **Metodi di trasporto**: sono disponibili sette codici di una cifra per i metodi di trasporto Intrastat. **1** via mare, **2** via ferrovia, **3** su strada, **4** via area, **5** per posta, **7** per installazioni fisse e **9** con proprio mezzo (ad esempio il trasporto con la propria auto). [!INCLUDE[prod_short](includes/prod_short.md)] non richiede tali codici, tuttavia, si consiglia di inserire descrizioni con un significato simile a questi codici.  
* **Cod. paese destin./proven.**: utilizzare a completamento delle descrizioni della natura delle transazioni.  
* **Paese di origine**: utilizzare i codici alfa ISO di due lettere per il paese o l'area geografica in cui il bene è stato ottenuto o prodotto. Se il bene è stato prodotto in più paesi, il paese o l'area geografica di origine è l'ultimo paese o l'area geografica in cui è stato elaborato in modo significativo.
* **Numero di identificazione IVA dell'operatore partner nello Stato membro di importazione**: questo è il numero di partita IVA dell'operatore partner nello Stato membro dell'importazione. La partita IVA viene utilizzata anche nello scambio di dati di esportazione intra-UE tra gli Stati Membri e consente agli Stati Membri di allocare i dati ricevuti alla società importatrice nel proprio paese o area geografica. Le unità di creazione dei report devono riportare la partita IVA della società che ha dichiarato l'acquisto intra Unione di beni nello Stato membro di importazione.

> [!NOTE]
> La partita IVA del partner aziendale da utilizzare può variare a seconda della circostanza aziendale. Ad esempio, l'ID da utilizzare è diverso per scenari come le vendite a catena, in cui un fornitore vende un prodotto in un altro paese e quindi l'azienda rivende l'articolo a un'altra attività nello stesso paese, commercio triangolare e così via. Se non sei sicuro della partita IVA corretta da utilizzare, ti consigliamo di rivolgerti a un esperto nel tuo paese o nella tua regione.

Facoltativamente è anche possibile impostare le opzioni seguenti:

* **Aree**: utilizzare a completamento delle informazioni sui paesi e le aree.  
* **Cod. spedizione Intrastat**: utilizzare per specificare le ubicazioni da cui si spediscono o si ricevono gli articoli da o verso altri paesi o aree geografiche. Un esempio di codice di spedizione Intrastat è l'aeroporto di Heathrow. I codici di spedizione Intrastat possono essere immessi nei documenti di vendita e di acquisto nella Scheda dettaglio **Commercio estero**. Queste informazioni vengono inoltre copiate dai movimenti articoli creati per le registrazioni Intrastat.  

### <a name="to-set-up-intrastat-templates-and-batches"></a>Per impostare le definizioni e i batch di registrazioni Intrastat

I processi batch Intrastat includono solo i movimenti articoli, non i movimenti di contabilità generale. Se nella contabilità generale sono presenti movimenti adatti per il reporting Intrastat, è necessario immetterli manualmente. Ad esempio, se si acquista un computer da un altro paese UE o un'altra area UE, il computer non viene inserito nell'inventario, ma registrato in un conto di contabilità generale. Questo tipo di movimento deve essere immesso manualmente nella registrazione Intrastat.  

È possibile esportare i movimenti in un file da inviare successivamente alle autorità Intrastat. È inoltre possibile stampare un report manualmente, immettere le informazioni nei moduli delle autorità, quindi inviare le informazioni.

> [!NOTE]
> È consigliabile impostare un batch Registrazione Intrastat per ogni mese.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Definizioni registrazioni Intrastat**, quindi scegli il collegamento correlato.  
2. Compila i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Crea una definizione per ogni modulo Intrastat che utilizzi.  
3. Per creare batch, scegliere l'azione **Batch**.  
4. Compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]. Creare una definizione per ogni modulo Intrastat che si utilizza.

> [!NOTE]
> Nel campo **Periodo statistico** immettere il periodo statistico sotto forma di numero a quattro cifre, dove le prime due rappresentano l'anno e le altre due il mese. Immettere, ad esempio, 1706 per indicare giugno 2017.

### <a name="to-set-up-transport-methods"></a>Per impostare i metodi di trasporto

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Metodi di trasporto**, quindi scegli il collegamento correlato.  
2. Compilare i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="to-set-up-which-intrastat-report-fields-are-mandatory"></a>Per impostare quali campi del report Intrastat sono obbligatori

In alcuni paesi/aree geografiche, come Spagna e Regno Unito, le autorità richiedono che i report Intrastat includano, ad esempio, il metodo di spedizione per gli acquisti o altri valori quando le vendite superano una certa soglia. Nella pagina **Setup Intrastat** è possibile selezionare **Setup checklist Intrastat** per impostare i campi obbligatori nella pagina **Registrazioni Intrastat**.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup Intrastat**, quindi scegli il collegamento correlato.
2. Scegliere l'azione **Setup checklist Intrastat**.
3. Nella pagina **Setup checklist Intrastat**, seleziona **Nome campo** per scegliere il campo del report Intrastat che vuoi rendere obbligatorio.

### <a name="czechia"></a>Repubblica Ceca

In particolare per le aziende ceche, devi anche impostare codici merce e codici natura transazione.  

#### <a name="to-set-up-commodity-codes"></a>Per impostare i codici di voci doganali

Tutti gli articoli acquistati o venduti devono disporre di un codice voce doganale.  

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Codici voci doganali**, quindi scegli il collegamento correlato.  
2. Compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Per assegnare un codice voce doganale a un articolo, nella pagina **Scheda articolo** espandere la Scheda dettaglio **Costi e registrazione**, quindi immettere il codice nel campo **Codice voce doganale**.

### <a name="italy"></a>Italia

In particolare per le aziende italiane, devi anche impostare codici merce e codici natura transazione.  

#### <a name="to-set-up-transaction-nature-codes"></a>Per impostare il codici della natura delle transazioni

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Codici natura transazione**, quindi scegli il collegamento correlato.  
2. Compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

> [!TIP]
> Se si utilizza con frequenza un determinato codice natura transazione, è possibile impostarlo come predefinito. A tale scopo, andare alla pagina **Impostazione Intrastat** e selezionare il codice.

## <a name="to-report-intrastat"></a>Per creare un report Intrastat

Dopo aver compilato le registrazioni Intrastat, puoi eseguire l'azione **Report Intrastat - Checklist** per verificare che tutte le informazioni nelle registrazioni siano corrette. I campi obbligatori impostati nella pagina **Setup checklist Intrastat** in cui mancano i valori verranno mostrati in Dettaglio informazioni di Errori e e avvisi nella pagina **Registrazioni Intrastat**. È successivamente possibile stampare un report Intrastat come form, oppure creare un file da inviare a un'autorità fiscale del proprio paese.  

### <a name="to-fill-in-intrastat-journals"></a>Per compilare le registrazioni Intrastat

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registrazioni Intrastat**, quindi scegli il collegamento correlato.  
2. Nella pagina **Registrazioni Intrastat**, nel campo **Nome batch** scegliere il batch di registrazioni interessato e quindi scegliere **OK**.  
3. Scegliere l'azione **Suggerisci righe**. I campi **Data inizio** e **Data fine** verranno compilati automaticamente con le date specificate per il periodo statistico del batch di registrazioni.  
4. Nel campo **% regolazione costi** è possibile immettere una percentuale per coprire trasporto e assicurazione. In questo caso il valore contenuto del campo **Valore Statistico** sarà proporzionalmente maggiore.  
5. Selezionare **OK** per avviare il processo batch.  

Il processo batch recupererà tutti i movimenti articolo nel periodo statistico indicato e li inserirà come righe nelle registrazioni Intrastat. Le righe possono essere modificate secondo le esigenze.  

> [!IMPORTANT]  
> Il processo batch recupera soltanto i movimenti che contengono un codice paese per il quale è stato immesso un codice Intrastat nella pagina **Paesi**. È quindi importante immettere codici Intrastat per i codici paese che verranno inclusi nel processo batch. Il lavoro batch imposta il campo **Partita IVA partner** su *QV999999999999* per i privati o le imprese senza partita IVA (clienti con il campo **Tipo di partner Intrastat** impostato su *Persona*), e utilizza il valore del campo **Tipo di transazione** sul movimento contabile articolo registrato o sul movimento contabile processo.

### <a name="to-modify-intrastat-journals-lines"></a>Per modificare le righe dei giornali di registrazione Intrastat

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registrazioni Intrastat**, quindi scegli il collegamento correlato.  
2. Nella pagina **Registrazioni Intrastat**, nel campo **Nome batch** scegliere il batch di registrazioni interessato e quindi scegliere **OK**.  
3. Usa il riquadro dei filtri per filtrare le righe del giornale di registrazione Intrastat in base ad alcuni criteri. Ad esempio, filtra per i campi **Partita IVA partner** con il valore *QV999999999999*.
4. Scegli l'icona **Condividi** ![Condividi una pagina in un'altra app.](media/share-icon.png) e seleziona **Modifica in Excel**
5. In Excel, modifica le righe del giornale di registrazione Intrastat che hai filtrato. Ad esempio, modifica i valori dei campi **Tipo di transazione**.  
6. Pubblica le modifiche apportate in Excel nuovamente in [!INCLUDE[prod_short](includes/prod_short.md)]

> [!NOTE]
> Nelle versioni di [!INCLUDE[prod_short](includes/prod_short.md)] che non supportano [**Modifica in Excel**](across-work-with-excel.md#edit-in-excel) per i giornali di registrazione, puoi creare pacchetti di configurazione per esportare e importare le righe del giornale di registrazione Intrastat in Excel. Per ulteriori informazioni, vedere [Eseguire la migrazione dei dati locali in Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) nel contenuto amministrativo.

### <a name="report-intrastat-on-a-form-or-a-file"></a>Creare report Intrastat come form o come file

Per ottenere le informazioni richieste nel modulo Intrastat dagli enti di statistica, è necessario stampare il report **Intrastat - Form**. Prima di eseguire questa operazione, è necessario preparare le registrazioni Intrastat e compilarle. Se vi sono sia transazioni di vendita che di acquisto, è necessario compilare un form separato per ciascun tipo e stampare il report due volte.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registrazioni Intrastat**, quindi scegli il collegamento correlato.  
2. Nella pagina **Registrazioni Intrastat** selezionare il batch registrazioni desiderato nel campo **Nome batch**.  
3. Se non è stato fatto in precedenza, compilare le registrazioni manualmente o scegliere l'azione **Suggerisci righe**.  
4. Scegliere l'azione **Stampa registrazione Intrastat**.  
5. Nella Scheda dettaglio **Righe reg. Intrastat** aggiungere un filtro **Tipo**, quindi specificare se si tratta di **Carico** o **Spedizione**.  
6. Per stampare il report, fare clic su **Invia a**.  

### <a name="report-intrastat-in-a-file"></a>Creare un report Intrastat in un file

È possibile inviare il report Intrastat come file. Prima di creare il file è possibile stampare un report di controllo che conterrà le stesse informazioni presenti nel file.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registrazioni Intrastat**, quindi scegli il collegamento correlato.  
2. Nella pagina **Registrazioni Intrastat** selezionare il batch registrazioni desiderato nel campo **Nome batch**.  
3. Se non è stato fatto in precedenza, compilare le registrazioni manualmente o scegliendo l'azione **Suggerisci righe**.  
4. Scegliere l'azione **Crea file**.  
5. Nella pagina del processo batch scegliere il pulsante **OK**.  
6. Selezionare **Salva**.  
7. Spostarsi sul percorso in cui si desidera salvare il file, quindi immettere il nome file desiderato e fare clic su **Salva**.

> [!NOTE]
> Quando una riga del report Intrastat ha un'unità di misura supplementare, il peso dell'articolo non viene visualizzato perché il valore non è obbligatorio.

## <a name="reorganize-intrastat-journals"></a>Riorganizzare registrazioni Intrastat

I report Intrastat vengono presentati con cadenza mensile e per ogni report è necessario creare un nuovo batch di registrazioni. Dopo un certo periodo, si saranno accumulati diversi batch di registrazioni. Le righe di registrazioni non vengono eliminate automaticamente. È possibile riorganizzare periodicamente i nomi batch contabili. Questa operazione viene effettuata eliminando i batch di registrazioni non più necessari. Vengono eliminate anche le righe di registrazioni di questi batch.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registrazioni Intrastat**, quindi scegli il collegamento correlato.  
2. Per visualizzare le opzioni, scegliere il campo **Nome batch**.  
3. Scegli i batch registrazioni da eliminare a quindi scegli il pulsante **Elimina**.  

## <a name="tariff-numbers"></a>Nomenclatura combinata

In molti paesi o aree geografiche, le autorità doganali e fiscali hanno stabilito dei codici a otto cifre per i vari articoli. Perché i movimenti degli articoli contengano le necessarie informazioni quando vengono importati nella riga delle registrazioni Intrastat, è necessario che nella pagina **Nomenclature combinate** vengano specificate le opportune informazioni sulle nomenclature combinate. È necessario trovare i codici degli articoli di cui si occupa la propria società e immetterli nella pagina **Nomenclatura combinata**.

Impostare nella pagina **Nomenclature combinate** tutti i codici utilizzati. Prima di iniziare la registrazione è necessario immettere i codici nella scheda articolo. Una volta impostati, immetterli nel campo **Nomenclatura combinata** della scheda articolo. Compilare anche il campo **Peso netto** della scheda articolo.

## <a name="see-also"></a>Vedere anche

[Gestione contabile](finance.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
