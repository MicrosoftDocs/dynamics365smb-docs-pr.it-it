---
title: Prevedere pagamenti in ritardo per documenti di vendita
description: Questo argomento spiega come utilizzare il modello di previsione per verificare se una fattura verrà pagata con puntualità.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customer, payment, invoice, sales, invoice, quote'
ms.search.form: '1950, 1951,'
ms.date: 12/20/2021
ms.author: bholtorf
---
# Estensione Previsione pagamento ritardato

La gestione efficace dei crediti è importante per lo stato finanziario complessivo di un'azienda. L'estensione Previsione pagamento ritardato consente di ridurre i crediti in sospeso e perfezionare la strategia di riscossione prevedendo se le fatture di vendita verranno pagate con puntualità. Ad esempio, se si prevede che un pagamento sia in ritardo, è possibile decidere di adeguare i termini di pagamento o il metodo di pagamento per il cliente.

## Introduzione

Quando si apre un documento di vendita registrato, viene visualizzato un avviso nella parte superiore della pagina. Per utilizzare l'Estensione Previsione pagamento ritardato, è possibile l'opzione **Abilita** nella notifica. In alternativa, è possibile impostare manualmente l'estensione. Ad esempio, se la notifica è stata rifiutata accidentalmente.  

Per abilitare l'estensione manualmente, attenersi alla seguente procedura:

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Impostazione previsione pagamento ritardato**, quindi scegli il collegamento correlato.  
2. Compilare i campi in base alle esigenze.

> [!NOTE]
> Se si decide di abilitare l'estensione manualmente, tenere presente che [!INCLUDE[prod_short](includes/prod_short.md)]non consentirà di farlo se la qualità del modello è bassa. La qualità del modello indica l'accuratezza delle previsioni del modello. Numerosi fattori possono influire sulla qualità di un modello. Ad esempio, la quantità di dati potrebbe essere insufficiente oppure i dati non contengono variazioni sufficienti. È possibile visualizzare la qualità del modello attualmente in uso nella pagina **Impostazione previsione pagamento ritardato**. È inoltre possibile specificare una soglia minima per la qualità del modello.   

## Visualizzare tutte le previsioni di pagamento

Se si abilita l'estensione, nella Gestione ruolo utente **Manager aziendale** sarà disponibile un riquadro **Pagamenti con previsione di ritardo**. Il riquadro visualizza il numero di pagamenti che si prevede siano in ritardo e consente di aprire la pagina **Movimenti contabili clienti** in cui è possibile esaminare in dettaglio le fatture registrate. Sono presenti tre colonne a cui prestare attenzione:  

