---
title: Impostazione di campagne di marketing in Financials | Documenti Microsoft
description: "Viene descritto come è possibile impostare e svolgere campagne di marketing in Dynamics 365 for Financials"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, campaign, promo, prospect
ms.date: 05/20/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 92c5fb75f4f3d3180ba67b89481beed2e58c3dbe
ms.openlocfilehash: 68359d2dd2c2e07463babda91d86d47998f0912a
ms.contentlocale: it-it
ms.lasthandoff: 05/31/2017


---
# <a name="managing-marketing-campaigns"></a>Gestione di campagne di marketing
Per identificare, attirare e fidelizzare i clienti, è fondamentale mettere a punto un solido piano di marketing. Un piano di marketing comprende diverse campagne e altre interazioni correlate alle attività di marketing e di vendita. Quando si pianifica una campagna, è necessario decidere a quali contatti rivolgersi, quale tipo di campagna creare (fiera commerciale o messaggi e-mail) e a quali agenti assegnare ogni task.

Ogni campagna deve prevedere diverse attività o task. È possibile combinare più task, ad esempio task che rappresentano un passaggio, nelle attività. I task delle attività sono in relazione tra essi in base a una formula di date. I singoli task possono essere assegnati solo agli agenti. Le attività possono essere assegnate a opportunità, agenti, gruppi di venditori e contatti. Per ulteriori informazioni, vedere [Procedura: Impostare fasi ciclo e fasi di vendita delle opportunità](marketing-how-setup-opportunity-sales-cycles-stages.md).

## <a name="defining-individual-campaigns"></a>Definizione di campagne singole
Prima di creare una campagna, è necessario impostare *codici di stato campagna*. L'utilizzo di questi codici consente di gestire le campagne assegnando ad esse uno stato. Lavorando alle diverse fasi della campagna, sarà possibile sapere i passaggi completati e quelli ancora da iniziare. I codici stato campagna vengono impostati nella finestra **Stato campagna**.

È possibile creare una scheda campagna per ogni campagna di cui tenere traccia. È anche possibile visualizzare queste schede campagna per visualizzare informazioni generali su ogni campagna.
È possibile eliminare movimenti campagna, come se il movimento registrasse un'azione che è stata annullata. È possibile eliminare solo movimenti campagna annullati.

### <a name="selecting-the-target-audience"></a>Selezione del target
Dopo avere creato una campagna, è possibile iniziare a creare segmenti che specifichino il target della campagna. Per ulteriori informazioni, vedere [Gestione dei segmenti](marketing-segments.md).

### <a name="registering-discount-percentages"></a>Registrazione delle percentuali di sconto
Dopo avere impostato la campagna, avere stabilito quali segmenti coprirà la campagna e avere impostato la data di inizio e la data di fine, sarà possibile registrare la percentuale di sconto che verrà applicata al cliente per i singoli articoli nelle righe della finestra **Sconti riga vendita**. È inoltre possibile registrare prezzi di vendita dei singoli articoli nelle righe della finestra **Prezzi vendita**. È possibile accedere a entrambe le finestre dalla scheda campagna.

 Una volta impostati i prezzi di vendita e gli sconti riga, nonché i segmenti nella Scheda Campagna, è necessario attivarli in modo che i prezzi e gli sconti vengano riportati anche nelle righe.

**Nota**: per attivare i prezzi di vendita/ gli sconti riga, è necessario specificare se l'intero segmento o solo alcuni contatti sono obiettivi della campagna. Se i prezzi di vendita e gli sconti riga riguardano tutti i contatti del segmento, selezionare il campo **Target campagna** disponibile nella Scheda dettaglio **Campagna** della scheda **Segmento**.
Se i prezzi di vendita/gli sconti riga non vengono offerti a tutti i contatti del segmento, è possibile deselezionare il campo **Target campagna** per i contatti specifici. Se non è possibile visualizzare questo campo, è possibile aggiungerlo alla vista. Per ulteriori informazioni, vedere [Personalizzazione utente](ui-user-personalization.md).

## <a name="conducting-campaigns"></a>Esecuzione di campagne
Durante l'esecuzione di una campagna, vengono registrate tutte le interazioni con i contatti, o segmenti. In questo modo sarà possibile ottenere statistiche e altre informazioni sui costi e sulle probabilità di successo della campagna.

Le campagne vengono eseguite dagli agenti ed è necessario creare attività per rappresentare ciascun task e per assegnarlo agli agenti pertinenti. Per ulteriori informazioni, vedere [Procedura: Impostare fasi ciclo e fasi di vendita delle opportunità](marketing-how-setup-opportunity-sales-cycles-stages.md).

## <a name="see-also"></a>Vedi anche
[Gestione dei contatti](marketing-contacts.md)  
[Gestione dei segmenti](marketing-segments.md)  
[Gestione delle opportunità di vendita](marketing-manage-sales-opportunities.md)  
[Utilizzo di dati finanziari](ui-work-product.md)  

