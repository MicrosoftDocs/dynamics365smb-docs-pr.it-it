---
title: Riconciliare i pagamenti utilizzando il collegamento automatico
description: Descrive come utilizzare la funzione automatica di collegamento per collegare i pagamenti o gli incassi ai movimenti aperti relativi e per riconciliare i pagamenti.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, direct payment posting, reconcile payment, expenses, cash receipts
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 138edf1af85de2e9ac10697ea01d9003f0c3d16b
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5393426"
---
# <a name="reconcile-payments-using-automatic-application"></a>Riconciliare i pagamenti utilizzando il collegamento automatico

La pagina **Registrazione riconciliazione pagamenti** specifica i pagamenti in entrata e in uscita che sono stati registrati come transazioni nel conto bancario online o in un servizio di pagamento e che possono essere collegati ai relativi movimenti contabili aperti di conti correnti bancari, fornitori e clienti. Le righe nel giornale di registrazione possono essere compilate importando un estratto conto come feed bancario o file della banca o inserendo manualmente le transazioni effettuate sul servizio di pagamento.

> [!NOTE]
> La pagina offre funzionalità di corrispondenza automatica che collega i pagamenti ai relativi movimenti aperti in base a una corrispondenza di dati su una riga di estratto conto bancario (riga di registrazione) con i dati su uno o più movimenti aperti. Si noti che è possibile sovrascrivere i collegamenti automatici suggeriti ed è possibile scegliere di non utilizzare il collegamento automatico per nulla. Per ulteriori informazioni, vedere il passaggio 7.

Una registrazione riconciliazione pagamenti è correlata a un conto bancario in [!INCLUDE[prod_short](includes/prod_short.md)] che riflette il conto bancario online in cui vengono registrate le transazioni di pagamento. Se si sceglie l'azione **Registra pagamenti e riconcilia conto bancario**, qualsiasi movimento COGE aperto correlato ai movimenti contabilità fornitori o clienti collegati verrà chiuso. Questo significa che il conto bancario viene riconciliato automaticamente per i pagamenti che si registrano con le scritture registrazioni e chiudere i movimenti contabili correlati.

È possibile importare transazioni bancarie sotto forma di file con estensione CSV o in altro formato fornito dalla banca. Se si desidera importare gli estratti conto bancari come feed bancari, è necessario innanzitutto abilitare un servizio di integrazione bancaria dedicato e successivamente collegare il conto corrente bancario al relativo conto bancario online. La registrazione riconciliazione pagamenti viene quindi rilevata automaticamente dai feed bancari quando si sceglie l'azione **Importa transazioni bancarie**. Inoltre, è possibile impostare un conto corrente bancario in modo che importi nuovi feed bancari ogni ora. Le transazioni per i pagamenti che sono già state contabilizzate come collegate e/o riconciliate non verranno importate. A tale scopo, è possibile utilizzare il servizio Envestnet Yodlee Bank Feeds, preinstallato nelle versioni di [!INCLUDE[d365fin](includes/d365fin_md.md)] di alcuni paesi. Per ulteriori informazioni, vedere [Impostare il servizio Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md). In alternativa, contattare il proprio partner Microsoft per assistenza su come soddisfare i requisiti aziendali e del proprio paese.

L'azione **Mappa testo a conto** consente di impostare le mappature tra testo sui pagamenti e specifici conti debiti, crediti e contropartita in modo che i pagamenti vengano registrati nei conti specificati quando si contabilizzano le registrazioni riconciliazione pagamenti. Ciò è utile ad esempio per incassi e spese ricorrenti, quali acquisti frequenti di combustibile per auto o interessi e oneri bancari, che vengono riportati regolarmente sull'estratto conto bancario e non necessitano di un documento commerciale collegato. Vedere il passaggio 10 di seguito. Per ulteriori informazioni, vedere [Mappare il testo nei pagamenti ricorrenti a conti per la riconciliazione automatica](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).

Le righe di registrazione potrebbero non avere applicazioni suggerite. Ciò può essere dovuto a vari motivi, ad esempio in caso di un documento mancante o qualora un cliente abbia corrisposto un prezzo maggiore ed esista un importo in eccesso dopo aver collegato il pagamento su un'altra riga di registrazione. In questi casi, è possibile utilizzare l'azione **Trasferisci differenza a conto** per creare e registrare il movimento di contabilità generale mancante, ad esempio per un rimborso, a cui è necessario applicare il pagamento. Vedere il passaggio 11 di seguito. Per ulteriori informazioni, vedere [Riconciliare i pagamenti che non possono essere collegati](receivables-how-reconcile-payments-cannot-apply-auto.md).

