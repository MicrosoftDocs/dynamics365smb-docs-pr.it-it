---
title: Introduzione a Gestione assistenza di Contoso Coffee
description: In questo articolo vengono presentati i dati dimostrativi di Consoso Coffee per Gestione assistenza.
author: andreipanko
ms.author: andreipa
ms.topic: how-to
ms.date: 11/27/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="introduction-to-contoso-coffee-service-management"></a>Introduzione a Gestione assistenza di Contoso Coffee

Contoso Coffee è un'azienda fittizia che produce caffettiere di consumo e commerciali. Le app **Contoso Coffee** per Business Central aggiungono i dati demo che puoi usare per imparare a usare le funzionalità di Gestione assistenza in Business Central.

Questa app fornisce diversi elementi che vengono utilizzati per le procedure dettagliate principali:

- Risorse con competenze assegnate
- Articoli configurati per creare articoli in assistenza
- Articoli in prestito

> [!IMPORTANT]
> Prima di eseguire uno qualsiasi degli scenari per Contoso Coffee, registra le righe di registrazione articolo con i saldi di apertura. Per ulteriori requisiti, vedi la sezione [Impostare i dati di Contoso Coffee](#set-up-contoso-coffee-service-management-data).
>
> 
## <a name="set-up-contoso-coffee-service-management-data"></a>Impostare i dati di Gestione assistenza di Contoso Coffee

[!INCLUDE [contoso-coffee-app-install](../../includes/contoso-coffee-app-install.md)]

Una volta installate le app pertinenti, vai alla pagina [Strumento demo Contoso](https://businesscentral.dynamics.com/?page=5194) in [!INCLUDE [prod_short](../../includes/prod_short.md)], seleziona la riga *Modulo di assistenza* e utilizza l'azione **Configura** per preparare i moduli. Nella seguente tabella vengono illustrate le impostazioni:  

|Campo  |Descrizione  |
|---------|---------|
|**Nr. cliente**  |Il cliente da utilizzare per gli scenari nelle operazioni di vendita.|
|**N. fornitore**  |Il fornitore da utilizzare per tutti gli scenari nelle operazioni di acquisto.|
|**Nr. articolo 1**  |L'articolo da utilizzare per gli scenari di riparazione e manutenzione.|
|**Nr. articolo in assistenza 1**  |L'articolo da utilizzare nello scenario di riparazione.|
|**Nr. articolo in assistenza 2**  |L'articolo da utilizzare nello scenario di riparazione.|
|**Nr. risorsa 1**  |La risorsa da utilizzare per gli scenari relativi a contratti.|
|**Nr. risorsa 2**  |La risorsa da utilizzare per gli scenari relativi a problemi in garanzia.|
|**Ubicazione servizio** |Specifica il warehouse da usare per le operazioni di assistenza. L'impostazione predefinita è *PRINCIPALE*, ma puoi modificarla in base alle tue esigenze.|

Quando sei pronto, scegli l'azione **Crea dati demo**. Occorrono alcuni minuti per aggiungere i dati al database sottostante, ma poi sei pronto per eseguire i vari scenari.  

## <a name="scenarios"></a>Scenari

I dati demo di Contoso Coffee attualmente supportano i seguenti scenari di assistenza per test e formazione:

1. Crea un ordine di assistenza per richieste di riparazione ad hoc, inserisci e ricevi prestiti, registra il tempo e fattura i clienti con [Procedura dettagliata degli ordini di assistenza per articoli in assistenza](service-basic-flow-order.md)
2. Crea contratti di assistenza, genera ordini di assistenza, fattura le tariffe dei contratti e assegna le risorse con [Procedura dettagliata dei contratti di assistenza per articoli in assistenza](service-contract-flow.md)

Leggi i passaggi per ogni scenario nell'articolo pertinente.  

> [!IMPORTANT]
> Le procedure dettagliate di assistenza richiedono che l'esperienza utente sia impostata su **Premium** nella pagina **Informazioni società**.


## <a name="see-also"></a>Vedere anche

[Assistenza](../../service-service.md)
