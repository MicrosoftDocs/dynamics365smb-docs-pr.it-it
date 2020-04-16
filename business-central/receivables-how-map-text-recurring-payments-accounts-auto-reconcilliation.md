---
title: Impostare la mappatura testo a conto per i pagamenti ricorrenti | Documenti Microsoft
description: Si può collegare il testo sui pagamenti con determinati conti, in modo che i pagamenti vengano registrati nei conti quando si effettua la registrazione riconciliazione pagamenti.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account linking, direct payment posting, automatic payment processing, reconcile payment, recurring expense, recurring cash receipt
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 01ca3f718ecf469d01d743d1277ce1abc0d6dcde
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2020
ms.locfileid: "3193733"
---
# <a name="map-text-on-recurring-payments-to-accounts-for-automatic-reconciliation"></a>Mappare il testo nei pagamenti ricorrenti a conti per la riconciliazione automatica
Nella pagina **Mappatura testo a conto** che si apre dalla pagina **Registrazione riconciliazione pagamenti**, è possibile impostare le mappature tra il testo sui pagamenti e specifici conti debiti, crediti e contropartita in modo da registrare questi pagamenti nei conti specificati durante la registrazione della riconciliazione pagamenti.

Una funzionalità simile esiste per riconciliare gli importi in eccesso nelle righe di riconciliazione pagamenti su base ad hoc. Per ulteriori informazioni, vedere [Riconciliare i pagamenti che non possono essere collegati automaticamente](receivables-how-reconcile-payments-cannot-apply-auto.md).

I pagamenti registrati in base alla mappa testo a conto non vengono collegati ai movimenti aperti, ma vengono solo registrati nei conti specificati, oltre alla creazione dei movimenti contabili di conti correnti bancari. Di conseguenza, la mappa testo a conto è adatta a incassi e spese ricorrenti, ad esempio acquisti frequenti di combustibile per auto o interessi e oneri bancari, che vengono riportati regolarmente sul rendiconto bancario e non necessitano di un documento commerciale collegato. Per ulteriori informazioni, vedere la sezione “Esempio: mappatura testo a conto per la spesa di combustibile” in questo argomento.

> [!NOTE]  
>   I pagamenti nelle righe della registrazione della riconciliazione vengono impostati per essere registrati solo in base alla mappa testo a conto, se la funzione automatica di collegamento può fornire solo un'affidabilità di corrispondenza di livello **Basso** o **Medio**. Se la funzione di collegamento automatico fornisce un'affidabilità di corrispondenza Alta, il pagamento viene automaticamente collegato a uno o più movimenti e non viene contabilizzato nei conti specificati nella pagina **Mappatura testo a conto**. In altre parole, un'affidabilità di corrispondenza di valore **Alto** oltrepassa una mappa testo a conto.

In una riga di registrazione riconciliazione pagamenti dove il pagamento è stato impostato per la registrazione in base alla mappatura testo a conto, il campo **Affidabilità corrispondenza** contiene **Alta - Mappatura testo a conto** e i campi **Tipo conto** e **Nr. conto** contengono i conti mappati.

## <a name="to-map-text-on-recurring-payments-to-accounts-for-automatic-reconciliation"></a>Mappare il testo nei pagamenti ricorrenti a conti per la riconciliazione automatica
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Registrazioni riconciliazione pagamenti** e quindi scegliere il collegamento correlato.
2. Aprire una registrazione della riconciliazione di pagamento. Per ulteriori informazioni, vedere [Riconciliare i pagamenti utilizzando il collegamento automatico](receivables-how-reconcile-payments-auto-application.md).
3. Scegliere l'azione **Mappa testo a conto**. Verrà aperta la pagina **Mappatura testo a conto**.
4. Nel campo **Mapping testo** immettere qualsiasi testo che appare nei pagamenti da registrare in specifici conti senza collegamento a un movimento aperto. È possibile immettere fino a 50 caratteri.

    > [!NOTE]  
    >   Se nessun altro pagamento esiste con il testo di mappatura in questione, la mappatura da testo a conto si verifica anche quando solo una parte del testo nel pagamento esiste come testo di mappatura.
5. Nel campo **Nr. fornitore** immetti il fornitore per cui i pagamenti verranno registrati.
6. Nel campo **Tipo di origine saldo** specificare se il pagamento viene registrato in un conto di contabilità generale o in un conto relativo a un cliente o un fornitore.
7. Nel campo **Nr. origine saldo** specificare il conto in cui il pagamento viene registrato, a seconda della selezione del campo **Tipo di origine saldo**.

    > [!NOTE]
    > Non usare i campi **Nr. conto dare** e **Nr. conto avere** in relazione alla riconciliazione di pagamento. Vengono utilizzati solo per i documenti in entrata. Per ulteriori informazioni, vedere [Utilizzare OCR per convertire PDF e file di immagine in documenti elettronici](across-how-use-ocr-pdf-images-files.md).

8. Ripetere i passaggi da 3 a 7 per tutto il testo presente nei pagamenti che si desidera mappare agli account per la registrazione diretta senza collegamento.

La volta successiva che si importa un file di rendiconto bancario o si sceglie l'azione **Collega automaticamente** nella pagina **Registrazioni riconciliazione pagamenti**, le righe di registrazione dei pagamenti che contengono il testo di mappatura specificato conterranno i conti mappati nei campi **Tipo conto** e **Nr. conto**. Il campo **Affidabilità corrispondenza** conterrà **Alta - Mappatura testo a conto**. Ciò a condizione che la funzione di collegamento automatico possa fornire solo un'affidabilità di corrispondenza di livello **Basso** o **Medio**.

## <a name="example-text-to-account-mapping-for-fuel-expense"></a>Esempio: mappatura testo a conto per la spesa di combustibile
Per registrare sempre le spese in combustibile effettuate presso i distributori Shell nella contabilità generale per la benzina (conto 8510), compilare una riga nella pagina **Mappatura testo a conto** come indicato di seguito.

| Mapping testo | Nr. conto dare | Nr. conto avere | Tipo di origine saldo | Nr. origine saldo |
| --- | --- | --- | --- | --- |
| Shell |VUOTO |8510 |Conti C/G |VUOTO |

## <a name="see-also"></a>Vedere anche
[Gestione della contabilità clienti](receivables-manage-receivables.md)  
[Vendite](sales-manage-sales.md)  
[Impostare il servizio Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md)  
[Personalizzazione di [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzando le estensioni](ui-extensions.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