* **Pagamento in ritardo**: indica se il pagamento per la fattura è previsto in ritardo.
* **Affidabilità previsione**: indica quanto è affidabile la previsione. **Alta** significa che la previsione è affidabile almeno al 90%, **Media** è compresa tra l'80% e il 90%, **Bassa** è inferiore all'80%.
* **Affidabilità previsione in %**: mostra la percentuale effettiva della valutazione di affidabilità. Per impostazione predefinita, questa colonna non viene visualizzata, ma è possibile aggiungerla se lo si desidera. Per ulteriori informazioni, vedere [Personalizzare l'area di lavoro](ui-personalization-user.md).

> [!TIP]
> La pagina Movimenti Contabili Clienti mostra inoltre un riquadro Dettaglio informazioni a destra. Mentre si consultano le previsioni, le informazioni nella sezione **Dettagli cliente** possono essere utili. Quando si sceglie la fattura nell'elenco, la sezione mostra le informazioni sul cliente. È anche possibile agire immediatamente. Ad esempio, se un cliente smarrisce frequentemente il Portafoglio, è possibile aprire la scheda cliente dal riquadro Dettaglio informazioni e bloccare il cliente per le vendite future.  

## Visualizzazione di una previsione di pagamento per un documento di vendita specifico

È inoltre possibile prevedere i pagamenti in ritardo con anticipo. Nelle pagine **Offerte di vendita**, **Ordini di vendita** e **Fatture di vendita** è possibile utilizzare l' azione **Prevedi pagamento** per generare una previsione per il documento di vendita che si sta visualizzando.

<!--## Scheduling Payment Predictions
On the **Late Payment Prediction Setup** page you can schedule updates to payment predictions for a time that is convenient for you. -->

## Dettagli di progettazione

Microsoft distribuisce e gestisce un certo numero di servizi Web predittivi in tutte le aree geografiche in cui [!INCLUDE[prod_short](includes/prod_short.md)] è disponibile. L'accesso a questi servizi Web è incluso nel tuo abbonamento [!INCLUDE[prod_short](includes/prod_short.md)]. Per ulteriori informazioni, vedere Guida alle licenze di Microsoft Dynamics 365 Business Central. La guida è disponibile per il download sul sito Web di [Business Central](https://dynamics.microsoft.com/business-central/overview/).

I servizi Web funzionano in tre modalità:

* Training del modello. Il servizio Web effettua il training del modello in base al set di dati fornito.
* Valutazione del modello. Il servizio Web verifica se il modello restituisce dati affidabili per il set di dati fornito.
* Previsione. Il servizio Web applica il modello al set di dati fornito per effettuare una previsione.

Questi servizi Web sono apolidi, nel senso che utilizzano i dati solo per calcolare previsioni su richiesta. Non memorizzano dati. 

> [!NOTE]  
> In alternativa, è possibile utilizzare il proprio servizio Web predittivo. Per ulteriori informazioni, vedere [Creare e utilizzare la previsione di pagamento ritardato per il proprio servizio Web predittivo](#AnchorText).

### Dati obbligatori per il training e la valutazione del modello

Per ciascun **Movimento contabile clienti** che ha una relativa **Spedizione vendita registrate**:

* Importo (VL) imposta inclusa
* Le condizioni di pagamento in giorni sono calcolate come **Scadenza** meno **Data di registrazione**.
* Specifica se esiste una nota di credito applicata. 

Inoltre, il record è arricchito con dati aggregati provenienti da altre fatture correlate allo stesso cliente. È incluso quanto segue:

- Numero totale e importo delle fatture pagate
- Numero totale e importo delle fatture pagate in ritardo
- Numero totale e importo delle fatture inevase
- Numero totale e importo delle fatture inevase che sono già in ritardo
- Ritardo medio in giorni
- Rapporto: fatture pagate in ritardo/pagate
- Rapporto: importo pagate in ritardo/pagate
- Rapporto: numero di fatture inevase in ritardo/inevase
- Rapporto: importo fatture inevase in ritardo/inevase

> [!NOTE]
> Le informazioni sul cliente non sono incluse nel set di dati.

### Modello standard e modello personale

L'estensione Previsione pagamento ritardato contiene un modello predittivo il cui training viene effettuato utilizzando dati significativi di una serie di piccole e medie imprese. Quando inizi a registrare fatture e a ricevere pagamenti, [!INCLUDE[prod_short](includes/prod_short.md)] valuterà se il modello standard si adatta al tuo flusso aziendale. 

Se sembra che i tuoi processi non corrispondano al modello standard, puoi comunque utilizzare l'estensione, ma dovrai ottenere più dati. Continua semplicemente a utilizzare [!INCLUDE[prod_short](includes/prod_short.md)].
> [!NOTE]
> Una piccola parte del tempo di calcolo settimanale aziendale viene utilizzata per valutare ed eseguire nuovamente il training del modello. 

[!INCLUDE[prod_short](includes/prod_short.md)] esegue il traning e la valutazione automaticamente quando vi sono abbastanza fatture pagate e in ritardo, tuttavia è possibile eseguirlo manualmente ogni volta che lo si desidera.

#### Per eseguire il training del modello ed utilizzarlo

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Impostazione previsione pagamento ritardato**, quindi scegli il collegamento correlato.  
2. Nel campo **Modello selezionato** selezionare **Modello personale**.
3. Scegli l'azione **Crea modello personale** per eseguire il training del modello sui tuoi dati.  

## <a name="AnchorText"> </a>Creare e utilizzare il proprio servizio Web predittivo per la previsione di pagamento ritardato

È inoltre possibile creare il proprio servizio Web predittivo basato su un modello pubblico denominato **Sistema sperimentale predittivo per Dynamics 365 Business Central**. Il modello predittivo è disponibile anche online nella raccolta Azure AI. Attenersi alla seguente procedura per utilizzare il modello:  

1. Aprire un browser e accedere alla [Azure AI Gallery](https://go.microsoft.com/fwlink/?linkid=2086310)  
2. Cerca **Sistema sperimentale predittivo per Dynamics 365 Business Central**, quindi apri il modello in Azure Machine Learning Studio.  
3. Utilizzare l'account Microsoft per impostare un'area di lavoro, quindi copiare il modello.  
4. Eseguire il modello e pubblicarlo come servizio Web.  
5. Prendere nota dell'URL API e della chiave API. Usa queste le credenziali per un setup del flusso di cassa.  
6. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Impostazione previsione pagamento ritardato**, quindi scegli il collegamento correlato.  
7. Scegliere la casella di controllo **Utilizza sottoscrizione di Azure personale**.
8. Nella Scheda dettaglio **Credenziali modello personale**, immettere l'URL dell'API e la chiave API per il modello.  .  

## Vedi il relativo [training Microsoft](/training/modules/predict-late-payments-sales-documents/)

## Vedere anche

[Documentazione di Azure Machine Learning Studio](/azure/machine-learning/classic/)  
[Personalizzazione di Business Central con le estensioni](ui-extensions.md)  
[Benvenuto in [!INCLUDE[prod_long](includes/prod_long.md)]](index.md)  
[Usare l'intelligenza artificiale in Microsoft Dynamics 365 Business Central](/training/paths/use-artificial-intelligence/)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
