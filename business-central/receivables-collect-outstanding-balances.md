---
title: Riscuotere i saldi inevasi
description: 'Scopri come ricordare ai tuoi clienti i pagamenti inevasi. Invia un rendiconto cliente, emetti un promemoria o invia una nota di addebito finanziario.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: 'payment due, debt, overdue, fee, charge, reminder'
ms.search.form: '6, 25, 440, 443, 448, 452'
ms.date: 07/01/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="collect-outstanding-balances"></a>Riscuotere i saldi inevasi

La gestione dei crediti comprende il controllo del pagamento degli importi dovuti entro i termini di scadenza. Per i clienti con pagamenti scaduti, è possibile inviare innanzitutto il report **Rendiconto cliente** come promemoria. In alternativa, è possibile emettere dei solleciti.

Utilizzare i solleciti per indicare ai clienti gli importi scaduti. È anche possibile calcolare addebiti di interessi, ad esempio interessi o commissioni, e includerli nei solleciti. Utilizzare note di addebito interessi se si desidera addebitare ai clienti interessi o commissioni senza inviare solleciti relativi agli importi insoluti.

## <a name="statements"></a>Estratti conto

Dalla scheda cliente, puoi creare un estratto conto per le transazioni del cliente con l'utente. Quindi, puoi generare un file PDF e inviarlo al cliente. In alternativa, usare il report **Rendiconto cliente** per inviare ai clienti una panoramica della loro attività con l'utente. 

> [!TIP]
> Se necessario, puoi inviare l'estratto conto a Excel per apportare modifiche.  

### <a name="to-send-the-customer-statement-report"></a>Per inviare il report estratto conto cliente

1. Scegli la ![lampadina che apre la funzione Dimmi 10](media/ui-search/search_small.png "Dimmi cosa vuoi fare"). immetti **Rendiconto cliente**, quindi scegli il collegamento correlato.
2. Compilare i campi, se necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. In **Opzioni output** selezionare una modalità di invio del report al cliente.

> [!NOTE]
> Se si utilizzano più valute, il report Rendiconto cliente viene sempre stampato nella valuta del cliente. L'ultima data in un periodo di rendiconto viene inoltre utilizzata come data di rendiconto e data di aging, se è incluso l'aging.

## <a name="reminders"></a>Solleciti

[!INCLUDE [receivables-reminders](includes/receivables-reminders.md)]

## <a name="finance-charges"></a>Addebito interessi

Se un cliente non paga entro la data di scadenza, è possibile calcolare automaticamente gli oneri finanziari e aggiungerli agli importi scaduti sul conto del cliente. È possibile informare i clienti degli interessi aggiunti mediante l'invio di note di addebito interessi.  

> [!NOTE]  
> Le note di addebito interessi vengono utilizzate per calcolare interessi e addebiti interessi e informare i clienti su tali interessi e addebiti interessi senza inviare solleciti relativi ai pagamenti scaduti. In alternativa è possibile calcolare gli interessi sui pagamenti scaduti, è possibile effettuare questa operazione quando si creano i solleciti.  

Prima di poter creare nota addebito interessi, è necessario impostare i termini. Per ulteriori informazioni, vedere [Impostare condizioni interessi finanziari](finance-setup-finance-charges.md).  

È possibile creare manualmente una nota di addebito interessi per un singolo cliente e compilare le righe automaticamente. In alternativa è possibile utilizzare il processo della funzione **Crea note add. interessi** per creare tali documenti per tutti i clienti selezionati con saldi scaduti.  

Una volta create, le note di addebito interessi possono essere modificate. Il testo visualizzato all'inizio e alla fine della nota è determinato dalle condizioni relative agli interessi finanziari e può essere visualizzato nella colonna **Descrizione** delle righe. Se un importo calcolato è stato inserito automaticamente nel testo iniziale o finale, il testo non verrà modificato se si eliminano delle righe. e sarà necessario utilizzare la funzione **Aggiorna testi add. int.**.  

Dopo avere creato le note di addebito interessi e apportato le modifiche necessarie, è possibile stampare report di test o emettere le note di addebito interessi, in genere tramite posta elettronica.

### <a name="to-create-a-finance-charge-memo-manually"></a>Per creare una nota di addebito di interessi manualmente

Una nota di addebito di interessi è simile a una fattura. È possibile compilare una testata manualmente e le righe automaticamente, oppure le note di addebito di interessi possono venire create automaticamente per tutti i clienti.

1. Scegli la ![lampadina che apre la funzione Dimmi 2](media/ui-search/search_small.png "Dimmi cosa vuoi fare"). immetti **Note addebito interessi**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Nuovo** e compilare i campi necessari.  
3. Scegliere l'azione **Sugg. righe note add. int.**
4. Se si desidera creare note di addebito interessi solo per movimenti specifici, impostare un filtro nella Scheda dettaglio **Mov. contabili clienti** della pagina **Sugg. righe note add. int.**.

    > [!NOTE]
    > Sebbene siano elencati, selezionando **Pagamento** e **Nota di credito** come **tipo di documento** i filtri non avranno alcun effetto perché la funzione **Sugg. righe note add. int.** gestisce solo importi positivi.
