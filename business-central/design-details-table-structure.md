---
title: 'Dettagli di progettazione: Struttura della tabella | Microsoft Docs'
description: 'Per comprendere in che modo sono state riprogettate l''archiviazione e la registrazione dei movimenti dimensione, è importante comprendere la struttura della tabella.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/08/2021
ms.author: edupont
---
# Dettagli di progettazione: Struttura della tabella
Per comprendere in che modo i movimenti dimensione sono archiviati e registrati, è importante comprendere la struttura della tabella.  

## Tabella 480, Movimento set di dimensioni  
Non è possibile modificare questa tabella. Dopo avere scritto i dati nella tabella, non è possibile eliminarli o modificarli.

|Nr. campo|Nome campo|Tipo di dati|Commento|  
|---------------|----------------|---------------|-------------|  
|1|**ID**|Nr. intero|>0,0 è prenotato per il set di dimensioni vuoto. Fa riferimento al campo 3 nella tabella 481.|  
|2|**Codice dimensione**|Codice 20|Relazione tabella a tabella 348.|  
|3|**Codice valore dimensioni**|Codice 20|Relazione tabella a tabella 349.|  
|4|**ID valore dimensioni**|Nr. intero|Fa riferimento al campo 12 nella tabella 349. Si tratta della chiave secondaria utilizzata per lo scorrimento della tabella 481.|  
|5|**Nome dimensione**|Testo 30|CalcField. Vedere la tabella 348.|  
|6|**Nome valore dimensioni**|Testo 30|CalcField. Vedere la tabella 349.|  

## Tabella 481, Nodo albero set di dimensioni  
Non è possibile modificare questa tabella. Viene utilizzata per cercare un set di dimensioni. Se il set di dimensioni non viene trovato, verrà creato un nuovo set.  

|Nr. campo|Nome campo|Tipo di dati|Commento|  
|---------------|----------------|---------------|-------------|  
|1|**ID set di dimensioni padre**|Nr. intero|0 per il nodo di livello superiore.|  
|2|**ID valore dimensioni**|Nr. intero|Relazione tabella a campo 12 nella tabella 349.|  
|3|**ID set di dimensioni**|Nr. intero|AutoIncrement. Utilizzato nel campo 1 della tabella 480.|  
|4|**In uso**|Booleano|False se non in uso.|  

## Buffer set di dimensioni di riclassificazione tabella 482  
Questa tabella viene utilizzata quando si modifica un codice valore di dimensioni, ad esempio, in un movimento contabile articolo utilizzando la pagina **Registrazioni riclassificazione articolo**.  

|Nr. campo|Nome campo|Tipo di dati|Commento|  
|---------------|----------------|---------------|-------------|  
|1|**Codice dimensione**|Codice 20|Relazione tabella a tabella 348.|  
|2|**Codice valore dimensioni**|Codice 20|Relazione tabella a tabella 349.|  
|3|**ID valore dimensioni**|Nr. intero|Fa riferimento al campo 12 nella tabella 349.|  
|4|**Nuovo Codice Valore Dimensioni:**|Codice 20|Relazione tabella a tabella 349.|  
|5|**Nuovo ID valore dimensioni**|Nr. intero|Fa riferimento al campo 12 nella tabella 349.|  
|6|**Nome dimensione**|Testo 30|CalcField. Vedere la tabella 348.|  
|7|**Nome valore dimensioni**|Testo 30|CalcField. Vedere la tabella 349.|  
|8|**Nuovo nome valore dimensioni**|Testo 30|CalcField. Vedere la tabella 349.|  

## Tabelle del budget e delle transazioni  
Oltre agli altri campi dimensione nella tabella, questo campo è importante:  

|Nr. campo|Nome campo|Tipo di dati|Commento|  
|---------------|----------------|---------------|-------------|  
|480|**ID set di dimensioni**|Nr. intero|Fa riferimento al campo 1 nella tabella 480.|  

### Tabella 83, Righe reg. magazzino  
Oltre agli altri campi dimensione nella tabella, questi campi sono importanti.  

|Nr. campo|Nome campo|Tipo di dati|Commento|  
|---------------|----------------|---------------|-------------|  
|480|**ID set di dimensioni**|Nr. intero|Fa riferimento al campo 1 nella tabella 480.|  
|481|**Nuovo ID set di dimensioni**|Nr. intero|Fa riferimento al campo 1 nella tabella 480.|  

### Tabella 349, Valore dimensioni  
Oltre agli altri campi dimensione nella tabella, questi campi sono importanti.  

|Nr. campo|Nome campo|Tipo di dati|Commento|  
|---------------|----------------|---------------|-------------|  
|12|**ID valore dimensioni**|Nr. intero|AutoIncrement. Utilizzato per i riferimenti nelle tabelle 480 e 481.|  

