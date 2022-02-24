---
title: 'Procedura: Chiusura di un anno fiscale'
description: Per valutare i profitti e le perdite, alla fine di ogni anno fiscale viene fornito un report di chiusura dell'anno fiscale.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 77b122498d8b4230a8fa6464a96bf96755c0ee24
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2020
ms.locfileid: "3181141"
---
# <a name="close-a-fiscal-year"></a>Chiusura di un anno fiscale
Per valutare i profitti e le perdite, alla fine di ogni anno fiscale viene fornito un report di chiusura dell'anno fiscale.  

La chiusura dell'anno fiscale include i seguenti passaggi:  

- Chiusura dell'anno fiscale utilizzando l'opzione **Periodo contabile**.  
- Generazione di un movimento di chiusura di fine anno utilizzando l'opzione **Chiudi conto economico**.  
- Registrazione del movimento di chiusura di fine anno.  

## <a name="to-close-a-fiscal-year"></a>Per chiudere un anno fiscale  

1.  Scegliere l'icona ![Cerca pagina o report](../../media/ui-search/search_small.png "Icona Cerca pagina o report"), immettere **Periodi contabili** e quindi scegliere il collegamento correlato.  
2.  Per chiudere un periodo contabile, selezionare il periodo contabile, quindi scegliere l'azione **Chiudi anno**.  
3.  Selezionare il pulsante **Sì** per confermare che si desidera chiudere l'anno fiscale.  

    > [!IMPORTANT]  
    >  Dopo la chiusura dell'anno fiscale, non sarà possibile riaprilo, né modificare il periodo nell'anno fiscale.  

## <a name="to-generate-a-year-end-closing-entry-using-the-close-income-statement-option"></a>Per generare un movimento di chiusura di fine anno utilizzando l'opzione Chiudi conto economico  

1.  Scegliere l'icona ![Cerca pagina o report](../../media/ui-search/search_small.png "Icona Cerca pagina o report"), immettere **Chiudi conto economico** e quindi scegliere il collegamento correlato.  
2.  Compilare i campi nella scheda **Opzioni** come descritto nella tabella riportata di seguito.  

    |Campo|Description|  
    |---------------------------------|---------------------------------------|  
    |**Data fine anno fiscale**|Data di fine dell'anno fiscale.|  
    |**Def. Registrazioni Generali**|Nome della definizione di registrazioni COGE in cui collocare i movimenti.|  
    |**Batch Reg. Generali**|Nome del batch di registrazioni COGE in cui collocare i movimenti.|  
    |**Nr. conto profitti/perdite**|Selezionare il numero di conto pertinente.|  
    |**Nr. Documento**|In questo campo viene inserito automaticamente il successivo numero disponibile nel batch di registrazioni, se si specifica un valore nei campi **Def. registrazioni COGE** e **Batch registrazioni COGE**. È anche possibile immettere manualmente un numero in questo campo.|  
    |**Nr. conto utili d'esercizio**|Selezionare il numero univoco del conto utili d'esercizio.|  
    |**Nr. conto perdite d'esercizio**|Selezionare il numero univoco del conto perdite d'esercizio.|  
    |**Descr. registrazione**|Immettere una descrizione. Il testo predefinito è **Chiudi conto economico**.|  
    |**Cod. business unit**|Selezionare questa caselle di controllo se è necessario un movimento per ogni codice di business unit.|  
    |**Dimensioni**|Facoltativamente selezionare il campo per scegliere i codici di dimensione se è necessario un movimento per ogni dimensione utilizzata nel conto C/G.|  
    |**Chiusura periodo magazzino**|Questo campo indica che i periodi di magazzino con date di fine successive o corrispondenti all'ultima data del periodo contabile sono chiusi.|  

3.  Scegliere il pulsante **OK** per creare le scritture contabili.  

## <a name="to-post-the-year-end-closing-entry"></a>Per registrare il movimento di chiusura di fine anno  

1.  Scegliere l'icona ![Cerca pagina o report](../../media/ui-search/search_small.png "Icona Cerca pagina o report"), immettere **Registrazioni COGE** e quindi scegliere il collegamento correlato.  
2.  Nel campo **Batch** specificare il batch contenente i movimenti di chiusura.  
3.  Aggiungere i movimenti corrispondenti alle righe di registrazione.  
4.  Per contabilizzare le registrazioni, scegliere l'azione **Registra**.  

Viene registrato un movimento in ogni conto economico in modo che il saldo sia zero. Il risultato di fine anno viene trasferito nel conto patrimoniale.  

## <a name="see-also"></a>Vedere anche  
 [Chiusura di anni e periodi](../../year-close-years-periods.md)   
 [Funzionalità locale per l'Italia](italy-local-functionality.md)
