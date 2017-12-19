---
title: "Inviare la dichiarazione IVA alle autorità fiscali | Microsoft Docs"
description: "Informazioni su come preparare un report che elenca l'IVA di vendita durante un periodo, o di vendite e acquisti, e inviarlo a un'autorità fiscale."
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, tax, report, EC sales list, statement
ms.date: 07/17/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: aa56764b5f3210229ad21eae6891fb201462209c
ms.openlocfilehash: eb261f0b5b2aae94cebd79c6b23b0a21cb9451ae
ms.contentlocale: it-it
ms.lasthandoff: 12/14/2017

---

# <a name="how-to-report-vat-to-a-tax-authority"></a>Procedura: Dichiarare l'IVA a un'autorità fiscale
Questo argomento descrive i report [!INCLUDE[d365fin](includes/d365fin_md.md)] che si possono utilizzare per inviare informazioni sugli importi IVA di vendite e di acquisti all'autorità fiscale del proprio paese.

È possibile utilizzare i seguenti report:

* Il report **Lista vendite UE** elenca gli importi IVA che l'azienda ha raccolto con la vendita a clienti con partita IVA nei paesi dell'Unione Europea.  
* Il report **Dichiarazione IVA** include gli importi IVA per vendite e acquisti a clienti in tutti i paesi che utilizzano l'IVA.

Se si desidera visualizzare uno storico completo delle voci di IVA, ogni registrazione che implica l'iVA crea una voce nella pagina **Movimenti IVA**. Questi movimenti vengono utilizzati per calcolare l'importo della liquidazione dell'IVA, ovvero un versamento o un rimborso, per un periodo specifico. Per visualizzare i movimenti IVA, scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Movimenti IVA**, quindi scegliere i collegamento correlato.

## <a name="about-the-ec-sales-list-report"></a>Informazioni sul report Lista vendite UE
Nel Regno Unito, tutte le società che vendono beni e servizi a clienti con partita IVA, inclusi i clienti in altri paesi dell'Unione Europea (UE), è necessario inviare una versione elettronica del report Lista vendite UE in formato XML tramite il sito Web HMRC (Her Majesty's Revenue and Customs). Il report Lista vendite UE è valido solo per i paesi dell'Unione Europea.

Il report include una riga per ogni tipo di transazione con il cliente e visualizza l'importo totale per ogni tipo di transazione. Esistono tre tipi di transazioni che il report può includere:  

* Prodotti B2B  
* Servizi B2B  
* Prodotti di triangolazione B2B  

I prodotti e i servizi B2B specificano se sono stati venduti prodotti o servizi e vengono controllati dall'impostazione **Assistenza UE** nel setup registrazioni IVA. I prodotti di triangolazione B2B indicano se è stato attivato un commercio con terze parti e vengono controllati dall'impostazione **Triangolazione intracomun.** nei documenti di vendita, ad esempio ordini di vendita, fatture, note di credito e così via.  

Dopo che l'autorità fiscale ha esaminato il report, invia un messaggio e-mail alla persona per la società. In [!INCLUDE[d365fin](includes/d365fin_md.md)], il nome del contatto è specificato nella pagina **Informazioni società**. Prima di inviare il report, assicurarsi che il contatto sia stato selezionato.

## <a name="about-the-vat-return-report"></a>Informazioni sul report Dichiarazione IVA
Utilizzare questo report per inviare l'IVA per i documenti di vendita e di acquisto, ad esempio gli ordini vendita e gli ordini acquisto, le fatture e le note di credito. Le informazioni nel report vengono mostrate nello stesso formato di quello utilizzato nel modulo di dichiarazione delle autorità fiscali e doganali.  

L'IVA viene calcolata in base al setup registrazioni IVA e alle categorie di registrazione IVA impostate.

Per la dichiarazione IVA è possibile specificare i movimenti per includere:

* Inviare solo le transazioni aperte, o aperte e chiuse. Questo approccio è utile, ad esempio, quando si prepara la dichiarazione IVA di fine anno.
* Inviare solo movimenti da periodi specificati, o includere anche i movimenti di periodi precedenti. Ciò risulta utile quando si deve aggiornare la dichiarazione IVA già inviata, ad esempio, se un fornitore invia una fattura in ritardo.    

