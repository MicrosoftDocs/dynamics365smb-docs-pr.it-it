---
title: Come utilizzare l'IVA nelle vendite e negli acquisti
description: 'Questo argomento descrive i vari modi di lavorare con l''IVA sia manualmente che con l''impostazione automatica, per aiutarti a soddisfare le normative specifiche del paese/area geografica.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'VAT, sales, purchases'
ms.search.form: '7, 118, 130, 142, 459, 460, 525'
ms.date: 06/16/2021
ms.author: bholtorf
---
# Usare l'IVA nelle vendite e negli acquisti

Se il tuo paese o area geografica richiede di calcolare e dichiarare l'imposta sul valore aggiunto (IVA) sulle transazioni di vendita e acquisto, puoi impostare [!INCLUDE[prod_short](includes/prod_short.md)] per calcolare l'IVA. Per ulteriori informazioni, vedere [Impostazione dei calcoli e registrazione dei metodi per l'IVA](finance-setup-vat.md).

Ci sono, tuttavia, alcuni task relativi all'IVA che è possibile eseguire manualmente. Ad esempio, potrebbe essere necessario correggere un importo già registrato se si scopre che un fornitore utilizza un metodo di arrotondamento diverso.  

> [!TIP]
> È possibile consentire a [!INCLUDE[prod_short](includes/prod_short.md)] di convalidare i numeri di partita IVA e altre informazioni sulla società durante la creazione o l'aggiornamento dei documenti. Per ulteriori informazioni, vedere [Convalidare i numeri di partita IVA](finance-how-validate-vat-registration-number.md).

## Calcolo e visualizzazione degli importi IVA nei documenti di vendita e di acquisto  

Quando si sceglie un numero di articolo nel campo **Nr.** su un documento di vendita o di acquisto, [!INCLUDE[prod_short](includes/prod_short.md)] compila i campi **Prezzo unitario** e **Importo riga**. Il prezzo unitario deriva dalla scheda **Articolo** o dai prezzi degli articoli definiti per l'articolo e il cliente. [!INCLUDE[prod_short](includes/prod_short.md)] calcola il valore l'importo riga quando immetti una quantità per la riga.  

Se desideri che i prezzi unitari e gli importi delle righe comprendano l'IVA, ad esempio, se vendi a consumatori al dettaglio, scegli la casella di controllo **Prezzi IVA inclusa** sul documento. Per ulteriori informazioni, vedi [IVA inclusa o esclusa nei prezzi e negli importi di riga](#including-or-excluding-vat-in-prices-and-line-amounts). 

Puoi calcolare e visualizzare gli importi IVA nei documenti di vendita e di acquisto in modo diverso, in base al tipo di cliente o di fornitore con cui hai relazioni commerciali. È inoltre possibile modificare l'importo IVA manualmente, ad esempio in modo che corrisponda all'importo IVA calcolato dal fornitore per una determinata transazione.

### IVA inclusa e IVA esclusa in prezzi e importi riga

Se la casella di controllo **Prezzi IVA inclusa** è selezionata in un documento di vendita, i campi **Prezzo unitario** e **Importo riga** includono l'IVA e questa impostazione è indicata anche nei nomi dei campi. Per impostazione predefinita, l'IVA non è inclusa nei valori di questi campi. I nomi dei campi indicano se i prezzi sono comprensivi di IVA.  

È possibile impostare l'opzione **Prezzi IVA inclusa** come impostazione di default per tutti i documenti di vendita per un cliente nel campo **Prezzi IVA inclusa** della scheda **Cliente**. È inoltre possibile impostare i prezzi degli articoli affinché l'IVA sia inclusa o esclusa. In genere, i prezzi sulla scheda articolo si intendono IVA esclusa. 

Nella tabella seguente viene fornita una panoramica del metodo utilizzato dall'applicazione per calcolare i prezzi unitari per i documenti di vendita quando non sono stati impostati prezzi nella pagina **Prezzi vendita**:  

|**Campo Prezzo IVA inclusa nella scheda articolo**|**Campo Prezzi IVA inclusa**|**Azione eseguita**|  
|-----------------------------------------------|----------------------------------------------------|--------------------------|  
|Non abilitato|Non abilitato|Il **Prezzo unitario** indicato nella scheda articolo viene copiato nel campo **Prezzo unitario IVA esclusa** nelle righe di vendita.|  
|Non abilitato|Abilitato|Viene calcolato l'importo IVA unitario, che viene aggiunto al valore del campo **Prezzo unitario** nella scheda articolo. Il prezzo unitario totale viene quindi immesso nel campo **Prezzo unitario IVA inclusa** nelle righe di vendita.|  
|Abilitato|Non abilitato|Viene calcolato l'importo IVA incluso nel campo **Prezzo unitario** nella **scheda articolo** utilizzando la percentuale IVA relativa alla combinazione di Cat. reg. business IVA (prezzo) e di Cat. reg. art./serv. IVA. Il valore del campo **Prezzo unitario** nella scheda articolo, sottratto di IVA, viene immesso nel campo **Prezzo unitario IVA esclusa** delle righe di vendita. Per ulteriori informazioni, vedi [Utilizzo delle categorie registrazione business IVA e dei gruppi prezzi cliente](finance-work-with-vat.md#using-vat-business-posting-groups-and-customer-price-groups).|  
|Abilitato|Abilitato|Il **Prezzo unitario** indicato nella scheda articolo viene copiato nel campo **Prezzo unitario IVA inclusa** nelle righe di vendita.|

#### Utilizzo delle categorie registrazione business IVA e dei gruppi prezzi cliente 

Se vuoi che i prezzi includano l'IVA, puoi utilizzare le categorie registrazione business IVA per calcolare l'importo in base all'impostazione di registrazione IVA per la categoria. Per ulteriori informazioni, vedi [Impostare le categorie registrazione business IVA](finance-setup-vat.md#set-up-vat-business-posting-groups).

A seconda di ciò che vuoi fare, puoi assegnare una categoria registrazione business IVA a clienti o documenti di vendita nei seguenti modi:

* Per utilizzare la stessa aliquota IVA per tutti i clienti, puoi scegliere un gruppo nel campo **Cat. reg. business IVA (prezzo)** della pagina **Setup contabilità clienti**.
* Per utilizzare un'aliquota IVA per un cliente specifico, puoi scegliere un gruppo nel campo **Cat. reg. business IVA (prezzo)** della pagina **Scheda cliente**. 
* Per utilizzare un'aliquota IVA per clienti specifici, puoi scegliere un gruppo nel campo **Cat. reg. business IVA (prezzo)** della pagina **Gruppo prezzi cliente**. Ad esempio, ciò è utile quando vuoi applicare un prezzo a tutti i clienti in una determinata area geografica o in un settore specifico.
* Su tutti i documenti di vendita nel campo **Cat. reg. business IVA**. L'importo IVA specificato per il gruppo viene utilizzato solo per il documento su cui stai attualmente lavorando.

> [!NOTE]
> Se non specifichi un gruppo nel campo **Cat. reg. business IVA (prezzo)** l'IVA non sarà inclusa nei prezzi.

#### Esempi

Fattori come il paese o l'area geografica in cui vendi o il tipo di settore a cui vendi possono influire sull'importo dell'IVA che devi contabilizzare. Ad esempio, un ristorante potrebbe addebitare il 6% di IVA per i pasti consumati in casa e il 17% per l'asporto. A tal fine, crei un gruppo di registrazione business IVA (prezzo) per il consumo in sede e uno per l'asporto.

## Utilizzo della Data IVA

### Data IVA nei documenti

Quando crei nuovi documenti di vendita o acquisto, la **Data IVA** sarà basata sull'impostazione nel campo **Data IVA predefinita** sulla pagina **Setup contabilità generale**. Questo valore predefinito può essere uguale alla **Data di registrazione** o alla **Data del documento**. Se hai bisogno di una data IVA diversa, puoi modificare manualmente il valore nel campo **Data IVA**. Quando registri il documento, la **Data IVA** sarà riportata sul documento di registrazione e sulle voci IVA e C/G.

> [!NOTE]
> Se il campo **Data IVA** non è disponibile nei tuoi documenti o giornali di registrazione, significa che **Non utilizzare la funzionalità Data IVA** è selezionato per il campo **Utilizzo data IVA** nella pagina **Setup contabilità generale**.  

> [!IMPORTANT]
> Se configuri **Controllo periodo IVA** in **Setup contabilità generale** come **Blocca registrazione all'interno periodo di chiusura**, o **Blocca registrazione entro il periodo di chiusura e avvisa per il periodo di rilascio**, puoi registrare il documento o il giornale di registrazione solo se la data nel campo **Data IVA** non è in un periodo chiuso in **Periodi di dichiarazione IVA**. Anche se il periodo in **Periodi di dichiarazione IVA** è aperto, potresti ricevere un avviso in base allo **Stato dichiarazione IVA** e alla configurazione nel **Controllo periodo IVA**.

> [!IMPORTANT]
> È possibile impedire o consentire la registrazione della **Data IVA** per un intervallo di dati specifico, utilizzando i campi **Consenti registrazione da** e **Consenti registrazione in** in **Setup contabilità generale** e **Setup utente**.  

> [!NOTE]
> Se lasci la **Data IVA** vuota, [!INCLUDE [prod_short](includes/prod_short.md)] usa la configurazione predefinita della **Data IVA predefinita** in **Setup contabilità generale** come **Data IVA** nella transazione registrata.  

### Modifica della data IVA nei movimenti registrati

Se necessario, è possibile modificare i documenti registrati con data IVA. Per cambiare la data nel campo **Data IVA** per i documenti registrati segui questi passaggi:

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Movimenti IVA**, quindi scegli il collegamento correlato. 
2. Trova il movimento con la data IVA errata.  
3. Scegli l'azione **Modifica elenco** e immetti la data corretta nel campo **Data IVA**.  
4. Quando chiudi la pagina, la nuova data IVA cambia nei **Movimenti C/G** correlati e nel documento registrato.  

> [!NOTE]
> È possibile modificare il campo **Data IVA** in **Movimenti IVA** solo se la data corrente non corrisponde a un periodo dichiarazione IVA chiuso. Anche se il periodo nel campo **Periodi di dichiarazione IVA** è aperto, potresti ricevere un avviso in base allo **Stato dichiarazione IVA**.  

> [!NOTE]
> Se il tuo documento ha più di un **Movimento IVA**, devi solo modificare il valore nel campo **Data IVA** in un movimento relativo al documento. Per mantenere la coerenza dei movimenti, [!INCLUDE[prod_short](includes/prod_short.md)] modifica automaticamente la data IVA nei movimenti IVA relativi a questa transazione. [!INCLUDE [prod_short](includes/prod_short.md)] aggiornerà la **Data IVA** in altre tabelle (Movimenti C/G e documenti), ma solo in relazione a questa transazione.  

## Correzione manuale degli importi IVA nei documenti di vendita e di acquisto  

È possibile apportare correzioni a movimenti IVA registrati e modificare gli importi dell'IVA di acquisto e vendita senza modificare l'imponibile. Ad esempio, se ricevi una fattura da un fornitore con un importo IVA errato.  

Anche se è possibile impostare una o più combinazioni per gestire l'IVA da importazione, è necessario impostare almeno una categoria di registrazione articoli/servizi IVA. Ad esempio, è possibile denominarlo **RETTIFICA** ai fini della rettifica, a meno che non sia possibile utilizzare lo stesso conto di contabilità generale nel campo **Conto IVA acquisti** nella riga di impostazione delle registrazioni IVA. Per ulteriori informazioni, vedere [Impostazione dei calcoli e registrazione dei metodi per l'IVA](finance-setup-vat.md).

