---
title: Report e analisi di inventario e warehouse
description: Vedere quali report e analisi di inventario e warehouse sono disponibili nella versione standard di Business Central in modo da poter tenere traccia della propria attività.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.search.keywords: reporting
ms.search.form: 'Report_707, Report_716, Report_813, Report_1001, Report_5807, Report_5808, Report_5809, Report_7313, Report_7319, Report_7320'
ms.date: 03/21/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="inventory-and-warehouse-reports-and-analytics"></a>Report e analisi di inventario e warehouse

Il report di inventario e warehouse in [!INCLUDE [prod_short](includes/prod_short.md)] consentono ai professionisti di inventario e aziendali di ottenere informazioni dettagliate e statistiche su attività di inventario e warehouse correnti e passate.  

## <a name="reports"></a>Report

[!INCLUDE [inventory_WMS_reports](includes/inventory-WMS-reports-include.md)]

## <a name="tasks"></a>Attività

I seguenti articoli descrivono alcune delle attività chiave per analizzare lo stato del tuo business:

* [Creare report di analisi](bi-how-create-analysis-views-reports.md)  
* [Visualizzare la disponibilità di articoli](inventory-how-availability-overview.md)

## <a name="print-and-scan-barcodes"></a>Stampare codici a barre ed eseguirne la scansione

L'uso di codici a barre può aiutare a semplificare i processi di warehouse in entrata, in uscita e interni. 

[!INCLUDE [barcode-mobile-app](includes/barcode-mobile-app.md)]

Dopo aver installato l'app, puoi utilizzare l'azione **Stampa etichetta** per stampare codici a barre 1D e 2D dalle pagine elencate nella tabella seguente.

|Pagina  |I valori dei campi che i codici a barre possono includere  |
|---------|---------|
|Articoli, Scheda articolo     |Nr. articolo, Descrizione e GTIN         |
|Lista riferimento articolo, Riferimento articolo     |Nr. articolo, Descrizione, Unità di misura e Nr. riferimento.         |
|Lista informazioni nr. lotto, Etichetta nr. lotto     |Nr. articolo, Descrizione e Numero lotto       |
|Etichetta NS     |Nr., Descrizione e Numero seriale         |

> [!NOTE]
> Alcune stampanti e formati di codici a barre/codici QR richiedono un'implementazione specifica. È possibile che tu debba caricare un modello Word differente o clonare il report per creare la tua versione personalizzata.

## <a name="see-also"></a>Vedere anche

[Impostazione del magazzino](inventory-setup-inventory.md)  
[Inventario](inventory-manage-inventory.md)  
[Impostazione Warehouse Management](warehouse-setup-warehouse.md)  
[Panoramica gestione del magazzino](design-details-warehouse-management.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
