---
title: Ricerca di dati e immissione di criteri di filtro | Microsoft Docs
description: Descrive come utilizzare i filtri, come il Filtro rapido, per perfezionare i risultati nella ricerca dei dati.
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
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 11d7ef56e980ba263dba6328b2f2f08b86410242
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="searching-filtering-and-sorting-data"></a>Ricerca, filtro e ordinamento di dati
La ricerca e l'individuazione di record in un elenco risultano più semplici grazie ad alcune opzioni di ordinamento, ricerca e filtro.

Quando si desidera cercare dei dati, ad esempio nomi e indirizzi dei clienti o gruppi di prodotti, si immettono dei criteri. Nei criteri di ricerca è possibile utilizzare nel campo specificato tutti i numeri e le lettere che normalmente si utilizzano. È inoltre possibile utilizzare alcuni simboli speciali per filtrare ulteriormente i risultati. È possibile effettuare la ricerca in due modi: utilizzando il Filtro rapido o filtri di colonna.

## <a name="sorting"></a>Ordinamento
L'ordinamento consente di ottenere in modo semplice e rapido una panoramica dei dati. Se si dispone di molti clienti, ad esempio, è possibile scegliere di ordinarli in base a **Nr. cliente**, **Cat. reg. cliente**, **Codice valuta**, **Codice paese** o **Identificativo fiscale** per ottenere la panoramica desiderata.

Per ordinare un elenco, fare clic sull'intestazione di una colonna per passare dall'ordine crescente a quello decrescente e viceversa, oppure scegliere la piccola freccia giù nell'intestazione della colonna e scegliere **Crescente** o **Decrescente**.  

> [!NOTE]  
>   L'ordinamento non è supportato nelle immagini, nei campi BLOB, in FlowFilter e nei campi che non appartengono a una tabella.  

## <a name="searching-by-using-the-quick-filter"></a>Ricerca con il Filtro rapido
È possibile aggiungere filtri a tutte le pagine, utilizzando la funzione Filtro rapido. Questa funzione viene abilitata scegliendo l'icona della lente di ingrandimento che si trova nell'angolo superiore destro di una pagina. Questo tipo di filtro viene utilizzato per una rapida immissione dei criteri.

> [!IMPORTANT]  
>   Il Filtro rapido consente di filtrare i dati facilmente immettendo testo normale, ma non offre molte opzioni di criteri di ricerca. A seconda se si immette il testo normale o il testo con i simboli, il filtro rapido funziona in modo diverso.  

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

> [!NOTE]  
>   Non è possibile utilizzare i carattere jolly quando si filtrano i campi di enumerazione, come il campo **Stato** negli ordini di vendita. Per immettere un filtro per il tipo di campo, è possibile immettere il valore numerico come parametro di filtro. Ad esempio, nel campo **Stato** in un ordine di vendita con i valori **Aperto**, **Rilasciato**, **In attesa di approvazione**e **Pagamento anticipato in sospeso**, utilizzare i valori **0**, **1**, **2**e **3** per filtrare in base a queste opzioni. 

## <a name="searching-by-using-column-filters"></a>Ricerca con filtri di colonna
È possibile applicare un filtro a una o più colonne di un elenco. I filtri di colonna sono più flessibili e avanzati del Filtro rapido. 

### <a name="to-add-a-filter-on-a-column"></a>Per applicare un filtro a una colonna
1.  Prima di applicare un filtro, scegliere l'icona ![Mostra come lista](media/ui_show_as_list_icon.png "freccia sinistra Mostra come lista") per modificare la vista dell'elenco.
2. Scegliere la freccia giù nell'intestazione della colonna, quindi scegliere **Filtro**.
3. Effettuare una delle seguenti operazioni: 
  -  Scegliere *…* accanto alla casella per selezionare un valore dall'elenco.
  -  Immettere i criteri di filtro nella casella. Per ulteriori informazioni, vedere la sezione successiva.
4. Scegliere il pulsante **OK**.

## <a name="filter-criteria-and-symbols"></a>Criteri e simboli di filtro
Quando si impostano criteri in un filtro, è possibile immettere tutti i numeri e le lettere in genere consentiti nel campo. È inoltre possibile utilizzare alcuni simboli speciali per filtrare ulteriormente i risultati. Nella tabella seguente sono inclusi i simboli che è possibile utilizzare nei filtri.  
  
> [!IMPORTANT]  
>  In alcuni casi è possibile che alcuni valori campo contengano tali simboli e che si intenda filtrarli. Per farlo, è necessario includere l'espressione di filtro contenente il simbolo tra virgolette ("). Ad esempio, se si desidera filtrare i record che iniziano con il testo *S&R*, l'espressione di filtro è **'S&R*'**.  
  
