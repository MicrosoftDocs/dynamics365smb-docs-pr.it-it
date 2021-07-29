---
title: Visualizzare e modificare in Excel da Business Central
description: Informazioni su come aprire le pagine in Microsoft Excel da Business Central per una migliore analisi dei dati.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 6bf12f55f6bce843c4ed12f2a40db542367fffde
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/08/2021
ms.locfileid: "6443481"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a>Visualizzare e modificare in Excel da Business Central

Con le pagine che visualizzano un elenco di record in righe e colonne, come un elenco di clienti, ordini di vendita o fatture, è anche possibile visualizzare i record utilizzando Microsoft Excel. A seconda della pagina, hai due opzioni per la visualizzazione in Excel. È possibile selezionare l'azione **Apri in Excel** o l'azione **Modifica in Excel** nella pagina. Questo articolo spiega le differenze tra le due azioni.

## <a name="open-in-excel"></a>Apri in Excel

Con l'azione **Apri in Excel** puoi apportare modifiche ai record in Excel, ma non puoi ripubblicare le modifiche in [!INCLUDE[prod_short](includes/prod_short.md)]. È possibile salvare le modifiche solo in un file Excel nel computer.

- Con questa azione, Excel rispetta tutti i filtri nella pagina che limitano i record visualizzati. La cartella di lavoro Excel conterrà le stesse righe e colonne presenti nella pagina in [!INCLUDE[prod_short](includes/prod_short.md)].

- Questa azione è compatibile con Windows e macOS.

- A partire dall'aggiornamento 18.3, è anche possibile visualizzare gli elenchi visualizzati nelle parti della pagina, come le righe di un ordine di vendita. Per ora, questa funzionalità è una funzionalità opzionale, che richiede l'abilitazione di **Esporta qualsiasi parte lista in Excel** in **Gestione funzionalità**. Per ulteriori informazioni, vedere [Abilitazione di funzionalità imminenti in anticipo](/dynamics365/business-central/dev-itpro/administration/feature-management). 

> [!NOTE]
> Per [!INCLUDE[prod_short](includes/prod_short.md)] in locale l'azione **Apri in Excel** è disponibile per impostazione predefinita. Tuttavia, se [!INCLUDE[prod_short](includes/prod_short.md)] in locale è configurato per la modifica dei dati in Excel, l'azione **Apri in Excel** è sostituita dall'azione **Modifica in Excel**.

[!INCLUDE [send-report-excel](includes/send-report-excel.md)]  

## <a name="edit-in-excel"></a>Modifica in Excel

Con l'azione **Modifica in Excel** puoi apportare modifiche ai record in Excel e poi puoi ripubblicare le modifiche in [!INCLUDE[prod_short](includes/prod_short.md)].

- Con questa azione, Excel rispetta la maggior parte dei filtri sulla pagina che limitano i record visualizzati, quindi la cartella di lavoro di Excel conterrà quasi gli stessi record e colonne.

- È compatibile con Windows ma non con macOS.

- Puoi cambiare la società con cui stai lavorando. Per cambiare azienda, seleziona l'icona **Opzioni** ![Opzioni del componente aggiuntivo di Excel.](media/cogwheel.png "Opzioni del componente aggiuntivo per Excel") nel riquadro del componente aggiuntivo di Excel, quindi seleziona l'azienda dal campo **Società**.  

    > [!IMPORTANT]
    > Quando si cambia la società, assicurarsi che il campo **Ambiente** non sia vuoto. In tal caso, impostarlo su una delle opzioni disponibili; in caso contrario, il componente aggiuntivo non funzionerà correttamente.  

Se si apportano modifiche al componente aggiuntivo, è necessario ricaricarlo per aggiornare la connessione. Per ricaricare, utilizzare il ![menu del componente aggiuntivo per Excel](media/excel-addin-menu.png "Menu del componente aggiuntivo per Excel") nell'angolo in alto a destra del componente aggiuntivo. Se non riesci a caricare il componente aggiuntivo, contatta l'amministratore. Se sei l'amministratore, vedi [Installazione del componente aggiuntivo di Excel per la modifica dei dati di Business Central](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).

> [!NOTE]
> Per [!INCLUDE[prod_short](includes/prod_short.md)] in locale, l'azione **Modifica in Excel** è disponibile solo se il componente aggiuntivo di Excel è stato configurato dall'amministratore ed è disponibile solo per il client Web. Gli amministratori che desiderano installare il componente aggiuntivo di Excel possono consultare [Installazione del componente aggiuntivo di Excel per la modifica dei dati di Business Central](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).

### <a name="see-the-differences-between-the-options"></a>Vedere le differenze tra le opzioni
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-related-training-at-microsoft-learn"></a>Vedere le informazioni relative al training in [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Vedere anche

[Analisi dei rendiconti finanziari in Microsoft Excel](finance-analyze-excel.md)  
[Utilizzo di Business Central](ui-work-product.md)  
[Miglioramenti all'integrazione di Excel nella seconda ondata di rilascio del 2019](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration)  


[!INCLUDE[footer-include](includes/footer-banner.md)]