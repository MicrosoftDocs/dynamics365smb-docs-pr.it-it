---
title: Dettagli di progettazione - Tracciabilità articolo e impegni
description: Questo argomento descrive la tracciabilità articolo e gli impegni nonché i concetti delle due opzioni.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/15/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Dettagli di progettazione: Tracciabilità articolo e impegni

L'utilizzo simultaneo degli impegni e della tracciabilità articolo specifica è raro, perché entrambi creano un accoppiamento tra approvvigionamento e domanda. Ad eccezione delle situazioni in cui un cliente o un responsabile della pianificazione di produzione richiede un lotto specifico, raramente ha senso impegnare gli articoli di magazzino che già hanno numeri di tracciabilità articolo per un'applicazione specifica. Sebbene sia possibile impegnare gli articoli che richiedono la tracciabilità articolo specifica, è necessaria una funzionalità speciale per evitare conflitti di disponibilità tra i processori di ordine che richiedono gli stessi articoli tracciati.  
  
Il concetto di combinazione tardiva garantisce che un impegno non specifico di un numero seriale o di lotto rimanga a regime di controllo libero ("loosely-coupled") fino alla registrazione. Al momento della registrazione, il sistema di impegno può rimescolare gli impegni non specifici per garantire che il collegamento fisso sia possibile rispetto al numero seriale o di lotto effettivamente selezionato. Nel frattempo, il numero seriale o di lotto viene reso disponibile per l'impegno specifico in altri documenti che richiedono quel determinato numero seriale o di lotto.  
  
Un impegno non specifico è uno in cui l'utente non si preoccupa di quale articolo specifico è selezionato e un impegno specifico è uno in cui l'utente si preoccupa.  
  
> [!NOTE]  
> La funzionalità di combinazione tardiva si riferisce solo agli articoli impostati con tracciabilità articolo specifica e si applica solo a impegni a fronte del magazzino, non rispetto a ordini di approvvigionamento in entrata.  
  
L'impegno dei numeri di tracciabilità articolo rientra in due categorie, come indicato nella tabella seguente.  
  
|Impegni|Description|  
|-----------------|---------------------------------------|  
|Specifico|Si seleziona un numero seriale o di lotto specifico quando si impegna l'articolo di magazzino da una domanda, ad esempio un ordine di vendita.<br /><br /> Questo è un impegno regolare. È un collegamento rigoroso tra approvvigionamento e domanda che includono entrambi i numeri seriali o di lotto. **Nota:** la domanda contiene numeri seriali o di lotto. <br /><br /> Ad esempio, si desidera impegnare una latta di vernice blu dal lotto A, in quanto il cliente lo richiede. Una latta di vernice blu dal Lotto A viene spedita al cliente.|  
|Non specifico|Non si seleziona un numero seriale o di lotto specifico quando si impegna l'articolo di magazzino da una domanda, ad esempio un ordine di vendita.<br /><br /> Questo è uno stato che viene imposto in un movimento di impegno per i numeri seriali o di lotto che non sono selezionati in modo specifico. **Nota:** la domanda non contiene numeri seriali o di lotto. <br /><br /> Ad esempio, si desidera impegnare una latta di vernice blu da un lotto per l'ordine di vendita. Una latta di vernice blu da un numero di serie o da un numero di lotto casuale viene spedita al cliente.|  
  
La principale differenza tra impegno specifico e impegno non specifico è definita dall'esistenza di numeri seriali o di lotto dal lato della domanda, come indicato nella tabella seguente.  

| Tipo            | Approvvigionamento                | Domanda                   |
|-----------------|-----------------------|--------------------------|
| **Specifico**    | Numero seriale o di lotto. | Numero seriale o di lotto.    |
| **Non specifico** | Numero seriale o di lotto. | Nessun numero seriale o di lotto. |
  
Quando si impegnano quantità di magazzino da una riga di documento in uscita per un articolo con numeri di tracciabilità assegnati e impostato per la tracciabilità di un articolo specifico, dalla pagina **Impegni** è possibile accedere a differenti workflow a seconda che si necessiti dei numeri seriali o dei numeri di lotto.  
  
## Impegno specifico  
Scegliendo **Impegno** dalla riga del documento in uscita, verrà visualizzata una finestra di dialogo nella quale verrà chiesto se si desidera impegnare numeri seriali o di lotto specifici. Se si sceglie **Sì**, viene visualizzato un elenco di tutti i numeri seriali o di lotto che sono assegnati alla riga del documento. La pagina **Impegni** viene aperta dopo che è stato selezionato uno dei numeri seriali o di lotto. Successivamente è possibile impegnare uno dei numeri seriali o di lotto secondo la normale procedura.  
  
Se alcuni dei numeri di tracciabilità articolo specifici che si sta tentando di impegnare sono utilizzati in impegni non specifici, verrà visualizzato un messaggio nella parte inferiore della pagina **Impegni** per indicare quanto della quantità impegnata totale è utilizzato in impegni non specifici e se c'è ancora disponibilità.  
  
## Impegno non specifico  
Se si sceglie **No** nella finestra di dialogo che viene visualizzata, viene visualizzata la pagina **Impegni** nella quale è possibile impegnare i numeri seriali o di lotto nel magazzino.  
  
