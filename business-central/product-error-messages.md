---
title: Avvisi e messaggi di errore
description: Informazioni su come risolvere i problemi e trovare soluzioni ai messaggi di errore quando si utilizza Business Central.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.date: 03/08/2024
ms.service: dynamics-365-business-central
ms.custom: bap-temeplate
---
# Avvisi e messaggi di errore

Durante la giornata lavorativa, è possibile che vengano visualizzate notifiche in [!INCLUDE [prod_short](includes/prod_short.md)] indicanti che qualcosa non ha funzionato o che non è stato possibile pubblicare qualcosa, ad esempio. In molti casi, la notifica semplifica la risoluzione del problema o il rollback delle modifiche apportate. In altri casi, è possibile che le informazioni necessarie non siano sufficienti per sbloccare la situazione. Questo articolo fornisce suggerimenti su come risolvere il problema.  

## Assistenza utente nel prodotto

La versione predefinita di [!INCLUDE [prod_short](includes/prod_short.md)] include descrizioni per la maggior parte dei campi, delle colonne e delle azioni a cui è possibile accedere scegliendone il nome. In combinazione con suggerimenti didatti per le pagine importanti, didascalie descrittive e testo didattico, questi suggerimenti, o callout, sono l'attuale implementazione di *assistenza utente incorporata*, che è un principio importante nel mondo attuale della progettazione del software.  

Per informazioni su un campo o un altro elemento dell'interfaccia utente, scegliere il nome e apparirà una breve descrizione. Scegliere il collegamento **Chiedi a Copilot** se ciò non è sufficiente. Puoi anche utilizzare il riquadro della Guida del prodotto per trovare le risposte alle tue domande.  

Per ulteriori informazioni, vedere [Modello di assistenza per gli utenti Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/user-assistance) nel contenuto di amministrazione per [!INCLUDE [prod_short](includes/prod_short.md)].  

## Pagina Guida e supporto

In [!INCLUDE[prod_short](includes/prod_short.md)], la voce di menu ? (nell'angolo superiore destro) fornisce accesso alla pagina **Guida e supporto**, che include collegamenti alle risorse che consentono di trovare risposte alle domande. Per ulteriori informazioni, vedere [Risorse per Guida e supporto](product-help-and-support.md).  

## Aiutare gli altri

Se si è amministratore o superutente, è possibile aiutare gli altri cercando i messaggi di errore nella pagina **Registro messaggi di errore** o nell'interfaccia di amministrazione. In molti casi, il messaggio di avviso o di errore riguarda l'installazione o la mancanza di autorizzazione e problemi simili che il superutente o l'amministratore possono facilmente risolvere. In altri casi, potrebbe essere necessario ispezionare le pagine per identificare la causa. Per ulteriori informazioni, vedere [Ricerca di informazioni tecniche](/dynamics365/business-central/dev-itpro/administration/manage-technical-support#finding-technical-information) nel contenuto amministrativo per [!INCLUDE [prod_short](includes/prod_short.md)].  

## Condividere i dettagli dell'errore per un'assistenza più rapida

Per superare gli ostacoli e ridurre al minimo i tempi di inattività, sfrutta l'esperienza di colleghi o esperti in materia. Quando sei bloccato da un errore, puoi condividere facilmente i dettagli relativi all'errore quando ricevi assistenza.

I dettagli includono il messaggio di errore, il codice di errore e altre informazioni utili per la risoluzione di un errore. Condividendo i dettagli dell'errore, puoi comunicare in modo efficace il problema specifico che stai affrontando, consentendo ai tuoi colleghi di aiutarti.  

Puoi copiare i dettagli scegliendo l**Icona Condividi** nelle finestre di dialogo di convalida in linea o nel menu **Condividi dettagli** nelle finestre di dialogo degli errori.  

Oltre a copiare i dettagli dell'errore, puoi anche scegliere di condividere i dettagli tramite Microsoft Teams scegliendo **Condividi dettagli in Teams** per eseguire le seguenti operazioni:

* Copiare i dettagli dell'errore.
* Aprire la finestra **Condividi in Teams**, dove puoi incollare i dettagli dell'errore che hai copiato e indicare le persone a cui vuoi chiedere aiuto. [!INCLUDE [prod_short](includes/prod_short.md)] aggiunge un collegamento alla pagina in cui si è verificato l'errore per semplificare la risoluzione dei problemi.

Puoi anche scegliere di condividere i dettagli via e-mail scegliendo **Condividi dettagli via e-mail** per effettuare le seguenti operazioni:

* Copiare i dettagli dell'errore.
* Aprire l'editor di posta elettronica, dove puoi incollare i dettagli dell'errore che hai copiato e indicare le persone a cui vuoi chiedere aiuto. [!INCLUDE [prod_short](includes/prod_short.md)] aggiunge un collegamento alla pagina in cui si è verificato l'errore.

## Auto-assistenza

I messaggi di errore forniscono informazioni e azioni che semplificano la comprensione, l'accesso e la risoluzione degli errori provenienti dalla piattaforma.

I messaggi di errore che la piattaforma [!INCLUDE [prod_short](includes/prod_short.md)] genera contengono tutti i dettagli tecnici, inclusi i nomi dei campi, nella sezione **Messaggio di errore dettagliato**. Seleziona l'icona **Copia dettagli** negli errori di convalida in linea o in un messaggio di errore per accedere alle informazioni tecniche.

Le azioni nei messaggi di errore ti portano direttamente alla pagina in cui un campo causa l'errore. Non devi sprecare tempo per trovare personalmente la pagina o il campo. Per risolvere l'errore, scegli semplicemente scegliere l'azione nel messaggio di errore e [!INCLUDE [prod_short](includes/prod_short.md)] accederà all'area appropriata.

Il video seguente mostra come utilizzare i messaggi di errore utilizzabili per ottenere lo sblocco.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RW1l2sM]

### Suggerimento per sviluppatori

Se sei uno sviluppatore, quando chiami il metodo [TestField](/dynamics365/business-central/dev-itpro/developer/methods-auto/record/record-testfield-joker-joker-errorinfo-method) e non passi l'oggetto |`ErrorInfo`, [!INCLUDE [prod_short](includes/prod_short.md)] genera automaticamente il collegamento a un pagina in cui un utente può correggere il problema. [!INCLUDE [prod_short](includes/prod_short.md)] dapprima ottiene la pagina di ricerca o di drill-down per il record, quindi trova la pagina scheda o di ricerca e aggiunge un collegamento di navigazione a quella pagina scheda. [!INCLUDE [prod_short](includes/prod_short.md)] non aggiunge un collegamento nelle seguenti situazioni:

* Se l'errore si trova nella pagina attualmente aperta.
* Se l'utente non dispone dell'autorizzazione per modificare il record sottostante.

## Vedi anche

[Risorse per guida e supporto](product-help-and-support.md)  
[Domande frequenti](across-faq.yml)  
[Domande frequenti relative alla funzionalità delle informazioni](ui-search-faq.md)  
[Domande frequenti su ricerca e filtro](ui-search-filter-faq.yml)  
[Domande frequenti sulla funzionalità di copia e incolla](faq-copy-paste.yml)  
[Modificare le impostazioni di base](ui-change-basic-settings.md)  
[Preparazione al business](ui-get-ready-business.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]