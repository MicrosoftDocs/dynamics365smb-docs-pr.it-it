---
title: Modificare l'importo annuo dei contratti di assistenza o delle offerte di contratto
description: È possibile modificare l'importo che verrà fatturato annualmente per i contratti di assistenza o le offerte di contratto.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Modificare l'importo annuo dei contratti di assistenza o delle offerte di contratto
È possibile modificare l'importo annuo del contratto di assistenza o dell'offerta di contratto per correggere l'importo da fatturare annualmente.  

## Per modificare l'importo annuo del contratto di assistenza o dell'offerta di contratto  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Contratti assistenza** o **Offerte contratto assistenza**, quindi seleziona il collegamento correlato.  
2. Scegliere l'offerta di contratto o il contratto.  
3. Scegliere l'azione **Apri contratto** per aprire il contratto o l'offerta di contratto per la modifica.  
4. Scegliere la casella di controllo **Permetti differenza importo** se si desidera modificare l'importo annuo e ripartire manualmente la differenza dell'importo annuo nelle righe di contratto. In altrernativa, deselezionare la casella di controllo per ripartire automaticamente la differenza dell'importo annuo nelle righe di contratto dopo la modifica dell'importo annuo.  
5. Modificare il contenuto del campo **Importo Annuo**. Non è possibile firmare, ovvero convertire in un contratto di assistenza se si utilizza un'offerta di contratto, né bloccare un contratto di assistenza se l'importo annuo è negativo. Se si azzera l'importo annuo, il contenuto del campo **Periodo di Fatturazione** deve essere **Nessuno** quando si firma o si blocca il contratto di assistenza.  
6. A seconda che la casella di controllo **Permetti differenza importo** sia selezionata o meno, eseguire la ripartizione manuale o automatica della differenza di importo annuo. Le righe di contratto verranno aggiornate in modo che il valore del campo **Importo annuo calcolato** sia uguale al nuovo importo annuo.  

## Differenze di distribuzione tra gli importi annui nuovo e calcolato
Se si modifica l'importo annuo di un contratto di assistenza o dell'offerta di contratto, è possibile ripartire la differenza tra il nuovo importo annuo e l'importo annuo calcolato nelle righe di contratto. Esistono tre modi ripartire gli importi:

* Ripartizione livellata  
* Ripartizione basata sugli importi riga  
* Ripartizione basata sul margine

### Ripartizione livellata
Se si modifica l'importo annuo del contratto di assistenza o dell'offerta di contratto, è possibile che sia necessario ripartire la differenza tra il nuovo importo annuo e l'importo annuo calcolato nelle righe di contratto. La ripartizione livellata è uno dei metodi di ripartizione automatica che consente di ripartire equamente la differenza degli importi annui nuovo e calcolato tra gli importi delle righe nelle righe di contratto. I passaggi riportati di seguito descrivono la procedura di ripartizione.  

1. La differenza tra il nuovo valore del campo **Importo annuo** e il valore del campo **Importo annuo calcolato** viene divisa per il numero delle righe di contratto presenti nel contratto di assistenza o nell'offerta di contratto.  
2. Il valore del campo **Importo Riga** viene aggiornato aggiungendo il risultato dell'operazione precedente.  
3. Il contenuto dei campi **Importo sconto riga**, **% sconto riga** e **Margine** viene aggiornato rispetto al nuovo valore del campo **Importo riga** nel modo seguente.   
    * Importo Sconto Riga = Valore Riga - Importo Riga  
    * % sconto riga = Importo sconto riga / Valore riga * 100  
    * Margine = Importo Riga - Costo Riga  

 I passaggi vengono ripetuti per ogni riga di contratto.  

#### Esempio  
La casella di controllo **Permetti differenza importo** non viene selezionata nel contratto di assistenza contenente tre righe di contratto con tali informazioni.  

|Articolo|Costo Riga|Valore Riga|% Sconto Riga|Importo Sconto Riga|Importo Riga|Margine|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Articolo 1|30,00|40,00|0.00|0.00|40,00|10,00|  
|Articolo 2|40,00|50.00|10,00|5.00|45.00|5.00|  
|Articolo 3|50.00|70.00|10,00|7.00|63.00|13.00|  

