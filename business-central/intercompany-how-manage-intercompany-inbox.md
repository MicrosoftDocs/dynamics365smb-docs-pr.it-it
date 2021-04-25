---
title: Elaborare le transazioni IC in entrata e in uscita | Microsoft Docs
description: Le transazioni intercompany che si ricevono dai partner IC sono elencate nella posta in arrivo IC. Qui è possibile elaborarle manualmente o automaticamente.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoming document
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 17c9c5202f7a7f7dae6a9eee14109c608db14c46
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5786300"
---
# <a name="manage-the-intercompany-inbox-and-outbox"></a>Gestire la casella in entrata e in uscita intercompany
Tutte le transazioni intercompany ricevute elettronicamente dai partner intercompany sono elencate nella posta in arrivo IC.  

## <a name="organizing-the-inbox"></a>Organizzazione della casella in arrivo  
 È possibile utilizzare i campi filtro disponibili nella parte superiore della pagina della posta in arrivo/casella in arrivo per determinare il tipo di transazioni visualizzate nella pagina. Se ad esempio si desidera visualizzare solo le transazioni create da un determinato partner, è possibile immettere filtri nei filtri **Origine transazione** e **Codice partner IC**.  

### <a name="transaction-source"></a>Origine transazione  
Le operazioni che è possibile eseguire con una determinata transazione variano a seconda che quest'ultima sia stata:  

- Creata da un partner intercompany  
- Restituita all'utente perché rifiutata da un partner intercompany  

È possibile utilizzare il campo **Mostra origine transazione** per filtrare il contenuto della pagina **Casella transazioni in arrivo intercompany** in modo da visualizzare solo uno di questi tipi di transazioni alla volta. È possibile filtrare il contenuto anche in base al partner IC oppure in base al contenuto del campo **Azione riga**.  

#### <a name="created-by-intercompany-partner"></a>Creata da un partner intercompany  
 Quando si riceve una nuova transazione creata da un partner, è possibile:

- Accettare la transazione.  
- Rifiutare la transazione, restituendola al partner.  
- Annullare la transazione, eliminandola senza restituirla al partner.  

#### <a name="returned-from-intercompany-partner"></a>Restituita da un partner intercompany  
 Se la transazione è stata rifiutata dal partner IC, l'unica possibilità è annullare la transazione nella casella in arrivo. Successivamente è necessario creare righe di rettifica o stornare la registrazione o il documento della società.  

## <a name="recreating-inbox-entries"></a>Ricostruzione di movimenti nella casella in arrivo  
 Se si accetta una transazione nella posta in arrivo/casella in arrivo e, successivamente, si elimina la registrazione o il documento anziché registrarlo, è possibile ricreare il movimento nella posta in arrivo/casella in arrivo e accettarlo nuovamente.  

## <a name="getting-an-overview-of-intercompany-transactions-for-a-period"></a>Sintesi delle transazioni intercompany per un periodo specifico  
 È possibile ottenere una sintesi di tutte le transazioni intercompany inviate e ricevute in un determinato periodo. Nel report **Transazioni intercompany** sono elencati tutti i movimenti C/G intercompany, i movimenti contabili dei clienti e quelli dei fornitori.

 > [!NOTE]  
 > Se i partner intercompany si trovano nello stesso database, le transazioni vengono trasferite senza la necessità di file o e-mail. Vedere il campo **Tipo trasferimento** nella pagina **Partner IC**. <br /><br />
In tal caso, è possibile impostare il sistema in modo che ignori le caselle di posta in arrivo e in uscita selezionando la casella di controllo **Accetta automaticamente le transazioni** nella pagina **Partner IC** e la casella di controllo **Invia automaticamente le transazioni** nella pagina **Setup intercompany**.

## <a name="to-import-intercompany-transactions-from-a-file"></a>Per importare transazioni intercompany da un file  
Le transazioni intercompany inviate dai partner intercompany non inclusi nello stesso database della società possono essere ricevute in un file XML. Tali transazioni devono essere quindi importate nella posta in arrivo/casella in arrivo.  

