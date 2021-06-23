---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 05/27/2021
ms.author: edupont
ms.openlocfilehash: 50b4b331f00bdcdf030bac2332ffb5dafdfd2de6
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115977"
---
<span data-ttu-id="49413-101">Nei documenti di vendita e nelle registrazioni è possibile specificare un numero documento che fa riferimento al sistema di numerazione del cliente.</span><span class="sxs-lookup"><span data-stu-id="49413-101">On sales documents and journals, you can specify a document number that refers to the customer's numbering system.</span></span> <!--You can enter a maximum of ten characters, both numbers and letters.--> <span data-ttu-id="49413-102">Utilizzare questo campo per registrare il numero assegnato dal cliente all'ordine, alla fattura o alla nota di credito.</span><span class="sxs-lookup"><span data-stu-id="49413-102">Use this field to record the number that the customer assigned to the order, invoice, or credit memo.</span></span> <span data-ttu-id="49413-103">Il numero potrà essere utilizzato per cercare la riga dopo che questa sia stata contabilizzata.</span><span class="sxs-lookup"><span data-stu-id="49413-103">You can then use the number later if, for some reason, you need to search for the posted entry using this number.</span></span>  

<span data-ttu-id="49413-104">Il campo **Nr. doc. esterno obblig.** della pagina **Setup contabilità clienti** specifica se è obbligatorio inserire un numero documento estenro nel campo **Nr. documento esterno** su un'intestazione vendite e il campo **Nr. documento esterno** in una riga registrazioni COGE.</span><span class="sxs-lookup"><span data-stu-id="49413-104">The **Ext. Doc. No. Mandatory** field on the **Sales & Receivables Setup** page specifies whether it is mandatory to enter an external document number in the **External Document No.** field on a sales header and the **External Document No.** field on a general journal line.</span></span>

<span data-ttu-id="49413-105">Selezionando questo campo, non sarà possibile registrare alcuna fattura o riga delle registrazioni generali senza un numero di documento esterno.</span><span class="sxs-lookup"><span data-stu-id="49413-105">If you select this field, it will not be possible to post an invoice or a general journal line without an external document number.</span></span>

<span data-ttu-id="49413-106">Il numero del documento esterno è incluso nei documenti registrati in cui è possibile eseguire la ricerca in base al numero pertinente.</span><span class="sxs-lookup"><span data-stu-id="49413-106">The external document number is included in posted documents where you can search by the relevant number.</span></span> <span data-ttu-id="49413-107">È inoltre possibile eseguire la ricerca utilizzando il numero di documento esterno durante la navigazione nei movimenti contabili clienti.</span><span class="sxs-lookup"><span data-stu-id="49413-107">You can also search using the external document number when navigating on customer ledger entries.</span></span>

<span data-ttu-id="49413-108">Un modo diverso di gestire i numeri dei documenti esterni consiste nell'utilizzare il campo **Vs. riferimento**.</span><span class="sxs-lookup"><span data-stu-id="49413-108">A different way to handle external document numbers is to use the **Your Reference** field.</span></span> <span data-ttu-id="49413-109">Se viene utilizzato il campo **Vs. riferimento**, il numero verrà incluso nei documenti registrati e puoi cercarlo come per i valori dei campi **Nr. documento esterno** .</span><span class="sxs-lookup"><span data-stu-id="49413-109">If you use the **Your Reference** field, the number will be included in posted documents, and you can search by it in the same way as for values from **External Document No.** fields.</span></span> <span data-ttu-id="49413-110">Ma il campo non è disponibile nelle righe di registrazione.</span><span class="sxs-lookup"><span data-stu-id="49413-110">But the field is not available on journal lines.</span></span>
