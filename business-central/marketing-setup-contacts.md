---
title: Impostare informazioni per i contatti| Documenti Microsoft
description: 'Descrive i task per specificare le informazioni e i codici, ad esempio, sui settori industriali e le relazioni d''affari, prima di impostare i contatti.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'relationship, prospect'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Setup contatti
Quando si creano contatti, è possibile immettere informazioni specifiche, ad esempio il settore a cui il contatto appartiene e la relazione d'affari con i contatti.

Prima di creare contatti e registrare dettagli sulle relazioni d'affari, è necessario impostare i diversi codici che verranno utilizzati per assegnare queste informazioni alle persone e alle società di contatto. È possibile impostare codici per gruppi di mailing, settori industriali, relazioni d'affari, origini Web, livelli organizzativi e responsabilità professionali. È possibile eseguire l'impostazione scegliendo l'azione **Nuovo** quando si cercano gli elenchi della scheda contatto.  

Dopo avere impostato queste informazioni, la creazione dei contatti risulterà molto più organizzata e la ricerca dei contatti in base a un determinato gruppo sarà più efficiente. Ogni gruppo della società sarà in grado di trovare le informazioni necessarie a rendere la comunicazione con i contatti più efficiente.

##  Per assegnare settori industriali a un contatto
I gruppi industriali vengono utilizzati per indicare il tipo di settore industriale a cui appartengono i contatti, ad esempio il settore del commercio al dettaglio o l'industria automobilistica.

> [!NOTE]
> Questa operazione è possibile soltanto per i contatti di tipo **Società**.

Il codice settore industriale definisce il tipo o la categoria del gruppo, ad esempio ANNUNCIO per la pubblicità o STAMPA per la TV e la radio. È possibile impostare più codici di settori industriali. Per definire i gruppi mailing, utilizzare la pagina **Settori industriali**.

1. Aprire la scheda contatto desiderata.
2. Scegliere l'azione **Società**, quindi l'azione **Settori industriali**. Verrà visualizzata la pagina **Settori industriali contatto**.
3. Nel campo **Codice settore industriale** selezionare il settore industriale da assegnare.

Ripetere tali passaggi per assegnare altri settori industriali. È inoltre possibile assegnare settori industriali nella finestra Lista Contatti seguendo la stessa procedura.

Il numero di settori industriali assegnati al contatto è visibile nel campo **Nr. settori industriali** della sezione **Segmentazione** della pagina **Scheda contatto**.

Una volta assegnati i settori industriali ai contatti, è possibile utilizzare queste informazioni per selezionare i contatti per i segmenti. Per ulteriori informazioni, vedere [Aggiungere contatti ai segmenti](marketing-add-contact-segment.md).

##  Per assegnare gruppi di mailing a un contatto
È possibile utilizzare i gruppi mailing per identificare gruppi di contatti a cui inviare le stesse informazioni. È possibile, ad esempio, impostare un gruppo mailing relativo ai contatti a cui si desidera inviare una notifica di un cambio di ufficio o un altro gruppo per inviare gli auguri delle festività.

Il codice gruppo mailing definisce il tipo o la categoria del gruppo, ad esempio SPOSTAMENTO per lo spostamento dell'ufficio o AUGURI per gli auguri festivi. È possibile impostare più codici di settori industriali. Per definire i gruppi mailing, utilizzare la pagina **Gruppi mailing**.

1. Aprire la scheda contatto desiderata.
2. Selezionare l'azione **Gruppi mailing**. Verrà visualizzata la pagina **Gruppi mailing contatto**.
3. Nel campo **Codice gruppi mailing** selezionare il gruppo mailing da assegnare.

Ripetere tali passaggi per assegnare altri gruppi mailing. È inoltre possibile assegnare altri gruppi di mailing dalla lista contatti seguendo la stessa procedura.

Il numero di gruppi di mailing assegnati al contatto viene visualizzato nel campo **Nr. di gruppi mailing** nella sezione **Segmentazione** della pagina **Scheda contatto**.

Dopo avere assegnato i gruppi di mailing ai contatti, è possibile utilizzare queste informazioni per selezionare i contatti per i segmenti. Per ulteriori informazioni, vedere [Aggiungere contatti ai segmenti](marketing-add-contact-segment.md).