Il valore del campo **Importo annuo** è uguale al contenuto del campo **Importo annuo calcolato**, che è sempre impostato sulla somma degli importi delle righe. In questo caso equivale a 40 + 45 + 63 = 148.  

Se si imposta il valore di **Importo annuo** su 139, viene calcolato l'importo da aggiungere a ogni valore del campo **Importo riga** . Questo importo viene calcolato sottraendo il valore di **Importo annuo calcolato** dal nuovo valore del campo **Importo annuo** e dividendo il risultato per il numero delle righe di contratto presenti nel contratto di assistenza. In questo caso equivarrà a (139 - 148) / 3 = -3. L'ultima cifra calcolata viene quindi aggiunta a ogni valore del campo **Importo riga** e i valori dei campi **% sconto riga**, **Importo sconto riga** e **Margine** vengono aggiornati tramite le formule riportate nella procedura descritta sopra.  

Al termine, le righe di contratto conterranno i seguenti dati.  

|Articolo|Costo Riga|Valore Riga|% Sconto Riga|Importo Sconto Riga|Importo Riga|Margine|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Articolo 1|30,00|40,00|7.50|3.00|37.00|7.00|  
|Articolo 2|40,00|50.00|16.00|8.00|42.00|2.00|  
|Articolo 3|50.00|70.00|14.29|10.00|60.00|10.00|  

### Ripartizione basata sull'importo riga
Se si modifica l'importo annuo del contratto di assistenza o dell'offerta di contratto, è possibile che sia necessario ripartire la differenza tra il nuovo importo annuo e l'importo annuo calcolato nelle righe di contratto. La ripartizione basata sull'importo riga è un metodo automatico che consente di ripartire la differenza degli importi annui nuovo e calcolato tra gli importi delle righe nelle righe di contratto. Questa ripartizione viene eseguita proporzionalmente alle quote degli importi delle righe sull'importo annuo calcolato. I passaggi riportati di seguito descrivono la procedura di ripartizione per ogni riga di contratto.  

1. Il contributo percentuale dell'importo riga viene calcolato dividendo il contenuto del campo **Importo riga** per i valori del campo **Importo annuo calcolato** in tutte le righe di contratto.  
2. Il valore del campo **Importo riga** viene aggiornato aggiungendo al valore stesso la differenza tra gli importi annui nuovo e calcolato, che viene moltiplicata per il contributo percentuale dell'importo riga.  
3. Il contenuto dei campi **Importo sconto riga**, **% sconto riga** e **Margine** viene aggiornato rispetto al nuovo valore del campo **Importo sconto riga** nel modo seguente.  

    * Importo sconto riga = Valore riga - Importo riga  
    * % sconto riga = Importo sconto riga / Valore riga * 100  
    * Margine = Importo riga - Costo riga  

I passaggi vengono ripetuti per ogni riga di contratto.  

#### Esempio  
La casella di controllo **Permetti differenza importo** non viene selezionata nel contratto di assistenza contenente tre righe di contratto con tali informazioni.  

|Articolo|Costo Riga|Valore Riga|% Sconto Riga|Importo Sconto Riga|Importo Riga|Margine|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Articolo 1|15.00|17.00|3.00|0.51|25.00|1.49|  
|Articolo 2|20,00|23.00|Nessuno|0.00|55.10|3.00|  
|Articolo 3|24.00|27.00|3.00|0.81|112.70|2.19|  

Il valore del campo **Importo annuo** è uguale al contenuto del campo **Importo annuo calcolato**, che è sempre impostato sulla somma degli importi delle righe. In questo caso equivale a 16,49 + 23,00 + 26,19 = 65,68.  

Se si imposta **Importo annuo** su 60, vengono calcolati i contributi percentuale del margine per ogni riga di contratto:  

* Articolo 1 – 5 / (5 + 5,1 + 12,7) = 0,2193 %  
* Articolo 2 – 5,1 / (5 + 5,1 + 12,7) = 0,2237  
* Articolo 3 – 12,7 / (5 + 5,1 + 12,7) = 0,557 %  

Il valore del campo **Importo riga** viene aggiornato in ogni riga del contratto mediante la formula seguente: Importo riga = Importo riga + differenza tra gli importi annui nuovo e calcolato * Contributo percentuale. Successivamente, i valori dei campi **Importo sconto riga**, **% sconto riga** e **Margine** vengono aggiornati tramite le formule descritte nella procedura riportata sopra.  

