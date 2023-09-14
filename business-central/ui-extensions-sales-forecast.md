---
title: Utilizzo delle previsioni di vendita e magazzino per gestire magazzino | Documenti Microsoft
description: 'Questa estensione consente di effettuare previsioni relative alle vendite, offre una chiara panoramica del magazzino in esaurimento e consente di creare richieste di approvvigionamento per i fornitori.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'app, add-in, manifest, customize, budget'
ms.search.form: '1850, 1851, 1853,'
ms.date: 12/20/2021
ms.author: bholtorf
---

# Estensione Previsione vendite e magazzino

La Gestione del magazzino è un trade-off tra l'assistenza clienti e la gestione dei costi. Da un lato, un magazzino basso richiede meno capitale di lavoro, ma dall'altro un magazzino in esaurimento potenzialmente porta a vendite mancate. L'estensione Previsione vendite e magazzino prevede le vendite potenziali utilizzando i dati storici e fornisce una chiara panoramica delle scorte esaurite previste. A seconda della previsione, l'estensione consente di creare le richieste di approvvigionamento per i fornitori e quindi di risparmiare tempo.  

## Impostazione delle previsioni

In [!INCLUDE[prod_short](includes/prod_short.md)], la connessione a [Azure AI](https://azure.microsoft.com/overview/ai-platform/) è già impostata. Tuttavia è possibile configurare la previsione per utilizzare un tipo diverso del periodo per il report, ad esempio cambiare dalle previsioni in base al mese alle previsioni in base al trimestre. È inoltre possibile scegliere il numero di periodi per calcolare la previsione, a seconda dei dettagli si desidera includere nella previsione. Si suggerisce di effettuare una previsione in base al mese e con un orizzonte di 12 mesi.

> [!TIP]  
> Considerare la durata del periodo che il servizio utilizzerà nei suoi calcoli. Più dati immessi, più accurate saranno le previsioni. Inoltre, prestare attenzione a scostamenti ampi nei periodi. Influiranno anche sulle previsioni. Se Azure AI non trova una quantità sufficiente di dati o i dati variano molto, il servizio non farà una previsione.

## Usare le previsioni

L'estensione utilizza Azure AI per stimare le vendite future in base allo storico delle vendite allo scopo di evitare l'insufficienza di scorte. Ad esempio, quando si sceglie un articolo nella pagina **Articoli**, nel grafico **Previsione articolo** vengono visualizzate le vendite stimate dell'articolo nel periodo futuro. In questo modo è possibile vedere se si stanno per esaurire le scorte dell'articolo.  

È inoltre possibile utilizzare l'estensione per suggerire quando rifornire il magazzino. Ad esempio, se si crea un ordine di acquisto per Fabrikam perché si desidera acquistare la loro nuova sedia da scrittorio, l'estensione Previsione vendite e magazzino suggerisce anche di rifornirsi della poltrona girevole LONDRA che in genere viene acquistata da questo fornitore. Ciò avviene in quanto l'estensione prevede che le scorte della poltrona girevole LONDRA si esauriranno nel prossimo bimestre e pertanto è possibile che si desideri ordinare già da ora altre sedie.  

## Dettagli di progettazione

Gli abbonamenti per [!INCLUDE[prod_short](includes/prod_short.md)] vengono forniti con l'accesso a diversi servizi Web predittivi in tutte le aree geografiche in cui [!INCLUDE[prod_short](includes/prod_short.md)] è disponibile. Per ulteriori informazioni, vedere Guida alle licenze di Microsoft Dynamics 365 Business Central. La guida è disponibile per il download sul sito Web di [Business Central](https://dynamics.microsoft.com/en-us/business-central/overview/). 

Questi servizi Web sono apolidi, nel senso che utilizzano i dati solo per calcolare previsioni su richiesta. Non memorizzano dati.

> [!NOTE]  
>   In alternativa, è possibile utilizzare il proprio servizio Web predittivo. Per ulteriori informazioni, vedere [Creare e utilizzare il proprio servizio Web predittivo per le previsioni di magazzino e vendite](#AnchorText). 

### Dati richiesti per la previsione

Per fare previsioni sulle vendite future, il servizio Web richiede dati quantitativi sulle vendite passate. Questi dati provengono dai campi **Data di registrazione**, **Nr. Articolo**, e **Quantità** nella pagina **Mov. contabili articoli**, dove:

- Il tipo di movimento è "Vendite".
- La data di registrazione è tra la data calcolata in base ai valori nei campi **Periodi storici** e **Tipo di periodo** della pagina **Setup previsione vendite e magazzino** e la data del lavoro.

Prima di utilizzare il servizio Web [!INCLUDE[prod_short](includes/prod_short.md)] comprime le transazioni di **Nr. Articolo** e **Data di registrazione** in base al valore nel campo **Tipo di periodo** della pagina **Setup previsione vendite e magazzino**.

## <a name="AnchorText"> </a>Creare e utilizzare il proprio servizio Web predittivo per le previsioni di magazzino e vendite

È inoltre possibile creare il proprio servizio Web predittivo basato su un modello pubblico denominato **Forecasting model per Microsoft Business Central**. Il modello predittivo è disponibile anche online nella raccolta Azure AI. Attenersi alla seguente procedura per utilizzare il modello:  

1. Aprire un browser e accedere alla [Azure AI Gallery](https://go.microsoft.com/fwlink/?linkid=828352)  
2. Cercare il modello **Forecasting Model per Microsoft Business Central**, quindi aprirlo in Azure Machine Learning Studio.  
3. Utilizzare l'account Microsoft per impostare un'area di lavoro, quindi copiare il modello.  
4. Eseguire il modello e pubblicarlo come servizio Web.  
5. Prendere nota dell'URL API e della chiave API. Usa queste le credenziali per un setup del flusso di cassa.  
6. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Setup previsione vendite e magazzino**, quindi scegli il collegamento correlato.  
7. Espandere la Scheda dettaglio **Generale** e compilare i campi URL API e Chiave API.  

## Vedi il relativo [training Microsoft](/training/modules/use-sales-inventory-forecast-extension/)

## Vedere anche

[Vendite](sales-manage-sales.md)  
[Magazzino](inventory-manage-inventory.md)  
[Personalizzazione di [!INCLUDE[prod_short](includes/prod_short.md)] utilizzando le estensioni](ui-extensions.md)  
[Usare l'intelligenza artificiale in Microsoft Dynamics 365 Business Central](/training/paths/use-artificial-intelligence/)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
