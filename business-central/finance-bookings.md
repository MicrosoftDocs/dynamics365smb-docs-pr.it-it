---
title: Fatturazione delle prenotazioni in Business Central | Documenti Microsoft
description: "Informazioni su come è possibile eseguire la fatturazione da Microsoft Bookings in Business Central."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: invoicing, bookings
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 8637df3f579af920168f059812b34ae5d0023afc
ms.contentlocale: it-it
ms.lasthandoff: 09/28/2018

---
# <a name="bulk-invoicing-for-microsoft-bookings-in-included365finincludesd365finmdmd"></a>Fatturazione in blocco per Microsoft Bookings in [!INCLUDE[d365fin](includes/d365fin_md.md)]
Se la società utilizza l'app Bookings in Office 365, è possibile eseguire la fatturazione in blocco per gli appuntamenti. La finestra **Bookings non fatturato** di [!INCLUDE[d365fin](includes/d365fin_md.md)] fornisce un elenco delle prenotazioni completate della società. Nella pagina è possibile selezionare rapidamente gli appuntamenti da fatturare e creare fatture in bozza per i servizi forniti.  

## <a name="connect-to-bookings"></a>Connessione a Bookings
Per collegare [!INCLUDE[d365fin](includes/d365fin_md.md)] a Bookings, è necessario specificare la società Bookings, cosa sincronizzazione con Bookings, la frequenza di sincronizzare e i modelli da utilizzare. Impostare queste informazioni nella finestra **Setup sincronizzazione registrazione** che è possibile aprire dalla finestra **Setup sincronizzazione con Exchange** che è possibile trovare tramite la [Ricerca](ui-search.md).  

Ad esempio, se si desidera sincronizzare i clienti tra Bookings e [!INCLUDE[d365fin](includes/d365fin_md.md)], è necessario specificare il modello di default da utilizzare per aggiungere i nuovi clienti in [!INCLUDE[d365fin](includes/d365fin_md.md)] sulla base dei clienti nella società Bookings.  

## <a name="invoice-appointments"></a>Fattura appuntamenti
Quando è tempo di inviare le fatture per le prenotazioni completate, aprire la finestra **Bookings non fatturato**. In base alla frequenza della sincronizzazione delle informazioni, l'elenco è lungo o breve. È possibile creare fatture per tutte le prenotazioni della lista o per una prenotazione alla volta. È possibile selezionare uno o più movimenti dell'elenco e fatturare solo quelli.  

Il supporto per la fatturazione degli appuntamenti da Bookings è più semplice del flusso di lavoro completo per l'utilizzo di offerte di vendita, ordini di vendita e fatture di vendita. Per ulteriori informazioni, vedere [Fatturare le vendite](sales-how-invoice-sales.md). È possibile scegliere di vendere i servizi con [!INCLUDE[d365fin](includes/d365fin_md.md)] o decidere di utilizzare Bookings, in base alle esigenze aziendali.  

## <a name="see-also"></a>Vedi anche
[Finanze](finance.md)  
[Fatturare le vendite](sales-how-invoice-sales.md)  
[Setup Vendite](sales-setup-sales.md)  
[Microsoft Bookings](https://products.office.com/en-us/business/scheduling-and-booking-app)  

