---
title: Riconciliare i conti correnti bancari separatamente| Documenti Microsoft
description: "Descrive come il valore di magazzino è riconciliato con la contabilità generale."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account balance, bank statement
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: b14f779a34f44bc8c41bb13b42ec06bea359c9b7
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="reconcile-bank-accounts-separately"></a>Riconciliare i conti correnti bancari separatamente
Per riconciliare i conti correnti bancari in [!INCLUDE[d365fin](includes/d365fin_md.md)] con estratti conto ricevuti dalla banca, è necessario compilare le righe nella finestra **Riconciliazioni C/C bancari**.

> [!NOTE]  
>   È inoltre possibile riconciliare i conti correnti bancari nella finestra **Registrazione riconciliazione pagamenti**. Se si sceglie l'azione **Registra pagamenti e riconcilia conto bancario**, qualsiasi movimento COGE aperto correlato ai movimenti contabilità fornitori o clienti collegati verrà chiuso. Questo significa che il conto bancario viene riconciliato automaticamente per i pagamenti che si registrano con le scritture registrazioni e chiudere i movimenti contabili correlati. Per ulteriori informazioni, vedere [Riconciliare i pagamenti utilizzando il collegamento automatico](receivables-how-reconcile-payments-auto-application.md).

Per abilitare l'importazione degli estratti conto bancari come feed bancari, è necessario innanzitutto abilitare il servizio Feed bancari di Envestnet Yodlee e successivamente collegare i conti correnti bancari ai conti bancari online correlati. Per ulteriori informazioni, vedere [Impostare il servizio Feed bancari di Envestnet Yodlee](bank-how-setup-bank-statement-service.md).

Le righe nella finestra **Riconciliazioni C/C bancari** sono suddivise in due riquadri. Il riquadro **Righe rendiconto bancario** mostra le transazioni bancarie importate o movimenti contabili con pagamenti scaduti. Il riquadro **Mov. contabili C/C bancari** mostra i movimenti contabili del conto corrente bancario.

L'attività di ricerca e collegamento dei movimenti da riconciliare è denominata *corrispondenza*. È possibile scegliere se eseguire la corrispondenza automaticamente utilizzando la funzione **Corrispondenza automatica**. In alternativa, è possibile selezionare manualmente le righe in entrambi i riquadri per collegare ogni riga del rendiconto bancario a uno o più movimenti contabili di conti correnti bancari, quindi utilizzare la funzione di **Corrispondenza manuale**. La casella di controllo **Collegato** è selezionata nelle righe in cui i movimenti corrispondono.

È possibile compilare il riquadro **Righe rendiconto bancario** nella finestra **Riconciliazioni C/C bancari** nei seguenti modi:

* Automaticamente, utilizzando la funzione **Importa rendiconto bancario** per compilare le righe a seconda degli importi degli estratti conto bancari basati su un file assegnato dalla banca.
* Manualmente, utilizzando la funzione **Suggerisci righe** per compilare le righe con i movimenti contabili per fatture con pagamenti scaduti.

Se il valore nel campo **Saldo totale** del riquadro **Righe rendiconto bancario** è pari al valore nel campo **Saldo da riconciliare** del riquadro **Mov. contabili C/C bancari**, è possibile scegliere l'azione **Registra** per riconciliare i movimenti contabili di conti correnti bancari collegati. Tutti i movimenti contabili di conti correnti bancari non collegati rimarranno nella finestra, indicante che i pagamenti elaborati per il conto corrente bancario non sono riflessi nell'ultimo rendiconto bancario o che alcuni pagamenti sono stati ricevuti tramite assegni.

> [!NOTE]  
>   Se le righe del rendiconto bancario sono collegate ai movimenti contabili assegni, non è possibile utilizzare le funzioni di corrispondenza. È invece necessario scegliere l'azione **Collega movimenti** quindi selezionare il movimento contabile degli assegni pertinente da applicare la corrispondenza alla riga del rendiconto bancario.

## <a name="to-fill-bank-reconciliation-lines-by-importing-a-bank-statement"></a>Per compilare le righe di riconciliazione bancaria importando un estratto conto bancario
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Riconciliazione C/C bancari**, quindi scegliere il collegamento correlato.
2. Scegliere l'azione **Nuovo**.
3. Nel campo **Nr. conto corrente** selezionare il conto corrente bancario importante. I movimenti contabili di conti correnti bancari esistenti nel conto corrente bancario vengono visualizzati nel riquadro **Mov. contabili C/C bancari**.
4. Nel campo **Data Estratto Conto** immettere la data dell'estratto conto.
5. Nel campo **Saldo Finale Estratto Conto** immettere il saldo che appare sull'estratto conto.
6. Se si dispone di un file dell'estratto conto, selezionare l'azione **Importa rendiconto bancario**.
7. Individuare il file, quindi selezionare il pulsante **Apri** per importare le transazioni bancarie nelle righe della finestra **Riconciliazioni C/C bancari**.

