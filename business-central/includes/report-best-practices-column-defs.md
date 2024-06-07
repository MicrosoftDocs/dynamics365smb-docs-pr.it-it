---
author: brentholtorf
ms.topic: include
ms.date: 04/05/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

## Procedure consigliate per utilizzare definizioni di colonna

Le definizioni di colonna non hanno una versione. Quando modifichi una definizione di colonna, la versione precedente viene sostituita quando la modifica viene salvata nel database. L'elenco seguente contiene alcune procedure consigliate per l'utilizzo delle definizioni di colonna:

- Se aggiungi una definizioni di colonna, scegli un buon codice e compila il campo Descrizione con un testo significativo mentre sai ancora per quale motivo usi la definizione di colonna. Queste informazioni aiutano i tuoi colleghi (e te stesso in futuro) a lavorare con Financial Reporting e magari a modificare la definizione di colonna.
- Prima di modificare una definizione di colonna, prendi in considerazione l'esecuzione di una copia di backup della stessa, nel caso in cui la modifica non funzioni come previsto. Puoi semplicemente copiare la definizione (dargli un nome appropriato) o esportarla. Per saperne di più, vedi [Importare o esportare le definizioni di colonna](#import-or-export-financial-report-column-definitions).
- Se hai bisogno di una nuova copia di una definizione che [!INCLUDE [prod_short](prod_short.md)] fornisce, un modo semplice di ottenerne una è creare una nuova società che contenga solo i dati di setup. Quindi, esporta la definizione e importala nella società in cui la definizione necessita di un aggiornamento.