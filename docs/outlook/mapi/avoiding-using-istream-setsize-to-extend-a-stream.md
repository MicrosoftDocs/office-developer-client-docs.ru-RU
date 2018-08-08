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
ms.openlocfilehash: 54d352c263fd34bc8494d8d76c76cb22e0bafa58
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808126"
---
# <a name="avoiding-using-istreamsetsize-to-extend-a-stream"></a><span data-ttu-id="f7f83-103">Расширение потока без использования IStream::SetSize</span><span class="sxs-lookup"><span data-stu-id="f7f83-103">Avoiding Using IStream::SetSize to Extend a Stream</span></span>

  
  
<span data-ttu-id="f7f83-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f7f83-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f7f83-105">При создании потоков, это необходимо увеличить размер, так как их исходный размер больше не достаточно.</span><span class="sxs-lookup"><span data-stu-id="f7f83-105">When writing to streams, it is sometimes necessary to enlarge them because their initial size is no longer sufficient.</span></span> <span data-ttu-id="f7f83-106">Используйте метод OLE **IStream::Write** для этого вместо **IStream::SetSize**.</span><span class="sxs-lookup"><span data-stu-id="f7f83-106">Use the OLE method **IStream::Write** to accomplish this rather than **IStream::SetSize**.</span></span> <span data-ttu-id="f7f83-107">**IStream::Write** автоматически расширяет потока, что ** IStream::SetSize ** ненужных.</span><span class="sxs-lookup"><span data-stu-id="f7f83-107">**IStream::Write** automatically extends the stream, making ** IStream::SetSize ** unnecessary.</span></span> <span data-ttu-id="f7f83-108">Вызов **IStream::Write** без **IStream::SetSize** может быть до трех раз быстрее, чем внесения **SetSize** звонков до **записи**.</span><span class="sxs-lookup"><span data-stu-id="f7f83-108">Calling **IStream::Write** without **IStream::SetSize** can be up to three times faster than making the **SetSize** call prior to **Write**.</span></span>
  

