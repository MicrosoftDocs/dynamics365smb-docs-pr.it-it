---
title: Impostare il connettore Documenti elettronici con endpoint esterni
description: Questo articolo spiega come configurare la funzionalità dei documenti elettronici quando è connessa a endpoint esterni.
author: altotovi
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, electronic invoice, e-document, e-invoice, access-point, endpoint'
ms.search.form: '359, 360, 6103, 6133'
ms.date: 12/13/2023
ms.author: altotovi
---

# <a name="set-the-e-documents-connector-with-external-endpoints"></a>Impostare il connettore Documenti elettronici con endpoint esterni

Questo articolo spiega come configurare la funzionalità dei documenti elettronici quando è connessa a endpoint esterni.

Prima di utilizzare la funzionalità descritta in questo articolo, installa l'app **Connettore Documenti elettronici con endpoint esterni** nella parte superiore dell'app globale **Documento elettronico di base**. Questa app può essere utilizzata per l'integrazione predefinita con punti di accesso esterni (di terze parti) per automatizzare il flusso di documenti elettronici. Poiché questa app rappresenta solo alcuni dei connettori selezionati, non sei limitato alle integrazioni esistenti al suo interno. La maggior parte dei connettori sarà disponibile su AppSource in futuro.

## <a name="set-up-the-connection"></a>Configurare la connessione

Per iniziare la configurazione, segui i passaggi in [Documento elettronico di base](finance-how-setup-edocuments.md). Dopo aver completato questi passaggi, torna a questo articolo e completa i seguenti passaggi:

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immetti **Servizi documenti elettronici**, quindi seleziona il collegamento correlato.
2. Nel campo **Integrazione servizio**, seleziona uno dei codici di integrazione offerti per la configurazione del servizio endpoint.
3. Seleziona **Setup integrazione del servizio**.
4. Nella pagina **Impostazione connessione esterna documento elettronico**, seleziona **Richiedi codice autorizzazione**. Verrai reindirizzato alla pagina Web di autorizzazione del servizio esterno e ti verranno richiesti i dettagli di accesso.
5. Copia il codice di autorizzazione nel campo **Inserisci codice autorizzazione**.
6. Seleziona **Aggiorna token di accesso** per assicurarti di poter aggiornare il token.

    > [!NOTE]
    > Questa connessione richiede la comunicazione con fornitori di servizi esterni che potrebbero essere soggetti a pagamenti aggiuntivi e richiedono contratti con loro. Per ottenere tutte le credenziali necessarie, contatta i fornitori di servizi.

7. Nella pagina  **Impostazione connessione esterna documento elettronico**, compila i seguenti campi:

    | Nome campo | Descrizione |
    |---|---|
    | URL API file | Specifica l'URL dell'API del file. |
    | URL file part | Specifica l'URL dei file part. |
    | URL API documento | Specifica l'URL dell'API del documento. |
    | ID società | Specifica l'ID società. |
    | Modalità di invio | Specificare la modalità di invio. È possibile selezionare **Produzione**, **Test** o **Certificazione**. |

    > [!NOTE]
    > Chiedi al tuo fornitore di servizi tutti i dettagli precedenti per stabilire una connessione con il suo punto di accesso.

## <a name="set-up-company-information"></a>Impostare le informazioni sulla società

Prima di iniziare a utilizzare i documenti elettronici, aggiorna la pagina **Informazioni società** completando i seguenti passaggi:

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](media/ui-search/search_small.png "Dimmi cosa vuoi fare"), immetti **Informazioni società**, quindi seleziona il collegamento correlato.
2. Oltre a compilare i soliti campi è necessario compilare anche i seguenti campi:

    | Nome campo | Descrizione |
    |---|---|
    | Codice SWIFT | Specifica il codice SWIFT (codice di identificazione internazionale) della banca principale. |
    | Nr. filiale banca | Specifica il numero della filiale della banca a quattro cifre. |
    | Partita IVA | Specifica la partita IVA della società. |

3. Chiudere la pagina.

## <a name="set-up-customers-to-receive-e-documents"></a>Configurare i clienti per ricevere documenti elettronici

Per consentire ai clienti di ricevere i tuoi documenti elettronici, completa i seguenti passaggi:

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](media/ui-search/search_small.png "Dimmi cosa vuoi fare"), immetti **Clienti**, quindi seleziona il collegamento correlato.
2. Apri la scheda **Cliente**.
3. Oltre a compilare i campi consueti, nel campo **GLN**, specifica il cliente in relazione all'invio di documenti elettronici.
4. Contrassegna il campo **Usa GLN in documenti elettronici** per indicare se il Global Location Number (GLN) viene utilizzato come numero di identificazione della parte nei documenti elettronici.
5. Chiudere la pagina.

## <a name="other-setup"></a>Altre configurazioni

Prima di iniziare a lavorare con i documenti elettronici, imposta i **flussi di lavoro** dei documenti lettronici e i **profili di invio dei documenti** per utilizzare i tuoi flussi di lavoro. Dopo aver stabilito la connessione al servizio, puoi iniziare a utilizzare la tua soluzione di documenti elettronici.

## <a name="available-service-providers"></a>Provider di servizio disponibili

Microsoft desidera incoraggiare i fornitori di punti di accesso ad aggiungere i propri connettori al framework **Documento elettronico di base**.

Attualmente Pagero è l'unico fornitore di punti di accesso coperto da questo sistema. Microsoft non ha alcun obbligo contrattuale con Pagero. Pertanto, è necessario stipulare un contratto con loro per ottenere tutte le credenziali necessarie.

Aggiorneremo questo elenco non appena avremo nuovi fornitori di punti di accesso per lo scambio di documenti elettronici.

## <a name="see-also"></a>Vedere anche

[Come impostare documenti elettronici in Business Central](finance-how-setup-edocuments.md)  
[Come utilizzare documenti elettronici in Business Central](finance-how-use-edocuments.md)  
[Come estendere documenti elettronici in Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments)  
[Gestione contabile](finance.md)  
[Fatturazione delle vendite](sales-how-invoice-sales.md)  
[Registrare gli acquisti con le fatture e gli ordini di acquisto](purchasing-how-record-purchases.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
