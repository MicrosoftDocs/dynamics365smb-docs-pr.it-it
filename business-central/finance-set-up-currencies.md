---
title: Impostare le valute
description: Devi impostare ogni valuta se acquisti o vendi in valute diverse dalla valuta locale (VL) o si registrano transazioni C/G in valute diverse.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: multiple currencies
ms.search.form: '5, 118'
ms.date: 06/10/2024
ms.service: dynamics-365-business-central
---
# Impostare le valute

[!INCLUDE [finance-currencies-def](includes/finance-currencies-def.md)]

Puoi utilizzare un servizio esterno per ottenere i tassi di cambio valuta più aggiornati nell'elenco **Valute**. Per ulteriori informazioni, vedere [Per impostare un servizio dei tassi di cambio delle valute](finance-how-update-currencies.md#set-up-a-currency-exchange-rate-service).  

[!INCLUDE [finance-currencies-lcy](includes/finance-currencies-lcy-note.md)]

## <a name="curr"></a>Valute

La tabella seguente descrive i campi dell'elenco **Valute**.

|Campo|Descrizione|  
|---------------------------------|---------------------------------------|  
|**Codice**|L'identificatore per la valuta.|
|**descrizione**|Una descrizione a testo libero della valuta.|
|**Codice ISO**|Il codice internazionale di tre lettere della valuta definita in ISO 4217.|
|**Codice numerico ISO**|Il riferimento internazionale numerico della valuta definita in ISO 4217.|
|**Data tasso di cambio**|L'ultima data del tasso di cambio effettivo.|
|**Valuta UE**|Specifica se la valuta è una valuta UE, ad esempio EUR.|
|**Conto utili realizzati**|Il conto in cui viene registrato il guadagno effettivo quando si ricevono i pagamenti per i crediti o si registra il tasso di cambio effettivo sui pagamenti ai debiti. Per un esempio di transazione in valuta clienti, vedere l'esempio sotto questa tabella. |
|**Conto perdite realizzate**|Il conto in cui viene registrata la perdita effettiva quando si ricevono i pagamenti per i crediti o si registra il tasso di cambio effettivo sui pagamenti ai debiti. Per un esempio di transazione in valuta clienti, vedere l'esempio sotto questa tabella. |
|**Conto utili non realizzati**|Il conto in cui viene registrato il guadagno teorico quando si esegue un aggiustamento valutario.|
|**Conto perdite non realizzate**|Il conto in cui viene registrata la perdita teorica quando si esegue un aggiustamento valutario.|
|**Precisione arrotondamento importo**|Alcune valute hanno altri formati per gli importi delle fatture rispetto a quelli definiti nella pagina **Impostazione della contabilità generale**. Se si modifica la precisione arrot. importo per una valuta, tutti gli importi fattura in quella valuta vengono arrotondati con la precisione aggiornata.|
|**Posizioni decimali importo**|Alcune valute hanno altri formati per gli importi delle fatture rispetto a quelli definiti nella pagina **Impostazione della contabilità generale**. Se si modificano le posizioni decimali importo per una valuta, tutti gli importi fattura nella valuta vengono arrotondati con i decimali aggiornati|
|**Tipo di arrotondamento fattura**|Specifica il metodo da utilizzare se gli importi devono essere arrotondati. Le opzioni sono **Più vicino**, **Su**, e **Giù**.|
|**Precisione arrot. importo unitario**|Alcune valute hanno altri formati per gli importi delle unità rispetto a quelli definiti nella pagina **Impostazione della contabilità generale**. Se si modifica la precisione arrot. importo per un'unità, tutti gli importi unitari nella valuta vengono arrotondati con la precisione aggiornata.|
|**Posizione decimale importo unitario**|Alcune valute hanno altri formati per gli importi delle unità rispetto a quelli definiti nella pagina **Impostazione della contabilità generale**. Se si modificano le posizioni decimali importo per un'unità, tutti gli importi unitari nella valuta vengono arrotondati con i decimali aggiornati.|
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
|**Max. differenza IVA permessa**|L'importo massimo consentito per le differenze IVA in questa valuta. Per ulteriori informazioni, vedi [Correzione manuale degli importi IVA nei documenti di vendita e di acquisto](finance-work-with-vat.md#correcting-vat-amounts-manually-on-sales-and-purchase-documents). Questo campo potrebbe non essere visibile per impostazione predefinita. Può essere recuperato personalizzando la pagina.|
|**Tipo arrotondamento IVA**|Specifica il metodo di arrotondamento per la correzione manuale degli importi IVA nei documenti di vendita e di acquisto. Questo campo potrebbe non essere visibile per impostazione predefinita. Può essere recuperato personalizzando la pagina.|

### Funzioni valuta disponibili

La tabella seguente illustra le azioni chiave sulla pagina **Valute**.  

