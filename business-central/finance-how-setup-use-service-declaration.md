---
title: Impostare e usare l'estensione Dichiarazione di servizio
description: Informazioni su come impostare e usare le funzionalità Dichiarazione di servizio e come segnalare le attività commerciali con società in altri paesi o aree geografiche dell'UE.
author: altotovi
ms.author: altotovi
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 12/21/2022
ms.custom: bap-template
ms.search.keywords: 'electronic document, Intrastat, trade, EU, service, declaration,'
ms.search.form: '30, 76, 5010, 5022, 5023, 5024, 5800'
---
# L'estensione Dichiarazione di servizio

In alcuni paesi o aree geografiche dell'UE, le autorità richiedono alle imprese di segnalare l'esportazione di servizi in altri paesi o aree geografiche dell'UE. L'estensione **Dichiarazione di servizio** consente di raccogliere informazioni sul commercio di servizi nell'UE e di segnalarle alle autorità. Sebbene sia denominata **Dichiarazione di servizio**, puoi utilizzarla anche come **Intrastat per servizi**. Questa estensione è disponibile per tutti i paesi o aree geografiche dell'UE come versione W1 e può essere utilizzata così com'è in Belgio. Per gli altri paesi o aree geografiche, sarà richiesta un'estensione basata sul paese o l'area geografica. Se un paese/area geografica necessita solo di un formato diverso, puoi usare la configurazione del report nel **Framework di scambio dei dati** per modificare il formato.

## Abilitare l'estensione Dichiarazione di servizio

Dopo aver installato l'estensione nell'ambiente, è necessario abilitarla.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Gestione funzionalità**, quindi scegli il collegamento correlato.
2. Trova **Funzione: abilita l'utilizzo Dichiarazione di servizio (Intrastat per servizi)** e nel campo **Abilitato per**, scegli **Tutti gli utenti**. Per ulteriori informazioni sulla gestione funzionalità vedi [Abilitazione di funzionalità imminenti in anticipo](/dynamics365/business-central/dev-itpro/administration/feature-management) nel contenuto per amministratori.
3. Quando si abilita la funzione, è necessario seguire i passaggi del processo di configurazione tramite l'Installazione guidata. La maggior parte dei campi sono configurati per impostazione predefinita.
4. Aggiungi solo **Tipi di transazioni di servizio** nel secondo passaggio scegliendo l'opzione **Aprire la pagina dei tipi di transazione del servizio per specificare la lista dei codici**.
5. Prima di iniziare, controlla il **Numero totale di codici** per capire quanti tipi di transazioni di servizi sono già stati specificati.
6. Scegli **Fine** nell'ultimo passaggio per terminare la configurazione.

## Configurare l'estensione Dichiarazione di servizio

È possibile impostare l'estensione manualmente o utilizzando un file di report in Definizioni di scambio dati.

### Per configurare Dichiarazione di servizio manualmente

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Setup dichiarazione di servizio**, quindi scegli il collegamento correlato.
2. Nella Scheda dettaglio **Generale** configurare i campi come descritto nella tabella seguente:

    |Campo  |Descrizione  |
    |---------|---------|
    |**Numerazione dichiarazione**     | Specifica la numerazione da usare per assegnare gli ID ai nuovi record.        |
    |**Dichiara addebiti articolo**  | Specifica se gli addebiti articolo devono essere riportati. Se abilitato, [!INCLUDE [prod_short](includes/prod_short.md)] controlla il codice della transazione di servizio per gli addebiti articolo e li include nelle dichiarazioni di servizio.        |
    |**Vendere a/Fatturare a - Nr. cliente**     | Specifica il cliente da usare per confrontare il proprio codice paese con il codice paese nella pagina **Informazioni sulla società**. Solo i documenti in cui questi due codici sono diversi saranno inclusi nella dichiarazione di servizio.<br><br>* **Fatturare a**: utilizza il prefisso internazionale del **Fatturare a - Nr. cliente**<br>* **Vendere a**: utilizza il prefisso internazionale del **Vendere a - Nr. cliente**.        |
    |**Acquistare da/Pagare a - Nr. fornitore**  | Specifica il fornitore da usare per confrontare il proprio codice paese con il codice paese dalla pagina **Informazioni sulla società**. Solo i documenti in cui questi due codici sono diversi saranno inclusi nella dichiarazione di servizio.<br><br> * **Acquistare da.**: usare il prefisso internazionale del **Acquistare da - Fornitore**. <br><br> * **Pagare a**: utilizza il prefisso internazionale del **Pagare a - ID fornitore**.         |
    |**Codice definizione di scambio dati**  | Specifica il codice della definizione di scambio dati utilizzato per generare il file esportato per la dichiarazione di servizio.        |
    |**Abilita nr. di identificazione fiscale**     |  Specifica se il **Nr. di identificazione fiscale** è abilitato per la dichiarazione di servizio.       |

3. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Tipi di transazione di servizio**, quindi scegli il collegamento correlato.
4. Nelle righe, specifica **Codici** e **Descrizioni** per i tipi di transazione del servizio che utilizzerai.

### Impostare un file di report

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti le **definizioni di scambio dati** e scegli il collegamento correlato.
2. Scegliere l'azione **Nuovo**.
3. Nella Scheda dettaglio **Generale** descrivi la definizione dello scambio di dati specificando il tipo di file di dati, il separatore di colonna, le codeunit correlate, XMLport e la compilazione di altri campi.
4. Sulla scheda dettaglio **Definizioni riga** descrivi la formattazione delle righe nel file di dati compilando i campi in base al campo **Tipo di riga** e a dove è necessario definire il numero di colonne per questa riga.
5. Sulla scheda dettaglio **Definizioni colonna** compila la riga per ogni colonna pianificata.
6. Scegli l'azione **Mapping dei campi** nella scheda dettaglio **Definizioni riga** per aprire la pagina **Mapping dei campi**.
7. Crea una nuova voce e nella scheda dettaglio **Generale** scegli l'**ID tabella** (per **Riga Dichiarazione servizio**, scegli **5024**), quindi compila i campi come segue:
   1. Nel campo **Indice chiave** specifica l'indice chiave per ordinare i record prima dell'esportazione.
   2. Seleziona **Codeunit mapping**.
8. Sulla scheda dettaglio **Mapping dei campi** aggiungi le colonne che hai precedentemente configurato nella scheda dettaglio **Definizioni colonna** quindi aggiungi quanto segue:
   1. Specifica l'**ID campo** per ciascuna delle colonne.
   2. Specifica la **Regola di trasformazione** per ciascuna colonna come necessario. La regola che trasforma il testo importato in un valore supportato prima di poterne eseguire il mapping a un campo specificato in [!INCLUDE[prod_short](includes/prod_short.md)]. Quando scegli un valore in questo campo, lo stesso valore viene inserito nel campo **Regola di trasformazione** nella tabella **Buf. mapping campo scambio dati** e viceversa.
9. Per raggruppare le voci in base ad alcune colonne, nella scheda dettaglio **Raggruppamento campi** scegli i campi che desideri usare per il raggruppamento.

> [!NOTE]
> [!INCLUDE[prod_long](includes/prod_long.md)] viene fornito con la definizione di scambio dati preconfigurata per **Dichiarazione di servizio** per tutti i paesi o le aree geografiche localizzati. Per informazioni sulla creazione di una nuova definizione di scambio dati, vedi [Impostare le definizioni di scambio dati](across-how-to-set-up-data-exchange-definitions.md).

## Altre configurazioni correlate

Prima di usare l'estensione Dichiarazione di servizio, configura alcuni campi per articoli, risorse e addebiti articolo.

### Articoli

Imposta le informazioni relative alla Dichiarazione di servizio nelle pagine Scheda articolo:

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") , inserisci **Elemento** e scegli il link relativo.
2. Seleziona l'articolo da configurare.
3. Espandi la Scheda dettaglio **Articolo** e configura i seguenti campi:
   1. Nel campo **Tipo** scegli **Servizio**.
   2. Nel campo **Codice tipo transazione servizio**, specifica il codice per un **Tipo transazione servizio**.
   3. Se non desideri includere questo articolo di servizio nelle dichiarazioni di servizio, seleziona il campo **Escludi dalla dichiarazione di servizio**.

### Risorse

Imposta le informazioni relative alla Dichiarazione di servizio nelle pagine Scheda risorsa:

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Risorse**, quindi scegli il collegamento correlato.
2. Seleziona la risorsa da configurare.
3. Espandi la Scheda dettaglio **Generale** e configura i seguenti campi:
   1. Nel campo **Codice tipo transazione servizio**, specifica il codice per un **Tipo transazione servizio**.
   2. Se non desideri includere questa risorsa nelle dichiarazioni di servizio, seleziona il campo **Escludi dalla dichiarazione di servizio**.

### Addebiti articoli

Imposta le informazioni relative alla Dichiarazione di servizio per gli addebiti articolo.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Addebiti articoli**, quindi scegli il collegamento correlato.
2. Seleziona l'addebito articolo da configurare.
3. Nel campo **Codice tipo transazione servizio**, specifica il codice per un **Tipo transazione servizio**.
4. Se non desideri includere questo addebito articolo nelle dichiarazioni di servizio, seleziona il campo **Escludi dalla dichiarazione di servizio**.