### Tabelle che contengono il campo ID set di dimensioni
 Il campo **ID set di dimensioni** (480) esiste nelle seguenti tabelle. Per le tabelle che memorizzano i dati registrati, il campo fornisce soltanto una visualizzazione non modificabile di dimensioni, contrassegnata come drill-down. Per le tabelle che memorizzano i documenti di lavoro, il campo è modificabile. Le tabelle buffer utilizzate internamente non richiedono funzionalità modificabili o non modificabili.  

 Il campo 480 non è modificabile nelle seguenti tabelle.  

|Nr. tabella|Nome tabella|  
|---------------|----------------|  
|17|**Movimenti C/G**|  
|21|**Mov. contabili clienti**|  
|25|**Mov. contabili fornitori**|  
|32|**Mov. Contabile Articoli**|  
|110|**Testate sped. vendita**|  
|111|**Righe sped. vendite**|  
|112|**Testate Fatt. Vendita**|  
|113|**Righe Fatt. Vendita**|  
|114|**Testate nota cr. vendita**|  
|115|**Righe nota cr. vendita**|  
|120|**Testata carico acq.**|  
|121|**Righe carico acq.**|  
|122|**Testate fatt. acq.**|  
|123|**Righe fatt. acq.**|  
|124|**Testate Nota Cr. Acq.**|  
|125|**Righe nota cr. acq.**|  
|169|**Mov. contabili commesse**|  
|203|**Mov. contabili risorse**|  
|271|**Mov. Contabili C/C Bancari**|  
|281|**Mov. contabile inventario fis.**|  
|297|**Testata sollecito emesso**|  
|304|**Testate note add. int. emesse**|  
|5107|**Archivio testate vendita**|  
|5108|**Archivio righe vendita**|  
|5109|**Archivio testate acquisto**|  
|5110|**Archivio Righe Acquisto**|  
|5601|**Mov. contabili cespiti**|  
|5625|**Mov. cont. manutenzioni**|  
|5629|**Mov. contabili copertura ass.**|  
|5744|**Testata spedizioni per trasf.**|  
|5745|**Riga spedizione trasferimento**|  
|5746|**Testata carico trasfer.**|  
|5747|**Righe carico trasferim.**|  
|5802|**Mov. valorizzazione**|  
|5832|**Movimento contabile capacità**|  
|5907|**Movimenti assistenza**|  
|5908|**Testata assistenza**|  
|5933|**Buffer reg. ordine assist.**|  
|5970|**Testata contratto assistenza archiviata**|  
|5990|**Testata spedizione assistenza**|  
|5991|**Riga spedizione assistenza**|  
|5992|**Testata fattura assistenza**|  
|5993|**Riga fattura assistenza**|  
|5994|**Testata nota credito assistenza**|  
|5995|**Riga nota credito assistenza**|  
|6650|**Testata spediz. per resi**|  
|6651|**Riga spedizione reso**|  
|6660|**Testata carico da reso**|  
|6661|**Riga carico da reso**|  

Il campo 480 è modificabile nelle seguenti tabelle.  

|Nr. tabella|Nome tabella|  
|---------------|----------------|  
|36|**Testate vendita**|  
|37|**Righe Vendite**|  
|38|**Testate acquisti**|  
|39|**Riga Acquisto**|  
|81|**Righe registrazioni COGE**|  
|83|**Righe reg. magazzino**|  
|89|**Riga registrazioni DBA**|  
|96|**Movimenti budget C/G**|  
|207|**Righe registrazioni risorse**|  
|210|**Righe reg. commesse**|  
|221|**Allocazioni registrazioni gen.**|  
|246|**Riga Richiesta**|  
|295|**Testata sollecito**|  
|302|**Testate note add. interessi**|  
|5405|**Ordine di produzione**|  
|5406|**Righe Ordini Prod.**|  
|5407|**Componenti Ordini Produzione**|  
|5615|**Allocazione cespiti**|  
|5621|**Righe registrazioni cespiti**|  
|5635|**Righe reg. assicurazioni**|  
|5740|**Testata trasferimenti**|  
|5741|**Riga trasferimento**|  
|5900|**Testata assistenza**|  
|5901|**Riga articolo in assistenza**|  
|5902|**Riga assistenza**|  
|5965|**Testata contratto assistenza**|  
|5997|**Riga assistenza standard**|  
|7134|**Mov. budget articoli**|  
|99000829|**Componente Pianificazione**|  

Il campo 480 esiste nelle seguenti tabelle buffer.  

|Nr. tabella|Nome tabella|  
|---------------|----------------|  
|49|**Buffer Reg. Fatture**|  
|212|**Buffer reg. commesse**|  
|372|**Buffer pagamenti**|  
|382|**Mov. buffer CF**|  
|461|**Buffer riga fattura pagam. anticipato**|  
|5637|**Buffer reg. C/G cespiti**|  
|7136|**Buffer budget articoli**|  

## Vedere anche

[Sintesi movimenti set di dimensioni](design-details-dimension-set-entries-overview.md)  
[Dettagli di progettazione: Ricerca delle combinazioni di dimensione](design-details-searching-for-dimension-combinations.md)   
