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
ms.openlocfilehash: 3b3f88495cafbd6ea764ca8901ac67c23749aebe
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578579"
---
# <a name="fbadsortorderset"></a><span data-ttu-id="c67b6-103">FBadSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="c67b6-103">FBadSortOrderSet</span></span>

  
  
<span data-ttu-id="c67b6-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c67b6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c67b6-105">Проверяет, порядок сортировки, задайте убедиться в его выделение памяти.</span><span class="sxs-lookup"><span data-stu-id="c67b6-105">Validates a sort order set by verifying its memory allocation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c67b6-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="c67b6-106">Header file:</span></span>  <br/> |<span data-ttu-id="c67b6-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="c67b6-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="c67b6-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="c67b6-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c67b6-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c67b6-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c67b6-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="c67b6-110">Called by:</span></span>  <br/> |<span data-ttu-id="c67b6-111">Поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="c67b6-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadSortOrderSet(
  LPSSortOrderSet lpsos
);
```

## <a name="parameters"></a><span data-ttu-id="c67b6-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="c67b6-112">Parameters</span></span>

 <span data-ttu-id="c67b6-113">_lpsos_</span><span class="sxs-lookup"><span data-stu-id="c67b6-113">_lpsos_</span></span>
  
> <span data-ttu-id="c67b6-114">[in] Указатель на структуру [SSortOrderSet](ssortorderset.md) , определяющее порядок сортировки, задайте для проверки.</span><span class="sxs-lookup"><span data-stu-id="c67b6-114">[in] Pointer to an [SSortOrderSet](ssortorderset.md) structure identifying the sort order set to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c67b6-115">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="c67b6-115">Return value</span></span>

<span data-ttu-id="c67b6-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="c67b6-116">TRUE</span></span> 
  
> <span data-ttu-id="c67b6-117">Набор порядок сортировки указанного является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="c67b6-117">The specified sort order set is invalid.</span></span> 
    
<span data-ttu-id="c67b6-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="c67b6-118">FALSE</span></span> 
  
> <span data-ttu-id="c67b6-119">Набор порядок сортировки указанного является допустимым.</span><span class="sxs-lookup"><span data-stu-id="c67b6-119">The specified sort order set is valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c67b6-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="c67b6-120">Remarks</span></span>

<span data-ttu-id="c67b6-121">Функция **FBadSortOrderSet** может использоваться для подготовки для вызова метода sort, таких как метод [IMAPITable::SortTable](imapitable-sorttable.md) .</span><span class="sxs-lookup"><span data-stu-id="c67b6-121">The **FBadSortOrderSet** function can be used to prepare for a call to a sort method such as the [IMAPITable::SortTable](imapitable-sorttable.md) method.</span></span> 
  

