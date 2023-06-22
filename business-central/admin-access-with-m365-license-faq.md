---
title: Domande frequenti sull'accesso con licenze Microsoft 365
description: Ottieni risposte a domande comuni sull'accesso a Business Central con licenze Microsoft 365.
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: faq
ms.date: 11/22/2022
ms.custom: bap-template
---
# <a name="access-with-microsoft--licenses-faq" />Domande frequenti sull'accesso con licenze Microsoft 365

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

Gli utenti possono accedere ai dati di Business Central in Microsoft Teams utilizzando la licenza Microsoft 365. Questo articolo risponde alle domande frequenti di amministratori, consulenti e altri. Gli sviluppatori devono fare riferimento alle Domande frequenti per gli sviluppatori. Per domande sull'integrazione di Business Central con Microsoft Teams, vai a [Domande frequenti su Teams](teams-faq.md).

## [Autorizzazioni](#tab/permissions) 

### <a name="can-i-proactively-configure-different-starting-permissions-for-different-groups-of-users" />Posso configurare in modo proattivo diverse autorizzazioni di avvio per diversi gruppi di utenti?

No, non attualmente. Business Central consente di configurare solo un gruppo di autorizzazioni che vengono assegnate a tutti gli utenti Microsoft 365 quando accedono a Business Central per la prima volta.

### <a name="can-i-proactively-configure-permissions-profiles-and-settings-for-individual-users-before-they-sign-in" />Posso configurare in modo proattivo autorizzazioni, profili e impostazioni per i singoli utenti prima che accedano?

Sì. Può essere raggiunto attraverso gruppi di sicurezza. Applicando un gruppo di sicurezza a un ambiente, definisci l'insieme totale di utenti che hanno accesso a quell'ambiente. Questo gruppo di sicurezza può includere utenti con una licenza Business Central e utenti con una licenza Microsoft 365. La prossima volta che aggiornerai gli utenti da Microsoft 365 nell'elenco **Utenti** , verranno creati i record utente Microsoft 365 . Puoi quindi assegnare gruppi di utenti, autorizzazioni, profili e altre impostazioni prima che abbiano effettuato l'accesso.

### <a name="after-a-user-signs-in-can-i-change-which-objects-they-have-access-to" />Dopo che un utente ha effettuato l'accesso, posso modificare gli oggetti a cui ha accesso?

Sì. Dopo che un utente ha effettuato l'accesso per la prima volta ed è stato eseguito il provisioning del relativo record utente, gli amministratori gestiscono tali utenti proprio come qualsiasi altro utente di Business Central. Ad esempio, possono aggiungere o rimuovere autorizzazioni a diversi oggetti. Se modifichi i set di autorizzazioni assegnati alla licenza Microsoft 365 nella pagina Configurazione licenza, la modifica avrà effetto solo sui prossimi utenti che accedono per la prima volta.

### <a name="how-do-i-prevent-access-to-sensitive-tables" />Come posso impedire l'accesso a tabelle sensibili?

Business Central offre un modello di autorizzazioni potenti e flessibili in cui gli amministratori possono definire insiemi di autorizzazioni che concedono l'accesso a oggetti specifici, processi aziendali o interi ruoli. Per impedire l'accesso alle tabelle sensibili, è possibile creare set di autorizzazioni personalizzati che escludono l'autorizzazione per gli oggetti sensibili. Per ulteriori informazioni sull'esclusione delle autorizzazioni, vedi [Crea set di autorizzazioni](ui-define-granular-permissions.md).  

### <a name="instead-of-customizing-the-license-configuration-can-i-customize-a-user-group" />Invece di personalizzare la configurazione della licenza, posso personalizzare un gruppo di utenti?

Sì. L'aggiunta di set di autorizzazioni al gruppo di utenti interni di Microsoft Teams in Business Central ha lo stesso effetto netto dell'aggiunta di set di autorizzazioni alla licenza Microsoft 365, a condizione che la licenza Microsoft 365 continui ad essere associata a questo gruppo di utenti. Questo approccio ha l'ulteriore vantaggio che i set di autorizzazioni vengono sempre sincronizzati con i membri del gruppo ogni volta che si modifica il gruppo di utenti.

