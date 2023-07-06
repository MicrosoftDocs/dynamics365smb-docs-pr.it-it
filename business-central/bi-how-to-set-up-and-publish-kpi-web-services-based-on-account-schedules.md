---
title: Impostare e pubblicare servizi Web KPI basati sui report finanziari
description: In questo articolo viene descritto come visualizzare i dati KPI del report finanziario in base a report finanziari specifici.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 12/16/2022
ms.custom: bap-template
ms.search.form: '103, 104, 108, 195, 196, 197, 198, 489, 490, 764, 765, 766'
---
# <a name="set-up-and-publish-kpi-web-services-based-on-financial-reports"></a><a name="set-up-and-publish-kpi-web-services-based-on-financial-reports"></a><a name="set-up-and-publish-kpi-web-services-based-on-financial-reports"></a>Impostare e pubblicare servizi Web KPI basati sui report finanziari

Nella pagina **Impostazione servizio Web KPI report finanziario**, si imposta come visualizzare i dati KPI del report finanziario e su quali report finanziari specifici basare i KPI. Quando scegli **Pubblica servizio Web**, i dati KPI del report finanziario specificati vengono aggiunti all'elenco di servizi Web pubblicati nella pagina **Servizi Web**.

> [!NOTE]
> Quando utilizzi questo servizio web, le date di chiusura non sono incluse nel tuo set di dati. Puoi utilizzare i filtri in Power BI per analizzare vari periodi di tempo.

## <a name="set-up-and-publish-a-kpi-web-service-based-on-financial-reports"></a><a name="set-up-and-publish-a-kpi-web-service-based-on-financial-reports"></a><a name="set-up-and-publish-a-kpi-web-service-based-on-financial-reports"></a>Impostare e pubblicare servizi Web KPI basati sui report finanziari
  
1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Impostazione servizio Web KPI report finanziario**, quindi seleziona il collegamento correlato.
2. Compila i campi della Scheda dettaglio **Generale**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Nella Scheda dettaglio **Definizioni riga**, riempire i campi.
4. Ripeti il passaggio 3 per tutti i report finanziari su cui vuoi basare il servizio Web KPI report finanziario.  
5. Per visualizzare o modificare il report finanziario selezionato, nella Scheda dettaglio **Definizioni riga**, scegli l'azione **Modifica definizione riga**.
6. Per visualizzare i dati KPI del report finanziario impostati, scegli l'azione **Servizio Web KPI report finanziario**.
7. Per pubblicare il servizio Web KPI report finanziario, scegli l'azione **Pubblica servizio Web**.

Ora puoi creare report finanziari in Power BI basati sul servizio o sui servizi Web che hai creato.

> [!NOTE]  
> È inoltre possibile pubblicare il servizio Web KPI puntando all'oggetto pagina **Impostazione servizio Web KPI report finanziario** dalla pagina **Servizi Web**. Per ulteriori informazioni, vedi [Pubblicare un servizio web](across-how-publish-web-service.md).

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Vedere anche

[Business Intelligence finanziario](bi.md)  
[Finanze](finance.md)  
[Impostazione di dati finanziari](finance-setup-finance.md)  
[Contabilità generale e piano dei conti](finance-general-ledger.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
