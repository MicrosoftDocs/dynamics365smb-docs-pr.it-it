---
title: Impostare il servizio di conversione dati bancari
description: 'È possibile impostare i conti correnti bancari per tenere traccia delle transazioni e importare o esportare i feed bancari, ad esempio Yodlee.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Yodlee, feed, stream, data exchange, AMC, bank file import, bank file export, re-export, bank transfer, AMC, AMC Banking 365 Fundamentals extension, funds transfer'
ms.search.form: '304, 20106, 20105, 20100, 20101, 20107, 20109'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="set-up-the-amc-banking-365-fundamentals-extension"></a>Impostare l'estensione AMC Banking 365 Fundamentals
Un provider di servizi globale per convertire le informazioni pagamento in qualsiasi formato di dati richiesto dalla banca viene connesso e preparato per essere abilitato in [!INCLUDE[prod_short](includes/prod_short.md)]. Questo è indicato in [!INCLUDE[prod_short](includes/prod_short.md)] come l'estensione AMC Banking 365 Fundamentals.

Tramite la pagina **Registraz. pagamenti** è possibile esportare le righe pagamento in un file o in un flusso di dati che viene quindi caricato nella banca per l'elaborazione automatica in modo che non sia necessario eseguire singolarmente i pagamenti elettronici. Per ulteriori informazioni, vedere [Esportare pagamenti in un file della banca](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

È possibile importare i file dell'estratto conto bancario nella pagina **Registrazione riconciliazione pagamenti** utilizzando l'estensione AMC Banking 365 Fundamentals per convertire un file ricevuto dalla banca in un flusso di dati che [!INCLUDE[prod_short](includes/prod_short.md)] può contenere. Per ulteriori informazioni, vedere [Collegare i pagamenti automaticamente e riconciliare i conti correnti bancari](receivables-apply-payments-auto-reconcile-bank-accounts.md).

In alternativa all'importazione di estratti conto con l'estensione AMC Banking 365 Fundamentals, è possibile utilizzare il servizio Envestnet Yodlee Bank Feeds. Per ulteriori informazioni, vedere [Impostare il servizio Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).

Per importare o esportare i file dei conti correnti bancari, è necessario impostare il proprio conto corrente bancario e i conti correnti bancari dei fornitori. Per ulteriori informazioni, vedere [Impostare i conti correnti bancari](bank-how-setup-bank-accounts.md).

> [!NOTE]  
> L'estensione AMC Banking 365 Fundamentals può imporre un limite al numero di righe che possono essere esportate in un file. Se il limite viene superato, viene visualizzato un messaggio di errore. È consigliabile che i file del estratto conto bancario non superino 1000 righe, dato che, in caso contrario, il tempo di elaborazione nell'estensione AMC Banking 365 Fundamentals può aumentare significativamente.

## <a name="to-sign-your-company-up-for-the-amc-banking-365-fundamentals-extension"></a>Per iscrivere la società all'estensione AMC Banking 365 Fundamentals
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Setup servizio conv. dati banca**, quindi scegli il collegamento correlato.  
2. Viene aperta la pagina **Setup servizio conv. dati banca** con tre campi precompilati con gli URL del provider dell'estensione AMC Banking 365 Fundamentals.

    > [!NOTE]  
    >   Nel database di dimostrazione CRONUS International Ltd. i campi Nome utente e Password sono precompilati con informazioni di connessione dimostrative, che dovranno essere sostituite con le informazioni effettive della società nel momento in cui si procederà all'iscrizione all'estensione AMC Banking 365 Fundamentals.
3. Nel campo **URL iscrizione** scegliere il pulsante Sfoglia per aprire la pagina di iscrizione del provider del servizio.  
4. Nella pagina di iscrizione del provider del servizio dati bancari, immettere il nome utente e la password per l'iscrizione della società al servizio, quindi eseguire il processo di registrazione come indicato dal provider del servizio.

    La società ora è iscritta all'estensione AMC Banking 365 Fundamentals. Continuare immettendo il nome utente e la password specificati per il servizio nei campi di setup correlati in [!INCLUDE[prod_short](includes/prod_short.md)].

5. Nella pagina **Setup servizio conv. dati banca**, nel campo **Nome utente**, immettere lo stesso valore che è stato immesso come nome di connessione nella pagina del provider del servizio nel passaggio 4.
6. Nel campo **Password** immettere lo stesso valore che è stato immesso nel campo **Password** nella pagina del provider del servizio nel passaggio 4.

> [!NOTE]  
> I dati di accesso vengono automaticamente crittografati.

## <a name="to-view-or-update-the-list-of-currently-supported-bank-data-formats"></a>Per visualizzare o aggiornare la lista dei formati di dati bancari attualmente supportato
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Setup servizio conv. dati banca**, quindi scegli il collegamento correlato.
2. Nella pagina **Setup servizio conv. dati banca**, scegliere l'azione **Nome banca - Lista conversione dati** per aprire l'elenco dei nomi di banca che rappresentano i formati di dati bancari che sono supportati dal servizio di conversione.
3. Nella pagina **Nome banca - Lista conversione dati** scegliere l'azione **Aggiorna lista nomi banche**.

La lista dei formati di dati bancari che sono supportati dall'estensione AMC Banking 365 Fundamentals ora è aggiornata. Si tratta dell'elenco di nomi di banca, filtrato per paese, che è possibile selezionare dal campo **Nome banca - Conversione dati** presente nella pagina **Scheda conto bancario**.

> [!NOTE]  
>   L'aggiornamento dei formati di dati bancari supportati si verifica anche quando si seleziona o si immette un valore nel campo **Nome banca - Conversione dati** del conto corrente bancario.

La società è stata iscritta all'estensione AMC Banking 365 Fundamentals. Continuare a riflettere le informazioni di iscrizione in ogni conto bancario che utilizzerà il servizio.

## <a name="see-also"></a>Vedere anche
[Impostazione delle attività bancarie](bank-setup-banking.md)  
[Riconciliazione dei conti correnti bancari](bank-manage-bank-accounts.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
