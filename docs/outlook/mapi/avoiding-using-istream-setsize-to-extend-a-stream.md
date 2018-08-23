---
title: Предотвращение использования с помощью IStreamSetSize для расширения потока
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b6de594f-e331-4421-956b-86ee0b5518fe
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 9245d4913c2832b8c942093e65cf088643a1947c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592082"
---
# <a name="avoiding-using-istreamsetsize-to-extend-a-stream"></a><span data-ttu-id="d893a-103">Расширение потока без использования IStream::SetSize</span><span class="sxs-lookup"><span data-stu-id="d893a-103">Avoiding Using IStream::SetSize to Extend a Stream</span></span>

  
  
<span data-ttu-id="d893a-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d893a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d893a-105">При создании потоков, это необходимо увеличить размер, так как их исходный размер больше не достаточно.</span><span class="sxs-lookup"><span data-stu-id="d893a-105">When writing to streams, it is sometimes necessary to enlarge them because their initial size is no longer sufficient.</span></span> <span data-ttu-id="d893a-106">Используйте метод OLE **IStream::Write** для этого вместо **IStream::SetSize**.</span><span class="sxs-lookup"><span data-stu-id="d893a-106">Use the OLE method **IStream::Write** to accomplish this rather than **IStream::SetSize**.</span></span> <span data-ttu-id="d893a-107">**IStream::Write** автоматически расширяет потока, что ** IStream::SetSize ** ненужных.</span><span class="sxs-lookup"><span data-stu-id="d893a-107">**IStream::Write** automatically extends the stream, making ** IStream::SetSize ** unnecessary.</span></span> <span data-ttu-id="d893a-108">Вызов **IStream::Write** без **IStream::SetSize** может быть до трех раз быстрее, чем внесения **SetSize** звонков до **записи**.</span><span class="sxs-lookup"><span data-stu-id="d893a-108">Calling **IStream::Write** without **IStream::SetSize** can be up to three times faster than making the **SetSize** call prior to **Write**.</span></span>
  

