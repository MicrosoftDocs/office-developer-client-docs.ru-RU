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
ms.openlocfilehash: fa1588d4a58824b57c132fc8e66a0abd6e9acd0a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419641"
---
# <a name="lpvalfindprop"></a><span data-ttu-id="b5559-103">LpValFindProp</span><span class="sxs-lookup"><span data-stu-id="b5559-103">LpValFindProp</span></span>

  
  
<span data-ttu-id="b5559-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b5559-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b5559-105">Поиск указанного свойства в наборе свойств.</span><span class="sxs-lookup"><span data-stu-id="b5559-105">Searches for a specified property in a property set.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b5559-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="b5559-106">Header file:</span></span>  <br/> |<span data-ttu-id="b5559-107">mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="b5559-107">mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="b5559-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="b5559-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b5559-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b5559-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b5559-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="b5559-110">Called by:</span></span>  <br/> |<span data-ttu-id="b5559-111">Клиентские приложения и поставщики услуг.</span><span class="sxs-lookup"><span data-stu-id="b5559-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
LPSPropValue LpValFindProp(
  ULONG ulPropTag,
  ULONG cValues,
  LPSPropValue lpPropArray
);
```

## <a name="parameters"></a><span data-ttu-id="b5559-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="b5559-112">Parameters</span></span>

 <span data-ttu-id="b5559-113">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="b5559-113">_ulPropTag_</span></span>
  
> <span data-ttu-id="b5559-114">[in] Тег свойства для поиска в наборе свойств, указанный _параметром lpPropArray._</span><span class="sxs-lookup"><span data-stu-id="b5559-114">[in] Tag for the property to search for in the property set, indicated by the  _lpPropArray_ parameter.</span></span> 
    
 <span data-ttu-id="b5559-115">_cValues_</span><span class="sxs-lookup"><span data-stu-id="b5559-115">_cValues_</span></span>
  
> <span data-ttu-id="b5559-116">[in] Количество свойств в наборе свойств, указанных параметром _lpPropArray._</span><span class="sxs-lookup"><span data-stu-id="b5559-116">[in] Count of properties in the property set, indicated by the  _lpPropArray_ parameter.</span></span> 
    
 <span data-ttu-id="b5559-117">_lpPropArray_</span><span class="sxs-lookup"><span data-stu-id="b5559-117">_lpPropArray_</span></span>
  
> <span data-ttu-id="b5559-118">[in] Массив **структур SPropValue,** определяя свойства, которые необходимо искать.</span><span class="sxs-lookup"><span data-stu-id="b5559-118">[in] Array of **SPropValue** structures that defines the properties to be searched.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b5559-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b5559-119">Return value</span></span>

<span data-ttu-id="b5559-120">Функция **LpValFindProp** возвращает структуру **SPropValue,** которая определяет свойство, которое соответствует тегу свойства ввода или NULL, если нет совпадения.</span><span class="sxs-lookup"><span data-stu-id="b5559-120">The **LpValFindProp** function returns an **SPropValue** structure that defines the property that matches the input property tag, or NULL if there is no match.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b5559-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="b5559-121">Remarks</span></span>

<span data-ttu-id="b5559-122">Функция **LpValFindProp** идентична **функции PpropFindProp.**</span><span class="sxs-lookup"><span data-stu-id="b5559-122">The **LpValFindProp** function is identical to **PpropFindProp**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b5559-123">См. также</span><span class="sxs-lookup"><span data-stu-id="b5559-123">See also</span></span>



[<span data-ttu-id="b5559-124">PpropFindProp</span><span class="sxs-lookup"><span data-stu-id="b5559-124">PpropFindProp</span></span>](ppropfindprop.md)
  
[<span data-ttu-id="b5559-125">SPropValue</span><span class="sxs-lookup"><span data-stu-id="b5559-125">SPropValue</span></span>](spropvalue.md)

