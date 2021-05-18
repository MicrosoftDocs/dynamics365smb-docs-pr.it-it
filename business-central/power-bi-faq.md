---
title: Domande frequenti su Power BI
description: Ottieni risposte ad alcune domande comuni sull'utilizzo di Power BI e Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Power BI, reports, faq, errors
ms.date: 04/22/2021
ms.author: jswymer
ms.openlocfilehash: 939b280e631113d3196f6fbbc90d9bf19b9fc408
ms.sourcegitcommit: a76475f124e79440a5bba20577b335c4d50a2d83
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "6025835"
---
# <a name="power-bi--faq"></a>Domande frequenti su Power BI

Questo articolo contiene le risposte ad alcune domande sull'utilizzo di Power BI e [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="general"></a>[Generale](#tab/general)
<!-- 26 -->
### <a name="ive-selected-a-report-for-my-role-center-in-business-central-if-i-later-make-changes-to-the-reports-visuals-online-will-the-role-center-automatically-update-to-my-changes"></a>Ho selezionato un report per il Gestione ruolo in Business Central. Se in seguito apporto modifiche agli elementi visivi online del report, Gestione ruolo si aggiornerà automaticamente con le mie modifiche?

Sì, perché i report sono incorporati da Power BI.

<!-- 3 -->
### <a name="are-the-business-central-apps-for-power-bi-available-in-languages-other-than-english"></a>Le app Business Central per Power BI sono disponibili in lingue diverse dall'inglese?

No. Queste app sono attualmente disponibili solo in inglese.

<!-- 24 -->
### <a name="once-a-report-is-published-on-mypowerbicomworkspace-can-i-download-its-pbix"></a>Una volta che un report è stato pubblicato sul mio spazio di lavoro powerbi.com, posso scaricare il suo pbix? 

Sì. Per ulteriori informazioni, vedi [Scarica un report dal servizio Power BI a Power BI Desktop](/power-bi/create-reports/service-export-to-pbix).  

<!-- 27 -->
### <a name="can-i-download-the-apps-as-pbix-files"></a>Posso scaricare le app come file pbix? 

No. Al momento, non offriamo il download di file pbix per le app Power BI ufficiali perché sono pubblicate su AppSource.

## <a name="license"></a>[Licenza](#tab/license)

<!-- 14 -->
### <a name="do-i-need-a-power-bi-pro-license-to-publish-reports"></a>Ho bisogno di una licenza Power BI Pro per pubblicare report? 

