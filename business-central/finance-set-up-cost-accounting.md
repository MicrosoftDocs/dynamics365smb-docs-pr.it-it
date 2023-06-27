---
title: Impostazione della contabilità industriale
description: 'Prima di iniziare a utilizzare la contabilità industriale, è necessario effettuare l''impostazione. A ogni movimento di costo deve essere assegnato un tipo di costo e un codice del centro di costo o un oggetto di costo.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '1100, 1112, 1113, 1122'
ms.date: 06/16/2021
ms.author: edupont
---
# <a name="setting-up-cost-accounting"></a>Impostazione della contabilità industriale

Prima di iniziare a utilizzare la contabilità industriale, è necessario effettuare attività di impostazione.

## <a name="balances-between-cost-type-cost-center-and-cost-object"></a>Saldi tra tipo di costo, centro di costo e oggetto di costo

Quando si imposta la contabilità industriale, è necessario assicurarsi che tutti i movimenti vengano assegnati a un tipo di costo, nonché a un centro di costo o a un oggetto di costo. Pertanto, a ogni movimento di costo deve essere assegnato un tipo di costo e un codice del centro di costo o un oggetto di costo. Questa regola garantisce la visualizzazione di ciascun movimento di costo nei centri di costo o negli oggetti di costo, ma mai in entrambe le aree.  

Tale operazione consente di creare la seguente equazione di contabilità:  

*Saldo tipo di costo* = *Saldo centro di costo* + *Saldo oggetto di costo*  

Quando si stampano i report dei grafici del tipo di costo, dei centri di costo e degli oggetti di costo, è possibile analizzare questa relazione.

## <a name="setting-up-cost-types"></a>Impostazione di tipi di costo

Il piano dei tipi di costo è simile al piano dei conti nella contabilità generale. È possibile impostare il piano dei tipi di costo nelle modalità seguenti:  

- Strutturare il piano dei tipi di costo in modo analogo ai conti economici del piano dei conti della contabilità generale. Successivamente, il piano dei conti della contabilità generale può essere trasferito al piano dei tipi di costo. È possibile apportare tutte le rettifiche necessarie dopo il trasferimento.  
- Creare un nuovo piano dei tipi di costo o aggiungere nuovi tipi di costo al piano dei tipi di costo esistente. È necessario creare ogni nuovo tipo di costo singolarmente.  

### <a name="to-transfer-the-general-ledger-chart-of-accounts-to-the-chart-of-cost-types"></a>Per trasferire il piano dei conti della contabilità generale al piano dei tipi di costo

1. Scegli la ![lampadina che apre la funzione Dimmi 1](media/ui-search/search_small.png "Dimmi cosa vuoi fare"). immetti **Piano dei tipi di costo**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Ottieni tipi costo da piano dei conti**. Nella finestra di dialogo fare clic sul pulsante **Sì** per confermare il trasferimento. La funzione utilizza il piano dei conti per creare un piano dei tipi di costo.  

    Il piano dei tipi di costo contiene ora tutti i conti economici nella contabilità generale e include le testate e i subtotali. È possibile modificare il piano dei tipi di costo, in base alle esigenze. Ad esempio, è possibile eliminare i tipi di costo esistenti duplicati.  

    > [!IMPORTANT]  
    >  Con la funzione **Registra tipi costo in piano dei conti** è possibile aggiornare la relazione tra il piano dei conti e il piano dei tipi di costo. Il campo **Nr.** viene compilato e verificato per garantire che ciascun conto di contabilità generale sia correlato a un solo tipo di costo. La funzione viene eseguita automaticamente prima del trasferimento dei movimenti C/G nella contabilità industriale.  

### <a name="to-set-up-new-cost-types-in-the-chart-of-cost-types-page"></a>Per impostare nuovi tipi di costo nella pagina Piano dei tipi di costo

1. Aprire la pagina **Piano dei tipi di costo** in modalità di modifica.  
2. Compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >  È possibile impostare e gestire tipi di costo nella scheda **Scheda tipo di costo** o nella pagina **Piano dei tipi di costo**. In questa procedura è possibile impostare i tipi di costo nella pagina **Piano dei tipi di costo**.

3. Dopo avere creato tutti i tipi di costo, scegliere l'azione **Indentazione tipi costo**. Nella finestra di dialogo scegliere il pulsante **Sì**.  
4. Collegare il nuovo tipo di costo al corrispondente conto di contabilità generale.  

    > [!IMPORTANT]  
    >  Se le definizioni per i conti sono state immesse nei campi **Totale** del tipo riga **Fine-Totale** prima di eseguire la funzione **Indentazione tipi costo**, sarà necessario inserirle nuovamente in seguito poiché questa funzione sovrascrive i valori in tutti i campi **Fine-Totale**.  

