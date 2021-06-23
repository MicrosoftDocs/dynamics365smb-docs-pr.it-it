---
title: 'Procedura dettagliata: impostazione e fatturazione dei pagamenti anticipati vendite'
description: I pagamenti anticipati sono pagamenti che vengono fatturati e registrati in un ordine di pagamento anticipato di vendita o di acquisto prima della fatturazione finale. La società può richiedere un deposito prima di produrre gli articoli oppure esigere il pagamento prima di spedire gli articoli al cliente. La funzionalità di pagamento anticipato in Business Central consente di fatturare e riscuotere i depositi richiesti dai clienti o di rimettere i depositi ai fornitori. In questo modo è possibile assicurarsi che tutti i pagamenti siano registrati a fronte di una fattura.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 05/25/2021
ms.author: edupont
ms.openlocfilehash: dacf9e5492f583513e69f2316a0440fce2597269
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216182"
---
# <a name="walkthrough-setting-up-and-invoicing-sales-prepayments"></a>Procedura dettagliata: impostazione e fatturazione dei pagamenti anticipati vendite

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

I pagamenti anticipati sono pagamenti che vengono fatturati e registrati in un ordine di pagamento anticipato di vendita o di acquisto prima della fatturazione finale. La società può richiedere un deposito prima di produrre gli articoli oppure esigere il pagamento prima di spedire gli articoli al cliente. La funzionalità di pagamento anticipato in [!INCLUDE[prod_short](includes/prod_short.md)]  consente di fatturare e riscuotere i depositi richiesti dai clienti o di rimettere i depositi ai fornitori. In questo modo è possibile assicurarsi che tutti i pagamenti siano registrati a fronte di una fattura.  

I requisiti del pagamento anticipato possono essere definiti per un cliente o un fornitore per tutti gli articoli o solo per alcuni. Una volta definite le impostazioni necessarie, è possibile generare fatture di pagamento anticipato da ordini di vendita o di acquisto per l'importo calcolato. È possibile modificare gli importi di default nella fattura in base alle esigenze. Ad esempio, è possibile inviare ulteriori fatture di pagamento anticipato se vengono aggiunti altri articoli all'ordine.  

## <a name="about-this-walkthrough"></a>Informazioni sulla procedura dettagliata  

In questa procedura dettagliata verranno descritti gli scenari seguenti:  

-  Impostazione dei pagamenti anticipati  
-  Creazione di un ordine che richiede un pagamento anticipato  
-  Creazione di una fattura di pagamento anticipato  
-  Correzione dei requisiti di pagamento anticipato di un ordine  
-  Collegamento di pagamenti anticipati a un ordine  
-  Fatturazione dell'importo finale di un ordine con pagamento anticipato  

### <a name="roles"></a>Ruoli

Questa procedura dettagliata include task per i seguenti ruoli:  

-  Manager contabilità (Barbara Zighetti)  
-  Gestore ordini (Elisabetta Scotti)  
-  Amministratore contabilità clienti (Armando Pinto)  

## <a name="story"></a>Scenario

 Barbara Zighetti è un manager contabilità. Spetta a lei decidere quali clienti devono versare un deposito prima che gli articoli siano lavorati o spediti. Barbara imposta [!INCLUDE[prod_short](includes/prod_short.md)] per calcolare i pagamenti anticipati automaticamente.  

 Elisabetta Scotti è un gestore ordini di vendita. Quando un cliente chiama per effettuare un ordine, inserisce l'ordine nel sistema mentre il cliente è al telefono. In questo modo, può verificare subito i prezzi e le condizioni di pagamento con il cliente e può procedere alle rettifiche all'ordine mentre negozia con il cliente.  

 Armando Pinto lavora nel reparto Contabilità clienti e registra fattura e pagamenti.  

 In questo scenario, Barbara definisce i requisiti di pagamento anticipato per il cliente Grafiche Magiche 2000 in base al suo storico di credito e dà istruzioni a Elisabetta su come gestire i loro ordini.  

 Quando il cliente chiama, Elisabetta negozia con il cliente fino a quando non raggiungono un accordo. Può scegliere di calcolare il pagamento anticipato in modi diversi.  

 Dopo che Elisabetta ha emesso la fattura per il pagamento anticipato, il cliente ordina un articolo aggiuntivo. Elisabetta aggiorna l'ordine e crea una seconda fattura per il pagamento anticipato.  

 Armando registra il pagamento del cliente, lo collega alle fatture e invia la fattura finale.  

## <a name="setting-up-prepayments"></a>Impostazione dei pagamenti anticipati

