---
title: Impostare contenuto e-mail specifico del documento | Documenti di Microsoft
description: È possibile definire il contenuto da inserire nel corpo di un messaggio e-mail, ad esempio, un collegamento a PayPal. È anche possibile collegare documenti ai messaggi e-mail.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.workload: na
ms.search.keywords: SMTP, mail, Office 365, cover, body, PayPal, layout
ms.date: 05/13/2020
ms.author: edupont
ms.openlocfilehash: d80b76614ad0ddf901a288859d8e6595d908c7ae
ms.sourcegitcommit: 3e9c89f90db5eaed599630299353300621fe4007
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/01/2020
ms.locfileid: "3527987"
---
# <a name="send-documents-by-email"></a>Inviare documenti via e-mail

Per comunicare rapidamente i contenuti dei documenti aziendali ai partner commerciali, quali le informazioni sui pagamenti nei documenti di vendita ai clienti, è possibile utilizzare la funzionalità di layout di report per definire il contenuto specifico del documento che deve essere inserito nel corpo e-mail automaticamente. Per ulteriori informazioni, vedere [Gestione dei layout di report e documento](ui-manage-report-layouts.md).

Per abilitare i messaggi e-mail dall'interno di [!INCLUDE[d365fin](includes/d365fin_md.md)], avviare la guida al setup assistito **Imposta indirizzo e-mail** nella Gestione ruolo utente.

È possibile inviare tramite e-mail praticamente tutti i tipi di documento come allegati ai messaggi e-mail direttamente dalla pagina che mostra il documento. Oltre all'allegato, è possibile impostare corpi e-mail specifici per il documento con le informazioni di base estratte dal documento, precedute da un testo standard di saluto e di introduzione al documento in questione. Per offrire ai clienti di pagare elettronicamente gli articoli acquistati utilizzando un servizio di pagamento come PayPal, è possibile inserire nel corpo e-mail anche le informazioni su PayPal e il collegamento ipertestuale di PayPal.

Da tutti i documenti supportati, avviare l'invio tramite e-mail scegliendo l'azione **Invia**, nei documenti registrati, o l'azione **Registra e invia** nei documenti non registrati.

Se il campo **E-mail** della pagina **Invia documento a** è impostato su **Sì (Chiedi impostazioni)**, la pagina **Invia messaggio e-mail** viene aperta con il contatto impostato nel campo **A:** e il documento allegato come file PDF. Nel campo **Corpo** è possibile immettere il testo manualmente oppure è possibile impostare il sistema in modo che il campo sia compilato con un corpo e-mail preparato specificatamente per il documento.

Nella procedura riportata di seguito viene descritto come impostare il report **Vendite - Fattura** in modo che venga utilizzato per il corpo e-mail specifico del documento quando si inviano tramite e-mail le fatture di vendita.

## <a name="to-set-up-a-document-specific-email-body-for-sales-invoices"></a>Per impostare un corpo e-mail specifico del documento per le fatture di vendita

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Selezioni report Vendite** e quindi scegliere il collegamento correlato.
2. Nella pagina **Selezione report - Vendite**, nel campo **Utilizzo**, selezionare **Fattura**.
3. In una nuova riga nel campo **ID report** selezionare ad esempio il report standard 1306.
4. Selezionare la casella di controllo **Utilizza per corpo e-mail**.
5. Scegliere il campo **Codice layout corpo e-mail** e selezionare un layout dall'elenco a discesa.

    I layout di report definiscono lo stile e il contenuto del corpo e-mail, incluso il testo standard che precede le informazioni principali del documento nel corpo e-mail. Per visualizzare tutti i layout di report disponibili scegliendo il pulsante **Seleziona da elenco completo** nell'elenco a discesa.
