---
title: Aggiornare i tassi di cambio delle valute (video)
description: Se tieni traccia degli importi in valute differenti puoi utilizzare Business Central per rettificare i tassi di cambio delle valute dei movimenti registrati con un servizio esterno.
author: edupont04
ms.topic: conceptual
ms.search.keywords: 'multiple currencies, adjust exchange rates, FX rates'
ms.search.form: '5, 118'
ms.date: 03/15/2022
ms.author: edupont
---
# Aggiornare i tassi di cambio valuta

Puoi definire diverse valute in [!INCLUDE [prod_short](includes/prod_short.md)], ad esempio se commerci in valute diverse dalla tua valuta locale. Quindi, per aiutarti a tenere traccia delle variazioni dei tassi di cambio valuta, puoi gestire le valute manualmente oppure puoi impostare un servizio di cambio valuta.

## Valute

> [!TIP]  
> In [!INCLUDE[prod_short](includes/prod_short.md)] se si stanno cercando informazioni in tempo reale sui tassi di cambio delle valute estere (FX) o sui tassi di cambio storici, queste informazioni vanno sotto il nome di valuta. Oltre a questo articolo, vedere anche [Impostare una valuta di rendicontazione aggiuntiva](finance-how-setup-additional-currencies.md).

[!INCLUDE [finance-currencies-def](includes/finance-currencies-def.md)]

Specifica i codici valuta nell'elenco **Valute**, comprese le informazioni e le impostazioni aggiuntive necessarie per ciascun codice valuta. Per ulteriori informazioni, vedi [Valute](finance-set-up-currencies.md#curr)

### Esempio di una transazione in valuta esigibile

[!INCLUDE [finance-currencies-example](includes/finance-currencies-example.md)]

## Tassi di cambio

I tassi di cambio sono lo strumento per calcolare il valore in valuta locale (LCY) di ogni transazione in valuta. La pagina **Tassi di cambio** include i seguenti campi:

|Campo|Descrizione|  
|---------------------------------|---------------------------------------|  
|**Data Inizio**|La data in cui il tasso di valuta è stato effettuato|  
|**Codice valuta**|Il codice valuta relativo a questo tasso di cambio|  
|**Cod. Valuta Relativa**|Se questa valuta fa parte di un calcolo di valuta triangolare, il relativo codice valuta può essere impostato qui|  
|**Importo Tasso di Cambio**|L'importo del tasso di cambio è il tasso da utilizzare per il codice valuta selezionato nella riga. Normalmente 1 o 100|  
|**Importo Tasso di Cambio Relativo**|L'importo del tasso di cambio relazionale è il tasso da utilizzare per il codice valuta relativa|  
|**Rett. Importo Tasso di Cambio**|L'importo del tasso di cambio di rettifica è il tasso da utilizzare per il codice valuta selezionato nella riga per l'utilizzo del processo batch **Regola tassi di cambio**|  
|**Importo Rett. Tasso Cambio Rel.**|L'importo del tasso di cambio di rettifica relazionale è il tasso da utilizzare per il codice valuta selezionato nella riga per l'utilizzo del processo batch **Regola tassi di cambio**|  
|**Fissa importo tasso di cambio**|Specifica se il tasso di cambio della valuta può essere modificato su fatture e righe di registrazione.|  

In generale, i valori dei campi **Importo del tasso di cambio** e **Importo del tasso di cambio relazionale** vengono utilizzati come tasso di cambio predefinito su tutti i nuovi documenti crediti e debiti creati in futuro. Al documento viene assegnato il tasso di cambio in base alla data di lavoro corrente.  

> [!Note]
> Il tasso di cambio effettivo verrà calcolato utilizzando questa formula:
>
> `Currency Amount = Amount / Exchange Rate Amount * Relational Exch. Rate Amount`

L'importo del tasso di cambio di rettifica o l'importo del tasso di cambio di rettifica relazionale verrà utilizzato per aggiornare tutte le transazioni bancarie, attive o passive aperte.  

