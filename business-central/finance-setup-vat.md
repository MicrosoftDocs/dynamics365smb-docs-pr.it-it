---
title: Impostare l'IVA (imposta sul valore aggiunto)
description: 'Assicurarsi di calcolare, registrare e creare report corretti per l''IVA di vendite e acquisti. Si consiglia di utilizzare il setup assistito per impostare l''IVA.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'VAT, posting, tax, value-added tax'
ms.search.form: '10, 118, 391, 470, 471, 472, 575, 734, 747, 748, 1877,'
ms.date: 01/31/2023
ms.author: bholtorf
---

# <a name="set-up-calculations-and-posting-methods-for-value-added-tax" />Setup dei calcoli e registrazione dei metodi per l'IVA

I consumatori e le imprese pagano l'imposta sul valore aggiunto (IVA) quando acquistano beni o servizi. L'importo dell'IVA da pagare può variare, a seconda di diversi fattori. In [!INCLUDE[prod_short](includes/prod_short.md)], puoi impostare l'IVA per specificare l'aliquota da utilizzare per calcolare gli importi IVA in base ai seguenti parametri:

* Persone a cui si vende  
* Persone da cui si acquista  
* Merci vendute  
* Merci acquistate  

È possibile impostare manualmente i calcoli IVA, ma può essere complesso e richiedere molto tempo. In caso contrario, sarebbe molto facile utilizzare erroneamente diverse aliquote IVA e creare report sull'IVA inaccurati. Per facilitare la configurazione dell'IVA, ti consigliamo di utilizzare La guida **Impostazione IVA** fornita nel prodotto. 

Tuttavia se vuoi impostare i calcoli IVA manualmente, o se vuoi conoscere ciascun passaggio, in questo articolo vengono fornite descrizioni per ogni fase.  

[!INCLUDE [finance-vat](includes/finance-vat.md)]

## <a name="set-up-vat-using-the-assisted-setup-guide-recommended" />Impostare l'IVA utilizzando la guida al setup assistito (consigliato)

> [!NOTE]
> Puoi utilizzare la procedura guidata **Impostazione IVA** solo se è stata creata una società *La mia azienda* e se non sono state registrate transazioni con IVA.

Per avviare la Guida assistita al setup, attenersi a questa procedura:

1. Scegli l'icona ![lampadina che apre la funzione Dimmi 1.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") e immetti **Setup assistito**. 
2. Scegli **Imposta IVA** e completa i passaggi.
3. Dopo aver completato il setup assistito, visita la pagina **Setup registrazioni IVA** e verifica se è necessario compilare campi aggiuntivi in base ai requisiti della versione di [!INCLUDE [prod_short](includes/prod_short.md)]. Ulteriori informazioni in [Funzionalità locale in Business Central](about-localization.md).  

### <a name="check-the-vat-posting-setup" />Controllare il setup registrazioni IVA

Per iniziare velocemente, [!INCLUDE [prod_short](includes/prod_short.md)] ti mostrerà le notifiche se mancano conti di contabilità generale (C/G) nelle categorie di registrazione o nei setup di registrazione, come la pagina **Setup registrazioni IVA**. Puoi attivare o disattivare questo tipo di notifica utilizzando la notifica *Il conto C/G non è presente nel setup o nella categoria di registrazione* nella pagina **Notifiche personali**. Vai alla pagina **Impostazioni personali** e scegli *Modifica il momento in cui ricevere le notifiche*. .  

Se scegli una tale notifica, [!INCLUDE [prod_short](includes/prod_short.md)] crea automaticamente i setup registrazioni in base alle categorie di registrazione nel documento o nella registrazione su cui stai attualmente lavorando.  

A questo punto, puoi semplicemente compilare i conti C/G mancanti. Quindi, in seguito, quando perfezioni ulteriormente la configurazione, potresti renderti conto che questa configurazione iniziale era sbagliata. [!INCLUDE [prod_short](includes/prod_short.md)] non consente l'eliminazione di un setup registrazioni IVA e di un setup registrazioni COGE quando sono presenti movimenti creati in base a tali configurazioni. A partire dal primo ciclo di rilascio del 2022, puoi utilizzare il campo **Bloccato** nella pagina **Setup registrazioni IVA** per impedire agli utenti di utilizzare erroneamente un'impostazione che non è più rilevante per le nuove registrazioni.

