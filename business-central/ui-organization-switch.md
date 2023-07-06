---
title: Passare a un'altra società o ambiente
description: 'Se si lavora per più organizzazioni, è possibile passare rapidamente tra ambienti e società.'
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'environments, companies, tenants, organization'
ms.search.form: '9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
ms.date: 08/16/2022
ms.author: bholtorf
---

# <a name="switching-to-another-company-or-environment"></a><a name="switching-to-another-company-or-environment"></a><a name="switching-to-another-company-or-environment"></a>Passare a un'altra società o ambiente

[!INCLUDE [prod_short](includes/prod_short.md)] è disponibile in molti paesi diversi e supporta molti tipi diversi di organizzazioni. La tua organizzazione può scegliere di organizzare il lavoro in [!INCLUDE [prod_short](includes/prod_short.md)] in più *società* e *ambienti*. Questo articolo ti aiuta a comprendere le differenze principali e come risolverle.

## <a name="about-companies-and-environments"></a><a name="about-companies-and-environments"></a><a name="about-companies-and-environments"></a>Informazioni su società e ambienti

[!INCLUDE [company_environment](includes/company_environment.md)]

> [!TIP]
> Se si passa spesso da una società all'altra o si lavora con [!INCLUDE[prod_short](includes/prod_short.md)] dall'interno di un'altra app, ad esempio Microsoft Teams, può essere facile perdere la cognizione di dove ci si trova. Per sapere dove ci si trova, è possibile aggiungere un badge che visualizzerà il nome della società, in modo da poter verificare rapidamente di essere nel posto giusto. Per ulteriori informazioni, vedi [Visualizzare un badge società](admin-company-information.md#badge).
> 
> A seconda del tuo browser, puoi anche aggiungere le diverse società alla barra dei preferiti.  

<!--
[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]-->

## <a name="features-for-switching-company-or-environment"></a><a name="features-for-switching-company-or-environment"></a><a name="features-for-switching-company-or-environment"></a>Funzionalità per passare a una società o un ambiente diverso

Ci sono alcune funzionalità che puoi utilizzare per cambiare società o ambiente mentre lavori. La tabella seguente confronta le capacità della funzione, che sono spiegate più dettagliatamente nelle sezioni seguenti.

