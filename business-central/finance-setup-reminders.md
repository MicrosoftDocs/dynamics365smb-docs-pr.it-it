---
title: Impostare i termini e i livelli di sollecito
description: Informazioni su come impostare Business Central per inviare un sollecito a un cliente per un pagamento scaduto e aggiungere addebiti o oneri al pagamento a causa del ritardo.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment due, debt, overdue, fee, charge, reminder'
ms.search.form: '431, 432, 436, 478'
ms.date: 03/12/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Impostare i termini e i livelli di sollecito

Puoi utilizzare i solleciti per ricordare ai clienti gli importi scaduti e il pagamento della richiesta. [!INCLUDE [reminder-terms](includes/reminder-terms.md)]

> [!TIP]
> Dopo aver impostato i termini e i livelli dei solleciti, puoi includerli nei processi automatizzati per creazione, emissione e invio di solleciti. Per ulteriori informazioni sul processo automatizzato, vai a [Automatizzare i solleciti nelle riscossioni](finance-automate-reminders.md).

## Termini di sollecito

Se per un cliente sono presenti pagamenti scaduti, è necessario decidere quando e con quale modalità inviare un sollecito. Può inoltre essere necessario addebitare sul relativo conto gli interessi o gli oneri. È possibile impostare un numero qualsiasi di termini di sollecito.  

