---
title: Riconciliare i pagamenti utilizzando il collegamento automatico
description: Descrive come riconciliare i pagamenti utilizzando l'applicazione automatica per applicare pagamenti o incassi ai movimenti aperti correlati.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'payment process, direct payment posting, reconcile payment, expenses, cash receipts'
ms.search.form: '389, 1290, 1294, 1287'
ms.date: 06/22/2022
ms.author: bholtorf
---
# Riconciliare i pagamenti utilizzando il collegamento automatico

La pagina **Giornale di riconciliazione pagamenti** specifica i pagamenti, in entrata o in uscita, che sono stati registrati come transazioni sul tuo conto bancario online o su un servizio di pagamento. È possibile applicare i pagamenti ai movimenti contabili aperti relativi a clienti, fornitori e conti bancari. Compila il giornale di registrazione importando un estratto conto come feed bancario o file della banca o inserendo manualmente le transazioni effettuate sul servizio di pagamento.

> [!NOTE]
> La pagina offre funzionalità di corrispondenza automatica che collega i pagamenti ai relativi movimenti aperti in base a una corrispondenza di dati su una riga di estratto conto bancario (riga di registrazione) con i dati su uno o più movimenti aperti. Si noti che è possibile sovrascrivere i collegamenti automatici suggeriti ed è possibile scegliere di non utilizzare il collegamento automatico per nulla. Per ulteriori informazioni, vedere il passaggio 7.

Un giornale di registrazione di riconciliazione pagamenti è correlato a un conto bancario in [!INCLUDE[prod_short](includes/prod_short.md)]. Il conto bancario rappresenta il conto bancario online dove vengono registrate le transazioni di pagamento. Se si sceglie l'azione **Registra pagamenti e riconcilia conto bancario**, qualsiasi movimento COGE aperto correlato ai movimenti contabilità fornitori o clienti collegati verrà chiuso. Il conto bancario verrà riconciliato automaticamente per i pagamenti registrati con il giornale di registrazione.

Se usi la pagina **Giornale di riconciliazione pagamenti** per registrare e applicare i pagamenti dei clienti, puoi impostare il giornale di registrazione per utilizzare una numerazione specifica. Successivamente, puoi specificare la numerazione nel campo **Numerazione riconciliazione pagamenti** in un conto bancario. L'uso di una numerazione dedicata può semplificare l'identificazione di tutti i movimenti che sono stati registrati tramite il giornale di registrazione.

Analogamente ad altri giornali di registrazione, quando si correggono i movimenti registrati è possibile stornare i movimenti registrati tramite il giornale di registrazione di riconciliazione pagamenti dalla pagina **Registro C/G**. Ad esempio, potresti voler stornare i movimenti per i pagamenti che hai applicato al cliente sbagliato. È necessario prima annullare l'applicazione dei movimenti contabili cliente registrati. Quindi puoi usare l'azione **Storna registro** nella pagina **Registro C/G** per stornare il giornale di registrazione che ha registrato i pagamenti. In alternativa, sulla pagina **Registrazioni CoGe contabilizzate**, è possibile utilizzare l'azione **Copia le righe selezionate nel giornale di registrazione** per stornare righe specifiche dal giornale di registrazione di riconciliazione pagamenti registrati. 

Quando si utilizza l'applicazione automatica, [!INCLUDE[prod_short](includes/prod_short.md)] riconosce i movimenti contabili bancari che sono già stati registrati, il che aiuta a prevenire la doppia registrazione.

