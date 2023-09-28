---
title: Impostazione di un'analisi di un flusso di cassa (video)
description: 'Usa i grafici della Gestione ruolo utente Contabile per analizzare il flusso di denaro nell''attività commerciale, incluse uscite ed entrate, liquidità, incassi meno i pagamenti in contanti.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'money flow, expense and income, liquidity, cash receipts minus cash payments, Cartera, funds'
ms.search.form: '846, 847, 849, 851, 855, 862, 869, 1818'
ms.date: 08/23/2022
ms.author: bholtorf
---
# <a name="setting-up-cash-flow-analysis"></a>Impostazione di un'analisi di un flusso di cassa

Se si desidera informazioni per decidere quali operazioni effettuare con i contanti, è possibile utilizzare i grafici nella Gestione ruolo utente Contabile:

* **Ciclo di cassa**  
* **Entrate e uscite**  
* **Flusso di cassa**  
* **Previsioni flusso di cassa**  

In questo articolo viene descritta l'origine dei dati nei grafici e, se necessario, cosa fare per iniziare a utilizzare i grafici.
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4mJhc?rel=0]

## <a name="the-cash-cycle-and-income--expense-charts"></a>Grafici Ciclo di cassa ed Entrate e uscite

I grafici **Ciclo di cassa** ed **Entrate e spese** sono pronti per l'utilizzo, in base al piano dei conti e ai report finanziari. I conti sono all'origine dei dati e i report finanziari calcolano la relazione tra le vendite e gli incassi. Vengono forniti alcuni conti e report finanziari. È possibile utilizzarle così come sono, cambiarli e aggiungerne nuovi. Se si aggiungono conti C/G al piano dei conti, ad esempio importandoli da QuickBooks, sarà necessario mapparli ai conti nella pagina **Report finanziari** per i seguenti report:

| Nome report finanziario | Dove è utilizzato |
| --- | --- |
| **I_CACYCLE** |Ciclo di cassa |
| **I_CASHFLOW** |Flusso di cassa |
| **I_INCEXP** |Entrate e uscite |
| **I_MINTRIAL** |Come conto economico se non si utilizza il piano dei conti |

> [!NOTE]
> Si consiglia di conservare i calcoli forniti per il report finanziario.

Immettere i conti nel campo **Totale** per **Totale ricavi**, **Totale contabilità clienti**, **Totale contabilità fornitori** e **Totale magazzino**. Per eseguire il mapping a un intervallo di conti, inserisci i numeri di conto separati da ".." come in **1111..4444**. In alternativa, per eseguire il mapping a conti specifici, inserisci i numeri di conto separati da una barra verticale come in **2222|3333|5555**.  

> [!TIP] 
> Verifica la mappatura scegliendo l'azione **Panoramica**.  

## <a name="set-up-the-cash-flow-chart"></a>Impostare il grafico Flusso di cassa

Il grafico Flusso di cassa è basato su:  

* Un grafico dei conti di cassa.
* Una o più impostazioni del flusso di cassa. Queste impostazioni specificano i conti da usare per contabilità generale, acquisti, vendite, servizi e cespiti.  

Per agevolare l'inizio, vengono forniti determinati conti ed impostazioni del flusso di cassa. È possibile aggiungerli, modificarli o rimuoverli.  

Per configurare i conti, cerca **Piano dei conti di cassa**, seleziona il collegamento e compila i campi. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Ripeti questa procedura per il **setup flusso di cassa**.

## <a name="set-up-cash-flow-forecasts"></a>Impostare le previsioni flusso di cassa

