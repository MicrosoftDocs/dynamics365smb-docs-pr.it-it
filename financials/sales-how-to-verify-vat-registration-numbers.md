---
title: 'Procedura: Verificare i numeri di partita IVA | Documenti Microsoft'
description: "È possibile utilizzare un servizio Web dell'UE per verificare che i numeri di partita IVA immessi nelle schede cliente, fornitore o contatto siano validi."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/10/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 7180c7823055dba52a398584ed2f4c2952d08492
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-verify-vat-registration-numbers"></a><span data-ttu-id="d35b1-103">Procedura: verificare i numeri di partita IVA</span><span class="sxs-lookup"><span data-stu-id="d35b1-103">How to: Verify VAT Registration Numbers</span></span>
<span data-ttu-id="d35b1-104">È possibile utilizzare un servizio Web dell'UE per verificare che i numeri di partita IVA immessi nelle schede cliente, fornitore o contatto siano validi.</span><span class="sxs-lookup"><span data-stu-id="d35b1-104">You can use an EU web service to verify that VAT registration numbers that you enter on customer, vendor, or contact cards are valid.</span></span>  

 <span data-ttu-id="d35b1-105">Quando si modifica il campo **Partita IVA** in una scheda in cui il valore nel campo **Codice paese** è un paese UE, il nuovo numero di partita IVA e il proprio ID utente vengono registrati nella finestra **Log partita IVA**.</span><span class="sxs-lookup"><span data-stu-id="d35b1-105">When you modify the **VAT Registration No.** field on a card where the value in the **Country/Region Code** field is an EU country/region, then the new VAT registration number and your user ID are logged in the **VAT Registration Log** window.</span></span> <span data-ttu-id="d35b1-106">Per verificare un numero di partita IVA, fare clic sul pulsante **Verifica partita IVA** nella finestra **Log partita IVA**.</span><span class="sxs-lookup"><span data-stu-id="d35b1-106">You verify a VAT registration number by choosing the **Verify Registration No.** button in the **VAT Registration Log** window.</span></span> <span data-ttu-id="d35b1-107">Una nuova riga viene creata ogni volta che si utilizza la funzione di verifica.</span><span class="sxs-lookup"><span data-stu-id="d35b1-107">A new line is created every time you use the verification function.</span></span> <span data-ttu-id="d35b1-108">Se si è potuto verificare il numero, il campo  **Stato** contiene **Valido**.</span><span class="sxs-lookup"><span data-stu-id="d35b1-108">If the number could be verified, the **Status** field contains **Valid**.</span></span> <span data-ttu-id="d35b1-109">Se non si è potuto verificare il numero, il campo**Stato** contiene **Non valido** ed è necessario quindi modificare il numero nel campo **Partita IVA** nella scheda e avviare nuovamente la funzione di verifica.</span><span class="sxs-lookup"><span data-stu-id="d35b1-109">If the number could not be verified, the **Status** field contains **Invalid**, and you must then change the number in the **VAT Registration No.** field on the card and start the verification function again.</span></span>  

 <span data-ttu-id="d35b1-110">L'URL di gestione del servizio Web di default viene impostato nel campo **URL convalida partita IVA** della finestra **Setup contabilità generale**.</span><span class="sxs-lookup"><span data-stu-id="d35b1-110">The URL of the default web service is set up in the **VAT Reg. No. Validation URL** field in the **General Ledger Setup** window.</span></span>  

 <span data-ttu-id="d35b1-111">Nella tabella **Formato nr. partita IVA**, è possibile cambiare per ogni paese i diversi formati di numero di partita IVA che gli utenti possono immettere nel campo **Partita IVA**.</span><span class="sxs-lookup"><span data-stu-id="d35b1-111">In the **VAT Registration No. Format** table, you can change for each country/region the different formats of VAT registration number that users are allowed to enter in the **VAT Registration No.** field.</span></span>  

