---
title: Utilizzo dei report Power BI in Business Central | Microsoft Docs
description: 'Ottenere informazioni dettagliate, business intelligence e KPI dai dati di Business Central utilizzando Power BI.'
author: jswymer
ms.topic: get-started
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.date: 12/19/2023
ms.author: jswymer
---
# <a name="work-with-power-bi-reports-in-"></a>Utilizzare i report Power BI in [!INCLUDE [prod_short](includes/prod_short.md)]

In questo articolo vengono spiegate alcune delle nozioni di base sulla visualizzazione dei report Power BI, incluse le scorecard, in [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="overview"></a>Panoramica

I report Power BI offrono informazioni dettagliate da [!INCLUDE[prod_short](includes/prod_short.md)]. Varie pagine in [!INCLUDE [prod_short](includes/prod_short.md)] includono una parte di un report Power BI che può visualizzare report Power BI. La Gestione ruolo utente è una tipica pagina in cui è visibile una parte di report Power BI. Alcune pagine di elenco, come **Elementi**, includono anche una parte Power BI.

[!INCLUDE [prod_short](includes/prod_short.md)] lavora insieme al servizio Power BI. I report da visualizzare in [!INCLUDE [prod_short](includes/prod_short.md)] sono memorizzati nel servizio Power BI. In [!INCLUDE [prod_short](includes/prod_short.md)], è possibile cambiare il report visualizzato nella parte Power BI di qualsiasi report Power BI disponibile nel servizio Power BI. La prima volta che si accede a [!INCLUDE [prod_short](includes/prod_short.md)] e finché non ci si connette al servizio Power BI le parti saranno vuote, come mostrato qui:

![Parte Power BI in Business Central.](./media/power-bi-part.png)

## <a name="get-started"></a>Inizia

### <a name="prerequisites"></a>Prerequisiti

Se si sta usando [!INCLUDE[prod_short](includes/prod_short.md)] in locale, deve essere abilitato per l'integrazione di Power BI. Questa attività è in genere eseguita da un amministratore. Per ulteriori informazioni, vedere [Impostare [!INCLUDE[prod_short](includes/prod_short.md)] in locale per l'integrazione di Power BI](admin-powerbi-setup.md#setup).

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] online è già impostato per l'integrazione con Power BI.

### <a name="sign-up-power-bi"></a>Iscrizione a Power BI

