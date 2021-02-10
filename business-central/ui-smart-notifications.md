---
title: Utilizzare le notifiche smart e specificare quando visualizzarle | Documenti Microsoft
description: È possibile ricevere notifiche con informazioni sulle modifiche di stato o di eventi, ad esempio, per un saldo scaduto o un magazzino in esaurimento.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: a297fd8381cf0af9de825cdaced658521e0335c8
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/17/2020
ms.locfileid: "4756644"
---
# <a name="manage-notifications"></a><span data-ttu-id="5f859-103">Gestire le notifiche</span><span class="sxs-lookup"><span data-stu-id="5f859-103">Manage Notifications</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="5f859-104">consente di lavorare in modo più intelligente tramite le notifiche che informano in merito a determinati eventi o modifiche dello stato, come, ad esempio, quando si sta per fatturare a un cliente che ha un saldo scaduto o la giacenza disponibile è inferiore alla quantità che si intende vendere.</span><span class="sxs-lookup"><span data-stu-id="5f859-104">can help you work smarter by notifying you about certain events or changes in status, such as when you are about to invoice a customer who has an overdue balance, or the available inventory is lower than the quantity you are about to sell, for example.</span></span> <span data-ttu-id="5f859-105">Queste notifiche vengono visualizzate come suggerimenti discreti nel contesto dell'attività che si sta eseguendo e consente di scegliere di ignorare la notifica o di visualizzare i dettagli sul problema.</span><span class="sxs-lookup"><span data-stu-id="5f859-105">These notifications are shown as discreet tips in the context of the task you are doing, and you can choose to ignore the notification or to see details about the issue.</span></span>  

<span data-ttu-id="5f859-106">Se si sceglie di visualizzare i dettagli relativi a una notifica, è possibile intraprendere azioni per risolvere il problema, come contattare il cliente, comprare altre scorte e così via.</span><span class="sxs-lookup"><span data-stu-id="5f859-106">If you choose to see details for a notification, you can take action to resolve the issue, such as contacting the customer, buying more inventory, and so on.</span></span> <span data-ttu-id="5f859-107">La scelta sulla cosa da fare è dell'utente, mentre [!INCLUDE[prod_short](includes/prod_short.md)] offre consigli e avvisi.</span><span class="sxs-lookup"><span data-stu-id="5f859-107">It's your choice what to do, and [!INCLUDE[prod_short](includes/prod_short.md)] gives you advice and recommendations.</span></span>  

<span data-ttu-id="5f859-108">Le notifiche consentono agli utenti non addestrati di completare attività poco familiari senza ridurre la produttività dell'utente più formato.</span><span class="sxs-lookup"><span data-stu-id="5f859-108">Notifications can help untrained users complete unfamiliar tasks, and do not reduce productivity for the more trained user.</span></span>  

## <a name="to-turn-notifications-on-or-off-and-control-when-they-are-sent"></a><span data-ttu-id="5f859-109">Per attivare o disattivare le notifiche e controllare quando vengono inviate</span><span class="sxs-lookup"><span data-stu-id="5f859-109">To turn notifications on or off, and control when they are sent</span></span>

<span data-ttu-id="5f859-110">Al primo avvio di [!INCLUDE[prod_short](includes/prod_short.md)] tutte le notifiche sono attivate, ma è possibile attivarle e disattivarle, ad esempio, se non si è interessati a un determinato evento o stato.</span><span class="sxs-lookup"><span data-stu-id="5f859-110">When you first start with [!INCLUDE[prod_short](includes/prod_short.md)] all notifications are turned on, but you can turn them on or off, for example, if you aren't interested in a certain event or status.</span></span>  

<span data-ttu-id="5f859-111">Inoltre, in alcune notifiche è possibile specificare le condizioni per l'invio.</span><span class="sxs-lookup"><span data-stu-id="5f859-111">Additionally, some notifications let you specify the conditions under which they are sent.</span></span> <span data-ttu-id="5f859-112">Ad esempio, se si desidera ricevere una notifica quando le scorte in magazzino sono insufficienti, ma solo per gli articoli acquistati da un determinato fornitore.</span><span class="sxs-lookup"><span data-stu-id="5f859-112">For example, if you want to be notified when inventory is running low, but only for items you buy from a certain vendor.</span></span>  

<span data-ttu-id="5f859-113">L'attivazione e la disattivazione delle notifiche e l'indicazione delle condizioni si applicano solo al cliente.</span><span class="sxs-lookup"><span data-stu-id="5f859-113">Turning notifications on or off, and specifying conditions, applies only to you.</span></span>  

1. <span data-ttu-id="5f859-114">Nell'angolo superiore destro scegliere l'icona **Impostazioni** ![Impostazioni](media/ui-experience/settings_icon_small.png "Icona Impostazioni per Gestione ruolo utente"), quindi scegliere l'azione **Impostazioni personali**.</span><span class="sxs-lookup"><span data-stu-id="5f859-114">In the top right corner, choose the **Settings** icon ![Settings](media/ui-experience/settings_icon_small.png "Settings icon for role center"), and then choose the **My Settings** action.</span></span>  
2. <span data-ttu-id="5f859-115">Nella pagina **Impostazioni personali**, nel campo **Notifiche**, scegliere il collegamento *Modificare il momento in cui ricevere le notifiche*</span><span class="sxs-lookup"><span data-stu-id="5f859-115">On the **My Settings** page, in the **Notifications** field, choose the *Change when I receive notifications.*</span></span> <span data-ttu-id="5f859-116">.</span><span class="sxs-lookup"><span data-stu-id="5f859-116">link.</span></span>  
3. <span data-ttu-id="5f859-117">Nella pagina visualizzata, attivare o disattivare una notifica selezionando o deselezionando la casella di controllo **Abilitato**.</span><span class="sxs-lookup"><span data-stu-id="5f859-117">In the page that appears, turn on or turn off a notification by selecting or clearing the **Enabled** check box.</span></span>  
4. <span data-ttu-id="5f859-118">Per specificare le condizioni che danno origine a una notifica, selezionare il collegamento **Visualizza dettagli filtro** e compilare i campi.</span><span class="sxs-lookup"><span data-stu-id="5f859-118">To specify conditions that trigger a notification, choose the **View filter details** link, and then fill in the fields.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5f859-119">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="5f859-119">See Also</span></span>

<span data-ttu-id="5f859-120">[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5f859-120">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
