---
title: Trasferire articoli tra le warehouse | Documenti Microsoft
description: Viene descritto come spostare il magazzino da un'area o una warehouse a un'altra con le registrazioni di riclassificazione o gli ordini di trasferimento.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: move, warehouse
ms.date: 01/25/2018
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 6f83607606d79d894cbe8f154566b9fe7a65a94c
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="transfer-inventory-between-locations"></a>Trasferire il magazzino tra le ubicazioni
È possibile trasferire articoli di magazzino tra ubicazioni creando ordini di trasferimento. In alternativa, è possibile utilizzare le registrazioni di riclassificazione articoli.

Con gli ordini di trasferimento, si spedisce il trasferimento in uscita da un'ubicazione e si riceve il trasferimento in entrata presso un'altra ubicazione. Ciò consente di gestire le attività di warehouse implicate e offre maggiore certezza che le quantità di magazzino di vengano aggiornate correttamente.

Con la registrazione di riclassificazione, si compila semplicemente i campi **Codice ubicazione** e **Nuovo codice ubicazione**. Quando si contabilizza la registrazione, i movimenti contabili articoli vengono rettificati nelle ubicazioni in questione. Con questo metodo, le attività di warehouse non vengono gestite.

> [!NOTE]  
>   Se sono stati registrati articoli in magazzino senza un codice ubicazione, ad esempio a partire da un periodo in cui era disponibile solo una warehouse, non è possibile trasferire gli articoli tramite ordini di trasferimento. Al contrario, è necessario utilizzare le registrazioni di riclassificazione per riclassificare gli articoli da un codice di un'ubicazione vuota a un codice di ubicazione effettiva.  Per ulteriori informazioni, vedere il passaggio 3 nella sezione "Per trasferire gli articoli con le registrazioni di riclassificazione articolo".

Per trasferire gli articoli, le ubicazioni e i percorsi di trasferimento devono essere impostati. Per ulteriori informazioni, vedere [Impostare le ubicazioni](inventory-how-setup-locations.md).

## <a name="to-transfer-items-with-a-transfer-order"></a>Per trasferire gli articoli con un ordine di trasferimento
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Ordini di trasferimento**, quindi scegliere il collegamento correlato.
2. Nella finestra **Ordine di trasferimento** compilare i campi secondo le necessità. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >   Se i campi **Codice in transito**, **Cod. spedizioniere** e **Servizi spedizioniere** nella finestra **Specifica percorso trasf.** sono stati compilati al momento dell'impostazione del percorso di trasferimento, i dati verranno immessi automaticamente nei campi corrispondenti dell'ordine di trasferimento.

    Se si compila il campo **Servizio spedizioniere**, il programma calcola la data di ricezione nell'ubicazione di trasferimento sommando il tempo di spedizione del servizio spedizioniere alla data di spedizione.

    Come lavoratore warehouse nell'ubicazione da cui viene effettuato il trasferimento, continuare con la spedizione degli articoli.
3. Scegliere l'azione **Registra**, selezionare l'opzione **Spedizione**, quindi il pulsante **OK**.

    Gli articoli sono ora in transito tra le ubicazioni specificate, in base al percorso indicato per il trasferimento.

    Come lavoratore warehouse nell'ubicazione da cui viene effettuato il trasferimento, continuare con la ricezione degli articoli.
4. Scegliere l'azione **Registra**, selezionare l'opzione **Ricevi**, quindi il pulsante **OK**.

## <a name="to-transfer-items-with-the-item-reclassification-journal"></a>Per trasferire gli articoli con le registrazioni di riclassificazione articolo
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Registrazioni riclassificazioni articoli**, quindi scegliere il collegamento correlato.
2. Nella finestra **Batch reg. riclass. articoli** compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Nel campo **Cod. ubicazione** immettere l'ubicazione in cui gli articoli si trovano attualmente.

    > [!NOTE]  
    >   Per trasferire gli articoli che non presentano codice ubicazione, lasciare vuoto il campo **Codice ubicazione**.
4. Nel campo **Nuovo codice ubicazione** immettere l'ubicazione verso cui si intende trasferire gli articoli.
5. Scegliere l'azione **Registra**.

## <a name="see-also"></a>Vedi anche
[Gestire i costi del magazzino](inventory-manage-inventory.md)  
[Impostare le ubicazioni](inventory-how-setup-locations.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Personalizzazione dell'esperienza [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md)  
[Funzionalità aziendali generali](ui-across-business-areas.md)

