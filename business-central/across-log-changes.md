---
title: Revisione delle modifiche | Microsoft Docs
description: È possibile attivare un registro utente in modo da disporre di uno storico di tutte le modifiche apportate ai dati delle tabelle tracciate. È anche possibile tenere traccia delle attività con determinati tipi di registri attività.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user log, user activity, tracking
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: bce5c61afd2a1119c25e37ece65081ef0519694e
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754344"
---
# <a name="auditing-changes-in-business-central"></a>Revisione delle modifiche in Business Central
Una sfida comune in molte applicazioni di gestione aziendale è evitare modifiche indesiderate nei dati. Potrebbe trattarsi di un numero di telefono errato del cliente o di una registrazione errata nella contabilità generale. Questo argomento descrive le funzionalità per scoprire cosa è cambiato, chi l'ha cambiato e quando è stato cambiato.

## <a name="about-the-change-log"></a>Informazioni sul log modifiche 
Il log modifiche consente di tenere traccia di tutte le modifiche dirette apportate da un utente ai dati nel database. È necessario specificare cosa si desidera venga registrato per ciascuna tabella e campo, quindi attivare il log modifiche.  

Il log modifiche è basato sulle modifiche apportate ai dati nelle tabelle che si traccia. Nella pagina **Movimenti log modifiche**, i movimenti vengono ordinati cronologicamente e mostrano tutte le modifiche apportate ai valori dei campi nelle tabelle specificate.

> [!Important]
> Le modifiche vengono visualizzate in **Voci log modifiche** solo dopo il riavvio della sessione dell'utente, che avviene come segue:
<br />
> * La sessione è scaduta ed è stata aggiornata.
> * L'utente ha selezionato un'altra società o gestione ruolo utente.
> * L'utente si è disconnesso e connesso di nuovo.

### <a name="working-with-the-change-log"></a>Utilizzo del log modifiche
Il log modifiche viene attivato e disattivato nella pagina **Setup log modifiche**. Quando un utente attiva o disattiva il log modifiche, questa attività viene registrata, in modo da poter visualizzare sempre quale utente ha disattivato o riattivato il log modifiche.

Nella pagina **Setup log modifiche** se si sceglie l'azione **Tabelle** è possibile specificare le tabelle di cui si desidera tracciare le modifiche e le modifiche da tracciare. [!INCLUDE[prod_short](includes/prod_short.md)] tiene traccia anche di una serie di tabelle di sistema.

> [!NOTE]
> È possibile monitorare campi specifici per le modifiche, come i campi che contengono dati sensibili, impostando il monitoraggio dei campi. In caso contrario, per evitare la ridondanza, la tabella che contiene il campo non sarà disponibile per l'impostazione del log delle modifiche. Per ulteriori informazioni, vedere [Monitoraggio di campi sensibili](across-log-changes.md#monitoring-sensitive-fields).

Dopo avere impostato e attivato il log modifiche e apportato una modifica ai dati, è possibile visualizzare e filtrare le modifiche nella pagina **Movimenti log modifiche**. Se si desidera rimuovere i movimenti, è possibile farlo nella pagina **Elimina mov. log modifiche**, in cui è possibile impostare filtri in base alle date e all'ora.  

## <a name="about-activity-logs"></a>Informazioni sui log attività
Da alcune pagine in [!INCLUDE [prod_short](includes/prod_short.md)], è possibile visualizzare un log attività che mostra lo stato e gli eventuali errori nei file esportati da o importati in [!INCLUDE [prod_short](includes/prod_short.md)].  

### <a name="working-with-activity-logs"></a>Utilizzare log di attività
Le informazioni vengono visualizzate nella finestra **Log attività** in base alla pagina di contesto dalla quale viene aperta. Ad esempio, è possibile aprire la pagina dalle pagine **Setup servizio di scambio documenti**, **Documento in entrata**, **Fattura vendita registrata** e **Note cr. vendita registrate**. È possibile svuotare l'elenco dei movimenti del log o semplicemente cancellare l'elenco dei movimenti più vecchi di sette giorni.  

## <a name="monitoring-sensitive-fields"></a>Monitoraggio dei campi riservati
Mantenere i dati sensibili protetti e privati è una preoccupazione fondamentale per la maggior parte delle aziende. Per aggiungere un livello di sicurezza, è possibile monitorare i campi importanti ed essere avvisati tramite e-mail quando qualcuno modifica un valore. Ad esempio, è possibile essere avvisati se qualcuno cambia il numero IBAN della tua azienda.

