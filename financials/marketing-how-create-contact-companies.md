---
title: "Creare società contatto| Documenti Microsoft"
description: "Descrive come creare un contatto per ogni società nuova o potenziale con cui si interagisce o si hanno relazioni."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: ed0f75f1e0ee8a282b58458e4fed3b4eef7c46fb
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="create-contact-companies"></a>Creare società contatto
È possibile creare un contatto per ogni nuova società con cui si interagisce, ad esempio cliente, fornitore, potenziale cliente, banca, studio legale, consulente e così via.

Esistono due modi per creare un contatto: da zero o da un cliente, un fornitore o da un conto corrente bancario esistente.

Prima di creare un contatto, si consiglia di verificare le impostazioni nella finestra **Setup marketing**. Per ulteriori informazioni, vedere [Setup Relationship Management](marketing-setup-marketing.md).

## <a name="create-a-company-contact-from-scratch"></a>Creare una società contatto da zero
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Contatti**, quindi scegliere il collegamento correlato.
2. Scegliere l'azione **Nuovo**.
3. Nel campo **Nr. campo** inserire un numero per il contatto.

    In alternativa, se è stata impostata una numerazione per i contatti nella finestra **Setup marketing**, è possibile premere INVIO per selezionare il successivo numero di contatto disponibile.  
4. Impostare il **Tipo** su **Società**.
5. Compilare gli altri campi come necessario.

## <a name="to-create-a-company-contact-from-a-customer-vendor-or-bank-account"></a>Per creare un contatto per una società da un cliente, fornitore o conto corrente bancario
Se è già stato impostato un numero di clienti, fornitori e conti correnti bancari, è possibile creare contatti sulla base dei dati esistenti. Quando si crea un contatto in questo modo, le informazioni di contatto verranno sincronizzate con clienti, fornitori, o le informazioni del conto corrente bancario.

> [!NOTE]  
>   Prima di creare la società contatto in questo modo, è necessario specificare un codice relazione d'affari per clienti, fornitori e conti correnti bancari nella finestra **Setup marketing**. Se verranno creati i contatti da conti bancari, sarà necessario specificare anche la serie di numeri di conti correnti bancari nella finestra **Setup contabilità generale**.

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report") e immettere una delle seguenti opzioni, in base a dove si desidera creare contatti, quindi selezionare il collegamento correlato.
   * **Crea contatti da clienti**
   * **Crea contatti da fornitori**
   * **Crea contatti da conti correnti bancari**
2. Nella finestra del processo batch che si apre, nella sezione **Cliente**, **Fornitore** o **Conti correnti bancari**, impostare i filtri se si desidera creare contatti rispettivamente da clienti, fornitori o conti correnti bancari specifici.
3. Scegliere **OK** per avviare la creazione di contatti.

    Ai nuovi contatti verranno assegnati numeri contatto successivi all'interno della numerazione. Ai nuovi contatti creati verrà assegnata la relazione d'affari per i fornitori specificata nella finestra **Setup marketing**.

> [!TIP]  
>   È anche possibile creare un cliente, fornitore o conto corrente bancario da un contatto. Per ulteriori informazioni, vedere [Creare un un cliente, un fornitore o un conto corrente bancario da un contatto](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).

## <a name="see-also"></a>Vedi anche
[Sincronizzazione di contatti con clienti, fornitori e conti correnti bancari](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[Assegnare relazioni d'affari ai contatti](marketing-business-relations.md#AssignBusRelContact)  
[Assegnare settori industriali a un contatto](marketing-industry-groups.md#AssignIndustryGroupContact)  
[Assegnare gruppi di mailing a un contatto](marketing-mailing-groups.md#AssignMailGroupContact)  
[Creare contatti](marketing-create-contact-persons.md)  
[Utilizzo di Finance and Operations, Business edition](ui-work-product.md)

