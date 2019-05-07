---
title: Panoramica dei task per la configurazione dei processi di vendita | Documenti Microsoft
description: Descrive i task per impostare le regole e i valori per definire i criteri e processi di vendita.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, configure
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 6903744c1be0492267c8dee307e4b012aed4ffa4
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2019
ms.locfileid: "935544"
---
# <a name="setting-up-sales"></a>Setup Vendite
Prima di poter dare inizio alla gestione dei processi di vendita, è necessario configurare le regole e i valori che definiscono i criteri di vendita dell'azienda.

È necessario definire la configurazione generale, ad esempio i documenti di vendita richiesti e le modalità di registrazione dei rispettivi valori. Queste impostazioni generali vengono in genere eseguite una volta durante l'implementazione iniziale.

Una serie di attività specifiche correlate alla registrazione di nuovi clienti è quella di prendere nota di tutti gli accordi riguardanti sconti o prezzi speciali in essere con ogni cliente.

L'impostazione delle vendite correlata all'aspetto contabile, come i metodi di pagamento e le valute, è descritta nella sezione Impostazione degli aspetti finanziari. Per ulteriori informazioni, vedere [Impostazione di dati finanziari](finance-setup-finance.md).

| Per | Vedere |
| --- | --- |
| Creare una scheda cliente per ogni cliente a cui si effettua una vendita. |[Registrare nuovi clienti](sales-how-register-new-customers.md) |
| Consentire ai clienti di pagare tramite PayPal selezionando il logo di PayPal nei documenti di vendita. |[Abilitare i pagamenti clienti attraverso PayPal](sales-how-enable-payment-service-extensions.md) |
| Immettere sconti diversi e prezzi speciali che vengono concessi ai clienti a seconda dell'articolo, delle quantità e/o della data. |[Registrazione di prezzi, sconti e contratti di pagamento per le vendite](sales-how-record-sales-price-discount-payment-agreements.md) |
| Impostare gli agenti in modo da poterli assegnare ai contatti clienti o misurarne le prestazioni per calcolare la provvigione sulle vendite o il premio. |[Impostare gli agenti](sales-how-setup-salespeople.md) |
| Specificare per i singoli clienti o per tutti il modo in cui i documenti di vendita vengono inviati per impostazione predefinita quando si sceglie l'azione **Registra e invia**. |[Impostare profili di invio documenti](sales-how-setup-document-send-profiles.md) |
| Impostare l'e-mail in modo che includa un riepilogo delle informazioni nel documento di vendita che viene inviato. |[Inviare documenti via e-mail](ui-how-send-documents-email.md). |
|Utilizzare un servizio Web UE per verificare il numero di partita IVA del cliente.|[Verificare i numeri di partita IVA](finance-setup-vat.md)|
|Immettere le informazioni sui diversi fornitori di servizi di trasporto utilizzati, incluso un collegamento al relativo servizio che consente di rintracciare il collo.|[Impostare gli spedizionieri](sales-how-to-set-up-shipping-agents.md)|

## <a name="see-also"></a>Vedi anche
[Vendite](sales-manage-sales.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
