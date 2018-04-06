---
title: Pacchetti di contenuto per Finance and Operations, Business edition e Power BI | Documenti Microsoft
description: "Ottenere informazioni approfondite, business intelligence e KPI sui dati di Finance and Operations, Business edition è semplice con Power BI e con i pacchetti di contenuto di Finance and Operations, Business edition."
author: edupont04
ms.service: dynamics365-financials
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 09/05/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: 8c8a52f20abe27de7063a0879f529086263d0675
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="enabling-your-business-data-for-power-bi"></a>Abilitare i dati aziendali per Power BI
Ottenere informazioni approfondite sui dati di [!INCLUDE[d365fin](includes/d365fin_md.md)] è semplice con Power BI e con i pacchetti di contenuto di [!INCLUDE[d365fin](includes/d365fin_md.md)]. Power BI recupera i dati e quindi sviluppa un dashboard e i report pronti per l'uso basati su tali dati.  

Microsoft ha pubblicato i seguenti pacchetti di contenuto:

| App | Description |
| --- | --- |
| Microsoft Finance and Operations, Business edition | Fornisce un dashboard con i principali dati finanziari nel tempo, quali gli utili rispetto alle spese, il margine operativo e il ciclo di cassa.|
| Microsoft Finance and Operations, Business edition - CRM | Fornisce un dashboard con i dati principali relativi alle opportunità di vendita e ai contatti.  |
| Microsoft Finance and Operations, Business edition - Sales | Fornisce un dashboard con i dati principali relativi alle vendite e al magazzino. |

## <a name="using-the-dashboards"></a>Utilizzo dei dashboard
Ogni pacchetto di contenuto include report che è possibile analizzare in dettaglio:

