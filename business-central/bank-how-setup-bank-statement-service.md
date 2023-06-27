---
title: Impostare il feed bancario di Yodlee
description: È possibile convertire le informazioni sui pagamenti in qualsiasi formato di dati richiesto dalla banca e abilitare l'esportazione o l'importazione dei file della banca.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Yodlee, feed, stream, payment process'
ms.search.form: '1280, 1290'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="set-up-the-envestnet-yodlee-bank-feeds-service"></a>Impostare il servizio Envestnet Yodlee Bank Feeds

È possibile importare gli estratti conto bancari elettronici dalla banca per compilare rapidamente la pagina **Registrazione riconciliazione pagamenti** in modo da poter collegare i pagamenti e riconciliare il conto bancario. Per ulteriori informazioni, vedere [Collegare i pagamenti automaticamente e riconciliare i conti correnti bancari](receivables-apply-payments-auto-reconcile-bank-accounts.md).

> [!IMPORTANT]
> A causa della direttiva sui servizi di pagamento in Europa (PSD2), dopo il 14 settembre 2019, non sarà più possibile importare automaticamente gli estratti conto bancari dalle banche del Regno Unito in [!INCLUDE[prod_short](includes/prod_short.md)]. Stiamo esaminando la possibilità di offrire nuovamente questa funzionalità in futuro.

> [!NOTE]
> Il servizio Envestnet Yodlee Bank Feeds è supportato solo nella versione online di Business Central. Per utilizzare questa funzionalità in locale, è necessario ottenere un un conto cobrand di Envestnet ed è necessario aggiungere codice per l'integrazione con l'API Yodlee.
>
> Il servizio Envestnet Yodlee Bank Feeds è supportato solo negli Stati Uniti e in Canada.
> Sono supportate solo le banche residenti in questi paesi, anche se le banche di altri paesi possono comparire nella finestra di selezione della banca Envestnet Yodlee Bank Feeds in [!INCLUDE[prod_short](includes/prod_short.md)].

> [!IMPORTANT]
> Per assistenza tecnica con la funzionalità Envestnet Yodlee, contattare il supporto Microsoft. Non contattare Envestnet Yodlee. Per ulteriori informazioni, vedere [Configurazione del supporto tecnico per Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/technical-support).

Il servizio Envestnet Yodlee Bank Feeds viene installato come un'estensione di [!INCLUDE[prod_short](includes/prod_short.md)] online ed è pronto per essere abilitato nei paesi supportati. Per maggiori informazioni, vedere [Personalizzazione di [!INCLUDE[prod_short](includes/prod_short.md)] utilizzando le estensioni](ui-extensions.md).

Dopo avere abilitato il servizio di feed bancari, è necessario collegare un conto corrente bancario al conto corrente bancario online da cui deriva il feed. I conti correnti bancari vengono collegati a conti bancari online nelle seguenti situazioni:

* Un conto corrente bancario non esiste in [!INCLUDE[prod_short](includes/prod_short.md)] per il conto corrente online. Di conseguenza, si crea il conto corrente bancario collegando il conto corrente bancario online.
* Un conto corrente bancario esiste in [!INCLUDE[prod_short](includes/prod_short.md)] e si desidera collegarlo a un conto corrente bancario online.
* Il collegamento di conto corrente bancario deve essere annullato perché non si desidera più usare il servizio di feed bancari per il conto.
* I conti correnti bancari online sono stati modificati e si desidera aggiornare le informazioni sui conti correnti bancari in [!INCLUDE[prod_short](includes/prod_short.md)].

Quando il servizio di feed bancari è abilitato, è possibile impostare un conto corrente bancario per importare automaticamente nuovi estratti conto bancari nella pagina **Registrazione riconciliazione pagamenti** ogni di due ore. Le transazioni per i pagamenti già registrate come applicate e/o riconciliate nella pagina **Registrazione riconciliazione pagamenti** non verranno incluse. Per ulteriori informazioni, vedere la sezione "Per abilitare l'importazione automatica degli estratti conto bancari".

> [!NOTE]  
> Se si utilizza la guida al setup assistito Imposta società, alcuni passaggi delle procedure riportate di seguito vengono eseguiti automaticamente quando si raggiunge il setup del conto corrente bancario della società. Per ulteriori informazioni, vedere [Preparazione al business](ui-get-ready-business.md).

