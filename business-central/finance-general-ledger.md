---
title: Informazioni sulla contabilità generale e COA
description: Descrive la contabilità generale, il piano dei conti e le categorie dei conti. Usa la pagina Setup contabilità generale per specificare le modalità di gestione di determinate questioni contabili relative alla società.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.search.form: 18, 20, 37, 65, 99, 312, 313, 395, 552, 569, 570, 634, 790, 791, 1158
ms.date: 12/03/2021
ms.author: edupont
ms.openlocfilehash: 78d4ce41c4c6e85751134b51efe181380da8a0e4
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2022
ms.locfileid: "8138071"
---
# <a name="understanding-the-general-ledger-and-the-chart-of-accounts"></a>Informazioni sulla contabilità generale e sul piano dei conti

La contabilità generale memorizza i dati finanziari e il piano dei conti indica in conti in cui sono registrati tutti i movimenti C/G. [!INCLUDE[prod_short](includes/prod_short.md)] include un piano dei conti standard pronto per supportare l'azienda.

## <a name="general-ledger-setup-and-general-posting-setup"></a>Setup contabilità generale e setup registrazioni COGE

Il setup della contabilità generale svolge un ruolo fondamentale nei processi finanziari perché definisce il modo in cui vengono registrati i dati.  

Nella pagina **Setup contabilità generale** è possibile specificare le modalità di gestione di determinate questioni contabili relative alla società, quali:  

* Dettagli relativi all'arrotondamento delle fatture  
* Formati indirizzi  
* Report finanziari  

> [!TIP]
> La pagina **Setup contabilità generale** include campi generici e campi specifici per il paese o la regione. Se non si è certi del significato di un campo, suggeriamo di collaborare con il contabile per determinare se è rilevante per l'organizzazione.  

Analogamente, nella pagina **Setup registrazioni COGE** è possibile specificare come si desidera impostare le combinazioni di categorie di registrazione business generale e le categorie di registrazione di articoli e servizi. Le categorie di registrazione associano entità come clienti, fornitori, articoli, risorse e documenti di vendita o di acquisto a conti di contabilità generale. Compilare una riga per ogni combinazione di categorie di registrazione business e di categorie di registrazione articoli/servizi. Ma è anche possibile aprire ogni riga nella relativa scheda di setup della registrazione. Per ulteriori informazioni, vedere [Setup categorie di registrazione](finance-posting-groups.md).  

> [!TIP]
> Se non è possibile vedere i campi cercati nella pagina **Setup registrazioni COGE**, utilizzare la barra di scorrimento orizzontale nella parte inferiore della pagina per scorrere verso destra.  

## <a name="the-chart-of-accounts"></a>Piano dei Conti

Nel piano dei conti sono visualizzati tutti i conti C/G. Tramite il piano dei conti è possibile eseguire operazioni, quali:  

* Visualizzare i report che mostrano i movimenti e i saldi di contabilità generale.  
* Chiudere il conto economico.  
* Apri la scheda del conto di contabilità generale (C/G) per aggiungere o modificare le impostazioni.  
* Visualizzare una lista delle categorie di registrazione che registrano nel conto.
* Visualizzare i saldi attivi e passivi separatamente per un singolo conto  

È possibile aggiungere, modificare o eliminare i conti di contabilità generale. Tuttavia, per evitare le differenze, non è possibile eliminare un conto di contabilità generale se i relativi dati vengono utilizzato nel piano dei conti.  

## <a name="account-categories"></a>Categorie di conti

È possibile personalizzare la struttura dei rendiconti finanziari mappando i conti di contabilità generale alle categorie dei conti.  

La pagina **Categorie conto C/G** visualizza le categorie e le sottocategorie principali esistenti e i conti di contabilità generale assegnati ad esse. È possibile creare nuove sottocategorie e assegnarle categorie ai conti esistenti.  

È possibile creare un gruppo di categoria definendo un'indentazione di altre categorie in una riga nella pagina **Categorie conto C/G**. Ciò consente di ottenere una panoramica, in quanto ogni raggruppamento mostra un saldo totale. Ad esempio, è possibile creare sottocategorie per i diversi tipi di cespiti e quindi creare gruppi di categorie per cespiti rispetto a cespiti correnti.  

È possibile specificare se i conti di questa sottocategoria devono essere inclusi in determinati tipi di report. Le categorie di conto consentono di definire il layout dei rendiconti finanziari.  

### <a name="example"></a>Esempio

Ad esempio, l'estratto conto di default presenta una sottocategoria relativa ai *contanti* nei *cespiti correnti*. Se vuoi che nell'estratto conto vengano considerate la piccola cassa e il conto assegni, effettua questi passaggi:  

1. Aggiungi due nuove sottocategorie:

    * Una per la piccola cassa  
    * Una per il conto assegni  
2. Specificare la definizione report addizionale **Conti cassa** per queste sottocategorie.  
3. Applicare un rientro sotto la sottocategoria **Contanti**.  

Alla successiva creazione di situazioni contabili, l'estratto conto mostrerà un saldo totale per la cassa contanti e due righe con saldi per la piccola cassa e il conto assegni.  

## <a name="getting-a-quick-overview"></a>Ottenere una rapida visione d'insieme

La pagina della struttura dei conti visualizza i conti in una lista gerarchica che offre un accesso veloce alle informazioni chiave per ogni conto. Tuttavia, l'elenco è statico, e se hai molti account potresti dover fare un po' di scorrimento per visualizzare le informazioni per i diversi account. Se vuoi solo una rapida panoramica delle basi, come i cambiamenti netti e i saldi, la pagina **Sintesi del piano dei conti** è un'utile alternativa. La disposizione delle colonne nella pagina è ora la stessa che troverete nella pagina del piano dei conti (ce ne sono solo di meno), quindi non dovrete riorientarvi, e potete espandere o ridurre i livelli gerarchici per condensare la vista. Per facilitare il passaggio tra le pagine, la pagina **Panoramica** del piano dei conti è disponibile dalla pagina del piano dei conti.

## <a name="access-to-create-and-edit-accounts-and-account-categories"></a>Accesso per creare e modificare conti e categorie di conti

In una piccola organizzazione, come la società dimostrativa CRONUS, la maggior parte degli utenti può modificare il piano dei conti, ad eccezione degli utenti con una licenza membro del team. Tuttavia, nelle organizzazioni più grandi, l'accesso per modificare il piano dei conti è limitato da ruoli e autorizzazioni. Se sei un amministratore o hai il ruolo *Manager aziendale* o *Contabile*, puoi controllare le autorizzazioni per tutti gli utenti per assicurarti che le persone giuste abbiano accesso alle tabelle pertinenti. Per ulteriori informazioni, vedere [Per ottenere una sintesi delle autorizzazioni di un utente](ui-define-granular-permissions.md#to-get-an-overview-of-a-users-permissions).  

## <a name="see-also"></a>Vedere anche

[Finanze](finance.md)  
[Impostazione o modifica del piano dei conti](finance-setup-chart-accounts.md)  
[Business Intelligence](bi.md)  
[Assegnare autorizzazioni a utenti e gruppi](ui-define-granular-permissions.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
