---
title: Esportare i pagamenti in un file di pagamento elettronico| Documenti Microsoft
description: Per eseguire i pagamenti ai fornitori, si può attivare un servizio di conversione dati bancari, esportare un file della banca, e caricare il file della banca elettronica per trasferire i fondi.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank file export, re-export, bank transfer, AMC, bank data conversion service, funds transfer
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer
ms.openlocfilehash: 539aac89d2da6b2eb81da7f6df729cdb5bc15cb1
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2019
ms.locfileid: "926560"
---
# <a name="export-payments-to-a-bank-file"></a>Esportare pagamenti in un file della banca
Quando si è pronti a effettuare i pagamenti ai fornitori o i rimborsi ai dipendenti, nella pagina **Registrazioni pagamenti** è possibile esportare un file con le informazioni di pagamento delle righe. È quindi possibile caricare il file sulla banca per elaborare i relativi trasferimenti di denaro.

Nella versione generica di [!INCLUDE[d365fin](includes/d365fin_md.md)], viene installato e connesso un provider di servizi globale per convertire i dati bancari in qualsiasi formato di file richiesto dalla banca. Nelle versioni per il Nord America, lo stesso servizio può essere utilizzato per inviare file di pagamento come trasferimento dei fondi elettronici (EFT), ma con un processo leggermente diverso. Vedere la sezione 6 [Per esportare pagamenti in un file della banca](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#to-export-payments-to-a-bank-file).    

> [!NOTE]  
>   Prima di esportare i file di pagamento dalle registrazioni dei pagamenti, è necessario specificare il formato elettronico per il conto corrente bancario di interesse ed è necessario abilitare il servizio di conversione dati bancari. Per ulteriori informazioni, vedere [Impostare i conti correnti bancari](bank-how-setup-bank-accounts.md) e [Impostare il servizio di conversione di dati bancari](bank-how-setup-bank-data-conversion-service.md). Inoltre, è necessario selezionare la casella di controllo **Consenti esportazione pagamento** nella pagina **Batch registrazioni COGE**. Per ulteriori informazioni, vedere [Utilizzo delle registrazioni COGE](ui-work-general-journals.md).  

Per visualizzare i file di pagamento che sono stati esportati dalle registrazioni pagamenti, si utilizza la pagina **Registri di bonifici**. Da questa pagina è inoltre possibile riesportare i file di pagamento in caso di errori tecnici o di modifiche al file. Si noti, tuttavia, che i file esportati EFT non sono visualizzati in questa pagina e non possono essere riesportati.  

## <a name="to-export-payments-to-a-bank-file"></a>Per esportare pagamenti in un file della banca
Di seguito viene descritto come pagare un fornitore tramite assegno. I passaggi sono simili al rimborso dei clienti tramite assegno.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Registrazioni pagamenti** e quindi scegliere il collegamento correlato.
2. Compilare le righe di registrazione pagamenti. Per ulteriori informazioni, vedere [Registrare pagamenti e rimborsi](payables-how-post-payments-refunds.md).

> [!NOTE]  
>   Se si utilizza EFT, è necessario selezionare **Pagamento elettronico** o **Pagamento elettronico IAT** nel campo **Tipo pagamento banca**. Servizi di esportazione file diversi e i rispettivi formati richiedono valori di configurazione differenti nelle pagine **Scheda conto corrente bancario** e **Scheda C/C bancari fornitori**. Si verrà informati sui valori di setup mancanti o non corretti mentre si tenta di esportare il file.

3. Una volta completate tutte le righe di registrazione pagamenti, scegliere l'azione **Esporta pagamenti su file**.
4. Nella pagina **Esporta pagamenti elettronici** compilare i campi secondo le necessità.

    Tutti i messaggi di errore verranno visualizzati nel riquadro Dettaglio informazioni di **Errori nel file di pagamento** dove è anche possibile scegliere un messaggio di errore per visualizzare informazioni dettagliate. È necessario risolvere tutti gli errori prima di esportare il file di pagamento.

    > [!TIP]  
    >   Quando si utilizza il servizio di conversione dati bancari, un messaggio di errore comune informa che il numero di conto corrente bancario non ha la lunghezza richiesta dalla banca. Per evitare o risolvere l'errore, è necessario rimuovere il valore nel campo **IBAN** nella pagina **Scheda conto corrente bancario**, quindi nel campo **Nr. conto bancario** , immettere un numero di conto corrente bancario nel formato richiesto dalla banca.

5. Nella pagina **Salva con nome** specificare il percorso in cui verrà esportato il file e scegliere **Salva**.

    > [!NOTE]  
    >   Se si utilizza EFT, salvare il modulo della risultante rimessa del fornitore come documento di Word o selezionare in modo che venga inviato tramite posta elettronica direttamente al fornitore. I pagamenti sono ora aggiunti alla pagina **Genera file EFT** da cui è possibile generare più ordini di pagamento contemporaneamente per ridurre i costi di trasmissione. Per ulteriori informazioni, vedere i seguenti passaggi:
6. Nella pagina **Registrazioni pagamenti** selezionare l'azione **Genera file EFT**.

    Nella pagina **Genera file EFT** tutti i pagamenti impostati per EFT esportati dalle registrazioni pagamento per un conto corrente bancario specificato ma non ancora generati sono elencati nella Scheda dettaglio **Righe**.
7. Scegliere l'opzione l'azione **Genera file EFT** per esportare un file per tutti i pagamenti EFT.
8. Nella pagina **Salva con nome** specificare il percorso in cui verrà esportato il file e scegliere **Salva**.

Il file di pagamento bancario viene esportato verso il percorso specificato, quindi è possibile procedere a caricarlo nel conto corrente bancario elettronico ed effettuare i pagamenti effettivi. Sarà quindi possibile registrare le righe esportate delle registrazioni pagamenti.

## <a name="to-plan-when-to-post-exported-payments"></a>Per pianificare quando registrare i pagamenti esportati
Se non si desidera registrare una riga di registrazione pagamenti per un pagamento esportato, ad esempio perché si sta attendendo la conferma che la transazione sia stata lavorata dalla banca, è possibile eliminare la riga di registrazione. Quando in seguito si crea una riga di registrazione pagamenti per pagare l'importo residuo nella fattura, il campo **Importo totale esportato** visualizza la quantità dell'importo pagamento già esportata. Inoltre, è possibile trovare informazioni dettagliate sul totale esportato scegliendo il pulsante **Movimenti dei registri di bonifici** per visualizzare i dettagli relativi ai file di pagamento esportati.

Se si segue una procedura secondo la quale i pagamenti non vengono registrati fino a quando non si riceve la conferma che sono stati elaborati dalla banca, è possibile controllare la situazione in due modi.

* Nelle registrazioni pagamenti con le righe di pagamento suggerite, è possibile ordinare la colonna **Esportato su file pagamento** o **Importo totale esportato** e poi eliminare i suggerimenti di pagamento per le fatture aperte per le quali i pagamenti sono già stati effettuati e per le quali non si desidera creare pagamenti.
* Nella pagina **Sugg. pagamenti fornitore**, dove si specifica quali pagamenti inserire nelle registrazioni pagamenti, è possibile selezionare la casella di controllo **Ignora pagamenti esportati** se non si desidera inserire le righe di registrazione per i pagamenti che sono già stati esportati.

Per visualizzare le informazioni sui pagamenti esportati, scegliere l'azione **Storico esportazione pagamento**.

## <a name="to-re-export-payments-to-a-bank-file"></a>Per riesportare i pagamenti in un file della banca
È possibile riesportare i file di pagamento dalla pagina **Registri di bonifici**. Prima di eliminare o registrare righe di registrazione pagamenti, è possibile anche riesportare il file di pagamento dalla pagina **Registrazioni pagamenti** semplicemente esportandolo di nuovo. Se sono state eliminate o registrate delle righe di registrazione pagamenti dopo l'esportazione, è possibile riesportare lo stesso file di pagamento dalla pagina **Registri di bonifici**. Selezionare la riga per il batch di bonifici che si desidera riesportare, quindi utilizzare l'azione **Riesporta pagamenti su file**.

> [!NOTE]  
>   I file esportati EFT non sono visualizzati nella pagina **Registri di bonifici** e non possono essere riesportati.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Registri di bonifici** e quindi scegliere il collegamento correlato.
2. Selezionare un'esportazione pagamento che si desidera riesportare quindi scegliere l'azione **Riesporta pagamenti su file**.

## <a name="see-also"></a>Vedi anche
[Effettuare i pagamenti](payables-make-payments.md)  
[Contabilità fornitori](payables-manage-payables.md)  
[Impostazioni acquisti](purchasing-setup-purchasing.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
