---
title: Aggiornare i tassi di cambio valuta
description: Tenere traccia degli importi in valute differenti utilizzando codici di valuta e utilizzare Business Central per rettificare i tassi di cambio dei movimenti registrati con un servizio esterno.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: multiple currencies, adjust exchange rates
ms.date: 06/03/2021
ms.author: edupont
ms.openlocfilehash: 0baa12a7f63e67184a00dab893c8222facfe269d
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/08/2021
ms.locfileid: "6441624"
---
# <a name="update-currency-exchange-rates"></a>Aggiornare i tassi di cambio valuta

Con l'espandersi delle attività delle società in un numero sempre maggiore di paesi/aree geografiche, diventa essenziale poter vendere e riportare dati finanziari in più di una valuta. La valuta locale (LCY) è definita nella pagina **Setup contabilità generale** come descritto nell'articolo [Impostazione delle finanze](finance-setup-finance.md). Una volta che la valuta locale (LCY) è stata definita, sarà rappresentata come una valuta vuota, quindi quando il campo **Valuta** è vuoto, significa che è LCY.  

Successivamente, è necessario impostare i codici valuta per ogni valuta che utilizzi se acquisti o vendi in valute diverse da quella locale (LCY). Anche i conti bancari possono essere creati utilizzando le valute. È possibile registrare transazioni Co.Ge. in valute diverse, tuttavia, la transazione Co.Ge. verrà sempre registrata nella valuta locale (LCY).

> [!Important]
> Non creare il codice valuta locale sia nella pagina **Setup contabilità generale** che nella pagina **Valute**. Ciò creerà confusione tra la valuta vuota e il codice LCY nella tabella delle valute e potrebbero essere creati accidentalmente conti bancari, clienti o fornitori, alcuni con la valuta vuota e altri con il codice LCY.

La contabilità generale è impostata per utilizzare la valuta locale (VL) ma è anche possibile impostarla per l'uso di un'altra valuta con un tasso di cambio della valuta assegnato. Se si imposta una seconda valuta come valuta contabile addizionale, in [!INCLUDE[prod_short](includes/prod_short.md)] gli importi in ogni movimento C/G e in tutti gli altri movimenti, ad esempio i movimenti IVA, vengono registrati automaticamente sia nella valuta locale che nella valuta addizionale. Per ulteriori informazioni, vedere [Impostare una valuta contabile addizionale](finance-how-setup-additional-currencies.md). La valuta di rendicontazione aggiuntiva viene spesso utilizzata per facilitare la rendicontazione finanziaria ai proprietari che risiedono in paesi/aree geografiche che utilizzano valute diverse dalla valuta locale (LCY).  

> [!IMPORTANT]
> Se desideri utilizzare una valuta aggiuntiva per i report finanziari, assicurati di aver compreso le limitazioni. Per ulteriori informazioni, vedere [Impostare una valuta contabile addizionale](finance-how-setup-additional-currencies.md).

## <a name="currencies"></a>Valute

Specificare i codici valuta in **Valute**, comprese le informazioni e le impostazioni aggiuntive necessarie per ciascun codice valuta.

> [!TIP]
> Crea le valute con il codice ISO internazionale come codice per semplificare il lavoro con la valuta in futuro.

