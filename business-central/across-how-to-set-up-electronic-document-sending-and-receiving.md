---
title: Come impostare l'invio e la ricezione di documenti elettronici | Microsoft Docs
description: 'Come alternativa all''invio tramite e-mail come allegati di file, è possibile inviare e ricevere documenti aziendali elettronicamente.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: bholtorf
---
# Impostare l'invio e la ricezione di documenti elettronici

Come alternativa all'invio tramite e-mail come allegati di file, è possibile inviare e ricevere documenti aziendali elettronicamente. Per documento elettronico si intende un file conforme agli standard che rappresenta un documento aziendale, ad esempio la fattura di un fornitore che può essere ricevuta e convertita in fattura di acquisto in [!INCLUDE[prod_short](includes/prod_short.md)]. Lo scambio di documenti elettronici tra due partner commerciali viene eseguito da un provider esterno dei servizi di Exchange per documenti. La versione generica di [!INCLUDE[prod_short](includes/prod_short.md)] supporta l'invio e la ricezione delle fatture e delle note di credito elettroniche e la ricezione delle fatture elettroniche nel formato PEPPOL, che è supportato dai principali provider di servizi di Exchange per documenti. Un provider importante dei servizi di Exchange per documenti è preconfigurato e pronto per l'installazione nell'azienda.  

Dai PDF o dai file di immagine che rappresentano i documenti in entrata, è possibile impostare un servizio esterno OCR (Optical Character Recognition, riconoscimento ottico dei caratteri) in modo che crei documenti elettronici che è possibile convertire in record di documenti in [!INCLUDE[prod_short](includes/prod_short.md)], come per i documenti elettronici PEPPOL. Ad esempio, quando si riceve una fattura nel formato PDF dal fornitore, è possibile inviarla al servizio OCR dalla pagina **Documenti in entrata**. Dopo alcuni secondi, viene ricevuto il file come fattura elettronica che può essere convertita in una fattura di acquisto per il fornitore. Se si invia il file al servizio OCR tramite e-mail, un nuovo record del documento in entrata viene creato quando si riceve nuovamente il documento elettronico.  

Il formato di documento elettronico **PEPPOL** è preconfigurato per consentire l'invio di fatture e di note di credito elettroniche nel formato PEPPOL. Innanzitutto, è necessario impostare diversi dati principali, ad esempio le informazioni sulla società, i clienti, gli articoli e le unità di misura. Questi dati vengono utilizzati per identificare i partner commerciali e gli articoli durante la conversione dei dati nei campi di [!INCLUDE[prod_short](includes/prod_short.md)] in elementi nel file di documento in uscita. Infine, è necessario selezionare il formato nella pagina **Formato documento elettronico** per ogni cliente a cui verranno inviati i documenti PEPPOL elettronici. Per ulteriori informazioni, vedere [Inviare documenti elettronici](sales-how-to-send-electronic-documents.md).  

Le definizioni di scambio di dati **PEPPOL - Fattura** e **PEPPOL – Nota di credito** sono preconfigurate per consentire la ricezione di fatture e note di credito elettroniche nel formato PEPPOL. Innanzitutto, è necessario impostare diversi dati principali, come ad esempio le informazioni sulla società, i fornitori, gli articoli e le unità di misura. Questi dati vengono utilizzati per identificare i partner commerciali e gli articoli durante la conversione dei dati presenti negli elementi del file di documento in entrata nei campi di [!INCLUDE[prod_short](includes/prod_short.md)]. Infine, è necessario selezionare la definizione di scambio dati nella pagina **Documenti in entrata** per ogni documento elettronico in arrivo che si desidera convertire in un documento di acquisto in [!INCLUDE[prod_short](includes/prod_short.md)].  

La definizione di scambio dati **OCR - Fattura** è preconfigurata per permettere la ricezione dei documenti elettronici generati dal servizio OCR. Per ricevere, ad esempio, una fattura come documento elettronico OCR, si impostano i dati principali e si elabora il documento come quando si riceve un documento PEPPOL elettronico. Per ulteriori informazioni, vedere [Utilizzare OCR per convertire PDF e file di immagine in documenti elettronici](across-how-use-ocr-pdf-images-files.md).  

