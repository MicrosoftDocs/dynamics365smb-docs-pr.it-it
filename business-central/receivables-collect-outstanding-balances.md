---
title: Riscuotere i saldi inevasi
description: Informazioni su come inviare un sollecito a un cliente per un pagamento scaduto e come aggiungere addebiti, od oneri aggiuntivi, al pagamento per il ritardo.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment due, debt, overdue, fee, charge, reminder
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 2c3e4bc2b75133b0a46d3d5746841d6caf76589c
ms.sourcegitcommit: 2ab6709741be16ca8029e2afadf19d28cf00fbc7
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/14/2022
ms.locfileid: "7971654"
---
# <a name="collect-outstanding-balances"></a>Riscuotere i saldi inevasi

La gestione dei crediti comprende il controllo del pagamento degli importi dovuti entro i termini di scadenza. Per i clienti con pagamenti scaduti, è possibile inviare innanzitutto il report **Rendiconto cliente** come promemoria. In alternativa, è possibile emettere dei solleciti.

È possibile utilizzare i solleciti per indicare ai clienti gli importi insoluti. È anche possibile calcolare addebiti di interessi, ad esempio interessi o commissioni, e includerli nei solleciti. Utilizzare note di addebito interessi se si desidera addebitare ai clienti interessi o commissioni senza inviare solleciti relativi agli importi insoluti.

## <a name="statements"></a>Estratti conto

Dalla scheda cliente, è possibile creare un estratto conto con le transazioni del cliente con l'utente. Quindi, si invia al cliente il file PDF generato. In alternativa, usare il report **Rendiconto cliente** per inviare ai clienti una panoramica della loro attività con l'utente. Il rendiconto del cliente può essere inviato a Excel per un'ulteriore elaborazione.  

### <a name="to-send-the-customer-statement-report"></a>Per inviare il report estratto conto cliente

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Rendiconto cliente**, quindi scegli il collegamento correlato.
2. Compilare i campi, se necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. In **Opzioni output** selezionare una modalità di invio del report al cliente.

> [!NOTE]
> Se si utilizzano più valute, il report Rendiconto cliente viene sempre stampato nella valuta del cliente. L'ultima data in un periodo di rendiconto viene inoltre utilizzata come data di rendiconto e data di aging, se è incluso l'aging.

## <a name="reminders"></a>Solleciti

Prima di creare i solleciti, è necessario impostarne i termini e assegnarli ai clienti. Per ulteriori informazioni, vedere [Impostare i termini e i livelli di sollecito](finance-setup-reminders.md). [!INCLUDE [reminder-terms](includes/reminder-terms.md)] Il contenuto della pagina **Condiz. interessi finanziari** determina se nel sollecito vengono calcolati anche gli interessi.  

È possibile eseguire periodicamente il processo batch **Crea solleciti** per creare solleciti per tutti i clienti con saldi scaduti oppure creare manualmente un sollecito per un cliente particolare e calcolare e compilare le righe automaticamente.  

Una volta creati i solleciti, è possibile modificarli. Il testo visualizzato all'inizio e alla fine di un sollecito è determinato dai termini del livello del sollecito e può essere visualizzato nella colonna **Descrizione**. Se un importo calcolato è stato inserito automaticamente nel testo iniziale o finale, questo non verrà rettificato se si eliminano righe Sarà quindi necessario utilizzare la funzione **Aggiorna testo soll.**.  

Per un movimento contabile cliente con selezionato il campo **In sospeso** non verrò richiesta la creazione di un sollecito. Se tuttavia viene creato un sollecito in base a un altro movimento, nel sollecito verrà incluso anche un movimento scaduto contrassegnato come in sospeso. Per le righe di questi movimenti non verranno calcolati interessi.

Dopo avere creato i solleciti e apportato le modifiche necessarie, è possibile stampare report di test o emettere i solleciti, in genere tramite posta elettronica.

### <a name="to-create-a-reminder-automatically"></a>Per creare un sollecito automaticamente

