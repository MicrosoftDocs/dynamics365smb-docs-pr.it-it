---
title: Ottenere il componente aggiuntivo Business Central per Excel
description: Scopri come ottenere per gli utenti l'add-in di Business Central per Excel.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.search.form: 1480
ms.search.keywords: 'Excel, add-in, centralized deployment, M365 admin center, individual acquisition, appsource'
ms.date: 10/07/2021
ms.author: jswymer
---
# <a name="get-the-business-central-add-in-for-excel" />Ottieni il Business Central Add-in per Excel

[!INCLUDE[prod_short](includes/prod_short.md)] include un add-in per Excel che permette agli utenti di selezionare un'azione **Modifica in Excel** su certe pagine per aprire i dati in un foglio di lavoro Excel. Questa azione è diversa dall'azione **Apri in Excel** perché consente agli utenti di apportare modifiche in Excel, quindi di ripubblicare le modifiche in [!INCLUDE[prod_short](includes/prod_short.md)]

## <a name="overview" />Sintesi

### <a name="about-the-add-in" />Informazioni sull'add-in

L'add-in si chiama **Add-in Microsoft Dynamics per Office** ed è disponibile per l'installazione su [Office Store (AppSource)](https://appsource.microsoft.com/). Con l'add-in installato, l'azione **Modifica in Excel** è disponibile nella maggior parte delle pagine dell'elenco e delle parti dell'elenco dall'icona **Condividi**  ![Condividi una pagina in un'altra app.](media/share-icon.png). Per ulteriori informazioni sull'uso dell'add-in, vedi [Visualizzazione e modifica in Excel da Business Central](across-work-with-excel.md).

> [!NOTE]
> L'add-in funziona solo su Windows; non su macOS.

### <a name="about-deployment-as-an-admin" />Riguardo all'impiego come amministratore

Con [!INCLUDE[prod_short](includes/prod_short.md)] online, ci sono alcune opzioni di distribuzione per portare l'add-in agli utenti. Un'opzione è l' *acquisizione individuale*, dove si lascia che gli utenti installino il componente aggiuntivo da soli. Con questa opzione, gli utenti devono avere accesso al download di file da Office Store. Un'altra opzione è quella di impostare la *distribuzione centralizzata* nell'interfaccia di amministrazione di Microsoft 365 per distribuire automaticamente l'add-in all'intera organizzazione, a gruppi o a utenti specifici. La distribuzione centralizzata fornisce un modo per ottenere l'add-in agli utenti se la tua organizzazione non dà agli utenti l'accesso a Office Store.

Per l'utente finale, l'esperienza di installazione è diversa per i due scenari di distribuzione:

- Con l'acquisizione individuale, la prima volta che gli utenti scelgono l'azione **Modifica in Excel**, il riquadro **Nuovo add-in per Office** si apre in Excel. Per installare l'add-in, l'utente sceglie **Considera questo add-in affidabile**, che a sua volta installa l'add-in direttamente da Office Store. Gli utenti accedono poi a [!INCLUDE[prod_short](includes/prod_short.md)] usando il loro nome utente e la loro password.

- Con la distribuzione centralizzata, la prima volta che gli utenti scelgono l'azione **Modifica in Excel**, il componente aggiuntivo viene automaticamente installato in Excel dalla distribuzione centralizzata; non da Office Store. L'unica cosa che gli utenti devono fare è accedere a [!INCLUDE[prod_short](includes/prod_short.md)]

Con entrambe queste opzioni di distribuzione, il componente aggiuntivo viene configurato automaticamente per connettersi a [!INCLUDE[prod_short](includes/prod_short.md)]. Una terza opzione di distribuzione è un'installazione manuale del componente aggiuntivo direttamente da Excel. Con questa opzione, gli utenti dovranno configurare il componente aggiuntivo a cui connettersi [!INCLUDE[prod_short](includes/prod_short.md)]

### <a name="a-nameswitchaswitching-from-individual-acquisition-to-centralized-deployment-or-the-other-way-around" /><a name="switch"></a>Passare dall'acquisizione individuale alla distribuzione centralizzata o viceversa

Quando si passa dall'acquisizione individuale del componente aggiuntivo alla distribuzione centralizzata, o viceversa, i file Excel che gli utenti hanno creato prima della transizione sono interessati. Dopo la transizione, gli utenti possono ancora aprire qualsiasi foglio di lavoro Excel precedentemente creato utilizzando l'azione **Modifica in Excel** o creato manualmente configurando l'add-in Excel. Ma non possono aggiornare i dati nel file da Business Central o spingere gli aggiornamenti a Business Central

Questa condizione è causata dal fatto che ad ogni file Excel viene assegnato un identificatore "add-in". Nella transizione da o verso la distribuzione centralizzata, viene assegnato un ID diverso, quindi l'ID precedente diventa bloccato.

## <a name="preparation-on-premises-only" />Preparazione (solo in sede)

[!INCLUDE[prod_short](includes/prod_short.md)] on-premises richiede che il tuo ambiente sia configurato per l'add-in. In caso contrario, l'azione **Modifica in Excel** non sarà disponibile per gli utenti. Per maggiori informazioni, vedi [Impostazione dell'add-in di Excel per la modifica dei dati di Business Central](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin) nella guida di Developer e IT Pro.

## <a name="deploy-the-add-in-by-using-centralized-deployment" />Distribuire il componente aggiuntivo utilizzando la distribuzione centralizzata

La distribuzione centralizzata è una funzione nell'interfaccia di amministrazione di Microsoft 365 che si usa per installare automaticamente i componenti aggiuntivi nelle applicazioni Office degli utenti, come Excel. Per aiutarvi con la distribuzione centralizzata, [!INCLUDE[prod_short](includes/prod_short.md)] include la configurazione assistita di **Distribuzione centralizzata Add-in Excel** .

### <a name="before-you-begin" />Prima di iniziare

- Per sapere come impedire agli utenti di scaricare dal negozio di Office, vedi [Gestire i componenti aggiuntivi nel centro amministrativo](/microsoft-365/admin/manage/manage-addins-in-the-admin-center).
- Verificate che la distribuzione centralizzata funzioni per la vostra organizzazione. Per ulteriori informazioni, vedere [Determinare se la distribuzione centralizzata degli add-in funziona per la propria organizzazione](/microsoft-365/admin/manage/centralized-deployment-of-add-ins)
- Se stai passando dall'acquisizione individuale, vedi [Passaggio dall'acquisizione individuale alla distribuzione centralizzata](#switch)

> [!NOTE]
> L'abilitazione della distribuzione centralizzata influisce sulle funzioni che usano il componente aggiuntivo di Excel, come l'azione **Modifica in Excel** . Non ha alcun effetto su altre funzionalità relative a Excel e/o sulle autorizzazioni assegnate agli utenti in [!INCLUDE[prod_short](includes/prod_short.md)]

### <a name="set-up-centralized-deployment-of-the-add-in" />Impostare la distribuzione centralizzata dell'add-in

Lavorerai sia in [!INCLUDE[prod_short](includes/prod_short.md)] sia nell'interfaccia di amministrazione di Microsoft 365.

1. In [!INCLUDE[prod_short](includes/prod_short.md)], scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") , immetti **Distribuzione centralizzata Add-in Excel**, quindi scegli il collegamento correlato.
2. Leggi le informazioni sulla pagina **d'impostazione dell'add-in di Business Central Excel** e scegli **Avanti**.
3. Accedi all'[interfaccia di amministrazione di Microsoft 365](https://go.microsoft.com/fwlink/?linkid=2163967), quindi vai ad **App integrate**<!--**Add-ins**-->.

    Completa i seguenti passi per configurare il componente aggiuntivo da distribuire da Office Store: 
    1. Scegliere **Scarica app** per aprire Office Store (AppSource). <!--**Deploy Add-in** 5. In the **Deploy a new add-in**, select **Choose from the store**.-->
    2. Cerca **Add-in di Microsoft Dynamics per Office**, poi seleziona **Scaricalo ora**. <!--On the **Select add-in** page, search for and select **Microsoft Dynamics Office Add-in** > **Add** > **Continue**.-->
    3. Nella pagina **Aggiungi utenti**, specifica gli utenti per i quali vuoi distribuire l'add-in, quindi scegli **Avanti**.<!--On the **Configure add-in**, specify the users that you want to deploy the add-in for.-->
    4. Esaminare le **richieste di autorizzazioni accettate**, quindi scegliere **Avanti** > **Termina distribuzione**.
    5. Attendere che il segno di spunta verde accanto a **Distribuito** appaia per l'add-in, quindi scegliere **Fatto**. <!--Select **Deploy** and wait til successful, then **Next** > **Continue**.-->

       L'add-in appare nella pagina **Add-in** . Per ulteriori informazioni sulla distribuzione dei componenti aggiuntivi nell'interfaccia di amministrazione di Microsoft 365, vedi [Distribuire i componenti aggiuntivi nell'interfaccia di amministrazione](/power-platform/admin/use-service-admin-role-manage-tenant?azure-portal=true).
4. Torna al setup assistito **Distribuzione centralizzata di componenti aggiuntivi per Excel** in [!INCLUDE[prod_short](includes/prod_short.md)], e scegli **Avanti**.
5. Attivare **Usa distribuzione centralizzata** e scegliere **Fine**.

    Se non si attiva questo interruttore, [!INCLUDE[prod_short](includes/prod_short.md)] otterrà l'add-in direttamente da Office Store.

Quando hai finito, puoi sempre cambiare la distribuzione nell'interfaccia di amministrazione di Microsoft 365, come assegnare più utenti. Per ulteriori informazioni sulla distribuzione dei componenti aggiuntivi nel centro amministrativo, vedi [Distribuzione di componenti aggiuntivi nel centro amministrativo](/power-platform/admin/use-service-admin-role-manage-tenant?azure-portal=true).

> [!IMPORTANT]
> Se hai più di un ambiente, devi eseguire l'installazione assistita di **Distribuzione centralizzata Add-in Excel** su ogni ambiente che vuoi usare la distribuzione centralizzata. Tuttavia, non è necessario configurare nuovamente la distribuzione centralizzata in Microsoft 365. L'unica cosa che devi fare è attivare l'interruttore **Usa distribuzione centralizzata** nella configurazione assistita. 

> [!NOTE]
> Può richiedere fino a 24 ore prima che gli utenti l'add-in distribuisce automaticamente in Excel di utenti.

## <a name="a-nameinstallaindividual-acquisition-install-the-add-in-manually-for-your-own-use" /><a name="install"></a>Acquisizione individuale: Installare manualmente l'add-in per uso personale

Nella maggior parte dei casi, quando aprirai Excel da Business Central, l'add-in verrà installato automaticamente per te o ti verrà richiesto di installarlo. Ci potrebbero essere casi, tuttavia, in cui è necessario installare manualmente l'add-in.

1. Aprire Excel, poi aprire una qualsiasi cartella di lavoro Excel.
2. Nel menu **Insert**, scegli **Add-ins** > **Get add-ins**
3. Vai su **Gestito da amministratore** e cerca **Add-in di Microsoft Dynamics per Office.** Se lo vedi, selezionalo e poi scegli **Aggiungi**. Se non lo vedi, vai su **Store**, poi cerca *Add-in di Microsoft Dynamics per Office* e segui le istruzioni sullo schermo per aggiungerlo.

Quando l'add-in è installato, si presenta come un pannello in Excel. Successivamente, configurate la connessione.

### <a name="configure-the-business-central-connection" />Configurare la connessione a Business Central

Se un utente non può connettersi automaticamente, puoi sbloccarlo chiedendogli di seguire questi passi:

1. Nel **Microsoft Dynamics** pannello add-in in Excel, scegli **Aggiungi informazioni server**. Se non lo vedi, scegli il pulsante ![More in Excel.](media/cogwheel.png) in alto per aprire la finestra di dialogo delle opzioni. 
2. Per [!INCLUDE[prod_short](includes/prod_short.md)] online, impostare l'**URL del server** su `https://exceladdinprovider.smb.dynamics.com`. Per [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, impostare l'URL del client web, come `https://myBCserver/190`.
3. scegli **OK**, e poi confermate che l'app si ricarica.
4. Quando ti viene richiesto, accedi con il tuo nome utente e la password di Business Central.
5. Opzionalmente, scegli l'ambiente e l'azienda a cui volete connettervi.

Il componente aggiuntivo è ora connesso a [!INCLUDE [prod_short](includes/prod_short.md)], e puoi modificare i dati e pubblicare le modifiche su [!INCLUDE [prod_short](includes/prod_short.md)].  

## <a name="prepare-devices-and-network-for-the-excel-add-in" />Preparare i dispositivi e la rete per l'Add-In di Excel

I servizi di rete come i proxy o i firewall devono permettere il routing tra ogni dispositivo client su cui è installato il componente aggiuntivo e molti endpoint di servizio. Per un elenco di endpoint, vedi [Preparare la tua rete per l'Add-In Excel](/dynamics365/business-central/dev-itpro/administration/configuring-network-for-addins).

## <a name="troubleshooting" />Troubleshooting

A volte, gli utenti incontrano problemi con l'add-in di Excel. Questa sezione fornisce alcuni suggerimenti su come sbloccare gli utenti in determinate circostanze.

|Problema  |Soluzione o soluzione alternativa  |Commenti  |
|---------|---------|---------|
|L'add-in non si avvia <br><br>Ad esempio, l'utente riceve il messaggio "Avviso del componente aggiuntivo: questo componente aggiuntivo non è più disponibile." quando tenta di utilizzare il componente aggiuntivo. Questo particolare problema può verificarsi se la distribuzione centralizzata è configurata correttamente, ma all'utente non è stato assegnato l'accesso.|Controlla se l'add-in è distribuito centralmente. Oppure, controlla se l'utente è bloccato dall'installazione locale. | L'amministratore può configurare Office in modo che gli utenti non possano acquisire add-in. In questi casi, l'amministratore deve distribuire l'add-in a livello centrale. Per maggiori informazioni, vedere [Distribuire i componenti aggiuntivi nel centro amministrativo](/microsoft-365/admin/manage/manage-deployment-of-add-ins?view=o365-worldwide&preserve-view=true).|
|I dati non vengono caricati in Excel|Prova la connessione aprendo un altro elenco in Excel da [!INCLUDE [prod_short](includes/prod_short.md)]. Oppure, apri la cartella di lavoro di Excel in un browser.|Se l'utente ha specificato un nome di società che contiene caratteri speciali, l'add-in non può connettersi. |
|I dati non possono essere ripubblicati su [!INCLUDE [prod_short](includes/prod_short.md)].|Testate la connessione aprendo la cartella di lavoro di Excel in un browser. |A volte un'estensione può bloccare il lavoro di pubblicazione. Se la pagina è estesa o personalizzata, rimuovi le estensioni e poi riprova.|
|Le date sono sbagliate  |Excel potrebbe mostrare orari e date in un formato diverso da [!INCLUDE [prod_short](includes/prod_short.md)]. Questa condizione non li rende sbagliati e i dati in [!INCLUDE [prod_short](includes/prod_short.md)] non saranno in confusione.|         |
|Per alcune pagine di elenco, la modifica di più righe in Excel causa costantemente degli errori. Questa condizione può verificarsi se le chiamate OData includono FlowFields e campi al di fuori del controllo del ripetitore.|Nella pagina **Servizi Web**, seleziona le caselle di controllo **Escludi i campi di flusso non modificabili** ed **Escludi campi fuori dal ripetitore** per la pagina pubblicata. Selezionando queste caselle di controllo si escludono i FlowFields e i campi non editabili dal calcolo dell'eTag. |Queste caselle di controllo sono nascoste per impostazione predefinita. Per mostrarli nella pagina dei **servizi web**, usa la [personalizzazione](/dynamics365/business-central/ui-personalization-user). |
|Gli utenti non possono più accedere al componente aggiuntivo. Quando tentano di accedere, il processo si interrompe senza essere completato.| Questo problema potrebbe essere causato da un aggiornamento che abbiamo apportato al componente aggiuntivo, nel luglio 2022. Per ulteriori informazioni e una correzione, vedi [Modificare la configurazione del componente aggiuntivo di Excel per supportare l'aggiornamento di luglio 2022](/dynamics365/business-central/dev-itpro/administration/update-excel-addin-configuration).|Si applica solo a [!INCLUDE [prod_short](includes/prod_short.md)] locale|

<!--
## <a name="deploy-the-excel-add-in-for-business-central-online" />Deploy the Excel add-in for Business Central online

For [!INCLUDE [prod_short](includes/prod_short.md)] online, the administrator can deploy the add-in for all users. But users can also install the add-in themselves, provided they have permission to configure their Office experience.  

> [!TIP]
> In some organizations, administrators cannot deploy add-ins centrally. For more information, see [Determine if Centralized Deployment of add-ins works for your organization](/microsoft-365/admin/manage/centralized-deployment-of-add-ins?view=o365-worldwide&preserve-view=true).

### <a name="to-deploy-the-excel-add-in-for-all-users" />To deploy the Excel add-in for all users

1. As the administrator, sign in to the Microsoft commercial website and find the add-in at [https://appsource.microsoft.com/product/office/WA104379629](https://appsource.microsoft.com/product/office/WA104379629).
2. Choose the **Get it now** button.

    You'll be redirected to the Microsoft 365 admin center.
3. In the left panel, go to **Settings**, and then choose **Add-ins**.
4. In the **Configure add-in** pane, specify which users to grant access to the add-in.
5. Save your changes.


### <a name="to-add-the-excel-add-in-locally" />To add the Excel add-in locally

1. Open Excel, and then open any Excel workbook.
2. On the **Insert** menu, choose **Office Add-ins**, and then choose **Admin managed** or **Store** as appropriate.
3. Search for *Dynamics Office Add-In*, and then install the add-in.

When the add-in is installed, it shows up as a panel in Excel. Next, you must configure the connection.

> [!TIP]
> If the workbook is not automatically saved to the user's OneDrive, then recommend them to save all workbooks that they export from [!INCLUDE [prod_short](includes/prod_short.md)].When they open the workbook again, the connection is still available, so they do not have to configure the connection again.

> [!NOTE]
> In certain deployments, the administrator must configure network access to unblock the Excel add-in. For more information, see [Preparing Your Network for the Excel Add-In](configuring-network-for-addins.md).-->

## <a name="see-related-microsoft-trainingtrainingmodulesconfigure-powerbi-excel-dynamics-365-business-centralindex" />Vedi il relativo [training Microsoft](/training/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also" />Vedi anche

[Analisi dei rendiconti finanziari in Microsoft Excel](finance-analyze-excel.md)  
[Utilizzare Business Central](ui-work-product.md)  
[Miglioramenti all'integrazione di Excel nella seconda ondata di rilascio del 2019](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
