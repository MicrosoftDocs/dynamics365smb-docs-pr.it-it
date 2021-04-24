---
title: Utilizzo dell'estensione di analisi immagini | Documenti Microsoft
description: Questa estensione consente di analizzare le immagini delle persone di contatto e degli articoli per trovare gli attributi e quindi assegnarli rapidamente in Business Central.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: API, extension, Cognitive Services, image, computer vision, attribute, tag, recognition
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 841ad4ff4963d8cfc6a284859affb60336e805a5
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5771314"
---
# <a name="the-image-analyzer-extension"></a>Estensione di analisi immagini

L'estensione di analisi immagini utilizza potenti funzionalità di analisi delle immagini fornite dall'API Visione artificiale dei Servizi cognitivi Microsoft per individuare gli attributi nelle immagini importate per gli articoli e le persone di contatto, in modo da potere esaminare e assegnare questi elementi con semplicità. Per gli articoli, agli attributi possono indicare, ad esempio, se si tratta di un tavolo o un'automobile o se è di colore rosso o blu. Per i contatti, gli attributi possono riguardare il sesso o l'età.

L'analisi immagini suggerisce gli attributi in base ai tag trovati dall'API Visione artificiale e ne indica il livello di affidabilità. Per impostazione predefinita, l'estensione suggerisce gli attributi solo se presentano un livello di affidabilità minimo dell'80% riguardo all'esattezza dell'attributo. È possibile impostare un livello di affidabilità diverso, se necessario. Per ulteriori informazioni su tag e livello di affidabilità, vedere [API Visione artificiale](https://go.microsoft.com/fwlink/?linkid=851476).  

L'estensione di analisi immagini è gratuita in [!INCLUDE[prod_short](includes/prod_short.md)], ma esiste un limite al numero di articoli che è possibile analizzare durante un determinato periodo di tempo. Per impostazione predefinita, è possibile analizzare 100 immagini al mese.

Dopo che l'estensione è stata abilitata, l'analisi delle immagini viene eseguita ogni volta che si importa un'immagine in un articolo o un contatto. Verranno visualizzati gli attributi, il livello di affidabilità e i dettagli immediatamente ed è possibile decidere quali azioni intraprendere con ogni attributo. Se le immagini sono state importate prima di avere abilitato l'estensione di analisi di immagini, è necessario passare all'articolo o alle schede contatti e scegliere l'azione **Analizza immagine**.  

## <a name="privacy-notice"></a>Informativa sulla privacy

Questa estensione utilizza l'API Visione artificiale di Servizi cognitivi Microsoft, che può avere livelli diversi di conformità rispetto a [!INCLUDE[prod_short](includes/prod_short.md)]. Quando si abilita l'estensione di analisi immagini, i dati del cliente quali un'immagine del contatto o un'immagine degli articoli verranno registrati nell'API Visione artificiale. Se si installa questa estensione si acconsente che questo set di dati limitato venga inviato all'API Visione artificiale. Si noti che è possibile disabilitare nonché disinstallare, l'estensione di analisi immagini in qualsiasi momento e interrompere utilizzo di questa funzione. Per ulteriori informazioni, vedere [Centro protezione Microsoft](https://go.microsoft.com/fwlink/?linkid=851463).

## <a name="requirements"></a>Requisiti

Le immagini devono soddisfare alcuni requisiti:

* Formato immagine: JPEG, PNG, GIF, BMP  
* Dimensione file massima: inferiore a 4 MB  
* Dimensioni immagine: superiori a 50 x 50 pixel  

## <a name="to-enable-image-analyzer"></a>Per abilitare l'analisi immagini

L'estensione di analisi delle immagini è incorporata in [!INCLUDE[prod_short](includes/prod_short.md)]. È solo necessario attivarla.

> [!NOTE]  
> Per abilitare l'estensione di analisi delle immagini, è necessario disporre dei diritti di amministratore. Assicurarsi di disporre del set di autorizzazioni come utente con privilegi **AVANZATI**.

1. Per attivare l'estensione di analisi immagini, effettuare una delle seguenti operazioni:

* Aprire un articolo o una scheda contatto. Nella barra di notifica scegliere **Analisi immagine** e seguire i passaggi nella Guida assistita di setup.  
* Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Connessioni servizio** e quindi scegliere **Setup analisi immagine**. Scegliere la casella di controllo **Abilita analisi immagine** e completare i passaggi nella Guida assistita di setup.  

    > [!TIP]  
    > Nella pagina **Setup analisi immagine** è possibile anche modificare il grado di affidabilità per i suggerimenti relativi all'attributo. Ad esempio, se si intende richiedere un maggior grado di affidabilità, è possibile immettere un valore percentuale più alto.

## <a name="to-analyze-an-image-of-an-item"></a>Per analizzare un'immagine di un articolo

Nei seguenti passaggi viene descritto come analizzare un'immagine importata prima dell'abilitazione dell'estensione di analisi immagini.  

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Articoli** e quindi scegliere il collegamento correlato.  
2. Selezionare l'articolo, quindi scegliere l'azione **Analizza immagine**.  
3. Nella pagina **Attributi analisi immagini** vengono visualizzati gli attributi trovati, il livello di affidabilità e altre informazioni relative all'attributo. Utilizzare le opzioni **Azione da eseguire** per specificare l'azione da intraprendere per l'attributo.  

    > [!TIP]  
    > È possibile aggiungere il nome dell'attributo alla descrizione dell'articolo selezionando **Aggiungi a descrizione articolo**. Ad esempio, questo può essere utile per aggiungere rapidamente un dettaglio.  

## <a name="to-analyze-a-picture-of-a-contact-person"></a>Per analizzare un'immagine di una persona di contatto

Nei seguenti passaggi viene descritto come analizzare un'immagine importata prima dell'abilitazione dell'estensione di analisi immagini.  

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Contatti** e quindi scegliere il collegamento correlato.  
2. Selezionare la persona di contatto, quindi scegliere l'azione **Analizza immagine**.  
3. Nella Scheda dettaglio **Questionario profilo**, esaminare i suggerimenti e apportare le correzioni, se necessario.  

## <a name="block-suggested-attributes"></a>Bloccare gli attributi suggeriti

Se l'analisi propone un attributo che non si desidera visualizzare, è possibile bloccare l'attributo. Tuttavia, prestare attenzione. Gli attributi bloccati non verranno suggeriti nemmeno per altri articoli o persone di contatto. Se si cambia idea sul blocco di un articolo, è possibile scegliere **Visualizza attributi in blacklist** e quindi eliminare l'attributo dall'elenco.

## <a name="to-use-your-own-account-for-the-computer-vision-api"></a>Per utilizzare il proprio account per l'API Visione artificiale

È anche possibile utilizzare il proprio account per l'API Visione artificiale, ad esempio, se si desidera analizzare più immagini rispetto al numero consentito.  

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup Analizzatore immagine** e quindi scegliere il collegamento correlato.  
2. Immettere l' **URI API** e la **Chiave API** ricevuti per l'API Visione artificiale.  

    > [!NOTE]  
    > È necessario aggiungere **/analyze** alla fine dell'URI API, se non è già presente. Ad esempio: ```https://cronus.api.cognitive.microsoft.com/vision/v1.0/analyze```

## <a name="to-see-how-many-analyses-you-have-left-in-the-current-period"></a>Per visualizzare il numero delle analisi rimanenti per il periodo corrente

È possibile visualizzare il numero delle analisi effettuate e il numero rimanente per il periodo corrente.  

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup Analizzatore immagine** e quindi scegliere il collegamento correlato.  
2. I campi **Tipo di limite**, **Valore limite** e **Analisi eseguite** forniscono informazioni sull'utilizzo.  

## <a name="to-stop-using-the-image-analyzer-extension"></a>Per interrompere l'utilizzo dell'estensione di analisi immagini

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Connessioni servizio** e quindi scegliere **Setup Analizzatore immagine**.  
2. Deselezionare la casella di controllo **Abilita analisi immagine**.  

## <a name="see-also"></a>Vedi anche

[Utilizzare gli attributi degli articoli](inventory-how-work-item-attributes.md)  
[Personalizzazione di [!INCLUDE[prod_short](includes/prod_short.md)] utilizzando le estensioni](ui-extensions.md)  
[Preparazione al business](ui-get-ready-business.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]