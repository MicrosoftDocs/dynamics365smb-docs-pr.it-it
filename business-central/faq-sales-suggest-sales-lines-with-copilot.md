---
title: Domande frequenti sui suggerimenti per le righe di vendita con Copilot
description: Queste domande frequenti forniscono informazioni sulla tecnologia di IA utilizzata in Business Central.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: article
ms.search.form: null
ms.date: 02/02/2024
ms.service: dynamics-365-business-central
ms.collection: bap-ai-copilot
ms.custom: responsible-ai-faqs
---

# <a name="faq-for-sales-line-suggestions-with-copilot-preview"></a>Domande frequenti sui suggerimenti per le righe di vendita con Copilot (anteprima)

[!INCLUDE[preview-banner](includes/preview-banner.md)]

Queste domande frequenti descrivono l'impatto sull''intelligenza artificiale della funzionalità dei suggerimenti per le righe di vendita in [!INCLUDE [prod_short](includes/prod_short.md)].

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

## <a name="what-is-sales-line-suggestions-with-copilot"></a>Che cos'è la funzionalità dei suggerimenti per le righe di vendita con Copilot?

I suggerimenti per righe di vendita con Copilot possono aiutare a creare righe in documenti di vendita come offerte di vendita, ordini e fatture basate su input strutturati o linguaggio naturale. La funzionalità non è una chat generica, ma un'esperienza altamente specifica e integrata che puoi utilizzare nei documenti di vendita. La funzionalità offre due capacità distinte che ti aiutano a trovare dati su singoli prodotti o interi documenti.

## <a name="what-are-capabilities-of-sales-line-suggestions-with-copilot"></a>Quali sono le funzionalità dei suggerimenti per le righe di vendita con Copilot?

* Trovare prodotti

  Le informazioni che descrivono i prodotti sono archiviate in più aree in [!INCLUDE [prod_short](includes/prod_short.md)]. Ad esempio, i numeri e le descrizioni degli articoli sono memorizzati nella tabella **Articolo**, più codici a barre sono memorizzati nella tabella **Riferimento articolo** e le proprietà del prodotto sono archiviate nella tabella **Attributi articolo**. Sebbene sia possibile immettere *Bicicletta rossa*, il prodotto effettivo potrebbe essere *Tourer cremisi*, dove *Bicicletta* è una categoria di prodotto e *rosso* è un attributo.

* Trovare un documento per riferimento

  Gli utenti spesso ripetono un ordine precedente o almeno lo usano come punto di partenza. Ma potrebbe essere complicato trovare l'ordine appropriato in una pila di ordini. Potresti ricordare parte dell'ID dell'ordine, che può essere un numero assegnato dalla società o un numero di riferimento ricevuto da un cliente. La possibilità di utilizzare prompt come *Ho bisogno dell'ultima fattura di aprile* dovrebbe aiutarti a trovare un ordine più velocemente.

## <a name="what-is-the-intended-use-of-sales-line-suggestions-with-copilot"></a>Qual è l'uso previsto dei suggerimenti per le righe di vendita con Copilot?

* Trovare prodotti

  Destinato a rispondere ai prompt degli utenti per trovare prodotti sulla base di descrizioni vaghe, incomplete o imprecise.

  Poiché il numero medio di articoli (prodotti/servizi) per i clienti [!INCLUDE [prod_short](includes/prod_short.md)] è 10.000, trovare quelli giusti potrebbe essere difficile senza esperienza o conoscenze precedenti. Il modo in cui i dati vengono archiviati in [!INCLUDE [prod_short](includes/prod_short.md)] non semplifica le cose, perché è necessario eseguire più ricerche o esercizi di filtro nelle diverse pagine che archiviano i dati del prodotto.

  Copilot estrae i prodotti e le quantità richiesti e identifica il termine e gli attributi di ricerca principali, in modo da poter inserire il prompt più rapidamente. Quindi, Copilot esegue una ricerca avanzata attraverso più tabelle correlate, applica sinonimi, corregge errori di battitura e valuta la qualità dell'output della ricerca.

