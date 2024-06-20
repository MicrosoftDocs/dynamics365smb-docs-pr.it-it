---
author: brentholtorf
ms.topic: include
ms.date: 09/21/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

Gli addetti al warehouse possono spedire e ricevere articoli non di magazzino insieme a beni fisici in ordini di vendita e di acquisto. Gli articoli non di magazzino sono beni immateriali, come assicurazioni o costi aggiuntivi.

Gli ordini di vendita e di acquisto spesso contengono vari tipi di elementi nelle righe. Ad esempio, gli ordini potrebbero includere articoli di contabilità generale, conti e cespiti. Se utilizzi documenti di warehouse per gestire articoli fisici, puoi registrare anche alcuni tipi di articoli non di magazzino. Quelli che seguono sono esempi di documenti di warehouse:

* Stoccaggi magazzino
* Carichi warehouse
* Prelievi magazzino
* Spedizioni warehouse

Per consentire agli addetti al warehouse di spedire e ricevere articoli non di magazzino, compila il campo **Registra automaticamente articoli non in mag. tramite whse.** nella pagine **Setup contabilità clienti e vendite** e **Setup contabilità fornitori e acquisti**. Il campo fornisce le seguenti opzioni:

|Opzione  |Descrizione  |
|---------|---------|
|Nessuna     |Non spedire o ricevere articoli non di magazzino.         |
|Collegato/Assegnato     | Registra gli addebiti articolo e altre righe di articoli non di magazzino assegnate o collegate ad articoli fisici. Per collegare righe non di magazzino ad articoli fisici, utilizze l'azione **Collega a riga di magazzino**.        |
|Tutto     | Registra tutte le righe non di magazzino nel documento di origine non appena almeno un articolo viene registrato dal documento di warehouse.        |

> [!NOTE]
> L'opzione **Completa** nel campo **Avviso spedizione** dell'ordine di vendita ha la priorità sulla selezione nel campo **Registra automaticamente articoli non in mag. tramite whse.** nella pagina **Setup contabilità clienti e vendite**.