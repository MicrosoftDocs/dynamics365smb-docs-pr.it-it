---
title: Impostare e creare report Intrastat| Microsoft Docs
description: Informazioni su come impostare le funzionalità di reporting Intrastat e come segnalare le attività commerciali con società in altri paesi UE.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, Intrastat, trade, EU, European Union
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: f0c10948aef6db58474de5c627e1ce82f0a13102
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3920524"
---
# <a name="set-up-and-report-intrastat"></a>Impostare e registrare report Intrastat
Tutte le società dell'Unione Europea devono creare report relativi alle attività commerciali con altri paesi UE. È necessario presentare ogni mese alle autorità statistiche del proprio paese report relativi al movimento delle merci, che devono quindi essere inviati alle autorità fiscali. Questa operazione è detta reporting Intrastat. Per compilare i report Intrastat periodici si utilizza la pagina **Registrazioni Intrastat**.  

## <a name="required-and-optional-setups"></a>Configurazioni obbligatorie e facoltative
Prima di poter usare la registrazione Intrastat per dichiarare le informazioni Intrastat, è necessario impostare varie opzioni:  

* **Setup Intrastat**: la pagina Setup Intrastat consente di abilitare il reporting Intrastat e impostare i relativi valori predefiniti. È possibile specificare se è necessario creare report Intrastat da spedizioni (invii), entrate (arrivi) o entrambi a seconda delle soglie impostate in base alle normative locali. È anche possibile impostare tipi di transazioni di default per documenti normali e di reso, utilizzati per la natura del reporting delle transazioni.
* **Definizioni di registrazioni Intrastat**: è necessario impostare le definizioni di registrazioni Intrastat e i batch che verranno utilizzati. Poiché il report Intrastat viene creato mensilmente, è necessario creare 12 batch di registrazioni Intrastat basati sulla stessa definizione.  
* **Codici voce doganale**: le autorità doganali e fiscali hanno stabilito codici numerici che classificano gli articoli e i servizi. Specificare questi codici negli articoli.
* **Codici natura transazione**: i paesi e le aree hanno codici differenti per la natura delle transazioni Intrastat, ad esempio acquisto o vendita ordinaria, cambio di merce resa e sostituzione di merce non resa. Impostare tutti codici che si applicano al proprio paese. È possibile utilizzare questi codici nei documenti di vendita e di acquisto e quando si elaborano i resi.  
* **Metodi di trasporto**: sono disponibili sette codici di una cifra per i metodi di trasporto Intrastat. **1** via mare, **2** via ferrovia, **3** su strada, **4** via area, **5** per posta, **7** per installazioni fisse e **9** con proprio mezzo (ad esempio il trasporto con la propria auto). [!INCLUDE[d365fin](includes/d365fin_md.md)] non richiede tali codici, tuttavia, si consiglia di inserire descrizioni con un significato simile a questi codici.  

Facoltativamente è anche possibile impostare le opzioni seguenti:

* **Cod. paese destin./proven.**: utilizzare a completamento delle descrizioni della natura delle transazioni.  
* **Aree**: utilizzare a completamento delle informazioni sui paesi e le aree.  
* **Cod. spedizione Intrastat**: utilizzare per specificare le ubicazioni da cui si spediscono o si ricevono gli articoli da o verso altri paesi. Un esempio di codice di spedizione Intrastat è l'aeroporto di Heathrow. I codici di spedizione Intrastat possono essere immessi nei documenti di vendita e di acquisto nella Scheda dettaglio **Commercio estero**. Queste informazioni vengono inoltre copiate dai movimenti articoli creati per le registrazioni Intrastat.  

### <a name="to-set-up-intrastat-templates-and-batches"></a>Per impostare le definizioni e i batch di registrazioni Intrastat
I processi batch Intrastat includono solo i movimenti articoli, non i movimenti di contabilità generale. Se nella contabilità generale sono presenti movimenti adatti per il reporting Intrastat, è necessario immetterli manualmente. Ad esempio, se si acquista un computer da un altro paese UE o un'altra area UE, il computer non viene inserito nell'inventario, ma registrato in un conto di contabilità generale. Questo tipo di movimento deve essere immesso manualmente nella registrazione Intrastat.  