> [!WARNING]  
>  <span data-ttu-id="d35b1-112">Questo servizio Web utilizza il protocollo HTTP, il che significa che i dati trasferiti tramite il servizio non sono crittografati.</span><span class="sxs-lookup"><span data-stu-id="d35b1-112">This web service uses the http protocol, which means that data transferred through the service is not encrypted.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="d35b1-113">È possibile che si verifichino periodi di inattività per questo servizio per i quali Microsoft non è responsabile, in quanto il servizio fa parte di un'ampia rete dell'UE di registri IVA locali.</span><span class="sxs-lookup"><span data-stu-id="d35b1-113">You may experience downtime for this service for which Microsoft is not responsible, as the service is part of a broad EU network of national VAT registers.</span></span>  

## <a name="to-verify-a-vat-registration-number-from-a-customer-card"></a><span data-ttu-id="d35b1-114">Per verificare un numero di partita IVA da una scheda cliente</span><span class="sxs-lookup"><span data-stu-id="d35b1-114">To verify a VAT registration number from a customer card</span></span>  
<span data-ttu-id="d35b1-115">Di seguito viene descritto come verificare un numero di partita IVA per un cliente.</span><span class="sxs-lookup"><span data-stu-id="d35b1-115">The following describes how to verify a VAT registration number for a customer.</span></span> <span data-ttu-id="d35b1-116">I passaggi sono simili per un contatto o un fornitore.</span><span class="sxs-lookup"><span data-stu-id="d35b1-116">The steps are similar for a vendor and a contact.</span></span>   
1.  <span data-ttu-id="d35b1-117">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Clienti**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="d35b1-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customers**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="d35b1-118">Aprire la scheda di un cliente in cui si desidera verificare il numero di partita IVA.</span><span class="sxs-lookup"><span data-stu-id="d35b1-118">Open the card of a customer where you want to verify the VAT registration number.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="d35b1-119">Il campo **Codice paese** nella scheda cliente deve contenere un paese UE.</span><span class="sxs-lookup"><span data-stu-id="d35b1-119">The **Country/Region Code** field on the customer card must contain an EU country/region.</span></span>  
3.  <span data-ttu-id="d35b1-120">Nella Scheda dettaglio **Fatturazione**, fare clic sul pulsante Drilldown a discesa accanto al campo **Partita IVA**.</span><span class="sxs-lookup"><span data-stu-id="d35b1-120">On the **Invoicing** FastTab, choose the DrillDown button next to the **VAT Registration No.** field.</span></span>  

    <span data-ttu-id="d35b1-121">La finestra **Log partita IVA** si apre visualizzando una riga in cui il campo **Stato** contiene **Non verificato**.</span><span class="sxs-lookup"><span data-stu-id="d35b1-121">The **VAT Registration Log** window opens showing one line where the **Status** field contains **Not Verified**.</span></span>  
4.  <span data-ttu-id="d35b1-122">Scegliere l'azione **Verifica partita IVA**.</span><span class="sxs-lookup"><span data-stu-id="d35b1-122">Choose the **Verify Registration No.** action.</span></span>  

     <span data-ttu-id="d35b1-123">Una nuova riga viene creata quando il campo **Stato** contiene **Valido** o **Non valido**.</span><span class="sxs-lookup"><span data-stu-id="d35b1-123">A new line is created where the **Status** field contains either **Valid** or **Invalid**.</span></span>  
5.  <span data-ttu-id="d35b1-124">Se il campo **Stato** contiene **Non valido**, modificare il numero nel campo **Partita IVA** nella scheda quindi ripetere i passaggi da 3 a 4.</span><span class="sxs-lookup"><span data-stu-id="d35b1-124">If the **Status** field contains **Invalid**, change the number in the **VAT Registration No.** field on the card, and then repeat steps 3 through 4.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d35b1-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d35b1-125">See Also</span></span>  
[<span data-ttu-id="d35b1-126">Finanze</span><span class="sxs-lookup"><span data-stu-id="d35b1-126">Finance</span></span>](finance.md)  
[<span data-ttu-id="d35b1-127">Procedura: Registrare nuovi clienti</span><span class="sxs-lookup"><span data-stu-id="d35b1-127">How to: Register New Customers</span></span>](sales-how-register-new-customers.md)  
[<span data-ttu-id="d35b1-128">Procedura: Registrare nuovi fornitori</span><span class="sxs-lookup"><span data-stu-id="d35b1-128">How to: Register New Vendors</span></span>](purchasing-how-register-new-vendors.md)  
<span data-ttu-id="d35b1-129">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d35b1-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

