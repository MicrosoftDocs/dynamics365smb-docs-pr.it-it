---
title: Assicurazione di cespiti
description: Puoi assegnare uno o più cespiti a una polizza assicurativa registrando nel registro di copertura assicurativa dalla pagina **Registr. assicuraz.**.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'policy, coverage'
ms.search.form: '5647, 5644, 5653, 5651, 5655, 5652, 5645, 5656, 5646, 5648, 9275'
ms.date: 05/15/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="insure-fixed-assets"></a>Assicurazione di cespiti

Utilizza la pagina  **Carta di assicurazione**  per impostare una polizza assicurativa a copertura di uno o più cespiti. È possibile assegnare un cespite a una polizza assicurativa oppure più cespiti a una polizza assicurativa.

Assegnare un cespite a una polizza assicurativa registrando nel registro di copertura assicurativa dalla pagina **Registr. assicuraz.**.

Inoltre, è possibile assegnare un cespite ad una polizza assicurativa e creare i movimenti contabili della copertura quando si registra il costo di acquisto. Si registra un costo di acquisizione dal giornale di registrazione cespiti con il campo  **N. assicurazione**  compilato. È necessario attivare l'opzione **Registrazione assicurativa automatica** nella pagina **Impostazione cespite** . Per ulteriori informazioni, vedere [Acquisire un cespite utilizzando un giornale di registrazione CoGe cespiti](fa-how-acquire.md#acquire-a-fixed-asset-by-using-a-fixed-asset-gl-journal).

Se l'interruttore **Registrazione assicurativa automatica** nella pagina **Impostazione cespite** non è attivato, la registrazione delle acquisizioni dal il giornale di registrazione cespiti crea righe nella pagina  **Registro assicurativo** . È necessario pubblicare quelle righe manualmente.

> [!WARNING]  
> Se non attivi la  **Registrazione assicurativa automatica** la pagina **Impostazione cespite**, il tuo giornale di registrazione assicurativo dovrebbe essere basato su un modello di giornale senza serie numeriche. Questo si verifica perché i numeri di documento inseriti dalla riga di registrazione cespiti saranno in conflitto con la numerazione della registrazione assicurazioni. Per ulteriori informazioni sui batch e sulle definizioni registrazioni, vedere [Impostare i valori generali per i cespiti](fa-how-setup-general.md).

Dopo aver assegnato un cespite a una polizza assicurativa, il campo **Assicurato** sulla scheda cespite contiene **Sì**. Quando vendi il cespite, l'interruttore viene automaticamente disattivato.

## <a name="to-create-or-modify-an-insurance-card"></a>Per creare o modificare una scheda assicurazione

In caso di ricezione di informazioni relative a modifiche dell'importo di copertura, è necessario immettere le nuove informazioni nella pagina **Scheda assicurazione** per assicurarsi che la copertura della polizza venga analizzata correttamente.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Assicurazione**, quindi scegli il collegamento correlato.
2. Scegliere l'azione **Nuovo** per creare una nuova scheda per una polizza assicurativa. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. In alternativa, selezionare la polizza assicurativa che si desidera modificare, quindi scegliere l'azione **Modifica**.

## <a name="to-assign-a-fixed-asset-to-an-insurance-policy-by-posting-from-the-insurance-journal"></a>Per assegnare un cespite a una polizza assicurativa mediante la registrazione dalla registrazione assicurazioni

Assegnare un cespite a una polizza assicurativa mediante la registrazione al registro della copertura assicurativa.  

La seguente procedura illustra come creare manualmente una riga di registrazione assicurazioni. Se l'interruttore **Registrazione assicurativa automatica** è attivato nella pagina **Impostazione cespite**, le righe del giornale di registrazione assicurativo vengono create automaticamente quando si registrano i costi di acquisizione. In tal caso, è sufficiente registrare la registrazione.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Registrazioni assicurazioni**, quindi scegli il collegamento correlato.  
2. Aprire la registrazione pertinente e compilare le righe di registrazione necessarie.  
3. Per assegnare più cespiti a una sola polizza, creare righe di registrazione con lo stesso valore nel campo **Nr. assicurazione** e valori diversi nel campo **Nr. cespite**.  
4. Scegliere l'azione **Registra**.  

    > [!NOTE]  
    > I movimenti delle registrazioni delle assicurazioni vengono registrati soltanto nelle registrazioni della copertura assicurativa.  

## <a name="to-update-the-insurance-value-of-a-fixed-asset"></a>Per aggiornare il valore dell'assicurazione di un cespite

Il processo batch **Indice Cespiti** consente di aggiornare il valore dei cespiti coperti da assicurazione.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Indice assicurazioni**, quindi scegli il collegamento correlato.
2. Compilare i campi, se necessario.

    > [!NOTE]  
    >   Nel campo **Cifra indicizzazione** immettere una riduzione del 5%, ad esempio 95, nel campo laddove si immette un aumento del 2% come 102.  
