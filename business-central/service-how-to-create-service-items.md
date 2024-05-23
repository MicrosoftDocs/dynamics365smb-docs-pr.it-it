---
title: Come creare articoli in assistenza
description: 'Leggi i diversi modi in cui puoi creare articoli in assistenza in Business Central, ad esempio all''interno di un ordine di assistenza o durante la spedizione di articoli.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: null
ms.date: 03/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="create-service-items"></a>Crea articoli in assistenza

In [!INCLUDE[prod_short](includes/prod_short.md)], il termine "articolo in assistenza" si riferisce alle attrezzature o agli articoli che necessitano di assistenza. Quando si crea un ordine di assistenza, si specificano gli articoli che necessitano di assistenza. Nell'ordine, è possibile collegare un articolo in assistenza a un articolo in magazzino o a un gruppo di articoli in assistenza.

Quando si riceve un articolo che necessita di assistenza, è possibile registrarlo come articolo in assistenza. Questa operazione può essere effettuata in vari modi. Ad esempio, è possibile creare un articolo in assistenza nella pagina **Articoli in assistenza**, o nell'ambito di un altro processo, ad esempio quando si lavora con un ordine di assistenza.

## <a name="to-create-a-service-item"></a>Per creare un articolo in assistenza

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Articoli in assistenza**, quindi scegli il collegamento correlato.
2. Compilare i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-create-service-items-within-a-service-order"></a>Per creare articoli in assistenza all'interno di un ordine di assistenza

Quando si ricevono articoli su cui prestare assistenza e li si intende registrare come articoli in assistenza, è possibile crearli come articoli in assistenza nelle pagine **Ordine Assistenza** o **Offerte Assistenza**.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ordini assistenza**, quindi scegli il collegamento correlato.  
2. Compilare i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Scegliere l'azione **Crea articolo in assistenza**.  

    Viene assegnato un numero all'articolo in assistenza e viene creata una scheda articolo in assistenza. Il campo **Nr. articolo in assistenza** viene compilato con il numero del nuovo articolo in assistenza.

## <a name="to-create-a-service-item-when-shipping-items"></a>Per creare un articolo in assistenza durante la spedizione degli articoli

Quando si spediscono articoli registrando ordini o fatture di vendita, gli articoli spediti vengono automaticamente registrati come articoli in assistenza se è rispettata la seguente condizione. Gli articoli devono appartenere a un gruppo di articoli in assistenza per cui la casella di controllo **Crea articolo in assistenza** risulta selezionata. Se i numeri seriali degli articoli sono registrati nella pagina Righe tracciabilità articolo, tali informazioni verranno automaticamente copiate nel campo **Nr. seriale** della scheda relativa all'articolo in assistenza al momento della creazione degli articoli stessi.  

La seguente procedura indica le modalità di creazione di articoli in assistenza durante la spedizione degli articoli presenti negli ordini di vendita.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ordini vendita**, quindi seleziona il collegamento correlato.  
2. Aprire l'ordine di vendita appropriato.  
3. Scegliere l'azione **Registra** o **Registra e stampa**.  
4. Scegliere l'azione **Spedizione** o **Spedizione e fattura**.  
5. Verranno automaticamente creati gli articoli in assistenza per gli articoli dell'ordine che appartengono a un gruppo di articoli in assistenza impostato per la creazione di articoli in assistenza. A tali articoli verranno inoltre assegnati i corrispondenti numeri seriali eventualmente registrati nella pagina **Righe tracciabilità articolo**.  

> [!NOTE]  
> Se un articolo è una distinta base e la distinta base è stata espansa, gli articoli in essa contenuti verranno trattati come normali articoli. Vengono creati articoli in assistenza in base alla condizione specificata per il gruppo degli articoli in assistenza ed eventualmente alla condizione specificata per i numeri seriali. Inoltre, se viene creato un articolo in assistenza per una distinta base espansa composta da altri componenti DB, tali articoli verranno creati come componenti articolo in assistenza per l'articolo in assistenza della distinta base espansa.  
>
> Se un articolo è una distinta base e la distinta base non è stata espansa, verrà creato un articolo in assistenza in base alla condizione specificata per il gruppo di articoli in assistenza ed eventualmente alla condizione specificata per i numeri seriali.  

## <a name="to-insert-a-starting-fee-for-a-service-item"></a>Per inserire una spesa iniziale per un articolo in assistenza

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Task assistenza**, quindi scegli il collegamento correlato.
2. Scegliere l'azione **Prospetto interv. articolo**.
3. Scegliere la riga di assistenza e quindi **Azioni**, **Funzioni**, quindi l'azione **Inserisci spesa iniziale**.  

    Verrà inserita una riga di assistenza di tipo **Costo** in cui viene indicata la spesa iniziale. La spesa iniziale viene applicata all'articolo in assistenza selezionato.

## <a name="block-items-item-variants-or-specific-service-items"></a>Bloccare articoli, varianti articoli o articoli in assistenza specifici

È possibile impedire l'utilizzo di articoli, varianti articoli o articoli in assistenza nelle transazioni di gestione dei servizi, ad esempio contratti di assistenza, ordini di assistenza e fatture di assistenza. Ciò può essere utile se si desidera limitare la disponibilità di alcuni articoli o articoli in assistenza per scopi di assistenza, ad esempio a causa dell'interruzione del supporto, delle scorte limitate o degli accordi contrattuali.

