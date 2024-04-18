---
title: Riconciliare conti correnti bancari con l'assistenza per la riconciliazione
description: Scopri come usare Copilot per riconciliare i conti correnti bancari in Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.collection:
  - get-started
  - bap-ai-copilot
ms.date: 03/27/2024
ms.custom: bap-template
---

# <a name="reconcile-bank-accounts-with-copilot-preview"></a>Riconciliare i conti correnti bancari con Copilot (anteprima)

[!INCLUDE[preview-banner](includes/preview-banner.md)]

Questo articolo spiega come utilizzare l'assistenza per la riconciliazione dei conti correnti bancari per riconciliare le transazioni bancarie con movimenti contabili in Business Central.

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

## <a name="about-bank-account-reconciliation-assist"></a>Informazioni sull'assistenza per la riconciliazione dei conti correnti bancari

L'assistenza per la riconciliazione dei conti correnti bancari è un insieme di funzionalità basate sull'intelligenza artificiale che ti assistono nella riconciliazione dei conti correnti bancari. L'assistenza per la riconciliazione dei conti correnti bancari ti offre due attività distinte tramite Copilot:

- Creazione migliorata delle corrispondenze tra transazioni e movimenti contabili

   È possibile che tu conosca già l'azione **Corrispondenza automatica** nella pagina **Riconciliazioni C/C bancari** che crea automaticamente corrispondenze tra la maggior parte delle transazioni bancarie e i movimenti contabili. Definiamo questa operazione come *corrispondenza automatica*. Sebbene la corrispondenza automatica funzioni correttamente, gli algoritmi che utilizza a volte possono generare molte transazioni senza corrispondenze. Copilot utilizza la tecnologia IA per ispezionare le transazioni rimanenti e identificare più corrispondenze, in base a date, importi e descrizioni. Ad esempio, se più fatture sono state pagate come un'unica somma forfettaria da un cliente, Copilot riconcilia la singola riga dell'estratto conto con più movimenti contabili delle fatture.

   Vedi [Riconciliare i conti correnti bancari con Copilot](#reconcile-bank-accounts-with-copilot).

- Conti di contabilità generale suggeriti

  Per le transazioni bancarie residue per le quali non è possibile creare corrispondenze con i movimenti contabili, Copilot confronta la descrizione della transazione con i nomi dei conti C/G, suggerendo il conto C/G più probabile in cui effettuare la pubblicazione. Ad esempio, Copilot potrebbe suggerire che le transazioni con la descrizione "Arresto carburante 24" vengano pubblicate nel conto "Trasporti".
  
   Vedi [Trasferire transazioni bancarie senza corrispondenze a conti di contabilità generale suggeriti](#transfer-unmatched-bank-transactions-to-suggested-general-ledger-accounts).

## <a name="prerequisites"></a>Prerequisiti

- L'assistenza per la riconciliazione dei conti correnti bancari è attivata. Questa attività è eseguita da un amministratore. [Scopri di più sulla configurazione delle funzionalità di Copilot e IA](enable-ai.md).
- I conti correnti bancari in Business Central che vuoi riconciliare sono collegati a un conto corrente bancario online o impostati con il formato di importazione dell'estratto conto. 
- Hai familiarità con la riconciliazione dei conti correnti bancari in Business Central come descritto in [Riconciliare i conti correnti bancari](bank-how-reconcile-bank-accounts-separately.md). 

<!--H2s. Required. A how-to article explains how to do a task. The bulk of each H2 should be a procedure.-->
## <a name="reconcile-bank-accounts-with-copilot"></a>Riconciliare i conti correnti bancari con Copilot

<!-- Similar to the **Match Automatically** capability on the **Bank Acc. Reconciliation** page, Bank account reconciliation assist can also automatically matches transactions in banks statements with bank entries. The difference is that **Match Automatically** uses a native rules-based algorithm, while Bank account reconciliation assist is based AI technology though Copilot. Bank account reconciliation assist is intended to supplement the **Match Automatically** capability. While **Match Automatically** is fairly successful at matching transactions, there are some instances where it can't&mdash;which is where Bank account reconciliation assist comes. By using the **Reconcile with Copilot** action on **Bank Acc. Reconciliation** page, you can find even more matches.-->

Copilot nella riconciliazione dei conti bancari è destinato a essere utilizzato come supplemento all'operazione di corrispondenza automatica. Per questo motivo, quando usi Copilot, l'operazione di corrispondenza automatica viene eseguita per prima per effettuare le corrispondenze iniziali. Viene quindi eseguito Copilot per provare a creare corrispondenze per le transazioni che l'operazione di corrispondenza automatica non ha gestito.   

Esistono due approcci per riconciliare i conti correnti bancari con Copilot. Puoi usare Copilot per avviare una nuova riconciliazione su un conto corrente bancario, direttamente dall'elenco **Riconciliazione conto corrente bancario** oppure puoi usare Copilot per una riconciliazione nuova o esistente nella scheda **Riconciliazioni C/C bancari**.

# [Dall'elenco di riconciliazioni di conti correnti bancari](#tab/fromlist) 

Con questo approccio, crei e riconcili da zero una nuova riconciliazione del conto corrente bancario. Questo approccio richiede la selezione del conto corrente bancario e l'importazione del file dell'estratto conto, se il conto corrente bancario non è collegato a un conto online.

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immetti **Riconciliazioni conti correnti bancari**, quindi scegli il collegamento correlato. 
1. Seleziona l'azione **Riconcilia con Copilot** per aprire la finestra **Riconcilia con Copilot**.
1. Imposta il campo **Esegui la riconciliazione per questo conto corrente bancario** sul conto corrente bancario che vuoi riconciliare.

   ![Finestra Riconcilia con Copilot per la riconciliazione da zero](media/reconcile-bank-accounts-new-copilot.svg) 
 
1. Se il conto corrente bancario selezionato non è collegato a un conto corrente bancario in linea, devi importare il file dell'estratto conto. Per importare il file, seleziona il valore nel campo **Utilizza dati delle transazioni da** o seleziona il pulsante della graffetta accanto al pulsante **Genera**. Quindi, utilizza **Seleziona il file da importare** per importare il file dell'estratto conto trascinandolo dal tuo dispositivo o navigando sul tuo dispositivo.
1. Per eseguire la riconciliazione con Copilot, seleziona **Genera**.

   Copilot inizia a generare le corrispondenze proposte. Al termine, la finestra Riconcilia con Copilot visualizza i risultati del processo di creazione di corrispondenze.

1. Esamina le corrispondenze proposte come descritto nella sezione seguente.

# [Dalla scheda di una riconciliazione di conti correnti bancari](#tab/fromcard) 

Con questo approccio, puoi utilizzare Copilot per una nuova riconciliazione del conto corrente bancario creata manualmente o modificando una riconciliazione esistente. 


1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](media/ui-search/search_small.png "Dimmi cosa vuoi fare"), immetti **Riconciliazioni conti correnti bancari**, quindi scegli il collegamento correlato. 
1. Effettua uno dei seguenti passaggi:

   - Seleziona **Nuovo** per avviare una nuova riconciliazione. 
   - Seleziona e apri una riconciliazione esistente dall'elenco.
1. Nella scheda **Riconciliazioni C/C bancari** seleziona **Riconcilia con Copilot**

   ![Azione Riconcilia con Copilot nella scheda Riconciliazioni C/C bancari](media/bank-reconciliation-copilot-card.svg) 

   Copilot inizia a generare le corrispondenze proposte. Al termine, la finestra **Riconcilia con Copilot** visualizza i risultati del processo di creazione di corrispondenze. 

1. Esamina le corrispondenze proposte come descritto nella sezione seguente. 
---

### <a name="review-save-or-discard-proposed-matches"></a>Esaminare, salvare o eliminare le corrispondenze proposte

Dopo aver eseguito Copilot, la finestra **Riconcilia con Copilot** mostra i risultati dettagliati, incluse eventuali corrispondenze proposte. A questo punto, nessuna corrispondenza proposta da Copilot è stata salvata, quindi ti offre l'opportunità di esaminare le proposte e di salvarle o scartarle come preferisci.

![Finestra Riconcilia con Copilot con le corrispondenze proposte](media/bank-reconciliation-copilot-window.png) 

La finestra Copilot è suddivisa in due sezioni. La sezione superiore fornisce alcuni dettagli generali sul risultato, come descritto nella tabella seguente.  La sezione **Proposte risultanti** inferiore elenca le corrispondenze suggerite da Copilot.

|Campo|Descrizione|
|-|-|
|Corrispondenza automatica|Specifica quante righe nell'estratto conto hanno corrispondenze create dall'operazione di corrispondenza automatica. Seleziona il valore per visualizzare la scheda di riconciliazione.  |
|Copilot corrispondente|Specifica per quante righe nell'estratto conto sono presenti corrispondenze proposte da Copilot. Puoi visualizzare i dettagli delle corrispondenze nella sezione **Corrispondenze proposte**.|
|Saldo finale estratto conto|Specifica il saldo finale visualizzato nell'estratto conto per il quale stai eseguendo la riconciliazione|
|Pubblica se completamente applicato|Attiva questo interruttore se desideri pubblicare automaticamente la riconciliazione del conto corrente bancario quando tutte le righe (100%) hanno corrispondenze e hai selezionato **Conservalo**.|

#### <a name="save-or-discard-proposed-matches"></a>Salvare o eliminare le corrispondenze proposte

Nella sezione **Proposte risultanti**, esamina le corrispondenze suggerite riga per riga, quindi intraprendi l'azione appropriata:

- Per eliminare una singola corrispondenza proposta, selezionala nell'elenco, quindi seleziona l'azione **Elimina riga**.

- Per eliminare tutte le corrispondenze proposte e chiudere la finestra di Copilot, seleziona il pulsante di eliminazione (cestino) ![Icona del cestino per l'eliminazione di tutte le proposte di Copilot per la riconciliazione del conto corrente bancario](media/copilot-delete-trash-can.png) accanto al pulsante **Conservalo** nella parte inferiore della finestra.

- Per pubblicare automaticamente la riconciliazione con corrispondenza completa quando la salvi, attiva l'interruttore **Pubblica se completamente applicato**.  
- Per salvare le corrispondenze attualmente visualizzate nella finestra di Copilot, seleziona **Conservalo**.


## <a name="post-unmatched-bank-transaction-amounts-to-suggested-general-ledger-accounts"></a>Trasferire transazioni bancarie senza corrispondenze a conti di contabilità generale suggeriti

In questa sezione, apprenderai a utilizzare Copilot per trasferire estratti conto non riconciliati dalla contabilità del conto corrente bancario a un conto di contabilità generale. Questa attività può essere eseguita solo da una riconciliazione esistente. 

1. Vai all'elenco **Riconciliazioni C/C bancari** e apri la riconciliazione esistente che include le righe non riconciliate.

   Inizia aprendo una riconciliazione esistente del conto corrente bancario. Questo passaggio fornisce una panoramica chiara di tutte le righe dell'estratto conto non riconciliate che devono essere trasferite al conto di contabilità generale.

2. Nel riquadro **Righe rendiconto bancario**, identifica il riquadro delle righe dell'estratto conto senza corrispondenze e seleziona una o più righe che vuoi riconciliare.

   Queste righe sono le righe dell'estratto conto su cui Copilot si concentra per il trasferimento al conto di contabilità generale.

3. Seleziona **Trasferisci su conto C/G** per avviare il processo.

   ![Azione Trasferisci su conto C/G di Copilot nella scheda Riconciliazioni C/C bancari](media/bank-reconciliation-transfer-gl-copilot-card.svg) 

   Questo passaggio richiede a Copilot di iniziare a generare proposte per il trasferimento.

4. Una volta che Copilot ha terminato di generare proposte, si apre la finestra **Proposte di trasferimento di conti C/G Copilot**.

   Questa finestra visualizza le proposte nella sezione **Proposte risultanti**. L'esperienza è simile alla riconciliazione con Copilot.

   ![Pagina delle corrispondenze proposte con l'azione Trasferisci su conto C/G per la riconciliazione del conto corrente bancario](media/bank-reconciliation-gl-transfer-proposed-matches.png) 

5. Esamina ogni proposta riga per riga per assicurare l'accuratezza dei trasferimenti suggeriti.

   - Se esegui il drill-down della proposta selezionandola nell'elenco, viene visualizzato a un elenco di account. Nell'elenco, scegli un altro account. Questo tipo di correzione manuale è possibile solo quando si utilizza il flusso **Trasferisci su conto C/G** e non il flusso di corrispondenza. 
   - Se selezioni **Salva...** accanto a una proposta, puoi aggiungere la mappatura alla pagina **Mappatura testo a conto**, quindi la prossima volta che questo testo viene visualizzato durante la creazione delle corrispondenze, verrà mappato all'account proposto.

6. Elimina o salva le proposte.

   - Se vuoi eliminare una specifica proposta, selezionala nell'elenco, quindi seleziona l'azione **Elimina riga**. Per eliminare tutte le proposte e chiudere Copilot, seleziona il pulsante di eliminazione (cestino) ![Icona del cestino per l'eliminazione di tutte le proposte di Copilot per la riconciliazione del conto corrente bancario](media/copilot-delete-trash-can.png) accanto al pulsante **Conservalo** nella parte inferiore della finestra.
   
   - Se le proposte soddisfano le tue esigenze e desideri salvarle, seleziona **Conservalo**. 

      Questo passaggio conferma il trasferimento delle proposte attualmente selezionate dalla contabilità del conto bancario al conto di contabilità generale. Pubblica nuovi pagamenti nei conti C/G proposti e applica le righe corrispondenti ai movimenti contabili C/C bancari risultanti.

## <a name="next-steps"></a>Passaggi successivi

[Convalidare la riconciliazione del conto corrente bancario](bank-how-reconcile-bank-accounts-separately.md#validate-your-bank-reconciliation)  

## <a name="see-also"></a>Vedere anche
[Risoluzione dei problemi relativi alle funzionalità di Copilot e IA](ai-copilot-troubleshooting.md)  
[Domande frequenti sull'intelligenza artificiale responsabile per l'assistenza per la riconciliazione dei conti correnti bancari](faqs-bank-reconciliation.md)  
[Impostazione delle attività bancarie](bank-setup-banking.md)  
[Riconciliare i conti correnti bancari](bank-how-reconcile-bank-accounts-separately.md)  
[Collegare i pagamenti automaticamente e riconciliare i conti correnti bancari](receivables-apply-payments-auto-reconcile-bank-accounts.md) 
