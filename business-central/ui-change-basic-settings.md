---
title: Modifica le impostazioni di base per l'utente corrente
description: 'Scopri come modificare alcune impostazioni di base in Business Central, ad esempio il ruolo e la gestione ruolo utente, l''azienda, la data di lavoro e il fuso orario.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'change Role Center, notification, change company, change work date, decimal separator'
ms.search.form: '9022, 9019, 9027, 9020, 9026, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
ms.date: 08/31/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Modificare le impostazioni di base

Nella pagina **Impostazioni personali** è possibile vedere e modificare le impostazioni di base per [!INCLUDE[prod_short](includes/prod_short.md)]. Le modifiche apportate interesseranno solo la propria area di lavoro, non quella di altri utenti.  

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

## Ruolo <a name="role-center"></a>

Il ruolo determina la home page, una schermata iniziale che è progettata per le esigenze di un ruolo specifico dell'organizzazione. A seconda del ruolo, la home page o la Gestione ruolo utente offre una panoramica del business, del reparto o dei task personali. Agevola anche l'esplorazione dei task quotidiane e la ricerca del lavoro assegnato.

* Nella parte superiore, lo spostamento consente di esplorare clienti, fornitori, articoli e altri importanti elenchi di informazioni. In modo simile, le azioni consentono di avviare task, come creare una nuova fattura di vendita, direttamente dalla home page.

* In Gestione ruolo utente, è presente l'area **Attività** che mostra i dati correnti e che può essere selezionata per visualizzare informazioni più dettagliate. È possibile impostare Indicatori delle prestazioni chiave (KPI) in modo da visualizzare un grafico selezionato per una rappresentazione visiva di, ad esempio, flussi di cassa o spese e ricavi. È inoltre possibile creare una lista di Clienti preferiti nella home page per gli account aziendali con cui si intrattengono affari spesso o a cui è importante prestare un'attenzione speciale.

### Modificare il ruolo

Il ruolo predefinito è **Manager aziendale**, ma è possibile selezionare un altro ruolo per utilizzare una gestione ruolo utente più adatta alle proprie esigenze.  

1. Nell'angolo superiore destro scegli l'icona **Impostazioni** ![Impostazioni.](media/ui-experience/settings_icon_small.png "Icona Impostazioni per Gestione ruolo utente"), quindi scegli l'azione **Impostazioni personali**.
2. Nella pagina **Impostazioni personali** nel campo **Ruolo** selezionare il ruolo che si desidera utilizzare per impostazione predefinita. Ad esempio, selezionare **Contabile**.
3. Selezionare **OK**.

## <a name="company"></a>Società

Una società funziona da contenitore dei dati in [!INCLUDE[prod_short](includes/prod_short.md)]. Possono essere presenti più società in un database, ma è possibile selezionarne solo una alla volta. La società di default è detta CRONUS e contiene solo i dati di esempio.

Il campo **Società** mostra la società in cui lavori attualmente e puoi usarlo per passare a un'altra società. Il nome della società viene sempre visualizzato nell'angolo in alto a sinistra e funziona come un'azione che è possibile scegliere per tornare a Gestione ruolo utente.

