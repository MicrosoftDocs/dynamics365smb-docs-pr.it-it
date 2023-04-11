---
title: Gestire le varianti di prodotto
description: 'Scopri come registrare prodotti quasi identici ma che variano per colore, dimensioni o materiale come varianti di articolo.'
author: edupont04
ms.topic: conceptual
ms.workload: na
ms.search.keywords: 'item, variant, finished good, component, raw material, assembly item, item substitution'
ms.search.form: '30, 5717, 31, 32, 346, 9091, 5718, 5716, 5720, 1384, 1383, 35, 5404, 1378, 5719'
ms.date: 09/26/2022
ms.author: edupont
---
# Gestire le varianti di prodotto

Le varianti degli articoli sono un ottimo modo per tenere sotto controllo il tuo elenco di prodotti. Ad esempio, hai un gran numero di articoli che sono quasi identici e variano solo nel colore. Puoi definire ogni variante come un articolo separato. Ma scegli di impostare un articolo e specificare i vari colori come varianti dell'articolo.  

> [!TIP]
> Per un'introduzione pratica all'utilizzo delle varianti nella produzione, vedi [Procedura dettagliata: varianti](contoso-coffee/manufacturing/variants.md) per i dati demo di Contoso Coffee.  

## Aggiungere varianti a un articolo

Se la tua organizzazione ha deciso di utilizzare le varianti, è abbastanza facile definire le varianti per un articolo.  

### Per aggiungere varianti

1. Apri [la pagina **Elenco articoli**](https://businesscentral.dynamics.com/?page=31), apri l'articolo rilevante.  
2. Nella scheda **Articolo** scegli l'azione **Articolo** quindi l'azione **Varianti**.  
3. Nella pagina **Varianti articolo** sono elencate le varianti.  

Quindi, quando crei un documento di vendita e aggiungi l'articolo, puoi specificare la variante dell'articolo nel campo **Codice variante**. Lo stesso vale per i documenti di acquisto.  

## Disponibilità articolo per variante

[!INCLUDE [inventory_variant-availability](includes/inventory_variant-availability.md)]

## Richiede l'uso di varianti

A partire dal secondo ciclo di rilascio del 2022, gli amministratori possono richiedere agli utenti di specificare la variante nei documenti e nei giornali di registrazione per gli articoli con varianti. Per attivare la funzionalità, vai alla pagina **Setup inventario** quindi seleziona il campo **Variante obbligatoria se esistente**. È possibile sostituire questa impostazione globale per articoli specifici.  

Nelle schede articolo, il campo **Variante obbligatoria se esistente** ha le seguenti opzioni:

|Valore campo |Descrizione|
|---------|----|
|Predefinito| L'impostazione di **Setup inventario** si applica a questo articolo.|
|Nr.| Gli utenti non sono tenuti a specificare una variante per questo articolo.|
|Sì| Se l'articolo ha una o più varianti, gli utenti devono specificare la variante pertinente. In caso contrario, verrà impedito loro di registrare la transazione.|

> [!NOTE]
> Queste impostazioni non influiscono sugli articoli che non hanno varianti.

Se la funzionalità è attivata, gli utenti non possono registrare un movimento se la variante non è specificata.

## Categorie, attributi e varianti

[!INCLUDE[inventory_variant](includes/inventory_variant.md)]

## Vedere anche

[Registrare nuovi articoli](inventory-how-register-new-items.md)  
[Impostare le informazioni generali di magazzino](inventory-how-setup-general.md)  
[Procedura dettagliata: varianti](contoso-coffee/manufacturing/variants.md)  
