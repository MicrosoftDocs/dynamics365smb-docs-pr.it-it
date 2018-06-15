---
title: Utilizzare i profili per classificare i contatti
description: Impostare i questionari profilo per classificare i contatti business
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: contacts, profiles
ms.author: edupont
ms.date: 05/09/2018
ms.translationtype: HT
ms.sourcegitcommit: 75501b9402bb1c14fcfeb2fc6e61f055a2247493
ms.openlocfilehash: 00cfce8b467040a4de419c1b59a258c0eacf0b9a
ms.contentlocale: it-it
ms.lasthandoff: 05/15/2018

---

# <a name="use-profile-questionnaires-to-classify-business-contacts"></a><span data-ttu-id="10709-103">Utilizzare i questionari profilo per classificare i contatti business</span><span class="sxs-lookup"><span data-stu-id="10709-103">Use Profile Questionnaires to Classify Business Contacts</span></span>
<span data-ttu-id="10709-104">È possibile impostare questionari profilo da utilizzare durante l'immissione di informazioni sul profilo dei contatti.</span><span class="sxs-lookup"><span data-stu-id="10709-104">You can set up profile questionnaires that you want to use when entering information about your contacts' profiles.</span></span> <span data-ttu-id="10709-105">In ogni questionario, è possibile impostare le diverse domande da porre ai contatti.</span><span class="sxs-lookup"><span data-stu-id="10709-105">Within each questionnaire, you can set up the different questions you intend to ask your contacts.</span></span>  

<span data-ttu-id="10709-106">È inoltre possibile eseguire il questionario per rispondere automaticamente ad alcune domande sulla base dei dati di contatto, cliente o fornitore.</span><span class="sxs-lookup"><span data-stu-id="10709-106">You can also run the questionnaire to answer some of the questions based on contact, customer, or vendor data automatically.</span></span>  

## <a name="to-add-a-profile-questionnaire"></a><span data-ttu-id="10709-107">Per aggiungere un questionario profilo</span><span class="sxs-lookup"><span data-stu-id="10709-107">To add a profile questionnaire</span></span>
1.  <span data-ttu-id="10709-108">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Setup questionari**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="10709-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Questionnaire Setup**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="10709-109">Nel gruppo **Nuovo** della scheda **Pagina iniziale** scegliere **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="10709-109">On the **Home** tab, in the **New** group, choose **New**.</span></span>  
3.  <span data-ttu-id="10709-110">Compilare i campi come necessario.</span><span class="sxs-lookup"><span data-stu-id="10709-110">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-add-questions-to-a-profile-questionnaire"></a><span data-ttu-id="10709-111">Per aggiungere domande a un questionario profilo</span><span class="sxs-lookup"><span data-stu-id="10709-111">To add questions to a profile questionnaire</span></span>
1.  <span data-ttu-id="10709-112">Scegliere il profilo pertinente e nel gruppo **Processo** della scheda **Pagina iniziale** scegliere **Modifica setup questionario**.</span><span class="sxs-lookup"><span data-stu-id="10709-112">Choose the relevant profile questionnaire, and then on the **Home** tab, in the **Process** group, choose **Edit Questionnaire Setup**.</span></span>  
2.  <span data-ttu-id="10709-113">Sulla prima riga vuota, nel campo **Tipo**, scegliere **Domanda** e digitare la domanda desiderata nel campo **Descrizione**.</span><span class="sxs-lookup"><span data-stu-id="10709-113">On the first empty line, in the **Type** field, choose **Question** and type your question in the **Description** field.</span></span> <span data-ttu-id="10709-114">Compilare gli altri campi della riga.</span><span class="sxs-lookup"><span data-stu-id="10709-114">Fill in the other fields on this line.</span></span>  
3.  <span data-ttu-id="10709-115">Sulla prima riga vuota successiva nel campo **Tipo**, scegliere **Risposta** e digitare la risposta desiderata nel campo **Descrizione**.</span><span class="sxs-lookup"><span data-stu-id="10709-115">On the next empty line, in the **Type** field, choose **Answer** and type your answer in the **Description** field.</span></span>  
4.  <span data-ttu-id="10709-116">Nel campo **Priorità** selezionare la priorità.</span><span class="sxs-lookup"><span data-stu-id="10709-116">In the **Priority** field, select the priority.</span></span> <span data-ttu-id="10709-117">Nei campi **Da valore** e **A valore** definire un intervallo di punti.</span><span class="sxs-lookup"><span data-stu-id="10709-117">In the **From Value** and **To Value** fields, define a point range.</span></span> <span data-ttu-id="10709-118">I contatti che ricevono punti entro l'intervallo stabilito otterranno la risposta.</span><span class="sxs-lookup"><span data-stu-id="10709-118">Contacts that receive points within the defined range will get the answer.</span></span>  

<span data-ttu-id="10709-119">Ripetere tali passaggi per immettere tutte le domande e le risposte nel questionario profilo.</span><span class="sxs-lookup"><span data-stu-id="10709-119">Repeat these steps to enter all the questions and answers within the profile questionnaire.</span></span>