I servizi preconfigurati per lo scambio di documenti e OCR devono essere abilitati prima dell'invio o della ricezione. Per ulteriori informazioni, vedere [Impostare un servizio di scambio documenti](across-how-to-set-up-a-document-exchange-service.md).  

In questo argomento sono contenute le seguenti procedure:  

* Per impostare la società per l'invio e la ricezione di documenti elettronici  
* Per impostare la registrazione IVA per l'invio e la ricezione di documenti elettronici  
* Per impostare i paesi per l'invio e la ricezione di documenti elettronici  
* Per impostare gli articoli per l'invio e la ricezione di documenti elettronici  
* Per impostare le unità di misura per l'invio e la ricezione di documenti elettronici  
* Per impostare i clienti per l'invio di documenti elettronici  
* Per selezionare il formato di documento elettronico **PEPPOL** per l'invio di documenti elettronici  
* Per impostare i fornitori per la ricezione di documenti elettronici  
* Per selezionare la definizione di scambio di dati **PEPPOL - Fattura** per la ricezione di documenti elettronici  
* Per impostare il conto C/G da utilizzare in nuove righe della fattura di acquisto per gli articoli non identificabili e gli elementi che non sono articoli  

### Per impostare la società per l'invio e la ricezione di documenti elettronici

1. Nella casella **Cerca** immettere **Informazioni società**, quindi selezionare il collegamento correlato.  
2. Nella Scheda dettaglio **Generale** compilare i campi come descritto nella tabella seguente.  

    |Campo|Descrizione|  
    |---------------------------------|---------------------------------------|  
    |**GLN**|Identificare la società.<br /><br /> Ad esempio, quando si inviano fatture elettroniche nel formato PEPPOL, il valore in questo campo viene utilizzato per popolare l'elemento **EndPointID** nel nodo **AccountingSupplierParty** nel file. Il numero sarà basato sullo standard GS1, che è conforme allo standard ISO 6523.|  
    |**Partita IVA**|Specificare il numero di registrazione IVA della propria società.|  
    |**Centro di responsabilità**|Se la società è impostata con un centro di responsabilità, assicurarsi che il campo **Codice paese** sia compilato.|  

### Per impostare la registrazione IVA per l'invio e la ricezione di documenti elettronici

1. Nella casella **Cerca** immettere **Setup registrazioni IVA**, quindi selezionare il collegamento correlato.  
2. Per ogni riga di impostazione della registrazione VAT che verrà utilizzata per i documenti elettronici, compilare il campo come descritto nella tabella seguente.  

    |Campo|Descrizione|  
    |---------------------------------|---------------------------------------|  
    |**Categoria imposta**|Specificare la categoria IVA.<br /><br /> Ad esempio, quando si inviano fatture elettroniche nel formato PEPPOL, il valore in questo campo viene utilizzato per popolare l'elemento **TaxApplied** nel nodo **AccountingSupplierParty** nel file. Il numero sarà basato sullo standard UNCL5305.|  

### Per impostare i paesi per l'invio e la ricezione di documenti elettronici

1. Nella casella **Cerca** immettere **Paese**, quindi selezionare il collegamento correlato.  
2. Per ogni paese con cui verranno scambiati documenti elettronici, compilare il campo come descritto nella tabella seguente.  

    |Campo|Descrizione|  
    |---------------------------------|---------------------------------------|  
    |**Schema IVA**|Identificare l'ente nazionale che emette il numero di partita IVA per il paese\/area geografica interessato dall'invio dei documenti elettronici.<br /><br /> Ad esempio, quando si inviano fatture elettroniche nel formato PEPPOL, il valore in questo campo viene utilizzato per popolare l'attributo **SchemeID** dell'elemento **EndPointID** in entrambi i nodi **AccountingSupplierParty** e **AccountingCustomerParty** nel file.<br /><br /> Il campo **Schema IVA** viene utilizzato solo se il campo **GLN** nella pagina **Informazioni società** non è compilato. **Nota:** il valore nel campo **Codice** della pagina **Paesi\/Aree geografiche** deve essere conforme allo standard ISO 3166\-1:Alpha2.|  

### Per impostare gli articoli per l'invio e la ricezione di documenti elettronici

