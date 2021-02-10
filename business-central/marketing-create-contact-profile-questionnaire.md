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
ms.date: 10/01/2020
ms.openlocfilehash: 65c27bee86d273c467709f1e238b996829d73f37
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/17/2020
ms.locfileid: "4755444"
---
# <a name="use-profile-questionnaires-to-classify-business-contacts"></a><span data-ttu-id="43caf-103">Utilizzare i questionari profilo per classificare i contatti business</span><span class="sxs-lookup"><span data-stu-id="43caf-103">Use Profile Questionnaires to Classify Business Contacts</span></span>
<span data-ttu-id="43caf-104">È possibile impostare questionari profilo da utilizzare durante l'immissione di informazioni sul profilo dei contatti.</span><span class="sxs-lookup"><span data-stu-id="43caf-104">You can set up profile questionnaires that you want to use when entering information about your contacts' profiles.</span></span> <span data-ttu-id="43caf-105">In ogni questionario, è possibile impostare le diverse domande da porre ai contatti.</span><span class="sxs-lookup"><span data-stu-id="43caf-105">Within each questionnaire, you can set up the different questions you intend to ask your contacts.</span></span>  

<span data-ttu-id="43caf-106">È inoltre possibile eseguire il questionario per rispondere automaticamente ad alcune domande sulla base dei dati di contatto, cliente o fornitore.</span><span class="sxs-lookup"><span data-stu-id="43caf-106">You can also run the questionnaire to answer some of the questions based on contact, customer, or vendor data automatically.</span></span>  

## <a name="to-add-a-profile-questionnaire"></a><span data-ttu-id="43caf-107">Per aggiungere un questionario profilo</span><span class="sxs-lookup"><span data-stu-id="43caf-107">To add a profile questionnaire</span></span>
1.  <span data-ttu-id="43caf-108">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup questionario** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="43caf-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Questionnaire Setup**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="43caf-109">Scegliere l'azione **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="43caf-109">Choose the **New** Action.</span></span>  
3.  <span data-ttu-id="43caf-110">Compilare i campi in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="43caf-110">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-add-questions-to-a-profile-questionnaire"></a><span data-ttu-id="43caf-111">Per aggiungere domande a un questionario profilo</span><span class="sxs-lookup"><span data-stu-id="43caf-111">To add questions to a profile questionnaire</span></span>
1.  <span data-ttu-id="43caf-112">Scegliere il questionario profilo pertinente e quindi scegliere l'azione **Modifica setup questionario**.</span><span class="sxs-lookup"><span data-stu-id="43caf-112">Choose the relevant profile questionnaire, and then choose the **Edit Questionnaire Setup** action.</span></span>  
2.  <span data-ttu-id="43caf-113">Sulla prima riga vuota, nel campo **Tipo**, scegliere **Domanda** e digitare la domanda desiderata nel campo **Descrizione**.</span><span class="sxs-lookup"><span data-stu-id="43caf-113">On the first empty line, in the **Type** field, choose **Question** and type your question in the **Description** field.</span></span> <span data-ttu-id="43caf-114">Compilare gli altri campi della riga.</span><span class="sxs-lookup"><span data-stu-id="43caf-114">Fill in the other fields on this line.</span></span>  
3.  <span data-ttu-id="43caf-115">Sulla prima riga vuota successiva nel campo **Tipo**, scegliere **Risposta** e digitare la risposta desiderata nel campo **Descrizione**.</span><span class="sxs-lookup"><span data-stu-id="43caf-115">On the next empty line, in the **Type** field, choose **Answer** and type your answer in the **Description** field.</span></span>  
4.  <span data-ttu-id="43caf-116">Nel campo **Priorità** selezionare la priorità.</span><span class="sxs-lookup"><span data-stu-id="43caf-116">In the **Priority** field, select the priority.</span></span> <span data-ttu-id="43caf-117">Nei campi **Da valore** e **A valore** definire un intervallo di punti.</span><span class="sxs-lookup"><span data-stu-id="43caf-117">In the **From Value** and **To Value** fields, define a point range.</span></span> <span data-ttu-id="43caf-118">I contatti che ricevono punti entro l'intervallo stabilito otterranno la risposta.</span><span class="sxs-lookup"><span data-stu-id="43caf-118">Contacts that receive points within the defined range will get the answer.</span></span>  

<span data-ttu-id="43caf-119">Ripetere tali passaggi per immettere tutte le domande e le risposte nel questionario profilo.</span><span class="sxs-lookup"><span data-stu-id="43caf-119">Repeat these steps to enter all the questions and answers within the profile questionnaire.</span></span>

<span data-ttu-id="43caf-120">Dopo avere creato un questionario, è necessario creare le valutazioni dei contatti per classificare i contatti.</span><span class="sxs-lookup"><span data-stu-id="43caf-120">After you have created a questionnaire, you must create contact ratings to classify your contacts.</span></span> <span data-ttu-id="43caf-121">È inoltre possibile impostare le domande classificate automaticamente in base alle informazioni presenti nella scheda contatto.</span><span class="sxs-lookup"><span data-stu-id="43caf-121">You can also set up questions that are rated automatically based on information in the contact card.</span></span>  