Se è stato calcolato uno sconto sul pagamento sulla base dell'importo di una fattura che include l'IVA, è possibile stornare la parte di sconto sul pagamento dell'importo IVA quando viene concesso lo sconto. È necessario attivare il campo **Rett. per sconto pagam.** sia nel setup della contabilità generale che nel setup delle registrazioni IVA per combinazioni specifiche di una categoria di registrazione business IVA e una categoria di registrazione articoli/servizi IVA.  

### Per impostare il sistema per il movimento IVA manuale nei documenti di vendita
Di seguito viene descritto come abilitare le modifiche manuali dell'IVA nei documenti di vendita. I passaggi sono simili nella pagina **Setup contabilità fornitori**.

1. Nella pagina **Setup contabilità generale** specificare un valore per **Max. differenza IVA permessa** tra l'importo calcolato dall'applicazione e quello immesso manualmente.  
2. Nella pagina **Setup contabilità clienti e vendite** inserire un segno di spunta nel campo **Permetti differenze IVA**.  

### Per rettificare l'IVA per un documento di vendita

1. Aprire l'ordine di vendita appropriato.  
2. Scegliere l'azione **Statistiche**.  
3. Nella Scheda dettaglio **Fatturazione**, scegliere il valore nel campo **Nr. righe di imposta**.
4. Modificare il campo **Importo IVA**.   

