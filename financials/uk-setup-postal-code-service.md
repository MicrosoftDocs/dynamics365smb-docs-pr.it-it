---
title: 'Procedura: Impostare l''estensione dei codici postali GetAddress.io per il Regno Unito | Documenti Microsoft'
description: "Descrive le funzionalità generali utilizzate per interagire con i dati in Financials, ad esempio per immettere valori, ordinare dati e modificare le visualizzazioni."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: getaddress.io, postcodes, extension
ms.date: 06/02/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: c5a99f7a90b2f832bba3eb088d0faa7514c14708
ms.contentlocale: it-it
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-set-up-the-getaddressio-uk-postcodes-extension"></a><span data-ttu-id="1579f-103">Procedura: Impostare l'estensione dei codici postali GetAddress.io per il Regno Unito</span><span class="sxs-lookup"><span data-stu-id="1579f-103">How to: Set Up the GetAddress.io UK Postcodes Extension</span></span>
<span data-ttu-id="1579f-104">Questa estensione semplifica l'inserimento di indirizzi del Regno Unito per entità come clienti, contatti, dipendenti, fornitori, conti bancari e così via.</span><span class="sxs-lookup"><span data-stu-id="1579f-104">This extension makes it easy to enter addresses in the UK for entities like customers, contacts, employees, vendors, bank accounts, and so on.</span></span> 

<span data-ttu-id="1579f-105">L'estensione dei codici postali GetAddress.io per il Regno Unito utilizza l'API getAddress per trovare gli indirizzi nei codici postali del Regno Unito.</span><span class="sxs-lookup"><span data-stu-id="1579f-105">The GetAddress.io UK Postcodes extension uses the getAddress API to find addresses in postcodes in the UK.</span></span> <span data-ttu-id="1579f-106">Per utilizzare l'estensione, è necessario disporre di un piano e una chiave API per l'API getAddress.</span><span class="sxs-lookup"><span data-stu-id="1579f-106">To use the extension, you need to get a plan and an API Key for the getAddress API.</span></span> <span data-ttu-id="1579f-107">Questa operazione è semplice e può essere effettuata quando si imposta l'estensione dei codici postali GetAddress.io per il Regno Unito.</span><span class="sxs-lookup"><span data-stu-id="1579f-107">That's easy, and we help you do that when you set up the GetAddress.io UK Postcodes extension.</span></span> <span data-ttu-id="1579f-108">I piani sono basati sull'utilizzo, o ciò che viene talvolta detto "chiamate".</span><span class="sxs-lookup"><span data-stu-id="1579f-108">Plans are based on use, or what's sometimes referred to as calls.</span></span> <span data-ttu-id="1579f-109">In questo caso, una chiamata si verifica quando [!INCLUDE[d365fin](includes/d365fin_md.md)] visualizza un elenco di indirizzi per un codice postale.</span><span class="sxs-lookup"><span data-stu-id="1579f-109">A call, in this case, is when [!INCLUDE[d365fin](includes/d365fin_md.md)] displays a list of addresses in a postcode.</span></span> <span data-ttu-id="1579f-110">In base alla frequenza con cui si aggiungono gli indirizzi, scegliere il piano migliore in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="1579f-110">Depending on how often you add addresses, choose the plan that is best for you.</span></span> <span data-ttu-id="1579f-111">Se si sceglie **Ottieni chiave API** nella pagina, si utilizzerà il piano **Gratuito** che consente di aggiungere 20 indirizzi al giorni e che è valido per 30 giorni.</span><span class="sxs-lookup"><span data-stu-id="1579f-111">If you just choose **Get API Key** in the page, you'll use the **Free** plan, which lets you add 20 addresses per day, and is valid for 30 days.</span></span> 

