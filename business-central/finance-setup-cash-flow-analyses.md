---
title: Impostazione di un'analisi di un flusso di cassa| Documenti Microsoft
description: Impostare i grafici nella Gestione ruolo utente Conti per consentire di analizzare il flusso di denaro nell'attività commerciale, incluse uscite ed entrate, liquidità, incassi meno i pagamenti in contanti.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: money flow, expense and income, liquidity, cash receipts minus cash payments, Cartera, funds
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 442d16561321acc552a2cf39a1659d763e6f319a
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/29/2019
ms.locfileid: "1244080"
---
# <a name="setting-up-cash-flow-analysis"></a>Impostazione di un'analisi di un flusso di cassa
Se si desidera informazioni per decidere quali operazioni effettuare con i contanti, è possibile utilizzare i grafici nella Gestione ruolo utente Contabile:  

* **Ciclo di cassa**  
* **Entrate e uscite**  
* **Flusso di cassa**  
* **Previsioni flusso di cassa**  

In questo argomento viene descritta l'origine dei dati nei grafici e, se necessario, cosa fare per iniziare a utilizzare i grafici.  

## <a name="the-cash-cycle-and-income--expense-charts"></a>Grafici Ciclo di cassa ed Entrate e uscite
I grafici **Ciclo di cassa** ed **Entrate e spese** sono pronti per l'utilizzo, in base al piano dei conti e alle situazioni contabili. I conti sono all'origine dei dati e le situazioni contabili calcolano la relazione tra le vendite e gli incassi. Vengono forniti alcuni conti e situazioni contabili. È possibile utilizzarle così come sono, cambiarli e aggiungerne nuovi. Se si aggiungono conti C/G al piano dei conti, ad esempio importandoli da QuickBooks, sarà necessario mapparli ai conti nella pagina **Situazioni contabili** per i seguenti nomi della situazione contabile:  

| Nome situaz. contabile | Dove è utilizzato |
| --- | --- |
| **I_CACYCLE** |Ciclo di cassa |
| **I_CASHFLOW** |Flusso di cassa |
| **I_INCEXP** |Entrate e uscite |
| **I_MINTRIAL** |Come conto economico se non si utilizza il piano dei conti |

**Nota**: si consiglia di conservare i calcoli forniti per la situazione contabile.  

Immettere i conti nel campo **Totale** per **Totale ricavi**, **Totale contabilità clienti**, **Totale contabilità fornitori** e **Totale magazzino**. Per mappare a un intervallo dei conti, o a più di un conto specifico, immettere i numeri di conto separati da ".." o da una barra verticale, rispettivamente. Ad esempio, **1111..4444** o **2222|3333|5555**.  

**Suggerimento**: verificare la mappatura scegliendo l'azione **Panoramica**.  

## <a name="set-up-the-cash-flow-chart"></a>Impostare il grafico Flusso di cassa
Il grafico Flusso di cassa è basato sui seguenti elementi:  

* Un grafico dei conti di cassa.
* Una o più impostazioni del flusso di cassa. Specifica i conti da usare per contabilità generale, acquisti, vendite, servizi e cespiti.  

Per agevolare l'inizio, vengono forniti determinati conti ed impostazioni del flusso di cassa. È possibile aggiungerli, modificarli o rimuoverli.  

Per configurarli, cercare **conti di cassa**, selezionare il collegamento e compilare i campi. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Ripetere questa procedura per il **setup flusso di cassa**.  