Utilizzare la funzione **Collega automaticamente** quando si importa il feed bancario o il file della banca con transazioni di pagamento o quando lo si attiva, per collegare i pagamenti ai relativi movimenti aperti in base a una corrispondenza di testo in una riga di estratto conto bancario (riga di registrazione) con testo su uno o più movimenti aperti. Questa automazione si basa su regole definite nella pagina **Regole di collegamento pagamenti**, in cui si definisce anche se un suggerimento di collegamento deve essere rivisto. Per ulteriori informazioni, vedere [Impostare le regole per il collegamento automatico dei pagamenti](receivables-how-set-up-payment-application-rules.md).

Nelle righe di registrazione in cui un pagamento è stato collegato automaticamente a uno o più movimenti aperti, il campo **Affidabilità corrispondenza** contiene un valore **Bassa**, **Media** e **Alta** per indicare la qualità di corrispondenza di dati sulla quale si basa il collegamento del pagamento suggerito.

Alcuni collegamenti dei pagamenti richiedono la revisione, come definito dalla regola di corrispondenza utilizzata, ad esempio le righe con affidabilità corrispondenza **Bassa**. Altre righe richiedono la revisione e la modifica manuale perché è presente un valore nel campo **Differenza**. Per rivedere uno o più collegamenti dei pagamenti, scegliere il campo **Righe per la revisione** o **Righe con differenza** nel campo in basso. Verrà aperta la pagina **Revisione collegamento del pagamento** che mostra tutte le informazioni rilevanti sul cliente o sul fornitore a cui è collegato il pagamento, i dettagli corrispondenti e le azioni per elaborare la riga, ad esempio **Accetta applicazione**. Vedere i passaggi 7 e 8 di seguito.

Per ogni riga di registrazione nella pagina **Registrazione riconciliazione pagamenti** è possibile aprire la pagina **Collegamento pagamenti** per vedere tutti i movimenti aperti candidati per il pagamento e visualizzare, per ciascun movimento, informazioni dettagliate sulla corrispondenza dei dati su cui si basa un collegamento di pagamento. Qui è possibile collegare manualmente i pagamenti o applicare nuovamente i pagamenti che sono stati collegati automaticamente a un movimento aperto scorretto. Vedere il passaggio 10 di seguito. Per ulteriori informazioni, vedere [Rivedere o collegare i pagamenti in seguito al collegamento automatico](receivables-how-review-apply-payments-auto-application.md).

> [!NOTE]  
> È possibile avviare l'importazione delle transazioni bancarie contemporaneamente all'apertura della pagina **Registrazione riconciliazione pagamenti** per la registrazione esistente. Nella procedura riportata di seguito viene descritto come importare le transazioni bancarie nella pagina **Registrazione riconciliazione pagamenti** dopo avere creato nuove registrazioni.

## <a name="to-reconcile-payments-using-automatic-application"></a>Per riconciliare i pagamenti utilizzando il collegamento automatico
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Registrazioni riconciliazione pagamenti** e quindi scegliere il collegamento correlato.
2. Per utilizzare nuove registrazioni riconciliazione pagamenti, scegliere l'azione **Nuove registrazioni**.
3. Nella pagina **Lista C/C bancari pagamenti** selezionare il conto bancario per il quale si desidera riconciliare i pagamenti, quindi scegliere **OK**.
   Verrà aperta la pagina **Registrazione riconciliazione pagamenti** predisposta per il conto corrente bancario selezionato.
4. Scegliere l'azione **Importa transazioni bancarie**.
   Se il conto corrente bancario della registrazione selezionata non è impostato per importare transazioni bancarie, verrà aperta una finestra di dialogo per aiutare l'utente a compilare i campi pertinenti.
5. Nella pagina **Seleziona file da importare** selezionare il file contenente le transazioni bancarie dei pagamenti che si desidera riconciliare, quindi fare clic sul pulsante **Apri**.  
6. Se il servizio Envestnet Yodlee Bank Feeds è abilitato, nella pagina **Filtro rendiconto bancario** che viene visualizzata automaticamente viene specificato l'intervallo di date per gli estratti conto bancari che devono essere importati.

    La pagina **Registrazione riconciliazione pagamenti** viene compilata con righe per i pagamenti che rappresentano le transazioni bancarie nel rendiconto importato.

     Nelle righe dei pagamenti che sono stati collegati automaticamente ai relativi movimenti aperti, il campo **Affidabilità corrispondenza** include un valore tra **Bassa** e **Alta** a indicare la qualità della corrispondenza dei dati su cui si basa il collegamento del pagamento suggerito. Inoltre, i campi **Nome conto**, **Tipo conto** e **Nr. conto** vengono popolati con le informazioni relative al cliente o al fornitore a cui il pagamento è collegato.

    I collegamenti automatici, le qualità di corrispondenza e l'eventuale necessità di revisione delle righe sono definite da regole che è possibile modificare per rettificare i risultati. Per ulteriori informazioni, vedere [Impostare le regole per il collegamento automatico dei pagamenti](receivables-how-set-up-payment-application-rules.md).