### <a name="when-a-business-central-user-shares-a-record-in-teams-do-they-grant-new-permissions" />Quando un utente di Business Central condivide un record in Teams, concede nuove autorizzazioni?

Nr. Questa azione non equivale a condividere un collegamento a un documento di SharePoint in cui la persona che condivide il documento può scegliere di concedere l'autorizzazione ad altri. In Business Central solo gli amministratori possono configurare e assegnare le autorizzazioni. Confrontato con la condivisione di documenti SharePoint equivale a scegliere l'opzione "Condividi con persone con accesso esistente".

### <a name="does-this-feature-support-row-level-security" />Questa funzione supporta la sicurezza a livello di riga?

Sì. Anche se una persona che accede a un record in Teams con la propria licenza Microsoft 365 può disporre delle autorizzazioni corrette per la tabella e l'oggetto della pagina, le autorizzazioni a livello di riga verranno applicate se sono state implementate per quella tabella.  

### <a name="if-i-configure-permissions-that-include-write-access-will-users-be-able-to-write-in-teams" />Se configuro autorizzazioni che includono l'accesso in scrittura, gli utenti potranno scrivere in Teams?

Se configuri Business Central affinché assegni un set di autorizzazioni che include l'inserimento, la modifica o l'eliminazione dell'accesso a uno o più oggetti, gli utenti con quel set di autorizzazioni non saranno comunque in grado di scrivere in Teams quando hanno solo una licenza Microsoft 365. Il servizio Business Central applica l'accesso in sola lettura indipendentemente dall'autorizzazione di inserimento, modifica o eliminazione assegnata.  

Anche se Business Central fornisce questo livello di protezione, ti consigliamo comunque di evitare i set di autorizzazioni con accesso in scrittura. In questo modo si evitano problemi a valle quando gli utenti cambiano ruolo o acquisiscono nuove licenze.  

## [Configurazione e impostazione](#tab/setup)

### <a name="why-is-the-setting-to-enable-access-not-available-for-my-environment" />Perché l'impostazione per abilitare l'accesso non è disponibile per il mio ambiente?

L'abilitazione dell'accesso con licenze Microsoft 365 è disponibile solo per gli ambienti Business Central della versione della piattaforma 21.1 o successiva. Quando l'ambiente viene aggiornato a questa versione minima, l'impostazione diventa automaticamente disponibile. Per controllare la versione del tuo ambiente, vai alla pagina dei dettagli dell'ambiente per l'ambiente nell'interfaccia di amministrazione di Business Central. In alternativa, accedi all'ambiente e vai alla pagina **Guida e supporto** dal menu **Guida**.

### <a name="can-i-access-business-central-on-premises-with-microsoft--licenses" />Posso accedere a Business Central in locale con le licenze Microsoft 365?

No, non è supportato. Business Central visualizza un errore quando gli utenti tentano di accedere ai record locali di Business Central in Teams.

### <a name="what-is-the-employee-profile" />Cos'è il profilo del dipendente?

Il profilo **Dipendente** visualizzato nella pagina di elenco **Profili (ruoli)** è stato introdotto con l'aggiornamento 21.1. È il profilo predefinito assegnato agli utenti che accedono a Business Central con la propria licenza Microsoft 365. Questo profilo è destinato agli utenti di un'organizzazione che non hanno un ruolo specifico in Business Central e hanno solo bisogno di visualizzare i dati che sono stati condivisi con loro.

### <a name="what-is-the-teams-users-user-group" />Che cos'è il gruppo di utenti Utenti di Teams?

Il gruppo **Utenti interni di Microsoft Teams** visualizzato nella pagina **Gruppi utenti** è stato introdotto con l'aggiornamento 21.1. Questo gruppo è il gruppo utente predefinito assegnato agli utenti che accedono a Business Central con la propria licenza Microsoft 365. Il gruppo utenti è destinato alle persone all'interno della stessa organizzazione in cui è ospitato Business Central che collaborano in Microsoft Teams.  