<span data-ttu-id="10709-120">Dopo avere creato un questionario, è necessario creare le valutazioni dei contatti per classificare i contatti.</span><span class="sxs-lookup"><span data-stu-id="10709-120">After you have created a questionnaire, you must create contact ratings to classify your contacts.</span></span> <span data-ttu-id="10709-121">È inoltre possibile impostare le domande classificate automaticamente in base alle informazioni presenti nella scheda contatto.</span><span class="sxs-lookup"><span data-stu-id="10709-121">You can also set up questions that are rated automatically based on information in the contact card.</span></span>  

> [!NOTE]
> <span data-ttu-id="10709-122">Se si immette una domanda con risposta automatica, selezionare <STRONG>Riga</STRONG> e quindi <STRONG>Dettagli domanda</STRONG> per immettere i criteri da utilizzare per fornire la risposta automatica.</span><span class="sxs-lookup"><span data-stu-id="10709-122">If you enter a question that is automatically answered, choose <STRONG>Line</STRONG>, and then choose <STRONG>Question Details</STRONG>, to enter the criteria to automatically answer the question.</span></span>

## <a name="the-automatic-classification-of-contacts"></a><span data-ttu-id="10709-123">Classificazione automatica dei contatti</span><span class="sxs-lookup"><span data-stu-id="10709-123">The Automatic Classification of Contacts</span></span>
<span data-ttu-id="10709-124">È possibile classificare automaticamente i contatti in base alle informazioni relative a cliente, fornitore e contatto, mediante una serie di domande sul profilo con risposta automatica nella finestra **Setup questionario profilo**.</span><span class="sxs-lookup"><span data-stu-id="10709-124">You can automatically classify your contacts according to customer, vendor, and contact information, by setting up automatically answered profile questions in the **Profile Questionnaire Setup** window.</span></span>  

> [!NOTE]
> <span data-ttu-id="10709-125">È possibile assegnare una classificazione basata sui dati dei clienti solo ai contatti registrati come clienti e una classificazione basata sui dati dei fornitori solo ai contatti registrati come fornitori.</span><span class="sxs-lookup"><span data-stu-id="10709-125">Only contacts that are recorded as customers can be assigned a classification based on customer data and only contacts that are recorded as vendors can be assigned a classification based on vendor data.</span></span> <span data-ttu-id="10709-126">La classificazione automatica non viene aggiornata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="10709-126">The automatic classification is not updated automatically.</span></span> <span data-ttu-id="10709-127">Si consiglia pertanto di aggiornare i questionari profilo una volta effettuato l'aggiornamento dei dati relativi a clienti, fornitori o contatti su cui tali questionari si basano.</span><span class="sxs-lookup"><span data-stu-id="10709-127">Consequently, you may want to update the profile questionnaires, after you have updated the customer, vendor or contact data they are based on.</span></span>  