## <a name="to-fill-bank-reconciliation-lines-with-the-suggest-lines-function"></a>Per compilare le righe di riconciliazione con la funzione Suggerisci righe
1. Nella finestra **Riconciliazioni C/C bancari** scegliere l'azione **Suggerisci righe**.
2. Nel campo **Data Inizio** immettere la prima data di registrazione dei movimenti contabili che devono essere riconciliati.
3. Nel campo **Data di fine** immettere l'ultima data di registrazione dei movimenti contabili che devono essere riconciliati.
4. Se si desidera suggerire movimenti contabili di assegni anziché quelli corrispondenti relativi a banche, selezionare il campo **Includi assegni**.
5. Scegliere il pulsante **OK**.

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-automatically"></a>Per associare automaticamente le righe del rendiconto bancario con i movimenti contabili di conti correnti bancari
1. Nella finestra **Riconciliazioni C/C bancari** scegliere l'azione **Corrispondenza automatica**. Verrà visualizzata la finestra **Movimenti bancari corrispondenti**.
2. Nel campo **Tolleranza data transazione (giorni)** specificare l'intervallo di giorni prima e dopo la data di registrazione del movimento contabile del conto corrente bancario entro cui la funzione eseguirà la ricerca delle date di transazione corrispondenti nel rendiconto bancario.

    Se si immette 0 o si lascia vuoto il campo, la funzione di **Corrispondenza automatica** cercherà solo le date di transazioni di corrispondenza sulla data di registrazione del movimento contabile di conto corrente bancario.
3. Scegliere il pulsante **OK**.

    Tutte le righe del rendiconto bancario e i movimenti contabili di conti correnti bancari che possono corrispondere vengono modificati con carattere verde e la casella di controllo **Collegato** è selezionata.
4. Per rimuovere una corrispondenza, selezionare la riga dell'estratto conto bancario quindi selezionare l'azione **Rimuovi corrispondenza**.

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-manually"></a>Per associare manualmente le righe del rendiconto bancario con i movimenti contabili di conti correnti bancari
1. Nella finestra **Riconciliazioni C/C bancari** selezionare una riga non collegata nel riquadro **Righe rendiconto bancario**.
2. Nel riquadro **Mov. contabili C/C bancari** selezionare uno o più movimenti contabili del conto bancario che possono corrispondere alla riga selezionata del rendiconto bancario. Per selezionare più righe, tenere premuto il tasto CTRL.
3. Selezionare l'azione **Corrispondenza manuale**.

    La riga del rendiconto bancario selezionata e i movimenti contabili di conti correnti bancari selezionati cambiano in un tipo di carattere verde e la casella di controllo **Collegato** nel riquadro di destra viene selezionata.
4. Ripetere i passaggi da 1 a 3 per tutte le righe del rendiconto bancario non associate.
5. Per rimuovere una corrispondenza, selezionare la riga dell'estratto conto bancario quindi selezionare l'azione **Rimuovi corrispondenza**.

## <a name="to-create-missing-ledger-entries-to-match-bank-transactions-with"></a>Per creare i movimenti contabili mancanti per applicare la corrispondenza con le transazioni bancarie
Talvolta un estratto conto contiene importi corrispondenti ad interessi o all'addebito di commissioni. Per tali transazioni bancarie non può essere effettuata alcuna corrispondenza perché nessun movimento contabile collegato è presente in [!INCLUDE[d365fin](includes/d365fin_md.md)]. È quindi necessario registrare una riga di registrazione per ogni transazione per creare un movimento contabile collegato per cui può essere effettuata una corrispondenza.

1. Nella finestra **Riconciliazioni C/C bancari** scegliere l'azione **Trasferisci a registrazioni COGE**.  
2. Nella finestra **Trans. ric. banc. in reg. gen.** specificare quali registrazioni COGE utilizzare, quindi scegliere **OK**.

    Verrà visualizzata la finestra **Registrazioni COGE** contenente le nuove righe registrazioni per tutte le righe rendiconto bancario con movimenti contabili mancanti.
3. Completare la riga di registrazione con le informazioni rilevanti, ad esempio il conto profitti/perdite. Per ulteriori informazioni, vedere [Utilizzo delle registrazioni COGE](ui-work-general-journals.md).  
4. Scegliere l'azione **Registra**.

    Quando il movimento è stato registrato, continuare per associare a esso la transazione bancaria.
5. Aggiornare o riaprire la finestra **Riconciliazioni C/C bancari**. Il nuovo movimento contabile verrà visualizzato nel riquadro **Mov. contabili C/C bancari**.
6. Effettuare la corrispondenza della riga dell'estratto conto con il movimento contabile del conto corrente bancario, manualmente o automaticamente.

## <a name="see-also"></a>Vedi anche
[Gestione di conti correnti bancari](bank-manage-bank-accounts.md)  
[Impostazione delle attività bancarie](bank-setup-banking.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