### <a name="do-users-that-only-have-a-microsoft--license-show-up-in-the-users-list-in-business-central" />Gli utenti che dispongono di una sola licenza Microsoft 365 vengono visualizzati nell'elenco Utenti in Business Central?

Sì. Se applichi i gruppi di sicurezza agli ambienti, tali utenti verranno visualizzati nell'elenco Utenti dopo aver utilizzato l'azione Aggiorna utenti da Microsoft 365 dall'elenco **Utenti**. Se non si applicano i gruppi di sicurezza, i record utente vengono visualizzati nell'elenco Utenti dopo il primo accesso a un record di Business Central.

### <a name="does-this-feature-work-for-embed-isv-solutions" />Questa caratteristica funziona per le soluzioni ISV integrate?

Sì. Gli utenti con una sola licenza Microsoft 365 possono anche accedere ai record in ambienti eseguiti sotto il dominio *.bc.dynamics.com.

## [Licenze](#tab/license)

### <a name="can-a-customer-use-this-feature-if-they-dont-have-business-central" />Un cliente può usare questa funzione se non dispone di Business Central?

L'accesso a Business Central con una licenza Microsoft 365 è destinato alle organizzazioni che sono già abbonate a Business Central e gestiscono uno o più ambienti Business Central con utenti Business Central con licenza. Non fornisce nuove funzionalità o diritti di utilizzo ai clienti Microsoft 365 che non dispongono di un piano Business Central.

### <a name="how-does-this-help-me-manage-subscription-costs-in-my-organization" />In che modo questo mi aiuta a gestire i costi di abbonamento nella mia organizzazione?

Per massimizzare la produttività e semplificare le operazioni, le PMI spesso acquistano Dynamics 365 Business Central insieme a Microsoft 365. In tal caso, la maggior parte degli utenti riceve una licenza Microsoft 365, ma solo ruoli o persone specifici ricevono una licenza Business Central. Business Central offre flessibilità nelle licenze in modo che i clienti paghino solo ciò di cui hanno bisogno:

- Agli utenti che richiedono l'accesso completo a Business Central viene in genere assegnata una licenza Business Central Essentials o Business Central Premium. 
- Agli utenti che richiedono un accesso in scrittura limitato viene in genere assegnata una licenza Membro del team di Business Central.
- Tutti gli altri dipendenti dell'organizzazione che hanno bisogno solo occasionalmente di leggere i dati aziendali condivisi con loro, possono farlo se dispongono di una licenza Microsoft 365. Non è necessario assegnare loro una licenza Membro del team. Sono disponibili altre opzioni di licenza. Per ulteriori informazioni, scarica e leggi la [Guida alle licenze di Dynamics 365](https://go.microsoft.com/fwlink/?LinkId=866544).

### <a name="is-this--free-of-charge" />È gratuito al 100%?
 
Nr. L'accesso ai dati di Business Central in Microsoft Teams richiede che ciascun utente disponga di una licenza Business Central o di una licenza Microsoft 365 dall'elenco dei piani supportati.

### <a name="does-this-work-with-microsoft--trials-and-business-central-trials" />Funziona con le versioni di valutazione Microsoft 365 e le versioni di valutazione di Business Central?