1. Nella casella **Cerca** immettere **Articoli**, quindi selezionare il collegamento correlato.  
2. Per ogni articolo che si acquista o si vende su documenti elettronici, compilare il campo come descritto nella tabella seguente.  

    |Campo|Descrizione|  
    |---------------------------------|---------------------------------------|  
    |**GTIN**|Identifica l'articolo in relazione all'invio e alla ricezione del documento elettronico. Per il formato PEPPOL, il campo viene utilizzato come segue:<br /><br /> Se l'elemento **StandardItemIdentification\/ID** dispone dell'attributo **SchemeID** impostato su **GTIN**, l'elemento viene mappato al campo **GTIN** nella scheda articolo.|  

### Per impostare le unità di misura per l'invio e la ricezione di documenti elettronici

1. Nella casella **Cerca** immettere **Unità di misura**, quindi selezionare il collegamento correlato.  
2. Per ogni unità di misura che verrà utilizzata per gli articoli sui documenti elettronici, compilare il campo come descritto nella tabella seguente.  

    |Campo|Descrizione|  
    |---------------------------------|---------------------------------------|  
    |**Codice standard internazionale**|Specificare il codice dell'unità di misura espresso secondo lo standard UNECERec20 in relazione all'invio di documenti elettronici.<br /><br /> Ad esempio, quando si inviano fatture elettroniche nel formato PEPPOL, il valore in questo campo viene utilizzato per popolare l'attributo **unitCode** dell'elemento **InvoicedQuantity** nel nodo **InvoiceLine**. **Nota:** se il campo **Unità di misura** nella riga di vendita è vuoto, viene inserito per impostazione predefinita il valore dello standard UNECERe20 per "Pezzo" \(H87\). Per ulteriori informazioni e un elenco dei codici unità di misura validi, vedere [Recommendation No. 20 \-  Units of Measure used in International Trade](https://www.unece.org/fileadmin/DAM/cefact/recommendations/rec20/rec20_rev3_Annex2e.pdf).|  

### Per impostare i clienti per l'invio di documenti elettronici

1. Nella casella **Cerca** immettere **Clienti**, quindi selezionare il collegamento correlato.  
2. Per ogni cliente a cui si invieranno documenti elettronici, compilare i campi come descritto nella tabella seguente.  

    |Campo|Descrizione|  
    |---------------------------------|---------------------------------------|  
    |**GLN**|Identificare il cliente.<br /><br /> Ad esempio, quando si inviano fatture elettroniche nel formato PEPPOL, il valore in questo campo viene utilizzato per popolare l'elemento **EndPointID** nel nodo **AccountingCustomerParty** nel file. Il numero sarà basato sullo standard GS1, che è conforme allo standard ISO 6523.<br /><br /> Se il campo **GLN** è vuoto, viene usato il valore del campo **Partita IVA**.|  
    |**Partita IVA**|Specificare il numero di partita IVA del cliente. **Suggerimento:** nelle versioni localizzate supportate, selezionare il pulsante Drilldown per utilizzare il servizio Web che consente di verificare l'esistenza del numero nel registro delle imprese del paese.|  
    |**Centro di responsabilità**|Se il cliente è impostato con un centro di responsabilità, assicurarsi che il campo **Codice paese** sia compilato.|  

    È possibile impostare ogni cliente con un metodo di invio documenti commerciali preferito, in modo da non dover selezionare un'opzione di invio ogni volta che è necessario inviare un documento al cliente. Per ulteriori informazioni, vedere [Impostare profili di invio documenti](sales-how-setup-document-send-profiles.md).  

### Per selezionare il formato di documento elettronico PEPPOL per l'invio di documenti elettronici  
1. Nella casella **Cerca** immettere **Profili di invio documenti**, quindi selezionare il collegamento correlato.  
2. Aprire un profilo di invio di documento esistente oppure crearne uno nuovo. Per ulteriori informazioni, vedere [Impostare profili di invio documenti](sales-how-setup-document-send-profiles.md).  
3. Nella pagina **Profilo di invio documenti** scegliere il **Formato elettronico**, selezionare la riga per PEPPOL e quindi scegliere **OK**.  
4. Nel campo **Documento elettronico** selezionare **Sì (Tramite il servizio di scambio documenti)**.  

    > [!NOTE]  
    >  In [!INCLUDE[prod_short](includes/prod_short.md)] viene automaticamente rilevato se il documento è una fattura o una nota di credito e viene applicato il formato PEPPOL di conseguenza.  

5. Per applicare questo profilo di invio del documento a tutti i clienti, selezionare la casella di controllo **Default** nella Scheda dettaglio **Generale**. Per applicarlo solo a clienti specifici, compilare il campo **Profilo di invio documenti** nelle schede cliente interessate. Per ulteriori informazioni, vedere [Impostare profili di invio documenti](sales-how-setup-document-send-profiles.md).  

    A questo punto è possibile inviare il documento elettronico con i dati convertiti. Per ulteriori informazioni, vedere [Inviare documenti elettronici](sales-how-to-send-electronic-documents.md).  

### Per impostare i fornitori per la ricezione di documenti elettronici  
1. Nella casella **Cerca** immettere **Fornitori**, quindi selezionare il collegamento correlato.  
2. Per ogni fornitore da cui si riceveranno documenti elettronici, compilare i campi come descritto nella tabella seguente.  

    |Campo|Descrizione|  
    |---------------------------------|---------------------------------------|  
    |**GLN**|Identificare il fornitore.<br /><br /> Ad esempio, quando si ricevono fatture elettroniche nel formato PEPPOL, il valore in questo campo viene utilizzato per popolare l'elemento **EndPointID** nel nodo **AccountingSupplierParty** nel file. Il numero sarà basato sullo standard GS1, che è conforme allo standard ISO 6523.<br /><br /> Se il campo **GLN** è vuoto, viene usato il valore del campo **Partita IVA**.|  
    |**Partita IVA**|Specificare il numero di partita IVA del fornitore. **Suggerimento:** nelle versioni localizzate supportate, selezionare il pulsante Drilldown per utilizzare il servizio Web che consente di verificare l'esistenza del numero nel registro delle imprese del paese.|  
    |**Centro di responsabilità**|Se il fornitore è impostato con un centro di responsabilità, assicurarsi che il campo **Codice paese** sia compilato.|  

### Per selezionare la definizione di scambio di dati PEPPOL - Fattura per la ricezione di documenti elettronici  
1. Nella casella **Cerca** immettere **Documenti in arrivo**, quindi selezionare il collegamento correlato.  
2. Nella riga del documento elettronico che si desidera ricevere e convertire, scegliere il campo **Tipo scambio dati** e quindi selezionare **PEPPOLINVOICE**.  

     Se il documento da ricevere è una nota di credito, selezionare **PEPPOLCREDITMEMO**.  

    A questo punto è possibile ricevere il documento elettronico iniziando il processo di conversione dei dati nella pagina **Documenti in entrata**. Per ulteriori informazioni, vedere [Ricevere e convertire documenti elettronici](purchasing-how-to-receive-and-convert-electronic-documents.md).  

### Per impostare il conto C/G da utilizzare in nuove righe della fattura di acquisto per gli articoli non identificabili e gli elementi che non sono articoli  
1. Nella casella **Cerca** immettere **Setup contabilità fornitori e acquisti**, quindi selezionare il collegamento correlato.  
2. Nella Scheda dettaglio **Conti di default** compilare il campo come descritto nella tabella seguente.  

    |Campo|Descrizione|  
    |---------------------------------|---------------------------------------|  
    |**Conto C/G per righe non articolo**|Specifica il conto C/G che viene inserito automaticamente nelle righe di acquisto create dai documenti elettronici quando la riga del documento in ingresso non contiene un articolo identificabile. Tutte le righe di documenti in entrata che non hanno un GTIN o il numero di articolo del fornitore verranno convertite in una riga di acquisto di tipo **Conto C/G** e il campo **Nr.** della riga di acquisto conterrà il conto selezionato nel campo **Conto C/G per righe non articolo**.<br /><br /> Se si lascia vuoto il campo **Conto C/G per righe non articolo** e il documento in entrata dispone di righe senza articoli identificabili, il documento di acquisto non verrà creato. Un messaggio di errore avviserà l'utente che è necessario compilare il campo **Conto C/G per righe non articolo** prima di poter completare il task.|  

## Vedi anche  
[Scambio di dati in modalità elettronica](across-data-exchange.md)   
[Fatturare le vendite](sales-how-invoice-sales.md)   
[Registrare gli acquisti](purchasing-how-record-purchases.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
