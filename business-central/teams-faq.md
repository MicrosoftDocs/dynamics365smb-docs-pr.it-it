---
title: Domande frequenti su Teams
description: Ottenere risposte ad alcune domande tipiche sull'utilizzo di Teams e Business Central.
author: jswymer
ms.author: jswymer
ms.topic: faq
ms.search.keywords: 'Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, faq, errors'
ms.date: 09/28/2022
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Domande frequenti su Teams

[!INCLUDE [online_only](includes/online_only.md)]

Questo articolo risponde ad alcune delle domande che potresti avere sull'utilizzo di Microsoft Teams e [!INCLUDE [prod_short](includes/prod_short.md)].

## [Generale](#tab/general)

### Come si accede all'app [!INCLUDE [prod_short.md](includes/prod_short.md)] in Teams?

Dopo aver installato l'app, ti verrà chiesto di accedere la prima volta che usi l'app, quando incolli un collegamento [!INCLUDE [prod_short.md](includes/prod_short.md)] nella chat di Teams o quando scegli l'azione **Dettagli** in una scheda di Teams. A seconda del client Teams, potrebbe essere necessario immettere le credenziali utilizzate per l'accesso a [!INCLUDE [prod_short.md](includes/prod_short.md)].

### Come ci si disconnette dall'app [!INCLUDE [prod_short.md](includes/prod_short.md)] in Teams?

Per disconnettersi dall'identità in Teams usata per connetterti a [!INCLUDE [prod_short.md](includes/prod_short.md)], vai a qualsiasi casella di composizione della chat, fai clic con il pulsante destro sull'icona [!INCLUDE [prod_short.md](includes/prod_short.md)] sotto la casella, quindi scegli **Impostazioni**. Quando viene visualizzata la finestra, controlla la tua identità attualmente collegata e quindi scegli **Disconnetti**.

### L'app per Teams si connette a [!INCLUDE [prod_short.md](includes/prod_short.md)] in locale? 

Nr. L'app [!INCLUDE [prod_short.md](includes/prod_short.md)] per Teams funziona solo con [!INCLUDE [prod_short.md](includes/prod_short.md)] Online. Non ci sono piani per supportare tipi di implementazione [!INCLUDE [prod_short.md](includes/prod_short.md)], ad esempio locale, cloud ibrido o cloud privato, che Microsoft non ospita o gestisce direttamente.

### L'app è utilizzabile con più società e ambienti? 

Sì. Per cercare contatti in un'altra azienda, vai a [Impostazioni](across-teams-settings.md). Quando l'app [!INCLUDE [prod_short.md](includes/prod_short.md)] espande un collegamento in una scheda, il collegamento deve contenere il nome dell'ambiente e dell'azienda affinché l'app corrisponda al record nella società appropriata. Puoi incollare collegamenti a qualsiasi società e ambiente a cui hai accesso nella tua organizzazione e dall'account [!INCLUDE [prod_short.md](includes/prod_short.md)] che hai utilizzato per accedere. I partecipanti alla chat vedranno la scheda. Ma non possono visualizzare i dettagli della scheda a meno che non dispongano delle autorizzazioni per la società o l'ambiente in cui è archiviato il record.

### In quali paesi o regioni è disponibile l'app [!INCLUDE [prod_short.md](includes/prod_short.md)]? 

L'app [!INCLUDE [prod_short.md](includes/prod_short.md)] per Teams non è limitata per paese o area geografica. L'app è disponibile in tutti i mercati attualmente supportati dal marketplace di Teams. 

### L'app [!INCLUDE [prod_short.md](includes/prod_short.md)] è utilizzabile con qualsiasi localizzazione di [!INCLUDE [prod_short.md](includes/prod_short.md)]? 

Sì. L'app è progettata per funzionare con qualsiasi localizzazione di [!INCLUDE [prod_short.md](includes/prod_short.md)], indipendentemente dal fatto che la localizzazione sia offerta direttamente da Microsoft o tramite un partner. Per ulteriori informazioni, vedi [Disponibilità a livello di paese/area geografica e lingue supportate](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json).

### <a name="language"></a>Quali lingue sono supportate dall'app [!INCLUDE [prod_short.md](includes/prod_short.md)]?

Due cose determinano la lingua utilizzata per le schede e i dettagli delle schede in Teams:

