---
title: Come impostare aree di produzione e centri di lavoro | Microsoft Docs
description: Una scheda **Area di produzione** consente di organizzare i valori e i requisiti fissi della risorsa di produzione e, quindi, di gestire l'output della produzione effettuata in tale area di produzione.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 08/10/2020
ms.author: sgroespe
ms.openlocfilehash: 4e3a6c646605d5c1da26ff0d0795413a53fabe82
ms.sourcegitcommit: 007b331b6974983ee614db0406f00777da359ecb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/10/2020
ms.locfileid: "3677285"
---
# <a name="set-up-work-centers-and-machine-centers"></a>Impostare aree di produzione e centri di lavoro

L'applicazione distingue tra tre tipi di capacità. Questi sono disposti in modo gerarchico. Ogni livello contiene i livelli inferiori.  

Il livello più alto è rappresentato dal reparto di produzione. Ai reparti di produzione vengono assegnate le aree di produzione. Ogni area di produzione può far parte di un solo reparto di produzione.

A ogni area di produzione è possibile assegnare diversi centri di lavoro. Un centro di lavoro può far parte di una sola area di produzione.  

La capacita pianificata di un'area di produzione consiste della disponibilità dei centri di lavoro corrispondenti oltre che della disponibilità pianificata dell'area stessa. La disponibilità pianificata di un reparto di produzione è data quindi dalla somma di tutte le disponibilità delle relative aree di produzione e dei relativi centri di lavoro.  

La disponibilità viene memorizzata nei movimenti di calendario. Prima di impostare le aree di produzione o i centri di lavoro, è necessario impostare calendari del reparto produzione. Per ulteriori informazioni, vedere [Creare calendari del reparto produzione](production-how-to-create-work-center-calendars.md).  

## <a name="to-set-up-a-work-center"></a>Per impostare un'area di produzione

Di seguito viene descritto come impostare un'area di produzione. I passaggi per impostare un calendario centro di lavoro sono gli stessi ad eccezione della Scheda dettaglio **Setup cicli**.  

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Aree di produzione** e quindi scegliere il collegamento correlato.  
2. Scegliere l'azione **Nuovo**.  
3. Compilare i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Nel campo **Gruppo aree di produzione** selezionare il raggruppamento di risorse di livello più alto in base a cui è organizzata l'area di produzione, se pertinente. Scegliere l'azione **Nuovo** nell'elenco a discesa.  
5. Selezionare il campo **Bloccato** se si desidera evitare che l'area di produzione venga utilizzata in qualsiasi elaborazione. In tal caso, non sarà quindi possibile registrare l'output per un articolo prodotto nell'area di produzione. Per ulteriori informazioni, vedere [Registrare l'output di produzione](production-how-to-post-output-quantity.md).
6. Nel campo **Costo Unitario Diretto** specificare il costo di produzione di un'unità di misura nell'area di produzione selezionata, escludendo altri elementi di costo. Tale valore viene spesso definito *costo diretto manodopera*.  
7. Nel campo **% costi indiretti** specificare il costo operativo generale dell'utilizzo dell'area di produzione come percentuale del costo unitario diretto. Tale importo percentuale viene aggiunto al costo diretto nel calcolo del costo unitario.  
8. Nel campo **Coeff. costi generali** specificare come importo assoluto qualunque costo non operativo, ad esempio le spese di manutenzione, dell'area di produzione.  

    Il campo **Costo Unitario** contiene il costo unitario calcolato della produzione di un'unità di misura nell'area di produzione specificata, inclusi tutti gli elementi di costo, come illustrato di seguito:  

    Costo Unitario = Costo Unitario Diretto + (Costo Unitario Diretto x % Costi Indiretti) + Coeff. Costi Generali.  

