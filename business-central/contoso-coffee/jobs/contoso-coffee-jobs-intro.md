---
title: Introduzione a Gestione progetti di Contoso Coffee
description: In questo articolo vengono presentati i dati dimostrativi di Consoso Coffee per Commesse e Gestione progetti.
author: andreipanko
ms.author: andreipa
ms.topic: how-to
ms.date: 05/31/2023
ms.custom: bap-template
---

# Introduzione a Commesse e Gestione progetti di Contoso Coffee

Contoso Coffee è un'azienda fittizia che produce caffettiere di consumo e commerciali. Le app **Contoso Coffee** per Business Central aggiungono dati demo che puoi usare per imparare a usare le funzionalità Commesse e Gestione progetti in Business Central.

Questa app fornisce diversi elementi che vengono utilizzati per le procedure dettagliate principali:

- Risorse con competenze e zone assegnate
- Articoli configurati per creare articoli in assistenza

> [!IMPORTANT]
> Prima di eseguire uno qualsiasi degli scenari per Contoso Coffee, registra le righe di registrazione articolo con i saldi di apertura. Per ulteriori requisiti, vedi la sezione [Impostare i dati di Contoso Coffee](#set-up-contoso-coffee-jobs-and-project-management-data).
>
> 
## Configurare dati di Commesse e Gestione progetti di Contoso Coffee

[!INCLUDE [contoso-coffee-app-install](../contoso-coffee-app-install.md)].

Una volta installate le app pertinenti, vai alla pagina [Dati demo commesse Contoso Coffee](https://businesscentral.dynamics.com/?page=4767) in [!INCLUDE [prod_short](../../includes/prod_short.md)] e modifica le impostazioni predefinite in base alle tue esigenze. Nelle seguenti tabelle vengono illustrate le impostazioni:  

|Campo  |Descrizione  |
|---------|---------|
|**Anno di inizio** |Specifica il primo anno da usare per i dati dimostrativi di Contoso Coffee. A seconda della configurazione dell'azienda, l'anno può essere un anno solare o un anno fiscale.|
|**Nr. cliente**  |Il cliente da utilizzare per gli scenari nelle operazioni di vendita.|
|**Nr. articolo 1**  |L'articolo da utilizzare per gli scenari relativi a contratti.|
|**Nr. articolo 2**  |L'articolo da utilizzare per gli scenari relativi a problemi in garanzia.|
|**Risorsa locale nr. 1**  |La risorsa da utilizzare per gli scenari relativi a contratti.|
|**Risorsa remota nr. 1**  |La risorsa da utilizzare per gli scenari relativi a problemi in garanzia.|
|**Cat. Reg. Cliente**|Specifica un codice aziendale per clienti nazionali. I codici aziendali vengono utilizzati durante la registrazione delle transazioni. |
|**Categoria registrazione business generale clienti**|Specifica un codice aziendale per clienti nazionali. I codici aziendali vengono utilizzati durante la registrazione delle transazioni. |
|**Nazionale - Categoria registrazione business generale**|Specifica un codice aziendale per clienti e fornitori nazionali. I codici aziendali vengono utilizzati durante la registrazione delle transazioni. |
|**Rivendita - Categoria registrazione magazzino**    |Specifica un codice per gli articoli che devono essere utilizzati per la registrazione della vendita.|
|**Vendita al dettaglio - Categoria registrazione articoli/servizi**    |Specifica un codice per gli articoli che devono essere utilizzati per la registrazione della vendita al dettaglio.|
|**Cat. reg. art./serv. IVA**    |Specifica un codice prodotto IVA per articoli per la registrazione dell'IVA, se l'IVA è abilitata.|
|**Fattore prezzo**     |Specifica un fattore per convertire un prezzo da USD/EUR nella valuta locale. *1* significa che il prezzo è lo stesso in qualsiasi valuta. Un numero alto viene utilizzato per ottenere il prezzo nella valuta locale. |
|**Precisione arrotondamento**  |Definisce il modo in cui le quantità di consumo calcolate vengono arrotondate una volta immesse nelle righe di registrazione consumi. Le quantità minori di 0,5 verranno arrotondate per difetto. Le quantità uguali a maggiori di 0,5 saranno arrotondate per eccesso.|

Quando sei pronto, scegli l'azione **Crea dati demo**. Occorrono alcuni minuti per aggiungere i dati al database sottostante, ma poi sei pronto per eseguire i vari scenari.  

## Vedere anche
