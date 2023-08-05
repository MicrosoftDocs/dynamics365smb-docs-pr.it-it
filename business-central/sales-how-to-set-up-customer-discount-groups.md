---
title: Impostare le categorie sconto clienti
description: Impara come impostare le categorie sconto clienti e creare sconti riga di vendita per questi gruppi.
author: rubenseishima
ms.service: dynamics365-business-central
ms.topic: article
ms.date: 06/08/2022
ms.author: a-reishima
---
# Impostare le categorie sconto clienti

È possibile definire gli sconti riga di vendita per un gruppo di clienti invece di applicarli singolarmente.

Le **categorie sconto clienti** lavorano in modo simile ai [gruppi di prezzi clienti](sales-how-to-set-up-customer-price-groups.md) ma possono essere combinate con le categorie sconto articoli per impostare rapidamente sconti riga su molti articoli per clienti selezionati.

## Creare righe sconto di vendita per un gruppo di clienti

1. Scegli la ![lampadina che apre la funzione Dimmi 1](media/ui-search/search_small.png "Dimmi cosa vuoi fare"). , immetti **Gruppi sconto cliente** e poi scegliere il link relativo.
2. Sulla pagina **Gruppi sconto cliente** seleziona **Nuovo** per creare un nuovo gruppo di sconti e assegnagli un nome sotto la colonna **Codice** e aggiungi una descrizione.
3. Seleziona l'azione **Naviga** e scegli **Sconti riga vendita**.
4. Compila la colonna **Codice vendita** con il gruppo di sconti creato nella pagina precedente.
5. Immetti le informazioni nei campi **Tipo** (Articolo o Gruppo sconti articolo), **Codice**, **Codice unità di misura**, e **% Sconto Riga**.
6. Se il gruppo di clienti deve acquistare una quantità minima per raggiungere la percentuale di sconto, compila il campo **Quantità minima**.
7. Se necessario, immetti la **Data inizio** e la **Data fine** per il gruppo di sconti.
8. Se pertinente, puoi anche specificare il **Codice valuta** o il **Codice variante** dopo la [personalizzazione delle colonne](ui-personalization-user.md).

Ripetere i passaggi da 4 a 8 per ciascun articolo o gruppo di sconti articolo per cui vuoi creare uno sconto riga vendita.

## Assegnare un cliente a un gruppo di sconti

Dopo aver impostato i gruppi di sconti cliente, puoi inserire i codici dei gruppi di sconti cliente sulle schede clienti.

1. Scegli la ![lampadina che apre la funzione Dimmi 1](media/ui-search/search_small.png "Dimmi cosa vuoi fare"). , immetti **Clienti**, quindi scegli il collegamento correlato.
2. Aprite la **scheda cliente** per un cliente che deve far parte di un gruppo di sconti cliente.
3. Nella scheda dettaglio **Fatturazione**, nel campo **Gruppo sconti cliente**, seleziona il codice gruppo.

## Vedere anche

[Vendite](sales-manage-sales.md)  
[Setup Vendite](sales-setup-sales.md)  
[Registrazione di prezzi speciali e sconti](sales-how-record-sales-price-discount-payment-agreements.md)  
[Impostazione di gruppi di prezzi dei clienti](sales-how-to-set-up-customer-price-groups.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
