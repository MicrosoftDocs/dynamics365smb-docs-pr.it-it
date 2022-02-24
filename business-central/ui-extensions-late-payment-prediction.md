---
title: Prevedere pagamenti ritardati per documenti di vendita | Documenti Microsoft
description: Utilizzare il modello di previsione per verificare se una fattura verrà pagata con puntualità.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customer, payment, invoice, sales, invoice, quote
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 613d20e3b4132cdf797586441bff0688a2076692
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2019
ms.locfileid: "2315505"
---
# <a name="the-late-payment-prediction-extension"></a>Estensione Previsione pagamento ritardato  
La gestione efficace dei crediti è importante per lo stato finanziario complessivo di un'azienda. L'estensione Previsione pagamento ritardato consente di ridurre i crediti in sospeso e perfezionare la strategia di riscossione prevedendo se le fatture di vendita verranno pagate con puntualità. Ad esempio, se si prevede che un pagamento sia in ritardo, è possibile decidere di adeguare i termini di pagamento o il metodo di pagamento per il cliente.

## <a name="what-are-predictions-based-on"></a>Su cosa si basano le previsioni?  
L'estensione Previsione pagamento ritardato utilizza un modello predittivo sviluppato in Azure Machine Learning Studio e formato utilizzando dati significativi di una serie di piccole e medie imprese. Anche se già predisposto e valutato, il modello predittivo continuerà ad apprendere dai dati dell'azienda. Più si utilizza il modello, più dati lo alimentano, più diventeranno accurate le previsioni. Per impostazione predefinita, l'estensione valuta il modello e aggiorna le previsioni su base settimanale. Tuttavia, è possibile aggiornare le previsioni ogni volta che si desidera, scegliendo l' azione **Aggiorna previsione** nella pagina **Movimenti contabili clienti** .  

> [!Note]
> Una piccola parte del tempo di calcolo settimanale aziendale viene utilizzata per valutare il modello e aggiornare le previsioni. Oltre all'aggiornamento manuale delle previsioni, altre azioni che consumano tempo di elaborazione sono la preparazione del modello (che si potrebbe fare se si sono aggiunti di recente dati) e la valutazione del modello (che esamina la qualità del modello).

## <a name="getting-started"></a>Introduzione
L'estensione è gratuita in [!INCLUDE[d365fin](includes/d365fin_md.md)] e viene fornita una sottoscrizione ad Azure Machine Learning. La sottoscrizione offre 30 minuti di tempo di elaborazione al mese. Se è necessario altro tempo, è possibile creare un modello predittivo personalizzato e utilizzarlo al posto del modello predefinito. Per ulteriori informazioni, vedere la sezione _Creare un modello predittivo personalizzato_ più avanti in questo argomento.  

Quando si apre un documento di vendita registrato, viene visualizzato un avviso nella parte superiore della pagina. Per utilizzare l'Estensione Previsione pagamento ritardato, è possibile l'opzione **Abilita** nella notifica. In alternativa, è possibile impostare manualmente l'estensione. Ad esempio, se la notifica è stata rifiutata accidentalmente.  

Per abilitare l'estensione manualmente, attenersi alla seguente procedura:

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Connessioni servizio** e quindi scegliere il collegamento correlato.  
2. Scegliere l'opzione **Impostazione previsione pagamento ritardato** e compilare i campi in base alle esigenze.

## <a name="viewing-all-payment-predictions"></a>Visualizzare tutte le previsioni di pagamento
Se si abilita l'estensione, nella Gestione ruolo utente **Manager aziendale** sarà disponibile un riquadro **Pagamenti con previsione di ritardo**. Il riquadro visualizza il numero di pagamenti che si prevede siano in ritardo e consente di aprire la pagina **Movimenti contabili clienti** in cui è possibile esaminare in dettaglio le fatture registrate. Sono presenti tre colonne a cui prestare attenzione:  