3. Scegliere il pulsante **OK**.  

   Tramite il processo batch verrà calcolato il nuovo importo come percentuale del valore totale assicurato, come indicato nella pagina **Statistiche Assicurazioni** e verrà creata una riga nelle registrazioni delle assicurazioni.  
4. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registrazioni assicurazioni**, quindi scegli il collegamento correlato.  
5. Aprire la registrazione assicurazioni appropriata, esaminare i valori creati e registrarli nel registro di copertura assicurativa.  

## <a name="to-monitor-insurance-coverage"></a>Per controllare la copertura assicurativa

[!INCLUDE[prod_short](includes/prod_short.md)] fornisce le pagine dedicate per statistiche e report da utilizzare per analizzare le polizze assicurative e controllare se i cespiti sono sovra o sotto assicurati.  

### <a name="overview-of-insurance-policies"></a>Panoramica delle polizze assicurative

Per una sintesi delle polizze assicurative, visualizzare in anteprima o stampare il report **Assicurazione - Lista**. Nel report vengono visualizzate tutte le polizze e i campi più importanti delle schede assicurative.  

### <a name="insurance-coverage"></a>Copertura assicurativa

Per sapere quale polizza assicurativa copre ogni risorsa e per quale importo, è possibile visualizzare in anteprima o stampare il report **Assicurazione - Totale valori assicurati**.  

#### <a name="overunder-coverage"></a>Sovra/sottocopertura

È possibile verificare se i cespiti sono sovraassicurati o sottoassicurati nei seguenti modi:  

* La pagina **Statistiche assicurazioni**. Un importo positivo nel campo **Sopra/sotto assicurato** indica che il cespite è soprassicurato. Un importo negativo significa che il bene è sottoassicurato.  
* La pagina **Statistiche cespiti**. Scegliere il campo **Valore totale assicurato** per visualizzare la pagina **Mov.cont. copert. assicurativa**.  
* Il report **Sopra/sottocopertura**.  
* Il report **Analisi assicurazioni**.  

### <a name="uninsured-fixed-assets"></a>Immobilizzazioni non assicurate

Per verificare se ci si è dimenticati di assegnare un cespite a una polizza assicurativa, è possibile stampare o visualizzare in anteprima il report  **Assicurazione - FA non assicurati** . Questo report visualizza i cespiti per i quali gli importi non vengono registrati nel registro della copertura assicurativa.  

## <a name="to-view-insurance-coverage-ledger-entries"></a>Per visualizzare i movimenti contabili di copertura assicurativa

È possibile visualizzare le voci effettuate nel registro della copertura assicurativa.  

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Assicurazione**, quindi scegli il collegamento correlato.  
2. Selezionare la polizza assicurativa rilevante e scegliere l'azione **Mov.cont. copert. assicurativa**.  

## <a name="to-view-the-total-insurance-value-of-fixed-assets"></a>Per visualizzare il valore totale assicurato dei cespiti

Una pagina matrice mostra i valori assicurativi registrati per ciascuna polizza assicurativa per ciascun cespite risultante dagli importi relativi all'assicurazione registrati.  

1. Scegli l'icona ![lampadina che apre la funzionalità Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Assicurazione**, quindi scegli il collegamento correlato.  
2. Selezionare la polizza assicurativa rilevante e scegliere l'azione **Val. tot. assicurato per cespite**.  
3. Compilare i campi, se necessario.  
4. Scegliere l'azione **Mostra matrice**.  
5. Per visualizzare i movimenti contabili sottostanti della copertura assicurativa, selezionare un valore nella matrice.  

## <a name="to-correct-insurance-coverage-entries"></a>Per correggere i movimenti di copertura assicurativa

Se un cespite è stato attribuito alla polizza assicurativa sbagliata, è possibile correggerlo creando due movimenti di riclassificazione dal giornale di registrazione dell'assicurazione.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registrazioni assicurazioni**, quindi scegli il collegamento correlato.  
2. Creare una riga di registrazione per il cespite e la polizza assicurativa corretta in cui il valore del campo **Importo** è positivo.  
3. Creare un'altra riga di registrazione per il cespite e la polizza assicurativa non corretta in cui il valore del campo **Importo** è negativo.  
4. Scegli l'azione **Registra**.  

Il cespite viene rimosso dalla polizza assicurativa errata nella seconda riga. Il bene viene assegnato alla polizza assicurativa corretta nella prima riga del giornale.  

## <a name="see-also"></a>Vedere anche

[Cespiti](fa-manage.md)  
[Impostazione di cespiti](fa-setup.md)  
[Dati finanziari](finance.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
