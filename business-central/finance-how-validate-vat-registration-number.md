---
title: Convalidare i numero di partita IVA
description: 'Consenti a Business Central di convalidare i numeri di partita IVA per i contatti, i clienti e i fornitori, in base al servizio di convalida dei numeri di partita IVA (VIES) dell''Unione europea.'
author: andregu
ms.topic: conceptual
ms.reviewer: edupont
ms.search.keywords: 'VAT, posting, tax, value-added tax'
ms.search.form: '249, 575, 1279'
ms.date: 06/16/2021
ms.author: andregu
---

# <a name="validate-vat-registration-numbers" />Convalidare i numero di partita IVA

È importante che le partite IVA per clienti, fornitori e contatti siano valide, qualora si utilizzi [!INCLUDE [prod_short](includes/prod_short.md)] in un paese che utilizza l'IVA. Ad esempio, le società cambiano talvolta lo stato di passività fiscale e in alcuni paesi le autorità fiscali potrebbero chiedere di fornire report, come il report **Lista vendite UE**, che elenca i numeri di partita IVA utilizzati per l'attività.

La Commissione Europea offre un servizio di convalida dei numeri di partita IVA (VIES) tramite il proprio sito Web, che è pubblico e libero. [!INCLUDE [prod_short](includes/prod_short.md)] consente di risparmiare un passaggio e di utilizzare il servizio VIES per convalidare e tracciare i numeri IVA e altre informazioni sulla società per i clienti, i fornitori e i contatti. Il servizio in [!INCLUDE [prod_short](includes/prod_short.md)] è denominato **servizio di convalida partita IVA comunitaria**. Il servizio è disponibile nella pagina **Connessioni servizio** e sarà possibile iniziare a utilizzarlo da subito. La connessione del servizio è gratuita e l'ulteriore registrazione non è necessaria.

## <a name="configure-the-service-to-verify-vat-registration-numbers-automatically" />Configurare il servizio per verificare automaticamente i numeri di partita IVA

Per abilitare **Setup servizio di convalida partita IVA comunitaria**, aprire la voce nella pagina **Connessione servizio**. Se il campo **Endpoint servizio** non è ancora compilato, utilizzare l'azione **Imposta endpoint di default**. Impostare quindi il campo **Abilitato** e sarà possibile proseguire.  

> [!IMPORTANT]
> Per abilitare il servizio di convalida, è necessario disporre di autorizzazioni di amministratore.

Facoltativamente, impostare i modelli per i tipi di dati relativi all'IVA che si desidera vengano controllati dal servizio. Per ulteriori informazioni, vedere la sezione [Modelli di convalida](#validation-templates).

Quando si utilizza la connessione del servizio, viene registrata una cronologia dei numeri di partita IVA e delle verifiche per ogni cliente, fornitore o contatto, nel **Log partita IVA**, in modo da poterli facilmente tracciare. Il log è specifico per ogni cliente. Ad esempio, il log è utile per dimostrare di aver verificato che il numero di partita IVA corrente è corretto. Quando si verifica un numero di partita IVA, la colonna **Identificatore di richiesta** nel log indicherà che l'azione è stata eseguita.

È possibile visualizzare il log di registrazione IVA nella scheda cliente, fornitore o di contatto, nella Scheda dettaglio **Fatturazione**, scegliendo il pulsante di ricerca nel campo **Partita IVA**.  

Ci sono un paio di cose da notare sul servizio di convalida dei numeri di partita IVA VIES:

* Il servizio Web utilizza il protocollo HTTP, il che significa che i dati trasferiti tramite il servizio non sono crittografati.  
* È possibile che si verifichi un tempo di inattività per questo servizio per cui Microsoft non è responsabile. Il servizio fa parte di un'ampia rete europea di registri IVA nazionali.

> [!IMPORTANT]
> È responsabilità dell'utente verificare che i dati siano validi. A volte, i dati con errori vengono restituiti dal servizio di convalida dei numeri di partita IVA VIES. Se la convalida non riesce, convalidare i numeri di partita IVA nel [sito Web](https://ec.europa.eu/taxation_customs/vies/), stampare il risultato o salvarlo in una posizione condivisa, quindi aggiungere il collegamento al record per il cliente, il fornitore o il contatto. Per ulteriori informazioni, vedere [Gestire allegati, collegamenti e note in schede e documenti](ui-how-add-link-to-record.md).

## <a name="validation-templates" />Modelli di convalida

È possibile utilizzare il servizio VIES anche per controllare altre informazioni sulla società, come l'indirizzo e il numero di partita IVA. Nella pagina **Modelli convalida partita IVA** creare una voce per ogni paese per il quale si desidera ottenere un'ulteriore convalida, quindi specificare le informazioni che si desidera vengano convalidate automaticamente.  

Aggiungere ad esempio una voce per la Spagna, per cui si desidera ottenere la convalida per nome, via, città e codice postale, quindi un'altra voce per la Germania, per cui si desidera solo la convalida del codice postale. Nella pagina **Setup servizio di convalida partita IVA comunitaria** specificare quindi il modello di default.  

> [!NOTE]
> Verificare sempre che il modello di default funzioni per le esigenze specifiche. È possibile modificare l'impostazione di default in base alle esigenze, ad esempio per ottenere la convalida per tutti i campi o di nessun campo.

La volta successiva che si specifica un numero di partita IVA, il servizio convaliderà tale numero e tutti i dati aggiuntivi, come stabilito dai modelli di convalida. Se i valori specificati sono diversi da quelli restituiti dal servizio, verranno visualizzati i dettagli nella pagina **Dettagli convalida**, dove è possibile accettare o reimpostare i valori.  

## <a name="see-also" />Vedere anche

[Impostare l'IVA (imposta sul valore aggiunto)](finance-setup-vat.md)  
[Setup dell'IVA ad esigibilità differita](finance-setup-unrealized-vat.md)  
[Dichiarare l'IVA a un'autorità fiscale](finance-how-report-vat.md)  
[Utilizzare l'IVA nelle vendite e negli acquisti](finance-work-with-vat.md)  
[Funzionalità locale in Business Central](about-localization.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
