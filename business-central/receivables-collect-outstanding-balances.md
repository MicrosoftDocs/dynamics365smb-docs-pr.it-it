---
title: Sollecitare o applicare sanzioni per clienti con pagamenti scaduti | Documenti Microsoft
description: Descrive come inviare un sollecito a un cliente per un pagamento scaduto e come aggiungere addebiti, od oneri aggiuntivi, al pagamento per il ritardo.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment due, debt, overdue, fee, charge, reminder
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: a4b6f58c434c563021e94e55e47c547d39967502
ms.sourcegitcommit: d3035c32bb79b51179540787b98579ac0c528cc4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/06/2019
ms.locfileid: "1985888"
---
# <a name="collect-outstanding-balances"></a>Riscuotere i saldi inevasi
La gestione dei crediti comprende il controllo del pagamento degli importi dovuti entro i termini di scadenza. Per i clienti con pagamenti scaduti, è possibile inviare innanzitutto il report Rendiconto cliente come promemoria. In alternativa, è possibile emettere dei solleciti.

È possibile utilizzare i solleciti per indicare ai clienti gli importi insoluti. È anche possibile calcolare addebiti di interessi, ad esempio interessi o commissioni, e includerli nei solleciti. Utilizzare note di addebito interessi se si desidera addebitare ai clienti interessi o commissioni senza inviare solleciti relativi agli importi insoluti.

## <a name="reminders"></a>Solleciti
Prima di creare i solleciti, è necessario impostarne i termini e assegnarli ai clienti. Ogni termine di sollecito ha un livelli di sollecito predefinito. e ogni livello include le regole relative all'emissione del sollecito, ad esempio il numero di giorni dopo la data di scadenza della fattura o dopo la data del sollecito precedente. Nella pagina **Condiz. interessi finanziari** viene determinato se nel sollecito vengono calcolati anche gli interessi.  

È possibile eseguire periodicamente il processo batch **Crea solleciti** per creare solleciti per tutti i clienti con saldi scaduti oppure creare manualmente un sollecito per un cliente particolare e calcolare e compilare le righe automaticamente.  

Una volta creati i solleciti, è possibile modificarli. Il testo visualizzato all'inizio e alla fine di un sollecito è determinato dai termini del livello del sollecito e può essere visualizzato nella colonna **Descrizione**. Se un importo calcolato è stato inserito automaticamente nel testo iniziale o finale, questo non verrà rettificato se si eliminano righe Sarà quindi necessario utilizzare la funzione **Aggiorna testo soll.**.  

Per un movimento contabile cliente con selezionato il campo **In sospeso** non verrò richiesta la creazione di un sollecito. Se tuttavia viene creato un sollecito in base a un altro movimento, nel sollecito verrà incluso anche un movimento scaduto contrassegnato come in sospeso. Per le righe di questi movimenti non verranno calcolati interessi.

Dopo avere creato i solleciti e apportato le modifiche necessarie, è possibile stampare report di test o emettere i solleciti, in genere tramite posta elettronica.

## <a name="finance-charges"></a>Spese finanziarie
Quando un cliente non effettua il pagamento entro la data di scadenza, è possibile fare in modo che gli addebiti per interessi vengano calcolati automaticamente e aggiunti agli importi insoluti nel conto del cliente. È possibile informare i clienti degli interessi aggiunti mediante l'invio di note di addebito interessi.  

> [!NOTE]  
> Le note di addebito interessi vengono utilizzate per calcolare interessi e addebiti interessi e informare i clienti su tali interessi e addebiti interessi senza inviare solleciti relativi ai pagamenti scaduti. In alternativa è possibile calcolare gli interessi sui pagamenti scaduti, è possibile effettuare questa operazione quando si creano i solleciti.  

È possibile creare manualmente una nota di addebito interessi per un singolo cliente e compilare le righe automaticamente. In alternativa è possibile utilizzare il processo della funzione **Crea note add. interessi** per creare tali documenti per tutti i clienti selezionati con saldi scaduti.  

Una volta create, le note di addebito interessi possono essere modificate. Il testo visualizzato all'inizio e alla fine della nota è determinato dalle condizioni relative agli interessi finanziari e può essere visualizzato nella colonna **Descrizione** delle righe. Se un importo calcolato è stato inserito automaticamente nel testo iniziale o finale, questo non verrà rettificato se si eliminano righe e sarà necessario utilizzare la funzione **Aggiorna testi add. int.**.  

