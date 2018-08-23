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
ms.openlocfilehash: f720160193613bbbb4bbd447f78c14e6e5378eb8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565657"
---
# <a name="ppropfindprop"></a><span data-ttu-id="cb411-103">PpropFindProp</span><span class="sxs-lookup"><span data-stu-id="cb411-103">PpropFindProp</span></span>

  
  
<span data-ttu-id="cb411-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cb411-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cb411-105">Настройка поиска для указанного свойства в свойстве.</span><span class="sxs-lookup"><span data-stu-id="cb411-105">Searches for a specified property in a property set.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cb411-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="cb411-106">Header file:</span></span>  <br/> |<span data-ttu-id="cb411-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="cb411-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="cb411-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="cb411-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="cb411-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="cb411-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="cb411-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="cb411-110">Called by:</span></span>  <br/> |<span data-ttu-id="cb411-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="cb411-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSPropValue PpropFindProp(
  LPSPropValue rgprop,
  ULONG cprop,
  ULONG ulPropTag
);
```

## <a name="parameters"></a><span data-ttu-id="cb411-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="cb411-112">Parameters</span></span>

 <span data-ttu-id="cb411-113">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="cb411-113">_rgprop_</span></span>
  
> <span data-ttu-id="cb411-114">[in] Массив структур [SPropValue](spropvalue.md) , которые определяют свойства для поиска.</span><span class="sxs-lookup"><span data-stu-id="cb411-114">[in] Array of [SPropValue](spropvalue.md) structures that define the properties to be searched.</span></span> 
    
 <span data-ttu-id="cb411-115">_cprop_</span><span class="sxs-lookup"><span data-stu-id="cb411-115">_cprop_</span></span>
  
> <span data-ttu-id="cb411-116">[in] Число свойств в набор свойств, указанное с помощью параметра _rgprop_ .</span><span class="sxs-lookup"><span data-stu-id="cb411-116">[in] Count of properties in the property set indicated by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="cb411-117">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="cb411-117">_ulPropTag_</span></span>
  
> <span data-ttu-id="cb411-118">[in] Свойство tag для свойства для поиска в набор свойств, указанное с помощью параметра _rgprop_ .</span><span class="sxs-lookup"><span data-stu-id="cb411-118">[in] Property tag for the property to search for in the property set indicated by the  _rgprop_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="cb411-119">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="cb411-119">Return value</span></span>

 <span data-ttu-id="cb411-120">**PpropFindProp** возвращает структуру [SPropValue](spropvalue.md) , определяющего свойство, соответствующий тег ввода свойство или значение NULL, если нет соответствия.</span><span class="sxs-lookup"><span data-stu-id="cb411-120">**PpropFindProp** returns an [SPropValue](spropvalue.md) structure defining the property that matches the input property tag, or NULL if there is no match.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="cb411-121">Замечания</span><span class="sxs-lookup"><span data-stu-id="cb411-121">Remarks</span></span>

<span data-ttu-id="cb411-122">Если данное свойство tag указывает свойство типа PT_UNSPECIFIED, функция **PpropFindProp** будет выполняться только для идентификатора свойства в теге.</span><span class="sxs-lookup"><span data-stu-id="cb411-122">If the given property tag indicates a property of type PT_UNSPECIFIED, the **PpropFindProp** function finds a match only for the property identifier in the tag.</span></span> <span data-ttu-id="cb411-123">В противном случае находит соответствие для тега всего свойства, включая тип свойства и возвращает свойство определяемую.</span><span class="sxs-lookup"><span data-stu-id="cb411-123">Otherwise, it finds a match for the entire property tag, including the property type, and returns the property identified.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="cb411-124">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="cb411-124">MFCMAPI reference</span></span>

<span data-ttu-id="cb411-125">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="cb411-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="cb411-126">**����**</span><span class="sxs-lookup"><span data-stu-id="cb411-126">**File**</span></span>|<span data-ttu-id="cb411-127">**�������**</span><span class="sxs-lookup"><span data-stu-id="cb411-127">**Function**</span></span>|<span data-ttu-id="cb411-128">**�����������**</span><span class="sxs-lookup"><span data-stu-id="cb411-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cb411-129">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="cb411-129">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="cb411-130">CContentsTableListCtrl::BuildDataItem</span><span class="sxs-lookup"><span data-stu-id="cb411-130">CContentsTableListCtrl::BuildDataItem</span></span>  <br/> |<span data-ttu-id="cb411-131">Mfcmapi (en) использует метод **PpropFindProp** для поиска набора свойств в свойство, добавляемого в список.</span><span class="sxs-lookup"><span data-stu-id="cb411-131">MFCMAPI uses the **PpropFindProp** method to find properties in a property set being added to the list.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cb411-132">См. также</span><span class="sxs-lookup"><span data-stu-id="cb411-132">See also</span></span>



[<span data-ttu-id="cb411-133">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="cb411-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

