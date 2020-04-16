---
title: Visualizzazione e modifica delle impostazioni di base | Microsoft Docs
description: Informazioni su come modificare alcune impostazioni di base, ad esempio, la Gestione ruolo utente, la società o la data di lavoro.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: change Role Center, notification, change company, change work date
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: cd3d7a821c088b6e9f457e3bf3dc05d0c53525c4
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2020
ms.locfileid: "3194597"
---
# <a name="change-basic-settings"></a>Modificare le impostazioni di base

Nella pagina **Impostazioni personali** è possibile vedere e modificare le impostazioni di base per [!INCLUDE[d365fin](includes/d365fin_md.md)]. Le modifiche apportate interesseranno solo la propria area di lavoro, non quella di altri utenti.  

## <a name="role-center"></a><a name="role-center"></a> Gestione ruolo utente
Gestione ruolo utente rappresenta la home page, una schermata iniziale che è progettata per le esigenze di un ruolo specifico dell'organizzazione. A seconda del ruolo, Gestione ruolo utente offre una panoramica del business, del reparto o dei task personali. Agevola anche l'esplorazione dei task quotidiane e la ricerca del lavoro assegnato.

-   Nella parte superiore, lo spostamento consente di esplorare clienti, fornitori, articoli e altri importanti elenchi di informazioni. In modo simile, le azioni consentono di avviare task, come creare una nuova fattura di vendita, direttamente da Gestione ruolo utente.

-   In Gestione ruolo utente, è presente l'area **Attività** che mostra i dati correnti e che può essere selezionata o toccata per visualizzare informazioni più dettagliate. È possibile impostare Indicatori delle prestazioni chiave (KPI) in modo da visualizzare un grafico selezionato per una rappresentazione visiva di, ad esempio, flussi di cassa o spese e ricavi. È inoltre possibile creare una lista di clienti preferiti in Gestione ruolo utente per gli account aziendali con cui si fanno spesso affari o a cui è importante prestare un'attenzione speciale.

### <a name="to-change-the-role"></a>Per modificare il ruolo
Il ruolo predefinito è **Manager aziendale**, ma è possibile selezionare un altro ruolo per utilizzare una gestione ruolo utente più adatta alle proprie esigenze.
1. Nell'angolo superiore destro scegliere l'icona **Impostazioni** ![Impostazioni](media/ui-experience/settings_icon_small.png "Icona Impostazioni per Gestione ruolo utente"), quindi scegliere l'azione **Impostazioni personali**.
2. Nella pagina **Impostazioni personali** nel campo **Ruolo** selezionare il ruolo che si desidera utilizzare per impostazione predefinita. Ad esempio, selezionare **Contabile**.
3. Scegliere il pulsante **OK**.

## <a name="company"></a><a name="company"></a>Società
Una società funziona da contenitore dei dati in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Possono essere presenti più società in un database, ma è possibile selezionarne solo una alla volta.

La società di default è detta CRONUS e contiene solo i dati di esempio. È possibile creare una nuova società con dati personalizzati. Per ulteriori informazioni, vedere [Creazione di nuove società](about-new-company.md).

## <a name="to-change-the-company-name"></a>Per cambiare il nome della società
Il nome della società viene sempre visualizzato nell'angolo in alto a sinistra e funziona come un'azione che è possibile scegliere per tornare a Gestione ruolo utente. Questo nome può essere modificato nella pagina **Informazioni società**.

1. Scegliere l'![icona ingranaggio per aprire il menu Impostazioni](media/ui-experience/settings_icon_small.png), quindi scegliere l'azione **Informazioni società**.
2. Nel campo **Nome** immettere il nuovo nome della società.
3. Chiudere la pagina. Il sistema si riavvia e visualizza la nuova società nell'angolo superiore sinistro.

## <a name="to-display-a-company-badge-for-quick-access-to-company-information"></a>Per visualizzare un badge società per un rapido accesso alle informazioni della società  
È possibile aggiungere un badge personalizzato nell'angolo in alto a destra. Questo badge consente di visualizzare rapidamente il nome della società e le informazioni sul tenant in una finestra a comparsa.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Informazioni società** e quindi scegliere il collegamento correlato.
2. Nella Scheda dettaglio **Badge società** compilare i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

