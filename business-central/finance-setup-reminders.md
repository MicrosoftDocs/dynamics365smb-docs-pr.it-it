---
title: Impostare i termini e i livelli di sollecito
description: Informazioni su come impostare Business Central per inviare un sollecito a un cliente per un pagamento scaduto e aggiungere addebiti o oneri al pagamento a causa del ritardo.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'payment due, debt, overdue, fee, charge, reminder'
ms.search.form: '431, 432, 436, 478'
ms.date: 02/09/2022
ms.author: bholtorf
---
# Impostare i termini e i livelli di sollecito

È possibile utilizzare i solleciti per indicare ai clienti gli importi insoluti. [!INCLUDE [reminder-terms](includes/reminder-terms.md)]

## Termini di sollecito

Se per un cliente sono presenti pagamenti scaduti, è necessario decidere quando e con quale modalità inviare un sollecito. Può inoltre essere necessario addebitare sul relativo conto gli interessi o gli oneri. È possibile impostare un numero qualsiasi di termini di sollecito.  

> [!NOTE]
> Se si desidera calcolare gli interessi sui pagamenti scaduti, è possibile effettuare questa operazione quando si creano i solleciti. Se tuttavia si desidera semplicemente calcolare gli interessi e informarne i clienti senza inviare solleciti, utilizzare [note addebito interessi](finance-setup-finance-charges.md). Per ulteriori informazioni, vedere rispettivamente [Solleciti](receivables-collect-outstanding-balances.md#reminders) o [Addebiti interessi](receivables-collect-outstanding-balances.md#finance-charges).

### Per impostare i termini di sollecito

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Termini di sollecito**, quindi scegli il collegamento correlato.  
2. Compilare i campi, se necessario. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
3. Per utilizzare più di una combinazione dei termini di sollecito, impostare un codice per ciascuno di essi.

## Livelli di sollecito

A ciascun codice dei termini di sollecito corrispondono un numero illimitato di livelli di sollecito. La prima volta che si crea un sollecito per un cliente, viene utilizzata l'impostazione del livello 1. Quando si emette il solletico, il numero del livello viene registrato nei movimenti del sollecito creati e collegati ai singoli movimenti contabili cliente. Se è necessario sollecitare nuovamente il cliente, vengono controllati tutti i movimenti del sollecito collegati ai movimenti contabili cliente aperti per individuare il numero di livello più alto. Per il nuovo sollecito verranno quindi utilizzate le condizioni del numero di livello successivo.

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
    > La data di scadenza viene calcolata in base alla formula immessa per la data. Per ulteriori informazioni, vedi [Utilizzare le formule per le date](ui-enter-date-ranges.md#use-date-formulas).

Dopo avere impostato i termini di sollecito, con livelli e testo aggiuntivi, immettere uno dei codici in ognuna delle schede clienti. Per ulteriori informazioni, vedere [Registrare nuovi clienti](sales-how-register-new-customers.md).  

## Vedere anche

[Riscuotere i saldi inevasi](receivables-collect-outstanding-balances.md)  
[Inviare promemoria per saldi inevasi](receivables-send-reminders.md)  
[Impostare condizioni interessi finanziari](finance-setup-finance-charges.md)  
[Impostazione di dati finanziari](finance-setup-finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