## <a name="to-connect-to-your-tax-authoritys-web-service"></a>Per connettersi al servizio Web dell'autorità fiscale
[!INCLUDE[d365fin](includes/d365fin_md.md)] include le connessioni di servizio ai siti Web delle autorità fiscali. Nel Regno Unito, ad esempio, è possibile abilitare la connessione di servizio **GovTalk** per inviare elettronicamente i report Lista vendite UE e Dichiarazione IVA. Se si desidera inviare il report manualmente, ad esempio inserendo i dati sul sito Web dell'autorità fiscale, questa connessione non è necessaria.   

Per dichiarare l'IVA a un'autorità fiscale elettronicamente, è necessario connettere [!INCLUDE[d365fin](includes/d365fin_md.md)] al servizio Web dell'autorità fiscale. Tale soluzione richiede l'impostazione di un account con l'autorità fiscale. Dopo avere impostato un account, è possibile abilitare la connessione di servizio fornita in [!INCLUDE[d365fin](includes/d365fin_md.md)].

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Connessioni servizio**, quindi scegliere il collegamento appropriato.
2. Compilare i campi necessari. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
>   È consigliabile testare la connessione. A tal fine, selezionare la casella di controllo **Modalità di test**, quindi preparare e inviare la dichiarazione IVA come descritto nella sezione _Per preparare e inviare una dichiarazione IVA_. Mentre è attiva la modalità di test, il servizio verifica se l'autorità fiscale può ricevere la dichiarazione e lo stato del report indicherà se l'invio ha avuto esito positivo. È importante ricordare che non si tratta di un invio effettivo. Per inviare realmente il report, è necessario deselezionare la casella di controllo **Modalità di test** e quindi ripetere la procedura di invio.

## <a name="to-set-up-vat-reports-in-included365finincludesd365finmdmd"></a>Per impostare i report IVA in [!INCLUDE[d365fin](includes/d365fin_md.md)]
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Setup report IVA** e scegliere il collegamento correlato.  
2. Per permettere agli utenti di modificare e ripresentare questo report, selezionare la casella di controllo **Modifica report inviati**.  
3. Scegliere la numerazione da utilizzare per ogni report.  

## <a name="to-prepare-and-submit-a-vat-report"></a>Per salvare e inviare un report IVA
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Lista vendite UE** o **Dichiarazione IVA**, quindi scegliere il collegamento correlato.  
2. Scegliere **Nuovo** e compilare i campi necessari. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Per generare il contenuto del report, scegliere l'azione **Suggerisci righe**.  

    > [!NOTE]  
>   Nel report Lista vendite UE, è possibile rivedere le transazioni incluse nelle righe del report prima di inviarlo. A tale scopo, selezionare la riga e scegliere l'azione **Mostra movimenti IVA**.  
4. Per convalidare e preparare il report per l'invio, scegliere l'azione **Rilascio**.  

    >  [!NOTE]  
>   [!INCLUDE[d365fin](includes/d365fin_md.md)] verifica che il report sia impostato correttamente. Se la convalida ha esito negativo, gli errori vengono visualizzati in **Errori e avvisi** per consentirne la correzione. In genere, se il messaggio è relativo a un'impostazione mancante in [!INCLUDE[d365fin](includes/d365fin_md.md)], è possibile fare clic sul messaggio per aprire la pagina che contiene le informazioni da correggere.  
5. Per inviare il report, scegliere l'azione **Invia**.  

Dopo avere inviato il report, [!INCLUDE[d365fin](includes/d365fin_md.md)] controlla il servizio e memorizza un record delle comunicazioni. Il campo **Stato** indica se il report è in esecuzione. Ad esempio, quando le autorità elaborano il report, lo stato del report diventa **Operazione completata**. Se l'autorità fiscale trova errori nel report inviato, lo stato del report diventa **Operazione non riuscita**. È possibile visualizzare gli errori in **Errori e avvisi**, correggerli e quindi inviare il report nuovamente. Per visualizzare un elenco di tutti i report Lista vendite UE, andare alla pagina **Report lista vendite UE**.  