È possibile importare transazioni bancarie sotto forma di file con estensione CSV o in altro formato fornito dalla banca. Se vuoi importare gli estratti conto bancari come feed bancari, devi innanzitutto abilitare un servizio di integrazione bancaria dedicato e successivamente collegare il conto corrente bancario al relativo conto bancario online. La registrazione riconciliazione pagamenti viene quindi rilevata automaticamente dai feed bancari quando si sceglie l'azione **Importa transazioni bancarie**. Inoltre, è possibile impostare un conto corrente bancario in modo che importi nuovi feed bancari ogni ora. Le transazioni per i pagamenti che sono già state contabilizzate come collegate e/o riconciliate non verranno importate. Per ottenere tali transazioni, puoi utilizzare il servizio Envestnet Yodlee Bank Feeds, preinstallato nelle versioni di [!INCLUDE[d365fin](includes/d365fin_md.md)] di alcuni paesi. Per ulteriori informazioni, vedere [Impostare il servizio Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md). In alternativa, contatta il tuo partner Microsoft per assistenza su come soddisfare i requisiti aziendali e del tuo paese.

L'azione **Mappa testo a conto** consente di impostare le mappature tra testo sui pagamenti e specifici conti debiti, crediti e contropartita in modo che i pagamenti vengano registrati nei conti specificati quando si contabilizzano le registrazioni riconciliazione pagamenti. Ciò è utile ad esempio per incassi e spese ricorrenti, quali acquisti frequenti di combustibile per auto o interessi e oneri bancari, che vengono riportati regolarmente sull'estratto conto bancario e non necessitano di un documento commerciale collegato. Vedi il passaggio 10. Per ulteriori informazioni, vedi [Mappare il testo nei pagamenti ricorrenti a conti per la riconciliazione automatica](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).

Le righe del giornale di registrazione potrebbero non avere un'applicazione suggerita, il che può verificarsi per vari motivi. Ad esempio, perché un documento è mancante o un cliente ha pagato in eccesso e c'è un importo in eccesso dopo aver applicato il pagamento su un'altra riga del giornale di registrazione. In questi casi, è possibile utilizzare l'azione **Trasferisci differenza a conto** per creare e registrare il movimento di contabilità generale mancante, ad esempio per un rimborso, a cui è necessario applicare il pagamento. Vedi il passaggio 11. Per ulteriori informazioni, vedi [Riconciliare i pagamenti che non possono essere collegati](receivables-how-reconcile-payments-cannot-apply-auto.md).

Utilizzare la funzione **Collega automaticamente** quando si importa il feed bancario o il file della banca con transazioni di pagamento o quando lo si attiva, per collegare i pagamenti ai relativi movimenti aperti in base a una corrispondenza di testo in una riga di estratto conto bancario (riga di registrazione) con testo su uno o più movimenti aperti. Questa automazione si basa su regole definite nella pagina **Regole di collegamento pagamenti**, in cui si definisce anche se un suggerimento di collegamento deve essere rivisto. Per ulteriori informazioni, vedere [Impostare le regole per il collegamento automatico dei pagamenti](receivables-how-set-up-payment-application-rules.md).

Nelle righe di registrazione in cui un pagamento è stato collegato automaticamente a uno o più movimenti aperti, il campo **Affidabilità corrispondenza** contiene un valore **Bassa**, **Media** e **Alta** per indicare la qualità di corrispondenza di dati sulla quale si basa il collegamento del pagamento suggerito.

Alcuni collegamenti dei pagamenti richiedono la revisione, come definito dalla regola di corrispondenza utilizzata, ad esempio le righe con affidabilità corrispondenza **Bassa**. Altre righe richiedono la revisione e la modifica manuale perché è presente un valore nel campo **Differenza**. Per rivedere uno o più collegamenti dei pagamenti, scegliere il campo **Righe per la revisione** o **Righe con differenza** nel campo in basso. Verrà aperta la pagina **Revisione collegamento del pagamento** che mostra tutte le informazioni rilevanti sul cliente o sul fornitore a cui è collegato il pagamento, i dettagli corrispondenti e le azioni per elaborare la riga, ad esempio **Accetta applicazione**. Vedi i passaggi 7 e 8