> [!NOTE]  
> L'importo totale per la fattura, raggruppato in base al codice IVA, viene visualizzato nelle righe. È possibile rettificare manualmente l'importo nel campo **Importo IVA** nelle righe per ogni codice IVA. Quando si modifica il campo **Importo IVA** viene effettuato un controllo per verificare che l'IVA non sia stata modificata di un importo superiore a quello specificato come massima differenza consentita. Se l'importo è superiore a quello specificato nel campo **Max. differenza IVA permessa**, viene visualizzato un avviso che indica la massima differenza consentita. Per continuare, è necessario rettificare l'importo in modo che rientri nei parametri accettabili. Fare clic su **OK** e immettere un diverso **Importo IVA** che rientri nell'intervallo consentito. Se la differenza nell'IVA è uguale o inferiore a quella massima consentita, l'IVA verrà divisa proporzionalmente tra le righe del documento con lo stesso codice IVA.  

## Calcolo manuale dell'IVA utilizzando le registrazioni  
È anche possibile rettificare gli importi IVA nelle registrazioni COGE, vendite e acquisti. Ad esempio, questa operazione potrebbe essere necessaria quando si immette una fattura del fornitore nelle registrazioni e vi è una differenza tra l'importo IVA calcolato da [!INCLUDE[prod_short](includes/prod_short.md)] e quello specificato nella fattura del fornitore.  

