---
title: Informazioni sulla contabilità generale e COA
description: Descrive la contabilità generale, il piano dei conti e le categorie dei conti. Usa la pagina Setup contabilità generale per specificare le modalità di gestione di determinate questioni contabili relative alla società.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.search.form: 18, 20, 37, 65, 99, 312, 314, 313, 395, 552, 569, 570, 634, 790, 791, 1158
ms.date: 08/23/2022
ms.author: edupont
ms.openlocfilehash: 1d246e342d286e75da5aacaf1e6a305c5d0559e4
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/19/2022
ms.locfileid: "9534644"
---
# <a name="understanding-the-general-ledger-and-the-chart-of-accounts"></a>Informazioni sulla contabilità generale e sul piano dei conti

La contabilità generale memorizza i tuoi dati finanziari. Il piano dei conti mostra i conti in cui sono registrati i movimenti di contabilità generale. [!INCLUDE[prod_short](includes/prod_short.md)] include un piano dei conti standard pronto per supportare l'azienda.

## <a name="general-ledger-setup-and-general-posting-setup"></a>Setup contabilità generale e setup registrazioni COGE

Il setup della contabilità generale svolge un ruolo fondamentale nei processi finanziari perché definisce il modo in cui vengono registrati i dati. Due pagine svolgono un ruolo importante nella configurazione dei processi finanziari:  

