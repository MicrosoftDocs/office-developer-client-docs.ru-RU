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
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: e6963fc373f771289e3dbff3a0b41857352b4b9a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808444"
---
# <a name="fbadrowset"></a><span data-ttu-id="282fe-103">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="282fe-103">FBadRowSet</span></span>

  
  
<span data-ttu-id="282fe-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="282fe-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="282fe-105">Проверяет все строки в таблице, включенных в набор строк таблицы.</span><span class="sxs-lookup"><span data-stu-id="282fe-105">Validates all table rows included in a set of table rows.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="282fe-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="282fe-106">Header file:</span></span>  <br/> |<span data-ttu-id="282fe-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="282fe-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="282fe-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="282fe-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="282fe-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="282fe-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="282fe-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="282fe-110">Called by:</span></span>  <br/> |<span data-ttu-id="282fe-111">Поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="282fe-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadRowSet(
  LPSRowSet lpRowSet
);
```

## <a name="parameters"></a><span data-ttu-id="282fe-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="282fe-112">Parameters</span></span>

 <span data-ttu-id="282fe-113">_lpRowSet_</span><span class="sxs-lookup"><span data-stu-id="282fe-113">_lpRowSet_</span></span>
  
> <span data-ttu-id="282fe-114">[in] Указатель на структуру [SRowSet](srowset.md) , идентифицирующий набор для проверки строк.</span><span class="sxs-lookup"><span data-stu-id="282fe-114">[in] Pointer to an [SRowSet](srowset.md) structure identifying the row set to be validated.</span></span> <span data-ttu-id="282fe-115">Если указатель имеет значение NULL, структура является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="282fe-115">If the pointer is NULL, the structure is invalid.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="282fe-116">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="282fe-116">Return value</span></span>

<span data-ttu-id="282fe-117">TRUE</span><span class="sxs-lookup"><span data-stu-id="282fe-117">TRUE</span></span> 
  
> <span data-ttu-id="282fe-118">Строки набора указанных строке является недопустимым или набор самого строк является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="282fe-118">A row of the specified row set is invalid, or the row set itself is invalid.</span></span> 
    
<span data-ttu-id="282fe-119">FALSE</span><span class="sxs-lookup"><span data-stu-id="282fe-119">FALSE</span></span> 
  
> <span data-ttu-id="282fe-120">Строки набора указанной строки и набор самого строк являются допустимыми.</span><span class="sxs-lookup"><span data-stu-id="282fe-120">The rows of the specified row set and the row set itself are all valid.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="282fe-121">См. также</span><span class="sxs-lookup"><span data-stu-id="282fe-121">See also</span></span>



[<span data-ttu-id="282fe-122">FBadRow</span><span class="sxs-lookup"><span data-stu-id="282fe-122">FBadRow</span></span>](fbadrow.md)

