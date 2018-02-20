---
title: 'Procedura: Utilizzare l''IVA nelle vendite e negli acquisti | Documenti Microsoft'
description: "In questo argomento viene descritto come eseguire task quali la correzione di movimenti IVA già registrati. Nei paesi dell'Unione Europea ogni transazione di vendita e di acquisto è soggetta ai calcoli IVA. In questo argomento viene descritta la procedura."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, sales, purchases,
ms.date: 09/08/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 31b28811529cb4e5296a04c18f1f41d9f452a9be
ms.contentlocale: it-it
ms.lasthandoff: 01/30/2018

---
# <a name="work-with-vat-on-sales-and-purchases"></a>Utilizzare l'IVA nelle vendite e negli acquisti
Se il proprio paese o la propria area geografica richiede il calcolo dell'imposta sul valore aggiunto (IVA) nelle transazioni di vendita e di acquisto in modo da poter segnalare gli importi a un'autorità fiscale, è possibile impostare [!INCLUDE[d365fin](includes/d365fin_md.md)] affinché calcoli automaticamente l'IVA nei documenti di vendita e di acquisto. Per ulteriori informazioni, vedere [Impostazione dei calcoli e registrazione dei metodi per l'IVA] (finance-setup-vat.md).

Ci sono, tuttavia, alcuni task relativi all'IVA che è possibile eseguire manualmente. Ad esempio, potrebbe essere necessario correggere un importo già registrato se si scopre che un fornitore utilizza un metodo di arrotondamento diverso.

## <a name="calculating-and-displaying-vat-amounts-in-sales-and-purchase-documents"></a>Calcolo e visualizzazione degli importi IVA nei documenti di vendita e di acquisto  
È possibile calcolare e visualizzare gli importi IVA nei documenti di vendita e di acquisto in modo diverso, in base al tipo di cliente o di fornitore con cui si hanno relazioni commerciali. È inoltre possibile sovrascrivere l'importo IVA calcolato in modo che corrisponda all'importo IVA calcolato dal fornitore per una determinata transazione.  

### <a name="unit-price-and-line-amount-includingexcluding-vat-on-sales-documents"></a>Prezzo unitario e importo riga con IVA inclusa ed esclusa nei documenti di vendita  
Quando si sceglie un numero di articolo nel campo **Nr.** in un documento di vendita, [!INCLUDE[d365fin](includes/d365fin_md.md)] compila automaticamente il campo **Prezzo unitario**. Il prezzo unitario deriva dalla scheda **Articolo** o dai prezzi degli articoli definiti per l'articolo e il cliente. [!INCLUDE[d365fin](includes/d365fin_md.md)] calcola il valore del campo **Importo riga** quando si immette una quantità per la riga.  

Nei casi in cui si vende a clienti che si occupano di vendita al dettaglio, potrebbe essere necessario che i prezzi sui documenti di vendita siano comprensivi dell'IVA. A tale scopo, selezionare la casella di controllo **Prezzi IVA inclusa** nel documento.  

### <a name="including-or-excluding-vat-on-prices"></a>IVA inclusa o esclusa nei prezzi
Se la casella di controllo **Prezzi IVA inclusa** è selezionata in un documento di vendita, i campi **Prezzo unitario** e **Importo riga** includeranno l'IVA e questa impostazione sarà indicata anche nei nomi dei campi. Per impostazione predefinita, l'IVA non è inclusa in questi campi.  

Se questo campo non è selezionato, nei campi **Prezzo unitario** e **Importo riga** verranno inseriti importi IVA esclusa e questa impostazione sarà indicata nei nomi dei campi.  

È possibile impostare l'opzione **Prezzi IVA inclusa** come impostazione di default per tutti i documenti di vendita per un cliente nel campo **Prezzi IVA inclusa** della scheda **Cliente**. È inoltre possibile impostare i prezzi degli articoli affinché l'IVA sia inclusa o esclusa. In genere, i prezzi degli articoli nella scheda articolo sono IVA esclusa. Le informazioni del campo **Prezzo IVA inclusa** nella scheda **Articolo** vengono utilizzate per determinare il prezzo unitario per i documenti di vendita.  

