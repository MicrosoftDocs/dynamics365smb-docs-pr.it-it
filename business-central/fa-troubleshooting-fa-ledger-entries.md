---
title: Estensione Risoluzione dei problemi relativi a movimenti contabili dei cespiti
description: È più facile lavorare con numeri interi. Utilizza questa estensione per arrotondare gli importi dei cespiti nella contabilità dei cespiti.
documentationcenter: ''
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'machinery, buildings'
ms.date: 10/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="the-troubleshooting-fa-ledger-entries-extension"></a>Estensione Risoluzione dei problemi relativi a movimenti contabili dei cespiti
Utilizza l'estensione Risoluzione dei problemi relativi a movimenti contabili dei cespiti per arrotondare a numeri interi gli importi di ammortamento e acquisizione nei movimenti contabili cespiti. Ad esempio, per arrotondare un importo da 30.000,44 a 30.000. Le cause tipiche dei problemi di arrotondamento sono la migrazione dei dati, che inizia improvvisamente a registrare importi nella contabilità generale oppure le personalizzazioni apportate a [!INCLUDE[prod_short](includes/prod_short.md)].

L'estensione Risoluzione dei problemi relativi a movimenti contabili dei cespiti è preinstallata e pronta per l'uso. Se rimuovi l'estensione, ma desideri installarla di nuovo, puoi trovarla su AppSource.

## <a name="troubleshooting-fixed-asset-ledger-entries"></a>Risoluzione dei problemi relativi a movimenti contabili dei cespiti
Quando apri la pagina **Scheda cespite** per la prima volta, il movimento coda processi **Scansione movimenti contabili cespiti** è programmato per monitorare gli importi ogni domenica. Se trova importi che potresti voler arrotondare, verrà visualizzata una notifica alla successiva apertura della pagina Scheda cespite. La notifica include un'opzione **Vedi altro** che apre la pagina **Movimenti contabili cespiti con problemi di arrotondamento** che elenca i movimenti con gli importi che potresti voler arrotondare. Per arrotondare gli importi, scegli i movimenti quindi scegli l'azione  **Accetta selezione**. Puoi usare l'azione **Trova movimenti con problemi** per aggiornare l'elenco con i nuovi problemi che si sono verificati dopo che l'inserimento nella coda processi è stato eseguito la domenica precedente.

## <a name="see-also"></a>Vedere anche
[Cespiti](fa-manage.md)  
[Gestione dei cespiti](fa-manage.md)  
[Gestione di cespiti](fa-how-maintain.md)  
[Personalizzazione di Business Central Online utilizzando le estensioni](ui-extensions.md)  
[Finanze](finance.md)  
[Prepararsi a fare affari](ui-get-ready-business.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]



