---
title: Addebito diretto SEPA in Business Central
description: 'Con il consenso del cliente, è possibile riscuotere i pagamenti direttamente dal conto bancario del cliente in conformità al formato SEPA.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '371, 423, 424, 427, 1208, 1207, 1230'
ms.date: 06/16/2021
ms.author: edupont
---
# Riscuotere pagamenti con addebito diretto SEPA

Con il consenso del cliente, è possibile riscuotere i pagamenti direttamente dal conto bancario del cliente in conformità al formato SEPA.  

Innanzitutto, impostare il formato di esportazione del file della banca che indica di eseguire un addebito diretto. A questo punto, impostare il metodo di pagamento del cliente. Infine, impostare il mandato di addebito diretto che riflette l'accordo con il cliente per riscuotere i pagamenti in un determinato periodo del contratto.  

Per indicare alla banca di trasferire l'importo del pagamento dal conto bancario del cliente al conto della propria società, è possibile creare un movimento riscossione di addebiti diretti, contenente informazioni sui conti bancari, sulle fatture di vendita interessate e sul mandato di addebito diretto. È quindi possibile esportare un file XML basato sul movimento riscossione inviato alla banca per l'elaborazione. I pagamenti che non sono stati elaborati verranno comunicati dalla banca, pertanto sarà necessario rifiutare manualmente i movimenti riscossione addebiti diretti in questione.  

È possibile impostare codici di vendita cliente standard con le informazioni sul mandato e sul metodo di pagamento in addebito diretto. È quindi possibile utilizzare il processo batch **Crea fatture pers. standard** per generare più fatture di vendita con le informazioni di addebito diretto precompilate. Questa operazione può essere eseguita manualmente o automaticamente, in base alla data di scadenza del pagamento.  

Quando i pagamenti vengono elaborati correttamente, come comunicato dalla banca, è possibile registrare le ricevute dei pagamenti direttamente dalla pagina **Movimenti riscossioni addebiti diretti** o spostando le righe dei pagamenti nel giornale di registrazione in cui si registrano le ricevute di pagamento, ad esempio la pagina **Registrazioni incassi**. In alternativa, a seconda del processo di gestione di cassa, è possibile attendere e collegare i pagamenti solo come parte della riconciliazione bancaria.  

> [!NOTE]  
> Per raccogliere i pagamenti tramite l'Addebito diretto SEPA, la valuta nella fattura di vendita deve essere EURO.  

## Impostare gli addebiti diretti SEPA

Nella pagina **Riscossioni addebiti diretti** è possibile esportare le istruzioni nella banca elettronica per eseguire una riscossione di addebiti diretti dal conto corrente del cliente al conto corrente della banca usando il formato di addebito diretto SEPA.

> [!NOTE]
> La versione globale di [!INCLUDE[prod_short](includes/prod_short.md)] supporta solo il formato di addebito diretto SEPA. La versione del proprio paese/area geografica può supportare altri formati per i pagamenti elettronici. Vedere **Funzionalità locale** nel sommario.  

Per abilitare l'esportazione di formati di file della banca che non sono supportati come predefiniti in [!INCLUDE[prod_short](includes/prod_short.md)], è possibile impostare una definizione di scambio dati utilizzando il framework di scambio dati. Per ulteriori informazioni, vedere [Impostare le definizioni di scambio di dati](across-how-to-set-up-data-exchange-definitions.md).  

Prima di poter elaborare elettronicamente i pagamenti del cliente esportando le istruzioni di addebito diretto nel formato di addebito diretto SEPA, è necessario effettuare i seguenti passaggi di impostazione:  

* Impostare il formato di esportazione del file della banca che indica di eseguire la riscossione di un addebito diretto dal conto bancario del cliente al proprio.  
* Impostare il metodo di pagamento del cliente.  
* Impostare il mandato di addebito diretto che riflette l'accordo con il cliente per riscuotere i pagamenti in un determinato periodo del contratto.  

