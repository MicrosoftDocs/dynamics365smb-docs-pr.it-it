---
title: Impostare contenuto specifico del documento e allegati per i messaggi e-mail | Documenti Microsoft
description: "È possibile definire il contenuto da inserire nel corpo di un messaggio e-mail, ad esempio, un collegamento a PayPal. È anche possibile collegare documenti ai messaggi e-mail."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, mail, Office 365, cover, body, PayPal, layout
ms.date: 03/30/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 445982644c7491df2090b56b0a7ce3e7277c4a57
ms.contentlocale: it-it
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-send-documents-by-email"></a>Procedura: Inviare documenti via e-mail
Per comunicare rapidamente i contenuti dei documenti aziendali ai partner commerciali, quali le informazioni sui pagamenti nei documenti di vendita ai clienti, è possibile utilizzare la funzionalità di layout del report per definire il contenuto specifico del documento che deve essere inserito nel corpo e-mail automaticamente. Per ulteriori informazioni, vedere [Gestione dei layout dei report e dei documenti](ui-manage-report-layouts.md).

Per abilitare i messaggi e-mail dall'interno di [!INCLUDE[d365fin](includes/d365fin_md.md)], avviare il setup assistito **Imposta indirizzo e-mail** nella home page.

È possibile inviare tramite e-mail praticamente tutti i tipi di documento come allegati ai messaggi e-mail direttamente dalla finestra che mostra il documento. Oltre all'allegato, è possibile impostare corpi e-mail specifici per il documento con le informazioni di base estratte dal documento, precedute da un testo standard di saluto e di introduzione al documento in questione. Per offrire ai clienti di pagare elettronicamente gli articoli acquistati utilizzando un servizio di pagamento come PayPal, è possibile inserire nel corpo e-mail anche le informazioni su PayPal e il collegamento ipertestuale di PayPal.

Da tutti i documenti supportati, avviare l'invio tramite e-mail scegliendo l'azione **Invia**, nei documenti registrati, o l'azione **Registra e invia** nei documenti non registrati.

Se il campo **E-mail** della finestra **Invia documento a** è impostato su **Sì (Chiedi impostazioni)**, la finestra **Invia messaggio e-mail** viene aperta con il contatto impostato nel campo **A:** e il documento allegato come file PDF. Nel campo **Corpo** è possibile immettere il testo manualmente oppure è possibile impostare il sistema in modo che il campo sia compilato con un corpo e-mail preparato specificatamente per il documento.

Nella procedura riportata di seguito viene descritto come impostare il report **Vendite - Fattura** in modo che venga utilizzato per il corpo e-mail specifico del documento quando si inviano tramite e-mail le fatture di vendita.

## <a name="to-set-up-a-document-specific-email-body-for-sales-invoices"></a>Per impostare un corpo e-mail specifico del documento per le fatture di vendita
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Selezioni report Vendite**, quindi scegliere il collegamento correlato.
2. Nella finestra **Selezione report - Vendite**, nel campo **Utilizzo**, selezionare **Fattura**.
3. In una nuova riga nel campo **ID report** selezionare ad esempio il report standard 1306.
4. Selezionare la casella di controllo **Utilizza per corpo e-mail**.
5. Scegliere il campo **Codice layout corpo e-mail** e selezionare un layout dall'elenco a discesa.

    I layout dei report definiscono lo stile e il contenuto del corpo e-mail, incluso il testo standard che precede le informazioni principali del documento nel corpo e-mail. Per visualizzare tutti i layout dei report disponibili scegliendo il pulsante **Seleziona da elenco completo** nell'elenco a discesa.
6. Per visualizzare o modificare il layout su cui si basa il corpo e-mail, selezionare il layout nella finestra **Layout report personalizzati** e scegliere l'azione **Modifica layout**.
7. Se si desidera offrire ai clienti la possibilità di pagare elettronicamente gli articoli acquistati, è possibile configurare il servizio di pagamento correlato, come PayPal, inserire nel corpo e-mail anche le informazioni su PayPal e il collegamento ipertestuale a PayPal. Per ulteriori informazioni, vedere [Procedura: Abilitare i pagamenti clienti attraverso PayPal](sales-how-enable-payment-service-extensions.md).
8. Scegliere il pulsante **OK**.

A questo punto, quando si sceglie ad esempio l'azione **Invia** nella finestra **Fattura vendita registrata**, il corpo e-mail conterrà le informazioni del report 1306 precedute dal testo standard creato in base al layout di report selezionato nel passaggio 5.

Nella procedura riportata di seguito viene descritto come inviare una fattura di vendita registrata come messaggio e-mail con il documento allegato come file PDF e con il corpo e-mail specifico del documento.

## <a name="to-send-documents-by-email"></a>Per inviare i documenti tramite e-mail
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Fatture di vendita registrate** e quindi scegliere il collegamento correlato.
2. Selezionare la fattura di vendita registrata appropriata, quindi scegliere l'azione **Invia**. Verrà visualizzata la finestra **Invia documento a**.
3. Nel campo **E-mail** selezionare **Sì (Chiedi impostazioni)**. Per ulteriori informazioni, vedere [Procedura: Impostare profili di invio documenti](sales-how-setup-document-send-profiles.md).
4. Scegliere il pulsante **OK**. Verrà visualizzata la finestra **Invia messaggio e-mail**.
5. Nel campo **A:** immettere un indirizzo e-mail valido. Il valore predefinito è l'indirizzo e-mail del cliente.
6. Nel campo **Oggetto**, immettere un testo descrittivo dell'oggetto. Il valore predefinito è il nome e il numero di fattura del cliente.
7. Nel campo **Allegato** la fattura generata viene allegata per impostazione predefinita come file PDF. Scegliere il pulsante di ricerca per aprire il file o per allegarne un altro.
8. Nel campo **Corpo**, immettere un breve messaggio per il destinatario.

    Se il corpo e-mail specifico del documento è impostato nella finestra **Selezione report - Vendite**, il campo **Corpo** viene compilato automaticamente. Per ulteriori informazioni, vedere la sezione "Per impostare un corpo e-mail specifico del documento per le fatture di vendita" in questo argomento.
9. Scegliere **OK** per inviare il messaggio e-mail.

> [!NOTE]  
>   Se non si desidera specificare le impostazioni dell'e-mail ogni volta che si invia un documento, è possibile selezionare l'opzione **Sì (Usa impostazioni di default)** nel campo **E-mail** della finestra **Invia documento a**. In questo caso, non verrà visualizzata la finestra **Invia messaggio e-mail**. Vedere il passaggio 4. Per ulteriori informazioni, vedere [Procedura: Impostare profili di invio documenti](sales-how-setup-document-send-profiles.md).

## <a name="see-also"></a>Vedi anche
[Gestione dei layout dei report e dei documenti](ui-manage-report-layouts.md)  
[Procedura: Impostare la posta elettronica](madeira-how-setup-email.md)  
[Procedura: Fatturare le vendite](sales-how-invoice-sales.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

