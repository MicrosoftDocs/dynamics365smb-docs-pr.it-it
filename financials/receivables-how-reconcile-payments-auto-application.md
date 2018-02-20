---
title: Utilizzare il collegamento automatico per riconciliare i pagamenti | Documenti Microsoft
description: Descrive come utilizzare la funzione automatica di collegamento per collegare i pagamenti o gli incassi ai movimenti aperti relativi e per riconciliare i pagamenti.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, direct payment posting, reconcile payment, expenses, cash receipts
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 79e7b23efb22f606351840ad613de9537fe30289
ms.contentlocale: it-it
ms.lasthandoff: 01/30/2018

---
# <a name="reconcile-payments-using-automatic-application"></a>Riconciliare i pagamenti utilizzando il collegamento automatico
La finestra **Registrazione riconciliazione pagamenti** specifica i pagamenti, sia in entrata che in uscita, registrati come transazioni nel conto bancario in linea e che possono essere collegati ai relativi movimenti aperti dei conti COGE, fornitore e cliente. Le righe delle registrazioni vengono compilate importando un rendiconto bancario come feed bancario o file della banca.

Una registrazione riconciliazione pagamenti è correlata a un conto bancario in [!INCLUDE[d365fin](includes/d365fin_md.md)] che riflette il conto bancario online in cui vengono registrate le transazioni di pagamento. Se si sceglie l'azione **Registra pagamenti e riconcilia conto bancario**, qualsiasi movimento COGE aperto correlato ai movimenti contabilità fornitori o clienti collegati verrà chiuso. Questo significa che il conto bancario viene riconciliato automaticamente per i pagamenti che si registrano con le scritture registrazioni e chiudere i movimenti contabili correlati.

Se si desidera importare i rendiconti bancari come feed bancari, è necessario innanzitutto abilitare il servizio Feed bancari di Envestnet Yodlee e successivamente collegare il conto corrente bancario al relativo conto bancario online. La registrazione riconciliazione pagamenti viene quindi rilevata automaticamente dai feed bancari quando si sceglie l'azione **Importa transazioni bancarie**. Inoltre, è possibile impostare un conto corrente bancario in modo che importi nuovi feed bancari ogni ora. Le transazioni per i pagamenti che sono già state contabilizzate come collegate e/o riconciliate non verranno importate. Per ulteriori informazioni, vedere [Impostare il servizio Feed bancari di Envestnet Yodlee](bank-how-setup-bank-statement-service.md).

Con l'azione **Mappa testo a conto** è possibile impostare le mappature tra testo sui pagamenti e specifici conti debiti, crediti e contropartita in modo che i pagamenti vengano registrati nei conti specificati quando si contabilizzano le registrazioni riconciliazione pagamenti. Vedere il passaggio 8. Per ulteriori informazioni, vedere [Mappare il testo nei pagamenti ricorrenti a conti per la riconciliazione automatica](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).

Una funzionalità simile esiste per riconciliare gli importi in eccesso nelle righe di riconciliazione pagamenti su base ad hoc. Per ulteriori informazioni, vedere [Riconciliare i pagamenti che non possono essere collegati.](receivables-how-reconcile-payments-cannot-apply-auto.md)

Utilizzare la funzione **Collega automaticamente** automaticamente quando si importa il feed bancario o il file di banca con transazioni di pagamento o quando lo si attiva, per collegare i pagamenti ai relativi movimenti aperti in base a una corrispondenza dei dati in una riga di registrazione con i dati di uno o più movimenti aperti.

Nelle righe di registrazione in cui un pagamento è stato collegato automaticamente a uno o più movimenti aperti, il campo **Affidabilità corrispondenza** contiene un valore tra Bassa e Alta per indicare la qualità di corrispondenza di dati sulla quale si basa il collegamento di pagamento suggerito. Inoltre, i campi **Tipo conto** e **Nr. conto** vengono popolati con le informazioni relative al cliente o al fornitore a cui il pagamento è collegato. Se è stata impostata una mappatura testo a conto, il collegamento automatico può ottenere un valore di affidabilità di corrispondenza di **Alta - Mappatura testo a conto**.

Per ogni riga di registrazione nella finestra **Registrazione riconciliazione pagamenti** è possibile aprire la finestra **Collegamento pagamenti** per vedere tutti i movimenti aperti candidati per il pagamento e visualizzare, per ciascun movimento, informazioni dettagliate sulla corrispondenza dei dati su cui si basa un collegamento di pagamento. Qui è possibile collegare manualmente i pagamenti o applicare nuovamente i pagamenti che sono stati collegati automaticamente a un movimento aperto scorretto. Per ulteriori informazioni, vedere [Esaminare o collegare i pagamenti in seguito al collegamento automatico](receivables-how-review-apply-payments-auto-application.md).

