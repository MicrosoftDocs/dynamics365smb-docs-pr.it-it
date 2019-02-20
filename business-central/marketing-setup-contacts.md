---
title: Impostare informazioni per i contatti| Documenti Microsoft
description: Descrive i task per specificare le informazioni e i codici, ad esempio, sui settori industriali e le relazioni d'affari, prima di impostare i contatti.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 12/07/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 8a73de1aa2f4a0f633c401ea341bb7bde6579723
ms.openlocfilehash: 1f186a1eb1386d1f54b27a7ee9a9b3445c19e469
ms.contentlocale: it-it
ms.lasthandoff: 12/11/2018

---
# <a name="setting-up-contacts"></a>Configurazione dei contatti
Quando si creano contatti, è possibile immettere informazioni specifiche, ad esempio il settore a cui appartengono le loro società e la relazione d'affari con i contatti.

Prima di creare contatti e registrare dettagli sulle relazioni d'affari, è necessario impostare i diversi codici che verranno utilizzati per assegnare queste informazioni alle persone e alle società di contatto. È possibile impostare codici per gruppi di mailing, settori industriali, relazioni d'affari, origini Web, livelli organizzativi e responsabilità professionali.

Dopo avere impostato queste informazioni, la creazione dei contatti risulterà molto più organizzata e la ricerca dei contatti in base a un determinato gruppo sarà più efficiente. Ogni gruppo della società sarà in grado di trovare le informazioni necessarie a rendere la comunicazione con i contatti più efficiente.

In relazione alla configurazione dei contatti, è necessario Impostare la relazione d'affari che intercorre con i contatti, ad esempio potenziale cliente, banca, consulente e fornitore di servizi. Per ulteriori informazioni, vedere [Impostazione delle relazioni d'affari nelle società contatto](marketing-business-relations.md).

## <a name="setting-up-industry-groups-for-contact-companies"></a>Impostazione di settori industriali per le società contatto
I gruppi industriali vengono utilizzati per indicare il tipo di settore industriale a cui appartengono i contatti, ad esempio il settore del commercio al dettaglio o l'industria automobilistica.

L'utilizzo dei settori industriali nei contatti è un processo a due passaggi. Innanzitutto, occorre definire il codice dei settori industriali. Questo passaggio deve essere eseguito una sola volta per ogni settore industriale. Dopo aver creato un codice di settore industriale, è possibile iniziare ad assegnarlo alle società.

> [!NOTE]  
>   Per sincronizzare i contatti con fornitori, clienti o conti correnti bancari in altre sezioni dell'applicazione, è consigliabile impostare una relazione d'affari.

### <a name="to-define-an-industry-group-code"></a>Per definire un codice di settore industriale
Il codice settore industriale definisce il tipo o la categoria del gruppo, ad esempio ANNUNCIO per la pubblicità o STAMPA per la TV e la radio. È possibile impostare più codici di settori industriali. Per definire i gruppi mailing, utilizzare la pagina **Settori industriali**.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Settori industriali** e quindi scegliere il collegamento correlato.
2. Selezionare l'azione **Nuovo** e immettere un codice e una descrizione. Il codice può avere un massimo di 11 caratteri e può essere qualsiasi combinazione di numeri o lettere.

### <a name="AssignIndustryGroupContact"></a> Per assegnare settori industriali a un contatto
Non è possibile assegnare i settori industriali a un contatto, ma solo alle società.

1. Aprire il contatto.
2. Scegliere l'azione **Società**, quindi l'azione **Settori industriali**. Verrà visualizzata la pagina **Settori industriali contatto**.
3. Nel campo **Codice settore industriale** selezionare il settore industriale da assegnare.

Ripetere tali passaggi per assegnare altri settori industriali. È inoltre possibile assegnare settori industriali nella finestra Lista Contatti seguendo la stessa procedura.

Il numero di settori industriali assegnati al contatto è visibile nel campo **Nr. settori industriali** della sezione **Segmentazione** della pagina **Contatto**.

Una volta assegnati i settori industriali ai contatti, è possibile utilizzare queste informazioni per selezionare i contatti per i segmenti. Per ulteriori informazioni, vedere [Aggiungere contatti ai segmenti](marketing-add-contact-segment.md).

## <a name="setting-up-mailing-groups-for-contacts"></a>Impostazione di gruppi mailing per i contatti
È possibile utilizzare i gruppi mailing per identificare gruppi di contatti a cui inviare le stesse informazioni. È possibile, ad esempio, impostare un gruppo mailing relativo ai contatti a cui si desidera inviare una notifica di un cambio di ufficio o un altro gruppo per inviare gli auguri delle festività.

L'utilizzo dei gruppi mailing nei contatti è un processo a due passaggi. Innanzitutto, occorre definire il codice dei gruppi mailing. Questo passaggio deve essere eseguito una sola volta per ogni gruppo mailing. Dopo aver creato un codice di gruppo di mailing, è possibile iniziare ad assegnarlo alle società.