9. Nel campo **Calcolo costo unitario** specificare se basare il calcolo precedente sulla quantità di tempo utilizzata, ovvero **Ora**, o sul numero di unità prodotte, ovvero **Unità**.  
10. Selezionare il campo **Costo unitario specifico** se si desidera definire il costo unitario dell'area di produzione nella riga ciclo in cui viene utilizzato. Tale soluzione potrebbe risultare utile per le operazioni che prevedono costi delle capacità notevolmente diversi rispetto a quelli consueti per l'area di produzione specificata.  
11. Nel campo **Metodo consuntivazione** specificare se calcolare e registrare registrazione di output nell'area di produzione manualmente o automaticamente, mediante uno dei metodi seguenti.

    |Opzione|Descrizione|
    |------|-----------|
    |**Manuale**|Il consumo viene registrato manualmente nelle registrazioni di output o di produzione.|
    |**Aut. inizio**|Il consumo viene calcolato e registrato automaticamente quando l'ordine di produzione viene rilasciato.|
    |**Aut. fine**|Il consumo viene calcolato e registrato automaticamente quando l'ordine di produzione viene chiuso.|

    > [!NOTE]
    > Se necessario, il metodo consuntivazione selezionato qui e nella scheda **Articolo** può essere sostituito per singole operazioni, mediante la modifica delle impostazioni delle righe ciclo.

12. Nel campo **Cod. Unità di Misura** immettere l'unità di tempo utilizzata per il calcolo del costo dell'area di produzione specificata e per la programmazione della capacità.
    Per tenere costantemente sotto controllo il consumo, è necessario innanzitutto impostare un metodo di misura. Le unità immesse sono unità di base. Ad esempio, il tempo di elaborazione viene misurato in ore e minuti.

    > [!NOTE]  
    > Se si decide di utilizzare Giorni, tenere presente che un giorno equivale a 24 ore e non a 8 ore lavorative.

13. Il campo **Capacità** consente di specificare se nell'area di produzione sono disponibili più macchinari o persone che lavorano contemporaneamente. Se nell'installazione di [!INCLUDE[d365fin](includes/d365fin_md.md)] non è inclusa la funzionalità Centro di lavoro, è necessario che il valore di questo campo sia impostato su **1**.  
14. Specificare nel campo **Efficienza** la percentuale di output standard previsto prodotta effettivamente dall'area di produzione selezionata. Se si immette un valore pari a **100**, si indica che l'output effettivo dell'area di produzione corrisponde all'output standard.  
15. Selezionare la casella di controllo **Calendario consolidato** se si utilizzano anche centri di lavoro. In questo modo viene eseguito il roll up dei movimenti di calendario dai calendari centro di lavoro.  
16. Selezionare un calendario reparto produzione nel campo **Cod. calendario reparto prod.**. Per ulteriori informazioni, vedere [Creare calendari del reparto produzione](production-how-to-create-work-center-calendars.md).  
17. Il campo **Tempo in coda** consente di specificare un intervallo di tempo fisso che deve trascorrere prima di potere iniziare l'attività assegnata all'area di produzione selezionata. Si noti che il valore specificato in Tempo in coda viene aggiunto ad altri elementi di tempo non legati alla produzione, ad esempio Tempo attesa e Tempo spostamento, che possono essere definiti nelle righe ciclo mediante l'area di produzione selezionata.  

## <a name="example---different-machine-centers-assigned-to-a-work-center"></a>Esempio: diversi centri di lavoro assegnati a un'area di produzione

Quando si impostano i centri di lavoro e le aree di produzione, è importante pianificare quali capacità formeranno la capacità totale.

Se vengono assegnati diversi centri di lavoro (ad esempio, 210 tavolo da imballaggio 1, 310 cabina verniciatura etc.) a un'area di produzione, risulta importante prendere in considerazione le singole capacità dei centri di lavoro in quanto il mancato funzionamento di uno di essi può interrompere l'intero processo. I gruppi di macchine possono essere immessi in base alla loro capacità, senza essere necessariamente inclusi nella pianificazione. Disattivando il campo **Calendario consolidato** viene assegnata nel planning solo la capacità dell'area di produzione e non del centro lavoro.

