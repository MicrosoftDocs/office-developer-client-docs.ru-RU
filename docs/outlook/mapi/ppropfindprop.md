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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350733"
---
# <a name="ppropfindprop"></a><span data-ttu-id="73a8c-103">PpropFindProp</span><span class="sxs-lookup"><span data-stu-id="73a8c-103">PpropFindProp</span></span>

  
  
<span data-ttu-id="73a8c-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="73a8c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="73a8c-105">Выполняет поиск указанного свойства в наборе свойств.</span><span class="sxs-lookup"><span data-stu-id="73a8c-105">Searches for a specified property in a property set.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="73a8c-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="73a8c-106">Header file:</span></span>  <br/> |<span data-ttu-id="73a8c-107">Мапиутил. h</span><span class="sxs-lookup"><span data-stu-id="73a8c-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="73a8c-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="73a8c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="73a8c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="73a8c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="73a8c-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="73a8c-110">Called by:</span></span>  <br/> |<span data-ttu-id="73a8c-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="73a8c-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSPropValue PpropFindProp(
  LPSPropValue rgprop,
  ULONG cprop,
  ULONG ulPropTag
);
```

## <a name="parameters"></a><span data-ttu-id="73a8c-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="73a8c-112">Parameters</span></span>

 <span data-ttu-id="73a8c-113">_ргпроп_</span><span class="sxs-lookup"><span data-stu-id="73a8c-113">_rgprop_</span></span>
  
> <span data-ttu-id="73a8c-114">возврата Массив структур [спропвалуе](spropvalue.md) , определяющих свойства для поиска.</span><span class="sxs-lookup"><span data-stu-id="73a8c-114">[in] Array of [SPropValue](spropvalue.md) structures that define the properties to be searched.</span></span> 
    
 <span data-ttu-id="73a8c-115">_кпроп_</span><span class="sxs-lookup"><span data-stu-id="73a8c-115">_cprop_</span></span>
  
> <span data-ttu-id="73a8c-116">возврата Количество свойств в наборе свойств, указанном с помощью параметра _ргпроп_ .</span><span class="sxs-lookup"><span data-stu-id="73a8c-116">[in] Count of properties in the property set indicated by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="73a8c-117">_Улпроптаг_</span><span class="sxs-lookup"><span data-stu-id="73a8c-117">_ulPropTag_</span></span>
  
> <span data-ttu-id="73a8c-118">возврата Тег Property для свойства, которое необходимо найти в наборе свойств, указанном с помощью параметра _ргпроп_ .</span><span class="sxs-lookup"><span data-stu-id="73a8c-118">[in] Property tag for the property to search for in the property set indicated by the  _rgprop_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="73a8c-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="73a8c-119">Return value</span></span>

 <span data-ttu-id="73a8c-120">**Ппропфиндпроп** возвращает структуру [спропвалуе](spropvalue.md) , определяющую свойство, которое соответствует тегу входного свойства, или значение null, если совпадение отсутствует.</span><span class="sxs-lookup"><span data-stu-id="73a8c-120">**PpropFindProp** returns an [SPropValue](spropvalue.md) structure defining the property that matches the input property tag, or NULL if there is no match.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="73a8c-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="73a8c-121">Remarks</span></span>

<span data-ttu-id="73a8c-122">Если заданный тег свойства указывает свойство типа ПТ_УНСПЕЦИФИЕД, функция **ппропфиндпроп** находит соответствующее значение только для идентификатора свойства в теге.</span><span class="sxs-lookup"><span data-stu-id="73a8c-122">If the given property tag indicates a property of type PT_UNSPECIFIED, the **PpropFindProp** function finds a match only for the property identifier in the tag.</span></span> <span data-ttu-id="73a8c-123">В противном случае обнаруживается сравнение для всего тега свойства, включая тип свойства, и возвращается указанное свойство.</span><span class="sxs-lookup"><span data-stu-id="73a8c-123">Otherwise, it finds a match for the entire property tag, including the property type, and returns the property identified.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="73a8c-124">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="73a8c-124">MFCMAPI reference</span></span>

<span data-ttu-id="73a8c-125">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="73a8c-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="73a8c-126">**Файл**</span><span class="sxs-lookup"><span data-stu-id="73a8c-126">**File**</span></span>|<span data-ttu-id="73a8c-127">**Функция**</span><span class="sxs-lookup"><span data-stu-id="73a8c-127">**Function**</span></span>|<span data-ttu-id="73a8c-128">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="73a8c-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="73a8c-129">Контентстаблелистктрл. cpp</span><span class="sxs-lookup"><span data-stu-id="73a8c-129">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="73a8c-130">Кконтентстаблелистктрл:: Буилддатаитем</span><span class="sxs-lookup"><span data-stu-id="73a8c-130">CContentsTableListCtrl::BuildDataItem</span></span>  <br/> |<span data-ttu-id="73a8c-131">MFCMAPI использует метод **ппропфиндпроп** для поиска свойств в наборе свойств, добавляемом в список.</span><span class="sxs-lookup"><span data-stu-id="73a8c-131">MFCMAPI uses the **PpropFindProp** method to find properties in a property set being added to the list.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="73a8c-132">См. также</span><span class="sxs-lookup"><span data-stu-id="73a8c-132">See also</span></span>



[<span data-ttu-id="73a8c-133">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="73a8c-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

