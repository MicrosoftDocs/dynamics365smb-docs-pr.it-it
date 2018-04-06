---
title: Definizione della allocazioni statiche in base al rapporto di allocazione | Microsoft Docs
description: "Il metodo di allocazione statica è basato su un valore definito, ad esempio i metri quadri utilizzati, o su un rapporto di allocazione stabilito, quale 5:2:4."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 8b4d26e3cb8a1364745dd25ca5341635c49a5718
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="scenario-example-defining-static-allocations-based-on-allocation-ratio"></a>Esempio dello scenario: definizione della allocazioni statiche in base al rapporto di allocazione
Il metodo di allocazione statica è basato su un valore definito, ad esempio i metri quadri utilizzati, o su un rapporto di allocazione stabilito, quale 5:2:4.  

In questo argomento viene descritto come definire i tre nuovi oggetti di costo di destinazione di allocazione per il centro di costo PROD di origine di allocazione utilizzando il rapporto di allocazione stabilito 5:2:4. I tre oggetti di costo di destinazione sono ACCESSORI, VERNICE e ARREDI.  

> [!NOTE]  
>  Nell'esempio vengono utilizzati i dati di esempio di [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="to-define-the-allocation-source-prod-cost-center-on-the-general-fasttab"></a>Per definire il centro di costo PROD di origine di allocazione nella Scheda dettaglio Generale  

1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Allocazione costi**, quindi scegliere il collegamento correlato.  
2.  Nella finestra **Allocazione costi** scegliere l'azione **Nuovo**.  
3.  Nel campo **ID** premere INVIO o immettere un ID.  
4.  Nel campo **Livello** immettere **1**.  
5.  Nei campi **Data di inizio validità** e **Data di fine validità**, immettere le date appropriate.  
6.  Nel campo **Codice centro di costo** immettere **PROD**.  
7.  Nel campo **Importo dare in tipo di costo** immettere il tipo di costo **9903**.  

## <a name="to-define-the-allocation-target-cost-objects-on-the-lines-fasttab"></a>Per definire gli oggetti di costo di destinazione di allocazione nella Scheda dettaglio Righe  

1.  Nel campo **Tipo di costo di destinazione** della prima riga immettere **9903**.  
2.  Nel campo **Oggetto di costo di destinazione** della prima riga selezionare **ACCESSO**.  
3.  Nella prima riga nel campo **Tipo di destinazione allocazione** selezionare **Tutti i costi** per definire la modalità di allocazione di tutti i costi sospesi.  
4.  Nella prima riga nel campo **Base** selezionare **Statica** per utilizzare il metodo di allocazione statica.  
5.  Nella prima riga nel campo **Quota** immettere il rapporto di allocazione **5**.  
6.  Nel campo **Tipo di costo di destinazione** della seconda riga immettere **9903**.  
7.  Nel campo **Oggetto di costo di destinazione** della seconda riga selezionare **VERNICE**.  
8.  Nella seconda riga nel campo **Tipo di destinazione allocazione** selezionare **Tutti i costi** per definire la modalità di allocazione di tutti i costi sospesi.  
9. Nella seconda riga nel campo **Base** selezionare **Statica** per utilizzare il metodo di allocazione statica.  
10. Nella seconda riga nel campo **Quota** immettere il rapporto di allocazione **2**.  
11. Nel campo **Tipo di costo di destinazione** della terza riga immettere **9903**.  
12. Nel campo **Oggetto di costo di destinazione** della terza riga selezionare **ARREDI**.  
13. Nella terza riga nel campo **Tipo di destinazione allocazione** selezionare **Tutti i costi** per definire la modalità di allocazione di tutti i costi sospesi.  
14. Nella terza riga nel campo **Base** selezionare **Statica** per utilizzare il metodo di allocazione statica.  
15. Nella terza riga nel campo **Quota** immettere il rapporto di allocazione **4**.  

> [!IMPORTANT]  
>  In [!INCLUDE[d365fin](includes/d365fin_md.md)] il campo **Percentuale** viene calcolato automaticamente utilizzando un tasso percentuale che dipende da tutti e tre i rapporti di allocazione immessi nel campo **Quota**  per tutte e tre le righe.  

## <a name="see-also"></a>Vedi anche  
[Impostare origini e destinazioni dell'allocazione](finance-how-to-set-up-allocation-source-and-targets.md)   
[Definizione e allocazione dei costi](finance-define-and-allocate-costs.md)   
[Esempio di scenario: definizione delle allocazioni dinamiche in base agli articoli venduti](finance-scenario-example-defining-dynamic-allocations-based-on-items-sold.md)   
[Definizione e allocazione dei costi](finance-define-and-allocate-costs.md)