### Per impostare il sistema per il movimento IVA manuale in una registrazione COGE
È necessario eseguire i passaggi seguenti prima di inserire manualmente l'IVA in una registrazione COGE.  

1. Nella pagina **Setup contabilità generale** specificare un valore per **Max. differenza IVA permessa** tra l'importo calcolato dall'applicazione e quello immesso manualmente.  
2. Nella pagina **Def. registrazioni COGE** selezionare la casella di controllo **Permetti differenze IVA** per le registrazioni pertinenti.  

### Per impostare il sistema per il movimento IVA manuale in una registrazione COGE

È necessario eseguire i passaggi seguenti prima di inserire manualmente l'IVA in una registrazione acquisti o vendite.

1. Nella pagina **Setup contabilità fornitori e acquisti** selezionare la casella di controllo **Permetti differenze IVA**.  
2. Ripetere il passaggio 1 per la pagina **Setup contabilità clienti**.
3. Una volta completata l'impostazione descritta sopra, è possibile rettificare il campo **Importo IVA** nella riga di registrazioni COGE o il campo **Imp. IVA controp.** nelle righe di registrazioni vendite o acquisti. [!INCLUDE[prod_short](includes/prod_short.md)] verificherà che la differenza non sia maggiore dell'importo massimo specificato.  

> [!NOTE]  
> Se la differenza è maggiore, verrà visualizzato un avviso che indica la massima differenza consentita. Per continuare, è necessario rettificare l'importo. Scegliere **OK** e immettere un importo che rientri nell'intervallo consentito. Se la differenza nell'IVA è uguale o minore di quella massima consentita, [!INCLUDE[prod_short](includes/prod_short.md)] mostrerà la differenza nel campo **Differenza IVA**.  

## Registrare l'IVA da importazione con fatture di acquisto
Anziché utilizzare le registrazioni per registrare una fattura con IVA da importazione, è possibile utilizzare una fattura di acquisto.  

### Per impostare l'acquisto per registrare le fatture con IVA da importazione

