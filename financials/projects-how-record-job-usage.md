---
title: Registrare l'utilizzo previsto e fatturabile delle risorse commesse| Documenti Microsoft
description: Descrive come registrare il consumo o l'utilizzo degli articoli o di risorse nelle commesse per semplificare la gestione progetti.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, consumption
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: b0bd4f9a4c0963520631e1571fd182adce85fdd9
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="record-usage-for-jobs"></a>Registrare l'utilizzo nelle commesse
Nella finestra **Righe pianificazione commessa** è possibile esaminare e registrare l'utilizzo nelle diverse parti della commessa, che viene automaticamente aggiornato quando si modificano e si trasferiscono le informazioni tra le commesse e le registrazioni delle commesse o le fatture commessa. Questo richiede che sia stata impostata una commessa in modo da attivare **Applica collegamento utilizzo**. Per ulteriori informazioni, vedere [Impostare le commesse](projects-how-setup-jobs.md).  

Ad esempio, per le righe di pianificazione di tipo **Budget**, è possibile immettere la quantità di una risorsa e indicare la quantità da trasferire nelle registrazioni commesse. Se il tipo di righe di pianificazione è **Fatturabile**, è possibile immettere la quantità della risorsa e indicare la quantità da trasferire in una fattura. Confrontando la quantità che è stata trasferita nelle registrazioni o nella fattura con la quantità residua, è possibile verificare rapidamente le informazioni di utilizzo.

Di seguito viene descritto come registrare i prezzi e i costi di commessa effettivi (fatturabili) o a budget. Per informazioni sulla stima dei valori a budget durante la pianificazione, vedere [Gestire i budget delle commesse](projects-how-manage-budgets.md).

## <a name="to-record-usage-for-a-job-planning-line-of-type-budget"></a>Per registrare l'utilizzo per una riga di pianificazione commessa di tipo Budget
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Commesse**, quindi scegliere il collegamento correlato.  
2. Selezionare la relativa commessa, quindi scegliere l'azione **Righe pianificazione commessa**.
3. Selezionare una riga di pianificazione commessa di tipo **Budget** o **Budget e fatturabile** per la quale si desidera registra l'utilizzo.
4. Nel campo **Qtà da trasferire per registrazione**, immettere il numero che si desidera trasferire. La quantità di default è il valore che si immette nel campo **Quantità**.

    Il campo **Quantità residua** mostra la quantità che rimane per completare la commessa e da trasferire nelle registrazioni.  
5. Scegliere l'azione **Crea righe registrazioni commesse**.
6. Nella finestra **Trasferimento commessa a riga pianificazione** compilare i campi in base alle esigenze, quindi scegliere **OK**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Scegliere l'azione **Apri registrazioni commesse**.  
8. Nella finestra **Registrazioni commesse**, selezionare la riga pertinente e scegliere l'azione **Registra**.
9. Nella finestra **Righe pianificazione commessa**, esaminare l'utilizzo registrato osservando i campi **Quantità**, **Quantità residua** e **Qtà da trasferire per registrazione**.  
10. Ripetere i passaggi da 3 a 8 per registrare altri utilizzi.  

## <a name="to-record-usage-for-a-job-planning-line-of-type-billable"></a>Per registrare l'utilizzo per una riga di pianificazione commessa di tipo Fatturabile
Anche nel task successivo si registra l'utilizzo, ma per una riga di pianificazione commessa di tipo **Fatturabile**. In genere, in questo caso, si fattura l'utilizzo, ma è anche possibile trasferirlo alle registrazioni. Tuttavia, quando si esegue questa operazione, viene creata una riga di pianificazione commessa di tipo **Budget** da associare alla riga fatturabile. Per ulteriori informazioni, vedere [Gestire i budget delle commesse](projects-how-manage-budgets.md).

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Commesse**, quindi scegliere il collegamento correlato.
2. Selezionare la relativa commessa, quindi scegliere l'azione **Righe pianificazione commessa**.  
3. Selezionare una riga di pianificazione commessa di tipo **Fatturabile** per la quale si desidera registrare l'utilizzo.
4. Nel campo **Qtà da trasferire in fattura**, immettere il numero che si desidera trasferire. La quantità di default è il valore che si immette nel campo **Quantità**.

    Il campo **Quantità da fatturare** mostra la quantità che rimane per completare la commessa e da fatturare.  
