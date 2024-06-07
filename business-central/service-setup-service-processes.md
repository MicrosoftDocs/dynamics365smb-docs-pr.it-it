---
title: Impostare i processi di gestione assistenza
description: Scopri su come impostare i processi che consentono di assicurarsi che i clienti siano soddisfatti dei tuoi servizi.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: 'service, number sequences, setup, warnings, fee, contracts, warranties'
ms.date: 02/27/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="configure-service-management-processes"></a>Configurare i processi di gestione assistenza

Di seguito vengono forniti alcuni esempi delle impostazioni che è possibile applicare ai processi di gestione assistenza:  
  
* Alcune impostazioni globali per vari processi, quali gli avvisi, i seguenti calcoli per gli articoli in assistenza, la spesa di valutazione iniziale, il livello di reporting di guasti da utilizzare e così via.  
* I tipi di informazioni che i tecnici devono immettere nei documenti di assistenza. Ad esempio, è possibile richiedere loro di specificare il tipo di ordine, le date di inizio e/o di fine del lavoro e il tipo di lavoro fatto.  
* Alcune impostazioni di default per i tempi di risposta e le garanzie. Sono inclusi un tempo di risposta di default per l'avvio dell'assistenza, le percentuali di sconto in garanzia per ricambi e manodopera e la durata di validità delle garanzie.  
* Impostazioni per i contratti, come il numero massimo di giorni che è possibile utilizzare per ordini di assistenza contratto, se utilizzare le causali quando viene annullato un contratto, testi standard per le descrizioni e i valori del contratto.  
* Sequenze numeriche da utilizzare per gli articoli e i documenti correlati all'assistenza.  

## <a name="to-enter-general-and-mandatory-settings"></a>Per immettere le impostazioni generali e obbligatorie

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup gestione assistenza**, quindi scegli il collegamento correlato.
2. Compila i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="set-up-service-invoice-posting-policies-for-users"></a>Impostare criteri di registrazione delle fatture di assistenza per gli utenti

Le società hanno spesso processi univoci per fatture e spedizioni. Ad esempio, i processi possono variare da una persona che registra tutto su un ordine di servizio a più dipendenti, ognuno che utilizza le proprie pagine.

Puoi utilizzare criteri di registrazione per impedire agli utenti di registrare fatture di assistenza o richiedere loro di registrare le fatture insieme alla relativa spedizione di servizi. Per impostare un criterio di registrazione nella pagina **Setup utente** nel campo **Criterio di registrazione fattura di assistenza**, scegli una delle seguenti opzioni:

* **Consentito** (predefinito): mantiene il comportamento corrente, in cui puoi scegliere le opzioni di registrazione, ad esempio **Spedizione**, **Fattura** e **Spedizione e fattura**.
* **Non consentito**: impedisce agli utenti di registrare fatture di assistenza. [!INCLUDE [prod_short](includes/prod_short.md)] mostra una finestra di dialogo di conferma che fornisce solo l'opzione **Spedizione**.
* **Obbligatorio**: consente agli utenti di registrare fatture insieme alle spedizioni di servizi. [!INCLUDE [prod_short](includes/prod_short.md)] mostra una finestra di dialogo di conferma che fornisce solo l'opzione **Spedizione e fattura**.

Questa impostazione influisce sui seguenti documenti:

* Ordini assistenza
* Spedizioni warehouse
* Fatture assistenza
* Note credito assistenza

Nella seguente tabella vengono descritti gli effetti sui differenti documenti.

|Documento  |Consenti<br>Visualizza una serie di opzioni   |Non consentito<br>Finestra di dialogo di conferma  |Obbligatorio<br>Finestra di dialogo di conferma  |
|---------|---------|---------|---------|
|Ordine assistenza     | * Spedizione<br>* Fattura<br>* Spedizione e fattura<br>* Spedizione e consumo         |* Spedizione<br>* Spedizione e consumo  |Registrare la spedizione e la fattura?         |
|Spedizione warehouse     |* Spedizione<br>* Spedizione e fattura         |Registrare la spedizione?         | Registrare la spedizione e la fattura?        |
|Fattura assistenza     | Registrare la fattura?         | Errore: impossibile registrare.       |Registrare la fattura?         |
|Nota di credito assistenza     | Registrare la nota di credito?         | Errore: impossibile registrare.        |Registrare la nota di credito?         |

> [!NOTE]
> Quando registri note di credito e fatture di assistenza, non sono disponibili opzioni di registrazione. I documenti registrano sempre insieme transazioni fisiche e finanziarie. Non puoi registrare parzialmente note di credito e fatture di assistenza.

## <a name="see-also"></a>Vedere anche

[Impostare il report dei guasti](service-how-setup-fault-reporting.md)  
[Impostare l'assegnazione delle risorse](service-how-setup-resource-allocation.md)  
[Impostare codici per servizi standard](service-how-setup-service-coding.md)  
[Impostare costi aggiuntivi per i servizi assistenza](service-how-setup-service-costs-pricing.md)  
[Impostare il troubleshooting](service-how-setup-troubleshooting.md)  
[Gestione assistenza](service-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
