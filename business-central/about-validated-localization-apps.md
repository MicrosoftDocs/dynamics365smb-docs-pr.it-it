---
title: Sviluppo di app di localizzazione convalidate
description: Rispettare i requisiti normativi in Dynamics 365 Business Central come app di localizzazione convalidata.
author: altotovi
ms.date: 06/04/2024
ms.reviewer: bholtorf
ms.topic: conceptual
ms.author: altotovi
---

# <a name="development-of-validated-localization-apps"></a>Sviluppo di app di localizzazione convalidate

Questo articolo descrive i requisiti e le linee guida per lo sviluppo di un'app di localizzazione convalidata per [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="what-is-a-validated-localization-app"></a>Che cos'è un'app di localizzazione convalidata?

[!INCLUDE[prod_short](includes/prod_short.md)] è disponibile [a livello globale in oltre 170 mercati](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json). In una serie di mercati, Microsoft collabora con i partner ISV per la localizzazione [!INCLUDE[prod_short](includes/prod_short.md)] tramite app di localizzazione disponibili su [Microsoft AppSource](https://go.microsoft.com/fwlink/?linkid=2081646). Per tali regioni, le localizzazioni possono essere disponibili tramite il programma dell'app di localizzazione preferito. Il programma delle app di localizzazione preferite riconosce le app create secondo le linee guida sulla qualità specifiche di Microsoft. I partner ISV che rispettano i requisiti e le linee guida del programma possono trarre vantaggi tecnici e commerciali per servire i propri rivenditori e clienti.  

Nelle sezioni seguenti sono disponibili requisiti e linee guida. Puoi contattare il team del programma se desideri partecipare a questo programma e soddisfare i requisiti seguenti contattandoci tramite il [team di localizzazione Microsoft](mailto:d365bcloc@microsoft.com).   

> [!IMPORTANT]
> L'iniziativa per le app di localizzazione [!INCLUDE[prod_short](includes/prod_short.md)] convalidate è attualmente in fase di implementazione come programma pilota. I requisiti e i vantaggi indicati di seguito possono cambiare in base al feedback del partner e dei clienti.  

Le app che fanno parte del programma pilota di localizzazione convalidato contengono una serie di funzionalità che soddisfano i requisiti normativi locali che rientrano in una delle categorie nell'elenco seguente.  

- **Requisiti normativi**: funzionalità locale che aiuta le aziende a soddisfare i propri requisiti legali, come reporting fiscale, formati di fatturazione elettronica locali, GAAP locali e altri requisiti normativi.
- **Requisito degli standard nazionali**: funzionalità locale che soddisfa gli standard locali, come formati di indirizzi, formati bancari nazionali o interpretazioni locali di standard globali.
- **Lingua locale**: lingua locale nell'app di localizzazione, ma anche per un'app di base se questa lingua non è attualmente nell'elenco delle [lingue supportate](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json).

> [!NOTE]
> Le esigenze del mercato locale o i requisiti del settore non dovrebbero essere inclusi nelle app di localizzazione preferite. Se le app contengono queste funzionalità, non possono essere approvate come app di localizzazione convalidata.

> [!NOTE]
> Le funzionalità locali sono vantaggiose per la produttività dei processi aziendali in un paese e quindi aggiungono valore al business, ma non sono richieste da un punto di vista normativo, come formati bancari e di pagamento specifici, note spese, funzionalità HR, buste paga e simili più o meno grandi, e le funzionalità utili dovrebbero essere isolate in altre app. Se le app contengono queste funzionalità, non possono essere approvate come app di localizzazione convalidate.   

## <a name="validated-localization-app-business-requirements"></a>Requisiti aziendali dell'app di localizzazione convalidata

- Il provider dell'app di localizzazione convalidata soddisfa tutti i requisiti per essere un provider CSP indiretto.  
- Il fornitore dell'app di localizzazione convalidata porta sul mercato un minimo di offerte in cinque paesi/aree, che raggruppano Dynamics 365 Business Central con un'app di localizzazione convalidata. 
- Il fornitore dell'app di localizzazione convalidata ha un minimo di 10 clienti online [!INCLUDE[prod_short](includes/prod_short.md)] con ambienti di produzione, che utilizzano attivamente l'app di localizzazione convalidata. 
- Il fornitore dell'app di localizzazione convalidata presenta un piano aziendale su base annuale al v-team del programma. Ciò include attività di marketing e preparazione pianificate per promuovere l'offerta in bundle con i rivenditori indiretti CSP nei paesi o nelle aree geografiche applicabili. Il piano può essere presentato all'inizio di ogni trimestre al [Team di localizzazione Microsoft](mailto:d365bcloc@microsoft.com).  
- Le app di localizzazione convalidate vengono messe a disposizione di tutti i clienti e partner che desiderano trarne vantaggio.     
- Il fornitore dell'app di localizzazione convalidata si impegna in flussi di lavoro ricorrenti con Microsoft.

## <a name="validated-localization-app-functional-and-technical-requirements"></a>Requisiti tecnici e funzionali dell'app di localizzazione convalidata

### <a name="functionality-requirements"></a>Requisiti di funzionalità

Oltre a soddisfare i requisiti tecnici per l'app di localizzazione preferita, l'ambito minimo del prodotto praticabile per l'app di localizzazione preferita è:  

- Funzionalità relative alle normative locali:   
  - Requisiti legali.   
  - Funzionalità ufficialmente obbligatorie. 
  - Funzionalità solo orizzontali (non specifiche del settore).  
  - Applicabile nella maggior parte delle aziende.  
  - All'interno del seguente Blueprint:   
    - Aree delle modifiche legislative più frequenti. 
    - Già tracciato come localizzazione nelle localizzazioni Microsoft. 
    - Riferimenti alle funzionalità: raramente nuovi.  
    - Nessun formato specifico per fornitore/banca, buste paga o simili. 
    - Nessuna funzionalità globale se non è creata da Microsoft. 
- Traduzioni: 
  - Traduzione di un'app di localizzazione nelle lingue locali. 
  - Traduzione di un'app di base nelle lingue locali, se la lingua non è già [ supportata](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json).  
  - Traduzione della documentazione dell'app di localizzazione nelle lingue locali. 
- Anche se fanno entrambe parte della localizzazione, è consigliabile che le funzionalità standard nazionali (parte locale) siano create come app separate dalle funzionalità normative locali. 
- Dati dimostrativi nella lingua locale applicabili per il mercato specifico.   
- Tutte le funzionalità devono essere progettate per mantenere un'interfaccia utente semplificata; tieni presente che sono destinate principalmente al mercato delle PMI.  
- Evitare di creare nuove funzionalità se le stesse funzionalità o simili esistono già nell'app di base, come fatturazione elettronica, esportazioni di controllo, funzionalità IVA, scambio di dati e altre in cui la maggior parte delle funzionalità è comune a tutti i paesi o aree geografiche ma esistono alcune regole locali o formati aziendali che sono estensioni di strutture o formati globali. Invece di creare nuove funzionalità, estendi quelle esistenti.  
- Prepara guide di configurazione (procedure guidate) per aree complesse da configurare per aiutare gli utenti ad abilitare, scoprire e avere una buona prima esperienza con l'app di localizzazione.  
- I partner devono fornire la documentazione funzionale per tutti gli aspetti della loro localizzazione.  

### <a name="technical-requirements"></a>Requisiti tecnici

Di seguito è riportato un elenco di controllo di tutti i requisiti che è necessario soddisfare prima di inviare l'app per la localizzazione convalidata come estensione per la convalida. Questo elenco non modifica l' [elenco di convalida tecnica](/dynamics365/business-central/dev-itpro/developer/devenv-checklist-submission) e si limita ad estendere i requisiti da lì.  

- I fornitori dell'app di localizzazione convalidata devono creare l'app di localizzazione convalidata in base all'app di base W1.  
- I fornitori di app di localizzazione convalidata devono seguire il ciclo di vita e i criteri di supporto di Microsoft.   
- L'automazione obbligatoria dei test deve coprire almeno l'80% del codice e di tutti i processi aziendali che cambiano con l'app Localizzazione convalidata devono essere coperti dall'automazione dei test.  
- I fornitori dell'app di localizzazione convalidata devono aggiornare e/o testare l'app di localizzazione convalidata prima del lancio ufficiale della nuova versione (minimo con RC prima della nuova versione) per confermare che non vi siano problemi. 
- Tutti gli oggetti nel codice dell'app di localizzazione convalidata devono essere in inglese.   
- I fornitori di app di localizzazione convalidata devono seguire i criteri Microsoft per gli oggetti obsoleti, le modifiche sostanziali e le procedure consigliate per la deprecazione del codice AL.  
- I fornitori di app di localizzazione convalidata dovrebbero aggiungere nuovi eventi se richiesto dal mercato (altri partner di implementazione o clienti) se ciò ha un ragionevole senso commerciale, seguendo i criteri e le pratiche di Microsoft. In caso contrario, i fornitori di app di localizzazione convalidate devono fornire una risposta a tali richieste con un'adeguata giustificazione del motivo per cui non ha ragionevole senso commerciale aggiungerle. 
- I fornitori di app di localizzazione convalidata devono fornire scenari di test scritti in inglese e consentire a Microsoft di eseguire test manuali se richiesto da Microsoft.  
- Se un'app di localizzazione convalidata estende il modello dati di [!INCLUDE[prod_short](includes/prod_short.md)] con nuove tabelle e/o campi, il fornitore dell'app di localizzazione convalidata deve impostare la proprietà **DataClassification** correttamente.

> [!NOTE]  
> Puoi anche creare un'integrazione se ritieni vantaggioso avere alcune funzionalità posizionate all'esterno dell'ambiente [!INCLUDE[prod_short](includes/prod_short.md)] e connetterti invece a [!INCLUDE[prod_short](includes/prod_short.md)] utilizzando ad esempio API o servizi Web.

## <a name="see-also"></a>Vedere anche

[Convalida tecnica](/dynamics365/business-central/dev-itpro/developer/devenv-checklist-submission)  
[Sviluppo di una soluzione di localizzazione standard](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-develop-localization)  
[Disponibilità nazionale/regionale e lingue supportate](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations)  
[Cos'è la funzionalità locale in Dynamics 365 [!INCLUDE[prod_short](includes/prod_short.md)]?](about-localization.md)  
[Disponibilità internazionale di Microsoft Dynamics 365](/dynamics365/get-started/availability)  
[Panoramica della conformità](compliance/compliance-overview.md)  
[Disponibilità geografica per Dynamics 365](https://dynamics.microsoft.com/en-us/availability-reports/georeport/)  
