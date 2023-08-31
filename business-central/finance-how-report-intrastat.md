---
title: Utilizzare il reporting Intrastat
description: Scopri come dichiarare gli scambi con aziende in altri paesi o aree geografiche dell'UE utilizzando il sistema Intrastat.
author: altotovi
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, Intrastat, trade, EU, European Union'
ms.search.form: '308, 309, 310, 311, 325, 326, 327, 328, 405, 406, 4810, 4811, 8451, 12202, 31077'
ms.date: 09/02/2022
ms.author: altotovi
---
# <a name="work-with-intrastat-reporting"></a>Usare il report Intrastat

Tutte le società dell'Unione Europea (UE) devono creare report relativi alle attività commerciali con altri paesi UE. È necessario presentare ogni mese alle autorità statistiche del proprio paese report relativi al movimento delle merci, che devono quindi essere inviati alle autorità fiscali. Intrastat è il sistema per la raccolta di statistiche commerciali di prodotti all'interno di questi paesi/aree geografiche. Usa **Report Intrastat** per completare il reporting Intrastat periodico (tipicamente mensile), la raccolta, la registrazione e i report degli scambi di prodotti secondo la legislazione del governo locale.

Il reporting Intrastat si basa sui regolamenti di base dell'UE che si applicano a tutti i paesi o aree geografiche, tuttavia, in pratica, vi sono alcune differenze all'interno dei singoli paesi o aree geografiche. Ogni paese/area geografica ha le sue regole su cosa e come dichiarare esattamente.