> [!NOTE]  
>   È possibile avviare l'importazione delle transazioni bancarie nello stesso momento in cui si apre la finestra **Registrazione riconciliazione pagamenti** per una registrazione riconciliazione pagamenti nella finestra **Registrazioni riconciliazione pagamenti**. Nella procedura riportata di seguito viene descritto come importare le transazioni bancarie nella finestra **Registrazione riconciliazione pagamenti** dopo avere creato nuove registrazioni.

## <a name="to-reconcile-payments-using-automatic-application"></a>Per riconciliare i pagamenti utilizzando il collegamento automatico
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Registrazioni riconciliazione pagamenti**, quindi scegliere il collegamento correlato.
2. Per utilizzare nuove registrazioni riconciliazione pagamenti, scegliere l'azione **Nuove registrazioni**.
3. Nella finestra **Lista C/C bancari pagamenti** selezionare il conto bancario per il quale si desidera riconciliare i pagamenti, quindi scegliere **OK**.
   Verrà aperta la finestra **Registrazione riconciliazione pagamenti** predisposta per il conto corrente bancario selezionato.
4. Scegliere l'azione **Importa transazioni bancarie**.
   Se il conto corrente bancario della registrazione selezionata non è impostato per importare transazioni bancarie, verrà aperta una finestra di dialogo per aiutare l'utente a compilare i campi pertinenti.
5. Nella finestra **Seleziona file da importare** selezionare il file contenente le transazioni bancarie dei pagamenti che si desidera riconciliare, quindi fare clic sul pulsante **Apri**.  
6. Se il Servizio rendiconti bancari è abilitato, nella finestra **Filtro rendiconto bancari**, che viene visualizzata automaticamente, viene specificato l'intervallo di date per i rendiconti bancari che devono essere importati.

    La finestra **Registrazione riconciliazione pagamenti** viene compilata con righe per i pagamenti che rappresentano le transazioni bancarie nel rendiconto importato.

    Nelle righe dei pagamenti che sono stati collegati automaticamente ai relativi movimenti aperti, il campo **Affidabilità corrispondenza** include un valore tra **Bassa** e **Alta** a indicare la qualità della corrispondenza dei dati su cui si basa il collegamento del pagamento suggerito. Inoltre, i campi **Tipo conto** e **Nr. conto** vengono popolati con le informazioni relative al cliente o al fornitore a cui il pagamento è collegato.
7. Selezionare una riga di registrazione, scegliere l'azione **Collega manualmente** per esaminare, ricollegare o collegare il pagamento manualmente nella finestra **Collegamento pagamenti**. Per ulteriori informazioni, vedere [Esaminare o collegare i pagamenti in seguito al collegamento automatico](receivables-how-review-apply-payments-auto-application.md).

    Una volta completato il collegamento manuale, il campo **Affidabilità corrispondenza** nella riga di registrazione elaborata manualmente contiene **Accettata**.
8. Selezionare una riga di registrazione scollegata per un incasso o una spesa ricorrente, ad esempio l'acquisto di carburante auto, quindi scegliere l'azione **Mappa testo a conto**. Per ulteriori informazioni, vedere [Mappare il testo nei pagamenti ricorrenti a conti per la riconciliazione automatica](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md)
9. Dopo avere completato la mappatura testo a conto dei pagamenti, scegliere l'azione **Collega manualmente**.
10. Una volta che tutti i pagamenti nelle righe di registrazione sono collegati correttamente o sono impostati per la registrazione diretta, scegliere l'azione **Registra**.

Quando si registrano le registrazioni della riconciliazione di pagamento, i movimenti aperti collegati vengono chiusi e i relativi conti cliente, fornitore o di contabilità generale vengono aggiornati. Per i pagamenti nelle righe di registrazione basate sul mapping testo a conto, vengono aggiornati i conti della contabilità generale, cliente e fornitore specificati. Per tutte le righe di registrazione, vengono creati i movimenti contabili di conti correnti bancari. Se si sceglie l'azione **Registra pagamenti e riconcilia conto bancario**, qualsiasi movimento COGE aperto correlato ai movimenti contabilità fornitori o clienti collegati verrà chiuso. Questo significa che il conto bancario viene riconciliato automaticamente per i pagamenti che si registrano con le scritture registrazioni e chiudere i movimenti contabili correlati.

È possibile confrontare il valore del campo **Saldo su conto bancario dopo la registrazione** con il valore del campo **Saldo finale estratto conto** per tenere traccia di quando il conto bancario viene riconciliato in base ai pagamenti che vengono registrati.

> [!NOTE]  
>   Se non si desidera riconciliare il conto bancario dalla finestra **Registrazione riconciliazione pagamenti**, è necessario utilizzare la finestra **Riconciliazioni C/C bancari**. Per ulteriori informazioni, vedere [Riconciliare i conti correnti bancari separatamente](bank-how-reconcile-bank-accounts-separately.md).

## <a name="see-also"></a>Vedi anche
[Gestione della contabilità clienti](receivables-manage-receivables.md)  
[Vendite](sales-manage-sales.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