> [!NOTE]
> Se si desidera calcolare gli interessi sui pagamenti scaduti, è possibile effettuare questa operazione quando si creano i solleciti. Se tuttavia desideri semplicemente calcolare gli interessi e informarne i clienti senza inviare un sollecito, utilizza una [nota di addebito degli interessi](finance-setup-finance-charges.md). Per ulteriori informazioni, vedi [Solleciti](receivables-collect-outstanding-balances.md#reminders) o [Addebiti interessi](receivables-collect-outstanding-balances.md#finance-charges).

### Impostare i tesi degli allegati e del corpo e-mail per le comunicazioni

Nella pagina **Impostazione dei termini di sollecito**, puoi impostare i testi degli allegati e i messaggi e-mail standard da utilizzare per tutti i livelli di sollecito o creare messaggi specifici per ciascun livello. Ad esempio, il messaggio inviato per il primo livello di sollecito potrebbe avere un tono o un contenuto diverso rispetto al secondo o al terzo. Per creare testi di allegati e messaggi e-mail per tutti i livelli, scegli **Comunicazione del cliente** nella parte superiore della pagina. Per creare messaggi per righe specifiche, nella scheda dettaglio **Livello sollecito** scegli una riga, quindi scegli l'azione **Comunicazione del cliente** nella Scheda dettaglio.

Per impostazione predefinita, i testi degli allegati e delle e-mail utilizzano l'impostazione della lingua. Se invii solleciti ai clienti in altri paesi, tuttavia, potresti voler comunicare in lingue diverse. Puoi creare testi per ogni lingua che [!INCLUDE [prod_short](includes/prod_short.md)] supporta utilizzando l'azione **Aggiungi testo per la lingua**. In tal caso, assicurati che le lingue siano le stesse per i testi degli allegati e per i testi delle e-mail. Se non corrispondono e il termine del sollecito ha più di un livello, l'automazione potrebbe non essere in grado di personalizzare il messaggio per uno o più livelli. Per verificare che le lingue corrispondano, utilizza l'azione **Panoramica comunicazioni** e confronta le comunicazioni per i testi.

Quando invii un'e-mail, il sollecito è un report che alleghi all'e-mail. Puoi definire il report che genera il sollecito nella pagina **Selezioni report - Sollecito e addebito interessi**, dove selezioni anche il report che contiene il testo del corpo e-mail nel campo **Nome layout corpo e-mail**. Quando invii e-mail ai tuoi clienti, i testi presenti nella Scheda dettaglio **Testo e-mail** vengono inseriti nel report selezionato nel campo **Nome layout corpo e-mail**. Il report standard dispone di un campo di testo per questo testo. Se lo desideri, puoi modificare questo report, ad esempio, per aggiungere o rimuovere contenuti. Modifica il layout di questi report nella pagina **Layout report**. Per ulteriori informazioni sui layout di report, vedi [Iniziare a creare layout di report](ui-get-started-layouts.md).

> [!NOTE]
> Per comunicare tramite email direttamente da [!INCLUDE [prod_short](includes/prod_short.md)] è necessario che tu sia configurato per farlo. Per ulteriori informazioni sulla connessione della posta elettronica con [!INCLUDE [prod_short](includes/prod_short.md)], vedi [Impostare la posta elettronica](admin-how-setup-email.md).

### Impostare i termini di sollecito

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Termini di sollecito**, quindi scegli il collegamento correlato.  
2. Compilare i campi, se necessario. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
3. Per utilizzare più di una combinazione dei termini di sollecito, impostare un codice per ciascuno di essi.

## Livelli di sollecito

Per ciascun termine di sollecito puoi definire un numero illimitato di livelli di sollecito, sebbene la maggior parte delle società utilizzi solo due o tre livelli. La prima volta che si crea un sollecito per un cliente, viene utilizzata l'impostazione del livello 1. Quando si emette il solletico, il numero del livello viene registrato nei movimenti del sollecito creati e collegati ai singoli movimenti contabili cliente. Se è necessario sollecitare nuovamente il cliente, vengono controllati tutti i movimenti del sollecito collegati ai movimenti contabili cliente aperti per individuare il numero di livello più alto. Per il nuovo sollecito verranno quindi utilizzate le condizioni del numero di livello successivo.

Se si creano più solleciti di quanti livelli sono stati definiti, verranno utilizzate le condizioni del livello massimo. È possibile creare tanti solleciti quanti sono consentiti dall'impostazione del campo **Nr. max solleciti** nei termini del sollecito.

### Per impostare i livelli di sollecito

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Termini di sollecito**, quindi scegli il collegamento correlato.  
2. Nella pagina **Termini di sollecito** selezionare la riga con i termini di sollecito per cui si desidera impostare i livelli e scegliere l'azione **Livelli**.  
3. Compilare i campi come necessario. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

    > [!TIP]
    > L'impostazione del campo **Interessi calcolati** determina se l'interesse apparirà sul sollecito quando viene emesso il sollecito. Il campo **Registra interesse** nella pagina **Termini di sollecito** determina se l'interesse calcolato deve essere registrato nei conti C/G e clienti.
    >
    > Per indicare che l'interesse deve essere calcolato, scegliere il campo **Interessi calcolati** campo.

    Facoltativamente, per ogni livello di sollecito, specificare gli oneri aggiuntivi sia in VL che in valuta estera. È possibile definire molti oneri addizionali in valuta estera per ogni codice nella pagina **Livelli di sollecito**.  

    Le commissioni aggiuntive possono essere calcolate in tre modi diversi che sono definiti dal valore del campo **Tipo calcolo onere addiz.**.  

    - **Fisso**

        Gli oneri sono calcolati in base ai valori dei campi **Onere addizionale** nella riga per il livello di sollecito stesso.  
    - **Dinamico singolo**

        Gli oneri sono calcolati in base ai valori dei campi nella riga pertinente nella pagina **Setup onere addizionale** di quel livello di sollecito.
    - **Dinamico accumulato**

        Gli oneri sono calcolati in base ai valori dei campi nelle righe pertinenti nella pagina **Setup onere addizionale** di quel livello di sollecito.

4. Scegliere l'azione **Valute**.
5. Nella pagina **Valute per livello sollecito**, per ogni codice del livello di sollecito e per il corrispondente numero del livello di sollecito, definire un codice di valuta e un onere addizionale.

    > [!NOTE]  
    > Creando solleciti in valuta estera, le condizioni per la valuta estera impostate qui verranno utilizzate per la creazione di solleciti. Se non sono state impostate condizioni per i solleciti in valuta estera, verranno utilizzate le condizioni per i solleciti in valuta locale impostate nella pagina **Livelli di sollecito** e quindi convertite nella relativa valuta.

    Per ogni livello di sollecito è possibile specificare il testo che verrà stampato prima (**Testo iniziale**) o dopo (**Testo finale**) nei movimenti nel sollecito.

6. Scegliere rispettivamente le azioni **Testo iniziale** o **Testo finale** e compilare la pagina **Testi di sollecito**.
7. Per inserire automaticamente i valori correlati nel testo di sollecito, puoi immettere i seguenti segnaposto nel campo **Testo**.  

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

    Ad esempio, se scrivi **È dovuto il pagamento di %9 %7 con scadenza %2**, nel sollecito viene visualizzato il seguente testo: **È dovuto il pagamento di 1.200,50 USD con scadenza 02-02-2024.**

    > [!NOTE]
    > [!INCLUDE [prod_short](includes/prod_short.md)] calcola la data di scadenza in base alla formula immessa per la data. Per ulteriori informazioni, vedi [Utilizzare le formule per le date](ui-enter-date-ranges.md#use-date-formulas).

8. Per specificare la lingua per un messaggio e-mail, scegli l'azione **Aggiungi testo per la lingua**. Il campo **Codice lingua** si aggiorna per mostrare la selezione. Nella Scheda dettaglio veloce **Testo e-mail** immetti il contenuto del messaggio nella lingua selezionata.

Dopo aver impostato i termini del sollecito, puoi assegnarli ai clienti nelle pagine Scheda cliente. Per ulteriori informazioni, vedere [Registrare nuovi clienti](sales-how-register-new-customers.md).  

## Vedere anche

[Riscuotere i saldi inevasi](receivables-collect-outstanding-balances.md)  
[Inviare promemoria per saldi inevasi](receivables-send-reminders.md)  
[Impostare condizioni interessi finanziari](finance-setup-finance-charges.md)  
[Impostazione di dati finanziari](finance-setup-finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
