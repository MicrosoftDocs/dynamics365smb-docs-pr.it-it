---
title: 'Procedura: Impostazione di definizioni e batch di registrazioni'
description: Tutte le società dell'Unione Europea (UE) sono tenute e presentare dichiarazioni Intrastat all'ufficio doganale, indicando in dettaglio le cessioni e gli acquisti intracomunitari relativamente all'anno in corso.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 6e6cb1bfde545fd6ac815c8d5fe4bc01d061a4c2
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5771436"
---
# <a name="set-up-journal-templates-and-batches"></a>Impostazione di definizioni e batch di registrazioni
Tutte le società dell'Unione Europea (UE) sono tenute e presentare dichiarazioni Intrastat all'ufficio doganale, indicando in dettaglio le cessioni e gli acquisti intracomunitari relativamente all'anno in corso. Un report riepilogativo Intrastat viene presentato agli uffici tributari con cadenza mensile, trimestrale o annuale, a seconda dell'entità delle operazioni della società.  

È possibile stampare i report Intrastat nella pagina **Batch reg. Intrastat** in base ai movimenti delle registrazioni Intrastat. I movimenti possono essere inseriti nella registrazione manualmente o mediante un processo batch. Prima di eseguire queste operazioni, è necessario impostare i batch e le definizioni di registrazioni Intrastat.  

## <a name="to-set-up-intrastat-journal-templates"></a>Per impostare definizioni di registrazioni Intrastat  

1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Definizioni registrazioni Intrastat** e quindi scegliere il collegamento correlato.  
2.  Per creare una nuova definizione di registrazione Intrastat, scegliere l'azione **Nuovo**.  
3.  Nella pagina **Def. registrazioni Intrastat** compilare i campi come indicato nella tabella riportata di seguito.  

    |Campo|Description|  
    |---------------------------------|---------------------------------------|  
    |**Nome**|Nome della definizione di registrazione Intrastat. È possibile immettere un massimo di 10 caratteri alfanumerici.|  
    |**Description**|Descrizione della definizione di registrazione Intrastat. È possibile immettere un massimo di 80 caratteri alfanumerici.|  

4.  Scegliere il pulsante **OK**.  

## <a name="to-set-up-intrastat-journal-batches"></a>Per impostare batch di registrazioni Intrastat  

1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Definizioni registrazioni Intrastat** e quindi scegliere il collegamento correlato.  
2.  Per aprire la pagina **Batch reg. Intrastat**, selezionare il modello desiderato, quindi scegliere **Batch**.  
3.  Compilare i campi come indicato nella tabella seguente.  

    |Campo|Description|  
    |---------------------------------|---------------------------------------|  
    |**Nome**|Nome della registrazione Intrastat. È possibile immettere un massimo di 10 caratteri alfanumerici.|  
    |**Description**|Descrizione della registrazione Intrastat. È possibile immettere un massimo di 50 caratteri alfanumerici.|  
    |**Periodicità**|Selezionare una delle seguenti opzioni:<br /><br /> -   **Mese**<br />-   **Trimestre**<br />-   **Anno**|  
    |**Tipo**|Selezionare una delle seguenti opzioni:<br /><br /> -   **Acquisti**<br />-   **Vendite**|  
    |**Periodo statistico**|Periodo statistico che sarà coperto dal report. Immettere il valore nel formato AAMM.|  
    |**Mov. di rettifica**|Selezionare la casella di controllo **Mov. di rettifica** per rettificare un movimento.|  
    |**Nr. dischetto**|Numero del dischetto.<br /><br /> Questo campo viene utilizzato quando si esegue il processo batch Intrastat - Floppy dichiaraz.|  
    |**Identificatore valuta**|Codice identificativo della valuta per il report Intrastat.|  
    |**Riportato**|Se il movimento è già stato dichiarato agli uffici tributari, selezionare la casella di controllo **Riportato**. Questa casella di controllo viene selezionata automaticamente quando si esegue il processo batch **Intrastat - Floppy dichiaraz.** per il movimento in questione.|  

4.  Per chiudere la pagina, scegliere il pulsante **OK**.  

## <a name="see-also"></a>Vedi anche  
  [Funzionalità locale per l'Italia](italy-local-functionality.md)   
 [Stampa di report Intrastat per l'Italia](how-to-print-intrastat-reports-for-italy.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]