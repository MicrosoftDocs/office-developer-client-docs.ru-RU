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
ms.openlocfilehash: c4a201411e2232a3e5fdcd97dcbc9460f657b12a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578096"
---
# <a name="lpvalfindprop"></a><span data-ttu-id="d7b8e-103">LpValFindProp</span><span class="sxs-lookup"><span data-stu-id="d7b8e-103">LpValFindProp</span></span>

  
  
<span data-ttu-id="d7b8e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d7b8e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d7b8e-105">Настройка поиска для указанного свойства в свойстве.</span><span class="sxs-lookup"><span data-stu-id="d7b8e-105">Searches for a specified property in a property set.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d7b8e-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="d7b8e-106">Header file:</span></span>  <br/> |<span data-ttu-id="d7b8e-107">mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="d7b8e-107">mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="d7b8e-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="d7b8e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d7b8e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d7b8e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d7b8e-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="d7b8e-110">Called by:</span></span>  <br/> |<span data-ttu-id="d7b8e-111">Клиентские приложения и поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="d7b8e-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
LPSPropValue LpValFindProp(
  ULONG ulPropTag,
  ULONG cValues,
  LPSPropValue lpPropArray
);
```

## <a name="parameters"></a><span data-ttu-id="d7b8e-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="d7b8e-112">Parameters</span></span>

 <span data-ttu-id="d7b8e-113">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="d7b8e-113">_ulPropTag_</span></span>
  
> <span data-ttu-id="d7b8e-114">[in] Тег для свойства для поиска в набор свойств, указанное с помощью параметра _lpPropArray_ .</span><span class="sxs-lookup"><span data-stu-id="d7b8e-114">[in] Tag for the property to search for in the property set, indicated by the  _lpPropArray_ parameter.</span></span> 
    
 <span data-ttu-id="d7b8e-115">_cValues_</span><span class="sxs-lookup"><span data-stu-id="d7b8e-115">_cValues_</span></span>
  
> <span data-ttu-id="d7b8e-116">[in] Число свойств в набор свойств, указанное с помощью параметра _lpPropArray_ .</span><span class="sxs-lookup"><span data-stu-id="d7b8e-116">[in] Count of properties in the property set, indicated by the  _lpPropArray_ parameter.</span></span> 
    
 <span data-ttu-id="d7b8e-117">_lpPropArray_</span><span class="sxs-lookup"><span data-stu-id="d7b8e-117">_lpPropArray_</span></span>
  
> <span data-ttu-id="d7b8e-118">[in] Массив структур **SPropValue** , который определяет свойства для поиска.</span><span class="sxs-lookup"><span data-stu-id="d7b8e-118">[in] Array of **SPropValue** structures that defines the properties to be searched.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d7b8e-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d7b8e-119">Return value</span></span>

<span data-ttu-id="d7b8e-120">Функция **LpValFindProp** возвращает структуру **SPropValue** , который определяет свойство, которое сопоставляется входного свойства tag, или значение NULL, если нет соответствия.</span><span class="sxs-lookup"><span data-stu-id="d7b8e-120">The **LpValFindProp** function returns an **SPropValue** structure that defines the property that matches the input property tag, or NULL if there is no match.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d7b8e-121">Замечания</span><span class="sxs-lookup"><span data-stu-id="d7b8e-121">Remarks</span></span>

<span data-ttu-id="d7b8e-122">Функция **LpValFindProp** идентична **PpropFindProp**.</span><span class="sxs-lookup"><span data-stu-id="d7b8e-122">The **LpValFindProp** function is identical to **PpropFindProp**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d7b8e-123">См. также</span><span class="sxs-lookup"><span data-stu-id="d7b8e-123">See also</span></span>



[<span data-ttu-id="d7b8e-124">PpropFindProp</span><span class="sxs-lookup"><span data-stu-id="d7b8e-124">PpropFindProp</span></span>](ppropfindprop.md)
  
[<span data-ttu-id="d7b8e-125">SPropValue</span><span class="sxs-lookup"><span data-stu-id="d7b8e-125">SPropValue</span></span>](spropvalue.md)

