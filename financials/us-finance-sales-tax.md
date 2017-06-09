---
title: Imposte di vendita e categorie fiscali negli Stati Uniti e in Canada | Documenti Microsoft
description: Vengono fornite informazioni sulla configurazione delle imposte di vendita e sul funzionamento delle categorie fiscali, delle aree imposte, delle giurisdizioni fiscali e dei dettagli imposta.
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: local
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: ff1981a428a2cd3b3864b7f0cc795a1abeab7a10
ms.contentlocale: it-it
ms.lasthandoff: 05/04/2017


---
# <a name="sales-tax-and-tax-groups-in-the-us-and-canada"></a>Imposte di vendita e categorie fiscali negli Stati Uniti e in Canada
La prima volta che si avvia [!INCLUDE[d365fin](includes/d365fin_md.md)] è possibile eseguire una guida al setup assistito per impostare in modo semplice e rapido le informazioni fiscali della società, dei clienti e dei fornitori. In pochi minuti si è pronti a creare documenti di vendita e di acquisto con le imposte calcolate correttamente. Una spiegazione dettagliata è disponibile nel [nostro post del blog](https://madeira.microsoft.com/blog/sales-tax-setup-made-easy).
Se si passa a una società vuota, consigliamo di iniziare utilizzando ciascuna guida al setup assistito, inclusa quella per le imposte di vendita. Se si preferisce impostare le imposte manualmente, questo articolo spiega i fattori da tenere in considerazione.  

## <a name="tax-groups-tax-areas-and-tax-jurisdictions"></a>Categorie fiscali, aree imposte e giurisdizioni fiscali
In [!INCLUDE[d365fin](includes/d365fin_md.md)] una categoria fiscale rappresenta un gruppo di articoli in magazzino o di risorse assoggettati alle stesse aliquote. Ad esempio, è possibile impostare una categoria fiscale per gli articoli tassabili e un'altra per gli articoli non soggetti a tassazione. È necessario assegnare i codici di categoria fiscale agli articoli di magazzino e ai conti C/G. Analogamente, è necessario assegnare i codici area imposte ai clienti, alle ubicazioni e alle impostazioni della società. Queste assegnazioni possono essere effettuate tramite la guida al setup assistito.  

Ogni area imposte è un raggruppamento delle giurisdizioni fiscali basate su una determinata ubicazione geografica. Ad esempio, l'area imposte di Miami, Florida, include tre giurisdizioni fiscali: città (Miami), provincia (Dade) e stato (Florida). [!INCLUDE[d365fin](includes/d365fin_md.md)] include un set di aree imposte limitato con una configurazione predefinita, ma è possibile modificare queste aree e aggiungerne di nuove.  

Se si creano nuove aree e giurisdizioni fiscali è necessario verificare di completare correttamente i campi. Negli Stati Uniti gli stati, le province, le città e le località possono applicare l'imposta di vendita. In Canada, il governo federale e le province possono imporre le imposte di vendita. Le società incassano e rimettono queste imposte alle autorità governative per i prodotti venduti agli utenti finali. Le imposte di vendita possono inoltre essere sommate a un'imposta di vendita esistente. Ad esempio, un'imposta può essere calcolata su un importo di fattura di vendita che già include le imposte di altre giurisdizioni.  

In Canada, gli importi fiscali devono essere dettagliati nei documenti per ogni giurisdizione fiscale. In un documento possono comparire fino a un massimo di quattro giurisdizioni e le giurisdizioni che hanno lo stesso ordine di stampa vengono combinate quando vengono stampate.  

## <a name="tax-details"></a>Dettagli imposta
Nella finestra **Dettagli imposta** vengono mostrate le differenti combinazioni delle giurisdizioni fiscali e delle categorie di imposte per determinare le aliquote. Per ogni giurisdizione fiscale, è consigliabile impostare una categoria di imposte per la tassazione normale, un'altra categoria per gli articoli o i servizi che non sono soggetti a tassazione e una categoria aggiuntiva per ogni tipo di articolo o servizio gestito con un'aliquota differente in quella giurisdizione.  

Negli Stati Uniti, quando si vende a un cliente presso un'ubicazione in cui non si ha una *sede* legale, non si incassano le imposte. Per le ubicazioni in cui non è presente una sede legale, assicurarsi che entrambi i campi **Imposta sotto minimo** e **Imposta sopra massimo** siano impostati su 0,00.  

## <a name="see-also"></a>Vedi anche
[Finanza](finance.md)  
[Impostazione di dati finanziari](finance-setup-finance.md)  
[Imposte sulla vendita e Goods and Services Tax in Canada](ca-finance-tax.md)  
[Setup semplificato delle imposte](https://madeira.microsoft.com/blog/sales-tax-setup-made-easy)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