### <a name="-interval"></a>(..) Intervallo  
  
|espressione di esempio|Record visualizzati|  
|-----------------------|-----------------------|  
|1100..2100|Numeri da 1100 a 2100|  
|..2500|Fino a 2500 compreso.|  
|..12 31 00|Le date fino al 31/12/00 incluso|  
|P8..|Informazioni sul periodo contabile 8 e successivi|  
|..23|Dalla data di inizio fino al 23-mese corrente-anno corrente ore 23:59:59|  
|23..|Dal 23-mese corrente-anno corrente ore 0:00:00 alla fine|  
|22..23|Dal 22-mese corrente-anno corrente ore 0:00:00 fino al 23-mese corrente-anno corrente ore 23:59:59|  
  
### <a name="124-eitheror"></a>(&#124;) Oppure  
  
|espressione di esempio|Record visualizzati|  
|-----------------------|-----------------------|  
|1200&#124;1300|Numeri con 1200 o 1300|  
  
### <a name="-not-equal-to"></a>(<>) Diverso da  
  
|espressione di esempio|Record visualizzati|  
|-----------------------|-----------------------|  
|<>0|Tutti i numeri tranne 0<br /><br /> SQL Server Option consente di combinare questo simbolo con un'espressione contenente caratteri jolly. <>A*, ad esempio, si riferisce a un testo diverso da qualunque testo che inizia con la lettera A.|  
  
### <a name="-greater-than"></a>(>) Maggiore di  
  
|espressione di esempio|Record visualizzati|  
|-----------------------|-----------------------|  
|>1200|Numeri maggiori di 1200|  
  
### <a name="-greater-than-or-equal-to"></a>(>=) Maggiore di o uguale a  
  
|espressione di esempio|Record visualizzati|  
|-----------------------|-----------------------|  
|>=1200|Numeri maggiori o uguali a 1200|  
  
### <a name="-less-than"></a>(<) Minore di  
  
|espressione di esempio|Record visualizzati|  
|-----------------------|-----------------------|  
|<1200|Numeri minori di 1200|  
  
### <a name="-less-than-or-equal-to"></a>(<=) Minore di o uguale a  
  
|espressione di esempio|Record visualizzati|  
|-----------------------|-----------------------|  
|<=1200|Numeri minori o uguali a 1200|  
  
### <a name="-and"></a>(&) E  
  
|espressione di esempio|Record visualizzati|  
|-----------------------|-----------------------|  
|>200&<1200|Numeri maggiori di 200 e minori di 1200.|  
  
### <a name="-an-exact-character-match"></a>('') Una corrispondenza esatta di carattere  
  
|espressione di esempio|Record visualizzati|  
|-----------------------|-----------------------|  
|'man'|Testo con corrispondenza esatta a man e con distinzione tra maiuscole e minuscole.|  
  
### <a name="-case-insensitive"></a>(@) Senza distinzione tra maiuscole e minuscole  
  
|espressione di esempio|Record visualizzati|  
|-----------------------|-----------------------|  
|@man*|Testo che inizia con man e senza distinzione tra maiuscole e minuscole.|  
  
### <a name="-an-indefinite-number-of-unknown-characters"></a>(*) Un numero indefinito di caratteri non noti  
  
|espressione di esempio|Record visualizzati|  
|-----------------------|-----------------------|  
|*Co*|Testo contenente "Co" per il quale viene osservata la distinzione tra maiuscole e minuscole.|  
|*Co|Testo che termina con "Co" e per il quale viene osservata la distinzione tra maiuscole e minuscole.|  
|Co*|Testo che inizia con "Co" e per il quale viene osservata la distinzione tra maiuscole e minuscole.|  
  
### <a name="-one-unknown-character"></a>(?) Un carattere non noto  
  
|espressione di esempio|Record visualizzati|  
|-----------------------|-----------------------|  
|Mar?o|Testo come Marco o Mario|  
  
### <a name="combined-format-expressions"></a>Espressioni di formato combinate  
  
|espressione di esempio|Record visualizzati|  
|-----------------------|-----------------------|  
|5999&#124;8100..8490|Include qualsiasi record con il numero 5999 oppure con un numero compreso tra 8100 e 8490.|  
|..1299&#124;1400..|Include record con un numero minore o uguale a 1299 oppure un numero uguale a 1400 o maggiore, vale a dire tutti i numeri tranne quelli compresi tra 1300 e 1399.|  
|>50&<100|Include record con numeri maggiori di 50 e minori di 100, vale a dire i numeri compresi tra 51 e 99.|  
 
## <a name="see-also"></a>Vedi anche
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

