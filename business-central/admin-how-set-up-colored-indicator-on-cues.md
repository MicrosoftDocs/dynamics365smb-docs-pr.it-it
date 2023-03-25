---
title: Configurare indicatori colorati personalizzati per l'attività della pila
description: 'Come amministratore, è possibile impostare le pile che vengono visualizzate in gestione ruolo utente degli utenti in modo che includano un indicatore che cambia colore in base ai valori dei dati presenti nelle pile.'
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '9701, 9702'
ms.date: 04/01/2021
ms.author: jswymer
---
# Impostare un indicatore colorato nelle pile per la società o per i singoli utenti

Come amministratore, è possibile impostare le pile che vengono visualizzate in gestione ruolo utente degli utenti in modo che includano un indicatore che cambia colore in base ai valori dei dati presenti nelle pile.  

L'indicatore viene visualizzato come una barra colorata lungo il bordo superiore della pila. Fornisce un segnale visivo dello stato dell'attività della pila, che può indicare le condizioni favorevoli o sfavorevoli per spingere l'utente a intraprendere un'azione. Ad esempio, se una pila visualizza le fatture di vendita in corso, è possibile impostare l'indicatore in modo che appaia verde (favorevole) quando il totale delle fatture di vendita in corso è minore di 10 e rosso (sfavorevole) quando il totale è maggiore di 20.  

Nella pagina **Setup pila**, si impostano gli indicatori di tutte le pile disponibili nel database della società. È possibile impostare gli indicatori perché siano applicati a tutti gli utenti della società o a un singolo utente. Le impostazioni dell'indicatore nella pagina **Setup pila** fungono da impostazioni predefinite dell'indicatore. Se la pagina **Utente finale setup pila** è disponibile per gli utenti, questi possono personalizzare le impostazioni degli indicatori definiti nella pagina **Setup pila**.  

Per impostare l'indicatore, specificare fino a due valori di soglia che definiscono tre intervalli dei valori dei dati (basso, medio e alto) e a cui è possibile applicare un colore diverso (o stile).  

### Per impostare indicatori colorati nelle pile  
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup pila**, quindi scegli il collegamento correlato.  

     Verrà visualizzata la pagina **Setup pila**. La pagina elenca gli indicatori che attualmente sono impostati nelle pile. Gli indicatori che si applicano a tutti gli utenti della società hanno un campo **Nome utente** vuoto. Gli indicatori che si applicano a un utente specifico comprendono il nome dell'utente nel campo **Nome utente**.  

    > [!NOTE]  
    >  Se si imposta un indicatore per tutta la società e un utente modifica in seguito l'indicatore, una registrazione distinta relativa all'indicatore viene visualizzata nella lista per tale utente.  

2. Scegliere l'azione **Modifica lista**.  
3. Per impostare un indicatore per una pila non elencata nella pagina, selezionare l'azione **Nuovo**, quindi compilare i campi come descritto di seguito. Se si desidera modificare un indicatore esistente, passare alla fase successiva.  

    |  Campo  |  Description  |    
    |---------|---------------|  
    |**Nome utente**|Se si desidera impostare l'indicatore per tutti gli utenti, lasciare vuoto questo campo.<br /><br /> Se si desidera impostare l'indicatore per un utente specifico, impostare questo campo con il nome utente.|  
    |**Nr. tabella**|Specifica l'ID dell'oggetto tabella che contiene la Pila. Utilizzare la lista di menu a discesa per trovare la tabella. La lista del menu a discesa include tutte le tabelle della pila presenti nel database della società.<br /><br /> Il campo **Nome tabella** verrà automaticamente compilato in base alla selezione.|  
    |**Nr. campo**|Specifica l'ID della pila nella quale si desidera impostare in indicatore. Utilizzare la lista del menu a discesa per trovare la pila desiderata. **Nota:**  l'ID della pila corrisponde al numero del campo assegnato alla pila nella tabella. <br /><br /> Il campo **Nome campo** viene automaticamente compilato in base alla selezione|  

4. Per impostare l'indicatore per una pila, impostare i campi come descritto nella tabella seguente.  

    |  Campo  |  Description  |    
    |---------|---------------|  
    |**LowStyle**|Specifica il colore dell'indicatore quando il valore della pila è inferiore al valore del campo **Soglia 1**.|  
    |**LowThreshold**|Specifica il valore a partire dal quale l'indicatore cambia il colore specificato nel campo **Stile intervallo medio**.|  
    |**MiddleStyle**|Specifica il colore dell'indicatore quando il valore della pila è superiore o uguale al valore del campo **Soglia 1** ma inferiore o uguale al valore del campo **Soglia 2**.|  
    |**HighThreshold**|Specifica il valore al di sopra del quale l'indicatore cambia il colore specificato nel campo **Stile intervallo superiore**.|  
    |**HighStyle**|Specifica il colore da utilizzare quando il valore della pila è superiore al valore del campo **Soglia 2**.|  

     Nella tabella seguente sono elencati i colori corrispondenti alle opzioni dei campi **LowStyle**, **MiddleStyle** e **HighStyle**.  

    |  Opzione  |  Colore  |  
    |----------|---------|  
    |**Nessuno**|Nessun colore (lo stesso colore della sezione Pila)|  
    |**Favorevole**|Verde|  
    |**Sfavorevole**|Rosso|  
    |**Ambiguo**|Giallo|  
    |**Subordinato**|Grigio|  

## Vedere anche


[!INCLUDE[footer-include](includes/footer-banner.md)]