---
title: Creare depositi bancari
description: È possibile effettuare depositi per mantenere un record di transazione contenente informazioni che possono essere applicate a fatture e note di credito in sospeso.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '10140, 10141, 10143, 10144, 10146, 10147, 10148, 36646'
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="create-bank-deposits"></a><a name="create-bank-deposits"></a>Creare depositi bancari
> [!NOTE]
> La possibilità di creare depositi bancari è una novità del primo ciclo di rilascio del 2022 di Business Central per molte versioni nazionali. Se utilizzavi Business Central negli Stati Uniti, in Canada o in Messico prima di tale versione, puoi usare le funzionalità precedenti. Puoi continuare, ma le nuove funzionalità sostituiranno quelle precedenti in una versione futura. Per iniziare a utilizzare le nuove funzionalità descritte in questo articolo, l'amministratore può accedere alla pagina **Gestione funzionalità** e accendere ad **Aggiornamento delle funzionalità: riconciliazione e depositi bancari standardizzati**.  

Usa la pagina **Depositi bancari** per registrare i depositi come un unico documento che registra una o più movimenti su un conto bancario. In genere, i depositi bancari vengono utilizzati per registrare depositi di cassa. La pagina Depositi bancari è disponibile nel menu **Gestione cassa** in Gestione ruolo utente manager aziendale e in altre gestioni ruolo utente che si occupano della gestione di cassa.

Gli importi dei depositi bancari possono provenire da diverse origini:

* Vendite, utilizzando un conto C/G per i ricavi.
* Pagamenti cliente.
* Rimborsi di cassa dei fornitori o pagamenti di cassa. 

Le righe di deposito bancario contengono informazioni sui singoli depositi, come gli assegni dei clienti. Il totale degli importi nelle righe deve essere l'importo totale del deposito.

Dopo aver compilato le informazioni e le righe sul deposito, è necessario registrarlo. La registrazione aggiornerà i registri pertinenti. Questi registri includono la contabilità generale e i libri mastri di banca, cliente e fornitore. I depositi registrati vengono archiviati per riferimenti futuri nella pagina **Depositi bancari registrati**.

Il report **Deposito bancario** mostra i depositi di clienti e fornitori con l'importo del deposito originale, l'importo del deposito che rimane aperto e l'importo applicato. Il rapporto mostra anche l'importo totale del deposito registrato da riconciliare.

## <a name="before-you-start"></a><a name="before-you-start"></a>Operazioni preliminari
Ci sono alcune cose da impostare prima di poter utilizzare i depositi bancari. È necessario disporre di una numerazione e di un modello di giornale di registrazione generale pronto. È inoltre necessario specificare se registrare gli importi dei depositi bancari in un'unica soluzione. Cioè, come totale di tutti gli importi sulle righe di deposito. In caso contrario, ogni riga viene registrata come voce singola. La registrazione di un deposito come un unico movimento contabile bancario può semplificare la riconciliazione bancaria.

### <a name="number-series-and-lump-sum-deposits"></a><a name="number-series-and-lump-sum-deposits"></a>Numerazione e depositi forfettari
È necessario impostare una numerazione per i depositi bancari, quindi specificare la numerazione nel campo **Nr. depositi bancari** della pagina **Setup contabilità clienti**. Per ulteriori informazioni, vedi [Creare le numerazioni](ui-create-number-series.md). 

Sempre nella pagina **Setup contabilità clienti** se vuoi registrare i depositi come somme forfettarie anziché come singole righe, attiva l'interruttore **Registra depositi bancari come somma forfettaria**. La registrazione di un deposito come somma forfettaria, che crea un movimento contabile bancario per l'intero importo del deposito, può semplificare la riconciliazione bancaria.

### <a name="general-journal-templates-for-bank-deposits"></a><a name="general-journal-templates-for-bank-deposits"></a>Definizione registrazioni COGE per depositi bancari
È inoltre necessario creare una definizione registrazioni COGE per i depositi. I giornali di registrazione generali vengono utilizzati per registrare i movimenti in conti bancari, clienti, fornitori, cespiti e contabilità generale. Le definizioni registrazioni progettano le registrazioni COGE in base allo scopo del tuo lavoro. Cioè, i campi della definizione registrazioni sono esattamente quelli di cui hai bisogno. 

I depositi saranno ricevute di cassa, quindi potresti voler riutilizzare le tue numerazioni per le registrazione incassi. In alternativa, se è necessario distinguere tra registrazioni di depositi bancari e registrazioni di ricevute di cassa, puoi utilizzare una numerazione diversa.

Dovrai anche creare un processo batch per il modello. Per creare un processo batch, nella pagina **Definizioni registrazioni COGE**, scegli l'azione **Batch**. Per ulteriori informazioni, vedi [Utilizzo di batch e definizioni di registrazioni](ui-work-general-journals.md#use-journal-templates-and-batches).

## <a name="dimensions-on-bank-deposit-lines"></a><a name="dimensions-on-bank-deposit-lines"></a>Dimensioni nelle righe di deposito bancario
Le righe sul deposito bancario utilizzeranno automaticamente le dimensioni predefinite specificate nei campi **Codice reparto** e **Codice gruppo di clienti**. Quando scegli **Cliente** o **Fornitore** nel campo **Tipo di account**, le dimensioni specificate per il cliente o il fornitore sostituiranno le impostazioni predefinite. Puoi modificare le dimensioni nelle righe in base alle esigenze.