|Menu|Azione|Descrizione|
|-------------|--------------|------------------------------|
|**Processo**|**Suggerisci conti**|Usa conti di altre valute. Vengono inseriti gli account utilizzati più di frequente.|
||**Modifica tolleranza pagamento**|Modificare la tolleranza di pagamento massima e/o la percentuale di tolleranza di pagamento e applicare un filtro in base alla valuta. Per ulteriori informazioni, vedere [Tolleranza pagamento e Tolleranza sconto pagamento](finance-payment-tolerance-and-payment-discount-tolerance.md)|
||**Tassi di cambio**|Visualizzare i tassi di cambio aggiornati per le valute utilizzate.|
||**Rettifica tassi di cambio**|Aggiorna i saldi dei movimenti di contabilità generale, clienti, fornitori e conti correnti bancari. L'aggiornamento è utile se il tasso di cambio è cambiato dopo la registrazione dei movimenti.|
||**Registro rettifica tassi di cambio**|Visualizza i risultati dell'esecuzione del processo batch **Regola i tassi di cambio**. Per ogni combinazione di categoria di registrazione e valuta inclusa nella rettifica viene creata una riga.|
|**Servizio tasso di cambio**|**Servizi tasso di cambio**|Visualizza o modifica il setup dei servizi impostati per recuperare i tassi di cambio valuta aggiornati quando si sceglie l'azione **Aggiorna tassi di cambio**.|
||**Aggiorna tassi di cambio**|Ottenere i tassi di cambio valuta più recenti da un provider di servizi.|
|**Report**|**Saldo valuta estera**|Visualizza i saldi di tutti i clienti e i fornitori, sia in valuta estera che in valuta locale (VL). Il report fornisce due tipi di saldo in valuta locale. Uno è il saldo in valuta estera convertito in valuta locale utilizzando il tasso di cambio al momento della transazione. L'altro è il saldo in valuta estera convertito in valuta locale utilizzando il tasso di cambio della data di lavoro.|

## VL e altre valute

[!INCLUDE [finance-currencies-lcy-def](includes/finance-currencies-lcy-def.md)]

## Arrotondamento delle valute

Per gestire le valute che non utilizzano decimali e per evitare decimali non necessari in valuta estera, è possibile utilizzare due diverse funzionalità di arrotondamento:

- Arrotondamento importo unitario  

- Arrotondamento importo  

Queste funzionalità possono essere utilizzate separatamente o insieme. Possono inoltre essere utilizzate insieme all'arrotondamento fattura.

Contrariamente alle funzionalità di arrotondamento fattura, le funzionalità di arrotondamento importo e arrotondamento importo unitario hanno impatto unicamente sugli importi in valuta estera-non sugli importi corrispondenti in valuta locale. Queste due funzionalità non generano alcuna registrazione nei conti CoGe. Di conseguenza, non è necessario specificare alcun conto CoGe nelle categorie di registrazione o altrove.

### Arrotondamento importo unitario

La funzionalità di arrotondamento importo unitario controlla il modo in cui i prezzi di vendita per gli articoli e le risorse in valuta estera vengono arrotondati nelle righe di acquisto e vendita. È necessario specificare separatamente le regole per ogni valuta nel campo **Precisione arrot. importo unit** nell'elenco **Valute**.

La funzionalità di arrotondamento importo unitario viene utilizzata automaticamente ogni volta che viene immesso un numero di articolo o risorsa in una riga di vendita. Se la fattura viene emessa per un cliente con un codice valuta, il prezzo dell'articolo o della risorsa viene convertito nella valuta del cliente. Il prezzo viene arrotondato in base alla precisione di arrotondamento importo unitario per la valuta.

### Arrotondamento importo

La funzionalità di arrotondamento importo controlla il modo in cui gli importi in valuta estera vengono arrotondati nelle righe registrazioni COGE, nelle righe di vendita e di acquisto. È necessario specificare separatamente le regole per ogni valuta nel campo **Precisione arrot. importo** nell'elenco **Valute**.

Gli importi in valuta estera vengono arrotondati quando si compilano e si registrano le righe registrazioni COGE, le righe di vendita e di acquisto.

## Tassi di cambio

È possibile registrare i tassi di cambio per ogni valuta estera e specificare da quali date risultano validi i tassi di cambio. Ad esempio, è possibile immettere tassi di cambio giornalieri, mensili o trimestrali per ogni valuta estera.

È possibile mantenere tassi di cambio storici nella pagina **Tassi di cambio valuta** a scopo di riferimento. Quando è necessario aggiornare i tassi di cambio, è possibile utilizzare il pulsante **Aggiorna tassi di cambio** per acquisire i tassi di cambio più aggiornati da un provider di servizi esterno.

## Conti di contabilità generale

Non è possibile collegare codici valuta a conti di contabilità generale perché gli importi in questi conti sono espressi in valuta locale. Se si è stipulato un mutuo bancario in USD e si effettuano depositi in un conto bancario in SEK, è possibile tenere traccia di questi conti impostando conti bancari in USD e SEK. Mediante le categorie di registrazione, è possibile collegare i conti ai conti di contabilità generale rilevanti. Nella contabilità generale il valore degli importo è espresso in valuta locale.

È possibile immettere un codice valuta in una riga registrazioni COGE e registrare la riga in un conto CoGe. Il tasso di cambio rilevante viene utilizzato per convertire l'importo in valuta locale prima che sia registrato nel conto CoGe.  

## Esempio di una transazione in valuta esigibile

[!INCLUDE [finance-currencies-example](includes/finance-currencies-example.md)]

## Vedere anche

[Aggiornare i tassi di cambio valuta](finance-how-update-currencies.md)  
[Impostare una valuta contabile addizionale](finance-how-setup-additional-currencies.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