Per ogni riga di registrazione nella pagina **Registrazione riconciliazione pagamenti** è possibile aprire la pagina **Collegamento pagamenti** per vedere tutti i movimenti aperti candidati per il pagamento e visualizzare, per ciascun movimento, informazioni dettagliate sulla corrispondenza dei dati su cui si basa un collegamento di pagamento. Qui è possibile collegare manualmente i pagamenti o applicare nuovamente i pagamenti che sono stati collegati automaticamente a un movimento aperto scorretto. Vedi il passaggio 10. Per ulteriori informazioni, vedi [Rivedere o collegare i pagamenti in seguito al collegamento automatico](receivables-how-review-apply-payments-auto-application.md).

> [!NOTE]  
> È possibile avviare l'importazione delle transazioni bancarie contemporaneamente all'apertura della pagina **Registrazione riconciliazione pagamenti** per la registrazione esistente. Nella procedura riportata di seguito viene descritto come importare le transazioni bancarie nella pagina **Registrazione riconciliazione pagamenti** dopo avere creato nuove registrazioni.

## Per riconciliare i pagamenti utilizzando il collegamento automatico
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Registrazioni riconciliazione pagamenti**, quindi scegli il collegamento correlato.
2. Per utilizzare nuove registrazioni riconciliazione pagamenti, scegliere l'azione **Nuove registrazioni**.
3. Nella pagina **Lista C/C bancari pagamenti** selezionare il conto bancario per il quale si desidera riconciliare i pagamenti, quindi scegliere **OK**.
   Verrà aperta la pagina **Registrazione riconciliazione pagamenti** predisposta per il conto corrente bancario selezionato.
4. Scegliere l'azione **Importa transazioni bancarie**.
   Se il conto bancario per il giornale di registrazione selezionato non è impostato per l'importazione di transazioni bancarie, [!INCLUDE[d365fin](includes/d365fin_md.md)] ti aiuterà a farlo.
5. Nella pagina **Seleziona file da importare** selezionare il file contenente le transazioni bancarie dei pagamenti che si desidera riconciliare, quindi fare clic sul pulsante **Apri**.  
6. Se il servizio Envestnet Yodlee Bank Feeds è abilitato, nella pagina **Filtro rendiconto bancario** che viene visualizzata automaticamente viene specificato l'intervallo di date per gli estratti conto bancari che devono essere importati.

    La pagina **Registrazione riconciliazione pagamenti** viene compilata con righe per i pagamenti che rappresentano le transazioni bancarie nel rendiconto importato.

     Nelle righe per i pagamenti che sono stati applicati automaticamente ai relativi movimenti aperti, il campo **Affidabilità corrispondenza** indica la qualità della corrispondenza dei dati su cui si basa la richiesta di pagamento suggerita. Inoltre, i campi **Nome conto**, **Tipo conto** e **Nr. conto** mostrano le informazioni relative al cliente o al fornitore a cui il pagamento è collegato.

    I collegamenti automatici, le qualità di corrispondenza e l'eventuale necessità di revisione delle righe sono definite da regole. Puoi modificare le regole per regolare i risultati. Per ulteriori informazioni, vedere [Impostare le regole per il collegamento automatico dei pagamenti](receivables-how-set-up-payment-application-rules.md).

7. Per rivedere, accettare/rimuovere o modificare manualmente più collegamenti dei pagamenti con un valore nel campo **Differenza**, scegliere l'azione **Linee con differenza** nella parte inferiore.

    Viene aperta la pagina **Revisione collegamento del pagamento** che mostra il primo collegamento da rivedere. Il successivo collegamento da rivedere verrà visualizzato nella pagina durante l'elaborazione del precedente. La revisione include le informazioni sul cliente o sul fornitore a cui è collegato il pagamento, i dettagli corrispondenti e le azioni per elaborare la riga, ad esempio **Accetta applicazione** e **Collega manualmente**.

8. Per rivedere, accettare o rimuovere o modificare manualmente più applicazioni di pagamento che la regola ha impostato per la revisione, scegli l'azione **Righe per la revisione**. 

