---
title: 'Procedura: Impostare il servizio di conversione di dati bancari | Documenti Microsoft'
description: 'Procedura: Impostare il servizio di conversione di dati bancari'
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream, data exchange, AMC, bank file import, bank file export, re-export, bank transfer, AMC, bank data conversion service, funds transfer
ms.date: 03/23/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 84834fab38217fb161ed16e3215a34978a4c6137
ms.contentlocale: it-it
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-set-up-the-bank-data-conversion-service"></a>Procedura: Impostare il servizio di conversione di dati bancari
Un provider di servizi globale per convertire le informazioni pagamento in qualsiasi formato di dati richiesto dalla banca viene connesso e preparato per essere abilitato in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Ciò viene indicato in [!INCLUDE[d365fin](includes/d365fin_md.md)] come il servizio di conversione di dati bancari.

Tramite la finestra **Registraz. pagamenti** è possibile esportare le righe pagamento in un file o in un flusso di dati che viene quindi caricato nella banca per l'elaborazione automatica in modo che non sia necessario eseguire singolarmente i pagamenti elettronici. Per ulteriori informazioni, vedere [Procedura: Esportare pagamenti in un file della banca](payables-how-export-payments-bank-file.md).

È possibile importare i file dell'estratto conto nella finestra **Registrazione riconciliazione pagamenti** utilizzando il servizio di conversione di dati bancari per convertire un file ricevuto dalla banca in un flusso di dati che [!INCLUDE[d365fin](includes/d365fin_md.md)] può contenere. Per ulteriori informazioni, vedere [Procedura: Collegare i pagamenti automaticamente e Riconciliazione dei conti correnti bancari](receivables-apply-payments-auto-reconcile-bank-accounts.md).

In alternativa all'importazione di estratti conto con il servizio di conversione di dati bancari, è possibile utilizzare il servizio Feed bancari di Envestnet Yodlee. Per ulteriori informazioni, vedere [Procedura: Impostare il servizio Feed bancari di Envestnet Yodlee](bank-how-setup-bank-statement-service.md).

Per importare o esportare i file dei conti correnti bancari, è necessario impostare il proprio conto corrente bancario e i conti correnti bancari dei fornitori. Per ulteriori informazioni, vedere [Procedura: Impostare i conti correnti bancari](bank-how-setup-bank-accounts.md).

**Nota**: il servizio di conversione di dati bancari può imporre un limite al numero di righe che possono essere esportate in un file. Se il limite viene superato, viene visualizzato un messaggio di errore. È consigliabile che i file del rendiconto bancario non superino 1000 righe, dato che, in caso contrario, il tempo di elaborazione nel servizio di conversione dati bancari può aumentare significativamente.

## <a name="to-sign-your-company-up-for-the-bank-data-conversion-service"></a>Per iscrivere la società al servizio di conversione di dati bancari
1. Nell'angolo superiore destro scegliere l'icona **Cerca pagina o report** ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), inserire **Setup servizio conv. dati banca**, quindi scegliere il collegamento correlato.  
2. Viene aperta la finestra **Setup servizio conv. dati banca** con tre campi precompilati con gli URL del provider del servizio di conversione di dati bancari.

    **Nota**: nel database dimostrativo CRONUS International Ltd. i campi Nome utente e Password sono precompilati con informazioni di connessione dimostrative, che dovranno essere sostituite con le informazioni effettive della società nel momento in cui si procederà all'iscrizione al servizio di conversione di dati bancari.
3. Nel campo **URL iscrizione** scegliere il pulsante Sfoglia per aprire la pagina di iscrizione del provider del servizio.  
4. Nella pagina di iscrizione del provider del servizio dati bancari, immettere il nome utente e la password per l'iscrizione della società al servizio, quindi eseguire il processo di registrazione come indicato dal provider del servizio.

    La società è ora iscritta al servizio di conversione di dati bancari. Continuare immettendo il nome utente e la password specificati per il servizio nei campi di setup correlati in [!INCLUDE[d365fin](includes/d365fin_md.md)].
5. Nella finestra **Setup servizio conv. dati banca**, nel campo **Nome utente**, immettere lo stesso valore che è stato immesso come nome di connessione nella pagina del provider del servizio nel passaggio 4.
6. Nel campo **Password** immettere lo stesso valore che è stato immesso nel campo **Password** nella pagina del provider del servizio nel passaggio 4.

## <a name="to-encrypt-your-login-information"></a>Per crittografare le informazioni di accesso
Si consiglia di proteggere le informazioni di accesso immesse nella finestra **Setup servizio conv. dati banca**. È possibile crittografare dati nel server [!INCLUDE[d365fin](includes/d365fin_md.md)] generando nuove chiavi di crittografia o importando quelle esistenti che vengono abilitate nell'istanza del server [!INCLUDE[d365fin](includes/d365fin_md.md)] che collega al database.

1. Nella finestra **Setup servizio conv. dati banca** scegliere l'azione **Gestione crittografia**.
2. Nella finestra **Gestione crittografia dati** abilitare la crittografia dei dati.

## <a name="to-view-or-update-the-list-of-currently-supported-bank-data-formats"></a>Per visualizzare o aggiornare la lista dei formati di dati bancari attualmente supportato
1. Nell'angolo superiore destro scegliere l'icona **Cerca pagina o report** ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), inserire **Setup servizio conv. dati banca**, quindi scegliere il collegamento correlato.
2. Nella finestra **Setup servizio conv. dati banca**, scegliere l'azione **Nome banca - Lista conversione dati** per aprire l'elenco dei nomi di banca che rappresentano i formati di dati bancari che sono supportati dal servizio di conversione.
3. Nella pagina **Nome banca - Lista conversione dati** scegliere l'azione **Aggiorna lista nomi banche**.

La lista dei formati di dati bancari che sono supportati dal servizio di conversione di dati bancari ora è aggiornata. Si tratta dell'elenco di nomi di banca, filtrato per paese, che è possibile selezionare dal campo **Nome banca - Conversione dati** presente nella finestra **Scheda conto bancario**.

**Nota**: l'aggiornamento dei formati di dati bancari supportati si verifica anche quando si seleziona o si immette un valore nel campo **Nome banca - Conversione dati** del conto corrente bancario.

A questo punto è stata eseguita l'iscrizione al servizio di conversione di dati bancari. Continuare a riflettere le informazioni di iscrizione in ogni conto bancario che utilizzerà il servizio.

## <a name="see-also"></a>Vedi anche
[Impostazione delle attività bancarie](bank-setup-banking.md)  
[Gestione di conti correnti bancari](bank-manage-bank-accounts.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

