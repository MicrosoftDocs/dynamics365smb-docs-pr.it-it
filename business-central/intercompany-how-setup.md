---
title: Impostazione della registrazione delle transazioni intercompany | Documenti Microsoft
description: Creare i fornitori e i clienti intercompany come partner intercompany e impostare un piano dei conti intercompany.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: IC, group, consolidation, affiliate, subsidiary
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: e6f44cfc8dc5eb3591aadd520a4ec58086d5f823
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2019
ms.locfileid: "2300093"
---
# <a name="set-up-intercompany"></a>Impostare la contabilità interaziendale
Per inviare una transazione, ad esempio una riga registrazioni vendita, da una società e creare automaticamente la transazione corrispondente, ad esempio una riga registrazioni acquisto, per la società partner, le società interessate devono accettare un piano dei conti comune e un set di dimensioni da utilizzare per le transazioni intercompany. Il piano dei conti intercompany può essere dato, ad esempio, da una versione semplificata del piano dei conti della casa madre. Ogni società deve mappare il suo piano dei conti completo al piano dei conti intercompany comune e le sue dimensioni alle dimensioni intercompany.  

È inoltre necessario impostare un codice partner IC per ogni società partner, accettato da tutte le società, quindi assegnarlo alle schede clienti e fornitori rispettivamente compilando il campo **Codice partner IC**.  

Se si creano o si ricevono righe intercompany con articoli, è possibile utilizzare i propri numeri articolo oppure impostare i numeri articolo del partner per ogni articolo menzionato, nel campo **Nr. articolo fornitore** o nel campo **Nr. articolo comune** della scheda articolo. È inoltre possibile usare la funzione **Cross reference articolo**: per mappare i numeri di articolo alle descrizioni degli articoli dei partner IC, aprire la scheda di ciascun articolo e scegliere l'azione **Cross reference** per impostare i riferimenti incrociati tra le descrizioni degli articoli dell'utente e quelle del partner IC.  

Se si effettuano transazioni di vendita intercompany che includono risorse, è necessario compilare il campo **Nr. conto C/G acq. partner IC** della scheda risorsa per ogni risorsa interessata. Si tratta del numero del conto di contabilità generale intercompany in cui verrà contabilizzato l'importo di questa risorsa nella società partner. Per ulteriori informazioni, vedere [Impostare risorse](projects-how-setup-resources.md).

## <a name="to-set-up-companies-for-intercompany-transactions"></a>Per impostare le società per le transazioni intercompany
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Informazioni società** e quindi scegliere il collegamento correlato.  
2. Nella pagina **Informazioni società**, compilare i campi **Codice partner IC**, **Tipo casella in arrivo Intercompany** e **Dettagli casella in arrivo Intercompany**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-intercompany-partners"></a>Per impostare i partner IC
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Partner IC** e quindi scegliere il collegamento correlato.
2. Scegliere l'azione **Nuovo**.
3. Nella pagina **Partner IC** compilare i campi secondo le necessità.

## <a name="to-set-up-intercompany-vendors-and-intercompany-customers"></a>Per impostare fornitori intercompany e clienti intercompany
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Fornitori** e quindi scegliere il collegamento correlato.
2. In alternativa, accedere al fornitore dal campo **Nr. Fornitore** della pagina **Partner IC**.
3. Aprire la scheda di un fornitore che è un partner intercompany. Per ulteriori informazioni, vedere [Registrare nuovi fornitori](purchasing-how-register-new-vendors.md).
4. Nel campo **Codice partner IC**, selezionare il codice partner IC desiderato.
5. Ripetere i passaggi da 1 a 4 per i clienti.

## <a name="to-set-up-intercompany-charts-of-accounts"></a>Per impostare il piano dei conti intercompany
Per poter effettuare transazioni intercompany, un gruppo di società deve concordare un piano dei conti da utilizzare come riferimento comune. È necessario concordare con le società partner i numeri di conto da utilizzare per la creazione delle transazioni intercompany. La casa madre del gruppo può ad esempio creare una versione semplificata del proprio piano dei conti, esportare tale piano dei conti intercompany dal proprio database a un file XML e distribuirlo a tutte le società del gruppo.  