Barbara imposta il sistema per la gestione dei pagamenti anticipati da parte dei clienti.  

-  Decide di adottare per i pagamenti anticipati la stessa numerazione utilizzata per le fatture di vendita.  
-  Imposta l'applicazione in modo che controlli automaticamente se sono previsti pagamenti anticipati prima della fatturazione finale di un ordine.  
-  Imposta i valori predefiniti per le percentuali di pagamento anticipato da richiedere per specifici articoli e clienti.  

Le seguenti procedure illustrano come svolgere i task di Barbara:  

#### <a name="to-set-up-number-series-for-prepayments"></a>Per impostare la numerazione per i pagamenti anticipati

1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup contabilità clienti e vendite** e quindi scegliere il collegamento correlato.  
2.  Nella pagina **Setup contabilità clienti** espandere la Scheda dettaglio **Numerazioni**.  
3.  Verificare che la numerazione per le fatture di pagamento anticipato registrate nel campo **Nr. fatt. pagam. ant. reg.** sia la stessa delle fatture di vendita registrate (**Nr. fatture registrate**) e che la numerazione per le note di credito registrate per i pagamenti anticipati (**Nr. note cr. pagam. ant. reg.**) sia la stessa delle note di credito registrate (**Nr. note credito registrate**).  

#### <a name="to-block-shipments-for-unpaid-prepayment"></a>Per bloccare le spedizioni in caso di mancato versamento del pagamento anticipato

1.  Nella Scheda dettaglio **Generale** della pagina **Setup contabilità clienti** selezionare la casella di controllo **Verifica pagamento anticipato durante la registrazione**.

Non è possibile spedire o fatturare un ordine con un importo pagamento anticipato non pagato.  

Barbara stabilisce che, come regola di default, al cliente 20000 venga fatturato il 30% di anticipo su tutti gli ordini. Pertanto, inserisce una percentuale predefinita di pagamento anticipato nella scheda cliente.  

Stabilisce altresì che a tutti i clienti sia richiesto un deposito del 20% per l'articolo 1896-S. Il cliente 20000 ha uno storico dei pagamenti insoddisfacente e quindi Barbara richiede un pagamento anticipato del 40% dal cliente 20000 per l'articolo 1896-S. La procedura seguente spiega come impostare le percentuali di pagamento anticipate di default.  

#### <a name="to-assign-default-prepayment-percentages-to-customers-and-items"></a>Per assegnare percentuali predefinite di pagamento anticipato a clienti e articoli

1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Clienti** e quindi scegliere il collegamento correlato.  
2.  Aprire la scheda per il cliente 20000 (Trey Research).
3.  Nel campo **% pagamento** immettere **30**.  
4.  Selezionare **Relazionato** quindi **Saldi** poi **Percentuali di pagamento anticipato**
5.  Compilare nel modo seguente due righe della pagina **Percentuali pagamenti anticipati vendite**:  

    |**Tipo vendita**|**Codice vendita**|**Nr. Articolo**|**% pagamento anticipato**|  
    |--------------------|--------------------|------------------|----------------------|  
    |**Cliente**|**20000**|**1896-S**|**40**|  
    |**Tutti i clienti**| |**1896-S**|**20**|  

    > [!IMPORTANT]  
    >  In base al proprio paese/area geografica, è inoltre necessario specificare un codice gruppo imposta nella Scheda dettaglio **Fatturazione** per gli articoli 1896-S.  

6.  Chiudere tutte le pagine.  

#### <a name="to-specify-an-account-for-sales-prepayments-in-general-posting-setup"></a>Per specificare un conto per i pagamenti anticipati di vendita nel setup registrazioni COGE

1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup registrazioni COGE** e quindi scegliere il collegamento correlato.  
2.  Selezionare la riga in cui il campo **Cat. reg. business gen.** è impostato su **DOMESTICO** e il campo **Cat. reg. articolo/servizio** è impostato su **DETTAGLIO**.  
3.  Nel campo **Conto pagam. anticipati vendite**, specificare l'account pertinente. La tua selezione viene salvata automaticamente.  

## <a name="creating-an-order-that-requires-a-prepayment"></a>Creazione di un ordine che richiede un pagamento anticipato

 Nello scenario seguente, Elisabetta, il gestore ordini, crea un ordine mentre parla con un cliente. Gli articoli ordinati dal cliente richiedono un pagamento anticipato e il cliente in passato non ha saldato puntualmente. Di conseguenza, Elisabetta ha ricevuto istruzione di richiedergli l'importo fisso di **800** euro come pagamento anticipato per l'ordine.  

