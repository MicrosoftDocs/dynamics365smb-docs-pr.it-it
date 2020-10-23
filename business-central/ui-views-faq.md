---
title: Domande frequenti sulle visualizzazioni elenco
description: Informazioni dettagliate sul salvataggio di filtri come visualizzazioni elenco.
author: mikebcMSFT
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: list, filter, pane, views
ms.date: 10/01/2020
ms.author: mikebc
ms.openlocfilehash: 7b992fe4f5db07605015a88ea69d9a510adbcca4
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3925507"
---
# <a name="list-views-faq"></a>Domande frequenti sulle visualizzazioni elenco
Questo argomento contiene le risposte alle domande più frequenti sull'utilizzo di visualizzazioni elenco e sul salvataggio di filtri poste da utenti esperti.  

### <a name="how-do-views-handle-expressions"></a>In che modo le visualizzazioni gestiscono le espressioni?
Quando si salva una visualizzazione che include filtri con espressioni, come intervalli di date, operatori, parole chiave o token di filtro, viene salvata l'espressione ma non i valori risultanti. Ad esempio, il salvataggio di una visualizzazione che filtra in base al campo **Data di creazione** con l'espressione **-1W..today** troverà sempre record relativi alla data corrente, anche quando alla visualizzazione si accede il mese successivo.

### <a name="where-are-list-views-saved"></a>Dove vengono salvate le visualizzazioni elenco?
Analogamente alle operazioni eseguite per nascondere un campo o riorganizzare il menu di navigazione, le visualizzazioni elenco fanno parte della personalizzazione dell'utente e sono archiviate nel database. L'annullamento dell'intera personalizzazione in un elenco rimuoverà in modo permanente anche le visualizzazioni personali e ulteriori personalizzazioni come il riordino delle visualizzazioni. Per ulteriori informazioni, vedere [Personalizzare l'area di lavoro](ui-personalization-user.md).

### <a name="why-dont-i-have-a-save-icon"></a>Perché non è presente un'icona Salva?
L'icona Salva e il menu delle opzioni non sono visualizzati insieme alle visualizzazioni nel riquadro filtri se la personalizzazione è disabilitata per un ruolo utente. Gli utenti che non hanno la personalizzazione abilitata sono comunque in grado di accedere alle visualizzazioni di sistema che sono una parte standard della pagina, nonché di modificare o creare altri filtri.

### <a name="on-which-page-types-can-i-use-list-views"></a>In quali tipi di pagina è possibile utilizzare visualizzazioni elenco?
Le visualizzazioni sono disponibili solo nelle pagine di elenchi e fogli di lavoro.

### <a name="are-views-also-available-on-other-form-factors"></a>Le visualizzazioni sono disponibili anche in altri fattori di forma?
Sì. Tutte le visualizzazioni salvate nel browser desktop o nell'applicazione desktop saranno disponibili anche nel tablet o nello smartphone. Non è possibile modificare o personalizzare visualizzazioni in dispositivi mobili.

### <a name="are-my-personal-views-always-accessible"></a>Le visualizzazioni personali sono sempre accessibili?
Le stesse visualizzazioni sono disponibili in una pagina di elenco se vi si accede dal menu di navigazione, tramite la finestra della **funzionalità delle informazioni** o tramite un collegamento URL alla pagina elenco. Le visualizzazioni non sono disponibili in parti di elenco, ricerche o ogni volta che una pagina di elenco viene visualizzata come finestra di dialogo.

### <a name="how-do-i-return-a-view-to-its-original-filters-after-modifying-them"></a>Come è possibile ripristinare i filtri originali di una visualizzazione dopo averli modificati?
Nella parte inferiore del riquadro filtri, selezionare l'azione **Reimposta filtri** per annullare le modifiche ai filtri apportate alla visualizzazione e ripristinare i campi filtrati e i criteri di filtro originali.

### <a name="what-is-the-difference-between-hiding-and-removing-views"></a>Qual è la differenza tra nascondere e rimuovere le visualizzazioni?
La rimozione di una visualizzazione eliminerà definitivamente quella visualizzazione. Quando si nasconde una visualizzazione, questa viene rimossa temporaneamente dal riquadro filtri, ma è possibile renderla di nuovo visibile in seguito scegliendo l'azione **Mostra**.