##<a name="to-set-up-the-getaddressio-uk-postcodes-extension"></a><span data-ttu-id="1579f-112">Per impostare l'estensione dei codici postali GetAddress.io per il Regno Unito</span><span class="sxs-lookup"><span data-stu-id="1579f-112">To set up the GetAddress.io UK Postcodes extension</span></span> 
1. <span data-ttu-id="1579f-113">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Connessioni servizio**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="1579f-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Connections**, and then choose the related link.</span></span>  
2. <span data-ttu-id="1579f-114">Nel finestra **Connessioni servizio** scegliere **Servizio CAP UK**.</span><span class="sxs-lookup"><span data-stu-id="1579f-114">In the **Service Connections** window, choose **UK Postcode Service**.</span></span>
3. <span data-ttu-id="1579f-115">Nella pagina **Configurazione fornitore codice postale** scegliere **Disabilitata**.</span><span class="sxs-lookup"><span data-stu-id="1579f-115">In the **Postcode provider configuration** page, choose **Disabled**.</span></span>
4. <span data-ttu-id="1579f-116">Nella finestra **Selezione servizio CAP**, scegliere **GetAddress.io**.</span><span class="sxs-lookup"><span data-stu-id="1579f-116">In the **Postal code service selection** window, choose **GetAddress.io**.</span></span>
5. <span data-ttu-id="1579f-117">Nella finestra **Config GetAddress.io** selezionare **Ottieni chiave API** per aprire la pagina **Piani** nel sito Web dell'API getAddress.</span><span class="sxs-lookup"><span data-stu-id="1579f-117">In the **GetAddress.io Config** window, choose **Get API Key** to open the **Plans** page on the website for the getAddress API.</span></span>  

    > [!NOTE]  
>   <span data-ttu-id="1579f-118">Potrebbe essere necessario disabilitare i pop-up nel browser.</span><span class="sxs-lookup"><span data-stu-id="1579f-118">You might need to allow pop-ups in your browser.</span></span>
6. <span data-ttu-id="1579f-119">Acquistare un piano o scegliere **Ottieni chiave API** e immettere il proprio indirizzo e-mail.</span><span class="sxs-lookup"><span data-stu-id="1579f-119">Purchase a plan, or just choose **Get API Key**, and then provide your email address.</span></span>
7. <span data-ttu-id="1579f-120">Aprire l'e-mail da getAddress.io e copiare la chiave il codice API.</span><span class="sxs-lookup"><span data-stu-id="1579f-120">Open the email from getAddress.io, and copy the API key.</span></span> <span data-ttu-id="1579f-121">La chiave si trova sotto l'intestazione **La tua chiave API**.</span><span class="sxs-lookup"><span data-stu-id="1579f-121">The key is under the **Your API Key** heading.</span></span>
8. <span data-ttu-id="1579f-122">Nella finestra **Config GetAddress.io** incollare la chiave API nel campo **Chiave API** e scegliere **OK**.</span><span class="sxs-lookup"><span data-stu-id="1579f-122">In the **GetAddress.io Config** window, paste the API key in the **API Key** field, and then choose **OK**.</span></span>
9. <span data-ttu-id="1579f-123">Nella pagina **Connessioni servizio** verificare che il campo **Fornitore indirizzo** mostri **GetAddress.io**.</span><span class="sxs-lookup"><span data-stu-id="1579f-123">In the **Service Connections** page, verify that the **Address Provider** field shows **GetAddress.io**.</span></span> <span data-ttu-id="1579f-124">Se così, il servizio è abilitato.</span><span class="sxs-lookup"><span data-stu-id="1579f-124">If it does, the service is enabled.</span></span>

## <a name="see-also"></a><span data-ttu-id="1579f-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1579f-125">See Also</span></span>
<span data-ttu-id="1579f-126">[Utilizzare codici postali di GetAddress.io per il Regno Unito](ui-extensions-getaddressio.md)
[Personalizzazione di [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzando le estensioni](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="1579f-126">[GetAddress.io UK Postcodes](ui-extensions-getaddressio.md)
[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
<span data-ttu-id="1579f-127">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1579f-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
