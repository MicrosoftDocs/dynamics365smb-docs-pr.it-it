---
title: Business Central per organizzazioni multisito e internazionali | Microsoft Docs
description: Business Central fornisce funzionalità che supportano un modello di business hub and spoke.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'hub-and-spoke, multi-site, headquarter, sites'
ms.date: 10/01/2020
ms.author: bholtorf
---

# <a name="business-central-for-multi-site-and-international-organizations"></a>Business Central per organizzazioni multisito e internazionali
Le organizzazioni con più siti utilizzano spesso un modello di business hub e spoke in cui una società madre, o sede centrale, gestisce tutte le operazioni dell'azienda mentre ogni sito funziona come una singola entità autonoma. I siti sono spesso distribuiti geograficamente e hanno esigenze diverse di condivisione delle informazioni con la sede centrale. Inoltre, i siti in genere non richiedono lo stesso livello di complessità e spesso mancano delle risorse per mantenere un sistema di grandi dimensioni.

[!INCLUDE[prod_short](includes/prod_short.md)] offre alle piccole e medie imprese una soluzione di gestione aziendale facile da usare e da mantenere a un basso costo di proprietà.

Questo articolo introduce alcuni dei modi in cui [!INCLUDE[prod_short](includes/prod_short.md)] supporta un modello di business hub e spoke.

## <a name="integrating-the-headquarter-company-and-the-sites"></a>Integrazione della sede centrale e dei siti

[!INCLUDE[prod_short](includes/prod_short.md)] può integrarsi con il sistema contabile della sede centrale, soddisfacendo al contempo le diverse esigenze dei diversi siti, indipendentemente dalle dimensioni, dall'ubicazione o dal tipo di attività.

Il diagramma seguente è un esempio di diversi siti integrati con una sede aziendale centrale.

![Descrizione diagramma generata automaticamente.](media/multisite-headquarter-sites.png)

## <a name="meet-the-needs-of-domestic-and-international-sites"></a>Soddisfare le esigenze dei siti nazionali e internazionali

Le esigenze aziendali nei diversi siti spesso differiscono in base al settore, ai metodi aziendali o al loro rapporto con la sede centrale. [!INCLUDE[prod_short](includes/prod_short.md)] può essere facilmente adattato ed esteso a vari tipi di attività commerciali e sedi. Microsoft AppSource offre una vasta gamma di app di Microsoft e dei nostri partner e i partner possono distribuire rapidamente [!INCLUDE[prod_short](includes/prod_short.md)] con interruzioni minime delle operazioni quotidiane.

Per le organizzazioni multinazionali, [!INCLUDE[prod_short](includes/prod_short.md)] supporta i requisiti legali e le pratiche commerciali locali.

* Per le versioni online, esistono più di [40 versioni nazionali localizzate](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json) che puoi installare come estensioni da Microsoft AppSource.  
* Per le versioni locali, [versioni nazionali](/azure/architecture/solution-ideas/articles/business-central) sono disponibili come versioni localizzate da Microsoft o come localizzazioni di componenti aggiuntivi gestite dai partner.

Una rete di oltre 4.000 partner Microsoft in tutto il mondo fornisce competenze locali.