9. Per modificare il collegamento automatico, selezionare una riga di registrazione, quindi scegliere l'azione **Collega manualmente** per ricollegare o collegare il pagamento manualmente nella pagina **Collegamento pagamenti**. Per ulteriori informazioni, vedere [Esaminare o collegare i pagamenti in seguito al collegamento automatico](receivables-how-review-apply-payments-auto-application.md).

10. Selezionare una riga di registrazione scollegata per un incasso o una spesa ricorrente, ad esempio l'acquisto di carburante auto, quindi scegliere l'azione **Mappa testo a conto**. Per ulteriori informazioni, vedere [Mappare il testo nei pagamenti ricorrenti a conti per la riconciliazione automatica](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).

    Dopo avere completato la mappatura testo a conto dei pagamenti, scegli l'azione **Collega manualmente**.

    Quando viene impostata una mappatura da testo a conto, il collegamento del pagamento automatico risultante conterrà **Alta - Mappatura testo a conto** nel campo **Affidabilità corrispondenza**.

11. Per una riga di registrazione che non ha un collegamento suggerito perché non esiste alcun movimento contabile a cui può essere collegato, scegli l'azione **Trasferisci differenza a conto** per creare e registrare il movimento C/G mancante a cui è necessario collegare il pagamento. Per ulteriori informazioni, vedi [Riconciliare i pagamenti che non possono essere collegati.](receivables-how-reconcile-payments-cannot-apply-auto.md)

12. Quando non è richiesta la revisione per altre righe e il campo **Differenza** è vuoto su tutte le righe, scegliere l'azione **Registra**, quindi scegliere una delle seguenti opzioni:

    - **Registra pagamenti e riconcilia conto bancario** - Per registrare i pagamenti come collegati e anche per chiudere i movimenti correlati dei conti correnti bancari come riconciliati.
    - **Registra solo pagamenti** - Per registrare solo i pagamenti come collegati, ma lasciare aperti i relativi movimenti contabili bancari. È necessario riconciliare il conto bancario separatamente, ad esempio: Per ulteriori informazioni, vedere [Riconciliare i conti correnti bancari](bank-how-reconcile-bank-accounts-separately.md).
    - Per visualizzare i risultati di una registrazione prima di eseguirla, scegliere l'azione **Report test**. Il report **Estratto conto bancario** si apre e mostra gli stessi campi nella parte inferiore della pagina **registrazione riconciliazione pagamenti**.

Quando si registra il giornale di registrazione di riconciliazione pagamenti, i movimenti aperti applicati vengono chiusi. I conti cliente, fornitore o contabilità generale vengono aggiornati. Per i pagamenti nelle righe di registrazione basate sul mapping testo a conto, vengono aggiornati i conti della contabilità generale, cliente e fornitore specificati. Per tutte le righe di registrazione, vengono creati i movimenti contabili di conti correnti bancari. Se si sceglie l'azione **Registra pagamenti e riconcilia conto bancario**, qualsiasi movimento COGE aperto correlato ai movimenti contabilità fornitori o clienti collegati verrà chiuso. Questo significa che il conto bancario viene riconciliato automaticamente per i pagamenti che si registrano con le scritture registrazioni e chiudere i movimenti contabili correlati.

È possibile confrontare il valore del campo **Saldo su conto bancario dopo la registrazione** con il valore del campo **Saldo finale estratto conto** per tenere traccia di quando il conto bancario viene riconciliato in base ai pagamenti che vengono registrati.

> [!NOTE]  
>   Se non si desidera riconciliare il conto bancario dalla pagina **Registrazione riconciliazione pagamenti**, è necessario utilizzare la pagina **Riconciliazioni C/C bancari**. Per ulteriori informazioni, vedere [Riconciliare i conti correnti bancari](bank-how-reconcile-bank-accounts-separately.md).

## Vedi il relativo [training Microsoft](/training/modules/use-journals-dynamics-365-business-central/)

## Vedere anche

[Gestione della contabilità clienti](receivables-manage-receivables.md)  
[Vendite](sales-manage-sales.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
