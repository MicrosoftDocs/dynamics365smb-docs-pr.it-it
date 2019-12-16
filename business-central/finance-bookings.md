---
title: Fatturazione delle prenotazioni in Business Central | Documenti Microsoft
description: Informazioni su come è possibile eseguire la fatturazione da Microsoft Bookings in Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: invoicing, bookings
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: 924876abbe532384d568c6c260b22397f98a40ad
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/03/2019
ms.locfileid: "2879898"
---
# <a name="bulk-invoicing-for-microsoft-bookings-in-included365finincludesd365fin_mdmd"></a>Fatturazione in blocco per Microsoft Bookings in [!INCLUDE[d365fin](includes/d365fin_md.md)]
Se la società utilizza l'app Bookings in Office 365, è possibile eseguire la fatturazione in blocco per gli appuntamenti. La pagina **Bookings non fatturato** di [!INCLUDE[d365fin](includes/d365fin_md.md)] fornisce una lista delle prenotazioni completate della società. Nella pagina è possibile selezionare rapidamente gli appuntamenti da fatturare e creare fatture in bozza per i servizi forniti.  

## <a name="connect-to-bookings"></a>Connessione a Bookings
Per collegare [!INCLUDE[d365fin](includes/d365fin_md.md)] a Bookings, è necessario specificare la società Bookings, cosa sincronizzazione con Bookings, la frequenza di sincronizzare e i modelli da utilizzare. Impostare queste informazioni nella pagina **Setup sincronizzazione registrazione** che è possibile aprire dalla pagina **Setup sincronizzazione con Exchange** che è possibile trovare tramite la [Ricerca](ui-search.md).  

Ad esempio, se si desidera sincronizzare i clienti tra Bookings e [!INCLUDE[d365fin](includes/d365fin_md.md)], è necessario specificare il modello di default da utilizzare per aggiungere i nuovi clienti in [!INCLUDE[d365fin](includes/d365fin_md.md)] sulla base dei clienti nella società Bookings.  

> [!NOTE]
> L'app Bookings è progettata per prenotare appuntamenti per singoli clienti anziché società. La sincronizzazione con [!INCLUDE[d365fin](includes/d365fin_md.md)], pertanto, sincronizzerà solo i contatti del cliente con un tipo di "Persona". È inoltre necessario un l'indirizzo e-mail per il contatto da sincronizzare.  

Analogamente, se si desidera sincronizzare gli articoli in assistenza tra Bookings e [!INCLUDE[d365fin](includes/d365fin_md.md)], è necessario specificare il modello di default da utilizzare per aggiungere nuovi articoli in assistenza in [!INCLUDE[d365fin](includes/d365fin_md.md)] sulla base dei servizi nella società Bookings.  

> [!NOTE]
> Solo gli articoli di tipo *Assistenza* verranno sincronizzati tra Bookings e [!INCLUDE[d365fin](includes/d365fin_md.md)]. Il modello impostato nella pagina **Modelli di configurazione** di modo che possa essere utilizzato per la sincronizzazione degli articoli deve definire il tipo come *Assistenza*.

## <a name="invoice-appointments"></a>Fattura appuntamenti
Quando è tempo di inviare le fatture per le prenotazioni completate, aprire la pagina **Bookings non fatturato**. In base alla frequenza della sincronizzazione delle informazioni, l'elenco è lungo o breve. È possibile creare fatture per tutte le prenotazioni della lista o per una prenotazione alla volta. È possibile selezionare uno o più movimenti dell'elenco e fatturare solo quelli.  

Il supporto per la fatturazione degli appuntamenti da Bookings è più semplice del flusso di lavoro completo per l'utilizzo di offerte di vendita, ordini di vendita e fatture di vendita. Per ulteriori informazioni, vedere [Fatturare le vendite](sales-how-invoice-sales.md). È possibile scegliere di vendere i servizi con [!INCLUDE[d365fin](includes/d365fin_md.md)] o decidere di utilizzare Bookings, in base alle esigenze aziendali.  

## <a name="see-also"></a>Vedi anche
[Finanze](finance.md)  
[Fatturare le vendite](sales-how-invoice-sales.md)  
[Setup Vendite](sales-setup-sales.md)  
[Microsoft Bookings](https://products.office.com/business/scheduling-and-booking-app)  