|Campo|Descrizione|  
|---------------------------------|---------------------------------------|  
|**Codice**|L'identificatore per la valuta.|
|**descrizione**|Una descrizione a testo libero della valuta.|
|**Codice ISO**|Il codice internazionale di tre lettere della valuta definita in ISO 4217.|
|**Codice numerico ISO**|Il riferimento internazionale numerico della valuta definita in ISO 4217.|
|**Data tasso di cambio**|L'ultima data del tasso di cambio effettivo.|
|**Valuta UE**|Specifica se la valuta è una valuta UE, ad esempio EUR.|
|**Conto utili realizzati**|Il conto in cui verrà registrato il guadagno effettivo quando si ricevono i pagamenti per i crediti o si registra il tasso di cambio effettivo sui pagamenti ai debiti. Per un esempio di transazione in valuta clienti, vedere l'esempio sotto questa tabella. |
|**Conto perdite realizzate**|Il conto in cui verrà registrata la perdita effettiva quando si ricevono i pagamenti per i crediti o si registra il tasso di cambio effettivo sui pagamenti ai debiti. Per un esempio di transazione in valuta clienti, vedere l'esempio sotto questa tabella. |
|**Conto utili non realizzati**|Il conto in cui verrà registrato il guadagno teorico quando si esegue un aggiustamento valutario.|
|**Conto perdite non realizzate**|Il conto in cui verrà registrata la perdita teorica quando si esegue un aggiustamento valutario.|
|**Precisione arroto. importo**|Alcune valute hanno altri formati per gli importi delle fatture rispetto a quelli definiti nella pagina **Impostazione della contabilità generale**. Se si modifica la precisione arrot. importo per una valuta, tutti gli importi fattura in quella valuta verranno arrotondati con la precisione aggiornata.|
|**Posizioni decimali importo**|Alcune valute hanno altri formati per gli importi delle fatture rispetto a quelli definiti nella pagina **Impostazione della contabilità generale**. Se si modificano le posizioni decimali importo per una valuta, tutti gli importi fattura nella valuta verranno arrotondati con i decimali aggiornati|
|**Tipo di arrotondamento fattura**|Specifica il metodo da utilizzare se gli importi devono essere arrotondati. Le opzioni sono **Più vicino**, **Su**, e **Giù**.|
|**Precisione arrot. importo unitario**|Alcune valute hanno altri formati per gli importi delle unità rispetto a quelli definiti nella pagina **Impostazione della contabilità generale**. Se si modifica la precisione arrot. importo per un'unità, tutti gli importi unitari nella valuta verranno arrotondati con la precisione aggiornata.|
|**Posizione decimale importo unitario**|Alcune valute hanno altri formati per gli importi delle unità rispetto a quelli definiti nella pagina **Impostazione della contabilità generale**. Se si modificano le posizioni decimali importo per un'unità, tutti gli importi unitari nella valuta verranno arrotondati con i decimali aggiornati.|
|**Precisione arrot. importo**|Specifica le dimensioni dell'intervallo consentito come differenza di arrotondamento quando si collegano tra loro movimenti in valute diverse.|
|**Conversione Arrotondamento Conv. LCY. Conto di debito**|Specifica le informazioni sulla conversione che devono contenere anche un conto a debito se si desidera inserire delle righe di correzione per le differenze di arrotondamento nelle registrazioni COGE utilizzando la funzione **Inserisci righe arrot. conv.VL**.|
|**Conversione Arrotondamento Conv. LCY. Conto di credito**|Specifica le informazioni sulla conversione che devono contenere anche un conto a credito se si desidera inserire delle righe di correzione per le differenze di arrotondamento nelle registrazioni COGE utilizzando la funzione **Inserisci righe arrot. conv.VL**.|
|**Data ultima rettifica**|La data dell'ultimo aggiustamento valutario.|
|**Data ultima modifica**|La data di modifica dell'impostazione della valuta.|
|**% tolleranza pagamento**|La percentuale massima di tolleranza di pagamento impostata per questa valuta. Per ulteriori informazioni, vedere [Tolleranza pagamento e Tolleranza sconto pagamento](finance-payment-tolerance-and-payment-discount-tolerance.md). |
|**Importo massimo tolleranza pagamento**|L'importo massimo di tolleranza di pagamento impostata per questa valuta. Per ulteriori informazioni, vedere [Tolleranza pagamento e Tolleranza sconto pagamento](finance-payment-tolerance-and-payment-discount-tolerance.md). |
|**Fattore valuta**|Specifica la relazione tra la valuta contabile addizionale e la valuta locale utilizzando il tasso di valuta effettivo.|
|**Conto utili C/G realizzati**|Specifica il conto C/G utilizzato per registrate gli utili di conversione per le rettifiche valutarie tra la valuta locale e la valuta contabile addizionale. Gli utili di conversione vengono calcolati quando viene eseguito il processo batch Rettifica tassi di cambio per rettificare i conti di contabilità generale. Questo campo potrebbe non essere visibile per impostazione predefinita. Può essere recuperato personalizzando la pagina.|
|**Conto perdite C/G realizzate**|Specifica il conto C/G utilizzato per registrate le perdite di conversione per le rettifiche valutarie tra la valuta locale e la valuta contabile addizionale. Gli utili di conversione vengono calcolati quando viene eseguito il processo batch Rettifica tassi di cambio per rettificare i conti di contabilità generale. Questo campo potrebbe non essere visibile per impostazione predefinita. Può essere recuperato personalizzando la pagina.|
|**Conto guadagni residui**|Specifica il conto C/G utilizzato per registrare gli importi dei guadagni residui (differenze di arrotondamento) quando viene utilizzata una valuta contabile addizionale nell'area di applicazione della contabilità generale. Questo campo potrebbe non essere visibile per impostazione predefinita. Può essere recuperato personalizzando la pagina.|
|**Conto perdite residue**|Specifica il conto C/G utilizzato per registrare gli importi delle perdite residue (differenze di arrotondamento) quando viene utilizzata una valuta contabile addizionale nell'area di applicazione della contabilità generale. Questo campo potrebbe non essere visibile per impostazione predefinita. Può essere recuperato personalizzando la pagina.|
|**Max. differenza IVA permessa**|L'importo massimo consentito per le differenze IVA in questa valuta. Per ulteriori informazioni, vedere [Correzione manuale degli importi IVA nei documenti di vendita e di acquisto](finance-work-with-vat.md#correcting-vat-amounts-manually-in-sales-and-purchase-documents). Questo campo potrebbe non essere visibile per impostazione predefinita. Può essere recuperato personalizzando la pagina.|
|**Tipo arrotondamento IVA**|Specifica il metodo di arrotondamento per la correzione manuale degli importi IVA nei documenti di vendita e di acquisto. Questo campo potrebbe non essere visibile per impostazione predefinita. Può essere recuperato personalizzando la pagina.|