> [!TIP]
> Le dimensioni nelle linee vengono impostate in base alle priorità delle dimensioni predefinite. Le dimensioni della riga sono prioritarie rispetto alle dimensioni dell'intestazione. Per evitare conflitti, puoi creare regole che stabiliscono la priorità quando utilizzare una dimensione a seconda dell'origine. Se desideri modificare la priorità delle dimensioni, puoi modificare le classifiche nella pagina **Priorità dimensione predefinita**. Per ulteriori informazioni, vedi [Per impostare priorità nelle dimensioni predefinite](finance-dimensions.md#to-set-up-default-dimension-priorities).

## <a name="create-a-bank-deposit"></a><a name="create-a-bank-deposit"></a>Creare un deposito bancario
1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Depositi bancari**, quindi scegli il collegamento correlato.
2. Scegli **Nuovo** per aprire la pagina **Deposito bancario**. 
3. Scegli la definizione di registrazioni COGE che hai creato per i depositi bancari.  

    > [!NOTE]
    > Se la definizione di registrazioni COGE ha più di un batch, ti verrà richiesto di sceglierne uno.

4. Nel campo **Nr. conto bancario** seleziona il conto bancario in cui vuoi effettuare il deposito.

    > [!TIP]
    > Puoi ricontrollare che stai depositando sul conto corretto utilizzando le azioni **Scheda conto** e **Movimenti contabili** per cercare i movimenti contabili per il conto bancario selezionato. Ad esempio, per vedere se sono stati effettuati depositi simili sul conto.

5. Nel campo **Importo totale deposito** inserisci l'importo totale del deposito. Questo totale deve essere la somma degli importi di tutte le righe.
6. Compilare i rimanenti campi, se necessario. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)]

    La data nel campo **Data registrazione** e le dimensioni nei campi **Codice reparto** e **Codice gruppo di clienti** verranno assegnate alle righe che crei per il deposito bancario. Se necessario, puoi modificarle. 

7. A seconda che tu voglia registrare il deposito bancario come somma forfettaria o ogni riga singolarmente nel libro mastro della banca, attiva o disattiva l'interruttore **Registra come somma forfettaria**. L'impostazione predefinita deriva dallo stesso interruttore della pagina **Setup contabilità clienti**.

    > [!NOTE]
    > Il campo **Codice valuta** mostra la valuta specificata per il conto bancario scelto. Non puoi scegliere una valuta diversa.

8. Nella scheda dettaglio **Righe** crea una nuova riga per ogni pagamento di cassa che vuoi depositare.
9. Nel campo **Tipo di account** specifica l'origine del pagamento. Per i depositi bancari, il tipo è in genere **Cliente** o **Venditore**. 

    > [!NOTE]
    > Puoi anche registrare un pagamento di cassa per un fornitore. Per farlo, scegli **Fornitore** e quindi immetti l'importo del pagamento come numero negativo nel campo **Avere** della riga. 

10. Nel campo **Nr. documento esterno**, immetti il numero documento della fattura da cui ha origine l'importo. Puoi utilizzare un numero di documento per ciascuna riga o lo stesso numero per tutte le righe.

    > [!TIP]
    > In genere, non è necessario compilare il campo **Tipo di documento** per le voci finanziarie. Ad esempio, se stai depositando contanti dalla vendita del giorno, lasci il campo vuoto. Se stai depositando contanti da un pagamento cliente, scegli **Pagamento**.

11. Se stai depositando un pagamento di cassa per una fattura cliente specifica, scegli l'azione **Applica voci** quindi immetti il numero di fattura nel campo **Collega a ID**. 
12. Se sei pronto per registrare il deposito bancario, scegli l'azione **Registra**.

    > [!TIP]
    > Prima di registrare il deposito puoi utilizzare l'azione **Report test** per rivedere i tuoi dati. Il rapporto mostrerà se ci sono problemi, come dati mancanti, che impediscono la registrazione.  

## <a name="finding-posted-bank-deposits"></a><a name="finding-posted-bank-deposits"></a>Ricerca dei depositi bancari registrati
La pagina **Depositi bancari registrati** elenca i depositi precedenti della tua azienda. Nell'elenco è possibile rivedere i commenti e le dimensioni specificati per i depositi. Puoi aprire il deposito bancario per visualizzare maggiori dettagli e puoi indagare ulteriormente. Ad esempio, è possibile scegliere l'azione Trova movimenti per visualizzare i movimenti contabili bancari registrati. Dal movimento contabile bancario, puoi trovare il corrispondente movimento di contabilità generale registrato.

Se vuoi cercare tutti i movimenti di contabilità generale per le righe di deposito registrate, vai alla pagina **Registro C/G** e utilizza l'azione **Contabilità generale**. Troverai tutti i movimenti di contabilità generale, inclusi i movimenti per clienti e fornitori.

## <a name="reversing-a-posted-bank-deposit"></a><a name="reversing-a-posted-bank-deposit"></a>Storno di un deposito bancario registrato
Per stornare un deposito registrato, vai alla pagina **Registri C/G** trova il registro per il deposito, quindi scegli l'azione **Storna registro**.

> [!NOTE]
> È possibile stornare solo un registro che contiene un solo tipo di voce. Cioè, il registro deve contenere solo voci cliente o voci fornitore, ma non entrambe. Se un registro contiene entrambi è necessario stornare manualmente il deposito.      

## <a name="see-also"></a><a name="see-also"></a>Vedere anche
[Finanze](finance.md)  
[Impostazione di dati finanziari](finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]