## <a name="set-up-a-default-vat-date-for-documents-and-journals" />Impostare una data IVA predefinita per documenti e giornali di registrazione

La dichiarazione IVA in [!INCLUDE [prod_short](includes/prod_short.md)] si basa sulla **Data IVA** per includere i movimenti IVA nei report IVA in un periodo IVA. La data IVA può essere modificata su tutti i documenti e giornali di registrazione, ma è necessario specificare un valore predefinito per la data IVA.

> [!NOTE]
> Dopo la registrazione del documento o del giornale, la **Data IVA** apparirà in **Movimenti IVA** e **Movimenti C/G** così come sul documento registrato se esiste.

Per impostare un valore predefinito per una data IVA, attieniti alla seguente procedura:

1. Scegli l'icona ![lampadina che apre la funzione Dimmi 1.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") e immetti **Setup contabilità generale**, quindi scegli il collegamento correlato.  
2. Sulla Scheda dettaglio **Generale**, nel campo **Data IVA predefinita** scegli **Data di registrazione** o **Data del documento**.
3. Chiudere la pagina.  

> [!NOTE]
> Per impostazione predefinita, la **Data IVA predefinita** è la **Data di registrazione**.

### <a name="enabling-or-disabling-the-vat-date-feature" />Abilitazione o disabilitazione della funzione Data IVA

Alcuni paesi richiedono che le aziende utilizzino una data IVA specifica, mentre altri paesi no. Alcuni paesi richiedono inoltre alle aziende di modificare la data IVA in situazioni specifiche dopo aver registrato i documenti, mentre altri paesi non consentono modifiche alle date IVA. Per consentire contesti diversi, puoi scegliere se utilizzare questa funzionalità e, in tal caso, in quale misura.

Per impostare il livello di utilizzo della data IVA, procedi nel seguente modo:

