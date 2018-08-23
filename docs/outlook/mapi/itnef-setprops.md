---
title: ITnefSetProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.SetProps
api_type:
- COM
ms.assetid: 09e4b427-316b-4630-9f3d-81e74f040d7b
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 81f9388b67d3194fe1442091b9f4f75a7671cb6d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579650"
---
# <a name="itnefsetprops"></a><span data-ttu-id="0940e-103">ITnef::SetProps</span><span class="sxs-lookup"><span data-stu-id="0940e-103">ITnef::SetProps</span></span>

  
  
<span data-ttu-id="0940e-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0940e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0940e-105">Задает значение одного или нескольких свойств для инкапсулированное сообщение или вложение без изменения исходного сообщения или вложения.</span><span class="sxs-lookup"><span data-stu-id="0940e-105">Sets the value of one or more properties for an encapsulated message or attachment without modifying the original message or attachment.</span></span> 
  
```cpp
HRESULT SetProps(
  ULONG ulFlags,
  ULONG ulElemID,
  ULONG cValues,
  LPSPropValue lpProps
);
```

## <a name="parameters"></a><span data-ttu-id="0940e-106">���������</span><span class="sxs-lookup"><span data-stu-id="0940e-106">Parameters</span></span>

 <span data-ttu-id="0940e-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0940e-107">_ulFlags_</span></span>
  
> <span data-ttu-id="0940e-108">[in] Битовая маска флаги, который определяет, как задать значения свойств.</span><span class="sxs-lookup"><span data-stu-id="0940e-108">[in] A bitmask of flags that controls how property values are set.</span></span> <span data-ttu-id="0940e-109">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="0940e-109">The following flag can be set:</span></span>
    
<span data-ttu-id="0940e-110">TNEF_PROP_CONTAINED</span><span class="sxs-lookup"><span data-stu-id="0940e-110">TNEF_PROP_CONTAINED</span></span> 
  
> <span data-ttu-id="0940e-111">Кодирует только свойства из сообщения или вложения, указанного с помощью параметра _ulElemID_ .</span><span class="sxs-lookup"><span data-stu-id="0940e-111">Encodes only properties from the message or attachment specified by the  _ulElemID_ parameter.</span></span> 
    
 <span data-ttu-id="0940e-112">_ulElemID_</span><span class="sxs-lookup"><span data-stu-id="0940e-112">_ulElemID_</span></span>
  
> <span data-ttu-id="0940e-113">[in] Свойство **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) вложения, которое содержит число, однозначно идентифицирует вложения в сообщение его родительского.</span><span class="sxs-lookup"><span data-stu-id="0940e-113">[in] An attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property, which contains a number that uniquely identifies the attachment in its parent message.</span></span>
    
 <span data-ttu-id="0940e-114">_cValues_</span><span class="sxs-lookup"><span data-stu-id="0940e-114">_cValues_</span></span>
  
> <span data-ttu-id="0940e-115">[in] Количество значений свойств в структуре [SPropValue](spropvalue.md) указывает параметр _lpProps_ .</span><span class="sxs-lookup"><span data-stu-id="0940e-115">[in] The number of property values in the [SPropValue](spropvalue.md) structure pointed to by the  _lpProps_ parameter.</span></span> 
    
 <span data-ttu-id="0940e-116">_lpProps_</span><span class="sxs-lookup"><span data-stu-id="0940e-116">_lpProps_</span></span>
  
> <span data-ttu-id="0940e-117">[in] Указатель на структуру **SPropValue** , который содержит значения свойств свойства, которые нужно установить.</span><span class="sxs-lookup"><span data-stu-id="0940e-117">[in] A pointer to an **SPropValue** structure that contains the property values of the properties to set.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0940e-118">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="0940e-118">Return value</span></span>

<span data-ttu-id="0940e-119">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="0940e-119">S_OK</span></span> 
  
> <span data-ttu-id="0940e-120">Вызов успешно и возвращается ожидаемым значением или значения.</span><span class="sxs-lookup"><span data-stu-id="0940e-120">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0940e-121">Замечания</span><span class="sxs-lookup"><span data-stu-id="0940e-121">Remarks</span></span>

<span data-ttu-id="0940e-122">Для передачи поставщиков, поставщиков хранилища сообщений и шлюзов вызова метода **ITnef::SetProps** для настройки свойств для включения в инкапсуляция вложения или сообщения без изменения исходного сообщения или вложения.</span><span class="sxs-lookup"><span data-stu-id="0940e-122">Transport providers, message store providers, and gateways call the **ITnef::SetProps** method to set properties to include in the encapsulation of a message or an attachment without modifying the original message or attachment.</span></span> <span data-ttu-id="0940e-123">Все свойства, заданные с этим звонком переопределить существующие свойства в инкапсулированное сообщение.</span><span class="sxs-lookup"><span data-stu-id="0940e-123">Any properties set with this call override existing properties in the encapsulated message.</span></span> 
  
 <span data-ttu-id="0940e-124">**SetProps** поддерживается только для объектов TNEF, которые открываются с флагом TNEF_ENCODE для функции [OpenTnefStream](opentnefstream.md) или [OpenTnefStreamEx](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="0940e-124">**SetProps** is supported only for TNEF objects that are opened with the TNEF_ENCODE flag for the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> <span data-ttu-id="0940e-125">С помощью этого вызова можно задать любое количество свойств.</span><span class="sxs-lookup"><span data-stu-id="0940e-125">Any number of properties can be set with this call.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="0940e-126">Без фактического кодировка TNEF для **SetProps** происходит до того времени, после вызова метода [ITnef::Finish](itnef-finish.md) .</span><span class="sxs-lookup"><span data-stu-id="0940e-126">No actual TNEF encoding for **SetProps** happens until after the [ITnef::Finish](itnef-finish.md) method is called.</span></span> <span data-ttu-id="0940e-127">Данная функциональная возможность означает, что был передан в **SetProps** указатели должны оставаться действительно до, после **завершения** вызова.</span><span class="sxs-lookup"><span data-stu-id="0940e-127">This functionality means that pointers passed into **SetProps** must remain valid until after the call to **Finish** is made.</span></span> <span data-ttu-id="0940e-128">На этом этапе всех объектов и данных, передаваемых в **SetProps** вызовы можно выпущен или освобождении.</span><span class="sxs-lookup"><span data-stu-id="0940e-128">At that point, all objects and data passed into **SetProps** calls can be released or freed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0940e-129">См. также</span><span class="sxs-lookup"><span data-stu-id="0940e-129">See also</span></span>



[<span data-ttu-id="0940e-130">ITnef::Finish</span><span class="sxs-lookup"><span data-stu-id="0940e-130">ITnef::Finish</span></span>](itnef-finish.md)
  
[<span data-ttu-id="0940e-131">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="0940e-131">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="0940e-132">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="0940e-132">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="0940e-133">Каноническое свойство PidTagAttachNumber</span><span class="sxs-lookup"><span data-stu-id="0940e-133">PidTagAttachNumber Canonical Property</span></span>](pidtagattachnumber-canonical-property.md)
  
[<span data-ttu-id="0940e-134">SPropValue</span><span class="sxs-lookup"><span data-stu-id="0940e-134">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="0940e-135">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0940e-135">ITnef : IUnknown</span></span>](itnefiunknown.md)