## <a name="to-enable-the-bank-feed-service"></a>Per abilitare il servizio di feed bancari
1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **C/C bancari**, quindi scegli il collegamento correlato.
2. Aprire il conto corrente bancario da utilizzare per il servizio di feed bancari.
3. Nella pagina **Conto bancario** nel campo **Formato importazione rendiconto bancario** selezionare YODLEEBANKFEED.  

Il servizio di feed bancari verrà abilitato quando si collega un conto corrente bancario al conto corrente bancario online correlato. Vedere la procedura seguente.  

> [!NOTE]
> Se si utilizza la guida di setup assistito **Setup società**, si attiva l'assistenza selezionando la casella di controllo **Utilizza servizio feed bancari**. Per ulteriori informazioni, vedere [Creazione di nuove società in Business Central](about-new-company.md).

## <a name="to-create-a-new-linked-bank-account"></a>Per creare un nuovo conto bancario collegato
1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **C/C bancari**, quindi scegli il collegamento correlato.
2. Selezionare il conto corrente bancario appropriato e fare clic su **Crea nuovo conto bancario collegato**. Dopo alcuni istanti, si apre la pagina **Collegamento conto bancario**.

    > [!NOTE]  
    > Questa pagina mostra l'effettiva pagina Web del servizio Envestnet Yodlee Bank Feeds. La terminologia e la funzionalità della pagina potrebbero non corrispondere alle indicazioni fornite in questo argomento.  
3. Nella pagina **Collegamento conto bancario online** nel riquadro **Collegamento conto**, utilizzare la funzione di ricerca per trovare la banca presso cui si trovano uno o più conti correnti bancari online.
4. Scegliere il nome della banca. Viene visualizzato il riquadro di **accesso**.
5. Immettere il nome utente e la password utilizzati per accedere alla banca online, quindi selezionare il pulsante **Avanti**.  
6. Il servizio di feed bancari prepara il collegamento del primo conto corrente bancario online della banca specificata a un nuovo conto corrente bancario in [!INCLUDE[prod_short](includes/prod_short.md)].

    > [!NOTE]  
    > Se si dispone di più di un conto corrente bancario online presso la banca, è necessario creare conti correnti bancari aggiuntivi in [!INCLUDE[prod_short](includes/prod_short.md)] per tali conti. Vedere i passaggi da 8 a 10.  

    Al termine del processo, il nome della banca sarà visualizzato nel riquadro **Conti personali** della scheda **Collegato**. Il numero tra parentesi indica il numero di conti bancari online che sono stati collegati.  
7. Scegliere il pulsante **OK**.

    Se si collega solo un conto corrente bancario online, la pagina **Scheda conto corrente bancario** si apre e visualizza il nome del conto corrente bancario online. Questo indica che l'attività di collegamento del conto corrente bancario è stata completata. L'unica cosa che rimane da fare è impostare il conto bancario. Per ulteriori informazioni, vedere [Impostare i conti correnti bancari](bank-how-setup-bank-accounts.md).

    Se si collegano più conti bancari online, si apre la pagina **Collegamento conto bancario** con un elenco dei conti bancari online aggiuntivi che non sono ancora collegati ai conti bancari in [!INCLUDE[prod_short](includes/prod_short.md)]. In questo caso, seguire il passaggio successivo.  
8. Nella pagina **Collegamento conto bancario**, selezionare la riga per un conto corrente bancario online quindi selezionare l'azione **Collega a nuovo conto bancario**.  

    Si apre la pagina **Scheda conto bancario** per un nuovo conto e visualizza il nome del conto bancario online.

    Se un conto corrente bancario è già esistente in [!INCLUDE[prod_short](includes/prod_short.md)] al quale si desidera collegare il conto bancario online aggiuntivo, seguire il passaggio successivo.  
9. Nella pagina **Collegamento conto bancario**, selezionare la riga per un conto corrente bancario online quindi selezionare l'azione **Collega a conto bancario esistente**.
10. Nella pagina **Lista C/C bancari** selezionare il conto bancario per il quale si desidera effettuare il collegamento e quindi fare clic su **OK**.

