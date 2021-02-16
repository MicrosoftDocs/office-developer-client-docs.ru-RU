---
title: Предотвращение использования IStreamSetSize для расширения потока
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b6de594f-e331-4421-956b-86ee0b5518fe
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 614bb3d142b7aaabe89223b6ce3552469edfce27
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428916"
---
# <a name="avoiding-using-istreamsetsize-to-extend-a-stream"></a><span data-ttu-id="15674-103">Предотвращение использования IStream::SetSize для расширения потока</span><span class="sxs-lookup"><span data-stu-id="15674-103">Avoiding Using IStream::SetSize to Extend a Stream</span></span>

  
  
<span data-ttu-id="15674-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="15674-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="15674-105">При записи в потоки иногда требуется увеличить их, так как их начального размера больше недостаточно.</span><span class="sxs-lookup"><span data-stu-id="15674-105">When writing to streams, it is sometimes necessary to enlarge them because their initial size is no longer sufficient.</span></span> <span data-ttu-id="15674-106">Для этого используйте метод OLE **IStream::Write,** а не **IStream::SetSize.**</span><span class="sxs-lookup"><span data-stu-id="15674-106">Use the OLE method **IStream::Write** to accomplish this rather than **IStream::SetSize**.</span></span> <span data-ttu-id="15674-107">**IStream::Write** автоматически расширяет поток, делая \*\* IStream::SetSize \*\* ненужным.</span><span class="sxs-lookup"><span data-stu-id="15674-107">**IStream::Write** automatically extends the stream, making \*\* IStream::SetSize \*\* unnecessary.</span></span> <span data-ttu-id="15674-108">Вызов **IStream::Write** без **IStream::SetSize** может быть в три раза быстрее, чем вызов **SetSize** до **записи.**</span><span class="sxs-lookup"><span data-stu-id="15674-108">Calling **IStream::Write** without **IStream::SetSize** can be up to three times faster than making the **SetSize** call prior to **Write**.</span></span>
  