> [!NOTE]
> L'invio di notifiche tramite e-mail richiede la configurazione della funzione e-mail in [!INCLUDE[prod_short](includes/prod_short.md)]. Per ulteriori informazioni, vedere [Configurare la posta elettronica](admin-how-setup-email.md).

### <a name="setting-up-field-monitoring"></a>Impostazione del monitoraggio campi
Usare la guida al setup assistito **Setup monitoraggio modifiche campi** per specificare i campi che si desidera monitorare in base a criteri di filtro, come la classificazione dei dati riservati per i campi. Per ulteriori informazioni, vedere [Classificazione di dati riservati](admin-classifying-data-sensitivity.md). La guida consente inoltre di specificare la persona che riceverà la notifica e-mail quando si verifica una modifica e l'account e-mail che invierà l'e-mail di notifica. È necessario specificare sia la notifica dell'utente che l'account da cui inviare la notifica. Al termine della guida, è possibile gestire le impostazioni per il monitoraggio dei campi nella pagina **Setup monitoraggio campi**. 

Nel tempo, l'elenco delle voci nella pagina **Voci del log dei campi monitorati** cresce. Per ridurre il numero di voci è possibile creare un criterio di conservazione che eliminerà le voci dopo un periodo di tempo specificato. Per ulteriori informazioni, vedere [Definire i criteri di conservazione](admin-data-retention-policies.md).

Quando si imposta il monitoraggio dei campi o si cambia qualcosa nella configurazione, vengono create voci per le modifiche. È possibile specificare se visualizzare le voci relative alla configurazione del monitoraggio mostrandole o nascondendole. 

È possibile gestire le impostazioni per il monitoraggio dei campi, ad esempio se inviare una notifica e-mail o semplicemente registrare la modifica, per ogni campo nella pagina **Foglio di lavoro dei campi monitorati**. Nella pagina è anche possibile aggiungere o rimuovere i campi da monitorare.

> [!NOTE]
> Dopo aver aggiunto uno o più campi e avviato il monitoraggio, è necessario disconnettersi da [!INCLUDE[prod_short](includes/prod_short.md)] e accedere di nuovo per applicare le tue impostazioni.

### <a name="working-with-field-monitoring"></a>Utilizzo del monitoraggio campi

Le voci per tutti i valori modificati per i campi monitorati sono disponibili nella pagina **Voci del log dei campi monitorati**. Ad esempio, le voci contengono informazioni come il campo per il quale il valore è stato modificato, i valori originali e nuovi e chi ha apportato la modifica e quando lo ha fatto. Per esaminare ulteriormente una modifica, scegliere un valore per aprire la pagina in cui è stata apportata. Per visualizzare un elenco di tutte le voci, scegliere **Movimenti modifica campo**.

### <a name="viewing-field-monitoring-telemetry"></a>Visualizzare la telemetria di monitoraggio dei campi 

È possibile configurare [!INCLUDE[prod_short](includes/prod_short.md)] per inviare attività di monitoraggio dei campi a una risorsa Application Insights in Microsoft Azure. Quindi, utilizzando Monitoraggio di Azure, si creano report e si configurano avvisi sui dati raccolti. Per ulteriori informazioni, vedere i seguenti articoli nella Guida per sviluppatori e professionisti IT di [!INCLUDE[prod_short](includes/prod_short.md)].

- [Monitoraggio e analisi della telemetria - Abilitazione di Application Insights](/dynamics365/business-central/dev-itpro/administration/telemetry-overview#enable)
- [Analizzare la telemetria di monitoraggio dei campi](/dynamics365/business-central/dev-itpro/administration/telemetry-field-monitoring-trace)

## <a name="defining-retention-policies"></a>Definizione dei criteri di conservazione

È possibile creare criteri di conservazione per eliminare i dati non necessari nei log dopo un periodo di tempo specificato. Ad esempio, nel tempo il numero di voci in un log può aumentare. Eliminando le vecchie voci è possibile concentrarsi più facilmente sulle voci più recenti e probabilmente più rilevanti. Per ulteriori informazioni, vedere [Definire i criteri di conservazione](admin-data-retention-policies.md).

## <a name="see-also"></a>Vedere anche
[Modificare le impostazioni di base](ui-change-basic-settings.md)  
[Ricerca, filtro e ordinamento](ui-enter-criteria-filters.md)  
[Individuare pagine e informazioni con la funzionalità delle informazioni](ui-search.md)  
[Assegnare autorizzazioni a utenti e gruppi](ui-define-granular-permissions.md)    
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Definire i criteri di conservazione](admin-data-retention-policies.md)  