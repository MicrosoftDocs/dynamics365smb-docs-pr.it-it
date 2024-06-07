---
title: Consolidare i saldi per un'azienda che è cliente e fornitore
description: Descrive come consolidare i saldi per un cliente che è anche un fornitore.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment process, cash receipt'
ms.search.form: '5052, 21, 5050'
ms.date: 10/11/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="consolidate-balances-for-a-company-that-is-a-customer-and-a-vendor"></a>Consolidare i saldi per un'azienda che è cliente e fornitore
Un'azienda con cui fai affari potrebbe essere sia un cliente che un fornitore. In tal caso, puoi evitare di effettuare pagamenti o ricevute non necessari e forse risparmiare sulle commissioni di transazione, consolidando i saldi di clienti e fornitori dell'azienda. Il consolidamento confronta i saldi dell'azienda come fornitore e come cliente, quindi compensa l'importo in modo che il saldo del cliente o del fornitore rimanga, a seconda dell'importo più alto. 

Per consolidare i saldi, è necessario prima collegare le società cliente e fornitore tramite un contatto di tipo **Società**. Un cliente o un fornitore può avere un solo contatto di tipo **Società**. Per ulteriori informazioni, vedi [Creare contatti](marketing-create-contact-companies.md).

Dopo aver collegato le società, la pagina **Scheda cliente** offre il campo **Saldo come fornitore** e la pagina **Scheda fornitore** include il campo **Saldo come cliente**.

Sebbene non sia un requisito, le società del cliente e del fornitore sono in genere la stessa persona giuridica. 

## <a name="before-you-start"></a>Operazioni preliminari
Prima di consolidare i saldi, specifica alcune impostazioni nella pagina **Setup marketing**. 

* Nella Scheda dettaglio **Interazioni** devi specificare i codici delle relazioni commerciali nei campi **Clienti** e **Fornitori**. [!INCLUDE[prod_short](includes/prod_short.md)] utilizza queste informazioni per determinare il tipo di relazione da visualizzare per i contatti. 
* Opzionale: nella Scheda dettaglio **Duplicati** attiva o disattiva la ricerca di duplicati. Per impostazione predefinita, la ricerca di duplicati è attivata. Per ulteriori informazioni, vedi [Gestione dei duplicati](#handling-duplicates). 

## <a name="link-an-existing-customer-and-vendor-company-through-a-contact"></a>Collegare un cliente e un fornitore esistente tramite un contatto
I passaggi seguenti descrivono come collegare un cliente e un fornitore tramite un contatto.

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Cliente** o **Fornitore**, quindi scegli il collegamento correlato.
2. Scegli il cliente o il fornitore quindi l'azione **Contatto**.   
3. Scegli il contatto, quindi scegli l'azione **Collega con esistente**.
4. Scegli il tipo di entità con cui creare una relazione commerciale.
5. Compila i campi in base alle esigenze. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

## <a name="create-a-vendor-from-a-customer-or-vice-versa"></a>Creare un fornitore da un cliente o viceversa
È possibile creare un nuovo fornitore da un cliente esistente o un nuovo cliente da un fornitore. Dalle pagine **Cliente** o **Fornitore** apri la pagina **Contatto**. Scegli l'azione **Crea come**, quindi scegli l'opzione **Cliente** o **Fornitore**. 

## <a name="create-a-new-customer-or-vendor-and-link-them-through-a-vendor-or-customer-contact"></a>Creare un nuovo cliente o fornitore e collegarlo tramite un contatto fornitore o cliente
1. Crea un nuovo cliente o fornitore. Per ulteriori informazioni, vedi [Registrare nuovi clienti](sales-how-register-new-customers.md) o [Registrare nuovi clienti](sales-how-register-new-customers.md).
2. Dopo aver impostato il cliente o il fornitore, scegli l'azione **Crea** quindi scegli l'opzione **Cliente** o **Fornitore**. 

## <a name="to-consolidate-the-customer-and-vendor-balances-for-a-contact-company"></a>Per consolidare i saldi di clienti e fornitori per una società di contatto
Nella pagina **Registrazioni pagamenti**, utilizza l'azione **Saldi netti cliente/fornitore** per consolidare i saldi clienti e fornitori in un unico importo netto. L'azione crea, ma non registra, le righe di registrazione pagamenti che contengono i saldi netti.

> [!NOTE]
> Se i saldi cliente o fornitore contengono importi in valute diverse, viene creata una riga per l'importo in ciascuna valuta.

## <a name="handling-duplicates"></a>Gestione dei duplicati
Se attivi la ricerca dei duplicati nella scheda dettaglio **Duplicati** della pagina **Setup marketing** verrà visualizzato un avviso quando si modificano i valori dei campi che fanno parte dell'impostazione per le stringhe di ricerca dei duplicati. Quando viene trovato un duplicato, puoi eseguire le seguenti azioni:

* Combina i contatti duplicati in un unico contatto che è lo stesso sia per il cliente che per il fornitore utilizzando la capacità **Unisci con** della pagina **Scheda contatto**. In genere, l'unione dei contatti viene eseguita solo quando il cliente e il fornitore sono la stessa persona giuridica. Per ulteriori informazioni, vedere [Unire record duplicati](sales-how-merge-duplicate-records.md). 
* Elimina la relazione commerciale fornitore per il contatto del fornitore o del cliente, quindi utilizza l'azione **Collega a esistente** per collegare un contatto diverso.    

## <a name="see-also"></a>Vedi anche
[Vendite](sales-manage-sales.md)  
[Registrare nuovi clienti](sales-how-register-new-customers.md)  
