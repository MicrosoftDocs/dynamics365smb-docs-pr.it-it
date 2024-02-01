---
title: Gestire la casella in entrata e in uscita intercompany
description: Le transazioni intercompany che si ricevono dai partner sono elencate nella casella in entrata IC. Qui è possibile elaborarle manualmente o automaticamente.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.date: 02/06/2023
ms.custom: bap-template
ms.search.keywords: incoming document
ms.search.form: '600, 605, 618, 650, 651, 648, 649, 617, 614, 642, 643, 640, 641, 613, 616, 646, 647, 644, 645, 615, 619, 612, 638, 639, 636, 637, 611'
ms.service: dynamics-365-business-central
---
# <a name="manage-the-intercompany-inbox-and-outbox"></a>Gestire la casella in entrata e in uscita intercompany

Le transazioni intercompany ricevute dai partner sono elencate nella pagina **Casella in entrata intercompany**. Per informazioni su come elaborare transazioni intercompany in entrata, vai a [Elaborare transazioni intercompany in entrata](#process-incoming-intercompany-transactions). Le transazioni intercompany inviate ai partner sono elencate nella pagina **Casella in uscita intercompany**. Per informazioni su come elaborare transazioni intercompany in uscita, vai a [Elaborare transazioni intercompany in uscita](#to-process-outgoing-intercompany-transactions).

Tuttavia, a seconda della configurazione intercompany, alcune transazioni vengono gestite automaticamente. È possibile impostare la società di origine e le società partner in modo che creino automaticamente documenti e giornali di registrazione corrispondenti alle transazioni che i partner registrano tramite il giornale di registrazioni COGE intercompany. Per informazioni sull'utilizzo dei giornali di registrazione intercompany, vai a [Compilare e registrare un giornale di registrazione intercompany](intercompany-how-work-documents-journals.md#fill-in-and-post-an-intercompany-journal).  

## <a name="organizing-the-inbox"></a>Organizzazione della casella in arrivo

È possibile utilizzare i campi filtro disponibili nella parte superiore della pagina casella in entrata per determinare il tipo di transazioni visualizzate nella pagina. Se ad esempio vuoi visualizzare solo le transazioni create da un determinato partner, puoi usare i filtri **Origine transazione** e **Codice partner IC**.  

### <a name="transaction-source"></a>Origine transazione

Le operazioni che è possibile eseguire con una determinata transazione variano a seconda che quest'ultima sia stata:  

* Creata da un partner intercompany  
* Restituita all'utente perché rifiutata da un partner intercompany  

Utilizza il campo **Mostra origine transazione** per filtrare il contenuto della pagina **Casella transazioni in arrivo intercompany** in modo da visualizzare solo uno di questi tipi di transazioni alla volta. Puoi filtrare il contenuto anche in base al partner IC oppure in base al contenuto del campo **Azione riga**.  

#### <a name="created-by-intercompany-partner"></a>Creata da un partner intercompany

 Quando si riceve una nuova transazione creata da un partner, è possibile:

* Accettare la transazione.  
* Rifiutare la transazione, restituendola al partner  
* Annullare la transazione, eliminandola senza restituirla al partner  

#### <a name="returned-from-intercompany-partner"></a>Restituita da un partner intercompany

Se il partner intercompany rifiuta una transazione, è necessario annullare la transazione nella casella in entrata e quindi creare righe di correzione o stornare il giornale di registrazione o il documento.  

## <a name="recreating-inbox-entries"></a>Ricostruzione di movimenti nella casella in entrata

Se si accetta una transazione nella posta in arrivo/casella in arrivo e, successivamente, si elimina la registrazione o il documento anziché registrarlo, è possibile ricreare il movimento nella posta in arrivo/casella in arrivo e accettarlo nuovamente.  

## <a name="get-an-overview-of-intercompany-transactions-for-a-period"></a>Ottenere una panoramica delle transazioni intercompany per un periodo

È possibile ottenere una sintesi di tutte le transazioni intercompany inviate e ricevute in un determinato periodo. Nel report **Transazioni intercompany** sono elencati tutti i movimenti C/G intercompany, i movimenti contabili dei clienti e quelli dei fornitori.

> [!NOTE]  
> Se i partner intercompany si trovano nello stesso database, i partner possono accettare automaticamente le transazioni. Vai direttamente alle pagine **Transazioni in entrata intercompany gestite** e **Transazioni in uscita intercompany gestite**. Per ulteriori informazioni sull'accettazione automatica delle transazioni, vai a [Accettare automaticamente transazioni da partner intercompany](intercompany-how-setup.md#auto-accept-transactions-from-intercompany-partners).  
>
> * Per il partner di sincronizzazione, sulla pagina **Setup intercompany** attiva l'interruttore **Invia automaticamente le transazioni**.
> * Per le società partner, sulla pagina **Partner IC** attiva l'interruttore **Accetta automaticamente transazioni**.  

## <a name="import-intercompany-transactions-from-a-file"></a>Importare transazioni intercompany da un file

[!INCLUDE [onprem_only_md](includes/onprem_only_md.md)]

Le transazioni intercompany inviate dai partner intercompany non inclusi nello stesso database della società possono essere ricevute in un file XML. Tali transazioni devono essere quindi importate nella posta in arrivo/casella in arrivo.  

1. Salva il file nel percorso che hai specificato nel campo **Dettagli casella in arrivo Intercompany** quando hai impostato l'intercompany.  
2. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Casella transazioni in arrivo intercompany**, quindi scegli il collegamento correlato.
3. Nella pagina **Casella transazioni in arrivo intercompany** scegliere l'azione **Importa file di transazioni**.  
4. Nella pagina visualizzata selezionare il file XML contenente le transazioni, quindi scegliere **Apri**.  

Le transazioni vengono importata nella posta in arrivo/casella in arrivo ed è quindi possibile elaborarle.

## <a name="process-incoming-intercompany-transactions"></a>Elaborare le transazioni intercompany in entrata

Le transazioni intercompany inviate dai partner intercompany vengono inserite nella posta in arrivo/casella in arrivo IC. È necessario valutare singolarmente ogni transazione presente nella posta in arrivo/casella in arrivo per determinare l'operazione da eseguire.  

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Casella transazioni in arrivo intercompany**, quindi scegli il collegamento correlato.  
2. Nella pagina **Casella transazioni in arrivo intercompany** selezionare una riga e scegliere un'azione, ad esempio **Accetta**, per elaborare la riga.
3. Nella pagina **Az. casella in arr. IC completa** compilare i campi secondo le necessità. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Scegli il pulsante **OK**.  

Per le righe accettate, vengono create righe di documento o di registrazione nella società. Aprire i singoli documenti o registrazioni, apportare le modifiche necessarie ed effettuare la registrazione.  

Le righe che rifiuti e restituisci al tuo partner vanno nella tua casella in uscita intercompany, dove puoi inviarle al tuo partner.

Per le righe che un partner ha rifiutato e ti ha restituito, è necessario registrare una correzione alla transazione origine contabilizzata nella società.

## <a name="to-process-outgoing-intercompany-transactions"></a>Per elaborare le transazioni intercompany in uscita

Quando si annotano registrazioni o documenti intercompany oppure si invia una conferma d'ordine intercompany, le transazioni corrispondenti vengono inviate alla Posta in Uscita IC. Per inviarle ai partner IC, è necessario aprire la casella in uscita ed elaborarle.  

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Casella transazioni in uscita intercompany**, quindi scegli il collegamento correlato.  
2. Nella pagina **Casella transazioni in uscita intercompany** selezionare una riga e scegliere un'azione, ad esempio **Torna a casella in arrivo**, per elaborare la riga.

Utilizza l'azione **Invia a partner IC** per inviare righe alla casella in entrata del partner interessato.

Usa l'azione **Torna a casella in arrivo** per spostare le righe nella casella in arrivo, dove sarà possibile accettarle per creare righe di documento o di registrazioni nella società.  

Se usi l'azione **Annulla**, è necessario registrare una correzione alla transazione origine contabilizzata nella società.  

## <a name="recreate-intercompany-inbox-transactions"></a>Ricreare transazioni nella casella in entrata intercompany

Potrebbe essere utile ricreare una transazione nella casella in entrata o in uscita. Se ad esempio si accetta una transazione nella posta in arrivo/casella in arrivo e, successivamente, si elimina il documento o le registrazioni anziché registrarle, è possibile ricreare il movimento nella posta in arrivo/casella in arrivo e accettarlo nuovamente.  

Nella procedura seguente viene descritto come ricreare transazioni in arrivo, tuttavia è possibile applicare gli stessi passaggi per quelle in uscita.

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Casella transazioni in arrivo IC gestite**, quindi scegli il collegamento correlato.  
2. Nella pagina **Casella transazioni in arrivo IC gestite** selezionare la riga con la transazione che si desidera ricreare nella casella in arrivo, quindi scegliere l'azione **Ricrea casella transazione in arrivo**.  

## <a name="see-also"></a>Vedi anche

[Gestione delle transazioni Intercompany](intercompany-manage.md)  
[Finanze](finance.md)  
[Impostazione di dati finanziari](finance-setup-finance.md)  
[Utilizzare le registrazioni COGE](ui-work-general-journals.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
