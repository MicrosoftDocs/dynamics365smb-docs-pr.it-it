---
title: IVA italiana
description: 'Nella versione italiana, l''IVA può essere dedotta se i beni o i servizi acquistati dall''azienda sono utilizzati nella produzione del suo reddito.'
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: null
ms.search.form: '12100, 12104, 12105, 12111, 12112, 12113, 12122, 12126, 12127, 12133, 12135, 12151, 12158, 12187, 12189, 12198, 12199, 12202'
ms.date: 06/18/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="italian-vat"></a>IVA italiana

Le società sono soggette al pagamento dell'IVA allo Stato per la maggior parte dei beni e dei servizi acquistati. L'IVA può essere detraibile se i beni o i servizi acquistati sono utilizzati nella produzione del reddito della società stessa.  

 In [!INCLUDE[prod_short](../../includes/prod_short.md)], è possibile definire i report periodici IVA nella pagina **Report IVA**. È possibile compilare le righe in base ai movimenti IVA, quindi esportare il report IVA alle autorità competenti.  

## <a name="vat-codes-and-rates"></a>Codici e aliquote IVA

I codici e le aliquote IVA devono essere impostati anche se alcune transazioni non sono soggette a IVA. Esistono inoltre molte operazioni soggette a IVA per cui è prevista un'aliquota zero per legge.  

Il codice IVA correlato viene stampato per ogni riga fattura. Le fatture per i movimenti transazioni IVA esenti da IVA devono essere registrate e stampate con una nota che indica che l'IVA non è dovuta.  

### <a name="computing-vat"></a>Elaborazione dell'IVA

L'IVA per le transazioni viene elaborata in conformità con le normative in vigore nel giorno in cui hanno luogo le transazioni. È quindi necessario tenere traccia della data di esecuzione legale delle transazioni durante la registrazione delle transazioni.  

### <a name="dates"></a>Date

La data d'emissione è la data del documento e la data di registrazione è la data di registrazione. I filtri dalla data reporting si basano sulle date di registrazione. Questo è cambiato dal comportamento precedente in cui i filtri per le date di segnalazione erano basati sulla data in cui è avvenuta l'operazione.  

### <a name="non-deductible-vat"></a>IVA non detraibile

Non è possibile detrarre l'IVA per alcuni acquisti per i seguenti motivi:  

- Tipologia di beni e servizi acquistati: l'IVA non è detraibile completamente o parzialmente per legge su beni quali automobili, telefoni cellulari, alimentari acquistati presso ristoranti e così via.  

- IVA proporzionale parzialmente detraibile: l'IVA viene ripartita proporzionalmente tra le operazioni di vendita soggette a IVA e tutte le operazioni eseguite. L'IVA eccedente questo rapporto non può essere detratta.  

## <a name="service-tariffs"></a>Nomenclatura articoli in assistenza

L'Unione Europea (UE) ha emesso le direttive che cambiano la dichiarazione dell'IVA per il commercio transfrontaliere di beni o servizi nell'Unione Europea.  

In Italia, i report elenco vendite UE (Intrastat) ed elenco annuale vengono aggiornati per includere i servizi. Ciò include una modifica nel formato di dichiarazione. Una nuova tabella per la nomenclatura articoli in assistenza è stata aggiunta in modo da consentire alle società di classificare i servizi che devono essere inclusi nel report INTRASTAT. Gli utenti devono aggiungere la nomenclatura di assistenza pertinente a tutti i documenti destinati alle transazioni transfrontaliere. La nomenclatura articoli in assistenza specificata nella Scheda dettaglio **Commercio estero** per il documento può essere modificato in ogni riga del documento.  

## <a name="vat-transaction-reports"></a>Report transazioni IVA

È necessario inviare periodicamente i report alle autorità fiscali per elencare le transazioni che includono l'IVA con importi superiori a una soglia specificata. I report transazioni IVA vengono creati in base alle transazioni con clienti o fornitori da un paese esterno all'UE e non incluso nell'elenco dei paesi bloccati delle autorità italiane. Le transazioni con clienti o fornitori dai paesi UE sono riportate nei report **Intrastat**. [!INCLUDE[prod_short](../../includes/prod_short.md)] fornisce il supporto per i seguenti tipi di transazione:  

|**Tipo di transazione**|**Supportata**|
|--------------------|-------------|  
|FE - Fatture cliente (fatture emesse)|Sì|  
|FR - Fatture fornitore (fatture ricevute)|Sì|  
|NE - Note di accredito cliente (note emesse)|Sì|  
|NR - Note di accredito fornitore (note ricevute)|Sì|  
|DF - Transazioni senza fatture (fatture dirette) (cliente)|No|  
|FN - Fatture cliente, quando il cliente non è residente|Sì|  
|SE - Fatture fornitore, quando il fornitore non è residente|Sì **Nota:** si presume l'acquisto dei servizi, ma la differenziazione tra beni e servizi deve essere implementata dall'utente.|  

 [!INCLUDE[prod_short](../../includes/prod_short.md)] non dichiara i seguenti tipi di transazioni:  

- Fatture pagamento anticipato, in quanto l'importo totale sarà riportato al momento della fattura finale.  

- Operazioni senza fattura, ad esempio, i movimenti IVA registrati nei conti di contabilità generale, perché un numero di partita IVA, un codice fiscale o un riferimento del cliente o del fornitore deve essere incluso nel report.  

- Le transazioni autofatturate, che non sono supportate.  

