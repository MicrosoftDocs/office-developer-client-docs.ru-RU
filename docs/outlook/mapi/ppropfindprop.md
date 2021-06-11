---
title: PpropFindProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PpropFindProp
api_type:
- HeaderDef
ms.assetid: f23dd6f4-915b-4fe8-ab3f-6d625c7d6061
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 97021128f92af0486af1ba3125c7843eaa357648
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406341"
---
# <a name="ppropfindprop"></a><span data-ttu-id="bf787-103">PpropFindProp</span><span class="sxs-lookup"><span data-stu-id="bf787-103">PpropFindProp</span></span>

  
  
<span data-ttu-id="bf787-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bf787-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bf787-105">Поиск указанного свойства в наборе свойств.</span><span class="sxs-lookup"><span data-stu-id="bf787-105">Searches for a specified property in a property set.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bf787-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="bf787-106">Header file:</span></span>  <br/> |<span data-ttu-id="bf787-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="bf787-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="bf787-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="bf787-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="bf787-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="bf787-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="bf787-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="bf787-110">Called by:</span></span>  <br/> |<span data-ttu-id="bf787-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="bf787-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSPropValue PpropFindProp(
  LPSPropValue rgprop,
  ULONG cprop,
  ULONG ulPropTag
);
```

## <a name="parameters"></a><span data-ttu-id="bf787-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="bf787-112">Parameters</span></span>

 <span data-ttu-id="bf787-113">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="bf787-113">_rgprop_</span></span>
  
> <span data-ttu-id="bf787-114">[in] Массив [структур SPropValue,](spropvalue.md) которые определяют свойства, которые необходимо искать.</span><span class="sxs-lookup"><span data-stu-id="bf787-114">[in] Array of [SPropValue](spropvalue.md) structures that define the properties to be searched.</span></span> 
    
 <span data-ttu-id="bf787-115">_cprop_</span><span class="sxs-lookup"><span data-stu-id="bf787-115">_cprop_</span></span>
  
> <span data-ttu-id="bf787-116">[in] Количество свойств в наборе свойств, указанных _параметром rgprop._</span><span class="sxs-lookup"><span data-stu-id="bf787-116">[in] Count of properties in the property set indicated by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="bf787-117">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="bf787-117">_ulPropTag_</span></span>
  
> <span data-ttu-id="bf787-118">[in] Тег свойства для свойства для поиска в наборе свойств, указанных _параметром rgprop._</span><span class="sxs-lookup"><span data-stu-id="bf787-118">[in] Property tag for the property to search for in the property set indicated by the  _rgprop_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="bf787-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bf787-119">Return value</span></span>

 <span data-ttu-id="bf787-120">**PpropFindProp** возвращает структуру [SPropValue,](spropvalue.md) определяя свойство, которое соответствует тегу свойств ввода, или NULL, если нет совпадения.</span><span class="sxs-lookup"><span data-stu-id="bf787-120">**PpropFindProp** returns an [SPropValue](spropvalue.md) structure defining the property that matches the input property tag, or NULL if there is no match.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="bf787-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="bf787-121">Remarks</span></span>

<span data-ttu-id="bf787-122">Если указанный тег свойства указывает свойство типа PT_UNSPECIFIED, функция **PpropFindProp** находит совпадение только для идентификатора свойства в теге.</span><span class="sxs-lookup"><span data-stu-id="bf787-122">If the given property tag indicates a property of type PT_UNSPECIFIED, the **PpropFindProp** function finds a match only for the property identifier in the tag.</span></span> <span data-ttu-id="bf787-123">В противном случае он находит совпадение для всего тега свойства, включая тип свойства, и возвращает идентифицированное свойство.</span><span class="sxs-lookup"><span data-stu-id="bf787-123">Otherwise, it finds a match for the entire property tag, including the property type, and returns the property identified.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="bf787-124">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="bf787-124">MFCMAPI reference</span></span>

<span data-ttu-id="bf787-125">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="bf787-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="bf787-126">**Файл**</span><span class="sxs-lookup"><span data-stu-id="bf787-126">**File**</span></span>|<span data-ttu-id="bf787-127">**Функция**</span><span class="sxs-lookup"><span data-stu-id="bf787-127">**Function**</span></span>|<span data-ttu-id="bf787-128">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="bf787-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bf787-129">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="bf787-129">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="bf787-130">CContentsTableListCtrl::BuildDataItem</span><span class="sxs-lookup"><span data-stu-id="bf787-130">CContentsTableListCtrl::BuildDataItem</span></span>  <br/> |<span data-ttu-id="bf787-131">MFCMAPI использует **метод PpropFindProp** для поиска свойств в наборе свойств, добавляемом в список.</span><span class="sxs-lookup"><span data-stu-id="bf787-131">MFCMAPI uses the **PpropFindProp** method to find properties in a property set being added to the list.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bf787-132">См. также</span><span class="sxs-lookup"><span data-stu-id="bf787-132">See also</span></span>



[<span data-ttu-id="bf787-133">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="bf787-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