### <a name="example-of-a-receivable-currency-transaction"></a>Esempio di una transazione in valuta esigibile

Quando ricevi una fattura da un'azienda in valuta estera, è abbastanza facile calcolare il valore in valuta locale (VL) della fattura in base al tasso di cambio corrente. Tuttavia, la fattura spesso viene fornita con termini di pagamento in modo da poter ritardare il pagamento a una data successiva, il che implica un tasso di cambio potenzialmente diverso. Questo problema, in combinazione con il fatto che i tassi di valuta bancaria differiscono sempre dai tassi di valuta ufficiali, rende impossibile anticipare l'importo esatto in valuta locale (VL) richiesto per coprire la fattura. Se la data di scadenza della fattura si estende al mese successivo, potrebbe essere necessario rivalutare l'importo in valuta locale (VL) alla fine del mese. La rettifica della valuta è necessaria perché il nuovo valore VL richiesto per coprire l'importo della fattura potrebbe essere diverso e il debito della società nei confronti del fornitore è potenzialmente cambiato. Il nuovo importo VL potrebbe essere superiore o inferiore all'importo precedente e rappresenta quindi un guadagno o una perdita. Tuttavia, poiché la fattura non è stata ancora pagata, si considera l'utile o la perdita come *non realizzati*. Successivamente, la fattura viene pagata e la banca restituisce il tasso di cambio effettivo per il pagamento. Fino ad allora l'utile o la perdita *realizzati* non vengono calcolati. L'utile o la perdita non realizzati vengono quindi stornati e al loro posto vengono registrati l'utile o la perdita realizzati.

Nell'esempio seguente, il 1° gennaio viene ricevuta una fattura con l'importo in valuta di 1000. Al momento il tasso di cambio è 1,123.

|Date|Azione|Importo valuta|Aliquota documento|Importo LCY nel documento|Tasso di cambio|Importo utili non realizzati|Aliquota Pagamento|Importo perdite realizzate|  
|-----|----------|------------|-----------|---------|-----------|-------------|---------|---------|
|1/1|**Fattura**|1000|1,123|1123|||||
|1/31|**Rettifica**|1000||1125|1,125|2|||
|2/15|**Rettifica Storno al pagamento**|1000||||-2|||
|2/15|**Pagamento**|1000||1120|||1,120|-3|

Alla fine del mese viene eseguito un aggiustamento valutario in cui il tasso di valuta aggiustamento è stato impostato a 1,125, che attiva un guadagno non realizzato di 2.

Al momento del pagamento, il tasso di cambio effettivo registrato sulla transazione bancaria mostra un tasso di valuta di 1,120.

Qui c'è una transazione non realizzata, e quindi verrà stornata insieme al pagamento.

Infine, il pagamento viene registrato e la perdita effettiva viene registrata nel conto delle perdite realizzate.