7. Per rivedere, accettare/rimuovere o modificare manualmente più collegamenti dei pagamenti con un valore nel campo **Differenza**, scegliere l'azione **Linee con differenza** nella parte inferiore.

    Verrà aperta la pagina **Revisione collegamento del pagamento** che mostra il primo collegamento da rivedere. Il successivo collegamento da rivedere verrà visualizzato nella pagina durante l'elaborazione del precedente. Tutte le informazioni rilevanti sul cliente o sul fornitore a cui è collegato il pagamento, i dettagli corrispondenti e le azioni per elaborare la riga, ad esempio **Accetta applicazione** e **Collega manualmente**.

8. Per rivedere, accettare/rimuovere o modificare manualmente più collegamenti dei pagamenti impostati per essere rivisti, in base alla regola di collegamento dei pagamenti, selezionare l'azione **Righe per la revisione** in fondo. Viene presentata la stessa esperienza descritta per il passaggio 8

9. Per modificare il collegamento automatico, selezionare una riga di registrazione, quindi scegliere l'azione **Collega manualmente** per ricollegare o collegare il pagamento manualmente nella pagina **Collegamento pagamenti**. Per ulteriori informazioni, vedere [Esaminare o collegare i pagamenti in seguito al collegamento automatico](receivables-how-review-apply-payments-auto-application.md).

10. Selezionare una riga di registrazione scollegata per un incasso o una spesa ricorrente, ad esempio l'acquisto di carburante auto, quindi scegliere l'azione **Mappa testo a conto**. Per ulteriori informazioni, vedere [Mappare il testo nei pagamenti ricorrenti a conti per la riconciliazione automatica](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).

    Dopo avere completato la mappatura testo a conto dei pagamenti, scegliere l'azione **Collega manualmente**.

    Quando viene impostata una mappa da testo a conto, il collegamento del pagamento automatico risultante conterrà **Alta - Mappatura testo a conto** nel campo **Affidabilità corrispondenza**.

11. Per una riga di registrazione che non ha un collegamento suggerito perché non esiste alcun movimento contabile a cui può essere collegato, scegliere l'azione **Trasferisci differenza a conto** per creare e registrare il movimento C/G mancante a cui è necessario collegare il pagamento. Per ulteriori informazioni, vedere [Riconciliare i pagamenti che non possono essere collegati.](receivables-how-reconcile-payments-cannot-apply-auto.md)

10. Quando non è richiesta la revisione per altre righe e il campo **Differenza** è vuoto su tutte le righe, scegliere l'azione **Registra**, quindi scegliere una delle seguenti opzioni:

    - **Registra pagamenti e riconcilia conto bancario** - Per registrare i pagamenti come collegati e anche per chiudere i movimenti correlati dei conti correnti bancari come riconciliati.
    - **Registra solo pagamenti** - Per registrare solo i pagamenti come collegati, ma lasciare aperti i relativi movimenti contabili bancari. È necessario riconciliare il conto bancario separatamente, ad esempio: Per ulteriori informazioni, vedere [Riconciliare i conti correnti bancari](bank-how-reconcile-bank-accounts-separately.md).
    - Per visualizzare i risultati di una registrazione prima di eseguirla, scegliere l'azione **Report test**. Il report **Estratto conto bancario** si apre e mostra gli stessi campi nella parte inferiore della pagina **registrazione riconciliazione pagamenti**.

Quando si registrano le registrazioni della riconciliazione di pagamento, i movimenti aperti collegati vengono chiusi e i relativi conti cliente, fornitore o di contabilità generale vengono aggiornati. Per i pagamenti nelle righe di registrazione basate sul mapping testo a conto, vengono aggiornati i conti della contabilità generale, cliente e fornitore specificati. Per tutte le righe di registrazione, vengono creati i movimenti contabili di conti correnti bancari. Se si sceglie l'azione **Registra pagamenti e riconcilia conto bancario**, qualsiasi movimento COGE aperto correlato ai movimenti contabilità fornitori o clienti collegati verrà chiuso. Questo significa che il conto bancario viene riconciliato automaticamente per i pagamenti che si registrano con le scritture registrazioni e chiudere i movimenti contabili correlati.

È possibile confrontare il valore del campo **Saldo su conto bancario dopo la registrazione** con il valore del campo **Saldo finale estratto conto** per tenere traccia di quando il conto bancario viene riconciliato in base ai pagamenti che vengono registrati.

> [!NOTE]  
>   Se non si desidera riconciliare il conto bancario dalla pagina **Registrazione riconciliazione pagamenti**, è necessario utilizzare la pagina **Riconciliazioni C/C bancari**. Per ulteriori informazioni, vedere [Riconciliare i conti correnti bancari](bank-how-reconcile-bank-accounts-separately.md).

## <a name="see-also"></a>Vedere anche
[Gestione della contabilità clienti](receivables-manage-receivables.md)  
[Vendite](sales-manage-sales.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]