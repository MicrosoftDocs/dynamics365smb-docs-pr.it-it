---
title: Utilizzare OCR per convertire il PDF in fatture elettroniche
description: Descrive come è possibile utilizzare un servizio OCR per convertire i file di immagine o i PDF in entrata in documenti elettronici.
documentationcenter: ''
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice'
ms.date: 06/14/2022
ms.author: edupont
---
# <a name="use-ocr-to-turn-pdf-and-image-files-into-electronic-documents"></a><a name="use-ocr-to-turn-pdf-and-image-files-into-electronic-documents"></a><a name="use-ocr-to-turn-pdf-and-image-files-into-electronic-documents"></a>Utilizzare OCR per convertire PDF e file di immagine in documenti elettronici

Dai PDF o dai file di immagine che si ricevono dai partner commerciali, è possibile impostare che un servizio OCR (Optical Character Recognition, riconoscimento ottico dei caratteri) generi documenti elettronici che si possono convertire in record di documento in [!INCLUDE[prod_short](includes/prod_short.md)]. Ad esempio, quando si riceve una fattura nel formato PDF dal fornitore, è possibile [inviarla al servizio OCR dalla pagina **Documenti in entrata**](#to-send-a-pdf-or-image-file-to-the-ocr-service-from-the-incoming-documents-page).

In alternativa all'invio del file dalla pagina **Documenti in entrata**, il servizio OCR può offrire la possibilità di [elaborare i file inoltrati a un indirizzo e-mail dedicato](#to-send-a-pdf-or-image-file-to-the-ocr-service-by-email). Successivamente, quando si riceve il documento elettronico, un record di documento entrata correlato viene creato automaticamente in [!INCLUDE[prod_short](includes/prod_short.md)].

Dopo alcuni secondi, il servizio OCR invierà il file elaborato alla pagina **Documenti in arrivo** come un record di documento elettronico che può essere [convertito in fattura di acquisto per il fornitore](#to-receive-the-resulting-electronic-document-from-the-ocr-service), una fattura di vendita, una nota di credito o un movimento contabile.

Poiché OCR si basa sul riconoscimento ottico, è probabile che il servizio OCR interpreti scorrettamente i caratteri nei file PDF o di immagine quando, ad esempio, elabora per la prima volta i documenti di un determinato fornitore. Potrebbe non interpretare il logo della società come nome del fornitore o potrebbe comprendere erroneamente l'importo totale in una ricevuta a causa del layout. Per evitare che questi errori aumentino, è possibile correggerli in una versione separata della pagina **Documenti in entrata**. Quindi si inviano le correzioni al servizio di OCR per permettergli di interpretare correttamente i caratteri e i campi specifici la volta successiva che elabora un PDF o un documento di immagine dello stesso fornitore. Per ulteriori informazioni, vedi [Istruire il servizio OCR a evitare errori](across-how-use-ocr-pdf-images-files.md#to-train-the-ocr-service-to-avoid-errors).

Il traffico di file da e verso il servizio OCR viene elaborato da un movimento coda processi dedicata. Questa coda processi viene creata automaticamente quando si abilita la connessione al servizio OCR esterno. Per ulteriori informazioni, vedere [Impostare documenti in entrata](across-how-setup-income-documents.md).

> [!NOTE]
> La funzione OCR è fornita da fornitori esterni. Scegliere un pacchetto di servizi appropriato per l'organizzazione e/o paese/area geografica. Trova i servizi compatibili con [!INCLUDE[prod_short](includes/prod_short.md)] e i dettagli sulle funzionalità disponibili su [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).

## <a name="to-send-a-pdf-or-image-file-to-the-ocr-service-from-the-incoming-documents-page"></a><a name="to-send-a-pdf-or-image-file-to-the-ocr-service-from-the-incoming-documents-page"></a><a name="to-send-a-pdf-or-image-file-to-the-ocr-service-from-the-incoming-documents-page"></a>Per inviare un file di immagine o PDF al servizio OCR dalla pagina Documenti in entrata

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Documenti in entrata**, quindi scegli il collegamento correlato.
2. Creare un nuovo record di documento in entrata e allegare il file. Per ulteriori informazioni, vedere [Creare i record di documenti in entrata](across-how-create-income-document-records.md).  
3. Nella pagina **Documenti in entrata** selezionare una o più righe e quindi scegliere **Invia a coda processi**.

   Il valore nel campo **Stato OCR** diventa **Pronto**. Il file di immagine o PDF allegato viene inviato al servizio OCR dalla coda processi in base alla pianificazione, se non sono presenti errori.
4. In alternativa, nella pagina **Documenti in entrata** selezionare una o più righe e quindi scegliere l'azione **Invia al servizio OCR** per inviare immediatamente i file all'elaborazione.

   Il valore nel campo **Stato OCR** diventa **Inviato**, se non sono presenti errori.

## <a name="to-send-a-pdf-or-image-file-to-the-ocr-service-by-email"></a><a name="to-send-a-pdf-or-image-file-to-the-ocr-service-by-email"></a><a name="to-send-a-pdf-or-image-file-to-the-ocr-service-by-email"></a>Per inviare un file di immagine o PDF del servizio OCR tramite e-mail

Dall'applicazione e-mail, è possibile inoltrare un messaggio e-mail al provider di servizi OCR con il file di immagine o PDF allegato. Per informazioni sull'indirizzo e-mail di destinazione, vedi il sito Web del provider di servizi OCR.

Dal momento che non esiste alcun record di documento in entrata per il file, un nuovo record verrà creato automaticamente nella pagina **Documenti in entrata** quando si riceve il documento elettronico risultante dal servizio OCR. Per ulteriori informazioni, vedere [Creare i record di documenti in entrata](across-how-create-income-document-records.md).

> [!NOTE]  
> Se si utilizza un tablet o un telefono, è possibile inviare il file al servizio OCR non appena viene scattata la foto del documento oppure è possibile creare direttamente un documento in entrata. Per ulteriori informazioni, vedere [Creare un record di documento in entrata facendo una foto](across-how-create-income-document-records.md#create-an-incoming-document-record-by-taking-a-photo).

## <a name="to-receive-the-resulting-electronic-document-from-the-ocr-service"></a><a name="to-receive-the-resulting-electronic-document-from-the-ocr-service"></a><a name="to-receive-the-resulting-electronic-document-from-the-ocr-service"></a>Per ricevere il documento elettronico risultante dal servizio OCR

Il documento elettronico creato dal servizio OCR dal PDF o dal file di immagine viene ricevuto automaticamente nella pagina **Documenti in entrata** dal movimento coda processi impostato quando si abilita il servizio OCR.

Se non viene utilizzata una coda processi o vuoi ricevere un documento OCR finito prima di quanto previsto dal programma coda processi, è possibile scegliere l'azione **Ricevi dal servizio OCR**. In tal modo verrà ricevuto qualsiasi documento completato dal servizio OCR.

> [!NOTE]  
> Se il servizio OCR è impostato per richiedere la verifica manuale dei documenti elaborati, nel campo **Stato OCR** è presente **In attesa di verifica**. In tal caso, esegui le seguenti operazioni per accedere al sito Web del servizio OCR per verificare manualmente un documento OCR.

1. Nel campo **Stato OCR** scegliere il collegamento ipertestuale **In attesa di verifica**.
2. Nel sito Web del servizio OCR, accedi utilizzando le credenziali dell'account del servizio OCR. Per ulteriori informazioni, vedi [Impostare un servizio OCR](across-how-setup-income-documents.md#to-set-up-an-ocr-service).

   Vengono visualizzate le informazioni per il documento OCR, inclusi il contenuto di origine del PDF o del file di immagine e i valori dei campi OCR risultanti.
3. Analizza i valori dei campi e modifica o immetti manualmente i valori nei campi che il servizio OCR ha etichettato come incerti.
4. Scegliere il pulsante **OK**. Il processo OCR è completato e il documento elettronico risultante viene inviato alla pagina **Documenti in entrata** in [!INCLUDE[prod_short](includes/prod_short.md)], in base al programma coda processi.
5. Ripeti i passaggi da 2 a 4 per qualsiasi altro documento OCR da verificare.

A questo punto è possibile passare alla creazione dei record per i documenti elettronici ricevuti in [!INCLUDE[prod_short](includes/prod_short.md)], manualmente o automaticamente. Per ulteriori informazioni, vedere la procedura che segue. È inoltre possibile [connettere il nuovo record del documento in entrata ai documenti esistenti registrati o non registrati](across-how-connect-disconnect-income-document-records.md) in modo che il file di origine sia facilmente accessibile da [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="to-create-a-purchase-invoice-from-an-electronic-document-received-from-the-ocr-service"></a><a name="to-create-a-purchase-invoice-from-an-electronic-document-received-from-the-ocr-service"></a><a name="to-create-a-purchase-invoice-from-an-electronic-document-received-from-the-ocr-service"></a>Per creare una fattura di acquisto da un documento elettronico ricevuto dal servizio OCR

Di seguito viene descritto come creare un record di fattura di acquisto da una fattura fornitore ricevuta come documento elettronico dal servizio OCR. La procedura è identica a quella per creare, ad esempio, una riga di registrazione COGE da una ricevuta di spesa o un ordine di reso vendita da un cliente.

> [!NOTE]  
> I campi **Descrizione** e **Nr.** nelle righe di documento create verranno compilati solo se è stato precedentemente mappato il testo individuato nel documento OCR ai due campi in [!INCLUDE[prod_short](includes/prod_short.md)]. Si può fare questa mappatura come riferimenti di elementi, per linee di documento di tipo Elemento. Per maggiori informazioni, vedere [Use Elemento References](inventory-how-use-item-cross-refs.md). È anche possibile utilizzare la funzione di **mappatura testo a conto**. Per ulteriori informazioni, vedi [Mappare il testo di un documento in entrata a un determinato fornitore, C/G o conto corrente bancario](across-how-use-ocr-pdf-images-files.md#to-map-text-on-an-incoming-document-to-a-specific-vendor-account).

1. Selezionare la riga relativa al documento in entrata quindi scegliere l'azione **Crea documento**.

Una fattura di acquisto verrà creata in [!INCLUDE[prod_short](includes/prod_short.md)] sulla base delle informazioni contenute nel documento elettronico del fornitore che è stato ricevuto dal servizio OCR. Le informazioni saranno inserite nella nuova fattura d'acquisto in base alla mappatura che hai definito come riferimento o come mappatura testo-conto.

Tutti gli errori di convalida, in genere correlati a dati mancanti o errati in [!INCLUDE[prod_short](includes/prod_short.md)], verranno visualizzati nella Scheda dettaglio **Errori e avvisi**. Per ulteriori informazioni, vedi [Gestire gli errori durante la ricezione di documenti elettronici](across-how-use-ocr-pdf-images-files.md#to-handle-errors-when-receiving-electronic-documents).

### <a name="to-map-text-on-an-incoming-document-to-a-specific-vendor-account"></a><a name="to-map-text-on-an-incoming-document-to-a-specific-vendor-account"></a><a name="to-map-text-on-an-incoming-document-to-a-specific-vendor-account"></a>Per mappare il testo di un documento in entrata a un determinato conto del fornitore

Per i documenti in entrata, in genere l'azione **Mappa testo a conto** si utilizza per definire che un determinato testo in una fattura fornitore ricevuta dal servizio OCR viene mappato a un determinato conto fornitore. Andando avanti, qualsiasi parte della descrizione del documento in entrata che esiste come testo di mappatura significa che il campo **Nr. fornitore** sul documento risultante o sulle righe del giornale di registrazione di tipo *Conto CoGe* è compilato con il fornitore in questione.

Oltre alla mappatura a un conto fornitore o ad altri conti C/G, è possibile mappare il testo a un conto bancario. Questa opzione è utile, ad esempio, per i documenti elettronici relativi alle spese che sono già state pagate e in cui desideri creare una riga registrazione COGE pronta per essere registrata in un conto corrente bancario.

1. Seleziona la riga del documento in entrata pertinente quindi scegli l'azione **Mappa testo a conto**. Verrà aperta la pagina **Mappatura testo a conto**.
2. Nel campo **Mapping testo**, immetti qualsiasi testo presente nelle fatture del fornitore per cui desideri creare documenti di acquisto o righe delle registrazioni. È possibile immettere fino a 50 caratteri.
3. Nel campo **Nr. fornitore** immetti il fornitore per cui verrà creata la riga del documento o di registrazione acquisto.
4. Nel campo **Nr. conto dare**, immetti il conto C/G di tipo dare che verrà inserito nel documento di acquisto o nella riga di registrazione creata di tipo Conto C/G.
5. Nel campo **Nr. conto avere**, immetti il conto C/G di tipo avere che verrà inserito nel documento di acquisto o nella riga di registrazione creata di tipo Conto C/G.

   > [!NOTE]
   > Non usare i campi **Tipo di origine saldo** e **Nr. origine saldo** in relazione ai documenti in entrata. Vengono utilizzati solo per la riconciliazione automatica di pagamento. Per ulteriori informazioni, vedere [Mappare il testo nei pagamenti ricorrenti a conti per la riconciliazione automatica](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).
6. Ripeti i passaggi da 2 a 5 per qualsiasi testo su documenti in entrata per cui vuoi creare automaticamente i documenti.

## <a name="to-handle-errors-when-receiving-electronic-documents"></a><a name="to-handle-errors-when-receiving-electronic-documents"></a><a name="to-handle-errors-when-receiving-electronic-documents"></a>Per gestire gli errori durante la ricezione di documenti elettronici

1. Nella pagina **Documenti in entrata**, seleziona la riga per un documento elettronico ricevuto dal servizio OCR con errori, indicato dal valore *Errore* nel campo **Stato OCR**.
2. Scegliere l'azione **Modifica** per aprire la pagina **Documento in entrata**.
3. Nella Scheda dettaglio **Errori e avvisi**, selezionare il messaggio quindi scegliere l'azione **Apri record correlato**.
4. Viene visualizzata la pagina contenente i dati errati o mancanti, ad esempio una scheda fornitore con un valore di campo mancante.
5. Correggere l'errore o gli errori come descritto in ogni messaggio di errore.
6. Continuare a elaborare il documento elettronico in entrata scegliendo di nuovo l'azione **Crea manualmente**.
7. Ripetere i passaggi 5 e 6 per tutti gli errori rimanenti finché il documento elettronico non può essere ricevuto correttamente.

## <a name="to-train-the-ocr-service-to-avoid-errors"></a><a name="to-train-the-ocr-service-to-avoid-errors"></a><a name="to-train-the-ocr-service-to-avoid-errors"></a>Per istruire il servizio OCR a evitare errori

Poiché OCR si basa sul riconoscimento ottico, è possibile che il servizio OCR interpreti scorrettamente i caratteri nei file PDF o di immagine quando, ad esempio, elabora per la prima volta i documenti da un determinato fornitore. Potrebbe non interpretare il logo della società come nome del fornitore o potrebbe comprendere erroneamente l'importo totale in una ricezione di spese a causa del layout. Per evitare che tali errori vanno avanti, è possibile correggere i dati ricevuti dal servizio OCR e quindi inviare il feedback all'assistenza.

La pagina **Correzione dati OCR** che si apre dalla pagina **Documento in entrata** mostra i campi della Scheda dettaglio **Informazioni finanziarie** in due colonne, una con i dati OCR modificabili e una con i dati OCR di sola lettura. Scegliendo il pulsante **Invia commenti e suggerimenti OCR** il contenuto della pagina **Correzione dati OCR** viene inviato al servizio OCR. La volta successiva che il servizio elabora file PDF o di immagine contenenti i dati in questione, le correzioni verranno incluse per migliorare il riconoscimento del documento.

1. Scegli l'icona a forma di ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") e immetti **Documenti in entrata**, quindi scegli il collegamento correlato.
2. Aprire un record del documento in entrata contenente i dati ricevuti dal servizio OCR da correggere.
3. In alternativa, nella pagina **Documento in entrata** scegliere l'azione **Correggi dati OCR**.
4. Nella pagina **Correggi dati OCR** sovrascrivere i dati nella colonna modificabile per ogni campo contenente un valore non corretto.
5. Per annullare le correzioni apportate dall'apertura della pagina **Correzione dati OCR**, scegliere l'azione **Reimposta dati OCR**.
6. Per inviare le correzioni al servizio OCR, scegliere l'azione **Invia commenti e suggerimenti OCR**.
7. Per salvare le correzioni, chiudere la pagina **Correzione dati OCR**.

I campi della Scheda dettaglio **Informazioni finanziarie** nella pagina **Documento in entrata** vengono aggiornati con i nuovi valori immessi nel passaggio 4.

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Vedi il relativo [training Microsoft](/training/modules/incoming-documents-dynamics-365-business-central/)

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Vedere anche

[Creare i record di documenti in entrata](across-how-create-income-document-records.md)
[Creare i record di documenti in entrata direttamente da documenti e movimenti](across-how-connect-disconnect-income-document-records.md)
[Documenti in entrata](across-income-documents.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