È possibile esportare i movimenti in un file da inviare successivamente alle autorità Intrastat. È inoltre possibile stampare un report manualmente, immettere le informazioni nei moduli delle autorità, quindi inviare le informazioni.

> [!Note]
> È consigliabile impostare un batch Registrazione Intrastat per ogni mese.  

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Definizioni registrazioni Intrastat** e quindi scegliere il collegamento correlato.  
2. Compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]. Creare una definizione per ogni modulo Intrastat che si utilizza.  
3. Per creare batch, scegliere l'azione **Batch**.  
4. Compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]. Creare una definizione per ogni modulo Intrastat che si utilizza. 

> [!Note]
> Nel campo **Periodo statistico** immettere il periodo statistico sotto forma di numero a quattro cifre, dove le prime due rappresentano l'anno e le altre due il mese. Immettere, ad esempio, 1706 per indicare giugno 2017.

### <a name="to-set-up-commodity-codes"></a>Per impostare i codici di voci doganali
Tutti gli articoli acquistati o venduti devono disporre di un codice voce doganale.  

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Codici voci doganali** e quindi scegliere il collegamento correlato.  
2. Compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Per assegnare un codice voce doganale a un articolo, nella pagina **Scheda articolo** espandere la Scheda dettaglio **Costi e registrazione**, quindi immettere il codice nel campo **Codice voce doganale**.   

### <a name="to-set-up-transaction-nature-codes"></a>Per impostare il codici della natura delle transazioni
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Codici natura transazione** e quindi scegliere il collegamento correlato.  
2. Compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

> [!Tip]
> Se si utilizza con frequenza un determinato codice natura transazione, è possibile impostarlo come predefinito. A tale scopo, andare alla pagina **Impostazione Intrastat** e selezionare il codice.

### <a name="to-set-up-transport-methods"></a>Per impostare i metodi di trasporto
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Metodi di trasporto** e quindi scegliere il collegamento correlato.  
2. Compilare i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="to-set-up-which-intrastat-report-fields-are-mandatory"></a>Per impostare quali campi del report Intrastat sono obbligatori
In alcuni paesi, come Spagna e Regno Unito, le autorità richiedono che i report Intrastat includano, ad esempio, il metodo di spedizione per gli acquisti o altri valori quando le vendite superano una certa soglia. Nella pagina **Setup Intrastat** è possibile selezionare **Setup checklist Intrastat** per impostare i campi obbligatori nella pagina **Registrazioni Intrastat**.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup Intrastat** e quindi scegliere il collegamento correlato.
2. Scegliere l'azione **Setup checklist Intrastat**.
3. Nella pagina **Setup checklist Intrastat**, fare clic su **Nome campo** per selezionare il campo del report Intrastat che si desidera rendere obbligatorio.

## <a name="to-report-intrastat"></a>Per creare un report Intrastat
Dopo aver compilato le registrazioni Intrastat, è possibile eseguire l'azione **Report Intrastat - Checklist** per verificare che tutte le informazioni nelle registrazioni siano corrette. I campi obbligatori impostati nella pagina **Setup checklist Intrastat** in cui mancano i valori verranno mostrati in Dettaglio informazioni di Errori e e avvisi nella pagina **Registrazioni Intrastat**. È successivamente possibile stampare un report Intrastat come form, oppure creare un file da inviare a un'autorità fiscale del proprio paese.  

### <a name="to-fill-in-intrastat-journals"></a>Per compilare le registrazioni Intrastat  
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Registrazioni Intrastat** e quindi scegliere il collegamento correlato.  
2. Nella pagina **Registrazioni Intrastat**, nel campo **Nome batch** scegliere il batch di registrazioni interessato e quindi scegliere **OK**.  
3. Scegliere l'azione **Suggerisci righe**. I campi **Data inizio** e **Data fine** verranno compilati automaticamente con le date specificate per il periodo statistico del batch di registrazioni.  
4. Nel campo **% regolazione costi** è possibile immettere una percentuale per coprire trasporto e assicurazione. In questo caso il valore contenuto del campo **Valore Statistico** sarà proporzionalmente maggiore.  
5. Selezionare **OK** per avviare il processo batch.  

Il processo batch recupererà tutti i movimenti articolo nel periodo statistico indicato e li inserirà come righe nelle registrazioni Intrastat. Le righe possono essere modificate secondo le esigenze.  