Un sollecito è simile a una fattura. Quando viene creato un sollecito, è necessario compilare una testata e una o più righe. È possibile utilizzare una funzione che consente di creare i solleciti automaticamente per tutti i clienti.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Solleciti**, quindi scegli il collegamento correlato.
2. Nella pagina **Sollecito**, selezionare l'azione **Crea sollecito**.
3. Nella pagina **Crea solleciti** compilare i campi per definire come e per chi vengono creati i solleciti.
4. Scegliere il pulsante **OK**.

### <a name="to-create-a-reminder-manually"></a>Per creare un sollecito manualmente

Nella pagina **Sollecito** è possibile compilare manualmente la Scheda dettaglio **Generale** e quindi compilare automaticamente le righe.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Solleciti**, quindi scegli il collegamento correlato.
2. Scegliere l'azione **Nuovo**.
3. Compilare i campi appropriati nella Scheda dettaglio **Generale**.
4. Scegliere l'azione selezionare **Suggerisci riga sollecito**.
5. Nella finestra **Crea solleciti** compilare i campi per definire come e per chi vengono creati i solleciti.
6. Se si desidera che i solleciti contengano i movimenti aperti con importi insoluti che sono in sospeso, selezionare la casella di controllo **Includi movimenti in sospeso**.
7. Se si desidera che i solleciti contengano solo i movimenti aperti con importi insoluti, selezionare la casella di controllo **Solo movimenti con importi insoluti**. Verranno visualizzate solo fatture e pagamenti in quanto si tratta dei movimenti per i quali i pagamenti dei clienti potrebbero essere scaduti.

    > [!Important]
    > I movimenti aperti che sono in sospeso verranno inseriti, indipendentemente dall'impostazione nella casella di controllo **Solo movimenti con importi insoluti**.

8. Scegliere il pulsante **OK**.

### <a name="to-replace-reminder-texts"></a>Per sostituire i testi di un sollecito

Esistono diverse modalità per determinare il testo che verrà visualizzato nella stampa del sollecito. In alcuni casi può essere necessario sostituire i testi iniziali e finali definiti per il livello attuale con i testi di un livello diverso.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Solleciti**, quindi scegli il collegamento correlato.
2. Aprire il sollecito pertinente quindi scegliere l'azione **Aggiorna testo sollecito**.
3. Nella pagina **Aggiorna testo sollecito**, immettere il livello richiesto nel campo **Livello di sollecito**.
4. Scegliere **OK** per aggiornare il testo iniziale e finale.

### <a name="to-issue-a-reminder"></a>Per emettere un sollecito

Dopo avere creato i solleciti e apportato le modifiche necessarie, è possibile stampare report di test o emettere i solleciti.

Quando si emette un sollecito, i dati vengono trasferiti in una pagina distinta relativa ai solleciti emessi e vengono contemporaneamente registrati i movimenti del sollecito. Se sono stati calcolati interessi o oneri addizionali, i movimenti vengono registrati nella contabilità clienti e nella contabilità generale.

Quando viene generato un sollecito, vengono registrati i movimenti secondo le scelte immesse nella pagina **Termini di sollecito**. Questa specifica determina se interessi e/o oneri addizionali vengono registrati nel conto del cliente e nella contabilità generale. Il setup nella pagina **Cat. reg. cliente** stabilisce in quali conti vengono registrati.

Per ogni movimento contabile cliente sulla nota addebito interessi, viene creato un movimento nella pagina **Mov. soll./Note add. int.**.

Se sono selezionate le caselle di controllo **Registra interesse** o **Registra onere addizionale** nella pagina **Termini di Sollecito**, vengono creati anche i seguenti movimenti:

- un movimento nella pagina **Movimenti contabili clienti**
- un movimento incassi nel relativo Conto C/G
- un movimento interessi e/o un movimento onere addizionale nel relativo Conto C/G

L'emissione di un sollecito può inoltre risultare nei movimenti IVA.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Solleciti**, quindi scegli il collegamento correlato.
2. Selezionare il sollecito di interesse e quindi scegliere l'azione **Emetti**.
3. Nella pagina **Emetti sollecito** compilare i campi secondo le necessità.
4. Scegliere il pulsante **OK**.

