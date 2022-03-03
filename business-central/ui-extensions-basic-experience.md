---
title: Estensione dell'esperienza di base | Microsoft Docs
description: Questa estensione è un'alternativa moderna di Microsoft Dynamics C5.
author: bholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: C5, financials, extension
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: b423ce61a5bc8a7f5c580d0b4f3348792c4b02ab
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2022
ms.locfileid: "8132474"
---
# <a name="the-basic-experience-extension"></a>Estensione dell'esperienza di base
Se è stato utilizzato Microsoft Dynamics C5, i partner Microsoft possono aiutare a passare a una soluzione più moderna basata su [!INCLUDE[prod_short](includes/prod_short.md)], in modo da poter continuare a godere delle stesse funzionalità semplificate di Dynamics C5.

Questa estensione è destinata alle piccole imprese e può supportare fino a tre utenti. Se sono necessari più utenti, eseguire l'aggiornamento a una licenza [!INCLUDE[prod_short](includes/prod_short.md)] e disinstallare questa estensione.

> [!NOTE]
> Al momento, questa estensione è disponibile solo per i clienti in Danimarca e Islanda. 

## <a name="whats-available"></a>Funzionalità disponibili
La tabella seguente descrive le funzionalità disponibili se si installa l'estensione dell'esperienza di base.

|Area  |Funzionalità  |
|---------|---------|
|**Contabilità generale** |Finanza di base, schemi contabili, cespiti, gestione bancaria, riconciliazione bancaria, pagamenti, addebito diretto, dimensioni, valute multiple, budget, flusso di lavoro, gestione documenti/OCR, consolidamento, società illimitate|
|**Contabilità clienti/Vendite** |Contabilità clienti di base, fatturazione di vendita, sconti di vendita, prezzi, IVA, gestione contatti |
|**Contabilità fornitori/Acquisti** |Contabilità fornitori di base, fatturazione degli acquisti |
|**Gestione progetti** |Commesse, prezzi delle commesse, fogli presenze, incarichi, task, risorse |
|**Magazzino** |Inventario di base, sostituzioni di articolo, cross reference dell'articolo |

## <a name="getting-started"></a>Introduzione
Questa estensione è leggermente diversa dalla maggior parte e sarà necessario l'aiuto di un partner Microsoft per installarla e configurarla. Solo per sapere cosa aspettarsi, ecco una visualizzazione ad alto livello di ciò che farà il partner Microsoft.

1. Creare un nuovo tenant [!INCLUDE[prod_short](includes/prod_short.md)]. Può essere una versione di prova o CSP.
2. Aggiungere almeno un utente assegnato a una licenza dell'esperienza di base nell'account Azure Active Directory.
3. Rimuovere tutte le società, inclusa la società Cronus di esempio.
4. Creare una nuova società che non contenga dati o configurazioni di esempio.
5. Aggiungere il pacchetto **Demo RapidStart**. <!--what does the pockage contain?-->
6. Scaricare e installare l'estensione dell'esperienza di base da AppSource.

## <a name="migrating-data"></a>Migrazione dei dati
Portare con sé i propri dati Dynamics C5. Dopo che il partner Microsoft avrà installato l'estensione dell'esperienza di base, sarà disponibile un'azienda vuota. Un modo semplice per spostare i dati da Dynamics C5 all'esperienza di base consiste nell'utilizzare l'estensione Migrazione dei dati C5, inclusa in [!INCLUDE[prod_short](includes/prod_short.md)]. L'estensione esegue la migrazione di clienti, fornitori, articoli, conti di contabilità generale e relativi movimenti.

## <a name="see-also"></a>Vedere anche
[Estensione di migrazione dati C5](ui-extensions-c5-data-migration.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]