## <a name="available-currency-functions"></a>Funzioni valuta disponibili

La tabella seguente illustra le azioni chiave sulla pagina **Valute**. Alcune delle azioni sono spiegate nelle sezioni successive.  

|Menu|Azione|Descrizione|
|-------------|--------------|------------------------------|
|**Processo**|**Suggerisci conti**|Usa conti di altre valute. Verranno inseriti gli account utilizzati più di frequente.|
||Modifica tolleranza pagamento|Modificare la tolleranza di pagamento massima e/o la percentuale di tolleranza di pagamento e applicare un filtro in base alla valuta. Per ulteriori informazioni, vedere [Tolleranza pagamento e Tolleranza sconto pagamento](finance-payment-tolerance-and-payment-discount-tolerance.md)|
||**Tassi di cambio**|Visualizzare i tassi di cambio aggiornati per le valute utilizzate.|
||**Rettifica tassi di cambio**|Rettificare i movimenti nei conti C/G, cliente, fornitore e bancari, al fine di presentare un saldo aggiornato nel caso in cui il tasso di cambio sia stato modificato dopo la data di registrazione.|
||**Registro rettifica tassi di cambio**|Visualizza i risultati dell'esecuzione del processo batch **Regola i tassi di cambio**. Per ogni combinazione di categoria di registrazione e valuta inclusa nella rettifica viene creata una riga.|
|**Servizio tasso di cambio**|**Servizi tasso di cambio**|Visualizza o modifica il setup dei servizi impostati per recuperare i tassi di cambio valuta aggiornati quando si sceglie l'azione **Aggiorna tassi di cambio**.|
||**Aggiorna tassi di cambio**|Ottenere i tassi di cambio valuta più recenti da un provider di servizi.|
|**Report**|**Saldo valuta estera**|Visualizza i saldi di tutti i clienti e i fornitori, sia in valuta estera che in valuta locale (VL). Il report fornisce due tipi di saldo in valuta locale. Uno è il saldo in valuta estera convertito in valuta locale utilizzando il tasso di cambio al momento della transazione. L'altro è il saldo in valuta estera convertito in valuta locale utilizzando il tasso di cambio della data di lavoro.|

## <a name="exchange-rates"></a>Tassi di cambio

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

## <a name="adjusting-exchange-rates"></a>Rettifica di tassi di cambio

Poiché i tassi di cambio oscillano costantemente, gli equivalenti in valuta addizionale nel sistema devono essere rettificati periodicamente. Se queste rettifiche non vengono apportate, gli importi che sono stati convertiti da valute estere (o addizionali) e registrati nella contabilità generale in valuta locale possono essere fuorvianti. Inoltre, i movimenti quotidiani registrati prima dell'immissione di un tasso di cambio quotidiano nell'applicazione devono essere aggiornati dopo l'immissione delle informazioni su tale tasso di cambio.

Il processo batch **Rettifica tassi di cambio** viene utilizzato manualmente per rettificare i tassi di cambio dei movimenti cliente, fornitore e conti C/C bancari registrati. Consente inoltre di aggiornare gli importi nella valuta contabile addizionale nei movimenti C/G.  

