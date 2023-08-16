---
title: Rispondere a richieste relative a dati personali degli utenti
description: Questo articolo spiega come rispondere alle richieste sui dati personali.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.date: 04/25/2023
ms.custom: bap-template
---

# Rispondere a richieste relative a dati personali degli utenti

Gli oggetti dati possono richiedere diversi tipi di azioni riguardanti i relativi dati personali. Ad esempio, ai sensi di alcune norme e regolamenti in materia di privacy, i residenti dell'UE hanno il diritto di chiedere l'esportazione, la cancellazione e la modifica dei loro dati personali. Queste richieste sono denominate *Richieste degli interessati*. Se i dati riservati sono stati classificati e si è certi della correttezza dell'operazione, un amministratore può rispondere alle richieste utilizzando le opzioni nella scheda **Privacy dati** in Gestione ruolo utente **Manager IT**. Per ulteriori informazioni sulla classificazione dei dati e sulla riservatezza dei dati in [!INCLUDE[prod_long](includes/prod_long.md)], consulta i seguenti articoli:

* [Classificazione di dati](/dynamics-nav/classifying-data?toc=/dynamics365/business-central/toc.json) 
* [Classificazione di dati riservati](admin-classifying-data-sensitivity.md)  

## Tipi di richieste

Nella tabella seguente vengono forniti esempi dei tipi di richieste a cui un amministratore può rispondere.

> [!Note]
> Sebbene forniamo le funzionalità per rispondere a questi tipi di richieste e quindi per accedere a dati personali, è responsabilità dell'utente assicurare la corretta archiviazione e classificazione dei dati personali e riservati.

|Tipo richiesta|Descrizione e risposta suggerita|
|-----|-----|
|Richieste di trasferibilità|L'interessato può presentare una richiesta di portabilità dei dati. Devi esportare i dati personali dell'interessato dai tuoi sistemi e fornirli in un formato strutturato e di uso comune. Per rispondere a queste richieste, è possibile utilizzare **Utilità privacy dei dati** per esportare dati personali in un file di Excel o in un pacchetto di configurazione di RapidStart. Con Excel, è possibile modificare i dati personali e salvarli in un formato comune leggibile da computer, ad esempio .csv o .xml. Per i pacchetti di configurazione di RapidStart è possibile configurare le tabelle di dati master e le relative tabelle che contengono dati personali. <br><br> **Nota**: quando si esportano i dati, si specifica un livello minimo di sensibilità. L'esportazione includerà il livello minimo e tutti i livelli di sensibilità sopra di esso. Ad esempio, se esporti i dati classificati come Personali, l'esportazione includerà anche dati classificati come Sensibili. <br><br>Quando si esportano dati relativi a una persona interessata, l'**Utilità privacy dei dati** cerca relazioni dirette tra l'interessato e i dati relativi all'interessato. Le relazioni indirette tra i dati relativi alla persona interessata e gli altri dati non vengono esportate automaticamente dall'**Utilità privacy dei dati**. Ad esempio, la tabella Contatto ha messo in correlazione diretta i dati di Risposte profilo contatto e la tabella Risposte profilo contatto è collegata a sua volta ai dati di Domande profilo. Se si desidera esportare anche Domande profilo, è necessario aggiungere questa tabella manualmente come una riga con i filtri appropriati nel pacchetto di configurazione creato dall'**Utilità privacy dei dati**.|
|Richieste di eliminazione|Un oggetto dati può richiedere di eliminare i relativi dati personali. Esistono svariati metodi per eliminare dati personali utilizzando le funzionalità di personalizzazione, ma la decisione e l'implementazione sono di responsabilità dell'utente. In alcuni casi, potresti scegliere di modificare direttamente i tuoi dati. Ad esempio, eliminando un contatto e quindi eseguendo il processo batch relativo all'eliminazione di interazioni annullate per il contatto. <br><br> **Nota:** se è stata specificata una data nel campo **Consenti eliminazione documenti anteriori a** nelle pagine **Setup contabilità clienti e vendite** o **Setup contabilità fornitori e acquisti**, potrebbe essere necessario modificare la data in modo da eliminare i documenti di acquisto e vendita registrati che sono stati stampati e le cui date di registrazione sono uguali o antecedenti a quella data.|
|Richieste di correzione|Un oggetto dati può richiedere di correggere dati personali inaccurati. Questa operazione può essere effettuata in vari modi. In alcuni casi, si potrebbero esportare liste in Excel per modificare in blocco più record e quindi importare i dati aggiornati. Per ulteriori informazioni, vedere [Esportazione dei dati aziendali in Excel](about-export-data.md). È inoltre possibile modificare manualmente i campi contenenti dati personali, ad esempio modificare informazioni relative a un cliente nella scheda cliente. Tuttavia, i record come i movimenti contabili generali, clienti e fiscali sono importanti. Se si archiviano dati personali nei record delle transazioni commerciali, si deve prendere in considerazione l'utilizzo delle funzionalità di personalizzazione per modificare tali dati personali.|