### <a name="how-can-i-share-my-views-with-others"></a>Come è possibile condividere le visualizzazioni con altri utenti?
[!INCLUDE[d365fin](includes/d365fin_md.md)] non fornisce un modo di condividere la visualizzazione elenco precisa, ma è possibile condividere i filtri correnti di modo che altri utenti possano visualizzare un elenco di record simile. Nel browser desktop, copiare semplicemente l'URL e condividerlo con i colleghi. La condivisione dei filtri non garantisce al destinatario un set di filtri identico a quello visualizzato nel proprio browser.

### <a name="can-i-search-for-views-in-the-tell-me-window"></a>È possibile cercare visualizzazioni nella finestra della funzionalità delle informazioni?
No. La finestra della **funzionalità delle informazioni** visualizza solo i risultati della ricerca per la pagina, ma è comunque possibile accedere alla visualizzazione preferita dalla pagina.

### <a name="what-is-shared-layout"></a>Cos'è un layout condiviso?
Tutte le visualizzazioni in una pagina di elenco condividono un layout di colonna comune che include le colonne che vengono visualizzate, la relativa sequenza, larghezza, riquadro di blocco e impostazioni Accesso rapido. La personalizzazione di qualsiasi layout di colonna influirà anche su altre visualizzazioni che condividono lo stesso layout nella pagina di elenco.

Alcune visualizzazioni di sistema possono avere layout univoci delle colonne nell'elenco. Ad esempio, potrebbero riorganizzare le colonne per visualizzare solo le colonne più pertinenti a quella visualizzazione. È possibile identificare quali visualizzazioni hanno layout univoci scegliendo l'icona ![Mostra altre opzioni](media/show-more-options-icon.png "Mostra altre opzioni") e deselezionando la casella di controllo **Layout condiviso** se questa è selezionata. Come utente, è possibile personalizzare il layout di colonna di una visualizzazione con un layout univoco senza che ciò influisca sulle altre visualizzazioni nella pagina di elenco. Solo gli sviluppatori possono definire un layout di colonna univoco per una visualizzazione che inizialmente ha un layout condiviso.

### <a name="what-does-the-show-system-filters-link-do"></a>Qual è la funzione del collegamento Mostra filtri di sistema?
In alcune pagine di elenco, il riquadro filtri visualizzerà **Mostra filtri di sistema** nella parte inferiore quando la pagina include filtri specificati dal sistema. Questi filtri speciali sono in genere utilizzati per visualizzare record basati sul contesto corrente, ad esempio quando un elenco di ordini deve essere filtrato per un cliente specifico.

I filtri di sistema sono impostati dagli sviluppatori utilizzando il gruppo di filtri 0. Per dettagli tecnici sui filtri di sistema, vedere [Metodo Filtergroup](/dynamics365/business-central/dev-itpro/developer/methods-auto/record/record-filtergroup-method)

### <a name="i-see-multiple-views-on-my-page-but-i-did-not-create-them-where-did-they-come-from"></a>La pagina contiene varie visualizzazioni non create dall'utente. Qual è la loro origine?
Le visualizzazioni presenti in un qualsiasi elenco sono una combinazione delle visualizzazioni personali e delle visualizzazioni di sistema. Le visualizzazioni di sistema possono essere originate dall'applicazione aziendale, dalle estensioni oppure possono essere specifiche del ruolo se l'elenco è stato personalizzato per il proprio ruolo.

