---
title: Riclassificare i cespiti
description: 'Riclassificare un cespite da trasferire in un altro reparto, dividere o raggruppare con altri cespiti.'
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '5638, 5636, 5640, 5637'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="transfer-split-or-combine-fixed-assets"></a><a name="transfer-split-or-combine-fixed-assets"></a>Trasferimento, divisione o raggruppamento dei cespiti

Utilizzare le registrazioni di riclassificazione cespiti per trasferire, suddividere e raggruppare i cespiti. Visualizzare o stampare i risultati della riclassificazione cespiti con il report **Cespiti - Valore contabile 02**.

## <a name="to-transfer-a-fixed-asset-to-a-different-department"></a><a name="to-transfer-a-fixed-asset-to-a-different-department"></a>Per trasferire un cespite in un reparto diverso

Il trasferimento dei cespiti in ubicazioni diverse può essere utilizzato, ad esempio, quando si assegna un cespite al reparto produzione mentre è in costruzione e al termine della costruzione viene spostato nel reparto amministrativo.  

1. Impostare un nuovo cespite. Inserire il nuovo dipartimento come dimensione.  
2. Assegnare un registro beni ammortizzabili al nuovo cespite. Per ulteriori informazioni, vedere [Acquisire i cespiti](fa-how-acquire.md).
3. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Registrazioni riclassificazione cespiti**, quindi scegli il collegamento correlato.
4. Creare una riga di registrazione in cui il campo **Nr. cespite** contiene il cespite originale e il campo **Nuovo nr. cespite** contiene il nuovo cespite da spostare. Compilare debitamente gli altri campi.  
5. Scegliere l'azione **Riclassifica**.

    Vengono create due righe in Registrazioni C/G cespiti utilizzando la definizione ed il batch specificati nella pagina **Setup Reg. Cespiti** per il registro beni ammortizzabili indicato. Per ulteriori informazioni, vedere [Impostare l'ammortamento cespiti](fa-how-setup-depreciation.md).
6. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Registrazioni cespiti in C/G**, quindi scegli il collegamento correlato.    
7. Nella pagina **Registrazioni cespiti in C/G**, scegliere l'azione **Registra** per registrare la riclassificazione eseguita ai passaggi 4 e 5.

Se per un cespite è stato registrato un costo d'acquisto, è possibile utilizzare le registrazioni di riclassificazione cespiti per suddividere i costi di acquisto in diversi cespiti.  

## <a name="to-split-a-fixed-asset-into-three-fixed-assets"></a><a name="to-split-a-fixed-asset-into-three-fixed-assets"></a>Per dividere un cespite in tre cespiti
È possibile dividere un unico cespite in più cespiti, ad esempio quando è necessario distribuire un cespite in tre diversi reparti. In tal caso, è possibile spostare ad esempio il 25 percento del costo di acquisto e dell'ammortamento del cespite originale al secondo cespite ed il 45 percento al terzo cespite. Il rimanente 30 percento resterà al cespite originale.

1. Impostare due nuovi cespiti. Inserire i dipartimenti rilevanti come dimensione.  
2. Assegnare i registri beni ammortizzabili ai nuovi cespiti. Per ulteriori informazioni, vedere [Acquisire i cespiti](fa-how-acquire.md).
3. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Registrazioni riclassificazione cespiti**, quindi scegli il collegamento correlato.
4. Creare due righe di registrazione riclassificazione, una per ogni nuovo cespite.
5. Nella prima riga immettere il secondo cespite nel campo **Nuovo nr. cespite** e 25 nel campo **Riclassifica costi di acq. %**.
6. Nella seconda riga immettere il terzo cespite nel campo **Nuovo nr. cespite** e 40 nel campo **Riclassifica costi di acq. %**.
7. In entrambe le righe, selezionare le caselle di controllo **Riclassifica costi di acq.** e **Riclassifica ammortamento**.  
8. Scegliere l'azione **Riclassifica**.  

    Vengono create due righe in Registrazioni C/G cespiti utilizzando la definizione ed il batch specificati nella pagina **Setup Reg. Cespiti** per il registro beni ammortizzabili indicato. Per ulteriori informazioni, vedere [Impostare l'ammortamento cespiti](fa-how-setup-depreciation.md).    
9. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registrazioni cespiti in C/G**, quindi scegli il collegamento correlato.
10. Nella pagina **Registrazioni cespiti in C/G**, scegliere l'azione **Registra** per registrare la riclassificazione eseguita ai passaggi da 4 a 8.

## <a name="to-combine-two-fixed-assets-into-one"></a><a name="to-combine-two-fixed-assets-into-one"></a>Per raggruppare due cespiti in uno

È possibile raggruppare più cespiti in un unico cespite, ad esempio quando si spostano i cespiti distribuiti in un unico reparto. Se sono stati registrati i costi di acquisto e l'ammortamento del cespite da spostare, i valori verranno raggruppati singolo cespite.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registrazioni riclassificazione cespiti**, quindi scegli il collegamento correlato.
2. Creare una registrazione riclassificazione in cui il campo **Nr. cespite** contiene il cespite da spostare/combinare e il campo **Nuovo nr. cespite** contiene il cespite con cui sarà combinato.
3. Lasciare vuoti il campo **Riclassifica costi di acq. %** per sposare/raggruppare l'intero costo di acquisto.  
4. Selezionare le caselle di controllo **Riclassifica costi di acq.** e **Riclassifica ammortamento**.
5. Scegliere l'azione **Riclassifica**.

    Vengono create due righe in Registrazioni C/G cespiti utilizzando la definizione ed il batch specificati nella pagina **Setup registrazioni cespiti** per il registro beni ammortizzabili indicato. Per ulteriori informazioni, vedere [Impostare l'ammortamento cespiti](fa-how-setup-depreciation.md).   
6. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registrazioni cespiti in C/G**, quindi scegli il collegamento correlato.
7. Nella pagina **Registrazioni cespiti in C/G**, scegliere l'azione **Registra** per registrare la riclassificazione eseguita ai passaggi da 2 a 5.

## <a name="to-view-changed-depreciation-book-values-due-to-fixed-asset-reclassification"></a><a name="to-view-changed-depreciation-book-values-due-to-fixed-asset-reclassification"></a>Per visualizzare i valori del registro beni ammortizzabili modificati a causa dalla riclassificazione dei cespiti

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Valore contabile cespiti 02**, quindi scegli il collegamento correlato.
2. Compilare i campi in base alle esigenze.
3. Seleziona il pulsante **Stampa** o **Anteprima**.  

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Vedi il relativo [training Microsoft](/training/paths/reclassify-fixed-assets/)

## <a name="see-also"></a><a name="see-also"></a>Vedere anche

[Cespiti](fa-manage.md)  
[Impostazione di cespiti](fa-setup.md)  
[Finanze](finance.md)  
[Prepararsi a fare affari](ui-get-ready-business.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
