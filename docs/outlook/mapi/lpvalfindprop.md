---
title: LpValFindProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 67461a38-bb60-467b-901b-39c645e764f7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d7601eb50818fa6f39384a6b024215fc4917e83a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809658"
---
# <a name="lpvalfindprop"></a><span data-ttu-id="a1733-103">LpValFindProp</span><span class="sxs-lookup"><span data-stu-id="a1733-103">LpValFindProp</span></span>

  
  
<span data-ttu-id="a1733-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a1733-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a1733-105">Настройка поиска для указанного свойства в свойстве.</span><span class="sxs-lookup"><span data-stu-id="a1733-105">Searches for a specified property in a property set.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a1733-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="a1733-106">Header file:</span></span>  <br/> |<span data-ttu-id="a1733-107">mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="a1733-107">mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="a1733-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="a1733-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a1733-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a1733-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a1733-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="a1733-110">Called by:</span></span>  <br/> |<span data-ttu-id="a1733-111">Клиентские приложения и поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="a1733-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
LPSPropValue LpValFindProp(
  ULONG ulPropTag,
  ULONG cValues,
  LPSPropValue lpPropArray
);
```

## <a name="parameters"></a><span data-ttu-id="a1733-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="a1733-112">Parameters</span></span>

 <span data-ttu-id="a1733-113">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="a1733-113">_ulPropTag_</span></span>
  
> <span data-ttu-id="a1733-114">[in] Тег для свойства для поиска в набор свойств, указанное с помощью параметра _lpPropArray_ .</span><span class="sxs-lookup"><span data-stu-id="a1733-114">[in] Tag for the property to search for in the property set, indicated by the  _lpPropArray_ parameter.</span></span> 
    
 <span data-ttu-id="a1733-115">_cValues_</span><span class="sxs-lookup"><span data-stu-id="a1733-115">_cValues_</span></span>
  
> <span data-ttu-id="a1733-116">[in] Число свойств в набор свойств, указанное с помощью параметра _lpPropArray_ .</span><span class="sxs-lookup"><span data-stu-id="a1733-116">[in] Count of properties in the property set, indicated by the  _lpPropArray_ parameter.</span></span> 
    
 <span data-ttu-id="a1733-117">_lpPropArray_</span><span class="sxs-lookup"><span data-stu-id="a1733-117">_lpPropArray_</span></span>
  
> <span data-ttu-id="a1733-118">[in] Массив структур **SPropValue** , который определяет свойства для поиска.</span><span class="sxs-lookup"><span data-stu-id="a1733-118">[in] Array of **SPropValue** structures that defines the properties to be searched.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a1733-119">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="a1733-119">Return value</span></span>

<span data-ttu-id="a1733-120">Функция **LpValFindProp** возвращает структуру **SPropValue** , который определяет свойство, которое сопоставляется входного свойства tag, или значение NULL, если нет соответствия.</span><span class="sxs-lookup"><span data-stu-id="a1733-120">The **LpValFindProp** function returns an **SPropValue** structure that defines the property that matches the input property tag, or NULL if there is no match.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a1733-121">Замечания</span><span class="sxs-lookup"><span data-stu-id="a1733-121">Remarks</span></span>

<span data-ttu-id="a1733-122">Функция **LpValFindProp** идентична **PpropFindProp**.</span><span class="sxs-lookup"><span data-stu-id="a1733-122">The **LpValFindProp** function is identical to **PpropFindProp**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a1733-123">См. также</span><span class="sxs-lookup"><span data-stu-id="a1733-123">See also</span></span>



[<span data-ttu-id="a1733-124">PpropFindProp</span><span class="sxs-lookup"><span data-stu-id="a1733-124">PpropFindProp</span></span>](ppropfindprop.md)
  
[<span data-ttu-id="a1733-125">SPropValue</span><span class="sxs-lookup"><span data-stu-id="a1733-125">SPropValue</span></span>](spropvalue.md)

