---
title: Impostare il log delle e-mail | Documenti Microsoft
description: Informazioni su come trasformare le interazioni e-mail tra venditori e clienti in reali opportunità di vendita.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect, opportunity, email
ms.date: 07/01/2020
ms.author: bholtorf
ms.openlocfilehash: 9ca381bfebcd6db8e67d8153d4d2bc17eeffad81
ms.sourcegitcommit: f9aec4a72172d9270e14e2938c5550d69508f1aa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/02/2020
ms.locfileid: "3532671"
---
# <a name="track-email-message-exchanges-between-salespeople-and-contacts"></a><span data-ttu-id="dfcfe-103">Tenere traccia degli scambi di messaggi e-mail tra venditori e contatti</span><span class="sxs-lookup"><span data-stu-id="dfcfe-103">Track Email Message Exchanges Between Salespeople and Contacts</span></span>

<span data-ttu-id="dfcfe-104">Ottenere di più dalle comunicazioni tra i venditori e i tuoi clienti esistenti o potenziali monitorando gli scambi di e-mail e trasformandoli in opportunità fruibili.</span><span class="sxs-lookup"><span data-stu-id="dfcfe-104">Get more out of the communications between salespeople and your existing or potential customers by tracking email exchanges, and then turning them into actionable opportunities.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="dfcfe-105">può utilizzare Exchange Online per tenere un log dei messaggi in entrata e in uscita.</span><span class="sxs-lookup"><span data-stu-id="dfcfe-105">can work with Exchange Online to keep a log of the inbound and outbound messages.</span></span> <span data-ttu-id="dfcfe-106">È possibile visualizzare e analizzare i contenuti di ciascun messaggio nella pagina **Movimenti log interazione**.</span><span class="sxs-lookup"><span data-stu-id="dfcfe-106">You can view and analyze the contents of each message on the **Interaction Log Entries** page.</span></span>

## <a name="set-up-public-folders-and-rules-for-email-logging-in-exchange-online"></a><span data-ttu-id="dfcfe-107">Impostare le cartelle pubbliche e le regole per il log delle e-mail in Exchange Online</span><span class="sxs-lookup"><span data-stu-id="dfcfe-107">Set up Public Folders and Rules for Email Logging in Exchange Online</span></span>