1. Scegli la ![lampadina che apre la funzione Dimmi 1.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") e immetti **Setup contabilità generale**, quindi scegli il collegamento correlato.  
2. Nella scheda dettaglio **Generale**, nel campo **Utilizzo data IVA**, specifica il grado in cui vuoi utilizzare la funzionalità data IVA. È possibile scegliere tra le seguenti opzioni:

| Tipo | Descrizione |
|--------------------|-----------------------------------------|
| **Utilizzare la funzionalità Data IVA completa** | Tutto ciò che riguarda **Data IVA** funziona per impostazione predefinita, offrendoti il massimo della funzionalità **Data IVA**. È possibile impostare la data, modificarla nei documenti, creare report basati sulla data e modificare la data dopo la pubblicazione, purché il periodo non sia chiuso o protetto con date consentite per la pubblicazione. |
| **Utilizzare ma non consentire le modifiche** | Tutto ciò che riguarda la **Data IVA** funziona per impostazione predefinita con un'eccezione. Non puoi modificare la **Data IVA** in **Movimenti IVA**. |
| **Non utilizzare la funzionalità Data IVA** | [!INCLUDE [prod_short](includes/prod_short.md)] nasconderà e renderà non disponibili i campi **Data IVA** su documenti, registrazioni e movimenti. La **Data IVA predefinita** sarà configurata come **Data di registrazione**. |

3. Chiudere la pagina.

> [!IMPORTANT]
> Anche se hai scelto l'opzione **Non utilizzare la funzionalità Data IVA**, [!INCLUDE [prod_short](includes/prod_short.md)] usa la **Data IVA** in background. Poiché la **Data IVA predefinita** è configurata come **Data di registrazione** e in questo caso non è possibile modificarla, otterrai la stessa esperienza senza questa funzione. I campi **Data IVA** saranno rimossi da tutte le pagine, ma questo campo continuerà a esistere nelle tabelle e i report funzioneranno in base ad esso.

### <a name="limiting-periods-for-posting-and-changing-the-vat-date" />Limitazione dei periodi per la registrazione e modifica della data IVA

Puoi impedire alle persone di registrare o modificare i movimenti IVA in intervalli di date specifici. Puoi impostare la restrizione utilizzando due impostazioni:

* In base al **periodo di dichiarazione IVA** chiuso
* In base ai campi **Consenti registrazione da** e **Consenti registrazione a**.

#### <a name="to-limit-posting-based-on-vat-return-period" />Per limitare la registrazione in base al periodo di dichiarazione IVA

1. Scegli l'icona ![lampadina che apre la funzione Dimmi 1.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup contabilità generale**, quindi scegli il collegamento correlato.  
2. Nella scheda dettaglio **Generale**, nel campo **Controllo periodo IVA**, specifica il grado di controllo del periodo di dichiarazione IVA. Nella seguente tabella vengono illustrate le opzioni.

| Tipo | Descrizione |
|--------------------|-----------------------------------------|
| **Blocca registrazione per periodo chiuso e avvisa per periodo rilasciato** | Impedisci alle persone di registrare un documento o una registrazione o di modificare i movimenti IVA che hanno una data IVA in un **periodo di dichiarazione IVA** chiuso. [!INCLUDE [prod_short](includes/prod_short.md)] mostrerà anche un avviso se il tuo **Periodo di dichiarazione IVA** è aperto, ma lo stato della **Dichiarazione IVA** è **Rilasciato** or **Inviato**. |
| **Blocca registrazione per periodo chiuso** | Impedisci alle persone di registrare un documento o una registrazione o di modificare i movimenti IVA che hanno una data IVA nel **periodo di dichiarazione IVA** chiuso. |
| **Avvisa per registrazione in periodo chiuso** | Mostra un avviso, ma non bloccare la registrazione, se desideri registrare un documento o una registrazione che ha una data IVA in un **periodo di dichiarazione IVA** chiuso. |
| **Disabilitato** | Non intraprendere alcuna azione sulla base di un **periodo di dichiarazione IVA** chiuso. |

#### <a name="to-limit-posting-based-on-allow-fromto-period" />Per limitare la registrazione in base a Consenti dal/al periodo

È possibile impostare limitazioni per l'azienda o livelli utente specifici.

Per limitare tutte le registrazioni per l'intera azienda:

1. Scegli l'icona ![lampadina che apre la funzione Dimmi 1.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup contabilità generale**, quindi scegli il collegamento correlato.  
2. Nella scheda dettaglio **Generale**, nel campo **Consenti registrazione da** , specifica la data IVA a partire dalla quale consenti la registrazione. La registrazione di un documento o un giornale con una data IVA precedente a questa data non è consentita.  
3. Nella scheda dettaglio **Generale**, nel campo **Consenti registrazione a** , specifica la data IVA fino alla quale consenti la registrazione. La registrazione di un documento o un giornale con una data IVA dopo questa data non è consentita.

Per limitare le registrazioni per l'utente specifico:

1. Scegli l'icona ![lampadina che apre la funzione Dimmi 1.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup utente**, quindi scegli il collegamento correlato.  
2. Nel campo **ID utente** specifica l'utente a cui desideri consentire di registrare in un periodo specifico.  
3. Nel campo **Consenti registrazione da** specifica la data IVA a partire dalla quale consenti la registrazione. La registrazione di un documento o un giornale con una data IVA precedente a questa data non è consentita.
4. Nel campo **Consenti registrazione a** specifica la data IVA fino alla quale consenti la registrazione. La registrazione di un documento o un giornale con una data IVA dopo questa data non è consentita.

## <a name="set-up-vat-registration-numbers-for-your-country-or-region" />Impostare i numeri di partita IVA per il paese o l'area geografica

Per garantire che le persone inseriscano numeri di partita IVA validi, è possibile definire i formati per i numeri di partita IVA utilizzati nei paesi in cui si opera. [!INCLUDE[prod_short](includes/prod_short.md)] visualizza un messaggio di errore quando qualcuno commette un errore o utilizza un formato non corretto per il paese.

Per impostare i numeri di partita VAT, attenersi a questa procedura:

1. Scegli la ![lampadina che apre la funzione Dimmi 2](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"). immetti **Paesi/Aree geografiche**.
2. Specificare il paese e quindi scegliere l'azione **Formati Nr. P. IVA**.
3. Nel campo **Formati**, specificare il formato immettendo uno o più dei seguenti caratteri:  

* **#** Richiede un numero a una cifra.  
* **@** Richiede una lettera. Il formato non rispetta la distinzione tra maiuscole e minuscole.  
* **?** Consente qualsiasi carattere.  

    > [!TIP]
    > È possibile utilizzare altri caratteri purché siano sempre presenti nel formato del paese. Se è necessario includere un punto o un trattino tra i set di numeri, è possibile definire il formato come ##.####.### o @@-###-###.  

## <a name="set-up-vat-business-posting-groups" />Impostare le categorie di registrazione business IVA

Le categorie di registrazione business IVA dovrebbero rappresentare i mercati in cui si intrattengono relazioni commerciali con clienti e fornitori e dovrebbero definire il modo in cui calcolare l'IVA in ogni mercato. Esempi di categoria di registrazione business IVA sono **Nazionale** e **Unione Europea (UE)**.  

Utilizzare codici semplici da ricordare e che descrivano la categoria di registrazione business, ad esempio **Nazionale**, **UE**, **Non UE**. Ogni codice deve essere univoco e non è possibile utilizzare lo stesso codice più volte in una tabella, sebbene sia possibile impostare un numero indefinito di codici.

Per impostare una categoria di registrazione business IVA, attenersi a questa procedura:

1. Scegli la ![lampadina che apre la funzione Dimmi 3.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Cat. reg. business IVA**, quindi scegli il collegamento correlato.  
2. Compilare i campi in base alle esigenze.

Le categorie di registrazione business IVA di default vengono impostate collegandole alle categorie di registrazione business. [!INCLUDE[prod_short](includes/prod_short.md)] assegna automaticamente la categoria di registrazione business IVA quando viene assegnata la categoria di registrazione business a un cliente, un fornitore o un conto di contabilità generale.

## <a name="set-up-vat-product-posting-groups" />Impostare le categorie di registrazione articoli/servizi IVA

Le categorie di registrazione articoli/servizi IVA rappresentano articoli e risorse acquistate o vendute e determinano la tipologia di calcolo e di registrazione dell'IVA in base al tipo di articolo o risorsa.

Si consiglia di utilizzare codici semplici da ricordare e descrittivi. Ad esempio, **NO-IVA** o **Zero**, **IVA10** o **Ridotta** per IVA al 10% e **IVA25** o **Standard** per il 25%.

Per impostare una categoria di registrazione business IVA, attenersi a questa procedura:

1. Scegli la ![lampadina che apre la funzione Dimmi 4.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Categorie registrazioni articoli/servizi IVA**, quindi scegli il collegamento correlato.  
2. Compilare i campi in base alle esigenze.

## <a name="combine-vat-posting-groups-in-vat-posting-setups" />Combinare le categorie di registrazione IVA nei setup registrazione IVA

[!INCLUDE[prod_short](includes/prod_short.md)] calcola gli importi IVA su vendite e acquisti in base alle impostazioni di registrazione IVA, che sono combinazioni di categorie di registrazione business e di categorie di registrazione articoli/servizi IVA. Per ogni combinazione, è possibile specificare la percentuale IVA, la tipologia di calcolo IVA e i numeri di conto C/G per la registrazione dell'IVA relativa a vendite e acquisti e dell'IVA intracomunitaria. È inoltre possibile specificare se l'IVA viene ricalcolata quando viene applicato o ricevuto uno sconto pagamento.  

È possibile impostare un numero illimitato di combinazioni. Se si desidera raggruppare combinazioni di setup di registrazioni IVA con attributi simili, è possibile definire un **codice IVA** per ogni categoria e assegnare il codice ai membri della categoria.

Per combinare setup di registrazioni IVA, attenersi a questa procedura:

1. Scegli l'icona ![lampadina che apre la funzione Dimmi 5.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup registrazioni IVA**, quindi scegli il collegamento correlato.
2. Compilare i campi in base alle esigenze. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

## <a name="assign-vat-posting-groups-by-default-to-multiple-entities" />Assegnare le categorie di registrazione IVA per impostazione predefinita a più entità

Se si desidera applicare le stesse categorie di registrazione IVA a più entità, è possibile impostare [!INCLUDE[prod_short](includes/prod_short.md)] per effettuare questa operazione in modo predefinita. Esistono due metodi per farlo:

* È possibile assegnare le categorie di registrazione business IVA a categorie di registrazione business generali, o modelli cliente o fornitore
* È possibile assegnare le categorie di registrazione articolo/categorie IVA in categorie di registrazione di articoli e servizi generali  

La categoria registrazione business o articoli/servizi IVA è assegnata quando si sceglie una categoria registrazione business o articoli/servizi per un cliente, un fornitore, un articolo o una risorsa.

## <a name="assign-vat-posting-groups-to-accounts-customers-vendors-items-and-resources" />Assegnare le categorie di registrazione IVA a conti, clienti, fornitori, articoli e risorse

Nelle sezioni successive viene descritto come assegnare le categorie di registrazione IVA alle singole entità.

### <a name="to-assign-vat-posting-groups-to-individual-general-ledger-accounts" />Per assegnare categorie di registrazione IVA a singoli conti di contabilità generale

1. Scegli l'icona ![lampadina che apre la funzione Dimmi 6.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Piano dei conti**, quindi scegli il collegamento correlato.  
2. Aprire la scheda **Conto C/G** per il conto.  
3. Nella Scheda dettaglio **Registrazione**, nel campo **Tipo reg. gen.**, selezionare **Vendita** o **Acquisto**.  
4. Scegliere le categorie di registrazione IVA da utilizzare per il conto vendite o acquisti.  

### <a name="to-assign-vat-business-posting-groups-to-customers-and-vendors" />Per assegnare le categorie di registrazione business IVA a clienti e fornitori

1. Scegli l'icona ![lampadina che apre la funzione Dimmi 7.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Cliente** o **Fornitore**, quindi scegli il collegamento correlato.  
2. Nella scheda del **Cliente** o **Fornitore**, espandere la Scheda dettaglio **Fatturazione**.  
3. Scegliere la categoria di registrazione business IVA.  

### <a name="to-assign-vat-product-posting-groups-to-individual-items-and-resources" />Per assegnare le categorie di registrazione articoli/servizi IVA a singoli articoli e risorse

1. Scegli l'icona ![lampadina che apre la funzione Dimmi 8.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Articolo** o **Risorsa**, quindi scegli il collegamento correlato.  
2. Effettuare una delle seguenti operazioni:  

    * Nella scheda **Articolo** espandere la Scheda dettaglio **Prezzo e registrazione** quindi scegliere **Mostra di più** per visualizzare il campo **Cat. reg. art./serv. IVA**.  
    * Nella scheda **Risorsa** espandere la Scheda dettaglio **Fatturazione**.  
3. Scegliere la categoria di registrazione articoli/servizi IVA.  

## <a name="set-up-clauses-to-explain-vat-exemption-or-non-standard-vat-rates" />Impostare le categorie per spiegare l'esenzione IVA o le aliquote IVA non standard

È possibile impostare una categoria IVA per descrivere informazioni sul tipo di IVA che viene applicata. Le informazioni possono essere obbligatorie per la normativa statale. Dopo aver impostato una categoria IVA e averla associata a un setup registrazioni IVA, la categoria IVA viene visualizzata su tutti i documenti di vendita stampati con tale categoria di setup registrazioni IVA.

Se necessario, è anche possibile specificare come tradurre automaticamente le categorie IVA in altre lingue. Successivamente, quando si crea e si stampa un documento di vendita contenente un codice IVA, il documento includerà la categoria IVA nel testo tradotto. Il codice lingua specificato nella scheda cliente determina la lingua.

Quando vengono utilizzate aliquote IVA non standard in diversi tipi di documenti, come fatture o note di credito, le società sono generalmente tenute a includere un testo di esenzione (categoria IVA) indicante il motivo per cui è stata calcolata un'IVA ridotta o un'aliquota IVA zero. È possibile definire diverse categorie IVA da includere nei documenti commerciali per tipo di documento, come fattura o nota di credito. È possibile eseguire questa operazione nella pagina **Categorie IVA per tipo di documento**.

È possibile modificare o eliminare una categoria IVA. Le modifiche si rifletteranno in un report generato. Tuttavia, [!INCLUDE[prod_short](includes/prod_short.md)] non conserva una cronologia della modifica. Nel report, le descrizioni della categoria IVA vengono stampate e visualizzate per tutte le righe del report accanto all'importo IVA e all'imponibile IVA. Se una categoria IVA non è stata definita per alcune righe del documento di vendita, allora viene omessa l'intera sezione quando il report viene stampato.

### <a name="to-set-up-vat-clauses" />Impostare categorie IVA

1. Scegli l'icona ![lampadina che apre la funzione Dimmi 9.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Categorie IVA**, quindi scegli il collegamento correlato.  
2. Nella pagina **Categorie IVA** creare una nuova riga.  
3. Nel campo **Codice** immettere un identificatore per la categoria. Il codice viene usato per assegnare la categoria ai categorie di registrazione IVA.  
4. Nel campo **Descrizione** immettere il testo per l'esenzione IVA che si desidera visualizzare nei documenti che possono includere l'IVA. Nel campo **Descrizione 2** immetti testo aggiuntivo, se necessario. Il testo verrà visualizzato sulle nuove righe dei documenti.
5. Scegli l'azione **Descrizione per tipo di documento**.
6. Nella pagina **Categorie IVA per tipo di documento**, compila i campi per impostare il testo per l'esenzione IVA da visualizzare tipi di documento specifici.  
7. Facoltativo: per assegnare direttamente la categoria IVA a un setup registrazioni IVA, scegliere **Setup** e quindi la categoria. Se si desidera attendere, è possibile assegnare la categoria in seguito nella pagina **Setup registrazioni IVA**.  
8. Facoltativo: per specificare come tradurre automaticamente la categoria IVA scegliere l'azione **Traduzioni**.

### <a name="to-assign-a-vat-clause-to-a-vat-posting-setup" />Per assegnare una categoria IVA a un setup di registrazione

1. Scegli l'icona ![lampadina che apre la funzione Dimmi 10.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup registrazioni IVA**, quindi scegli il collegamento correlato.  
2. Nella colonna **Categoria IVA** selezionare la categoria e utilizzarla per ogni setup registrazione IVA a cui si applica.  

### <a name="to-specify-translations-for-vat-clauses" />Per specificare le traduzioni per le categorie IVA

1. Scegli l'icona ![lampadina che apre la funzione Dimmi 11.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Categorie IVA**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Traduzioni**.  
3. Nel campo **Codice lingua** selezionare la lingua verso cui tradurre.  
4. Nei campi **Descrizione** e **Descrizione 2** immettere il testo tradotto delle descrizioni. Questo testo viene visualizzato nei documenti di report IVA tradotti.  

### <a name="to-specify-extended-text-for-vat-clauses" />Per specificare il testo esteso per le clausole IVA

> [!NOTE]  
> Se il tuo paese o area richiede un testo più lungo per le clausole IVA rispetto a quanto supportato dalla versione predefinita, puoi specificare il testo più lungo per le clausole IVA come *testo esteso* in modo che venga stampato sui report di vendita e acquisto.  

1. Scegli l'icona ![lampadina che apre la funzione Dimmi 11.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Categorie IVA**, quindi scegli il collegamento correlato.  
2. Scegli l'azione **Testi estesi**.  
3. Scegliere l'azione **Nuovo**.  
4. Compila i campi **Codice lingua** e **Descrizione**.  
5. Facoltativamente, seleziona il campo **Tutti cod. lingua** o specifica la lingua pertinente nel campo **Codice lingua** se utilizzi i codici lingua.  
6. Compilare i campi **Data inizio** e **Data fine** se si desidera limitare il periodo in cui il testo esteso verrà utilizzato.  
7. Nelle righe **Testo** scrivi il testo esteso per le tue clausole IVA.  
8. Seleziona i campi rilevanti per i tipi di documento su cui desideri stampare il testo esteso.  
9. Chiudere la pagina.  

## <a name="create-a-vat-posting-setup-to-handle-import-vat" />Creare un setup registrazioni IVA per gestire l'IVA sulle importazioni

La funzionalità relativa all'*IIVA sulle importazioni* viene utilizzata quando è necessario registrare un documento in cui l'intero importo è IVA. Si userà questa funzionalità quando si riceve una fattura con IVA dalle autorità fiscali per merci importate.  

Per impostare i codici per l'IVA sull'importazione, attenersi a questa procedura:  

1. Scegli l'icona ![lampadina che apre la funzione Dimmi 12.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Categorie registrazioni articoli/servizi IVA**, quindi scegli il collegamento correlato.  
2. Nella pagina Categorie reg. art./serv. IVA impostare una nuova categoria di registrazione articoli/servizi IVA per l'IVA da importazione.  
3. Scegli l'icona ![lampadina che apre la funzione Dimmi 13.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup registrazioni IVA**, quindi scegli il collegamento correlato.  
4. Nella pagina Setup registrazioni IVA creare una nuova riga o utilizzare una delle categorie di registrazione business IVA esistenti in combinazione con la nuova categoria di registrazione articoli/servizi IVA per l'IVA da importazione.  
5. Nel campo **Tipologia IVA** selezionare **Sola IVA**.  
6. Nel campo **Conto IVA Acquisti** immettere il conto C/G da utilizzare per registrare l'IVA da importazione. Tutti gli altri conti sono facoltativi.  

## <a name="use-reverse-charge-vat-for-trade-between-eu-countries-or-regions" />Usare l'IVA intracomunitaria per il commercio tra i paesi della UE

Per il commercio tre due società nell'Unione Europea, per alcune società è necessario utilizzare l'IVA intracomunitaria. Ad esempio, la regola si applica agli acquisti e alle vendite nei paesi UE.  

> [!NOTE]  
> Questa regola è valida per il commercio con società registrate come soggette a IVA in un altro paese UE. Se si hanno relazioni commerciali dirette con clienti in altri paesi UE, è necessario contattare le autorità fiscali per informazioni sulle regole IVA applicabili.  

> [!TIP]  
> È possibile verificare che la società sia registrata come soggetto IVA in un altro paese UE utilizzando il servizio di convalida partita IVA UE. Il servizio è disponibile gratuitamente in [!INCLUDE[prod_short](includes/prod_short.md)]. Per ulteriori informazioni, vedi [Verificare i numeri di partita IVA](finance-how-validate-vat-registration-number.md).

### <a name="sales-to-eu-countries-or-regions" />Vendite ai paesi UE

Sulle vendite a società soggette a IVA in altri paesi UE l'IVA non viene calcolata. È necessario indicare il valore di tali vendite ai paesi UE separatamente nella dichiarazione IVA.  

Per calcolare correttamente l'IVA sulle vendite nei paesi UE, è necessario effettuare le seguenti operazioni:  

* Impostare una riga per le vendite con le stesse informazioni degli acquisti. Se sono già state impostate righe nella pagina **Setup registrazioni IVA** per gli acquisti dai paesi UE, è possibile quindi utilizzare tali righe anche per le vendite.  
* Assegnare categorie di registrazione business IVA nel campo **Cat. reg. business IVA** nella Scheda dettaglio **Fatturazione** della scheda cliente di ciascun cliente dell'UE. È inoltre necessario immettere la partita IVA del cliente nel campo **Partita IVA** della Scheda dettaglio **Commercio estero**.  

Quando si registra una vendita a un cliente in un altro paese UE, viene calcolato l'importo IVA e viene creato un movimento IVA con le informazioni sull'IVA intracomunitaria e sull'imponibile IVA, ovvero l'importo utilizzato per calcolare l'importo IVA. Non vengono registrati movimenti nei conti IVA nella contabilità generale.

Per usare questa combinazione delle categorie di registrazione business IVA e articoli/servizi IVA per dichiararla come servizio nei report IVA periodici, contrassegnare il campo **Servizio UE**.

> [!NOTE]  
> Il campo **Servizio UE** è applicabile solo per le dichiarazioni IVA. Il campo non è correlato alle funzionalità **Dichiarazione di servizio** o **Intrastat per servizi** .

## <a name="vat-rounding-for-documents" />Arrotondamento IVA per i documenti

Gli importi nei documenti che non sono ancora stati registrati vengono arrotondati e visualizzati in modo da corrispondere all'arrotondamento finale degli importi effettivamente registrati. L'IVA viene calcolata per un documento completo, cioè l'IVA che viene calcolata è basata sulla somma di tutte le righe con lo stesso identificatore IVA nel documento.  

## <a name="set-up-vat-reporting" />Impostazione report IVA

È necessario impostare le informazioni su come le autorità fiscali del proprio paese o area geografica richiedono l'invio dei report IVA. I passaggi seguenti illustrano le informazioni più comunemente utilizzate. Tuttavia, il tuo paese o la tua area geografica potrebbero richiedere altri passaggi. Per ulteriori informazioni, vedi l'articolo pertinente nella sezione *Funzionalità locale* nel pannello a sinistra.

[!INCLUDE [vat-report-setup](includes/vat-report-setup.md)]

## <a name="see-related-microsoft-trainingtrainingpathsprocess-vat-dynamics--business-central" />Vedi il relativo [training Microsoft](/training/paths/process-vat-dynamics-365-business-central/)

## <a name="see-also" />Vedere anche

[Impostazione di definizioni di dichiarazione IVA e di nomi delle dichiarazioni IVA](finance-how-setup-vat-statement.md)  
[Impostare l'IVA ad esigibilità differita](finance-setup-unrealized-vat.md)  
[Dichiarare l'IVA a un'autorità fiscale](finance-how-report-vat.md)  
[Utilizzare l'IVA nelle vendite e negli acquisti](finance-work-with-vat.md)  
[Utilizzare lo strumento di modifica dell'aliquota IVA](finance-how-use-vat-rate-change-tool.md)  
[Verificare i numeri di partita IVA](finance-how-validate-vat-registration-number.md)  
[Funzionalità locale in Business Central](about-localization.md)  
[Report IVA norvegese nella versione tedesca](LocalFunctionality/Germany/vat-reporting.md)  
[IVA belga](LocalFunctionality/Belgium/belgian-vat.md)  
[IVA italiana](LocalFunctionality/Italy/italian-vat.md)  
[Impostare le dichiarazioni elettroniche IVA e ICP nella versione olandese](LocalFunctionality/Netherlands/how-to-set-up-electronic-vat-and-icp-declarations.md)  
[Report IVA nella versione spagnola](LocalFunctionality/Spain/vat-reports.md)  
[Impostare la registrazione fiscale di beni e servizi nella versione australiana](LocalFunctionality/Australia/how-to-set-up-goods-and-service-tax-posting.md)  
[IVA nella versione ceca](LocalFunctionality/Czech/finance-vat.md)  
[Report IVA norvegese nella versione norvegese](LocalFunctionality/Norway/norwegian-vat-reporting.md)  
[Report imposta su beni e servizi e vendite armonizzate in Canada](LocalFunctionality/Canada/sales-tax-goods-services.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