<!-- todo What does " or for every user that consults the published report" mean? fixed -->
No. Non è necessario disporre di una licenza Pro per pubblicare report. La licenza Power BI (gratuita) standard è sufficiente. Per ulteriori informazioni, vedere [Licenze Power BI](admin-powerbi-setup.md#license).

<!-- 15 -->
### <a name="is-there-anything-i-cant-do-with-the-free-license"></a>C'è qualcosa che non posso fare con la licenza gratuita?

Non puoi condividere report né installare le app Business Central per Power BI. Oltre a questo, la licenza gratuita ti consente di creare quasi tutte le varianti di grafici e report.

<!-- 16 -->
### <a name="if-someone-shares-a-report-with-another-person-then-that-person-needs-a-pro-license-to-see-the-report-are-there-plans-to-make-this-capability-possible-with-the-free-license"></a>Se qualcuno condivide un report con un'altra persona, tale persona necessita di una licenza Pro per visualizzarlo. È previsto che questa funzionalità venga resa disponibile con la licenza gratuita?

Non abbiamo alcun controllo su questo requisito. Questo requisito è stabilito da Power BI. Per ulteriori informazioni, vedi [Condividere dashboard e report di Power BI con colleghi e altre persone](/power-bi/collaborate-share/service-share-dashboards).  

## <a name="designer"></a>[Designer](#tab/designer)

<!-- 7 -->
### <a name="does-the-connector-work-with-api-pages"></a>Il connettore funziona con le pagine API?

Non ancora. Ma a partire da giugno 2021, il nuovo connettore di Power BI supporterà sia i servizi Web di Business Central sia le pagine API. Per ulteriori informazioni, vedi [Abilitare il connettore di Power BI per utilizzarlo con le API di Business Central, anziché solo con i servizi Web](/dynamics365-release-plan/2021wave1/smb/dynamics365-business-central/enable-power-bi-connector-work-business-central-apis-instead-web-services-only).

<!-- 11 --> 
### <a name="is-it-possible-to-choose-which-business-central-environment-to-get-data-from-for-power-bi-for-example-like-a-sandbox-or-production-environment"></a>È possibile scegliere da quale ambiente Business Central ottenere i dati per Power BI, ad esempio, come una sandbox o un ambiente di produzione? 

Sì. Può essere scelto facilmente. Quando ti connetti a Business Central utilizzando il connettore, è necessario scegliere l'ambiente e il nome della società.

<!-- 6 --> 
### <a name="can-i-merge-data-from-several-production-environments-of-the-same-tenant"></a>Posso unire i dati da diversi ambienti di produzione dello stesso tenant?

Sì. In Power BI, esegui di nuovo l'operazione di recupero dei dati e scegli l'ambiente che desideri.

<!-- 25 -->
### <a name="which-pages-in-business-central-have-the-power-bi-report-part"></a>Quali pagine in Business Central includono la parte Report Power BI?  

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
### <a name="is-there-any-way-to-filter-a-dataset-from-business-central-before-i-pull-it-into-power-bi-instead-of-applying-filters-afterwards"></a>Esiste un modo per filtrare un set di dati da Business Central *prima* che io lo inserisca in Power BI, anziché applicare filtri in seguito?

Per filtrare set di dati più grandi, il modo più semplice è impostare un filtro sul report Power BI modificando direttamente la formula di Power Query. La maggior parte dei filtri impostati in questo modo verrà trasmessa a Business Central tramite la riduzione della query. Vedi [Aggiornamento incrementale per set di dati](/power-bi/admin/service-premium-incremental-refresh).

Al momento non è possibile impostare un filtro per i dati del servizio Web da Business Central. Se la tua applicazione deve impostare un filtro da Business Central, dovrai creare un'app Business Central personalizzata per questo scopo.

<!-- 8 and 9 -->

### <a name="for-embedding-reports-in-business-central-pages-right-now-its-only-possible-to-get-reports-from-my-workspace-in-power-bi-are-there-plans-to-make-it-possible-to-get-them-from-custom-workspaces"></a>Per incorporare report nelle pagine di Business Central, al momento è possibile solo ottenere report da *Area di lavoro personale* in Power BI. Esisono piani per ottenerli da aree di lavoro personalizzate?

Sì. Abbiamo in programma di aggiungere il supporto per le aree di lavoro condivise, ma non abbiamo ancora una tempistica da fornirti.  

<!-- 10 -->
### <a name="from-power-bi-besides-using-a-query-is-there-another-way-to-get-data-from-business-central-tables-that-dont-have-an-associated-page-for-example-like-the-item-attributes-value-mapping-table"></a>Da Power BI, oltre a utilizzare una query, esiste un altro modo per ottenere dati dalle tabelle di Business Central che non dispongono di una pagina associata? Ad esempio, come la tabella *Mapping valore attributo articolo*.

No. Non a questo punto.

<!-- 12 --> 
### <a name="are-published-queries-faster-to-use-than-published-pages"></a>Le query pubblicate sono più veloci da utilizzare rispetto alle pagine pubblicate?

Quando si tratta di servizi Web, le query pubblicate sono generalmente più veloci delle pagine pubblicate equivalenti. Il motivo è che le query sono ottimizzate per la lettura dei dati e non contengono trigger costosi come OnAfterGetRecord.

Quando il nuovo connettore sarà disponibile a giugno 2021, ti consigliamo di utilizzare le pagine API sulle query pubblicate come servizi Web.

<!-- 13 --> 
### <a name="is-there-a-way-for-an-end-user-to-create-a-web-service-with-a-column-thats-in-a-business-central-table-but-not-a-page-or-will-developer-have-to-create-a-custom-query"></a>Esiste un modo per un utente finale di creare un servizio Web con una colonna che si trova in una tabella di Business Central, ma non in una pagina? Oppure lo sviluppatore dovrà creare una query personalizzata? 

Non ancora. Ma quando il nuovo connettore sarà disponibile a giugno 2021, uno sviluppatore potrà creare una nuova pagina API per soddisfare questo requisito. 

<!-- 28 --> 
### <a name="can-i-connect-power-bi-to-a-read-only-database-server-of-business-central-online"></a>Posso connettere Power BI a un server di database di sola lettura di Business Central Online? 

No. Ma abbiamo questa funzionalità nella nostra roadmap a lungo termine. 

## <a name="performance"></a>[Prestazioni](#tab/performance)

<!-- 17 -->

### <a name="is-it-faster-to-get-data-using-api-pages-than-using-web-services"></a>È più veloce ottenere i dati utilizzando le pagine API rispetto ai servizi Web?

Sì. I nostri test indicano che le pagine API sono fino al 25% più performanti rispetto ai servizi Web.

<!-- 18 -->
### <a name="are-there-plans-to-have-a-mirror-on-the-azure-sql-database-instance-which-i-can-connect-to-directly"></a>È previsto un mirror nell'istanza del database SQL di Azure, a cui posso connettermi direttamente?

No. Non a questo punto. È possibile comunicare con Business Central solo tramite API.

<!-- 19 -->
### <a name="loading-data-from-business-central-web-services-seems-slow-is-there-any-way-to-get-data-directly-from-the-sql-database-table"></a>Il caricamento dei dati dai servizi Web di Business Central sembra lento. C'è un modo per ottenere i dati direttamente dalla tabella del database SQL?

No. L'accesso diretto al database non è possibile, ma il passaggio alle pagine API (quando il nuovo connettore sarà disponibile) sarà molto utile.

## <a name="advanced"></a>[Avanzate](#tab/advanced)
<!-- 1 -->

### <a name="are-there-plans-for-the-power-bi-connector-to-support-the-incremental-refresh-features-in-the-power-bi-service"></a>È previsto che il connettore di Power BI supporti le funzionalità di aggiornamento incrementale nel servizio Power BI?

Sì. È nella nostra roadmap.

<!-- 2 -->
### <a name="if-a-business-central-on-premises-solution-doesnt-have-internet-access-can-i-still-use-power-bi"></a>Se una soluzione locale di Business Central non dispone dell'accesso a Internet, posso comunque utilizzare Power BI?
<!-- todo: please explain this one-->

Sì. In questo caso, utilizzi Power BI Desktop localmente e ti connetti a Business Central in locale. Dopo la connessione, puoi creare e visualizzare report, ma non puoi pubblicarli nel servizio Power BI. 
<!-- 20 -->
### <a name="are-there-any-plans-to-make-it-possible-to-replicate-business-central-online-databases-so-theyre-accessible-for-read-only-sql-queries-this-capability-would-support-incremental-refresh-and-be-a-lot-faster-than-apis-or-web-services"></a>È prevista la possibilità di replicare database di Business Central Online in modo che siano accessibili per le query SQL di sola lettura? Questa funzionalità supporterebbe l'aggiornamento incrementale e sarebbe molto più veloce di quello delle API o dei servizi Web.

<!-- todo: what does "BC-Saas-DB-replicated DB accessible" mean? fixe-->
Sì. Abbiamo questa funzionalità nella nostra roadmap a lungo termine. 

<!-- 21 -->
### <a name="if-i-use-azure-data-factory-to-get-data-from-business-central-and-consume-it-on-power-bi-will-that-help-in-increase-in-performance"></a>Se utilizzo Azure Data Factory per ottenere dati da Business Central e utilizzarli in Power BI, le prestazioni verranno migliorate? 

Sì. Questo scenario avanzato aiuterà Business Central a rimanere performante, perché l'accesso ai dati avverrebbe tramite Azure Data Factory.

<!-- 22 -->
### <a name="are-there-any-plans-to-support-power-bi-deployment-pipelines-or-a-way-to-build-deployment-pipelines-for-pbi-reports-similar-to-extensions-or-maybe-even-a-simple-api-in-the-business-admin-center"></a>È previsto il supporto di pipeline di distribuzione di Power BI o un modo per creare pipeline di distribuzione per report PBI, simili alle estensioni? O forse anche una semplice API nell'interfaccia di amministrazione Business? 

Stiamo esaminando questa funzionalità. Power BI offre API complete per controllare le distribuzioni di report. Per ulteriori informazioni, vedi [Introduzione alle pipeline di distribuzione](/power-bi/create-reports/deployment-pipelines-overview).

### <a name="ive-tried-the-preview-of-the-new-connector-which-will-be-live-in-june-2021-i-see-some-values-like-_x0020_-when-connecting-to-api-v20-what-are-these-values"></a>Ho provato l'anteprima del nuovo connettore, che sarà disponibile a giugno 2021. Vedo alcuni valori come "_x0020_" durante la connessione ad API v2.0. Quali sono questi valori?

La prossima versione del connettore di Power BI consente di connettersi alle pagine API di Business Central, inclusa API v2.0. Queste pagine includono alcuni campi basati su [Oggetti AL Enum](/dynamics365/business-central/dev-itpro/developer/devenv-extensible-enums). I campi basati su oggetti AL Enum devono avere nomi coerenti e sempre uguali, in modo che i filtri nel report funzionino sempre, indipendentemente dalla lingua o dal sistema operativo in uso. Per questo motivo, i campi basati su AL Enum non vengono tradotti e sono codificati per evitare qualsiasi carattere speciale, incluso lo spazio. In particolare, ogni volta che è presente un'opzione vuota nell'oggetto AL Enum, è codificata in "_x0020_". Puoi sempre applicare una trasformazione ai tuoi dati su Power BI se desideri visualizzare un valore diverso per questi campi, ad esempio "Vuoto".


---

## <a name="see-also"></a>Vedere anche

[Licenze Power BI](admin-powerbi-setup.md#license)
[Introduzione a Business Central e a Power BI](admin-powerbi.md)  
[Panoramica dell'integrazione di Power BI](admin-powerbi-overview.md)  
[Abilitazione di Power BI in Business Central](admin-powerbi-setup.md)  
[Utilizzo dei report Power BI in Business Central](across-working-with-powerbi.md)  
[Utilizzo dei dati Business Central in Power BI](across-working-with-business-central-in-powerbi.md)  
[Creazione di report di Power BI per la visualizzazione di dati di Business Central](across-how-use-financials-data-source-powerbi.md)    
[Documentazione di Power BI](/power-bi/)  


[!INCLUDE[footer-include](includes/footer-banner.md)]