[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

<span data-ttu-id="dfcfe-108">Quindi, connettersi a [!INCLUDE[prodshort](includes/prodshort.md)] con Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="dfcfe-108">Next, you connect [!INCLUDE[prodshort](includes/prodshort.md)] with Exchange Online.</span></span>

## <a name="setting-up-d365fin-to-log-email-messages"></a><span data-ttu-id="dfcfe-109">Impostare [!INCLUDE[d365fin](includes/d365fin_md.md)] per registrare i messaggi e-mail</span><span class="sxs-lookup"><span data-stu-id="dfcfe-109">Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)] to Log Email Messages</span></span>

<span data-ttu-id="dfcfe-110">Iniziare la registrazione dei messaggi e-mail con due semplici passaggi:</span><span class="sxs-lookup"><span data-stu-id="dfcfe-110">Get started with email logging in two easy steps:</span></span>

1. <span data-ttu-id="dfcfe-111">Collegare [!INCLUDE[d365fin](includes/d365fin_md.md)]con Exchange Online per l'abbonamento di Office 365.</span><span class="sxs-lookup"><span data-stu-id="dfcfe-111">Connect [!INCLUDE[d365fin](includes/d365fin_md.md)] with Exchange Online for your Office 365 subscription.</span></span> <span data-ttu-id="dfcfe-112">Exchange Online gestisce i messaggi di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="dfcfe-112">Exchange Online handles your email messages.</span></span> <span data-ttu-id="dfcfe-113">Questo passaggio è stato semplificato con una guida di installazione assistita.</span><span class="sxs-lookup"><span data-stu-id="dfcfe-113">We've made this step easy by providing an assisted setup guide.</span></span> <span data-ttu-id="dfcfe-114">Sono solo necessarie le credenziali di amministratore per l'account amministratore in Office 365.</span><span class="sxs-lookup"><span data-stu-id="dfcfe-114">You just need your administrator credentials for your administrator account in Office 365.</span></span> <span data-ttu-id="dfcfe-115">Per iniziare la guida, andare a **Setup assistito** e quindi scegliere **Configurare la registrazione e-mail**.</span><span class="sxs-lookup"><span data-stu-id="dfcfe-115">To start the guide, go to **Assisted Setup**, and then choose **Set up email logging**.</span></span>  

2. <span data-ttu-id="dfcfe-116">Assicurarsi che siano stati inseriti indirizzi email validi in [!INCLUDE[d365fin](includes/d365fin_md.md)] per gli addetti alle vendite e i contatti, a seconda che si tratti di clienti potenziali o esistenti.</span><span class="sxs-lookup"><span data-stu-id="dfcfe-116">Make sure that valid email addresses have been entered in [!INCLUDE[d365fin](includes/d365fin_md.md)] for your sales people and contacts, depending on whether they are potential or existing customers.</span></span> <span data-ttu-id="dfcfe-117">Per fare ciò, per ogni cliente o venditore, aprire la scheda **Contatto** o **Venditore/Acquirente** e osservare il campo **E-mail**.</span><span class="sxs-lookup"><span data-stu-id="dfcfe-117">To do that, for each customer or salesperson, open the **Contact** or **Salesperson/Purchaser** card and have a look in the **Email** field.</span></span>

> [!Tip]
> <span data-ttu-id="dfcfe-118">Dopo aver completato i passaggi nella guida, è possibile verificare se la connessione ha avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="dfcfe-118">After you complete the steps in the guide you can check whether the connection was successful.</span></span> <span data-ttu-id="dfcfe-119">Cercare **Impostazione marketing**, scegliere **Processi**, **Funzioni** e **Convalida configurazione registrazione email**.</span><span class="sxs-lookup"><span data-stu-id="dfcfe-119">Search for **Marketing Setup**, choose **Process**, then **Functions**, and then **Validate Email Logging Setup**.</span></span>

## <a name="viewing-email-message-exchanges-in-the-interaction-log"></a><span data-ttu-id="dfcfe-120">Visualizzazione degli scambi di messaggi e-mail nel log delle interazioni</span><span class="sxs-lookup"><span data-stu-id="dfcfe-120">Viewing Email Message Exchanges in the Interaction Log</span></span>

[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="dfcfe-121">crea una voce nella pagina **Log delle interazioni** ogni volta che un venditore e un contatto scambiano un messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="dfcfe-121">creates an entry on the **Interaction Log** page each time a salesperson and a contact exchange an email message.</span></span> <span data-ttu-id="dfcfe-122">Per visualizzare il log delle interazioni, aprire la scheda **Contatto** o **Venditore/Acquirente** per la persona, quindi scegliere **Naviga**, **Cronologia** e **Voci del registro delle interazioni**.</span><span class="sxs-lookup"><span data-stu-id="dfcfe-122">To view the interaction log, open the **Contact** or **Salesperson\*Purchaser** card for the person, and then choose **Navigate**, **History**, and then choose **Interaction Log Entries**.</span></span> <span data-ttu-id="dfcfe-123">Ci sono alcune cose che si possono fare con ogni voce del log, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="dfcfe-123">There are a few things we can do with each entry in the log, for example:</span></span>

- <span data-ttu-id="dfcfe-124">Visualizzare il contenuto del messaggio di posta elettronica che è stato scambiato facendo clic sull'azione **Mostra allegati**.</span><span class="sxs-lookup"><span data-stu-id="dfcfe-124">View the content of the email message that was exchanged by clicking the **Show Attachments** action.</span></span>
- <span data-ttu-id="dfcfe-125">Trasformare uno scambio di e-mail in un'opportunità di vendita: se una voce sembra promettente, è possibile trasformarla in un'opportunità e gestirne i progressi verso una vendita.</span><span class="sxs-lookup"><span data-stu-id="dfcfe-125">Turn an email exchange into a sales opportunity - If an entry looks promising, you can turn it into an opportunity and then manage its progress toward a sale.</span></span> <span data-ttu-id="dfcfe-126">A tale scopo, selezionare la voce e scegliere l'azione **Crea opportunità**.</span><span class="sxs-lookup"><span data-stu-id="dfcfe-126">To do that, choose the entry, and then choose the **Create Opportunity** action.</span></span> <span data-ttu-id="dfcfe-127">Per ulteriori informazioni, vedere [Gestire opportunità di vendita](marketing-manage-sales-opportunities.md).</span><span class="sxs-lookup"><span data-stu-id="dfcfe-127">For more information, see [Managing Sales Opportunities](marketing-manage-sales-opportunities.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="dfcfe-128">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="dfcfe-128">See Also</span></span>
[<span data-ttu-id="dfcfe-129">Gestione delle relazioni</span><span class="sxs-lookup"><span data-stu-id="dfcfe-129">Managing Relationships</span></span>](marketing-relationship-management.md)