5. Scegliere **OK** per avviare il processo batch.  

### <a name="to-update-finance-charge-memo-texts"></a>Per aggiornare i testi delle note di addebito di interessi

In alcuni casi, potrebbe essere necessario modificare il testo iniziale e finale impostato per i termini di addebito finanziario. Se la modifica viene effettuata dopo la creazione ma prima dell'emissione di note di addebito di interessi, è possibile aggiornare le note con il testo modificato.

1. Scegli la ![lampadina che apre la funzione Dimmi 3](media/ui-search/search_small.png "Dimmi cosa vuoi fare"). immetti **Nota addebito interessi**, quindi scegli il collegamento correlato.  
2. Aprire la nota di addebito degli interessi per cui si desidera modificare il testo di quindi scegliere l'azione **Aggiorna testi add. int.**.
3. Nella pagina **Aggiorna testi add. int.** è possibile impostare un filtro per aggiornare più note.
4. Scegliere **OK** per aggiornare il testo iniziale e finale.  

### <a name="to-issue-finance-charge-memos"></a>Per emettere note di addebito interessi

Dopo avere creato le note di addebito interessi e apportato le modifiche necessarie, puoi stampare report di test o emettere le note di addebito interessi.

Quando generi un sollecito, i movimenti vengono registrati secondo le specifiche nella pagina **Condiz. interessi finanziari**. Questa specifica determina se interessi e/o oneri addizionali vengono registrati nel conto del cliente e nella contabilità generale. Le impostazioni nella pagina **Categoria registrazione clienti** determinano i conti su cui vengono contabilizzati gli interessi o le commissioni.

Per ogni movimento contabile cliente sulla nota addebito interessi, viene creato un movimento nella pagina **Mov. soll./Note add. int.**.

Se sono selezionate le caselle di controllo **Registra interesse** o **Registra onere addizionale** nella pagina **Condizioni interessi finanziari**, vengono creati anche i seguenti movimenti:

- un movimento nella pagina **Mov. contabili clienti**
- un movimento incassi nel relativo Conto C/G
- un movimento interessi e/o un movimento onere addizionale nel relativo Conto C/G

Inoltre, l'emissione di una nota di addebito interessi potrebbe risultare nei movimenti IVA.

1. Scegli la ![lampadina che apre la funzione Dimmi 4.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Note addebito interessi**, quindi scegli il collegamento correlato.
2. Selezionare la nota pertinente e quindi scegliere l'azione **Emetti**.
3. Nella pagina **Emetti note add. interessi** compilare i campi secondo le necessità.
4. Scegliere il pulsante **OK**.

La nota di addebito finanziario viene stampata o inviata all'indirizzo e-mail specificato come allegato PDF.

### <a name="to-cancel-an-issued-finance-charge-memo"></a>Per annullare una nota di addebito degli interessi emessa

Se le note di addebito finanziario sono state emesse per errore, puoi Annulla prima che vengano rispedite. Puoi farlo una alla volta o in batch.

1. Nella pagina **Note addebito interessi emesse**, selezionare una o più righe per le note di addebito degli interessi che si desidera annullare, quindi scegliere l'azione **Annulla**.
2. Nella pagina **Annulla note addebito interessi emesse** compilare i campi in base alle esigenze, quindi scegliere il pulsante **OK**.

### <a name="to-view-reminder-and-finance-charge-entries"></a>Per visualizzare i movimenti di sollecito e di addebito di interessi

All'emissione di un sollecito, nella pagina **Mov. soll./Note add. int.** viene creato un movimento di sollecito per ciascuna riga di sollecito che contiene un movimento contabile clienti. È possibile quindi ottenere una panoramica dei movimenti di sollecito creati per un cliente specifico.

1. Scegli la ![lampadina che apre la funzione Dimmi 5.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") , immetti **Clienti**, quindi scegli il collegamento correlato.  
2. Aprire la scheda cliente interessata e scegliere l'azione **Movimenti contabili**.
3. Nella pagina **Movimenti contabili clienti** selezionare la riga con il movimento contabile per il quale si desidera visualizzare i movimenti di sollecito, quindi scegliere l'azione **Mov. soll./Note add. int.**.

## <a name="multiple-interest-rates"></a>Tassi d'interesse multipli

[!INCLUDE [multiple-interest-rates-def](includes/multiple-interest-rates-def.md)] Per ulteriori informazioni, vedere [Impostare più tassi di interesse](finance-how-to-set-up-multiple-interest-rates.md).  

## <a name="see-also"></a>Vedere anche

[Impostare i termini e i livelli di sollecito](finance-setup-reminders.md)  
[Impostare condizioni interessi finanziari](finance-setup-finance-charges.md)  
[Gestione della contabilità clienti](receivables-manage-receivables.md)  
[Vendite](sales-manage-sales.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
