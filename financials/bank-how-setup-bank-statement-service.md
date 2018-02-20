---
title: Impostare i feed bancari di Yodlee| Documenti Microsoft
description: "È possibile convertire le informazioni sui pagamenti in qualsiasi formato di dati richiesto dalla banca e abilitare l'esportazione o l'importazione dei file della banca."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream, payment process
ms.date: 09/14/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: fa5c0c39dbbce40b59d639f810522c66da1a09ab
ms.contentlocale: it-it
ms.lasthandoff: 01/30/2018

---
# <a name="set-up-the-envestnet-yodlee-bank-feeds-service"></a>Impostare il servizio di Feed bancario di Envestnet Yodlee
È possibile importare gli estratti conto bancari elettronici dalla banca per compilare rapidamente la finestra **Registrazione riconciliazione pagamenti** in modo da poter collegare i pagamenti e riconciliare il conto bancario. Per ulteriori informazioni, vedere [Collegare i pagamenti automaticamente e riconciliare i conti correnti bancari](receivables-apply-payments-auto-reconcile-bank-accounts.md).

Il servizio Feed bancari di Envestnet Yodlee viene installato come un'estensione in [!INCLUDE[d365fin](includes/d365fin_md.md)] ed è pronto per essere abilitato. Per maggiori informazioni, vedere [Personalizzazione di [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzando le estensioni](ui-extensions.md).

> [!NOTE]
> Il servizio Feed bancari di Envestnet Yodlee è supportato solo negli Stati Uniti, in Canada e nel Regno Unito.

Dopo avere abilitato il servizio di feed bancari, è necessario collegare un conto corrente bancario al conto corrente bancario online da cui deriva il feed. I conti correnti bancari vengono collegati a conti bancari online nelle seguenti situazioni:

* Un conto corrente bancario non esiste in [!INCLUDE[d365fin](includes/d365fin_md.md)] per il conto corrente online. Di conseguenza, si crea il conto corrente bancario collegando il conto corrente bancario online.
* Un conto corrente bancario esiste in [!INCLUDE[d365fin](includes/d365fin_md.md)] e si desidera collegarlo a un conto corrente bancario online.
* Il collegamento di conto corrente bancario deve essere annullato perché non si desidera più usare il servizio di feed bancari per il conto.
* I conti correnti bancari online sono stati modificati e si desidera aggiornare le informazioni sui conti correnti bancari in [!INCLUDE[d365fin](includes/d365fin_md.md)].

Quando il servizio di feed bancari è abilitato, è possibile impostare un conto corrente bancario per importare automaticamente nuovi estratti conto bancari nella finestra **Registrazione riconciliazione pagamenti** ogni di due ore. Le transazioni per i pagamenti già registrate come applicate e/o riconciliate nella finestra **Registrazione riconciliazione pagamenti** non verranno incluse. Per ulteriori informazioni, vedere la sezione "Per abilitare l'importazione automatica degli estratti conto bancari".