### <a name="to-define-mailing-group-codes"></a>Per definire i codici di gruppo di mailing
Il codice gruppo mailing definisce il tipo o la categoria del gruppo, ad esempio SPOSTAMENTO per lo spostamento dell'ufficio o AUGURI per gli auguri festivi. È possibile impostare più codici di settori industriali. Per definire i gruppi mailing, utilizzare la pagina **Gruppi mailing**.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Gruppi mailing** e quindi scegliere il collegamento correlato.
2. Selezionare l'azione **Nuovo** e immettere un codice e una descrizione. Il codice può avere un massimo di 11 caratteri e può essere qualsiasi combinazione di numeri o lettere.

### <a name="AssignMailGroupContact"></a> Per assegnare gruppi di mailing a un contatto
1. Aprire il contatto.
2. Selezionare l'azione **Gruppi mailing**. Verrà visualizzata la pagina **Gruppi mailing contatto**.
3. Nel campo **Codice gruppi mailing** selezionare il gruppo mailing da assegnare.

Ripetere tali passaggi per assegnare altri gruppi mailing. È inoltre possibile assegnare altri gruppi di mailing dalla lista contatti seguendo la stessa procedura.

Il numero di gruppi di mailing assegnati al contatto viene visualizzato nel campo **Nr. di gruppi mailing** nella sezione **Segmentazione** della pagina **Contatto**.

Dopo avere assegnato i gruppi di mailing ai contatti, è possibile utilizzare queste informazioni per selezionare i contatti per i segmenti. Per ulteriori informazioni, vedere [Aggiungere contatti ai segmenti](marketing-add-contact-segment.md).

## <a name="setting-up-alternate-addresses-for-contacts"></a>Impostare indirizzi alternativi per i contatti
È possibile assegnare un indirizzo alternativo presso il quale talvolta i contatti ricevono messaggi di posta e informazioni, ad esempio la casa per le vacanze estive. È possibile anche assegnare uno o più intervalli di date per ogni indirizzo alternativo inserito per i contatti per specificarne il periodo di validità.

### <a name="to-assign-an-alternate-address"></a>Per assegnare un indirizzo alternativo
1. Aprire il contatto.
2. Selezionare **Indirizzo alternativo** l'azione quindi selezionare **Scheda**. Verrà visualizzata la pagina **Lista indirizzi alt. contatto**.
3. Inserire un nuovo indirizzo alternativo e compilare i campi nella pagina dell'**indirizzo alternativo del contatto**.

Ripetere tali passaggi per assegnare altri indirizzi alternativi. Per ogni indirizzo alternativo è possibile specificare uno o più intervalli di date.

È inoltre possibile assegnare indirizzi alternativi dalla pagina della lista dei contatti seguendo la stessa procedura.

### <a name="to-assign-an-alternate-address-date-range"></a>Per assegnare intervalli di date per gli indirizzi alternativi
1. Aprire il contatto.
2. Selezionare l'azione **Indirizzo alternativo**, quindi selezionare **Intervallo date**. Verrà visualizzata la pagina **Intervallo date ind. altern.contatto**.
3. Scegliere l'azione **Nuovo**.
4. Nel campo **Codice indirizzi alt. contatto** selezionare un indirizzo alternativo del contatto e compilare i campi **Data di inizio** e **Data di fine**.

Ripetere tali passaggi per assegnare altri intervalli date.

## <a name="setting-up-job-responsibilities-for-contact-persons"></a>Impostazione di ruoli professionali per i contatti
È possibile aggiungere informazioni sui ruoli professionali che indicano il ruolo svolto dal contatto all'interno della propria società, ad esempio IT, gestione o produzione. È possibile utilizzare queste informazioni quando si inseriscono informazioni sui contatti.

L'utilizzo dei ruoli professionali nei contatti è un processo a due passaggi. Innanzitutto, occorre definire il codice ruolo professionale. Questo passaggio deve essere eseguito una sola volta per ogni ruolo professionale. Dopo aver creato un codice ruolo professionale, è possibile iniziare ad assegnarlo ai contatti.

### <a name="to-define-a-job-responsibility-code"></a>Per definire un codice ruolo professionale
Il codice ruolo professionale definisce il tipo o la categoria di processo, ad esempio MARKETING o ACQUISTO. È possibile impostare più codici di ruoli professionali. Per definire il ruolo professionale, utilizzare la pagina **Ruoli professionali**.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ruoli professionali** e quindi scegliere il collegamento correlato.
2. Selezionare l'azione **Nuovo** e immettere un codice e una descrizione. Il codice può avere un massimo di 11 caratteri e può essere qualsiasi combinazione di numeri o lettere.

### <a name="to-assign-job-responsibilities-to-a-contact-person"></a>Per assegnare ruoli professionali a un contatto
Non è possibile assegnare ruoli professionali alle società contatto.

1. Aprire il contatto.
2. Scegliere l'azione **Persona**, quindi l'azione **Ruoli professionali**. Verrà visualizzata la pagina **Ruolo professionale contatto**.
3. Nel campo **Cod. ruolo professionale** selezionare il ruolo professionale da assegnare.

