---
author: brentholtorf
ms.topic: include
ms.date: 02/09/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
È possibile utilizzare i solleciti per indicare ai clienti gli importi insoluti. È anche possibile calcolare addebiti di interessi, ad esempio interessi o commissioni, e includerli nei solleciti.

Prima di creare i solleciti, è necessario impostarne i termini e assegnarli ai clienti. Per ulteriori informazioni, vedi [Impostare i termini e i livelli di sollecito](../finance-setup-reminders.md). [!INCLUDE [reminder-terms](reminder-terms.md)] Il contenuto della pagina **Condiz. interessi finanziari** determina se nel sollecito vengono calcolati anche gli interessi.  

È possibile eseguire periodicamente il processo batch **Crea solleciti** per creare solleciti per tutti i clienti con saldi scaduti oppure creare manualmente un sollecito per un cliente particolare e calcolare e compilare le righe automaticamente.  

Una volta creati i solleciti, è possibile modificarli. Il testo visualizzato all'inizio e alla fine di un sollecito è determinato dai termini del livello del sollecito e può essere visualizzato nella colonna **Descrizione**. Se un importo calcolato è stato inserito automaticamente nel testo iniziale o finale, questo non verrà rettificato se si eliminano righe Sarà quindi necessario utilizzare la funzione **Aggiorna testo soll.**.  

Per un movimento contabile cliente con selezionato il campo **In sospeso** non verrò richiesta la creazione di un sollecito. Se tuttavia viene creato un sollecito in base a un altro movimento, nel sollecito verrà incluso anche un movimento scaduto contrassegnato come in sospeso. Per le righe di questi movimenti non verranno calcolati interessi.

Dopo avere creato i solleciti e apportato le modifiche necessarie, è possibile stampare report di test o emettere i solleciti, in genere tramite posta elettronica.

### Per creare un sollecito automaticamente

Un sollecito è simile a una fattura. Quando viene creato un sollecito, è necessario compilare una testata e una o più righe. È possibile utilizzare una funzione che consente di creare i solleciti automaticamente per tutti i clienti.

1. Scegli la ![lampadina che apre la funzione Dimmi 0](../media/ui-search/search_small.png "Dimmi cosa vuoi fare"). immetti **Solleciti**, quindi scegli il collegamento correlato.
2. Nella pagina **Sollecito**, selezionare l'azione **Crea sollecito**.
3. Nella pagina **Crea solleciti** compilare i campi per definire come e per chi vengono creati i solleciti.
4. Scegliere il pulsante **OK**.

### Per creare un sollecito manualmente

Nella pagina **Sollecito** è possibile compilare manualmente la Scheda dettaglio **Generale** e quindi compilare automaticamente le righe.

1. Scegli la ![lampadina che apre nuovamente la funzione Dimmi 2.](../media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Solleciti**, quindi scegli il collegamento correlato.
2. Scegliere l'azione **Nuovo**.
3. Compilare i campi appropriati nella Scheda dettaglio **Generale**.
4. Scegliere l'azione selezionare **Suggerisci riga sollecito**.
5. Nella finestra **Crea solleciti** compilare i campi per definire come e per chi vengono creati i solleciti.
6. Se si desidera che i solleciti contengano i movimenti aperti con importi insoluti che sono in sospeso, selezionare la casella di controllo **Includi movimenti in sospeso**.
7. Se si desidera che i solleciti contengano solo i movimenti aperti con importi insoluti, selezionare la casella di controllo **Solo movimenti con importi insoluti**. Verranno visualizzate solo fatture e pagamenti in quanto si tratta dei movimenti per i quali i pagamenti dei clienti potrebbero essere scaduti.

    > [!Important]
    > I movimenti aperti che sono in sospeso verranno inseriti, indipendentemente dall'impostazione nella casella di controllo **Solo movimenti con importi insoluti**.

8. Scegliere il pulsante **OK**.

### Per sostituire i testi di un sollecito

Esistono diverse modalità per determinare il testo che verrà visualizzato nella stampa del sollecito. In alcuni casi può essere necessario sostituire i testi iniziali e finali definiti per il livello attuale con i testi di un livello diverso.

1. Scegli la ![lampadina che apre nuovamente la funzione Dimmi 3.](../media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Solleciti**, quindi scegli il collegamento correlato.
2. Aprire il sollecito pertinente quindi scegliere l'azione **Aggiorna testo sollecito**.
3. Nella pagina **Aggiorna testo sollecito**, immettere il livello richiesto nel campo **Livello di sollecito**.
4. Scegliere **OK** per aggiornare il testo iniziale e finale.

### Per emettere un sollecito

Dopo avere creato i solleciti e apportato le modifiche necessarie, è possibile stampare report di test o emettere i solleciti.

Quando si emette un sollecito, i dati vengono trasferiti in una pagina distinta relativa ai solleciti emessi e vengono contemporaneamente registrati i movimenti del sollecito. Se sono stati calcolati interessi o oneri addizionali, i movimenti vengono registrati nella contabilità clienti e nella contabilità generale.

Quando viene generato un sollecito, vengono registrati i movimenti secondo le scelte immesse nella pagina **Termini di sollecito**. Questa specifica determina se interessi e/o oneri addizionali vengono registrati nel conto del cliente e nella contabilità generale. Il setup nella pagina **Cat. reg. cliente** stabilisce in quali conti vengono registrati.

Per ogni movimento contabile cliente sulla nota addebito interessi, viene creato un movimento nella pagina **Mov. soll./Note add. int.**.

Se sono selezionate le caselle di controllo **Registra interesse** o **Registra onere addizionale** nella pagina **Termini di Sollecito**, vengono creati anche i seguenti movimenti:

- un movimento nella pagina **Movimenti contabili clienti**
- un movimento incassi nel relativo Conto C/G
- un movimento interessi e/o un movimento onere addizionale nel relativo Conto C/G

L'emissione di un sollecito può inoltre risultare nei movimenti IVA.

1. Scegli la ![lampadina che apre nuovamente la funzione Dimmi 4](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"). immetti **Solleciti**, quindi scegli il collegamento correlato.
2. Selezionare il sollecito di interesse e quindi scegliere l'azione **Emetti**.
3. Nella pagina **Emetti sollecito** compilare i campi secondo le necessità.
4. Scegliere il pulsante **OK**.

Il sollecito viene stampato per l'invio a un indirizzo e-mail specificato come allegato PDF.

### Per annullare un sollecito emesso

Se i solleciti sono stati emessi per errore, è possibile annullarli uno a uno o come batch prima che vengano inviati.

1. Nella pagina **Solleciti emessi**, selezionare una o più righe per i solleciti emessi che si desidera annullare, quindi selezionare l'azione **Annulla**.
2. Nella pagina **Annulla solleciti emessi** compilare i campi in base alle esigenze, quindi scegliere il pulsante **OK**.


