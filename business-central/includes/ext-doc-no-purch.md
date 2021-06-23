---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 05/27/2021
ms.author: edupont
ms.openlocfilehash: 59376b96dcd6f755040b07784ceca53e157bcf14
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115974"
---
<span data-ttu-id="861c9-101">Nei documenti acquisto e nelle registrazioni è possibile specificare un numero documento che fa riferimento al sistema di numerazione del fornitore.</span><span class="sxs-lookup"><span data-stu-id="861c9-101">On purchase documents and journals, you can specify a document number that refers to the vendor's numbering system.</span></span> <span data-ttu-id="861c9-102">Utilizzare questo campo per registrare il numero assegnato dal fornitore all'ordine, alla fattura o alla nota di credito.</span><span class="sxs-lookup"><span data-stu-id="861c9-102">Use this field to record the number that the vendor assigned to the order, invoice, or credit memo.</span></span> <span data-ttu-id="861c9-103">Il numero potrà essere utilizzato per cercare la riga dopo che questa sia stata contabilizzata.</span><span class="sxs-lookup"><span data-stu-id="861c9-103">You can then use the number later if, for some reason, you need to search for the posted entry using this number.</span></span>

<span data-ttu-id="861c9-104">Il campo **Nr. doc. esterno obblig.** nella pagina **Setup contabilità fornitori** specifica se è obbligatorio inserire un numero di documento esterno nelle seguenti situazioni:</span><span class="sxs-lookup"><span data-stu-id="861c9-104">The **Ext. Doc. No. Mandatory** field in the **Purchases & Payables Setup** page specifies whether it is mandatory to enter an external document number in the following situations:</span></span>

* <span data-ttu-id="861c9-105">Nel campo **Nr. fattura fornitore**, **Nr. ordine fornitore**</span><span class="sxs-lookup"><span data-stu-id="861c9-105">In the **Vendor Invoice No.** field, **Vendor Order No.**</span></span> <span data-ttu-id="861c9-106">o **Nr. nota credito for.**</span><span class="sxs-lookup"><span data-stu-id="861c9-106">field, or the **Vendor Cr. Memo No.**</span></span> <span data-ttu-id="861c9-107">in una testata acquisto</span><span class="sxs-lookup"><span data-stu-id="861c9-107">field on a purchase header</span></span>

* <span data-ttu-id="861c9-108">Nel campo **Nr. documento esterno** in una riga registrazioni COGE, dove il campo **Tipo di Documento** è impostato su *Fattura*, *Nota Credito* o *Nota addebito interessi* e il campo **Tipo conto** è impostato su *Fornitore*.</span><span class="sxs-lookup"><span data-stu-id="861c9-108">In the **External Document No.** field on a general journal line, where the **Document Type** field is set to *Invoice*, *Credit Memo*, or *Finance Charge Memo*, and the **Account Type** field is set to *Vendor*.</span></span>

<span data-ttu-id="861c9-109">Selezionando questo campo con un segno di spunta, non sarà possibile registrare alcuna fattura, nota di credito o riga delle registrazioni generali del tipo descritto sopra senza un numero di documento esterno.</span><span class="sxs-lookup"><span data-stu-id="861c9-109">If you select this field, it will not be possible to post an invoice, a credit memo, or the type of general journal line described above without an external document number.</span></span>

<span data-ttu-id="861c9-110">Il numero del documento esterno è incluso nei documenti registrati in cui è possibile eseguire la ricerca in base al numero pertinente.</span><span class="sxs-lookup"><span data-stu-id="861c9-110">The external document number is included in posted documents where you can search by the relevant number.</span></span> <span data-ttu-id="861c9-111">È inoltre possibile eseguire la ricerca utilizzando il numero di documento esterno durante la navigazione nei movimenti contabili fornitori.</span><span class="sxs-lookup"><span data-stu-id="861c9-111">You can also search using the external document number when navigating on vendor ledger entries.</span></span>

<span data-ttu-id="861c9-112">Un modo diverso di gestire i numeri dei documenti esterni consiste nell'utilizzare il campo **Vs. riferimento**.</span><span class="sxs-lookup"><span data-stu-id="861c9-112">A different way to handle external document numbers is to use the **Your Reference** field.</span></span> <span data-ttu-id="861c9-113">Se viene utilizzato il campo **Vs. riferimento**, il numero verrà incluso nei documenti registrati e puoi cercarlo come per i valori dei campi **Nr. documento esterno** .</span><span class="sxs-lookup"><span data-stu-id="861c9-113">If you use the **Your Reference** field, the number will be included in posted documents, and you can search by it in the same way as for values from **External Document No.** fields.</span></span> <span data-ttu-id="861c9-114">Ma il campo non è disponibile nelle righe di registrazione.</span><span class="sxs-lookup"><span data-stu-id="861c9-114">But the field is not available on journal lines.</span></span>
