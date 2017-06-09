---
title: Immissione di criteri di filtro | Documenti Microsoft
description: Informazioni sull&quot;utilizzo dei filtri in Financials.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delimit, FlowFilter
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 1a94e2ead59a40081920a0b11ed545a895d89910
ms.contentlocale: it-it
ms.lasthandoff: 05/04/2017


---
# <a name="entering-criteria-in-filters"></a>Immissione di criteri di filtro
Quando si desidera cercare dei dati, ad esempio nomi e indirizzi dei clienti o gruppi di prodotti, si immettono dei criteri. Nei criteri di ricerca è possibile utilizzare nel campo specificato tutti i numeri e le lettere che normalmente si utilizzano. È inoltre possibile utilizzare alcuni simboli speciali per filtrare ulteriormente i risultati.

## <a name="searching-using-the-quick-filter"></a>Ricerca con l'utilizzo di Filtro rapido
È possibile aggiungere filtri a tutte le pagine, utilizzando la funzione Filtro rapido. Questa funzione viene abilitata scegliendo l'icona della lente di ingrandimento che si trova nell'angolo superiore destro di una pagina. Questo tipo di filtro viene utilizzato per una rapida immissione dei criteri.

**Importante**: la funzione Filtro rapido consente di filtrare i dati facilmente immettendo testo normale, ma non offre molte opzioni di criteri di ricerca. A seconda se si immette il testo normale o il testo con i simboli, il filtro rapido funziona in modo diverso.  

* Se si immette testo normale nei criteri di ricerca, i criteri di ricerca vengono interpretati come una ricerca senza distinzione tra maiuscole e minuscole contenente un determinato testo.  
* Se si immette del testo includendo dei simboli nei criteri di ricerca, i criteri di ricerca vengono interpretati esattamente così come sono stati immessi e la ricerca rileva la differenza tra maiuscole e minuscole.

### <a name="quick-filter-criteria"></a>Criteri di Filtro rapido
<!-- html syntax because symbols conflict with MarkDown syntax -->
<TABLE>
  <TR>
    <TH>Criteri di ricerca</TH>
    <TH>Interpretato come...</TH>
    <TH>Reso come...</TH>
  </TR>
  <TR>
    <TD>man</TD>
    <TD>@&#42;man&#42;</TD>
    <TD>Tutti i record che contengono il testo <b>man</b> e senza distinzione tra maiuscole e minuscole.</TD>
  </TR>
  <TR>
    <TD>se</TD>
    <TD>@&#42;se&#42;</TD>
    <TD>Tutti i record che contengono il testo <b>e</b> e senza distinzione tra maiuscole e minuscole.</TD>
  </TR>
  <TR>
    <TD>Man&#42;</TD>
    <TD>Inizia con <b>Man</b> e con distinzione tra maiuscole e minuscole.</TD>
    <TD>Tutti i record che iniziano con il testo <b>Man</b>.</TD>
  </TR>
  <TR>
    <TD>'man'</TD>
    <TD>Un testo esatto e con distinzione tra maiuscole e minuscole.</TD>
    <TD>Tutti i record che corrispondono esattamente a <b>man</b>.</TD>
  </TR>
  <TR>
    <TD>@man* </TD>
    <TD>Inizia con e senza distinzione tra maiuscole e minuscole.</TD>
    <TD>Tutti i record che iniziano con <b>man</b>.</TD>
  </TR>
    <TR>
    <TD>@&#42;man</TD>
    <TD>Termina con e senza distinzione tra maiuscole e minuscole.</TD>
    <TD>Tutti i record che terminano con <b>man</b>.</TD>
  </TR>
</TABLE>

**Nota**: non è possibile utilizzare i carattere jolly quando si filtrano i campi di enumerazione, come il campo **Stato** negli ordini di vendita. Per immettere un filtro per il tipo di campo, è possibile immettere il valore numerico come parametro di filtro. Ad esempio, nel campo **Stato** in un ordine di vendita con i valori **Aperto**, **Rilasciato**, **In attesa di approvazione**e **Pagamento anticipato in sospeso**, utilizzare i valori **0**, **1**, **2**e **3** per filtrare in base a queste opzioni.  

## <a name="see-also"></a>Vedi anche
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

