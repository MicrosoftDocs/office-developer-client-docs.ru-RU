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
ms.openlocfilehash: b7755f2ec067003e47d358a9736c6d7d96ede267
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812073"
---
# <a name="ppropfindprop"></a><span data-ttu-id="8c7a1-103">PpropFindProp</span><span class="sxs-lookup"><span data-stu-id="8c7a1-103">PpropFindProp</span></span>

  
  
<span data-ttu-id="8c7a1-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8c7a1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8c7a1-105">Настройка поиска для указанного свойства в свойстве.</span><span class="sxs-lookup"><span data-stu-id="8c7a1-105">Searches for a specified property in a property set.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8c7a1-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="8c7a1-106">Header file:</span></span>  <br/> |<span data-ttu-id="8c7a1-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="8c7a1-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="8c7a1-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="8c7a1-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="8c7a1-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="8c7a1-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="8c7a1-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="8c7a1-110">Called by:</span></span>  <br/> |<span data-ttu-id="8c7a1-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="8c7a1-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSPropValue PpropFindProp(
  LPSPropValue rgprop,
  ULONG cprop,
  ULONG ulPropTag
);
```

## <a name="parameters"></a><span data-ttu-id="8c7a1-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="8c7a1-112">Parameters</span></span>

 <span data-ttu-id="8c7a1-113">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="8c7a1-113">_rgprop_</span></span>
  
> <span data-ttu-id="8c7a1-114">[in] Массив структур [SPropValue](spropvalue.md) , которые определяют свойства для поиска.</span><span class="sxs-lookup"><span data-stu-id="8c7a1-114">[in] Array of [SPropValue](spropvalue.md) structures that define the properties to be searched.</span></span> 
    
 <span data-ttu-id="8c7a1-115">_cprop_</span><span class="sxs-lookup"><span data-stu-id="8c7a1-115">_cprop_</span></span>
  
> <span data-ttu-id="8c7a1-116">[in] Число свойств в набор свойств, указанное с помощью параметра _rgprop_ .</span><span class="sxs-lookup"><span data-stu-id="8c7a1-116">[in] Count of properties in the property set indicated by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="8c7a1-117">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="8c7a1-117">_ulPropTag_</span></span>
  
> <span data-ttu-id="8c7a1-118">[in] Свойство tag для свойства для поиска в набор свойств, указанное с помощью параметра _rgprop_ .</span><span class="sxs-lookup"><span data-stu-id="8c7a1-118">[in] Property tag for the property to search for in the property set indicated by the  _rgprop_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8c7a1-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9">Return value</span></span>

 <span data-ttu-id="8c7a1-120">**PpropFindProp** возвращает структуру [SPropValue](spropvalue.md) , определяющего свойство, соответствующий тег ввода свойство или значение NULL, если нет соответствия.</span><span class="sxs-lookup"><span data-stu-id="8c7a1-120">**PpropFindProp** returns an [SPropValue](spropvalue.md) structure defining the property that matches the input property tag, or NULL if there is no match.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="8c7a1-121">Замечания</span><span class="sxs-lookup"><span data-stu-id="8c7a1-121">Remarks</span></span>

<span data-ttu-id="8c7a1-122">Если данное свойство tag указывает свойство типа PT_UNSPECIFIED, функция **PpropFindProp** будет выполняться только для идентификатора свойства в теге.</span><span class="sxs-lookup"><span data-stu-id="8c7a1-122">If the given property tag indicates a property of type PT_UNSPECIFIED, the **PpropFindProp** function finds a match only for the property identifier in the tag.</span></span> <span data-ttu-id="8c7a1-123">В противном случае находит соответствие для тега всего свойства, включая тип свойства и возвращает свойство определяемую.</span><span class="sxs-lookup"><span data-stu-id="8c7a1-123">Otherwise, it finds a match for the entire property tag, including the property type, and returns the property identified.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="8c7a1-124">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="8c7a1-124">MFCMAPI reference</span></span>

<span data-ttu-id="8c7a1-125">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="8c7a1-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="8c7a1-126">**����**</span><span class="sxs-lookup"><span data-stu-id="8c7a1-126">**File**</span></span>|<span data-ttu-id="8c7a1-127">**�������**</span><span class="sxs-lookup"><span data-stu-id="8c7a1-127">**Function**</span></span>|<span data-ttu-id="8c7a1-128">**�����������**</span><span class="sxs-lookup"><span data-stu-id="8c7a1-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8c7a1-129">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="8c7a1-129">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="8c7a1-130">CContentsTableListCtrl::BuildDataItem</span><span class="sxs-lookup"><span data-stu-id="8c7a1-130">CContentsTableListCtrl::BuildDataItem</span></span>  <br/> |<span data-ttu-id="8c7a1-131">Mfcmapi (en) использует метод **PpropFindProp** для поиска набора свойств в свойство, добавляемого в список.</span><span class="sxs-lookup"><span data-stu-id="8c7a1-131">MFCMAPI uses the **PpropFindProp** method to find properties in a property set being added to the list.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8c7a1-132">См. также</span><span class="sxs-lookup"><span data-stu-id="8c7a1-132">See also</span></span>



[<span data-ttu-id="8c7a1-133">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="8c7a1-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

