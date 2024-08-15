---
title: Come lavorare con i centri di responsabilità
description: I centri di responsabilità in quanto centri amministrativi aiutano le aziende a impostare viste specifiche dell'utente dei documenti di vendita e di acquisto relativi esclusivamente a ciascun centro.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.forms: '5714, 5715'
ms.date: 05/16/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Lavorare con i centri di responsabilità

I centri di responsabilità consentono di gestire i centri di amministrazione. Possono essere centri di costo, centri di profitto, centri di investimento o altri centri amministrativi definiti dalla società. Esempi di centri di responsabilità possono essere un ufficio vendite, un reparto acquisti per più ubicazioni e un ufficio di pianificazione di sede. Ad esempio, le società possono impostare viste specifiche per determinati utenti di documenti di vendita e acquisto relativi a un particolare centro di responsabilità.  

L'utilizzo di più ubicazioni insieme ai centri di responsabilità offre la possibilità di gestire le operazioni aziendali in modo flessibile e ottimale.

Grazie alla presenza di più sedi, le aziende possono gestire il proprio inventario in più sedi utilizzando un unico database. I due concetti di ubicazione e unità di stockkeeping costituiscono il punto centrale di questa area. Per ubicazione si intende un luogo in cui vengono gestiti il posizionamento fisico e le quantità degli articoli. Il concetto è sufficientemente ampio da includere sedi quali stabilimenti o strutture di produzione e centri di distribuzione, magazzini, showroom e veicoli di assistenza. Per unità di stockkeeping si intende un articolo in un'ubicazione specifica e/o come variante. Utilizzando le unità di stockkeeping, le società con più ubicazioni possono aggiungere informazioni sul rifornimento, indirizzi e alcune informazioni relative alla registrazione finanziaria a livello di ubicazione. Di conseguenza, possono rifornire varianti dello stesso articolo per ogni sede e ordinare articoli in base alle informazioni di rifornimento specifiche della sede.  

## Per impostare i centri di responsabilità

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Centri di responsabilità**, quindi scegli il collegamento correlato.  
2. Scegli l'azione **Nuovo**.  
3. Compila i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    In caso di utilizzo di centri di responsabilità per gestire una società, può risultare utile impostare un centro di responsabilità predefinito.
4. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Informazioni società**, quindi scegli il collegamento correlato.
5. Nella scheda dettaglio **Spedizione**, nel campo **Centro di responsabilità**, inserisci un codice centro di responsabilità.

Questo codice è utilizzato in tutti i documenti di acquisto, vendita o assistenza, se per l'utente, il cliente o il fornitore non è stato impostato un centro di responsabilità di default. Nei documenti di acquisto, vendita o assistenza è possibile immettere un altro centro di responsabilità diverso da quello di default.

> [!NOTE]  
> L'immissione di un codice di centro di responsabilità in un documento influisce sull'indirizzo, le dimensioni e i prezzi del documento.  

## Per assegnare i centri di responsabilità agli utenti

È possibile impostare gli utenti in modo che [!INCLUDE [prod_short](includes/prod_short.md)] recuperi soltanto i documenti relativi all'area di lavoro specifica. Gli utenti sono associati a un centro di responsabilità e lavorano solo con documenti relativi ad aree applicative specifiche di quel particolare centro.  

Per poter procedere a queste impostazioni è necessario assegnare i centri di responsabilità agli utenti in tre aree funzionali: Acquisti, Vendite e Gestione assistenza.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Setup utente**, quindi scegli il collegamento correlato.  
2. Selezionare l'utente a cui si intende assegnare un centro di responsabilità nella pagina **Setup utente**. Se l'utente non è nella lista è necessario immettere un ID utente nel campo **User ID**.  
3. Nel campo **Filtro Centro Resp. Vendite** immettere il centro di responsabilità per cui l'utente dovrà svolgere task correlati alle vendite.  
4. Nel campo  **Filtro Centro Resp. Acquisti** immettere il centro di responsabilità per cui l'utente dovrà svolgere dei compiti correlati agli acquisti.  
5. Nel campo **Filtro Centro Resp. Assistenza** immettere il centro di responsabilità per cui l'utente dovrà svolgere task correlati alla gestione dell'assistenza.  

> [!NOTE]  
> Gli utenti possono visualizzare solo i documenti registrati relativi al proprio centro di responsabilità. Tuttavia, possono visualizzare tutti i movimenti contabili e passare ad altri documenti registrati dai movimenti contabili.

## Vedere anche

[Impostazione dell'inventario](inventory-setup-inventory.md)    
[Impostazione Warehouse Management](warehouse-setup-warehouse.md)    
[Magazzino](inventory-manage-inventory.md)    
[Panoramica della gestione warehouse](design-details-warehouse-management.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    
[Definire un criterio di registrazione delle fatture per gli utenti](admin-setup-invoice-posting-policy.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
