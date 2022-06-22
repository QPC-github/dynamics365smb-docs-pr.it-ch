---
title: Risolvere i problemi dei flussi di lavoro automatizzati
description: Scopri come risolvere i problemi di connessione tra Business Central e Power Automate quando crei un flusso di lavoro automatizzato.
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 05/12/2022
ms.author: edupont
author: jswymer
ms.openlocfilehash: b8fff95ced93e7ee2a3112969f45525532b19445
ms.sourcegitcommit: e86f0bd15604c2fb327e3182929c44a4172790c7
ms.translationtype: HT
ms.contentlocale: it-CH
ms.lasthandoff: 05/20/2022
ms.locfileid: "8786214"
---
# <a name="troubleshoot-your-prod_short-automated-workflows"></a>Risolvere i problemi dei[!INCLUDE[prod_short](includes/prod_short.md)] flussi di lavoro auomatizzati

Quando ti connetti a[!INCLUDE [prod_short](includes/prod_short.md)] insieme aPower Automate per creare flussi di lavoro automatizzati, potrebbero essere visualizzati messaggi di errore. Questo articolo fornisce soluzioni suggerite per problemi ricorrenti.

## <a name="flow-doesnt-run-on-all-records-created-or-changed"></a>Il flusso non viene eseguito su tutti i record creati o modificati

### <a name="problem"></a>Problema

Se un evento crea o modifica molti record, il flusso non viene eseguito su alcuni o tutti i record.

### <a name="possible-cause"></a>Causa possibile

Attualmente esiste un limite al numero di record che un flusso può elaborare. Se vengono creati o modificati più di 100 record entro 30 secondi, il flusso non verrà attivato.

> [!NOTE]
> Per gli sviluppatori, l'attivazione del flusso viene eseguita tramite notifiche webhook e questa limitazione è dovuta al modo in cui il connettore Business Central gestisce le notifiche `collection`. Per ulteriori informazioni, vedere [Utilizzo dei webhook in Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/api-reference/v2.0/dynamics-subscriptions#notes-for-power-automate-flows) nella Guida per sviluppatori e amministratori.

## <a name="entity-set-not-found-error"></a>Errore "Set di entità non trovato"

### <a name="problem"></a>Problema

Quando si crea un nuovo flusso Power Automate usando un trigger di approvazione [!INCLUDE[prod_short](includes/prod_short.md)], ad esempio *Quando viene richiesta l'approvazione di un documento di acquisto*, si potrebbe ricevere un messaggio di errore simile al seguente:

`Entity set not found: \<name\>`

Il segnaposto, `\<name\>` è il nome del servizio Web mancante, come *workflowWebhookSubscriptions* o *workflowPurchaseDocumentLines*.

### <a name="possible-cause"></a>Causa possibile

L'utilizzo di Power Automate per le approvazioni richiede che determinati oggetti pagina e codeunit objects vengano pubblicati come servizi Web. Per impostazione predefinita, la maggior parte degli oggetti richiesti viene pubblicata come servizi Web. In alcuni casi, tuttavia, l'ambiente potrebbe essere stato personalizzato in modo che questi oggetti non vengano più pubblicati.

### <a name="fix"></a>Correzione

Accedere alla pagina **Servizi Web** e assicurarsi che i seguenti oggetti vengano pubblicati come servizi Web. Dovrebbe esserci una voce nell'elenco per ogni oggetto, con la casella di controllo **Pubblicato** selezionata.  

|Tipo oggetto|ID oggetto|Nome oggetto|Nome servizio|
|-----------|---------|-----------|------------|
|Codeunit|  1544    |WorkflowWebhookSubscription|WorkflowActionResponse|
|Pagina|  6408|   workflowCustomers|  workflowCustomers|
|Pagina   |6406   |workflowGenJournalBatches| workflowGenJournalBatches|
|Pagina   |6407   |workflowGenJournalLines|workflowGenJournalLines|
|Pagina   |6409   |workflowItems| workflowItems|
|Pagina   |6405   |Entità riga documento di acquisto|workflowPurchaseDocumentLines|
|Pagina|  6404    |workflowPurchaseDocuments| workflowPurchaseDocuments|
|Pagina|  6403    |Entità riga documento di vendita |workflowSalesDocumentLines|
|Pagina|  6402|   workflowSalesDocuments| workflowSalesDocuments|
|Pagina|  6410    |workflowVendors|   workflowVendors|
|Pagina|  831 |workflowWebhookSubscriptions|  workflowWebhookSubscriptions|

> [!NOTE]
> Il valore **Nome servizio** deve essere esattamente quello mostrato nella tabella. Non modificare o tradurre il nome del servizio.

Per ulteriori informazioni sulla pubblicazione di servizi Web, vedere [Pubblicare un servizio Web](across-how-publish-web-service.md).

## <a name="see-also"></a>Vedi anche

[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)] in un flusso di lavoro automatizzato](across-how-use-financials-data-source-flow.md)  
[Workflow](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]