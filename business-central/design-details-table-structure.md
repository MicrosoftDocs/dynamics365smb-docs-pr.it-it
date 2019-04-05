---
title: 'Dettagli di progettazione: Struttura della tabella | Microsoft Docs'
description: Per comprendere in che modo sono state riprogettate l'archiviazione e la registrazione dei movimenti dimensione, è importante comprendere la struttura della tabella.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 02/11/2019
ms.author: sgroespe
ms.openlocfilehash: b2e87b2ef999c04cc4c878d4ad087329d644b709
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/08/2019
ms.locfileid: "801315"
---
# <a name="design-details-table-structure"></a>Dettagli di progettazione: Struttura della tabella
Per comprendere in che modo sono state riprogettate l'archiviazione e la registrazione dei movimenti dimensione, è importante comprendere la struttura della tabella.  

## <a name="new-tables"></a>Nuove tabelle  
 Sono state progettate tre nuove tabelle per gestire i movimenti di set di dimensioni.  

### <a name="table-480-dimension-set-entry"></a>Voce set di dimensioni tabella 480  
 Non è possibile modificare questa tabella. Dopo avere scritto i dati nella tabella, non è possibile eliminarli o modificarli.

|Nr. campo|Nome campo|Tipo di dati|Commento|  
|---------------|----------------|---------------|-------------|  
|1|**ID**|Nr. intero|>0,0 è prenotato per il set di dimensioni vuoto. Fa riferimento al campo 3 nella tabella 481.|  
|2|**Codice dimensione**|Codice 20|Relazione tabella a tabella 348.|  
|3|**Codice valore dimensioni**|Codice 20|Relazione tabella a tabella 349.|  
|4|**ID valore dimensioni**|Nr. intero|Fa riferimento al campo 12 nella tabella 349. Si tratta della chiave secondaria utilizzata per lo scorrimento della tabella 481.|  
|5|**Nome dimensione**|Testo 30|CalcField. Vedere la tabella 348.|  
|6|**Nome valore dimensioni**|Testo 30|CalcField. Vedere la tabella 349.|  

### <a name="table-481-dimension-set-tree-node"></a>Nodo albero set di dimensioni tabella 481  
 Non è possibile modificare questa tabella. Viene utilizzata per cercare un set di dimensioni. Se il set di dimensioni non viene trovato, verrà creato un nuovo set.  

|Nr. campo|Nome campo|Tipo di dati|Commento|  
|---------------|----------------|---------------|-------------|  
|1|**ID set di dimensioni padre**|Nr. intero|0 per il nodo di livello superiore.|  
|2|**ID valore dimensioni**|Nr. intero|Relazione tabella a campo 12 nella tabella 349.|  
|3|**ID set di dimensioni**|Nr. intero|AutoIncrement. Utilizzato nel campo 1 della tabella 480.|  
|4|**In uso**|Booleano|False se non in uso.|  

### <a name="table-482-reclas-dimension-set-buffer"></a>Buffer set di dimensioni di riclassificazione tabella 482  
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

## <a name="modified-tables"></a>Tabelle modificate  
 Tutte le tabelle del budget e delle transazioni sono state modificate per gestire i movimenti set di dimensioni.  

### <a name="changes-to-transaction-and-budget-tables"></a>Modifiche alle Tabelle del budget e delle transazioni  
 Un nuovo campo è stato aggiunto a tutte le tabelle di budget e di transazione.  

|Nr. campo|Nome campo|Tipo di dati|Commento|  
|---------------|----------------|---------------|-------------|  
|480|**ID set di dimensioni**|Nr. intero|Fa riferimento al campo 1 nella tabella 480.|  

### <a name="changes-to-table-83-item-journal-line"></a>Modifiche alla riga registrazione magazzino della Tabella 83  
 Sono stati aggiunti due nuovi campi alla tabella 83 **Righe reg. magazzino**.  

|Nr. campo|Nome campo|Tipo di dati|Commento|  
|---------------|----------------|---------------|-------------|  
|480|**ID set di dimensioni**|Nr. intero|Fa riferimento al campo 1 nella tabella 480.|  
|481|**Nuovo ID set di dimensioni**|Nr. intero|Fa riferimento al campo 1 nella tabella 480.|  

### <a name="changes-to-table-349-dimension-value"></a>Modifiche al valore delle dimensioni della tabella 349  
 Un nuovo campo è stato aggiunto alla tabella 349 **Valore dimensioni**.  

|Nr. campo|Nome campo|Tipo di dati|Commento|  
|---------------|----------------|---------------|-------------|  
|12|**ID valore dimensioni**|Nr. intero|AutoIncrement. Utilizzato per i riferimenti nelle tabelle 480 e 481.|  

### <a name="tables-that-get-new-field-480-dimension-set-id"></a>Tabelle che ottengono il nuovo campo ID set di dimensioni 480  
 Un nuovo campo, 480 **ID set di dimensioni**, è stato aggiunto alle seguenti tabelle. Per le tabelle che memorizzano i dati registrati, il campo fornisce soltanto una visualizzazione non modificabile di dimensioni, contrassegnata come drill-down. Per le tabelle che memorizzano i documenti di lavoro, il campo è modificabile. Le tabelle buffer utilizzate internamente non richiedono funzionalità modificabili o non modificabili.  

 Il campo 480 non può essere modificato nelle seguenti tabelle.  

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

 Il campo 480 può essere modificato nelle seguenti tabelle.  

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

 Il campo 480 è stato aggiunto alle seguenti tabelle buffer.  

|Nr. tabella|Nome tabella|  
|---------------|----------------|  
|49|**Buffer Reg. Fatture**|  
|212|**Buffer reg. commesse**|  
|372|**Buffer pagamenti**|  
|382|**Mov. buffer CF**|  
|461|**Buffer riga fattura pagam. anticipato**|  
|5637|**Buffer reg. C/G cespiti**|  
|7136|**Buffer budget articoli**|  

## <a name="see-also"></a>Vedi anche  
 [Dettagli di progettazione: Movimenti set di dimensioni](design-details-dimension-set-entries.md)   
 [Sintesi movimenti set di dimensioni](design-details-dimension-set-entries-overview.md)   
 [Dettagli di progettazione: Ricerca delle combinazioni di dimensione](design-details-searching-for-dimension-combinations.md)   
 [Dettagli di progettazione: Gestione dimensioni della codeunit 408](design-details-codeunit-408-dimension-management.md)   
 [Dettagli di progettazione: Esempi di codice dei modelli modificati nelle modifiche](design-details-code-examples-of-changed-patterns-in-modifications.md)
