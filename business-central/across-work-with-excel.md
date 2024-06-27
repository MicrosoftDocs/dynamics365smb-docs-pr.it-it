---
title: Visualizzare e modificare in Excel da Business Central
description: Informazioni su come aprire le pagine in Microsoft Excel da Business Central per una migliore analisi dei dati.
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.form: 1480
ms.search.keywords: 'accountant, accounting, financial report'
ms.date: 06/13/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---
# <a name="view-and-edit-in-excel-from-business-central"></a>Visualizzare e modificare in Excel da Business Central

Con le pagine che visualizzano una lista di record in righe e colonne, come una lista di clienti, ordini di vendita o fatture, è possibile esportare la lista in Microsoft Excel, e visualizzarla lì. A seconda della pagina, hai due opzioni per la visualizzazione in Excel. Entrambe le opzioni sono disponibili dall'icona **Condividi**  ![Condividi una pagina in un'altra app.](media/share-icon.png) all'inizio di una pagina. È possibile selezionare l'azione **Apri in Excel** o l'azione **Modifica in Excel** nella pagina. Questo articolo spiega le due azioni.

## <a name="open-in-excel"></a>Apri in Excel

Con l'azione **Apri in Excel** puoi apportare modifiche ai record in Excel, ma non puoi ripubblicare le modifiche in [!INCLUDE[prod_short](includes/prod_short.md)]. È possibile salvare solo le modifiche al file Excel, senza influenzare i dati in [!INCLUDE[prod_short](includes/prod_short.md)].

- Con questa azione, Excel rispetta tutti i filtri nella pagina che limitano i record visualizzati. La cartella di lavoro Excel conterrà le stesse righe e colonne presenti nella pagina in [!INCLUDE[prod_short](includes/prod_short.md)].

- Questa azione è compatibile con Windows e macOS.
- [!INCLUDE[open-edit-excel](includes/open-and-edit-excel.md)]

<!-- 
> [!IMPORTANT]
> For [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, the **Open in Excel** action is available by default. However, if you set up [!INCLUDE[prod_short](includes/prod_short.md)] on-premises for editing data in Excel, then the **Open in Excel** action is replaced by the **Edit in Excel** action.-->

[!INCLUDE [send-report-excel](includes/send-report-excel.md)] 

> [!NOTE]
> In Excel, i numeri interi nelle colonne avranno un simbolo decimale alla fine (come un punto `.` o una virgola `,`) anche se il simbolo decimale non viene visualizzato in Business Central. Il simbolo decimale dipende dalle impostazioni della regione del tuo dispositivo. Ad esempio, `10` in Business Central potrebbe apparire come `10.` o `10,` in Excel. È possibile modificare il formato in Excel selezionando i valori, quindi selezionando <kbd>CTRL</kbd>+<kbd>1</kbd>. Per ulteriori informazioni sulla modifica del formato dei numeri in Excel, vai a [Formato dei numeri](https://support.microsoft.com/office/format-numbers-f27f865b-2dc5-4970-b289-5286be8b994a).

## <a name="edit-in-excel"></a>Modifica in Excel

L'azione **Modifica in Excel** è disponibile nella maggior parte delle liste, ma non in tutte. Con l'azione **Modifica in Excel** puoi apportare modifiche ai record in Excel e poi puoi ripubblicare le modifiche in [!INCLUDE[prod_short](includes/prod_short.md)]. Quando Excel si apre, vedrai il pannello **Add-in Excel** sulla destra.

- Con questa azione, Excel rispetta la maggior parte dei filtri sulla pagina che limitano i record visualizzati, quindi la cartella di lavoro di Excel conterrà quasi gli stessi record e colonne.

- Per ottenere gli ultimi dati da [!INCLUDE[prod_short](includes/prod_short.md)], scegli **Aggiorna** nel pannello del componente aggiuntivo di Excel.
- [!INCLUDE[open-edit-excel](includes/open-and-edit-excel.md)]

### <a name="first-time-sign-in"></a>Primo accesso

L'azione **Modifica in Excel** richiede che l'add-in di Business Central sia installato in Excel. In alcuni casi, il tuo amministratore potrebbe aver impostato l'add-in per installarlo automaticamente per te. In questo caso, devi solo accedere a Business Central nel pannello **Add-in Excel** con il tuo nome utente e password. Altrimenti, si apre il riquadro **Nuovo componente aggiuntivo di Office** . Per installare l'add-in, scegli **Il componente aggiuntivo è attendibile**, che installerà l'add-in direttamente da Office Store.

Se il componente aggiuntivo non si installa, contatta il tuo amministratore o prova a installarlo manualmente. Per maggiori informazioni, vedi [Installare l'add-in manualmente per uso personale](admin-deploy-excel-addin.md#install).

### <a name="work-across-environments-and-companies"></a>Utilizzo di ambienti e società

Puoi cambiare la compagnia con cui stai lavorando. Per cambiare azienda, seleziona l'icona **Opzioni** ![Opzioni del componente aggiuntivo di Excel.](media/cogwheel.png "Opzioni del componente aggiuntivo per Excel") nel riquadro del componente aggiuntivo di Excel, quindi seleziona l'azienda dal campo **Società**.  

> [!IMPORTANT]
> Quando si cambia la società, assicurarsi che il campo **Ambiente** non sia vuoto. In tal caso, impostarlo su una delle opzioni disponibili; in caso contrario, il componente aggiuntivo non funzionerà correttamente.  

Se si apportano modifiche al componente aggiuntivo, è necessario ricaricarlo per aggiornare la connessione. Per ricaricare, utilizzare il ![menu del componente aggiuntivo per Excel](media/excel-addin-menu.png "Menu del componente aggiuntivo per Excel") nell'angolo in alto a destra del componente aggiuntivo. Se non riesci a caricare l'add-in, parla con il tuo amministratore. Se sei l'amministratore, vedi [Ottenere il Business Central Add-in per Excel](admin-deploy-excel-addin.md).

> [!NOTE]
> L'add-in funziona con Excel per il web (online) da qualsiasi dispositivo, purché si usi un browser supportato. Funziona anche con l'applicazione Excel per Windows (PC), ma non per macOS.
>
> Per [!INCLUDE[prod_short](includes/prod_short.md)] in locale, l'azione **Modifica in Excel** è disponibile solo se il componente aggiuntivo di Excel è stato configurato dall'amministratore ed è disponibile solo per il client Web. Gli amministratori che desiderano installare il componente aggiuntivo di Excel possono consultare [Installazione del componente aggiuntivo di Excel per la modifica dei dati di Business Central](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).

### <a name="limits-when-using-excel-for-the-web"></a>Limiti quando si utilizza Excel per il Web

Quando **Modifica in Excel** viene utilizzato nelle pagine elenco per tabelle con molte colonne, la cartella di lavoro risultante potrebbe avere troppe colonne per consentire la visualizzazione del file in Excel per il Web. [!INCLUDE[prod_short](includes/prod_short.md)] limita automaticamente la cartella di lavoro esportata a 100 colonne quando OneDrive è configurato per le funzioni del sistema. 

<!--## See the differences between the options
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]-->

## <a name="see-also"></a>Vedere anche

[Analisi dei rendiconti finanziari in Microsoft Excel](finance-analyze-excel.md)  
[Utilizzare Business Central](ui-work-product.md)  
[Miglioramenti all'integrazione di Excel nella seconda ondata di rilascio del 2019](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
