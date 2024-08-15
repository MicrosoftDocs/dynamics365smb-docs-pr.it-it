---
title: Prevedere pagamenti in ritardo per documenti di vendita
description: Questo articolo spiega come utilizzare il modello di previsione per verificare se un cliente pagherà una fattura con puntualità.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'customer, payment, invoice, sales, invoice, quote'
ms.search.form: '1950, 1951,'
ms.date: 07/11/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Estensione Previsione pagamento ritardato

La gestione efficace dei crediti è importante per lo stato finanziario complessivo di un'azienda. Per ridurre i crediti in sospeso e perfezionare la strategia di riscossione, l'estensione prevede se si avranno pagamenti in ritardo. Ad esempio, se si prevede che un pagamento sia in ritardo, è possibile decidere di adeguare i termini di pagamento o il metodo di pagamento per il cliente.

## Introduzione

Quando si apre un documento di vendita registrato, viene visualizzato un avviso nella parte superiore della pagina. Per utilizzare l'Estensione Previsione pagamento ritardato, scegliere l'opzione **Abilita** nella notifica. In alternativa, è possibile impostare manualmente l'estensione. Ad esempio, se la notifica è stata rifiutata accidentalmente.

Per abilitare l'estensione manualmente, attenersi alla seguente procedura:

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Impostazione previsione pagamento ritardato**, quindi scegli il collegamento correlato.  
2. Compilare i campi in base alle esigenze.

> [!NOTE]
> Se si decide di abilitare l'estensione manualmente, tenere presente che [!INCLUDE[prod_short](includes/prod_short.md)]non consentirà di farlo se la qualità del modello è bassa. La qualità del modello indica l'accuratezza delle previsioni del modello. Numerosi fattori possono influire sulla qualità di un modello. Ad esempio, la quantità di dati potrebbe essere insufficiente oppure non c'erano variazioni sufficienti nei dati. È possibile visualizzare la qualità del modello attualmente in uso nella pagina **Impostazione previsione pagamento ritardato**. È inoltre possibile specificare una soglia minima per la qualità del modello.

## Visualizzare tutte le previsioni di pagamento

Se si abilita l'estensione, nella Gestione ruolo utente **Manager aziendale** sarà disponibile un riquadro **Pagamenti con previsione di ritardo**. Il riquadro visualizza il numero di pagamenti che si prevede siano in ritardo e consente di aprire la pagina **Movimenti contabili clienti** in cui è possibile esaminare in dettaglio le fatture registrate. Sono presenti tre colonne a cui prestare attenzione:  

