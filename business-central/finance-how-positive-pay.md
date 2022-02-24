---
title: Esportare file Positive Pay| Documenti Microsoft
description: Assicurarsi che la banca compensi solo gli assegni e gli importi convalidati tramite l'esportazione di file Positive Pay che contengano informazioni sul fornitore e pagamento.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: check, clearing
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: d1a7922895e357e51ba66dd8853961300a8fcc6c
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2020
ms.locfileid: "3183630"
---
# <a name="export-a-positive-pay-file"></a>Esportare un file Positive Pay
Per assicurarsi che la banca compensi solo gli assegni e gli importi convalidati, è possibile esportare un file Positive Pay con informazioni su fornitore, numero di assegno e importo del pagamento da inviare alla banca per riferimento quando si elaborano i pagamenti.

[!INCLUDE[d365fin](includes/d365fin_md.md)] è preconfigurato per supportare i file Positive Pay per Bank of America e City Bank.

## <a name="to-set-up-a-bank-account-for-positive-pay"></a>Per impostare un conto bancario per i file Positive Pay
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Conti correnti bancari** e quindi scegliere il collegamento correlato.
2. Aprire la scheda della banca per cui si desidera utilizzare il Positive Pay.
3. Nel campo **Codice esportazione Positive Pay** immettere POSPAYBANK.
4. Chiudere la pagina.

## <a name="to-export-a-positive-pay-file"></a>Per esportare un file Positive Pay
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Conti correnti bancari** e quindi scegliere il collegamento correlato.
2. Selezionare il conto bancario per cui si desidera esportare un file Positive Pay.
3. Scegliere l'opzione **Esportazione Positive Pay**.

    Verrà visualizzata la pagina **Esportazione Positive Pay** che mostra i pagamenti che sono stati effettuati per il conto bancario dalla data dell'ultimo caricamento, come mostrato nei campi **Data ultimo caricamento** e **Data ultimo caricamento**.
4. Nel campo **Data limite caricamento** specificare una data prima della quale i pagamenti non sono inclusi nel file esportato.
5. Scegliere l'azione **Esporta**.
6. Nella pagina **Esporta file** scegliere il pulsante **Salva**, quindi salvare il file in un percorso appropriato.
7. Caricare il file nel sito elettronico della banca.
8. Annotare o copiare il numero di conferma visualizzato quando il file viene caricato.

Per visualizzare i record Positive Pay esportati

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Conti correnti bancari** e quindi scegliere il collegamento correlato.
2. Selezionare il conto bancario per cui si desidera visualizzare i record di esportazione Positive Pay.
3. Scegliere l'azione **Movimenti Positive Pay**.

    Nella pagina **Movimenti Positive Pay** è possibile visualizzare tutti i record di esportazione Positive Pay per il conto corrente bancario.
4. Nel campo **Numero di conferma** immettere per ogni record esportare il numero di conferma che si riceve quando il caricamento del file alla banca è riuscito.
5. Per visualizzare le righe di pagamento, scegliere l'azione **Dettagli movimenti Positive Pay**.

Per riesportare file Positive Pay

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Conti correnti bancari** e quindi scegliere il collegamento correlato.
2. Selezionare il conto bancario per cui si desidera riesportare i file Positive Pay.
3. Scegliere l'azione **Movimenti Positive Pay**.
4. Selezionare la riga per il file di esportazione Positive Pay da riesportare.
5. Nella pagina **Movimenti Positive Pay** selezionare l'azione **Riesporta Positive Pay su file**.

## <a name="see-also"></a>Vedi anche
[Finanze](finance.md)  
[Impostazione di dati finanziari](finance-setup-finance.md)  
[Utilizzo delle registrazioni COGE](ui-work-general-journals.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
