---
title: Domande frequenti su Chat con Copilot
description: Questo articolo fornisce le risposte ad alcune domande comuni su Chat con Copilot in Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: conceptual
ms.collection:
  - bap-ai-copilot
ms.date: 05/17/2024
ms.custom: bap-template jswymer
---
# Domande frequenti su Chat con Copilot

[!INCLUDE[preview-banner](includes/preview-banner.md)]

Questo articolo fornisce le risposte ad alcune domande comuni sulla chat con Copilot in [!INCLUDE[prod_short](includes/prod_short.md)]. Per domande relative all'intelligenza artificiale e alla chat, consulta [Domande frequenti sull'intelligenza artificiale responsabile per Chat con Copilot](faqs-chat-with-copilot.md).

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

## Gli amministratori possono concedere o negare l'autorizzazione a singoli utenti per accedere alla chat?

No, non esiste alcuna autorizzazione o set di autorizzazioni per la chat. Se la chat è attivata nella pagina [Funzionalità di Copilot e IA](enable-ai.md), ogni utente in un ambiente ha accesso alla chat.
 
## La chat è disponibile su tablet, telefono o altri fattori di forma?

No, il riquadro della chat è disponibile solo nel client Web [!INCLUDE[web_client](includes/web_client.md)].

## Non utilizzo Business Central in inglese. Quali sono le opzioni disponibili?

Al momento la chat è disponibile solo in inglese. Puoi impostare l'inglese come lingua utente in [Impostazioni personali](ui-change-basic-settings.md#language).

## Quale versione di Business Central è necessaria per provare la chat?

La chat è disponibile in anteprima pubblica dalla versione 24.0 (ciclo di rilascio 1 del 2024).

## La chat funziona con le mie personalizzazioni?

Dipende dal tipo di domanda che poni a Copilot. Ad esempio:

- Quando poni domande per individuare record, Copilot è in grado di trovare i record nelle tabelle personalizzate identificate utilizzando campi personalizzati.
- Quando chiedi spiegazioni o indicazioni, Copilot non ha accesso ad alcuna informazione sulle tue personalizzazioni o documentazione per i tuoi componenti aggiuntivi.

## Sembra che Copilot non apra mai il record o la pagina che ho richiesto. Che cosa sto facendo di sbagliato?

Quando chiedi a Copilot di trovare record in [!INCLUDE[prod_short](includes/prod_short.md)], visualizza tutti i record trovati come riquadri o collegamenti selezionabili nel riquadro della chat. Durante l'anteprima, Copilot non passa automaticamente ad alcuna pagina.

## Le risposte che ricevo da Copilot variano anche se faccio la stessa domanda. È un errore?

Copilot potrebbe occasionalmente rispondere in modi diversi. Le risposte non sono necessariamente identiche.

## Quando dovrei utilizzare la funzione Copia nei messaggi di chat?

Puoi utilizzare il pulsante Copia per copiare un messaggio precedente nella conversazione con Copilot, incollarlo nella casella di input per provare o riprovare una variante del tuo messaggio a Copilot.

## Come posso personalizzare o estendere la chat?

Durante l'anteprima, il riquadro della chat e le risposte di Copilot non possono essere modificati in alcun modo tramite personalizzazione, componenti aggiuntivi o individualizzazione.

## Copilot trova dati in altre aziende o ambienti?

Copilot cerca solo i record dell'azienda a cui hai effettuato l'accesso&mdash; anche se la tua organizzazione utilizza più ambienti o aziende per separare i dati.

## Il riquadro della chat di Copilot non viene visualizzato. Come si deve procedere?

Verifica che la lingua utente in Impostazioni personali sia impostata su Inglese e che la versione del tuo ambiente sia 24.0 o successiva. Nella pagina Funzionalità di Copilot e IA, assicurati che gli amministratori abbiano attivato il consenso per i dati in tutte le aree geografiche e abbiano attivato la chat. Assicurati che la localizzazione del tuo ambiente non sia il Canada.

Se ancora non vedi la funzionalità chat con Copilot, è possibile che Microsoft stia ancora implementando la funzionalità nella tua regione. Copilot sarà disponibile inizialmente per i clienti statunitensi nell'aprile 2024 e successivamente, nel corso delle settimane, nelle localizzazioni di altri paesi/regioni.

## Perché Copilot mostra solo tre record nel riquadro Chat?

Quando chiedi a Copilot di recuperare i record, il modo in cui formuli la domanda determina il modo in cui Copilot identifica e applica i filtri sulle pagine per trovare ciò che stai cercando. Per mantenere le risposte compatte e concise, il riquadro Chat visualizza un massimo di tre riquadri di record, anche quando Copilot trova un numero maggiore di record pertinenti.

## Copilot restituisce risposte errate ai totali e ad altri calcoli

Durante l'anteprima, Chat con Copilot può individuare record, spiegare concetti e guidare l'utente su come completare le attività in Business Central. Non sono supportati altri casi d'uso, come la somma di un campo tra record o il calcolo dell'importo medio mensile. Ci auguriamo di aggiungere competenze matematiche di base a Copilot in futuro.

## Posso usare la voce invece di digitare i miei messaggi?

Puoi chattare con Copilot utilizzando la digitazione vocale per parlare invece di digitare le parole nel riquadro Chat. La digitazione vocale utilizza il riconoscimento vocale online ed è disponibile con Windows. Per utilizzare la voce, attiva la finestra dei messaggi di chat, quindi utilizza la scorciatoia <kbd>Windows</kbd>+<kbd>H</kbd> e inizia a parlare. Per ulteriori informazioni, vedi [Utilizzare la digitazione vocale per parlare anziché digitare sul PC](https://support.microsoft.com/windows/use-voice-typing-to-talk-instead-of-type-on-your-pc-fec94565-c4bd-329d-e59a-af033fa5689f).

## Passaggi successivi

[Chat con Copilot (anteprima)](chat-with-copilot.md)
