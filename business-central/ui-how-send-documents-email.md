---
title: Inviare documenti ed e-mail
description: È possibile definire il contenuto da inserire nel corpo di un messaggio e-mail, ad esempio, un collegamento a PayPal. È anche possibile collegare documenti ai messaggi e-mail.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.workload: na
ms.search.keywords: SMTP, mail, Microsoft 365, cover, body, PayPal, layout
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 3322199feee09c656b01c7723a8c95396015cde4
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2021
ms.locfileid: "7588453"
---
# <a name="send-documents-and-emails"></a>Inviare documenti ed e-mail

È possibile condividere facilmente informazioni e documenti, come ordini di vendita e di acquisto e fatture, via e-mail direttamente da [!INCLUDE[prod_short](includes/prod_short.md)], senza dover aprire un'applicazione di posta elettronica.  

È possibile inviare quasi tutti i tipi di documenti come allegati PDF. In alternativa, è possibile impostare un layout di report che include le informazioni del documento nel testo del messaggio di posta elettronica, insieme al testo che rende il messaggio di posta elettronica più semplice, ad esempio un saluto standard. Per ulteriori informazioni, vedere [Gestione dei layout di report e documento](ui-manage-report-layouts.md). <!--this topic does not mention how to set up a layout for email. Need to investigate.-->

Quando si inviano fatture, è possibile semplificare i pagamenti per i clienti tramite un servizio di pagamento, come PayPal, aggiungendo automaticamente informazioni e un collegamento al servizio nell'e-mail. Per ulteriori informazioni, vedere [Abilitare i pagamenti clienti tramite i servizi di pagamento](sales-how-enable-payment-service-extensions.md).

Per abilitare i messaggi e-mail da [!INCLUDE[prod_short](includes/prod_short.md)], avviare la guida al setup assistito **Configurare la posta elettronica**. Per ulteriori informazioni, vedere [Configurare la posta elettronica](admin-how-setup-email.md).

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] supporta solo comunicazioni via e-mail in uscita. Non è inoltre possibile ricevere risposte dall'app.

## <a name="to-send-documents-by-email"></a>Per inviare i documenti tramite e-mail

Questa procedura descrive come associare una fattura vendita registrata a un'e-mail come file PDF e con il testo dell'e-mail specifico del documento. <!--update this-->

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Fatture vendite registrate**, quindi seleziona il collegamento correlato.
2. Seleziona la fattura, scegli l'azione **Stampa/Invia** e poi scegli **Invia**.
3. Nel campo **E-mail** selezionare **Sì (Chiedi impostazioni)**. Per ulteriori informazioni, vedere [Impostare profili di invio documenti](sales-how-setup-document-send-profiles.md).
    
    Se il campo **E-mail** della pagina **Invia documento a** è impostato su **Sì (Chiedi impostazioni)**, la pagina **Invia messaggio e-mail** viene aperta con il contatto impostato nel campo **A:** e il documento allegato come file PDF. Nel campo **Corpo** è possibile immettere il testo manualmente oppure è possibile impostare il sistema in modo che il campo sia compilato con un corpo e-mail preparato specificatamente per il documento.

4. Scegliere il pulsante **OK**.
5. Nel campo **A:** immettere un indirizzo e-mail valido. Il valore di default è l'indirizzo e-mail del cliente.
6. Nel campo **Oggetto**, immettere un testo descrittivo dell'oggetto. Il valore di default è il nome e il numero di fattura del cliente.
7. Nel campo **Allegato** la fattura generata viene allegata per impostazione di default come file PDF.
8. Nel campo **Corpo**, immettere un breve messaggio per il destinatario.

    Se il testo e-mail specifico del documento è impostato nella pagina **Selezione report - Vendite**, il campo **Corpo** viene compilato automaticamente. Per ulteriori informazioni, [Impostare testi e layout e-mail riutilizzabili per documenti vendita e acquisto](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts-for-sales-and-purchase-documents).
9. Scegliere **OK** per inviare il messaggio e-mail.

> [!NOTE]  
> Se non si desidera specificare le impostazioni dell'e-mail ogni volta che si invia un documento, è possibile selezionare l'opzione **Sì (Usa impostazioni di default)** nel campo **E-mail** della pagina **Invia documento a**. In questo caso, non verrà visualizzata la pagina **Invia messaggio e-mail**. Vedere il passaggio 4. Per ulteriori informazioni, vedere [Impostare i profili di invio dei documenti](sales-how-setup-document-send-profiles.md).  

## <a name="to-compose-and-send-an-email"></a>Per comporre e inviare un'e-mail
È possibile comporre rapidamente e-mail per contatti, clienti, venditori, venditori/acquirenti e conti bancari direttamente dalle pagine per queste entità. Basta scegliere **Processo** e poi **Invia e-mail** per aprire l'editor di e-mail. Per i conti bancari, l'azione **Invia email** è sotto **Azioni**.

> [!TIP]
> Se si inviano spesso messaggi di posta elettronica di natura simile, o si vuole inviare una comunicazione di massa, ad esempio, per pubblicizzare una campagna di vendita, l'uso di modelli di Word con le e-mail può accelerare il processo. È possibile creare un modello per entità come clienti, fornitori e contatti, che genererà il contenuto di un messaggio e-mail per voi, e anche personalizzare il contenuto per il destinatario in base ai dati in [!INCLUDE[prod_short](includes/prod_short.md)]. Per maggiori informazioni, vedi [Usare i modelli di Word per le comunicazioni di massa](ui-mail-merge.md).  

## <a name="documents-marked-as-printed-when-they-are-sent"></a>Documenti contrassegnati come stampati al momento dell'invio

Alcuni documenti in [!INCLUDE[prod_short](includes/prod_short.md)] hanno un campo che specifica quante volte quel documento è stato stampato. Il numero in quel campo <!--"that field?" need a name...--> viene aggiornato anche se si invia il documento tramite posta elettronica poiché viene generato un file PDF per lo stesso. Il numero viene aggiornato anche se non invii l'e-mail. <!--guessing this is because emails are technically reports, so the counter bumps up whenever someone creates an email. Need to verify.-->

## <a name="sent-emails-and-your-email-outbox"></a>E-mail inviate e posta in uscita

[!INCLUDE[prod_short](includes/prod_short.md)] memorizza le e-mail inviate nella pagina **Elementi inviati**. Questo per consentire di inviare nuovamente le e-mail o inoltrarle a qualcun altro. Se non si riesce a trovare un'e-mail negli elementi inviati, cercarla nella pagina **Posta in uscita**. 

> [!NOTE]
> A seconda dell'utilizzo della posta elettronica da parte della società, gli amministratori possono visualizzare un elenco di messaggi inviati da tutti, ma non il contenuto dei messaggi

La **Posta in uscita** è dove si trovano le e-mail salvate come bozze e le e-mail che non è stato possibile inviare, ad esempio, se l'indirizzo email non era valido. Per i messaggi che non sono stati inviati, è possibile scegliere **Mostra errore** o **Analizza errore** per risolvere il problema.  

## <a name="see-related-training-at-microsoft-learn"></a>Vedi le informazioni relative al training in [Microsoft Learn](/learn/modules/set-up-email/)

## <a name="see-also"></a>Vedere anche

[Gestione dei layout di report e documenti](ui-manage-report-layouts.md)  
[Configurare la posta elettronica](admin-how-setup-email.md)  
[Fatturare le vendite](sales-how-invoice-sales.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
