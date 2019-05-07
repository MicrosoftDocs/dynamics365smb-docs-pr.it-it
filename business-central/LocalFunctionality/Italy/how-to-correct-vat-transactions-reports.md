---
title: 'Procedura: Correggere i report di transazioni IVA'
description: È possibile correggere e inviare nuovamente i report di transazioni IVA.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: b0b269bd6a4aae48c70342ecbe4690059116e485
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2019
ms.locfileid: "919625"
---
# <a name="correct-vat-transactions-reports"></a>Correggere i report di transazioni IVA

1.  Scegliere l'icona ![Cerca pagina o report](../../media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Report IVA** e scegliere il collegamento correlato.  
2.  Creare un nuovo report. Per ulteriori informazioni, vedere [Creare report elettronici di transazioni IVA](how-to-create-electronic-vat-transactions-reports.md).  
3.  Nel nuovo report, impostare il campo **Tipo report IVA** su **Correttiva** o **Annullamento**. Nel campo **Nr. report originale** selezionare il report che si desidera correggere dalla lista dei report disponibili. I campi **Data di fine** e **Data di inizio** vengono copiati dal report originale.  

    > [!NOTE]  
    >  È possibile selezionare soltanto i report IVA che risultano contrassegnati come inviati, in quanto è necessario che il report originale abbia un **Nr. ricevuta ufficio fiscale**  
    >   
    >  Se si tratta di un report correttivo, nella scheda **Pagina iniziale**, nel gruppo **Processo**, scegliere **Suggerisci righe** per ottenere i movimenti IVA corrispondenti per il periodo. In un report di annullamento non sono incluse righe.  
    >   
    >  Le righe suggerite sono basate sui movimenti IVA all'interno del periodo specificato e sul setup corrente della soglia. Non è correlato alle informazioni del report originale.  

4.  Esaminare i dettagli della transazione. Per evitare che una riga venga dichiarata all'autorità fiscale, nella riga, deselezionare la casella di controllo **Elementi inclusi in report**.  

    Scegliere l'azione **Esporta**. Il processo batch **Esporta transazioni IVA** viene aperto.  

    > [!NOTE]  
    >  Scegliendo **Esporta** per un report con lo stato Aperto, verrà convalidato automaticamente e lo stato verrà modificato in Rilasciato. A questo punto, è possibile riaprire il report per apportare le modifiche.  

5.  Inviare il file all'autorità competente. Utilizzare le indicazioni fornite dall'autorità. Per ulteriori informazioni, vedere l'[agenzia delle entrate italiana](https://go.microsoft.com/fwlink/?LinkID=206524).  

    Una volta ricevuta una risposta dalle autorità fiscali, è necessario aggiornare il report IVA.  

6.  Nella Scheda dettaglio **Generale** nel campo **Nr. ricevuta ufficio fiscale** specificare il numero di carico ricevuto dalle autorità fiscali.  
7.  Scegliere l'azione **Contrassegna come inviato** per completare il report. Il valore del campo **Stato** diventa Inviato.  

## <a name="see-also"></a>Vedi anche  
 [Esportare i report di transazioni IVA](how-to-export-vat-transactions-reports.md)