Il sollecito viene stampato per l'invio a un indirizzo e-mail specificato come allegato PDF.

### <a name="to-cancel-an-issued-reminder"></a>Per annullare un sollecito emesso

Se i solleciti sono stati emessi per errore, è possibile annullarli uno a uno o come batch prima che vengano inviati.

1. Nella pagina **Solleciti emessi**, selezionare una o più righe per i solleciti emessi che si desidera annullare, quindi selezionare l'azione **Annulla**.
2. Nella pagina **Annulla solleciti emessi** compilare i campi in base alle esigenze, quindi scegliere il pulsante **OK**.

## <a name="finance-charges"></a>Spese finanziarie

Quando un cliente non effettua il pagamento entro la data di scadenza, è possibile fare in modo che gli addebiti per interessi vengano calcolati automaticamente e aggiunti agli importi insoluti nel conto del cliente. È possibile informare i clienti degli interessi aggiunti mediante l'invio di note di addebito interessi.  

> [!NOTE]  
> Le note di addebito interessi vengono utilizzate per calcolare interessi e addebiti interessi e informare i clienti su tali interessi e addebiti interessi senza inviare solleciti relativi ai pagamenti scaduti. In alternativa è possibile calcolare gli interessi sui pagamenti scaduti, è possibile effettuare questa operazione quando si creano i solleciti.  

Prima di poter creare nota addebito interessi, è necessario impostare i termini. Per ulteriori informazioni, vedere [Impostare condizioni interessi finanziari](finance-setup-finance-charges.md).  

È possibile creare manualmente una nota di addebito interessi per un singolo cliente e compilare le righe automaticamente. In alternativa è possibile utilizzare il processo della funzione **Crea note add. interessi** per creare tali documenti per tutti i clienti selezionati con saldi scaduti.  

Una volta create, le note di addebito interessi possono essere modificate. Il testo visualizzato all'inizio e alla fine della nota è determinato dalle condizioni relative agli interessi finanziari e può essere visualizzato nella colonna **Descrizione** delle righe. Se un importo calcolato è stato inserito automaticamente nel testo iniziale o finale, questo non verrà rettificato se si eliminano righe e sarà necessario utilizzare la funzione **Aggiorna testi add. int.**.  

Dopo avere creato le note di addebito interessi e apportato le modifiche necessarie, è possibile stampare report di test o emettere le note di addebito interessi, in genere tramite posta elettronica.

### <a name="to-create-a-finance-charge-memo-manually"></a>Per creare una nota di addebito di interessi manualmente

Una nota di addebito di interessi è simile a una fattura. È possibile compilare una testata manualmente e le righe automaticamente, oppure le note di addebito di interessi possono venire create automaticamente per tutti i clienti.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Note addebito interessi**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Nuovo** e compilare i campi necessari.  
3. Scegliere l'azione **Sugg. righe note add. int.**
4. Se si desidera creare note di addebito interessi solo per movimenti specifici, impostare un filtro nella Scheda dettaglio **Mov. contabili clienti** della pagina **Sugg. righe note add. int.**.

    > [!NOTE]
    > Sebbene siano elencati, selezionando **Pagamento** e **Nota di credito** come **tipo di documento** i filtri non avranno alcun effetto perché la funzione **Sugg. righe note add. int.** gestisce solo importi positivi.
5.  Scegliere **OK** per avviare il processo batch.  

### <a name="to-update-finance-charge-memo-texts"></a>Per aggiornare i testi delle note di addebito di interessi  
Talvolta può essere necessario modificare il testo iniziale e finale impostato per le condizioni degli interessi finanziari. Se la modifica viene effettuata dopo la creazione ma prima dell'emissione di note di addebito di interessi, è possibile aggiornare le note con il testo modificato.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Nota addebito interessi**, quindi scegli il collegamento correlato.  
2. Aprire la nota di addebito degli interessi per cui si desidera modificare il testo di quindi scegliere l'azione **Aggiorna testi add. int.**.
3. Nella pagina **Aggiorna testi add. int.** è possibile impostare un filtro per aggiornare più note.
4. Scegliere **OK** per aggiornare il testo iniziale e finale.  