Al termine, le righe di contratto conterranno i seguenti dati.  

|Articolo|Costo Riga|Valore Riga|% Sconto Riga|Importo Sconto Riga|Importo Riga|Margine|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Articolo 1|15.00|17.00|11.41|1.94|15.06|0.06|  
|Articolo 2|20,00|23.00|8.65|1.99|21.01|1.01|  
|Articolo 3|24.00|27.00|11.37|3.07|23.93|-0,07|  

### Ripartizione basata sul margine
Se si modifica l'importo annuo del contratto di assistenza o dell'offerta di contratto, è possibile che sia necessario ripartire la differenza tra il nuovo importo annuo e l'importo annuo calcolato nelle righe di contratto. La ripartizione basata sul margine è uno dei metodi di ripartizione automatica che consente di ripartire la differenza degli importi annui nuovo e calcolato tra gli importi delle righe nelle righe di contratto. Questa ripartizione viene eseguita proporzionalmente alle relative quote di margine sul margine totale del contratto o dell'offerta di contratto. I passaggi riportati di seguito descrivono la procedura di ripartizione per ogni riga di contratto.  

1. Il contributo percentuale del margine viene calcolato dividendo il contenuto del campo **Margine** per la somma dei valori del campo **Margine** in tutte le righe di contratto.  
2. Il valore del campo **Importo Riga** viene aggiornato aggiungendo al valore stesso la differenza tra gli importi annui nuovo e calcolato, che viene moltiplicata per il contributo percentuale del margine.  
3. Il contenuto dei campi Importo sconto riga, % sconto riga e Margine viene aggiornato rispetto al nuovo valore del campo **Importo riga** nel modo seguente:  

    * Importo sconto riga = Valore riga - Importo riga  
    * % sconto riga = Importo sconto riga / Valore riga * 100  
    * Margine = Importo riga - Costo riga  

#### Esempio  
La casella di controllo **Permetti differenza importo** non viene selezionata nel contratto di assistenza contenente tre righe di contratto con tali informazioni.  

|Articolo|Costo Riga|Valore Riga|% Sconto Riga|Importo Sconto Riga|Importo Riga|Margine|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Articolo 1|20,00|25.00|0.00|0.00|25.00|5.00|  
|Articolo 2|50.00|58.00|5.00|2.90|55.10|5.10|  
|Articolo 3|100.00|115.00|2.00|2.30|112.70|12.70|  

Il valore del campo **Importo annuo** è uguale al contenuto del campo **Importo annuo calcolato**, che è sempre impostato sulla somma degli importi delle righe. In questo caso equivale a 25,00 + 55,10 + 112,70 = 192,80.  

 Se si imposta **Importo annuo** su 180, vengono calcolati i contributi percentuale del margine per ogni riga di contratto:  

* Articolo 1 – 5 / (5 + 5,1 +12,7) = 0,2193%  
* Articolo 2 – 5,1 / (5 + 5,1 + 12,7) = 0,2237  
* Articolo 3 – 12,7 / (5 + 5,1 + 12,7) = 0,557 %  

Il valore del campo **Importo riga** viene aggiornato in ogni riga del contratto mediante la formula seguente: Importo riga = Importo riga + differenza tra gli importi annui nuovo e calcolato * Contributo percentuale. Successivamente, i valori dei campi **Importo sconto riga**, **% sconto riga** e **Margine** vengono aggiornati tramite le formule del passaggio 3 della procedura descritta sopra.  

Al termine, le righe di contratto conterranno i seguenti dati.  

|Articolo|Costo Riga|Valore Riga|% Sconto Riga|Importo Sconto Riga|Importo Riga|Margine|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Articolo 1|20,00|25.00|11.24|2.81|22.19|2.19|  
|Articolo 2|50.00|58.00|9.93|5.76|52.24|2.24|  
|Articolo 3|100.00|115.00|8.20|9.43|105.57|5.57|  

## Vedi anche  
[Creare contratti e offerte di contratto di assistenza](service-how-to-create-service-contracts-and-service-contract-quotes.md)  
[Impostazione della gestione assistenza](service-setup-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]