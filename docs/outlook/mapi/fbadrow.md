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
ms.openlocfilehash: 153bcbfd87ea9e85d834cba2fd9028e98fa25750
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420621"
---
# <a name="fbadrow"></a><span data-ttu-id="53b91-103">FBadRow</span><span class="sxs-lookup"><span data-stu-id="53b91-103">FBadRow</span></span>

  
  
<span data-ttu-id="53b91-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="53b91-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="53b91-105">Проверяет строку в таблице.</span><span class="sxs-lookup"><span data-stu-id="53b91-105">Validates a row in a table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="53b91-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="53b91-106">Header file:</span></span>  <br/> |<span data-ttu-id="53b91-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="53b91-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="53b91-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="53b91-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="53b91-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="53b91-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="53b91-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="53b91-110">Called by:</span></span>  <br/> |<span data-ttu-id="53b91-111">Поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="53b91-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadRow(
  LPSRow lprow
);
```

## <a name="parameters"></a><span data-ttu-id="53b91-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="53b91-112">Parameters</span></span>

 <span data-ttu-id="53b91-113">_lprow_</span><span class="sxs-lookup"><span data-stu-id="53b91-113">_lprow_</span></span>
  
> <span data-ttu-id="53b91-114">[in] Указатель на [структуру SRow,](srow.md) определяя строку, которая должна быть проверена.</span><span class="sxs-lookup"><span data-stu-id="53b91-114">[in] Pointer to an [SRow](srow.md) structure identifying the row to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="53b91-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="53b91-115">Return value</span></span>

<span data-ttu-id="53b91-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="53b91-116">TRUE</span></span> 
  
> <span data-ttu-id="53b91-117">Указанная строка недействительна.</span><span class="sxs-lookup"><span data-stu-id="53b91-117">The specified row is invalid.</span></span>
    
<span data-ttu-id="53b91-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="53b91-118">FALSE</span></span> 
  
> <span data-ttu-id="53b91-119">Указанная строка действительна.</span><span class="sxs-lookup"><span data-stu-id="53b91-119">The specified row is valid.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="53b91-120">См. также</span><span class="sxs-lookup"><span data-stu-id="53b91-120">See also</span></span>



[<span data-ttu-id="53b91-121">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="53b91-121">FBadRowSet</span></span>](fbadrowset.md)

