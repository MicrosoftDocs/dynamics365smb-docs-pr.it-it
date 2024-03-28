---
title: Specificare una stampante predefinita
description: Informazioni sui modi per configurare le stampanti che vengono utilizzate per impostazione predefinita per i lavori di stampa.
author: jswymer
ms.topic: how-to
ms.reviewer: na
ms.service: dynamics-365-business-central
ms.custom: bap-template
ms.search.keywords: 'online printing, email printing, cloud printing, Universal Print'
ms.search.form: '2650, 2750, 2752, 2753, 2754, 8900,'
ms.date: 02/09/2023
ms.author: jswymer
---
# <a name="default"></a>Specificare una stampante predefinita  

Dopo aver configurato le stampanti in Business Central, è possibile specificare quale stampante utilizzare per impostazione predefinita. Esistono due modi per specificare le stampanti che vengono utilizzate per impostazione predefinita per i report e altri lavori di stampa. Una stampante predefinita è utile se si lavora con report diversi che richiedono stampanti diverse a causa del loro posizionamento nell'azienda o delle loro capacità di output.

> [!IMPORTANT]
> Le uniche stampanti che puoi specificare come predefinite sono **Microsoft Print to PDF** e le stampanti cloud che sono già state configurate per l'uso in Business Central, come le stampanti e-mail e le stampanti di Stampa universale. Le stampanti cloud sono in genere configurate da un amministratore. Per ulteriori informazioni, vedi [Configurazione e gestione della stampante](admin-printer-setup-overview.md).   

## Imposta una stampante come stampante predefinita per tutti i lavori di stampa

La pagina **Gestione stampante** ti consente di impostare una stampante come stampante predefinita per tutti i lavori di stampa. Puoi specificare la stampante come predefinita solo per te o per tutti gli utenti.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Gestione stampante**, quindi scegli il collegamento correlato.

    > [!TIP]
    > Puoi anche aprire la pagina **Gestione stampante** dalla pagina **Selezioni della stampante** scegliendo **Gestione stampante**.  
2. Nella pagina **Gestione stampante**, seleziona una stampante dall'elenco, scegli **Gestisci**, quindi scegli **Imposta come stampante di default personale** o **Imposta come stampante predefinita per tutti gli utenti**.

> [!NOTE]
> L'impostazione di una stampante predefinita da **Gestione stampante** aggiunge una voce in **Selezioni della stampante**.

## Imposta una stampante predefinita per report specifici

La pagina **Selezioni della stampante** ti consente di specificare la stampante che un report utilizza per impostazione predefinita. Le stampanti predefinite vengono impostate in base all'account utente. Puoi impostare una stampante predefinita solo per te stesso, per un altro utente o per tutti gli utenti.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Selezioni della stampante**, quindi scegli il collegamento correlato. In alternativa, seleziona una stampante dalla pagina **Gestione stampante**, quindi scegli l'azione **Selezioni stampante**.
2. Scegli l'azione **Nuovo** per aggiungere una selezione di stampanti per un report specifico.
3. Compilare i campi in base alle esigenze.

Il report specificato è ora impostato per la stampa sulla stampante selezionata per impostazione predefinita.

> [!NOTE]
> Quando si stampa il report in questione, puoi selezionarne uno diverso utilizzando il campo **Stampa** nella pagina della richiesta report.

> [!NOTE]
> Se non si imposta un report per una stampante specifica sulla pagina **Selezioni stampante**, la stampa viene effettuata sulla stampante predefinita della società, come definito nella pagina **Gestione stampante**.

Tu o l'amministratore potete anche usare la pagina **Selezioni stampante** per definire altre varianti di stampa per utenti e report. Nella seguente tabella viene descritta la combinazione dei valori per specificare diverse configurazioni di stampa per un report.

|A                                                 |Impostare i seguenti valori                                             |
|---------------------------------------------------|---------------------------------------------------------------------|
|Stampare un report su una stampante specifica per tutti gli utenti |Specificare i valori nei campi **Nome stampante** e **ID report** e lasciare vuoto il campo **ID utente**.|
|Stampare tutti i report su una stampante specifica per un utente specifico|Specificare i valori nei campi **ID utente** e **Nome stampante** e lasciare vuoto il campo **ID utente**. Questa voce ha la stessa funzione di **Imposta come stampante di default personale** nella pagina **Gestione della stampa**.|
|Impostare la stampante di default per tutti gli utenti|Specificare un valore nel campo **Nome stampante** e lasciare vuoti i campi **ID utente** e **ID report**. Questa voce ha la stessa funzione di **Imposta come stampante predefinita per tutti gli utenti** nella pagina **Gestione della stampa**.|
|Stampare un report specifico sulla stampante di default dell'utente|Specificare un valore nel campo **ID report** e lasciare vuoti i campi **Nome stampante** e **ID utente**.|
|Stampare un report specifico su una stampante specifica per un utente specifico|Specificare i valori in tutti e tre i campi.|

> [!NOTE]
> Altre selezioni stampante specifiche hanno la precedenza su una selezione stampante generale. Ad esempio, una selezione di stampante che ha valori nei campi **ID utente**, **ID report** e **Nome stampante** ha la precedenza su una selezione di stampante che ha voci vuote nei campi **ID utente** o **ID report**.

## Scelta della stampante durante l'esecuzione di un report

Invece di utilizzare la stampante predefinita durante l'esecuzione di un report, è possibile ignorare questa impostazione dalla pagina della richiesta. Basta scegliere la stampante che vuoi utilizzare per questa generazione del report nel menu a discesa **Stampante**.

## Ridimensionamento dei lavori di stampa

La stampa cloud è progettata per documenti di dimensioni ragionevoli. La maggior parte dei servizi cloud, inclusi PrintNode e HP ePrint, ha un limite di 10 MB per processo. Se è necessario stampare report più grandi, potrebbe essere necessario dividerli in più stampe.

## Vedere anche

[Gestione stampante](admin-printer-setup-overview.md)  
[Impostare le stampanti di Stampa universale](admin-printer-setup-universal-print.md)  
[Impostare le stampanti con indirizzo e-mail](admin-printer-setup-email.md)  
[Stampa di un report](ui-work-report.md#PrintReport)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Eseguire i processi batch](ui-how-run-batch-jobs.md)  
[Inviare documenti via e-mail](ui-how-send-documents-email.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
