---
title: Funzionalità di accessibilità
description: Questo articolo fornisce informazioni sui tasti di scelta rapida e altre funzionalità di assistenza in Business Central per le persone con disabilità.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accessibility, shortcuts, charts, tooltips, screen reader
ms.search.form: 9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017
ms.date: 06/23/2021
ms.author: jswymer
ms.openlocfilehash: 8f9759f0ed024b1137b27ed79b67e18b6acfdf35
ms.sourcegitcommit: f9143302b8271f5924a027cacdf29dc37c95f4c6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/29/2022
ms.locfileid: "8655698"
---
# <a name="accessibility-and-keyboard-shortcuts"></a>Accessibilità e tasti di scelta rapida

In questo articolo vengono fornite informazioni sulle funzionalità che rendono [!INCLUDE[prod_short](includes/prod_short.md)] disponibile per gli utenti con esigenze particolari. [!INCLUDE[prod_short](includes/prod_short.md)] supporta le seguenti funzionalità di accessibilità:  

- Tasti di scelta rapida. Vedere [Tasti di scelta rapida](keyboard-shortcuts.md).
- Movimenti tocco e della penna su tablet e telefoni. Vedere [Movimenti tocco e della penna](touch-gestures.md).
- Spostamento  
- Intestazioni  
- Testo alternativo per le immagini e i collegamenti  
- Supporto per le tecnologie per l'accessibilità comuni 
- Ingrandire o rimpicciolire qualsiasi pagina
- Descrizioni comandi sugli elementi nell'interfaccia utente

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

## <a name="navigation"></a><a name="Navigation"></a> Spostamento
  
Puoi utilizzare diverse combinazioni dei tasti TAB, MAIUSC e di direzione della tastiera per spostarti tra gli elementi di una pagina. Gli elementi includono azioni, campi e colonne, parti e altri controlli. In generale, premere TAB o MAIUSC + TAB per passare all'elemento successivo o precedente.

Quando si evidenzia un'area che contiene azioni, come la barra di spostamento nella parte superiore di Gestione ruolo o la barra delle azioni in altre pagine, utilizzare i tasti di direzione per spostarti tra i diversi gruppi e azioni. Premere Invio su un gruppo per aprire le azioni sottostanti, quindi continuare a utilizzare i tasti di direzione. Premere Tab o Maiusc + Tab per uscire dall'area di azione.

Utilizzando l'ordine delle schede è inoltre possibile passare, ad esempio, dalla pagina principale del browser alle finestre di dialogo che richiedono conferma o alla pagina di accesso.  

## <a name="headings-in-content"></a><a name="Headings"></a> Intestazioni nel contenuto

L'origine HTML per il contenuto di [!INCLUDE[prod_short](includes/prod_short.md)] utilizza tag per aiutare gli utenti della tecnologia per l'accessibilità a comprendere la struttura e il contenuto della pagina. Ad esempio, nelle pagine di elenchi, le colonne vengono definite in tag TH e le intestazioni di colonna sono impostate con l'attributo TITLE all'interno del tag. Le didascalie per elementi quali Schede dettaglio, Riquadri Dettaglio informazioni e campi sono incluse nei tag delle intestazioni (H1, H2, H3 e H4).  

## <a name="image-and-links"></a><a name="Images"></a> Immagine e collegamenti

Un testo descrittivo per le immagini è impostato con l'attributo ALT all'interno del tag IMG. Un testo descrittivo per i collegamenti ipertestuali è impostato con l'attributo TITLE all'interno del tag A.  

## <a name="assistive-technologies"></a><a name="AssistiveTech"></a> Tecnologie per l'accessibilità

[!INCLUDE[prod_short](includes/prod_short.md)] supporta diverse tecnologie per l'accessibilità, ad esempio il contrasto elevato, le utilità per la lettura dello schermo e il software di riconoscimento vocale. Alcune tecnologie per l'accessibilità potrebbero non funzionare correttamente con determinati elementi nelle pagine di [!INCLUDE[prod_short](includes/prod_short.md)].  

## <a name="zoom"></a><a name="zoom"></a> Zoom

La maggior parte dei browser utilizza tasti di scelta rapida standard per ingrandire e ridurre la pagina corrente. Questi tasti di scelta rapida non sono specifici per [!INCLUDE [prod_short](includes/prod_short.md)], ma funzionano quando si utilizza [!INCLUDE [prod_short](includes/prod_short.md)] in un browser. Per un elenco dei tasti di scelta rapida supportati, vedere [Tasti di scelta rapida per ingrandire e ridurre](keyboard-shortcuts.md#zoomshortcuts).

## <a name="tooltips"></a>Descrizioni comando

Le descrizioni comando sono disponibili sulla maggior parte degli elementi dell'interfaccia utente, come campi e colonne della pagina, azioni, riquadri pile e grafici. Una descrizione comando fornisce un testo aggiuntivo che descrive un elemento per comprenderne meglio lo scopo. 

È possibile accedere alle descrizioni comandi in modi diversi, a seconda del client (Web o mobile) e del dispositivo utilizzato. Utilizzare la tabella seguente come riferimento. Alcune descrizioni comando possono essere lette dalle utilità per la lettura dello schermo. In questo caso, accedere alle descrizioni comando come descritto nella tabella, quindi utilizzare l'utilità per la lettura dello schermo per navigare alla descrizione come si farebbe con qualsiasi altro elemento.

#### <a name="accessing-tooltips"></a>Accesso alle descrizioni comando

|Elemento|Azione del mouse per client Web|Tasti di scelta rapida per client Web|Movimento touch su tablet/telefono per app per dispositivi mobili|Supporto di utilità per la lettura dello schermo|
|-------|-----------------|------------|--------------------------|---------------------|
|Campi della pagina e intestazioni di colonna|Passare il mouse o fare clic sulla didascalia del campo o sull'intestazione della colonna|Spostare lo stato attivo sul campo o sull'intestazione della colonna e premere i tasti Alt + Freccia su|Toccare la didascalia del campo |si|
|Elementi grafici, come una barra, una linea, una sezione del grafico a torta|Passare il mouse sopra l'elemento|Spostare lo stato attivo sull'elemento, ad esempio, utilizzando i tasti di direzione|Tenere premuto l'elemento|si|
|Azioni|Passare il mouse sopra l'azione|nessuno|nessuno |no|
|Riquadri pile|Passare il mouse sopra il riquadro |nessuno|nessuno|no|


<!--
- With a mouse, hover over the element.
- With keyboard, press the Alt+Up Arrow keys.
- On a tablet or phone, tap and hold on the element. To learn about more gestures, see [Touch and Pen Gestures](touch-gestures.md)

-->

## <a name="for-more-accessibility-information"></a>Per ulteriori informazioni sull'accessibilità

È possibile trovare informazioni aggiuntive sull'accessibilità con i prodotti Microsoft e le tecnologie per l'accessibilità sul sito Web [Accessibilità di Microsoft](https://go.microsoft.com/fwlink/?LinkId=262160).

## <a name="see-also"></a>Vedere anche

[Prepararsi a fare affari](ui-get-ready-business.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Domande frequenti](across-faq.yml)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