## <a name="to-link-a-bank-account-to-an-online-bank-account"></a>Per collegare un conto bancario a un conto bancario online
1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **C/C bancari**, quindi scegli il collegamento correlato.
2. Selezionare la riga per un conto bancario non collegato a un conto bancario online quindi selezionare l'azione **Collega a conto bancario online**. Si apre la pagina **Collegamento conto bancario online** con il nome della banca precompilato nel riquadro **Collegamento conto**.
3. Scegliere il nome della banca. Viene visualizzato il riquadro di **accesso**.
4. Immettere il nome utente e la password utilizzati per accedere alla banca online, quindi selezionare il pulsante **Avanti**.  

    Il servizio di feed bancari prepara il collegamento del conto corrente bancario in [!INCLUDE[prod_short](includes/prod_short.md)] al conto bancario online corrispondente.  

    Al termine del processo, il nome della banca sarà visualizzato nel riquadro **Conti personali** della scheda **Collegato**. Se la banca ha più conti bancari, viene collegato solo il conto che è stato selezionato nel passaggio 2.  
5. Scegliere il pulsante **OK**.

Nella pagina **Lista C/C bancari** è selezionata la casella di controllo **Collegato**.

## <a name="to-edit-the-credentials-for-an-online-bank-account"></a>Per modificare le credenziali di un conto bancario online
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Conti correnti bancari** e quindi scegliere il collegamento correlato.  
2. Scegli la riga per un conto bancario collegato a un conto bancario online quindi seleziona l'azione **Modifica informazioni sul conto bancario online**.
3. Aggiorna le credenziali.

## <a name="to-unlink-a-bank-account"></a>Per scollegare un conto bancario
1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **C/C bancari**, quindi scegli il collegamento correlato.  
2. Selezionare la riga per un conto bancario collegato che si desidera scollegare dal relativo conto bancario online e quindi selezionare l'azione **Scollega conto bancario online**.

> [!NOTE]  
> Se si sceglie **Sì** nella finestra di dialogo di conferma, il collegamento al conto bancario online viene rimosso e i dettagli di accesso vengono cancellati. Per collegare il nuovo conto bancario al conto bancario online, è necessario collegarsi ancora alla banca. Per ulteriori informazioni, vedere la sezione "Per collegare un conto bancario a un conto bancario online".

## <a name="to-update-bank-account-linking"></a>Per aggiornare il collegamento del conto bancario
1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **C/C bancari**, quindi scegli il collegamento correlato.
2. Selezionare il conto corrente bancario appropriato e selezionare l'azione **Aggiorna collegamento conto bancario**.

Se esistono dei problemi per uno dei conti bancari collegati nella pagina **Lista C/C bancari** si apre la finestra **Collegamento conto bancario** in cui sono specificati i conti correnti bancari con problemi. Il modo migliore per risolvere i problemi consiste nello scollegare il conto bancario online e quindi ricreare il collegamento. Per ulteriori informazioni, vedere la sezione "Per collegare un conto bancario a un conto bancario online".

## <a name="to-enable-automatic-import-of-bank-statements"></a>Per abilitare l'importazione automatica degli estratti conto bancari
1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **C/C bancari**, quindi scegli il collegamento correlato.
2. Selezionare la riga per un conto corrente bancario collegato quindi selezionare l'azione **Setup importazione automatica rendiconti bancari**.
3. Nella pagina **Setup importazione automatica rendiconti bancari** nel campo **Numero di giorni inclusi** specificare il periodo per recuperare le nuove transazioni bancarie.

    > [!NOTE]  
    > Si consiglia di impostare il valore di 7 o più giorni.  
4. Selezionare la casella **Abilitato**.  

Ogni ora la pagina **Registrazione riconciliazione pagamenti** visualizzerà i nuovi pagamenti che vengono effettuati sul conto bancario online.

> [!NOTE]  
> Le transazioni per i pagamenti già registrate come applicate e/o riconciliate nella pagina **Registrazione riconciliazione pagamenti** non verranno incluse.

## <a name="see-also"></a>Vedere anche
[Impostazione delle attività bancarie](bank-setup-banking.md)  
[Riconciliazione dei conti correnti bancari](bank-manage-bank-accounts.md)  
[Collegare i pagamenti automaticamente e riconciliare i conti correnti bancari](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Personalizzazione di [!INCLUDE[prod_short](includes/prod_short.md)] utilizzando le estensioni ](ui-extensions.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