* Trovare un documento per riferimento

  Destinato a rispondere alle domande degli utenti per trovare documenti di vendita esistenti per un cliente specifico utilizzando informazioni parziali o approssimative.

  Negli ambienti B2B, le persone spesso hanno a che fare con richieste ricorrenti e gli elaboratori degli ordini possono ricevere richieste per ripetere un documento precedente o almeno utilizzarlo come punto di partenza. Ma potrebbe essere difficile trovarne uno per diversi motivi:

  - Nel corso del relativo ciclo di vita, un documento di vendita può evolversi da offerta a ordine fino a fattura registrata o spedizione. I documenti possono anche essere archiviati.
  - Potresti avere un identificatore esatto, ma non puoi dire cosa rappresenta. Ad esempio, è il numero dell'ordine, il numero di fattura o un riferimento esterno?
  - A volte hai una data o un punto, ma non un ID per il documento.

  Per trovare manualmente un documento di origine, dovrai aprire più pagine e utilizzare la ricerca e il filtro più volte. Tuttavia, Copilot può semplificarlo in un'unica query in linguaggio naturale che ti consente di esprimere ciò che stai cercando a modo tuo. 

  * *Ottieni prodotti dall'ordine 103031*
  * *Ho bisogno dei prodotti dell'ultima fattura di agosto*

## <a name="how-was-sales-line-suggestions-with-copilot-evaluated-what-metrics-are-used-to-measure-performance"></a>Come sono stati valutati i suggerimenti per le righe di vendita con Copilot? Quali metriche vengono utilizzate per misurare le prestazioni?

La funzionalità è stata sottoposta a test approfonditi con numerosi prompt in inglese americano che rappresentano sia l'uso tipico che l'uso da parte di soggetti malintenzionati. I test erano basati sui dati dimostrativi di [!INCLUDE [prod_short](includes/prod_short.md)] e su un ampio catalogo di prodotti etichettati disponibile come open source.