> [!TIP]
> È inoltre possibile modificare la società utilizzando il selettore di società (CTRL+O). Per ulteriori informazioni su questa funzionalità e altri modi per cambiare società o ambiente, vedi [Passaggio a un'altra società o ambiente](ui-organization-switch.md).

La società di default è detta CRONUS e contiene solo i dati di esempio. È possibile creare una nuova società con dati personalizzati. Per ulteriori informazioni, vedere [Creazione di nuove società](about-new-company.md).

<!--
### To change the company name

The company name is always displayed at the top left corner and works as an action that you can choose to go back to the Role Center. You can change this name on the **Company Information** page.

1. Choose the ![Sprocket icon to open the Settings menu.](media/ui-experience/settings_icon_small.png) icon, and then choose the **Company Information** action.
2. In the **Name** field, enter the new company name.
3. Leave the page. The system restarts and displays the new company in the top-left corner.

### <a name="badge"></a>To display a company badge for quick access to company information

You can add a customized badge in the top-right corner, which you can choose to quickly view company name and tenant information in a pop-up box. The company badge is also useful when [!INCLUDE[prod_short](includes/prod_short.md)] is embedded in another application, like Microsoft Teams or in some other web application. In these cases, because the [!INCLUDE[web_client](includes/web_client.md)] displays less surrounding contextual information, the company badge serves as the only way to determine which company or environment a record belongs to.

1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Company Information**, and then choose the related link.
2. On the **Company Badge** FastTab, fill in the fields as necessary. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

> [!NOTE]
> If a company badge is defined, then you cannot change the company name as described in [To change the company name](ui-change-basic-settings.md#to-change-the-company-name)-->

## Data lavoro <a name="work-date"></a>

La data di lavoro più comunemente utilizzata è la data odierna. Per poter eseguire task quali il completamento delle transazioni per una data che non corrisponde alla data odierna, può essere necessario modificare temporaneamente la data di lavoro.

> [!TIP]  
> In tutti i campi di data, digitare **t** per immettere rapidamente la data odierna e digitare **w** per immettere rapidamente la data di lavoro, ovvero il valore nel campo **Data di lavoro** nella pagina **Impostazioni personali**.

> [!IMPORTANT]  
> Dopo che si modifica la data di lavoro, se ci si disconnette o si passa a un'altra società, la data di lavoro è di nuovo quella predefinita. Di conseguenza, quando si accede o si passa di nuovo alla società originale, può essere necessario reimpostare la data di lavoro.

### Indicazione della data del lavoro

La data del lavoro è fondamentale nelle pagine che possono essere modificate. Ogni volta che la data del lavoro non è impostata sulla data odierna su una pagina modificabile, vengono visualizzati due tipi di indicatori nella pagina:

* Un promemoria viene visualizzato nella parte superiore della pagina e indica l'impostazione della data di lavoro. Questo promemoria fornisce un collegamento diretto all'impostazione della data di lavoro nella pagina **Impostazioni personali** in modo da poter modificare la data, se lo si desidera. È anche possibile scegliere di chiudere il promemoria per il resto della sessione. A meno che non si imposti la data di lavoro su "oggi", il promemoria verrà visualizzato al prossimo accesso.

* Se si chiude il promemoria, la data di lavoro verrà visualizzata nel titolo della pagina.  

Se la data del lavoro non è impostata sul giorno corrente (oggi), in tutte le pagine in cui è possibile modificare i dati, la data del lavoro corrente è visualizzata nell'angolo superiore sinistro.

## <a name="region"></a> Area geografica

L'impostazione **Area geografica** determina il modo in cui date, ore, numeri e valute vengono visualizzati o formattati. Determina anche quale carattere viene usato come separatore decimale quando si usa una tastiera numerica per inserire i dati. Per ulteriori informazioni, vedi [Immissione dati](ui-enter-data.md#decimal).

## <a name="language"></a> Lingua

Cambia la lingua di visualizzazione. Questo campo viene visualizzato solo quando c'è più di una lingua tra cui scegliere.

La lingua iniziale è determinata dall'amministratore o dalle impostazioni del browser quando ci si registri per [!INCLUDE[prod_short](includes/prod_short.md)]. La lingua impostata verrà utilizzata su tutti i dispositivi dai quali si accede, ad esempio da telefono o tablet.

Altre lingue per [!INCLUDE[prod_short](includes/prod_short.md)] posssono essere installate da AppSource. Mentre tutte le lingue di visualizzazione supportate sono visualizzate nell'elenco, l'amministratore deve installare l'app della lingua relativa al tenant prima che gli utenti possano passare alla nuova lingua in [!INCLUDE[prod_short](includes/prod_short.md)].  

## Fuso orario

Definisce il fuso orario in cui ti trovi. Quando accedi per la prima volta a [!INCLUDE [prod_short](includes/prod_short.md)], il fuso orario viene impostato in base all'indirizzo della tua azienda. Modificalo se non si adatta alla tua posizione fisica.  

## Notifiche

Scegli il collegamento *Modifica il momento in cui ricevere le notifiche* per visualizzare o modificare le notifiche ricevute in merito a determinati eventi o modifiche dello stato, come, ad esempio, quando si sta per fatturare a un cliente che ha un saldo scaduto o la giacenza disponibile è inferiore alla quantità che si intende vendere. Per ulteriori informazioni, vedi [Gestione delle notifiche](ui-smart-notifications.md).

## Suggerimenti didattici

[!INCLUDE [ua-teachingtips](includes/ua-teachingtips.md)]

## Vedere anche

[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Modificare le funzionalità visualizzate](ui-experiences.md)  
[Creazione di nuove società](about-new-company.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
