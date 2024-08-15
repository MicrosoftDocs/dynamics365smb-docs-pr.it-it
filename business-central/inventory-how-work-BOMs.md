---
title: Usare le distinte base
description: Si crea una distinta base di assemblaggio o di produzione per specificare i componenti o le risorse richieste per un l'articolo che la distinta rappresenta.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'bills of material, assembly BOM, production BOM,'
ms.search.form: null
ms.date: 06/06/2024
ms.service: dynamics-365-business-central
---
# Usare le distinte base

Utilizzare le distinte base (DB) per strutturare gli articoli padre che devono essere assemblati con altri articoli o prodotti dalle risorse o dai centri di lavoro a partire dai componenti.

## DB di assemblaggio o DB di produzione

[!INCLUDE[prod_short](includes/prod_short.md)] supporta due diversi tipi di distinte base:

| Tipo di distinta base | Categoria generale | Esempio |
| -------- | ---------------- | ------- |
| [DB assemblaggio](assembly-how-work-assembly-boms.md) | Magazzino/assemblaggio | Articoli che consistono in altri articoli, assemblati con risorse di base o senza risorse. |
| [DB di produzione](production-how-to-create-production-boms.md) | Produzione | Articoli costituiti da diversi componenti e sottoassiemi, prodotti in un centro di lavoro o di produzione. |

Gli ordini di assemblaggio vengono utilizzati per realizzare articoli finali a partire da componenti in un processo semplice che può essere eseguito da una o più risorse di base, che non sono centri di lavoro o macchine, oppure sono prive di risorse. Ad esempio, un processo di assemblaggio potrebbe consistere nel prelevare due bottiglie di vino e un pacchetto di caffè, quindi di imballarli come articolo da regalo.  

Una DB di assemblaggio contiene i dati master che definiscono gli articoli componenti che costituiscono un articolo finale assemblato e le risorse che vengono utilizzate per assemblare l'articolo di assemblaggio. Immettendo un articolo di assemblaggio e una quantità nella testata di un nuovo ordine di assemblaggio, le righe ordine di assemblaggio vengono automaticamente immesse in base alla distinta base di assemblaggio con una riga ordine di assemblaggio per ogni componente o risorsa. Per ulteriori informazioni, vedi [Gestione assemblaggio](assembly-assemble-items.md).

Utilizzare gli ordini di produzione per la creazione dio articoli finali dai componenti in una processo complesso che richiede un ciclo di produzione e centri di lavoro o aree di produzione che rappresentano le capacità di produzione. Ad esempio, un processo di produzione potrebbe consistere nel tagliare piastre di acciaio in un'unica operazione, saldarle nell'operazione successiva e verniciare l'articolo finale nell'ultima operazione. Per ulteriori informazioni, vedi [Produzione](production-manage-manufacturing.md).

La distinta base di produzione corrisponde ai dati master che definiscono un articolo di produzione e ai componenti che lo costituiscono. Per gli articoli di assemblaggio, la distinta base di produzione deve essere certificata e assegnata all'articolo di produzione prima che possa essere utilizzata in un ordine di produzione. Immettendo l'articolo di produzione in una riga ordine di produzione, manualmente o aggiornando l'ordine, i contenuti della DB di produzione diventano i componenti dell'ordine di produzione. Per ulteriori informazioni, vedi [Creare distinte base di produzione](production-how-to-create-production-boms.md).

Il concetto di risorse in produzione è molto più avanzato rispetto alla gestione assemblaggio. Le aree di produzione e i centri lavoro fungono da risorse. Le operazioni assegnate alle risorse nei cicli di produzione rappresentano le fasi di produzione. Scopri di più nell'articolo [Creare cicli](production-how-to-create-routings.md).

Gli ordini di assemblaggio e gli ordini di produzione potrebbero essere collegati direttamente agli ordini di vendita. Tuttavia, è possibile utilizzare soltanto gli ordini di assemblaggio per personalizzare direttamente l'articolo finale per una richiesta cliente con l'ordine di vendita.

## Vedere anche

[Lavorare con le distinte base di assemblaggio](assembly-how-work-assembly-boms.md)    
[Creare BOM di produzione](production-how-to-create-production-boms.md)    
[Registra nuovi articoli](inventory-how-register-new-items.md)    
[Gestisci le varianti del prodotto](inventory-item-variants.md)    
[Magazzino](inventory-manage-inventory.md)    
[Produzione](production-manage-manufacturing.md)    
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    

[!INCLUDE[footer-include](includes/footer-banner.md)]
