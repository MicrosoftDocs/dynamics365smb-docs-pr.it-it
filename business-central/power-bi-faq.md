---
title: Domande frequenti su Power BI
description: Ottieni risposte ad alcune domande comuni sull'utilizzo di Power BI e Business Central.
author: jswymer
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Power BI, reports, faq, errors'
ms.date: 04/22/2021
ms.author: jswymer
---
# <a name="power-bi--faq"></a><a name="power-bi--faq"></a>Domande frequenti su Power BI

Questo articolo contiene le risposte ad alcune domande sull'utilizzo di Power BI e [!INCLUDE [prod_short](includes/prod_short.md)].

## [Generale](#tab/general)
<!-- 26 -->
### <a name="ive-selected-a-report-for-my-role-center-in-business-central-if-i-later-make-changes-to-the-reports-visuals-online-will-the-role-center-automatically-update-to-my-changes"></a><a name="ive-selected-a-report-for-my-role-center-in-business-central-if-i-later-make-changes-to-the-reports-visuals-online-will-the-role-center-automatically-update-to-my-changes"></a>Ho selezionato un report per il Gestione ruolo in Business Central. Se in seguito eport modifiche agli elementi visivi online del report, Gestione ruolo si aggiornerà automaticamente con le mie modifiche?

Sì, perché i report sono incorporati da Power BI.

<!-- 3 -->
### <a name="are-the-business-central-apps-for-power-bi-available-in-languages-other-than-english"></a><a name="are-the-business-central-apps-for-power-bi-available-in-languages-other-than-english"></a>Le app Business Central per Power BI sono disponibili in lingue diverse dall'inglese?

No. Queste app sono attualmente disponibili solo in inglese.

<!-- 24 -->
### <a name="once-a-report-is-published-on-mypowerbicomworkspace-can-i-download-its-pbix"></a><a name="once-a-report-is-published-on-mypowerbicomworkspace-can-i-download-its-pbix"></a>Una volta che un report è stato pubblicato sul mio spazio di lavoro powerbi.com, posso scaricare il suo pbix?

Sì. Per ulteriori informazioni, vedi [Scarica un report dal servizio Power BI a Power BI Desktop](/power-bi/create-reports/service-export-to-pbix).  

<!-- 27 -->
### <a name="can-i-download-the-apps-as-pbix-files"></a><a name="can-i-download-the-apps-as-pbix-files"></a>Posso scaricare le app come file pbix?

No. Al momento, non offriamo il download di file pbix per le app Power BI ufficiali perché sono pubblicate su AppSource.

## [Licenza](#tab/license)

<!-- 14 -->
### <a name="do-i-need-a-power-bi-pro-license-to-publish-reports"></a><a name="do-i-need-a-power-bi-pro-license-to-publish-reports"></a>Ho bisogno di una licenza Power BI Pro per pubblicare report?

