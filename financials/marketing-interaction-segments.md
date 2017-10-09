---
title: Tenere traccia dei segmenti e delle interazioni correlate| Documenti Microsoft
description: Informazioni su come creare segmenti per definire gruppi di contatti e specificare delle interazioni per i segmenti.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 899bdda7448810b029216c66402b739004193a61
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="managing-interactions-for-segments"></a>Gestione di interazioni per i segmenti
La finestra **Segmento** è una sorta di prospetto in cui è possibile:

* Creare segmenti.
* Salvare i criteri di segmentazione utilizzati per selezionare i contatti.
* Registrare il segmento e le interazioni che coinvolgono i contatti all'interno del segmento.

## <a name="segmenting"></a>Segmentazione
Esistono numerosi modi per creare segmenti:

* È possibile inserire manualmente i contatti che si desidera includere nel segmento in corrispondenza delle righe del segmento.
* È possibile selezionare i contatti:
* È possibile riutilizzare un segmento registrato come base per la creazione di un nuovo segmento.
* È possibile riutilizzare i criteri di segmentazione creati.

## <a name="interactions"></a>Interazioni
Nella finestra **Segmento** è possibile creare interazioni per più contatti contemporaneamente. È ad esempio possibile unire un segmento con un documento di Microsoft Word, in modo da inviare una lettera a tutti i contatti all'interno del segmento.

È possibile specificare informazioni relative all'interazione di un determinato segmento nella testata **Segmento**. È ad esempio possibile decidere quale modello di interazione utilizzare per tutti i contatti, specificare una descrizione, un tipo di corrispondenza e così via. Queste informazioni possono tuttavia essere modificate nella riga del segmento per ogni contatto, ad esempio specificando un'altra descrizione relativa a un determinato contatto. Se si effettua l'unione tra un segmento e un documento di Microsoft Word, è possibile personalizzare tale documento affinché sia inviato a uno o più contatti all'interno del segmento, ad esempio aggiungendo commenti personalizzati al documento.

## <a name="logging"></a>Registrazione
Facendo clic su **Registrazione** nella finestra **Segmento**, le interazioni vengono salvate nella tabella **Mov. log interazione** e il segmento viene registrato. Dopo aver registrato il segmento, è possibile trovarlo solo nella finestra **Segmenti registrati**.

Nella finestra **Segmenti registrati**, è possibile decidere di creare un segmento di follow-up contenente gli stessi identici contatti del segmento registrato.

## <a name="see-also"></a>Vedi anche
[Procedura: Creare segmenti](marketing-how-create-segment.md)  
[Procedura: Creare interazioni per i segmenti](marketing-how-create-interactions.md)  
[Gestione dei segmenti](marketing-segments.md)  
[Registrazione di interazioni con i contatti](marketing-interactions.md)  
[Gestione delle opportunità di vendita](marketing-manage-sales-opportunities.md)  
[Creazione e gestione di contatti](marketing-contacts.md)  
[Utilizzo di Financials](ui-work-product.md)

