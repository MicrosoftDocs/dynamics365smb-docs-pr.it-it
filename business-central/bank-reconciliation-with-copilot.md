---
title: Riconciliare i conti correnti bancari con Copilot (anteprima)
description: Scopri come usare Copilot per riconciliare i conti correnti bancari in Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.collection:
  - get-started
  - bap-ai-copilot
ms.date: 06/13/2024
ms.custom: bap-template
---

# <a name="reconcile-bank-accounts-with-copilot-preview"></a>Riconciliare i conti correnti bancari con Copilot (anteprima)

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

Questo articolo spiega come l'assistenza per la riconciliazione dei conti correnti bancari può aiutarti a riconciliare le transazioni bancarie con movimenti contabili in Microsoft Dynamics 365 Business Central.

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

## <a name="about-bank-account-reconciliation-assist"></a>Informazioni sull'assistenza per la riconciliazione dei conti correnti bancari

L'assistenza per la riconciliazione dei conti correnti bancari è un insieme di funzionalità basate sull'intelligenza artificiale che ti assistono nella riconciliazione dei conti correnti bancari. Offre due attività distinte tramite Copilot:

- Creazione migliorata delle corrispondenze tra transazioni e movimenti contabili

    Come forse già sai, il pulsante **Corrispondenza automatica** nella pagina **Riconciliazioni C/C bancari** che crea automaticamente corrispondenze tra la maggior parte delle transazioni bancarie e i movimenti contabili. Definiamo questa operazione come *corrispondenza automatica*. Sebbene la corrispondenza automatica funzioni correttamente, gli algoritmi che utilizza a volte possono generare molte transazioni senza corrispondenze. Copilot utilizza la tecnologia IA per ispezionare le transazioni senza corrispondenze e identificare più corrispondenze, in base a date, importi e descrizioni. Ad esempio, se un cliente ha pagato più fatture con un'unica somma forfettaria, Copilot riconcilia la singola riga dell'estratto conto con più movimenti contabili delle fatture.

    [Ulteriori informazioni su questa attività](#reconcile-bank-accounts-with-copilot).

- Conti di contabilità generale (C/G) suggeriti

    Per le transazioni bancarie residue per le quali non è possibile creare corrispondenze con i movimenti contabili, Copilot confronta la descrizione della transazione con i nomi dei conti C/G e quindi suggerisce il conto C/G più probabile in cui effettuare la registrazione. Ad esempio, se le transazioni senza corrispondenze hanno la descrizione *Arresto carburante 24*, Copilot potrebbe suggerire di pubblicarle nel conto *Trasporti*.

    [Ulteriori informazioni su questa attività](#post-unmatched-bank-transaction-amounts-to-suggested-gl-accounts)

## <a name="available-languages"></a>Lingue disponibili

[!INCLUDE[bank-recon-assist-language-support](includes/bank-recon-assist-language-support.md)]

## <a name="prerequisites"></a>Prerequisiti

- L'assistenza per la riconciliazione dei conti correnti bancari è attivata. Un amministratore deve completare questa attività. [Scopri di più sulla configurazione delle funzionalità di Copilot e IA](enable-ai.md).
- I conti correnti bancari in Business Central che vuoi riconciliare sono collegati a un conto corrente bancario online o impostati con il formato di importazione dell'estratto conto.
- Hai familiarità con la riconciliazione dei conti correnti bancari in Business Central, come descritto in [Riconciliare i conti correnti bancari](bank-how-reconcile-bank-accounts-separately.md).

## <a name="reconcile-bank-accounts-with-copilot"></a>Riconciliare i conti correnti bancari con Copilot

<!-- Similar to the **Match Automatically** capability on the **Bank Acc. Reconciliation** page, Bank account reconciliation assist can also automatically matches transactions in banks statements with bank entries. The difference is that **Match Automatically** uses a native rules-based algorithm, while Bank account reconciliation assist is based AI technology though Copilot. Bank account reconciliation assist is intended to supplement the **Match Automatically** capability. While **Match Automatically** is fairly successful at matching transactions, there are some instances where it can't&mdash;which is where Bank account reconciliation assist comes. By using the **Reconcile with Copilot** action on **Bank Acc. Reconciliation** page, you can find even more matches.-->

Copilot nella riconciliazione dei conti bancari è destinato come supplemento all'operazione di corrispondenza automatica. Pertanto, quando usi Copilot, l'operazione di corrispondenza automatica viene eseguita per prima per effettuare le corrispondenze iniziali. Viene quindi eseguito Copilot per provare a creare corrispondenze per le transazioni che l'operazione di corrispondenza automatica non ha gestito.

Puoi usare due approcci per riconciliare i conti correnti bancari con Copilot:

- Utilizza Copilot per avviare una nuova riconciliazione su un conto corrente bancario, direttamente dall'elenco **Riconciliazione conto corrente bancario**.
- Utilizza Copilot per una riconciliazione nuova o esistente in una scheda **Riconciliazioni C/C bancari**.

# [Dall'elenco Riconciliazioni C/C bancari](#tab/fromlist)

Per questo approccio, crei e riconcili da zero una nuova riconciliazione del conto corrente bancario. Questo approccio richiede la selezione del conto corrente bancario. Se il conto corrente bancario non è collegato a un conto in linea, devi importare anche il file dell'estratto conto.

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immetti **Riconciliazioni C/C bancari**, quindi seleziona il collegamento correlato.
1. Seleziona **Riconcilia con Copilot** per aprire la finestra **Riconcilia con Copilot**.
1. Imposta il campo **Esegui la riconciliazione per questo conto corrente bancario** sul conto corrente bancario che vuoi riconciliare.

    ![Screenshot che mostra la finestra Riconcilia con Copilot per la riconciliazione da zero.](media/reconcile-bank-accounts-new-copilot.svg)

1. Se il conto corrente bancario selezionato non è collegato a un conto corrente bancario in linea, devi importare il file dell'estratto conto. Per importare il file, seleziona il valore nel campo **Utilizza dati delle transazioni da** o seleziona il pulsante della graffetta accanto al pulsante **Genera**. Quindi utilizza **Seleziona il file da importare** per importare il file dell'estratto conto trascinandolo dal tuo dispositivo o navigando sul tuo dispositivo.
1. Per eseguire la riconciliazione con Copilot, seleziona **Genera**.

    Copilot inizia a generare le corrispondenze proposte. Al termine, la finestra **Riconcilia con Copilot** mostra i risultati del processo di creazione di corrispondenze.

1. Esamina le corrispondenze proposte come descritto nella sezione successiva.

# [Da una scheda Riconciliazioni C/C bancari](#tab/fromcard)

Per questo approccio, puoi utilizzare Copilot per una nuova riconciliazione del conto corrente bancario creata manualmente o modificando una riconciliazione esistente.

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](media/ui-search/search_small.png "Dimmi cosa vuoi fare"), immetti **Riconciliazioni C/C bancari**, quindi seleziona il collegamento correlato.
1. Effettuare una delle seguenti operazioni:

    - Seleziona **Nuovo** per avviare una nuova riconciliazione.
    - Seleziona e apri una riconciliazione esistente nell'elenco.

1. Nella scheda **Riconciliazioni C/C bancari** seleziona **Riconcilia con Copilot**.

    ![Screenshot che mostra il pulsante Riconcilia con Copilot in una scheda Riconciliazioni C/C bancari.](media/bank-reconciliation-copilot-card.svg)

    Copilot inizia a generare le corrispondenze proposte. Al termine, la finestra **Riconcilia con Copilot** mostra i risultati del processo di creazione di corrispondenze.

1. Esamina le corrispondenze proposte come descritto nella sezione successiva.
---

### <a name="review-save-or-discard-proposed-matches"></a>Esaminare, salvare o eliminare le corrispondenze proposte

Dopo aver eseguito Copilot, la finestra **Riconcilia con Copilot** mostra i risultati dettagliati, incluse eventuali corrispondenze proposte. A questo punto, nessuna corrispondenza proposta da Copilot è stata salvata. Pertanto, hai l'opportunità di ispezionare le proposte e salvarle o rifiutarle come desideri.

![Screenshot che mostra le corrispondenze proposte nella finestra Riconcilia con Copilot.](media/bank-reconciliation-copilot-window.png)

La finestra **Riconcilia con Copilot** è divisa in due sezioni. La sezione superiore fornisce alcuni dettagli generali sul risultato. La sezione inferiore **Proposte risultanti** elenca le corrispondenze proposte da Copilot.

La tabella seguente descrive i campi della sezione superiore.

| Campo | Descrizione |
|---|---|
| Corrispondenza automatica | Il numero di righe nell'estratto conto che hanno corrispondenze create dall'operazione di corrispondenza automatica. Seleziona il valore per visualizzare la scheda di riconciliazione. |
| Corrispondenze di Copilot | Il numero di righe dell'estratto conto per le quali Copilot ha proposto delle corrispondenze. Puoi visualizzare i dettagli delle corrispondenze nella sezione **Proposte risultanti**. |
| Saldo finale estratto conto | Il saldo finale visualizzato nell'estratto conto per il quale stai eseguendo la riconciliazione. |
| Pubblica se completamente applicato | Attiva questa opzioni se desideri pubblicare automaticamente la riconciliazione del conto corrente bancario quando tutte le righe (100%) hanno corrispondenze e selezioni **Conservalo**. |

Nella sezione **Proposte risultanti**, esamina le corrispondenze proposte riga per riga. Quindi esegui l'azione appropriata:

- Per eliminare una singola corrispondenza proposta, selezionala nell'elenco, quindi seleziona l'azione **Elimina riga**.
- Per rimuovere tutte le corrispondenze proposte e chiudere la finestra **Riconcilia con Copilot**, seleziona il pulsante Rimuovi (cestino) ![pulsante Rimuovi.](media/copilot-delete-trash-can.png) accanto al pulsante **Mantieni** nella parte inferiore della finestra.
- Per pubblicare automaticamente la riconciliazione con corrispondenza completa quando la salvi, attiva l'opzione **Pubblica se completamente applicato**.
- Per salvare le corrispondenze attualmente visualizzate nella finestra **Riconcilia con Copilot**, seleziona **Mantieni**.

## <a name="post-unmatched-bank-transaction-amounts-to-suggested-gl-accounts"></a>Pubblicare importi di transazioni bancarie senza corrispondenze in conti di contabilità generale suggeriti

In questa sezione viene descritto come utilizzare Copilot per pubblicare importi della riga di estratti conto non riconciliati (specificato nel campo **Differenza**) a un conto C/G. Questa attività può essere eseguita solo da una riconciliazione esistente.

1. Vai all'elenco **Riconciliazioni C/C bancari** e apri la riconciliazione esistente che include le righe non riconciliate.

    Questo passaggio fornisce una panoramica chiara di tutte le righe dell'estratto conto non riconciliate che devono essere trasferite al conto C/G.

1. Nel riquadro **Righe rendiconto bancario**, identifica il riquadro delle righe dell'estratto conto senza corrispondenze e seleziona una o più righe che vuoi riconciliare.

    Copilot si concentra sulle righe selezionate per pubblicare nuovi pagamenti nel conto C/G.

1. Seleziona **Registra differenza in conto C/G** per avviare il processo.

    ![Screenshot che mostra il pulsante Registra differenza in conto C/G nella scheda Riconciliazioni C/C bancari.](media/bank-reconciliation-transfer-gl-copilot-card.png)

    Copilot inizia a generare proposte per registrare nuovi pagamenti.

1. Una volta che Copilot ha terminato di generare proposte, si apre la finestra **Proposte Copilot per la registrazione delle differenze nei conti C/G**.

    La sezione **Proposte risultanti** di questa finestra mostra le proposte. L'esperienza assomiglia all'esperienza di riconciliazione con Copilot.

    ![Screenshot che mostra la finestra Proposte Copilot per la registrazione delle differenze nei conti C/G.](media/bank-reconciliation-gl-transfer-proposed-matches.png)

1. Esamina le proposte riga per riga per assicurare l'accuratezza dei pagamenti suggeriti da registrare.

    - Se esegui il drill-down della proposta selezionandola nell'elenco, viene visualizzato a un elenco di account. Nell'elenco, puoi selezionare un altro account. Puoi eseguire questo tipo di correzione manuale solo quando utilizzi il flusso **Registra differenza in conto C/G** e non il flusso di corrispondenza.
    - Se selezioni **Salva** accanto a una proposta, puoi aggiungere la mappatura a **Mappatura testo a conto**  pagina. Quindi la prossima volta che questo testo viene visualizzato durante la ricerca di corrispondenze, viene mappato al conto proposto.

1. Elimina o salva le proposte.

    - Per eliminare una specifica proposta, selezionala nell'elenco, quindi seleziona **Elimina riga**. Per eliminare tutte le proposte e chiudere Copilot, seleziona il pulsante Elimina (cestino) ![pulsante Elimina.](media/copilot-delete-trash-can.png) accanto al pulsante **Mantieni** nella parte inferiore della finestra.
    - Se le proposte soddisfano le tue esigenze e desideri salvarle, seleziona **Mantieni**.

         Questo passaggio conferma il trasferimento delle proposte attualmente selezionate dalla contabilità del conto bancario al conto C/G. Registra nuovi pagamenti nei conti C/G proposti e collega le righe corrispondenti ai movimenti contabili di conti correnti bancari risultanti.

## <a name="next-steps"></a>Passaggi successivi

[Convalidare la riconciliazione del conto corrente bancario](bank-how-reconcile-bank-accounts-separately.md#validate-your-bank-reconciliation)

## <a name="see-also"></a>Vedere anche

[Risoluzione dei problemi relativi alle funzionalità di Copilot e IA](ai-copilot-troubleshooting.md)  
[Domande frequenti sull'intelligenza artificiale responsabile per l'assistenza per la riconciliazione dei conti correnti bancari](faqs-bank-reconciliation.md)  
[Impostazione delle attività bancarie](bank-setup-banking.md)  
[Riconciliare i conti correnti bancari](bank-how-reconcile-bank-accounts-separately.md)  
[Collegare i pagamenti automaticamente e riconciliare i conti correnti bancari](receivables-apply-payments-auto-reconcile-bank-accounts.md)
