---
title: Impostare i valori generali per i cespiti
description: 'Prima di utilizzare i cespiti occorre impostare i conti di default in contabilità generale, le categorie di registrazione, le chiavi di allocazione, le definizioni e i batch di registrazioni e i codici di classi.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.search.form: '5623, 5615, 5661, 5662, 5627, 5616, 5620, 5629, 5633, 5609, 5631, 5630, 5617, 5612, 5613, 5608, 5609, 5635, 9277'
ms.date: 03/25/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Impostare i valori generali per i cespiti

Per poter gestire i cespiti, devi dapprima impostare i conti C/G predefiniti, le chiavi di allocazione e i batch e le definizioni di registrazioni per registrare e riclassificare i cespiti. Inoltre, devi definire una gerarchia di classificazione (classi e sottoclassi) per strutturare i cespiti e, se necessario, definire le posizioni in cui archiviarli.

## Per impostare il comportamento generale per la funzionalità dei cespiti

Definisci il comportamento generale della funzionalità dei cespiti e la relativa numerazione dei documenti nella pagina **Setup cespiti**.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup cespiti**, quindi scegli il collegamento correlato.  
2. Compila i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Per impostare le categorie di registrazione dei cespiti

Utilizzo delle categorie di registrazione per definire categorie di cespiti. I movimenti per queste categorie di registrazione vengono registrati negli stessi conti di contabilità generale.

1. Scegli l'icona ![lampadina che apre la funzionalità Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Categorie registrazione cespiti**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Nuovo**.
3. Nella pagina **Scheda Cat. Reg. Cespite** compilare i campi in base alle esigenze.

    > [!NOTE]  
    >   Per assicurarsi che le contropartite per le diverse registrazioni cespiti vengono inserite automaticamente quando si sceglie l'azione **Inserisci conto cespiti** nelle righe di registrazione, seguire il passo successivo, sulla base della registrazione della rivalutazione.
4. Nella Scheda dettaglio **Contropartita**, selezionare nel campo **Contropartita rivalutazione** il conto di contabilità generale per cui si desidera inserire i movimenti di contropartita per la rivalutazione.

Per ulteriori informazioni sull'utilizzo dell'azione **Inserisci conto cespiti** nelle righe registrazioni cespiti in C/G richieste, vedi [Rivalutare i cespiti](fa-how-revalue.md).

## Per impostare le definizioni di registrazioni di cespiti

Una definizione è un layout predefinito di registrazioni. La definizione contiene informazioni relative ai codici di traccia, ai report e alla numerazione. Per ulteriori informazioni, vedi [Elaborazione delle registrazioni COGE](ui-work-general-journals.md).

Una definizione di registrazioni di cespiti viene creata automaticamente la prima volta che in [!INCLUDE[prod_short](includes/prod_short.md)] si apre la pagina **Registrazioni cespiti**, ma è possibile impostare altri modelli di registrazioni.  

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Definizioni registrazioni cespiti**, quindi scegli il collegamento correlato.  
2. Compila i campi come necessario.

## Per impostare codici di classi e sottoclassi di cespiti

Nei cespiti puoi definire una gerarchia di classificazione che può essere utilizzata per raggruppare i cespiti. La gerarchia ha due livelli: classi e sottoclassi.

### Codici di classi di cespiti

Le classi di cespiti rappresentano i movimenti di livello superiore nella gerarchia di classificazione in cui si raggruppano i cespiti. Ad esempio, utilizza le classi per dividere i cespiti in cespiti materiali o immateriali. Devi creare almeno una classe di cespiti nell'impostazione.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Classi cespiti**, quindi scegli il collegamento correlato.
2. Immetti i codici e i nomi delle classi di cespiti da creare.

### Codici di sottoclassi di cespiti

Le sottoclassi di cespiti rappresentano i movimenti di secondo livello nella gerarchia di classificazione in cui si raggruppano i cespiti. Ogni sottoclasse punta a una classe di livello superiore. Usa i codici di sottoclassi di cespiti per raggruppare i cespiti in categorie più specifiche quali edifici, veicoli, mobili e macchinari. Devi creare almeno una sottoclasse di cespiti nell'impostazione.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Sottoclassi cespiti**, quindi scegli il collegamento correlato.
2. Immetti i codici e i nomi delle sottoclassi di cespiti da creare.

## Avviare la registrazione dei cespiti

Se utilizzi i cespiti in [!INCLUDE[prod_short](includes/prod_short.md)] per la prima volta, devi impostare l'area di applicazione della contabilità generale prima di impostare i cespiti. La modalità di impostazione dipende dall'eventuale integrazione dei cespiti nella contabilità generale.  

La seguente procedura viene utilizzata se le transazioni cespiti devono essere registrate in contabilità generale.  

1. Completa le impostazioni di base per i cespiti.  
2. Riempi una scheda cespite per ogni cespite esistente.  
3. Creare un registro beni ammortizzabili cespiti per ogni scopo di ammortamento (ad esempio dichiarazioni fiscali e rendiconti finanziari). Per ogni registro beni ammortizzabili definisci i termini e le condizioni, ad esempio l'integrazione con la contabilità generale.

    Consentire l'integrazione con la contabilità generale eseguendo i passaggi seguenti. Innanzitutto, assicurati che l'integrazione con la contabilità generale non sia disabilitata per tutti i registri beni ammortizzabili, quindi registra i movimenti aperti e infine attiva l'integrazione con la contabilità generale.  