Se, tuttavia, centri di lavoro uguali tra loro (ad esempio, 210 tavolo da imballaggio 1 e 220 tavolo da imballaggio 2) vengono combinati in un'area di produzione, è importante considerare l'area di produzione come la somma dei centri di lavoro assegnati. L'area di produzione verrà pertanto elencata con capacità pari a zero. Attivando il campo **Calendario consolidato**, all'area di produzione viene assegnata la capacità standard.

Se le capacità delle aree di produzione non devono contribuire a formare la capacità totale, l'efficienza deve risultare uguale a zero.

## <a name="to-set-up-a-capacity-constrained-machine-or-work-center"></a>Per impostare un centro lavoro o area di produzione con capacità-vincolata

È necessario impostare le risorse di produzione considerate critiche e contrassegnarle per l'accettazione soltanto di carichi limitati, escludendo in questo modo il carico illimitato predefinito che viene accettato da altre risorse di produzione. Una risorsa critica può essere costituita da un'area di produzione o da un centro lavoro che costituiscono strozzature nel ciclo produttivo e per i quali si desidera stabilire un limite finito di carico.

[!INCLUDE[d365fin](includes/d365fin_md.md)] non supporta il controllo della produzione o del reparto dettagliato. Consente di pianificare un utilizzo fattibile di risorse fornendo una pianificazione approssimativa, ma non consente di creare e gestire automaticamente pianificazioni dettagliate in base alle priorità o alle regole di ottimizzazione.

Nella pagina **Risorse critiche** è possibile effettuare impostazioni per evitare il sovraccarico di risorse specifiche e garantire che nessuna capacità resti senza allocazione se ciò può aumentare il tempo di completamento di un ordine di produzione. Nel campo **Smorzamento (% cap. totale)**, è possibile aggiungere il tempo di smorzamento alle risorse per ridurre al minimo la suddivisione dell'operazione. Ciò consente al sistema di programmare il carico nell'ultimo giorno possibile superando leggermente la percentuale di carico critico se ciò può ridurre il numero di operazioni che vengono suddivise.

Nella pianificazione con risorse vincolate alla capacità, il sistema garantisce che nessuna risorsa venga caricata oltre la propria capacità definita (carico critico). Questa operazione viene effettuata assegnando ogni operazione alla fascia oraria disponibile più vicina. Se la fascia oraria non è sufficiente a completare l'intera operazione, l'operazione verrà divisa in due o più parti e collocate nelle fasce orarie adiacenti disponibili.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Risorse critiche** e quindi scegliere il collegamento correlato.
2. Scegliere l'azione **Nuovo**.
3. Compilare i campi come necessario.

> [!NOTE]
> Le operazioni nelle aree di produzione o nei centri di lavoro impostati come risorse vincolate verranno sempre pianificate in modo seriale. Ciò significa che se una risorsa vincolata ha più capacità disponibili, allora tali capacità possono solo essere pianificate in sequenza e non in parallelo, come invece accade nel caso in cui l'area di produzione o il centro di lavoro non è stato impostato come risorsa vincolata. In una risorsa vincolata, il campo Capacità nell'area di produzione o nel centro di lavoro è maggiore di 1.

> Nel caso che l'operazione venga suddivisa, il tempo di setup viene assegnato una sola volta perché si presuppone che vengano apportate alcune rettifiche manuali per ottimizzare la pianificazione.

## <a name="see-also"></a>Vedi anche

[Creare calendari del reparto produzione](production-how-to-create-work-center-calendars.md)  
[Impostazione della produzione](production-configure-production-processes.md)  
[Manufacturing](production-manage-manufacturing.md)  
[Pianif.](production-planning.md)  
[Magazzino](inventory-manage-inventory.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
