---
title: Creare un cliente o un fornitore da un contatto| Documenti Microsoft
description: "Si può registrare un contatto esistente come cliente, fornitore o conto corrente bancario utilizzando i dati esistenti e specificando la relazione d'affari."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, client, prospect
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 07c56f109ee2e4c348c0f654ceadc4018174c0d5
ms.contentlocale: it-it
ms.lasthandoff: 09/28/2018

---
# <a name="create-a-customer-vendor-or-bank-account-from-a-contact"></a>Per creare un contatto da un cliente, un fornitore o un conto corrente bancario
È possibile registrare alcuni contatti come clienti, fornitori oppure conti correnti bancari esistenti. La creazione di un cliente, un fornitore o un conto bancario da un contatto consente di utilizzare i dati esistenti. Quando si crea un cliente, un fornitore o un conto bancario in questo modo, le informazioni verranno sincronizzate con il contatto. La sincronizzazione rende uguali le informazioni comuni tra i contatti e clienti, fornitori o conti bancari.

Prima di poter registrare i contatti in questo modo, è necessario specificare un codice relazione d'affari per clienti, fornitori e conti correnti bancari nella finestra **Setup marketing**. Se verranno registrati i contatti come conti bancari, sarà necessario specificare anche la serie di numeri di conti correnti bancari nella finestra **Setup contabilità generale**.

## <a name="to-create-a-contact-as-a-customer-vendor-or-bank-account"></a>Per creare un contatto come cliente, fornitore o conto corrente bancario.
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Contatti** e quindi scegliere il collegamento correlato.
2. Selezionare il contatto che si desidera creare come cliente, fornitore o conto corrente bancario.
3. Scegliere l'azione **Crea come**, quindi scegliere **Cliente**, **Fornitore** oppure **C.to/corrente**.
4. Scegliere Sì nel messaggio che verrà visualizzato.

Le informazioni di contatto vengono trasferite dalla scheda **Contatto** alla scheda **C/C bancario**, alla scheda **Cliente** o alla scheda **Fornitore**. È possibile aggiungere informazioni specifiche a ciascuna delle schede, ad esempio dettagli di pagamento e fatturazione.

## <a name="see-also"></a>Vedi anche
[Creare società contatto](marketing-create-contact-companies.md)  
[Creare contatti](marketing-create-contact-persons.md)  
[Setup Relationship Management](marketing-setup-marketing.md)  
[Sincronizzazione di contatti con clienti, fornitori e conti correnti bancari](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[Collegare i contatti con clienti, fornitori o conti correnti bancari esistenti](marketing-how-link-contact.md)  
[Assegnare relazioni d'affari ai contatti](marketing-business-relations.md#AssignBusRelContact)  
[Utilizzo di Business Central](ui-work-product.md)