A causa della struttura del sistema di impegno, quando si inserisce un impegno non specifico di un articolo tracciato, il sistema deve selezionare i movimenti contabili articolo specifici da impegnare. Poiché i movimenti contabili articoli sono dotati di numeri di tracciabilità articolo, specifici numeri di serie o di lotto vengono indirettamente riservati anche se non si intendeva farlo. Per gestire questo caso, il sistema di impegno prova a ridistribuire i movimenti impegni non specifici prima della registrazione.  
  
Il sistema in realtà impegna ancora a fronte di movimenti specifici, ma utilizza un meccanismo di consuntivazione ogni volta che si presenta una domanda specifica per il numero seriale o di lotto nell'impegno non specifico. Un esempio potrebbe essere quando si registra una transazione di domanda, ad esempio un ordine di vendita, le registrazioni consumi o un ordine di trasferimento, per il numero seriale o di lotto, o quando si tenta di impegnare in modo specifico il numero seriale o di lotto. Il sistema ridistribuisce gli impegni per rendere il numero seriale o di lotto disponibile alla domanda o all'impegno specifico, collocando in tal modo un numero seriale o di lotto differente nell'impegno non specifico. Se la quantità in magazzino è insufficiente, il sistema ridistribuisce il più possibile. Viene visualizzato un errore di disponibilità se, al momento della registrazione, la quantità risulta ancora insufficiente.  
  
> [!NOTE]  
>  In un impegno non specifico il campo del numero seriale o di lotto è vuoto nel movimento di impegno che punta alla domanda, ad esempio la vendita.  
  
## Ridistribuzione  
Quando un utente registra un documento in uscita dopo aver prelevato il numero seriale o di lotto errato, gli altri impegni non specifici vengono ridistribuiti per riflettere l'effettivo numero seriale o di lotto prelevato. Ciò soddisfa il motore di registrazione con un collegamento fisso tra approvvigionamento e domanda.  
  
Per tutti gli scenari aziendali supportati, è possibile rimescolare solo a fronte dei movimenti contabili articoli positivi che includono l'impegno e i numeri seriali o di lotto ma senza numero seriale o di lotto definito dal lato della domanda.  
  
## Scenari aziendali supportati  
La funzionalità di combinazione tardiva supporta i seguenti scenari aziendali:  
  
* Immettere un numero seriale o di lotto specifico in un documento in uscita con impegni non specifici o un numero seriale o di lotto errato.  
* Impegno di un numero seriale o di lotto specifico.  
* Registrazione di un documento in uscita con impegno non specifico di un numero seriale o di lotto.  
  
### Immissione di numeri seriali o di lotto in un documento in uscita con impegno non specifico errato  
Questo è il più comune dei tre scenari supportati. In questo caso, la funzionalità di combinazione tardiva garantisce che un utente possa immettere un numero seriale o di lotto, che in quel momento è prelevato, in un documento in uscita che ha già un impegno non specifico con un altro numero seriale o di lotto.  
  
Ad esempio, la necessità deriva da quando un gestore ordini ha eseguito prima un impegno non specifico di un numero seriale o di lotto. Successivamente, quando l'articolo viene effettivamente prelevato dal magazzino, il numero seriale o di lotto selezionato deve essere immesso nell'ordine prima che venga registrato. L'impegno non specifico viene ridistribuito in fase di registrazione per garantire che il numero seriale o di lotto selezionato possa essere inserito senza perdere l'impegno e per garantire che il numero seriale o di lotto selezionato sia completamente applicato e registrato.  
  
### Impegna un numero seriale o numeri di lotto  
In questo scenario di business, la funzionalità di combinazione tardiva garantisce che un utente, che tenta di impegnare un numero seriale o di lotto specifico che in quel momento è impegnato in modo non specifico, possa effettuare questa operazione. Un impegno non specifico viene ridistribuito al momento dell'impegno per liberare il numero seriale o di lotto per la richiesta specifica.  
  
La consuntivazione avviene automaticamente, ma nella parte inferiore della pagina **Impegni** viene visualizzata la Guida incorporata con il seguente testo:  
  
**XX della quantità impegnata totale non è specifico e potrebbe essere disponibile.**  
  
Inoltre, il campo **Qtà impegnata non specifica** mostra quanti movimenti impegno sono non specifici. Per impostazione predefinita, questo campo non è visibile agli utenti.  
  
### Registrazione di un documento in uscita con impegno non specifico di un numero seriale o di lotto  
Questo scenario aziendale è supportato con la funzionalità di combinazione tardiva che consente il collegamento fisso e la registrazione in uscita della quantità effettivamente prelevata tramite la ridistribuzione di un altro impegno non specifico di un numero seriale o di lotto. Se non è possibile procedere con la ridistribuzione, verrà visualizzato il seguente messaggio di errore standard nel momento in cui l'utente proverà a registrare la spedizione:  
  
**Impossibile collegare in modo completo l'articolo XX.**  
  
## Vedi anche  
[Dettagli di progettazione: Tracciabilità articolo](design-details-item-tracking.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]