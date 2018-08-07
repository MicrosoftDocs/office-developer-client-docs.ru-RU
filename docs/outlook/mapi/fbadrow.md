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
ms.openlocfilehash: c3025c353c71958a19303c5e79cec319a3bf8015
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808437"
---
# <a name="fbadrow"></a><span data-ttu-id="38409-103">FBadRow</span><span class="sxs-lookup"><span data-stu-id="38409-103">FBadRow</span></span>

  
  
<span data-ttu-id="38409-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="38409-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="38409-105">Проверяет строку в таблице.</span><span class="sxs-lookup"><span data-stu-id="38409-105">Validates a row in a table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="38409-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="38409-106">Header file:</span></span>  <br/> |<span data-ttu-id="38409-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="38409-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="38409-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="38409-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="38409-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="38409-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="38409-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="38409-110">Called by:</span></span>  <br/> |<span data-ttu-id="38409-111">Поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="38409-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadRow(
  LPSRow lprow
);
```

## <a name="parameters"></a><span data-ttu-id="38409-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="38409-112">Parameters</span></span>

 <span data-ttu-id="38409-113">_lprow_</span><span class="sxs-lookup"><span data-stu-id="38409-113">_lprow_</span></span>
  
> <span data-ttu-id="38409-114">[in] Указатель на структуру [SRow](srow.md) , идентифицирующий строку для проверки.</span><span class="sxs-lookup"><span data-stu-id="38409-114">[in] Pointer to an [SRow](srow.md) structure identifying the row to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="38409-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5">Return value</span></span>

<span data-ttu-id="38409-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="38409-116">TRUE</span></span> 
  
> <span data-ttu-id="38409-117">Указанная строка является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="38409-117">The specified row is invalid.</span></span>
    
<span data-ttu-id="38409-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="38409-118">FALSE</span></span> 
  
> <span data-ttu-id="38409-119">Указанная строка является допустимым.</span><span class="sxs-lookup"><span data-stu-id="38409-119">The specified row is valid.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="38409-120">См. также</span><span class="sxs-lookup"><span data-stu-id="38409-120">See also</span></span>



[<span data-ttu-id="38409-121">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="38409-121">FBadRowSet</span></span>](fbadrowset.md)