Ripetere tali passaggi per assegnare altri ruoli professionali. È inoltre possibile assegnare ruoli professionali dalla lista Contatti seguendo la stessa procedura.

Il numero di ruoli professionali assegnati al contatto viene visualizzato nella pagina **Contatto**, sezione **Segmentazione**, in corrispondenza del campo **Nr. ruoli professionali**.

Dopo avere assegnato i ruoli professionali ai contatti, è possibile utilizzare queste informazioni per selezionare i contatti per i segmenti. Per ulteriori informazioni, vedere [Aggiungere contatti ai segmenti](marketing-add-contact-segment.md).

## <a name="setting-up-organizational-levels-for-contact-persons"></a>Configurazione di livelli organizzativi per i contatti
È possibile usare i livelli organizzativi con i contatti per specificarne la posizione all'interno della società, ad esempio alta dirigenza. È possibile utilizzare queste informazioni quando si inseriscono informazioni sui contatti.

L'utilizzo dei livelli organizzativi nei contatti è un processo a due passaggi. Innanzitutto, occorre definire il codice livello organizzativo. Questo passaggio deve essere eseguito una sola volta per ogni livello organizzativo. Dopo aver creato un codice livello organizzativo, è possibile iniziare ad assegnarlo ai contatti.

### <a name="to-define-an-organizational-level-code"></a>Per definire un codice livello organizzativo
Il codice livello organizzativo definisce il tipo o la categoria di livello organizzativo, ad esempio CEO o CFO. È possibile impostare più codici di livello organizzativo. Per definire il livello organizzativo, utilizzare la pagina **Livelli organizzativi**.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Livelli organizzativi** e quindi scegliere il collegamento correlato.
2. Selezionare l'azione **Nuovo** e immettere un codice e una descrizione. Il codice può avere un massimo di 11 caratteri e può essere qualsiasi combinazione di numeri o lettere.

### <a name="to-assign-organizational-levels-to-a-contact-person"></a>Per assegnare livelli organizzativi a un contatto
È possibile assegnare un livello organizzativo ai contatti costituiti da persone, non alle società contatto. È possibile assegnare un livello organizzativo a ciascun contatto.

1. Aprire il contatto.
2. Nel campo **Livelli organizzativi** scegliere il codice che si desidera assegnare.

Una volta assegnati livelli organizzativi ai contatti, è possibile utilizzare queste informazioni per la creazione di segmenti.

Dopo avere assegnato i ruoli professionali ai contatti, è possibile utilizzare queste informazioni per selezionare i contatti per i segmenti. Per ulteriori informazioni, vedere [Aggiungere contatti ai segmenti](marketing-add-contact-segment.md).

## <a name="setting-up-web-sources-for-contact-companies"></a>Impostazione delle origini Web per le società contatto
È possibile utilizzare le origini Web con le società contatto per identificare, ad esempio, motori di ricerca e siti Web dove effettuare la ricerca di informazioni sui contatti. Quando si assegna un'origine Web, specificare il motore di ricerca e la parola di ricerca che saranno utilizzati per individuare le informazioni richieste.

L'utilizzo delle origini Web nei contatti è un processo a due passaggi. Innanzitutto, occorre definire il codice origine Web. Questo passaggio deve essere eseguito una sola volta per ogni origine Web. Dopo aver creato un codice origine Web, è possibile iniziare ad assegnarlo ai contatti.

### <a name="to-define-a-web-source-code"></a>Per definire un codice origine Web
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Origini Web** e quindi scegliere il collegamento correlato.
2. Scegliere l'azione **Nuovo**.
3. Compilare i campi **Codice**, **Descrizione** e **URL**.

    Nel campo **URL** immettere %1 per inserire un segnaposto per una parola di ricerca nell'URL. Quando si apre l'origine Web da un contatto, %1 verrà automaticamente sostituito con la parola da ricercare (ad esempio il nome della società) inserita nella pagina **Origini Web contatto**.

Ripetere tali passaggi per impostare altre origini Web.

### <a name="to-assign-web-sources-to-a-contact-company"></a>Per assegnare origini Web a una società contatto
Quando si assegna un'origine Web, specificare il motore di ricerca e la parola di ricerca che saranno utilizzati per individuare le informazioni richieste.

1. Aprire il contatto.
2. Scegliere l'azione **Società**, quindi l'azione **Origini Web**. Verrà visualizzata la pagina **Origine Web contatto**.
3. Nel campo **Codice origine Web** scegliere l'origine Web che si desidera assegnare.
4. Nel campo **Parola ricerca** inserire la parola ricerca che verrà utilizzata per individuare le informazioni.

Ripetere tali passaggi per assegnare altre origini Web.

È inoltre possibile assegnare l'origine Web dalla pagina **Lista Contatti** seguendo la stessa procedura.

## <a name="see-also"></a>Vedi anche
[Gestione dei contatti](marketing-contacts.md)  
[Gestione delle opportunità di vendita](marketing-manage-sales-opportunities.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