Dopo avere creato le note di addebito interessi e apportato le modifiche necessarie, è possibile stampare report di test o emettere le note di addebito interessi, in genere tramite posta elettronica.

## <a name="multiple-interest-rates"></a>Tassi d'interesse multipli
Quando si impostano le condizioni di addebito degli interessi e i termini di sollecito, per la penalità per pagamento ritardato, è possibile specificare più tassi di interesse in modo che la penalità sia calcolata in base a tassi di interesse differenti in diversi periodi. Se non si impostano più tassi di interesse, verranno utilizzati il tasso di interesse e il periodo definito nelle pagine **Condiz. interessi finanziari** e **Termini di sollecito** per l'intero periodo di calcolo. Per ulteriori informazioni, vedere [Impostare più tassi di interesse](finance-how-to-set-up-multiple-interest-rates.md).  

## <a name="to-send-the-customer-statement-report"></a>Per inviare il report estratto conto cliente
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Rendiconto cliente** e quindi scegliere il collegamento correlato.
2. Compilare i campi, se necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. In **Opzioni output** selezionare una modalità di invio del report al cliente.

> [!NOTE]  
>   Se si utilizzano più valute, il report Rendiconto cliente viene sempre stampato nella valuta del cliente. L'ultima data in un periodo di rendiconto viene inoltre utilizzata come data di rendiconto e data di aging, se è incluso l'aging.

## <a name="to-set-up-reminder-terms"></a>Per impostare i termini di sollecito
Se per un cliente sono presenti pagamenti scaduti, è necessario decidere quando e con quale modalità inviare un sollecito. Può inoltre essere necessario addebitare sul relativo conto gli interessi e/o altre competenze. È possibile impostare un numero qualsiasi di termini di sollecito. A ciascun codice dei termini di sollecito corrispondono un numero illimitato di livelli di sollecito.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Termini di sollecito** e quindi scegliere il collegamento correlato.  
2. Compilare i campi, se necessario.  
3. Per utilizzare più di una combinazione dei termini di sollecito, impostare un codice per ciascuno di essi.

## <a name="to-set-up-reminder-levels"></a>Per impostare i livelli di sollecito
La prima volta che si crea un sollecito per un cliente, viene utilizzata l'impostazione del livello 1. Quando si emette il solletico, il numero del livello viene registrato nei movimenti del sollecito creati e collegati ai singoli movimenti contabili cliente. Se è necessario sollecitare nuovamente il cliente, vengono controllati tutti i movimenti del sollecito collegati ai movimenti contabili cliente aperti per individuare il numero di livello più alto. Per il nuovo sollecito verranno quindi utilizzate le condizioni del numero di livello successivo.

Se si creano più solleciti di quanti livelli sono stati definiti, verranno utilizzate le condizioni del livello massimo. È possibile creare tanti solleciti quanti sono consentiti dall'impostazione del campo **Nr. max solleciti** nei termini del sollecito.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Termini di sollecito** e quindi scegliere il collegamento correlato.  
2. Nella pagina **Termini di sollecito** selezionare la riga con i termini di sollecito per cui si desidera impostare i livelli e scegliere l'azione **Livelli**.  
3. Compilare i campi, se necessario.  

    Per ogni livello di sollecito, è possibile specificare singole condizioni, tra cui oneri addizionali sia in VL sia in valuta estera. È possibile definire molti oneri addizionali in valuta estera per ogni codice nella pagina **Livelli di sollecito**.
4. Scegliere l'azione **Valute**.
5. Nella pagina **Valute per livello sollecito**, per ogni codice del livello di sollecito e per il corrispondente numero del livello di sollecito, definire un codice di valuta e un onere addizionale.

    > [!NOTE]  
    > Creando solleciti in valuta estera, le condizioni per la valuta estera impostate qui verranno utilizzate per la creazione di solleciti. Se non sono state impostate condizioni per i solleciti in valuta estera, verranno utilizzate le condizioni per i solleciti in valuta locale impostate nella pagina **Livelli di sollecito** e quindi convertite nella relativa valuta.

    Per ogni livello di sollecito è possibile specificare il testo che verrà stampato prima (**Testo iniziale**) o dopo (**Testo finale**) nei movimenti nel sollecito.

6. Scegliere rispettivamente le azioni **Testo iniziale** o **Testo finale** e compilare la pagina **Testi di sollecito**.
7. Per inserire automaticamente i relativi valori nel testo di sollecito risultante, fornire seguenti segnaposti nel campo **Testo**.  