Nella tabella seguente viene fornita una panoramica del metodo utilizzato dal programma per calcolare i prezzi unitari per i documenti di vendita quando non sono stati impostati prezzi nella finestra **Prezzi vendita**:  

|**Campo Prezzo IVA inclusa nella scheda articolo**|**Campo Prezzi IVA inclusa nella testata di vendita**|**Azione eseguita**|  
|-----------------------------------------------|----------------------------------------------------|--------------------------|  
|Deselezionato|Deselezionato|Il **Prezzo unitario** indicato nella scheda articolo viene copiato nel campo **Prezzo unitario IVA esclusa** nelle righe di vendita.|  
|Deselezionato|Selezionato|Viene calcolato l'importo IVA unitario, che viene aggiunto al valore del campo **Prezzo unitario** nella scheda articolo. Il prezzo unitario totale viene quindi immesso nel campo **Prezzo unitario IVA inclusa** nelle righe di vendita.|  
|Selezionato|Deselezionato|Viene calcolato l'importo IVA incluso in **Prezzo unitario** nella scheda articolo utilizzando la percentuale IVA relativa alla combinazione di Cat. reg. business IVA(prezzo) e di Cat. reg. art./serv. IVA. Il valore del campo **Prezzo unitario** nella scheda articolo, sottratto di IVA, viene immesso nel campo **Prezzo unitario IVA esclusa** delle righe di vendita.|  
|Selezionato|Selezionato|Il **Prezzo unitario** indicato nella scheda articolo viene copiato nel campo **Prezzo unitario IVA inclusa** nelle righe di vendita.|

## <a name="correcting-vat-amounts-manually-in-sales-and-purchase-documents"></a>Correzione manuale degli importi IVA nei documenti di vendita e di acquisto  
È possibile apportare delle correzioni a movimenti IVA registrati. In questo modo, è possibile modificare gli importi IVA vendite o acquisti totali senza modificare l'imponibile IVA. Questo tipo di rettifica può rendersi necessario, ad esempio, se in una fattura ricevuta da un fornitore l'IVA è stata calcolata erroneamente.  

Anche se è possibile impostare una o più combinazioni per gestire l'IVA da importazione, è necessario impostare almeno una categoria di registrazione articoli/servizi IVA. Ad esempio, è possibile denominarlo **RETTIFICA** ai fini della rettifica, a meno che non sia possibile utilizzare lo stesso conto di contabilità generale nel campo **Conto IVA acquisti** nella riga di impostazione delle registrazioni IVA. Per ulteriori informazioni, vedere [Impostazione dei calcoli e registrazione dei metodi per l'IVA](finance-setup-vat.md).

Se è stato calcolato uno sconto sul pagamento sulla base dell'importo di una fattura che include l'IVA, è possibile stornare la parte di sconto sul pagamento dell'importo IVA quando viene concesso lo sconto. È necessario attivare il campo **Rett. per sconto pagam.** sia nel setup della contabilità generale che nel setup delle registrazioni IVA per combinazioni specifiche di una categoria di registrazione business IVA e una categoria di registrazione articoli/servizi IVA.  

#### <a name="to-manually-enter-vat-in-sales-documents"></a>Per immettere manualmente l'IVA nei documenti di vendita  
1. Nella pagina **Setup contabilità generale** specificare un valore per **Max. differenza IVA permessa** tra l'importo calcolato dal programma e quello immesso manualmente.  
2. Nella pagina **Setup contabilità clienti e vendite** inserire un segno di spunta nel campo **Permetti differenze IVA**.  

#### <a name="to-adjust-vat-for-a-sales-document"></a>Per rettificare l'IVA per un documento di vendita  
1. Aprire l'ordine di vendita appropriato.  
2. Scegliere l'azione **Statistiche**.  
3. Scegliere la Scheda dettaglio **Fatturazione**.  
  
    > [!NOTE]  
    >  L'importo totale per la fattura, raggruppato in base al codice IVA, viene visualizzato nelle righe. È possibile rettificare manualmente l'importo nel campo **Importo IVA** nelle righe per ogni codice IVA. Quando si modifica il campo **Importo IVA** viene effettuato un controllo per verificare che l'IVA non sia stata modificata di un importo superiore a quello specificato come massima differenza consentita. Se l'importo è superiore a quello specificato nel campo **Max. differenza IVA permessa**, viene visualizzato un avviso che indica la massima differenza consentita. Per continuare, è necessario rettificare l'importo in modo che rientri nei parametri accettabili. Fare clic su **OK** e immettere un diverso **Importo IVA** che rientri nell'intervallo consentito. Se la differenza nell'IVA è uguale o inferiore a quella massima consentita, l'IVA verrà divisa proporzionalmente tra le righe del documento con lo stesso codice IVA.  

