---
title: "Informazioni sulla contabilità generale e COA| Documenti Microsoft"
description: "Descrive la contabilità generale, il piano dei conti e le categorie dei conti."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 63d414f4c81a9e20b4bb81b632edd9c91fb34a87
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="understanding-the-general-ledger-and-the-coa"></a>Informazioni sulla contabilità generale e COA
La contabilità generale memorizza i dati finanziari e il piano dei conti indica in conti in cui sono registrati tutti i movimenti C/G. [!INCLUDE[d365fin](includes/d365fin_md.md)] include un piano dei conti standard pronto per supportare l'azienda.

## <a name="general-ledger-setup-and-general-posting-setup"></a>Setup contabilità generale e setup registrazioni COGE
Il setup della contabilità generale svolge un ruolo fondamentale nei processi finanziari perché definisce il modo in cui vengono registrati i dati.  

Nella finestra **Setup contabilità generale** è possibile specificare le modalità di gestione di determinate questioni contabili relative alla società, quali:  

* Dettagli relativi all'arrotondamento delle fatture  
* Formati indirizzi  
* Report finanziari  

Analogamente, nella finestra **Setup registrazioni COGE** è possibile specificare come si desidera impostare le combinazioni di categorie di registrazione business generale e le categorie di registrazione di articoli e servizi. Le categorie di registrazione associano entità come clienti, fornitori, articoli, risorse e documenti di vendita o di acquisto a conti di contabilità generale. Compilare una riga per ogni combinazione di categorie di registrazione business e di categorie di registrazione articoli/servizi. Per ulteriori informazioni, vedere [Setup categorie di registrazione](finance-posting-groups.md)  

## <a name="the-chart-of-accounts"></a>Piano dei Conti
Nel piano dei conti sono visualizzati tutti i conti C/G. Tramite il piano dei conti è possibile eseguire operazioni, quali:  

* Visualizzare i report che mostrano i movimenti e i saldi di contabilità generale.  
* Chiudere il conto economico.  
* Aprire la scheda del conto C/G per aggiungere o modificare le impostazioni.  
* Visualizzare una lista delle categorie di registrazione che registrano nel conto.
* Visualizzare i saldi attivi e passivi separatamente per un singolo conto  

È possibile aggiungere, modificare o eliminare i conti di contabilità generale. Tuttavia, per evitare le differenze, non è possibile eliminare un conto di contabilità generale se i relativi dati vengono utilizzato nel piano dei conti.  

## <a name="account-categories"></a>Categorie di conti
È possibile personalizzare la struttura dei rendiconti finanziari mappando i conti di contabilità generale alle categorie dei conti.  

La finestra **Categorie conto C/G** visualizza le categorie e le sottocategorie principali esistenti e i conti C/G assegnati ad esse. È possibile creare nuove sottocategorie e assegnarle categorie ai conti esistenti.  

È possibile creare un gruppo di categoria definendo un'indentazione di altre categorie in una riga nella finestra **Categorie conto C/G**. Ciò consente di ottenere una panoramica, in quanto ogni raggruppamento mostra un saldo totale. Ad esempio, è possibile creare sottocategorie per i diversi tipi di cespiti e quindi creare gruppi di categorie per cespiti rispetto a cespiti correnti.  

È possibile specificare se i conti di questa sottocategoria devono essere inclusi in determinati tipi di report. Le categorie di conto consentono di definire il layout dei rendiconti finanziari.  

Ad esempio, l'estratto conto di default presenta una sottocategoria relativa ai contanti nei cespiti correnti. Se si desidera che nell'estratto conto vengano considerate la piccola cassa e il conto assegni, è possibile:  

1. Aggiungere due nuove sottocategorie. Una per la piccola cassa e una per il conto assegni.  
2. Specificare la definizione report addizionale **Conti cassa** per queste sottocategorie.  
3. Applicare un rientro sotto la sottocategoria **Contanti**.  

Alla successiva creazione di situazioni contabili, l'estratto conto mostrerà un saldo totale per la cassa contanti e due righe con saldi per la piccola cassa e il conto assegni.  

## <a name="see-also"></a>Vedi anche
[Finanze](finance.md)  
[Impostazione o modifica del piano dei conti](finance-setup-chart-accounts.md)  
[Business Intelligence](bi.md)  