4. Scegli l'icona ![lampadina che apre la funzionalità Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registri beni ammortizzabili**, quindi scegli il collegamento correlato.  
5. Selezionare il registro beni ammortizzabili rilevante e quindi scegliere l'azione **Modifica** per aprire la pagina **Scheda registro beni ammortizz**.
6. Nella Scheda dettaglio **Integrazione**, disattiva tutti gli interruttori. Se hai più registri beni ammortizzabili, ripeti questo passaggio per ciascuno di essi.  
7. Nelle registrazioni cespiti immettere le seguenti righe per ogni cespite:
   * Una riga con il costo di acquisto.
   * Una riga con il fondo ammortamento alla fine dell'anno fiscale precedente.
   * Una riga con il fondo ammortamento dall'inizio dell'anno fiscale corrente alla data in cui [!INCLUDE[prod_short](includes/prod_short.md)] è impostato per iniziare il calcolo dell'ammortamento.

    È possibile ora inserire anche gli altri eventuali saldi di apertura, ad esempio svalutazione e rivalutazione.  
8. Dopo aver immesso e registrato le righe delle registrazioni per ogni cespite, attiva l'integrazione con la contabilità generale nel registro beni ammortizzabili.

Se i cespiti non sono integrati nella contabilità generale, ignora i passaggi 6 e 8.

## Per impostare i codici di ubicazione cespiti (facoltativo)

I codici di ubicazione cespiti definiscono gli identificatori per l'ubicazione dei cespiti, ad esempio reparto vendite, reception, amministrazione, produzione o warehouse. Puoi utilizzarli per registrare l'ubicazione di un cespite. Queste informazioni sono utili per le attività legate alle assicurazioni e al magazzino.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ubicazioni cespiti**, quindi scegli il collegamento correlato.
2. Immettere i codici e i nomi delle ubicazioni cespiti da creare.

## Per impostare le chiavi di allocazione dei cespiti (facoltativo)

Utilizza le chiavi di allocazione per allocare le transazioni a vari reparti o progetti. Ad esempio, puoi impostare una chiave di allocazione per allocare i costi di ammortamento dei veicoli all'amministrazione per il 35% ed al reparto vendite per il 65%. Per ulteriori informazioni, vedere [Allocazione di costi e ricavi](year-allocate-costs-income.md).

Le chiavi di allocazione sono valide per le classi di cespiti e non per singoli cespiti.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Categorie registrazione cespiti**, quindi scegli il collegamento correlato.  
2. Nella pagina **Categorie registrazione cespiti** scegliere l'azione **Allocazioni** e selezionare un tipo di registrazione.
3. Nella pagina **Allocazioni cespiti** compilare i campi in base alle esigenze.
4. Ripetere i passaggi 2 e 3 per ogni tipo di registrazione per cui si intendono definire le chiavi di allocazione.

## Per impostare i batch registrazioni dei cespiti (facoltativo)

È possibile impostare più batch di registrazioni, cioè registrazioni individuali per ogni definizione di registrazioni. Ad esempio, gli impiegati possono avere propri batch registrazioni in cui le loro iniziali vengono utilizzate come nome batch contabile. Per ulteriori informazioni, vedere [Elaborazione delle registrazioni COGE](ui-work-general-journals.md).  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Definizioni registrazioni cespiti**, quindi scegli il collegamento correlato.  
2. Selezionare la definizione di registrazioni opportuna e quindi scegliere l'azione **Batch**.
3. Nella pagina **Batch registrazioni cespiti** compilare i campi in base alle esigenze.

## Per impostare le definizioni di registrazioni di riclassificazione dei cespiti (facoltativo)

Usa registrazioni di riclassificazione dedicate per trasferire, suddividere o combinare cespiti. Una definizione di registrazione di riclassificazione dei cespiti viene creata automaticamente la prima volta che in [!INCLUDE[prod_short](includes/prod_short.md)] si apre la pagina **Reg. ricl. cespiti** ma puoi impostare altre definizioni di registrazioni di riclassificazione dei cespiti. Per ulteriori informazioni, vedere [Utilizzare le registrazioni COGE](ui-work-general-journals.md).  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Def. reg. riclass. cespiti**, quindi scegli il collegamento correlato.  
2. Compila i campi come necessario.

## Per impostare i batch registrazioni di riclassificazione dei cespiti (facoltativo)

È possibile impostare più batch di registrazioni, cioè registrazioni individuali per ogni definizione di registrazioni di riclassificazione. Ad esempio, gli impiegati possono avere un proprio batch di registrazioni di riclassificazione in cui le loro iniziali vengono utilizzate come nome del batch. Per ulteriori informazioni, vedere [Elaborazione delle registrazioni COGE](ui-work-general-journals.md).

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Def. reg. riclass. cespiti**, quindi scegli il collegamento correlato.  
2. Selezionare la definizione di registrazioni opportuna e quindi scegliere l'azione **Batch**.
3. Nella pagina **Batch reg. riclass. cespiti** compilare i campi in base alle esigenze.

## Vedere anche

[Impostazione di cespiti](fa-setup.md)  
[Panoramica dei cespiti](fa-manage.md)  
[Dati finanziari](finance.md)  
[Prepararsi a fare affari](ui-get-ready-business.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
