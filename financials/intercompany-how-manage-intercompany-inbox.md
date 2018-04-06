---
title: Elaborare le transazioni IC in entrata e in uscita | Microsoft Docs
description: "Le transazioni intercompany che si ricevono dai partner IC sono elencate nella posta in arrivo IC. Qui è possibile elaborarle manualmente o automaticamente."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoming document
ms.date: 07/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: abeb3ee24434ca3549e7ed88ecfae54cc395002d
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="manage-the-intercompany-inbox-and-outbox"></a>Gestire la casella in entrata e in uscita intercompany
Tutte le transazioni intercompany ricevute elettronicamente dai partner intercompany sono elencate nella posta in arrivo IC.  

## <a name="organizing-the-inbox"></a>Organizzazione della casella in arrivo  
 È possibile utilizzare i campi filtro disponibili nella parte superiore della finestra della posta in arrivo/casella in arrivo per determinare il tipo di transazioni visualizzate nella finestra. Se ad esempio si desidera visualizzare solo le transazioni create da un determinato partner, è possibile immettere filtri nei filtri **Origine transazione** e **Codice partner IC**.  

### <a name="transaction-source"></a>Origine transazione  
Le operazioni che è possibile eseguire con una determinata transazione variano a seconda che quest'ultima sia stata:  

- Creata da un partner intercompany  
- Restituita all'utente perché rifiutata da un partner intercompany  

È possibile utilizzare il campo **Mostra origine transazione** per filtrare il contenuto della finestra **Casella transazioni in arrivo intercompany** in modo da visualizzare solo uno di questi tipi di transazioni alla volta. È possibile filtrare il contenuto anche in base al partner IC oppure in base al contenuto del campo **Azione riga**.  

#### <a name="created-by-intercompany-partner"></a>Creata da un partner intercompany  
 Quando si riceve una nuova transazione creata da un partner, è possibile:

- Accettare la transazione.  
- Rifiutare la transazione, restituendola al partner.  
- Annullare la transazione, eliminandola senza restituirla al partner.  

#### <a name="returned-from-intercompany-partner"></a>Restituita da un partner intercompany  
 Se la transazione è stata rifiutata dal partner IC, l'unica possibilità è annullare la transazione nella casella in arrivo. Successivamente è necessario creare righe di rettifica o stornare la registrazione o il documento della società.  

## <a name="re-creating-inbox-entries"></a>Ricostruzione di movimenti nella casella in arrivo  
 Se si accetta una transazione nella posta in arrivo/casella in arrivo e, successivamente, si elimina la registrazione o il documento anziché registrarlo, è possibile ricreare il movimento nella posta in arrivo/casella in arrivo e accettarlo nuovamente.  

## <a name="getting-an-overview-of-intercompany-transactions-for-a-period"></a>Sintesi delle transazioni intercompany per un periodo specifico  
 È possibile ottenere una sintesi di tutte le transazioni intercompany inviate e ricevute in un determinato periodo. Nel report **Transazioni intercompany** sono elencati tutti i movimenti C/G intercompany, i movimenti contabili dei clienti e quelli dei fornitori.

 > [!NOTE]  
 > Se i partner intercompany si trovano nello stesso database, le transazioni vengono trasferite senza la necessità di file o e-mail. Vedere il campo **Tipo trasferimento** nella finestra **Partner IC**. <br /><br />
In tal caso, è possibile impostare il sistema in modo che ignori le caselle di posta in arrivo e in uscita selezionando la casella di controllo **Accetta automaticamente le transazioni** nella finestra **Partner IC** e la casella di controllo **Invia automaticamente le transazioni** nella finestra **Setup intercompany**.

## <a name="to-import-intercompany-transactions-from-a-file"></a>Per importare transazioni intercompany da un file  
Le transazioni intercompany inviate dai partner intercompany non inclusi nello stesso database della società possono essere ricevute in un file XML. Tali transazioni devono essere quindi importate nella posta in arrivo/casella in arrivo.  

