---
title: Terminologia nella contabilità dei costi
description: 'In questo articolo vengono definiti i termini chiave utilizzati nella contabilità dei costi, quali chiave di allocazione e fonte di allocazione.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: 1123
ms.date: 07/25/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="terminology-in-cost-accounting"></a>Terminologia nella contabilità dei costi

In questo articolo vengono definiti i termini chiave utilizzati nella contabilità dei costi.  

## <a name="key-terms"></a>Termini chiave

 Nella tabella seguente vengono mostrate le definizioni dei termini chiave della contabilità industriale.  

|**Termine**|**Definizione**|  
|--------------|--------------------|  
|Chiave di allocazione|Una chiave di allocazione è la base utilizzata per allocare i costi. Di solito si tratta di una quantità, come i metri quadrati occupati, il numero di dipendenti o le ore di lavoro impiegate. Ad esempio, due reparti, rispettivamente con 20 e 10 impiegati, condividono i costi della mensa. I costi vengono distribuiti tra i reparti utilizzando una chiave di allocazione che rappresenta il numero di impiegati. Due terzi dei costi vengono allocati al primo reparto e un terzo dei costi al secondo reparto.|  
|Origine allocazione|L'origine di allocazione determina i costi che vengono allocati. Le assegnazioni sono definite nelle tabelle di origine e di destinazione delle allocazioni. Ogni allocazione è costituita da un'origine di allocazione e da una o più destinazioni di allocazione. Ad esempio, tutti i costi per il tipo di costo relativo al riscaldamento, che è un'origine di allocazione, possono essere allocati ai centri di costo workshop, produzione e vendite, vale a dire le tre destinazioni di allocazione.|  
|Destinazione allocazione|Le destinazioni di allocazione determinano dove i costi vengono allocati. Le assegnazioni sono definite nelle tabelle di origine e di destinazione delle allocazioni. Ogni allocazione è costituita da un'origine di allocazione e da una o più destinazioni di allocazione. Ad esempio, tutti i costi per il tipo di costo relativo al riscaldamento, che è un'origine di allocazione, possono essere allocati ai centri di costo workshop, produzione e vendite, vale a dire le tre destinazioni di allocazione.|  
|Contabilità industriale|Nella contabilità industriale vengono registrati i costi effettivi per operazioni, processi, reparti o prodotti. Questi costi vengono allocati ai centri di costo e agli oggetti di costo utilizzando metodi di allocazione costi differenti. I manager utilizzano statistiche e report, ad esempio il prospetto della distribuzione dei costi e l'analisi dei profitti e delle perdite per prendere decisioni e ridurre i costi. La contabilità industriale recupera i dati dalla contabilità generale, ma funziona in modo indipendente. Pertanto le transazioni registrate nella contabilità dei costi non influiscono sui dati presenti in contabilità generale.|  
|Tipo costo|La funzione del piano dei tipi di costo è analoga a quella del piano dei conti della contabilità generale. Spesso sono strutturati in modo simile. Pertanto è possibile trasferire il piano dei conti contabilità generale al piano dei tipi di costo e quindi modificarlo. Il piano dei tipi di costo può anche essere creato da zero.|  
|Centro di costo|I centri di costo sono molto spesso i reparti e i centri profitto che sono ampiamente responsabili dei costi e delle entrate della società. I centri di costo possono essere sincronizzati con le dimensioni della contabilità generale. È anche possibile aggiungere nuovi centri di costo e definire il loro ordinamento con subtotali.|  
|Oggetto di costo|Gli oggetti di costo sono prodotti, gruppi di prodotti o servizi di un'azienda, i beni finiti di un'azienda, che alla fine sostengono i costi. Gli oggetti di costo possono essere sincronizzati con le dimensioni della contabilità generale. È anche possibile aggiungere nuovi oggetti di costo e definire il loro ordinamento con subtotali.|  
|Allocazione costi|L'allocazione costi è un processo di assegnazione dei costi ai centri di costo o agli oggetti di costo. Ad esempio, lo stipendio del camionista del reparto vendite è allocato al centro di costo del reparto vendite. Non è necessario allocare il costo salariale ad altri centri di costo. Un altro esempio consiste nell'allocazione del costo di un sistema di computer costoso ai prodotti della società in cui viene utilizzato il sistema.|  
|Allocazione dinamica|Le allocazioni dinamiche dipendono dalle basi di allocazioni variabili, ad esempio, il numero di dipendenti di reparto o i ricavi vendite del progetto in un determinato periodo. Sono disponibili nove basi predefinite di allocazione dinamica che gli utenti possono stabilire utilizzando cinque filtri.|  
|Costo diretto|I costi diretti sono i costi che possono essere allocati direttamente a un oggetto di costo, ad esempio l'acquisto di materiale per un prodotto specifico.|  
|Costo fisso|I costi fissi sono i costi che non dipendono dal livello di beni o servizi prodotti dall'azienda. Tendono a essere collegati al tempo, ad esempio stipendi o affitti pagati ogni mese, a differenza dei costi variabili, che sono correlati a volumi e vengono pagati in base alle quantità prodotte.|  
|Costo indiretto|I costi indiretti non sono direttamente imputabili a un oggetto di costo, come una particolare funzione o un prodotto. e possono essere fissi o variabili. I costi indiretti possono essere costi per la protezione, il personale, l'amministrazione, le imposte e sono noti anche come costi generali.|  
|Livello|Il livello viene utilizzato per definire l'ordine di allocazione. Il livello è definito come numero tra 1 e 99. La registrazione di allocazione segue l'ordine dei livelli. Ad esempio, con il livello è possibile assicurarsi che, prima di allocare il workshop al veicolo e alla produzione, venga allocata l'amministrazione al workshop.|  
|Allocazione statica|Le allocazioni statiche sono basate su un insieme fisso di valori, ad esempio i metri quadri utilizzati, o su un rapporto di allocazione stabilito, quale 5:2:4.|  
|Costo operativo|I costi operativi sono le spese ricorrenti legate al funzionamento di un'azienda, di un dispositivo e di un componente.|  
|Costo generale|I costi generali si riferiscono alle spese in corso per l'attività di un'azienda. Sono tutti costi presenti nel conto economico, ad eccezione della manodopera diretta, dei materiali diretti e delle spese dirette. I costi generali includono spese di contabilità, pubblicità, ammortamento, assicurazione, interesse, spese notarili, affitto, riparazioni, forniture, imposte, fatture del telefono, spese per viaggi e trasferte e costi dei servizi pubblici.|  
|Costo variabile incrementale|Passaggio I costi variabili sono costi che cambiano drasticamente in determinati momenti perché comportano acquisti ingenti che non possono essere distribuiti nel tempo. Ad esempio, un impiegato può produrre 100 tabelle in un mese. Lo stipendio dell'impiegato è costante in un intervallo di produzione compreso tra 1 e 100 tabelle. Se la società intende produrre 110 tabelle, necessita di due impiegati. Pertanto il costo si raddoppierà.|  
|Quota|La porzione o parte allocata tra i centri di costo e gli oggetti di costo.|  
|Ponderazione statica|I costi vengono allocati in base alle chiavi di allocazione, che possono essere modificate mediante un moltiplicatore. <br />Ad esempio, due reparti, rispettivamente con 20 e 10 impiegati, condividono i costi della mensa. I costi vengono distribuiti tra i reparti utilizzando una chiave di allocazione che rappresenta il numero di impiegati che mangiano alla mensa. Nel primo reparto solo cinque dipendenti mangiano alla mensa, quindi questo reparto ha un moltiplicatore di 0,25. La base dell'assegnazione è 20 x 0,25 = 5. Il numero totale degli impiegati che mangiano nella mensa è 15. Un terzo dei costi viene allocato al primo reparto e due terzi dei costi al secondo reparto.|  
|Costo variabile|I costi variabili sono spese che cambiano proporzionalmente all'attività di un'azienda. Rappresentano la somma dei costi marginali in tutte le unità prodotte. I costi fissi e quelli variabili costituiscono i due componenti dei costi totali.|  
|Variante|Viene utilizzata una variante come etichetta personalizzata opzionale relativa alle allocazioni. Lo scopo dell'etichetta è quello di filtrare i gruppi di allocazione.|  

## <a name="see-also"></a>Vedere anche

 [Informazioni sulla contabilità industriale](finance-about-cost-accounting.md)  
 [Contabilizzazione dei costi](finance-manage-cost-accounting.md)  
 [Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