## <a name="set-up-cash-flow-forecasts"></a>Impostare le previsioni flusso di cassa
Nel grafico **Previsione flusso di cassa** sono utilizzati i conti di cassa, le impostazioni del flusso di cassa e le previsioni dei flussi di cassa. Alcuni conti vengono forniti, tuttavia, è possibile impostare il proprio conto utilizzando una guida assistita di setup. La guida aiuta a specificare aspetti, quali la frequenza di aggiornamento della previsione, i conti sui cui basarla, le informazioni su quando effettuare i pagamenti delle imposte e se utilizzare [Cortana Intelligence](https://www.microsoft.com/en-us/cloud-platform/what-is-cortana-intelligence-suite).  

La previsione di flussi di cassa possono utilizzare Cortana Intelligence per includere i documenti con una data di scadenza in futuro. Il risultato una previsione è più completa. La connessione a Cortana Intelligence è già impostata. È solo necessario attivarla. Quando si accede a [!INCLUDE[d365fin](includes/d365fin_md.md)],viene visualizzata una notifica in una barra blue che fornisce un collegamento al setup del flusso di cassa predefinito. La notifica viene visualizzata solo una volta. Se la si chiude, ma si decide di attivare Cortana Intelligence, è possibile utilizzare la Guida assistita di setup, o un processo manuale.  

> [!NOTE]  
>   In alternativa, è possibile utilizzare il proprio servizio Web predittivo. Per ulteriori informazioni, vedere [Creare e utilizzare il proprio servizio Web predittivo per le previsioni di flussi di cassa](#AnchorText).  

Per utilizzare guida al setup assistito:  

1. Nella Gestione ruolo utente Contabile, nel grafico **Previsione flusso di cassa**, scegliere l'azione **Apri setup assistito**.  
2. Compilare i campi in ogni step della guida.  
3. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Previsione flusso di cassa** e quindi scegliere il collegamento correlato.
4. Nella pagina **Previsione flusso di cassa**, scegliere l'azione **Ricalcola previsione**.  

Per utilizzare una procedura manuale:  

1. Nella Gestione ruolo utente Contabile cercare **Setup flusso di cassa** quindi selezionare il collegamento correlato.  
2. Espandere la Scheda dettaglio **Cortana Intelligence**, quindi scegliere la casella **Cortana Intelligence abilitato**.  
3. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Previsione flusso di cassa** e quindi scegliere il collegamento correlato.
4. Nella pagina **Previsione flusso di cassa**, scegliere l'azione **Ricalcola previsione**.  

> [!TIP]  
>   Considerare la durata del periodo che il servizio utilizzerà nei suoi calcoli. Più dati immessi, più accurate saranno le previsioni. Inoltre, prestare attenzione a scostamenti ampi nei periodi. Influiranno anche sulle previsioni. Se Cortana Intelligence non trova una quantità sufficiente di dati o i dati variano molto, il servizio non farà una previsione.  

## <a name="AnchorText"> </a>Per ulteriori informazioni, vedere Creare e utilizzare il proprio servizio Web predittivo per le previsioni di flussi di cassa.
È inoltre possibile creare il proprio servizio Web predittivo basato su un modello pubblico denominato **Forecasting model per Microsoft Business Central**. Il modello predittivo è disponibile anche online nella raccolta Cortana Intelligence. Attenersi alla seguente procedura per utilizzare il modello:  

1. Aprire un browser e andare alla [Galleria Cortana Intelligence](https://go.microsoft.com/fwlink/?linkid=828352)  
2. Cercare il modello **Forecasting Model per Microsoft Business Central**, quindi aprirlo in Azure Machine Learning Studio.  
3. Utilizzare l'account Microsoft per impostare un'area di lavoro, quindi copiare il modello.  
4. Eseguire il modello e pubblicarlo come servizio Web.  
5. Prendere nota dell'URL API e della chiave API. Usare queste le credenziali per un setup del flusso di cassa.  
6. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup flusso di cassa** e quindi scegliere il collegamento correlato.  
7. Espandere la Scheda dettaglio **Cortana Intelligence** e compilare i campi.  

## <a name="see-also"></a>Vedi anche
[Analizzare il flusso di cassa dell'azienda](finance-analyze-cash-flow.md)  
[Impostazione di dati finanziari](finance-setup-finance.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