## Limitazione dell'elaborazione dei dati per un oggetto dati

Un oggetto dati può richiedere di interrompere temporaneamente l'elaborazione dei relativi dati personali. Per soddisfare tali richieste, è possibile contrassegnare i record come bloccati a causa della privacy. Quando un record viene contrassegnato come bloccato, non è possibile creare nuove transazioni che utilizzano quel record. Ad esempio, non è possibile creare una nuova fattura per un cliente quando il cliente o il venditore è bloccato. Per contrassegnare un oggetto dati come bloccato, aprire la scheda per l'oggetto dati, ad esempio le schede cliente, fornitore o contatto, e scegliere la casella du controllo **Bloccato dalla privacy**. Potrebbe essere necessario scegliere **Mostra di più** per visualizzare il campo.  

## Gestione delle richieste per un oggetto dati in una versione di valutazione

Alcuni tipi di dati personali fanno parte di un account Microsoft 365 e solo gli amministratori possono esportare i dati. Il processo per la gestione delle richieste degli interessati è diverso in base al tipo di tenant di [!INCLUDE[prod_short](includes/prod_short.md)].

Se si dispone di un abbonamento a pagamento per [!INCLUDE[prod_short](includes/prod_short.md)], è necessario contattare l'amministratore del tenant della propria organizzazione per inoltrare una richiesta dell'interessato. Gli amministratori dispongono di diritti e strumenti amministrativi per soddisfare le richieste di un oggetto dati.

Se ti sei registrato a [!INCLUDE[prod_short](includes/prod_short.md)] dalla pagina [Versioni di valutazione](https://trials.dynamics.com/) e stai ancora utilizzando la versione di valutazione, gli utenti possono scaricare ed esportare i propri dati nella [pagina della privacy dell'account aziendale o dell'istituto scolastico nel portale di Azure](https://portal.azure.com#blade/Microsoft_AAD_IAM/GDPRViralBlade).

Nella pagina sulla privacy per la privacy, è anche possibile chiudere il proprio account. Tuttavia, ti consigliamo di esportare ed eliminare prima tutti i dati. Eliminare il tuo account significa perdere l'accesso a [!INCLUDE[prod_short](includes/prod_short.md)].

È comunque possibile contrassegnare le persone come bloccate in base alla privacy ed esportare, modificare o eliminare le transazioni come spiegato in altre sezioni di questo articolo.  

## Esportazione dei dati da tabelle non classificate dagli oggetti dati

Devi esportare i dati non classificati in modo che vangano esportati automaticamente, ad esempio i dati dalla tabella Risposte profilo, è necessario effettuare le seguenti azioni:

* Considerare se devi davvero esportare dati supplementari che non sono direttamente correlati al contatto.
* Aggiungere manualmente la tabella e la relazione al pacchetto RapidStart ed esportarla direttamente dal pacchetto RapidStart. Generiamo un pacchetto RapidStart per te, in modo che tu possa modificarlo in tali situazioni.

## Gestione dei dati relativi ai minori

Se l'età di una persona di contatto è inferiore all'età legale stabilita dalle leggi nella propria area geografica, è possibile indicare tale condizione selezionando la casella di controllo **Minorenne** nella scheda **Contatto**. Quando si seleziona tale casella, la casella di controllo **Bloccato dalla privacy** viene selezionata automaticamente. Quando si riceve il consenso dal genitore o dal tutore legale, è possibile scegliere la casella di controllo **Consenso dei genitori ricevuto** per sbloccare il contatto. Sebbene sia possibile elaborare i dati personali dei minori, non è possibile utilizzare la funzione di profiling in Dynamics 365 Sales.

> [!Note]
> Il log modifiche consente di registrare informazioni dettagliate, ad esempio quando e da chi la casella di controllo **Consenso dei genitori ricevuto** è stata selezionata. Un amministratore può eseguire tale impostazione utilizzando la guida **Setup log modifiche** e anche scegliendo la casella di controllo **Modifica log per Consenso dei genitori ricevuto** nella scheda **Contatto**. Per ulteriori informazioni, vedere [Registrazione di modifiche](across-log-changes.md).  

### Vedere anche

[Classificazione di dati](/dynamics-nav/classifying-data?toc=/dynamics365/business-central/toc.json)  
[Classificazione di dati riservati](admin-classifying-data-sensitivity.md)  
[Esportazione dei dati aziendali in Excel](about-export-data.md)  
[Registrazione di modifiche](across-log-changes.md)  
[Richieste degli interessati](/microsoft-365/compliance/gdpr-data-subject-requests)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