> [!NOTE]
> Se viene definito un badge società, non è possibile modificare il nome della società come descritto in [Per cambiare il nome della società](ui-change-basic-settings.md#to-change-the-company-name)

## <a name="work-date"></a><a name="work-date"></a>Data lavoro
La data di lavoro più comunemente utilizzata è la data odierna. Per poter eseguire task quali il completamento delle transazioni per una data che non corrisponde alla data odierna, può essere necessario modificare temporaneamente la data di lavoro.

> [!TIP]  
> In tutti i campi di data, digitare **t** per immettere rapidamente la data odierna e digitare **w** per immettere rapidamente la data di lavoro, ovvero il valore nel campo **Data di lavoro** nella pagina **Impostazioni personali**.

> [!IMPORTANT]  
>  Dopo che si modifica la data di lavoro, se ci si disconnette o si passa a un'altra società, la data di lavoro è di nuovo quella predefinita. Di conseguenza, quando si accede o si passa di nuovo alla società originale, può essere necessario reimpostare la data di lavoro.

### <a name="work-date-indication"></a>Indicazione della data di lavoro
Ogni volta che la data di lavoro non è impostata sulla data odierna, nelle pagine verranno visualizzati due tipi di indicatori modificabili in cui la data di lavoro è quindi essenziale:

- Un promemoria viene visualizzato nella parte superiore della pagina e indica l'impostazione della data di lavoro. Questo promemoria fornisce un collegamento diretto all'impostazione della data di lavoro nella pagina **Impostazioni personali** in modo da poter modificare la data, se lo si desidera. È anche possibile scegliere di chiudere il promemoria per il resto della sessione. A meno che non si imposti la data di lavoro su "oggi", il promemoria verrà visualizzato al prossimo accesso.

- Se si chiude il promemoria, la data di lavoro verrà visualizzata nel titolo della pagina.  
--> Se la data di lavoro non è impostata sul giorno corrente (oggi), in tutte le pagine in cui è possibile modificare dati, la data di lavoro corrente è visualizzata nell'angolo superiore sinistro.

## <a name="region"></a><a name="region"></a> Area geografica

L'impostazione **Area geografica** determina il modo in cui date, ore, numeri e valute vengono visualizzati o formattati.

## <a name="language"></a><a name="language"></a> Lingua
Cambia la lingua di visualizzazione. Questo campo viene visualizzato solo quando c'è più di una lingua tra cui scegliere.

La lingua iniziale è determinata dall'amministratore o dalle impostazioni del browser quando ci si registri per [!INCLUDE[d365fin](includes/d365fin_md.md)]. La lingua impostata verrà utilizzata su tutti i dispositivi dai quali si accede, ad esempio da telefono o tablet.

Altre lingue per [!INCLUDE[prodshort](includes/prodshort.md)] posssono essere installate da AppSource. Mentre tutte le lingue di visualizzazione supportate sono visualizzate nell'elenco, l'amministratore deve installare l'app della lingua relativa al tenant prima che gli utenti possano passare alla nuova lingua in [!INCLUDE[prodshort](includes/prodshort.md)].  

## <a name="changing-when-i-receive-notifications"></a>Modifica del momento in cui ricevere le notifiche
Scegliere questo collegamento per visualizzare o modificare le notifiche ricevute in merito a determinati eventi o modifiche dello stato, come, ad esempio, quando si sta per fatturare a un cliente che ha un saldo scaduto o la giacenza disponibile è inferiore alla quantità che si intende vendere. Per ulteriori informazioni, vedere [Gestione delle notifiche](ui-smart-notifications.md).

## <a name="see-related-training-at-microsoft-learn"></a>Vedere le informazioni relative al training in [Microsoft Learn](/learn/modules/personalize-ui-dynamics-365-business-central/index)

## <a name="see-also"></a>Vedere anche
[Creazione di nuove società](about-new-company.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Modifica delle funzionalità visualizzate](ui-experiences.md)  
