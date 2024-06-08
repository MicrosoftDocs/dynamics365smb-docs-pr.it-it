---
title: Modificare l'aspetto di un report selezionando un layout diverso
description: È possibile utilizzare diversi layout per un report e passate tra i layout per modificare l'aspetto di un report.
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '9652, 9650'
ms.date: 03/07/2022
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# <a name="legacy-set-the-layout-used-by-a-report"></a>(Legacy) Impostare il layout utilizzato da un report

[!INCLUDE[legacy-custom-layouts](includes/legacy-custom-layouts.md)]

Un report può essere impostato con diversi layout di report, che è possibile alternare a seconda delle necessità.

In base ai layout disponibili per un report, è possibile scegliere di utilizzare un layout di report RDLC o Word predefinito o un layout personalizzato. Per ulteriori informazioni sui layout di report RDLC e Word, sui layout personalizzati integrati e altro ancora, vedere [Gestire i layout dei report](ui-manage-report-layouts.md).

Quando vengono definiti layout di report personalizzati, è possibile selezionarli da schede cliente e fornitore per specificare che i layout selezionati verranno utilizzati per documenti creati per il cliente o il fornitore in questione. Per ulteriori informazioni, vedere [Definire layout di documenti per clienti e fornitori](ui-define-customer-vendor-document-layouts.md).

> [!TIP]  
> I report documento (non elenchi) che utilizzano un layout report Word sono in genere più rapidi di quelli che utilizzano un layout report RDLC. Quindi, se si ha la possibilità di scegliere tra un layout report Word o RDLC per un report documento, utilizzare il report layout Word per ottenere le migliori prestazioni.

## <a name="to-change-which-report-layout-to-use-for-a-report-or-document"></a>Per modificare il layout di report da utilizzare per un report o un documento

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Selezione layout report**, quindi scegli il collegamento correlato.
  
   Nella pagina **Selezione layout report** sono elencati tutti i report disponibili per la società specificata nel campo **Società** nella parte superiore della pagina. Il campo **Descrizione layout** <!-- **Selected Layout** -->specifica il layout che attualmente è utilizzato nel report.
2. Imposta il campo **Società** nella parte superiore della pagina sulla società che include il report.

   Questo campo consente di impostare layout diversi per lo stesso report in società diverse.

3. Per modificare il layout utilizzato da un report, nella riga del report, impostare il campo **Layout selezionato** su una delle seguenti opzioni:
   * **RDLC (predefinito)** utilizza il layout di report RDLC integrato nel report.
   * **Word (predefinito)** utilizza il layout di report Word integrato nel report.
   * **Personalizzato** utilizza nel report un layout personalizzato.  

> [!NOTE]
> Se si sceglie un layout di report di tipo **RDLC (predefinito)** o **Word (predefinito)** e si visualizza un messaggio di errore che indica che il report non dispone di un layout del tipo specificato, è necessario selezionare un'altra opzione di layout o creare un layout di report personalizzato del tipo che si desidera utilizzare. Vedere la procedura seguente.

Se è stato selezionato un layout di report RDLC o Word predefinito, non sono necessarie ulteriori azioni e il layout verrà utilizzato alla successiva esecuzione del report.

## <a name="to-change-the-custom-layout-to-use-for-a-report-layout"></a>Per modificare il layout personalizzato da utilizzare per un layout di report

È anche possibile che si intenda modificare il layout personalizzato attualmente utilizzato. Per ulteriori informazioni, vedere [Creare e modificare layout di report personalizzati](ui-how-create-custom-report-layout.md).

Tutti i layout di report personalizzati esistenti per layout di report in una società sono elencati nella pagina **Layout di report personalizzati**. Nella pagina **Selezione layout report** è possibile visualizzare i layout personalizzati disponibili per ogni report nel Dettaglio informazioni **Report personalizzati**.

1. Nella pagina **Selezione layout report**, sulla riga per il layout di report che si desidera modificare, scegliere il pulsante di ricerca nel campo **Descrizione layout personalizzato**.
2. Nella pagina **Layout report personalizzati** selezionare la riga per il layout personalizzato che si desidera utilizzare, quindi scegliere **OK**.

Il nome del layout personalizzato selezionato è ora visualizzato nel campo **Descrizione layout personalizzato** e verrà utilizzato la volta successiva che il report o il documento viene visualizzato in anteprima, stampato o inviato.

Ora è possibile andare alle schede cliente e fornitore per specificare quali layout utilizzare per diversi documenti creati per il cliente o il fornitore in questione, come conferme di ordini o solleciti di pagamento. Per ulteriori informazioni, vedere [Definire layout di documenti per clienti e fornitori](ui-define-customer-vendor-document-layouts.md).

## <a name="see-also"></a>Vedi anche
[Gestione dei layout di report](ui-manage-report-layouts.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
