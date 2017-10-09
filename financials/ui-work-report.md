---
title: Programmazione dell'esecuzione di un report per una data e un'ora specifiche | Documenti Microsoft
description: Informazioni su come inserire un report in una coda di processi e programmare per l'elaborazione per una data e un'ora specifiche.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, report
ms.date: 07/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: badcdee3dfa5bec3c2462149989cf9d4fb5af2a0
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="working-with-reports"></a>Utilizzo dei report
Un report raccoglie informazioni basate su un set di criteri specificato e organizza e presenta le informazioni in un formato di stampa facile da leggere. Sono disponibili molti report a cui è possibile accedere dall'applicazione. I report in genere forniscono informazioni relative al contesto della pagina visualizzata. Ad esempio, la pagina **Cliente** include i report per i principali 10 clienti, le statistiche di vendita e altro ancora.

I report sono disponibili nella scheda **Report** delle pagine selezionate oppure è possibile utilizzare una ricerca per trovare i report in base al nome. Quando si apre un report, viene visualizzata una pagina con le informazioni (opzioni e filtri) che determina cosa includere nel report. Ad esempio, a seconda del report, è possibile specificare l'intervallo di date, un record specifico come un cliente o un ordinamento.

## <a name="previewing-a-report"></a>Anteprima di un report
Scegliere **Anteprima** per vedere il report nel browser Internet. Puntare un'area del report per visualizzare la barra dei menu.  

![Barra degli strumenti di anteprima del report](media/report_viewer.png "Barra degli strumenti di anteprima del report").

Utilizzare la barra dei menu per:

-   Spostarsi tra le pagine
-   Ingrandire o ridurre
-   Ridimensionare per adattare alla finestra
-   Seleziona testo

    È possibile copiare il testo di un report e incollarlo altrove, come una pagina in [!INCLUDE[d365fin](includes/d365fin_md.md)] o Microsoft Word.  Ad esempio, tenere premuto il pulsante del mouse sul punto da cui si desidera iniziare, quindi spostare il mouse per selezionare una o più parole, frasi o paragrafi. È quindi possibile premere il pulsante destro del mouse e selezionare **Copia**. È possibile incollare il testo selezionato nella posizione desiderata.
-   Panoramica del documento

    È possibile spostare l'area visibile del report in qualsiasi direzione in modo da poter visualizzare altre aree o il report. Ciò risulta utile quando è stato eseguito l'ingrandimento per visualizzare i dettagli.  Ad esempio, tenere premuto il pulsante del mouse su un punto dell'anteprima del report, quindi spostare il mouse.

-   Scaricare in un file PDF sul computer o in rete.


## <a name="saving-a-report"></a>Salvataggio di un report
È possibile salvare un report in un documento PDF, documento di Microsoft Word o documento di Microsoft Excel scegliendo **Invia a** ed effettuando la scelta desiderata. 

## <a name="ScheduleReport"></a> Pianificazione dell'esecuzione di un report
È possibile pianificare l'esecuzione di un report per data e orario specifici. I report previsti vengono inseriti nella coda commesse e vengono elaborati all'orario pianificato, in maniera analoga alle altre commesse. È possibile salvare il report elaborato in un file, ad esempio un file Excel, Word, PDF, o stamparlo con una stampante selezionata, o semplicemente elaborare il report. Se si sceglie di salvare il report in un file, il report elaborato viene inviato nell'area **Report elaborati** della home page, dove è possibile visualizzarlo.

È possibile programmare un report quando si apre un report. Scegliere l'azione **Programmazione**, quindi immettere informazioni, come la stampante e la data e l'ora. Il report viene aggiunto alla coda processi e sarà eseguito alla data specificata. Quando il report viene elaborato, l'elemento verrà rimosso dalla coda commesse. Se il report elaborato è stato salvato in un file, sarà disponibile nell'area **Report elaborati**.

## <a name="PrintReport"></a>Stampa di un report
Quando si desidera stampare un report, è necessario scaricarlo come documento PDF, Word o Excel prima di tutto scegliendo il pulsante **Invia a**. A questo punto è possibile aprire il documento report immediatamente e stamparlo oppure salvarlo e stamparlo in seguito.

## <a name="using-saved-settings"></a>Uso delle impostazioni salvate
Un report possono includere una o più voci nella casella **Impostazioni salvate**. Le *Impostazioni salvate* costituiscono fondamentalmente un gruppo di default di opzioni e filtri che si possono applicare al report prima di visualizzarlo in anteprima o inviarlo in un file. L'utilizzo delle impostazioni salvate è un metodo rapido e affidabile di generare coerentemente report contenenti dati corretti.

Esiste sempre una voce Impostazioni salvate, che viene chiamata **Filtri e opzioni utilizzati di recente**. Questa voce imposta il report per utilizzare le opzioni e i filtri che sono stati utilizzati l'ultima volta che è stato visualizzato il report.

>[!NOTE]
>In qualità di amministratore, è possibile creare e gestire le impostazioni salvate per i report di tutti gli utenti. Per ulteriori informazioni, vedere [Gestione impostazioni salvate nei report](reports-saving-reusing-settings.md).

## <a name="changing-the-layout-and-look-of-a-report"></a>Modifica del layout e dell'aspetto di un report
Un layout di report determina le informazioni che verranno visualizzate nel report, nonché la disposizione e l'aspetto delle stesse. Se si desidera passare a un layout diverso, vedere [Procedura: Modificare il layout attualmente utilizzato in un report](ui-how-change-layout-currently-used-report.md) Per personalizzare un layout di report, vedere [Procedura: Creare e modificare un layout di report personalizzato](ui-how-create-custom-report-layout.md).

## <a name="see-also"></a>Vedi anche
[Specificare la selezione della stampante per i report](ui-specify-printer-selection-reports.md)  
[Gestione dei layout di report e documento](ui-manage-report-layouts.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