## Per definire l'indirizzo alternativo di un contatto
È possibile assegnare un indirizzo alternativo al quale il contatto desidera ricevere messaggi di posta elettronica e informazioni, ad esempio la residenza estiva. È possibile anche assegnare uno o più intervalli di date per ogni indirizzo alternativo inserito per i contatti per specificarne il periodo di validità.

1. Aprire la scheda contatto desiderata.
2. Selezionare l'azione **Indirizzo alternativo** quindi scegliere l'azione **Scheda**.

    Per definire uno specifico periodo di validità dell'indirizzo alternativo, scegliere invece l'azione **Intervallo date**.
3. Nella pagina **Lista indirizzi alt. contatto**, immettere un indirizzo alternativo e compilare i campi nella pagina **indirizzo alternativo contatto**.

Ripetere tali passaggi per assegnare altri indirizzi alternativi. Per ogni indirizzo alternativo è possibile specificare uno o più intervalli di date.

## Per assegnare ruoli professionali a un contatto
È possibile aggiungere informazioni sui ruoli professionali che indicano il ruolo svolto dal contatto all'interno della propria società, ad esempio IT, gestione o produzione. È possibile utilizzare queste informazioni quando si inseriscono informazioni sui contatti.

> [!NOTE]
> Ciò è possibile solo per i contatti di tipo **Persona**.

Il codice ruolo professionale definisce il tipo o la categoria di processo, ad esempio MARKETING o ACQUISTO. È possibile impostare più codici di ruoli professionali. Per definire il ruolo professionale, utilizzare la pagina **Ruoli professionali**.

1. Aprire la scheda contatto desiderata.
2. Scegliere l'azione **Persona**, quindi l'azione **Ruoli professionali**. Verrà visualizzata la pagina **Ruolo professionale contatto**.
3. Nel campo **Cod. ruolo professionale** selezionare il ruolo professionale da assegnare.

Ripetere tali passaggi per assegnare altri ruoli professionali. È inoltre possibile assegnare ruoli professionali dalla lista Contatti seguendo la stessa procedura.

Il numero di ruoli professionali assegnati al contatto viene visualizzato nella pagina **Contatto**, sezione **Segmentazione**, in corrispondenza del campo **Nr. ruoli professionali**.

Dopo avere assegnato i ruoli professionali ai contatti, è possibile utilizzare queste informazioni per selezionare i contatti per i segmenti. Per ulteriori informazioni, vedere [Aggiungere contatti ai segmenti](marketing-add-contact-segment.md).

## Per assegnare livelli organizzativi a un contatto
È possibile usare i livelli organizzativi con i contatti per specificarne la posizione all'interno della società, ad esempio alta dirigenza. È possibile utilizzare queste informazioni quando si inseriscono informazioni sui contatti.

> [!NOTE]
> Ciò è possibile solo per i contatti di tipo **Persona**.

Il codice livello organizzativo definisce il tipo o la categoria di livello organizzativo, ad esempio CEO o CFO. È possibile impostare più codici di livello organizzativo. Per definire il livello organizzativo, utilizzare la pagina **Livelli organizzativi**.

1. Aprire la scheda contatto desiderata.
2. Nel campo **Livelli organizzativi** scegliere il codice che si desidera assegnare.

Una volta assegnati livelli organizzativi ai contatti, è possibile utilizzare queste informazioni per la creazione di segmenti.

Dopo avere assegnato i ruoli professionali ai contatti, è possibile utilizzare queste informazioni per selezionare i contatti per i segmenti. Per ulteriori informazioni, vedere [Aggiungere contatti ai segmenti](marketing-add-contact-segment.md).

## Per assegnare origini Web a un contatto
È possibile utilizzare le origini Web con le società contatto per identificare, ad esempio, motori di ricerca e siti Web dove effettuare la ricerca di informazioni sui contatti. Quando si assegna un'origine Web, specificare il motore di ricerca e la parola di ricerca che saranno utilizzati per individuare le informazioni richieste.

> [!NOTE]
> Questa operazione è possibile soltanto per i contatti di tipo **Società**.

Quando si assegna un'origine Web, specificare il motore di ricerca e la parola di ricerca che saranno utilizzati per individuare le informazioni richieste.

1. Aprire la scheda contatto desiderata.
2. Scegliere l'azione **Società**, quindi l'azione **Origini Web**. Verrà visualizzata la pagina **Origine Web contatto**.
3. Nel campo **Codice origine Web** scegliere l'origine Web che si desidera assegnare.
4. Nel campo **Parola ricerca** inserire la parola ricerca che verrà utilizzata per individuare le informazioni.