|Funzionalità|Cambia società|Cambia ambiente|Passa alla nuova scheda del browser| Disponibile in locale|
|-------|--------------|------------------|-------------------------|----------------------|
|[Selettore di società](#use-the-company-switcher)|![segno di spunta](media/check.png "selezionato")|![segno di spunta](media/check.png "selezionato")|![segno di spunta](media/check.png "selezionato")|![segno di spunta](media/check.png "selezionato")|
|[Utilità di avvio app](#use-the-app-launcher)||![segno di spunta](media/check.png "selezionato")|![segno di spunta](media/check.png "selezionato")||
|[Impostazioni personali](#use-my-settings)|![segno di spunta](media/check.png "selezionato")|||![segno di spunta](media/check.png "selezionato")|
|[Hub aziendale](#use-company-hub)|![segno di spunta](media/check.png "selezionato")|![segno di spunta](media/check.png "selezionato")|![segno di spunta](media/check.png "selezionato")||

## <a name="use-the-company-switcher"></a><a name="use-the-company-switcher"></a><a name="use-the-company-switcher"></a>Usa il selettore di società

L'utilizzo del selettore di società è probabilmente il modo più rapido e versatile per cambiare società. Il selettore di società è un riquadro immediatamente disponibile da qualsiasi pagina. Il riquadro offre una panoramica di tutte le società in tutti gli ambienti a cui hai accesso e ti consente di passare direttamente a una qualsiasi di esse, nella stessa scheda del browser o in una nuova. È particolarmente utile quando lavori in molte società in ambienti diversi.

1. Nell'angolo in alto a destra, vicino all'icona di ricerca, vedrai l'icona della società standard, come ![icona di avvio della società.](media/ui-experience/company-icon.png "Visualizza l'icona del selettore società utilizzata quando è presente un unico ambiente") e ![company-icon-mult-env](media/ui-experience/company-icon-multi-env.png "Visualizza l'icona del selettore società utilizzata quando sono presenti più ambienti"), o un [badge personalizzato](admin-company-information.md#badge) per la società con cui lavori attualmente. Selezionare l'icona per aprire il riquadro del selettore società.

   :::image type="content" source="media/ui-experience/company-switch-2.png" alt-text="Mostra l'icona del selettore società nell'intestazione del client Business Central.":::  

   > [!TIP]
   > Puoi anche usare i tasti di scelta rapida <kbd>Crtl</kbd>+<kbd>O</kbd> per aprire il riquadro.
2. Nel riquadro **Società disponibili** seleziona la società a cui vuoi passare, seleziona la freccia **Passa**, quindi scegli una delle seguenti opzioni:

   |Opzione|Descrizione|
   |------|-----------|
   |Passa|Apre la gestione ruoli utente per la società selezionata nella stessa scheda del browser in cui stai lavorando. La società diventa la società predefinita che si apre in Business Central, finché non si cambia nuovamente o si cambia società utilizzando **Impostazioni personali**. |
   |Apri in una nuova scheda|Apre la gestione ruoli utente per la società selezionata in una nuova scheda del browser, mantenendo aperta la società originale nell'altra scheda.|
   |Apri in una nuova scheda e vai alla stessa pagina|Questa opzione è attiva solo nelle pagine elenco, come clienti, ordini cliente o articoli. Apre lo stesso elenco, ma per la società selezionata, in una nuova scheda del browser. |

> [!TIP]
> Premi <kbd>F5</kbd> per aggiornare l'elenco di ambienti e società.

## <a name="use-the-app-launcher"></a><a name="use-the-app-launcher"></a><a name="use-the-app-launcher"></a>Usare l'icona di avvio delle app

Quando hai effettuato l'accesso a [!INCLUDE[prod_short](includes/prod_short.md)], gli ambienti a cui puoi accedere sono disponibili su Office.com.  

1. Seleziona l'icona **Avvio delle app** ![Icona di avvio delle app.](media/app-launcher-icon.png "L'avvio delle applicazioni fornisce l'accesso a più funzionalità")
2. Nel riquadro che si apre, cerca e scegli [!INCLUDE[prod_short](includes/prod_short.md)]. Se non visualizzi [!INCLUDE[prod_short](includes/prod_short.md)], scegli **Tutte le app**, quindi immetti **Business Central** nella casella **Ricerca**.

   :::image type="content" source="media/app-launcher-bc-tile.png" alt-text="Avvio delle applicazioni di Microsoft 365 che mostra il riquadro Business Central.":::  

3. Se c'è più di un ambiente, ti verrà chiesto di scegliere l'ambiente a cui accedere.

<!--
The following image shows tiles for accessing production and sandbox environments on the Dynamics 365 Home page.

:::image type="content" source="media/app-picker-environments.png" alt-text="The Dynamics 365 Home page showing production and sandbox environments.":::
-->
## <a name="use-my-settings"></a><a name="use-my-settings"></a><a name="use-my-settings"></a>Usare le Impostazioni personali

Quando accedi a [!INCLUDE[prod_short](includes/prod_short.md)], puoi passare rapidamente a un'altra società nello stesso ambiente. Dopo aver effettuato il passaggio, la società scelta diventa la società predefinita e verrà aperta al successivo accesso.

1. Nell'angolo superiore destro scegli l'icona **Impostazioni** ![Impostazioni.](media/ui-experience/settings_icon_small.png "Icona Impostazioni per Gestione ruolo utente"), quindi scegli l'azione **Impostazioni personali**.

    > [!TIP]
    > È possibile anche usare la scelta rapida da tastiera <kbd>Alt</kbd>+<kbd>T</kbd> per aprire rapidamente la pagina delle impostazioni personali.

2. Nella pagina **Impostazioni personali** selezionare la società nel campo **Società**.  
3. Scegliere il pulsante **OK**.

> [!TIP]
> Un buon modo per andare direttamente alla società predefinita al momento dell'accesso ed evitare di specificare un ambiente è aggiungere l'URL all'elenco dei preferiti dopo aver effettuato l'accesso.

## <a name="use-company-hub"></a><a name="use-company-hub"></a><a name="use-company-hub"></a>Usare l'hub aziendale

L'*hub aziendale* è una gestione ruoli utente altamente specializzata che offre una panoramica finanziaria di società e ambienti. Disponibile come [estensione](ui-extensions-company-hub.md), l'hub aziendale fornisce un dashboard con dati di riepilogo per ciascuna società a cui hai accesso. La home page mostra i KPI finanziari e un collegamento diretto ai singoli ambienti e alle aziende. Per ulteriori informazioni, vedere [Gestire il lavoro tra più aziende nell'hub aziendale](company-hub.md).

[![Mostra la pagina dell'hub aziendale che elenca tutte le società.](media/company-hub.png)](media/company-hub.png#lightbox)  

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Vedere anche

[Creazione di nuove società in [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md)  
[Modificare le impostazioni di base](ui-change-basic-settings.md)  
[Ambienti e società (solo in inglese)](/dynamics365/business-central/dev-itpro/administration/tenant-environment-topology)  
[Informazioni società](admin-company-information.md)  
[Interfaccia di amministrazione di Business Central](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
