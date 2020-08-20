---
title: Convalidare un numero di partita IVA | Microsoft Docs
description: Convalidare un numero di partita IVA
author: andregu
ms.service: dynamics365-business-central
ms.topic: article
ms.reviewer: edupont
ms.search.keywords: VAT, posting, tax, value-added tax
ms.date: 07/21/2020
ms.author: andregu
ms.openlocfilehash: 9624a51f040ae6231d9d0354cb0c571287ccd3e8
ms.sourcegitcommit: e22666f90262c7d2084ca6c74ca7d66652fc6df6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/23/2020
ms.locfileid: "3617290"
---
# <a name="validate-a-vat-registration-number"></a>Convalidare un numero di partita IVA

È importante che la partita IVA per clienti, fornitori e contatti sia valida. Ad esempio, le aziende cambiano talvolta lo stato di passività fiscale e in alcuni paesi le autorità fiscali potrebbero chiedere di fornire report, come il report IVA dell'elenco vendite UE, che elenca i numeri di partita IVA utilizzati per l'attività.

La Commissione Europea offre un servizio di convalida dei numeri di partita IVA (VIES) tramite il proprio sito Web, che è pubblico e libero. [!INCLUDE[d365fin](includes/d365fin_md.md)] consente di risparmiare tale passaggio e di utilizzare il servizio VIES per convalidare e tracciare i numeri IVA per i clienti, i fornitori e i contatti direttamente dalle schede cliente, venditore e di contatto. Il servizio in [!INCLUDE[d365fin](includes/d365fin_md.md)] è denominato **servizio di convalida partita IVA comunitaria**. Il servizio è disponibile nella pagina **Connessioni servizio** e sarà possibile iniziare a utilizzarlo da subito. La connessione del servizio è gratuita e la registrazione non è necessaria.

## <a name="to-verify-vat-registration-numbers"></a>Per verificare la partita IVA

Per abilitare il **Setup servizio di convalida partita IVA comunitaria** aprire la voce nella pagina **Connessione servizio**. Il campo **Endpoint servizio** è già popolato. In caso contrario, è possibile utilizzare l'azione **Imposta endpoint di default**. Quindi impostare il campo **Abilitato** ed è possibile proseguire.

> [!NOTE]
> Per abilitare il servizio di convalida partita IVA comunitaria, è necessario disporre di autorizzazioni di amministratore.

Quando si utilizza la connessione del servizio, viene registrata una cronologia dei numeri di partita IVA e delle verifiche per ogni cliente, fornitore o contatto, nel **Log partita IVA**, in modo da poterli facilmente tracciare. Il log è specifico per ogni cliente. Ad esempio, il log è utile per dimostrare di aver verificato che il numero di partita IVA corrente è corretto. Quando si verifica un numero di partita IVA, la colonna **Identificatore di richiesta** nel log indicherà che l'azione è stata eseguita.

È possibile visualizzare il log di registrazione IVA nella scheda cliente, fornitore o di contatto, nella Scheda dettaglio **Fatturazione**, scegliendo il pulsante di ricerca nel campo **Partita IVA**.  

Il servizio consente anche di risparmiare tempo quando si crea un cliente o un fornitore. Se si conosce il numero di partita IVA del cliente, è possibile immetterlo nel campo **Partita IVA** nelle schede Cliente o Fornitore e la ragione sociale del cliente verrà compilato automaticamente. Alcuni paesi forniscono anche indirizzi aziendali in un formato strutturato. In questi paesi, l'indirizzo verrà compilato automaticamente.  

Ci sono un paio di cose da notare sul servizio di convalida dei numeri di partita IVA VIES:

* Il servizio Web utilizza il protocollo HTTP, il che significa che i dati trasferiti tramite il servizio non sono crittografati.  
* È possibile che si verifichi un tempo di inattività per questo servizio per cui Microsoft non è responsabile. Il servizio fa parte di un'ampia rete europea di registri IVA nazionali.

> [!IMPORTANT]
> È responsabilità dell'utente verificare che i dati siano validi. A volte, i dati con errori vengono restituiti dal servizio di convalida dei numeri di partita IVA VIES. Se la convalida non riesce, convalidare i numeri di partita IVA nel [sito Web](https://ec.europa.eu/taxation_customs/vies/), stampare il risultato o salvarlo in una posizione condivisa, quindi aggiungere il collegamento al record per il cliente, il fornitore o il contatto. Per ulteriori informazioni, vedere [Gestire allegati, collegamenti e note in schede e documenti](ui-how-add-link-to-record.md).

## <a name="see-also"></a>Vedere anche

[Impostare l'IVA (imposta sul valore aggiunto)](finance-setup-vat.md)  
[Setup dell'IVA ad esigibilità differita](finance-setup-unrealized-vat.md)  
[Dichiarare l'IVA a un'autorità fiscale](finance-how-report-vat.md)  
[Utilizzare l'IVA nelle vendite e negli acquisti](finance-work-with-vat.md)  
[Funzionalità locale in Business Central](about-localization.md)  