<span data-ttu-id="10709-128">Dopo avere impostato le domande relative al profilo, se si assegna il questionario profilo a un contatto, le risposte corrette relative a tale contatto vengono assegnate automaticamente da [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="10709-128">After you have set up automatically answered profile questions, if you assign the profile questionnaire containing these questions to a contact, [!INCLUDE[d365fin](includes/d365fin_md.md)] will automatically assign the right answers for the contact.</span></span>  

## <a name="example"></a><span data-ttu-id="10709-129">Esempio</span><span class="sxs-lookup"><span data-stu-id="10709-129">Example</span></span>
<span data-ttu-id="10709-130">È possibile classificare i contatti in base al volume di acquisti da essi effettuati:</span><span class="sxs-lookup"><span data-stu-id="10709-130">You can classify your contacts according to how much they bought from you:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="10709-131"><strong>Risposta</strong></span><span class="sxs-lookup"><span data-stu-id="10709-131"><strong>Answer</strong></span></span></th>
<th><span data-ttu-id="10709-132"><strong>Si applica a</strong></span><span class="sxs-lookup"><span data-stu-id="10709-132"><strong>Applies to</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="10709-133">A</span><span class="sxs-lookup"><span data-stu-id="10709-133">A</span></span></p></td>
<td><p><span data-ttu-id="10709-134">contatti che hanno effettuato acquisti per 500.000 VL o più</span><span class="sxs-lookup"><span data-stu-id="10709-134">contacts who bought for 500,000 LCY or more</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10709-135">B</span><span class="sxs-lookup"><span data-stu-id="10709-135">B</span></span></p></td>
<td><p><span data-ttu-id="10709-136">contatti che hanno effettuato acquisti per un importo compreso tra 100.000 e 499.999 VL</span><span class="sxs-lookup"><span data-stu-id="10709-136">contacts who bought for 100,000 up to 499,999 LCY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10709-137">C</span><span class="sxs-lookup"><span data-stu-id="10709-137">C</span></span></p></td>
<td><p><span data-ttu-id="10709-138">contatti che hanno effettuato acquisti per 99.999 VL o meno</span><span class="sxs-lookup"><span data-stu-id="10709-138">contacts who bought for 99,999 LCY or less</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="10709-139">Per effettuare questa operazione, completare la finestra **Setup Questionario Profilo** nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="10709-139">To do this, fill in the **Profile Questionnaire Setup** window as follows:</span></span>


<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="10709-140"><strong>Tipo</strong></span><span class="sxs-lookup"><span data-stu-id="10709-140"><strong>Type</strong></span></span></th>
<th><span data-ttu-id="10709-141"><strong>Descrizione</strong></span><span class="sxs-lookup"><span data-stu-id="10709-141"><strong>Description</strong></span></span></th>
<th><span data-ttu-id="10709-142"><strong>Classificazione Automatica</strong></span><span class="sxs-lookup"><span data-stu-id="10709-142"><strong>Automatic Classification</strong></span></span></th>
<th><span data-ttu-id="10709-143"><strong>Da Valore</strong></span><span class="sxs-lookup"><span data-stu-id="10709-143"><strong>From Value</strong></span></span></th>
<th><span data-ttu-id="10709-144"><strong>A Valore</strong></span><span class="sxs-lookup"><span data-stu-id="10709-144"><strong>To Value</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="10709-145">Domanda</span><span class="sxs-lookup"><span data-stu-id="10709-145">Question</span></span></p></td>
<td><p><span data-ttu-id="10709-146">Classificazione di ABC</span><span class="sxs-lookup"><span data-stu-id="10709-146">ABC Classification</span></span></p></td>
<td><p><span data-ttu-id="10709-147">Fare clic per inserire un segno di spunta</span><span class="sxs-lookup"><span data-stu-id="10709-147">Click to insert a check mark</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10709-148">Risposta</span><span class="sxs-lookup"><span data-stu-id="10709-148">Answer</span></span></p></td>
<td><p><span data-ttu-id="10709-149">A</span><span class="sxs-lookup"><span data-stu-id="10709-149">A</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="10709-150">500.000</span><span class="sxs-lookup"><span data-stu-id="10709-150">500,000</span></span></p></td>
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10709-151">Risposta</span><span class="sxs-lookup"><span data-stu-id="10709-151">Answer</span></span></p></td>
<td><p><span data-ttu-id="10709-152">B</span><span class="sxs-lookup"><span data-stu-id="10709-152">B</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="10709-153">100.000</span><span class="sxs-lookup"><span data-stu-id="10709-153">100,000</span></span></p></td>
<td><p><span data-ttu-id="10709-154">499.999</span><span class="sxs-lookup"><span data-stu-id="10709-154">499,999</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10709-155">Risposta</span><span class="sxs-lookup"><span data-stu-id="10709-155">Answer</span></span></p></td>
<td><p><span data-ttu-id="10709-156">C</span><span class="sxs-lookup"><span data-stu-id="10709-156">C</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="10709-157">99.999</span><span class="sxs-lookup"><span data-stu-id="10709-157">99,999</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="10709-158">Compilare la finestra **Dettagli domande profilo** nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="10709-158">Then fill in the **Profile Question Details** window as follows:</span></span>
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="10709-159"><strong>Campo</strong></span><span class="sxs-lookup"><span data-stu-id="10709-159"><strong>Field</strong></span></span></th>
<th><span data-ttu-id="10709-160"><strong>Valore</strong></span><span class="sxs-lookup"><span data-stu-id="10709-160"><strong>Value</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="10709-161"><strong>Campo Classificazione clienti</strong></span><span class="sxs-lookup"><span data-stu-id="10709-161"><strong>Customer Classification Field</strong></span></span></td>
<td><span data-ttu-id="10709-162"><emphasis>Vendite (VL)</emphasis></span><span class="sxs-lookup"><span data-stu-id="10709-162"><emphasis>Sales (LCY)</emphasis></span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10709-163"><strong>Metodo di classificazione</strong></span><span class="sxs-lookup"><span data-stu-id="10709-163"><strong>Classification Method</strong></span></span></td>
<td><span data-ttu-id="10709-164"><emphasis>Valore Definito</emphasis></span><span class="sxs-lookup"><span data-stu-id="10709-164"><emphasis>Defined Value</emphasis></span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="10709-165">Quando si assegna il questionario profilo contenente questa domanda a un contatto, la risposta pertinente al contatto viene automaticamente inserita nelle righe profilo della scheda del contatto.</span><span class="sxs-lookup"><span data-stu-id="10709-165">When you assign the profile questionnaire containing this question to a contact, the program automatically enters the relevant answer for this contact on the profile lines of the contact card.</span></span>

## <a name="see-also"></a><span data-ttu-id="10709-166">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="10709-166">See Also</span></span>
[<span data-ttu-id="10709-167">Creazione di contatti</span><span class="sxs-lookup"><span data-stu-id="10709-167">Creating Contact Persons</span></span>](marketing-create-contact-persons.md)  
[<span data-ttu-id="10709-168">Creare contatti</span><span class="sxs-lookup"><span data-stu-id="10709-168">Create Contact Persons</span></span>](marketing-how-create-contact-persons.md)  
[<span data-ttu-id="10709-169">Creazione di società contatto</span><span class="sxs-lookup"><span data-stu-id="10709-169">Creating Contact Companies</span></span>](marketing-create-contact-companies.md)  