### <a name="to-update-cost-types"></a>Per aggiornare i tipi di costo

1. Nella pagina **Setup contabilità industriale** selezionare se si desidera che il piano dei tipi di costo venga aggiornato automaticamente quando il piano dei conti viene modificato.  
2. Nel campo **Allinea conto C/G** è possibile selezionare una delle seguenti opzioni.  

- **Nessun allineamento**: non esiste alcuna modifica corrispondente nel grafico dei tipi di costo quando si modifica il piano dei conti.  
- **Automatico**: viene apportata una modifica corrispondente nel grafico dei tipi di costo quando si modifica il piano dei conti.  
- **Richiesta**: viene visualizzato un messaggio in cui viene chiesto se apportare una modifica corrispondente nel grafico dei tipi di costo quando si modifica il piano dei conti.

## <a name="defining-the-relationship-between-cost-types-and-general-ledger-accounts"></a>Definizione della relazione tra i tipi di costo e i conti di contabilità generale

La relazione tra il tipo di costo e il conto di contabilità generale viene creata nel tipo di costo e nel conto di contabilità generale.  

- Tramite il campo **Intervallo conti CG** della tabella **Tipo costo** è possibile stabilire quali conti di contabilità generale appartengono a un tipo di costo.  
- Con il campo **Nr. tipo di costo** nel piano dei conti è possibile stabilire il tipo di costo a cui appartiene un conto di contabilità generale.  

Questi due campi vengono compilati automaticamente quando si utilizza la funzione **Ottieni tipi costo da piano dei conti**.  

### <a name="relationship-between-general-ledger-accounts-and-cost-types"></a>Relazione tra i conti di contabilità generale e i tipi di costo

Tra i conti di contabilità generale e i tipi di costo esiste una relazione n:1. A un tipo di costo possono appartenere più conti di contabilità generale, ma ognuno di questi appartiene a un solo tipo di costo. Nella seguente tabella vengono descritti i dettagli delle relazioni.  

|Relazione|**Intervallo conti C/G**|**Nr. tipo di costo**|  
|------------------|------------------------------------------------|-------------------------------------------|  
|Un conto di contabilità generale per ogni tipo di costo|Un conto di contabilità generale|Un tipo di costo|  
|Più conti di contabilità generale per un tipo di costo|Intervallo di conti di contabilità generale, ad esempio da 7110 a 7193, per ciascun conto di contabilità generale|Per ciascun conto di contabilità generale nell'intervallo, esiste un solo tipo di costo|  
|Tipi di costo senza conti di contabilità generale corrispondenti|\<Empty\>||  
|Conti di contabilità generale i cui movimenti non saranno trasferiti||\<Empty\>|  

### <a name="cost-types-without-a-relationship-to-the-general-ledger"></a>Tipi di costo senza una relazione con la contabilità generale

Un tipo di costo non può avere una relazione con i conti di contabilità generale se una delle seguenti condizioni è vera:  

- I conti per la contabilità operativa, ad esempio il calcolo interessi e l'ammortamento, vengono ricavati solo dalla contabilità operativa.  
- I tipi di costo di supporto, ad esempio i tipi 9901, 9902 e 9903 nel database di [!INCLUDE[prod_short](includes/prod_short.md)], vengono utilizzati come dare e avere per le allocazioni.  
- Il conto di supporto, 9920 nel database di [!INCLUDE[prod_short](includes/prod_short.md)], contiene i ratei effettivi che mostrano la differenza tra i costi e le spese della contabilità generale.

## <a name="setting-up-cost-centers"></a>Impostazione di centri di costo

I centri di costo sono i reparti responsabili dei costi e delle entrate. Il grafico dei centri di costo è simile alle informazioni sulle dimensioni relative alla contabilità generale. È possibile impostare il grafico dei centri di costo nelle modalità seguenti:  

- Trasferire i valori dimensioni nella contabilità generale al grafico dei centri di costo. È possibile apportare tutte le rettifiche necessarie dopo il trasferimento.  
- Creare un nuovo grafico del centro di costo che sia indipendente dalla contabilità generale o aggiungere un nuovo centro di costo a un grafico del centro di costo esistente. È necessario creare ogni centro di costo singolarmente.  

### <a name="to-transfer-dimension-values-in-the-general-ledger-to-the-chart-of-cost-centers"></a>Per trasferire i valori dimensioni nella contabilità generale al grafico dei centri di costo

