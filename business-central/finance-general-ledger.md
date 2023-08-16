---
title: Informazioni sulla contabilità generale e COA
description: 'Descrive la contabilità generale, il piano dei conti e le categorie dei conti. Usa la pagina Setup contabilità generale per specificare le modalità di gestione di determinate questioni contabili relative alla società.'
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'analysis, history, track'
ms.search.form: '18, 20, 37, 65, 99, 312, 314, 313, 395, 552, 569, 570, 634, 790, 791, 1158'
ms.date: 08/24/2022
ms.author: edupont
---
# Informazioni sulla contabilità generale e sul piano dei conti

La contabilità generale (C/G) memorizza i dati finanziari e il piano dei conti indica in conti in cui sono registrati tutti i movimenti di contabilità generale. [!INCLUDE[prod_short](includes/prod_short.md)] include un piano dei conti standard pronto per supportare l'azienda.

## Setup contabilità generale e setup registrazioni COGE

Il setup della contabilità generale svolge un ruolo fondamentale nei processi finanziari perché definisce il modo in cui vengono registrati i dati. Due pagine in particolare svolgono un ruolo importante nella configurazione dei processi finanziari:  

* La pagina **Setup contabilità generale**

  Nella pagina **Setup contabilità generale** è possibile specificare le modalità di gestione di determinate questioni contabili relative alla società, quali:  

  * Dettagli relativi all'arrotondamento delle fatture  
  * Formati indirizzi  
  * Report finanziari

  > [!TIP]
  > La pagina **Setup contabilità generale** include campi generici e campi specifici per il paese o la regione. Se non si è certi del significato di un campo, suggeriamo di collaborare con il contabile per determinare se è rilevante per l'organizzazione. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

  Apri la pagina [qui](https://businesscentral.dynamics.com/?page=118).
  
* La pagina **Setup registrazioni COGE**

  Analogamente, nella pagina **Setup registrazioni COGE** è possibile specificare come si desidera impostare le combinazioni di categorie di registrazione business generale e le categorie di registrazione di articoli e servizi. I gruppi di registrazione mappano entità come clienti, venditori, articoli, risorse e documenti di vendita e acquisto ai conti della contabilità generale. Compilare una riga per ogni combinazione di categorie di registrazione business e di categorie di registrazione articoli/servizi. Ma è anche possibile aprire ogni riga nella relativa scheda di setup della registrazione. Per ulteriori informazioni vedi [Setup categorie di registrazione](finance-posting-groups.md).  

  > [!TIP]
  > Se non riesci a vedere i campi cercati nella pagina **Setup registrazioni COGE**, utilizza la barra di scorrimento orizzontale nella parte inferiore della pagina per scorrere verso destra.  

  Apri la pagina [qui](https://businesscentral.dynamics.com/?page=314).

## Il piano dei conti

Nel piano dei conti sono visualizzati tutti i conti C/G. Tramite il piano dei conti è possibile eseguire operazioni, quali:  

* Visualizzare i report che mostrano i movimenti e i saldi di contabilità generale.  
* Chiudere il conto economico.  
* Apri la scheda del conto di contabilità generale (C/G) per aggiungere o modificare le impostazioni.  
* Visualizza una lista delle categorie di registrazione per il conto.
* Visualizza i saldi attivi e passivi separatamente per un singolo conto.

È possibile aggiungere, modificare o eliminare i conti di contabilità generale. Tuttavia, per evitare le differenze, non è possibile eliminare un conto di contabilità generale se i relativi dati vengono utilizzato nel piano dei conti. Inoltre, a partire dal secondo ciclo di rilascio del 2022, puoi anche bloccare l'eliminazione accidentale di conti in periodi sensibili. Ulteriori informazioni nella sezione [Eliminazione di conti](finance-setup-chart-accounts.md#delete-accounts).  

## Categorie di conti

È possibile personalizzare la struttura dei rendiconti finanziari mappando i conti di contabilità generale alle categorie dei conti.  

La pagina **Categorie conto C/G** visualizza le categorie e le sottocategorie principali esistenti e i conti di contabilità generale assegnati ad esse. È possibile creare nuove sottocategorie e assegnarle categorie ai conti esistenti.  

Puoi creare un gruppo di categoria definendo un'indentazione di altre categorie in una riga nella pagina **Categorie conto C/G**. I gruppi di categorie consentono di ottenere una panoramica, in quanto ogni raggruppamento mostra un saldo totale. Ad esempio, puoi creare sottocategorie per i diversi tipi di cespiti e quindi creare gruppi di categorie per cespiti rispetto a cespiti correnti.  

È possibile definire se tipi specifici di report devono includere i conti in ciascuna sottocategoria. Le categorie di conto consentono di definire il layout dei rendiconti finanziari.  

### Esempio

Ad esempio, l'estratto conto di default presenta una sottocategoria relativa ai *contanti* nei *cespiti correnti*. Se vuoi che nell'estratto conto vengano considerate la piccola cassa e il conto assegni, effettua questi passaggi:

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Categorie conto C/G**, quindi scegli il collegamento correlato.
   1. In alternativa, apri la pagina [qui](https://businesscentral.dynamics.com/?page=790).
2. Scegliere l'azione **Modifica lista**.
3. Aggiungi due nuove sottocategorie: una per la piccola cassa e una per il conto assegni:
   1. Seleziona la categoria **Cespiti correnti**.
   2. Scegli l'azione **Nuovo**.
   3. Immetti il nome della sottocategoria nel campo **Descrizione**.
   4. Sul campo **Conti C/G nella categoria**, seleziona il conto C/G appropriato.
   5. Sul campo **Definizione report aggiuntivo** seleziona l'opzione **Conti di cassa**.
4. Applicare un rientro sotto la sottocategoria **Contanti**.
   1. Seleziona la sottocategoria creata nel passaggio 3.
   2. Scegli l'azione **Rientra**.
   3. Scegli l'azione **Sposta giù**.
   4. Scegli l'azione **Rientra** per impostare un rientro nella sottocategoria **Cassa**.

Quando scegli l'azione **Genera report finanziari**, o la prossima volta che viene generato il report, il tuo estratto conto mostrerà le seguenti righe:

* Saldo totale per contanti.
* Righe con saldi per piccola cassa e conto corrente.  

> [!NOTE]
> Se crei un conto C/G senza assegnare una categoria di conto, quando assegni il conto a un gruppo di registrazione [!INCLUDE[prod_short](includes/prod_short.md)] assegna automaticamente la categoria conto dal conto C/G immediatamente sopra il conto nel piano dei conti. Tuttavia, per includere il nuovo conto nei tuoi report finanziari, devi scegliere l'azione **Genera report finanziari** nella pagina **Categorie di conti C/G**. In alternativa, puoi aprire la pagina Scheda conto C/G, specificare la categoria del conto e quindi rigenerare il tuo report finanziario.

## Ottenere una rapida visione d'insieme

La pagina **Piano dei conti** visualizza i conti in una lista gerarchica che offre un accesso veloce alle informazioni chiave per ogni conto. Tuttavia, l'elenco è statico, e se hai molti account potresti dover scorrere per visualizzare diversi account. Se vuoi solo una rapida panoramica delle basi, come i cambiamenti netti e i saldi, la pagina **Sintesi del piano dei conti** è un'utile alternativa. Il layout delle colonne sulla pagina è ora lo stesso che troverai nella pagina **Piano dei conti** (anche se con meno colonne), quindi non dovrai riorientarti. È possibile espandere o comprimere i livelli gerarchici per condensare la vista. Per facilitare il passaggio tra le pagine, la pagina **Panoramica del piano dei conti** è disponibile dalla pagina **Piano dei conti**.

## Accesso per creare e modificare conti e categorie di conti

In una piccola organizzazione, come la società dimostrativa CRONUS, la maggior parte degli utenti può modificare il piano dei conti, ad eccezione degli utenti con una licenza membro del team. Tuttavia, le organizzazioni più grandi in genere utilizzano ruoli e autorizzazioni per limitare l'accesso alla modifica del piano dei conti. Se sei un amministratore o hai il ruolo *Manager aziendale* o *Contabile*, puoi controllare le autorizzazioni utente per assicurarti che le persone giuste abbiano accesso alle tabelle pertinenti. Per ulteriori informazioni, vedi la sezione [Per ottenere una sintesi delle autorizzazioni di un utente](ui-define-granular-permissions.md#to-get-an-overview-of-a-users-permissions).  

## Vedi il relativo [training Microsoft](/training/modules/business-central-configure-general-ledger-setup/)

## Vedere anche

[Impostare o modificare il piano dei conti](finance-setup-chart-accounts.md)  
[Assegnare autorizzazioni a utenti e gruppi](ui-define-granular-permissions.md)  
[Business Intelligence](bi.md)  
[Finanze](finance.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
