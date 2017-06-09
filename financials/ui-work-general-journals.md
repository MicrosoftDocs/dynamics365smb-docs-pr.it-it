---
title: Utilizzo delle registrazioni COGE | Documenti Microsoft
description: "Imparare a utilizzare le registrazioni di contabilità generale."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 02/03/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 13257a5d82d742d92fb22da9da7ff7f773d7d2f8
ms.contentlocale: it-it
ms.lasthandoff: 05/04/2017


---
# <a name="working-with-general-journals"></a>Utilizzo delle registrazioni COGE
Le registrazioni generali vengono utilizzate per la contabilizzazione nei conti C/G e in altri conti delle transazioni finanziarie, ad esempio i conti correnti bancari, i conti clienti e fornitori. La contabilizzazione mediante una registrazione generale crea sempre movimenti nei conti di contabilità generale. Ciò è vero anche quando, ad esempio, viene contabilizzata una riga di registrazione in un conto cliente, in quanto tramite una categoria di registrazione viene registrata una riga in un conto crediti nella contabilità generale.

[!INCLUDE[d365fin](includes/d365fin_md.md)] include anche registrazioni non di carattere finanziario, come le registrazioni magazzino e la registrazione inventario magazzino; tuttavia queste registrazioni non sono visibili nell'interfaccia utente.

Le informazioni immesse in una registrazione sono temporanee e possono essere modificate mentre si trovano nella registrazione. Quando si contabilizza la registrazione, le informazioni vengono trasferite a movimenti in singoli conti, dove non possono essere modificate. È tuttavia possibile scollegare i movimenti registrati e stornare o correggere i movimenti.

## <a name="journal-templates-and-batches"></a>Batch e definizioni di registrazioni
Esistono numerose definizioni registrazioni COGE. Ogni definizione registrazioni è rappresentata da una finestra dedicata con funzioni specifiche e campi necessari per supportare tali funzioni, ad esempio la finestra **Registrazione riconciliazione pagamenti** per elaborare i pagamenti bancari e la finestra **Registrazioni pagamenti** per pagare i fornitori.

**Nota**: se si esportano file di pagamento nella banca dalle registrazioni dei pagamenti, è necessario selezionare la casella di controllo **Consenti esportazione pagamento** per il batch di registrazioni in questione nella finestra **Batch registrazioni COGE**. Per ulteriori informazioni, vedere [Procedura: Esportare pagamenti in un file della banca](payables-how-export-payments-bank-file.md).

Per ogni definizione registrazioni è possibile impostare le proprie registrazioni personali come batch registrazioni. Ad esempio, è possibile definire dei batch registrazioni personali per le registrazioni pagamenti che abbiano delle impostazioni e un layout personali.

Un esempio di impostazione personale per la definizione del batch registrazioni COGE consiste nella compilazione automatica dei campi degli importi da parte del sistema. Se si seleziona la casella di controllo **Suggerisci importo contropartita** nella riga per il proprio batch nella finestra **Batch registrazioni COGE**, il campo **Importo** ad esempio nelle righe di registrazione COGE per lo stesso numero di documento viene precompilato automaticamente con il valore richiesto per saldare il documento. Per ulteriori informazioni, vedere [Suggerimento automatico dei valori in [!INCLUDE[d365fin](includes/d365fin_md.md)]] (ui-let-system-suggest-values.md).

## <a name="main-accounts-and-balancing-accounts"></a>Conti principali e contropartita
Se sono state impostate contropartite predefinite per i batch di registrazioni, il conto di contropartita verrà compilato automaticamente quando si inserisce un valore nel campo **Nr. conto** . In caso contrario, occorre compilare sia il campo **Nr. conto** che il campo **Contropartita** manualmente. Un importo positivo nel campo **Importo** viene addebitato sul conto principale e accreditato nella contropartita. Un importo negativo viene accreditato sul conto principale e addebitato nella contropartita.

**Nota**: l'IVA viene calcolata separatamente per il conto principale e il conto di contropartita, quindi possono essere utilizzate percentuali IVA diverse.

## <a name="recurring-journals"></a>Registrazioni periodiche
Una registrazione periodica è una registrazione generale con campi specifici per la gestione di transazioni registrate frequentemente con poche o nessuna modifica. Se si utilizzano questi campi per le transazioni ricorrenti, è possibile registrare sia gli importi fissi sia quelli variabili. È inoltre possibile specificare i movimenti di storno automatico il giorno successivo alla data di registrazione e utilizzare chiavi di allocazione con i movimenti periodici.

## <a name="see-also"></a>Vedi anche
[Procedura: Utilizzare le chiavi di allocazione nelle registrazioni COGE](ui-how-use-allocation-keys-general-journals.md)  
[Finanza](finance.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

