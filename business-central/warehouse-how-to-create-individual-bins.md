---
title: 'Procedura: Creare collocazioni | Documenti Microsoft'
description: "Il metodo più efficace per creare le collocazioni della warehouse consiste nel generare gruppi di collocazioni simili nel prospetto di creazione delle collocazioni. È tuttavia possibile creare le collocazioni singolarmente."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 7d5b2ce28f1eaebfca26c2db3801b44ff5278e78
ms.contentlocale: it-it
ms.lasthandoff: 09/28/2018

---
# <a name="create-bins"></a>Creare collocazioni
Il metodo più efficace per creare le collocazioni della warehouse consiste nel generare gruppi di collocazioni simili nel prospetto di creazione collocazioni. È tuttavia possibile creare le collocazioni singolarmente dalla scheda ubicazione. È inoltre possibile utilizzare una funzione nella finestra **Prospetto creaz. collocazione** per creare automaticamente le collocazioni.  

## <a name="to-create-a-bin-from-the-location-card"></a>Per creare una collocazione nella scheda ubicazione  
1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ubicazioni** e scegliere il collegamento correlato.  
2.  Selezionare l'ubicazione da cui si desidera creare una collocazione e scegliere l'azione **Collocazioni**.  
3. Scegliere l'azione **Nuovo**.
4. Compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-create-bins-individually-in-the-bin-creation-worksheet"></a>Per creare singole collocazioni nel prospetto di creazione delle collocazioni  
1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Prospetto creaz. collocazione** e scegliere il collegamento correlato.  
2.  In ciascuna riga, compilare i campi necessari per assegnare un nome e caratteristiche specifiche alle collocazioni che si sta creando.  
3.  Scegliere l'azione **Crea collocazioni**.  

## <a name="to-make-bins-automatically-in-the-bin-creation-worksheet"></a>Per creare collocazioni automaticamente nel prospetto di creazione collocazioni  
Prima di avviare la creazione automatica delle collocazioni, è necessario individuare i generi di collocazione essenziali per le operazioni da eseguire, nonché determinare il percorso più efficiente per il flusso degli articoli attraverso la struttura fisica della warehouse.  

> [!NOTE]  
>  Dopo aver utilizzato una collocazione, non sarà possibile eliminarla a meno che non sia vuota. Se tuttavia si desidera utilizzare un altro sistema di denominazione delle collocazioni, è possibile utilizzare la registrazione di riclassificazione per trasferire gli articoli in un nuovo sistema di collocazioni. Poiché questo processo viene eseguito manualmente e richiede molto tempo, si consiglia di impostare le collocazioni in modo corretto sin dall'inizio.  

Per utilizzare la finestra **Prospetto creaz. collocazione**, è necessario essere impostato come impiegato warehouse nell'ubicazione in cui si trovano le collocazioni. Per ulteriori informazioni, vedere [Impostare impiegati warehouse](warehouse-how-to-set-up-warehouse-employees.md).    

1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Prospetto creaz. collocazione** e quindi scegliere il collegamento correlato.  
2.  Scegliere l'azione **Calcola collocazioni**.
3. Nella finestra **Calcola collocazioni**, nel campo **Codice modello collocazione**, quindi selezionare il modello da utilizzare per le collocazioni che si stanno creando.
4.  Immettere una descrizione per le collocazioni in fase di creazione.  
5.  Per creare i codici di collocazione, compilare i campi **Dal nr.** e **A nr.** delle tre categorie visualizzate nella finestra: **Scaffalatura**, **Sezione** e **Livello**. Il codice di collocazione può contenere un massimo di 20 caratteri.  

    > [!NOTE]  
    >  Il numero di caratteri immesso nei singoli campi per le tre categorie, ad esempio i caratteri immessi nei tre campi **Dal nr.**, più gli eventuali separatori di campo, devono essere 20 o meno.  

     Nel codice è possibile utilizzare lettere per ottenere una combinazione di identificazione alfanumerica, ma in tal caso è necessario immettere le stesse lettere nei campi **Dal nr.** e **A nr.** . È ad esempio possibile definire la parte Scaffalatura del codice come **Dal nr. A01** e **A nr. A10**. Il programma non è impostato per la generazione di codici con sequenze di lettere, ad esempio da A01 a F05.  

6.  Se si desidera utilizzare un carattere, ad esempio il trattino (-), per separare le parti del codice collocazione definite nei campi relativi alle categorie, immettere tale carattere nel campo **Separatore Campo**.  
7.  Se si desidera che non venga automaticamente creata una riga per una collocazione già esistente, selezionare il campo **Controllo su collocazione esistente**.  
8. Al termine della compilazione dei campi, scegliere **OK**.

    Verrà automaticamente creata una riga per ciascuna collocazione nel prospetto. A questo punto, è possibile eliminare alcune collocazioni,ad esempio nel caso in cui si disponga di una scaffalatura con un passaggio attraverso i primi due livelli di una coppia di sezioni.  

9. Dopo avere eliminato tutte le collocazioni non necessarie, scegliere l'azione **Crea collocazioni**. Verranno create automaticamente le collocazioni per ciascuna riga del prospetto.  

Ripetere la procedura per un altro gruppo di collocazioni finché non sono state create tutte le collocazioni desiderate per la warehouse.  

## <a name="see-also"></a>Vedi anche  
[Gestione warehouse](warehouse-manage-warehouse.md)  
[Magazzino](inventory-manage-inventory.md)  
[Impostazione gestione warehouse](warehouse-setup-warehouse.md)     
[Gestione assemblaggio](assembly-assemble-items.md)    
[Dettagli di progettazione: Gestione warehouse](design-details-warehouse-management.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