### <a name="to-issue-finance-charge-memos"></a>Per emettere note di addebito interessi
Dopo avere creato le note di addebito interessi e apportato le modifiche necessarie, è possibile stampare report di test o emettere le note di addebito interessi.

Quando viene generato un sollecito, vengono registrati i movimenti secondo le scelte immesse nella pagina **Condiz. interessi finanziari**. Questa specifica determina se interessi e/o oneri addizionali vengono registrati nel conto del cliente e nella contabilità generale. Il setup nella pagina **Cat. reg. cliente** stabilisce in quali conti vengono registrati.

Per ogni movimento contabile cliente sulla nota addebito interessi, viene creato un movimento nella pagina **Mov. soll./Note add. int.**.

Se sono selezionate le caselle di controllo **Registra interesse** o **Registra onere addizionale** nella pagina **Condiz. interessi finanziari**, vengono creati anche i seguenti movimenti:

- un movimento nella pagina **Mov. contabili clienti**
- un movimento incassi nel relativo Conto C/G
- un movimento interessi e/o un movimento onere addizionale nel relativo Conto C/G

L'emissione di una nota di addebito di interessi può inoltre risultare nei movimenti IVA.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Note addebito interessi**, quindi scegli il collegamento correlato.
2. Selezionare la nota pertinente e quindi scegliere l'azione **Emetti**.
3. Nella pagina **Emetti note add. interessi** compilare i campi secondo le necessità.
4. Scegliere il pulsante **OK**.

La nota di addebito di interessi viene stampata per l'invio a un indirizzo e-mail specificato come allegato PDF.

### <a name="to-cancel-an-issued-finance-charge-memo"></a>Per annullare una nota di addebito degli interessi emessa
Se le note di addebito degli interessi sono state emesse per errore, è possibile annullarle uno a uno o come batch prima che vengano inviate.
1. Nella pagina **Note addebito interessi emesse**, selezionare una o più righe per le note di addebito degli interessi che si desidera annullare, quindi scegliere l'azione **Annulla**.
2. Nella pagina **Annulla note addebito interessi emesse** compilare i campi in base alle esigenze, quindi scegliere il pulsante **OK**.

### <a name="to-view-reminder-and-finance-charge-entries"></a>Per visualizzare i movimenti di sollecito e di addebito di interessi  
All'emissione di un sollecito, nella pagina **Mov. soll./Note add. int.** viene creato un movimento di sollecito per ciascuna riga di sollecito che contiene un movimento contabile clienti. È possibile quindi ottenere una panoramica dei movimenti di sollecito creati per un cliente specifico.    
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Clienti**, quindi scegli il collegamento correlato.  
2. Aprire la scheda cliente interessata e scegliere l'azione **Movimenti contabili**.
3. Nella pagina **Movimenti contabili clienti** selezionare la riga con il movimento contabile per il quale si desidera visualizzare i movimenti di sollecito, quindi scegliere l'azione **Mov. soll./Note add. int.**.

## <a name="multiple-interest-rates"></a>Tassi d'interesse multipli

[!INCLUDE [multiple-interest-rates-def](includes/multiple-interest-rates-def.md)] Per ulteriori informazioni, vedere [Impostare più tassi di interesse](finance-how-to-set-up-multiple-interest-rates.md).  

## <a name="see-related-training-at-microsoft-learn"></a>Vedere le informazioni relative al training in [Microsoft Learn](/learn/paths/process-financial-periodic-activities-dynamics-365-business-central/)

## <a name="see-also"></a>Vedere anche

[Impostare i termini e i livelli di sollecito](finance-setup-reminders.md)  
[Impostare condizioni interessi finanziari](finance-setup-finance-charges.md)  
[Gestione della contabilità clienti](receivables-manage-receivables.md)  
[Vendite](sales-manage-sales.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]