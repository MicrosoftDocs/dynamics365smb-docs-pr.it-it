---
title: Gestire le varianti di prodotto
description: 'Scopri come registrare prodotti quasi identici ma che variano per colore, dimensioni o materiale come varianti di articolo.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'item, variant, finished good, component, raw material, assembly item, item substitution'
ms.search.form: '30, 5717, 31, 32, 346, 9091, 5718, 5716, 5720, 1384, 1383, 35, 5404, 1378, 5719'
ms.date: 06/13/2024
ms.service: dynamics-365-business-central
---

# Gestire le varianti di prodotto

Le varianti degli articoli sono un ottimo modo per tenere sotto controllo il tuo elenco di prodotti. Ad esempio, hai un gran numero di articoli che sono quasi identici e variano solo nel colore. Puoi definire ogni variante come un articolo separato. Ma puoi anche scegliere di impostare un articolo e specificare i vari colori come varianti dell'articolo.  

> [!TIP]
> Per un'introduzione pratica all'utilizzo delle varianti nella produzione, vedi [Procedura dettagliata: varianti](contoso-coffee/manufacturing/variants.md) per i dati demo di Contoso Coffee.  

## Aggiungere varianti a un articolo

È abbastanza semplice definire varianti per un articolo.  

### Per aggiungere varianti

1. Apri [la pagina **Elenco articoli**](https://businesscentral.dynamics.com/?page=31), apri l'articolo rilevante.  
2. Nell' **Elemento** scheda, seleziona l'azione **Correlato**, quindi seleziona **Elemento** e infine seleziona l'azione **Varianti** .  
3. Nella pagina  **Varianti articolo**, elenca le varianti.  

Quindi, quando crei un documento di vendita e aggiungi l'articolo, puoi specificare la variante dell'articolo nel campo Variante **Codice** . Lo stesso vale per l'acquisto di documenti.  

## Disponibilità articolo per variante

[!INCLUDE [inventory_variant-availability](includes/inventory_variant-availability.md)]

## Richiede l'uso di varianti

A partire dal secondo ciclo di rilascio del 2022, gli amministratori possono richiedere agli utenti di specificare la variante nei documenti e nei giornali di registrazione per gli articoli con varianti. Per attivare la funzionalità, nella pagina **Setup inventario** seleziona il campo **Variante obbligatoria se esistente**. È possibile sostituire questa impostazione globale per articoli specifici.  

Nelle schede articolo, il campo **Variante obbligatoria se esistente** ha le seguenti opzioni:

|Valore campo |Descrizione|
|---------|----|
|Valore predefinito (No)| L'impostazione di **Setup inventario** si applica a questo articolo.|
|Nr.| Gli utenti non sono tenuti a specificare una variante per questo articolo.|
|Sì| Se l'articolo ha una o più varianti, gli utenti devono specificare la variante pertinente. In caso contrario, viene impedito loro di registrare la transazione.|

> [!NOTE]
> Queste impostazioni non influiscono sugli articoli che non hanno varianti.

Se la funzionalità è attivata, non puoi registrare un movimento se la variante non è specificata.

## Categorie, attributi e varianti

[!INCLUDE[inventory_variant](includes/inventory_variant.md)]

## Vedere anche

[Registra nuovi articoli](inventory-how-register-new-items.md)    
[Imposta le informazioni generali dell'inventario](inventory-how-setup-general.md)    
[Procedura dettagliata: varianti](contoso-coffee/manufacturing/variants.md)    