Se la società è la società padre e dispone del piano dei conti intercompany che dovrà essere utilizzato come riferimento da tutte le società del gruppo, attenersi alla procedura [Per impostare il piano dei conti intercompany](intercompany-how-setup.md#to-set-up-the-defining-intercompany-chart-of-accounts).  

Se la società è una filiale e si riceve un file XML contenente il piano dei conti intercompany comune, attenersi alla procedura [Per importare il piano dei conti intercompany](intercompany-how-setup.md#to-import-the-intercompany-chart-of-accounts).  

### <a name="to-set-up-the-defining-intercompany-chart-of-accounts"></a>Per impostare il piano dei conti intercompany
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Piano dei conti intercompany** e quindi scegliere il collegamento correlato.
2. Nella pagina **Piano dei conti intercompany** immettere ogni conto su una riga nella pagina.  
3. Se il piano dei conti intercompany è identico o simile a quello utilizzato normalmente, è possibile compilare automaticamente la pagina scegliendo l'azione **Copia da piano dei conti**. Le nuove righe possono essere modificate secondo le esigenze.

### <a name="to-export-an-intercompany-chart-of-accounts"></a>Per esportare un piano dei conti intercompany
Per consentire ai partner intercompany di importare il piano dei conti è necessario esportarlo in file.      
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Piano dei conti intercompany** e quindi scegliere il collegamento correlato.
2. Nella pagina **Piano dei conti intercompany**, selezionare l'azione **Esporta** quindi scegliere il pulsante **Salva**.
3. Specificare il nome del file e il percorso in cui salvare il file XML, quindi fare clic sul pulsante **Salva**.  

### <a name="to-import-the-intercompany-chart-of-accounts"></a>Per importare il piano dei conti intercompany  
Una volta che il file del piano dei conti intercompany è presente, i partner intercompany possono importarlo per essere certi che abbiano gli stessi conti.  
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Piano dei conti intercompany** e quindi scegliere il collegamento correlato.  
2. Nella pagina **Piano dei conti intercompany**, selezionare l'azione **Importa**.  
3. Selezionare il nome e il percorso del file XML, quindi scegliere il pulsante **Apri**.  

La pagina **Piano dei conti IC** viene compilata con le righe nuove o modificate del conto C/G in base al piano dei conti IC del file. Eventuali righe esistenti e non correlate della pagina restano invariate.

### <a name="to-map-the-intercompany-chart-of-accounts-to-your-companys-chart-of-accounts"></a>Per mappare il piano dei conti intercompany a quello della società  
Una volta definito o importato il piano dei conti IC concordato con i partner intercompany, è necessario associare ogni conto C/G intercompany al corrispondente conto C/G della società. Nella pagina **Piano dei Conti IC** è possibile specificare come convertire i conti C/G intercompany utilizzati nelle transazioni in entrata nei conti C/G del piano dei conti della società.

Se i numeri dei conti del piano dei conti intercompany sono uguali a quelli dei conti del piano dei conti, è possibile eseguirne automaticamente il mapping.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Piano dei conti intercompany** e quindi scegliere il collegamento correlato.  
2. Selezionare le righe che si desidera mappare automaticamente, quindi scegliere l'azione **Associa a conti con stesso nr.**.  
3. Per ogni conto di contabilità generale intercompany non mappato automaticamente, compilare il campo **Nr. Conto C/G Assoc.**.  

## <a name="to-set-up-default-intercompany-partner-general-ledger-accounts"></a>Per impostare i conti C/G predefiniti per i partner intercompany  
Quando si crea una riga di acquisto o vendita intercompany da inviare come transazione in uscita, è necessario immettere un conto del piano dei conti intercompany come impostazione di default per il conto della società partner in cui deve essere registrato l'importo. Nella pagina **Piano dei conti** è possibile specificare un conto di contabilità generale partner intercompany di default per i conti maggiormente utilizzati nelle righe di acquisto o di vendita intercompany in uscita. Per i conti crediti vs clienti è ad esempio possibile specificare i conti debiti corrispondenti del piano dei conti intercompany.  

Quando si specifica un conto C/G nel campo **Nr. contropartita** di una riga intercompany con **Partner IC** nel campo **Tipo conto**, il campo **Nr. conto C/G partner IC** viene compilato automaticamente.  

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Piano dei conti** e quindi scegliere il collegamento correlato.  
2. Nella riga di un conto C/G utilizzato per le transazioni intercompany, nel campo **Conto C/G partner IC di default**, immettere il conto di contabilità generale intercompany in cui il partner effettuerà le registrazioni al momento della registrazione del conto C/G nella riga.  
3. Ripetere il passaggio 2 per ogni conto immesso di frequente nel campo **Nr. contropartita** di una riga di documento o registrazione intercompany.

## <a name="to-set-up-intercompany-dimensions"></a>Per impostare le dimensioni intercompany
Per poter scambiare con i propri partner intercompany transazioni con dimensioni collegate, è necessario concordare le dimensioni che verranno usate da tutti. La casa madre del gruppo può ad esempio creare una versione semplificata del proprio insieme di dimensioni ed esportare tali dimensioni intercompany in un file XML da distribuire a tutte le società del gruppo. Ogni filiale può quindi importare il file XML nella pagina **Dimensioni intercompany** e associare le dimensioni intercompany a quelle presenti nella pagina **Dimensioni** della società.  

Se la società è la società padre e dispone del set di dimensioni intercompany che il gruppo utilizzerà come riferimento comune, seguire la procedura [Per definire le dimensioni intercompany](intercompany-how-setup.md#to-define-the-intercompany-dimensions).

Se la società è una filiale ed è stato ricevuto un file XML contenente le dimensioni intercompany che il gruppo utilizzerà come riferimento comune, attenersi alla procedura [Per importare le dimensioni intercompany](intercompany-how-setup.md#to-import-the-intercompany-dimensions).

### <a name="to-define-the-intercompany-dimensions"></a>Per definire le dimensioni intercompany
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Dimensioni intercompany** e quindi scegliere il collegamento correlato.  
2. Nella pagina **Dimensioni intercompany** immettere ogni dimensione su una riga della pagina.

    Se le dimensioni intercompany sono simili o identiche a quelle dell'azienda, è possibile compilare automaticamente la pagina scegliendo **Copia da dimensioni**, quindi modificando le righe risultanti.  
3. Per esportare le dimensioni intercompany in un file XML da distribuire alle società partner, scegliere l'azione **Esporta**.  
4. Specificare il nome del file e il percorso in cui salvare il file XML, quindi fare clic sul pulsante **Salva**.  

### <a name="to-import-the-intercompany-dimensions"></a>Per importare le dimensioni intercompany  
Una volta che il file delle dimensioni intercompany è presente, i partner intercompany possono importarlo per essere certi che abbiano le stesse dimensioni.  
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Dimensioni intercompany** e quindi scegliere il collegamento correlato.  
2. Nella pagina **Piano dei conti intercompany**, selezionare l'azione **Importa**.  
3. Specificare il nome e il percorso del file XML, quindi scegliere il pulsante **Apri**.  

Le righe delle pagine **Dimensioni intercompany** e **Valori dimensioni intercompany** vengono importate.  

### <a name="to-map-intercompany-dimensions-to-your-companys-dimensions"></a>Per mappare le dimensioni IC alle dimensioni della società
Dopo aver importato o definito le dimensioni concordate con i partner intercompany, è necessario associare ogni dimensione IC con la corrispondente dimensione della società e viceversa. Nella pagina **Dimensioni intercompany** è possibile specificare come convertire le dimensioni intercompany utilizzate nelle transazioni in entrata nelle dimensioni definite nell'elenco delle dimensione della società. Nella pagina **Dimensioni** è possibile specificare come convertire le dimensioni della società nelle dimensioni intercompany utilizzate nelle transazioni in uscita.

Le dimensioni intercompany con lo stesso codice delle corrispondenti dimensioni definite nell'elenco delle dimensioni della società possono essere associate automaticamente, quindi è possibile associare i conti automaticamente.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Dimensioni intercompany** e quindi scegliere il collegamento correlato.
2. Nella pagina **Dimensioni intercompany** selezionare le righe che si desidera associare automaticamente, quindi scegliere l'azione **Associa a dim. con stesso codice**.
3. Per ogni dimensione intercompany di cui non viene eseguito automaticamente il mapping, compilare il campo **Codice dim. associaz.**.
4. Scegliere l'azione **Valori dimensioni intercompany**.
5. Nella pagina **Valori dimensioni intercompany** compilare il campo **Codice val. dim. associaz.**.

    Continuare ad associare le dimensioni alle dimensioni intercompany eseguendo passaggi simili.
6. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Dimensioni** e quindi scegliere il collegamento correlato.
7. Nella pagina **Dimensioni intercompany** selezionare le righe che si desidera associare automaticamente, quindi scegliere l'azione **Associa a dim. IC con stesso codice**.
8. Per ogni dimensione intercompany di cui non viene eseguito automaticamente l'associazione, compilare il campo **Mapping codice valore dim. IC**.
9. Scegliere l'azione **Valori dimensioni intercompany**.
10. Nella pagina **Valori dimensioni intercompany** compilare il campo **Mapping codice valore dim. IC**.

## <a name="see-also"></a>Vedi anche
[Gestione delle transazioni Intercompany](intercompany-manage.md)  
[Finanze](finance.md)  
[Impostazione di dati finanziari](finance-setup-finance.md)  
[Utilizzo delle registrazioni COGE](ui-work-general-journals.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
