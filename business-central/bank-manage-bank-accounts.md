---
title: Gestire i conti correnti bancari| Documenti Microsoft
description: È necessario riconciliare regolarmente i movimenti contabili bancari con le transazioni bancarie correlate nei conti bancari.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reconcile
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 050519c77f7c1dca5dd451a57ac47f71b4803a91
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2020
ms.locfileid: "3186190"
---
# <a name="reconciling-bank-accounts"></a>Riconciliazione dei conti correnti bancari
Una riconciliazione bancaria deve essere completata a intervalli regolari per tutti i conti bancari al fine di garantire che i registri di cassa dell'azienda siano corretti. È possibile farlo confrontando e abbinando i movimenti nei conti bancari interni con le transazioni bancarie presso la banca, quindi registrando i saldi sui conti bancari interni per rendere i totali disponibili ai gestori finanziari. La riconciliazione bancaria è anche un modo pratico per scoprire e risolvere i pagamenti mancanti e gli errori di contabilità.

È possibile eseguire l'attività nella pagina **Riconciliazioni C/C bancari** in cui associare (riconciliare) le righe del rendiconto bancario nel riquadro a sinistra con i movimenti contabili interni del conto corrente nel riquadro di destra. In alternativa, è possibile eseguire l'attività come parte dell'elaborazione dei pagamenti rappresentati in un estratto conto bancario nella pagina **Registrazione riconciliazione pagamenti**. In entrambe le pagine è possibile compilare le informazioni sull'estratto conto bancario importando un file o feed ed è possibile utilizzare i suggerimenti automatici di corrispondenza.

> [!NOTE]  
> Nelle versioni per il Nord America è possibile eseguire la riconciliazione bancaria nella pagina **Prospetto riconciliazione bancaria**, più adatta per assegni e depositi ma non offre l'importazione di file di rendiconti bancari. Per utilizzare questa finestra al posto della pagina **Riconciliazioni C/C bancari**, deselezionare il campo **Riconciliazione bancaria con collegamento automatico** nella pagina **Setup contabilità generale**. Per ulteriori informazioni, vedere “Riconciliazione dei conti correnti bancari" nella funzionalità locale per gli Stati Uniti.

Prima di poter gestire i conti correnti bancari in [!INCLUDE[d365fin](includes/d365fin_md.md)], è necessario impostare ogni conto bancario come scheda conto corrente bancario. Inoltre, è necessario impostare i servizi elettronici che è possibile utilizzare per l'importazione dell'estratto conto bancario e l'esportazione del file di pagamento. Per ulteriori informazioni, vedere [Impostare i conti correnti bancari](bank-setup-banking.md).

Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.

| A | Vedere |
| --- | --- |
| Riconciliare i conti bancari come attività separata nella pagina **Riconciliazioni C/C bancari**. |[Riconciliazione dei conti correnti bancari](bank-how-reconcile-bank-accounts-separately.md) |
| Riconciliare i conti correnti bancari in relazione all'elaborazione dei pagamenti nella pagina **Registrazione riconciliazione pagamenti**. |[Collegare i pagamenti automaticamente e riconciliare i conti correnti bancari](receivables-apply-payments-auto-reconcile-bank-accounts.md) |

## <a name="see-related-training-at-microsoft-learn"></a>Vedere le informazioni relative al training in [Microsoft Learn](/learn/paths/reconcile-bank-accounts-dynamics-365-business-central/)

## <a name="see-also"></a>Vedere anche
[Impostazione delle attività bancarie](bank-setup-banking.md)  
[Trasferimento di fondi bancari](bank-how-transfer-bank-funds.md)  
[Gestione della contabilità clienti](receivables-manage-receivables.md)  
[Gestione della contabilità fornitori](payables-manage-payables.md)    
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Funzionalità aziendali generali](ui-across-business-areas.md)