### <a name="why-do-some-views-provide-fewer-options"></a>Perché alcune visualizzazioni presentano meno opzioni?
Alcune visualizzazioni forniscono solo l'opzione di salvare una copia della visualizzazione, mentre altre non consentono il salvataggio delle modifiche alla visualizzazione. Il modo in cui la visualizzazione è stata creata determina le opzioni disponibili per quella visualizzazione. Le visualizzazioni possono essere create in vari modi:
- Visualizzazioni personali salvate
- Visualizzazioni di sistema che sono una parte standard dell'applicazione aziendale o che vengono aggiunte dalle estensioni o dalle visualizzazioni specifiche del ruolo. A differenza delle visualizzazioni personali, non è possibile salvare le modifiche ai filtri nelle visualizzazioni di sistema.
- Visualizzazioni di sistema legacy che sono una parte standard dell'applicazione aziendale ma che sono state create utilizzando versioni precedenti di [!INCLUDE[d365fin](includes/d365fin_md.md)]. Queste visualizzazioni offrono molte meno opzioni. È possibile salvarle solo come nuova visualizzazione e non possono nemmeno essere nascoste o riordinate. Da notare che le visualizzazioni di sistema legacy verranno sospese in un futuro aggiornamento di [!INCLUDE[d365fin](includes/d365fin_md.md)].

### <a name="how-do-i-convert-legacy-system-views"></a>Come si convertono le visualizzazioni di sistema legacy?
Le visualizzazioni di sistema legacy sono visualizzazioni elenco che sono state create dagli sviluppatori nelle versioni precedenti di [!INCLUDE[d365fin](includes/d365fin_md.md)] mediante posizionamento delle stesse nella pagina Gestione ruolo utente. Queste visualizzazioni sono ora visualizzate direttamente nella pagina di elenco ma offrono un'esperienza meno qualitativa e un numero significativamente inferiore di opzioni. È possibile convertire una visualizzazione di sistema legacy in una visualizzazione personale completamente personalizzabile salvandola come nuova visualizzazione. Allo stesso modo, gli amministratori possono scegliere di convertire visualizzazioni di sistema legacy specifiche del ruolo personalizzando il ruolo utente e salvando la visualizzazione legacy come nuova visualizzazione specifica del ruolo.

Da notare che le visualizzazioni di sistema legacy verranno sospese in un futuro aggiornamento di [!INCLUDE[d365fin](includes/d365fin_md.md)].

### <a name="others-in-my-organization-need-similar-list-views-as-standard-what-can-i-do"></a>Altri utenti nell'organizzazione necessitano di visualizzazioni elenco simili. Come si deve procedere?
L'utilizzo di visualizzazioni personali è rapido ed efficace, ma [!INCLUDE[d365fin](includes/d365fin_md.md)] fornisce strumenti aggiuntivi per definire visualizzazioni elenco necessarie a ruoli utente specifici o a tutti gli utenti nell'organizzazione.
 - Gli sviluppatori possono personalizzare l'ambiente e creare visualizzazioni elenco nelle estensioni per tutti gli utenti nell'organizzazione.
 - Gli utenti non programmatori come gli amministratori o i responsabili di reparto possono creare visualizzazioni elenco specifiche del ruolo quando personalizzano un ruolo dalla pagina **Profili (ruoli)**.

### <a name="i-work-with-multiple-languages-how-do-i-translate-the-name-of-the-view"></a>Come è possibile tradurre il nome della visualizzazione?
Quando si salva una nuova visualizzazione o si rinomina una visualizzazione esistente, è necessario immettere un nome riconoscibile e significativo per quella visualizzazione. Il nome viene salvato per la lingua corrente e verrà visualizzato anche quando si utilizza [!INCLUDE[d365fin](includes/d365fin_md.md)] in altre lingue. Per fornire nomi di visualizzazioni tradotti, è necessario cambiare lingua nella pagina **Impostazioni personali** e quindi rinominare la visualizzazione. In questo modo, si memorizzerà il nome tradotto nella nuova lingua.

### <a name="do-views-with-expressions-work-in-all-languages"></a>Le visualizzazioni con espressioni sono utilizzabili con tutte le lingue?
Le espressioni che utilizzano solo simboli, come "**|**" o **..**, sono considerate sicure in qualsiasi lingua. Le visualizzazioni con espressioni che includono lettere, parole chiave o token di filtro sono utilizzabili solo con la lingua in cui sono state create.


### <a name="see-also"></a>Vedere anche  
[Salvare e personalizzare visualizzazioni elenco](ui-views.md)  
[Individuazione di funzionalità e informazioni](ui-search.md)    
[Ricerca, filtro e ordinamento](ui-enter-criteria-filters.md)  
