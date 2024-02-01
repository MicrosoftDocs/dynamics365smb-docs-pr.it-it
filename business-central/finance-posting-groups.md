---
title: Configurazione di categorie di registrazione
description: Scopri come utilizzare categorie di registrazione per risparmiare tempo ed evitare errori quando si registrano le transazioni.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.search.keywords: 'posting setup, initialize'
ms.search.form: '312, 313'
ms.date: 12/21/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="set-up-posting-groups"></a>Impostare le categorie di registrazione

I gruppi di registrazione mappano le entità ai conti di contabilità generale. Esempi di entità sono clienti, fornitori, articoli, risorse e documenti di vendita e acquisto. I gruppi di registrazione consentono di risparmiare tempo e contribuiscono a evitare errori quando si registrano transazioni. I valori di transazione verranno registrati nei conti specificati nella categoria di registrazione per tale particolare entità. L'unico requisito consiste nella presenza di un piano dei conti. Per ulteriori informazioni, vedere [Impostare il piano dei conti](finance-setup-chart-accounts.md).  

Le categorie di registrazione possono essere di tre tipi:  

* Generale

  Specifica a quali clienti vendi o da quali fornitori compri e gli articoli/servizi venduti o acquistati. È inoltre possibile combinare le categorie per specificare le operazioni come i conti economici in cui effettuare la registrazione oppure utilizzare le categorie per filtrare i report.  
* Specifico

  Consente, ad esempio, di utilizzare i documenti di vendita anziché effettuare la registrazione direttamente nella contabilità generale. Quando vengono creati movimenti contabili nel registro clienti , le categorie di registrazione garantiscono che nella contabilità generale vengano creati i movimenti corrispondenti.  
* Imposta

  Consente di definire le aliquote dell'imposta e i tipi di calcolo da applicare a clienti o fornitori e agli articoli venduti o acquistati.

Nelle sezioni che seguono sono indicate le categorie di registrazione che rientrano in ciascun tipo.  

## <a name="general-posting-groups"></a>Categorie di registrazione generali

La tabella che segue descrive le categorie di registrazione generali.

| Tipo | Descrizione |
| --- | --- |
| Categorie di registrazione business |Assegnare il gruppo a clienti e fornitori per specificare a chi si vende e da chi si acquista. Imposta questi gruppi di registrazione nella pagina **Cat. reg. business**. Durante l'impostazione, pensa a quante categorie sono necessarie per suddividere vendite e acquisti. Ad esempio, le categorie di clienti e fornitori per aree geografiche o per tipo di attività. |
| Categorie di registrazione articoli/servizi |Assegnare questa categoria ad articoli e risorse per specificare gli articoli venduti o acquistati. Imposta questi gruppi di registrazione nella pagina **Cat. reg. articoli/servizi**. Durante l'impostazione, pensa al numero di categorie necessario per ripartire le vendite per prodotto (articoli e risorse) e gli acquisti per articolo. Ad esempio, suddivide queste categorie per materie prime, vendita al dettaglio, risorse, capacità e così via. |
| Setup Registrazioni Generali |Combinare le categorie di registrazione business e le categorie di registrazione articoli/servizi e scegliere i conti per effettuare la registrazione. A ogni combinazione di categorie di registrazione business e articoli/servizi, è possibile assegnare un insieme di conti C/G. È possibile, ad esempio, registrare la vendita dello stesso articolo in conti di contabilità generale diversi se ai clienti sono assegnate categorie di registrazione business diverse. Imposta queste configurazioni nella pagina **Setup registrazioni COGE**. |

## <a name="specific-posting-groups"></a>Categorie di registrazione specifiche

La tabella seguente descrive le categorie di registrazione che sono specifiche per i tipi di dati.

