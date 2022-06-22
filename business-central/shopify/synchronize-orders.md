---
title: Sincronizzare ed evadere gli ordini di vendita
description: Configura ed esegui l'importazione e l'elaborazione dell'ordine cliente da Shopify.
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: 4e8d640f6de61d642037a55fdfeb09e32f197a96
ms.sourcegitcommit: fb43bc843be4ea9c0c674a14945df727974d9bb9
ms.translationtype: HT
ms.contentlocale: it-CH
ms.lasthandoff: 05/27/2022
ms.locfileid: "8809031"
---
# <a name="synchronize-and-fulfill-sales-orders"></a>Sincronizzare ed evadere gli ordini cliente

Questo articolo descrive le impostazioni e i passaggi necessari da eseguire per sincronizzare ed evadere gli ordini cliente.

## <a name="set-import-of-orders-on-the-shopify-shop-card"></a>Imposta l'importazione di ordini nella scheda del punto vendita Shopify

Un ordine Shopify regolare può avere importi extra in aggiunta, come spese di spedizione o, se abilitate, mance. Questi importi verranno registrati direttamente nei conti CoGe. Scegli il conto Co.Ge. da utilizzare per transazioni specifiche:

- **Conto costo spedizione**
- **Conto buono regalo venduto**, per ulteriori informazioni, vedi [Buono regalo](synchronize-orders.md#gift-cards).
- **Conto mance**  

Abilita **Creazione automatica degli ordini** per creare automaticamente documenti di vendita in [!INCLUDE[prod_short](../includes/prod_short.md)] una volta importato l'ordine Shopify.
Il documento di vendita in[!INCLUDE[prod_short](../includes/prod_short.md)] contiene un collegamento all'ordine Shopify. Se selezioni il campo **Nr. ordine Shopify nella riga documento**, queste informazioni verranno ripetute nelle righe di vendita di tipo *Commento*.

Nel campo **Origine area fiscale**, è possibile definire la priorità su come selezionare il codice area fiscale o il gruppo di registrazione attività IVA in base all'indirizzo. Questo passaggio è rilevante per i paesi con imposta sulle vendite, ma può essere utilizzato per i paesi con IVA. Per ulteriori informazioni, vedere [Note sulle imposte](synchronize-orders.md#tax-remarks).

### <a name="shipment-method-mapping"></a>Mapping metodo spedizione

**Codice metodo di spedizione** per documenti di vendita importati da Shopify può essere compilato automaticamente. Devi configurare **Mapping metodo di spedizione**.

1. Vai alla ![lampadina che apre la funzione Dimmi](../media/ui-search/search_small.png "Dimmi cosa vuoi fare") della ricerca. icona, immetti **Punto vendita Shopify**, quindi scegli il collegamento correlato.
2. Seleziona il punto vendita per il quale desideri definire il mapping per l'apertura della pagina **Scheda del punto vendita Shopify**.
3. Scegli l'azione **Mapping metodo di spedizione**. I record per i metodi di spedizione definiti nelle impostazioni [**Spedizione**](https://www.shopify.com/admin/settings/payments) nel tuo **Amministratore Shopify** vengono creati automaticamente.
4. Nel campo **Nome**, puoi vedere il nome del metodo di spedizione da Shopify.
5. Immetti il **Codice metodo di spedizione** con il metodo di spedizione corrispondente in [!INCLUDE[prod_short](../includes/prod_short.md)].

> [!NOTE]  
> Se più spese di spedizione sono associate a un ordine cliente; solo uno verrà selezionato come metodo di spedizione e assegnato al documento di vendita.

### <a name="payment-method-mapping"></a>Mapping metodo di pagamento

Per compilare il **Codice metodo di pagamento** per documenti di vendita importati da Shopify automaticamente, è necessario configurare **Mapping metodo di pagamento**.

1. Vai alla ![lampadina che apre la funzione Dimmi](../media/ui-search/search_small.png "Dimmi cosa vuoi fare") della ricerca. icona, immetti **Punto vendita Shopify**, quindi scegli il collegamento correlato.
2. Seleziona il punto vendita per il quale desideri definire il mapping per l'apertura della pagina **Scheda del punto vendita Shopify**.
3. Scegli l'azione **Mapping metodo di pagamento**.
4. Nei campi **Gateway** e **Società emittente carte di credito**, immetti il nome del metodo di pagamento da Shopify. Il record viene creato automaticamente quando importi gli ordini shopify.
5. Immetti il **Codice metodo di pagamento** con il metodo di pagamento corrispondente in [!INCLUDE[prod_short](../includes/prod_short.md)].
6. Imposta la **Priorità** per i casi in cui il cliente utilizza più mezzi di pagamento. Il metodo di pagamento con la priorità più alta viene selezionato nel documento di vendita. Se entrambi i metodi di pagamento hanno la stessa priorità, viene utilizzato il metodo di pagamento con l'importo più alto.

## <a name="run-order-synchronization"></a>Eseguire la sincronizzazione degli ordini

Di seguito viene descritto come importare e aggiornare gli ordini di vendita.

> [!NOTE]  
> Gli ordini archiviati in Shopify non possono essere importati. Disattiva **Archivia automaticamente l'ordine** nella sezione **Elaborazione dell'ordine** delle impostazioni **Checkout** in **Amministratore Shopify** per verificare che tutti gli ordini vengano importati in [!INCLUDE[prod_short](../includes/prod_short.md)]. Se devi importare ordini archiviati, usa l'azione **Annulla l'archiviazione degli ordini** nella pagina [Ordini](https://www.shopify.com/admin/orders) di Amministratore Shopify.

1. Vai alla ![lampadina che apre la funzione Dimmi](../media/ui-search/search_small.png "Dimmi cosa vuoi fare") della ricerca. icona, immetti **Punto vendita Shopify**, quindi scegli il collegamento correlato.
2. Seleziona il punto vendita per il quale desideri importare gli ordini per l'apertura della pagina **Scheda del punto vendita Shopify**.
3. Scegliere l'azione **Ordini**.
4. Scegli l'azione **Sincronizza ordini da Shopify**.
5. Definisci i filtri sugli ordini secondo necessità. Ad esempio, puoi importare ordini interamente pagati o quelli con un livello di rischio basso.
6. Scegli il pulsante **OK**.

In alternativa, puoi cercare il processo batch **Sincronizza ordini da Shopify**.

È possibile pianificare l'attività da eseguire in modo automatizzato. Per ulteriori informazioni, vedi [Programmare le attività ricorrenti](background.md#to-schedule-recurring-tasks).

## <a name="review-imported-orders"></a>Esaminare gli ordini importati

Una volta completata l'importazione, puoi esplorare l'ordine Shopify e trovare tutte le informazioni relative. Ad esempio, trova le transazioni di pagamento, i costi di spedizione, il livello di rischio o le evasioni se l'ordine è già stato evaso in Shopify. Puoi anche vedere la conferma di ogni ordine inviata al cliente scegliendo l'azione **Pagina di stato Shopify**.

> [!NOTE]  
> Puoi accedere alla finestra **Ordini Shopify** direttamente e vedrai gli ordini con lo stato *aperto* di tutti i punti vendita Per rivedere gli ordini completati, è necessario aprire la pagina **Ordini Shopify** dalla specifica finestra **Scheda del punto vendita Shopify**.

## <a name="create-sales-documents-in-business-central"></a>Creare documenti di vendita in Business Central

Se l'opzione **Creazione automatica ordini** è abilitata in **Scheda del punto vendita Shopify**, il[!INCLUDE[prod_short](../includes/prod_short.md)] tenta di creare un documento di vendita una volta importato l'ordine. Se durante il processo si verificano problemi, ad esempio se manca un cliente o un prodotto, dovrai risolvere il problema. Quindi puoi provare a creare di nuovo l'ordine cliente.

### <a name="to-create-sales-documents"></a>Per creare i documenti di vendita

1. Vai alla ![lampadina che apre la funzione Dimmi](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") della ricerca. icona, immetti **Punto vendita Shopify**, quindi scegli il collegamento correlato.
2. Seleziona il punto vendita per il quale desideri sincronizzare gli ordini per l'apertura della pagina **Scheda del punto vendita Shopify**.
3. Scegliere l'azione **Ordini**.
4. Seleziona l'ordine per il quale desideri creare un documento di vendita e scegli l'azione **Crea documenti di vendita**.
5. Selezionare **Sì**.

Se l'ordine Shopify richiede l'evasione, l'**Ordine di vendita** sarà creato. Per gli ordini Shopify completamente evasi, come gli ordini che contengono solo un buono regalo o che sono già gestiti in Shopify, la **Fattura di vendita** viene creata.

Viene ora creato un documento di vendita che può essere gestito utilizzando le funzionalità di [!INCLUDE[prod_short](../includes/prod_short.md)] standard.

### <a name="manage-missing-customers"></a>Gestire i clienti mancanti

Se le tue impostazioni impediscono la creazione automatica di un cliente e non è possibile trovare un cliente esistente corretto, assegnerai un cliente a un ordine Shopify manualmente. Sono disponibili alcune opzioni:

- Puoi assegnare **Nr. cliente di vendita** direttamente nell'**ordine Shopify** scegliendo un cliente dall'elenco dei clienti esistenti.
- È possibile selezionare un codice modello cliente, creare e assegnare il cliente tramite l'azione **Crea nuovo cliente** nell'**ordine Shopify**.
- È possibile mappare il cliente esistente al relativo **cliente Shopify** nella finestra **Clienti Shopify** e quindi scegliere l'azione **Trova mapping** nell'**ordine Shopify**.

### <a name="tax-remarks"></a>Note sulle imposte

Mentre l'ordine Shopify importato contiene informazioni sulle imposte, queste vengono ricalcolate quando si crea un documento di vendita. Il ricalcolo rende importante che le impostazioni IVA/imposta siano corrette in [!INCLUDE[prod_short](../includes/prod_short.md)].

- Tasse/aliquote IVA multiple sui prodotti. Ad esempio, alcune categorie di prodotti sono soggette a aliquote fiscali ridotte. Tali elementi devono esistere in [!INCLUDE[prod_short](../includes/prod_short.md)] ed essere mappati ai prodotto Shopify. In caso contrario, con la creazione automatica degli articoli mancanti, verrà utilizzato il gruppo di registrazione dei prodotti IVA.

- Aliquote fiscali dipendenti dall'indirizzo. Usa il campo **Priorità area fiscale** insieme alla tabella **Modelli per clienti** per sovrascrivere la logica standard che riempie **Codice area Fiscale** nel documento di vendita. Il campo **Priorità area fiscale** specifica la priorità da cui la funzione dovrebbe prendere le informazioni su paese/area geografica e stato/provincia. Quindi il record corrispondente nei modelli cliente Shopify viene trovato e **Codice area fiscale**, **debito fiscale** e **Cat. Reg. Business IVA** viene utilizzata quando viene creato un documento di vendita.

## <a name="synchronize-shipments-to-shopify"></a>Sincronizzare le spedizioni con Shopify

Quando un ordine cliente creato da un ordine Shopify viene spedito, è possibile sincronizzare le spedizioni a Shopify.

1. Vai alla ![lampadina che apre la funzione Dimmi](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") della ricerca. icona, immetti **Sincronizza spedizioni con Shopify**, quindi scegli il collegamento correlato.
2. Definisci i filtri sulle spedizioni secondo necessità. Ad esempio, puoi aggiornare la spedizione registrata in una data specifica.
3. Scegli il pulsante **OK**.

L'ordine in Shopify sarà contrassegnato come evaso. Il cliente riceve automaticamente un messaggio e-mail o SMS di avviso di spedizione. Se sulla spedizione sono specificati un agente di spedizione e un codice di tracciabilità, le informazioni di tracciabilità sono incluse nell'e-mail.

> [!NOTE]  
> Ricordati di eseguire **Sincronizza ordini da Shopify** per aggiornare lo stato di evasione dell'ordine in [!INCLUDE[prod_short](../includes/prod_short.md)]. La funzionalità del connettore archivia anche gli ordini completamente pagati ed evasi in entrambi Shopify e in [!INCLUDE[prod_short](../includes/prod_short.md)] purché le condizioni siano soddisfatte.

### <a name="shipping-agents-and-tracking-url"></a>Agenti di spedizione e URL di tracciamento

Se il documento **Spedizione vendita registrate** contiene **sodice Spedizioniere** e/o **Numero di tracciabilità del pacco**, queste informazioni saranno inviate a Shopify e al cliente finale nell'e-mail di conferma della spedizione.

La società di tracciamento viene popolata in base al record dello spedizioniere con le seguenti priorità (dalla più alta alla più bassa):

- **Società tracciabilità Shopify**
- **Nome**
- **Codice**

Se il campo **URL tracciabilità pacchetto** è compilato per il record dello spedizioniere, la conferma della spedizione conterrà anche un URL di tracciamento.

## <a name="gift-cards"></a>Buoni regalo

Nel punto vendita Shopify puoi vendere buoni regalo, che possono essere successivamente utilizzati per pagare prodotti reali.

Quando si tratta di buoni regalo, è importante inserire un valore nel campo **Conto buono regalo venduto** nella finestra **Scheda punto vendita Shopify**. Il buono regalo venduto verrà sincronizzato insieme agli ordini in linea. Con l'ordine verrà importato anche un buono regalo applicato, ma ora come transazione. Si noti che il buono regalo non riduce l'importo da fatturare.

Per rivedere i buoni regalo emessi e applicati, scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") icona, immetti **Buoni regalo**, quindi scegli il collegamento correlato.

## <a name="transactions"></a>Transazioni

Le operazioni di pagamento avvenute su Shopify sono sincronizzate insieme agli ordini e possono essere visualizzate da *Ordine Shopify*.

Per rivedere tutte le transazioni, scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") icona, immetti **Transazioni** e scegli il collegamento correlato.

## <a name="payouts"></a>Pagamenti

Se nel tuo store sono abilitati i pagamenti Shopify, riceverai i pagamenti tramite *Pagamenti Shopify* quando un cliente paga utilizzando i pagamenti e i checkout accelerati Shopify.

1. Vai alla ![lampadina che apre la funzione Dimmi](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") della ricerca. icona, immetti **Punto vendita Shopify**, quindi scegli il collegamento correlato.
2. Seleziona il punto vendita per il quale desideri sincronizzare i pagamenti per l'apertura della pagina **Scheda del punto vendita Shopify**.
3. Scegliere l'azione **Sincronizza pagamenti**.

Per rivedere tutti i pagamenti, scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") icona, immetti **Pagamenti** e scegli il collegamento correlato.

## <a name="see-also"></a>Vedi anche

[Iniziare a utilizzare il connettore per Shopify](get-started.md)  