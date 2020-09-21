---
title: Utilizzo dei report Power BI in Business Central | Microsoft Docs
description: Ottenere informazioni dettagliate, business intelligence e KPI a partire dai dati di Business Central è semplice con le app Business Central per Power BI.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 07/10/2020
ms.author: jswymer
ms.openlocfilehash: 7f28e763cd2a72bda79c088c3a1268e3443f86dc
ms.sourcegitcommit: aeaa0dc64e54432a70c4b0e1faf325cd17d01389
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "3697773"
---
# <a name="working-with-power-bi-reports-in-prodshort"></a>Utilizzo dei report Power BI in [!INCLUDE [prodshort](includes/prodshort.md)]

In questo articolo vengono spiegate alcune delle nozioni di base sulla visualizzazione dei report Power BI in [!INCLUDE [prodshort](includes/prodshort.md)].

## <a name="overview"></a>Sintesi

I report Power BI offrono informazioni dettagliate da [!INCLUDE[prodshort](includes/prodshort.md)]. Varie pagine in [!INCLUDE [prodshort](includes/prodshort.md)] includono una parte di un report Power BI che può visualizzare report Power BI. La Gestione ruolo utente è una tipica pagina in cui è visibile una parte di report Power BI. Alcune pagine di elenco, come **Elementi**, includono anche una parte Power BI.

[!INCLUDE [prodshort](includes/prodshort.md)] lavora insieme al servizio Power BI. I report da visualizzare in [!INCLUDE [prodshort](includes/prodshort.md)] sono memorizzati nel servizio Power BI. In [!INCLUDE [prodshort](includes/prodshort.md)], è possibile cambiare il report visualizzato nella parte Power BI di qualsiasi report Power BI disponibile nel servizio Power BI. La prima volta che si accede a [!INCLUDE [prodshort](includes/prodshort.md)] e finché non ci si connette al servizio Power BI le parti saranno vuote, come mostrato qui:

![Parte Power BI in Business Central](./media/power-bi-part.png)

## <a name="prerequisites"></a>Prerequisiti