Per bloccare l'utilizzo di un articolo o di una variante articolo nelle transazioni di gestione dell'assistenza, attiva l'interruttore **Servizio bloccato** nella pagina **Scheda articolo**, **Varianti articolo** e **Scheda variante articolo**. Puoi anche impostare questo campo nella pagina **Modello articolo** e verrà copiato negli articoli creati da quel modello.

Quando l'assistenza per un articolo o una variante articolo è bloccata, non è disponibile per la selezione nelle seguenti pagine:

- Riga assistenza (ad eccezione delle note di credito di assistenza, dove vedrai una notifica che l'articolo o la variante è bloccato, ma consentito in questo tipo di documento)
- Articolo in assistenza
- Riga contratto assistenza
- Riga assistenza standard

Se inserisci manualmente un numero di articolo o una variante bloccata, viene visualizzato il messaggio di errore: "Il campo contiene un valore non trovato nella tabella correlata".

Inoltre, se disponi di contratti di assistenza, offerte di contratti di assistenza o ordini di assistenza che includono articoli di servizio bloccati o varianti articoli, non puoi utilizzare le seguenti azioni:

- **Blocca** o **Crea contratto** nella pagina **Offerte contratto assistenza**.
- **Blocca contratto**, **Firma contratto**, **Crea ordini assistenza a contratto** o **Crea fatture contratto** nella pagina **Contratto di assistenza**.
- **Crea ordine** nella pagina **Offerta assistenza**.
- **Rilascia a spedizione** o **Registra** nella pagina **Ordine assistenza**.
- **Registra** nella pagina **Fattura assistenza**.

### <a name="block-a-service-item"></a>Bloccare un articolo in assistenza

Per bloccare l'utilizzo di un articolo in assistenza nelle transazioni di gestione dell'assistenza, nella pagina **Scheda articolo in assistenza**, nel campo **Bloccati** scegli una delle seguenti opzioni:

- **Contratto assistenza**: blocca l'utilizzo dell'articolo in assistenza nei contratti di assistenza e nelle offerte di contratti di assistenza, ma non negli ordini di assistenza o in altri documenti di assistenza.
- **Tutto**: blocca l'utilizzo dell'articolo in assistenza in qualsiasi transazione di gestione dell'assistenza, inclusi contratti di assistenza, ordini di assistenza e altri documenti di assistenza.

Quando un articolo in assistenza è bloccato, non puoi selezionarlo nelle seguenti pagine:

- Riga contratto assistenza (se bloccato per il contratto di assistenza o tutto)
- Riga articolo in assistenza (ad eccezione delle note di credito di assistenza, se bloccato per tutto)

Se inserisci manualmente un numero di articolo in assistenza per un articolo in assistenza bloccato, viene visualizzato il messaggio di errore: "Il campo contiene un valore non trovato nella tabella correlata".

Inoltre, se disponi di contratti di assistenza, offerte di contratti di assistenza o ordini di assistenza che includono articoli di servizio bloccati, non puoi utilizzare le seguenti azioni:

- **Blocca** e **Crea contratto** nella pagina **Offerte contratto assistenza** (se bloccato per il contratto di assistenza o tutto).
- **Blocca contratto**, **Firma contratto** o **Cambia cliente** nella pagina **Contratto assistenza** (se bloccato per il contratto di assistenza o tutto).
- **Crea ordine** in **Offerta assistenza** (se bloccato per tutti).
- **Rilascia a spedizione**, **Registra** in **Ordine assistenza** (se bloccato per tutto). Se i documenti dell'ordine di assistenza contengono più articoli in assistenza e alcuni sono bloccati e altri no, è possibile rilasciare e registrare le righe non bloccate. Valuta se attivare l'interruttore **Una riga art. in assistenza/ordine** nella pagina **Impostazione gestione assistenza**).
- **Registra** nella pagina **Fattura assistenza** (se bloccato per tutto).

È inoltre possibile visualizzare gli articoli in assistenza bloccati applicando un filtro ai seguenti report:

- Articoli in assistenza (report 5935)
- Articoli in assistenza fuori garanzia (report 5937)
- Profitto assistenza (articoli in assistenza) (report 5938)

### <a name="data-upgrade"></a>Aggiornamento dati

Questa funzionalità non richiede configurazioni aggiuntive. Tuttavia, se aggiorni [!INCLUDE [prod_short](includes/prod_short.md)], tieni presente quanto segue:

- Se disponi di articoli, varianti articoli o modelli di articolo in cui l'interruttore **Vendite bloccate** è attivato, il campo **Servizio bloccato** viene attivato anche per tali record durante l'aggiornamento. Ciò garantisce l'applicazione della logica di blocco delle vendite esistente anche alle transazioni di gestione dell'assistenza.
- Aggiornamenti dei dati solo se hai almeno un articolo in assistenza nella tua società, il che significa che stai utilizzando la funzionalità di gestione dell'assistenza e hai bisogno dell'aggiornamento dei dati. Se non disponi di articoli in assistenza, l'aggiornamento dei dati viene ignorato e l'interruttore **Servizio bloccato** è disattivata per impostazione predefinita per tutti gli articoli, le varianti articoli e modelli di articoli.

## <a name="see-also"></a>Vedere anche

[Impostare gli articoli in assistenza e i componenti degli articoli in assistenza](service-how-setup-service-items.md)  
[Impostazione della gestione assistenza](service-setup-service.md)  
[Gestione assistenza](service-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