1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Informazioni società** e quindi scegliere il collegamento correlato.
2. Salvare il file nel percorso specificato nel campo **Dettagli casella in arrivo Intercompany** della pagina **Informazioni società**.  
3. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Casella transazioni in arrivo intercompany** e quindi scegliere il collegamento correlato.
4. Nella pagina **Casella transazioni in arrivo intercompany** scegliere l'azione **Importa file di transazioni**.  
5. Nella pagina visualizzata selezionare il file XML contenente le transazioni, quindi scegliere **Apri**.  

Le transazioni vengono importata nella posta in arrivo/casella in arrivo ed è quindi possibile elaborarle.

## <a name="to-process-incoming-intercompany-transactions"></a>Per elaborare le transazioni intercompany in entrata  
Le transazioni intercompany inviate dai partner intercompany vengono inserite nella posta in arrivo/casella in arrivo IC. È necessario valutare singolarmente ogni transazione presente nella posta in arrivo/casella in arrivo per determinare l'operazione da eseguire.  

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Casella transazioni in arrivo intercompany** e quindi scegliere il collegamento correlato.  
2. Nella pagina **Casella transazioni in arrivo intercompany** selezionare una riga e scegliere un'azione, ad esempio **Accetta**, per elaborare la riga.
3. Nella pagina **Az. casella in arr. IC completa** compilare i campi secondo le necessità. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Scegliere il pulsante **OK**.  

Per le righe elaborate con l'azione **Accetta**, verranno create righe di documento o di registrazione nella società. Aprire i singoli documenti o registrazioni, apportare le modifiche necessarie ed effettuare la registrazione.  

Le righe elaborate con l'azione **Rinvia a Partner** verranno spostate nella casella di posta in uscita da cui sarà possibile inviarle al partner.

Per le righe elaborate con l'azione **Reso da partner**, è necessario registrare una correzione alla transazione origine contabilizzata nella società.

## <a name="to-process-outgoing-intercompany-transactions"></a>Per elaborare le transazioni intercompany in uscita  
Quando si annotano registrazioni o documenti intercompany oppure si invia una conferma d'ordine intercompany, le transazioni corrispondenti vengono inviate alla Posta in Uscita IC. Per inviarle ai partner IC, è necessario aprire la Posta in Uscita ed elaborarle.  

1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Casella transazioni in uscita intercompany** e quindi scegliere il collegamento correlato.  
2. Nella pagina **Casella transazioni in uscita intercompany** selezionare una riga e scegliere un'azione, ad esempio **Torna a casella in arrivo**, per elaborare la riga.

Le righe elaborate con l'azione **Invia a Partner IC** verranno inviate alla casella di posta in arrivo del partner di pertinenza.

Le righe elaborate con l'azione **Torna a casella in arrivo** saranno spostate nella casella in arrivo, dove sarà possibile accettarle per creare righe di documento o di registrazioni nella società.  

Per le righe elaborate con l'azione **Annulla**, è necessario registrare una correzione alla transazione origine contabilizzata nella società.  

## <a name="to-recreate-intercompany-inbox-transactions"></a>Per ricreare transazioni nella posta in arrivo intercompany  
Talvolta, potrebbe essere utile ricreare una transazione nella casella di posta in arrivo o in uscita. Se ad esempio si accetta una transazione nella posta in arrivo/casella in arrivo e, successivamente, si elimina il documento o le registrazioni anziché registrarle, è possibile ricreare il movimento nella posta in arrivo/casella in arrivo e accettarlo nuovamente.  

Nella procedura seguente viene descritto come ricreare transazioni in arrivo, tuttavia è possibile applicare gli stessi passaggi per quelle in uscita.

  1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Casella transazioni in arrivo IC gestite** e quindi scegliere il collegamento correlato.  

  2.  Nella pagina **Casella transazioni in arrivo IC gestite** selezionare la riga con la transazione che si desidera ricreare nella casella in arrivo, quindi scegliere l'azione **Ricrea casella transazione in arrivo**.  

## <a name="see-also"></a>Vedi anche
[Gestione delle transazioni Intercompany](intercompany-manage.md)  
[Finanze](finance.md)  
[Impostazione di dati finanziari](finance-setup-finance.md)  
[Utilizzo delle registrazioni COGE](ui-work-general-journals.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]