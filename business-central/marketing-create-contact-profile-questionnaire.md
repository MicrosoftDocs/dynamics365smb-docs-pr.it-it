---
title: Utilizzare i profili per classificare i contatti
description: Impostare i questionari profilo per classificare i contatti business
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: contacts, profiles
ms.author: edupont
ms.date: 10/01/2019
ms.openlocfilehash: 22471a6e0281f6f7aa4e9c9bbf0b2d9c5a0fd710
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2019
ms.locfileid: "2309294"
---
# <a name="use-profile-questionnaires-to-classify-business-contacts"></a>Utilizzare i questionari profilo per classificare i contatti business
È possibile impostare questionari profilo da utilizzare durante l'immissione di informazioni sul profilo dei contatti. In ogni questionario, è possibile impostare le diverse domande da porre ai contatti.  

È inoltre possibile eseguire il questionario per rispondere automaticamente ad alcune domande sulla base dei dati di contatto, cliente o fornitore.  

## <a name="to-add-a-profile-questionnaire"></a>Per aggiungere un questionario profilo
1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup questionari** e quindi scegliere il collegamento correlato.  
2.  Nel gruppo **Nuovo** della scheda **Pagina iniziale** scegliere **Nuovo**.  
3.  Compilare i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-add-questions-to-a-profile-questionnaire"></a>Per aggiungere domande a un questionario profilo
1.  Scegliere il profilo pertinente e nel gruppo **Processo** della scheda **Pagina iniziale** scegliere **Modifica setup questionario**.  
2.  Sulla prima riga vuota, nel campo **Tipo**, scegliere **Domanda** e digitare la domanda desiderata nel campo **Descrizione**. Compilare gli altri campi della riga.  
3.  Sulla prima riga vuota successiva nel campo **Tipo**, scegliere **Risposta** e digitare la risposta desiderata nel campo **Descrizione**.  
4.  Nel campo **Priorità** selezionare la priorità. Nei campi **Da valore** e **A valore** definire un intervallo di punti. I contatti che ricevono punti entro l'intervallo stabilito otterranno la risposta.  

Ripetere tali passaggi per immettere tutte le domande e le risposte nel questionario profilo.

Dopo avere creato un questionario, è necessario creare le valutazioni dei contatti per classificare i contatti. È inoltre possibile impostare le domande classificate automaticamente in base alle informazioni presenti nella scheda contatto.  

> [!NOTE]
> Se si immette una domanda con risposta automatica, selezionare <STRONG>Riga</STRONG> e quindi <STRONG>Dettagli domanda</STRONG> per immettere i criteri da utilizzare per fornire la risposta automatica.

## <a name="the-automatic-classification-of-contacts"></a>Classificazione automatica dei contatti
È possibile classificare automaticamente i contatti in base alle informazioni relative a cliente, fornitore e contatto, mediante una serie di domande sul profilo con risposta automatica nella pagina **Setup questionario profilo**.  

> [!NOTE]
> È possibile assegnare una classificazione basata sui dati dei clienti solo ai contatti registrati come clienti e una classificazione basata sui dati dei fornitori solo ai contatti registrati come fornitori. La classificazione automatica non viene aggiornata automaticamente. Si consiglia pertanto di aggiornare i questionari profilo una volta effettuato l'aggiornamento dei dati relativi a clienti, fornitori o contatti su cui tali questionari si basano.  

Dopo avere impostato le domande relative al profilo, se si assegna il questionario profilo a un contatto, le risposte corrette relative a tale contatto vengono assegnate automaticamente da [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="example"></a>Esempio
È possibile classificare i contatti in base al volume di acquisti da essi effettuati:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Risposta</strong></th>
<th><strong>Si applica a</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>A</p></td>
<td><p>contatti che hanno effettuato acquisti per 500.000 VL o più</p></td>
</tr>
<tr class="even">
<td><p>B</p></td>
<td><p>contatti che hanno effettuato acquisti per un importo compreso tra 100.000 e 499.999 VL</p></td>
</tr>
<tr class="odd">
<td><p>C</p></td>
<td><p>contatti che hanno effettuato acquisti per 99.999 VL o meno</p></td>
</tr>
</tbody>
</table>

Per effettuare questa operazione, completare la pagina **Setup questionario profilo** nel modo seguente:


<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Tipo</strong></th>
<th><strong>Descrizione</strong></th>
<th><strong>Classificazione Automatica</strong></th>
<th><strong>Da Valore</strong></th>
<th><strong>A Valore</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Domanda</p></td>
<td><p>Classificazione di ABC</p></td>
<td><p>Fare clic per inserire un segno di spunta</p></td>
<td><p> </p></td>
<td><p> </p></td>
</tr>
<tr class="even">
<td><p>Risposta</p></td>
<td><p>A</p></td>
<td><p> </p></td>
<td><p>500.000</p></td>
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p>Risposta</p></td>
<td><p>B</p></td>
<td><p> </p></td>
<td><p>100,000</p></td>
<td><p>499,999</p></td>
</tr>
<tr class="even">
<td><p>Risposta</p></td>
<td><p>C</p></td>
<td><p> </p></td>
<td><p> </p></td>
<td><p>99,999</p></td>
</tr>
</tbody>
</table>

Compilare la pagina **Dettagli domande profilo** nel modo seguente:
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Campo</strong></th>
<th><strong>Valore</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Campo Classificazione clienti</strong></td>
<td><emphasis>Vendite (VL)</emphasis></td>
</tr>
<tr>
<td><strong>Metodo di classificazione</strong></td>
<td><emphasis>Valore Definito</emphasis></td>
</tr>
</tbody>
</table>

Quando si assegna il questionario profilo contenente questa domanda a un contatto, la risposta pertinente al contatto viene automaticamente inserita nelle righe profilo della scheda del contatto.

## <a name="see-also"></a>Vedi anche
[Creazione di contatti](marketing-create-contact-companies.md)  