5. Scegliere l'azione **Crea fattura di vendita**.
6. Nella finestra **Commessa - Trasferimento a fattura vendita** compilare i campi in base alle esigenze, quindi scegliere **OK**.
7. Nella finestra **Righe pianificazione commessa** selezionare la riga interessata, quindi scegliere l'azione **Registra**.
8. Esaminare l'utilizzo registrato osservando i campi **Quantità**, **Quantità da fatturare**, **Qtà da trasferire in fattura** e, se la fattura di vendita è registrata, il campo **Qtà fatturata**.
9. Ripetere i passaggi da 3 a 8 per registrare altri utilizzi.  
10. Per esaminare la fattura di vendita registrata correlata, scegliere l'azione **Fatture/Note credito vendite**.  
11. Nella finestra **Fatture commessa** selezionare la fattura pertinente, quindi scegliere l'azione **Apri fattura/nota credito vendita**.         

## <a name="to-create-job-journal-lines-from-job-planning-lines"></a>Per creare le righe delle registrazioni delle commesse dalle righe di pianificazione commessa
Quando si è pronti a registrare le informazioni finanziarie per le commesse, è necessario creare le righe di registrazione commessa che è possibile registrare.

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Commesse**, quindi scegliere il collegamento correlato.  
2. Selezionare una commessa aperta, quindi scegliere l'azione **Righe pianificazione commessa**.  
3. Nella finestra **Righe pianificazione commessa**, in una riga di pianificazione commessa pertinente, nel campo **Qtà da trasferire per registrazione**, immettere la quantità che si desidera trasferire nelle registrazioni commessa.  
4. Scegliere l'azione **Crea righe registrazioni commesse**.
5. Nella finestra **Trasferimento commessa a riga pianificazione** compilare i campi in base alle esigenze.  
6. Scegliere il pulsante **OK**. Vengono create le righe di registrazione commessa.
7. Per verificare il trasferimento, aprire il batch di registrazioni delle commesse rilevante e controllare i movimenti.  
8. Una volta completate le righe di registrazione commessa, scegliere l'azione **Registra**.  

## <a name="to-create-job-journal-lines-manually"></a>Per creare le righe delle registrazioni delle commesse manualmente
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Registrazioni commesse**, quindi scegliere il collegamento correlato.  
2. Nel campo **Nome batch** scegliere un nome batch di registrazioni commesse pertinente.  
3. In una nuova riga, immettere il numero di documento, il numero di commessa, il numero di task commessa, il tipo e la quantità del tipo consumata.  
4. Una volta completate le righe di registrazione commessa, scegliere l'azione **Registra**.  

## <a name="to-review-planning-lines-for-a-job-ledger-entry"></a>Per esaminare le righe di pianificazione per un movimento contabile commessa
Dopo avere registrato le righe di registrazione commessa registrate, è possibile visualizzare le righe di pianificazione associate ai movimenti di registrazione commesse che sono stati registrati.

> [!NOTE]  
>   Questo richiede che la casella di controllo **Applica collegamento utilizzo** sia stata selezionata per la commessa oppure che sia l'impostazione di default per tutte le commesse nell'organizzazione. Per ulteriori informazioni, vedere [Impostare le commesse](projects-how-setup-jobs.md).  

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Registrazioni commesse**, quindi scegliere il collegamento correlato.  
2. Selezionare una registrazione commessa corrispondente, quindi scegliere l'azione **Mov. contabili**.  
3. Nella finestra **Movimenti contabili commesse** scegliere l'azione **Mostra righe pianificazione commessa collegate**.

## <a name="see-also"></a>Vedi anche
[Gestione progetti](projects-manage-projects.md)  
[Finanze](finance.md)  
[Acquisti](purchasing-manage-purchasing.md)         
[Vendite](sales-manage-sales.md)      
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