Se si sta usando [!INCLUDE[prodshort](includes/prodshort.md)] in locale, deve essere abilitato per l'integrazione di Power BI. Questa attività è in genere eseguita da un amministratore. Per ulteriori informazioni, vedere [Impostare [!INCLUDE[prodshort](includes/prodshort.md)] in locale per l'integrazione di Power BI](admin-powerbi-setup.md#setup).

> [!NOTE]
> [!INCLUDE[prodshort](includes/prodshort.md)] online è già impostato per l'integrazione con Power BI.

## <a name="get-ready"></a>Preparazione

Iscriversi al servizio Power BI. Se non si è già registrati andare a [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Quando ci si registra, utilizzare l'indirizzo e-mail e la password di lavoro.

## <a name="connect-to-power-bi---one-time-only"></a>Connettersi a Power BI - una sola volta

Quando si accede per la prima volta a [!INCLUDE [prodshort](includes/prodshort.md)], è possibile vedere una parte Power BI vuota in qualche pagina, come mostrato nella figura precedente. La prima cosa da fare è connettersi all'account Power BI. Una volta connessi, è possibile vedere i report. È necessario eseguire questo passaggio solo una volta.

Per connettersi a Power BI, selezionare il collegamento **Introduzione a Power BI** nella parte **Report Power BI**.

Durante il processo di connessione, [!INCLUDE [prodshort](includes/prodshort.md)] comunica con il servizio Power BI per determinare se si dispone di un account Power BI valido e di una licenza. Dopo la verifica della licenza, il report Power BI predefinito viene visualizzato nella pagina. Se non viene visualizzato un report, è possibile selezionare un report dalla parte.

> [!TIP]
> Con [!INCLUDE [prodshort](includes/prodshort.md)] online, questo passaggio caricherà automaticamente i report Power BI predefiniti utilizzati in [!INCLUDE [prodshort](includes/prodshort.md)] nell'area di lavoro Power BI.

##### <a name="from-prodshort-on-premises"></a>Da [!INCLUDE [prodshort](includes/prodshort.md)] in locale

La connessione a Power BI da [!INCLUDE [prodshort](includes/prodshort.md)] è simile a quella per la soluzione online. Tuttavia, verrà richiesto nella pagina **AUTORIZZAZIONI DI SERVIZIO AZURE ACTIVE DIRECTORY** di concedere l'accesso ai servizi Power BI. Per concedere l'accesso, selezionare **Autorizza i servizi di Azure** e poi **Accetta**.

Una volta connessi è possibile selezionare un report dalla parte Power BI nelle pagine.

## <a name="show-power-bi-reports-on-list-pages"></a>Mostrare i report Power BI sulle pagine di elenco

[!INCLUDE[prodlong](includes/prodlong.md)] include un riquadro Dettaglio informazioni Power BI su diverse pagine elenco chiave. Questo riquadro Dettaglio informazioni fornisce ulteriori informazioni sui dati nell'elenco. Spostandosi tra le righe dell'elenco, il report viene aggiornato e filtrato per la voce selezionata. Se non è visibile questa parte, dalla barra delle azioni selezionare **Azioni** > **Schermo** > **Mostra/Nascondi report Power BI**. Per ulteriori informazioni, vedere [Creazione di report Power BI per la visualizzazione dei dati di elenco in [!INCLUDE[prodshort](includes/prodshort.md)]](across-how-use-powerbi-reports-factbox.md).

## <a name="select-power-bi-reports"></a>Selezionare report Power BI

Una parte Power BI su una pagina può visualizzare qualsiasi report Power BI disponibile. Per passare alla visualizzazione di un altro report, scegliere l'azione **Seleziona report** dall'elenco a discesa dei comandi nella parte superiore della parte.  

La pagina **di selezione dei report Power BI** mostra un elenco di tutti i report Power BI a cui si ha accesso. Questo elenco viene recuperato dall'area di lavoro Power BI. Selezionare la casella **Abilita** per ogni report che si intende visualizzare nella pagina quindi scegliere **OK**. Viene visualizzata di nuovo la pagina con l'ultimo report abilitato. Mediante l'elenco a discesa, utilizzare i comandi **Precedente** e **Successivo** per spostarsi tra i report.  

## <a name="get-reports"></a>Ottenere i report

Se non è visualizzato alcun report nella pagina **di selezione dei report Power BI** o non è visualizzato il report desiderato, scegliere **Ottieni report**. Questa azione consente di cercare i report in due posizioni: *Organizzazione personale* o *Servizi*.

- Scegliere **Organizzazione personale** per andare ai servizi Power BI. Da qui è possibile visualizzare i report all'interno dell'organizzazione per i quali sono stati concessi i diritti di visualizzazione. Quindi è possibile aggiungerli all'area di lavoro.
- Scegliere **Servizi** per passare a Microsoft AppSource dove è possibile installare le app Power BI.  

> [!TIP]
> Se Power BI Desktop è disponibile, è anche possibile creare nuovi report Power BI. Quindi, dopo la pubblicazione di questi report nell'area di lavoro Power BI, visualizzati nella pagina **di selezione dei report Power BI**.  

## <a name="manage-and-modify-reports"></a>Gestire e modificare i report

È possibile apportare modifiche a un report nella parte Power BI. Le modifiche apportate verranno quindi pubblicate nel servizio Power BI. Se il report è condiviso con altri utenti, anche loro vedranno le modifiche, a meno che non si salvano le modifiche in un nuovo report.

Per modificare un report, scegliere l'azione **Gestisci report** dall'elenco a discesa dei comandi nella parte Power BI. Quindi iniziare ad apportare le modifiche. Una volta terminate le modifiche, selezionare **File** > **Salva**. Se si tratta di un report condiviso e non si desidera applicare la modifica per tutti gli utenti, selezionare **Salva come** per evitare di applicare questa modifica a tutti gli utenti.

Quando si ritorna a Gestione ruolo utente, il report aggiornato verrà visualizzato. Se è stato usato **Salva come**, è necessario scegliere **Seleziona report**, quindi abilitare il nuovo report per visualizzarlo.

> [!NOTE]
> Questa funzionalità non è disponibile con [!INCLUDE [prodshort](includes/prodshort.md)] locale.

## <a name="upload-reports"></a><a name="upload"></a>Caricare i report

I report Power BI possono essere distribuiti tra gli utenti come file .pbix. Se sono disponibili file .pbix, è possibile caricarli e condividerli con tutti gli utenti di [!INCLUDE [prodshort](includes/prodshort.md)]. I report sono condivisi in ogni società in [!INCLUDE [prodshort](includes/prodshort.md)].  

Per caricare un report, selezionare l'azione **Carica report** dall'elenco a discesa dei comandi nella parte **Report Power BI**. Quindi individuare il file .pbix che definisce i report che si desidera condividere. È possibile modificare il nome predefinito del file.  

Dopo che il report è stato caricato nell'area di lavoro Power BI viene automaticamente caricato nelle aree di lavoro Power BI degli altri utenti.

> [!NOTE]
> Il caricamento di un report richiede privilegi avanzati in [!INCLUDE[prodshort](includes/prodshort.md)]. Inoltre, non è possibile caricare report con [!INCLUDE [prodshort](includes/prodshort.md)] locale. Con la soluzione locale i report vengono caricati direttamente nell'area di lavoro Power BI. Per ulteriori informazioni, vedere [Utilizzo dei dati di [!INCLUDE [prodshort](includes/prodshort.md)] in Power BI](across-working-with-business-central-in-powerbi.md).

## <a name="fixing-problems"></a>Risolvere i problemi

Tuttavia, se si verifica un errore, in questa sezione viene fornita una soluzione alternativa per i problemi più comuni.  

### <a name="you-dont-have-a-power-bi-account"></a>Non si dispone di un account Power BI

Un account Power BI non è stato impostato. Per ottenere un account Power BI valido, è necessario avere una licenza e aver effettuato l'accesso a Power BI in precedenza per creare un'area di lavoro Power BI.   

### <a name="message-there-are-no-enabled-reports-choose-select-report-to-see-a-list-of-reports-that-you-can-display"></a>Messaggio: Non sono presenti report abilitati. Scegliere Seleziona report per visualizzare un elenco di report che è possibile visualizzare.

Questo messaggio viene visualizzato se la distribuzione del report predefinito non è riuscita nell'area di lavoro Power BI. In alternativa il report è stato distribuito ma non è stato aggiornato correttamente. Accedere al report nella propria area di lavoro Power BI, selezionare **Set di dati**, **Impostazioni** e quindi aggiornare manualmente le credenziali. Dopo aver aggiornato correttamente il set di dati, tornare a [!INCLUDE[prodshort](includes/prodshort.md)] e selezionare manualmente il report dalla pagina **Selezionare i report**.


## <a name="see-related-training-at-microsoft-learn"></a>Vedere le informazioni relative al training in [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Vedere anche

[Business Central e Power BI](admin-powerbi.md)  
[Creazione di report di Power BI per visualizzare i dati di [!INCLUDE [prodlong](includes/prodlong.md)]](across-how-use-financials-data-source-powerbi.md)  
[Componente di integrazione Power BI e panoramica dell'architettura per [!INCLUDE[prodshort](includes/prodshort.md)]](admin-powerbi-overview.md)  
[Utilizzo di dati di [!INCLUDE [prodshort](includes/prodshort.md)] in Power BI](across-working-with-business-central-in-powerbi.md)  
[Power BI per i consumatori](/power-bi/consumer/end-user-consumer)  
[Il "nuovo look" del servizio Power BI](/power-bi/service-new-look)  
[Avvio rapido: connettersi ai dati in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Documentazione di Power BI](/power-bi/)  
[Business Intelligence](bi.md)  
[Introduzione](product-get-started.md)  
[Importazione dei dati aziendali da altri sistemi contabili](across-import-data-configuration-packages.md)  
[Impostazione di [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Uso di [!INCLUDE[d365fin](includes/d365fin_md.md)] come origine dati di Power BI](across-how-use-financials-data-source-powerbi.md)  
[Uso di [!INCLUDE[d365fin](includes/d365fin_md.md)] come origine dati di Power Apps](across-how-use-financials-data-source-powerapps.md)  
[Uso di [!INCLUDE[d365fin](includes/d365fin_md.md)] in Power Automate](across-how-use-financials-data-source-flow.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
