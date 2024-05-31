---
title: Acquisizione dei cespiti
description: 'È possibile impostare un cespite, assegnare un registro beni ammortizzabili e registrare il costo di acquisizione del cespite.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: purchase fixed asset
ms.search.form: '5605, 5551, 5600, 5628, 5629, 5633'
ms.date: 05/15/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="acquire-fixed-assets"></a>Acquisizione dei cespiti

Utilizza la pagina **Scheda cespite** per inserire informazioni su un cespite. È possibile impostare edifici o attrezzature di produzione come bene principale con un elenco di componenti ed è possibile raggrupparli in vari modi, ad esempio per classe, reparto o ubicazione. È necessario impostare e attribuire un registro beni ammortizzabili a ciascun cespite prima di poterlo acquisire.

Dopo aver impostato un cespite e assegnato un registro beni ammortizzabili, è necessario acquisire il cespite. Per acquisire un cespite, occorre registrare il costo di acquisizione nel relativo conto C/G, conto bancario o fornitore registrando una transazione di acquisizione dalla pagina **Registrazioni cespiti in C/G**. È possibile utilizzare la pagina **Acquisizione assistita cespiti** per creare e registrare le righe registrazioni COGE richieste automaticamente.

Utilizzare l'indicizzazione per adeguare i valori alle variazioni generali del livello dei prezzi. Utilizzare il processo batch **Indice cespiti** per calcolare i costi di acquisizione e i costi di sostituzione.

## <a name="add-a-fixed-asset-to-your-list-of-fixed-assets"></a>Aggiungere un cespite all'elenco dei cespiti

Prima di poter acquisire un cespite, è necessario aggiungerlo all'elenco dei cespiti. Esistono diversi modi per aggiungere cespiti all'elenco:

* Immettere le informazioni sulle risorse nella pagina  **Scheda cespiti** .
* Utilizza l'azione **Modifica in Excel** per scaricare l'elenco delle risorse in un foglio di lavoro, aggiungere nuove risorse all'elenco e quindi pubblicare l'aggiornamento in [!INCLUDE [prod_short](includes/prod_short.md)].
* Utilizzare un ordine di acquisto per aggiungere asset.
* Utilizzare l'azione **Copia cespite** .

Dopo aver aggiunto i cespiti all'elenco, il passaggio successivo consiste nell'acquisirli in modo da poterli utilizzare nelle transazioni. Scopri di più su [Acquisire un cespite](#acquire-fixed-assets).

### <a name="add-a-fixed-asset-on-the-fixed-asset-card-page"></a>Aggiungere un cespite nella pagina Scheda cespite

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Cespiti**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Nuovo** e compilare i campi necessari della Scheda dettaglio **Generale**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Nella Scheda dettaglio **Registro beni ammortizzabili** compilare i campi secondo le necessità. In questo passaggio viene assegnato un registro beni ammortizzabili al cespite.  
4. Se è necessario assegnare più di un registro beni ammortizzabili al cespite, scegliere l'azione **Aggiungi più registri beni ammortizzabili**. Per ulteriori informazioni, vedere [Per assegnare un registro beni ammortizzabili a un cespite](fa-how-setup-depreciation.md#to-assign-a-depreciation-book-to-a-fixed-asset).

    Dopo aver compilato i campi obbligatori, **Sei pronto per acquisire il cespite.** La notifica viene visualizzata nella parte superiore della pagina. Se sei pronto per acquisire la risorsa adesso, scegli l'azione **Acquisisci** . Segui i passaggi nella pagina  **Acquisizione assistita di cespiti** per completare l'acquisizione. Se non sei pronto, puoi sempre acquisire la risorsa in un secondo momento.

### <a name="use-edit-in-excel-to-add-assets"></a>Utilizza Modifica in Excel per aggiungere risorse

Se desideri aggiungere numerosi cespiti, Modifica in Excel è un ottimo strumento da utilizzare. Lo strumento scarica l'elenco corrente dei cespiti in un foglio di lavoro che include la maggior parte dei campi disponibili nella pagina Scheda cespite. Puoi compilare alcuni o tutti i campi su una riga per ciascuna risorsa e pubblicare le modifiche per aggiungerle al tuo elenco in [!INCLUDE [prod_short](includes/prod_short.md)]. Se non riesci a compilare tutti i campi obbligatori, va bene. Puoi aggiornarli  [!INCLUDE [prod_short](includes/prod_short.md)] quando sei pronto.

> [!NOTE]
> Per utilizzare l'azione Modifica in Excel, è necessario che sia installato il Microsoft Dynamics componente aggiuntivo di Office. Il componente aggiuntivo crea la connessione tra Excel e [!INCLUDE [prod_short](includes/prod_short.md)]. Per ulteriori informazioni, vai a [Ottenere il componente aggiuntivo Business Central per Excel](admin-deploy-excel-addin.md).

1. Scegli l'icona ![lampadina che apre la funzionalità Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Cespiti**, quindi scegli il collegamento correlato.
2. Scegli l'icona  :::image type="content" source="media/share-icon.png" alt-text="Condividi questa pagina con altri utenti o app."::: , quindi scegli **Modifica in Excel**.
3. Aprire il file scaricato e immettere le informazioni sui nuovi cespiti.

   > [!TIP]
   > Non è necessario inserire un identificatore nel  **No.** . Quando pubblichi l'aggiornamento, [!INCLUDE [prod_short](includes/prod_short.md)] assegna un identificatore in base alla serie numerica utilizzata per i cespiti.

4. Per aggiornare [!INCLUDE [prod_short](includes/prod_short.md)], nel riquadro **Microsoft Dynamics** scegli **Pubblica**.

### <a name="add-a-fixed-asset-from-a-purchase-order-or-invoice"></a>Aggiungere un cespite da un ordine di acquisto o da una fattura

I passaggi seguenti descrivono come aggiungere un cespite da un ordine di acquisto. I passaggi sono simili per una fattura di acquisto.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ordini acquisto**, quindi scegli il collegamento correlato.
2. Scegli **Nuovo** per creare un nuovo ordine d'acquisto.
3. Compilare i campi appropriati nella Scheda dettaglio **Generale**. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)]
4. Nella scheda dettaglio **Righe**, nel campo **Tipo** scegliere **Cespite**.
5. Nel campo **Nr.** Campo, scegliere un cespite esistente per aggiungere una spesa oppure scegliere **Nuovo** per aggiungere un nuovo cespite.
6. Dopo aver immesso le informazioni per la nuova risorsa e l'ordine di acquisto, seleziona **Registra**.

