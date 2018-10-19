---
title: Copiare e incollare i dati
description: Copiare i campi e le righe dalle pagine di Business Central e incollarli in un'altra posizione.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accessibility, shortcuts, keyboarding
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: e924eeb10e98b81035837ca498ec4f1a7b28bf60
ms.contentlocale: it-it
ms.lasthandoff: 09/28/2018

---

# <a name="copying-and-pasting-in-included365finincludesd365finmdmd"></a>Copia e incolla in [!INCLUDE[d365fin](includes/d365fin_md.md)].
È possibile copiare una o più righe da un elenco o un singolo campo in una pagina e quindi incollare ciò che è stato copiato nella stessa pagina, in un'altra pagina o in un documento esterno (ad esempio di Microsoft Excel o Outlook). In breve, per copiare, premere CTRL + C (cmd + C in macOS) sulla tastiera. Per incollare, premere CTRL + V (cmd + V in macOS).

Sono disponibili altri tasti di scelta rapida da tastiera per copiare e incollare che consentono di risparmiare tempo quando si inseriscono i dati. Per ulteriori informazioni su questo argomento, vedere [Tasti di scelta rapida](keyboard-shortcuts.md#CopyRows).

Questo articolo risponde alle domande più frequenti relative alle operazioni di copia e incolla.  

## <a name="what-can-i-copy-and-paste"></a>Elementi che è possibile copiare e incollare
-   Copiare una o più righe di [!INCLUDE[d365fin](includes/d365fin_md.md)] nello stesso elenco o in qualsiasi elenco con colonne identiche.
-   Copiare una o più righe in [!INCLUDE[d365fin](includes/d365fin_md.md)] quindi incollarle in Excel o in altre applicazioni.
-   Copiare una o più righe in Excel e incollarle in un elenco di [!INCLUDE[d365fin](includes/d365fin_md.md)].
-   Copiare il valore di un singolo campo in [!INCLUDE[d365fin](includes/d365fin_md.md)] e incollarlo ovunque.

## <a name="how-do-i-copy-rows"></a>Come copiare le righe
Per copiare una singola riga, selezionarla e premere CTRL + C.

Per copiare più righe, è possibile:
-   Premi CTRL + fare clic su un'altra riga o premere MAIUSC + fare clic per selezionare la riga e tutte le righe intermedie. Vedere [Tasti di scelta rapida](keyboard-shortcuts.md#CopyRows) più per combinazioni di tastiera e del mouse per la selezione di righe.
-   Selezionare ![Mostra più opzioni](media/show-more-options-icon.png "Icona Mostra più opzioni") nella prima colonna di una riga, selezionare **Seleziona più elementi**, selezionare la casella di controllo accanto a ciascuna riga che si desidera copiare, quindi premere CTRL + C.

## <a name="how-do-i-paste-rows"></a>Come incollare le righe
Selezionare una riga vuota e premere CTRL+V. Se si desidera sostituire le righe esistenti, selezionare le righe desiderate e premere CTRL+V. In questo caso, è possibile copiare solo lo stesso numero di righe che selezionate.

<!-- Rows are pasted directly where your cursor is located. If you paste into an empty line, any existing subsequent lines will be moved after the pasted lines. If you paste into an existing line or lines, this will be overwritten.-->

## <a name="can-i-paste-rows-into-an-outlook-email-or-onenote"></a>È possibile incollare le righe in un'email di Outlook o OneNote?
Sì. Queste righe vengono incollate come una tabella ben formattata che conserva indentazione, allineamento numerico e colorazione, proprio come si vedrebbe in [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="does-copy-and-paste-work-with-tiles"></a>Le operazioni di copia e incolla sono compatibili con i riquadri?
No. No. L'elenco deve essere visualizzato come righe (Visualizzazione elenco) per poter copiare e incollare.

## <a name="in-which-lists-can-i-copy-and-paste-rows"></a>In quali elenchi si possono copiare e incollare righe?
È possibile copiare righe in qualsiasi tipo di elenco, inclusi fogli di lavoro, caselle di controllo o elenchi incorporati in una pagina (come le righe di un ordine di vendita). Tuttavia, per incollare le righe, l'elenco deve essere modificabile.

In alcune pagine, la progettazione dell'applicazione potrebbe impedire di incollare righe. Contattare l'amministratore o lo sviluppatore dell'applicazioni per modificare la [proprietà modificabile](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/properties/devenv-editable-property) nella pagina o la [proprietà PasteIsValid](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/properties/devenv-pasteisvalid-property) nella tabella di origine.

## <a name="on-which-clients-is-copy-and-paste-available"></a>In quali client quali client è disponibile copia e incolla?
Copia e incolla sono disponibili nel browser o nell'app [!INCLUDE[d365fin](includes/d365fin_md.md)] per Windows 10

## <a name="what-is-the-maximum-number-of-rows-that-can-be-copied"></a>Qual è numero massimo di righe copiabile?
È possibile copiare tutte le righe visualizzate. Ad esempio, per copiare tutte le 1000 righe in una pagina, è necessario innanzitutto scorrere fino alla fine della pagina e attendere che le righe vengano visualizzate prima della copia. Il numero massimo di righe che è possibile copiare è limitato solo dalla memoria del dispositivo in uso.

## <a name="must-i-have-the-exact-same-number-of-columns-when-pasting-rows"></a>Devo disporre dello stesso numero di colonne quando incollo le righe?
Sì. Sia che si copi da [!INCLUDE[d365fin](includes/d365fin_md.md)], Excel o da altra origine di tabella, le righe che si incollano devono avere le colonne di corrispondenza esatte, né più né meno.

## <a name="why-do-i-get-errors-when-pasting-rows"></a>Perché vengono visualizzati degli errori quando incollo le righe? 
Quando si incolla in [!INCLUDE[d365fin](includes/d365fin_md.md)], ogni riga viene controllata per assicurarsi che i valori in ogni colonna siano validi. Se una colonna contiene un valore che non è valido, l'operazione incolla viene interrotta e viene visualizzato un messaggio di errore. Per evitare ciò, assicurarsi che le colonne abbiano valori validi prima di incollarli.


## <a name="see-also"></a>Vedere anche
[Funzionalità di accessibilità](ui-accessibility.md)  
[Introduzione](product-get-started.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Domande frequenti](across-faq.md)  

