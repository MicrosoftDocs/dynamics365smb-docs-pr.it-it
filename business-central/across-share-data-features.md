---
title: Condivisione dei dati
description: Scopri i diversi modi per condividere i dati aziendali da Business Central.
author: jswymer
ms.topic: conceptual
ms.workload: na
ms.search.keywords: null
ms.date: 09/21/2022
ms.author: jswymer
---
# <a name="sharing-business-data-from-business-central" />Condivisione dei dati aziendali da Business Central

La collaborazione tra le persone all'interno e all'esterno di un'organizzazione è parte integrante della maggior parte delle aziende. [!INCLUDE[prod_short](includes/prod_short.md)] offre diverse funzionalità per la condivisione dei dati aziendali, come un elenco di record, record specifici o documenti. <!--, with others&mdash;even those people who don't have a Business Central license in some cases.-->

Con tutte queste funzionalità, l'accesso ai dati è protetto dalla licenza e dalle autorizzazioni di Business Central.

## <a name="copying-a-link" />Copia di un collegamento

![Supportata](media/check.png) Business Central Online ![Supportata](media/check.png) Business Central in locale

Da qualsiasi pagina puoi copiare l'URL della pagina, quindi incollarlo e distribuirlo in altre forme di file multimediali come e-mail, chat di Teams o SMS. Il modo più semplice per copiare un collegamento è selezionare **Condividi** > **Copia collegamento** dalla parte superiore della pagina. Un altro modo è copiare l'URL direttamente dalla casella dell'indirizzo del browser.

### <a name="modify-the-page-link" />Modificare il collegamento alla pagina

Dopo aver copiato un collegamento, prima di inviarlo, puoi modificare l'URL per manipolare ciò che viene visualizzato all'apertura della pagina. È possibile, ad esempio, aggiungere filtri o specificare un'azienda diversa.

Per ulteriori informazioni, vedi [URL del client Web](/dynamics365/business-central/dev-itpro/developer/devenv-web-client-urls).

### <a name="about-filtered-lists" />Informazioni sugli elenchi filtrati

Utilizzando il riquadro dei filtri nelle pagine elenco, è possibile applicare i filtri per limitare i record visualizzati nell'elenco. Se usi l'azione **Copia collegamento** o copi l'URL dal browser, il collegamento della pagina non includerà le modifiche al filtro. Gli utenti che aprono il collegamento vedranno la raccolta completa. Il modo per mantenere il filtro su un collegamento della pagina di raccolta consiste nel salvare la pagina filtrata come una **Visualizzazione**. Quindi, apri la visualizzazione e copia il collegamento da lì.

Per ulteriori informazioni, vedere [Ricerca, filtro e ordinamento](ui-enter-criteria-filters.md).

## <a name="sharing-to-teams" />Condivisione in Teams

![Supportata](media/check.png) Business Central Online ![Non supportato](media/x-icon.png) Business Central in locale

Direttamente dalla maggior parte delle pagine di raccolta e delle pagine dei dettagli, puoi inviare un collegamento della pagina a persone, chat di gruppo o canali. Per esempio, puoi condividere un collegamento a una visualizzazione filtrata dei tuoi record. Se hai installato l'app [!INCLUDE[prod_short](includes/prod_short.md)] per Teams, il collegamento si espanderà automaticamente in una scheda compatta da includere nel messaggio. I destinatari possono quindi selezionare il collegamento o la scheda per aprire la pagina in Business Central.

Per ulteriori informazioni, vedi [Condivisione di record e collegamenti di pagina in Teams](across-working-with-teams.md).

## <a name="sharing-through-onedrive" />Condivisione tramite OneDrive

![Supportata](media/check.png) Business Central Online ![Supportata](media/check.png) Business Central in locale

Business Central rende facile archiviare, gestire e condividere i file con altre persone attraverso OneDrive for Business. Nella maggior parte delle pagine in cui i file sono disponibili, come Report elaborati o i file allegati ai record, troverai le azioni **Apri in OneDrive** e **Condividi**. Entrambe le azioni salvano una copia di un file in OneDrive. Una volta in OneDrive, puoi utilizzare le funzioni di condivisione e contributo per il file. La differenza nelle azioni è che **Apri in OneDrive** apre il file in OneDrive. **Condividi** apre una pagina che ti permette di selezionare con chi vuoi condividere il file. I destinatari riceveranno un'e-mail di notifica per accedere al file dal tuo OneDrive.

Per ulteriori informazioni, vedi [Condivisione di file in OneDrive](across-share-onedrive.md).

## <a name="opening-in-excel" />Apertura in Excel

![Supportata](media/check.png) Business Central Online ![Supportata](media/check.png) Business Central in locale

Per le pagine elenco e gli elenchi incorporati in una pagina, è possibile utilizzare l'azione **Apri in Excel**. Questa azione esporta l'elenco di record in una cartella di lavoro di Excel (file .xlsx), che puoi condividere con altri. Nella cartella di lavoro puoi anche usare la funzionalità Condividi che fa parte di Excel.

Per ulteriori informazioni, vedi [Visualizzazione e modifica in Excel](across-work-with-excel.md).

## <a name="sharing-rows-or-tables" />Condivisione di righe o tabelle

![Supportata](media/check.png) Business Central Online ![Supportata](media/check.png) Business Central in locale

Puoi condividere uno o più record in un elenco. Basta premere i tasti di scelta rapida <kbd>CTRL</kbd>+<kbd>C</kbd> per copiare negli appunti. Quindi incolla ciò che hai copiato in un'altra applicazione premendo <kbd>CTRL</kbd>+<kbd>V</kbd>. Ad esempio, copiando tre ordini di vendita e incollandoli in un'e-mail verranno visualizzati gli ordini in una tabella ben formattata.

Per ulteriori informazioni, vedi [Domande frequenti sulla funzionalità di copia e incolla](faq-copy-paste.yml).

## <a name="see-also" />Vedere anche

[Business Central e integrazione OneDrive](across-onedrive-overview.md)  
[Gestione dell'integrazione di OneDrive con Business Central](admin-onedrive-integration.md)  
[OneDrive FAQ](admin-onedrive-faq.md)
