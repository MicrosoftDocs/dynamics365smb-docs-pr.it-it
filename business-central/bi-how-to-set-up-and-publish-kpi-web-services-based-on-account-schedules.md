---
title: Impostare e pubblicare servizi Web KPI per le situazioni contabili
description: In questo argomento viene descritto come visualizzare i dati KPI della situazione contabile in base alle situazioni contabili specifiche.
author: bholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.form: 103, 104, 197, 196, 195, 198, 490, 764, 765, 766
ms.date: 06/15/2021
ms.author: bholtorf
ms.openlocfilehash: 29816a5812ce5d5cfe19b8c27b475ddd2090710f
ms.sourcegitcommit: cdb57f14960f58b1d36a1b373fbf35dfed5fad9e
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/23/2022
ms.locfileid: "8335424"
---
# <a name="set-up-and-publish-kpi-web-services-based-on-account-schedules"></a>Impostare e pubblicare servizi Web KPI basati sulle situazioni contabili
Nella pagina **Impostazione servizio Web KPI situazione contabile**, si imposta come visualizzare i dati KPI della situazione contabile e su quali situazioni contabili specifiche basare i KPI. Quando si sceglie il pulsante **Pubblica servizio Web**, i dati KPI della situazione contabile specificati vengono aggiunti all'elenco di servizi Web pubblicati nella pagina **Servizi Web**.  

> [!NOTE]
> Quando utilizzi questo servizio web, le date di chiusura non sono incluse nel tuo set di dati. Ciò ti consente di utilizzare i filtri in Power BI per analizzare vari periodi di tempo.

## <a name="to-set-up-and-publish-a-kpi-web-service-that-is-based-on-account-schedules"></a>Per impostare e pubblicare un servizio Web KPI basato sulle situazioni contabili  
1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Impostazione servizio Web KPI situazione contabile**, quindi seleziona il collegamento correlato.  
2.  Nella Scheda Dettaglio **Generale** compilare i campi come indicato nella tabella seguente.  

    |Campo|Descrizione|  
    |---------------------------------|---------------------------------------|  
    |**Inizio valori previsti**|Specificare il momento nel tempo in cui i valori previsti vengono mostrati sull'indicatore KPI situazione contabile.<br /><br /> I valori previsti vengono recuperati dal budget di contabilità generale che si seleziona nel campo **Nome budget CG**. **Nota:**  Per ottenere gli indicatori KPI che mostrano le cifre previste dopo una determinata data e le cifre effettive prima della data, è possibile modificare il campo **Consenti registraz. da** nella pagina **Setup contabilità generale**. Per ulteriori informazioni, vedere Consenti registraz. da.|  
    |**Nome budget C/G**|Specificare il nome del budget di contabilità generale che fornisce i valori previsti al servizio Web KPI situazione contabile.|  
    |**Periodo**|Specificare il periodo su cui è basato il servizio Web KPI situazione contabile.|  
    |**Visualizza per**|Specificare l'intervallo di tempo in cui viene mostrato l'indicatore KPI situazione contabile.|  
    |**Nome servizio Web**|Specificare il nome del servizio Web KPI situazione contabile.<br /><br /> Il nome verrà visualizzato nel campo **Nome servizio** della pagina **Servizi Web**.|  

    Specificare una o più situazioni contabili che si desidera pubblicare come servizio Web KPI in base all'impostazione effettuata nella tabella precedente.  

3.  Compilare i campi nella Scheda dettaglio **Situazioni contabili** come descritto nella tabella riportata di seguito.  

    |Campo|Descrizione|  
    |---------------------------------|---------------------------------------|  
    |**Nome situazione contabile**|Specificare la situazione contabile sulla quale è basato il servizio Web KPI situazione contabile.|  
    |**Descrizione situazione contabile**|Specificare la descrizione della situazione contabile sulla quale è basato il servizio Web KPI situazione contabile.|  

4.  Ripetere il passaggio 3 per tutte le situazioni contabili su cui si desidera basare il servizio Web KPI situazione contabile.  
5.  Per visualizzare o modificare la situazione contabile selezionata, nella Scheda dettaglio **Situazione contabile**, scegliere l'azione **Modifica situazione contabile**.  
6.  Per visualizzare i dati KPI della situazione contabile impostati, scegliere l'azione **Servizio Web KPI situazione contabile**.  
7.  Per pubblicare il servizio Web KPI situazione contabile, scegliere l'azione **Pubblica servizio Web**. Il servizio Web viene aggiunto all'elenco dei servizi Web pubblicati nella pagina **Servizi Web**.  

> [!NOTE]  
>  È inoltre possibile pubblicare il servizio Web KPI puntando all'oggetto pagina **Impostazione servizio Web KPI situazione contabile** dalla pagina **Servizi Web**. Per ulteriori informazioni, vedere [Pubblicare un servizio Web](across-how-publish-web-service.md).  

## <a name="see-also"></a>Vedi anche  
[Business Intelligence](bi.md)  
[Finanze](finance.md)  
[Impostazione di dati finanziari](finance-setup-finance.md)  
[Contabilità generale e piano dei conti](finance-general-ledger.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]