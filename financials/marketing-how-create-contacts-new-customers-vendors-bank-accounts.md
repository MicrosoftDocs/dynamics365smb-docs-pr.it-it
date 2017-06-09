---
title: Creare un cliente, un fornitore o un conto corrente bancario da un contatto | Documenti Microsoft
description: Viene descritto come creare un cliente, un fornitore o un conto corrente bancario da un contatto in Financials
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, client, prospect
ms.date: 02/28/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 6ecbc24e447917e6316b0579fa8c3ee046e73915
ms.contentlocale: it-it
ms.lasthandoff: 05/04/2017


---
# <a name="create-a-customer-vendor-or-bank-account-from-a-contact"></a>Per creare un contatto da un cliente, un fornitore o un conto corrente bancario
È possibile registrare alcuni contatti come clienti, fornitori oppure conti correnti bancari esistenti. La creazione di un cliente, un fornitore o un conto bancario da un contatto consente di utilizzare i dati esistenti. Quando si crea un cliente, un fornitore o un conto bancario in questo modo, le informazioni verranno sincronizzate con il contatto. La sincronizzazione rende uguali le informazioni comuni tra i contatti e clienti, fornitori o conti bancari.

Prima di poter registrare i contatti in questo modo, è necessario specificare un codice relazione d'affari per clienti, fornitori e conti correnti bancari nella finestra **Setup marketing**. Se verranno registrati i contatti come conti bancari, sarà necessario specificare anche la serie di numeri di conti correnti bancari nella finestra **Setup contabilità generale**.

## <a name="to-create-a-contact-as-a-customer-vendor-or-bank-account"></a>Per creare un contatto come cliente, fornitore o conto corrente bancario.
1. Nell'angolo superiore destro scegliere l'icona **Cerca pagina o report** ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), inserire **Contatti**, quindi scegliere il collegamento correlato.
2. Selezionare il contatto che si desidera creare come cliente, fornitore o conto corrente bancario.
3. Scegliere l'azione **Crea come**, quindi scegliere **Cliente**, **Fornitore** oppure **C.to/corrente**.
4. Scegliere Sì nel messaggio che verrà visualizzato.

Le informazioni di contatto vengono trasferite dalla scheda **Contatto** alla scheda **C/C bancario**, alla scheda **Cliente** o alla scheda **Fornitore**. È possibile aggiungere informazioni specifiche a ciascuna delle schede, ad esempio dettagli di pagamento e fatturazione.

## <a name="see-also"></a>Vedi anche
[Procedura: Creare società contatto](marketing-create-contact-companies.md)  
[Procedura: Creare contatti](marketing-create-contact-persons.md)  
[Setup Relationship Management](marketing-setup-marketing.md)  
[Sincronizzazione di contatti con clienti, fornitori e conti correnti bancari](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[Procedura: Collegare i contatti con clienti, fornitori o conti correnti bancari esistenti](marketing-how-link-contact.md)  
[Assegnare relazioni d'affari ai contatti](marketing-business-relations.md#AssignBusRelContact)  
[Utilizzo di dati finanziari](ui-work-product.md)