<!-- todo What does " or for every user that consults the published report" mean? fixed -->
No. Non è necessario disporre di una licenza Pro per pubblicare report. La licenza Power BI (gratuita) standard è sufficiente. Per ulteriori informazioni, vedere [Licenze Power BI](admin-powerbi-setup.md#license).

<!-- 15 -->
### <a name="is-there-anything-i-cant-do-with-the-free-license"></a><a name="is-there-anything-i-cant-do-with-the-free-license"></a>C'è qualcosa che non posso fare con la licenza gratuita?

Non puoi condividere report né installare le app Business Central per Power BI. Oltre a questo, la licenza gratuita ti consente di creare quasi tutte le varianti di grafici e report.

<!-- 16 -->
### <a name="if-someone-shares-a-report-with-another-person-then-that-person-needs-a-pro-license-to-see-the-report-are-there-plans-to-make-this-capability-possible-with-the-free-license"></a><a name="if-someone-shares-a-report-with-another-person-then-that-person-needs-a-pro-license-to-see-the-report-are-there-plans-to-make-this-capability-possible-with-the-free-license"></a>Se qualcuno condivide un report con un'altra persona, tale persona necessita di una licenza Pro per visualizzarlo. È previsto che questa funzionalità venga resa disponibile con la licenza gratuita?

Non abbiamo alcun controllo su questo requisito. Questo requisito è stabilito da Power BI. Per ulteriori informazioni, vedi [Condividere dashboard e report di Power BI con colleghi e altre persone](/power-bi/collaborate-share/service-share-dashboards).  

## [Designer](#tab/designer)

<!-- 7 -->
### <a name="does-the-connector-work-with-api-pages"></a><a name="does-the-connector-work-with-api-pages"></a>Il connettore funziona con le pagine API?

Sì. A partire da giugno 2021, il nuovo connettore di Power BI supporta sia i servizi Web di Business Central sia le pagine API. Per ulteriori informazioni, vedi [Abilitare il connettore di Power BI per utilizzarlo con le API di Business Central, anziché solo con i servizi Web](/dynamics365-release-plan/2021wave1/smb/dynamics365-business-central/enable-power-bi-connector-work-business-central-apis-instead-web-services-only).

### <a name="can-i-build-a-power-bi-report-using-the-sales-invoice-lines-or-journal-lines-apis"></a><a name="can-i-build-a-power-bi-report-using-the-sales-invoice-lines-or-journal-lines-apis"></a>Posso creare un report Power BI utilizzando le API Righe fattura vendita o Righe registrazioni?

I record di riga più comunemente usati sono disponibili nelle [API di Business Central v2.0](/dynamics365/business-central/dev-itpro/api-reference/v2.0/). Quindi puoi usarli per creare report in Power BI selezionandoli nel connettore **Dynamics 365 Business Central**. Comunque, le API **Righe** sono progettate per essere utilizzate solo con alcuni filtri molto specifici e potrebbero non funzionare nel tuo scenario. Potresti ricevere un errore simile a "È necessario specificare un ID o un ID documento per ottenere le righe". Per risolvere questo problema, esegui i passaggi seguenti quando ricevi i dati da Business Central per il report in Power BI Desktop:

1. Invece di includere l'origine dati per l'entità righe, aggiungi l'origine dati padre. Ad esempio, aggiungi **Fattura di vendita** invece di **Righe fattura vendita**.
2. Seleziona **Trasforma dati** nella barra delle azioni di Power BI Desktop.
3. Seleziona la query che hai appena aggiunto, ad esempio **Fatture di vendita**.
4. Applica qualsiasi filtro necessario sui record per ridurre la quantità di record caricati nel report.
5. Scorri verso destra fino a trovare una colonna denominata come Righe, ad esempio **Righe fattura vendita**.
6. Seleziona il pulsante di espansione nell'intestazione della colonna, accanto al nome della colonna.

   :::image type="content" source="media/saleinvoicelines.png" alt-text="Mostra la colonna SalesInvoiceLines in Power BI Desktop.":::
<!-- 11 --> 
### <a name="is-it-possible-to-choose-which-business-central-environment-to-get-data-from-for-power-bi-for-example-like-a-sandbox-or-production-environment"></a><a name="is-it-possible-to-choose-which-business-central-environment-to-get-data-from-for-power-bi-for-example-like-a-sandbox-or-production-environment"></a>È possibile scegliere da quale ambiente Business Central ottenere i dati per Power BI, ad esempio, come una sandbox o un ambiente di produzione?

Sì. Può essere scelto facilmente. Quando ti connetti a Business Central utilizzando il connettore, è necessario scegliere l'ambiente e il nome della società.

<!-- 6 --> 
### <a name="can-i-merge-data-from-several-production-environments-of-the-same-tenant"></a><a name="can-i-merge-data-from-several-production-environments-of-the-same-tenant"></a>Posso unire i dati da diversi ambienti di produzione dello stesso tenant?

Sì. In Power BI, esegui di nuovo l'operazione di recupero dei dati e scegli l'ambiente che desideri.

<!-- 25 -->
### <a name="which-pages-in-business-central-have-the-power-bi-report-part"></a><a name="which-pages-in-business-central-have-the-power-bi-report-part"></a>Quali pagine in Business Central includono la parte Report Power BI?

Attualmente, sono presenti alcune pagine selezionate che dispongono di un FactBox con una parte **Report Power BI** per la visualizzazione di un report. 

Nelle pagine di elenco, la parte **Report Power BI** viene filtrata per mostrare i report che riguardano i dati nell'elenco. Di seguito sono riportate le pagine del tipo di elenco che includono la parte **Report Power BI**:

|ID pagina|Name|
|-------|----|
|22|Lista clienti|
|27|Lista fornitori|
|31|Elenco articoli|
|9305|Lista ordini di vendita|
|9308|Fatture di acquisto|

Di seguito sono riportate altre pagine che contengono la parte **Report Power BI** non filtrata, più grande:

|ID pagina|Name|
|-------|----|
|1156|Dettagli società|
|4013|Informazioni su Cloud intelligente |
|9006|Centro gestione ruolo Addetto elaborazione ordini|
|9008|Registrazioni  Centro gestione ruolo di base|
|9010|Gestione ruolo utente pianificatore di produzione|
|9015|Gestione ruolo utente manager commessa|
|9016|Gestione ruolo utente distributore assistenza|
|9022|Gestione ruolo utente manager aziendale|
|9024|Gestione ruolo utente amministratore sicurezza|
|9026|Gestione vendite e relazioni Gestione ruolo|
|9027|Gestione ruolo utente Contabile|

> [!TIP]
> Al momento non abbiamo in programma di aggiungerlo a tutte le pagine dell'elenco. Tuttavia, puoi creare una semplice estensione di pagina che aggiunge la parte **Report Power BI** in un riquadro Dettaglio informazioni. Per ulteriori informazioni, vedi [Aggiunta di parti Report Power BI alle pagine](/dynamics365/business-central/dev-itpro/developer/devenv-power-bi-report-parts) nella Guida per sviluppatori e professionisti IT.

<!-- 5 -->
### <a name="is-there-any-way-to-filter-a-dataset-from-business-central-before-i-pull-it-into-power-bi-instead-of-applying-filters-afterwards"></a><a name="is-there-any-way-to-filter-a-dataset-from-business-central-before-i-pull-it-into-power-bi-instead-of-applying-filters-afterwards"></a>Esiste un modo per filtrare un set di dati da Business Central *prima* che io lo inserisca in Power BI, anziché applicare filtri in seguito?

Per filtrare set di dati più grandi, il modo più semplice è impostare un filtro sul report Power BI modificando direttamente la formula di Power Query. La maggior parte dei filtri impostati in questo modo verrà trasmessa a Business Central tramite la riduzione della query. Vedi [Aggiornamento incrementale per set di dati](/power-bi/admin/service-premium-incremental-refresh).

Al momento non è possibile impostare un filtro per i dati del servizio Web da Business Central. Se la tua applicazione deve impostare un filtro da Business Central, dovrai creare un'app Business Central personalizzata per questo scopo.

<!-- 10 -->
### <a name="from-power-bi-besides-using-a-query-is-there-another-way-to-get-data-from-business-central-tables-that-dont-have-an-associated-page-for-example-like-the-item-attributes-value-mapping-table"></a><a name="from-power-bi-besides-using-a-query-is-there-another-way-to-get-data-from-business-central-tables-that-dont-have-an-associated-page-for-example-like-the-item-attributes-value-mapping-table"></a>Da Power BI, oltre a utilizzare una query, esiste un altro modo per ottenere dati dalle tabelle di Business Central che non dispongono di una pagina associata? Ad esempio, come la tabella *Mapping valore attributo articolo*.

No. Non a questo punto.

<!-- 12 --> 
### <a name="are-published-queries-faster-to-use-than-published-pages"></a><a name="are-published-queries-faster-to-use-than-published-pages"></a>Le query pubblicate sono più veloci da utilizzare rispetto alle pagine pubblicate?

Quando si tratta di servizi Web, le query pubblicate sono generalmente più veloci delle pagine pubblicate equivalenti. Il motivo è che le query sono ottimizzate per la lettura dei dati e non contengono trigger costosi come OnAfterGetRecord.

I servizi Web si basano su pagine o query create per l'accesso dal Web e generalmente non ottimizzate per l'accesso da servizi esterni. Anche se il connettore Business Central supporta ancora l'acquisizione di dati dai servizi Web, ti invitiamo a utilizzare le pagine API anziché i servizi Web quando possibile.

<!-- 13 --> 
### <a name="is-there-a-way-for-an-end-user-to-create-a-web-service-with-a-column-thats-in-a-business-central-table-but-not-a-page-or-will-the-developer-have-to-create-a-custom-query"></a><a name="is-there-a-way-for-an-end-user-to-create-a-web-service-with-a-column-thats-in-a-business-central-table-but-not-a-page-or-will-the-developer-have-to-create-a-custom-query"></a>Esiste un modo per un utente finale di creare un servizio Web con una colonna che si trova in una tabella di Business Central, ma non in una pagina? Oppure lo sviluppatore dovrà creare una query personalizzata?

Al momento non è possibile aggiungere un nuovo campo a un servizio Web. Le pagine API offrono piena flessibilità della struttura della pagina, quindi uno sviluppatore può creare una nuova pagina API per soddisfare questo requisito. 

<!-- 28 --> 
### <a name="can-i-connect-power-bi-to-a-read-only-database-server-of-business-central-online"></a><a name="can-i-connect-power-bi-to-a-read-only-database-server-of-business-central-online"></a>Posso connettere Power BI a un server di database di sola lettura di Business Central Online?

Questa funzionalità sarà presto disponibile. A partire da febbraio 2022, i nuovi report creati in base ai dati di Business Central online tenteranno automaticamente di connettersi a una replica del database di sola lettura. Ciò farà sì che i tuoi report si aggiornino più velocemente, con un impatto minore sulle prestazioni se utilizzi Business Central durante l'aggiornamento di un report. Ti consigliamo comunque, quando possibile, di pianificare l'aggiornamento dei report al di fuori del normale orario di lavoro.

Se disponi di vecchi report basati sui dati di Business Central, non si collegheranno alla replica del database di sola lettura.

### <a name="ive-tried-the-preview-of-the-new-connector-for-the-february-2022-update-when-i-connect-to-my-custom-business-central-api-page-i-get-the-error-cannot-insert-a-record-current-connection-intent-is-read-only-how-can-i-fix-it"></a><a name="ive-tried-the-preview-of-the-new-connector-for-the-february-2022-update-when-i-connect-to-my-custom-business-central-api-page-i-get-the-error-cannot-insert-a-record-current-connection-intent-is-read-only-how-can-i-fix-it"></a><a name="databasemods"></a>Ho provato l'anteprima del nuovo connettore per l'aggiornamento di febbraio 2022. Quando mi collego alla mia pagina API Business Central personalizzata, viene visualizzato l'errore "Impossibile inserire un record. L'intento di connessione corrente è di sola lettura." Come posso risolverlo?

Con il nuovo connettore, i nuovi report che utilizzano i dati di Business Central si collegheranno a una replica di sola lettura del database di Business Central per impostazione predefinita. Questa modifica porterà un miglioramento delle prestazioni. Tuttavia, in rari casi, potrebbe causare l'errore. Questo errore si verifica in genere perché l'API personalizzata sta apportando modifiche ai record di Business Central mentre Power BI cerca di ottenere i dati. In particolare, si verifica come parte dei trigger AL: OnInit, OnOpenPage, OnFindRecord, OnNextRecord, OnAfterGetRecord e OnAfterGetCurrRecord.

Per risolvere questo problema forzando il connettore Business Central a consentire questo comportamento, vedi [Creazione di report di Power BI per visualizzare i dati di Business Central - Risoluzione dei problemi](across-how-use-financials-data-source-powerbi.md#fixing-problems).

<!--
In general, we recommend avoiding any database modifications in API pages when they're opening or loading records, because they cause performance issues and might cause your report refresh to fail. In some cases, you might still need to make a database modification when your custom API page opens or loads records. You can force the Business Central connector to allow this behavior. Do the following steps when getting data from Business Central for the report in Power BI Desktop:

1. Start Power BI Desktop.
2. In the ribbon, select **Get Data** > **Online Services**.
3. In the **Online Services** pane, select **Dynamics 365 Business Central**, then **Connect**.
4. In the **Navigator** window, select the API endpoint that you want to load data from.
5. In the preview pane on the right, you'll see the following error:

   *Dynamics365BusinessCentral: Request failed: The remote server returned an error: (400) Bad Request. (Cannot insert a record. Current connection intent is Read-Only. CorrelationId: [...])".*

6.  Select **Transform Data** instead of **Load** as you might normally do.
7. In **Power Query Editor**, select **Advanced Editor** from the ribbon.
8.  Replace the following line:

   ```
   Source = Dynamics365BusinessCentral.ApiContentsWithOptions(null, null, null, null),
   ```

   with the line:

   ```
   Source = Dynamics365BusinessCentral.ApiContentsWithOptions(null, null, null, [UseReadOnlyReplica = false]),
   ```

9.  Select **Done**.
10. Select **Close & Apply** from the ribbon to save the changes and close Power Query Editor.

-->
### <a name="how-do-i-change-or-clear-the-user-account-im-currently-using-to-connect-to-business-central-from-power-bi-desktop"></a><a name="how-do-i-change-or-clear-the-user-account-im-currently-using-to-connect-to-business-central-from-power-bi-desktop"></a><a name="perms"></a>Come posso modificare o cancellare l'account utente che sto utilizzando attualmente per connettermi a Business Central da Power BI Desktop?

In Power BI Desktop, effettua i seguenti passaggi:

1. Nel menu File, seleziona **Opzioni e impostazioni** > **Impostazioni origine dati**.
2. Seleziona **Dynamics Business Central** dall'elenco, quindi seleziona **Cancella autorizzazioni** > **Elimina**.

Quindi, la prossima volta che ti connetterai a Business Central per ottenere dati, ti verrà chiesto di accedere.

## [Prestazioni](#tab/performance)

<!-- 17 -->

### <a name="is-it-faster-to-get-data-using-api-pages-than-using-web-services"></a><a name="is-it-faster-to-get-data-using-api-pages-than-using-web-services"></a>È più veloce ottenere i dati utilizzando le pagine API rispetto ai servizi Web?

Sì. I nostri test indicano che le pagine API sono fino al 25% più performanti rispetto ai servizi Web.

<!-- 18 -->
### <a name="are-there-plans-to-have-a-mirror-on-the-azure-sql-database-instance-which-i-can-connect-to-directly"></a><a name="are-there-plans-to-have-a-mirror-on-the-azure-sql-database-instance-which-i-can-connect-to-directly"></a>È previsto un mirror nell'istanza del database SQL di Azure, a cui posso connettermi direttamente?

No. Non a questo punto. È possibile comunicare con Business Central solo tramite API.

<!-- 19 -->
### <a name="loading-data-from-business-central-web-services-seems-slow-is-there-any-way-to-get-data-directly-from-the-sql-database-table"></a><a name="loading-data-from-business-central-web-services-seems-slow-is-there-any-way-to-get-data-directly-from-the-sql-database-table"></a>Il caricamento dei dati dai servizi Web di Business Central sembra lento. C'è un modo per ottenere i dati direttamente dalla tabella del database SQL?

No. L'accesso diretto al database non è possibile, ma il passaggio alle pagine API (quando il nuovo connettore sarà disponibile) sarà molto utile.

## [Avanzate](#tab/advanced)
<!-- 1 -->

### <a name="are-there-plans-for-the-power-bi-connector-to-support-the-incremental-refresh-features-in-the-power-bi-service"></a><a name="are-there-plans-for-the-power-bi-connector-to-support-the-incremental-refresh-features-in-the-power-bi-service"></a>È previsto che il connettore di Power BI supporti le funzionalità di aggiornamento incrementale nel servizio Power BI?

Sì. È nella nostra roadmap.

<!-- 2 -->
### <a name="if-a-business-central-on-premises-solution-doesnt-have-internet-access-can-i-still-use-power-bi"></a><a name="if-a-business-central-on-premises-solution-doesnt-have-internet-access-can-i-still-use-power-bi"></a>Se una soluzione locale di Business Central non dispone dell'accesso a Internet, posso comunque utilizzare Power BI?
<!-- todo: please explain this one-->

Sì. In questo caso, utilizzi Power BI Desktop localmente e ti connetti a Business Central in locale. Dopo la connessione, puoi creare e visualizzare report, ma non puoi pubblicarli nel servizio Power BI. 
<!-- 20 -->
### <a name="are-there-any-plans-to-make-it-possible-to-replicate-business-central-online-databases-so-theyre-accessible-for-read-only-sql-queries-this-capability-would-support-incremental-refresh-and-be-a-lot-faster-than-apis-or-web-services"></a><a name="are-there-any-plans-to-make-it-possible-to-replicate-business-central-online-databases-so-theyre-accessible-for-read-only-sql-queries-this-capability-would-support-incremental-refresh-and-be-a-lot-faster-than-apis-or-web-services"></a>È prevista la possibilità di replicare database di Business Central Online in modo che siano accessibili per le query SQL di sola lettura? Questa funzionalità supporterebbe l'aggiornamento incrementale e sarebbe molto più veloce di quello delle API o dei servizi Web.

<!-- todo: what does "BC-Saas-DB-replicated DB accessible" mean? fixe-->
Sì. Abbiamo questa funzionalità nella nostra roadmap a lungo termine. 

<!-- 21 -->
### <a name="if-i-use-azure-data-factory-to-get-data-from-business-central-and-consume-it-on-power-bi-will-that-help-in-increase-in-performance"></a><a name="if-i-use-azure-data-factory-to-get-data-from-business-central-and-consume-it-on-power-bi-will-that-help-in-increase-in-performance"></a>Se utilizzo Azure Data Factory per ottenere dati da Business Central e utilizzarli in Power BI, le prestazioni verranno migliorate?

Sì. Questo scenario avanzato aiuterà Business Central a rimanere performante, perché l'accesso ai dati avverrebbe tramite Azure Data Factory.

<!-- 22 -->
### <a name="are-there-any-plans-to-support-power-bi-deployment-pipelines-or-a-way-to-build-deployment-pipelines-for-pbi-reports-similar-to-extensions-or-maybe-even-a-simple-api-in-the-business-admin-center"></a><a name="are-there-any-plans-to-support-power-bi-deployment-pipelines-or-a-way-to-build-deployment-pipelines-for-pbi-reports-similar-to-extensions-or-maybe-even-a-simple-api-in-the-business-admin-center"></a>È previsto il supporto di pipeline di distribuzione di Power BI o un modo per creare pipeline di distribuzione per report PBI, simili alle estensioni? O forse anche una semplice API nell'interfaccia di amministrazione Business?

Stiamo esaminando questa funzionalità. Power BI offre API complete per controllare le distribuzioni di report. Per ulteriori informazioni, vedi [Introduzione alle pipeline di distribuzione](/power-bi/create-reports/deployment-pipelines-overview).

### <a name="when-i-get-data-from-business-central-to-use-in-my-power-bi-reports-i-see-some-values-like-_x0020_-what-are-these-values"></a><a name="when-i-get-data-from-business-central-to-use-in-my-power-bi-reports-i-see-some-values-like-_x0020_-what-are-these-values"></a>Quando ottengo i dati di Business Central da utilizzare nei report Power BI, vedo alcuni valori come "_x0020_". Quali sono questi valori?

Alcune pagine API, inclusa la maggior parte delle pagine API v2.0, hanno campi basati su [oggetti enumerazione AL](/dynamics365/business-central/dev-itpro/developer/devenv-extensible-enums). I campi basati su oggetti enumerazione AL devono avere nomi coerenti e sempre uguali, in modo che i filtri nel report funzionino sempre, indipendentemente dalla lingua o dal sistema operativo in uso. Per questo motivo, i campi basati sulle enumerazioni AL non vengono tradotti e sono codificati per evitare qualsiasi carattere speciale, incluso lo spazio. In particolare, ogni volta che è presente un'opzione vuota nell'oggetto AL Enum, è codificata in "_x0020_". Puoi sempre applicare una trasformazione ai tuoi dati su Power BI se desideri visualizzare un valore diverso per questi campi, ad esempio "Vuoto".


---

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Vedi il relativo [training Microsoft](/training/modules/change-documents-dynamics-365-business-central/)

## <a name="see-also"></a><a name="see-also"></a>Vedere anche

[Licenze Power BI](admin-powerbi-setup.md#license)  
[Introduzione a Business Central e Power BI](admin-powerbi.md)  
[Panoramica dell'integrazione di Power BI](admin-powerbi-overview.md)  
[Abilitazione di Power BI in Business Central](admin-powerbi-setup.md)  
[Utilizzare i report Power BI in Business Central](across-working-with-powerbi.md)  
[Utilizzare i dati Business Central in Power BI](across-working-with-business-central-in-powerbi.md)  
[Creazione di report di Power BI per la visualizzazione di dati di Business Central](across-how-use-financials-data-source-powerbi.md)  
[Documentazione di Power BI](/power-bi/)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