Il cliente chiede di poter versare il 35% ed Elisabetta può accettare. Di conseguenza, modifica l'ordine.  

Crea quindi la fattura di pagamento anticipato e la invia al cliente  

#### <a name="to-create-a-sales-order-with-a-prepayment"></a>Per creare un ordine di vendita con un pagamento anticipato

1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ordini vendita** e quindi scegliere il collegamento correlato.  
2.  Scegliere l'azione **Nuovo**.  
3.  Per il campo **Nr. cliente** selezionare **20000**.  
4.  Chiudere l'avviso di oltre fido visualizzato.  
5.  Compilare due righe di vendita nel modo seguente.  

    |**Tipo**|**Nr.**|**Quantità**|  
    |--------------|-------------|------------------|  
    |**Articolo**|**1896-S**|**1**|  
    |**Articolo**|**1900-S**|**1**|

    I campi del pagamento anticipato nella riga di vendita sono nascosti per default, quindi occorre visualizzarli. Per fare ciò è necessario personalizzare la pagina. Per ulteriori informazioni, vedere [Per avviare la personalizzazione di una pagina tramite il banner Personalizzazione](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).

6.  Verificare che il campo **% pagamento anticipato** sulla riga dell'articolo **1900-S** contenga **30**. Il valore di default è stato copiato dalla testata di vendita, popolata dalla scheda cliente.  

    Il campo **% pagamento anticipato** sulla riga dell'articolo **1896-S** contiene **40**. Si tratta della percentuale immessa nella pagina **Percentuali pagamenti anticipati vendite** per l'articolo **1896-S** e il cliente **20000**.  

    Per ulteriori informazioni, vedere [Impostare i pagamenti anticipati](finance-set-up-prepayments.md).  
7.  Nell'azione **Ordine**, scegli **Statistiche**.  
8.  Nella Scheda dettaglio **Pagamento anticipato**, il campo **Importo riga pagam. ant. IVA esclusa** contiene **458.16**. Se si crea ora una fattura pagamento anticipato per l'ordine, questo è l'importo che verrà visualizzato nella fattura.  

    In questo scenario, Elisabetta deve chiedere al cliente un pagamento anticipato totale di **800**.  

    > [!IMPORTANT]  
    >  In base al proprio paese/area geografica, il seguente passaggio potrebbe non essere applicabile.  
9.  Modificare in **800** l'importo nel campo **Importo riga pagam. ant. IVA escl.** e chiudere la pagina.  
10.  Controllare il campo **% pagamento anticipato** nelle righe di vendita: si constaterà che è stato ricalcolato in **67.02438** e **67.02282**.  

     Il calcolo include tutte le righe che hanno una percentuale di pagamento anticipato superiore a zero.  

     Ora il cliente chiede se la percentuale di pagamento anticipato può essere impostata su 35%. Il supervisore di Elisabetta accetta la modifica.
11.  Nella pagina **Ordine vendita**, nella Scheda dettaglio **Pagamento anticipato** del campo **% pagamento anticipato**, immettere **35**.  
12.  Nel messaggio di avviso visualizzato, selezionare il pulsante **Sì** . Un tasso del 35% verrà applicato come percentuale di pagamento per l'intero ordine.  
13.  Verificare che le righe siano state aggiornate di conseguenza.  

## <a name="creating-a-prepayment-invoice"></a>Creazione di una fattura di pagamento anticipato  
Dopo aver inserito nell'ordine i valori di pagamento anticipato corretti, Elisabetta crea la fattura di pagamento anticipato e la invia al cliente.  

#### <a name="to-create-a-prepayment-invoice"></a>Per creare una fattura di pagamento anticipato

1.  Nella pagina **Ordine vendita**, selezionare **Azioni**, quindi **Registrazione**, **Pagamento anticipato** e quindi selezionare **Registra e stampa fattura pagamento anticipato**
2.  Scegliere **Sì** per registrare la fattura.  

> [!NOTE]  
>  Selezionare **Registra e stampa fattura pagam. ant.** e spedire la fattura al cliente.  

## <a name="creating-an-additional-prepayment-invoice"></a>Creazione di una fattura di pagamento anticipato aggiuntiva

Il giorno seguente, il cliente chiama Elisabetta e apporta modifiche all'ordine. Il cliente desidera due dell'articolo 1100. Elisabetta riapre e aggiorna l'ordine e crea una seconda fattura per il pagamento anticipato dell'ordine e la invia al cliente.  

#### <a name="to-create-an-additional-prepayment-invoice"></a>Per creare una fattura di pagamento anticipato aggiuntiva