* **Pagamento in ritardo**: indica se il pagamento per la fattura è previsto in ritardo.
* **Affidabilità previsione**: indica quanto è affidabile la previsione. **Alta** significa che la previsione è affidabile almeno al 90%, **Media** è compresa tra l'80% e il 90%, **Bassa** è inferiore all'80%.
* **Affidabilità previsione in %**: mostra la percentuale effettiva della valutazione di affidabilità. Per impostazione predefinita, questa colonna è nascosta, ma è possibile aggiungerla se lo si desidera. Per ulteriori informazioni, vedi [Personalizzare l'area di lavoro](ui-personalization-user.md).

> [!TIP]
> La pagina Movimenti contabili clienti mostra un riquadro Dettaglio informazioni. Mentre si consultano le previsioni, le informazioni nella sezione **Dettagli cliente** possono essere utili. Quando si sceglie la fattura nell'elenco, la sezione mostra le informazioni sul cliente. È anche possibile agire immediatamente. Ad esempio, se un cliente smarrisce frequentemente il Portafoglio, è possibile aprire la scheda cliente dal riquadro Dettaglio informazioni e bloccare il cliente per le vendite future.  

## Dettagli di progettazione

Microsoft distribuisce e gestisce servizi Web predittivi in tutte le aree geografiche in cui [!INCLUDE[prod_short](includes/prod_short.md)] è disponibile. L'accesso a questi servizi Web è incluso nel tuo abbonamento [!INCLUDE[prod_short](includes/prod_short.md)]. Per ulteriori informazioni, vedere Guida alle licenze di Microsoft Dynamics 365 Business Central. La guida è disponibile per il download sul sito Web di [Business Central](https://dynamics.microsoft.com/business-central/overview/).

I servizi Web funzionano in tre modalità:

* Training del modello. Il servizio Web effettua il training del modello in base al set di dati fornito.
* Valutazione del modello. Il servizio Web verifica se il modello restituisce dati affidabili per il set di dati fornito.
* Previsione. Il servizio Web applica il modello al set di dati fornito per effettuare una previsione.

Questi servizi Web sono apolidi, nel senso che utilizzano i dati solo per calcolare previsioni su richiesta. Non memorizzano dati.

> [!NOTE]  
> In alternativa, è possibile utilizzare il proprio servizio Web predittivo. Per ulteriori informazioni, vedere [Creare e utilizzare la previsione di pagamento ritardato per il proprio servizio Web predittivo](#AnchorText).

### Dati obbligatori per il training e la valutazione del modello

Per ciascun **Movimento contabile clienti** che ha una relativa **Spedizione vendita registrate**:

* Importo in valuta locale, incluse tasse
* Le condizioni di pagamento in giorni sono calcolate come **Scadenza** meno **Data di registrazione**
* Specifica se esiste una nota di credito applicata

Inoltre, il record include dati aggregati provenienti da altre fatture correlate allo stesso cliente.

- Numero totale e importi delle fatture pagate
- Numero totale e importi delle fatture pagate in ritardo
- Numero totale e importi delle fatture inevase
- Numero totale e importi delle fatture inevase che sono già in ritardo
- Ritardo medio in giorni
- Rapporto: fatture pagate in ritardo/pagate
- Rapporto: importo pagate in ritardo/pagate
- Rapporto: numero di fatture inevase in ritardo/inevase
- Rapporto: importo fatture inevase in ritardo/inevase

> [!NOTE]
> Le informazioni sul cliente non sono incluse nel set di dati.

### Modello standard e modello personale

Il training del modello predittivo dell'estensione Previsione pagamento ritardato viene effettuato sui dati che rappresentano una serie di piccole e medie imprese. Quando inizi a registrare fatture e a ricevere pagamenti, [!INCLUDE[prod_short](includes/prod_short.md)] valuta se il modello standard si adatta al tuo flusso aziendale.

Se i tuoi processi non corrispondano al modello standard, puoi comunque utilizzare l'estensione, ma dovrai ottenere più dati. Continua semplicemente a utilizzare [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> Una piccola parte del tempo di calcolo settimanale aziendale viene utilizzata per valutare ed eseguire nuovamente il training del modello.

[!INCLUDE[prod_short](includes/prod_short.md)] esegue il training e la valutazione automaticamente quando sono disponibili abbastanza fatture pagate e in ritardo. Tuttavia, puoi eseguirlo manualmente quando vuoi.

#### Per eseguire il training del modello ed utilizzarlo

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Impostazione previsione pagamento ritardato**, quindi scegli il collegamento correlato.  
2. Nel campo **Modello selezionato** selezionare **Modello personale**.
3. Scegli l'azione **Crea modello personale** per eseguire il training del modello sui tuoi dati.  

## <a name="AnchorText"> </a>Creare e utilizzare il proprio servizio Web predittivo per la previsione di pagamento ritardato

Per [!INCLUDE[prod_short](includes/prod_short.md)] online, il modello è pubblicato da Microsoft e collegato all'abbonamento Microsoft. Per altre opzioni di distribuzione, è necessario creare risorse di Machine Learning nella propria sottoscrizione di Azure. Puoi trovare passaggi di esempio nel [repository di esempio](https://github.com/microsoft/BCTech/tree/master/samples/MachineLearning). Lo scopo di questa attività è ottenere l'URI API e la chiave API.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Impostazione previsione pagamento ritardato**, quindi scegli il collegamento correlato.  
2. Scegliere la casella di controllo **Utilizza sottoscrizione di Azure personale**.
3. Nella scheda dettaglio  **Usa il mio abbonamento Azure**, immetti l'URL API e la chiave API per il tuo modello.  

## Vedere anche

[Personalizzazione di Business Central tramite estensioni](ui-extensions.md)    
[Benvenuto a [!INCLUDE[prod_long](includes/prod_long.md)]](welcome.md)    
[Utilizzare l'intelligenza artificiale in Microsoft Dynamics 365 Business Central](/training/paths/use-artificial-intelligence/)    
[Panoramica della previsione API](/dynamics365/business-central/dev-itpro/developer/ml-prediction-api-overview)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
