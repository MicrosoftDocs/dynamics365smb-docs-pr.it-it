---
title: Impostare report da stampare su stampanti specifiche | Documenti Microsoft
description: Informazioni su come specificare una stampante per un report utilizzando la pagina Selezioni stampante.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online printing
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: d027999692323960327e8b34ddb2efaea23c59a8
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2020
ms.locfileid: "3189485"
---
# <a name="set-up-printers"></a>Configurare le stampanti
Poiché [!INCLUDE[prodshort](includes/prodshort.md)] è un servizio cloud, non può raggiungere le stampanti locali collegate ai computer degli utenti. Tuttavia, può connettersi a stampanti abilitate per il cloud. Nella versione generica di [!INCLUDE[prodshort](includes/prodshort.md)], una stampante cloud denominata **Stampante e-mail** è installata come estensione ed è pronta per l'uso dopo l'installazione iniziale.

Se una stampante cloud non è installata e configurata, o se una stampante installata non funziona, la stampa imposterà automaticamente le opzioni di stampa per il browser. Questo è indicato da questo valore nel campo **Stampante** della pagina di richiesta del report: *(nessuno, gestito dal browser)*.

Nella pagina **Gestione stampante**, è possibile visualizzare le stampanti configurate. Dopo aver configurato una o più stampanti, è possibile aprire la pagina **Selezioni stampante** per effettuare la confiugurazione per l'account utente per indicare i report specifici da stampare e con quale stampante.

Quando una stampante viene configurata e assegnata a report specifici, si stampa un report selezionando il pulsante **Stampa** nella pagina di richiesta del report. Per ulteriori informazioni, vedere [Stampa di un report](ui-work-report.md#PrintReport).

## <a name="to-set-up-a-printer"></a>Per configurare una stampante
Nella pagina **Gestione della stampante**, puoi vedere le stampanti che sono state configurate e puoi accedere alla pagina **Impostazioni** per ciascuna stampante per modificare una configurazione esistente o configurare una nuova stampante.

La seguente procedura descrive come configurare l'attuale **Stampante e-mail**, che è un'estensione preinstallata.

> [!NOTE]
> Per utilizzare la stampa e-mail, è necessario configurare la funzionalità e-mail. Per ulteriori informazioni, vedere [Imposta indirizzo e-mail](admin-how-setup-email.md).

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immetti **Gestione stampante**, quindi seleziona il collegamento correlato.
2. Seleziona la riga per la **Stampante e-mail**, quindi selezionare l'azione **Modifica impostazioni stampante**.
3. Compilare i campi nella pagina **Impostazioniì** in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > È necessario selezionare manualmente il formato carta appropriato per una stampante poiché non è possibile memorizzare alcuna stampante locale o impostazioni dell'utente.
    >
    > Assicurarsi che l'estensione Stampante e-mail non sia impostata sul formato carta **A4** per impostazione predefinita, che non è adatto in Nord America, ad esempio.
4. Per impostare una stampante come predefinita, nella pagina **Gestione stampante**, scegli **Imposta come stampante di default personale**.

### <a name="privacy-notice"></a>Informativa sulla privacy
Se si utilizza l'estensione Stampante e-mail, tutti o alcuni lavori di stampa verranno inviati all'indirizzo e-mail fornito durante la configurazione della stampante. Si consiglia vivamente di associare un ID e-mail univoco a un dispositivo stampante utilizzando solo i servizi ufficiali forniti dal produttore dell'hardware, come HP ePrint, KonicaMinolta EveryonePrint o Epson Email Print.

È necessario prendere tutte le precauzioni sulla privacy necessarie, incluso assicurarsi che la soluzione di stampa e-mail abbia le autorizzazioni, le impostazioni sulla privacy e i criteri di conservazione configurati correttamente. È responsabilità dell'utente fornire un indirizzo e-mail corretto, verificato e operativo. Per ulteriori informazioni, vedere [Informativa sulla privacy di Microsoft](https://privacy.microsoft.com/en-us/privacystatement).

## <a name="to-select-which-printers-print-which-reports"></a>Per scegliere quali stampanti devono stampare quali report
Nella pagina **Selezioni stampante**, è possibile impostare per il proprio account utente quali report vengono stampati da quale stampante. Ciò è utile se si lavora con report diversi che richiedono stampanti diverse a causa del loro posizionamento nell'azienda o delle loro capacità di output.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immetti **Selezioni stampante**, quindi seleziona il collegamento correlato. In alternativa, dalla pagina **Gestione stampante**, seleziona una stampante, quindi scegli l'azione **Selezioni stampante**.
2. Scegli l'azione **Nuovo** per aggiungere una selezione di stampanti per un report specifico.
3. Compilare i campi in base alle esigenze.

Il report specificato è ora impostato per la stampa sulla stampante selezionata per impostazione predefinita.

> [!NOTE]
> Quando si stampa il report in questione, è possibile ignorare questa impostazione selezionando un'altra stampante nella pagina **Impostazioni di stampa**.

> [!NOTE]
> Se non si imposta un report per una stampante specifica sulla pagina **Selezioni stampante**, la stampa verrà effettuata sulla stampante predefinita della società, come definito nella pagina **Gestione stampante**.

Tu o l'amministratore potete anche usare la pagina **Selezioni stampante** per definire altre varianti di stampa per utenti e report. Nella seguente tabella viene descritta la combinazione dei valori per specificare diverse configurazioni di stampa per un report.

|A                                                 |Impostare i seguenti valori                                             |
|---------------------------------------------------|---------------------------------------------------------------------|
|Stampare un report su una stampante specifica per tutti gli utenti |Specificare i valori nei campi **Nome stampante** e **ID report** e lasciare vuoto il campo **ID utente**.|
|Stampare tutti i report su una stampante specifica per un utente specifico|Specificare i valori nei campi **ID utente** e **Nome stampante** e lasciare vuoto il campo **ID utente**.|
|Impostare la stampante di default per tutti i report|Specificare un valore nel campo **Nome stampante** e lasciare vuoti i campi **ID utente** e **ID report**.|
|Stampare un report specifico sulla stampante di default dell'utente|Specificare un valore nel campo **ID report** e lasciare vuoti i campi **Nome stampante** e **ID utente**.|
|Stampare un report specifico su una stampante specifica per un utente specifico|Specificare i valori in tutti e tre i campi.|

> [!NOTE]
> Altre selezioni stampante specifiche hanno la precedenza su una selezione stampante generale. Ad esempio, una selezione di stampante che ha valori nei campi **ID utente**, **ID report** e **Nome stampante** ha la precedenza su una selezione di stampante che ha voci vuote nei campi **ID utente** o **ID report**.

## <a name="see-also"></a>Vedere anche
[Stampa di un report](ui-work-report.md#PrintReport)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Eseguire i processi batch](ui-how-run-batch-jobs.md)  
[Inviare documenti via e-mail](ui-how-send-documents-email.md)  
