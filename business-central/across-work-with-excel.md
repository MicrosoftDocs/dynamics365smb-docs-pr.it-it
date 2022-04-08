---
title: Visualizzare e modificare in Excel da Business Central (video)
description: Informazioni su come aprire le pagine in Microsoft Excel da Business Central per una migliore analisi dei dati.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: f03e67b0205af92fcdbb731a74ffe7f4507c39d3
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2022
ms.locfileid: "8511261"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a>Visualizzare e modificare in Excel da Business Central

Con le pagine che visualizzano una lista di record in righe e colonne, come una lista di clienti, ordini di vendita o fatture, è possibile esportare la lista in Microsoft Excel, e visualizzarla lì. A seconda della pagina, hai due opzioni per la visualizzazione in Excel. Entrambe le opzioni sono disponibili dall'icona **Condividi**  ![Condividi una pagina in un'altra app.](media/share-icon.png) all'inizio di una pagina. È possibile selezionare l'azione **Apri in Excel** o l'azione **Modifica in Excel** nella pagina. Questo articolo spiega le differenze tra le due azioni.

## <a name="open-in-excel"></a>Apri in Excel

Con l'azione **Apri in Excel** puoi apportare modifiche ai record in Excel, ma non puoi ripubblicare le modifiche in [!INCLUDE[prod_short](includes/prod_short.md)]. È possibile salvare solo le modifiche al file Excel, senza influenzare i dati in [!INCLUDE[prod_short](includes/prod_short.md)].

- Con questa azione, Excel rispetta tutti i filtri nella pagina che limitano i record visualizzati. La cartella di lavoro Excel conterrà le stesse righe e colonne presenti nella pagina in [!INCLUDE[prod_short](includes/prod_short.md)].

- Questa azione è compatibile con Windows e macOS.

- A partire dall'aggiornamento 18.3, è anche possibile visualizzare gli elenchi visualizzati nelle parti della pagina, come le righe di un ordine di vendita. 

> [!NOTE]
> Per [!INCLUDE[prod_short](includes/prod_short.md)] in locale l'azione **Apri in Excel** è disponibile per impostazione predefinita. Tuttavia, se [!INCLUDE[prod_short](includes/prod_short.md)] in locale è configurato per la modifica dei dati in Excel, l'azione **Apri in Excel** è sostituita dall'azione **Modifica in Excel**.

[!INCLUDE [send-report-excel](includes/send-report-excel.md)]  

## <a name="edit-in-excel"></a>Modifica in Excel

L'azione **Modifica in Excel** è disponibile nella maggior parte delle liste, ma non in tutte. Con l'azione **Modifica in Excel** puoi apportare modifiche ai record in Excel e poi puoi ripubblicare le modifiche in [!INCLUDE[prod_short](includes/prod_short.md)]. Quando Excel si apre, vedrai il pannello **Add-in Excel** sulla destra.

- Con questa azione, Excel rispetta la maggior parte dei filtri sulla pagina che limitano i record visualizzati, quindi la cartella di lavoro di Excel conterrà quasi gli stessi record e colonne.

- Per ottenere gli ultimi dati da [!INCLUDE[prod_short](includes/prod_short.md)], scegli **Aggiorna** nel pannello dell'add-in di Excel.

- Puoi cambiare la compagnia con cui stai lavorando. Per cambiare azienda, seleziona l'icona **Opzioni** ![Opzioni del componente aggiuntivo di Excel.](media/cogwheel.png "Opzioni del componente aggiuntivo per Excel") nel riquadro del componente aggiuntivo di Excel, quindi seleziona l'azienda dal campo **Società**.  

    > [!IMPORTANT]
    > Quando si cambia la società, assicurarsi che il campo **Ambiente** non sia vuoto. In tal caso, impostarlo su una delle opzioni disponibili; in caso contrario, il componente aggiuntivo non funzionerà correttamente.  

Se si apportano modifiche al componente aggiuntivo, è necessario ricaricarlo per aggiornare la connessione. Per ricaricare, utilizzare il ![menu del componente aggiuntivo per Excel](media/excel-addin-menu.png "Menu del componente aggiuntivo per Excel") nell'angolo in alto a destra del componente aggiuntivo. Se non riesci a caricare l'add-in, parla con il tuo amministratore. Se sei l'amministratore, vedi [Ottenere il Business Central Add-in per Excel](admin-deploy-excel-addin.md).

> [!NOTE]
> L'add-in funziona con Excel per il web (online) da qualsiasi dispositivo, purché si usi un browser supportato. Funziona anche con l'applicazione Excel per Windows (PC), ma non per macOS.
>
> Per [!INCLUDE[prod_short](includes/prod_short.md)] in locale, l'azione **Modifica in Excel** è disponibile solo se il componente aggiuntivo di Excel è stato configurato dall'amministratore ed è disponibile solo per il client Web. Gli amministratori che desiderano installare il componente aggiuntivo di Excel possono consultare [Installazione del componente aggiuntivo di Excel per la modifica dei dati di Business Central](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).


<!-- Note for later: here we're immediately jumping to pretty advanced topics like changing company or reloading the addin. Fine to keep them for now. In the future, we will first need to explain in more detail the actual functionality of the addin, primarily these sub-sections:

Refreshing record data in Excel
Editing and publishing back to Business Central
Creating new records from Excel
Crafting your own editable Excel.
Point (4) is where it gets interesting for changing/specifying company, environment and other connection settings-->

### <a name="first-time-sign-in"></a>Primo accesso

L'azione **Modifica in Excel** richiede che l'add-in di Business Central sia installato in Excel. In alcuni casi, il tuo amministratore potrebbe aver impostato l'add-in per installarlo automaticamente per te. In questo caso, devi solo accedere a Business Central nel pannello **Add-in Excel** con il tuo nome utente e password. Altrimenti, si apre il riquadro **Nuovo componente aggiuntivo di Office** . Per installare l'add-in, scegli **Il componente aggiuntivo è attendibile**, che installerà l'add-in direttamente da Office Store.

Se per qualche motivo l'add-in non si installa, contatta il tuo amministratore o prova a installarlo manualmente. Per maggiori informazioni, vedi [Installare l'add-in manualmente per uso personale](admin-deploy-excel-addin.md#install).

## <a name="see-the-differences-between-the-options"></a>Vedere le differenze tra le opzioni
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-related-training-at-microsoft-learn"></a>Vedere le informazioni relative al training in [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Vedere anche

[Analisi dei rendiconti finanziari in Microsoft Excel](finance-analyze-excel.md)  
[Utilizzare Business Central](ui-work-product.md)  
[Miglioramenti all'integrazione di Excel nella seconda ondata di rilascio del 2019](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration)  


[!INCLUDE[footer-include](includes/footer-banner.md)]