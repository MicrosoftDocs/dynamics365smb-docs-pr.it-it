---
title: Utilizzare Invoicing e Finance and Operations, Business edition | Documenti Microsoft
description: Soluzione alternativa per l'accesso a Microsoft Invoicing dopo aver effettuato l'iscrizione a Dynamics 365 for Finance and Operations, Business edition.
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/22/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: 803569ed99f00b9055c5a6ec6e4ffae67d9df2bd
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="using-the-same-office-365-account-in-included365finincludesd365finlongmdmd-and-microsoft-invoicing"></a><span data-ttu-id="556e5-103">Utilizzo dello stesso account di Office 365 in [!INCLUDE[d365fin](includes/d365fin_long_md.md)] e Microsoft Invoicing</span><span class="sxs-lookup"><span data-stu-id="556e5-103">Using the same Office 365 Account in [!INCLUDE[d365fin](includes/d365fin_long_md.md)] and Microsoft Invoicing</span></span>
<span data-ttu-id="556e5-104">Quando si effettua l'iscrizione per una versione di prova con [!INCLUDE[d365fin](includes/d365fin_md.md)], è possibile passare a una fase di valutazione di 30 giorni, effettuare una sottoscrizione oppure interrompere l'utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="556e5-104">When you sign up for a trial with [!INCLUDE[d365fin](includes/d365fin_md.md)], you can move to a 30-day evaluation phase, you can start a subscription, or you can stop using [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="556e5-105">In tutti i casi, se si accede al portale di Office, è possibile che venga visualizzata una sezione denominata **Business Center** selezionabile con un clic.</span><span class="sxs-lookup"><span data-stu-id="556e5-105">In all cases, if you log into the Office Portal, you might see a tile called **Business center** and click it.</span></span> <span data-ttu-id="556e5-106">Questo elemento fa parte della sottoscrizione a Office 365 Business Premium, quindi non tutti gli utenti visualizzeranno tale sezione nel portale di Office.</span><span class="sxs-lookup"><span data-stu-id="556e5-106">This is part of the Office 365 Business Premium subscription, so not everyone will see that tile in the Office Portal.</span></span>  

<span data-ttu-id="556e5-107">Se si accede al Business Center, verrà visualizzata una sezione denominata **Fatturazione**.</span><span class="sxs-lookup"><span data-stu-id="556e5-107">If you do access the Business center, you will see a section called **Invoicing**.</span></span> <span data-ttu-id="556e5-108">Se si accede a tale sezione, verrà visualizzato un messaggio nel quale viene comunicato che non è possibile accedere a Microsoft Invoicing perché l'account è utilizzato in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="556e5-108">If you access that section, you will see a message that you cannot access Microsoft Invoicing because your account is used in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

<span data-ttu-id="556e5-109">Un messaggio simile viene visualizzato se si installa l'app mobile per Invoicing.</span><span class="sxs-lookup"><span data-stu-id="556e5-109">You see a similar message if you install the mobile app for Invoicing.</span></span>  

## <a name="workaround"></a><span data-ttu-id="556e5-110">Soluzione alternativa</span><span class="sxs-lookup"><span data-stu-id="556e5-110">Workaround</span></span>
<span data-ttu-id="556e5-111">Invoicing e [!INCLUDE[d365fin](includes/d365fin_md.md)] dispongono di una piattaforma condivisa.</span><span class="sxs-lookup"><span data-stu-id="556e5-111">Invoicing and [!INCLUDE[d365fin](includes/d365fin_md.md)] have a shared platform.</span></span> <span data-ttu-id="556e5-112">Di conseguenza, quando l'utente fa clic su Invoicing nel Business Center, viene riconosciuto come un utente esistente di [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="556e5-112">That means that you are recognized as an existing user of [!INCLUDE[d365fin](includes/d365fin_md.md)] when you click Invoicing in the Business center.</span></span> <span data-ttu-id="556e5-113">Ciò si verifica perché Invoicing non può utilizzare la stessa società in uso in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="556e5-113">The reason is that Invoicing cannot use the same company as [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

<span data-ttu-id="556e5-114">Sarà necessario accedere a [!INCLUDE[d365fin](includes/d365fin_md.md)], rinominare la società esistente, quindi creare una nuova società che potrà essere utilizzata in Invoicing.</span><span class="sxs-lookup"><span data-stu-id="556e5-114">So you will have to log into [!INCLUDE[d365fin](includes/d365fin_md.md)] and rename your existing company, and then create a new company that you can then use in Invoicing.</span></span> <span data-ttu-id="556e5-115">Nessun dato viene spostato né sovrascritto durante questa soluzione alternativa.</span><span class="sxs-lookup"><span data-stu-id="556e5-115">No data is moved or overwritten during this workaround.</span></span>

### <a name="to-rename-your-company"></a><span data-ttu-id="556e5-116">Per rinominare la società</span><span class="sxs-lookup"><span data-stu-id="556e5-116">To rename your company</span></span>
1.  <span data-ttu-id="556e5-117">Accedere a [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="556e5-117">Sign in to your [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
2.  <span data-ttu-id="556e5-118">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Società**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="556e5-118">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Companies**, and then choose the related link.</span></span>  
3.  <span data-ttu-id="556e5-119">Nella finestra **Società**, scegliere il pulsante **Modifica lista**.</span><span class="sxs-lookup"><span data-stu-id="556e5-119">In the **Companies** window, choose the **Edit List** button.</span></span>  
4.  <span data-ttu-id="556e5-120">Modificare il nome dell'elemento *La mia società* inserendo una denominazione diversa.</span><span class="sxs-lookup"><span data-stu-id="556e5-120">Change the name of the *My Company* entry to something else.</span></span>  

    <span data-ttu-id="556e5-121">Attendere alcuni minuti.</span><span class="sxs-lookup"><span data-stu-id="556e5-121">Wait a number of minutes.</span></span> <span data-ttu-id="556e5-122">Apporteremo alcune modifiche nel database sottostante e tale operazione richiede del tempo.</span><span class="sxs-lookup"><span data-stu-id="556e5-122">We’ll be making a number of changes in the underlying database, and that takes a while.</span></span>
5.  <span data-ttu-id="556e5-123">Quando il sistema è nuovamente pronto all'uso, scegliere il pulsante **Crea nuova società**.</span><span class="sxs-lookup"><span data-stu-id="556e5-123">When the system is ready again, choose the **Create New Company** button.</span></span>  
6.  <span data-ttu-id="556e5-124">Nella finestra di dialogo visualizzata, specificare il nome come *La mia società*, quindi scegliere l'opzione **Produzione - Solo dati setup**.</span><span class="sxs-lookup"><span data-stu-id="556e5-124">In the dialog that appears, specify the name as *My Company*, and choose the **Production – Setup Data Only** option.</span></span>  

<span data-ttu-id="556e5-125">Anche tale operazione richiede alcuni minuti.</span><span class="sxs-lookup"><span data-stu-id="556e5-125">This again takes a number of minutes.</span></span> <span data-ttu-id="556e5-126">Al completamento del processo, sarà possibile accedere a Invoicing come parte dell'esperienza Office 365 Business Premium.</span><span class="sxs-lookup"><span data-stu-id="556e5-126">When the process completes, you will be able to access Invoicing as part of your Office 365 Business Premium experience.</span></span>  

### <a name="what-about-my-data"></a><span data-ttu-id="556e5-127">Quali modifiche vengono apportate ai miei dati?</span><span class="sxs-lookup"><span data-stu-id="556e5-127">What about my data?</span></span>
<span data-ttu-id="556e5-128">Quando si rinomina l'elemento originale in La mia società, le tabelle del database in cui sono memorizzati i dati [!INCLUDE[d365fin](includes/d365fin_md.md)] esistenti vengono rinominate, ma i dati stessi non subiscono alcuna modifica.</span><span class="sxs-lookup"><span data-stu-id="556e5-128">When you rename the original My Company, the database tables that store your existing [!INCLUDE[d365fin](includes/d365fin_md.md)] data are renamed, but the data itself is not touched.</span></span>  

<span data-ttu-id="556e5-129">Se si utilizza sia Invoicing che [!INCLUDE[d365fin](includes/d365fin_md.md)], i dati vengono memorizzati in due contenitori diversi (le due società).</span><span class="sxs-lookup"><span data-stu-id="556e5-129">If you use both Invoicing and [!INCLUDE[d365fin](includes/d365fin_md.md)], the data is stored in two different containers (the two companies).</span></span> <span data-ttu-id="556e5-130">Nessun elemento viene condiviso, quindi sarà necessario gestire i clienti e gli articoli in entrambe le società.</span><span class="sxs-lookup"><span data-stu-id="556e5-130">Nothing is shared, so you'll have to manage customers and items in both companies.</span></span>  

## <a name="see-also"></a><span data-ttu-id="556e5-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="556e5-131">See Also</span></span>
[<span data-ttu-id="556e5-132">Domande frequenti</span><span class="sxs-lookup"><span data-stu-id="556e5-132">Frequently Asked Questions</span></span>](across-faq.md)  
[<span data-ttu-id="556e5-133">Setup e amministrazione</span><span class="sxs-lookup"><span data-stu-id="556e5-133">Setup and Administration</span></span>](admin-setup-and-administration.md)  