1. Impostare una scheda fornitore per l'autorità di importazione che invia la fattura con IVA da importazione. I campi **Cat. reg. business** e **Cat. reg. business IVA** devono essere impostati in modo analogo al conto C/G per l'IVA da importazione.  
2. Creare una categoria **Cat. reg. articoli/servizi** per l'IVA da importazione e impostare una categoria **Cat. reg. art. serv. IVA default** relativa all'IVA da importazione per la categoria correlata creata in **Cat. reg. articoli/servizi**.  
3. Scegli l'icona a forma di ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Piano dei conti**, quindi scegli il collegamento correlato.  
4. Selezionare il conto di contabilità generale per l'IVA da importazione e scegliere l'azione **Modifica**.  
5. Nella Scheda dettaglio **Registrazione** selezionare il setup **Cat. reg. articolo/servizio** per l'IVA da importazione. In [!INCLUDE[prod_short](includes/prod_short.md)] il campo **Cat. reg. art./serv. IVA** viene compilato automaticamente.  
6. Scegli l'icona a forma di ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup registrazioni COGE**, quindi scegli il collegamento correlato.  
7. Creare una combinazione tra la **Cat. reg. business** per l'autorità competente sull'IVA e la **Cat. reg. articolo/servizio** per l'IVA da importazione. Per questa nuova combinazione, nel campo **Conto acquisti** scegliere il conto di contabilità generale per l'IVA da importazione.  

### Per creare una nuova fattura per il fornitore dell'importazione competente dopo avere completato il setup  

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Fatture di acquisto**, quindi scegli il collegamento correlato.  
2. Creare una nuova fattura di acquisto.  
3. Nel campo **Acquistare da - Nr. for.** scegliere il fornitore dell'importazione competente, quindi scegliere il pulsante **OK**.  
4. Nel campo **Tipo** della riga di acquisto scegliere **Conto CG** e nel campo **Nr.** scegliere il conto di contabilità generale per l'IVA da importazione.  
5. Nel campo **Quantità** digitare **1**.  
6. Nel campo **Costo unitario diretto IVA escl.** specificare l'importo IVA.  
7. Contabilizzare la fattura.  

## Elaborare certificati di fornitura

Quando si vendono merci a un cliente in un altro paese UE, è necessario inviare il cliente un certificato di fornitura che il cliente deve firmare e restituire all'utente. Le procedure riportate di seguito sono utili a elaborare i certificati di fornitura per le spedizioni vendita, ma gli stessi passaggi sono applicabili anche per le spedizioni di assistenza per gli articoli e per le spedizioni di reso ai fornitori.  

### Per visualizzare i dettagli del certificato di fornitura  
1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Spedizioni vendita registrate**, quindi scegli il collegamento correlato.  
2. Selezionare la spedizione vendita appropriata a un cliente in un altro paese UE.  
3. Scegliere **Dettagli certificato di fornitura**.  
4. Per impostazione predefinita, se è selezionata la casella di controllo **Certificato di fornitura obbligatorio** per l'impostazione della categoria di registrazione IVA per il cliente, il campo **Stato** è impostato su **Obbligatorio**. È possibile aggiornare il campo per specificare se il cliente ha restituito il certificato.  

> [!Note]  
>  Se l'impostazione della categoria di registrazione IVA non ha la casella di controllo **Certificato di fornitura richiesto** selezionata, viene creato un record e il campo **Stato** è impostato su **Non applicabile**. È possibile aggiornare il campo per riflettere le corrette informazioni relative allo stato. È possibile modificare manualmente lo stato da **Non applicabile** a **Obbligatorio** e da **Obbligatorio** a **Non applicabile** in base alle esigenze.  

   Quando si aggiorna il campo **Stato** su **Obbligatorio**, **Ricevuto** o **Non ricevuto**, viene creato un certificato.  

> [!TIP]  
>  È possibile utilizzare la pagina **Certificati di fornitura** per visualizzare lo stato di tutte le spedizioni registrate per le quali un certificato di fornitura è stato creato.  

5. Scegliere **Stampa certificato di fornitura**.  

> [!Note]  
>  È possibile visualizzare in anteprima o stampare il documento. Scegliendo **Stampa certificato di fornitura** e si stampa il documento, la casella di controllo **Stampato** viene selezionata. Inoltre, se non è già specificato, lo stato del certificato viene aggiornato a **Obbligatorio**. Se necessario, includere il certificato stampato con la spedizione.  

### Per stampare un certificato di fornitura

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Spedizioni vendita registrate**, quindi scegli il collegamento correlato.  
2. Selezionare la spedizione vendita appropriata a un cliente in un altro paese UE.  
3. Scegliere l'azione **Stampa certificato di fornitura**.  

> [!NOTE]  
>  In alternativa, è possibile stampare un certificato dalla pagina **Certificato di fornitura**.  

