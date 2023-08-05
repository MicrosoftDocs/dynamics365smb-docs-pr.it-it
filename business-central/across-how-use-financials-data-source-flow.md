---
title: Utilizzare flussi di Power Automate in Business Central
description: Configurare e utilizzare flussi di Power Automate per creare o modificare i dati di Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: 'workflow, OData, Power App, SOAP, Power Automate,'
ms.search.form: '1500,'
ms.date: 10/10/2022
ms.custom: bap-template
---
# Utilizzare i flussi di Power Automate in [!INCLUDE[prod_short](includes/prod_short.md)]

Con [!INCLUDE[prod_short](includes/prod_short.md)], ti viene assegnata una licenza per Microsoft Power Automate. Questa licenza ti consente di utilizzare i dati di [!INCLUDE[prod_short](includes/prod_short.md)] come parte di un flusso di lavoro in Microsoft Power Automate. Crea i tuoi flussi e connettiti ai tuoi dati da origini interni ed esterni tramite il connettore [!INCLUDE [prod_short](includes/prod_short.md)].

I flussi Power Automate vengono attivati da eventi, ad esempio la creazione, la modifica o l'eliminazione di un record. Possono anche essere eseguiti su una pianificazione definita dall'utente o su richiesta.

> [!NOTE]
> Gli amministratori possono limitare l'accesso a Power Automate. Se ritieni di non avere accesso ad alcune o a tutte le funzionalità descritte in questo articolo, contatta il tuo amministratore. Se desideri imparare come puoi controllare l'accesso a Power Automate come amministratore, vedi [Configurare l'integrazione di Power Automate](/dynamics365/business-central/dev-itpro/powerplatform/power-automate-setup).

<!-- You must have a valid account with both [!INCLUDE[prod_short](includes/prod_short.md)] and Power Automate. --> 

> [!TIP]
> Oltre a Power Automate, è possibile utilizzare i modelli di flusso di lavoro di approvazione in [!INCLUDE[prod_short](includes/prod_short.md)]. Sebbene siano presenti due sistemi del flusso di lavoro, qualsiasi modello di flusso di lavoro di approvazione creato con Power Automate viene aggiunta all'elenco dei workflow in [!INCLUDE[prod_short](includes/prod_short.md)]. Ulteriori informazioni in [Flussi di lavoro](across-workflow.md).

## Informazioni sui flussi Power Automate

Power Automate è un servizio che ti aiuta a creare flussi di lavoro (o flussi) automatizzati tra app e servizi, ad esempio [!INCLUDE[prod_short](includes/prod_short.md)]. I flussi Power Automate richiedono poca o nessuna conoscenza di codifica. Possono essere associati a un'ampia gamma di eventi e risposte, come ad esempio:

- Registrare le modifiche
- Aggiornamenti di file esterni
- Documenti registrati
- Diversi servizi Microsoft e di terze parti, come Microsoft Outlook, Excel, Dataverse, Teams, SharePoint, Power Apps e altro ancora.

Esistono tre diversi tipi di flussi cloud con cui puoi lavorare:

|Tipo di flusso|Descrizione|
|---------|-----------|
|Automatizzato|Questo tipo di flusso viene eseguito automaticamente da un evento. In [!INCLUDE[prod_short](includes/prod_short.md)], un evento potrebbe verificarsi quando un record o un documento viene creato, modificato o eliminato. Ad esempio, una nuova fattura di vendita può attivare un flusso per una richiesta di approvazione, che può avere eventi diversi impostati a seconda della risposta dell'approvatore. Una risposta negativa invia una notifica e un'e-mail al richiedente l'approvazione. Una risposta positiva aggiorna contemporaneamente un foglio di calcolo Excel che si trova in una cartella di SharePoint e invia un aggiornamento a una chat di Teams. I flussi automatizzati possono essere avviati da eventi interni ed esterni in [!INCLUDE[prod_short](includes/prod_short.md)].|
|Pianificato|Anche questo tipo di flusso viene eseguito automaticamente, ma viene eseguito periodicamente a una data e un'ora pianificate. |
|Istantaneo |Questo tipo di flusso viene eseguito su richiesta, richiedendo all'utente di eseguirlo manualmente da un pulsante o un'azione in un'altra app o dispositivo, in questo caso, il client [!INCLUDE[prod_short](includes/prod_short.md)]. I flussi istantanei funzionano in modo simile ai collegamenti batch, eseguendo più passaggi lunghi con poche pressioni di pulsanti e vengono avviati da pagine o tabelle specifiche. Ad esempio, un flusso può aggiungere un pulsante al menu delle azioni nella pagina **Fornitori** per bloccare i pagamenti a un fornitore e, allo stesso tempo, inviare e-mail personalizzabili al contatto del fornitore e agli acquirenti della tua azienda, nonché aggiornare il contatto in Outlook. |

## Funzionalità di Power Automate

Puoi esplorare tutti i flussi Power Automate attualmente disponibili per te effettuando l'accesso a [Power Automate](https://powerautomate.com) e selezionando **I miei flussi** dalla barra di spostamento sul lato sinistro. Qui troverai tutti i flussi che hai già creato e i flussi condivisi con te da un amministratore o un collega.

- I flussi istantanei sono disponibili anche per essere eseguiti direttamente dalla maggior parte delle pagine di elenchi, schede e documenti in [!INCLUDE[prod_short](includes/prod_short.md)]. Troverai i flussi istantanei nel gruppo di azioni **Automatizza** nella barra delle azioni delle pagine. Per eseguire un flusso, selezionalo e segui le istruzioni visualizzate. Ulteriori informazioni nelle sezioni di seguito.
 
- Con i flussi automatizzati in [!INCLUDE[prod_short](includes/prod_short.md)], non c'è niente che puoi fare, a meno che tu non voglia cambiarli o disattivarli. Altrimenti, funzioneranno solo se attivati. 
<!--

## Automated flows

With Power Automate, you can create business flows directly in-house and rely on citizen developers. Automated workflows can be started by both internal and external events in [!INCLUDE[prod_short](includes/prod_short.md)], and also be set to run periodically. Learn more and get instructions on how to create flows in the [Set Up Automated Workflows](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) article in the administration content.

-->

## Eseguire flussi istantanei

I flussi di lavoro istantanei vengono aperti in [!INCLUDE [prod_short](includes/prod_short.md)] online in modo da rimanere nel contesto del processo aziendale corrente. Puoi eseguire un flusso istantaneo dalla maggior parte degli elenchi, delle schede o dei documenti.

1. Nella barra delle azioni, seleziona **Automatizza**, quindi scegli un flusso dall'elenco dei flussi disponibili nell'azione **Power Automate**

    :::image type="content" source="media/power-automate-action-intro.png" alt-text="Mostra l'azione Automatizza nella barra delle azioni con le azioni espanse.":::

    In alcune pagine, **Automatizza** è nidificato in **Altre opzioni (...)**. 
2. Nel riquadro **Esegui flusso**, compila tutti i campi richiesti, quindi seleziona **Continua** per eseguire il flusso.

> [!NOTE]
> La prima volta che usi l'elemento **Automatizza**, potresti vedere solo l'azione **Introduzione a Power Automate**. Visualizzi questa azione perché non hai accettato l'informativa sulla privacy per Microsoft Power Automate. Per continuare, seleziona **Introduzione a Power Automate** e segui le istruzioni per accettare o meno.  
>
> :::image type="content" source="media/power-automate-action.png" alt-text="Mostra l'elemento Automatizza nella barra delle azioni.":::

<!--

[!INCLUDE [prod_short](includes/prod_short.md)] can run a Power Automate flow from most list, card, and document pages. Once the admin has connected [!INCLUDE [prod_short](includes/prod_short.md)] with Power Automate, you'll see any flows your organization has added when you choose the **Automate** action on the relevant pages. Instant flows are run without leaving [!INCLUDE [prod_short](includes/prod_short.md)]. Learn more in the [Set Up Automated Workflows](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) article in the administration content.

These instant flows open on a page inside [!INCLUDE [prod_short](includes/prod_short.md)] online so you can remain within the context of the business process you were in the middle of. Choose the **Automate** action—on some pages nested under the **More Options** menu—choose the **Power Automate** menu item, then choose the relevant link to trigger the workflow. The connection to Power Automate is already set up for you.

Most flows require you to fill in a field or two before you choose the **Run flow** action.

> [!TIP]
> If you don't see an **Automate** action, then your [!INCLUDE [prod_short](includes/prod_short.md)] probably hasn't yet been set up to use Power Automate. Learn more from your admin.-->

## Creare, modificare e gestire flussi

È possibile creare nuovi flussi, modificare e gestire quelli esistenti (attivarli o disattivarli) direttamente in Power Automate. Puoi persino avviare alcune di queste attività da dentro [!INCLUDE[prod_short](includes/prod_short.md)]:

- Per creare un flusso istantaneo da una pagina elenco, scheda o documento, seleziona **Automatizza** > **Crea un flusso**.
- Per aprire Power Automate da una pagina elenco, scheda o documento, seleziona **Automatizza** > **Gestisci flussi**.
<!--- To create new flows or manage existing flows from inside [!INCLUDE[prod_short](includes/prod_short.md)], got to the **Manage Power Automate Flows** page.-->

Queste attività vengono in genere eseguite da un amministratore o un utente con privilegi avanzati. Le attività richiedono una conoscenza più ampia dei processi aziendali in [!INCLUDE[prod_short](includes/prod_short.md)]. Per ulteriori informazioni, vedi [Integrazione di Power Automate](/dynamics365/business-central/dev-itpro/powerplatform/power-automate-overview), [Imposta flussi istantanei](/dynamics365/business-central/dev-itpro/powerplatform/instant-flows) e [Gestisci flussi Power Automate](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows).
<!-- 

## Add more automated flows and instant flows

You can create flows through the [powerautomate.microsoft.com](https://powerautomate.microsoft.com) website. However, if your admin has switched on the capability to run Power Automate flows from inside [!INCLUDE [prod_short](includes/prod_short.md)] online, you can start the process of building a flow from the **Automate** action on the relevant pages, which can be found under the **More Options** menu depending on the page. Then choose the **Power Automate** menu item, and then choose the **Create a flow** action. Power Automate then opens in a new browser tab, and you're signed in automatically.

You can find sample templates to adapt to your company and all available trigger events, using both [!INCLUDE [prod_short](includes/prod_short.md)] and external tools, by choosing the **Connectors** menu on the Power Automate website. Learn more about available templates and triggers in the [Set Up Automated Workflows](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) article in the administration content.

## Create and manage Power Automate flows

You can create new flows or manage existing Power Automate flows in [!INCLUDE [prod_short](includes/prod_short.md)] on the **Manage Power Automate Flows** page. Learn more in the [Manage Power Automate Flows](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows) article in the administration content.

<!--
You can also manage available Power Automate workflows on the **Workflows** page in [!INCLUDE[prod_short](includes/prod_short.md)]. The page lists both the built-in approval and Power Automate workflows, with options for the latter to enable/disable, delete, and view the workflow on the Power Automate website.-->

## Vedi il relativo [training Microsoft](/training/modules/use-power-automate/)

## Vedere anche

[Risolvere i problemi dei flussi di lavoro automatizzati di [!INCLUDE[prod_short](includes/prod_short.md)]](across-flow-troubleshoot.md)  
[Preparazione al business](ui-get-ready-business.md)  
[Flussi di lavoro](across-workflow.md)  
[Importazione dei dati aziendali da altri sistemi contabili](across-import-data-configuration-packages.md)  
[Assegnare autorizzazioni a utenti e gruppi](ui-define-granular-permissions.md)  
[Configurare [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Finanze](finance.md)  
[Gestire flussi di Power Automate](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows)  
[Configurare flussi di lavoro automatizzati](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows)  
[Attivare flussi istantanei](/dynamics365/business-central/dev-itpro/powerplatform/instant-flows)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
a