1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Informazioni società**, quindi scegliere il collegamento correlato.
2. Salvare il file nel percorso specificato nel campo **Dettagli casella in arrivo Intercompany** della finestra **Informazioni società**.  
3. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Casella transazioni in arrivo intercompany**, quindi scegliere il collegamento correlato.
4. Nella finestra **Casella transazioni in arrivo intercompany** scegliere l'azione **Importa file di transazioni**.  
5. Nella finestra visualizzata selezionare il file XML contenente le transazioni, quindi scegliere **Apri**.  

Le transazioni vengono importata nella posta in arrivo/casella in arrivo ed è quindi possibile elaborarle.

## <a name="to-process-incoming-intercompany-transactions"></a>Per elaborare le transazioni intercompany in entrata  
Le transazioni intercompany inviate dai partner intercompany vengono inserite nella posta in arrivo/casella in arrivo IC. È necessario valutare singolarmente ogni transazione presente nella posta in arrivo/casella in arrivo per determinare l'operazione da eseguire.  

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Casella transazioni in arrivo intercompany**, quindi scegliere il collegamento correlato.  
2. Nella finestra **Casella transazioni in arrivo intercompany** selezionare una riga e scegliere un'azione, ad esempio **Accetta**, per elaborare la riga.
3. Nella finestra **Az. casella in arr. IC completa** compilare i campi secondo le necessità. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Scegliere il pulsante **OK**.  

Per le righe elaborate con l'azione **Accetta**, verranno create righe di documento o di registrazione nella società. Aprire i singoli documenti o registrazioni, apportare le modifiche necessarie ed effettuare la registrazione.  

Le righe elaborate con l'azione **Rinvia a Partner** verranno spostate nella casella di posta in uscita da cui sarà possibile inviarle al partner.

Per le righe elaborate con l'azione **Reso da partner**, è necessario registrare una correzione alla transazione origine contabilizzata nella società.

## <a name="to-process-outgoing-intercompany-transactions"></a>Per elaborare le transazioni intercompany in uscita  
Quando si annotano registrazioni o documenti intercompany oppure si invia una conferma d'ordine intercompany, le transazioni corrispondenti vengono inviate alla Posta in Uscita IC. Per inviarle ai partner IC, è necessario aprire la Posta in Uscita ed elaborarle.  

1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Casella transazioni in uscita intercompany**, quindi scegliere il collegamento correlato.  
2. Nella finestra **Casella transazioni in uscita intercompany** selezionare una riga e scegliere un'azione, ad esempio **Torna a casella in arrivo**, per elaborare la riga.

Le righe elaborate con l'azione **Invia a Partner IC** verranno inviate alla casella di posta in arrivo del partner di pertinenza.

Le righe elaborate con l'azione **Torna a casella in arrivo** saranno spostate nella casella in arrivo, dove sarà possibile accettarle per creare righe di documento o di registrazioni nella società.  

Per le righe elaborate con l'azione **Annulla**, è necessario registrare una correzione alla transazione origine contabilizzata nella società.  

## <a name="to-recreate-intercompany-inbox-transactions"></a>Per ricreare transazioni nella posta in arrivo intercompany  
Talvolta, potrebbe essere utile ricreare una transazione nella casella di posta in arrivo o in uscita. Se ad esempio si accetta una transazione nella posta in arrivo/casella in arrivo e, successivamente, si elimina il documento o le registrazioni anziché registrarle, è possibile ricreare il movimento nella posta in arrivo/casella in arrivo e accettarlo nuovamente.  

Nella procedura seguente viene descritto come ricreare transazioni in arrivo, tuttavia è possibile applicare gli stessi passaggi per quelle in uscita.

  1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Casella transazioni in arrivo IC gestite**, quindi scegliere il collegamento correlato.  

  2.  Nella finestra **Casella transazioni in arrivo IC gestite** selezionare la riga con la transazione che si desidera ricreare nella casella in arrivo, quindi scegliere l'azione **Ricrea casella transazione in arrivo**.  

## <a name="see-also"></a>Vedi anche
[Gestione delle transazioni Intercompany](intercompany-manage.md)  
[Finanze](finance.md)  
[Impostazione di dati finanziari](finance-setup-finance.md)  
[Utilizzo delle registrazioni COGE](ui-work-general-journals.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

