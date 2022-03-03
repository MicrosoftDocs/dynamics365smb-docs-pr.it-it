---
title: Trasferire articoli tra le ubicazioni di warehouse
description: Viene descritto come spostare il magazzino da un'area o una warehouse a un'altra con le registrazioni di riclassificazione o gli ordini di trasferimento.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: move, warehouse
ms.search.forms: 5746, 5745, 5759, 5753, 5743, 5758, 5752, 5744, 5749, 5740, 5741, 5742, 5757, 5748, 5747, 9285, 5756, 5755
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: b51bd44099c85ae16498e2f40abc86db7134cb1b
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2022
ms.locfileid: "8148500"
---
# <a name="transfer-inventory-between-locations"></a>Trasferire il magazzino tra le ubicazioni
È possibile trasferire articoli di magazzino tra ubicazioni creando ordini di trasferimento. In alternativa, è possibile utilizzare le registrazioni di riclassificazione articoli.

Con gli ordini di trasferimento, si spedisce il trasferimento in uscita da un'ubicazione e si riceve il trasferimento in entrata presso un'altra ubicazione. Ciò consente di gestire le attività di warehouse implicate e offre maggiore certezza che le quantità di magazzino di vengano aggiornate correttamente.

Con la registrazione di riclassificazione, si compila semplicemente i campi **Codice ubicazione** e **Nuovo codice ubicazione**. Quando si contabilizza la registrazione, i movimenti contabili articoli vengono rettificati nelle ubicazioni in questione. Con questo metodo, le attività di warehouse non vengono gestite.

> [!NOTE]  
>   Se sono stati registrati articoli in magazzino senza un codice ubicazione, ad esempio a partire da un periodo in cui era disponibile solo una warehouse, non è possibile trasferire gli articoli tramite ordini di trasferimento. Al contrario, è necessario utilizzare le registrazioni di riclassificazione per riclassificare gli articoli da un codice di un'ubicazione vuota a un codice di ubicazione effettiva.  Per ulteriori informazioni, vedere il passaggio 3 in [Per trasferire gli articoli con le registrazioni di riclassificazione articolo](inventory-how-transfer-between-locations.md#to-transfer-items-with-the-item-reclassification-journal).

Per trasferire gli articoli, le ubicazioni e i percorsi di trasferimento devono essere impostati. Per ulteriori informazioni, vedere [Impostare le ubicazioni](inventory-how-setup-locations.md).

## <a name="to-transfer-items-with-a-transfer-order"></a>Per trasferire gli articoli con un ordine di trasferimento
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ordini di trasferimento**, quindi scegli il collegamento correlato.
2. Nella pagina **Ordine di trasferimento** compilare i campi secondo le necessità. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >   Se i campi **Codice in transito**, **Cod. spedizioniere** e **Servizi spedizioniere** nella pagina **Specifica percorso trasf.** sono stati compilati al momento dell'impostazione del percorso di trasferimento, i dati verranno immessi automaticamente nei campi corrispondenti dell'ordine di trasferimento.

    Se si compila il campo **Servizio spedizioniere**, il programma calcola la data di ricezione nell'ubicazione di trasferimento sommando il tempo di spedizione del servizio spedizioniere alla data di spedizione.

3. Per compilare le righe, immetterle manualmente o scegliere una delle seguenti opzioni sotto l'azione **Funzioni**:
    - Scegliere l'azione **Ottieni contenuto collocazione** per selezionare elementi esistenti da una specifica collocazione nella posizione.
    - Scegliere **Ottieni righe di carico** per selezionare articoli che sono appena arrivati nell'ubicazione da cui viene effettuato il trasferimento.   

    Come lavoratore warehouse nell'ubicazione da cui viene effettuato il trasferimento, continuare con la spedizione degli articoli.
4. Scegliere l'azione **Registra**, selezionare l'opzione **Spedizione**, quindi il pulsante **OK**.

    Gli articoli sono ora in transito tra le ubicazioni specificate, in base al percorso indicato per il trasferimento.

    Come lavoratore warehouse nell'ubicazione da cui viene effettuato il trasferimento, continuare con la ricezione degli articoli. Le righe degli ordini di trasferimento sono le stesse di quelle spedite e non possono essere modificate.
5. Scegliere l'azione **Registra**, selezionare l'opzione **Ricevi**, quindi il pulsante **OK**.

## <a name="to-transfer-items-with-the-item-reclassification-journal"></a>Per trasferire gli articoli con le registrazioni di riclassificazione articolo
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registrazioni riclass. articoli**, quindi scegli il collegamento correlato.
2. Nella pagina **Batch reg. riclass. articoli** compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Nel campo **Cod. ubicazione** immettere l'ubicazione in cui gli articoli si trovano attualmente.

    > [!NOTE]  
    >   Per trasferire gli articoli che non presentano codice ubicazione, lasciare vuoto il campo **Codice ubicazione**.
4. Nel campo **Nuovo codice ubicazione** immettere l'ubicazione verso cui si intende trasferire gli articoli.
5. Scegliere l'azione **Registra**.

## <a name="see-also"></a>Vedere anche
[Gestire i costi del magazzino](inventory-manage-inventory.md)  
[Impostare le ubicazioni](inventory-how-setup-locations.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Modifica delle funzionalità visualizzate](ui-experiences.md)  
[Funzionalità aziendali generali](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]