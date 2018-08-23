---
title: FBadRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadRow
api_type:
- COM
ms.assetid: 205d00df-488d-4888-8782-a1f70f54d720
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 23b4ed78f4b65a5af4c2f3e11fa770030fe4eeee
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590164"
---
# <a name="fbadrow"></a><span data-ttu-id="aa74a-103">FBadRow</span><span class="sxs-lookup"><span data-stu-id="aa74a-103">FBadRow</span></span>

  
  
<span data-ttu-id="aa74a-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aa74a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aa74a-105">Проверяет строку в таблице.</span><span class="sxs-lookup"><span data-stu-id="aa74a-105">Validates a row in a table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="aa74a-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="aa74a-106">Header file:</span></span>  <br/> |<span data-ttu-id="aa74a-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="aa74a-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="aa74a-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="aa74a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="aa74a-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="aa74a-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="aa74a-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="aa74a-110">Called by:</span></span>  <br/> |<span data-ttu-id="aa74a-111">Поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="aa74a-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadRow(
  LPSRow lprow
);
```

## <a name="parameters"></a><span data-ttu-id="aa74a-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="aa74a-112">Parameters</span></span>

 <span data-ttu-id="aa74a-113">_lprow_</span><span class="sxs-lookup"><span data-stu-id="aa74a-113">_lprow_</span></span>
  
> <span data-ttu-id="aa74a-114">[in] Указатель на структуру [SRow](srow.md) , идентифицирующий строку для проверки.</span><span class="sxs-lookup"><span data-stu-id="aa74a-114">[in] Pointer to an [SRow](srow.md) structure identifying the row to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="aa74a-115">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="aa74a-115">Return value</span></span>

<span data-ttu-id="aa74a-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="aa74a-116">TRUE</span></span> 
  
> <span data-ttu-id="aa74a-117">Указанная строка является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="aa74a-117">The specified row is invalid.</span></span>
    
<span data-ttu-id="aa74a-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="aa74a-118">FALSE</span></span> 
  
> <span data-ttu-id="aa74a-119">Указанная строка является допустимым.</span><span class="sxs-lookup"><span data-stu-id="aa74a-119">The specified row is valid.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="aa74a-120">См. также</span><span class="sxs-lookup"><span data-stu-id="aa74a-120">See also</span></span>



[<span data-ttu-id="aa74a-121">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="aa74a-121">FBadRowSet</span></span>](fbadrowset.md)