* Selezionare una qualsiasi visualizzazione nel dashboard per portare in primo piano uno dei report sottostanti.  
* Filtrare il report o aggiungere i campi che si desidera monitorare.  
* Aggiungere la visualizzazione personalizzata al dashboard per continuare la tracciabilità.  
  È possibile aggiornare manualmente i dati e configurare la pianificazione degli aggiornamenti. Per ulteriori informazioni, vedere [Configurazione di aggiornamenti pianificati](https://powerbi.microsoft.com/en-us/documentation/powerbi-refresh-scheduled-refresh/)  

I pacchetti di contenuti sono preconfigurati per utilizzare i dati della società demo che si crea quando si effettua l'iscrizione a [!INCLUDE[d365fin](includes/d365fin_md.md)]. Quando si installano le app in Power BI e si collegano dati personali, alcuni report potrebbero non funzionare perché si basano su dati di cui la società non dispone. In tali casi è possibile semplicemente rimuovere tali report dal dashboard.  

> [!NOTE]  
>   È inoltre possibile creare i propri report e dashboard in Power BI in base ai dati di [!INCLUDE[d365fin](includes/d365fin_md.md)]. Per ulteriori informazioni, vedere [Collegare i dati aziendali a Power BI](across-how-use-financials-data-source-powerbi.md).  

## <a name="accessing-included365finincludesd365finmdmd-in-power-bi"></a>Accedere a [!INCLUDE[d365fin](includes/d365fin_md.md)] in Power BI
Per visualizzare i dati di [!INCLUDE[d365fin](includes/d365fin_md.md)] in Power BI, è necessario disporre di quanto segue:  

* Accesso a [!INCLUDE[d365fin](includes/d365fin_md.md)]. Per ulteriori informazioni, vedere [Finance and Operations, Business edition](http://go.microsoft.com/fwlink/?LinkID=759714).  
* Accesso a Power BI. Per ulteriori informazioni, vedere [Power BI](https://powerbi.microsoft.com).

Nel sito di Power BI è possibile trovare informazioni aggiuntive su [connettere i servizio con i pacchetti di contenuto per Power BI](http://go.microsoft.com/fwlink/?LinkID=760850).  

Per accedere ai dati di [!INCLUDE[d365fin](includes/d365fin_md.md)] in Power BI, ella pagina di connessione è necessario specificare le seguenti informazioni:

| Campo | Descrizione |
| --- | --- |
| **URL Feed OData** |L'URL OData in modo che Power BI possa accedere ai dati della società, ad esempio https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/Company('My%2Business'). |
| **Metodo di autenticazione** |Selezionare **Di base**. |
| **Nome utente** |Il nome come visualizzato per l'account in [!INCLUDE[d365fin](includes/d365fin_md.md)], ad esempio *John Smith*. |
| **Password** |Questa è la chiave di accesso al servizio Web per il proprio account utente in [!INCLUDE[d365fin](includes/d365fin_md.md)]. |

Ciò significa che è necessario ottenere due informazioni da [!INCLUDE[d365fin](includes/d365fin_md.md)]: l'*URL OData* e la *chiave di accesso al servizio Web* per il proprio account utente.  

### <a name="getting-the-url"></a>Ottenere l'URL
Quando si aggiunge [!INCLUDE[d365fin](includes/d365fin_md.md)] a Power BI, è necessario specificare un URL in modo da Power BI possa accedere ai dati dalla società. Nella pagina di connessione, l'URL è denominato **URL Feed OData** e deve avere il seguente formato:

         https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/Company('CRONUS%20US')  
In questo esempio, *mybusiness* è il nome del servizio [!INCLUDE[d365fin](includes/d365fin_md.md)] e *CRONUS US* è il nome della società demo in cui *%20* rappresenta lo spazio nel nome.   
Per ottenere l'URL, in [!INCLUDE[d365fin](includes/d365fin_md.md)] cercare e aprire la finestra **Servizi Web**. In questa finestra viene visualizzato un elenco dei servizi Web attualmente disponibili ed è possibile copiare il collegamento dal campo **OData URL** per uno dei servizi Web predefiniti di OData.  

### <a name="getting-the-user-name-and-the-web-service-access-key"></a>Ottenere il nome utente e la chiave di accesso al servizio Web
Per utilizzare i dati di [!INCLUDE[d365fin](includes/d365fin_md.md)] in Power BI, nella finestra **Connetti a Financials**, è necessario specificare un nome utente e una password. Il nome utente è il nome come visualizzato per l'account in [!INCLUDE[d365fin](includes/d365fin_md.md)], in modo che Power BI possa accedere a [!INCLUDE[d365fin](includes/d365fin_md.md)]. La password è la chiave di accesso al servizio Web impostata per il proprio account utente in [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Per trovare questa informazione, in [!INCLUDE[d365fin](includes/d365fin_md.md)] cercare la finestra **Utenti** e quindi aprire la scheda relativa al proprio account utente. Nella Scheda dettaglio **Generale** copiare il contenuto del campo **Nome utente** e nella Scheda dettaglio **Accesso al servizio Web** copiare il contenuto del campo **Chiave di accesso al servizio Web**. Se il campo **Chiave di accesso al servizio Web** è vuoto, nella barra multifunzione, selezionare **Modifica chiave di accesso al servizio Web**, selezionare il campo **La chiave non scade mai** e quindi fare clic sul pulsante OK. È quindi possibile copiare la chiave.  

## <a name="getting-data-from-included365finincludesd365finmdmd"></a>Acquisizione dei dati da [!INCLUDE[d365fin](includes/d365fin_md.md)]
Il dashboard di [!INCLUDE[d365fin](includes/d365fin_md.md)] mostra i report tipici che più opportuno utilizzare per tenere traccia delle attività. I dati vengono estratti dalla società di [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzando i servizi Web per la lettura dei dati live. Nella finestra **Servizi Web** di [!INCLUDE[d365fin](includes/d365fin_md.md)] sono elencati i servizi Web che sono stati impostati.

> [!NOTE]  
>   Se si modifica il nome di uno qualsiasi dei servizi Web, i dati non verranno mostrati in Power BI.  
Se si desidera aggiungere altri dati in Power BI, è necessario trovare le tabelle in [!INCLUDE[d365fin](includes/d365fin_md.md)], esporle come servizi Web e aggiungerle al pacchetto di contenuto. Questo è uno scenario avanzato e è consigliabile iniziare con i dati che sono già disponibili in Power BI.  

## <a name="troubleshooting"></a>Troubleshooting
Il dashboard di Power BI si basa sui servizi Web rilasciati che sono elencati sopra e visualizza i dati della società demo o della società dell'utente se si importano i dati della soluzione finanziario corrente. Tuttavia, se si verifica un errore, in questa sezione viene fornita una soluzione alternativa per i problemi più comuni.  

**"La convalida dei parametri non è riuscita. Assicurarsi che tutti i parametri siano validi."**  
Se l'errore viene visualizzato dopo l'accesso all'URL di [!INCLUDE[d365fin](includes/d365fin_md.md)], assicurarsi che i seguenti requisiti vengano soddisfatti:  

* l'URL segue esattamente questo modello:

    https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/Company('CRONUS%20US')  
* Eliminare qualsiasi testo dopo il nome della società tra parentesi  
* Assicurarsi che non vi sia una barra finale alla fine dell'URL.  
* Assicurarsi che sia una connessione sicura come indicato dall'URL che inizia con *https*.  

**"Accesso non riuscito"**  
Se viene visualizzato un errore di accesso non riuscito quando si accede al dashboard con le credenziali di [!INCLUDE[d365fin](includes/d365fin_md.md)], questo potrebbe essere causato da uno dei seguenti problemi:

* L'account che si sta utilizzando non dispone delle autorizzazioni di lettura per i dati di [!INCLUDE[d365fin](includes/d365fin_md.md)] da tale account.

    Verificare il proprio account utente in [!INCLUDE[d365fin](includes/d365fin_md.md)] e assicurarsi che sia stata utilizzata la chiave di accesso al servizio Web corretta come password, quindi riprovare.  
* L'istanza di [!INCLUDE[d365fin](includes/d365fin_md.md)] a cui ci si sta provando a connettere non dispone di un certificato SSL valido. In questo caso verrà visualizzato un messaggio di errore più dettagliato ("impossibile stabilire una relazione SSL attendibile").

    > [!NOTE]  
>   Non sono supportati i certificati autofirmati.  

**"Oops"**  
Se viene visualizzata una finestra di dialogo "Oops" dopo aver superato la finestra di dialogo di autenticazione, nei casi più frequenti questo errore è causato da un problema di connessione ai dati del pacchetto di contenuto.

* Verificare che l'URL corrisponda al modello che è stato specificato in precedenza:

    `https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/Company('CRONUS%20US')`  
* Un errore comune consiste nello specificare l'URL completo per un servizio Web specifico:

    `https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/Company('CRONUS%20US')/powerbifinance`
* Oppure è possibile che si sia stato dimenticato di specificare il nome della società:

    `https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/`

## <a name="see-also"></a>Vedi anche
[Business Intelligence](bi.md)  
[Benvenuto in [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Migrare i dati aziendali da altri sistemi contabili](upload-data.md)  
[Uso di [!INCLUDE[d365fin](includes/d365fin_md.md)] come origine dati di Power BI](across-how-use-financials-data-source-powerbi.md)  
[Uso di [!INCLUDE[d365fin](includes/d365fin_md.md)] come origine dati di PowerApps](across-how-use-financials-data-source-powerapps.md)  
[Uso di [!INCLUDE[d365fin](includes/d365fin_md.md)] in Microsoft Flow](across-how-use-financials-data-source-flow.md)   

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

