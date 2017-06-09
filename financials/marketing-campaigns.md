---
title: Impostazione di campagne di marketing in Financials | Documenti Microsoft
description: "Viene descritto come è possibile impostare e svolgere campagne di marketing in Dynamics 365 for Financials"
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, campaign, promo, prospect
ms.date: 03/08/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 8f616382e28e29aab1ce7d9b45b8efb4ad374b96
ms.contentlocale: it-it
ms.lasthandoff: 05/04/2017


---
# <a name="managing-marketing-campaigns"></a>Gestione di campagne di marketing
Per identificare, attirare e fidelizzare i clienti, è fondamentale mettere a punto un solido piano di marketing. Un piano di marketing comprende diverse campagne e altre interazioni correlate alle attività di marketing e di vendita. Quando si pianifica una campagna, è necessario decidere a quali contatti rivolgersi, quale tipo di campagna creare (fiera commerciale o messaggi e-mail) e a quali agenti assegnare ogni task.

<!-- Each campaign consists of various activities or to-dos. Activities are large tasks that can be broken down into several smaller tasks or to-dos. To-dos are individual or team tasks that can be created within activities or individually and then be assigned to individual salespeople or groups of salespeople.-->

## <a name="defining-individual-campaigns"></a>Definizione di campagne singole
Prima di creare una campagna, è necessario impostare *codici di stato campagna*. L'utilizzo di questi codici consente di gestire le campagne assegnando ad esse uno stato. Lavorando alle diverse fasi della campagna, sarà possibile sapere i passaggi completati e quelli ancora da iniziare. I codici stato campagna vengono impostati nella finestra **Stato campagna**.

È possibile creare una *scheda campagna* per ogni campagna di cui tenere traccia. È anche possibile visualizzare queste schede campagna per visualizzare informazioni generali su ogni campagna.
È possibile eliminare movimenti campagna, come se il movimento registrasse un'azione che è stata annullata. È possibile eliminare solo movimenti campagna annullati.

### <a name="selecting-the-target-audience"></a>Selezione del target
Dopo avere creato una campagna, è possibile iniziare a creare segmenti che specifichino il target della campagna. Per ulteriori informazioni, vedere [Gestione dei segmenti](marketing-segments.md).

### <a name="registering-discount-percentages"></a>Registrazione delle percentuali di sconto
Dopo avere impostato la campagna, avere stabilito quali segmenti coprirà la campagna e avere impostato la data di inizio e la data di fine, sarà possibile registrare la percentuale di sconto che verrà applicata al cliente per i singoli articoli nelle righe della finestra **Sconti riga vendita**. È inoltre possibile registrare prezzi di vendita dei singoli articoli nelle righe della finestra **Prezzi vendita**. È possibile accedere a entrambe le finestre dalla scheda campagna.

 Una volta impostati i prezzi di vendita e gli sconti riga, nonché i segmenti nella Scheda Campagna, è necessario attivarli in modo che i prezzi e gli sconti vengano riportati anche nelle righe.

> [!NOTE]  
>  Per attivare i prezzi di vendita/ gli sconti riga, è necessario specificare se l'intero segmento o solo alcuni contatti sono obiettivi della campagna. Se i prezzi di vendita e gli sconti riga riguardano tutti i contatti del segmento, selezionare il campo **Target campagna** disponibile nella Scheda dettaglio **Campagna** della scheda **Segmento**.
Se i prezzi di vendita/gli sconti riga non vengono offerti a tutti i contatti del segmento, è possibile deselezionare il campo **Target campagna** per i contatti specifici. Se non è possibile visualizzare questo campo, è possibile aggiungerlo alla vista. Per ulteriori informazioni, vedere [Personalizzazione utente](ui-user-personalization.md).

<!-- ## Conducting campaigns
As a campaign runs, all interactions with your contacts, or segment, are recorded so that you can get statistics and other information about the costs and success rates of the campaign.

Campaigns are conducted by salespeople, and you must create activities to represent each task and assign them to the relevant salespeople.  -->

## <a name="see-also"></a>Vedi anche
[Gestione dei contatti](marketing-contacts.md)  
[Gestione dei segmenti](marketing-segments.md)  
[Gestione delle opportunità di vendita](marketing-manage-sales-opportunities.md)  
[Utilizzo di dati finanziari](ui-work-product.md)  

