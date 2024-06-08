---
title: Informazioni sul piano dei conti
description: 'Descrive il piano dei conti, come impostarlo e come utilizzarlo.'
author: kennienp
ms.topic: conceptual
ms.search.keywords: 'analysis, history, track'
ms.search.form: '18, 20, 37, 65, 99, 312, 314, 313, 395, 552, 569, 570, 634, 790, 791, 1158'
ms.date: 04/17/2024
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
---

# <a name="understanding-the-chart-of-accounts"></a>Informazioni sul piano dei conti

Un piano dei conti (COA) funge da elenco completo dei conti finanziari e dei relativi numeri di riferimento. Un COA comprende in genere due categorie principali di conti:

- Conti patrimoniali: questi conti tengono traccia delle attività, dei debiti e del patrimonio netto della società.
- Conti economici: questi conti registrano le entrate provenienti da varie fonti e tengono traccia anche delle spese.

I conti patrimoniali sono ulteriormente classificati in tre gruppi:

1. Conti cespiti: questi conti tengono traccia di tutte le risorse preziose possedute dalla società.
1. Conti passività: registrano i debiti della società.
1. Conti patrimonio netto: rappresentano il valore residuo dell'azienda dopo aver sottratto le passività dalle attività.

I conti economici sono divisi in due gruppi:

1. Conti ricavi: questi conti acquisiscono le entrate della società da varie fonti.
1. Conti spesa: questi conti acquisiscono tutte le spese della società.

Utilizza il COA per registrare le transazioni nella contabilità generale della tua organizzazione. Ogni conto ha in genere un identificatore (numero di conto) e una didascalia o intestazione descrittiva e sono sistematicamente codificati in base al tipo di conto.

[!INCLUDE[prod_short](includes/prod_short.md)] include un piano dei conti standard pronto per supportare l'azienda.

La composizione del piano dei conti della società è una decisione strategica presa dal management (o dalla normativa specifica del paese). Varia in base al settore, al modello di business e alla struttura finanziaria della società. Ad esempio, a seconda del settore, potresti avere conti cespiti specifici su misura per le operazioni e le esigenze specifiche della società:

* Un'attività di vendita al dettaglio potrebbe enfatizzare l'inventario e la contabilità clienti.
* Un’azienda tecnologica potrebbe concentrarsi su cespiti immateriali come brevetti e software.
* Un impianto di produzione monitorerebbe i cespiti e le forniture.

## <a name="the-chart-of-accounts-page"></a>Pagina Piano dei conti

Nel piano dei conti sono visualizzati tutti i conti C/G. Tramite il piano dei conti puoi eseguire operazioni, quali:  

* Visualizzare i report che mostrano i movimenti e i saldi di contabilità generale.  
* Chiudere il conto economico.  
* Aprire la scheda Conto contabilità generale per aggiungere o modificare le impostazioni.  
* Visualizza una lista delle categorie di registrazione per il conto.
* Visualizza i saldi attivi e passivi separatamente per un singolo conto.