|Segnaposto|Valore|  
|-----------------|-----------|  
|%1|Contenuto del campo **Data documento** della testata sollecito|  
|%2|Contenuto del campo **Data scadenza** della testata sollecito|  
|%3|Contenuto del campo **Tasso di interesse** nelle condizioni di addebito degli interessi finanziari correlate|  
|%4|Contenuto del campo **Importo residuo** della testata sollecito|  
|%5|Contenuto del campo **Importo interessi** della testata sollecito|  
|%6|Contenuto del campo **Onere addizionale** della testata sollecito|  
|%7|Importo totale del sollecito|  
|%8|Contenuto del campo **Livello di sollecito** della testata sollecito|  
|%9|Contenuto del campo **Codice valuta** della testata sollecito|  
|%10|Contenuto del campo **Data di registrazione** della testata sollecito|  
|%11|Nome della società|  
|%12|Contenuto del campo **Onere add. per riga** della testata sollecito|  

Ad esempio, se si scrive **È dovuto il pagamento di %9 %7 con scadenza %2**, nel sollecito risultante verrà visualizzato il seguente testo: **È dovuto il pagamento di 1.200,50 USD con scadenza 02-02-2014.**

> [!NOTE]
> La data di scadenza viene calcolata in base alla formula immessa per la data. Per ulteriori informazioni, vedere [Utilizzo di formule per le date](ui-enter-date-ranges.md#using-date-formulas).

Dopo avere impostato i termini di sollecito, con livelli e testo aggiuntivi, immettere uno dei codici in ognuna delle schede clienti. Per ulteriori informazioni, vedere [Registrare nuovi clienti](sales-how-register-new-customers.md).

## <a name="to-create-a-reminder-automatically"></a>Per creare un sollecito automaticamente
Un sollecito è simile a una fattura. Quando viene creato un sollecito, è necessario compilare una testata e una o più righe. È possibile utilizzare una funzione che consente di creare i solleciti automaticamente per tutti i clienti.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Solleciti** e quindi scegliere il collegamento correlato.
2. Nella pagina **Sollecito**, selezionare l'azione **Crea sollecito**.
3. Nella pagina **Crea solleciti** compilare i campi per definire come e per chi vengono creati i solleciti.
4. Scegliere il pulsante **OK**.

## <a name="to-create-a-reminder-manually"></a>Per creare un sollecito manualmente
Nella pagina **Sollecito** è possibile compilare manualmente la Scheda dettaglio **Generale** e quindi compilare automaticamente le righe.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Solleciti** e quindi scegliere il collegamento correlato.
2. Scegliere l'azione **Nuovo**.
3. Compilare i campi appropriati nella Scheda dettaglio **Generale**.
4. Scegliere l'azione selezionare **Suggerisci riga sollecito**.
5. Nella finestra **Crea solleciti** compilare i campi per definire come e per chi vengono creati i solleciti.
6. Se si desidera che i solleciti contengano i movimenti aperti con importi insoluti che sono in sospeso, selezionare la casella di controllo **Includi movimenti in sospeso**.

    > [!Important]
    > I movimenti aperti che sono in sospeso verranno inseriti, indipendentemente dall'impostazione nella casella di controllo Solo movimenti con importi insoluti.

7. Scegliere il pulsante **OK**.

## <a name="to-replace-reminder-texts"></a>Per sostituire i testi di un sollecito  
Esistono diverse modalità per determinare il testo che verrà visualizzato nella stampa del sollecito. In alcuni casi può essere necessario sostituire i testi iniziali e finali definiti per il livello attuale con i testi di un livello diverso.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Solleciti** e quindi scegliere il collegamento correlato.
2. Aprire il sollecito pertinente quindi scegliere l'azione **Aggiorna testo sollecito**.
3. Nella pagina **Aggiorna testo sollecito**, immettere il livello richiesto nel campo **Livello di sollecito**.
3. Scegliere **OK** per aggiornare il testo iniziale e finale.

## <a name="to-issue-a-reminder"></a>Per emettere un sollecito
Dopo avere creato i solleciti e apportato le modifiche necessarie, è possibile stampare report di test o emettere i solleciti.

Quando si emette un sollecito, i dati vengono trasferiti in una pagina distinta relativa ai solleciti emessi e vengono contemporaneamente registrati i movimenti del sollecito. Se sono stati calcolati interessi o oneri addizionali, i movimenti vengono registrati nella contabilità clienti e nella contabilità generale.

Quando viene generato un sollecito, vengono registrati i movimenti secondo le scelte immesse nella pagina **Termini di sollecito**. Questa specifica determina se interessi e/o oneri addizionali vengono registrati nel conto del cliente e nella contabilità generale. Il setup nella pagina **Cat. reg. cliente** stabilisce in quali conti vengono registrati.

Per ogni movimento contabile cliente sulla nota addebito interessi, viene creato un movimento nella pagina **Mov. soll./Note add. int.**.

Se sono selezionate le caselle di controllo **Registra interesse** o **Registra onere addizionale** nella pagina **Termini di Sollecito**, vengono creati anche i seguenti movimenti:

- un movimento nella pagina **Mov. contabili clienti**
- un movimento incassi nel relativo Conto C/G
- un movimento interessi e/o un movimento onere addizionale nel relativo Conto C/G

L'emissione di un sollecito può inoltre risultare nei movimenti IVA.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Solleciti** e quindi scegliere il collegamento correlato.
2. Selezionare il sollecito di interesse e quindi scegliere l'azione **Emetti**.
3. Nella pagina **Emetti sollecito** compilare i campi secondo le necessità.
4. Scegliere il pulsante **OK**.

Il sollecito viene stampato per l'invio a un indirizzo e-mail specificato come allegato PDF.

## <a name="to-set-up-finance-charge-terms"></a>Per impostare le condizioni di addebito degli interessi
Interessi Finanziari per impostare le condizioni per i calcoli di addebito degli interessi. Immettere quindi il codice nel campo **Cod. addebito interessi** nelle schede cliente o fornitore.

È possibile calcolare gli addebiti degli interessi utilizzando il metodo del saldo giornaliero medio oppure il metodo del saldo dovuto.

* Metodo del saldo dovuto

    L'addebito di interessi è semplicemente una percentuale dell'importo insoluto:  
    *Metodo del saldo dovuto* - *Addebito interessi* = *Importo insoluto* x *(Tasso di interesse / 100)*

*   Metodo del saldo giornaliero medio

    Viene considerato il numero di giorni che il pagamento è dovuto:  
    *Metodo Saldo giornaliero medio* - *Addebito interessi* = *Importo insoluto* x *(Giorni in arretrato / Periodo di interesse)* x *(Tasso di interesse/100)*

Inoltre ogni codice nella tabella Condiz.Interessi Finanziari è collegato a una sottotabella, detta tabella Testi addebiti interessi. Per ciascun gruppo di condizioni degli interessi finanziari, è possibile creare un testo iniziale e/o uno finale da inserire nella nota di addebito degli interessi.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Condiz. interessi finanziari** e quindi scegliere il collegamento correlato.  
2. Compilare i campi, se necessario.
3. Per utilizzare più di una combinazione di condizioni di interessi finanziari, impostare un codice per ciascuno di essi.

    Per ogni condizione di interessi finanziari, è possibile specificare singole condizioni, tra cui oneri addizionali sia in VL sia in valuta estera. È possibile definire molti oneri addizionali in valuta estera per ogni codice nella pagina **Condiz. interessi finanziari**.
4. Scegliere l'azione **Valute**.
5. Nella pagina **Valute per addebito interessi**, specificare per ogni termine un codice valuta e un onere addizionale.

    > [!NOTE]  
    > Creando addebiti di interessi in una valuta estera, le condizioni per la valuta estera impostate qui verranno utilizzate per creare note di addebito interessi. Se non sono state impostate condizioni degli interessi finanziari in valuta estera, verranno automaticamente utilizzate le condizioni degli interessi finanziari in valuta locale impostate nella pagina **Condiz. interessi finanziari** convertite nella relativa valuta.

    Per ciascuna condizione di interessi finanziari è possibile specificare il testo che sarà stampato prima (**Testo Iniziale**) o dopo (**Testo Finale**) nei movimenti nella nota di addebito di interessi.  
6. Scegliere rispettivamente le azioni **Testo iniziale** o **Testo finale** e compilare la pagina **Testi addebiti interessi**.
7. Per inserire automaticamente i relativi valori nel testo di addebito di interessi risultante, fornire seguenti segnaposti nel campo **Testo**.

|Segnaposto|Valore|  
|-----------------|-----------|  
|%1|Contenuto del campo **Data documento** della testata della nota di addebito interessi|  
|%2|Contenuto del campo **Data scadenza** della testata della nota di addebito interessi|  
|%3|Contenuto del campo **Tasso di interesse** nelle condizioni di addebito degli interessi finanziari correlate|  
|%4|Contenuto del campo **Importo residuo** della testata della nota di addebito interessi|  
|%5|Contenuto del campo **Importo interessi** della testata della nota di addebito interessi|  
|%6|Contenuto del campo **Onere addizionale** della testata della nota di addebito interessi|  
|%7|Importo totale del sollecito|  
|%8|Contenuto del campo **Codice valuta** della testata della nota di addebito interessi|  
|%9|Contenuto del campo **Data reg.** della testata della nota di addebito interessi|  

## <a name="to-create-a-finance-charge-memo-manually"></a>Per creare una nota di addebito di interessi manualmente  
Una nota di addebito di interessi è simile a una fattura. È possibile compilare una testata manualmente e le righe automaticamente, oppure le note di addebito di interessi possono venire create automaticamente per tutti i clienti.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Note addebito interessi** e quindi scegliere il collegamento correlato.  
2. Scegliere l'azione **Nuovo** e compilare i campi necessari.  
3. Scegliere l'azione **Sugg. righe note add. int.**
4. Se si desidera creare note di addebito interessi solo per movimenti specifici, impostare un filtro nella Scheda dettaglio **Mov. contabili clienti** della pagina **Sugg. righe note add. int.**.  
5.  Scegliere **OK** per avviare il processo batch.  

## <a name="to-update-finance-charge-memo-texts"></a>Per aggiornare i testi delle note di addebito di interessi  
Talvolta può essere necessario modificare il testo iniziale e finale impostato per le condizioni degli interessi finanziari. Se la modifica viene effettuata dopo la creazione ma prima dell'emissione di note di addebito di interessi, è possibile aggiornare le note con il testo modificato.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Nota addebito interessi** e quindi scegliere il collegamento correlato.  
2. Aprire la nota di addebito degli interessi per cui si desidera modificare il testo di quindi scegliere l'azione **Aggiorna testi add. int.**.
3. Nella pagina **Aggiorna testi add. int.** è possibile impostare un filtro per aggiornare più note.
4. Scegliere **OK** per aggiornare il testo iniziale e finale.  

## <a name="to-issue-finance-charge-memos"></a>Per emettere note di addebito interessi
Dopo avere creato le note di addebito interessi e apportato le modifiche necessarie, è possibile stampare report di test o emettere le note di addebito interessi.

Quando viene generato un sollecito, vengono registrati i movimenti secondo le scelte immesse nella pagina **Condiz. interessi finanziari**. Questa specifica determina se interessi e/o oneri addizionali vengono registrati nel conto del cliente e nella contabilità generale. Il setup nella pagina **Cat. reg. cliente** stabilisce in quali conti vengono registrati.

Per ogni movimento contabile cliente sulla nota addebito interessi, viene creato un movimento nella pagina **Mov. soll./Note add. int.**.

Se sono selezionate le caselle di controllo **Registra interesse** o **Registra onere addizionale** nella pagina **Condiz. interessi finanziari**, vengono creati anche i seguenti movimenti:

- un movimento nella pagina **Mov. contabili clienti**
- un movimento incassi nel relativo Conto C/G
- un movimento interessi e/o un movimento onere addizionale nel relativo Conto C/G

L'emissione di una nota di addebito di interessi può inoltre risultare nei movimenti IVA.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Note addebito interessi** e quindi scegliere il collegamento correlato.
2. Selezionare la nota pertinente e quindi scegliere l'azione **Emetti**.
3. Nella pagina **Emetti note add. interessi** compilare i campi secondo le necessità.
4. Scegliere il pulsante **OK**.

La nota di addebito di interessi viene stampata per l'invio a un indirizzo e-mail specificato come allegato PDF.

## <a name="to-view-reminder-and-finance-charge-entries"></a>Per visualizzare i movimenti di sollecito e di addebito di interessi  
All'emissione di un sollecito, nella pagina **Mov. soll./Note add. int.** viene creato un movimento di sollecito per ciascuna riga di sollecito che contiene un movimento contabile clienti. È possibile quindi ottenere una panoramica dei movimenti di sollecito creati per un cliente specifico.    
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Clienti** e quindi scegliere il collegamento correlato.  
2. Aprire la scheda cliente interessata e scegliere l'azione **Movimenti contabili**.
3. Nella pagina **Movimenti contabili clienti** selezionare la riga con il movimento contabile per il quale si desidera visualizzare i movimenti di sollecito, quindi scegliere l'azione **Mov. soll./Note add. int.**.

## <a name="see-also"></a>Vedi anche
[Gestione della contabilità clienti](receivables-manage-receivables.md)  
[Vendite](sales-manage-sales.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