|Tipo | Descrizione |
| --- | --- |
| Cat. reg. clienti |Definire i conti da utilizzare quando si registrano transazioni clienti. Se usi il magazzino insieme alla contabilità clienti, i conti in cui vengono registrate le righe ordine cliente vengono determinati dalla categoria di registrazione business assegnata al cliente e categoria di registrazione articoli/servizi assegnata all'articolo di magazzino. Vedere *Categorie di registrazione aziendali generali* e *Categorie di registrazione prodotti generali* nella sezione [Categorie di registrazione generali](#general-posting-groups). Imposta queste categorie registrazioni nella pagina **Cat. reg. clienti**. |
| Cat. reg. fornitori |Definire dove registrare le transazioni relative a conti fornitori, conti di addebito assistenza e conti sconto pagamento. Questo è simile alle categorie di registrazione clienti. Imposta queste categorie registrazioni nella pagina **Cat. reg. fornitori**. |
| Cat. reg. magazzino |Definire le categorie di registrazione magazzino che si assegnano ai conti articoli pertinenti nella pagina **Setup registrazione magazzino**. Le registrazioni di movimenti relativi a un articolo vengono quindi effettuate nel conto C/G impostato per la combinazione di categoria di registrazione magazzino e ubicazione che è collegata all'articolo. Le categorie di registrazione magazzino rappresentano inoltre un buon metodo per organizzare il magazzino. Quando si generano report, è possibile separare gli articoli in base alle relative categorie di registrazione. Imposta queste categorie registrazioni nella pagina **Cat. reg. magazzino**. |
| Cat. reg. C/C bancari |Definire i conti di contabilità generale su cui sono postati i conti correnti registrati. Ad esempio, è possibile semplificare i processi di tracciamento delle transazioni e di riconciliazione dei conti correnti bancari. Imposta queste categorie registrazioni nella pagina **Cat. reg. C/C bancari**. Si consiglia di impostare il campo **Registrazione diretta** di questi conti C/G su *No*. |
| Categorie di registrazione cespiti |È possibile definire diversi tipi di spese e costi, come conti per costi di acquisto, importi di fondo ammortamento, costi di acquisto di cessione, fondo ammortamento di cessione, guadagni su cessione, perdite su cessione, spese di manutenzione e spese di ammortamento. Imposta queste categorie registrazioni nella pagina **Cat. reg. cespiti**. |

### <a name="allow-substitute-customer-or-vendor-posting-groups-on-documents"></a>Consentire categorie registrazione di clienti o fornitori sostitutivi nei documenti

Puoi consentire alle persone di scegliere altre categorie di registrazione business cliente e fornitore diverse rispetto a quelle predefinite quando usi documenti e giornali di registrazione di vendita o acquisto.

Per consentire le modifiche alle categorie di registrazione clienti, scegli **Consenti più categorie di registrazione** nelle pagine **Setup contabilità clienti** e **Setup gest. assist.** e nella pagina **Setup contabilità fornitori** per le modifiche alla categoria di registrazione fornitori.

Nelle pagine **Cat. reg. clienti** o **Cat. reg. fornitori** puoi specificare le categorie di registrazione da consentire come sostituti scegliendo **Sostituzioni**. Le categorie di registrazione sostitutive possono sostituire le categorie di registrazione clienti o fornitori predefinite specificate per un cliente o un fornitore.

Dopo aver configurato questa impostazione, è possibile scegliere tra le categorie di registrazione sostitutive consentite e modificare la categoria di registrazione cliente o fornitore durante la registrazione di documenti e giornali di registrazione di vendita o acquisto. Le categorie di registrazione clienti o fornitori sostitutive vengono copiate nei documenti e nei giornali di registrazione registrati e i movimenti C/G passivi o attivi vengono registrati nei conti C/G specificati per i sostituti.

Quando si applica, ad esempio, una fattura e un pagamento registrati con diverse categorie di registrazione clienti o fornitori (diversi conti C/G), [!INCLUDE[prod_short](includes/prod_short.md)] trasferisce gli importi tra i conti C/G per bilanciarli.

## <a name="tax-posting-groups"></a>Categorie di registrazione IVA

La tabella che segue descrive le categorie di registrazione relativi alle imposte.

| Tipo | Descrizione |
| --- | --- |
| Categorie reg. business IVA |Stabilire come calcolare e registrare l'IVA per clienti e fornitori. Imposta questi gruppi di registrazione nella pagina **Cat. reg. business IVA**. Durante l'impostazione, pensare a quante categorie saranno necessarie. Ad esempio, questo può dipendere da diversi fattori, quali la legislazione locale e il fatto che l'azienda svolga un'attività commerciale sia a livello nazionale che internazionale. |
| Cat. reg. articoli/servizi IVA |Specificare i calcoli IVA necessari per i tipi di articoli o risorse acquistati o venduti. |
| Setup registrazioni IVA |Combinare le categorie di registrazione business IVA e di categorie di registrazione articoli/servizi IVA. Quando si compila una riga di registrazioni COGE, di acquisto o di vendita, si esamina la combinazione per identificare i conti da utilizzare. |

Se il tuo paese/area geografica utilizza l'imposta sul valore aggiunto (IVA), vedi [Impostare calcoli e metodi di registrazione per l'imposta sul valore aggiunto](finance-setup-vat.md).  

## <a name="example-of-linking-posting-groups"></a>Esempio di collegamento di categorie di registrazione

Ecco uno scenario.  

Le categorie di registrazione vengono selezionati in una scheda cliente:  

* Categoria di registrazione business
* Cat. reg. cliente  

Le categorie di registrazione vengono selezionate in una scheda articolo:  

* Categorie di registrazione articoli/servizi:  
* Cat. reg. magazzino  

Quando viene creato un documento di vendita, le informazioni della scheda cliente vengono utilizzate nella testata di vendita e quelle della scheda articolo nelle righe di vendita.  

