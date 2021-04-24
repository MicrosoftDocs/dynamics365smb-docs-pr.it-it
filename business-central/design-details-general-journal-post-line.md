---
title: 'Dettagli di progettazione: riga di registrazione di contabilità generale | Microsoft Docs'
description: Questo argomento fornisce informazioni dettagliate sui concetti e sui principi utilizzati per riprogettare la funzionalità della riga di registrazione di contabilità generale in Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, general journal, posting, codeunit 12
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 3ea2ea8a4ef5bbdff70346022ee226fd5e26748d
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5777825"
---
# <a name="design-details-general-journal-post-line"></a>Dettagli di progettazione: riga di registrazione di contabilità generale
Questa documentazione fornisce informazioni tecniche dettagliate sui concetti e sui principi utilizzati per riprogettare la funzionalità della riga di registrazione di contabilità generale in [!INCLUDE[prod_short](includes/prod_short.md)]. La riprogettazione semplifica e rende più facile la manutenzione di codeunit 12. Viene innanzitutto illustrata una panoramica dei concetti alla base della riprogettazione. Viene quindi illustrata l'architettura tecnica per mostrare le modifiche conseguenti alla riprogettazione.  

## <a name="in-this-section"></a>In questa sezione  
[Sintesi della riga di registrazione di contabilità generale](design-details-general-journal-post-line-overview.md)  
[Dettagli di progettazione: Struttura dell'interfaccia di registrazione](design-details-posting-interface-structure.md)  
[Dettagli di progettazione: Struttura del motore di registrazione](design-details-posting-engine-structure.md)  
[Modifiche relative alla codeunit 12: variabili globali di mappatura per la riga di registrazione di contabilità generale](design-details-codeunit-12-changes-mapping-global-variables-for-general-journal-post-line.md)  
[Modifiche relative alla codeunit 12: modifiche nelle procedure di registrazione di contabilità generale](design-details-codeunit-12-changes-changes-in-general-journal-post-procedures.md)  

## <a name="see-also"></a>Vedi anche  
[Utilizzo delle registrazioni COGE](ui-work-general-journals.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]