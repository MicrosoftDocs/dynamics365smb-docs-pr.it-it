---
title: Utilizzare i riferimenti dell'elemento
description: 'Imposta i riferimenti tra le descrizioni, le unità di misura e le varianti che tu e il tuo fornitore o cliente utilizzate per un articolo.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'item reference, cross reference, inventory'
ms.search.forms: '5737, 5735, 5736'
ms.date: 10/27/2021
ms.author: bholtorf
---
# <a name="use-item-references"></a>Utilizzare i riferimenti dell'elemento

Se acquisti o vendi articoli per i quali tu e il tuo fornitore o cliente utilizzate termini diversi, puoi impostare un riferimento tra i termini per gli articoli e i termini utilizzati dal cliente o dal venditore di quell'articolo. In questo modo, la descrizione dell'articolo, l'unità di misura o il codice variante del fornitore o del cliente vengono automaticamente inseriti nei documenti pertinenti quando si compila il **Nr. di riferimento articolo** .  

> [!NOTE]
> [!INCLUDE [2021_releasewave2](includes/2021_releasewave2.md)]
>
> Non tutte le aziende utilizzano i riferimenti degli articoli. Per minimizzare il disordine nelle pagine abbiamo nascosto i campi e le azioni relative per impostazione predefinita. Se decidi di usarli, seleziona il campo **Utilizzare i riferimenti dell'elemento** nella pagina **Setup magazzino**. Dopo aver attivato i riferimenti agli articoli, i campi e le azioni sono disponibili nelle pagine Scheda articolo, Scheda venditore e Scheda cliente e dai documenti di vendita e acquisto.
>
> Nelle versioni precedenti al secondo ciclo di rilascio del 2021, l'amministratore può attivare la funzionalità *scrittura di riferimenti articolo più lunghi* nella pagina [Gestione delle funzionalità](https://businesscentral.dynamics.com/?page=2610) (il collegamento richiede un tenant [!INCLUDE [prod_short](includes/prod_short.md)]). Il modo in cui si usano i riferimenti non cambia, ma i nomi di cose come pagine e pulsanti cambia. Ad esempio, la pagina **Cross reference per l'articolo** diventerà la pagina**Movimenti riferimento per l'articolo**.

## <a name="to-start-using-item-references"></a>Per iniziare a usare i riferimenti agli elementi

[!INCLUDE [2021_releasewave2](includes/2021_releasewave2.md)]

1. Scegli l'icona :::image type="icon" source="media/ui-search/search_small.png" border="false"::: immetti **Setup magazzino** e scegli il collegamento correlato.
2. Seleziona il campo **Usa riferimenti articolo**.

## <a name="to-set-up-an-item-reference"></a>Per impostare un riferimento articolo

1. Scegli l'icona :::image type="icon" source="media/ui-search/search_small.png" border="false"::: immetti **Articoli** e scegli il collegamento correlato.
2. Apri la scheda di un articolo per cui vuoi creare un riferimento.
3. Scegli l'azione **Riferimenti elemento** .

     Se non riesci a trovare l'azione **Riferimenti dell'elemento**, scegli di visualizzare altre opzioni, e poi trovala sotto **Elemento** > **correlato**.
  
4. Su una nuova riga della pagina **Voci di riferimento dell’elemento**, compila i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

La seguente procedura descrive come specificare il riferimento articolo in un ordine di acquisto. La stessa procedura si applica ai documenti di vendita e ad altri documenti di acquisto.  

## <a name="to-enter-a-vendors-item-description-on-a-document"></a>Per immettere la descrizione articolo di un fornitore in un documento

1. Scegli l'icona :::image type="icon" source="media/ui-search/search_small.png" border="false"::: immetti **Ordini di acquisto** e scegli il collegamento correlato.
2. Create un ordine di acquisto per il fornitore per il quale avete impostato un riferimento di articolo nella procedura precedente.
3. Crea una linea di acquisto per l'articolo per il quale hai impostato un riferimento di articolo nella procedura precedente.
4. Nel **numero di riferimento della voce** seleziona il riferimento articolo rilevante e poi scegli il pulsante **OK**.

Il campo **Descrizione** sulla riga viene sovrascritto con la descrizione dell'articolo del venditore, come impostato nella voce di riferimento dell'articolo. Se il riferimento articolo include un codice variante o un'unità di misura, anche questi valori vengono copiati nel documento.  

## <a name="see-also"></a>Vedere anche

[Registrare nuovi articoli](inventory-how-register-new-items.md)  
[Magazzino](inventory-manage-inventory.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