## <a name="calculating-vat-manually-using-journals"></a>Calcolo manuale dell'IVA utilizzando le registrazioni  
È anche possibile rettificare gli importi IVA nelle registrazioni COGE, vendite e acquisti. Ad esempio, questa operazione potrebbe essere necessaria quando si immette una fattura del fornitore nelle registrazioni e vi è una differenza tra l'importo IVA calcolato da [!INCLUDE[d365fin](includes/d365fin_md.md)] e quello specificato nella fattura del fornitore.  

#### <a name="before-you-manually-enter-vat-on-a-general-journal"></a>Prima di immettere manualmente l'IVA in una registrazione COGE  
1. Nella pagina **Setup contabilità generale** specificare un valore per **Max. differenza IVA permessa** tra l'importo calcolato dal programma e quello immesso manualmente.  
2. Nella pagina **Def. registrazioni COGE** selezionare la casella di controllo **Permetti differenze IVA** per le registrazioni pertinenti.  

#### <a name="before-you-manually-enter-vat-on-sales-and-purchase-journals"></a>Prima di immettere manualmente l'IVA nelle registrazioni vendite e acquisti  
1. Nella pagina **Setup contabilità fornitori e acquisti** selezionare la casella di controllo **Permetti differenze IVA**.  
2. Una volta completata l'impostazione descritta sopra, è possibile rettificare il campo **Importo IVA** nella riga di registrazioni COGE o il campo **Imp. IVA controp.** nelle righe di registrazioni vendite o acquisti. [!INCLUDE[d365fin](includes/d365fin_md.md)] verificherà che la differenza non sia maggiore dell'importo massimo specificato.  
  
    > [!NOTE]  
    > Se la differenza è maggiore, verrà visualizzato un avviso che indica la massima differenza consentita. Per continuare, è necessario rettificare l'importo. Scegliere **OK** e immettere un importo che rientri nell'intervallo consentito. Se la differenza nell'IVA è uguale o minore di quella massima consentita, [!INCLUDE[d365fin](includes/d365fin_md.md)] mostrerà la differenza nel campo **Differenza IVA**.  

## <a name="to-post-import-vat-with-purchase-invoices"></a>Per registrare l'IVA da importazione con le fatture di acquisto
Anziché utilizzare le registrazioni COGE per registrare una fattura con IVA da importazione, è possibile utilizzare una fattura di acquisto.  

### <a name="to-set-up-purchasing-for-posting-import-vat-invoices"></a>Per impostare l'acquisto per registrare le fatture con IVA da importazione  
1. Impostare una scheda fornitore per l'autorità di importazione che invia la fattura con IVA da importazione. I campi **Cat. reg. business** e **Cat. reg. business IVA** devono essere impostati in modo analogo al conto C/G per l'IVA da importazione.  
2. Creare una categoria **Cat. reg. articoli/servizi** per l'IVA da importazione e impostare una categoria **Cat. reg. art. serv. IVA default** relativa all'IVA da importazione per la categoria correlata creata in **Cat. reg. articoli/servizi**.  
3. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Piano dei conti**, quindi scegliere il collegamento correlato.  
4. Selezionare il conto C/G per l'IVA da importazione e nel gruppo **Gestione** della scheda **Pagina iniziale** scegliere **Modifica**.  
5. Nella Scheda dettaglio **Registrazione** selezionare il setup **Cat. reg. articolo/servizio** per l'IVA da importazione. In [!INCLUDE[d365fin](includes/d365fin_md.md)] il campo **Cat. reg. art./serv. IVA** viene compilato automaticamente.  
6. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Setup registrazioni COGE**, quindi selezionare il collegamento correlato.  
7. Creare una combinazione tra la **Cat. reg. business** per l'autorità competente sull'IVA e la **Cat. reg. articolo/servizio** per l'IVA da importazione. Per questa nuova combinazione, nel campo **Conto acquisti** scegliere il conto di contabilità generale per l'IVA da importazione.  

