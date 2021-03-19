---
title: Domande frequenti sulle app per dispositivi mobili
description: Risposte alle domande frequenti sull'utilizzo di Business Central con un telefono o un tablet.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: phone, tablet
ms.date: 10/15/2020
ms.author: edupont
ms.openlocfilehash: 3b00eb417f2e51d87a58885a50e1262150837d93
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5385451"
---
# <a name="mobile-apps-faq"></a>Domande frequenti sulle app per dispositivi mobili

Questo articolo contiene le risposte alle domande più comuni poste dai nostri utenti esperti sulle app per dispositivi mobili per [!INCLUDE [prod_short](includes/prod_short.md)].  

## <a name="is-there-an-app-for-my-device"></a>Esiste un'app per il mio dispositivo?

Probabilmente. Installare l'app [!INCLUDE[prod_short](includes/prod_short.md)] sul dispositivo mobile scaricandola da Windows Store, App Store o Google Play.

- [Windows Store](https://go.microsoft.com/fwlink/?LinkId=734848) (solo PC)
- [App Store](https://go.microsoft.com/fwlink/?LinkId=734847)
- [Google Play](https://go.microsoft.com/fwlink/?LinkId=734849)

## <a name="is-it-the-same-experience-in-the-apps-as-in-the-browser"></a>L'esperienza con le app e identica a quella con il browser?

No, non esattamente. Ad esempio, a livello di app viene visualizzato solo il gruppo attività **Home** a causa delle dimensioni di schermo limitate sui dispositivi mobili. Inoltre, i tasti di scelta rapida non sono disponibili poiché si utilizza principalmente il tocco anziché una tastiera per navigare nei dispositivi mobili.

La tabella seguente descrive alcune delle differenze e delle limitazioni più comuni riscontrabili durante l'utilizzo di [!INCLUDE [prod_short](includes/prod_short.md)] nei dispositivi mobili rispetto al browser.

| Concetto | Su tablet | Su telefoni | Esempio nel browser |
|--|--|--|--|
| Gruppi attività | È visualizzato solo il gruppo attività **Home**. | È visualizzato solo il gruppo attività **Home**. | **Home** e **Documenti registrati** nella gestione ruolo utente `Sales Order Processor`. |  |
| Selezione di più record negli elenchi | Non disponibile. | Non disponibile. | `Ctrl+A` o `Ctrl+Click` sulle righe in un elenco nel browser. |
| Azioni nella barra delle azioni | Sono visualizzate solo le azioni essenziali. | Sono visualizzate solo le azioni essenziali. |  |
| Riquadri Dettaglio informazioni | Non visualizzati nelle pagine di elenco o nelle pagine di prospetto. | Non visualizzati nelle pagine di elenco o nelle pagine di prospetto. | Elenco `Customer` nella gestione ruolo utente `Small Business` |
| Filtri avanzati | Non è disponibile alcun filtro specifico per le colonne. | Non è disponibile alcun filtro specifico per le colonne. | Nella pagina di elenco `Customer`. |
| Funzionalità delle informazioni | Non ancora disponibile. | Non ancora disponibile. | Vedi [Individuare pagine e informazioni con la funzionalità delle informazioni](ui-search.md). |  |
| Esplora ruoli | Non ancora disponibile. | Non ancora disponibile. | Vedi [Ricerca di pagine con Esplora ruoli](ui-role-explorer.md). |
| Campi nelle Schede dettaglio | I campi nelle Schede dettaglio delle pagine di elenco non sono visualizzati. Nell'area del contenuto della pagina è visualizzato solo il controllo ripetitore. | Non disponibile. |  |
| Seleziona da elenco completo | Non disponibile nelle ricerche. Gli utenti non sono in grado di eseguire azioni in una pagina di ricerca e non possono accedere al set di record completo. | Non disponibile nelle ricerche. Gli utenti non sono in grado di eseguire azioni in una pagina di ricerca e non possono accedere al set di record completo. | Sulla `Item Card` quando si seleziona **Unità di misura base**. |
| Ricerca nelle colonne dell'elenco | Supportato parzialmente. La ricerca non includerà FlowField. | Supportato parzialmente. La ricerca non includerà FlowField. | Vedi gli esempi nella pagina di elenco `Customers`. |
| Ricerche | Disponibile. | Disponibile, con la differenza che il comportamento delle ricerche avanzate e semplici è lo stesso con un telefono. La ricerca non visualizzerà la scheda, non mostrerà i riquadri Dettaglio informazioni o alcun gruppo di campi. | Vedi gli esempi nella pagina `Customer Card`. |
| Controlli matrice | Non disponibile. | Non disponibile. | Vedi l'esempio in `G/L Budget`. |
| Scarica file | Disponibile. Non è possibile scaricare più file contemporaneamente. | Disponibile. Non è possibile scaricare più file contemporaneamente. | Report `Trial Balance` nella casella di controllo **Stampa in Excel**. |
| Pagine di prospetto | Disponibile. | Non disponibile; viene visualizzato un messaggio di errore. | Prospetto `Sales Price` o `Cash Flow`. |
| Elenchi | Disponibile. | Disponibile, con la differenza che sono visualizzati in un layout brick. | Pagine Clienti o Ordini vendita. |
| Rientro nei controlli ripetitore | Disponibile. | Non disponibile. Il rendering del controllo ripetitore sarà un layout flat brick normale. | Pagine Piano dei conti e Lista contatti. |
| Stato attivo automatico dell'input nel primo campo modificabile di una pagina | Non disponibile. | Non disponibile. | Pagina `Customer Card`.<BR /><BR />Nel browser, lo stato attivo sarà automaticamente nel primo campo modificabile (come il campo `Name`), consentendo di modificare immediatamente il valore.<BR /><BR />Nelle app per tablet e telefono, lo stato attivo non sarà su questo campo; sarà invece necessario selezionare manualmente il primo campo per apportare le modifiche.|

## <a name="is-it-the-same-experience-on-tables-and-phones"></a>L'esperienza è la stessa con tablet e telefoni?

Quasi, ma non del tutto. Vedi l'elenco nella sezione [L'esperienza con le app è identica a quella con il browser?](#is-it-the-same-experience-in-the-apps-as-in-the-browser).  

## <a name="can-i-connect-the-app-to-our-on-premises-solution"></a>Posso connettere l'app alla soluzione locale?

Sì, è possibile. L'accesso viene eseguito in un modo leggermente diverso. Per ulteriori informazioni, vedi [Utilizzo di Business Central in locale](install-mobile-app.md#using-business-central-on-premises).  

## <a name="see-also"></a>Vedere anche

[Scaricare Business Central sul dispositivo mobile](install-mobile-app.md)  
[Installare l'app Business Central per Microsoft Teams](across-install-app-for-teams.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]