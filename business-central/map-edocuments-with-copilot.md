---
title: Mappare documenti elettronici per acquistare righe di ordini di acquisto con Copilot
description: Scopri come utilizzare Copilot per mappare documenti elettronici a righe di ordini di acquisto.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: altotovi
ms.topic: how-to
ms.collection:
  - get-started
  - bap-ai-copilot
ms.date: 04/10/2024
ms.custom: bap-template
---

# <a name="map-e-documents-to-purchase-order-lines-with-copilot-preview"></a>Mappare documenti elettronici per acquistare righe di ordini di acquisto con Copilot (anteprima)

Man mano che i processi di approvvigionamento diventano più digitali, la funzionalità dei documenti elettronici in Business Central svolge un ruolo chiave nell'automazione della ricezione e dell'elaborazione delle fatture fornitore. Copilot può assistere in questo processo migliorando il mapping e la corrispondenza delle fatture fornitore a ordini di acquisto. Ciò riduce le attività dispendiose in termini di tempo che normalmente includerebbero ricerche approfondite, ricerche e immissione di dati. Il vantaggio è dato dal fatto che le fatture fornitore spesso non si riferiscono esattamente agli ordini d'acquisto, nel qual caso Copilot è in una posizione migliore per identificare gli ordini d'acquisto corrispondenti. Le funzionalità di corrispondenza migliorate avvantaggiano in particolare le organizzazioni di piccole e medie dimensioni che necessitano di un tracciamento efficiente dei documenti per le righe di ordini di acquisto. Copilot è l'assistente per il lavoro basato sull'intelligenza artificiale che stimola la creatività e migliora la produttività per gli utenti di Business Central.