> [!Note]
> Il tasso di cambio effettivo verrà calcolato utilizzando questa formula:
>
> `Currency Amount = Amount / Adjustment Exch. Rate Amount * Relational Adjmt Exch. Rate Amt`

## Rettifica di tassi di cambio

Poiché i tassi di cambio oscillano costantemente, gli equivalenti in valuta addizionale nel sistema devono essere rettificati periodicamente. Se queste rettifiche non vengono apportate, gli importi che sono stati convertiti da valute estere (o addizionali) e registrati nella contabilità generale in valuta locale possono essere fuorvianti. Inoltre, i movimenti quotidiani registrati prima dell'immissione di un tasso di cambio quotidiano nell'applicazione devono essere aggiornati dopo l'immissione delle informazioni su tale tasso di cambio.

Il processo batch **Rettifica tassi di cambio** viene utilizzato manualmente per rettificare i tassi di cambio dei movimenti cliente, fornitore e conti C/C bancari registrati. Consente inoltre di aggiornare gli importi nella valuta contabile addizionale nei movimenti C/G.  

> [!TIP]
> È possibile utilizzare un servizio per aggiornare automaticamente i tassi di cambio nel sistema. Per ulteriori informazioni, vedere [Per impostare un servizio dei tassi di cambio delle valute](finance-how-update-currencies.md#to-set-up-a-currency-exchange-rate-service). Tuttavia, ciò non modifica i tassi di cambio sulle transazioni già registrate. Per aggiornare i tassi di cambio sui movimenti registrati, utilizzare il processo batch **Modifica i tassi di cambio**.

Puoi visualizzare in anteprima l'effetto che una modifica avrà sulla pubblicazione prima di pubblicarla effettivamente selezionando **Anteprima** nella pagina **Rettifica tassi di cambio**. Inoltre, puoi selezionare se la registrazione della contabilità generale sarà dettagliata (per voce) o riepilogativa (per valuta) scegliendo **Raggruppa articoli**. Puoi inoltre specificare come gestire le dimensioni per registrazioni di utili e perdite non realizzati scegliendo una delle seguenti opzioni nel campo **Trasferire i valori dimensioni**:  

- **Movimento origine**: voci C/G per utili e perdite non realizzati avranno i valori delle dimensioni trasferiti dalla voce rettificata.
- **Per conto C/G**: le voci C/G per utili e perdite non realizzati avranno i valori delle dimensioni trasferiti dalla voce di origine delle impostazioni delle dimensioni del conto C/G non realizzati.
- **Nessun trasferimento**: i movimenti C/G per utili e perdite non realizzati non avranno valori dimensionali.

### Effetto su clienti e fornitori

Per i conti di clienti e fornitori, la valuta viene rettificata in base al tasso di cambio valido alla data di registrazione specificata nel processo batch. Durante il processo batch vengono calcolate le differenze per singoli saldi in valuta, quindi gli importi vengono registrati nel conto C/G specificato nel campo **Conto utili non-realizzati** o nel campo **Conto Perdite Non-Realizzate** della pagina **Valuta**. I movimenti rettificativi vengono automaticamente registrati nel conto crediti/debiti della contabilità generale.

Il processo batch consente di elaborare tutti i movimenti registro clienti e i movimenti fornitori aperti. Se per un movimento vi è una differenza di tasso di cambio, il processo batch crea un nuovo registro fornitori o un nuovo registro clienti dettagliato, che riflette l'importo rettificato nel registro fornitori o clienti.

#### Dimensioni nei movimenti clienti e fornitori

Ai movimenti di rettifica vengono assegnate le dimensioni dei movimenti del registro clienti/fornitori e le rettifiche vengono registrate per combinazione di valori di dimensione.

### Effetto su conti correnti bancari

Per i conti correnti bancari, la valuta viene rettificata utilizzando il tasso di cambio valido alla data di registrazione specificata nel processo batch. Durante il processo batch vengono calcolate le differenze per ogni conto corrente bancario che ha un codice di valuta, quindi gli importi vengono registrati nel conto C/G specificato nel campo **Conto utili realizzati** o nel campo **Conto Perdite Realizzate** della pagina **Valuta**. I movimenti rettificativi vengono automaticamente registrati nei conti correnti bancari CoGe specificati nelle categorie di registrazione dei conti correnti bancari. Viene calcolato un solo movimento per valuta per categoria di registrazione.

#### Dimensioni nei movimenti di conti correnti bancari

Ai movimenti di rettifica per il conto CoGe del conto corrente bancario e per il conto profitti/perdite vengono assegnate le dimensioni di default del conto corrente bancario.

### Effetto su conti C/G
Se si effettua una registrazione in una valuta contabile addizionale, è possibile impostare il processo batch per creare nuovi movimenti di contabilità generale per rettifiche valutarie comprese tra VL e la valuta contabile addizionale. Verranno calcolate le differenze per ogni movimento C/G e inserite delle rettifiche a seconda del contenuto del campo **Rettifica tasso di cambio** di ogni conto C/G.

##### Dimensioni nei movimenti del conto C/G
Ai movimenti di rettifica vengono assegnate le dimensioni di default dei conti in cui vengono registrati.

> [!Important]
> Prima di eseguire il processo batch, è necessario immettere i tassi di cambio di rettifica necessari alla rettifica dei saldi in valuta estera. Questa operazione viene eseguita nella pagina **Tassi di cambio valuta**.<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Q24s?rel=0]