## Creare una nuova dichiarazione di servizio

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Dichiarazione di servizio**, quindi scegli il collegamento correlato.
2. Scegli l'azione **Nuovo**.
3. Compila i seguenti campi della Scheda dettaglio **Generale**.
    1. Nel campo **Codice configurazione**, specifica il codice di configurazione usato per suggerire righe e creare file. Devi scegliere una **Dichiarazione di servizio**.
    2. Nei campi **Data di inizio** e **Data di fine**, specificare le date di inizio e di fine del periodo da includere nella dichiarazione di servizio.
4. Scegli l'azione **Suggerisci righe** per avviare un processo batch che raccoglie le righe dai documenti e compila le righe della dichiarazione di servizio.

Il processo batch recupera tutti i movimenti dai documenti di acquisto e di vendita applicabili nel periodo richiesto e li aggiunge alle righe della dichiarazione di servizio. Passa con il mouse sulle righe per leggere una breve descrizione.

## Modifica una dichiarazione di servizio

Se necessario, puoi modificare le righe o aggiungerne di nuove.

1. Nella pagina **Dichiarazione di servizio**, scegli l'azione **Nuova riga** nella Scheda dettaglio **Righe**.
2. Nel campo **Tipo documento** scegli l'opzione relativa al documento che desideri usare.
3. In base al **Tipo di documento**, compila il campo **N. documento**.
4. Compilare i campi rimanenti.

## Panoramica delle righe della dichiarazione di servizio

Dopo aver creato una dichiarazione di servizio, utilizza l'azione **Panoramica** per ottenere una panoramica delle righe della dichiarazione di servizio. Puoi raggruppare e riepilogare le righe allo stesso modo del file esportato. È anche possibile aprire le righe in Excel.

## Indica la dichiarazione di servizio in un file

È possibile inviare la dichiarazione di servizio come file in base ai requisiti delle diverse autorità locali. Per creare un file:

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Dichiarazioni di servizio**, quindi scegli il collegamento correlato.
2. Scegli la dichiarazione di servizio che desideri segnalare come file.
3. Se non è stato fatto in precedenza, compila la dichiarazione di servizio manualmente o scegli l'azione **Suggerisci righe**.
4. Scegliere l'azione **Crea file**.
5. La dichiarazione di servizio verrà salvata nel formato richiesto.

## Altre considerazioni

Quando utilizzi l'estensione **Dichiarazione di servizio**, ci sono alcune altre cose da considerare. Ad esempio, è importante che i tuoi gruppi soddisfino i requisiti delle autorità. È anche importante che i servizi siano inclusi correttamente nei documenti di vendita e acquisto.

### Raggruppamento di righe

Nelle righe della dichiarazione di servizio non è presente alcun raggruppamento per campo. Tutte le voci vengono copiate dal documento originale come origine.

Il raggruppamento richiesto dalle autorità verrà fornito nel file esportato. Devi configurarle i gruppi in **Definizione scambio dati**, che è completamente configurabile. Per ulteriori informazioni vedi [Impostare le definizioni di scambio di dati](across-how-to-set-up-data-exchange-definitions.md).

### Utilizzo dei servizi nelle righe del documento

Quando crei una fattura di acquisto, di vendita o di servizio, nelle relative righe troverai due campi relativi alle dichiarazioni di servizio. Entrambi i campi sono compilati con i valori predefiniti dell'articolo, della risorsa o delle impostazioni di addebito articolo.

- **Codice tipo di transazione di servizio**: specifica il codice per un tipo di transazione di servizio.
- **Applicabile per la dichiarazione di servizio**: specifica se un articolo o una risorsa è applicabile per una dichiarazione di servizio.

È possibile modificare i valori in questi campi, ma se si seleziona il campo **Applicabile per la dichiarazione di servizio**, è necessario specificare un valore nel campo **Codice tipo di transazione di servizio**. Se non lo fai, non puoi pubblicare il documento.

Se specifichi un valore nel campo **Codice tipo di transazione di servizio** ma non selezioni il campo **Applicabile per la dichiarazione di servizio**, puoi pubblicare il documento ma la riga non verrà calcolata quando lo fai.

## Vedere anche

[Impostare il reporting Intrastat](finance-how-setup-report-intrastat.md)
[Report Intrastat in Business Central](finance-how-report-intrastat.md)  
[Gestione contabile](finance.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