> [!NOTE]  
>   Se si utilizza il setup assistito Imposta società, alcuni passaggi delle procedure riportate di seguito vengono eseguiti automaticamente quando si raggiunge il setup del conto corrente bancario della società. Per ulteriori informazioni, vedere [Benvenuto in [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md).

## <a name="to-enable-the-bank-feed-service"></a>Per abilitare il servizio di feed bancari
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **C/C bancari**, quindi scegliere il collegamento correlato.
2. Aprire il conto corrente bancario da utilizzare per il servizio di feed bancari.
3. Nella finestra **Conto bancariot** nel campo **Formato importazione rendiconto bancario** selezionare YODLEEBANKFEED.  

Il servizio di feed bancari verrà abilitato quando si collega un conto corrente bancario al conto corrente bancario online correlato. Vedere la procedura seguente.  

## <a name="to-create-a-new-linked-bank-account"></a>Per creare un nuovo conto bancario collegato
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **C/C bancari**, quindi scegliere il collegamento correlato.
2. Selezionare il conto corrente bancario appropriato e fare clic su **Crea nuovo conto bancario collegato**. Dopo alcuni istanti, si apre la finestra **Collegamento conto bancario**.

    > [!NOTE]  
>   Questa finestra mostra l'effettiva pagina Web del servizio Feed bancari di Envestnet Yodlee. La terminologia e la funzionalità della finestra potrebbero non corrispondere alle indicazioni fornite in questo argomento.  
3. Nella finestra **Collegamento conto bancario online** nel riquadro **Collegamento conto**, utilizzare la funzione di ricerca per trovare la banca presso cui si trovano uno o più conti correnti bancari online.
4. Scegliere il nome della banca. Viene visualizzato il riquadro di **accesso**.
5. Immettere il nome utente e la password utilizzati per accedere alla banca online, quindi selezionare il pulsante **Avanti**.  
6. Il servizio di feed bancari prepara il collegamento del primo conto corrente bancario online della banca specificata a un nuovo conto corrente bancario in [!INCLUDE[d365fin](includes/d365fin_md.md)].

    > [!NOTE]  
>   Se si dispone di più di un conto corrente bancario online presso la banca, è necessario creare conti correnti bancari aggiuntivi in [!INCLUDE[d365fin](includes/d365fin_md.md)] per tali conti. Vedere i passaggi da 8 a 10.  

    Al termine del processo, il nome della banca sarà visualizzato nel riquadro **Conti personali** della scheda **Collegato**. Il numero tra parentesi indica il numero di conti bancari online che sono stati collegati.  
7. Scegliere il pulsante **OK**.

    Se si collega solo un conto corrente bancario online, la finestra **Scheda conto corrente bancario** si apre e visualizza il nome del conto corrente bancario online. Questo indica che l'attività di collegamento del conto corrente bancario è stata completata. L'unica cosa che rimane da fare è impostare il conto bancario. Per ulteriori informazioni, vedere [Impostare i conti correnti bancari](bank-how-setup-bank-accounts.md).

    Se si collegano più conti bancari online, si apre la finestra **Collegamento conto bancario** con un elenco dei conti bancari online aggiuntivi che non sono ancora collegati ai conti bancari in [!INCLUDE[d365fin](includes/d365fin_md.md)]. In questo caso, seguire il passaggio successivo.  
8. Nella finestra **Collegamento conto bancario**, selezionare la riga per un conto corrente bancario online quindi selezionare l'azione **Collega a nuovo conto bancario**.  

    Si apre la finestra **Scheda conto bancario** per un nuovo conto e visualizza il nome del conto bancario online.

    Se un conto corrente bancario è già esistente in [!INCLUDE[d365fin](includes/d365fin_md.md)] al quale si desidera collegare il conto bancario online aggiuntivo, seguire il passaggio successivo.  
9. Nella finestra **Collegamento conto bancario**, selezionare la riga per un conto corrente bancario online quindi selezionare l'azione **Collega a conto bancario esistente**.
10. Nella finestra **Lista C/C bancari** selezionare il conto bancario per il quale si desidera effettuare il collegamento e quindi fare clic su **OK**.

## <a name="to-link-a-bank-account-to-an-online-bank-account"></a>Per collegare un conto bancario a un conto bancario online
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **C/C bancari**, quindi scegliere il collegamento correlato.
2. Selezionare la riga per un conto bancario non collegato a un conto bancario online quindi selezionare l'azione **Collega a conto bancario online**. Si apre la finestra **Collegamento conto bancario online** con il nome della banca precompilato nel riquadro **Collegamento conto**.
3. Scegliere il nome della banca. Viene visualizzato il riquadro di **accesso**.
4. Immettere il nome utente e la password utilizzati per accedere alla banca online, quindi selezionare il pulsante **Avanti**.  

    Il servizio di feed bancari prepara il collegamento del conto corrente bancario in [!INCLUDE[d365fin](includes/d365fin_md.md)] al conto bancario online corrispondente.  

    Al termine del processo, il nome della banca sarà visualizzato nel riquadro **Conti personali** della scheda **Collegato**. Se la banca ha più conti bancari, viene collegato solo il conto che è stato selezionato nel passaggio 2.  
5. Scegliere il pulsante **OK**.

Nella finestra **Lista C/C bancari** è selezionata la casella di controllo **Collegato**.

## <a name="to-unlink-a-bank-account"></a>Per scollegare un conto bancario
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **C/C bancari**, quindi scegliere il collegamento correlato.  
2. Selezionare la riga per un conto bancario collegato che si desidera scollegare dal relativo conto bancario online e quindi selezionare l'azione **Scollega conto bancario online**.

> [!NOTE]  
>   Se si sceglie **Sì** nella finestra di dialogo di conferma, il collegamento al conto bancario online viene rimosso e i dettagli di accesso vengono cancellati. Per collegare il nuovo conto bancario al conto bancario online, è necessario collegarsi ancora alla banca. Per ulteriori informazioni, vedere la sezione "Per collegare un conto bancario a un conto bancario online".

## <a name="to-update-bank-account-linking"></a>Per aggiornare il collegamento del conto bancario
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **C/C bancari**, quindi scegliere il collegamento correlato.
2. Selezionare il conto corrente bancario appropriato e selezionare l'azione **Aggiorna collegamento conto bancario**.

Se esistono dei problemi per uno dei conti bancari collegati nella finestra **Lista C/C bancari** si apre la finestra **Collegamento conto bancario** in cui sono specificati i conti correnti bancari con problemi. Il modo migliore per risolvere i problemi consiste nello scollegare il conto bancario online e quindi ricreare il collegamento. Per ulteriori informazioni, vedere la sezione "Per collegare un conto bancario a un conto bancario online".

## <a name="to-enable-automatic-import-of-bank-statements"></a>Per abilitare l'importazione automatica degli estratti conto bancari
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **C/C bancari**, quindi scegliere il collegamento correlato.
2. Selezionare la riga per un conto corrente bancario collegato quindi selezionare l'azione **Setup importazione automatica rendiconti bancari**.
3. Nella finestra **Setup importazione automatica rendiconti bancari** nel campo **Numero di giorni inclusi** specificare il periodo per recuperare le nuove transazioni bancarie.

    > [!NOTE]  
>   Si consiglia di impostare il valore di 7 o più giorni.  
4. Selezionare la casella **Abilitato**.  

Ogni ora la finestra **Registrazione riconciliazione pagamenti** visualizzerà i nuovi pagamenti che vengono effettuati sul conto bancario online.

> [!NOTE]  
>   Le transazioni per i pagamenti già registrate come applicate e/o riconciliate nella finestra **Registrazione riconciliazione pagamenti** non verranno incluse.

## <a name="see-also"></a>Vedi anche
[Impostazione delle attività bancarie](bank-setup-banking.md)  
[Gestione di conti correnti bancari](bank-manage-bank-accounts.md)  
[Collegare i pagamenti automaticamente e riconciliare i conti correnti bancari](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Personalizzazione di [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzando le estensioni ](ui-extensions.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