Ripetere tali passaggi per assegnare altre origini Web.

##  Per assegnare relazioni d'affari a un contatto
È possibile utilizzare le relazioni d'affari vengono utilizzate per indicare il tipo di relazione commerciale che intercorre con i contatti, ad esempio potenziale cliente, banca, consulente e fornitore di servizi e così via.

> [!NOTE]
> Questa operazione è possibile soltanto per i contatti di tipo **Società**.

1. Aprire la scheda contatto desiderata.
2. Scegliere l'azione **Società**, quindi l'azione **Relazioni d'affari**.
3. Nella pagina **Relazioni d'affari contatto**, nel campo **Codice relazione d'affari**, selezionare la relazione d'affari che si desidera assegnare.

Ripetere questi passaggi per assegnare altre relazioni d'affari.

Il numero di relazioni d'affari assegnate al contatto viene visualizzato nel campo **Nr. relazione d'affari** nella sezione **Segmentazione** nella pagina **Contatto**.

Una volta assegnate le relazioni d'affari ai contatti, è possibile utilizzare queste informazioni per selezionare i contatti per i segmenti. Per ulteriori informazioni, vedere [Aggiungere contatti ai segmenti](marketing-add-contact-segment.md).

## Copiare automaticamente informazioni specifiche da Società contatto a Persone contatto
Alcune informazioni relative alle società contatto sono identiche alle informazioni sulle persone contatto che lavorano all'interno di tali società, ad esempio i dettagli dell'indirizzo. Nella Scheda dettaglio **Eredità** della pagina **Setup marketing** è possibile specificare quali campi nella scheda contatto di una società sono copiati nella scheda contatto di una persona ogni volta che si crea una persona contatto per la società contatto.

Se si modifica uno di questi campi nella scheda società contatto, gli stessi campi vengono modificati nella scheda persona contatto, a meno che i campi non siano stati modificati manualmente in tale scheda.

Per ulteriori informazioni, vedere [Creare contatti](marketing-create-contact-companies.md).

## Utilizzare le impostazioni predefinite nei nuovi contatti
È possibile impostare l'applicazione in modo da assegnare automaticamente un codice lingua, un codice territorio, un codice agente e un codice paese specifici come default per ogni nuovo contatto creato. È inoltre possibile inserire un codice ciclo di vendita di default che verrà assegnato automaticamente a ogni nuova opportunità creata. Questa impostazione viene eseguita nella Scheda dettaglio **Default** della pagina **Setup marketing**

L'eredità dei campi viene sovrascritta ai valori di default impostati. Se ad esempio la lingua di default è stata impostata su Inglese ma la lingua della società contatto è Tedesco, quest'ultimo viene automaticamente assegnato come codice lingua per i contatti registrati relativi a tale società.

## Sincronizzazione di contatti con clienti, fornitori e conti correnti bancari
Per sincronizzare la scheda contatto con una scheda cliente, fornitore o conto corrente bancario, è necessario compilare il campo corrispondente nella sezione **Per codice relazione di bus.** della Scheda dettaglio **Interazioni** nella pagina **Setup marketing**.  

Per ulteriori informazioni, vedere [Sincronizzazione di contatti con clienti, fornitori e conti correnti bancari](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-employees-and-bank-accounts).

## Ricerca di contatti duplicati
È possibile impostare l'applicazione affinché vengano ricercati i duplicati ogni volta che si creano contatti; in alternativa, è possibile effettuare tale ricerca manualmente una volta completata la creazione dei contatti. È inoltre possibile aggiornare automaticamente le stringhe di ricerca ogni volta che le informazioni sui contatti vengono modificate o si crea un contatto. È possibile stabilire una percentuale di ricerca, ossia la percentuale di stringhe identiche che due contatti devono avere per essere considerati duplicati. Questa impostazione viene eseguita nella Scheda dettaglio **Duplicati** della pagina **Setup marketing**.

Una volta individuato un contatto duplicato, è possibile utilizzare la pagina **Unisci duplicato** per unirlo in un record di contatto che si intende mantenere. Per ulteriori informazioni, vedere [Unire record duplicati](sales-how-merge-duplicate-records.md).

## Vedere anche
[Gestione dei contatti](marketing-contacts.md)  
[Creare contatti](marketing-create-contact-companies.md)  
[Gestione delle opportunità di vendita](marketing-manage-sales-opportunities.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]