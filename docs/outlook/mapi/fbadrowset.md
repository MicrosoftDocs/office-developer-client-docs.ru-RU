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
ms.openlocfilehash: 49e6c8254cbd527635685c3f974da57ee3ac82a5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411794"
---
# <a name="fbadrowset"></a><span data-ttu-id="c818b-103">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="c818b-103">FBadRowSet</span></span>

  
  
<span data-ttu-id="c818b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c818b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c818b-105">Проверяет все строки таблицы, включенные в набор строк таблицы.</span><span class="sxs-lookup"><span data-stu-id="c818b-105">Validates all table rows included in a set of table rows.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c818b-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="c818b-106">Header file:</span></span>  <br/> |<span data-ttu-id="c818b-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="c818b-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="c818b-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="c818b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c818b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c818b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c818b-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="c818b-110">Called by:</span></span>  <br/> |<span data-ttu-id="c818b-111">Поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="c818b-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadRowSet(
  LPSRowSet lpRowSet
);
```

## <a name="parameters"></a><span data-ttu-id="c818b-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="c818b-112">Parameters</span></span>

 <span data-ttu-id="c818b-113">_лпровсет_</span><span class="sxs-lookup"><span data-stu-id="c818b-113">_lpRowSet_</span></span>
  
> <span data-ttu-id="c818b-114">возврата Указатель на структуру [SRowSet](srowset.md) , определяющую набор строк, который необходимо проверить.</span><span class="sxs-lookup"><span data-stu-id="c818b-114">[in] Pointer to an [SRowSet](srowset.md) structure identifying the row set to be validated.</span></span> <span data-ttu-id="c818b-115">Если указатель равен NULL, структура является недопустимой.</span><span class="sxs-lookup"><span data-stu-id="c818b-115">If the pointer is NULL, the structure is invalid.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c818b-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c818b-116">Return value</span></span>

<span data-ttu-id="c818b-117">TRUE</span><span class="sxs-lookup"><span data-stu-id="c818b-117">TRUE</span></span> 
  
> <span data-ttu-id="c818b-118">Строка указанного набора строк является недопустимой, или сам набор строк является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="c818b-118">A row of the specified row set is invalid, or the row set itself is invalid.</span></span> 
    
<span data-ttu-id="c818b-119">FALSE</span><span class="sxs-lookup"><span data-stu-id="c818b-119">FALSE</span></span> 
  
> <span data-ttu-id="c818b-120">Все строки указанного набора строк и собственно набора строк являются допустимыми.</span><span class="sxs-lookup"><span data-stu-id="c818b-120">The rows of the specified row set and the row set itself are all valid.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c818b-121">См. также</span><span class="sxs-lookup"><span data-stu-id="c818b-121">See also</span></span>



[<span data-ttu-id="c818b-122">FBadRow</span><span class="sxs-lookup"><span data-stu-id="c818b-122">FBadRow</span></span>](fbadrow.md)