> [!NOTE]
> <span data-ttu-id="43caf-122">Se si immette una domanda con risposta automatica, selezionare <STRONG>Riga</STRONG> e quindi <STRONG>Dettagli domanda</STRONG> per immettere i criteri da utilizzare per fornire la risposta automatica.</span><span class="sxs-lookup"><span data-stu-id="43caf-122">If you enter a question that is automatically answered, choose <STRONG>Line</STRONG>, and then choose <STRONG>Question Details</STRONG>, to enter the criteria to automatically answer the question.</span></span>

## <a name="the-automatic-classification-of-contacts"></a><span data-ttu-id="43caf-123">Classificazione automatica dei contatti</span><span class="sxs-lookup"><span data-stu-id="43caf-123">The Automatic Classification of Contacts</span></span>
<span data-ttu-id="43caf-124">È possibile classificare automaticamente i contatti in base alle informazioni relative a cliente, fornitore e contatto, mediante una serie di domande sul profilo con risposta automatica nella pagina **Setup questionario profilo**.</span><span class="sxs-lookup"><span data-stu-id="43caf-124">You can automatically classify your contacts according to customer, vendor, and contact information, by setting up automatically answered profile questions on the **Profile Questionnaire Setup** page.</span></span>  

> [!NOTE]
> <span data-ttu-id="43caf-125">È possibile assegnare una classificazione basata sui dati dei clienti solo ai contatti registrati come clienti e una classificazione basata sui dati dei fornitori solo ai contatti registrati come fornitori.</span><span class="sxs-lookup"><span data-stu-id="43caf-125">Only contacts that are recorded as customers can be assigned a classification based on customer data and only contacts that are recorded as vendors can be assigned a classification based on vendor data.</span></span> <span data-ttu-id="43caf-126">La classificazione automatica non viene aggiornata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="43caf-126">The automatic classification is not updated automatically.</span></span> <span data-ttu-id="43caf-127">Si consiglia pertanto di aggiornare i questionari profilo una volta effettuato l'aggiornamento dei dati relativi a clienti, fornitori o contatti su cui tali questionari si basano.</span><span class="sxs-lookup"><span data-stu-id="43caf-127">Consequently, you may want to update the profile questionnaires, after you have updated the customer, vendor or contact data they are based on.</span></span>  

