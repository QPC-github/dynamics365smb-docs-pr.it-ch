---
title: Come esportare e importare workflow | Microsoft Docs
description: "Per trasferire i workflow ad altri database di Business Central, ad esempio per risparmiare tempo durante la creazione di nuovi workflow, è possibile esportare e importare i workflow."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 3491a8cf322c4a1ac5385c09e05ec6cd828b4c53
ms.contentlocale: it-ch
ms.lasthandoff: 03/22/2018

---
# <a name="export-and-import-workflows"></a>Importa ed esporta workflow
Per trasferire i workflow ad altri database di [!INCLUDE[d365fin](includes/d365fin_md.md)], ad esempio per risparmiare tempo durante la creazione di nuovi workflow, è possibile esportare e importare i workflow.  

 Un altro modo per creare rapidamente i flussi di lavoro prevede la creazione dei flussi di lavoro dai modelli di flusso di lavoro. Per ulteriori informazioni, vedere [Creare workflow da modelli di workflow](across-how-to-create-workflows-from-workflow-templates.md).  

 Nella finestra **Workflow** creare un workflow elencando le fasi interessate nelle righe. Ogni fase consiste in un evento del flusso di lavoro, moderato dalle condizioni di evento, e in una risposta del flusso di lavoro, moderata dalle opzioni di risposta. È possibile definire le fasi workflow compilando i campi delle righe del workflow in base a elenchi fissi di valori di evento e di risposta che rappresentano gli scenari supportati dal codice dell'applicazione. Per ulteriori informazioni, vedere [Creare workflow](across-how-to-create-workflows.md).  

## <a name="to-export-a-workflow"></a>Per esportare un flusso di lavoro  
1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Workflow** e quindi scegliere il collegamento correlato.  
2.  Selezionare un workflow e scegliere l'azione **Esporta in file**.  
3.  Nella finestra **Esporta file** fare clic sul pulsante **Salva**.  
4.  Nella finestra **Esporta** selezionare un percorso per il file e scegliere il pulsante **Salva**.  

## <a name="to-import-a-workflow"></a>Per importare un flusso di lavoro  
1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Workflow** e quindi scegliere il collegamento correlato.  
2.  Selezionare l'azione **Importa da file**.  
3.  Nella finestra **Importa** selezionare il file XML contenente il flusso di lavoro e quindi scegliere il pulsante **Apri**.  

> [!CAUTION]  
>  Se il codice del flusso di lavoro è già esistente nel database, i passaggi del flusso di lavoro verranno sovrascritti dai passaggi il flusso di lavoro importato.  

## <a name="see-also"></a>Vedi anche  
 [Creare i workflow](across-how-to-create-workflows.md)   
 [Creare flussi di lavoro da modelli di flusso di lavoro](across-how-to-create-workflows-from-workflow-templates.md)   
 [Visualizzare le istanze di fase workflow archiviate](across-how-to-view-archived-workflow-step-instances.md)   
 [Eliminare i workflow](across-how-to-delete-workflows.md)   
 [Procedura dettagliata: Impostazione e utilizzo di un workflow di approvazione di acquisto](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
 [Impostazione dei workflow](across-set-up-workflows.md)   
 [Utilizzo dei workflow](across-use-workflows.md)   
 [Workflow](across-workflow.md)   