1. Impostare una dimensione come dimensione centro di costo nella pagina **Aggiorna dimensioni cont. industriale** . Solo i valori di questa dimensione vengono trasferiti.  
2. Scegli la ![lampadina che apre la funzione Dimmi 2](media/ui-search/search_small.png "Dimmi cosa vuoi fare"). immetti **Piano dei centri di costo**, quindi scegli il collegamento correlato.  
3. Nel gruppo **Funzioni** della scheda **Azioni** selezionare **Ottieni centri di costo da dimensione** per trasferire i valori dimensioni al grafico dei centri di costo. Con la funzione è possibile trasferire i valori dimensioni definiti nel passaggio 1.  

    > [!NOTE]  
    >  È possibile impostare il campo **Allinea dimensione centro di costo** per definire una sincronizzazione unidirezionale dei valori delle dimensioni della contabilità generale con il piano dei centri di costo. Non è possibile definire una sincronizzazione del grafico dei centri di costo con i valori dimensioni della contabilità generale.  

Il grafico dei centri di costo contiene ora tutti i valori dimensioni specificati della contabilità generale e include i titoli e i subtotali.  

### <a name="to-create-new-cost-centers-in-the-chart-of-cost-centers-page"></a>Per creare nuovi centri di costo nella pagina Piano dei centri di costo

È possibile impostare e gestire centri di costo nella scheda **Scheda centro di costo** o nella pagina **Piano dei centri di costo**. In questa procedura è possibile impostare i centri di costo nella pagina **Piano dei centri di costo**.  

1. Aprire la pagina **Piano dei centri di costo** in modalità di modifica.  
2. Nel campo  **Codice** immettere il codice centro di costo. Tutti i centri di costo devono disporre di un codice.  
3. Nel campo **Nome** immettere il nome del centro di costo.  
4. Fare clic sulla freccia a discesa nel campo **Tipo riga** per specificare lo scopo del centro di costo.  

    - Per i centri di costo di tipo **Totale** compilare il campo **Totale**. Utilizzare l'operatore **or**, che è una barra verticale (**&#124;**) per impostare intervalli di centri di costo.  
    - Per i centri di costo del tipo di riga **Fine-Totale**, questo campo viene compilato automaticamente quando si utilizza la funzione di indentazione.  
5. Compilare i campi **Ordinamento** e **Sottotipo costo**.  
6. Scegliere la successiva riga vuota per creare un nuovo centro di costo, quindi ripetere i passaggi da 2 a 5.  
7. Dopo aver impostato tutti i centri di costo, scegliere l'azione **Indentazione centri di costo**. Scegliere il pulsante **Sì**.  

> [!IMPORTANT]  
> Se sono state immesse definizioni nei campi **Totale** per i centri di costo **Fine-Totale** prima di eseguire la funzione di indentazione, è necessario inserirle di nuovo. Questa funzione consente di sovrascrivere i valori in tutti i campi **Fine-Totale**.

## <a name="setting-up-cost-objects"></a>Impostazione di oggetti di costo

Gli oggetti di costo sono i progetti, i prodotti o i servizi di una società. Il grafico degli oggetti di costo è simile alle informazioni sulle dimensioni relative alla contabilità generale. È possibile impostare il grafico degli oggetti di costo nelle modalità seguenti:  

* Trasferendo i valori dimensioni nella contabilità generale al grafico degli oggetti di costo. È possibile apportare tutte le rettifiche necessarie dopo il trasferimento.  
* Creando un nuovo grafico dell'oggetto di costo che sia indipendente dalla contabilità generale o aggiungendo un nuovo oggetto di costo a un grafico degli oggetti di costo esistente. È necessario creare ogni oggetto di costo singolarmente.  

### <a name="to-transfer-dimension-values-from-the-general-ledger-to-the-chart-of-cost-objects"></a>Per trasferire i valori dimensioni dalla contabilità generale al grafico degli oggetti di costo

1.  Impostare una dimensione come dimensione dell'oggetto di costo nella pagina **Aggiorna dimensioni contabilità industriale**. Solo i valori di questa dimensione vengono trasferiti.  
2.  Scegli la ![lampadina che apre la funzione Dimmi 3](media/ui-search/search_small.png "Dimmi cosa vuoi fare"). immetti **Piano degli oggetti di costo**, quindi scegli il collegamento correlato.  
3.  Scegliere l'azione **Ottieni oggetti di costo da dimensione** per trasferire i valori dimensioni al piano degli oggetti di costo. Con la funzione è possibile trasferire i valori dimensioni definiti nel passaggio 1.  

    > [!NOTE]  
    >  È possibile impostare il campo **Allinea dimensione oggetto di costo** per definire una sincronizzazione unidirezionale dei valori delle dimensioni della contabilità generale con il piano degli oggetti di costo. Non è possibile definire una sincronizzazione del grafico degli oggetti di costo con i valori dimensioni della contabilità generale.  

Il grafico degli oggetti di costo contiene ora tutti i valori dimensioni specificati della contabilità generale e include i titoli e i subtotali.  

