---
title: Informazioni sui tipi di articolo | Documenti Microsoft
description: È possibile modificare la valutazione di magazzino di un articolo mediante i metodi di costing Media o FIFO, ad esempio, quando i costi degli articoli cambiano per i motivi diversi dalle transazioni.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: b3c9b79701296cd21492752e94b2a0ec7848658b
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/17/2020
ms.locfileid: "4746318"
---
# <a name="about-item-types"></a>Informazioni sui tipi di articolo
Nel campo **Tipo** nella pagina **Scheda articolo** è possibile selezionare l'articolo utilizzato nella propria azienda e quindi come viene gestito nel sistema. Sono disponibili tre opzioni:

|Opzione|Scopo tipico|
|------|-----------|
|Inventario|Un'unità fisica, come una bicicletta, per un pieno supporto commerciale.|
|Non in inventario|Un'unità fisica, ad esempio un bullone, per un supporto aziendale limitato, ad esempio perché l'articolo viene utilizzato solo internamente e ha un costo ridotto.|
|Assistenza|Un'unità di misura del tempo della manodopera, ad esempio un'ora di consulenza, per un supporto aziendale limitato.|

Il tipo **Inventario** prevede il monitoraggio completo della quantità e del valore di inventario. Di conseguenza, tutti i tipi di transazione dell'articolo sono supportati e gli articoli di tipo Inventario possono essere utilizzati con tutte le funzionalità di gestione degli articoli.

I tipi **Assistenza** e **Non in inventario** non prevedono il tracciamento della quantità e del valore dell'inventario. Di conseguenza, sono supportati solo i tipi e le funzionalità delle transazioni dell'articolo selezionato.

I tre tipi dell'articolo supportano rispettivamente le seguenti funzionalità.

|Tipo di articolo|Vendite|Acquisti|Consumo per la commessa|Consumo di assistenza|Consumo assemblaggio|Consumo produzione|Output assemblaggio|Output produzione|Trasferimento ubicazione|Conteggio fisico|Rivalutazione del magazzino|Costing di magazzino|Tracciabilità articolo|Impegni|Gestione della warehouse|Pianificazione|
|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|Magazzino|Sì|Sì|Sì|Sì|Sì|Sì|Sì|Sì|Sì|Sì|Sì|Sì|Sì|Sì|Sì|Sì|
|Non in inventario|Sì|Sì|Sì|Sì|Sì|Sì|No|No|No|No|No|No|No|No|No|No|
|Assistenza|Sì|Sì|Sì|No|No|No|No|No|No|No|No|No|No|No|No|No|

## <a name="costing-methods-for-types-of-items"></a>Metodi di costing per tipi di articoli
Quando si registrano le transazioni di magazzino, le modifiche alle quantità e al valore del magazzino vengono registrate rispettivamente nei movimenti contabili articoli e nei movimenti di valorizzazione. 

Per gli articoli di magazzino, il costo è registrato nel campo **Importo costo (effettivo)** della pagina **Movimenti di valorizzazione** e quando viene riconciliato con la contabilità generale, il costo verrà visualizzato nel campo **Costo registrato in C/G**. Per ulteriori informazioni, vedere [Dettagli di progettazione: Costing di magazzino](design-details-inventory-costing.md).

Per gli articoli non di inventario e di assistenza il costo è registrato nel campo **Importo costo (non-fatt.)** della pagina **Movimenti di valorizzazione**. Per gli articoli non di inventario e di assistenza il costo è specificato nei documenti e nelle registrazioni di vendita, assemblaggio e produzione. Il costo predefinito può essere specificato nel campo **Costo unitario** delle pagine **Scheda articolo** e **Unità di stockkeeping**. I costi per questi tipi di articoli non sono riconciliati nella contabilità generale. 

## <a name="catalog-and-service-items"></a>Catalogo e articoli in assistenza
Gli articoli offerti ai clienti che non si desidera gestire nel sistema fino a quando non si inizia a venderli possono essere impostati come articoli di catalogo. Gli articoli di catalogo non devono essere confusi con articoli normali di tipo Non in inventario. Per ulteriori informazioni, vedere [Utilizzare gli articoli di catalogo](inventory-how-work-nonstock-items.md).

Gli articoli dei clienti per cui si esegue il servizio di assistenza, come una stampante, sono denominati articoli in assistenza. Gli articoli in assistenza non hanno nulla a che fare con articoli normali o di catalogo. Tuttavia, i componenti di assistenza possono essere articoli regolari. Per ulteriori informazioni, vedere [Impostare gli articoli in assistenza e i componenti degli articoli in assistenza](service-how-setup-service-items.md).

## <a name="see-also"></a>Vedi anche
[Registrare nuovi articoli](inventory-how-register-new-items.md)  
[Impostazione del magazzino](inventory-setup-inventory.md)  
[Gestione dei costi di magazzino](finance-manage-inventory-costs.md)  
[Magazzino](inventory-manage-inventory.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]