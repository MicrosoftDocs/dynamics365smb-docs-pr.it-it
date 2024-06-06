---
title: Fatturare le prenotazioni in Business Central
description: Questo argomento spiega come eseguire la fatturazione in blocco da Microsoft Bookings in Business Central.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'invoicing, bookings'
ms.search.form: '1638, 6702, 6704'
ms.date: 05/20/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Fatturazione in blocco per Microsoft Bookings in [!INCLUDE[prod_short](includes/prod_short.md)]

Se la società utilizza l'app Bookings in Microsoft 365, è possibile eseguire la fatturazione in blocco per gli appuntamenti. La pagina **Registrazioni non fatturate** di [!INCLUDE[prod_short](includes/prod_short.md)] fornisce una lista delle prenotazioni completate della società. Nella pagina è possibile selezionare rapidamente gli appuntamenti da fatturare e creare fatture in bozza per i servizi forniti.  

## Connessione a Bookings

Per collegare [!INCLUDE[prod_short](includes/prod_short.md)] a Bookings, è necessario specificare la società Bookings, cosa sincronizzazione con Bookings, la frequenza di sincronizzare e i modelli da utilizzare. Impostare queste informazioni nella pagina **Setup sincronizzazione registrazione** che è possibile aprire dalla pagina **Setup sincronizzazione con Exchange** che è possibile trovare tramite la [Ricerca](ui-search.md).  

Ad esempio, se si desidera sincronizzare i clienti tra Bookings e [!INCLUDE[prod_short](includes/prod_short.md)], è necessario specificare il modello di default da utilizzare per aggiungere i nuovi clienti in [!INCLUDE[prod_short](includes/prod_short.md)] sulla base dei clienti nella società Bookings.  

> [!NOTE]
> L'app Bookings è progettata per prenotare appuntamenti per singoli clienti anziché società. La sincronizzazione con [!INCLUDE[prod_short](includes/prod_short.md)] pertanto sincronizzerà solo i contatti del cliente con un tipo di *Persona*. È inoltre necessario un l'indirizzo e-mail per il contatto da sincronizzare.  

Analogamente, se si desidera sincronizzare gli articoli in assistenza tra Bookings e [!INCLUDE[prod_short](includes/prod_short.md)], è necessario specificare il modello di default da utilizzare per aggiungere nuovi articoli in assistenza in [!INCLUDE[prod_short](includes/prod_short.md)] sulla base dei servizi nella società Bookings.  

> [!NOTE]
> Solo gli articoli di tipo *Assistenza* verranno sincronizzati tra Bookings e [!INCLUDE[prod_short](includes/prod_short.md)]. Il modello impostato nella pagina **Modelli di configurazione** di modo che possa essere utilizzato per la sincronizzazione degli articoli deve definire il tipo come *Assistenza*.

## Fattura appuntamenti

Quando è tempo di inviare le fatture per le prenotazioni completate, aprire la pagina **Registrazioni non fatturate**. In base alla frequenza della sincronizzazione delle informazioni, l'elenco è lungo o breve. È possibile creare fatture per tutte le prenotazioni della lista o per una prenotazione alla volta. È possibile selezionare uno o più movimenti dell'elenco e fatturare solo quelli.  

Il supporto per la fatturazione degli appuntamenti da Bookings è più semplice del flusso di lavoro completo per l'utilizzo di offerte di vendita, ordini di vendita e fatture di vendita. Per ulteriori informazioni, vedere [Fatturare le vendite](sales-how-invoice-sales.md). È possibile scegliere di vendere i servizi con [!INCLUDE[prod_short](includes/prod_short.md)] o decidere di utilizzare Bookings, in base alle esigenze aziendali.  

> [!NOTE]
> A maggio 2022 abbiamo scoperto un problema nell'integrazione con Bookings. Attualmente, la sincronizzazione da Bookings a [!INCLUDE [prod_short](includes/prod_short.md)] richiede di associare manualmente le fatture ai clienti in [!INCLUDE [prod_short](includes/prod_short.md)].

## Vedi anche

[Finanze](finance.md)  
[Fatturare le vendite](sales-how-invoice-sales.md)  
[Setup Vendite](sales-setup-sales.md)  
[Microsoft Bookings](https://products.office.com/business/scheduling-and-booking-app)  


[!INCLUDE[footer-include](includes/footer-banner.md)]