### <a name="to-create-new-cost-objects-in-the-chart-of-cost-objects-page"></a>Per creare nuovi oggetti di costo nella pagina Piano degli oggetti di costo

È possibile impostare e gestire oggetti di costo nella scheda **Scheda oggetto di costo** o nella pagina **Piano degli oggetti di costo**. In questa procedura è possibile impostare gli oggetti di costo nella pagina **Piano degli oggetti di costo**.  

1.  Aprire la pagina **Piano dei tipi di costo** in modalità di modifica.  
2.  Nel campo  **Codice** immettere il codice oggetto di costo. Tutti gli oggetti di costo devono disporre di un codice.  
3.  Nel campo **Nome** immettere il nome dell'oggetto di costo.  
4.  Fare clic sulla freccia a discesa nel campo **Tipo riga** per specificare lo scopo dell'oggetto di costo.  

    * Per gli oggetti di costo di tipo riga **Totale** compilare il campo **Totale da/a**. Utilizzare l'operatore **or**, vale a dire una riga verticale (**&#124;**), per impostare gli intervalli degli oggetti di costo.  
    * Per gli oggetti di costo del tipo di riga **Fine-Totale**, questo campo viene compilato automaticamente quando si utilizza la funzione di indentazione.  
5.  Compilare il campo **Ordinamento**.  
6.  Selezionare la successiva riga vuota per creare un nuovo oggetto di costo, quindi ripetere i passaggi da 2 a 5.  
7.  Dopo aver impostato tutti gli oggetti di costo, scegliere l'azione **Indentazione oggetti di costo**. Scegliere il pulsante **Sì**.  

> [!IMPORTANT]  
>  Se sono state immesse definizioni nei campi **Totale da/a** per gli oggetti di costo **Fine-Totale** prima di eseguire la funzione di indentazione, è necessario inserirle di nuovo. Questa funzione consente di sovrascrivere i valori in tutti i campi **Fine-Totale**.

## <a name="defining-cost-centers-and-cost-objects-for-chart-of-accounts"></a>Definizione dei centri di costo e degli oggetti di costo per il piano dei conti

È possibile trasferire automaticamente i movimenti delle entrate e delle spese della contabilità generale alla contabilità industriale per ogni registrazione di contabilità generale o tramite un processo batch. Durante il trasferimento, con [!INCLUDE[prod_short](includes/prod_short.md)] è possibile trasferire solo i movimenti che sono già stati collegati a un centro di costo o a un oggetto di costo. Per stabilire un trasferimento significativo, è necessario assicurarsi che i centri di costo e gli oggetti di costi siano correttamente definiti.  

### <a name="defining-default-dimension-values-for-general-ledger-accounts"></a>Definizione dei valori dimensioni di default per i conti di contabilità generale

Per ogni conto di contabilità generale, è possibile definire i valori dimensioni di default nella tabella **Dimensione di default**. Nell'esempio seguente viene illustrato come sia sempre necessaria la presenza di un centro di costo REPARTO e mai quella di un oggetto di costo PROGETTO quando si effettua una registrazione in un conto di contabilità generale.  

|**Codice dimensione**|**Registrazione valore**|  
|------------------------------------------|-----------------------------------------|  
|Reparto|Codice obbligatorio|  
|Progetto|Nessun Cod.|  

### <a name="defining-dimension-values-for-overhead-costs-and-direct-costs"></a>Definizione dei valori dimensioni per i costi generali e diretti

 È possibile trasferire i costi generali a un centro di costo e i costi diretti a un oggetto di costo. Nella tabella seguente viene mostrata la combinazione ottimale dei valori di impostazione delle dimensioni.  

|Trasferisci a|Registrazione del centro di costo|Registrazione dell'oggetto di costo|  
|-----------------|-------------------------|-------------------------|  
|Centro di costo|Codice obbligatorio|Nessun Cod.|  
|Oggetto di costo|Nessun Cod.|Codice obbligatorio|  

> [!NOTE]  
>  Per garantire che il centro di costo e l'oggetto di costo predefiniti impostati nella contabilità generale vengano riportati automaticamente nella contabilità industriale, selezionare la casella di controllo **Verifica registrazioni CG** nella pagina Setup contabilità industriale.

## <a name="see-related-microsoft-training"></a>Vedi il relativo [training Microsoft](/training/modules/cost-accounting-dynamics-365-business-central/)

## <a name="see-also"></a>Vedere anche

[Contabilizzazione dei costi](finance-manage-cost-accounting.md)  
[Trasferimento e registrazione di movimenti di costi](finance-transfer-and-post-cost-entries.md)  
[Definizione e allocazione dei costi](finance-define-and-allocate-costs.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