<span data-ttu-id="43caf-128">Dopo avere impostato le domande relative al profilo, se si assegna il questionario profilo a un contatto, le risposte corrette relative a tale contatto vengono assegnate automaticamente da [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="43caf-128">After you have set up automatically answered profile questions, if you assign the profile questionnaire containing these questions to a contact, [!INCLUDE[prod_short](includes/prod_short.md)] will automatically assign the right answers for the contact.</span></span>  

## <a name="example"></a><span data-ttu-id="43caf-129">Esempio</span><span class="sxs-lookup"><span data-stu-id="43caf-129">Example</span></span>
<span data-ttu-id="43caf-130">È possibile classificare i contatti in base al volume di acquisti da essi effettuati:</span><span class="sxs-lookup"><span data-stu-id="43caf-130">You can classify your contacts according to how much they bought from you:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="43caf-131"><strong>Risposta</strong></span><span class="sxs-lookup"><span data-stu-id="43caf-131"><strong>Answer</strong></span></span></th>
<th><span data-ttu-id="43caf-132"><strong>Si applica a</strong></span><span class="sxs-lookup"><span data-stu-id="43caf-132"><strong>Applies to</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="43caf-133">A</span><span class="sxs-lookup"><span data-stu-id="43caf-133">A</span></span></p></td>
<td><p><span data-ttu-id="43caf-134">contatti che hanno effettuato acquisti per 500.000 VL o più</span><span class="sxs-lookup"><span data-stu-id="43caf-134">contacts who bought for 500,000 LCY or more</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43caf-135">B</span><span class="sxs-lookup"><span data-stu-id="43caf-135">B</span></span></p></td>
<td><p><span data-ttu-id="43caf-136">contatti che hanno effettuato acquisti per un importo compreso tra 100.000 e 499.999 VL</span><span class="sxs-lookup"><span data-stu-id="43caf-136">contacts who bought for 100,000 up to 499,999 LCY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43caf-137">C</span><span class="sxs-lookup"><span data-stu-id="43caf-137">C</span></span></p></td>
<td><p><span data-ttu-id="43caf-138">contatti che hanno effettuato acquisti per 99.999 VL o meno</span><span class="sxs-lookup"><span data-stu-id="43caf-138">contacts who bought for 99,999 LCY or less</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="43caf-139">Per effettuare questa operazione, completare la pagina **Setup questionario profilo** nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="43caf-139">To do this, fill on the **Profile Questionnaire Setup** page as follows:</span></span>


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
<th><span data-ttu-id="43caf-140"><strong>Tipo</strong></span><span class="sxs-lookup"><span data-stu-id="43caf-140"><strong>Type</strong></span></span></th>
<th><span data-ttu-id="43caf-141"><strong>Descrizione</strong></span><span class="sxs-lookup"><span data-stu-id="43caf-141"><strong>Description</strong></span></span></th>
<th><span data-ttu-id="43caf-142"><strong>Classificazione Automatica</strong></span><span class="sxs-lookup"><span data-stu-id="43caf-142"><strong>Automatic Classification</strong></span></span></th>
<th><span data-ttu-id="43caf-143"><strong>Da Valore</strong></span><span class="sxs-lookup"><span data-stu-id="43caf-143"><strong>From Value</strong></span></span></th>
<th><span data-ttu-id="43caf-144"><strong>A Valore</strong></span><span class="sxs-lookup"><span data-stu-id="43caf-144"><strong>To Value</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="43caf-145">Domanda</span><span class="sxs-lookup"><span data-stu-id="43caf-145">Question</span></span></p></td>
<td><p><span data-ttu-id="43caf-146">Classificazione di ABC</span><span class="sxs-lookup"><span data-stu-id="43caf-146">ABC Classification</span></span></p></td>
<td><p><span data-ttu-id="43caf-147">Fare clic per inserire un segno di spunta</span><span class="sxs-lookup"><span data-stu-id="43caf-147">Click to insert a check mark</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43caf-148">Risposta</span><span class="sxs-lookup"><span data-stu-id="43caf-148">Answer</span></span></p></td>
<td><p><span data-ttu-id="43caf-149">A</span><span class="sxs-lookup"><span data-stu-id="43caf-149">A</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="43caf-150">500.000</span><span class="sxs-lookup"><span data-stu-id="43caf-150">500,000</span></span></p></td>
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43caf-151">Risposta</span><span class="sxs-lookup"><span data-stu-id="43caf-151">Answer</span></span></p></td>
<td><p><span data-ttu-id="43caf-152">B</span><span class="sxs-lookup"><span data-stu-id="43caf-152">B</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="43caf-153">100,000</span><span class="sxs-lookup"><span data-stu-id="43caf-153">100,000</span></span></p></td>
<td><p><span data-ttu-id="43caf-154">499,999</span><span class="sxs-lookup"><span data-stu-id="43caf-154">499,999</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43caf-155">Risposta</span><span class="sxs-lookup"><span data-stu-id="43caf-155">Answer</span></span></p></td>
<td><p><span data-ttu-id="43caf-156">C</span><span class="sxs-lookup"><span data-stu-id="43caf-156">C</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="43caf-157">99,999</span><span class="sxs-lookup"><span data-stu-id="43caf-157">99,999</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="43caf-158">Compilare la pagina **Dettagli domande profilo** nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="43caf-158">Then fill on the **Profile Question Details** page as follows:</span></span>
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="43caf-159"><strong>Campo</strong></span><span class="sxs-lookup"><span data-stu-id="43caf-159"><strong>Field</strong></span></span></th>
<th><span data-ttu-id="43caf-160"><strong>Valore</strong></span><span class="sxs-lookup"><span data-stu-id="43caf-160"><strong>Value</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="43caf-161"><strong>Campo Classificazione clienti</strong></span><span class="sxs-lookup"><span data-stu-id="43caf-161"><strong>Customer Classification Field</strong></span></span></td>
<td><span data-ttu-id="43caf-162"><emphasis>Vendite (VL)</emphasis></span><span class="sxs-lookup"><span data-stu-id="43caf-162"><emphasis>Sales (LCY)</emphasis></span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43caf-163"><strong>Metodo di classificazione</strong></span><span class="sxs-lookup"><span data-stu-id="43caf-163"><strong>Classification Method</strong></span></span></td>
<td><span data-ttu-id="43caf-164"><emphasis>Valore Definito</emphasis></span><span class="sxs-lookup"><span data-stu-id="43caf-164"><emphasis>Defined Value</emphasis></span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="43caf-165">Quando si assegna il questionario profilo contenente questa domanda a un contatto, la risposta pertinente al contatto viene automaticamente inserita nelle righe profilo della scheda del contatto.</span><span class="sxs-lookup"><span data-stu-id="43caf-165">When you assign the profile questionnaire containing this question to a contact, application automatically enters the relevant answer for this contact on the profile lines of the contact card.</span></span>

## <a name="see-also"></a><span data-ttu-id="43caf-166">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="43caf-166">See Also</span></span>
[<span data-ttu-id="43caf-167">Creazione di contatti</span><span class="sxs-lookup"><span data-stu-id="43caf-167">Creating Contacts</span></span>](marketing-create-contact-companies.md)  
