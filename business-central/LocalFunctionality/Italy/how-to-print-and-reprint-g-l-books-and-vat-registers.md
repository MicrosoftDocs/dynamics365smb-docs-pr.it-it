---
title: 'Procedura: Stampare e ristampare i libri giornale e i registri IVA'
description: Le autorità fiscali richiedono l'invio di due report fiscali che elencano tutti i movimenti contabili registrati, i report Libro giornale - Stampa e Registro IVA - Stampa.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 16f91d58ea3690aed279ceb8f6a7487705a4abe6
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3919985"
---
# <a name="print-and-reprint-gl-books-and-vat-registers"></a>Stampare e ristampare i libri giornale e i registri IVA
Le autorità fiscali richiedono l'invio di due report fiscali che elencano tutti i movimenti contabili registrati, i report **Libro giornale - Stampa** e **Registro IVA - Stampa**. Ogni pagina stampata deve avere un proprio numero progressive e pertanto è necessario aggiornare [!INCLUDE[d365fin](../../includes/d365fin_md.md)] con il numero dell'ultima pagina stampata prima di eseguire nuovamente il report.  

Di seguito viene descritto come stampare o ristampare il report **Libro giornale - Stampa**, ma gli stessi passaggi si applicano per la stampa o la ristampa del report **Registro IVA - Stampa**.  

## <a name="to-print-the-general-ledger-book-report"></a>Per stampare il report libro giornale  

1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Libro giornale - Stampa** e quindi scegliere il collegamento correlato.  
2.  Compilare i campi come indicato nella tabella seguente.  

    |Campo|Description|  
    |---------------------------------|---------------------------------------|  
    |**Tipo report**|Selezionare il tipo di report da creare.<br /><br /> Se si seleziona **Ristampa**, il campo **Da Nr. progressivo** si abilita automaticamente.|  
    |**Data Inizio**|Immettere la data iniziale del periodo a partire dal quale i movimenti registrati verranno visualizzati.|  
    |**Data Fine**|Immettere la data finale del periodo a partire dal quale i movimenti registrati verranno visualizzati.|  
    |**Da Nr. progressivo**|Indica il numero progressivo del report.|  
    |**Stampa informazioni società**|Selezionare per stampare le informazioni della società nel report.<br /><br /> I campi restanti sono popolati in base alla pagina **Informazioni società**.|  

    Quando si stampa il report, viene visualizzato un promemoria per aggiornare la pagina **Setup contabilità generale** con il numero dell'ultima pagina.  

    > [!IMPORTANT]  
    >  [!INCLUDE[d365fin](../../includes/d365fin_md.md)] non salva automaticamente il numero di pagina quando si esegue il report. Una volta eseguito il report Libro giornale - Stampa o il report Registro IVA - Stampa, è necessario aggiornare [!INCLUDE[d365fin](../../includes/d365fin_md.md)] con il numero dell'ultima pagina stampata.  

3.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup contabilità generale** e quindi scegliere il collegamento correlato.  

    Per impostare il numero dell'ultima pagina stampata per il report registro IVA, cercare **Registro IVA** e scegliere il collegamento per la pagina in **Categorie reg. IVA**.  

4.  Nella Scheda dettaglio **Stampe Fiscali**, nel campo **Ultima pag. libro giornale stampata**, specificare il numero dell'ultima pagina del report **Libro giornale - Stampa** appena stampato.  

Entrambi i report ufficiali possono essere ristampati. Quando si ristampa un report, la prima pagina del report deve avere lo stesso numero di pagina del report stampato la prima volta. Se si desidera ristampare uno di questi report e il numero di pagina non è corretto, modificare le informazioni di ristampa per il report  

Di seguito viene descritto come visualizzare o modificare la numerazione della pagina per le versioni precedentemente stampate del report **Libro giornale - Stampa**, ma gli stessi passaggi si applicano per il report **Registro IVA - Stampa**.  

## <a name="to-view-or-change-page-numbering-for-reprinting-the-general-ledger-book-report"></a>Per visualizzare o modificare la numerazione della pagina per la ristampa del report libro contabile  

1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup contabilità generale** e quindi scegliere il collegamento correlato.  
2.  Scegliere l'azione **Modifica informazioni ristampa libro giornale** . Nella pagina **Informazioni ristampa libro giornale**, il campo **Numero prima pagina** indica il numero della prima pagina dei report precedentemente stampati.  

Quando si aggiorna la pagina **Setup contabilità generale** o **Registri IVA** con il numero dell'ultima pagina del report stampato, accertarsi di specificare il numero di pagina corretto. Se il report ristampato inizia con il numero di pagina non corretto, il report non verrà accettato dalle autorità fiscali. La pagina **Informazioni ristampa libro giornale** e **Informazioni ristampa registro IVA** facilitano l'identificazione del numero corretto di pagina.  

## <a name="see-also"></a>Vedere anche  
[Funzionalità locale per l'Italia](italy-local-functionality.md)