> [!IMPORTANT]
> - Questa è una funzionalità di Anteprima pronta per la produzione per ambienti di produzione e sandbox in qualsiasi localizzazione, ad eccezione del Canada.
> - Le anteprime pronte per la produzione sono soggette a condizioni per l'utilizzo supplementari. Ulteriori informazioni: [Condizioni di utilizzo supplementari per l'anteprima di Dynamics 365](https://go.microsoft.com/fwlink/?linkid=2105274)
> - I contenuti generati dall'intelligenza artificiale potrebbero non essere corretti.

Nella versione iniziale dell'app **Documento elettronico**, abbiamo introdotto scenari fondamentali per documenti elettronici per l'intero processo di vendita. Tuttavia, sono necessari miglioramenti e automazione nella gestione dei documenti ricevuti, soprattutto nel contesto dei processi di acquisto. Copilot perfeziona il modo in cui gestisci i documenti elettronici nel processo di acquisto, in particolare per quanto riguarda gli ordini di acquisto. Il framework dei documenti elettronici ti consente di specificare il tipo di documento di acquisto da creare per ciascun fornitore quando ricevi fatture elettroniche da loro. In precedenza, l'unica opzione era creare una fattura di acquisto, come documento o registrazione COGE.

Ora puoi aggiornare un ordine di acquisto esistente in Business Central con le informazioni ricevute nella fattura elettronica.

<!--
> [!NOTE]
> - This feature is available as a production-ready preview for production and sandbox environments in any country localization, with the exception of Canada. Production-ready previews are subject to supplemental terms of use. For more information, see [Supplemental terms of use for Dynamics 365 preview](https://go.microsoft.com/fwlink/?linkid=2105274).
> - AI-generated content may be incorrect.-->

## <a name="to-activate-copilot"></a>Per attivare Copilot

Nel caso in cui non hai attivato il copilota **Assistenza per la corrispondenza dei documenti elettronici**, devi farlo manualmente. Per abilitare il copilota **Assistenza per la corrispondenza dei documenti elettronici**, segui questi passaggi: 

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immetti **Funzionalità di Copilot e IA**, quindi seleziona il collegamento correlato. 
2. Nell'elenco delle funzionalità, seleziona **Assistenza per la corrispondenza dei documenti elettronici** e modifica lo stato in **Attivo**.  

Puoi iniziare a utilizzare Copilot non appena viene attivato. 

## <a name="identify-purchase-orders"></a>Identificare ordini di acquisto

Innanzitutto, puoi identificare gli ordini di acquisto per i quali puoi trovare automaticamente una corrispondenza. Se il tuo **Fornitore** ha configurato il campo **Ricevi documento elettronico su** per l'utilizzo con **Ordini di acquisto**, una volta creato il documento elettronico in [!INCLUDE[prod_short](includes/prod_short.md)] (manualmente o da un punto finale esterno), [!INCLUDE[prod_short](includes/prod_short.md)] effettuerà quanto segue:

1. Se l'**ordine di acquisto** per questo particolare fornitore *esiste e c'è un numero di ordine di acquisto* nel file **Documento elettronico** ricevuto, [!INCLUDE[prod_short](includes/prod_short.md)] collegherà automaticamente questo **Documento elettronico** all'**Ordine di acquisto** specificato. Lo **Stato del documento** di questo **Documento elettronico** sarà **In corso** e lo **Stato del documento elettronico** nella pagina secondaria **Stato del servizio** sarà **Ordine collegato**.  
Questo collegamento sarà visibile nel campo **Documento** in questo specifico **Documento elettronico**. Se devi modificare l'**Ordine di acquisto** collegato automaticamente, puoi farlo utilizzando l'azione **Aggiorna collegamento ordine di acquisto** e quindi scegliendo manualmente uno degli ordini di acquisto esistenti per questo fornitore. Puoi farlo solo prima di abbinare le righe tra il **Documento elettronico** e l'**Ordine di acquisto**.  
2. Se l'**Ordine di acquisto** per questo particolare fornitore *esiste ma non è presente un numero di ordine di acquisto* nel file di ricezione di **Documenti elettronici**, [!INCLUDE[prod_short](includes/prod_short.md)] offre la possibilità di scegliere uno degli ordini di acquisto esistenti quando e se hai caricato manualmente questo documento, aprendo l'elenco **Ordini di acquisto** con solo ordini per il fornitore con il **Documento elettronico**, dove devi selezionare l'**Ordine di acquisto** che desideri e selezionare **OK**. Se non selezioni l'**Ordine di acquisto** corretto o hai ricevuto il **Documento elettronico** automaticamente da un endpoint esterno utilizzando la **Coda processi**, il nuovo **Documento elettronico** non sarà collegato ad alcun documento di acquisto e lo **Stato del documento** sarà **Errore** e lo **Stato del documento elettronico** nella pagina secondaria **Stato servizio** sarà **Errore di elaborazione documenti importati**. Per completare il collegamento con l'**Ordine di acquisto**, scegli l'azione **Aggiorna collegamento ordine di acquisto** e scegli uno degli ordini di acquisto esistenti per questo fornitore.  

## <a name="map-lines"></a>Mappare le righe

Copilot ti aiuta a trovare automaticamente una corrispondenza tra le righe della fattura elettronica e le righe di ordine di acquisto e offre informazioni aggiuntive sulla corrispondenza per migliorare le corrispondenze.

Una volta trovata la corrispondenza ed eseguito il mapping, [!INCLUDE [prod_short](includes/prod_short.md)] aggiorna l'ordine di acquisto corrispondente con le informazioni sul carico pertinenti per garantire che nelle righe di ordine vengano ricevute le quantità corrette.

Puoi abbinare i documenti elettronici ricevuti alle righe degli ordini di acquisto da due aree diverse, ovvero la pagina **Documento elettronico** o la pagina **Ordine di acquisto**. Il modo più semplice di individuare l'**Ordine di acquisto** collegato è usare il riquadro **Ordini di acquisto collegati** come parte di **Attività documento elettronico**. Tutti i documenti non collegati possono essere trovati utilizzando il riquadro **Attesa di fatture elettroniche di acquisto** dove hai un elenco di **Documenti elettronici** che devi rivedere.  

> [!NOTE]
> Le **Attività documento elettronico** con questi due riquadri si trova nelle Gestioni ruolo utente seguenti: **Valutazione manager aziendale**, **Manager aziendale**, **Contabile**, **Gestione inventario** e **Spedizione e carico**.

Quando si desidera eseguire la corrispondenza dall'ordine d'acquisto, scegli l'azione **Mappa righe documento elettronico**, presente sia nella pagina dell'ordine d'acquisto che in quella dell'elenco degli ordini d'acquisto. Tuttavia, se desideri eseguire la corrispondenza dalla pagina **Documenti elettronici**, scegli l'azione **Abbina ordine di acquisto** da questa pagina. Per eseguire l'elaborazione con l'associazione, segui i passaggi seguenti:

1. Scegli l'azione **Mappa righe documento elettronico** o **Abbina ordine di acquisto** per i documenti già collegati.  
2. Puoi notare che il prompt **Abbina righe dell'ordine del documento elettronico con Copilot** funziona e hai la pagina **Corrispondenza ordine di acquisto** in background. Ciò significa che è in esecuzione lo stesso processo ma con il supporto automatico di **Copilot**, che esegue il processo di abbinamento al posto tuo. 
3. Dopo alcuni secondi, **Abbina righe dell'ordine del documento elettronico con Copilot** suggerirà le righe da abbinare con alcuni dettagli aggiuntivi: 

    1. Nell'intestazione del prompt puoi trovare le seguenti informazioni: 

    |Nome campo |Descrizione |
    |--------|-----------------|
    |Corrispondenza automatica | Specifica il numero di corrispondenze proposte automaticamente. Ciò si basa su un confronto di stringhe e se si verifica una sovrapposizione dell'80% o più delle descrizioni, il sistema abbinerà automaticamente queste descrizioni senza utilizzare le funzionalità GPT. |
    |Corrispondenze di Copilot | Specifica il numero di corrispondenze proposte da Copilot utilizzando sia il confronto delle stringhe che quello semantico. |
    |Nr. documento elettronico | Specifica il numero di documento elettronico collegato. |
    |Importo totale fattura, IVA esclusa | Specifica l'importo totale della fattura IVA esclusa. |
    |Corrispondenza importo totale IVA inclusa | Specifica l'importo corrispondente, IVA esclusa. |
    
    2. Se tutte le righe corrispondono, vedrai il testo verde nell'angolo in alto a destra: **Tutte le righe (100%) corrispondono. Esaminare le corrispondenze proposte**.  
    3. Nelle righe **Proposta corrispondente** puoi trovare le seguenti informazioni:  

    |Nome campo |Descrizione |
    |--------|-----------------|
    |Nr. righe documento elettronico | Specifica il numero di riga del documento elettronico (presente nel file del documento elettronico originale). |
    |Descrizione riga documento elettronico | Specifica la descrizione della riga del documento elettronico (presente nel file del documento elettronico originale). |
    |Quantità corrispondente | Specifica la quantità che verrà applicata alla riga dell'ordine di acquisto. |
    |Proposta | Specifica l'azione proposta dall'IA e queste azioni suggerite sono correlate alla corrispondenza delle righe dell'ordine di acquisto. |

    4. Tutte le righe completamente suggerite e corrispondenti sono contrassegnate in verde. Se c'è qualche problema, ad esempio un prezzo diverso, ma nell'intervallo di prezzo consentito, questa riga sarà in giallo e se c'è qualche similarità tra i campi della descrizione ma la differenza di prezzo è maggiore del consentito, sarà in rosso. 
    5. Se non sei soddisfatto di alcuni suggerimenti, puoi eliminarli utilizzando l'azione **Elimina riga**.  
    6. Se desideri visualizzare le corrispondenze delle proposte, puoi selezionare il collegamento nella colonna **Proposta** per aprire la pagina **Dettagli della corrispondenza del documento elettronico**. 
    7. Nella pagina **Dettagli della corrispondenza del documento elettronico** puoi confrontare i dettagli del **Documento elettronico** e dell'**Ordine di acquisto**, per essere sicuro dell'abbinamento suggerito prima di confermarlo. 
    8. Dopo la revisione, chiudi la pagina.   

4. Se non sei soddisfatto della maggior parte dei suggerimenti o se non desideri utilizzare la funzionalità **Abbina righe dell'ordine del documento elettronico con Copilot**, seleziona **Ignora** e puoi continuare con l'[abbinamento manuale](finance-how-use-edocuments-purchase.md) come spiegato in precedenza.  
5. Se vuoi conservare i suggerimenti, scegli il pulsante **Mantieni** e il sistema salverà tutti i suggerimenti forniti da **Copilot**.  
6. [!INCLUDE[prod_short](includes/prod_short.md)] chiude il prompt di Copilot e le righe nella pagina **Corrispondenza ordine di acquisto** verranno contrassegnate in verde, poiché sono già abbinate.  
7. Da questo momento, puoi continuare a lavorare mentre esegui l'abbinamento manuale, e ciò significa che puoi rimuovere corrispondenze e corrispondenze manuali, ripristinare la corrispondenza o, se non ci sono modifiche che desideri apportare, scegliere l'azione **Applica all'ordine di acquisto** e continuare a lavorare con l'**Ordine di acquisto**. 

> [!NOTE]
> Puoi scegliere di nuovo l'azione **Confronta con Copilot** dalla pagina **Corrispondenza ordine di acquisto**, ma in questa In questo caso, ti verrà chiesto se desideri sovrascrivere le corrispondenze esistenti, poiché tutte le righe sono già state abbinate.  

> [!NOTE]
> L'analisi dei prezzi/costi e il controllo della quantità disponibile fanno parte dell'attività di pre-elaborazione. 

## <a name="see-also"></a>Vedere anche

[Panoramica dei documenti elettronici](finance-edocuments-overview.md)    
[Usare documenti elettronici nelle vendite](finance-how-use-edocuments.md)    
[Utilizzare documenti elettronici negli acquisti](finance-how-use-edocuments-purchase.md)   
[Risoluzione dei problemi relativi alle funzionalità di Copilot e IA](ai-copilot-troubleshooting.md)    
[Domande frequenti sull'intelligenza artificiale responsabile per l'assistenza per la riconciliazione dei conti correnti bancari](faqs-bank-reconciliation.md)    