### Per impostare il conto bancario per l'addebito diretto SEPA

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **C/C bancari**, quindi scegli il collegamento correlato.  
2. Aprire il conto bancario che si desidera utilizzare per l'addebito diretto.  
3. Nella Scheda dettaglio **Trasferimento**, nel campo **Formato esport. addebito dir. SEPA**, scegliere l'opzione per addebito diretto SEPA.  

### Per impostare il metodo di pagamento del cliente per l'addebito diretto SEPA

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Metodi di pagamento**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Nuovo**.  
3. Impostare un metodo di pagamento. Compilare i campi specifici dell'addebito diretto\-come descritto nella tabella riportata di seguito.  

    |Campo|Descrizione|  
    |---------------------------------|---------------------------------------|  
    |**Addebito diretto**|Specificare se il metodo di pagamento riguarda la riscossione di addebiti diretti SEPA.|  
    |**Cod. condizioni pag. addebiti dir.**|Specificare le condizioni di pagamento, ad esempio NON PAGARE, che vengono visualizzate sulle fatture di vendita pagate con addebito diretto SEPA per indicare al cliente che il pagamento verrà riscosso automaticamente. In alternativa, lasciare vuoto il campo.|  

    > [!NOTE]  
    >  Non immettere un valore nel campo **Nr. contropartita**.  

4. Fare clic sul pulsante **OK** per chiudere la pagina **Metodi di pagamento**.  
5. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Clienti**, quindi scegli il collegamento correlato.  
6. Aprire la scheda del cliente che si desidera impostare per la riscossione di addebiti diretti SEPA.  
7. Scegliere il campo **Codice metodo di pagamento**, quindi selezionare il codice del metodo di pagamento specificato nel passaggio 3.  
8. Ripetere i passaggi da 6 a 7 per tutti i clienti che si desidera impostare per la riscossione degli addebiti diretti SEPA.  

#### Per impostare il mandato di addebito diretto che rappresenta l'accordo con il cliente

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Clienti**, quindi scegli il collegamento correlato.  
2. Aprire la scheda del cliente che si desidera impostare per l'addebito diretto SEPA.  
3. Scegliere l'azione **C/C bancari**.  
4. Nella pagina **Lista C/C bancari clienti** selezionare il conto bancario cliente che utilizzerà gli addebiti diretti, quindi scegliere l'azione **Mandati di addebito diretto**.  
5. Nella pagina **Mandati per addebito diretto SEPA** compilare i campi come indicato nella tabella riportata di seguito.  

    |Campo|Descrizione|  
    |---------------------------------|---------------------------------------|  
    |**Codice C/C bancario clienti**|Specifica il conto bancario da cui vengono riscossi i\-pagamenti in addebito diretto. Questo campo viene compilato automaticamente.|  
    |**Data di inizio validità**|Specificare la data in cui ha inizio\-il mandato di addebito diretto.|  
    |**Data di fine validità**|Specificare la data in cui termina\-il mandato di addebito diretto.|  
    |**Data di firma**|Specificare la data in cui il cliente ha firmato il mandato di\-addebito diretto.|  
    |**Tipo di pagamento**|Specificare se l'accordo riguarda una (**Singola**) o più (**Ricorrente**) riscossioni di addebiti diretti.|  
    |**Numero previsto di debiti**|Specificare il numero di riscossioni di addebiti diretti che si prevede di eseguire. Questo campo è pertinente solo se nel campo **Tipo di pagamento** è stato selezionato **Ricorrente**.|  
    |**Contatore debiti**|Specifica quante riscossioni di addebiti diretti sono state effettuate mediante il mandato di\-addebito diretto. Questo campo viene aggiornato automaticamente.|  
    |**Bloccato**|Specificare che le riscossioni di addebiti diretti non possono essere eseguite mediante questo mandato di\-addebito diretto.|  