Prima di poter usare Power BI con [!INCLUDE[prod_short](includes/prod_short.md)], dovrai registrarti al servizio Power BI. Se non si è già registrati andare a [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Quando ci si registra, utilizzare l'indirizzo e-mail e la password di lavoro.

## <a name="connect-to-power-bi---one-time-only"></a><a name="connect"></a>Connettersi a Power BI - una sola volta

Quando si accede per la prima volta a [!INCLUDE [prod_short](includes/prod_short.md)], potrai vedere una parte di Power BI vuota (come mostrato nella figura precedente) su varie pagine. La prima cosa da fare è connettersi all'account Power BI. Una volta connessi, è possibile vedere i report. È necessario eseguire questo passaggio solo una volta.

1. Seleziona il collegamento **Introduzione a Power BI** nella parte **Report di Power BI**.
2. Viene avviato il setup assistito **Configura report Power BI in Business Central**. Seleziona **Avanti** per continuare.
3. Nella pagina **Verifica la tua licenza Power BI**. Effettua uno dei seguenti passaggi:

    - Se non ti sei ancora registrato a Power BI, seleziona [Vai alla Home Page di Power BI](https://powerbi.microsoft.com). Crea un account, quindi torna a [!INCLUDE[prod_short](includes/prod_short.md)] e completa la configurazione.

    - Se hai già una licenza, seleziona **Avanti**.
4. Nella pagina successiva, [!INCLUDE[prod_short](includes/prod_short.md)] caricherà ora un report demo su Power BI. Questo passaggio richiederà alcuni minuti, pertanto viene eseguito in background. Per completare la configurazione, seleziona **Avanti**, quindi **Fine**.

Viene avviato il processo di connessione. Durante il processo, [!INCLUDE [prod_short](includes/prod_short.md)] comunica con il servizio Power BI per determinare se si dispone di un account Power BI valido e di una licenza. Dopo la verifica della licenza, il report Power BI predefinito viene visualizzato nella pagina. Se non viene visualizzato un report, è possibile selezionare un report dalla parte.

> [!TIP]
> Con [!INCLUDE [prod_short](includes/prod_short.md)] online, questo passaggio caricherà automaticamente i report Power BI predefiniti utilizzati in [!INCLUDE [prod_short](includes/prod_short.md)] nell'area di lavoro Power BI.

#### <a name="from--on-premises"></a>Da [!INCLUDE [prod_short](includes/prod_short.md)] in locale

La connessione a Power BI da [!INCLUDE [prod_short](includes/prod_short.md)] è simile a quella per la soluzione online. È tuttavia possibile che nella pagina **AUTORIZZAZIONI DI SERVIZIO MICROSOFT ENTRA** venga richiesto di concedere l'accesso ai servizi Power BI. Per concedere l'accesso, selezionare **Autorizza i servizi di Azure** e poi **Accetta**.

Una volta connessi è possibile selezionare un report dalla parte Power BI nelle pagine.

## <a name="work-with-power-bi-reports"></a>Utilizzare i report Power BI

### <a name="show-reports-on-list-pages"></a>Visualizza i report sulle pagine di elenco

[!INCLUDE[prod_long](includes/prod_long.md)] include un riquadro Dettaglio informazioni Power BI su diverse pagine elenco chiave. Questo riquadro Dettaglio informazioni fornisce ulteriori informazioni sui dati nell'elenco. Spostandosi tra le righe dell'elenco, il report viene aggiornato e filtrato per la voce selezionata.

Per informazioni su come creare report per le pagine di elenco, vedi [Creazione di report Power BI per la visualizzazione dei dati dell'elenco in [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-powerbi-reports-factbox.md).

> [!TIP]
> Se non vedi il riquadro Dettaglio Power BI, potrebbe essere nascosto nella tua area di lavoro dalla personalizzazione. Seleziona l'icona ![Impostazioni.](media/ui-experience/settings_icon_small.png "Icona Impostazioni per Gestione ruolo utente") e poi l'azione **Personalizza**. Per ulteriori informazioni, vedi [Personalizzare l'area di lavoro](ui-personalization-user.md).
>
> Oppure, se disponi di una versione precedente di Business Central, vai alla barra delle azioni, seleziona **Azioni** > **Visualizza** > **Mostra/nascondi report Power BI**.

### <a name="switch-reports"></a>Cambia rapporti

Una parte Power BI su una pagina può visualizzare qualsiasi report Power BI disponibile. Per passare alla visualizzazione di un altro report, scegliere l'azione **Seleziona report** dall'elenco a discesa dei comandi nella parte superiore della parte.  

La pagina **di selezione dei report Power BI** mostra un elenco di tutti i report Power BI a cui si ha accesso. Questa lista viene recuperata da qualsiasi spazio di lavoro tuo o condiviso con te nel servizio Power BI . Selezionare la casella **Abilita** per ogni report che si intende visualizzare nella pagina quindi scegliere **OK**. Viene visualizzata di nuovo la pagina con l'ultimo report abilitato. Mediante l'elenco a discesa, utilizzare i comandi **Precedente** e **Successivo** per spostarsi tra i report.  

### <a name="get-more-reports"></a>Ottieni più report

Se non è visualizzato alcun report nella pagina **di selezione dei report Power BI** o non è visualizzato il report desiderato, scegliere **Ottieni report**. Questa azione consente di cercare i report in due posizioni: *Organizzazione personale* o *Servizi*.

- Scegliere **Organizzazione personale** per andare ai servizi Power BI. Da qui è possibile visualizzare i report all'interno dell'organizzazione per i quali sono stati concessi i diritti di visualizzazione. Quindi è possibile aggiungerli all'area di lavoro.
- Scegliere **Servizi** per passare a Microsoft AppSource dove è possibile installare le app Power BI.  

> [!TIP]
> Se Power BI Desktop è disponibile, è anche possibile creare nuovi report Power BI. Quindi, dopo la pubblicazione di questi report nell'area di lavoro Power BI, visualizzati nella pagina **di selezione dei report Power BI**.  

### <a name="manage-and-modify-reports"></a>Gestire e modificare i report

È possibile apportare modifiche a un report nella parte Power BI. Le modifiche apportate verranno quindi pubblicate nel servizio Power BI. Se il report è condiviso con altri utenti, anche loro vedranno le modifiche, a meno che non si salvano le modifiche in un nuovo report.

Per modificare un report, scegliere l'azione **Gestisci report** dall'elenco a discesa dei comandi nella parte Power BI. Quindi iniziare ad apportare le modifiche. Una volta terminate le modifiche, selezionare **File** > **Salva**. Se si tratta di un report condiviso e non si desidera applicare la modifica per tutti gli utenti, selezionare **Salva come** per evitare di applicare questa modifica a tutti gli utenti.

Quando si ritorna a Gestione ruolo utente, il report aggiornato verrà visualizzato. Se è stato usato **Salva come**, è necessario scegliere **Seleziona report**, quindi abilitare il nuovo report per visualizzarlo.

> [!NOTE]
> Questa funzionalità non è disponibile con [!INCLUDE [prod_short](includes/prod_short.md)] locale.

### <a name="upload-reports"></a><a name="upload"></a>Caricare i report

I report Power BI possono essere distribuiti tra gli utenti come file .pbix. Se sono disponibili file .pbix, è possibile caricarli e condividerli con tutti gli utenti di [!INCLUDE [prod_short](includes/prod_short.md)]. I report sono condivisi in ogni società in [!INCLUDE [prod_short](includes/prod_short.md)].  

Per caricare un report, selezionare l'azione **Carica report** dall'elenco a discesa dei comandi nella parte **Report Power BI**. Quindi individuare il file .pbix che definisce i report che si desidera condividere. È possibile modificare il nome predefinito del file.  

Dopo che il report è stato caricato nell'area di lavoro Power BI viene automaticamente caricato nelle aree di lavoro Power BI degli altri utenti.

> [!NOTE]
> Il caricamento di un report richiede privilegi avanzati in [!INCLUDE[prod_short](includes/prod_short.md)]. Inoltre, non è possibile caricare report con [!INCLUDE [prod_short](includes/prod_short.md)] locale. Con la soluzione locale i report vengono caricati direttamente nell'area di lavoro Power BI. Per ulteriori informazioni, vedi [Utilizzare dati di [!INCLUDE [prod_short](includes/prod_short.md)] in Power BI](across-working-with-business-central-in-powerbi.md).

## <a name="fixing-problems"></a>Risolvere i problemi

Tuttavia, se si verifica un errore, in questa sezione viene fornita una soluzione alternativa per i problemi più comuni.  

### <a name="you-dont-have-a-power-bi-account"></a>Non si dispone di un account Power BI

Un account Power BI non è stato impostato. Per ottenere un account Power BI valido, è necessario avere una licenza e aver effettuato l'accesso a Power BI in precedenza per creare un'area di lavoro Power BI.

### <a name="message-there-are-no-enabled-reports-choose-select-report-to-see-a-list-of-reports-that-you-can-display"></a>Messaggio: Non sono presenti report abilitati. Scegliere Seleziona report per visualizzare un elenco di report che è possibile visualizzare.

Questo messaggio viene visualizzato se la distribuzione del report predefinito non è riuscita nell'area di lavoro Power BI. In alternativa il report è stato distribuito ma non è stato aggiornato correttamente. Accedere al report nella propria area di lavoro Power BI, selezionare **Set di dati**, **Impostazioni** e quindi aggiornare manualmente le credenziali. Dopo aver aggiornato correttamente il set di dati, torna a [!INCLUDE[prod_short](includes/prod_short.md)] e seleziona manualmente il report dalla pagina **Selezionare i report**.

#### <a name="you-cant-see-a-report-on-the-select-report-page-on-a-list-page"></a>Non è possibile visualizzare un report nella pagina Seleziona report in una pagina di elenco

Probabilmente è perché il nome del report non contiene il nome della pagina di elenco. Rimuovere il filtro per ottenere un elenco completo dei report disponibili in Power BI.

## <a name="see-also"></a>Vedi anche

[Business Central e Power BI](admin-powerbi.md)  
[Creazione di report di Power BI per visualizzare i dati di [!INCLUDE [prod_long](includes/prod_long.md)]](across-how-use-financials-data-source-powerbi.md)  
[Componente di integrazione Power BI e panoramica dell'architettura per [!INCLUDE[prod_short](includes/prod_short.md)]](admin-powerbi-overview.md)  
[Utilizzare i dati di [!INCLUDE [prod_short](includes/prod_short.md)] in Power BI](across-working-with-business-central-in-powerbi.md)  
[Power BI per i consumatori](/power-bi/consumer/end-user-consumer)  
[Il "nuovo look" del servizio Power BI](/power-bi/service-new-look)  
[Avvio rapido: connettersi ai dati in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Documentazione di Power BI](/power-bi/)  
[Business Intelligence](bi.md)  
[Preparazione al business](ui-get-ready-business.md)  
[Importazione dei dati aziendali da altri sistemi contabili](across-import-data-configuration-packages.md)  
[Impostazione di [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)] come origine dati di Power Apps](across-how-use-financials-data-source-powerapps.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)] in Power Automate](across-how-use-financials-data-source-flow.md)  




[!INCLUDE[footer-include](includes/footer-banner.md)]