Questa funzionalità è stata creata in conformità con lo standard di intelligenza artificiale responsabile di Microsoft. [Scopri di più sull'intelligenza artificiale responsabile di Microsoft](https://aka.ms/RAI).

## <a name="what-are-the-limitations-of-sales-line-suggestions-with-copilot-how-can-users-minimize-the-impact-of-the-sales-line-suggestions-with-copilot-limitations-when-using-the-system"></a>Quali sono le limitazioni suggerimenti per le righe di vendita con Copilot? In che modo gli utenti possono ridurre al minimo l'impatto delle limitazioni relative ai suggerimenti per le righe di vendita con Copilot durante l'utilizzo del sistema?

* Trovare prodotti
  
  Trova prodotti funziona meglio in lingua inglese. Anche se puoi utilizzare questa funzionalità in qualsiasi lingua che [!INCLUDE [prod_short](includes/prod_short.md)] supporta, le ricerche di articoli in altre lingue potrebbero essere meno accurate.

Se il tuo settore o dominio si sovrappone a quelli che Microsoft considera argomenti sensibili (come droga, violenza, intrattenimento per adulti e così via), Copilot potrebbe rimandare a risposte neutre e curate o fornire risposte imprecise.

I suggerimenti per le righe di vendita popolano solo i campi **Tipo** come **Articolo**, **Nr.** e **Quantità** come descritto. Altri campi, incluso **Unità di misura**, **Prezzo unitario** e **Ubicazione** utilizzano la logica corrente e vengono popolati in base alle impostazioni dell'articolo o ai valori ereditati dall'intestazione del documento.

Il **Codice variante** non è attualmente supportato. Se puoi spedire un prodotto in due colori diversi, ad esempio, Copilot troverà il prodotto necessario ma lascerà il campo **Codice variante** vuoto. Dovrai compilare manualmente il campo.

Il modo in cui assegni un nome ai tuoi prodotti può influenzare l'output. Ad esempio, l'utilizzo di abbreviazioni criptiche anziché di nomi descrittivi può ridurre la qualità dell'output.

Per i prodotti, la tabella seguente elenca le tabelle e i campi che Copilot cerca.

|Tavolo  |Campi  |
|---------|---------|
|**Articoli**     |  * Nr.<br>* Descrizione<br>* Descrizione 2<br>* Descrizione ricerca<br>* GTIN<br>* Numero articolo fornitore       |
|**Variante articolo**     | * Codice<br>* Descrizione<br>* Descrizione 2          |
|**Riferimento articolo**     | * Nr. riferimento<br>* Descrizione<br>* Descrizione 2        |
|**Attributi articolo**     | * Nome<br>* Valore        |
|**Categoria articoli**     |  * Codice<br>* Descrizione<br>* Categoria padre - Livello 1           |
|**Traduzioni articolo**     | * Lingua<br>* Descrizione<br>* Descrizione 2          |
|**Identificativo articolo**     |  * Codice       |
|**Riga testo esteso**     |  * Testo      |

* Trovare documenti per riferimento

  Attualmente è possibile avviare i suggerimenti per le righe di vendita da ordini cliente, fatture e offerte ed eseguire ricerche nei seguenti documenti:

  * Ordini di vendita
  * Offerte di vendita
  * Fatture di vendita
  * Fatture di vendita registrate
  * Spedizioni di vendita registrate

  Copilot effettua la ricerca nei seguenti campi

  * Nr. documento
  * Nr. documento esterno
  * Riferimento personale
  * Nr. offerta
  * Data documento
  * Nr. cliente di vendita

  Copilot non restituisce tutte le righe di tipo Articolo. Vengono trasferiti solo i numeri degli articoli, i codici variante e le quantità. Le quantità del documento di origine vengono convertite nell'**Unità di misura vendita**.

## <a name="in-which-geographies-and-languages-is-sales-lines-suggestions-available"></a>In quali aree geografiche e lingue sono disponibili i suggerimenti per le righe di vendita?

Ad eccezione del Canada, questa funzionalità è disponibile per la localizzazione di tutti i paesi/aree geografiche dell'ambiente e in tutte le lingue supportate. A causa del supporto linguistico limitato, la funzionalità non sarà inizialmente disponibile per i clienti canadesi a causa della conformità linguistica normativa. Affinché questa funzionalità sia disponibile per gli ambienti dei clienti situati in paesi/aree geografiche in cui il servizio OpenAI di Azure non è distribuito, gli amministratori devono prima consentire lo spostamento dei dati oltre i confini per permettere la connessione di [!INCLUDE [prod_short](includes/prod_short.md)] al servizio OpenAI di Azure.  

## <a name="what-operational-factors-and-settings-allow-for-effective-and-responsible-use-of-the-feature"></a>Quali fattori operativi e impostazioni consentono un uso efficace e responsabile della funzionalità?

È possibile che a volte i suggerimenti basati sull'intelligenza artificiale siano errati o incompleti. Devi sempre verificare l'accuratezza dei suggerimenti di Copilot prima di scegliere se mantenerli. I suggerimenti di Copilot non vengono salvati nel database di [!INCLUDE [prod_short](includes/prod_short.md)] fino a che non scegli il pulsante **Mantieni** ed esci dalla finestra Copilot. Puoi modificare e correggere eventuali suggerimenti prima di scegliere di mantenerli o dopo averli inseriti in un documento di vendita.

### <a name="what-is-expected-of-administrators-and-end-users-when-using-sales-lines-suggestions"></a>Cosa ci si aspetta dagli amministratori e dagli utenti finali quando si utilizzano i suggerimenti per le righe di vendita?

Ogni singolo utente sceglie se utilizzare o meno **Suggerimenti per le righe di vendita**. Anche quando la funzionalità è abilitata dagli amministratori e disponibile, puoi scegliere di utilizzarla sempre, a volte o mai.  

Gli amministratori decidono se utilizzare le funzionalità di Copilot in [!INCLUDE [prod_short](includes/prod_short.md)]. Se gli amministratori abilitano Copilot, devono assicurarsi di concedere l'accesso agli utenti appropriati.   

> [NOTE!]
> - Non supportiamo questa funzionalità in [!INCLUDE [prod_short](includes/prod_short.md)] locale o in un cloud privato.
> - I partner non possono estendere questa funzionalità. Ciò significa che gli sviluppatori partner non possono modificarla, sostituirla o estenderla.

## <a name="is-copilot-the-only-means-to-create-sales-lines"></a>Copilot è l'unico mezzo per creare righe di vendita?

No. L'uso di Copilot è facoltativo. [!INCLUDE [prod_short](includes/prod_short.md)] offre modalità non basate sull'intelligenza artificiale per inserire righe di vendita o copiare documenti. Le organizzazioni possono utilizzare entrambi gli approcci contemporaneamente.  

## <a name="how-do-i-give-feedback-about-ai-generated-content"></a>Come posso fornire feedback sui contenuti generati dall'intelligenza artificiale?

Ogni volta che Copilot fornisce suggerimenti, puoi fornire feedback a Microsoft direttamente dalla finestra di Copilot, utilizzando i pulsanti Mi piace e Non mi piace. Il tuo feedback rimane anonimo e usiamo questi dati per migliorare la qualità del servizio.  

## <a name="see-also"></a>Vedere anche

[Suggerire righe in ordini vendita con Copilot](sales-suggest-sales-lines-with-copilot.md)  
[Configurare le funzionalità di Copilot e IA](enable-ai.md)  
[Domande frequenti sull'intelligenza artificiale responsabile per Dynamics 365 Business Central](responsible-ai-overview.md)  
