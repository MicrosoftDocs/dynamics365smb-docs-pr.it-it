---
title: Riclassificare i cespiti| Documenti Microsoft
description: Riclassificare un cespite da trasferire in un altro reparto, dividere o raggruppare con altri cespiti.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 392ba8da5a67a5cca4678e1817288b165d122864
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="transfer-split-or-combine-fixed-assets"></a>Trasferimento, divisione o raggruppamento dei cespiti
Utilizzare le registrazioni di riclassificazione cespiti per trasferire, suddividere e raggruppare i cespiti. Visualizzare o stampare i risultati della riclassificazione cespiti con il report **Cespiti - Valore contabile 02**.

## <a name="to-transfer-a-fixed-asset-to-a-different-department"></a>Per trasferire un cespite in un reparto diverso
Il trasferimento dei cespiti in ubicazioni diverse può essere utilizzato, ad esempio, quando si assegna un cespite al reparto produzione mentre è in costruzione e al termine della costruzione viene spostato nel reparto amministrativo.  

1. Impostare un nuovo cespite. Immettere il nuovo reparto nel campo **Cod. Reparto**.
2. Assegnare un registro beni ammortizzabili al nuovo cespite. Per ulteriori informazioni, vedere [Acquisire i cespiti](fa-how-acquire.md).
3. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Registrazioni riclass. cespiti**, quindi scegliere il collegamento correlato.
4. Creare una registrazione riclassificazione in cui il campo **Nr. cespite** contiene il cespite originale e il campo **Nuovo nr. cespite** contiene il nuovo cespite da spostare.  
5. Scegliere l'azione **Riclassifica**.

    Vengono create due righe in Registrazioni C/G cespiti utilizzando la definizione ed il batch specificati nella finestra **Setup Reg. Cespiti** per il registro beni ammortizzabili indicato. Per ulteriori informazioni, vedere [Impostare l'ammortamento cespiti](fa-how-setup-depreciation.md).
6. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Registrazioni cespiti in C/G**, quindi scegliere il collegamento correlato.    
7. Nella finestra **Registrazioni cespiti in C/G**, scegliere l'azione **Registra** per registrare la riclassificazione eseguita ai passaggi 4 e 5.

Se per un cespite è stato registrato un costo d'acquisto, è possibile utilizzare le registrazioni di riclassificazione cespiti per suddividere i costi di acquisto in diversi cespiti.  

## <a name="to-split-a-fixed-asset-into-three-fixed-assets"></a>Per dividere un cespite in tre cespiti
È possibile dividere un unico cespite in più cespiti, ad esempio quando è necessario distribuire un cespite in tre diversi reparti. In tal caso, è possibile spostare ad esempio il 25 percento del costo di acquisto e dell'ammortamento del cespite originale al secondo cespite ed il 45 percento al terzo cespite. Il rimanente 30 percento resterà al cespite originale.

1. Impostare due nuovi cespiti. Immettere il nuovo reparto nel campo **Cod. Reparto**.
2. Assegnare i registri beni ammortizzabili ai nuovi cespiti. Per ulteriori informazioni, vedere [Acquisire i cespiti](fa-how-acquire.md).
3. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Registrazioni riclass. cespiti**, quindi scegliere il collegamento correlato.
4. Creare due righe di registrazione riclassificazione, una per ogni nuovo cespite.
5. Nella prima riga immettere il secondo cespite nel campo **Nuovo nr. cespite** e 25 nel campo **Riclassifica costi di acq. %**.
6. Nella seconda riga immettere il terzo cespite nel campo **Nuovo nr. cespite** e 40 nel campo **Riclassifica costi di acq. %**.
7. In entrambe le righe, selezionare le caselle di controllo **Riclassifica costi di acq.** e **Riclassifica ammortamento**.   
8. Scegliere l'azione **Riclassifica**.

    Vengono create due righe in Registrazioni C/G cespiti utilizzando la definizione ed il batch specificati nella finestra **Setup Reg. Cespiti** per il registro beni ammortizzabili indicato. Per ulteriori informazioni, vedere [Impostare l'ammortamento cespiti](fa-how-setup-depreciation.md).    
9. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Registrazioni cespiti in C/G**, quindi scegliere il collegamento correlato.
10. Nella finestra **Registrazioni cespiti in C/G**, scegliere l'azione **Registra** per registrare la riclassificazione eseguita ai passaggi da 4 a 8.

## <a name="to-combine-two-fixed-assets-into-one"></a>Per raggruppare due cespiti in uno
È possibile raggruppare più cespiti in un unico cespite, ad esempio quando si spostano i cespiti distribuiti in un unico reparto. Se sono stati registrati i costi di acquisto e l'ammortamento del cespite da spostare, i valori verranno raggruppati singolo cespite.

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Registrazioni riclass. cespiti**, quindi scegliere il collegamento correlato.
2. Creare una registrazione riclassificazione in cui il campo **Nr. cespite** contiene il cespite da spostare/combinare e il campo **Nuovo nr. cespite** contiene il cespite con cui sarà combinato.
3. Lasciare vuoti il campo **Riclassifica costi di acq. %** per sposare/raggruppare l'intero costo di acquisto.    
4. Selezionare le caselle di controllo **Riclassifica costi di acq.** e **Riclassifica ammortamento**.
5. Nella scheda **Azioni** selezionare **Riclassifica**.

    Vengono create due righe in Registrazioni C/G cespiti utilizzando la definizione ed il batch specificati nella finestra **Setup Reg. Cespiti** per il registro beni ammortizzabili indicato. Per ulteriori informazioni, vedere [Impostare l'ammortamento cespiti](fa-how-setup-depreciation.md).   
6. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Registrazioni cespiti in C/G**, quindi scegliere il collegamento correlato.
7. Nella finestra **Registrazioni cespiti in C/G**, scegliere l'azione **Registra** per registrare la riclassificazione eseguita ai passaggi da 2 a 5.

## <a name="to-view-changed-depreciation-book-values-due-to-fixed-asset-reclassification"></a>Per visualizzare i valori del registro beni ammortizzabili modificati a causa dalla riclassificazione dei cespiti
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Valore contabile cespiti 02**, quindi scegliere il collegamento correlato.
2. Compilare i campi, se necessario.
3. Selezionare il pulsante **Stampa** o **Anteprima**.  

## <a name="see-also"></a>Vedi anche
[Cespiti](fa-manage.md)  
[Impostazione di cespiti](fa-setup.md)  
[Finanze](finance.md)  
[Benvenuto in [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