> [!IMPORTANT]  
>  Il processo batch recupera soltanto i movimenti che contengono un codice paese per il quale è stato immesso un codice Intrastat nella pagina **Paesi**. È quindi importante immettere codici Intrastat per i codici paese che verranno inclusi nel processo batch.  

### <a name="report-intrastat-on-a-form-or-a-file"></a>Creare report Intrastat come form o come file
Per ottenere le informazioni richieste nel modulo Intrastat dagli enti di statistica, è necessario stampare il report **Intrastat - Form**. Prima di eseguire questa operazione, è necessario preparare le registrazioni Intrastat e compilarle. Se vi sono sia transazioni di vendita che di acquisto, è necessario compilare un form separato per ciascun tipo e stampare il report due volte.  

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Registrazioni Intrastat** e quindi scegliere il collegamento correlato.  
2. Nella pagina **Registrazioni Intrastat** selezionare il batch registrazioni desiderato nel campo **Nome batch**.  
3. Se non è stato fatto in precedenza, compilare le registrazioni manualmente o scegliere l'azione **Suggerisci righe**.  
4. Scegliere l'azione **Stampa registrazione Intrastat**.  
5. Nella Scheda dettaglio **Righe reg. Intrastat** aggiungere un filtro **Tipo**, quindi specificare se si tratta di **Carico** o **Spedizione**.  
6. Per stampare il report, fare clic su **Invia a**.  

### <a name="report-intrastat-in-a-file"></a>Creare un report Intrastat in un file
È possibile inviare il report Intrastat come file. Prima di creare il file è possibile stampare un report di controllo che conterrà le stesse informazioni presenti nel file.  

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Registrazioni Intrastat** e quindi scegliere il collegamento correlato.  
2. Nella pagina **Registrazioni Intrastat** selezionare il batch registrazioni desiderato nel campo **Nome batch**.  
3. Se non è stato fatto in precedenza, compilare le registrazioni manualmente o scegliendo l'azione **Suggerisci righe**.  
4. Scegliere l'azione **Crea file**.  
5. Nella pagina del processo batch scegliere il pulsante **OK**.  
6. Selezionare **Salva**.  
7. Spostarsi sul percorso in cui si desidera salvare il file, quindi immettere il nome file desiderato e fare clic su **Salva**.

## <a name="reorganize-intrastat-journals"></a>Riorganizzare registrazioni Intrastat
I report Intrastat vengono presentati con cadenza mensile e per ogni report è necessario creare un nuovo batch di registrazioni. Dopo un certo periodo, si saranno accumulati diversi batch di registrazioni. Le righe di registrazioni non vengono eliminate automaticamente. È possibile riorganizzare periodicamente i nomi batch contabili. Questa operazione viene effettuata eliminando i batch di registrazioni non più necessari. Vengono eliminate anche le righe di registrazioni di questi batch.  

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Registrazioni Intrastat** e quindi scegliere il collegamento correlato.  
2. Per visualizzare le opzioni, scegliere il campo **Nome batch**.  
3. Scegliere i batch registrazioni da eliminare a quindi scegliere il pulsante **Elimina**.  

## <a name="tariff-numbers"></a>Nomenclatura combinata

In molti paesi, le autorità doganali e fiscali hanno stabilito dei codici a otto cifre per i vari articoli. Perché i movimenti degli articoli contengano le necessarie informazioni quando vengono importati nella riga delle registrazioni Intrastat, è necessario che nella pagina **Nomenclature combinate** vengano specificate le opportune informazioni sulle nomenclature combinate. È necessario trovare i codici degli articoli di cui si occupa la propria società e immetterli nella pagina **Nomenclatura combinata**.

Impostare nella pagina **Nomenclature combinate** tutti i codici utilizzati. Prima di iniziare la registrazione è necessario immettere i codici nella scheda articolo. Una volta impostati, immetterli nel campo **Nomenclatura combinata** della scheda articolo. Compilare anche il campo **Peso netto** della scheda articolo.

## <a name="see-related-training-at-microsoft-learn"></a>Vedere le informazioni relative al training in [Microsoft Learn](/learn/modules/process-intrastat-dynamics-365-business-central/index)

## <a name="see-also"></a>Vedere anche
[Gestione contabile](finance.md)
