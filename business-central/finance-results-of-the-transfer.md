---
title: Risultati del trasferimento | Microsoft Docs
description: Questo argomento descrive i risultati del trasferimento di movimenti C/G a movimenti di costo.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: general ledger, transfer, cost entries
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: finance-transfer-and-post-cost-entries
ms.translationtype: HT
ms.sourcegitcommit: 67400e424305cc705db5c1bd52a8e4de17ecc5a9
ms.openlocfilehash: 0e17ff5ad60014cba6ce866c9ddae848b1239167
ms.contentlocale: it-it
ms.lasthandoff: 11/20/2018

---
# <a name="results-of-transferring-general-ledger-entries-to-cost-entries"></a><span data-ttu-id="cca14-103">Risultati del trasferimento di movimenti C/G a movimenti di costi</span><span class="sxs-lookup"><span data-stu-id="cca14-103">Results of Transferring General Ledger Entries to Cost Entries</span></span>
<span data-ttu-id="cca14-104">Durante il trasferimento dei movimenti C/G ai movimenti di costo, in [!INCLUDE[d365fin](includes/d365fin_md.md)] vengono creati i collegamenti nei movimenti nelle tabelle **Movimento CG**, **Movimento di costo** e **Registro costi** per consentire di tenere traccia dei collegamenti tra i movimenti di costo e i movimenti C/G.</span><span class="sxs-lookup"><span data-stu-id="cca14-104">During the transfer of general ledger entries to cost entries, [!INCLUDE[d365fin](includes/d365fin_md.md)] creates connections in the entries in the **G/L Entry** table, the **Cost Entry** table, and the **Cost Register** table to make it possible to trace the connections between cost entries and general ledger entries.</span></span>  

## <a name="general-ledger-entries"></a><span data-ttu-id="cca14-105">Movimenti C/G</span><span class="sxs-lookup"><span data-stu-id="cca14-105">General Ledger Entries</span></span>  
<span data-ttu-id="cca14-106">Per ogni movimento C/G che viene trasferito alla contabilità industriale, in [!INCLUDE[d365fin](includes/d365fin_md.md)] viene compilato il campo **Nr. movimento** dei costi.</span><span class="sxs-lookup"><span data-stu-id="cca14-106">For each general ledger entry that is transferred to cost accounting, [!INCLUDE[d365fin](includes/d365fin_md.md)] fills the cost **Entry No.** field.</span></span>  

## <a name="cost-entries"></a><span data-ttu-id="cca14-107">Movimenti di costi</span><span class="sxs-lookup"><span data-stu-id="cca14-107">Cost Entries</span></span>  
<span data-ttu-id="cca14-108">Per ogni movimento di costo, [!INCLUDE[d365fin](includes/d365fin_md.md)] salva il numero del movimento C/G corrispondente nel campo **Nr. movimento C/G** della tabella **Movimento di costo**.</span><span class="sxs-lookup"><span data-stu-id="cca14-108">For each cost entry, [!INCLUDE[d365fin](includes/d365fin_md.md)] saves the entry number of the corresponding general ledger entry in the **G/L Entry No.** field in the **Cost Entry** table.</span></span>  

<span data-ttu-id="cca14-109">Per i movimenti di costi combinati, in [!INCLUDE[d365fin](includes/d365fin_md.md)] viene salvato il numero dell'ultimo movimento C/G, vale a dire il movimento con il numero più alto.</span><span class="sxs-lookup"><span data-stu-id="cca14-109">For combined cost entries, [!INCLUDE[d365fin](includes/d365fin_md.md)] saves the entry number of the last general ledger entry, which is the entry with the highest entry number.</span></span>  

<span data-ttu-id="cca14-110">Nel campo **Conto C/G** della tabella **Movimento di costo** è contenuto il numero del conto di contabilità generale da cui deriva il movimento di costo.</span><span class="sxs-lookup"><span data-stu-id="cca14-110">The **G/L Account** field in the **Cost Entry** table contains the number of the general ledger account that the cost entry came from.</span></span>  

<span data-ttu-id="cca14-111">Per i singoli movimenti di costo, in [!INCLUDE[d365fin](includes/d365fin_md.md)] viene trasferito il testo della registrazione dal movimento C/G al campo di testo **Descrizione**.</span><span class="sxs-lookup"><span data-stu-id="cca14-111">For single cost entries, [!INCLUDE[d365fin](includes/d365fin_md.md)] transfers the posting text from the general ledger entry to the **Description** text field.</span></span> <span data-ttu-id="cca14-112">Per i movimenti combinati, il campo di testo mostra che questi movimenti vengono trasferiti come movimenti combinati.</span><span class="sxs-lookup"><span data-stu-id="cca14-112">For combined entries, the text field shows these entries are transferred as combined entries.</span></span> <span data-ttu-id="cca14-113">Ad esempio, per un movimento combinato per il mese di ottobre 2013, il testo può essere **Movimenti combinati, ottobre 2013**.</span><span class="sxs-lookup"><span data-stu-id="cca14-113">For example, for a combined entry for the month of October in 2013, the text can be **Combined Entries, October 2013**.</span></span>  

## <a name="cost-register"></a><span data-ttu-id="cca14-114">Registro costi</span><span class="sxs-lookup"><span data-stu-id="cca14-114">Cost Register</span></span>  
<span data-ttu-id="cca14-115">Nella tabella **Registro costi**, [!INCLUDE[d365fin](includes/d365fin_md.md)] crea un movimento con il trasferimento di origine dalla contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="cca14-115">In the **Cost Register** table, [!INCLUDE[d365fin](includes/d365fin_md.md)] creates an entry with the source transfer from general ledger.</span></span> <span data-ttu-id="cca14-116">Il movimento registra il primo e l'ultimo numero dei movimenti C/G trasferiti, oltre al primo e all'ultimo numero dei movimenti di costo creati.</span><span class="sxs-lookup"><span data-stu-id="cca14-116">The entry records the first and last entry numbers of the general ledger entries that are transferred, in addition to the first and last entry numbers of the cost entries that are created.</span></span>  

## <a name="see-also"></a><span data-ttu-id="cca14-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cca14-117">See Also</span></span>  
[<span data-ttu-id="cca14-118">Trasferimento e registrazione di movimenti di costi</span><span class="sxs-lookup"><span data-stu-id="cca14-118">Transferring and Posting Cost Entries</span></span>](finance-transfer-and-post-cost-entries.md)   

