---
title: Impostare i metodi preferiti per l'invio dei documenti di vendita | Documenti Microsoft
description: "Descrive come impostare il metodo preferito di ogni cliente per l'invio dei documenti di vendita, ad esempio e-mail, PDF, documento elettronico, e così via."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: email, PDF, electronic document
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 7f7499e6e501207ed5fd6ebbee5b94d18c1d008e
ms.contentlocale: it-it
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-set-up-document-sending-profiles"></a><span data-ttu-id="f1054-103">Procedura: Impostare profili di invio documenti</span><span class="sxs-lookup"><span data-stu-id="f1054-103">How to: Set Up Document Sending Profiles</span></span>
<span data-ttu-id="f1054-104">È possibile impostare per ogni cliente un metodo preferito di invio documenti di vendita, in modo da non dover selezionare un'opzione di invio ogni volta che si sceglie l'azione **Registra e invia**.</span><span class="sxs-lookup"><span data-stu-id="f1054-104">You can set each customer up with a preferred method of sending sales documents, so that you do not have to select a sending option every time you choose the **Post and Send** action.</span></span>

<span data-ttu-id="f1054-105">Nella finestra **Profili di invio documenti** si impostano differenti profili di vendita che è possibile selezionare dal campo **Profilo di invio documenti** nella scheda cliente.</span><span class="sxs-lookup"><span data-stu-id="f1054-105">In the **Document Sending Profiles** window, you set up different sending profiles that you can select from in the **Document Sending Profile** field on a customer card.</span></span> <span data-ttu-id="f1054-106">È possibile selezionare la casella di controllo **Default** per specificare che il profilo di invio documenti è il profilo predefinito per tutti i clienti, eccetto per quelli per i quali il campo **Profilo di invio documenti** è compilato con un altro profilo di invio.</span><span class="sxs-lookup"><span data-stu-id="f1054-106">You can select the **Default** check box to specify that the document sending profile is the default profile for all customers, except for customers where the **Document Sending Profile** field is filled with another sending profile.</span></span>

<span data-ttu-id="f1054-107">Se si sceglie l'azione **Registra e invia** in un documento di vendita, nella finestra di dialogo **Registra e invia conferma** viene visualizzato anche il profilo di invio utilizzato, cioè quello impostato per il cliente o quello predefinito per tutti i clienti.</span><span class="sxs-lookup"><span data-stu-id="f1054-107">When you choose the **Post and Send** action on a sales document, the **Post and Send Confirmation** dialog box shows the sending profile used, either the one set up for the customer or the default for all customers.</span></span> <span data-ttu-id="f1054-108">Nella finestra di dialogo è possibile modificare il profilo di invio per il documento di vendita.</span><span class="sxs-lookup"><span data-stu-id="f1054-108">In the dialog box, you can change the sending profile for the sales document.</span></span> <span data-ttu-id="f1054-109">Per ulteriori informazioni, vedere [Procedura: Fatturare le vendite](sales-how-invoice-sales.md).</span><span class="sxs-lookup"><span data-stu-id="f1054-109">For more information, see [How to: Invoice Sales](sales-how-invoice-sales.md).</span></span>

## <a name="to-set-up-a-document-sending-profile"></a><span data-ttu-id="f1054-110">Per impostare un profilo di invio documenti</span><span class="sxs-lookup"><span data-stu-id="f1054-110">To set up a document sending profile</span></span>
1. <span data-ttu-id="f1054-111">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Profili di invio documenti**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="f1054-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Document Sending Profiles**, and then choose the related link.</span></span>
2. <span data-ttu-id="f1054-112">Nella finestra **Profili di invio documenti** scegliere l'azione **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="f1054-112">In the **Document Sending Profiles** window, choose the **New** action.</span></span>
3. <span data-ttu-id="f1054-113">Compilare i campi, se necessario.</span><span class="sxs-lookup"><span data-stu-id="f1054-113">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-specify-a-sending-profile-on-a-customer-card"></a><span data-ttu-id="f1054-114">Per specificare un profilo di invio in una scheda cliente</span><span class="sxs-lookup"><span data-stu-id="f1054-114">To specify a sending profile on a customer card</span></span>
1. <span data-ttu-id="f1054-115">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Clienti**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="f1054-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customers**, and then choose the related link.</span></span>
2. <span data-ttu-id="f1054-116">Aprire la scheda del cliente per cui si desidera impostare un profilo di invio.</span><span class="sxs-lookup"><span data-stu-id="f1054-116">Open the card of the customer who you want to set up a sending profile for.</span></span>
3. <span data-ttu-id="f1054-117">Nel campo **Profilo di invio documenti** selezionare un profilo che è stato impostato secondo la procedura descritta in precedenza.</span><span class="sxs-lookup"><span data-stu-id="f1054-117">In the **Document Sending Profile** field, select a profile that you have set up as described in the previous procedure.</span></span>

## <a name="see-also"></a><span data-ttu-id="f1054-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f1054-118">See Also</span></span>
[<span data-ttu-id="f1054-119">Setup Vendite</span><span class="sxs-lookup"><span data-stu-id="f1054-119">Setting Up Sales</span></span>](sales-setup-sales.md)  
[<span data-ttu-id="f1054-120">Vendite</span><span class="sxs-lookup"><span data-stu-id="f1054-120">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="f1054-121">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f1054-121">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

