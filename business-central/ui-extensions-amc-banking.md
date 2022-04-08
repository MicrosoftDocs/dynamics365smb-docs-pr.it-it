---
title: Utilizzo dell'estensione AMC Banking 365 Fundamentals
description: Scopri come scambiare con facilità i dati con le banche trasformando i dati nel formato richiesto.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: bank, format, data
ms.date: 06/23/2021
ms.author: bholtorf
ms.openlocfilehash: ec7ba151f94a7209e81f8e695b3053885d0fcc24
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2022
ms.locfileid: "8510534"
---
# <a name="use-the-amc-banking-365-fundamentals-extension"></a>Utilizzare l'estensione AMC Banking 365 Fundamentals
L'estensione AMC Banking 365 Fundamentals rende più semplice e preciso l'invio di dati alle banche. L'estensione connette [!INCLUDE[prod_short](includes/prod_short.md)] con AMC Banking 365 Fundamentals per Microsoft Dynamics 365 Business Central, che può convertire i dati bancari da [!INCLUDE[prod_short](includes/prod_short.md)] nei formati richiesti da oltre 600 banche in tutto il mondo. Ciò rende ad esempio più semplice il trasferimento di pagamenti e crediti ai fornitori immettendo i pagamenti in [!INCLUDE[prod_short](includes/prod_short.md)]e quindi caricandoli nella banca. I formati possono anche facilitare i processi di riconciliazione bancaria. Per ulteriori informazioni, vedere [AMC Banking per Microsoft Dynamics 365 Business Central](https://www.amcbanking.com/bc-fundamentals/).

> [!Note]
> AMC Banking ha creato estensioni aggiuntive che funzionano con [!INCLUDE[prod_short](includes/prod_short.md)]. Questo argomento descrive solo l'estensione Fundamentals.

> [!NOTE]
> Nella versione generica di [!INCLUDE[prod_short](includes/prod_short.md)], viene installato e connesso un provider di servizi globale per convertire i dati bancari in qualsiasi formato di file richiesto dalla banca. Nelle versioni per il Nord America, lo stesso servizio può essere utilizzato per inviare file di pagamento come trasferimento elettronico di fondi (EFT), ad esempio la rete ACH (Automated Clearing House) comunemente utilizzata, tuttavia con un processo leggermente diverso.

## <a name="use-our-demonstration-account"></a>Utilizzare l'account dimostrativo
[!INCLUDE[prod_short](includes/prod_short.md)] viene fornito con un account dimostrativo che consente di provare l'estensione AMC Banking 365 Fundamentals. Vengono fornite le impostazioni predefinite per la connessione a AMC Banking, specificando i conti correnti bancari per ottenere i dati da [!INCLUDE[prod_short](includes/prod_short.md)], oltre ad alcune definizioni di scambio dati. È possibile visualizzare le impostazioni di connessione nella pagina **Setup AMC Banking**. Per i conti correnti bancari, l'estensione applica i valori nei campi **Nome banca**, **Nr. messaggi bonifico**, **Formato importazione rendiconto bancario** e **Formato esportazione pagamento** sulle carte del conto corrente bancario.

Sebbene le impostazioni vengano fornite in automatico, per provare l'estensione è necessario eseguire la guida al setup assistito per applicarle. Per eseguire la guida, nella pagina **Setup AMC Banking** scegliere l'azione **Setup assistito**.

> [!Note]
> Esistono alcune limitazioni sull'account demo. Ad esempio, quando si convertono i pagamenti, l'importo nel file convertito non corrisponderà all'importo effettivo. L'importo sarà invece sempre costituito da cinque unità della valuta utilizzata per i pagamenti.  

## <a name="setting-up-the-extension"></a>Impostazione dell'estensione
Per iniziare a usare l'estensione sono necessari pochi semplici passaggi e una guida al setup assistito eseguirà la configurazione e attiverà l'estensione. La guida eseguirà operazioni come l'installazione delle definizione di scambio dati per i setup di esportazione/importazione degli estratti conto bancari e l'avvio delle numerazioni utilizzate per i messaggi di bonifico.  

### <a name="to-set-up-the-required-permission-sets"></a>Per impostare i set di autorizzazioni richiesti
Prima che le persone possano utilizzare questa estensione, l'amministratore deve copiare i seguenti set di autorizzazioni, modificarli e quindi assegnare agli utenti i nuovi set di autorizzazioni anziché gli originali:

* **D365 Basic**
* **D365 Team Member**
* **D365 Read**
* **IntelligentCloudBC**

Per ulteriori informazioni, vedere [Per copiare un set di autorizzazioni](ui-define-granular-permissions.md#to-copy-a-permission-set).

Per ogni nuovo set di autorizzazioni, concedere solo l'autorizzazione **Read** per **Tabella setup AMC Banking (20101)**. Per ulteriori informazioni, vedere [Per creare o modificare le autorizzazioni manualmente](ui-define-granular-permissions.md#to-create-or-modify-permissions-manually).

### <a name="to-connect-the-extension-to-amc-banking"></a>Per collegare l'estensione a AMC Banking
1. Ottenere un modulo e un piano di servizio per AMC Banking. A tale scopo, visitare la pagina [AMC License](https://license.amcbanking.com/register).
2. In [!INCLUDE[prod_short](includes/prod_short.md)], scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup AMC Banking**, quindi scegli il collegamento correlato.  
3. Nella pagina **Setup AMC Banking** scegliere l'azione **Setup assistito**.
4. Completare i passaggi nella guida di setup assistito.

### <a name="to-connect-bank-accounts-to-the-extension"></a>Per collegare i conti correnti bancari all'estensione
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **C/C bancari**, quindi scegli il collegamento correlato.
2. Aprire la scheda per il conto corrente bancario che si desidera collegare al servizio.
3. Nel campo **Nome banca** scegliere il formato richiesto dalla banca.  

   I formati vengono filtrati per mostrare solo quelli rilevanti per il paese specificato per il conto corrente bancario.
4. Nel campo **Nr. messaggi bonifico** selezionare le numerazioni da utilizzare per i messaggi che accompagnano i pagamenti.
5. Nel campo **Formato importazione rendiconto bancario** e **Formato esportazione pagamento** scegliere le definizioni di scambio dati richieste dalla banca.

## <a name="use-the-extension"></a>Utilizzare l'estensione
L'uso di questa estensione è solo per l'esportazione dei dati nella pagina **Registrazioni pagamenti** e per il successivo caricamento sul servizio Web della banca. Per ulteriori informazioni, vedere [Effettuare i pagamenti con servizio di conversione di dati bancari o bonifico SEPA](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md).

> [!Note]
> È necessario compilare i campi **Codice SWIFT** e **IBAN** per ciascun conto corrente bancario.

### <a name="to-export-data-and-submit-it-to-your-bank"></a>Per esportare i dati e inviarli alla banca
> [!CAUTION]  
>  Quando si esportano dati tramite l'estensione AMC Banking 365 Fundamentals alcuni dei dati aziendali verranno esposti al provider del servizio. Il provider di servizi, AMC Consult A/S, è responsabile per la privacy di questi dati. Per maggiori informazioni, vedere [Informativa sulla privacy di AMC](https://go.microsoft.com/fwlink/?LinkId=510158).

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registrazioni pagamenti**, quindi scegli il collegamento correlato.
2. Creare le righe di registrazione che si desidera esportare.  

   > [!Note]
   > Per ogni riga, ricordarsi di scegliere **Pagamento elettronico** nel campo **Tipo pagamento banca**.
3. Scegliere l'azione **Esporta**.

### <a name="to-import-and-apply-the-converted-file"></a>Per importare e applicare il file convertito
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registrazione riconciliazione pagamenti**, quindi scegli il collegamento correlato.
2. Scegliere l'azione **Importa transazioni bancarie**, quindi scegliere il file convertito.  

   [!INCLUDE[prod_short](includes/prod_short.md)] creerà una nuova registrazione riconciliazione pagamenti che contiene i dati nel file. Per ulteriori informazioni, vedere [Collegare i pagamenti automaticamente e riconciliare i conti correnti bancari](receivables-apply-payments-auto-reconcile-bank-accounts.md).

## <a name="see-also"></a>Vedere anche
[Personalizzazione di [!INCLUDE[prod_short](includes/prod_short.md)] utilizzando le estensioni](ui-extensions.md)  
[Preparazione al business](ui-get-ready-business.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]