| **Requisito di business** | **Come viene supportato da Business Central** | **Ulteriori informazioni** |
|-------------------------|-------------------------|-------------------------|
| Personalizza il sistema per adattarlo all'attività. | Goditi un sistema progettato fin dall'inizio per le aziende di medie dimensioni. | [Sintesi](https://dynamics.microsoft.com/business-central/overview/) |
| Affronta le pratiche normative e locali. | Rispetta i requisiti legali e le pratiche commerciali locali. | [Funzionalità locale](about-localization.md) |
| Accedi a più aziende da una singola pagina. | Ottieni un rapido accesso a qualsiasi società Business Central nella tua organizzazione. | [Hub aziendale](ui-extensions-company-hub.md) |
| Gestisci più lingue e valute. | Il supporto di più lingue e valute consente di soddisfare le esigenze locali. | [Funzionalità multilingue](about-locale-language.md)<br></br>[Funzionalità multivaluta](finance-how-setup-additional-currencies.md) |


## <a name="consolidate-financial-data"></a>Consolidare i dati finanziari

Un aspetto fondamentale del modello di business hub and spoke è la capacità della sede centrale e degli altri siti di scambiare dati finanziari, anche quando la sede centrale e gli altri siti utilizzano sistemi, strutture contabili, lingue e valute differenti.

| **Requisito di business** | **Come viene supportato da Business Central** | **Ulteriori informazioni** |
|-------------------------|-------------------------|-------------------------|
| Consolidare i dati finanziari dei siti. | Consolida i rendiconti finanziari dei siti, indipendentemente dal fatto che eseguano Business Central o un'altra applicazione, in un'unica entità aziendale (società). | [Consolidare dati finanziari di molteplici società](finance-consolidated-company-reporting.md) |
| Integrare le strutture contabili. | Trasferire i dati di consolidamento da diverse strutture contabili alla tua. Formato file integrato per F&O (disponibile con Wave 2, 2020) | [Importazione dei dati aziendali da altri sistemi contabili](across-import-data-configuration-packages.md)<br></br>[Preparare i conti di contabilità generale per il consolidamento](finance-consolidated-company-reporting-setup.md#glacc) |
| Effettuare transazioni in più valute. | Contribuire a garantire che i rendiconti finanziari in valute diverse siano accurati e utilizzino tassi di cambio corretti. | [Aggiornare i tassi di cambio valuta](finance-how-update-currencies.md) |

## <a name="share-business-insight-with-integrated-analytics"></a>Condividere le informazioni aziendali con l'analisi integrata

Allineare l'organizzazione ai propri obiettivi di business fornendo una comprensione generale della realtà attuale. L'analisi integrata può aiutare le persone a basare le proprie decisioni sullo stesso insieme di fatti.

| **Requisito di business** | **Come viene supportato da Business Central** | **Ulteriori informazioni** |
|-------------------------|-------------------------|-------------------------|
| Condividere le informazioni con i siti senza un supporto IT completo. | Creare KPI e dashboard di business intelligence in Power BI basati sui dati. | [Utilizzare i dati Business Central in Power BI](across-working-with-business-central-in-powerbi.md) |
| Sviluppare rapporti finanziari personalizzati. | Generare report finanziari basati su parametri. | [Business Intelligence](bi.md) |
| Allinearsi ai fatti. | Generare, visualizzare e condividere report con le parti interessate interne ed esterne. | [Report finanziari](finance-reports.md) |
| Analizzare dati in Excel. | Cercare i fatti, risolvere i problemi ed eseguire analisi ad hoc in Microsoft Excel. | [Analizzare i rendiconti finanziari in Excel](finance-analyze-excel.md) |


## <a name="exchange-data-using-apis-and-xmlports"></a>Scambiare dati utilizzando API e XMLports

API e XMLport semplificano il processo di connessione delle istanze di [!INCLUDE[prod_short](includes/prod_short.md)], comprese quelle che sono state personalizzate per ogni sito.

| **Requisito di business** | **Come viene supportato da Business Central** | **Ulteriori informazioni** |
|-------------------------|-------------------------|-------------------------|
| Collegare versioni personalizzate tra i siti e la sede centrale. | Le pagine API possono esporre qualsiasi rappresentazione di un'entità, comprese le sue personalizzazioni. | [Abilitazione delle API per Business Central](/dynamics-nav/enabling-apis-for-dynamics-nav) |
| Controllo delle versioni e sicurezza. | Le API utilizzano ODataV4, che fornisce controllo delle versioni, webhook e rilevamento delle modifiche. | [Sicurezza e protezione](/dynamics365/business-central/dev-itpro/security/security-and-protection) |
| Registrare e importare documenti XML. | Le codeunit possono essere esposte come azioni non associate per supportare la registrazione e l'importazione di documenti XML. Per l'elaborazione di documenti XML, è possibile applicare XMLports. Le azioni non associate sono anche in grado di generare un documento XML o JSON. | [Oggetti XMLport](/dynamics365/business-central/dev-itpro/developer/devenv-xmlport-object) |
| Semplificare la manutenzione attraverso lo scambio elettronico dei dati. | È possibile aggiungere una soluzione di scambio elettronico dei dati per utilizzarla come livello di integrazione tra la sede centrale e i siti. | [Framework di scambio dei dati](across-about-the-data-exchange-framework.md) |
| Scambiare dati tra diversi sistemi. | Utilizzare XMLports per creare documenti XML, che possono quindi essere scambiati tra una sede centrale che utilizza un sistema e siti che utilizzano Business Central. | [Panoramica di XMLport](/dynamics365/business-central/dev-itpro/developer/devenv-xmlport-overview) |
| Orchestrare scambi di dati complessi. | Utilizzare una combinazione di XMLports con Business Central e server Microsoft BizTalk per soddisfare le esigenze specifiche dei tuoi siti.</br>Per esigenze complesse, utilizzare una soluzione di scambio dati elettronici basata su server BizTalk e Commerce Gateway in Business Central in combinazione con XMLports. | [Utilizzare report, processi batch e XMLport](ui-work-report.md) |
| Connettersi a soluzioni e servizi di <sup></sup>terze parti. | Le API stabiliscono una connessione punto a punto tra Business Central e soluzioni e servizi di<sup></sup> terze parti. | [API v2.0](/dynamics-nav/api-reference/v2.0/) |


## <a name="promote-an-efficient-intercompany-supply-chain"></a>Promuovere una catena di approvvigionamento interaziendale efficiente

I siti hanno spesso bisogno di accedere alla catena di approvvigionamento e della capacità di gestirne alcuni aspetti. Ad esempio, i siti potrebbero utilizzare lo stesso fornitore, ma gestirne le risorse e le sedi fisiche separatamente.

| **Requisito di business** | **Come viene supportato da Business Central** | **Ulteriori informazioni** |
|-------------------------|-------------------------|-------------------------|
| Gestire le transazioni tra le divisioni come normali transazioni di vendita e acquisto. | Utilizzare le registrazioni interaziendali per creare documenti di vendita e acquisto e movimenti C/G per interi flussi di lavoro e per più di una società alla volta per eliminare l'immissione di dati duplicati. | [Gestione delle transazioni interaziendali](intercompany-manage.md) |
| Usare processi senza documenti cartacei. | Evitare i costi di invio, ricezione e stampa di documenti. | [Documenti in entrata](across-income-documents.md)<br><br> [Gestire allegati, collegamenti e note in schede e documenti](ui-how-add-link-to-record.md) |

## <a name="respond-quickly-to-new-business-conditions"></a>Rispondere rapidamente alle nuove condizioni commerciali

La sede centrale deve essere in grado di reagire rapidamente ai cambiamenti aziendali in ogni sito. In combinazione con Power Automate, [!INCLUDE[prod_short](includes/prod_short.md)] può fungere da meccanismo di allarme anticipato.

![Viene generato automaticamente uno screenshot della descrizione di un post sui social media.](media/multisite-apps.png)

| **Requisito di business** | **Come viene supportato da Business Central** | **Ulteriori informazioni** |
|-------------------------|-------------------------|-------------------------|
| Generare automaticamente avvisi e-mail. | Impostare avvisi in Power Automate che genereranno messaggi di posta elettronica per ricevere informazioni in merito al condizioni aziendali critiche nelle sedi o presso i partner della catena di fornitura. | [Business Central e Power BI](admin-powerbi.md) |
| Usare avvisi standard o personalizzati. | Utilizzare 12 diversi modelli inclusi per Business Central o impostare gli avvisi per adattarli alla propria attività. | [Usare Business Central in un flusso di lavoro automatizzato](across-how-use-financials-data-source-flow.md) |

## <a name="see-also"></a>Vedere anche
[Amministrazione di Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
