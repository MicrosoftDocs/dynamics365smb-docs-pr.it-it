---
title: Chiudere i movimenti contabili articoli derivanti dall'utilizzo del collegamento fisso
description: Scopri come creare un collegamento fisso tra una transazione in entrata e la transazione in uscita originale nelle registrazioni articoli.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: 40
ms.date: 07/30/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Chiudi registrazioni contabili articoli aperte risultanti dall'applicazione fissa nel giornale articoli

Utilizzare il campo **Collega da mov.** nella pagina **Registrazioni magazzino** per creare un collegamento fisso tra una transazione in entrata e la transazione in uscita originale. Ad esempio, per correggere la transazione in uscita o elaborare il suo reso.  

> [!IMPORTANT]  
> I collegamenti fissi creati in questo modo collegano solo il costo, non la quantità. Di conseguenza, il movimento contabile articoli positivo registrato non chiuderà il movimento in uscita collegato e rimarrà aperto. Ciò si applica anche quando si registra un collegamento fisso per un movimento positivo a un movimento negativo che non è stato chiuso da un movimento positivo normale, pertanto sia il movimento positivo che quello negativo rimarranno aperti.  
>
> Questo significa inoltre che non è possibile chiudere un periodo di magazzino se esiste tale movimento.  

È possibile modificare e riapplicare i movimenti di collegamento a certe condizioni utilizzando la pagina **Prospetto collegamento**.  

La seguente procedura illustra come chiudere tali movimenti con due registrazioni correttive nelle registrazioni magazzino.  

## Per chiudere i movimenti contabili articoli aperti risultanti da un collegamento fisso nelle registrazioni magazzino  

1. Utilizzare il campo **Collega-da mov.** per registrare una rettifica positiva con la quantità corrispondente. In questo modo si chiude il movimento negativo originale con un collegamento fisso.  

    Il campo **Collegare da - Movimento** specifica il numero del movimento contabile articoli in uscita il cui costo è inoltrato al movimento contabile articoli in ingresso quando si registra una transazione in ingresso di tipo **Rettifiche Positive** o **Acquisto** con le registrazioni magazzino.  
2. Utilizzare il campo **Collega-da mov.** per registrare una rettifica negativa. In questo modo si chiude il movimento positivo correttivo originale con un collegamento fisso.  

    Il campo **Collegare a - Movimento** specifica se la quantità nella riga di registrazione magazzino deve essere collegata a un documento già registrato. In questo caso, immettere il numero del movimento contabile articolo a cui la riga di registrazione magazzino deve essere collegata.

## Vedere anche

[Rimuovere e riapplicare le voci del registro degli articoli](finance-how-to-remove-and-reapply-item-entries.md)    
[Elaborare resi e annullamenti di vendite](sales-how-process-sales-returns-cancellations.md)    
[Impostazione della valutazione e dei costi dell'inventario](finance-set-up-inventory-valuation-and-costing.md)    
[Gestione dei costi di magazzino](finance-manage-inventory-costs.md)    
[Dettagli di progettazione: Metodi di costing](design-details-costing-methods.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]