1.  Nella pagina **Ordine vendita**, scegliere l'azione **Rilascia**, quindi **Riapri**.  
2.  Immettere **2** nel campo **Quantità** della riga dell'articolo **1896-S**.  

    Nell'azione **Ordine**, scegli **Statistiche**. Il campo **Importo riga pagam. ant. IVA esclusa** ora contiene **768.04** e il campo **Fattura importo pagam. ant. IVA esclusa** contiene **417.76**. Ciò indica l'esistenza di un importo di pagamento anticipato aggiuntivo che non è stato ancora fatturato.  
3.  Per registrare una fattura per l'importo aggiuntivo, selezionare **Azioni**, quindi **Registrazione**, **Pagamento anticipato** e infine selezionare **Registra e stampa fattura pagamento anticipato**.
4.  Scegliere **Sì** per registrare la fattura.  

## <a name="applying-the-prepayments"></a>Collegamento dei pagamenti anticipati  
Il cliente versa il pagamento anticipato e Armando, che lavora nel reparto contabilità, registra il pagamento e lo collega alle fatture di pagamento anticipato.  

#### <a name="to-apply-a-payment-to-the-prepayment-invoices"></a>Per collegare un pagamento a una fattura di pagamento anticipato

1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Registrazioni incassi** e quindi scegliere il collegamento correlato.  
2.  Compilare una riga di registrazione con le informazioni indicate di seguito.  

    |Nome campo|Immettere|  
    |----------------|-----------|  
    |**Tipo di documento**|**Pagamento**|  
    |**Tipo conto**|**Cliente**|  
    |**Nr. conto**|**20000**|  
3.  Scegli l'azione **Processi** e poi **Collega movimenti**.  
4.  Nella pagina **Collega mov. cliente** selezionare la prima fattura di pagamento anticipato e quindi scegliere l'azione **Processo**, quindi **Imposta Collega a ID**.  
5.  Ripetere il passaggio precedente per il secondo pagamento anticipato.  
6.  Scegliere il pulsante **OK**.  

    Nel campo dell'importo è ora riportata la somma delle due fatture di pagamento anticipato.  

7.  Per pubblicare il diario, scegliere l'azione **Registra/Stampa**, quindi selezionare **Invia**.
8.  Scegliere il pulsante **Sì**.

## <a name="invoicing-the-remaining-amount"></a>Fatturazione dell'importo residuo

Ora l'amministratore della contabilità clienti, Armando, è stato informato che gli articoli dell'ordine sono stati spediti e che l'ordine è pronto per essere fatturato. Armando crea quindi la fattura per l'ordine.  

#### <a name="to-invoice-the-remaining-amount"></a>Per fatturare l'importo residuo

1.  Aprire l'ordine di vendita.
2.  Scegliere l'azione **Pubblicazione**, quindi **Invia**.
3.  Selezionare **Spedizione e Fattura** e quindi fare clic sul pulsante **OK**.
4.  Se si desidera vedere in anteprima la fatture, fare clic sul pulsante **Sì**.

> [!NOTE]  
>  A questo punto il reparto spedizioni ha di norma già registrato la spedizione.  

Armando può visualizzare lo storico per verificare che la fattura di vendita sia stata creata come concepita.

1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), quindi immettere **Fatture vendita registrate** e scegliere il collegamento correlato.  

## <a name="next-steps"></a>Passaggi successivi

In questa procedura dettagliata sono stati esaminati i passaggi necessari per impostare la funzione di gestione dei pagamenti anticipati in [!INCLUDE[prod_short](includes/prod_short.md)]. Sono state impostate le percentuali di pagamento anticipato di default per clienti e articoli e sono stati inoltre utilizzati diversi metodi per calcolare il pagamento anticipato per un ordine. Si è cercato anche di assegnare un intero importo di pagamento anticipato all'ordine e calcolare la percentuale dell'anticipo rispetto all'ordine totale.  

Inoltre, è stata registrata una fattura di pagamento anticipato, creata una fattura per un secondo pagamento anticipato in seguito alla modifica dell'ordine e registrata la fattura finale per l'importo residuo.  

La funzionalità dei pagamenti anticipati in [!INCLUDE[prod_short](includes/prod_short.md)] agevola l'impostazione e l'applicazione di regole di pagamento anticipato per clienti e articoli e consente di registrare ogni pagamento a fronte di una fattura.  

## <a name="see-also"></a>Vedi anche  
[Fatturazione dei pagamenti anticipati](finance-invoice-prepayments.md)  
[Finanze](finance.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Procedure dettagliate per i processi aziendali](walkthrough-business-process-walkthroughs.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