1. La lingua in Teams, visibile nelle impostazioni dell'account in Teams. 
2. La lingua in [!INCLUDE [prod_short.md](includes/prod_short.md)], visibile nel client Web di [!INCLUDE [prod_short.md](includes/prod_short.md)] (vedi [Modificare l'impostazione di base - Lingua](ui-change-basic-settings.md#language)).

Nella tabella seguente viene descritto come l'esperienza differisce per autori e destinatari dei messaggi, a seconda delle impostazioni della lingua e della disponibilità delle lingue.

|Chi|Scheda|Dettagli scheda |
|-|----|--------------| 
|Autore messaggio |Visualizzata nella lingua specificata in Teams. Se [!INCLUDE [prod_short.md](includes/prod_short.md)] non offre la stessa lingua, la scheda è visualizzata in inglese. |Viene visualizzata nella lingua specificata per te in [!INCLUDE [prod_short.md](includes/prod_short.md)], che può includere le lingue delle app di lingua fornite dai partner. |
|Destinatario messaggio |Visualizzata nella lingua dell'autore del messaggio. |Visualizzata nella lingua specificata in [!INCLUDE [prod_short.md](includes/prod_short.md)], |

Per l'elenco delle lingue supportate per [!INCLUDE [prod_short.md](includes/prod_short.md)], vedi [Lingue supportate](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json#supported-languages).

### L'app [!INCLUDE [prod_short.md](includes/prod_short.md)] funziona con le soluzioni del settore?

Sì. Ma solo alcune funzionalità dell'app funzionano con [app Embed](/dynamics365/business-central/dev-itpro/deployment/embed-app-overview):

- L'app funziona con collegamenti basati sul modello **\*.bc.dynamics.com** tipicamente utilizzato con app Embed.
- La Ricerca Contatti non è disponibile per le app Embed che sostituiscono l'applicazione di base di Microsoft.

### [!INCLUDE [prod_short.md](includes/prod_short.md)] è utilizzabile con l'app per dispositivi mobili Teams?

Sì. L'app [!INCLUDE [prod_short.md](includes/prod_short.md)] può essere installata dall'app desktop o dal browser di Teams o da un amministratore per tutti gli utenti. Una volta installata, l'app [!INCLUDE [prod_short.md](includes/prod_short.md)] è automaticamente disponibile in Teams per iOS e Android. Nei dispositivi mobili, puoi visualizzare solo le schede inviate da altri, accedere ai dettagli o visualizzare la scheda per un'esperienza completa nell'app per dispositivi mobili [!INCLUDE [prod_short.md](includes/prod_short.md)]. Non puoi incollare collegamenti che si espandono nelle schede durante la composizione dei messaggi o la ricerca dei contatti. Per informazioni sui requisiti minimi per i dispositivi mobili, vedi [Requisiti minimi per l'utilizzo di Business Central](product-requirements.md).

### L'app [!INCLUDE [prod_short.md](includes/prod_short.md)] per Teams è uguale all'app [!INCLUDE [prod_short.md](includes/prod_short.md)] per iOS e Android?

No. L'app per Teams è un componente aggiuntivo di Microsoft Teams ed è progettata esclusivamente per la collaborazione in Teams. In alternativa, l'app per dispositivi mobili [!INCLUDE [prod_short.md](includes/prod_short.md)] offre un'esperienza completa per l'utilizzo dei dati di [!INCLUDE [prod_short.md](includes/prod_short.md)] nei dispositivi mobili.

Gli utenti di dispositivi mobili sono incoraggiati a installare sia l'app per dispositivi mobili che l'app per Teams per usufruire di tutti i vantaggi inerenti all'utilizzo di [!INCLUDE [prod_short.md](includes/prod_short.md)]. Con entrambe le app installate, puoi scegliere l'azione **Apri nuova finestra** in una scheda di Teams per aprire i dettagli della scheda nell'app per dispositivi mobili [!INCLUDE [prod_short.md](includes/prod_short.md)]. Per informazioni sull'installazione di [!INCLUDE [prod_short.md](includes/prod_short.md)] e sull'app per dispositivi mobili Teams, vedi:

- [Installare Business Central sul dispositivo mobile](install-mobile-app.md)
- [Scarica l'app per dispositivi mobili Teams](https://support.microsoft.com/office/download-the-mobile-app-for-teams-5940ebdc-0082-4fb1-83c4-751edc23dcb5) nel supporto tecnico Microsoft

### L'app [!INCLUDE [prod_short.md](includes/prod_short.md)] è utilizzabile in tutti i client Teams?

Nr. L'app [!INCLUDE [prod_short.md](includes/prod_short.md)] per Teams non è supportata se installata come pacchetto per macOS o Linux. Su queste piattaforme puoi invece accedere a Teams usando un browser supportato.

Per i requisiti minimi in [!INCLUDE [prod_short.md](includes/prod_short.md)], vedi [Requisiti minimi per l'utilizzo di Business Central](product-requirements.md#teams).

Per informazioni sulla scelta dei client Teams e su come installarli, vedi [Installare client per Microsoft Teams](/microsoftteams/get-clients) nella documentazione di Teams.

### Qual è il migliore client Teams per [!INCLUDE [prod_short.md](includes/prod_short.md)]?

Esistono solo piccole differenze e limitazioni tra i client Teams che possono influire sull'esperienza con l'app [!INCLUDE [prod_short.md](includes/prod_short.md)] per Teams. Quando scegli un client Teams, considera quanto segue:

- Non è possibile accedere alla fotocamera e alla posizione dalla finestra dei dettagli nell'app desktop Teams.
- I numeri di telefono non possono essere attivati dalla finestra dei dettagli in Teams per iOS, Android o nel browser.
- L'utilizzo di Microsoft Edge con Teams nel browser ti consente di lavorare facilmente in più identità e account accedendo a Teams da diversi profili. Per informazioni sull'utilizzo dei profili in Microsoft Edge, vedi [Accedere e crea più profili in Microsoft Edge](https://support.microsoft.com/office/sign-in-and-create-multiple-profiles-in-microsoft-edge-df94e622-2061-49ae-ad1d-6f0e43ce6435) nel supporto tecnico Microsoft.

### Qual è il modo migliore di presentare [!INCLUDE [prod_short.md](includes/prod_short.md)] e Microsoft Teams a potenziali clienti?

Se si è un partner rivenditore, è possibile che si intenda disporre di un ambiente da mostrare ai potenziali clienti nell'ambito di presentazioni prima della vendita. Per non influire sul funzionamento di Microsoft Teams nell'organizzazione, puoi ottenere un account demo di Microsoft 365 all'indirizzo [https://aka.ms/CDX](https://aka.ms/CDX). Questo account ti offre il controllo completo di un'organizzazione Azure indipendente che include Microsoft Teams e [!INCLUDE [prod_short.md](includes/prod_short.md)]. Per ulteriori informazioni, vedi [Preparazione degli ambienti dimostrativi di Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/administration/demo-environment).

### L'app [!INCLUDE [prod_short.md](includes/prod_short.md)] per Teams consente la personalizzazione?

L'app [!INCLUDE [prod_short.md](includes/prod_short.md)] per Teams può visualizzare schede per collegamenti a pagine e tabelle dei clienti in [!INCLUDE [prod_short.md](includes/prod_short.md)], come le pagine e tabelle originate dalle estensioni personalizzate o da AppSource.

I campi visualizzati in una scheda di Teams possono essere modificati dalle personalizzazioni di [!INCLUDE [prod_short.md](includes/prod_short.md)] installate per l'organizzazione. Le schede non considerano alcuna personalizzazione specifica del ruolo o personalizzazione dell'utente. Tuttavia, la finestra dei dettagli di una scheda mostra i dettagli dei record come visualizzati in [!INCLUDE [prod_short.md](includes/prod_short.md)], comprese estensioni, personalizzazioni dei ruoli e personalizzazione dell'utente.

Quando si cercano contatti, i campi corrispondenti nella tabella **Contatti** e i campi visualizzati nei risultati della ricerca non sono interessati da alcuna personalizzazione.

### In che modo le autorizzazioni richieste dall'app influiscono sulla privacy?

Prima di installare l'app [!INCLUDE [prod_short.md](includes/prod_short.md)] per Teams, è possibile rivedere le autorizzazioni minime necessarie per il funzionamento dell'app. Installando l'app, concedi all'app l'autorizzazione per ricevere i messaggi e i dati forniti e a Teams l'autorizzazione per archiviare ed elaborare tali messaggi.

Alcune funzionalità di [!INCLUDE [prod_short.md](includes/prod_short.md)] richiedono inoltre l'apertura di collegamenti esterni o l'accesso alla fotocamera o alla posizione geografica. Supponi ad esempio di voler acquisire una foto di una fattura di acquisto per l'elaborazione. L'app [!INCLUDE [prod_short.md](includes/prod_short.md)] non utilizza queste funzioni senza il consenso dell'utente. L'utilizzo avviene inoltre solo tramite funzionalità specifiche nella finestra **Dettagli**. Quando usi una di queste funzionalità per la prima volta, Teams visualizza una finestra di dialogo in cui ti richiede di concedere l'accesso alle funzionalità del dispositivo richieste.

- Nel desktop di Teams rivedere e modificare le autorizzazioni dell'app dalla finestra **Impostazioni**. Selezionare la propria immagine del profilo nella parte superiore dell'app, selezionare **Impostazioni** > **Autorizzazioni**, quindi l'app [!INCLUDE [prod_short.md](includes/prod_short.md)].

- Per Teams nel browser e Teams per iOS o Android, è possibile rivedere o modificare le autorizzazioni tramite le impostazioni del browser o del dispositivo.

> [!NOTE]
> Le funzionalità esatte di [!INCLUDE [prod_short.md](includes/prod_short.md)] che richiedono le autorizzazioni variano in base alle app aggiuntive e alle personalizzazioni applicate all'ambiente di [!INCLUDE [prod_short.md](includes/prod_short.md)] a cui ti colleghi.

### Dove posso ottenere informazioni sulla privacy? 

Puoi ottenere informazioni su come Microsoft gestisce i tuoi dati nell'[Informativa sulla privacy di Microsoft](https://go.microsoft.com/fwlink/?linkid=2030602). 

Contatta il tuo amministratore per informazioni su come la tua organizzazione gestisce la privacy dei tuoi dati.

### Come si disinstalla l'app [!INCLUDE [prod_short.md](includes/prod_short.md)] per Teams?

Per rimuovere l'app installata, vai a qualsiasi casella di composizione della chat, trova l'icona [!INCLUDE [prod_short.md](includes/prod_short.md)] sotto la casella, fai clic con il pulsante destro del mouse sull'icona e scegli **Disinstalla**.  

### Microsoft continuerà a migliorare l'app [!INCLUDE [prod_short.md](includes/prod_short.md)] per Teams?

In Microsoft, i feedback della nostra variegata comunità di utenti vengono costantemente monitorati e si agisce in base ai migliori suggerimenti. Per informazioni sui miglioramenti futuri dell'app [!INCLUDE [prod_short.md](includes/prod_short.md)] per Teams, vedi il [Piano di rilascio di Dynamics 365](/dynamics365-release-plan/2021wave1/).

Se desideri partecipare al miglioramento dell'app per Teams o hai un'idea che ti permetterebbe di semplificare il tuo lavoro o le tue esperienze collaborative in Teams, aggiungila o vota per quelle esistenti in [https://aka.ms/BusinessCentralIdeas](https://aka.ms/BusinessCentralIdeas).

### Dove posso trovare l'integrazione di Teams nel client Web di Business Central? 

Per informazioni sulla funzionalità nel client web che si collega a Teams, vedi [Condividere record e collegamenti di pagina in Microsoft Teams](across-working-with-teams.md#share-link).

## [Schede Business Central](#tab/tabs)

### <a name="who-can-view"></a>Chi può vedere il contenuto di una scheda?

Qualsiasi persona nella tua chat o canale che ha:

1. L'app Business Central per Teams installata.
2. Una licenza Business Central o accesso concesso a Business Central utilizzando la propria licenza Microsoft 365.
3. Autorizzazioni per visualizzare i dati sulla pagina.

### <a name=#recommended-content></a>Da dove provengono i contenuti consigliati?

Il contenuto consigliato tra cui puoi scegliere nell'opzione **Contenuto della scheda** in una scheda si basa sul tuo Centro di ruoli. Il contenuto consigliato include solo pagine di elenco, come Clienti, Ordini di vendita e Fornitori, non una pagina della singola scheda come un cliente o un fornitore specifico.

Nello specifico, i contenuti consigliati includono:

- Azioni nel menu di navigazione in alto nel centro ruoli
- Tutte le pagine dell'elenco che hai aggiunto ai preferiti.
- Se una pagina di elenco offre visualizzazioni diverse, comprese le visualizzazioni che hai creato, puoi anche scegliere tra quelle visualizzazioni

Puoi aggiungere pagine elenco al contenuto consigliato aggiungendo segnalibri. Puoi anche rimuovere i contenuti consigliati eliminando i segnalibri. Per informazioni su come aggiungere o eliminare segnalibri, vedi [Aggiungi una pagina o un report ai preferiti nel tuo centro ruoli](ui-bookmarks.md).

Se si cambia ambiente o azienda nell'opzione della scheda, il contenuto consigliato verrà modificato in base al Centro ruoli e ai segnalibri per l'ambiente e l'azienda a cui si passa.

### Quando creo una scheda, concede autorizzazioni alle persone nel canale o nella chat?

Nr. La creazione di schede non influisce sulle autorizzazioni e gli utenti devono già disporre dell'autorizzazione per tali dati quando accedono alla scheda.

### Posso chattare accanto a una scheda?

Sì. Usa l'icona della chat per iniziare la conversazione. Questo thread di chat viene quindi associato alla scheda. 

### Se rimuovo una scheda da una chat o da un canale, i dati di Business Central vengono eliminati?

Nr.

### Posso rinominare una scheda in sicurezza?

Sì. Il contenuto della scheda non è correlato al nome effettivo della scheda. Rinomina a piacimento! 

### Ho bisogno di operare su attività in diverse finestre. Posso farlo?

Sì. Puoi far uscire la scheda nella relativa finestra del browser per mostrare il client Web di Business Central. 

### Posso aggiungere una scheda nelle riunioni di Teams?

Nr. L'app Business Central per Teams non supporta le schede nelle riunioni.

### Non è possibile aggiungere una scheda se si utilizzano URL ISV come *.bc.dynamics.com (ma è possibile aggiungerle)

Non supportato.

### Quando eseguo operazioni nella scheda, come navigare, riordinare, applicare un filtro o eseguire ricerche, gli altri vedono le mie modifiche?

Nr. Solo le modifiche ai campi o le azioni in esecuzione influiscono sul modo in cui gli altri visualizzano il contenuto della scheda.

### Il contenuto della scheda si aggiorna automaticamente? In caso negativo, come posso aggiornarlo?

Il contenuto non si aggiorna automaticamente e al momento non esiste alcun pulsante di aggiornamento. Il modo migliore per aggiornare il contenuto per assicurarsi che rifletta i dati più recenti, lasciare la scheda e quindi tornare indietro. 

### Questo consente di visualizzaare elenchi e record dalle mie personalizzazioni e dei miei componenti aggiuntivi?

Sì. 

### Quando aggiungo una scheda, le persone la vedranno nella mia lingua?

Nr. Ciascun utente visualizza il contenuto della scheda nelle impostazioni di lingua, area geografica e fuso orario da Business Central. 

### Posso avere più schede che puntano a contenuti diversi?

Sì.

### Posso anche aggiungere schede per chattare con una sola persona?

Sì, a condizione che la chat non sia una bozza (ovvero, non sia stato inviato un messaggio per avviare quella chat) e che anche l'altra persona abbia installato l'app Business Central.

### Posso cambiare azienda all'interno di una scheda?

Nr. 

### È diverso dall'utilizzo della capacità generica di Teams di creare una scheda che ospita un sito Web?

Sì. Non consigliamo di utilizzare l'approccio. In molti casi, non funziona per Business Central.

## [Ricerca di contatti](#tab/contacts)

### In quali tabelle l'app esegue la ricerca?

Durante la ricerca dei contatti dall'app [!INCLUDE [prod_short.md](includes/prod_short.md)] per Teams, i termini di ricerca vengono confrontati con i record nella tabella **Contatti** in [!INCLUDE [prod_short.md](includes/prod_short.md)]. 

### In quali campi della tabella dei contatti posso eseguire la ricerca?

Mentre digiti i termini di ricerca nella casella di ricerca, i termini vengono confrontati con la maggior parte dei campi nella tabella **Contatti**. I campi includono, ad esempio, i campi **N.**, **Nome**, **Indirizzo**, **Nr. di telefono** oppure **Numero di telefono cellulare** e **E-mail**. 

I termini di ricerca non vengono abbinati a nessun campo personalizzato aggiunto alla tabella **Contatti** per app ed estensioni.

### I risultati della ricerca includono aziende e persone?

Sì. In [!INCLUDE [prod_short.md](includes/prod_short.md)], i contatti possono essere di tipo **Azienda** o digita **Persona**, dove una o più persone possono essere associate a un'azienda. Nei risultati della ricerca, le aziende e le persone hanno icone diverse.

### I contatti di una relazione d'affari compaiono nei risultati?

Sì. Alcuni contatti possono rappresentare clienti o fornitori o entrambi. Gli altri contatti senza una relazione d'affari definita in genere rappresentano i potenziali clienti. Contatti con altre relazioni d'affari, comprese le relazioni personalizzate che hai configurato in [!INCLUDE [prod_short.md](includes/prod_short.md)], verrà visualizzato anche nei risultati della ricerca.

### Posso cercare i dettagli di contatto durante le riunioni?

Sì. Puoi cercare le informazioni di contatto, la cronologia delle interazioni e i documenti correlati per il cliente o il fornitore durante una riunione o una chiamata di Teams nella riunione senza uscire da Teams.

In effetti, puoi cercare i dettagli di contatto da qualsiasi punto in Teams usando la casella di comando. Puoi, ad esempio, cercare i dettagli di contatto dal calendario di Teams per aiutarti a configurare le riunioni.

### Come posso visualizzare le mie ultime interazioni con un contatto?

La finestra dei dettagli di un contatto visualizza i movimenti del log delle interazioni. I movimenti del log delle interazioni forniscono la cronologia delle interazioni che l'organizzazione ha avuto con il contatto specifico. Le interazioni possono includere e-mail che hai scambiato, chiamate che hai ricevuto o documenti che hai inviato.

Per visualizzare le interazioni, [!INCLUDE [prod_short.md](includes/prod_short.md)] deve essere configurato per monitorare le interazioni. Per ulteriori informazioni sulla registrazione delle interazioni, vedi [Registra le interazioni con i contatti](marketing-interactions.md).

### Come si registra una chiamata o una riunione di Teams come interazione?

Nella finestra dei dettagli di un contatto, trova l'azione **Crea interazione** e sceglie tra le chiamate in entrata o in uscita come modelli di interazione. Puoi anche creare i tuoi modelli di interazione personalizzati specificamente per l'uso con le conversazioni di Teams.

### Posso chiamare un contatto dall'app [!INCLUDE [prod_short.md](includes/prod_short.md)] per Teams?

[!INCLUDE [prod_short.md](includes/prod_short.md)] ha un'integrazione limitata alle funzionalità di chiamata di Teams. Non è possibile avviare immediatamente una chiamata VOIP dalla scheda del contatto o dalla finestra dei dettagli del contatto. Tuttavia, quando si visualizzano i dettagli del contatto nell'app desktop Teams, puoi selezionare il campo del numero di telefono per comporre quel numero se Teams è configurato come app di composizione predefinita sul dispositivo. Per comporre numeri di telefono fisso o mobile tramite PSTN, il sistema telefonico tradizionale, Teams richiede l'app Microsoft 365 Business Voice. Per saperne di più, vedi [Cos'è Microsoft 365 Business Voice?](/MicrosoftTeams/business-voice/whats-business-voice)

### Come si visualizzano i documenti recenti per un cliente o un fornitore?

[!INCLUDE [prod_short.md](includes/prod_short.md)] in genere si riferisce a un contatto con un record cliente o fornitore che a sua volta è correlato ai record delle transazioni commerciali, come offerte di vendita o fatture di acquisto. Per visualizzare i documenti correlati per un contatto, vai alla finestra dei dettagli del contatto, scegli il valore del campo **Relazione d'affari** o utilizza le azioni per passare al cliente o fornitore associato. Nella pagina del cliente o del fornitore, espandi il riquadro FactBox per visualizzare le statistiche per vari documenti in cui è possibile eseguire il drill-down. La tua esperienza potrebbe differire in base alle tue personalizzazioni.

### Come cerco i contatti che usano caratteri speciali?

Puoi immettere criteri di ricerca utilizzando quasi tutti i caratteri Unicode. Tuttavia, [!INCLUDE [prod_short.md](includes/prod_short.md)] riserva i seguenti simboli per altri usi: **=**, **.**, **\***, e **@**. L'utilizzo di questi simboli nei termini di ricerca potrebbe non restituire i risultati previsti. Se non vedi i risultati attesi, racchiudi i simboli nei tuoi termini di ricerca tra virgolette singole, per esempio, **Contoso'='2**.

### Come posso cercare i contatti archiviati in un'altra azienda?

L'app [!INCLUDE [prod_short.md](includes/prod_short.md)] per Teams può cercare clienti, fornitori e altri contatti in una società alla volta.  
Per cercare i contatti archiviati in un altra azienda [!INCLUDE [prod_short.md](includes/prod_short.md)], apri [Impostazioni](across-teams-settings.md), quindi cambia l'ambiente e l'azienda da lì.

### I contatti [!INCLUDE [prod_short.md](includes/prod_short.md)] sono diversi da quelli nella schermata dei contatti di Teams?

Sì. I contatti archiviati in [!INCLUDE [prod_short.md](includes/prod_short.md)] rappresentano i contatti commerciali disponibili per la tua organizzazione. Sono contatti con i quali hai una relazione d'affari consolidata e ben definita, oppure contatti che rappresentano potenziali clienti. Questi contatti sono in genere contatti esterni. Al contrario, i contatti visualizzati nell'elenco dei contatti di chiamata di Teams sono i tuoi contatti. Questi contatti non sono necessariamente condivisi con altri nella tua organizzazione e in genere rappresentano i contatti interni alla tua organizzazione.

### [!INCLUDE [prod_short.md](includes/prod_short.md)] sincronizza i contatti con Teams?

No. I contatti archiviati in [!INCLUDE [prod_short.md](includes/prod_short.md)] rimangono separati dai contatti archiviati in Teams.
Al momento non ci sono piani per sincronizzare i due elenchi insieme.

### Qual è la versione minima di [!INCLUDE [prod_short.md](includes/prod_short.md)] per la ricerca di contatti?

La ricerca dei contatti richiede che tu abbia l'app [!INCLUDE [prod_short.md](includes/prod_short.md)] per Teams versione 1.0.4 o successiva installata e ti stai connettendo agli ambienti [!INCLUDE [prod_short.md](includes/prod_short.md)] della versione 18 o successiva.

### Posso eseguire ricerche dal mio dispositivo mobile?

In questo momento la ricerca dei contatti non è disponibile da Teams per iOS e Teams per Android.

### Di quali autorizzazioni ho bisogno per la ricerca dei contatti?

Per cercare contatti, è necessaria l'autorizzazione a livello di oggetto per la tabella **Contatti** all'interno dell'azienda [!INCLUDE [prod_short.md](includes/prod_short.md)] in cui si esegue la ricerca. Per visualizzare la finestra dei dettagli di un contatto, è necessaria almeno l'autorizzazione di lettura per la pagina **Contatti** all'interno dell'azienda [!INCLUDE [prod_short.md](includes/prod_short.md)] e qualsiasi altro oggetto correlato.

### Posso utilizzare la ricerca dei contatti se sono un amministratore delegato?

Sì. Puoi anche cercare contatti e dettagli dei contatti se disponi di un ruolo di amministratore delegato in un'organizzazione.

### La ricerca dei contatti è interessata dai limiti dell'API?

Sì. La ricerca di contatti da Teams si basa sull'API [!INCLUDE [prod_short.md](includes/prod_short.md)] v2.0 ed è soggetta a eventuali limiti API che gestiscono l'utilizzo. Puoi scoprire di più sui limiti nella sezione [Limiti API attuali](/dynamics-nav/api-reference/v2.0/dynamics-current-limits).

### Perché a volte mi chiede di configurare l'app?

Dopo aver effettuato l'accesso all'app [!INCLUDE [prod_short.md](includes/prod_short.md)] per Teams per la prima volta, l'app tenterà di determinare la tua azienda preferita in [!INCLUDE [prod_short.md](includes/prod_short.md)]. Se l'app non è in grado di determinare l'azienda, potresti dover andare a **Impostazioni** e scegliere l'azienda in cui desideri effettuare la ricerca. Questa situazione si verifica, ad esempio, se hai accesso a più società in tutti gli ambienti della tua organizzazione. In questo caso, dovrai scegliere un'azienda prima di poter iniziare la ricerca.  

L'app potrebbe anche richiedere di andare a **Impostazioni** se non si dispone di una sottoscrizione [!INCLUDE [prod_short.md](includes/prod_short.md)], non sono disponibili ambienti [!INCLUDE [prod_short.md](includes/prod_short.md)] o l'account non dispone di una licenza [!INCLUDE [prod_short.md](includes/prod_short.md)].

### Vorrei eseguire la ricerca di elementi o record da altre tabelle. Posso farlo da Teams?

La ricerca nelle altre tabelle non è possibile in questo momento. L'app [!INCLUDE [prod_short.md](includes/prod_short.md)] per Teams esegue solo la ricerca nell'elenco dei contatti [!INCLUDE [prod_short.md](includes/prod_short.md)], che può includere fornitori, clienti e altri contatti.

Se desideri vedere le funzionalità di ricerca evolversi per includere altre tabelle, incoraggiamo la nostra comunità ad aggiungere un'idea o votare per idee esistenti su https://aka.ms/BusinessCentralIdeas.

## [Lavorare con le carte](#tab/cards)

### Quali tipi di collegamento supporta l'app?

L'app [!INCLUDE [prod_short.md](includes/prod_short.md)] per Teams reagisce alla maggior parte dei collegamenti del client Web di [!INCLUDE [prod_short.md](includes/prod_short.md)]. Quando il collegamento fa riferimento a un singolo record in una pagina, la scheda visualizzerà i campi per quel record. I tipi di pagina supportati includono: 

- Pagine scheda, come la scheda Articolo
- Pagine documento, come il documento Ordine vendita
- Pagine ListPlus che rappresentano un singolo record composto da altri record, ad esempio Riconciliazione estratti conto
- Pagine elenco semplici in cui un record non offre la possibilità di eseguire il drill-down in una pagina di dettagli separata, come l'elenco dei codici postali

Quando si incolla un collegamento all'URL del client Web principale, ad esempio https://businesscentral.dynamics.com, la scheda visualizza invece informazioni per consentire ai nuovi utenti di accedere a [!INCLUDE [prod_short.md](includes/prod_short.md)].

### Come elimino una scheda che ho inviato a una chat?

Non puoi eliminare una scheda che hai già inviato alla chat. Puoi tuttavia eliminare l'intero messaggio di cui fa parte la scheda.

In qualità di autore del messaggio, puoi eliminare tutti i messaggi inviati alle chat con una persona, un gruppo o un canale, a meno che l'amministratore non abbia impostato criteri che impediscono l'eliminazione dei messaggi. Se moderi un canale come proprietario del canale, il tuo amministratore potrebbe anche averti concesso l'autorizzazione di eliminare tutti i messaggi nel canale, inclusi i messaggi inviati da altri utenti.

L'eliminazione di un messaggio che contiene una scheda non elimina né modifica i dati in [!INCLUDE [prod_short.md](includes/prod_short.md)].

### Le schede mostrano sempre informazioni aggiornate?

No. I valori dei campi in una scheda di Teams, incluse le immagini, sono basati sui dati disponibili al momento dell'invio della scheda alla chat. Le schede di [!INCLUDE [prod_short.md](includes/prod_short.md)] non vengono aggiornate automaticamente in Teams. 

### Perché le schede non mostrano più informazioni anziché solo il nome della pagina e il pulsante dei dettagli?

Un amministratore potrebbe aver configurato l'integrazione di Teams in modo che le schede non mostrino i dati sui record. Per ulteriori informazioni, vedi [Mostrare o nascondere i dati dei record sulle schede](admin-teams-integration.md#show-or-hide-record-data-on-cards).

### Gli altri utenti vedranno la mia scheda se non hanno l'app [!INCLUDE [prod_short.md](includes/prod_short.md)] per Teams? 

Quando scrivi e invii un messaggio in chat che include una scheda, tutti gli utenti vedranno la scheda&mdash;anche se non hanno installato l'app [!INCLUDE [prod_short.md](includes/prod_short.md)] per Teams.

### Come faccio a sapere a quale società appartiene una scheda in Teams?

Se si lavora per più aziende [!INCLUDE [prod_short.md](includes/prod_short.md)], chiedere all'amministratore di abilitare un badge per ogni società. Se abilitato, questo interessante suggerimento viene visualizzato in qualsiasi finestra dei dettagli all'interno di Teams e mostra la società e l'ambiente a cui appartiene il record. Per informazioni su come impostare il badge società, vedi [Visualizzare un badge società](admin-company-information.md#badge).

## [Lavorare con i dettagli della carta](#tab/carddetails)

### Dov'è il pulsante Salva nella finestra dei dettagli in Teams?

[!INCLUDE [prod_short.md](includes/prod_short.md)]salva automaticamente le modifiche apportate a qualsiasi campo non appena si esce dal campo. Per uscire da un campo, fai clic/tocca un punto qualsiasi al di fuori del campo o utilizza il tasto TAB per passare al campo successivo. Quando i dati sono visualizzati in una finestra di dialogo all'interno della finestra dei dettagli, è possibile che sia necessario scegliere il pulsante **OK** affinché [!INCLUDE [prod_short.md](includes/prod_short.md)] salvi le modifiche.

### Se scelgo di visualizzare i dettagli di una scheda, gli altri utenti vedranno la finestra dei dettagli?

No. Tutti gli utenti coinvolti nella chat o nella riunione possono visualizzare la scheda vera e propria, ma solo tu vedi la finestra dei dettagli quando selezioni **Dettagli**. Gli altri utenti devono a loro volta scegliere **Dettagli** se desiderano visualizzare la finestra dei dettagli sul loro dispositivo.

### Posso avviare una chiamata Teams dalla finestra dei dettagli in Teams?

Sì. Se stai usando l'app desktop Teams, avvia una chiamata selezionando il numero collegato in un campo con il numero di telefono, ad esempio **Numero di telefono cellulare** nella scheda **Contatto**. Teams deve essere l'app di composizione designata.

Per chiamare telefoni fissi e cellulari locali o internazionali, Teams richiede una licenza Business Voice per le chiamate aziendali. Inoltre, devi configurare Teams come soluzione per le chiamate. Per saperne di più, vedi [Pianificare la soluzione vocale di Teams](/microsoftteams/cloud-voice-landing-page) nella documentazione di Teams.

### Posso stampare documenti dalla finestra dei dettagli in Teams?

Sì. Puoi stampare report e altri documenti utilizzando la funzionalità di stampa di [!INCLUDE [prod_short.md](includes/prod_short.md)] standard e qualsiasi stampante abilitata per il cloud configurata in **Gestione stampante** in [!INCLUDE [prod_short.md](includes/prod_short.md)]. Non è possibile stampare da Teams su stampanti locali note al dispositivo client, ad esempio le stampanti su cui si stampa in genere dal browser. Per questo motivo, non è possibile stampare dalla finestra di anteprima del report, ma solo dalla pagina principale di richiesta del report, direttamente sulle stampanti cloud.

Per ulteriori informazioni sulla configurazione delle stampanti cloud, vedi [Imposta stampanti](ui-specify-printer-selection-reports.md).

### Posso accedere alla fotocamera dalla finestra dei dettagli in Teams?

Sì. Le funzionalità di [!INCLUDE [prod_short.md](includes/prod_short.md)] nella finestra dei dettagli che utilizzano la fotocamera sono disponibili in tutti i client di Teams.

### <a name="location"></a>Posso accedere alla mia posizione dalla finestra dei dettagli in Teams?

Se utilizzi la funzionalità in [!INCLUDE [prod_short.md](includes/prod_short.md)] che consente di accedere alle coordinate della posizione corrente, ad esempio con le mappe, devi utilizzare Teams nel browser o nell'app per dispositivi mobili Teams. La posizione non è disponibile quando si usa l'app desktop Teams.

### Come apro i dettagli in una nuova finestra?

L'apertura della finestra dei dettagli come finestra separata è utile per il multitasking o per poter lavorare con i dati aziendali pur continuando a usare la chat di Teams e altre funzioni di Teams. Per aprire i dettagli nella sua finestra, scegli **Apri nel browser** dal menu con i puntini di sospensione (**...**) nell'angolo in alto a destra della finestra.

## [Collaborare con gli ospiti](#tab/collaborating)

### Posso condividere le schede con utenti esterni all'organizzazione?

Sì. Quando componi e invii un messaggio che include una scheda, tutti i destinatari nella chat vedranno la scheda, anche se sono utenti guest o esterni alla tua organizzazione. Gli utenti guest possono anche aprire la finestra dei dettagli se dispongono delle autorizzazioni per accedere a quei dati in [!INCLUDE [prod_short.md](includes/prod_short.md)].

### L'esperienza è differenti per gli utenti ospiti?

Sì. Invitare utenti guest esterni alla tua organizzazione a partecipare a una chat o a un canale offre loro un'esperienza simile, ma non identica, rispetto agli utenti nell'organizzazione. Quando un utente guest riceve un messaggio che include una scheda, può visualizzarlo. Gli utenti guest possono anche aprire la pagina dei dettagli se dispongono delle autorizzazioni per accedere a quei dati in [!INCLUDE [prod_short.md](includes/prod_short.md)] e di una licenza [!INCLUDE [prod_short.md](includes/prod_short.md)] nell'organizzazione.

Scegliendo il collegamento ai dettagli su qualsiasi scheda Business Central accedi all'ambiente da cui è stata condivisa la scheda, presupponendo che disponi dell'autorizzazione per l'ambiente.

Gli utenti guest non sono autorizzati a usare la ricerca dei contatti perché è associata al tenant originale e attualmente non supportiamo uno scenario delegato di questo tipo.

Quando un utente guest compone un messaggio, i collegamenti al suo o al tuo [!INCLUDE [prod_short.md](includes/prod_short.md)] non si espanderanno in schede.

Per informazioni su altre similarità e differenze tra utenti guest e membri del team, vedi [Esperienza degli utenti guest in Teams](/MicrosoftTeams/guest-experience) nella documentazione di Teams.

### In che modo un utente guest installa l'app [!INCLUDE [prod_short.md](includes/prod_short.md)]? 

Gli utenti guest non hanno accesso al marketplace delle app per installare personalmente le app. Tuttavia, l'app può essere installata automaticamente per tali utenti in base ai criteri della tua organizzazione. Un altro modo per un utente guest di installare l'app [!INCLUDE [prod_short.md](includes/prod_short.md)] è quando riceve un messaggio di chat che include una scheda [!INCLUDE [prod_short.md](includes/prod_short.md)]. In questo caso, l'utente sceglie il pulsante **Dettagli** o il menu nella scheda, quindi installa l'app [!INCLUDE [prod_short.md](includes/prod_short.md)] da utilizzare con l'organizzazione. Dopo aver installato l'app, un utente non riceve automaticamente alcuna autorizzazione per accedere ai dati da [!INCLUDE [prod_short.md](includes/prod_short.md)].

## [Condividi su Teams](#tab/share)

### Condividi in Teams invia una scheda compatta? 

Sì. Il collegamento si espande automaticamente in una scheda se hai installato l'app Business Central per Teams. 

### I destinatari riceveranno il messaggio da me o da un account del servizio Business Central? 

Quando usi Condividi in Teams, il messaggio viene inviato a una persona, un gruppo o un canale, come se tu stesso avessi inviato il messaggio da Microsoft Teams. I destinatari vedono il tuo messaggio sul loro client Teams preferito, e possono reagire e rispondere come farebbero normalmente a un tuo messaggio. 

### Condividi in Teams è disponibile in Business Central on premises? 

No. Analogamente all'app [!INCLUDE [prod_short.md](includes/prod_short.md)] per Teams, questa funzione è disponibile solo per il client web in [!INCLUDE [prod_short.md](includes/prod_short.md)] online. Non ci sono piani per supportare i tipi di distribuzione di [!INCLUDE [prod_short.md](includes/prod_short.md)], come locale, cloud ibrido o cloud privato, che Microsoft non ospita o gestisce direttamente.

### Condividi in Teams concede i permessi ai destinatari? 

No. Quando si condivide con una persona, un gruppo o un canale, le autorizzazioni non vengono modificate. Gli utenti che hanno già il permesso di visualizzare la pagina e i dati a cui mira il link possono farlo. Gli utenti che non hanno il permesso di visualizzare quella pagina e quei dati, o che non hanno una licenza [!INCLUDE [prod_short.md](includes/prod_short.md)], ricevono un messaggio di errore. 
 
### Devo avere l'applicazione desktop Teams installata per usare Condividi in Teams? 

No. Tutto ciò di cui avete bisogno è un account valido che abbia accesso a Microsoft Teams. 

### Condividi in Teams è disponibile in tutti i clienti di Business Central? 

Al momento, Condividi in Teams è disponibile nel client Web desktop, nella finestra dei dettagli in Teams e quando si apre una pagina in una nuova finestra dal componente aggiuntivo per Outlook.

### Dove trovo Condividi in Teams in Business Central? 

L’**azione Condividi in Teams** si trova nel menu **Condividi** su tutte le pagine, come le pagine delle schede e dei documenti, le pagine delle liste o dei fogli di lavoro, comprese le pagine personalizzate. L'azione non è disponibile nelle finestre di dialogo o nelle pagine mostrate come finestre di dialogo, come le pagine di ricerca o le procedure guidate.

---
## Vedere anche

[[!INCLUDE [prod_short](includes/prod_short.md)] e Panoramica sull’integrazione di Microsoft Teams](across-teams-overview.md)  
[Installare l'App [!INCLUDE [prod_short](includes/prod_short.md)] per Microsoft Teams](across-install-app-for-teams.md)  
[Ricerca di clienti, fornitori e altri contatti da Microsoft Teams](across-search-contacts-teams.md)  
[Condividere i record in Microsoft Teams](across-working-with-teams.md)  
[Risoluzione dei problemi relativi a Teams](admin-teams-troubleshooting.md)  
[Modifica della società e di altre impostazioni in Teams](across-teams-settings.md)  
[Sviluppo per l'integrazione di Teams](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