* **Pagamento in ritardo**: indica se il pagamento per la fattura è previsto in ritardo.
* **Affidabilità previsione**: indica quanto è affidabile la previsione. **Alta** significa che la previsione è affidabile almeno al 90%, **Media** è compresa tra l'80% e il 90%, **Bassa** è inferiore all'80%.
* **Affidabilità previsione in %**: mostra la percentuale effettiva della valutazione di affidabilità. Per impostazione predefinita, questa colonna non viene visualizzata, ma è possibile aggiungerla se lo si desidera. Per ulteriori informazioni, vedere [Personalizzare l'area di lavoro](ui-personalization-user.md).

> [!Tip]
> La pagina Movimenti Contabili Clienti mostra inoltre un riquadro Dettaglio informazioni a destra. Mentre si consultano le previsioni, le informazioni nella sezione **Dettagli cliente** possono essere utili. Quando si sceglie la fattura nell'elenco, la sezione mostra le informazioni sul cliente. È anche possibile agire immediatamente. Ad esempio, se un cliente smarrisce frequentemente il Portafoglio, è possibile aprire la scheda cliente dal riquadro Dettaglio informazioni e bloccare il cliente per le vendite future.  

## <a name="viewing-a-payment-prediction-for-a-specific-sales-document"></a>Visualizzazione di una previsione di pagamento per un documento di vendita specifico
È inoltre possibile prevedere i pagamenti in ritardo con anticipo. Nelle pagine **Offerte di vendita**, **Ordini di vendita** e **Fatture di vendita** è possibile utilizzare l' azione **Prevedi pagamento** per generare una previsione per il documento di vendita che si sta visualizzando.

<!--## Scheduling Payment Predictions
On the **Late Payment Prediction Setup** page you can schedule updates to payment predictions for a time that is convenient for you. -->

## <a name="building-your-own-predictive-model"></a>Creare un modello predittivo personalizzato
Per creare un modello predittivo personalizzato, è possibile utilizzare Azure Machine Learning Studio per definire un proprio modello predittivo e utilizzarlo in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Per utilizzare il proprio modello, è necessaria una sottoscrizione ad Azure Machine Learning. Per ulteriori informazioni, vedere la [documentazione di Azure Machine Learning Studio](https://go.microsoft.com/fwlink/?linkid=861765).  

Tuttavia, è disponibile un modo più semplice per creare e utilizzare il modello predittivo personalizzato. È possibile condividere i dati delle fatture con il [sistema sperimentale predittivo per Dynamics 365 Business Central](https://go.microsoft.com/fwlink/?linkid=2086310) in Azure Machine Learning e lasciare che il sistema sperimentale crei e formi un modello predittivo basato sui dati aziendali forniti. Per condividere i tuoi dati, nella pagina **Impostazione previsione pagamento ritardato**, selezionare l' azione **Crea modello personale**. In seguito, le previsioni si baseranno sul modello personalizzato e sui dati aziendali e non sui dati standard.  

> [!Note]
>   La qualità del modello è importante. Quando il sistema predittivo sperimentale usa i dati per preparare un modello, determina un valore di qualità per il modello come percentuale. La qualità del modello indica l'accuratezza delle previsioni del modello. Numerosi fattori possono influire sulla qualità di un modello. Ad esempio, questi fattori potrebbero essere una quantità insufficiente di dati oppure dati senza variazioni sufficienti. È possibile visualizzare la qualità del modello attualmente in uso nella pagina **Impostazione previsione pagamento ritardato**. È inoltre possibile specificare una soglia minima per la qualità del modello. I modelli con un valore di qualità inferiore alla soglia non produrranno previsioni.  

### <a name="to-use-your-model-instead-of-ours"></a>Per utilizzare un modello personalizzato al posto del modello predefinito  
Se si crea il proprio modello in Azure Machine Learning Studio, senza utilizzare gli strumenti di [!INCLUDE[d365fin](includes/d365fin_md.md)], è necessario fornire le credenziali in modo che [!INCLUDE[d365fin](includes/d365fin_md.md)] possa accedere al modello. A tale scopo, sono necessari alcuni passaggi:

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Impostazione previsione pagamento ritardato** e quindi scegliere il collegamento correlato.  
2. Scegliere la casella di controllo **Utilizza sottoscrizione di Azure personale**.  
3. Nel campo **Modello selezionato** selezionare **Modello personale**.  
4. Nella Scheda dettaglio **Credenziali modello personale**, immettere l'URL dell'API e la chiave API per il modello.  

## <a name="see-also"></a>Vedi anche  
[Documentazione di Azure Machine Learning Studio](https://go.microsoft.com/fwlink/?linkid=861765)  
[Personalizzazione di Business Central con le estensioni](ui-extensions.md)  
[Benvenuto in [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
