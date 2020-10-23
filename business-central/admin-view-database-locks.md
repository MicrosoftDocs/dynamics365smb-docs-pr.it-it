---
title: Visualizzare blocchi di database
description: Informazioni su come visualizzare le informazioni sui blocchi di database direttamente dall'interfaccia client in Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 6880ffa9a2ab42c1af7c22f9cace64697c9f905b
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3922319"
---
# <a name="viewing-database-locks"></a><span data-ttu-id="1d48d-103">Visualizzazione di blocchi di database</span><span class="sxs-lookup"><span data-stu-id="1d48d-103">Viewing Database Locks</span></span>

<span data-ttu-id="1d48d-104">Il blocco del database controlla l'accesso da parte di più utenti agli stessi dati contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="1d48d-104">Database locking controls access by multiple users to the same data at the same time.</span></span> <span data-ttu-id="1d48d-105">Per proteggere una transazione dalla modifica degli stessi dati da parte di altre transazioni, la prima transazione blocca i dati.</span><span class="sxs-lookup"><span data-stu-id="1d48d-105">To protect a transaction against other transactions modifying the same data, the first transaction puts a lock on the data.</span></span> <span data-ttu-id="1d48d-106">Il blocco rimane fino al termine della transazione.</span><span class="sxs-lookup"><span data-stu-id="1d48d-106">The lock remains until the transaction's done.</span></span>

<span data-ttu-id="1d48d-107">Agli utenti potrebbe essere impedito di completare le transazioni sui dati bloccati.</span><span class="sxs-lookup"><span data-stu-id="1d48d-107">Users may be blocked from completing transactions on the locked data.</span></span> <span data-ttu-id="1d48d-108">In genere riceveranno un messaggio che indica la condizione di blocco.</span><span class="sxs-lookup"><span data-stu-id="1d48d-108">They'll typically get a message that indicates the lock condition.</span></span>

## <a name="to-view-database-locks"></a><span data-ttu-id="1d48d-109">Per visualizzare i blocchi di database</span><span class="sxs-lookup"><span data-stu-id="1d48d-109">To view database locks</span></span>

<span data-ttu-id="1d48d-110">Scegli l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Icona Cerca pagina o report"), immetti **Blocchi database**, quindi scegli il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="1d48d-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Database Locks**, and then choose the related link.</span></span>

<span data-ttu-id="1d48d-111">La pagina **Blocchi di database** fornisce uno snapshot di tutti i blocchi del database correnti.</span><span class="sxs-lookup"><span data-stu-id="1d48d-111">The **Database Locks** page gives snapshot of all current database locks.</span></span>

<span data-ttu-id="1d48d-112">Per ulteriori informazioni sul blocco del database, consultare [Monitoraggio dei blocchi del database](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) nella guida per sviluppatori e professionisti IT di Business Central.</span><span class="sxs-lookup"><span data-stu-id="1d48d-112">For more information about database locking, see [Monitoring Database Locks](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) in the Business Central Developer and IT Pro help.</span></span>

## <a name="see-also"></a><span data-ttu-id="1d48d-113">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="1d48d-113">See Also</span></span>

[<span data-ttu-id="1d48d-114">Monitorare i blocchi del database</span><span class="sxs-lookup"><span data-stu-id="1d48d-114">Monitor Database Locks</span></span>](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) 