## Per impostare un servizio dei tassi di cambio delle valute
È possibile utilizzare un servizio esterno per mantenere aggiornati i tassi di cambio delle valute, ad esempio FloatRates. 

> [!NOTE]
> La maggior parte dei servizi di tasso cambio fornisce dati compatibili con il processo di importazione in [!INCLUDE[prod_short](includes/prod_short.md)]. Tuttavia, a volte i dati vengono formattati in modo diverso e sarà necessario personalizzare il processo di importazione. A tale scopo, è possibile utilizzare il framework di scambio dati la propria codeunit. Per eseguire l'operazione, sarà probabilmente necessario l'aiuto di uno sviluppatore. Per ulteriori informazioni, vedere [Impostare le definizioni di scambio di dati](across-how-to-set-up-data-exchange-definitions.md).

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Servizi di tassi di cambio valute**, quindi seleziona il collegamento correlato.
2. Scegliere l'azione **Nuovo**.
3. Nella pagina **Servizi tasso di cambio valuta** compilare i campi secondo le necessità. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Attivare il pulsante **Abilitato** per attivare per abilitare il servizio.

> [!NOTE]
> Il seguente video mostra un esempio di come connettersi a un servizio di cambio valuta, utilizzando la Banca centrale europea come esempio. Nel segmento che descrive come impostare le mappature dei campi, l'impostazione nella colonna **Sorgente** per il **Nodo padre per codice valuta** restituirà solo la prima valuta trovata. L'impostazione deve essere `/gesmes:Envelope/Code/Code/Code`.

<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4A1jy?rel=0]

## Per aggiornare i tassi di cambio delle valute mediante un servizio
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Valute**, quindi scegli il collegamento correlato.
2. Scegliere l'azione **Aggiorna tassi di cambio**.

Il valore nel campo **Tasso di cambio** della pagina **Valute** viene aggiornato con il tasso di cambio delle valute più recente.

## Vedi il relativo [training Microsoft](/training/paths/use-multiple-currencies-dynamics-365-business-central/)

## Vedi anche

[Valute in Business Central](finance-currencies.md)  
[Impostare le valute](finance-set-up-currencies.md)  
[Impostare una valuta contabile addizionale](finance-how-setup-additional-currencies.md)  
[Chiusura di anni e periodi](year-close-years-periods.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
