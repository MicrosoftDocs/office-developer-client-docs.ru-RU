---
title: FBadSortOrderSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadSortOrderSet
api_type:
- COM
ms.assetid: b7f80e0a-8ddd-4b24-ab63-2078a8152058
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 31840923e24cddd0dc3dfa9cc67b610d0dcd7e47
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428461"
---
# <a name="fbadsortorderset"></a><span data-ttu-id="13dd8-103">FBadSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="13dd8-103">FBadSortOrderSet</span></span>

  
  
<span data-ttu-id="13dd8-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="13dd8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="13dd8-105">Проверяет порядок сортировки, проверяя его распределение памяти.</span><span class="sxs-lookup"><span data-stu-id="13dd8-105">Validates a sort order set by verifying its memory allocation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="13dd8-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="13dd8-106">Header file:</span></span>  <br/> |<span data-ttu-id="13dd8-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="13dd8-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="13dd8-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="13dd8-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="13dd8-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="13dd8-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="13dd8-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="13dd8-110">Called by:</span></span>  <br/> |<span data-ttu-id="13dd8-111">Поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="13dd8-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadSortOrderSet(
  LPSSortOrderSet lpsos
);
```

## <a name="parameters"></a><span data-ttu-id="13dd8-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="13dd8-112">Parameters</span></span>

 <span data-ttu-id="13dd8-113">_lpsos_</span><span class="sxs-lookup"><span data-stu-id="13dd8-113">_lpsos_</span></span>
  
> <span data-ttu-id="13dd8-114">[in] Указатель на [структуру SSortOrderSet,](ssortorderset.md) определяя набор сортировки для проверки.</span><span class="sxs-lookup"><span data-stu-id="13dd8-114">[in] Pointer to an [SSortOrderSet](ssortorderset.md) structure identifying the sort order set to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="13dd8-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="13dd8-115">Return value</span></span>

<span data-ttu-id="13dd8-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="13dd8-116">TRUE</span></span> 
  
> <span data-ttu-id="13dd8-117">Указанный набор порядка сортировки является недействительным.</span><span class="sxs-lookup"><span data-stu-id="13dd8-117">The specified sort order set is invalid.</span></span> 
    
<span data-ttu-id="13dd8-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="13dd8-118">FALSE</span></span> 
  
> <span data-ttu-id="13dd8-119">Указанный набор порядка сортировки действителен.</span><span class="sxs-lookup"><span data-stu-id="13dd8-119">The specified sort order set is valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="13dd8-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="13dd8-120">Remarks</span></span>

<span data-ttu-id="13dd8-121">Функцию **FBadSortOrderSet** можно использовать для подготовки вызова к методу сортировки, такому как [метод IMAPITable::SortTable.](imapitable-sorttable.md)</span><span class="sxs-lookup"><span data-stu-id="13dd8-121">The **FBadSortOrderSet** function can be used to prepare for a call to a sort method such as the [IMAPITable::SortTable](imapitable-sorttable.md) method.</span></span> 
  

