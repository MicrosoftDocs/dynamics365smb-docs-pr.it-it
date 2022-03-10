---
title: Utilizzare i profili per classificare i contatti
description: Informazioni su come impostare i questionari del profilo per aiutarti a classificare i profili dei tuoi contatti commerciali.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: contacts, profiles
ms.author: edupont
ms.date: 06/22/2021
ms.openlocfilehash: 42ef7c92d138d717f10eb98a7fa9208eaf73ef54
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2022
ms.locfileid: "8140867"
---
# <a name="use-profile-questionnaires-to-classify-business-contacts"></a>Utilizzare i questionari profilo per classificare i contatti business
È possibile impostare questionari profilo da utilizzare durante l'immissione di informazioni sul profilo dei contatti. In ogni questionario, è possibile impostare le diverse domande da porre ai contatti.  

È inoltre possibile eseguire il questionario per rispondere automaticamente ad alcune domande sulla base dei dati di contatto, cliente o fornitore.  

## <a name="to-add-a-profile-questionnaire"></a>Per aggiungere un questionario profilo
1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup questionario**, quindi scegli il collegamento correlato.  
2.  Scegliere l'azione **Nuovo**.  
3.  Compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-add-questions-to-a-profile-questionnaire"></a>Per aggiungere domande a un questionario profilo
1.  Scegliere il questionario profilo pertinente e quindi scegliere l'azione **Modifica setup questionario**.  
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

Dopo avere impostato le domande relative al profilo, se si assegna il questionario profilo a un contatto, le risposte corrette relative a tale contatto vengono assegnate automaticamente da [!INCLUDE[prod_short](includes/prod_short.md)].  

## <a name="example"></a>Esempio

È possibile classificare i contatti in base al volume di acquisti da essi effettuati:

|Risposta|Si applica a|
|--- |--- |
|A|contatti che hanno effettuato acquisti per 500.000 VL o più|
|B|contatti che hanno effettuato acquisti per un importo compreso tra 100.000 e 499.999 VL|
|C|contatti che hanno effettuato acquisti per 99.999 VL o meno|

Per effettuare questa operazione, completare la pagina **Setup questionario profilo** nel modo seguente:

| Tipo     | Descrizione        | Classificazione automatica     | Da Valore | Al valore |
|----------|--------------------|------------------------------|------------|----------|
| Domanda | Classificazione di ABC | Fare clic per inserire un segno di spunta |            |          |
| Risposta   | A                  |                              | 500.000    |          |
| Risposta   | B                  |                              | 100,000    | 499,999  |
| Risposta   | C                  |                              |            | 99,999   |

Compilare la pagina **Dettagli domande profilo** nel modo seguente:

| Campo                         | Valore         |
|-------------------------------|---------------|
| Campo di classificazione del cliente | Vendite (LCY)   |
| Metodo di classificazione         | Valore definito |

Quando si assegna il questionario profilo contenente questa domanda a un contatto, la risposta pertinente al contatto viene automaticamente inserita nelle righe profilo della scheda del contatto.

## <a name="see-also"></a>Vedere anche

[Creazione di contatti](marketing-create-contact-companies.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]