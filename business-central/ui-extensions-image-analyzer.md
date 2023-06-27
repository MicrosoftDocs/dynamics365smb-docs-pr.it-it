---
title: Estensione di analisi immagini
description: Questa estensione consente di analizzare le immagini delle persone di contatto e degli articoli per trovare gli attributi e quindi assegnarli rapidamente in Business Central.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'API, extension, Cognitive Services, image, computer vision, attribute, tag, recognition'
ms.search.form: '2026, 2027, 2029,'
ms.date: 05/19/2021
ms.author: bholtorf
---

# <a name="the-image-analyzer-extension"></a>Estensione di analisi immagini

L'estensione di analisi immagini utilizza potenti funzionalità di analisi delle immagini fornite dall'API per Azure Cognitive Services per individuare gli attributi nelle immagini importate per gli articoli e le persone di contatto, in modo da potere esaminare e assegnare questi elementi con semplicità. Per gli articoli, agli attributi possono indicare, ad esempio, se si tratta di un tavolo o un'automobile o se è di colore rosso o blu. Per i contatti, gli attributi possono riguardare il sesso o l'età.

L'analisi immagini suggerisce gli attributi in base ai tag trovati dall'API Visione artificiale e ne indica il livello di affidabilità. Per impostazione predefinita, l'estensione suggerisce gli attributi solo se presentano un livello di affidabilità minimo dell'80% riguardo all'esattezza dell'attributo. È possibile impostare un livello di affidabilità diverso, se necessario. Per ulteriori informazioni su tag e livello di affidabilità, vedere [API Visione artificiale](https://go.microsoft.com/fwlink/?linkid=851476).  

L'estensione di analisi immagini è gratuita in [!INCLUDE[prod_short](includes/prod_short.md)], ma esiste un limite al numero di articoli che è possibile analizzare durante un determinato periodo di tempo. Per impostazione predefinita, è possibile analizzare 100 immagini al mese.

Dopo che l'estensione è stata abilitata, l'analisi delle immagini viene eseguita ogni volta che si importa un'immagine in un articolo o un contatto. Verranno visualizzati gli attributi, il livello di affidabilità e i dettagli immediatamente ed è possibile decidere quali azioni intraprendere con ogni attributo. Se le immagini sono state importate prima di avere abilitato l'estensione di analisi di immagini, è necessario passare all'articolo o alle schede contatti e scegliere l'azione **Analizza immagine**.  

## <a name="privacy-notice"></a>Informativa sulla privacy

Questa estensione utilizza l'API Visione artificiale di Azure Cognitive Services, che può avere livelli diversi di conformità rispetto a [!INCLUDE[prod_short](includes/prod_short.md)]. Quando si abilita l'estensione di analisi immagini, i dati del cliente quali un'immagine del contatto o un'immagine degli articoli verranno registrati nell'API Visione artificiale. Se si installa questa estensione si acconsente che questo set di dati limitato venga inviato all'API Visione artificiale. Si noti che è possibile disabilitare e disinstallare, l'estensione di analisi immagini in qualsiasi momento e interrompere utilizzo di questa funzione. Per ulteriori informazioni, vedere [Centro protezione Microsoft](https://go.microsoft.com/fwlink/?linkid=851463).

## <a name="requirements"></a>Requisiti

Le immagini devono soddisfare alcuni requisiti:

* Formato immagine: JPEG, PNG, GIF, BMP  
* Dimensione file massima: inferiore a 4 MB  
* Dimensioni immagine: superiori a 50 x 50 pixel  

## <a name="switch-on-the-image-analyzer-extension"></a>Attiva l'estensione Analisi di immagini

L'estensione di analisi delle immagini è incorporata in [!INCLUDE[prod_short](includes/prod_short.md)]. È solo necessario attivarla.

> [!NOTE]  
> Per abilitare l'estensione di analisi delle immagini, è necessario disporre dei diritti di amministratore. Assicurarsi di disporre del set di autorizzazioni come utente con privilegi **AVANZATI**. Per ulteriori informazioni, vedere [Assegnare autorizzazioni a utenti e gruppi](ui-define-granular-permissions.md).

Per attivare l'estensione di analisi immagini, effettuare una delle seguenti azioni:

* Aprire un articolo o una scheda contatto. Nella barra di notifica scegliere **Analisi immagine**, seguire i passaggi nella Guida assistita di setup.  
* Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Connessioni servizio**, quindi scegli **Setup analisi immagine**. Scegliere la casella di controllo **Abilita analisi immagine** e completare i passaggi nella Guida assistita di setup.  

    > [!TIP]  
    > Nella pagina **Setup analisi immagine** è possibile anche modificare il grado di affidabilità per i suggerimenti relativi all'attributo. Ad esempio, se si intende richiedere un maggior grado di affidabilità, è possibile immettere un valore percentuale più alto.

## <a name="analyze-an-item-image"></a>Analizzare un'immagine dell'articolo

Nei seguenti passaggi viene descritto come analizzare un'immagine importata prima dell'abilitazione dell'estensione di analisi immagini.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Articoli**, quindi scegli il collegamento correlato.  
2. Selezionare l'articolo, quindi scegliere l'azione **Analizza immagine**.  
3. Nella pagina **Attributi analisi immagini** vengono visualizzati gli attributi trovati, il livello di affidabilità e altre informazioni relative all'attributo. Usa le opzioni **Azione da eseguire** per specificare cosa fare con l'attributo o scegliere **Aggiungi a descrizione articolo** per aggiungere il nome dell'attributo alla descrizione dell'oggetto. Ad esempio, questa azione può essere utile per aggiungere rapidamente un dettaglio.

Il campo **Azione da eseguire** ha le seguenti opzioni:

| Azione | Descrizione |
| ------ | ----------- |
| *Ignora* | Nessuna azione verrà eseguita. |
| *Usa come attributo* | Il valore viene aggiunto agli attributi dell'elemento. Ulteriori informazioni in [Utilizzare gli attributi degli articoli](inventory-how-work-item-attributes.md). |
| *Usa come categoria* | Il valore selezionato viene aggiunto come categoria. Ulteriori informazioni in [Classificare gli articoli](inventory-how-categorize-items.md). |
| *Aggiungi a elenco elementi bloccati* | Se l'analisi propone un attributo che non si desidera visualizzare, è possibile bloccare l'attributo. Tuttavia, prestare attenzione. Gli attributi bloccati non verranno suggeriti nemmeno per altri articoli. Se cambi idea sul blocco di un articolo, puoi scegliere **Visualizza attributi bloccati** e quindi eliminare l'attributo dall'elenco. |

> [!NOTE]  
> Per impostazione predefinita, in **Attributi oggetto** vengono visualizzati gli attributi in cui **Punteggio di fiducia** è al di sopra di **Soglia punteggio affidabilità in %** definito in **Setup analisi immagine**. Per vedere tutti gli attributi rilevati, scegli l'azione **Visualizza tutti gli attributi**.

## <a name="analyze-a-contact-person-picture"></a>Analizzare un'immagine di una persona di contatto

Nei seguenti passaggi viene descritto come analizzare un'immagine importata prima dell'abilitazione dell'estensione di analisi immagini.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Contatti**, quindi scegli il collegamento correlato.  
2. Selezionare la persona di contatto, quindi scegliere l'azione **Analizza immagine**.  
3. Nella Scheda dettaglio **Questionario profilo**, esaminare i suggerimenti e apportare le correzioni, se necessario. Ulteriori informazioni in [Utilizzare i questionari profilo per classificare i contatti business](marketing-create-contact-profile-questionnaire.md).  

    > [!NOTE]  
    >
    > L'API Visione artificiale restituisce i seguenti attributi:
    >
    > * *età*
    >
    >     Un'età visiva stimata in anni. È l'età di una persona rispetto all'età biologica effettiva.
    > * *sesso*
    >
    >    Maschio o femmina.
    >
    > L'API Visione artificiale non restituisce il livello di confidenza per gli attributi di età e sesso.
  
## <a name="use-your-own-computer-vision-api-account"></a>Utilizzare il proprio account per l'API Visione artificiale

È anche possibile utilizzare il proprio account per l'API Visione artificiale, ad esempio, se si desidera analizzare più immagini rispetto a quanto offre l'integrazione predefinita.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup analisi immagine**, quindi scegli il collegamento correlato.
2. Immettere l' **URI API** e la **Chiave API** ricevuti per l'API Visione artificiale.  

    > [!NOTE]  
    > È necessario aggiungere **/analyze** alla fine dell'URI API, se non è già presente. Ad esempio: ```https://cronus.api.cognitive.microsoft.com/vision/v2.0/analyze```.

## <a name="see-how-many-analyses-you-have-left-in-the-current-period"></a>Visualizzare il numero delle analisi rimanenti per il periodo corrente

È possibile visualizzare il numero delle analisi effettuate e il numero rimanente per il periodo corrente.  

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup analisi immagine**, quindi scegli il collegamento correlato.
2. I campi **Tipo di limite**, **Valore limite** e **Analisi eseguite** forniscono informazioni sull'utilizzo.  

## <a name="stop-using-the-image-analyzer-extension"></a>Interrompere l'utilizzo dell'estensione di analisi immagini

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Connessioni servizio**, quindi scegli **Setup analisi immagine**.  
2. Deselezionare il campo **Abilita analisi immagine**.  

In alternativa, disinstalla completamente l'estensione. Puoi sempre recuperarla da AppSource. Per ulteriori informazioni, vedi [Installazione e disinstallazione delle estensioni in Business Central](ui-extensions-install-uninstall.md#uninstall-an-app).  

## <a name="see-also"></a>Vedere anche

[Utilizzare gli attributi degli articoli](inventory-how-work-item-attributes.md)  
[Classificare gli articoli](inventory-how-categorize-items.md)  
[Utilizzare i questionari profilo per classificare i contatti business](marketing-create-contact-profile-questionnaire.md)  
[Personalizzazione di [!INCLUDE[prod_short](includes/prod_short.md)] utilizzando le estensioni](ui-extensions.md)  
[Preparazione al business](ui-get-ready-business.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
