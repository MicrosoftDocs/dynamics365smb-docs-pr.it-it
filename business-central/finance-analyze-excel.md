---
title: Utilizzare le sintesi finanziarie in Excel
description: Informazioni su come aprire i rendiconti finanziari in Microsoft Excel da Business Central per una migliore analisi.
author: edupont04
ms.topic: overview
ms.search.keywords: 'accountant, accounting, financial report'
ms.search.form: 9027
ms.date: 08/23/2022
ms.author: edupont
---
# <a name="analyzing-financial-statements-in-microsoft-excel" />Analisi dei rendiconti finanziari in Microsoft Excel

[!INCLUDE [prod_short](includes/prod_short.md)] fornisce i KPI e le panoramiche dei dati finanziari della tua azienda. Di seguito sono riportati esempi di modi per analizzare KPI e panoramiche in Excel:

* Apri gli elenchi in Excel e analizza i dati. 
* Esporta i rendiconti finanziari complessi, ad esempio il conto patrimoniale o il conto economico in Excel, analizza i dati e stampa i report.  

> [!TIP]
> Per impostazione predefinita, i report che puoi visualizzare in Excel sono progettati per aiutarti ad analizzare l'anno in corso. Il report conto economico è tuttavia un'eccezione. Tale report ti consente di filtrare i dati per includere gli anni precedenti nelle tue analisi.

## <a name="getting-the-overview-and-the-details-in-excel" />Visualizzazione di una panoramica e dei dettagli in Excel

Nella Gestione ruolo utente di Manager aziendale e Contabile, l'azione **Report** consente di scegliere i rendiconti finanziari da visualizzare in Excel. Quando si sceglie un rendiconto, questo viene aperto in Excel o Excel Online. Un componente aggiuntivo connette i dati a [!INCLUDE [prod_short](includes/prod_short.md)]. È tuttavia necessario connettersi con lo stesso account che si utilizza con [!INCLUDE [prod_short](includes/prod_short.md)]. La tabella seguente elenca i report e dove sono disponibili.  


|Report  |Gestione ruolo utente  |
|---------|---------|
|Conto patrimoniale                 | Manager aziendale, Contabile |
|Conto economico              | Manager aziendale, Contabile |
|Rendiconto dei flussi di cassa       | Manager aziendale, Contabile |
|Rendiconto degli utili non distribuiti| Manager aziendale, Contabile |
|IVA riscossa         | Manager aziendale, Contabile |
|Rendiconti cliente           | Manager aziendale, Contabile |
|Scadenziario fornitori         | Addetto contabile |
|Scadenziario clienti      | Addetto contabile |

Si supponga di voler analizzare meglio il flusso di cassa. Nella Gestione ruolo utente Contabile o Manager aziendale, è possibile aprire il report **Rendiconto dei flussi di cassa** in Excel, ma ciò che avviene realmente è che vengono esportati i dati pertinenti e viene creata una cartella di lavoro di Excel in base a un modello predefinito. A seconda del browser, potrebbe essere chiesto di salvare o aprire la cartella di lavoro.  

In Excel è disponibile una scheda in cui i dati sono disposti automaticamente nel primo foglio di lavoro. Tutti i dati che sono stati esportati sono inoltre presenti in altri fogli di lavoro in caso di necessità. È possibile stampare il report immediatamente o modificarlo fino a ottenere la sintesi e i dettagli desiderati. Utilizzare il componente aggiuntivo per Excel [!INCLUDE [prod_short](includes/prod_short.md)] per filtrare e analizzare ulteriormente i dati.  

### <a name="understanding-the-excel-templates" />Comprendere i modelli di Excel

I report di Excel predefiniti si basano sui dati dell'azienda attuale. Ad esempio, la società di dimostrazione ha impostato il piano dei conti per elencare tre conti di cassa sotto *Cespiti correnti* : 10100 **Conto assegni**, 10200 **Conto di risparmio** e 10300 **Piccola cassa**. I conti hanno il campo **Sottocategoria conto** impostato su *Cassa* e l'importo combinato che viene visualizzato come *Cassa* nel report di Excel **Conto patrimoniale**.  

Altri fogli nella cartella di lavoro di Excel mostrano i dati utilizzati per il report. Per scoprire cosa c'è dietro i raggruppamenti nei report di Excel, potrebbe essere necessario filtrare gli elenchi in [!INCLUDE [prod_short](includes/prod_short.md)].  

## <a name="the--excel-add-in" />Componente aggiuntivo per Excel [!INCLUDE [prod_short](includes/prod_short.md)]

L'esperienza [!INCLUDE [prod_short](includes/prod_short.md)] include un componente aggiuntivo per Excel. A seconda della sottoscrizione, esegui l'accesso automaticamente oppure devi specificare i dettagli di accesso per [!INCLUDE [prod_short](includes/prod_short.md)]. Per ulteriori informazioni, vedere [Visualizzare e modificare in Excel da Business Central](across-work-with-excel.md).  

Il componente aggiuntivo ti consente di ottenere dati aggiornati da [!INCLUDE [prod_short](includes/prod_short.md)], e importare nuovamente le modifiche in [!INCLUDE [prod_short](includes/prod_short.md)]. Tuttavia, la funzionalità che consente di importare nuovamente i dati nel database non è disponibile per i report finanziari di Excel.  

## <a name="see-related-microsoft-training" />Vedi il relativo [training Microsoft](/training/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also" />Vedi anche

[Visualizzare e modificare in Excel da Business Central](across-work-with-excel.md)  
[Finanze](finance.md)  
[Impostazione di dati finanziari](finance-setup-finance.md)  
[Contabilità generale e piano dei conti](finance-general-ledger.md)  
[Utilizzare Business Central](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
