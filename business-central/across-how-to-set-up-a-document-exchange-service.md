---
title: Come impostare un servizio di scambio documenti | Microsoft Docs
description: Utilizzare un provider di servizi esterno per scambiare documenti elettronici con i partner commerciali.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/11/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="set-up-a-document-exchange-service"></a>Impostare un servizio di scambio documenti

Come parte del Data Exchange Framework, potete scambiare documenti di vendita e di acquisto con i vostri partner commerciali senza ulteriori passaggi, come ad esempio allegare i documenti ai messaggi e-mail come file PDF. Per esempio, quando sei pronto a fatturare un cliente, puoi pubblicare la fattura e inviarla per il pagamento come un file che il tuo cliente può ricevere nella sua applicazione di gestione aziendale. Per ulteriori informazioni, vedere [Scambio di dati in modalità elettronica](across-data-exchange.md).

> [!NOTE]
> L'impostazione di un servizio di scambio di documenti per Business Central on-premises richiede alcuni passi aggiuntivi per l'autorizzazione. Per ulteriori informazioni, vedi [Impostazioni per Business Central On-Premises](#settings-for-business-central-on-premises).

## <a name="connecting-with-trading-partners"></a>Connessione con i partner commerciali

Lo scambio di documenti elettronici richiede una connessione con i vostri partner commerciali. Per facilitare la creazione di una connessione sicura, [!INCLUDE[prod_short](includes/prod_short.md)] online è configurato per utilizzare l'applicazione Business Central Integration. L'app è disponibile su Tradeshift App Store, e tutto ciò che tu e i tuoi partner commerciali dovete fare è creare un account Tradeshift e poi abilitare l'app. L'applicazione Business Central Integration è disponibile nelle versioni di produzione e sandbox. Per esempio, usare la versione sandbox è buono per testare lo scambio di documenti. Puoi passare dalla versione di produzione a quella di sandbox attivando o disattivando il toggle **Sandbox** sul **Doc. Exch. Pagina diimpostazione del servizio** . Quando lo fai, le informazioni sulla FastTab **Servizio** vengono aggiornate per te.

In alternativa, se si desidera utilizzare un altro servizio, è necessario fornire informazioni per effettuare la connessione. Per ulteriori informazioni, vedere [Per connettersi a un servizio di scambio di documenti](across-how-to-set-up-a-document-exchange-service.md#to-connect-to-a-document-exchange-service).

## <a name="to-connect-to-the-business-central-integration-app-on-tradeshift"></a>Per connettersi all'applicazione Business Central Integration su Tradeshift

È possibile creare rapidamente un account Tradeshift e iniziare con l'app Business Central Integration dal **Doc. Exch. Pagina di impostazione del servizio** . Scegli il link **Attiva app** nella notifica o il campo **URL app** per andare all'app nell'app store di Tradeshift. Nella pagina di accesso a Tradeshift, accedi o iscriviti.

> [!NOTE]
> Dopo aver effettuato l'accesso al tuo account Tradeshift, il sito potrebbe non portarti alla pagina in cui attivare l'app. Per farlo, potete cliccare sul link del **Doc. Exch. Pagina di Configurazione servizio** in Business Central di nuovo per andare direttamente all'app.

Se decidi di smettere di usare l'app Business Central Integration, devi disabilitarla nell'app store di Tradeshift. 

## <a name="to-connect-to-a-document-exchange-service"></a>Per connettersi a un servizio di scambio di documenti

Se preferisci usare un altro servizio di scambio di documenti, devi fornire alcune informazioni per connetterti al servizio.

1. Scegli la ![lampadina che apre l’icona della funzione Dimmi](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), entra in **Setup servizio di scambio documenti** e poi scegli il link correlato.  
2. Compilare i campi come indicato nella tabella seguente.  

    |Campo|Descrizione|  
    |---------------------------------|---------------------------------------|  
    |**Agente utente**|Inserisci un testo che può essere usato per identificare la tua azienda nei processi di scambio di documenti.|  
    |**Abilitato**|Specifica se la connessione al servizio è abilitata.<br><br> **Nota:**  Quando si abilita il servizio vengono create almeno due voci di coda di lavoro per inviare e ricevere documenti elettronici. Quando si disabilita il servizio, i movimenti della coda processi vengono eliminati.|  
    |**Sandbox**|Specifica se ti stai connettendo a una versione sandbox del servizio di scambio di documenti.|
    |**URL d'iscrizione**|Specificare la pagina Web a cui viene effettuata l'iscrizione per il servizio di Exchange per documenti.|  
    |**URL dell'app**|Scegli il link per aprire l'app store e attivare o disattivare l'app Business Central Integration.|
    |**URL servizio**|Specificare l'indirizzo del servizio di Exchange per documenti che verrà chiamato quando si inviano e ricevono documenti elettronici.|  
    |**URL di accesso**|Specifica l'URL della pagina che usi per accedere al servizio di scambio di documenti. Questa è la pagina in cui inserisci il nome utente e la password della tua azienda.|  
    
    > [!NOTE]  
    > Le tue credenziali di accesso sono automaticamente criptate. Non è possibile disattivare la crittografia.

    > [!NOTE]
    > Se non puoi connetterti al servizio di scambio di documenti a causa di un problema di autorizzazione, potrebbe essere perché [!INCLUDE[prod_short](includes/prod_short.md)] non può rinnovare automaticamente il token di accesso. Per esempio, questo potrebbe accadere se non hai usato il servizio per qualche tempo. Puoi rinnovare il token manualmente usando l'azione **Rinnova token** .

## <a name="settings-for-business-central-on-premises"></a>Impostazioni per Business Central On-Premises

Per collegare Business Central on-premises, è necessario creare un'app su Tradeshift App Store. Quando lo fai, usa l'URL di reindirizzamento dal campo **URL di reindirizzamento** nella pagina **Setup servizio di scambio documenti** . Dopo aver registrato la tua app, Tradeshift ti fornirà un ID cliente e un segreto cliente. In [!INCLUDE[prod_short](includes/prod_short.md)], inserisci questi valori nella FastTab **Autorizzazione** nella pagina di **impostazione del servizio di scambio documenti** .

Se si preferisce archiviare l'ID app e il segreto in una posizione diversa, è possibile lasciare vuoti i campi ID client e Segreto client e scrivere un'estensione per recuperare l'ID e il segreto dalla posizione. Puoi fornire il segreto a runtime sottoscrivendo gli eventi OnGetClientId e OnGetClientSecret nella codeunit 1410 "Doc. Exch. Gestione dei servizi"

## <a name="see-also"></a>Vedere anche

[Impostazione dello scambio di dati](across-set-up-data-exchange.md)  
[Scambio di dati in modalità elettronica](across-data-exchange.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
