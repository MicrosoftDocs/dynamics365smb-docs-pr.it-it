---
title: Informazioni sui tipi di articolo
description: 'È possibile modificare la valutazione di magazzino di un articolo mediante i metodi di costing Media o FIFO, quando i costi degli articoli cambiano per i motivi diversi dalle transazioni.'
documentationcenter: ''
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '9297, 5845, 30,'
ms.date: 06/16/2021
ms.author: edupont
---
# <a name="about-item-types" />Informazioni sui tipi di articolo
Nel campo **Tipo** nella pagina **Scheda articolo** è possibile selezionare l'articolo utilizzato nella propria azienda che influisce sul grado di gestione dell'articolo in magazzino. La tabella seguente elenca e descrive i tre tipi di articoli disponibili.

|Opzione|Scopo tipico|
|------|-----------|
|Inventario|Oggetti fisici, come biciclette, telefoni e scrivanie, per i quali vuoi essere in grado di utilizzare tutti i processi di magazzino. Questo può includere anche articoli non fisici, come licenze software e abbonamenti, se gli articoli hanno numeri di identificazione, come i numeri di serie. Puoi monitorare completamente i valori degli articoli e la disponibilità nell'inventario.|
|Non in inventario|In genere, gli articoli non di inventario sono oggetti fisici, come bulloni o penne, che un'azienda consuma ma non desidera tenere traccia completamente dell'inventario. Ad esempio, perché sono articoli a basso costo e vengono utilizzati solo internamente.|
|Assistenza|Un'unità di misura del tempo della manodopera, ad esempio un'ora di consulenza, per un supporto aziendale limitato.|

> [!NOTE]
> I tipi **Assistenza** e **Non in inventario** non supportano il tracciamento della quantità e del valore dell'inventario. Sono supportati solo i tipi e le funzionalità delle transazioni dell'articolo selezionato.

La seguente tabella include le funzionalità supportate dai tre tipi dell'articolo.

|Tipo di articolo|Vendite|Acquisti|Consumo per la commessa|Consumo di assistenza|Consumo assemblaggio|Consumo produzione|Output assemblaggio|Output produzione|Trasferimento ubicazione|Conteggio fisico|Rivalutazione del magazzino|Costing di magazzino|Tracciabilità articolo|Impegno|Gestione della warehouse|Piano|Pianificazione ordini|
|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|Inventario|Sì|Sì|Sì|Sì|Sì|Sì|Sì|Sì|Sì|Sì|Sì|Sì|Sì|Sì|Sì|Sì|Sì|
|Non magazzino|Sì|Sì|Sì|Sì|Sì|Sì|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Sì|
|Assistenza|Sì|Sì|Sì|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Sì|

## <a name="costing-methods-for-types-of-items" />Metodi di costing per tipi di articoli
Quando si registrano le transazioni di magazzino, le modifiche alle quantità e al valore del magazzino vengono registrate rispettivamente nei movimenti contabili articoli e nei movimenti di valorizzazione. 

Per gli articoli di magazzino, il costo è registrato nel campo **Importo costo (effettivo)** della pagina **Movimenti di valorizzazione** e quando viene riconciliato con la contabilità generale, il costo verrà visualizzato nel campo **Costo registrato in C/G**. Per ulteriori informazioni, vedere [Dettagli di progettazione: Costing di magazzino](design-details-inventory-costing.md).

Per gli articoli non di inventario e di assistenza il costo è registrato nel campo **Importo costo (non-fatt.)** della pagina **Movimenti di valorizzazione**. Per gli articoli non di inventario e di assistenza il costo è specificato nei documenti e nelle registrazioni di vendita, assemblaggio e produzione. Il costo predefinito può essere specificato nel campo **Costo unitario** delle pagine **Scheda articolo** e **Unità di stockkeeping**. I costi per questi tipi di articoli non sono riconciliati nella contabilità generale. 

## <a name="catalog-and-service-items" />Catalogo e articoli in assistenza
Gli articoli offerti ai clienti che non si desidera gestire nel sistema fino a quando non si inizia a venderli possono essere impostati come articoli di catalogo. Gli articoli di catalogo non devono essere confusi con articoli normali di tipo Non in inventario. Per ulteriori informazioni, vedere [Utilizzare gli articoli di catalogo](inventory-how-work-nonstock-items.md).

Gli articoli dei clienti per cui si esegue il servizio di assistenza, come una stampante, sono denominati articoli in assistenza. Gli articoli in assistenza non hanno nulla a che fare con articoli normali o di catalogo. Tuttavia, i componenti di assistenza possono essere articoli regolari. Per ulteriori informazioni, vedere [Impostare gli articoli in assistenza e i componenti degli articoli in assistenza](service-how-setup-service-items.md).

## <a name="see-also" />Vedi anche
[Registrare nuovi articoli](inventory-how-register-new-items.md)  
[Impostazione del magazzino](inventory-setup-inventory.md)  
[Gestione dei costi di magazzino](finance-manage-inventory-costs.md)  
[Magazzino](inventory-manage-inventory.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
