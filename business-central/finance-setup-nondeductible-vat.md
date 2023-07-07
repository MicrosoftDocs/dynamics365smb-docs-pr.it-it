---
title: Impostare l'IVA non detraibile
description: Questo articolo spiega come configurare l'IVA non detraibile in Microsoft Dynamics 365 Business Central.
author: altotovi
ms.author: altotovi
ms.reviewer: null
ms.service: dynamics365-business-central
ms.topic: how-to
ms.search.keywords: 'VAT, non-deductible, setup'
ms.search.form: '187, 472, 473'
ms.date: 04/26/2023
ms.custom: bap-template
---

# <a name="set-up-non-deductible-vat"></a>Impostare l'IVA non detraibile

L'imposta sul valore aggiunto (IVA) non detraibile è l'IVA che è dovuta da un acquirente, ma che non è detraibile dal proprio debito IVA dell'acquirente. Le aziende possono solitamente recuperare l'IVA sull'acquisto di beni e servizi correlati alle loro attività commerciali. Tuttavia, in alcune situazioni, un'azienda è soggetta all'IVA che non è detraibile. Queste situazioni sono in genere correlate alle normative locali e possono variare da paese a paese. Tuttavia, il modello di utilizzo dell'IVA non detraibile o parzialmente detraibile è simile. Puoi utilizzare l'IVA proporzionale per calcolare l'IVA quando c'è IVA detraibile e non detraibile.

In generale, l'IVA non può essere detratta per alcuni acquisti a causa dei seguenti fattori:

- **Tipologia di beni e servizi acquistati**: l'IVA non è detraibile completamente o parzialmente per legge su beni quali automobili, telefoni cellulari, alimentari acquistati presso ristoranti.
- **IVA proporzionale parzialmente detraibile**: l'IVA viene ripartita proporzionalmente tra le operazioni di vendita soggette a IVA e tutte le operazioni eseguite. L'IVA eccedente questo rapporto non può essere detratta.

Poiché può essere difficile sapere dove e come viene utilizzato un articolo, è necessario contattare le autorità fiscali locali del proprio paese per determinare se una determinata percentuale dell'IVA è detraibile in base ai dati storici. 

> [!IMPORTANT]
> Questa funzione globale è disponibile in tutti i paesi con IVA abilitata **ad eccezione di Belgio, Italia, Norvegia e Spagna**. Queste localizzazioni dispongono già di funzionalità locali esistenti e verranno aggiornate in futuro. Non eseguire questa funzione in questi paesi perché la procedura di aggiornamento non esiste.

## <a name="use-non-deductible-vat"></a>Usare IVA non detraibile

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi 3.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup e-mail VAT**, quindi seleziona il collegamento correlato.
2. Seleziona la casella di controllo **Abilita IVA non detraibile**.

    > [!IMPORTANT]
    > Dopo aver abilitato l'IVA non detraibile, non è possibile disattivarla perché la funzione potrebbe includere modifiche ai dati e potrebbe avviare un aggiornamento di alcune tabelle del database. Microsoft consiglia vivamente di abilitare e testare questa funzionalità nell'ambiente sandbox prima di abilitarla nell'ambiente di produzione.

3. Configurare il modo in cui il sistema tratterà i valori IVA non detraibile.

    1. Nel campo **Utilizza per costo articolo**, specifica se l'IVA non detraibile deve essere aggiunta al costo dell'articolo quando si acquistano gli articoli. In caso contrario, l'IVA non detraibile non influirà sul costo dell'articolo e l'intero importo verrà registrato solo a livello di contabilità generale.
    2. Seleziona la casella di controllo **Utilizza per costo cespite** per aggiungere l'IVA non detraibile al costo del cespite quando si acquistano nuovi cespiti. In caso contrario, l'IVA non detraibile non influirà sul costo del cespite e l'intero importo verrà registrato solo a livello di contabilità generale.
    3. Seleziona la casella di controllo **Utilizza per costo commessa** per specificare che l'IVA non detraibile deve essere aggiunta al costo del lavoro quando si acquistano articoli per il lavoro. In caso contrario, l'IVA non detraibile non influirà sul costo della commessa e l'intero importo verrà registrato solo a livello di contabilità generale.
    4. Seleziona la casella di controllo **Mostra IVA non detraibile nelle righe** per specificare che l'IVA non detraibile deve essere visualizzata nelle pagine delle righe del documento per facilitare la manipolazione degli importi IVA.

## <a name="use-the-non-deductible-vat-percentage"></a>Utilizza la percentuale IVA non detraibile

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi 3.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup registrazioni IVA**, quindi seleziona il collegamento correlato.
2. Compilare i campi nella pagina **Setup registrazioni IVA** come descritto nella tabella riportata di seguito.

    | Campo | Descrizione |
    |-------|-------------|
    | Consenti IVA non detraibile | Specifica se viene considerata l'IVA non detraibile per la combinazione corrente di categoria di registrazione business IVA e categoria di registrazione articoli/servizi IVA. |
    | % IVA non detraibile | Specifica la percentuale dell'importo della transazione a cui non viene applicata l'IVA. |
    | Conto IVA acquisti non detraibile | Specifica il conto associato all'importo dell'IVA non dedotta secondo il tipo di beni o servizi acquistati. |

    > [!NOTE]
    > Per avere movimenti di contabilità generale (G/L) che utilizzano il conto dedicato anziché il conto vendite/acquisti, è possibile lasciare il campo vuoto **Conto IVA acquisti non detraibile** o impostare il campo **Conti C/G**.

3. Seleziona **OK**.

> [!NOTE]
> Non è possibile utilizzare l'IVA non realizzata insieme all'IVA non detraibile.
>
> Non usare lo stesso valore per **Codice IVA** sia per IVA normale dove il campo **% IVA indetraibile** è impostato su **0** (zero) e IVA normale dove il campo **% IVA non detraibile** è impostato su un valore diverso da zero. In caso contrario, l'importo totale dell'IVA non detraibile sarà calcolato in modo errato.

## <a name="see-also"></a>Vedere anche

[Gestione contabile](finance.md)  
[Setup dei calcoli e registrazione dei metodi per l'IVA](finance-setup-vat.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