## <a name="acquire-a-fixed-asset-by-using-a-fixed-asset-gl-journal"></a>Acquisire un cespite utilizzando un giornale di registrazione CoGe cespite

La seguente procedura descrive come acquisire creando e registrando le righe di registrazione CoGe cespiti richieste. È inoltre possibile creare e registrare manualmente le righe di registrazione. Per ulteriori informazioni, consultare [Acquisire un cespite utilizzando un giornale di registrazione CoGe cespiti](#acquire-a-fixed-asset-by-using-a-fixed-asset-gl-journal).

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Cespiti**, quindi scegli il collegamento correlato.
1. Scegli la risorsa che desideri acquisire, quindi scegli l'azione **Acquisisci** .
1. Segui i passaggi nella pagina  **Acquisizione assistita di cespiti** per completare l'acquisizione.

> [!NOTE]  
> È inoltre possibile registrare i costi di acquisizione in Avere. In tal caso, ricordare che il valore nel campo **Costo di acquisizione IVA inclusa** deve avere il segno meno per indicare un credito.

Quando scegli **Finisci**, il campo **Valore contabile** nella **Scheda cespite**  è compilata, che indica che il cespite è stato acquisito al costo di acquisizione specificato.  

## <a name="to-post-a-fixed-asset-acquisition-manually-with-a-fixed-asset-gl-journal"></a>Per registrare manualmente un'acquisizione cespiti con un giornale di registrazione CoGe cespiti

Di seguito viene descritto come acquistare manualmente un cespite creando e registrando le righe nella pagina **Reg. cespiti in G/L**. È anche possibile acquisire un cespite automaticamente nella pagina **Scheda cespite** scegliendo l'azione **Acquisisci cespite** . Per ulteriori informazioni, vai a [Acquisire un cespite](#acquire-fixed-assets).

> [!NOTE]  
> È inoltre possibile registrare i costi di acquisizione in Avere. In tal caso, ricordare che il valore nel campo **Importo** deve avere il segno meno per indicare un credito.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registrazioni cespiti in C/G**, quindi scegli il collegamento correlato.
2. Nella pagina **Registrazioni cespiti in C/G**, nel campo **Tipo reg. cespite** selezionare **Costo di acquisto**.
3. Compilare i rimanenti campi, se necessario.
4. Scegli l'azione **Registra**.  

> [!TIP]  
> Se si compila il campo **N. assicurazione**, [!INCLUDE[prod_short](includes/prod_short.md)] registra anche il costo di acquisizione del cespite nel registro della copertura assicurativa. Per saperne di più, vai a [Assicurare le immobilizzazioni](fa-how-insure.md).

## <a name="to-set-up-a-component-list-for-a-main-asset"></a>Per impostare una lista di componenti per un bene principale

I cespiti possono essere raggruppati in beni principali e componenti. Ad esempio, potresti avere una macchina di produzione composta da diverse parti che desideri raggruppare in questo modo.  

È necessario impostare il cespite principale e tutti i suoi componenti come singolo cespite. Dopo aver impostato un elenco di componenti, [!INCLUDE[prod_short](includes/prod_short.md)] compila automaticamente **Componente/asset principale** e **Componenti dell'asset principale** campi relativi alle immobilizzazioni.

1. Scegli l'icona ![lampadina che apre la funzionalità Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Cespiti**, quindi scegli il collegamento correlato.
2. Selezionare il cespite che costituisce il bene principale, quindi scegliere l'azione **Componenti bene principale**.
3. Nella pagina **Componenti bene principale** scegliere il campo **Nr. cespite**, quindi selezionare il cespite che si desidera aggiungere come componente del bene principale.
4. Chiudere la pagina.
5. Ripetere i passaggi 3 e 4 per ogni bene componente che si intende aggiungere.
6. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup cespiti**, quindi scegli il collegamento correlato.
7. Attiva l'interruttore **Consenti pubblicazione su risorse principali** .

## <a name="to-cancel-an-acquisition-cost-posting-for-one-fixed-asset"></a>Per annullare una registrazione di costo di acquisto per un cespite

In caso di errore nella registrazione di un costo di acquisto, è possibile rimuovere il movimento con il processo batch **Rimuovi mov. cespiti** e registrare il movimento di acquisto corretto. I movimenti errati vengono trasferiti alla pagina **Mov. cont. cespiti errati**.

Ad esempio, se si registra un acquisto con la data errata, è necessario correggerla prontamente perché la data di registrazione del cespite viene utilizzata in diversi calcoli.

> [!IMPORTANT]  
> Non è possibile utilizzare l'azione **Storna transazioni** per i movimenti dei cespiti.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immettere **Movimenti contabili cespiti**, quindi scegliere il collegamento correlato.  
2. Nella pagina **Movimenti contabili cespiti** selezionare il movimento o i movimenti da annullare.  
3. Scegliere il menu **Azioni**, quindi scegliere l'azione **Annulla movimenti**.
4. Compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Scegliere **OK** per eseguire il processo batch.
6. Quando il movimento o i movimenti errati vengono annullati, continuare con la registrazione del costo di acquisto corretto.

## <a name="to-post-the-salvage-value-together-with-the-acquisition-cost"></a>Per registrare il valore di realizzo con il costo di acquisto

Il valore residuo di un cespite quando non può più essere utilizzato. È possibile registrare il valore di realizzo contemporaneamente alla registrazione del costo di acquisto. Per ulteriori informazioni, vai a [Ammortizzare o ammortizzare le immobilizzazioni](fa-how-depreciate-amortize.md).

È possibile registrare il valore di realizzo insieme al costo di acquisto da Registrazioni Cespiti.

> [!NOTE]
> Questo processo potrebbe richiedere la personalizzazione della pagina Registrazioni cespiti aggiungendo il campo Valore di realizzo. Il campo non viene visualizzato per impostazione predefinita nella pagina. Per saperne di più, vai a [Personalizza il tuo spazio di lavoro](ui-personalization-user.md).

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registrazioni cespiti**, quindi scegli il collegamento correlato.
2. Nella pagina **Registrazioni cespiti**, creare la linea di acquisizione. Per ulteriori informazioni, consultare [Per registrare manualmente un'acquisizione di cespiti con un giornale di registrazione CoGe cespiti](#to-post-a-fixed-asset-acquisition-manually-with-a-fixed-asset-gl-journal).
3. Nel campo **Valore di realizzo** nella riga di registrazione, immetti l'importo del valore di realizzo come avere (aggiungi il prefisso segno meno all'importo ad esempio **-** 100).
4. Scegli l'azione **Registra**.

> [!NOTE]
> Se esiste un valore di recupero per un cespite, tale valore viene utilizzato nella registrazione dell'ammortamento anziché il valore nel campo **Valore contabile finale** nel campo **Libri ammortamento FA** pagina. Per saperne di più, vai a [Per gestire il valore contabile finale](fa-how-depreciate-amortize.md#to-manage-the-ending-book-value).

## <a name="see-also"></a>Vedere anche

[Cespiti](fa-manage.md)  
[Impostazione di cespiti](fa-setup.md)  
[Dettagli di progettazione sull'impatto dell'IVA non deducibile sulle immobilizzazioni](design-details-nondeductible-vat.md)  
[Dati finanziari](finance.md)  
[Prepararsi a fare affari](ui-get-ready-business.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