Sì. Se a un utente viene assegnata una licenza Microsoft 365 da una versione di valutazione di un piano supportato, può anche accedere ai record di Business Central in Teams. È quindi possibile per i clienti provare le app di produttività e aziendali di Microsoft che funzionano insieme e consente ai venditori e ai consulenti dei partner di dimostrare facilmente questa funzionalità. Ad esempio, i partner possono eseguire il provisioning dei propri tenant di Azure AD da [https://aka.ms/CDX](https://aka.ms/CDX) che includono versioni di valutazione di Microsoft 365 e versioni di valutazione di Business Central per la dimostrazione di Business Central.

### <a name="the-list-of-licenses-in-business-central-shows-a-microsoft--license-whats-that" />L'elenco delle licenze in Business Central mostra una licenza Microsoft 365. Guida rapida

La pagina **Configurazione licenza** in Business Central visualizza i diversi tipi di licenze che possono fornire l'accesso al servizio Business Central. Nella versione 21, Microsoft ha aggiunto Microsoft 365 a questo elenco come nuovo modo per accedere a Business Central. Questo elenco di licenze non implica che la tua organizzazione abbia acquistato abbonamenti a nessuna di queste licenze o che la tua organizzazione abbia abilitato l'accesso tramite tali licenze.

### <a name="do-i-need-to-acquire-a-new-type-of-microsoft--license-for-this-feature-to-work" />Devo acquisire un nuovo tipo di licenza Microsoft 365 affinché funzioni?

Microsoft non ha creato nuove licenze o nuovi piani per potenziare questa funzionalità. Questa funzionalità si basa interamente su piani e licenze Microsoft 365 esistenti. Se sei già abbonato a uno dei piani Microsoft 365 supportati, disponi già di questo nuovo diritto di utilizzo. Altrimenti, se non ti abboni a Microsoft 365 oggi, puoi iscriverti a Microsoft 365 Business Premium o piani simili qui. 

### <a name="how-do-i-find-out-which-users-have-only-a-microsoft--license" />Come faccio a sapere quali utenti hanno una sola licenza Microsoft 365?

Ci sono diversi modi. Nell'interfaccia di amministrazione di Microsoft 365, vai all'elenco **Utenti attivi**  e fai riferimento alla colonna **Licenze**. In Business Central, vai all'elenco **Utenti** , scegli uno qualsiasi degli utenti e visualizza il riquadro Dettaglio informazioni **Licenze**.  

### <a name="how-do-i-filter-the-users-list-in-business-central-to-see-users-that-only-have-a-microsoft--license" />Come filtro l'elenco Utenti in Business Central per visualizzare gli utenti che dispongono di una sola licenza Microsoft 365.

Questa attività non è attualmente possibile utilizzando un filtro o una visualizzazione elenco. Tuttavia, puoi selezionare un utente nell'elenco e visualizzare il riquadro Dettaglio informazioni Licenze che includerà solo Microsoft 365, se l'utente dispone di una sola licenza Microsoft 365.

### <a name="what-about-users-that-have-both-a-microsoft--license-and-a-business-central-license" />E per gli utenti che hanno sia una licenza Microsoft 365 che una licenza Business Central?

Quando a un utente vengono assegnate più licenze, i maggiori diritti di utilizzo della licenza prevalgono sui diritti di utilizzo della licenza minori quando si accede a Business Central. In questo caso, la licenza Business Central conferisce all'utente più diritti utente. Pertanto, gli utenti possono leggere e scrivere i record di Business Central in Teams e accedere al client Web di Business Central nel browser, proprio come qualsiasi altro titolare di licenza di Business Central. Se sono stati configurati insiemi di autorizzazioni specifici per la licenza Microsoft 365, l'utente ottiene gli insiemi di autorizzazioni configurati combinati con gli insiemi di autorizzazioni dalla licenza Business Central o che sono già stati assegnati all'utente.

### <a name="is-this-licensing-related-to-the-business-central-team-member-license" />Questa licenza è correlata alla licenza Membro del team di Business Central?

Non esiste alcuna relazione tra le licenze di Membro del team di Business Central e l'accesso a Business Central in Microsoft Teams utilizzando licenze Microsoft 365. Sebbene Microsoft Teams e la sua documentazione facciano riferimento alle persone in un team come *membri del team*, è un termine collettivo per un gruppo di utenti di Microsoft Teams. Non si riferisce alle licenze di Business Central.

### <a name="does-business-central-enforce-any-of-the-constraints" />Business Central impone un vincolo?

Sì, tutti i vincoli della piattaforma e i requisiti minimi, inclusi i requisiti di licenza, vengono applicati dalla piattaforma Business Central. Questo guida gli utenti con messaggi di errore specifici per aiutarli a risolvere i problemi di configurazione e prevenire gli abusi. Ad esempio, se un utente che dispone di una sola licenza Microsoft 365 tenta di accedere al client Web di Business Central nel browser, l'accesso verrà negato e verrà visualizzato un messaggio di errore di guida. 

## [Utilizzo](#tab/usage)
 
### <a name="can-i-access-records-on-teams-for-ios-and-teams-for-android" />Posso accedere ai record in Teams per iOS e Teams per Android?

Al momento, non è possibile accedere ai dati di Business Central su Teams per dispositivi mobili utilizzando una sola licenza Microsoft 365. Microsoft sta lavorando per abilitare questa funzionalità a breve. 

### <a name="how-do-users-change-their-personal-settings-in-my-settings" />In che modo gli utenti modificano le proprie impostazioni personali in Impostazioni personali?

Quando un utente accede a Business Central per la prima volta utilizzando solo la propria licenza Microsoft 365, le sue impostazioni utente quali lingua, fuso orario e impostazioni internazionali vengono impostate automaticamente in base al sistema operativo o alle impostazioni del browser. Gli amministratori possono modificare queste impostazioni da Business Central per ogni utente. 

### <a name="what-determines-the-choice-of-language-when-you-sign-in-for-the-first-time" />Cosa determina la scelta della lingua al primo accesso?

La lingua con cui navighi in Business Central viene impostata in base a vari fattori, incluso il client Teams attraverso il quale hai effettuato l'accesso a Business Central per la prima volta. Per l'app desktop Teams, Teams per iOS e Teams per Android, viene applicata la lingua del sistema operativo. Per Teams per il Web, viene applicata la lingua del browser. In tutti i casi, la lingua di Teams non viene considerata. 

### <a name="why-cant-i-activate-some-of-the-colored-links-in-tabs-and-card-details" />Perché non riesco ad attivare alcuni dei collegamenti colorati nelle schede e nei dettagli della scheda?

I collegamenti attivabili nelle pagine di Business Central vengono spesso visualizzati come collegamenti ipertestuali in grassetto che possono essere attivati per navigare altrove o eseguire un'operazione. A livello tecnico, questi collegamenti sono tipicamente implementati come valori di campo senza didascalia che attivano del codice e dove la scelta dello stile spesso riflette lo stato. Quando gli utenti accedono alle pagine di Business Central con la loro licenza Microsoft 365, i collegamenti vengono definiti come se fossero utilizzabili. Ma non possono essere attivati perché questa licenza non offre diritti di utilizzo per eseguire azioni.  

### <a name="why-cant-i-activate-page-notification-actions" />Perché non riesco ad attivare le azioni di notifica della pagina?

Le notifiche contestuali mostrate sulle pagine sono spesso accompagnate da collegamenti utilizzabili. Quando gli utenti accedono alle pagine di Business Central con la loro licenza Microsoft 365, questi collegamenti vengono visualizzati, ma non possono essere attivati perché questa licenza non offre diritti di utilizzo per eseguire azioni. A livello tecnico, questi collegamenti sono implementati come azioni.

### <a name="can-microsoft--users-remove-tabs" />Gli utenti Microsoft 365 possono rimuovere le schede?

Sì. Chiunque nella chat o nel canale può rimuovere le schede create da altri. La rimozione di una scheda non rimuove né influisce sui dati in Business Central, ma la scheda verrà rimossa per tutti gli utenti nella chat o nel canale.

### <a name="if-i-cant-filter-will-i-still-see-a-filtered-list-that-was-created-by-others" />Se non riesco a filtrare, vedrò comunque un elenco filtrato creato da altri?

Gli utenti che accedono a Business Central con la propria licenza Microsoft 365 non dispongono dei diritti di utilizzo per filtrare utilizzando il riquadro dei filtri o applicare le visualizzazioni elenco. Tuttavia, se un altro utente ha creato una scheda contenente una pagina di elenco filtrata, gli utenti Microsoft 365 visualizzeranno anche i filtri applicati alla scheda.

---

## <a name="see-also" />Vedere anche

[Panoramica dell'accesso a Business Central con licenze Microsoft 365](admin-access-with-m365-license.md#minimum-requirements)  
[Configurare l'accesso con licenze Microsoft 365](admin-access-with-m365-license-setup.md)  
