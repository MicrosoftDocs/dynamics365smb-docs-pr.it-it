---
title: Definire criteri di registrazione fattura per gli utenti
description: Utilizza i criteri di registrazione delle fatture per controllare se un utente può registrare le fatture di vendita e acquisto.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 06/12/2024
ms.custom: bap-template
ms.search.forms: '119, 9807,'
ms.service: dynamics-365-business-central
---

# <a name="define-an-invoice-posting-policy-for-users"></a>Definire un criterio di registrazione delle fatture per gli utenti

Le aziende hanno spesso processi univoci per la registrazione di fatture di vendita e acquisto e spedizioni. Ad esempio, i processi possono variare da una persona che registra tutto su un ordine di acquisto a più dipendenti. È possibile impedire agli utenti di registrare fatture o richiedere che le fatture vengano registrate insieme a spedizioni o ricevute.

## <a name="to-specify-a-posting-policy"></a>Per specificare un criterio di registrazione

Nella pagina **Configurazione utente** nei campi **Criteri di registrazione delle fatture di vendita** e **Criteri di registrazione delle fatture di acquisto**, scegli una delle seguenti opzioni:

* **Consentito** (predefinito): mantiene il comportamento corrente, in cui un utente può scegliere l'opzione di pubblicazione da utilizzare, ad esempio **Spedizione**, **Fattura** e **Spedizione e fattura**. 
* **Proibito** - Impedisce all'utente di registrare le fatture. [!INCLUDE [prod_short](includes/prod_short.md)] mostra una finestra di dialogo di conferma che fornisce solo l'opzione **Spedisci** e **Ricevi**.
* **Obbligatorio** - Consente all'utente di registrare le fatture insieme a ricevute o spedizioni. [!INCLUDE [prod_short](includes/prod_short.md)] mostra una finestra di dialogo di conferma con le opzioni **Spedisci e fattura** o **Ricevi e fattura**.

## <a name="effect-on-documents"></a>Effetto sui documenti

La tabella seguente descrive in che modo i criteri di registrazione delle fatture influiscono sui documenti.

> [!NOTE]
> Quando registri fatture di vendita e di acquisto e note di credito, non sono disponibili opzioni di registrazione. I documenti registrano sempre insieme le transazioni fisiche e finanziarie. Non puoi registrare parzialmente fatture e note di credito.

|Documento | Opzione 1: Consenti <br>Visualizza una serie di opzioni| Opzione 2: Proibito <br>Finestra di dialogo di conferma | Opzione 3: Obbligatorio <br>Finestra di dialogo di conferma|
|--|--|--|--|
|Ordine di vendita |- Spedisci <br>- Fattura <br>- Spedisci e fattura |Registrare la spedizione? |Registrare la spedizione e la fattura?|
|Fattura di vendita|Nessuna opzione| La registrazione è vietata in base alla configurazione dell'utente|Registrare la fattura?|
|Note cred. vendita|Nessuna opzione|La registrazione è vietata in base alla configurazione dell'utente|Registrare la nota di credito?|
|Ord. reso di vendita |- Ricevi <br>- Fattura <br>- Ricevi e fattura |Registrare la ricevuta? |Registrare il carico e la fattura?|
|Prelievo inventario |- Spedisci <br>- Spedisci e fattura |Registrare la spedizione? |Registrare la spedizione e la fattura?|
|Ordine di acquisto |- Ricevi <br>- Fattura <br>- Ricevi e fattura |Registrare la ricevuta? |Registrare il carico e la fattura?|
|Fattura di acquisto|Nessuna opzione|La registrazione è vietata in base alla configurazione dell'utente|Registrare la fattura?|
|Nota di credito acquisto|Nessuna opzione|La registrazione è vietata in base alla configurazione dell'utente|Registrare la nota di credito?|
|Ord. reso di acquisto |- Spedisci <br>- Fattura <br>- Spedisci e fattura |Registrare la spedizione? |Registrare la spedizione e la fattura?|
|Stoccaggio in magazzino |- Ricevi <br>- Ricevi e fattura |Registrare la ricevuta? |Registrare la ricevuta e la fattura?|
|Spedizione warehouse |- Spedisci <br>- Spedisci e fattura | Registrare la spedizione? |Registrare la spedizione e la fattura?|

   > [!Note]
   > L'impostazione non influisce sulla registrazione delle righe di registrazioni generali in cui è possibile selezionare **Fattura** nel campo **Tipo di documento**.

## <a name="see-also"></a>Vedere anche

[Fatturare le vendite](sales-how-invoice-sales.md)  
[Registrare gli acquisti con le fatture e gli ordini di acquisto](purchasing-how-record-purchases.md)  
[Acquistare articoli per una vendita creando fatture di acquisto](purchasing-how-purchase-products-sale.md)
[Prepararsi per fare affari](ui-get-ready-business.md)  