6. Per visualizzare o modificare il layout su cui si basa il corpo e-mail, selezionare il layout nella pagina **Layout report personalizzati** e scegliere l'azione **Modifica layout**.
7. Se si desidera offrire ai clienti la possibilità di pagare elettronicamente gli articoli acquistati, è possibile configurare il servizio di pagamento correlato, come PayPal, inserire nel corpo e-mail anche le informazioni su PayPal e il collegamento ipertestuale a PayPal. Per ulteriori informazioni, vedere [Abilitare i pagamenti clienti attraverso PayPal](sales-how-enable-payment-service-extensions.md).
8. Scegliere il pulsante **OK**.

A questo punto, quando si sceglie ad esempio l'azione **Invia** nella pagina **Fattura vendita registrata**, il corpo e-mail conterrà le informazioni del report 1306 precedute dal testo standard creato in base al layout di report selezionato nel passaggio 5.

Nella procedura riportata di seguito viene descritto come inviare una fattura di vendita registrata come messaggio e-mail con il documento allegato come file PDF e con il corpo e-mail specifico del documento.

## <a name="to-send-documents-by-email"></a>Per inviare i documenti tramite e-mail

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), quindi immettere **Fatture di vendita registrate** e scegliere il collegamento correlato.
2. Selezionare la fattura di vendita registrata appropriata, quindi scegliere l'azione **Invia**. Verrà visualizzata la pagina **Invia documento a**.
3. Nel campo **E-mail** selezionare **Sì (Chiedi impostazioni)**. Per ulteriori informazioni, vedere [Impostare profili di invio documenti](sales-how-setup-document-send-profiles.md).
4. Scegliere il pulsante **OK**. Verrà visualizzata la pagina **Invia messaggio e-mail**.
5. Nel campo **A:** immettere un indirizzo e-mail valido. Il valore di default è l'indirizzo e-mail del cliente.
6. Nel campo **Oggetto**, immettere un testo descrittivo dell'oggetto. Il valore di default è il nome e il numero di fattura del cliente.
7. Nel campo **Allegato** la fattura generata viene allegata per impostazione di default come file PDF.
8. Nel campo **Corpo**, immettere un breve messaggio per il destinatario.

    Se il corpo e-mail specifico del documento è impostato nella pagina **Selezione report - Vendite**, il campo **Corpo** viene compilato automaticamente. Per ulteriori informazioni, vedere [Per impostare un corpo e-mail specifico del documento per le fatture di vendita](ui-how-send-documents-email.md#to-set-up-a-document-specific-email-body-for-sales-invoices).
9. Scegliere **OK** per inviare il messaggio e-mail.

> [!NOTE]  
> Se non si desidera specificare le impostazioni dell'e-mail ogni volta che si invia un documento, è possibile selezionare l'opzione **Sì (Usa impostazioni di default)** nel campo **E-mail** della pagina **Invia documento a**. In questo caso, non verrà visualizzata la pagina **Invia messaggio e-mail**. Vedere il passaggio 4. Per ulteriori informazioni, vedere [Impostare profili di invio documenti](sales-how-setup-document-send-profiles.md).  

## <a name="documents-marked-as-printed-when-they-are-sent"></a>Documenti contrassegnati come stampati al momento dell'invio

Alcuni documenti in [!INCLUDE[prodshort](includes/prodshort.md)] hanno un campo che specifica quante volte quel documento è stato stampato. Il campo viene aggiornato anche se non si stampa il documento ma lo si invia tramite e-mail. Il campo viene aggiornato anche se non si invia effettivamente il documento, ad esempio quando l'organizzazione non ha impostato la posta elettronica o quando il contatto a cui si desidera inviare il documento non ha un indirizzo di posta elettronica elencato. In tutti gli scenari, per quanto riguarda [!INCLUDE[prodshort](includes/prodshort.md)], il documento viene stampato perché viene generato un file PDF.  

L'utente potrebbe non vedere questo file generato, ma è per questo che il campo è stato aggiornato.

## <a name="see-also"></a>Vedere anche

[Gestione dei layout di report e documento](ui-manage-report-layouts.md)  
[Impostare la posta elettronica](admin-how-setup-email.md)  
[Fatturare le vendite](sales-how-invoice-sales.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