* La registrazione dei ricavi (conto economico) è determinata dalla combinazione di categoria di registrazione business e categoria di registrazione articoli/servizi.  
* La registrazione dei crediti v/clienti (conto patrimoniale) è determinata dalla categoria di registrazione cliente.  
* La registrazione di magazzino (conto patrimoniale) è determinata dalla categoria di registrazione magazzino.  
* La registrazione del costo delle merci vendute (COGS, Cost of Goods Sold) è determinata dalla combinazione di categoria di registrazione business e categoria di registrazione articoli/servizi.  

Il setup determina quando avviene la registrazione. Ad esempio, la sincronizzazione è influenzata da quando si eseguono le attività periodiche, come la registrazione dei costi di magazzino o la rettifica dei movimenti di costo articoli.

## <a name="copy-posting-setup-lines"></a>Copiare righe di setup registrazione

Maggiore è il numero di categorie di registrazione articoli/servizi e business, maggiore sarà la quantità di righe nella pagina **Setup registrazioni COGE**. Sebbene possano esserci numerose combinazioni diverse di categorie di registrazione business e articoli/servizi, le diverse combinazioni possono comportare la registrazione negli stessi conti C/G. Per limitare la quantità di dati da immettere manualmente, copiare i conti C/G da una riga esistente nella pagina **Setup registrazioni COGE**.

## <a name="set-up-posting-groups-on-the-go"></a>Impostare le categorie di registrazione ovunque ci si trovi

Per consentire agli utenti di iniziare più rapidamente, [!INCLUDE[prod_short](includes/prod_short.md)] offre assistenza tramite le notifiche di conti COGE mancanti in varie impostazioni di gruppi di registrazione. Per ricevere queste notifiche, assicurati che la notifica **Il conto C/G non è presente nel setup o nella categoria di registrazione** sia selezionata nella pagina **Notifiche personali** a cui puoi accedere dal campo **Modifica il momento in cui ricevere le notifiche** nella pagina **Impostazioni personali**.  

In questo modo, quando lavori su un documento che utilizza un gruppo di registrazione o una configurazione in cui manca un conto di contabilità generale richiesto, riceverai una notifica. Scegli il collegamento nella notifica per aprire una pagina in cui è possibile apportare le modifiche pertinenti, a condizione che si disponga dell'autorizzazione per farlo.  

> [!NOTE]
> Per portarti direttamente al gruppo di registrazione o all'impostazione a cui manca un conto di contabilità generale, [!INCLUDE[prod_short](includes/prod_short.md)] creerà un gruppo di registrazione segnaposto o un'impostazione. I gruppi e le impostazioni di registrazione sono un modo per il contabile di controllare il modo in cui i movimenti vengono registrati nella contabilità generale, quindi la creazione just-in-time di gruppi e impostazioni di registrazione potrebbe non essere consentita nella tua organizzazione.  
>
> In tal caso, disabilita la notifica *Il conto C/G non è presente nel setup o nella categoria di registrazione*, quindi collabora con il contabbile per apportare le modifiche pertinenti al gruppo di registrazione, all'impostazione o al documento. Questo è un passaggio importante, perché una volta che i documenti sono stati registrati, eventuali gruppi di registrazione o impostazioni utilizzati in modo errato non possono essere eliminati perché sono stati creati movimenti contabili generali.

A partire dal primo ciclo di rilascio del 2022, puoi utilizzare il campo **Bloccato** della pagina **Setup registrazioni COGE** per impedire agli utenti di utilizzare erroneamente un'impostazione che non è più rilevante per le nuove registrazioni.  

## <a name="troubleshooting-posting-group-errors"></a>Risoluzione degli errori del gruppo di posting

I gruppi di pubblicazione sono uno dei concetti più avanzati da impostare in [!INCLUDE[prod_short](includes/prod_short.md)]. Se non sono impostati correttamente, possono verificarsi errori quando si inseriscono documenti o linee del giornale. Per esempio, questi errori sono tipicamente causati da un errore nel modo in cui i conti della contabilità generale sono assegnati, o come i gruppi di registrazione sono combinati.

Quando qualcosa non va, [!INCLUDE[prod_short](includes/prod_short.md)] visualizza la pagina dei **messaggi di errore** . La pagina dei **messaggi di errore** può rendere più facile identificare e risolvere il problema. La pagina offre una descrizione dell'errore che indica la configurazione del gruppo di posting che ha bisogno di attenzione. Per esempio, il messaggio potrebbe essere "Sales Prepayment account is missing a General Posting Setup" C'è anche un link per aprire la pagina che è la fonte del problema, in modo da poterlo risolvere rapidamente.  

> [!NOTE]
> La gestione degli errori descritta sopra non è disponibile su diari di articoli, risorse, impiegati e attività fisse, o per conti G/L aggiunti in versioni locali di gruppi di registrazione.

## <a name="see-also"></a>Vedere anche

[Contabilità generale e piano dei conti](finance-general-ledger.md)  
[Impostazione di dati finanziari](finance-setup-finance.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
