---
title: Come impostare e pubblicare servizi Web KPI basati sulle situazioni contabili | Microsoft Docs
description: Nella finestra **Impostazione servizio Web KPI situazione contabile**, si imposta come visualizzare i dati KPI della situazione contabile e su quali situazioni contabili specifiche basare i KPI.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 0f2f91a9813b07b0868043a4a2a3ed0b3f838536
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-and-publish-kpi-web-services-based-on-account-schedules"></a>Procedura: Impostare e pubblicare servizi Web KPI basati sulle situazioni contabili
Nella finestra **Impostazione servizio Web KPI situazione contabile**, si imposta come visualizzare i dati KPI della situazione contabile e su quali situazioni contabili specifiche basare i KPI. Quando si sceglie il pulsante **Pubblica servizio Web**, i dati KPI della situazione contabile specificati vengono aggiunti all'elenco di servizi Web pubblicati nella finestra **Servizi Web**.  

## <a name="to-set-up-and-publish-a-kpi-web-service-that-is-based-on-account-schedules"></a>Per impostare e pubblicare un servizio Web KPI basato sulle situazioni contabili  

1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Impostazione servizio Web KPI situazione contabile**, quindi scegliere il collegamento correlato.  
2.  Nella Scheda Dettaglio **Generale** compilare i campi come indicato nella tabella seguente.  

    |Campo|Description|  
    |---------------------------------|---------------------------------------|  
    |**Inizio valori previsti**|Specificare il momento nel tempo in cui i valori previsti vengono mostrati sull'indicatore KPI situazione contabile.<br /><br /> I valori previsti vengono recuperati dal budget di contabilità generale che si seleziona nel campo **Nome budget CG**. **Nota:**  Per ottenere gli indicatori KPI che mostrano le cifre previste dopo una determinata data e le cifre effettive prima della data, è possibile modificare il campo **Consenti registraz. da** nella finestra **Setup contabilità generale**. Per ulteriori informazioni, vedere Consenti registraz. da.|  
    |**Nome budget C/G**|Specificare il nome del budget di contabilità generale che fornisce i valori previsti al servizio Web KPI situazione contabile.|  
    |**Periodo**|Specificare il periodo su cui è basato il servizio Web KPI situazione contabile.|  
    |**Visualizza per**|Specificare l'intervallo di tempo in cui viene mostrato l'indicatore KPI situazione contabile.|  
    |**Nome servizio Web**|Specificare il nome del servizio Web KPI situazione contabile.<br /><br /> Il nome verrà visualizzato nel campo  **Nome servizio** della finestra **Servizi Web**.|  

    Continuare per specificare una o più situazioni contabili che si desidera pubblicare come servizio Web KPI in base all'impostazione effettuata nella tabella precedente.  

3.  Compilare i campi nella Scheda dettaglio **Situazioni contabili** come descritto nella tabella riportata di seguito.  

    |Campo|Description|  
    |---------------------------------|---------------------------------------|  
    |**Nome situazione contabile**|Specificare la situazione contabile sulla quale è basato il servizio Web KPI situazione contabile.|  
    |**Descrizione situazione contabile**|Specificare la descrizione della situazione contabile sulla quale è basato il servizio Web KPI situazione contabile.|  

4.  Ripetere il passaggio 3 per tutte le situazioni contabili su cui si desidera basare il servizio Web KPI situazione contabile.  
5.  Per visualizzare o modificare la situazione contabile selezionata, nella Scheda dettaglio **Situazione contabile**, scegliere l'azione **Modifica situazione contabile**.  
6.  Per visualizzare i dati KPI della situazione contabile impostati, scegliere l'azione **Servizio Web KPI situazione contabile**.  
7.  Per pubblicare il servizio Web KPI situazione contabile, scegliere l'azione **Pubblica servizio Web**. Il servizio Web viene aggiunto all'elenco dei servizi Web pubblicati nella finestra **Servizi Web**.  

    > [!NOTE]  
    >  È inoltre possibile pubblicare il servizio Web KPI puntando all'oggetto pagina **Impostazione servizio Web KPI situazione contabile** dalla finestra **Servizi Web**. Per ulteriori informazioni, vedere [Procedura: Pubblicare un servizio Web](https://msdn.microsoft.com/en-us/library/dd338978.aspx) su MSDN.  

## <a name="see-also"></a>Vedi anche  
[Business Intelligence](bi.md)  
[Finanze](finance.md)  
[Impostazione di dati finanziari](finance-setup-finance.md)  
[Contabilità generale e piano dei conti](finance-general-ledger.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