6. Ripetere i passaggi da 1 a 5 per tutti i clienti che si desidera impostare per l'addebito diretto SEPA.  

 Il mandato di addebito diretto viene inserito automaticamente nel campo **ID mandato per addebito diretto** quando si crea una fattura di vendita per il cliente selezionato nel passaggio 2. Per altre informazioni, vedere [Creare righe di vendite e acquisti ricorrenti](sales-how-work-standard-lines.md).

## Creare movimenti riscossione addebiti diretti SEPA ed esportarli in un file della banca

Per indicare alla banca di trasferire l'importo del pagamento dal conto bancario del cliente al conto della propria società, è possibile creare un movimento riscossione di addebiti diretti, contenente informazioni sul conto bancario del cliente, sulle fatture di vendita interessate e sul mandato di addebito diretto. Dal movimento riscossione addebiti diretti risultante, è possibile esportare un file XML da inviare o caricare sul sito elettronico della banca per l'elaborazione. I pagamenti che non sono stati elaborati dalla banca verranno comunicati dalla banca stessa, pertanto sarà necessario rifiutare manualmente i movimenti riscossione addebiti diretti in questione.  

 > [!NOTE]  
 > Per raccogliere i pagamenti tramite l'Addebito diretto SEPA, la valuta nella fattura di vendita deve essere EURO.  

### Per creare una riscossione di addebiti diretti  

 1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Riscossioni addebiti diretti**, quindi scegli il collegamento correlato.  
 2. Nella pagina **Riscossioni addebiti diretti** scegliere l'azione **Crea riscossione di addebiti diretti**.  
 3. Nella pagina **Crea riscossione di addebiti diretti** compilare i campi come indicato nella tabella riportata di seguito.  

    |Campo|Descrizione|  
    |---------------------------------|---------------------------------------|  
    |**Da data scadenza**|Specificare la data di scadenza del pagamento più vicina sulle fatture di vendita per cui si desidera creare una riscossione di addebiti diretti.|  
    |**A data scadenza**|Specificare la data di scadenza del pagamento più lontana sulle fatture di vendita per cui si desidera creare una riscossione di addebiti diretti.|  
    |**Tipo di partner**|Specificare se la riscossione di addebiti diretti viene eseguita per clienti di tipo **Società** o **Persona fisica**.|  
    |**Solo clienti con mandato valido**|Specificare se viene creata una riscossione di addebiti diretti per i clienti che dispongono di un mandato di addebito diretto valido. **Nota:** viene creata una riscossione addebiti diretti anche se il campo **ID mandato per addebito diretto** non viene compilato nella fattura di vendita.|  
    |**Solo fatture con mandato valido**|Specificare se una riscossione addebiti diretti viene creata per le fatture di vendita solo se un mandato di addebito diretto valido è selezionato nel campo **ID mandato per addebito diretto** nella fattura di vendita.|  
    |**Nr. conto bancario**|Specificare in quale conto bancario della società verrà trasferito il pagamento riscosso dal conto bancario del cliente.|  
    |**Nome conto corrente**|Specifica il nome del conto bancario selezionato nel campo **Nr. conto corrente**. Questo campo viene compilato automaticamente.|  

 4. Scegliere il pulsante **OK**.  

Alla pagina **Riscossioni addebiti diretti** viene aggiunta una riscossione addebiti diretti e vengono creati uno o più movimenti di riscossione addebiti diretti.  

### Per esportare un movimento riscossione di addebiti diretti in un file della banca

 1. Nella pagina **Riscossioni addebiti diretti** scegliere l'azione **Movimenti riscossioni addebiti diretti**.  
 2. Nella pagina **Movimenti riscossioni addebiti diretti** selezionare il movimento che si desidera esportare, quindi scegliere l'azione **Crea file addebiti diretti**.  
 3. Salvare il file di esportazione nel percorso da cui verrà inviato o caricato sul sito elettronico della banca.  

      Nella pagina **Movimenti riscossioni addebiti diretti** il campo **Stato riscossione di addebiti diretti** viene impostato su File creato. Nella pagina **Mandati per addebito diretto SEPA** il campo **Contatore debiti** viene aggiornato con un conteggio.  

 Se il file esportato non può essere elaborato, ad esempio perché il cliente è insolvente, è possibile rifiutare il movimento riscossione addebiti diretti. Se il file esportato viene elaborato correttamente dalla banca, i pagamenti in scadenza relativi alle fatture di vendita interessate vengono automaticamente riscossi dai clienti interessati. In questo caso è possibile chiudere la riscossione.  