> [!TIP]
> È possibile utilizzare un servizio per aggiornare automaticamente i tassi di cambio nel sistema. Per ulteriori informazioni, vedere [Per impostare un servizio dei tassi di cambio delle valute](finance-how-update-currencies.md#to-set-up-a-currency-exchange-rate-service). Tuttavia, ciò non modifica i tassi di cambio sulle transazioni già registrate. Per aggiornare i tassi di cambio sui movimenti registrati, utilizzare il processo batch **Modifica i tassi di cambio**.

### <a name="effect-on-customers-and-vendors"></a>Effetto su clienti e fornitori

Per i conti di clienti e fornitori, la valuta viene rettificata in base al tasso di cambio valido alla data di registrazione specificata nel processo batch. Durante il processo batch vengono calcolate le differenze per singoli saldi in valuta, quindi gli importi vengono registrati nel conto C/G specificato nel campo **Conto utili non-realizzati** o nel campo **Conto Perdite Non-Realizzate** della pagina **Valuta**. I movimenti rettificativi vengono automaticamente registrati nel conto crediti/debiti della contabilità generale.

Il processo batch consente di elaborare tutti i movimenti registro clienti e i movimenti fornitori aperti. Se per un movimento vi è una differenza di tasso di cambio, il processo batch crea un nuovo registro fornitori o un nuovo registro clienti dettagliato, che riflette l'importo rettificato nel registro fornitori o clienti.

#### <a name="dimensions-on-customer-and-vendor-ledger-entries"></a>Dimensioni nei movimenti clienti e fornitori

Ai movimenti di rettifica vengono assegnate le dimensioni dei movimenti del registro clienti/fornitori e le rettifiche vengono registrate per combinazione di valori di dimensione.

### <a name="effect-on-bank-accounts"></a>Effetto su conti correnti bancari

Per i conti correnti bancari, la valuta viene rettificata utilizzando il tasso di cambio valido alla data di registrazione specificata nel processo batch. Durante il processo batch vengono calcolate le differenze per ogni conto corrente bancario che ha un codice di valuta, quindi gli importi vengono registrati nel conto C/G specificato nel campo **Conto utili realizzati** o nel campo **Conto Perdite Realizzate** della pagina **Valuta**. I movimenti rettificativi vengono automaticamente registrati nei conti correnti bancari CoGe specificati nelle categorie di registrazione dei conti correnti bancari. Viene calcolato un solo movimento per valuta per categoria di registrazione.

#### <a name="dimensions-on-bank-account-entries"></a>Dimensioni nei movimenti di conti correnti bancari

Ai movimenti di rettifica per il conto CoGe del conto corrente bancario e per il conto profitti/perdite vengono assegnate le dimensioni di default del conto corrente bancario.

### <a name="effect-on-gl-accounts"></a>Effetto su conti C/G
Se si effettua una registrazione in una valuta contabile addizionale, è possibile impostare il processo batch per creare nuovi movimenti di contabilità generale per rettifiche valutarie comprese tra VL e la valuta contabile addizionale. Verranno calcolate le differenze per ogni movimento C/G e inserite delle rettifiche a seconda del contenuto del campo **Rettifica tasso di cambio** di ogni conto C/G.

##### <a name="dimensions-on-gl-account-entries"></a>Dimensioni nei movimenti del conto C/G
Ai movimenti di rettifica vengono assegnate le dimensioni di default dei conti in cui vengono registrati.

> [!Important]
> Prima di eseguire il processo batch, è necessario immettere i tassi di cambio di rettifica necessari alla rettifica dei saldi in valuta estera. Questa operazione viene eseguita nella pagina **Tassi di cambio valuta**.<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Q24s?rel=0]

## <a name="to-set-up-a-currency-exchange-rate-service"></a>Per impostare un servizio dei tassi di cambio delle valute
È possibile utilizzare un servizio esterno per mantenere aggiornati i tassi di cambio delle valute, ad esempio FloatRates.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Servizi di tassi di cambio valute**, quindi seleziona il collegamento correlato.
2. Scegliere l'azione **Nuovo**.
3. Nella pagina **Servizi tasso di cambio valuta** compilare i campi secondo le necessità. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Attivare il pulsante **Abilitato** per attivare per abilitare il servizio.

> [!NOTE]
> Il seguente video mostra un esempio di come connettersi a un servizio di cambio valuta, utilizzando la Banca centrale europea come esempio. Nel segmento che descrive come impostare le mappature dei campi, l'impostazione nella colonna **Sorgente** per il **Nodo padre per codice valuta** restituirà solo la prima valuta trovata. L'impostazione deve essere `/gesmes:Envelope/Code/Code/Code`.

<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4A1jy?rel=0]

## <a name="to-update-currency-exchange-rates-through-a-service"></a>Per aggiornare i tassi di cambio delle valute mediante un servizio
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Valute**, quindi scegli il collegamento correlato.
2. Scegliere l'azione **Aggiorna tassi di cambio**.

Il valore nel campo **Tasso di cambio** della pagina **Valute** viene aggiornato con il tasso di cambio delle valute più recente.

## <a name="see-related-training-at-microsoft-learn"></a>Vedere le informazioni relative al training in [Microsoft Learn](/learn/paths/use-multiple-currencies-dynamics-365-business-central/)

## <a name="see-also"></a>Vedere anche
[Impostare una valuta contabile addizionale](finance-how-setup-additional-currencies.md)  
[Chiusura di anni e periodi](year-close-years-periods.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
