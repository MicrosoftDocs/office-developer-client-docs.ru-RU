---
title: FBadRowSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadRowSet
api_type:
- COM
ms.assetid: 3890dd50-e6ca-4859-bada-f6752ab61d41
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e86e9fbf4901b5944775886f38db1ba12c4b122d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590962"
---
# <a name="fbadrowset"></a><span data-ttu-id="d9a05-103">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="d9a05-103">FBadRowSet</span></span>

  
  
<span data-ttu-id="d9a05-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d9a05-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d9a05-105">Проверяет все строки в таблице, включенных в набор строк таблицы.</span><span class="sxs-lookup"><span data-stu-id="d9a05-105">Validates all table rows included in a set of table rows.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d9a05-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="d9a05-106">Header file:</span></span>  <br/> |<span data-ttu-id="d9a05-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="d9a05-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="d9a05-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="d9a05-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d9a05-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d9a05-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d9a05-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="d9a05-110">Called by:</span></span>  <br/> |<span data-ttu-id="d9a05-111">Поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="d9a05-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadRowSet(
  LPSRowSet lpRowSet
);
```

## <a name="parameters"></a><span data-ttu-id="d9a05-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="d9a05-112">Parameters</span></span>

 <span data-ttu-id="d9a05-113">_lpRowSet_</span><span class="sxs-lookup"><span data-stu-id="d9a05-113">_lpRowSet_</span></span>
  
> <span data-ttu-id="d9a05-114">[in] Указатель на структуру [SRowSet](srowset.md) , идентифицирующий набор для проверки строк.</span><span class="sxs-lookup"><span data-stu-id="d9a05-114">[in] Pointer to an [SRowSet](srowset.md) structure identifying the row set to be validated.</span></span> <span data-ttu-id="d9a05-115">Если указатель имеет значение NULL, структура является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="d9a05-115">If the pointer is NULL, the structure is invalid.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d9a05-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d9a05-116">Return value</span></span>

<span data-ttu-id="d9a05-117">TRUE</span><span class="sxs-lookup"><span data-stu-id="d9a05-117">TRUE</span></span> 
  
> <span data-ttu-id="d9a05-118">Строки набора указанных строке является недопустимым или набор самого строк является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="d9a05-118">A row of the specified row set is invalid, or the row set itself is invalid.</span></span> 
    
<span data-ttu-id="d9a05-119">FALSE</span><span class="sxs-lookup"><span data-stu-id="d9a05-119">FALSE</span></span> 
  
> <span data-ttu-id="d9a05-120">Строки набора указанной строки и набор самого строк являются допустимыми.</span><span class="sxs-lookup"><span data-stu-id="d9a05-120">The rows of the specified row set and the row set itself are all valid.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d9a05-121">См. также</span><span class="sxs-lookup"><span data-stu-id="d9a05-121">See also</span></span>



[<span data-ttu-id="d9a05-122">FBadRow</span><span class="sxs-lookup"><span data-stu-id="d9a05-122">FBadRow</span></span>](fbadrow.md)

