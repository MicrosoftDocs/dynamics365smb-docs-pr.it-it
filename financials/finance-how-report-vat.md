---
title: "Gestire la dichiarazione IVA alle autorità fiscali| Documenti Microsoft"
description: "Informazioni su come preparare un report che elenca l'IVA di vendita durante un periodo e inviare il report a un'autorità fiscale."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, tax, report, EC sales list, statement
ms.date: 06/02/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 9b0db56fc08881a94b1f80bafed32d7bcbc24fd8
ms.contentlocale: it-it
ms.lasthandoff: 07/07/2017


---

# <a name="how-to-report-vat-to-tax-authorities"></a>Procedura: Dichiarare l'IVA all'autorità fiscale
Il report dell'elenco delle vendite UE elenca gli importi IVA raccolti per le vendite nell'Unione Europea in modo che sia possibile inviare gli importi IVA al servizio Web di un'autorità fiscale.

> [!NOTE]  
>   Nel Regno Unito, tutte le società che vendono più di un determinato valore ogni anno ai clienti negli stati di membri dell'UE devono inviare una versione elettronica del report dell'elenco delle vendite UE in formato XML attraverso il sito Web HMRC (Her Majesty's Revenue and Customs).

Il report Lista vendite UE elenca solo i lavori per i paesi dell'Unione Europea. Ad esempio, non include l'IVA sulle vendite in paesi come Cina o Stati Uniti.

Per dichiarare l'IVA a un'autorità fiscale elettronicamente, è necessario connettere [!INCLUDE[d365fin](includes/d365fin_md.md)] al servizio Web dell'autorità fiscale. Tale soluzione richiede l'impostazione di un account con l'autorità fiscale. Dopo avere impostato un account, è possibile abilitare la connessione di servizio fornita in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Ad esempio, nel Regno Unito è possibile utilizzare la connessione di servizio **GovTalk**.

Il report include una riga per ogni tipo di transazione con il cliente e visualizza l'importo totale per ogni tipo di transazione. Esistono tre tipi di transazione che il report può includere:  
  
* Prodotti B2B  
* Servizi B2B  
* Prodotti di triangolazione B2B  
  
I prodotti e servizi B2B specificano se sono stati venduti prodotti o servizi e vengono controllati dall'impostazione **Assistenza UE** nel setup registrazioni IVA. I prodotti di triangolazione B2B indicano se è stato attivato un commercio con terze parti e vengono controllati dall'impostazione **Triangolazione intracomun.** nei documenti di vendita, ad esempio ordini di vendita, fatture, note di credito e così via.  
  
Dopo avere inviato il report, [!INCLUDE[d365fin](includes/d365fin_md.md)] controlla il servizio e memorizza un record delle comunicazioni. Il campo **Stato** indica se il report è in esecuzione. Ad esempio, quando le autorità elaborano il report, lo stato del report diventa **Operazione completata**. Se l'autorità fiscale trova errori nel report inviato, lo stato del report diventa **Operazione non riuscita**. È possibile visualizzare gli errori in **Errori e avvisi**, correggerli e quindi inviare il report nuovamente. Per visualizzare un elenco di tutti i report Lista vendite UE, andare alla pagina **Report lista vendite UE**.  
  
> [!NOTE]  
>   Se si utilizza un altro metodo per presentare il report, ad esempio esportando l'XML e caricandolo in un sito Web dell'autorità fiscale, in seguito sarà possibile scegliere **Contrassegna come Inviato** per chiudere il periodo contabile. Quando il report viene contrassegnato come rilasciato, non può più essere modificato. Se si deve modificare il report dopo averlo contrassegnato come rilasciato, è necessario riaprirlo. 
  
Dopo che l'autorità fiscale ha esaminato il report, invia un messaggio e-mail alla persona per la società. In [!INCLUDE[d365fin](includes/d365fin_md.md)], il nome del contatto è specificato nella pagina **Informazioni società**. Prima di inviare il report, assicurarsi che il contatto sia stato selezionato.

<!--> [!NOTE]  
>   Il report Lista vendite UE può contenere un massimo di 1000 righe. Se si dispone di più righe, è necessario inviare un altro report. -->

## <a name="to-connect-to-your-tax-authoritys-web-service"></a>Per connettersi al servizio Web dell'autorità fiscale
[!INCLUDE[d365fin](includes/d365fin_md.md)] fornisce le connessioni di servizio che connettono ai siti Web dell'autorità fiscale. Ad esempio, nel Regno Unito è necessario abilitare la connessione di servizio **GovTalk**.  

1. Nel campo **Cerca pagina o report**, immettere **Connessioni servizio** e scegliere il collegamento appropriato. <!-- remember to get the updated text for this-->  
2. Compilare i campi necessari.  

## <a name="to-set-up-the-ec-sales-list-report"></a>Per impostare il report Lista vendite UE
1. Nel campo **Cerca pagina o report**, immettere **Setup report IVA** e scegliere il collegamento correlato.  
2. Se si desidera permettere agli utenti di modificare e ripresentare questo report, selezionare la casella di controllo **Modifica report inviati**.  
3. Specificare il numero di serie da utilizzare per i report Lista vendite UE.  

## <a name="to-prepare-and-submit-the-ec-sales-list-report"></a>Per preparare e inviare il report Lista vendite UE
1. Nel campo **Cerca pagina o report**, immettere **Lista vendite UE** e scegliere il collegamento correlato.  
2. Scegliere **Nuovo** e compilare i campi necessari.  
3. Per generare il contenuto del report, scegliere l'azione **Suggerisci righe**.  

    > [!NOTE]  
>   È possibile esaminare le transazioni incluse nella riga prima da presentare il report. A tale scopo, selezionare la riga e scegliere l'azione **Mostra movimenti IVA**.  
4. Per preparare il report per l'invio, scegliere l'azione **Rilascio**.  
5. Per inviare il report, scegliere l'azione **Invia**.  
  
[!INCLUDE[d365fin](includes/d365fin_md.md)] verifica che il report sia impostato correttamente. Se la convalida ha esito negativo, gli errori vengono visualizzati in **Errori e avvisi** in modo da poter apportare le modifiche appropriate.

## <a name="viewing-communications-with-your-tax-authority"></a>Visualizzare le comunicazioni con l'autorità fiscale
In alcuni paesi, quando si invia il report si scambiano messaggi con l'autorità fiscale. È possibile visualizzare il primo e l'ultimo messaggio inviato o ricevuto scegliendo l'azione **Scarica messaggio di invio** e **Scarica messaggio di risposta**.  

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
[Impostare l'IVA](finance-setup-vat.md)  
[Impostare le vendite](sales-setup-sales.md)  
[Procedura: Fatturare le vendite](sales-setup-sales.md)  