### <a name="to-create-a-new-invoice-for-the-import-authority-vendor-once-you-have-completed-the-setup"></a>Per creare una nuova fattura per il fornitore dell'importazione competente dopo avere completato il setup  
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Fatture di acquisto**, quindi scegliere il collegamento correlato.  
2. Creare una nuova fattura di acquisto.  
3. Nel campo **Acquistare da - Nr. for.** scegliere il fornitore dell'importazione competente, quindi scegliere il pulsante **OK**.  
4. Nel campo **Tipo** della riga di acquisto scegliere **Conto CG** e nel campo **Nr.** scegliere il conto di contabilità generale per l'IVA da importazione.  
5. Nel campo **Quantità** digitare **1**.  
6. Nel campo **Costo unitario diretto IVA escl.** specificare l'importo IVA.  
7. Contabilizzare la fattura.  

## <a name="to-process-certificates-of-supply"></a>Per elaborare i certificati di fornitura
Quando si vendono merci a un cliente in un altro paese UE, è necessario inviare il cliente un certificato di fornitura che il cliente deve firmare e restituire all'utente. Le procedure riportate di seguito sono utili a elaborare i certificati di fornitura per le spedizioni vendita, ma gli stessi passaggi sono applicabili anche per le spedizioni di assistenza per gli articoli e per le spedizioni di reso ai fornitori.  

### <a name="to-view-certificate-of-supply-details"></a>Per visualizzare i dettagli del certificato di fornitura  
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Spedizioni vendite reg.**, quindi scegliere il collegamento correlato.  
2. Selezionare la spedizione vendita appropriata a un cliente in un altro paese UE.  
3. Scegliere **Dettagli certificato di fornitura**.  
4. Per impostazione predefinita, se è selezionata la casella di controllo **Certificato di fornitura obbligatorio** per l'impostazione della categoria di registrazione IVA per il cliente, il campo **Stato** è impostato su **Obbligatorio**. È possibile aggiornare il campo per specificare se il cliente ha restituito il certificato.  

    > [!Note]  
    >  Se l'impostazione della categoria di registrazione IVA non ha la casella di controllo **Certificato di fornitura richiesto** selezionata, viene creato un record e il campo **Stato** è impostato su **Non applicabile**. È possibile aggiornare il campo per riflettere le corrette informazioni relative allo stato. È possibile modificare manualmente lo stato da **Non applicabile** a **Obbligatorio** e da **Obbligatorio** a **Non applicabile** in base alle esigenze.  

   Quando si aggiorna il campo **Stato** su **Obbligatorio**, **Ricevuto** o **Non ricevuto**, viene creato un certificato.  
  
    > [!TIP]  
    >  È possibile utilizzare la finestra **Certificati di fornitura** per visualizzare lo stato di tutte le spedizioni registrate per le quali un certificato di fornitura è stato creato.  

5. Scegliere **Stampa certificato di fornitura**.  
  
    > [!Note]  
    >  È possibile visualizzare in anteprima o stampare il documento. Scegliendo **Stampa certificato di fornitura** e si stampa il documento, la casella di controllo **Stampato** viene selezionata. Inoltre, se non è già specificato, lo stato del certificato viene aggiornato a **Obbligatorio**. Se necessario, includere il certificato stampato con la spedizione.  

### <a name="to-print-a-certificate-of-supply"></a>Per stampare un certificato di fornitura  
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Spedizioni vendite reg.**, quindi scegliere il collegamento correlato.  
2. Selezionare la spedizione vendita appropriata a un cliente in un altro paese UE.  
3. Scegliere l'azione **Stampa certificato di fornitura**.  

    > [!NOTE]  
    >  In alternativa, è possibile stampare un certificato dalla pagina **Certificato di fornitura**.  

