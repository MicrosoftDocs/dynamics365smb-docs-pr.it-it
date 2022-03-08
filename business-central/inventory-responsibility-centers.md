---
title: 'Procedura: Utilizzare i centri di responsabilità | Documenti Microsoft'
description: I centri di responsabilità forniscono la possibilità di gestire centri di amministrazione. Possono essere centri di costo, centri di profitto, centri di investimento o altri centri amministrativi definiti dalla società.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 11/03/2020
ms.author: edupont
ms.openlocfilehash: bc06c1e143fce8a667ba7675b472a1518a54ebbc
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5393026"
---
# <a name="work-with-responsibility-centers"></a>Utilizzare i centri di responsabilità

I centri di responsabilità consentono di gestire i centri di amministrazione. Possono essere centri di costo, centri di profitto, centri di investimento o altri centri amministrativi definiti dalla società. Esempi di centri di responsabilità possono essere un ufficio vendite, un reparto acquisti per più ubicazioni e un ufficio di pianificazione di sede. Utilizzando questa funzionalità, ad esempio, le società possono impostare viste specifiche per determinati utenti di documenti di vendita e acquisto relativi esclusivamente a un particolare centro di responsabilità.  

L'utilizzo di più ubicazioni insieme ai centri di responsabilità offre la possibilità di gestire le operazioni aziendali nel modo più flessibile e ottimale.

Il supporto di più ubicazioni consente alle società di gestire il magazzino in più luoghi utilizzando un singolo database. I due concetti di ubicazione e unità di stockkeeping costituiscono il punto centrale di questa area. Per ubicazione si intende un luogo in cui vengono gestiti il posizionamento fisico e le quantità degli articoli. Il concetto è sufficientemente vasto per includere ubicazioni quali impianti o unità di produzione, nonché centri di distribuzione, warehouse, showroom e automezzi di servizio. Per unità di stockkeeping si intende un articolo in un'ubicazione specifica e/o come variante. Utilizzando le unità di stockkeeping, le società con più ubicazioni possono aggiungere informazioni sul rifornimento, indirizzi e alcune informazioni relative alla registrazione finanziaria a livello di ubicazione. Di conseguenza, le società possono rifornire varianti dello stesso articolo per ciascuna ubicazione, nonché ordinare articoli sulla base di informazioni sul rifornimento specifiche dell'ubicazione.  

## <a name="to-set-up-a-responsibility-center"></a>Per impostare i centri di responsabilità

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Centri di responsabilità** e quindi scegliere il collegamento correlato.  
2. Scegliere l'azione **Nuovo**.  
3. Compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    In caso di utilizzo di centri di responsabilità per gestire una società, può risultare utile impostare un centro di responsabilità di default per tale società.
4. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Informazioni società** e quindi scegliere il collegamento correlato.
5. Nel campo **Centro di responsabilità** immettere un codice del centro di responsabilità.

Questo codice verrà utilizzato in tutti i documenti di acquisto, vendita o assistenza, se per l'utente, il cliente o il fornitore non è stato impostato un centro di responsabilità di default. In tutti i documenti di acquisto, vendita o assistenza è possibile immettere un altro centro di responsabilità diverso da quello di default.

> [!NOTE]  
> L'immissione di un codice di centro di responsabilità in un documento influisce sull'indirizzo, le dimensioni e i prezzi del documento.  

## <a name="to-assign-responsibility-centers-to-users"></a>Per assegnare i centri di responsabilità agli utenti

È possibile impostare gli utenti in modo che durante il lavoro quotidiano vengano automaticamente recuperati soltanto i documenti relativi alla loro area di lavoro specifica. Gli utenti sono normalmente associati con un centro di responsabilità e hanno accesso soltanto a documenti collegati a specifiche aree di applicazione presso quel centro in particolare.  

Per poter procedere a queste impostazioni è necessario assegnare i centri di responsabilità agli utenti in tre aree funzionali: Acquisti, Vendite e Gestione assistenza.  

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup utente** e quindi scegliere il collegamento correlato.  
2. Selezionare l'utente a cui si intende assegnare un centro di responsabilità nella pagina **Setup utente**. Se l'utente non è nella lista è necessario immettere un ID utente nel campo **User ID**.  
3. Nel campo **Filtro Centro Resp. Vendite** immettere il centro di responsabilità per cui l'utente dovrà svolgere task correlati alle vendite.  
4. Nel campo  **Filtro Centro Resp. Acquisti** immettere il centro di responsabilità per cui l'utente dovrà svolgere dei compiti correlati agli acquisti.  
5. Nel campo **Filtro Centro Resp. Assistenza** immettere il centro di responsabilità per cui l'utente dovrà svolgere task correlati alla gestione dell'assistenza.  

> [!NOTE]  
> Gli utenti possono visualizzare solo i documenti registrati relativi al proprio centro di responsabilità. Tuttavia, possono visualizzare tutti i movimenti contabili e passare ad altri documenti registrati dai movimenti contabili.

## <a name="see-also"></a>Vedere anche

[Impostazione del magazzino](inventory-setup-inventory.md)  
[Impostazione gestione warehouse](warehouse-setup-warehouse.md)
[Magazzino](inventory-manage-inventory.md)[Gestione warehouse](warehouse-manage-warehouse.md)  
[Gestione warehouse](warehouse-manage-warehouse.md)  
[Dettagli di progettazione: Gestione warehouse](design-details-warehouse-management.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]