I report di transazioni IVA includono le righe in cui l'importo è oltre la soglia e le righe che devono essere incluse per altri motivi legali. L'importo di soglia viene impostato dalle autorità italiane.  

Le righe del documento contengono un campo per indicare se la riga deve essere inclusa nei report di transazione IVA. I campi **Includi in report transazioni IVA** vengono selezionati automaticamente in base al giorno della transazione e al confronto con l'importo di soglia dell'anno di calendario. Se le righe di vendita sono collegate a un ordine programmato, la soglia è confrontata con l'importo dell'ordine programmato. Questa opzione è valida solo per la riga di vendita di tipo **Articolo**. Per le righe di assistenza, il confronto viene eseguito con l'importo del contratto di assistenza.  

> [!NOTE]  
> Le note di credito vengono incluse nel report transazioni IVA se il cliente o il fornitore è di un paese esterno all'UE e non incluso nella lista come bloccato.  

Quando si registrano le note di credito, è necessario aggiornare il campo **Riferito a periodo** e specificare il periodo appropriato. I report di transazione IVA includono le note di credito in cui il campo **Riferito a periodo** è impostato su **Anno di calendario corrente** o **Anno di calendario precedente**.  

[!INCLUDE[prod_short](../../includes/prod_short.md)] aggiunto le note di credito ai report IVA in modi diversi a seconda dello stato dell'applicazione e del valore del campo **Riferito a periodo**. Nella seguente tabella vengono illustrate gli scenari.  

|Scenario|Impatto|  
|--------------|------------|  
|Una nota di credito è collegata a una singola fattura.<br /><br /> Il campo **Riferito a periodo** è impostato su **Anno di calendario corrente**.|Il campo **Nr. fattura** verrà impostato sul numero di documento della fattura.<br /><br /> Il campo **Data fattura** verrà impostato sulla data specificata nel campo **Data esecuzione operazione**<br /><br /> [!INCLUDE[prod_short](../../includes/prod_short.md)] sottrae l'importo della nota di credito dall'importo della fattura originale. Se l'importo risultante è oltre la soglia, sia la fattura che la nota di credito verranno incluse nel report di transazioni IVA. Se l'importo risultante è sotto la soglia, la fattura o la nota di credito non verranno incluse nel report di transazioni IVA.|  
|Una nota di credito è collegata a più fatture o non è collegata.<br /><br /> Il campo **Riferito a periodo** è impostato su **Anno di calendario corrente**.|Il campo **Data fattura** verrà impostato sull'ultimo giorno dell'anno specificato nel campo **Data esecuzione operazione**. Ad esempio, se il campo **Data esecuzione operazione** è **07-11-11**, il campo **Data fattura** verrà impostato su **31-12-11**.<br /><br /> Solo la nota di credito viene inclusa nel report di transazioni IVA.|  
|Una nota di credito è collegata a più fatture o non è collegata.<br /><br /> Il campo **Riferito a periodo** è impostato su **Anno di calendario precedente**.|Il campo **Data fattura** verrà impostato sull'ultimo giorno dell'anno prima della data specificata nel campo **Data esecuzione operazione**. Ad esempio, se il campo **Data esecuzione operazione** è **07-11-11**, il campo **Data fattura** verrà impostato su **31-12-10**.<br /><br /> Solo la nota di credito viene inclusa nel report di transazioni IVA.|  

Quando i contratti di assistenza sono confrontati con la soglia, il campo **Importo Annuo** viene convertito in valuta locale (VL). La conversione si basa sul campo **Codice valuta** e sul tasso di cambio alla data presente nel campo **Data inizio** per il contratto di assistenza.  

Le transazioni con IVA intracomunitaria non sono incluse nei report di transazione IVA. Le transazioni con pagamenti anticipati non sono incluse nei report di transazione IVA.  

Per prepararsi i dati per le dichiarazioni, è necessario impostare la registrazione IVA in modo da includere gli importi di dichiarazione della transazione IVA. Quando una transazione ad esempio la registrazione di una fattura di vendita viene eseguita utilizzando questo setup registrazioni IVA, [!INCLUDE[prod_short](../../includes/prod_short.md)] verifica se la transazione soddisfa gli importi di soglia. Il controllo è basato sulle righe del documento perché un documento può contenere le righe che devono essere incluse nel report transazione IVA e le righe che devono essere escluse. I report di transazione IVA devono contiene solo le righe che devono essere inviate, pertanto [!INCLUDE[prod_short](../../includes/prod_short.md)] confronta gli importi con la soglia per ogni riga anziché per un documento.  

È necessario inviare il report transazioni IVA elettronicamente alle autorità fiscali. Per ulteriori informazioni, vedere [Creare report elettronici di transazioni IVA](how-to-create-electronic-vat-transactions-reports.md).  

## <a name="see-also"></a>Vedere anche

[Impostare l'IVA](../../finance-setup-vat.md)  
[Dichiarare l'IVA](../../finance-how-report-vat.md)  
 [Preparare i report di transazioni IVA](how-to-prepare-for-vat-transactions-reports.md)  
 [Creare report elettronici di transazioni IVA](how-to-create-electronic-vat-transactions-reports.md)  
 [Inviare dichiarazioni IVA](how-to-submit-vat-statements.md)  
 [Aggiornare i dati delle transazioni IVA](how-to-update-vat-transactions-data.md)  
 [Funzionalità locale per l'Italia](italy-local-functionality.md)  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