4. Per includere le informazioni dalle righe presenti nel documento di spedizione nel certificato, selezionare la casella di controllo **Stampa dettagli riga**.  
5. Selezionare la casella di controllo **Crea certificati di fornitura se non ancora creati** per fare in modo che [!INCLUDE[d365fin](includes/d365fin_md.md)] crei certificati per le spedizioni registrate che non ne hanno uno al momento dell'esecuzione. Quando si seleziona la casella di controllo, vengono creati nuovi certificati per tutte le spedizioni registrate che non hanno certificati nell'intervallo selezionato.  
6. Per impostazione predefinita, le impostazioni del filtro sono per il documento di spedizione selezionato. Immettere le informazioni di filtro per selezionare un certificato specifico di fornitura da stampare.  
7. Nella pagina **Certificato di fornitura**, scegliere l'azione **Stampa** per stampare il report o scegliere l'azione **Anteprima** per visualizzarlo.  

    > [!Note]  
    > I campi **Certificato con stato di fornitura** e **Stampato** vengono aggiornati per la spedizione nella pagina **Certificati di fornitura**.  

8. Inviare il certificato di fornitura stampato al cliente per la firma.  

### <a name="to-update-the-status-of-a-certificate-of-supply-for-a-shipment"></a>Per aggiornare lo stato di un certificato di fornitura per una spedizione  
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Spedizioni vendite reg.**, quindi scegliere il collegamento correlato.  
2. Selezionare la spedizione vendita appropriata a un cliente in un altro paese UE.  
3. Nel campo **Stato** scegliere l'opzione pertinente.  

   Se il cliente restituisce il certificato di fornitura firmato, scegliere **Ricevuto**. Il campo **Data carico** viene aggiornato. Per impostazione predefinita, la data di carico è impostata come la data programma corrente.  

   È possibile modificare la data per indicare la data in cui è stato ricevuto il certificato di fornitura firmato dal cliente. È inoltre possibile aggiungere un collegamento al certificato firmato utilizzando la funzione standard di collegamento di [!INCLUDE[d365fin](includes/d365fin_md.md)].  

   Se il cliente non restituisce il certificato di fornitura firmato, scegliere **Non ricevuto**. È quindi necessario inviare al cliente una nuova fattura inclusiva di IVA, in quanto la fattura originale non verrà accettata dall'autorità fiscale.  

Per visualizzare un gruppo di certificati, si inizia dalla finestra **Certificati di fornitura** e quindi si aggiornano le informazioni relative allo stato dei certificati in sospeso appena vengono ricevuti dai clienti. Questo può risultare utile quando si desidera individuare tutti i certificati con un determinato stato, ad esempio, **Obbligatorio**, per i quali si desidera aggiornare lo stato a **Non ricevuto**.  

### <a name="to-update-the-status-of-a-group-of-certificates-of-supply"></a>Per aggiornare lo stato di un gruppo di certificati di fornitura.  
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Certificati di fornitura**, quindi scegliere il collegamento correlato.  
2. Filtrare il campo **Stato** secondo il valore che si desidera per creare l'elenco dei certificati che si desidera gestire.  
3. Per aggiornare le informazioni sullo stato, scegliere **Modifica lista**.  
4. Nel campo **Stato** scegliere l'opzione pertinente.  

   Se il cliente restituisce il certificato di fornitura firmato, scegliere **Ricevuto**. Il campo **Data carico** viene aggiornato. Per impostazione predefinita, la data di carico è impostata come la data programma corrente.  

   È possibile modificare la data per indicare la data in cui è stato ricevuto il certificato di fornitura firmato. È inoltre possibile aggiungere un collegamento al certificato firmato utilizzando la funzione standard di collegamento dei documenti di [!INCLUDE[d365fin](includes/d365fin_md.md)].  

    > [!NOTE]  
    >  Non è possibile creare un nuovo certificato di fornitura nella finestra **Certificato di fornitura** quando si arriva alla stessa utilizzando questa procedura. Per creare un certificato per una spedizione che non è stata impostata per richiederne uno, aprire la spedizione vendita registrata e utilizzare una delle due procedure descritte in precedenza:  
    >   
    > * Per creare manualmente un certificato di fornitura  
    > * Per stampare un certificato di fornitura.

## <a name="see-also"></a>Vedi anche  
[Impostazione dei calcoli e registrazione dei metodi per l'IVA](finance-setup-vat.md)   
[Procedura: Dichiarare l'IVA a un'autorità fiscale](finance-how-report-vat.md)   