* La pagina **Setup contabilità generale**

  Nella pagina **Setup contabilità generale** è possibile specificare le modalità di gestione di determinate questioni contabili relative alla società, quali:  

  * Dettagli relativi all'arrotondamento delle fatture  
  * Formati indirizzi  
  * Report finanziari  

  > [!TIP]
  > La pagina **Setup contabilità generale** include campi generici e campi specifici per il paese o la regione. Se non si è certi del significato di un campo, suggeriamo di collaborare con il contabile per determinare se è rilevante per l'organizzazione. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

    Apri la pagina [qui](https://businesscentral.dynamics.com/?page=118)
* La pagina **Setup registrazioni COGE**

    Analogamente, nella pagina **Setup registrazioni COGE** è possibile specificare come si desidera impostare le combinazioni di categorie di registrazione business generale e le categorie di registrazione di articoli e servizi. Le categorie di registrazione associano entità come clienti, fornitori, articoli, risorse e documenti di vendita o di acquisto a conti di contabilità generale. Compilare una riga per ogni combinazione di categorie di registrazione business e di categorie di registrazione articoli/servizi. Ma è anche possibile aprire ogni riga nella relativa scheda di setup della registrazione. Per ulteriori informazioni, vedere [Setup categorie di registrazione](finance-posting-groups.md).  

    > [!TIP]
    > Se non è possibile vedere i campi cercati nella pagina **Setup registrazioni COGE**, utilizzare la barra di scorrimento orizzontale nella parte inferiore della pagina per scorrere verso destra.  

    Apri la pagina [qui](https://businesscentral.dynamics.com/?page=314)

## <a name="the-chart-of-accounts"></a>Il piano dei conti

Nel piano dei conti sono visualizzati tutti i conti C/G. Tramite il piano dei conti è possibile eseguire operazioni, quali:  

* Visualizzare i report che mostrano i movimenti e i saldi di contabilità generale.  
* Chiudere il conto economico.  
* Apri la scheda del conto di contabilità generale (C/G) per aggiungere o modificare le impostazioni.  
* Visualizzare una lista delle categorie di registrazione che registrano nel conto.
* Visualizzare i saldi attivi e passivi separatamente per un singolo conto  

È possibile aggiungere, modificare o eliminare i conti di contabilità generale. Tuttavia, per evitare le differenze, non è possibile eliminare un conto di contabilità generale se i relativi dati vengono utilizzato nel piano dei conti. Per evitare errori in periodi delicati, puoi anche bloccare l'eliminazione dei conti. Per ulteriori informazioni, vedi [Eliminazione dei conti](finance-setup-chart-accounts.md#delete-accounts).  

## <a name="account-categories"></a>Categorie di conti

È possibile personalizzare la struttura dei rendiconti finanziari mappando i conti di contabilità generale alle categorie dei conti.  

La pagina **Categorie conto C/G** visualizza le categorie e le sottocategorie principali esistenti e i conti di contabilità generale assegnati ad esse. È possibile creare nuove sottocategorie e assegnarle categorie ai conti esistenti.  

È possibile creare un gruppo di categoria definendo un'indentazione di altre categorie in una riga nella pagina **Categorie conto C/G**. I gruppi di categorie consentono di ottenere una panoramica, in quanto ogni raggruppamento mostra un saldo totale. Ad esempio, è possibile creare sottocategorie per i diversi tipi di cespiti e quindi creare gruppi di categorie per cespiti rispetto a cespiti correnti.  

È possibile specificare se i conti di questa sottocategoria devono essere inclusi in determinati tipi di report. Le categorie di conto consentono di definire il layout dei rendiconti finanziari.  

### <a name="example"></a>Esempio

Ad esempio, l'estratto conto di default presenta una sottocategoria relativa ai *contanti* nei *cespiti correnti*. Se vuoi che nell'estratto conto vengano considerate la piccola cassa e il conto assegni, effettua questi passaggi:  

1. Aggiungi due nuove sottocategorie:

    * Una per la piccola cassa  
    * Una per il conto assegni  
2. Specifica la definizione report aggiuntiva **Conti cassa** per queste sottocategorie.  
3. Applicare un rientro sotto la sottocategoria **Contanti**.  

La prossima volta che generi i piani dei conti, il tuo estratto conto mostrerà le seguenti righe:

* Saldo totale per contanti.
* Righe con saldi per piccola cassa e conto corrente.  

> [!NOTE]
> Se crei un conto C/G senza assegnare una categoria di conto, quando assegni il conto a un gruppo di registrazione [!INCLUDE[prod_short](includes/prod_short.md)] assegna automaticamente la categoria conto dal conto C/G immediatamente sopra il conto nel piano dei conti. Tuttavia, per includere il nuovo conto nei tuoi report finanziari, devi scegliere l'azione **Genera report finanziari** nella pagina **Categorie di conti di contabilità generale**. In alternativa, puoi aprire la pagina Scheda conto C/G, specificare la categoria del conto e quindi rigenerare il tuo report finanziario.

## <a name="get-a-quick-overview"></a>Ottenere una rapida visione d'insieme

La pagina **Piano dei conti** visualizza i conti in una lista gerarchica che offre un accesso veloce alle informazioni chiave per ogni conto. Tuttavia, l'elenco è statico. Se hai molti conti potresti dover scorrere per visualizzarli. Se vuoi solo una rapida panoramica delle basi, come i cambiamenti netti e i saldi, la pagina **Sintesi del piano dei conti** è un'utile alternativa. Il layout delle colonne sulla pagina è ora lo stesso che troverai nella pagina **Piano dei conti** (anche se con meno colonne), quindi non dovrai riorientarti. È possibile espandere o comprimere i livelli gerarchici per condensare la vista. Per facilitare il passaggio tra le pagine, la pagina **Panoramica del piano dei conti** è disponibile dalla pagina **Piano dei conti**.

## <a name="access-to-create-and-edit-accounts-and-account-categories"></a>Accesso per creare e modificare conti e categorie di conti

In una piccola organizzazione, come la società dimostrativa CRONUS, la maggior parte degli utenti può modificare il piano dei conti. Esclusi gli utenti con licenza TEAM MEMBER. Tuttavia, le organizzazioni più grandi in genere utilizzano ruoli e autorizzazioni per limitare l'accesso alla modifica del piano dei conti. Se sei un amministratore o hai il ruolo **Manager aziendale** o **Contabile**, puoi controllare le autorizzazioni utente per assicurarti che le persone giuste abbiano accesso alle tabelle pertinenti. Per ulteriori informazioni, vedere [Per ottenere una sintesi delle autorizzazioni di un utente](ui-define-granular-permissions.md#to-get-an-overview-of-a-users-permissions).  

## <a name="see-related-microsoft-training"></a>Vedi il relativo [training Microsoft](/training/modules/business-central-configure-general-ledger-setup/)

## <a name="see-also"></a>Vedere anche

[Finanze](finance.md)  
[Impostare o modificare il piano dei conti](finance-setup-chart-accounts.md)  
[Business Intelligence](bi.md)  
[Assegnare autorizzazioni a utenti e gruppi](ui-define-granular-permissions.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