## <a name="viewing-communications-with-your-tax-authority"></a>Visualizzare le comunicazioni con l'autorità fiscale
In alcuni paesi, quando si invia il report si scambiano messaggi con l'autorità fiscale. È possibile visualizzare il primo e l'ultimo messaggio inviato o ricevuto scegliendo l'azione **Scarica messaggio di invio** e **Scarica messaggio di risposta**.  

## <a name="submitting-vat-reports-manually"></a>Inviare i report IVA manualmente
Se si utilizza un altro metodo per presentare il report, ad esempio esportando l'XML e caricandolo in un sito Web dell'autorità fiscale, in seguito sarà possibile scegliere **Contrassegna come Inviato** per chiudere il periodo contabile. Quando il report viene contrassegnato come rilasciato, non può più essere modificato. Se si deve modificare il report dopo averlo contrassegnato come rilasciato, è necessario riaprirlo.

## <a name="vat-settlement"></a>Liquidazione IVA
Periodicamente, è necessario rimettere l'IVA netta alle autorità fiscali. Se occorre liquidare l'IVA frequentemente, è possibile eseguire il processo batch **Calcolo e registrazione liquidazione IVA** per chiudere i movimenti IVA aperti e trasferire gli importi IVA di vendita e di acquisto nel conto di liquidazione IVA.

Quando si trasferiscono gli importi IVA nel conto di liquidazione, il conto relativo all'IVA acquisti viene accreditato mentre il conto relativo all'IVA vendite viene addebitato in base all'importo calcolato per il periodo specificato. L'importo netto viene accreditato sul conto di liquidazione dell'IVA. Nel caso in cui l'importo dell'IVA acquisti sia maggiore, l'importo netto verrà addebitato. È possibile registrare la liquidazione immediatamente o stampare prima un report di test.

>    [!NOTE]  
>    Quando si utilizza il processo batch **Calcolo e registrazione liquidazione IVA**, non si specifica una **Cat. reg. business IVA** e una **Cat. reg. art./serv. IVA**, vengono inclusi i movimenti con tutte le categorie di registrazione e i codici categoria di registrazione articoli/servizi IVA.

## <a name="configuring-your-own-vat-reports"></a>Configurazione dei report IVA personalizzati
È possibile utilizzare il report Lista vendite UE predefinito, tuttavia è anche possibile creare propri report. Tale soluzione richiede di creare alcune codeunit. Per assistenza, contattare un partner Microsoft.  

Nella tabella seguente sono descritte le codeunit da creare per il report.

| Codeunit | Operazione che deve eseguire |
|----|-----|
|Suggerisci righe| Recupera le informazioni contenute nella tabella Movimenti IVA e visualizzale nelle righe del report IVA.|
|Contenuto | Controllare il formato del report. Ad esempio, se è JSON o XML. Il formato da utilizzare varia a seconda dei requisiti del service Web dell'autorità fiscale |
|Invio | Controllare come e quando il report viene inviato in base ai requisiti dell'autorità fiscale. |
|Gestore risposte | Gestire le risposte dell'autorità fiscale. Ad esempio, potrebbe inviare un messaggio e-mail al contatto della società. |
|Annulla | Inviare un annullamento di un report IVA inviato in precedenza all'autorità fiscale. |

> [!NOTE]  
>   Quando si creano le codeunit per il report, prestare attenzione al valore nel campo **Versione report IVA**. Questo campo deve riflettere la versione del report che è o era richiesto dall'autorità fiscale. Ad esempio, si potrebbe immettere **2017** nel campo per indicare che il report è conforme ai requisiti in essere in quell'anno. Per individuare la versione corrente, contattare l'autorità fiscale.  

## <a name="see-also"></a>Vedere anche
[Impostazione dei calcoli e registrazione dei metodi per l'IVA](finance-setup-vat.md)  
[Procedura: Utilizzare l'IVA nelle vendite e negli acquisti](finance-work-with-vat.md)  
[Setup Vendite](sales-setup-sales.md)  
[Procedura: Fatturare le vendite](sales-setup-sales.md)  