Nel grafico **Previsione flusso di cassa** sono utilizzati i conti di cassa, le impostazioni del flusso di cassa e le previsioni dei flussi di cassa. Alcuni conti vengono forniti, tuttavia, è possibile impostare il proprio conto utilizzando una guida assistita di setup. La guida aiuta a specificare aspetti, quali la frequenza di aggiornamento della previsione, i conti sui cui basarla, le informazioni su quando effettuare i pagamenti delle imposte e se utilizzare [Azure AI](https://azure.microsoft.com/overview/ai-platform/).  

Le previsioni del flusso di cassa possono usare l'intelligenza artificiale di Azure per creare una previsione più completa. La connessione a Azure AI è già impostata. È solo necessario attivarla. Quando accedi a [!INCLUDE[prod_short](includes/prod_short.md)], viene visualizzata una notifica in una barra blue che fornisce un collegamento al setup del flusso di cassa predefinito. La notifica viene visualizzata solo una volta. Se la chiudi, ma poi decidi di attivare Azure AI, è possibile utilizzare la Guida assistita di setup, o un processo manuale.  

> [!NOTE]
>
> In alternativa, è possibile utilizzare il proprio servizio Web predittivo. Per ulteriori informazioni, vedere [Creare e utilizzare il proprio servizio Web predittivo per le previsioni di flussi di cassa](#AnchorText).  

Per utilizzare guida al setup assistito:  

1. Nella Gestione ruolo utente Contabile, nel grafico **Previsione flusso di cassa**, scegliere l'azione **Apri setup assistito**.
2. Compilare i campi in ogni step della guida. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Di nuovo nella Gestione ruolo utente Contabile, nel grafico **Previsione flusso di cassa**, scegli l'azione **Ricalcola previsione**.

Per utilizzare una procedura manuale:  

1. Nella Gestione ruolo utente Contabile, scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Setup flusso di cassa**, quindi seleziona il collegamento correlato.
2. Espandi la Scheda dettaglio **Azure AI**, quindi scegli il campo **Abilitato da Azure AI**.
3. Di nuovo nella Gestione ruolo utente Contabile, nel grafico **Previsione flusso di cassa**, scegli l'azione **Ricalcola previsione**.

> [!TIP]  
> Considerare la durata del periodo che il servizio utilizzerà nei suoi calcoli. Più dati immessi, più accurate saranno le previsioni. Inoltre, prestare attenzione a scostamenti ampi nei periodi. Influiranno anche sulle previsioni. Se Azure AI non trova una quantità sufficiente di dati o i dati variano molto, il servizio non farà una previsione.  

## <a name="design-details"></a>Dettagli di progettazione

Gli abbonamenti per [!INCLUDE[prod_short](includes/prod_short.md)] vengono forniti con l'accesso a diversi servizi Web predittivi in tutte le aree geografiche in cui [!INCLUDE[prod_short](includes/prod_short.md)] è disponibile. Per ulteriori informazioni, vedi Guida alle licenze di Microsoft Dynamics 365 Business Central. La guida è disponibile per il download sul sito Web di [Business Central](https://dynamics.microsoft.com/business-central/overview/).

Questi servizi Web sono apolidi, nel senso che utilizzano i dati solo per calcolare previsioni su richiesta. Non memorizzano dati.

> [!NOTE]
>
> In alternativa, è possibile utilizzare il proprio servizio Web predittivo. Per ulteriori informazioni, vedere [Creare e utilizzare il proprio servizio Web predittivo per le previsioni di flussi di cassa](#AnchorText).

### <a name="data-required-for-forecast"></a>Dati richiesti per la previsione

Per effettuare previsioni su entrate e spese future, i servizi Web richiedono dati storici su crediti, debiti e tasse.

#### <a name="receivables"></a>Contabilità clienti

I campi **Scadenza**, **Importo (VL)** della pagina **Movimenti contabili clienti**, dove:

* Il tipo di documento è *Fattura* o *Nota di credito*.
* La data di scadenza è tra la data calcolata in base ai valori nei campi **Periodi storici** e **Tipo di periodo** della pagina **Setup flusso di cassa** e la data del lavoro.

Prima di utilizzare il servizio Web predittivo [!INCLUDE[prod_short](includes/prod_short.md)] comprime le transazioni per **Scadenza** in base al valore nel campo **Tipo di periodo** della pagina **Setup flusso di cassa**.

#### <a name="payables"></a>Contabilità fornitori

I campi **Scadenza**, **Importo (VL)** della pagina **Movimenti contabili fornitori**, dove:

* Il tipo di documento è *Fattura* o *Nota di credito*.
* La data di scadenza è tra la data calcolata in base ai valori nei campi **Periodi storici** e **Tipo di periodo** della pagina **Setup flusso di cassa** e la data del lavoro.

Prima di utilizzare il servizio Web predittivo [!INCLUDE[prod_short](includes/prod_short.md)] comprime le transazioni per **Scadenza** in base al valore nel campo **Tipo di periodo** della pagina **Setup flusso di cassa**.

#### <a name="tax"></a>Imposta

I campi **Data documento**, **Importo (VAT)** della pagina **Movimenti contabili IVA**, dove:

* Il tipo di documento è *vendite*.
* La data del documento è tra la data calcolata in base ai valori nei campi **Periodi storici** e **Tipo di periodo** della pagina **Setup flusso di cassa** e la data del lavoro.

Prima di utilizzare il servizio Web predittivo [!INCLUDE[prod_short](includes/prod_short.md)] comprime le transazioni per **Data del documento** in base al valore nel campo **Tipo di periodo** della pagina **Setup flusso di cassa**.

## <a name="create-and-use-your-own-predictive-web-service-for-cash-flow-forecasts"></a><a name="AnchorText"></a>Creare e utilizzare il proprio servizio Web predittivo per le previsioni di flussi di cassa

È inoltre possibile creare il proprio servizio Web predittivo basato su un modello pubblico denominato **Forecasting model per Microsoft Business Central**. Il modello predittivo è disponibile anche online nella raccolta Azure AI. Attenersi alla seguente procedura per utilizzare il modello:  

1. Aprire un browser e accedere alla [Azure AI Gallery](https://go.microsoft.com/fwlink/?linkid=828352)  
2. Cerca il modello **Forecasting Model per Microsoft Business Central**, quindi aprilo in Microsoft Azure Machine Learning Studio.  
3. Utilizzare l'account Microsoft per impostare un'area di lavoro, quindi copiare il modello.  
4. Eseguire il modello e pubblicarlo come servizio Web.  
5. Prendere nota dell'URL API e della chiave API. Usa queste le credenziali per un setup del flusso di cassa.  
6. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Setup flusso di cassa**, quindi seleziona il collegamento correlato.  
7. Espandi la Scheda dettaglio **Azure per intelligenza artificiale** e quindi compila i campi, inclusi l'URL dell'API e la chiave API forniti da Azure Machine Learning Studio. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
8. Nella Gestione ruolo utente Contabile, nel grafico **Previsione flusso di cassa**, scegli l'azione **Ricalcola previsione**.

## <a name="see-also"></a>Vedere anche

[Analizzare il flusso di cassa dell'azienda](finance-analyze-cash-flow.md)  
[Impostazione di dati finanziari](finance-setup-finance.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