È possibile aggiungere, modificare o eliminare i conti di contabilità generale. Tuttavia, per evitare le differenze, non è possibile eliminare un conto di contabilità generale se i relativi dati vengono utilizzato nel piano dei conti. Inoltre, puoi bloccare l'eliminazione accidentale dei conti in periodi sensibili. Per ulteriori informazioni sulla protezione dei conti dall'eliminazione, vedi [Eliminazione di conti](finance-setup-chart-accounts.md#delete-accounts).  

## <a name="the-code-hierarchy-in-gl-accounts"></a>Gerarchia dei codici nei conti C/G

Le aziende in genere creano una struttura gerarchica nei codici dei conti C/G per riflettere la loro appartenenza nel piano dei conti. Ad esempio, in alcune implementazioni, i codici di conti C/G che iniziano con **1** indicano i conti cespiti, mentre i codici di conti C/G che iniziano con 3 indicano i conti patrimonio netto. In alcune aree esistono normative locali per l'utilizzo di un piano dei conti standard. Per aiutare gli utenti a comprendere questa gerarchia senza la necessità di conoscere la struttura del codice interno, puoi definire intestazioni e totali parziali nel piano dei conti che incapsulano queste strutture interne.

## <a name="designing-your-chart-of-accounts"></a>Progettazione del piano dei conti

Ogni riga nel piano dei conti è un conto C/G di uno dei seguenti tipi:

* Registrazione (i giornali possono registrare righe in questi conti)
* Intestazione (definisce un'intestazione complessiva nel piano dei conti)
* Totale (definisce una formula per un totale parziale nel piano dei conti)
* Inizio-Totale (definisce un'intestazione iniziale per un totale parziale nel piano dei conti. A tutte le righe successive fino alla riga Fine-Totale viene applicato un rientro)
* Fine-Totale (definisce un'intestazione finale per un totale parziale e la relativa formula nel piano dei conti. A tutte le righe successive dopo questa riga Fine-Totale viene applicato un rientro negativo)

Un piano dei conti minimalista può essere costituito solo da righe di conti di registrazione. Gli altri quattro tipi sono utilizzati per definire il modo in cui il piano dei conti mostra anche un rendiconto finanziario con intestazioni e totali parziali. I conti totali sono spesso utilizzati nei resoconti finanziari.

> [!TIP]
> Se utilizzi tipi di conto diversi da **Registrazione** nel tuo piano dei conti, puoi definire visualizzazioni diverse per mostrare i conti di registrazione "grezzi" senza i tipi di conto di tipo reporting per totale e intestazioni. Ad esempio, Mostra solo conti di registrazione e Nascondi conti bloccati.

## <a name="use-dimensions-to-simplify-your-chart-of-accounts"></a>Utilizzare le dimensioni per semplificare il piano dei conti

Le dimensioni sono valori che categorizzano i movimenti in modo da poterli seguire e analizzare nei documenti, ad esempio ordini vendita. Ad esempio, le dimensioni possono indicare il progetto o il reparto da cui un movimento proviene. Quindi, anziché impostare conti di contabilità generale distinti per ogni reparto e progetto, è possibile utilizzare le dimensioni come base per l'analisi ed evitare di dover creare un piano dei conti complesso.

Per ulteriori informazioni sulle dimensioni, vedi [Usare le dimensioni](finance-dimensions.md).

## <a name="get-a-quick-overview-of-your-finances"></a>Ottenere una rapida panoramica delle finanze

La pagina **Piano dei conti** visualizza i conti in una lista gerarchica che offre un accesso veloce alle informazioni chiave per ogni conto. Tuttavia, l'elenco è statico, e se hai molti account potresti dover scorrere per visualizzare diversi account. Se vuoi solo una rapida panoramica delle basi, come i cambiamenti netti e i saldi, la pagina **Sintesi del piano dei conti** è un'utile alternativa. Il layout delle colonne nella pagina è ora lo stesso della pagina **Piano dei conti** (anche se con meno colonne), quindi è facile capire. Puoi espandere o comprimere i livelli gerarchici. Per facilitare il passaggio tra le pagine, la pagina **Panoramica del piano dei conti** è disponibile dalla pagina **Piano dei conti**.

## <a name="access-to-create-and-edit-the-chart-of-accounts"></a>Accedere per creare e modificare il piano dei conti

In una piccola organizzazione, come la società dimostrativa CRONUS, la maggior parte degli utenti può modificare il piano dei conti, ad eccezione degli utenti con una licenza membro del team. Tuttavia, le organizzazioni più grandi in genere utilizzano ruoli e autorizzazioni per limitare l'accesso alla modifica del piano dei conti. Se sei un amministratore o hai il ruolo Manager aziendale o Contabile, puoi controllare le autorizzazioni utente per assicurarti che le persone giuste abbiano accesso alle tabelle pertinenti. Per ulteriori informazioni, vedi [Ottenere una sintesi delle autorizzazioni di un utente](ui-define-granular-permissions.md#get-an-overview-of-a-users-permissions).  


<!-- ## Standard chart of accounts in different regions
Uncomment when we have more examples added to our localization documentation

Some regions have defined standards for the chart of accounts structure you should use in your company. 

Here are some examples of such standards that have been implemented in localized versions of [!INCLUDE[prod_short](includes/prod_short.md)]:

* [Standard chart of accounts in Denmark](localfunctionality/denmark/how-to-set-up-standard-coa.md)
-->

## <a name="chart-of-accounts-best-practices"></a>Procedure consigliate relative al piano dei conti

Ecco alcune procedure consigliate che potresti prendere in considerazione quando sviluppi e mantieni i tuoi piani dei conti:

* Componi il piano dei conti della tua società per supportare le esigenze di reporting finanziario affinché il tuo management possa prendere decisioni strategiche.
* Considera l'idea di iniziare in modo semplice con meno conti C/G. Se necessario, puoi sempre aggiungere conti più dettagliati.
* Definisci intestazioni e totali parziali nel piano dei conti che riepilogano le strutture interne dei conti C/G.
* Utilizza le dimensioni per semplificare il piano dei conti. Non avere conti C/G specifici per ciascun prodotto o reparto.
* Aggiungi nuovi conti C/G non appena entrano, ma rimuovi i conti dal tuo piano dei conti solo durante la fine del periodo finanziario.

## <a name="see-also"></a>Vedere anche

[Impostare o modificare il piano dei conti](finance-setup-chart-accounts.md)  
[Informazioni sulla contabilità generale](finance-general-ledger.md)
[Analisi finanziaria](bi.md)  
[Panoramica dei dati finanziari](finance.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