### Per rifiutare un movimento riscossione di addebiti diretti  

* Nella pagina **Movimenti riscossioni addebiti diretti** selezionare il movimento che non è stato elaborato, quindi scegliere l'azione **Rifiuta movimento**.  

    Il valore nel campo **Stato** della pagina **Movimenti riscossioni addebiti diretti** viene modificato in **Rifiutato**.  

### Per chiudere una riscossione di addebiti diretti

* Nella pagina **Movimenti riscossioni addebiti diretti** selezionare il movimento che non è stato elaborato, quindi scegliere l'azione **Chiudi riscossione**.  

    La riscossione di addebiti diretti correlata è chiusa.  

 È ora possibile procedere con la registrazione delle ricevute dei pagamenti per le fatture di vendita interessate. È possibile eseguire questa operazione come si registrano le ricevute dei pagamenti, ad esempio nella pagina **Registrazione pagamenti**, oppure è possibile registrare le ricevute dei pagamenti correlate direttamente nella pagina **Movimenti riscossioni addebiti diretti**. Per ulteriori informazioni, vedere [Riscuotere pagamenti con addebito diretto SEPA](finance-collect-payments-with-sepa-direct-debit.md).

## Registrare ricevute di pagamento di addebiti diretti SEPA

Quando una riscossione di addebiti diretti viene elaborata correttamente dalla banca, è possibile procedere con la registrazione della ricevuta del pagamento per le fatture di vendita interessate. Per ulteriori informazioni, vedere [Creare movimenti riscossione addebiti diretti SEPA ed esportarli in un file della banca](finance-collect-payments-with-sepa-direct-debit.md#creating-sepa-direct-debit-collection-entries-and-export-to-a-bank-file).  

È possibile registrare la ricevuta di pagamento direttamente dalla pagina **Riscossioni addebiti diretti** o dalla pagina **Movimenti riscossioni addebiti diretti**. In alternativa, è possibile inoltrare il lavoro a un altro utente preparando le righe registrazioni correlate.  

### Per registrare una ricevuta di pagamento con addebito diretto dalla pagina Riscossioni di addebiti diretti

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Riscossioni addebiti diretti**, quindi scegli il collegamento correlato.  
2. Selezionare una riga per una riscossione di addebiti diretti esportata in un file della banca ed elaborata correttamente dalla banca.
3. Scegliere l'azione **Registra ricevute di pagamento**.  
4. Nella pagina **Registra riscossione addebiti diretti** compilare i campi come indicato nella tabella riportata di seguito.  

    |Campo|Descrizione|  
    |---------------------------------|---------------------------------------|  
    |**Nr. riscossione di addebiti diretti**|Specificare la riscossione di addebiti diretti per cui si desidera registrare la ricevuta di pagamento.|  
    |**Definizione registrazioni COGE**|Specificare quale definizione di registrazione COGE utilizzare per registrare la ricevuta di pagamento, ad esempio le ricevute delle entrate di cassa.|  
    |**Nome batch registrazioni COGE**|Specificare quale il batch di registrazioni COGE utilizzare per la registrazione della ricevuta di pagamento.|  
    |**Crea solo registrazioni**|Selezionare questa casella di controllo se non si desidera registrare la ricevuta di pagamento quando si sceglie il pulsante **OK**. La ricevuta di pagamento verrà preparata nella registrazione specificata e non verrà registrata finché non vengono contabilizzate le righe registrazioni in questione.|  

5. Scegliere il pulsante **OK**.

## Vedere anche

[Gestione della contabilità clienti](receivables-manage-receivables.md)  
[Gestione assistenza](service-service.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]