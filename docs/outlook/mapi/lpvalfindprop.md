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
# <a name="lpvalfindprop"></a><span data-ttu-id="225ff-103">LpValFindProp</span><span class="sxs-lookup"><span data-stu-id="225ff-103">LpValFindProp</span></span>

  
  
<span data-ttu-id="225ff-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="225ff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="225ff-105">Выполняет поиск указанного свойства в наборе свойств.</span><span class="sxs-lookup"><span data-stu-id="225ff-105">Searches for a specified property in a property set.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="225ff-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="225ff-106">Header file:</span></span>  <br/> |<span data-ttu-id="225ff-107">мапиутил. h</span><span class="sxs-lookup"><span data-stu-id="225ff-107">mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="225ff-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="225ff-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="225ff-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="225ff-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="225ff-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="225ff-110">Called by:</span></span>  <br/> |<span data-ttu-id="225ff-111">Клиентские приложения и поставщики услуг.</span><span class="sxs-lookup"><span data-stu-id="225ff-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
LPSPropValue LpValFindProp(
  ULONG ulPropTag,
  ULONG cValues,
  LPSPropValue lpPropArray
);
```

## <a name="parameters"></a><span data-ttu-id="225ff-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="225ff-112">Parameters</span></span>

 <span data-ttu-id="225ff-113">_Улпроптаг_</span><span class="sxs-lookup"><span data-stu-id="225ff-113">_ulPropTag_</span></span>
  
> <span data-ttu-id="225ff-114">возврата Для свойства, которое требуется найти в наборе свойств, указанном с помощью параметра _лппропаррай_ .</span><span class="sxs-lookup"><span data-stu-id="225ff-114">[in] Tag for the property to search for in the property set, indicated by the  _lpPropArray_ parameter.</span></span> 
    
 <span data-ttu-id="225ff-115">_Квалуес_</span><span class="sxs-lookup"><span data-stu-id="225ff-115">_cValues_</span></span>
  
> <span data-ttu-id="225ff-116">возврата Количество свойств в наборе свойств, определяемое параметром _лппропаррай_ .</span><span class="sxs-lookup"><span data-stu-id="225ff-116">[in] Count of properties in the property set, indicated by the  _lpPropArray_ parameter.</span></span> 
    
 <span data-ttu-id="225ff-117">_Лппропаррай_</span><span class="sxs-lookup"><span data-stu-id="225ff-117">_lpPropArray_</span></span>
  
> <span data-ttu-id="225ff-118">возврата Массив структур **спропвалуе** , определяющий свойства для поиска.</span><span class="sxs-lookup"><span data-stu-id="225ff-118">[in] Array of **SPropValue** structures that defines the properties to be searched.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="225ff-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="225ff-119">Return value</span></span>

<span data-ttu-id="225ff-120">Функция **лпвалфиндпроп** возвращает структуру **спропвалуе** , определяющую свойство, которое соответствует тегу входного свойства, или значение null, если совпадение отсутствует.</span><span class="sxs-lookup"><span data-stu-id="225ff-120">The **LpValFindProp** function returns an **SPropValue** structure that defines the property that matches the input property tag, or NULL if there is no match.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="225ff-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="225ff-121">Remarks</span></span>

<span data-ttu-id="225ff-122">Функция **лпвалфиндпроп** идентична **ппропфиндпроп**.</span><span class="sxs-lookup"><span data-stu-id="225ff-122">The **LpValFindProp** function is identical to **PpropFindProp**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="225ff-123">См. также</span><span class="sxs-lookup"><span data-stu-id="225ff-123">See also</span></span>



[<span data-ttu-id="225ff-124">PpropFindProp</span><span class="sxs-lookup"><span data-stu-id="225ff-124">PpropFindProp</span></span>](ppropfindprop.md)
  
[<span data-ttu-id="225ff-125">SPropValue</span><span class="sxs-lookup"><span data-stu-id="225ff-125">SPropValue</span></span>](spropvalue.md)

