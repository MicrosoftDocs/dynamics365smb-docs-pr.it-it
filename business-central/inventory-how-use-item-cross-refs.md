---
title: Utilizzare i riferimenti degli articoli
description: 'Imposta i riferimenti tra le descrizioni, le unità di misura e le varianti che tu e il tuo fornitore o cliente utilizzate per un articolo.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'item reference, cross reference, inventory'
ms.search.forms: '5737, 5735, 5736'
ms.date: 05/16/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Utilizzare i riferimenti degli articoli

Se acquisti o vendi articoli per i quali tu e il tuo fornitore o cliente utilizzate termini diversi, puoi impostare un riferimento tra i termini per gli articoli e i termini utilizzati dal cliente o dal venditore di quell'articolo. In questo modo, la descrizione dell'articolo, l'unità di misura o il codice variante del fornitore o del cliente vengono automaticamente inseriti nei documenti pertinenti quando si compila il **Nr. di riferimento articolo** .  

## Per impostare un riferimento articolo

1. Scegli l'icona :::image type="icon" source="media/ui-search/search_small.png" border="false"::: immetti **Articoli** e scegli il collegamento correlato.
2. Apri la scheda di un articolo per cui vuoi creare un riferimento.
3. Scegli l'azione **Riferimenti elemento** .

     Se non riesci a trovare l'azione  **Riferimenti elemento**, scegli di visualizzare altre opzioni, quindi cercala in  **Correlati** > **Elemento**.
  
4. Su una nuova riga della pagina **Voci di riferimento dell’elemento**, compila i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

La seguente procedura descrive come specificare il riferimento articolo in un ordine di acquisto. La stessa procedura si applica ai documenti di vendita e ad altri documenti di acquisto.  

## Per immettere la descrizione articolo di un fornitore in un documento

1. Scegli l'icona :::image type="icon" source="media/ui-search/search_small.png" border="false"::: immetti **Ordini di acquisto** e scegli il collegamento correlato.
2. Create un ordine di acquisto per il fornitore per il quale avete impostato un riferimento di articolo nella procedura precedente.
3. Crea una linea di acquisto per l'articolo per il quale hai impostato un riferimento di articolo nella procedura precedente.
4. Nel riferimento dell'articolo **n.** seleziona il riferimento articolo rilevante e poi scegli il pulsante **OK**.

Il campo **Descrizione** sulla riga viene sovrascritto con la descrizione dell'articolo del venditore, come impostato nella voce di riferimento dell'articolo. Se il riferimento articolo include un codice variante o un'unità di misura, anche questi valori vengono copiati nel documento.  

## Eseguire la scansione di codici a barre con l'app per dispositivi mobili Business Central

[!INCLUDE [barcode-mobile-app](includes/barcode-mobile-app.md)]

La seguente tabella elenca le pagine che supportano la scansione di codici a barre di riferimenti articolo dall'app per dispositivi mobili [!INCLUDE [prod_short](includes/prod_short.md)].

|Pagina  |Valore dei campi che è possibile scansionare  |
|---------|---------|
|Riferimento articolo     | Nr. riferimento        |
|Righe reg. magazzino     | Nr. riferimento articolo        |
|Riga ordine magazzino fisico     |Nr. riferimento articolo         |
|Righe Acquisto     |   Nr. riferimento articolo      |
|Righe vendite     | Nr. riferimento articolo        |

## Vedere anche

[Registrare nuovi articoli](inventory-how-register-new-items.md)  
[Inventario](inventory-manage-inventory.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
