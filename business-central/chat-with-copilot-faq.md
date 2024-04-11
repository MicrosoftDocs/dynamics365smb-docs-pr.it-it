---
title: Domande frequenti su Chat con Copilot
description: Questo articolo fornisce le risposte ad alcune domande comuni su Chat con Copilot in Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: conceptual
ms.collection:
  - bap-ai-copilot
ms.date: 02/27/2024
ms.custom: bap-template jswymer
---
# <a name="chat-with-copilot-faq"></a>Domande frequenti su Chat con Copilot

[!INCLUDE[preview-banner](includes/preview-banner.md)]

Questo articolo fornisce le risposte ad alcune domande comuni sulla chat con Copilot in [!INCLUDE[prod_short](includes/prod_short.md)]. Per domande relative all'intelligenza artificiale e alla chat, consulta [Domande frequenti sull'intelligenza artificiale responsabile per Chat con Copilot](faqs-chat-with-copilot.md).

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

## <a name="can-admins-grant-or-deny-permission-to-individual-users-to-get-access-to-chat"></a>Gli amministratori possono concedere o negare l'autorizzazione a singoli utenti per accedere alla chat?

No, non esiste alcuna autorizzazione o set di autorizzazioni per la chat. Se la chat è attivata nella pagina [Funzionalità di Copilot e IA](enable-ai.md), ogni utente in un ambiente ha accesso alla chat.
 
## <a name="is-chat-available-on-tablet-phone-or-other-form-factors"></a>La chat è disponibile su tablet, telefono o altri fattori di forma?

No, il riquadro della chat è disponibile solo nel client Web [!INCLUDE[web_client](includes/web_client.md)].

## <a name="i-dont-use-business-central-in-english-what-are-my-options"></a>Non utilizzo Business Central in inglese. Quali sono le opzioni disponibili?

Al momento la chat è disponibile solo in inglese. Puoi impostare l'inglese come lingua utente in [Impostazioni personali](ui-change-basic-settings.md#language).

## <a name="which-business-central-version-do-i-need-to-experience-chat"></a>Quale versione di Business Central è necessaria per provare la chat?

La chat è disponibile in anteprima pubblica dalla versione 24.0 (ciclo di rilascio 1 del 2024).

## <a name="does-chat-work-with-my-customizations"></a>La chat funziona con le mie personalizzazioni?

Dipende dal tipo di domanda che poni a Copilot. Ad esempio:

- Quando poni domande per individuare record, Copilot è in grado di trovare i record nelle tabelle personalizzate identificate utilizzando campi personalizzati.
- Quando chiedi spiegazioni o indicazioni, Copilot non ha accesso ad alcuna informazione sulle tue personalizzazioni o documentazione per i tuoi componenti aggiuntivi.

## <a name="copilot-never-seems-to-open-the-record-or-page-i-asked-for-what-am-i-doing-wrong"></a>Sembra che Copilot non apra mai il record o la pagina che ho richiesto. Che cosa sto facendo di sbagliato?

Quando chiedi a Copilot di trovare record in [!INCLUDE[prod_short](includes/prod_short.md)], visualizza tutti i record trovati come riquadri o collegamenti selezionabili nel riquadro della chat. Durante l'anteprima, Copilot non passa automaticamente ad alcuna pagina.

## <a name="the-answers-i-get-from-copilot-vary-even-though-i-ask-the-same-question-is-it-a-bug"></a>Le risposte che ricevo da Copilot variano anche se faccio la stessa domanda. È un errore?

Copilot potrebbe occasionalmente rispondere in modi diversi. Le risposte non sono necessariamente identiche.

## <a name="when-should-i-use-the-copy-function-on-chat-messages"></a>Quando dovrei utilizzare la funzione Copia nei messaggi di chat?

Puoi utilizzare il pulsante Copia per copiare un messaggio precedente nella conversazione con Copilot, incollarlo nella casella di input per provare o riprovare una variante del tuo messaggio a Copilot.

## <a name="how-do-i-customize-or-extend-chat"></a>Come posso personalizzare o estendere la chat?

Durante l'anteprima, il riquadro della chat e le risposte di Copilot non possono essere modificati in alcun modo tramite personalizzazione, componenti aggiuntivi o individualizzazione.

## <a name="does-copilot-find-data-in-other-companies-or-environments"></a>Copilot trova dati in altre aziende o ambienti?

Anche se la tua organizzazione utilizza più ambienti o società per separare i dati, Copilot cerca record solo nella società a cui hai effettuato l'accesso.

## <a name="the-copilot-chat-pane-doesnt-show-what-can-i-do"></a>Il riquadro della chat di Copilot non viene visualizzato. Come si deve procedere?

Verifica che la lingua utente in Impostazioni personali sia impostata su Inglese e che la versione del tuo ambiente sia 24.0 o successiva. Nella pagina Funzionalità di Copilot e IA, assicurati che gli amministratori abbiano attivato il consenso per i dati in tutte le aree geografiche e abbiano attivato la chat. Assicurati che la localizzazione del tuo ambiente non sia il Canada.

Se ancora non vedi la funzionalità Chat con Copilot, è possibile che Microsoft ne stia eseguendo la distribuzone nella tua area geografica. Copilot verrà distribuito dapprima ai clienti statunitensi nell'aprile 2024 e poi nelle settimane successive negli altri paesi.

## <a name="next-steps"></a>Passaggi successivi

[Chat con Copilot (anteprima)](chat-with-copilot.md)
