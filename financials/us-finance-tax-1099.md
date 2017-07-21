---
title: Registrazione delle transazioni 1099 negli Stati Uniti | Documenti Microsoft
description: "Internal Revenue Service (IRS) richiede il modulo imposte 1099 per pagamenti ai fornitori, è possibile specificare che un documento di acquisto è soggetto al modulo 1099 e specificare il codice 1099 per il fornitore."
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
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: c20c52927aa979e56aeef7975fbcee1564ca4dd7
ms.contentlocale: it-it
ms.lasthandoff: 07/07/2017


---
# <a name="reporting-transactions-as-1099-liable-in-the-us"></a>Registrazione delle transazioni soggette a 1099 negli Stati Uniti

Internal Revenue Service (IRS) richiede una o più versioni del modulo imposte 1099 per pagamenti ai fornitori. Le copie di questi moduli devono essere inviate ai fornitori annualmente o prima dell'ultimo giorno di gennaio. Nei documenti di acquisto, è possibile specificare se il documento è soggetto a 1099, nonché specificare il codice 1099 per il fornitore.  

## <a name="1099-codes"></a>Codici 1099
In [!INCLUDE[d365fin](includes/d365fin_md.md)] i codici 1099 più comuni sono già impostati in modo che sia già tutto pronto per generare i report necessari. I codici sono definiti nella finestra **casella modulo 1099 IRS** in cui è possibile aggiungere nuovi codici 1099. Per ciascun fornitore soggetto a imposta, è possibile specificare il codice 1099 appropriato nella Scheda dettaglio **Pagamenti** nella scheda fornitore.  

Tramite il report **Informazioni 1099 fornitore**, è possibile analizzarne le transazioni 1099 pagate in un periodo specificato. Alla fine dell'anno, è possibile stampare le transazioni 1099 su moduli prestampati.  

## <a name="printing-1099-tax-forms"></a>Stampare moduli per imposte 1099
Nella finestra **casella modulo 1099 IRS**, è possibile accedere ai seguenti moduli di imposte:  

* 1099 DIV - Fornitore  

  Stampa il modulo federale 1099-DIV per dividendi e ripartizioni. È possibile stampare tutti i moduli 1099-DIV oppure solo moduli specifici. Il report utilizza i codici applicabili alle caselle di importi del modulo DIV dalla finestra **casella modulo 1099 IRS**.  
* 1099 INT - Fornitore  

  Stampa il modulo federale 1099-INT per proventi finanziari. È possibile stampare tutti i moduli 1099-INT oppure solo moduli specifici. Il report utilizza i codici applicabili alle caselle di importi del modulo INT dalla finestra **casella modulo 1099 IRS**.  
* 1099 MISC - Fornitore - Altri proventi  

  Stampa il modulo federale 1099-MISC per altri proventi. È possibile stampare tutti i moduli 1099-MISC oppure solo moduli specifici. Il report utilizza i codici applicabili alle caselle di importi del modulo MISC dalla finestra **casella modulo 1099 IRS**.  

Le modifiche normative che hanno effetto su questo report e sui dati della tabella vengono gestite in genere negli aggiornamenti di fine d'anno.
Si consiglia di eseguire il report **Informazioni 1099 fornitore** per verificare i dati prima della stampa dei moduli.

## <a name="submitting-1099-tax-forms-electronically"></a>Invio elettronico del modulo per imposte 1099
Per inviare elettronicamente il modulo per imposte 1099, utilizzare il report **Supporto magnetico 1099 fornitore**. Specificare i moduli 1099 che possono essere esportati. Le informazioni del modulo esportate da questo report sono identiche a quelle dei report di stampa dei moduli 1099 descritti nella precedente sezione.  

Il report utilizza i codici applicabili alle caselle di importi del modulo dalla finestra **casella modulo 1099 IRS**. I codici sono associati alle caselle del modulo nei layout di file del report, pertanto la versione della tabella dei dati e del report per un particolare anno fiscale devono corrispondere. Se qualsiasi codice personalizzato viene aggiunto alla tabella, deve essere mappato alle caselle del modulo in questo oggetto.  

Le modifiche normative che hanno effetto su questo report e sui dati della tabella vengono gestite in genere negli aggiornamenti di fine d'anno.
Si consiglia di eseguire il report **Informazioni 1099 fornitore** per verificare i dati prima della generazione del file elettronico.  

## <a name="see-also"></a>Vedi anche
[Procedura: Registrare nuovi fornitori](purchasing-how-register-new-vendors.md)  
[Procedura: Registrare gli acquisti](purchasing-how-record-purchases.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