> [!IMPORTANT]
> Questo articolo descrive la nuova esperienza Intrastat disponibile in [!INCLUDE[prod_short](includes/prod_short.md)] a partire dal secondo ciclo di rilascio del 2022, che include funzionalità estese e [deve essere attivata per le società esistenti](finance-how-setup-report-intrastat.md#enable-the-new-intrastat-experience). Contatta l'amministratore per attivare e configurare la nuova funzionalità.
>
> Leggi l'articolo sulla configurazione e l'utilizzo di Intrastat della versione precedente in [Impostazione e report Intrastat](finance-how-setup-report-intrastat-v20.md).

> [!NOTE]
> Le informazioni Intrastat non si applicano alla circolazione di servizi tra paesi/aree geografiche, ma solo a beni (articoli e cespiti). Se il governo locale richiede la registrazione della circolazione dei servizi tra paesi o aree geografiche, è possibile farlo utilizzando la funzionalità **Dichiarazione di servizio**.
>
> Al momento prevediamo che questa funzione sarà disponibile da novembre 2022 come app in [AppSource](https://go.microsoft.com/fwlink/?linkid=2081646). A quel punto, per usarla, devi prima installarla nella pagina **Gestione estensioni**.

## <a name="fill-in-the-intrastat-report"></a>Compilare il report Intrastat

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Lista Intrastat**, quindi scegli il collegamento correlato.
2. Scegli l'azione **Nuovo** per creare un nuovo **report Intrastat**.
3. Se hai bisogno di inserire alcune informazioni interne sul **Report Intrastat**, inserisci queste informazioni nel campo **Descrizione**.
4. Nel campo **Periodo statistico** specifica il mese per il quale riportare i dati. Immetti il periodo come numero di quattro cifre senza spazi o simboli. A seconda del tuo paese/area geografica, inserisci prima il mese e poi l'anno o viceversa. Immetti, ad esempio, *2206* o *0622* per indicare giugno 2022.
5. Scegliere l'azione **Suggerisci righe**. I campi **Data inizio** e **Data fine** verranno compilati automaticamente con le date specificate per il periodo statistico dell'intestazione report Intrastat.
6. Nel campo **% regolazione costi** è possibile immettere una percentuale per coprire trasporto e assicurazione. In questo caso il valore contenuto del campo **Valore Statistico** sarà proporzionalmente maggiore. Ma se vuoi usare questa funzione, devi cambiare il campo **Importo inclusi addebiti articoli** su **sì**.
7. È possibile eventualmente impostare configurazioni aggiuntive nella scheda dettaglio **Aggiuntivo**:
   1. **Ignora ricalcolo per importi pari a zero** per specificare che le righe senza importi non verranno ricalcolate durante il processo batch.
   2. **Ignora importi pari a zero** per specificare che i movimenti contabili articoli senza importi non vengono ricalcolati nel processo batch.
   3. **Mostra movimenti addebito articolo** per specificare se mostrare i costi diretti che la società ha assegnato e registrato come addebiti articolo.
   4. **Ignora movimenti non fatturati** per specificare se i movimenti contabili articoli spediti o ricevuti ma non ancora fatturati devono essere esclusi dal processo.
8. Selezionare **OK** per avviare il processo batch.

Il processo batch recupererà tutti i movimenti articolo nel periodo statistico indicato e li inserirà come righe del **Report Intrastat**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="modify-the-intrastat-report"></a>Modificare il report Intrastat

Se necessario, è possibile modificare le righe, ma ogni volta che si modifica un valore nella riga del report Intrastat, il campo **Correzione** verrà automaticamente contrassegnato come **sì**. In caso, puoi aggiungere una nuova riga manualmente se c'è una ragione per farlo. Per aggiungere una nuova riga manualmente:

1. Nella pagina **Report Intrastat**, scegli l'azione **Nuova riga** nella Scheda dettaglio **Righe**.
2. Scegli l'opzione **Ricevuta** o **Spedizione** nel campo **Tipo**.
3. Nel campo **Tipo di origine** scegli una delle origini: **movimento articolo**, **movimento cespite**, o **movimento commessa**.
4. In base al **Tipo di origine** nel campo **Nr. articolo**, puoi scegliere un **movimento** (in entrambi i casi, **movimento articolo** o **movimento commessa**) o i **cespiti**.
5. Compila gli altri campi necessari per il reporting Intrastat.

> [!NOTE]
> Quando aggiungi manualmente una nuova riga al report Intrastat, il campo **Data** nella riga deve essere all'interno dell'intervallo **Periodo statistico** che hai aggiunto nell'intestazione.

## <a name="validate-intrastat-lines"></a>Convalidare le righe Intrastat

Dopo aver compilato il **Report Intrastat**, è possibile eseguire l'azione **Report elenco di controllo** per verificare che tutte le informazioni nel **Report Intrastat** siano corrette. I campi obbligatori impostati nella pagina **Elenco di controllo report Intrastat** in cui mancano i valori verranno mostrati in Dettaglio informazioni di **Errori e avvisi** nella pagina **Report Intrastat**.

Esegui il report **Elenco di controllo report Intrastat** per controllare le righe Intrastat prima che vengano esportate nel formato richiesto. Il controllo viene eseguito all'interno del **Report Intrastat**.

## <a name="recalculating-weight-or-supplementary-unit-of-measure"></a>Ricalcolo del peso o dell'unità di misura supplementare

Se hai ricevuto il messaggio di errore *"Peso totale" nella riga del report Intrastat non deve essere vuoto*, probabilmente è perché non hai impostato il campo **Peso netto** sull'origine, sull'articolo o sul cespite utilizzato. In questo caso, cerca l'articolo o la scheda cespiti e aggiungi il valore richiesto. Dopodiché, devi solo riaprire il **Report Intrastat** e seguire questi passaggi:

1. Scegli l'azione **Ricalcola peso/UDM supplementare** per ricalcolare il **Peso totale** e/o la **Quantità supplementare**.
2. Seleziona una delle seguenti opzioni:

    1. **Peso** – per ricalcolare solo il **Peso totale**, in base alle informazioni attuali su **Peso netto** nelle schede articolo e cespite.
    2. **Qtà UDM supplementare** – per ricalcolare solo la **Quantità supplementare** sulla riga del **Report Intrastat** se esiste, in base alle informazioni correnti su **UDM supplementare** nelle schede articolo e cespite.
    3. **Entrambi** – per ricalcolare il **Peso totale** e la **Quantità supplementare**, in base alle informazioni attuali nelle schede articolo e cespite.
3. Seleziona **OK** per avviare il processo batch.

## <a name="report-intrastat-in-a-file"></a>Creare un report Intrastat in un file

È possibile inviare il report Intrastat come file in base ai requisiti delle diverse autorità locali. Prima di creare il file, è necessario eseguire **Report elenco di controllo** per verificare se tutte le righe contengono tutte le informazioni necessarie e valide. Per creare un file:

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Lista Intrastat**, quindi scegli il collegamento correlato.
2. Scegli il **report Intrastat** che vuoi segnalare come file.
3. Se non è stato fatto in precedenza, compila il **Report Intrastat** manualmente o scegli l'azione **Suggerisci righe**.
4. Scegliere l'azione **Crea file**.
5. Il file Intrastat verrà salvato nel formato richiesto.

Una volta creato il file, [!INCLUDE[prod_short](includes/prod_short.md)] compilerà automaticamente i seguenti dettagli sul report:

* La **data di esportazione** per specificare la data in cui il report è stato esportato.
* L'**ora di esportazione** per specificare l'ora in cui il report è stato esportato.

> [!NOTE]
> La prossima volta che crei un file, i campi **Data di esportazione** e **Ora di esportazione** manterranno solo le informazioni sull'ultimo file che hai creato.

## <a name="intrastat-rules"></a>Regole Intrastat

### <a name="grouping-lines"></a>Raggruppamento di righe

Nelle righe del **Report Intrastat** non vi è alcun raggruppamento per nessun campo. Tutti movimenti vengono copiati dalla fonte originale, quindi puoi individuarli rapidamente in base alla combinazione di **Tipo di origine** e **Nr. movimento di origine**.

Il raggruppamento richiesto dalle autorità verrà fornito nel file esportato. Devi configurarlo nella **Definizione scambio dati**, che è completamente configurabile. Per ulteriori informazioni vedi [Impostare le definizioni di scambio di dati](across-how-to-set-up-data-exchange-definitions.md).

### <a name="fixed-assets-reporting"></a>Report cespiti

I cespiti verranno visualizzati nelle righe Intrastat solo se:

* Il **Tipo di registrazione cespiti** nel campo **Movimento contabile IVA** è **Costo di acquisizione** e se il **Tipo di documento** è **Fattura** in caso di acquisti, e
* Il **Tipo di registrazione cespiti** nel campo **Movimento contabile IVA** è **Proventi di cessione** e se il **Tipo di documento** è **Fattura** in caso di vendite.

### <a name="intrastat-report-statuses"></a>Stati del report Intrastat

Quando lavori con il **Report Intrastat** vedrai un campo **Stato** nell'intestazione del documento. È possibile trovare i seguenti stati insieme alle relative regole:

* *Aperto* : questo stato viene creato automaticamente quando crei un nuovo report Intrastat e puoi eseguire tutte le operazioni in questo stato.
* *Rilasciato*: [!INCLUDE[prod_short](includes/prod_short.md)] cambia automaticamente lo stato in *Rilasciato* quando crei un file. Da quel momento, non puoi modificare il **Report Intrastat**. Se è necessario modificare qualcosa e segnalare nuovamente, è possibile utilizzare l'azione **Riapri** per riaprire il report Intrastat. Una volta riaperto il documento, è possibile utilizzare l'azione **Rilascia** per rilasciare nuovamente il documento.
* **Riportato**: Specifica se il movimento è già stato comunicato alle autorità fiscali. Questo non è uno stato normale ma un campo indipendente e, anche se hai riaperto il report Intrastat, mostra comunque che il file è già stato creato per questo report.

### <a name="triangular-trade-in-intrastat"></a>Commercio triangolare in Intrastat

Il commercio triangolare prevede il commercio tra tre paesi o regioni in cui le merci bypassano il paese della società di reporting. In Business Central, ciò può essere facilitato tramite la funzionalità [Spedizione diretta](sales-how-drop-shipment.md) . Per abilitare questa opzione, attiva il campo **Includi spedizione diretta** in **Setup report Intrastat**.  

Quando abiliti questa opzione, il sistema utilizza le seguenti regole, ma solo se hai contrassegnato  **Spedizione diretta** in **Ordine di vendita**: 

| Ricevuto da | In consegna a | Risultato Intrastat previsto |
|----------|------------|----------------------|
| Paese come in **Informazioni società** | Paese come in **Informazioni società** | Nessuna riga Intrastat |  
| Paese come in **Informazioni società** | Paese UE diverso dal paese indicato nelle **Informazioni società** | Riga spedizione Intrastat | 
| Paese come in **Informazioni società** | Paese extra UE | Nessuna riga Intrastat |   
| Paese UE diverso dal paese indicato nelle **Informazioni società** | Paese come in **Informazioni società** | Riga ricezione Intrastat | 
| Paese UE diverso dal paese indicato nelle **Informazioni società** | Paese UE diverso dal paese indicato nelle **Informazioni società** | Nessuna riga Intrastat |
| Paese UE diverso dal paese indicato nelle **Informazioni società** | Paese extra UE | Nessuna riga Intrastat | 
| Paese extra UE | Paese come in **Informazioni società** | Nessuna riga Intrastat |  
| Paese extra UE | Paese UE diverso dal paese indicato nelle **Informazioni società** | Nessuna riga Intrastat |
| Paese extra UE | Paese extra UE | Nessuna riga Intrastat |   

## <a name="see-related-training-at-microsoft-learn"></a>Vedi le informazioni relative al training in [Microsoft Learn](/learn/modules/process-intrastat-dynamics-365-business-central/index).

## <a name="see-also"></a>Vedere anche

[Impostare il report Intrastat](finance-how-setup-report-intrastat.md)  
[Gestione contabile](finance.md)  
[Spedizione diretta](sales-how-drop-shipment.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