4. Per includere le informazioni dalle righe presenti nel documento di spedizione nel certificato, selezionare la casella di controllo **Stampa dettagli riga**.  
5. Selezionare la casella di controllo **Crea certificati di fornitura se non ancora creati** per fare in modo che [!INCLUDE[prod_short](includes/prod_short.md)] crei certificati per le spedizioni registrate che non ne hanno uno al momento dell'esecuzione. Quando si seleziona la casella di controllo, vengono creati nuovi certificati per tutte le spedizioni registrate che non hanno certificati nell'intervallo selezionato.  
6. Per impostazione predefinita, le impostazioni del filtro sono per il documento di spedizione selezionato. Immettere le informazioni di filtro per selezionare un certificato specifico di fornitura da stampare.  
7. Nella pagina **Certificato di fornitura**, scegliere l'azione **Stampa** per stampare il report o scegliere l'azione **Anteprima** per visualizzarlo.  

> [!Note]  
> I campi **Certificato con stato di fornitura** e **Stampato** vengono aggiornati per la spedizione nella pagina **Certificati di fornitura**.  

8. Inviare il certificato di fornitura stampato al cliente per la firma.  

### Per aggiornare lo stato di un certificato di fornitura per una spedizione  

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Spedizioni vendita registrate**, quindi scegli il collegamento correlato.  
2. Selezionare la spedizione vendita appropriata a un cliente in un altro paese UE.  
3. Nel campo **Stato** scegliere l'opzione pertinente.  

   Se il cliente restituisce il certificato di fornitura firmato, scegliere **Ricevuto**. Il campo **Data carico** viene aggiornato. Per impostazione predefinita, la data di carico è impostata come la data programma corrente.  

   È possibile modificare la data per indicare la data in cui è stato ricevuto il certificato di fornitura firmato dal cliente. È inoltre possibile aggiungere un collegamento al certificato firmato utilizzando la funzione standard di collegamento di [!INCLUDE[prod_short](includes/prod_short.md)].  

   Se il cliente non restituisce il certificato di fornitura firmato, scegliere **Non ricevuto**. È quindi necessario inviare al cliente una nuova fattura inclusiva di IVA, in quanto la fattura originale non verrà accettata dall'autorità fiscale.  

Per visualizzare un gruppo di certificati, si inizia dalla pagina **Certificati di fornitura** e quindi si aggiornano le informazioni relative allo stato dei certificati in sospeso appena vengono ricevuti dai clienti. Questo può risultare utile quando si desidera individuare tutti i certificati con un determinato stato, ad esempio, **Obbligatorio**, per i quali si desidera aggiornare lo stato a **Non ricevuto**.  

### Per aggiornare lo stato di un gruppo di certificati di fornitura.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Certificati di fornitura**, quindi scegli il collegamento correlato.  
2. Filtrare il campo **Stato** secondo il valore che si desidera per creare l'elenco dei certificati che si desidera gestire.  
3. Per aggiornare le informazioni sullo stato, scegliere **Modifica lista**.  
4. Nel campo **Stato** scegliere l'opzione pertinente.  

   Se il cliente restituisce il certificato di fornitura firmato, scegliere **Ricevuto**. Il campo **Data carico** viene aggiornato. Per impostazione predefinita, la data di carico è impostata come la data programma corrente.  

   È possibile modificare la data per indicare la data in cui è stato ricevuto il certificato di fornitura firmato. È inoltre possibile aggiungere un collegamento al certificato firmato utilizzando la funzione standard di collegamento dei documenti di [!INCLUDE[prod_short](includes/prod_short.md)].  

> [!NOTE]
> Non è possibile creare un nuovo certificato di fornitura nella pagina **Certificato di fornitura** quando si arriva alla stessa utilizzando questa procedura. Per creare un certificato per una spedizione che non è stata impostata per richiederne uno, aprire la spedizione vendita registrata e utilizzare una delle due procedure descritte in precedenza:  
>
> * Per creare manualmente un certificato di fornitura  
> * Per stampare un certificato di fornitura.

## Vedi il relativo [training Microsoft](/training/paths/process-vat-dynamics-365-business-central/)

## Vedi anche

[Impostazione dei calcoli e registrazione dei metodi per l'IVA](finance-setup-vat.md)  
[Dichiarare l'IVA a un'autorità fiscale](finance-how-report-vat.md)  
[Convalidare un numero di partita IVA](finance-how-validate-vat-registration-number.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
