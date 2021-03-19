---
title: Visualizzare Informazioni tabella
description: Informazioni su come visualizzare le informazioni sulle tabelle di database direttamente dall'interfaccia client in Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: a4695594573056ec492bc15c29d1b6fca3100e97
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5388676"
---
# <a name="viewing-table-information"></a><span data-ttu-id="35fce-103">Visualizzazione di Informazioni tabella</span><span class="sxs-lookup"><span data-stu-id="35fce-103">Viewing Table Information</span></span>

<span data-ttu-id="35fce-104">La pagina **Informazioni sulla tabella 8700** fornisce informazioni su tutte le tabelle di sistema e aziendali in una soluzione Business Central.</span><span class="sxs-lookup"><span data-stu-id="35fce-104">The page **8700 Table Information** provides information about all system and business tables in a Business Central solution.</span></span> <span data-ttu-id="35fce-105">In particolare, la pagina visualizza informazioni sulla quantità di dati contenuta nelle tabelle.</span><span class="sxs-lookup"><span data-stu-id="35fce-105">In particular, the page displays information about the amount of data the tables contain.</span></span>

<span data-ttu-id="35fce-106">Queste informazioni sono utili per la risoluzione dei problemi di prestazioni, perché consente di vedere la distribuzione delle dimensioni dei dati tra le tabelle.</span><span class="sxs-lookup"><span data-stu-id="35fce-106">This information is useful for troubleshooting performance problems, because let's you see the distribution of data size across tables.</span></span>

## <a name="viewing-table-information"></a><span data-ttu-id="35fce-107">Visualizzazione di Informazioni tabella</span><span class="sxs-lookup"><span data-stu-id="35fce-107">Viewing table information</span></span>

<span data-ttu-id="35fce-108">Per aprire questa pagina, scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Icona Cerca pagina o report"), immettere **Informazioni tabella** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="35fce-108">To open this page, select the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Table Information**, and then choose the related link.</span></span>

<span data-ttu-id="35fce-109">La tabella seguente descrive le informazioni fornite per ciascuna tabella:</span><span class="sxs-lookup"><span data-stu-id="35fce-109">The following table describes the information provided for each table:</span></span>

|<span data-ttu-id="35fce-110">Colonna</span><span class="sxs-lookup"><span data-stu-id="35fce-110">Column</span></span>|<span data-ttu-id="35fce-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="35fce-111">Description</span></span>|
|------|-----------|
|<span data-ttu-id="35fce-112">Nome società</span><span class="sxs-lookup"><span data-stu-id="35fce-112">Company Name</span></span>|<span data-ttu-id="35fce-113">Nome della società, se presente, a cui appartiene la tabella.</span><span class="sxs-lookup"><span data-stu-id="35fce-113">The name of the company, if any, that the table belongs to.</span></span>|
|<span data-ttu-id="35fce-114">Nome tabella</span><span class="sxs-lookup"><span data-stu-id="35fce-114">Table Name</span></span>|<span data-ttu-id="35fce-115">Il nome della tabella.</span><span class="sxs-lookup"><span data-stu-id="35fce-115">The name of the table.</span></span>|
|<span data-ttu-id="35fce-116">Nr. tabella</span><span class="sxs-lookup"><span data-stu-id="35fce-116">Table No.</span></span>|<span data-ttu-id="35fce-117">L'ID della tabella.</span><span class="sxs-lookup"><span data-stu-id="35fce-117">The ID of the table</span></span>|
|<span data-ttu-id="35fce-118">No.</span><span class="sxs-lookup"><span data-stu-id="35fce-118">No.</span></span> <span data-ttu-id="35fce-119">di record</span><span class="sxs-lookup"><span data-stu-id="35fce-119">of Records</span></span>|<span data-ttu-id="35fce-120">Il numero totale di record archiviati nella tabella.</span><span class="sxs-lookup"><span data-stu-id="35fce-120">The total number of records stored in the table.</span></span>|
|<span data-ttu-id="35fce-121">Dim. record</span><span class="sxs-lookup"><span data-stu-id="35fce-121">Record Size</span></span>|<span data-ttu-id="35fce-122">La dimensione media del record in KB/record.</span><span class="sxs-lookup"><span data-stu-id="35fce-122">The average record size in KB/record.</span></span> <span data-ttu-id="35fce-123">Il valore viene calcolato utilizzando la seguente formula: 1024 (Dimensione)/(N.</span><span class="sxs-lookup"><span data-stu-id="35fce-123">The value is calculated using the following formula: 1024(Size)/(No.</span></span> <span data-ttu-id="35fce-124">di record).</span><span class="sxs-lookup"><span data-stu-id="35fce-124">of Records)\`.</span></span> |

## <a name="see-also"></a><span data-ttu-id="35fce-125">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="35fce-125">See Also</span></span>

[<span data-ttu-id="35fce-126">Controllo di pagine</span><span class="sxs-lookup"><span data-stu-id="35fce-126">Inspecting Pages</span></span>](across-inspect-page.md)  
[<span data-ttu-id="35fce-127">Articoli sulle prestazioni per gli sviluppatori</span><span class="sxs-lookup"><span data-stu-id="35fce-127">Performance Articles For Developers</span></span>](/dynamics365/business-central/dev-itpro/performance/performance-developer)  


[!INCLUDE[footer-include](includes/footer-banner.md)]