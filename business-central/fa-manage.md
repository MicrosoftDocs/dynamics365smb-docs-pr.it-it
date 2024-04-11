---
title: Gestione cespiti (video)
description: Ottenere informazioni sulla funzionalità dei cespiti e una panoramica delle modalità di utilizzo e gestione dei cespiti.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.search.keywords: 'machinery, buildings'
ms.search.form: '5604, 5606, 5664, 5601, 5602, 5658, 5603, 5671, 5641, 5629, 5633, 5634, 5649, 5622, 5650'
ms.date: 03/25/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="manage-fixed-assets"></a>Gestire i cespiti

La funzionalità Cespiti di [!INCLUDE[prod_short](includes/prod_short.md)] fornisce una sintesi dei cespiti e garantisce che l'ammortamento periodico venga calcolato in modo corretto. Consente, inoltre, di tenere traccia dei costi di manutenzione, di gestire polizze assicurative, di registrare transazioni di cespiti e di generare diversi report e statistiche.

## <a name="video-overview"></a>Video di panoramica

Il video seguente illustra le nozioni di base dei cespiti:

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4AegS?rel=0]

## <a name="fixed-assets-overview"></a>Panoramica dei cespiti

Per ogni cespite occorre impostare una scheda che ne riporti le relative informazioni. È possibile impostare edifici o attrezzature di produzione come bene principale con un elenco di componenti ed è possibile raggrupparli in vari modi, ad esempio per classe, reparto o ubicazione. È quindi possibile iniziare ad acquistare, gestire e vendere i cespiti. È possibile anche impostare i cespiti previsti. L'impostazione di budget ti consente di includere qualsiasi vendita e acquisto previsti nei report.

> [!IMPORTANT]
> Per poter gestire i cespiti, devi dapprima completare le seguenti configurazioni:
>
> * Valori predefiniti
> * Contabilità cespiti
> * Categorie registrazione
> * Chiavi di allocazione
> * Registrazioni cespiti
>
> Per ulteriori informazioni, vedere [Impostazione di cespiti](fa-setup.md).

Per tenere traccia degli ammortamenti dei cespiti e altre transazioni finanziarie per cespiti, imposta uno o più registri beni ammortizzabili per ogni cespite. L'ammortamento viene eseguito mediante l'esecuzione di un report per calcolare l'ammortamento periodico, la compilazione della registrazione con i movimenti risultanti e infine la contabilizzazione della registrazione. [!INCLUDE[prod_short](includes/prod_short.md)] supporta diversi metodi di ammortamento. Per ulteriori informazioni, vedere [Metodi di ammortamento](fa-depreciation-methods.md). È possibile impostare più registri beni ammortizzabili per ogni cespite per scopi differenti, ad esempio uno per il reporting dell'IVA e un altro per il reporting interno.

È possibile registrare i costi di manutenzione e la data del prossimo intervento per ogni bene. Può essere importante tenere traccia delle spese di manutenzione ai fini dell'impostazione del budget e per decidere se un cespite debba essere sostituito.

Puoi associare ciascun cespite a una o più polizze assicurative e verificare che i premi della polizza siano allineati al valore dei cespiti.

> [!NOTE]  
> È possibile registrare le transazioni dei cespiti nella pagina **Reg. cespiti in G/L** o **Registraz. cespiti**, a seconda se le transazioni sono per la creazione di rendiconti finanziari o per la gestione interna. Nella Guida per i cespiti viene descritto solo come utilizzare la pagina **Reg. cespiti in G/L**. Per ulteriori informazioni, vedere [Impostare l'ammortamento cespiti](fa-how-setup-depreciation.md).

## <a name="how-to-use-fixed-assets"></a>Come utilizzare i cespiti

Nella tabella seguente viene descritta una sequenza di attività, con collegamenti agli articoli che le descrivono.

| A  | Vedere |
| --- | --- |
| Impostare prerequisiti per l'uso della funzionalità di cespiti (definire valori di default, contabilità dei cespiti, categorie di registrazione, chiavi di allocazione, registrazioni e tipi di registrazione). | [Impostazione di cespiti](fa-setup.md)|
| Creazione di cespiti, assegnazione di metodi di ammortamento, registrazione di acquisti, valori di realizzo e stampa di liste di cespiti. |[Acquisire i cespiti](fa-how-acquire.md) |
| Registrare le visite di assistenza, pubblicare e monitorare i costi di manutenzione. |[Gestione di cespiti](fa-how-maintain.md) |
| Aggiornare informazioni di assicurazione, registrare costi di acquisto in polizze assicurative, modificare la copertura assicurativa, visualizzare le statistiche di assicurazione e creare liste delle polizze assicurative. |[Assicurazione di cespiti](fa-how-insure.md) |
| Riclassificazione dei cespiti, trasferimento dei cespiti in ubicazioni diverse, suddivisione o raggruppamento dei cespiti. |[Trasferimento, divisione o combinazione di cespiti](fa-how-trans-split-combine.md) |
| Rettifica dei valori dei cespiti, registrazione dell'ammortamento e di transazioni di svalutazione. |[Rivalutazione dei cespiti](fa-how-revalue.md) |
| Calcolo dell'ammortamento, registrazione dell'ammortamento e analisi dell'ammortamento nei report sui cespiti. |[Ammortamento dei cespiti](fa-how-depreciate-amortize.md) |
| Ulteriori informazioni sui diversi metodi di ammortamento del cespite. |[Metodi di ammortamento](fa-depreciation-methods.md) |
| Registrazione di transazioni di cessione, visualizzazione dei movimenti contabili di cessione e registrazione di cessioni parziali. |[Smaltimento o ritiro dei cespiti](fa-how-dispose-retire.md) |
| Gestire budget per cespiti, costi di acquisto previsti, previsioni di cessione dei cespiti e previsioni di ammortamento. |[Gestione dei budget per i cespiti](fa-how-manage-budgets.md) |
| Ulteriori informazioni sulle funzionalità di reporting e analisi predefinite per cespiti. | [Report cespiti e analisi](fa-reports.md) |

## <a name="see-also"></a>Vedere anche

[Impostazione di cespiti](fa-setup.md)  
[Panoramica dei dati finanziari](finance.md)  
[Prepararsi a fare affari](ui-get-ready-business.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Modificare le funzionalità visualizzate](ui-experiences.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
