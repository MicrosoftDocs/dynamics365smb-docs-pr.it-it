---
title: Informazioni sui tipi di articolo
description: 'Puoi modificare la valutazione di magazzino di un articolo mediante i metodi di costing Media o FIFO, quando i costi degli articoli cambiano per i motivi diversi dalle transazioni.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: null
ms.search.form: '9297, 5845, 30,'
ms.date: 05/24/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="about-item-types"></a>Informazioni sui tipi di articolo

Nel campo **Tipo** nella pagina **Scheda articolo** è possibile selezionare l'articolo utilizzato nella propria azienda che influisce sul grado di gestione dell'articolo in magazzino. La tabella seguente elenca e descrive i tre tipi di articoli disponibili.

|Opzione|Scopo tipico|
|------|-----------|
|Magazzino|Oggetti fisici, come biciclette, telefoni e scrivanie, per i quali vuoi essere in grado di utilizzare tutti i processi di magazzino. Gli articoli di magazzino possono includere anche articoli non fisici, come licenze software e abbonamenti, se gli articoli hanno numeri di identificazione, come i numeri di serie. Puoi monitorare completamente i valori degli articoli e la disponibilità nel magazzino.|
|Non magazzino|In genere, gli articoli non di magazzino sono oggetti fisici, come bulloni o penne, che la tua azienda consuma ma di cui non desidera tenere traccia completamente nel magazzino. Ad esempio, perché sono articoli a basso costo e vengono utilizzati solo internamente.|
|Assistenza|Un'unità di misura del tempo della manodopera, ad esempio un'ora di consulenza, per un supporto aziendale limitato.|

> [!NOTE]
> I tipi **In assistenza** e **Non magazzino** non consentono il monitoraggio della quantità e del valore del magazzino. Sono supportati solo i tipi e le funzionalità delle transazioni dell'articolo selezionato. La seguente tabella include le funzionalità supportate dai tre tipi dell'articolo.

|Tipo di articolo|Vendite|Acquisti|Consumo per la commessa|Consumo di assistenza|Consumo assemblaggio|Consumo produzione|Output assemblaggio|Output produzione|Trasferimento ubicazione|Conteggio fisico|Rivalutazione del magazzino|Costing di magazzino|Tracciabilità articolo|Impegno|Gestione della warehouse|Piano|Pianificazione ordini|
|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|Magazzino|Sì|Sì|Sì|Sì|Sì|Sì|Sì|Sì|Sì|Sì|Sì|Sì|Sì|Sì|Sì|Sì|Sì|
|Non magazzino|Sì|Sì|Sì|Sì|Sì|Sì|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Sì|
|Assistenza|Sì|Sì|Sì|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Sì|

## <a name="costing-methods-for-types-of-items"></a>Metodi di costing per tipi di articoli

Quando si registrano le transazioni di magazzino, le modifiche alle quantità e al valore del magazzino vengono registrate rispettivamente nei movimenti contabili articoli e nei movimenti di valorizzazione.

Registri il costo degli articoli di magazzino nel campo **Importo costo (effettivo)** della pagina **Movimenti di valorizzazione**. Quando riconcili il movimento nella contabilità generale, il costo viene visualizzato nel campo **Costo registrato in C/G**. Per saperne di più sul costing di magazzino, vedi [Dettagli di progettazione: costing di magazzino](design-details-inventory-costing.md) .

Per gli articoli non di magazzino e in assistenza, il costo è registrato nel campo **Importo costo (non-fatt.)** della pagina **Movimenti di valorizzazione**. Per gli articoli non di magazzino e in assistenza, specifica il costo nei documenti e nelle registrazioni di vendita, assemblaggio e produzione. Specifica il costo predefinito nel campo **Costo unitario** delle pagine **Scheda articolo** e **Unità di stockkeeping**. I costi per questi tipi di articoli non sono riconciliati nella contabilità generale.

## <a name="catalog-and-service-items"></a>Articoli di catalogo e in assistenza

Puoi impostare gli articoli che offri ai clienti ma che non gestisci fino a quando non li vendi come articoli di catalogo. Sebbene gli articoli di catalogo siano simili agli articoli normali di tipo **Non magazzino** a questo riguardo, non confondere i due perché ci sono delle differenze. Per ulteriori informazioni, vedi [Usare gli articoli di catalogo](inventory-how-work-nonstock-items.md).

Gli articoli dei clienti per i quali si esegue il servizio di assistenza, come una stampante, sono denominati articoli in assistenza. Gli articoli in assistenza non hanno nulla a che fare con articoli normali o di catalogo. Tuttavia, i componenti in assistenza possono essere articoli regolari. Per ulteriori informazioni, vedi [Impostare gli articoli in assistenza e i componenti degli articoli in assistenza](service-how-setup-service-items.md).

## <a name="see-also"></a>Vedere anche

[Registrare nuovi articoli](inventory-how-register-new-items.md)  
[Impostazione del magazzino](inventory-setup-inventory.md)  
[Gestione dei costi di magazzino](finance-manage-inventory-costs.md)  
[Magazzino](inventory-manage-inventory.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
