---
title: Итнефсетпропс
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
ms.openlocfilehash: f7372830624d774fb914ae956e86a9e4476cf487
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315052"
---
# <a name="itnefsetprops"></a><span data-ttu-id="42eff-103">ITnef::SetProps</span><span class="sxs-lookup"><span data-stu-id="42eff-103">ITnef::SetProps</span></span>

  
  
<span data-ttu-id="42eff-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="42eff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="42eff-105">Задает значение одного или нескольких свойств для инкапсулированного сообщения или вложения, не изменяя исходное сообщение или вложение.</span><span class="sxs-lookup"><span data-stu-id="42eff-105">Sets the value of one or more properties for an encapsulated message or attachment without modifying the original message or attachment.</span></span> 
  
```cpp
HRESULT SetProps(
  ULONG ulFlags,
  ULONG ulElemID,
  ULONG cValues,
  LPSPropValue lpProps
);
```

## <a name="parameters"></a><span data-ttu-id="42eff-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="42eff-106">Parameters</span></span>

 <span data-ttu-id="42eff-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="42eff-107">_ulFlags_</span></span>
  
> <span data-ttu-id="42eff-108">возврата Битовая маска флагов, определяющих, как устанавливаются значения свойств.</span><span class="sxs-lookup"><span data-stu-id="42eff-108">[in] A bitmask of flags that controls how property values are set.</span></span> <span data-ttu-id="42eff-109">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="42eff-109">The following flag can be set:</span></span>
    
<span data-ttu-id="42eff-110">ТНЕФ_ПРОП_КОНТАИНЕД</span><span class="sxs-lookup"><span data-stu-id="42eff-110">TNEF_PROP_CONTAINED</span></span> 
  
> <span data-ttu-id="42eff-111">Кодирует только свойства из сообщения или вложения, заданного параметром _улелемид_ .</span><span class="sxs-lookup"><span data-stu-id="42eff-111">Encodes only properties from the message or attachment specified by the  _ulElemID_ parameter.</span></span> 
    
 <span data-ttu-id="42eff-112">_Улелемид_</span><span class="sxs-lookup"><span data-stu-id="42eff-112">_ulElemID_</span></span>
  
> <span data-ttu-id="42eff-113">возврата Свойство **пр_аттач_нум** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) вложения, которое содержит число, уникально идентифицирующее вложение в родительском сообщении.</span><span class="sxs-lookup"><span data-stu-id="42eff-113">[in] An attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property, which contains a number that uniquely identifies the attachment in its parent message.</span></span>
    
 <span data-ttu-id="42eff-114">_Квалуес_</span><span class="sxs-lookup"><span data-stu-id="42eff-114">_cValues_</span></span>
  
> <span data-ttu-id="42eff-115">возврата Число значений свойств в структуре [спропвалуе](spropvalue.md) , на которую указывает параметр _лппропс_ .</span><span class="sxs-lookup"><span data-stu-id="42eff-115">[in] The number of property values in the [SPropValue](spropvalue.md) structure pointed to by the  _lpProps_ parameter.</span></span> 
    
 <span data-ttu-id="42eff-116">_Лппропс_</span><span class="sxs-lookup"><span data-stu-id="42eff-116">_lpProps_</span></span>
  
> <span data-ttu-id="42eff-117">возврата Указатель на структуру **спропвалуе** , которая содержит значения свойств свойств, которые необходимо задать.</span><span class="sxs-lookup"><span data-stu-id="42eff-117">[in] A pointer to an **SPropValue** structure that contains the property values of the properties to set.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="42eff-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="42eff-118">Return value</span></span>

<span data-ttu-id="42eff-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="42eff-119">S_OK</span></span> 
  
> <span data-ttu-id="42eff-120">Вызов выполнен успешно и вернул ожидаемое значение или значения.</span><span class="sxs-lookup"><span data-stu-id="42eff-120">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="42eff-121">Замечания</span><span class="sxs-lookup"><span data-stu-id="42eff-121">Remarks</span></span>

<span data-ttu-id="42eff-122">Поставщики транспорта, поставщики хранилищ сообщений и шлюзы вызывают метод **итнеф:: SetProps** , чтобы задать свойства, включаемые в инкапсуляцию сообщения или вложения, не изменяя исходное сообщение или вложение.</span><span class="sxs-lookup"><span data-stu-id="42eff-122">Transport providers, message store providers, and gateways call the **ITnef::SetProps** method to set properties to include in the encapsulation of a message or an attachment without modifying the original message or attachment.</span></span> <span data-ttu-id="42eff-123">Все свойства, заданные с помощью этого вызова, переопределяют существующие свойства в инкапсулированном сообщении.</span><span class="sxs-lookup"><span data-stu-id="42eff-123">Any properties set with this call override existing properties in the encapsulated message.</span></span> 
  
 <span data-ttu-id="42eff-124">**SetProps** поддерживается только для объектов TNEF, открытых с флагом тнеф_енкоде для функции [опентнефстреам](opentnefstream.md) или [опентнефстреамекс](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="42eff-124">**SetProps** is supported only for TNEF objects that are opened with the TNEF_ENCODE flag for the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> <span data-ttu-id="42eff-125">С этим вызовом можно задать любое количество свойств.</span><span class="sxs-lookup"><span data-stu-id="42eff-125">Any number of properties can be set with this call.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="42eff-126">Фактическое кодирование TNEF для **SetProps** происходит до тех пор, пока не будет вызван метод [Итнеф:: Finish](itnef-finish.md) .</span><span class="sxs-lookup"><span data-stu-id="42eff-126">No actual TNEF encoding for **SetProps** happens until after the [ITnef::Finish](itnef-finish.md) method is called.</span></span> <span data-ttu-id="42eff-127">Эта функция означает, что указатели, передаваемые в **SetProps** , должны быть действительными до выполнения вызова метода **Finish** .</span><span class="sxs-lookup"><span data-stu-id="42eff-127">This functionality means that pointers passed into **SetProps** must remain valid until after the call to **Finish** is made.</span></span> <span data-ttu-id="42eff-128">В этот момент все объекты и данные, переданные в вызовы **SetProps** , могут быть освобождены или освобождены.</span><span class="sxs-lookup"><span data-stu-id="42eff-128">At that point, all objects and data passed into **SetProps** calls can be released or freed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="42eff-129">См. также</span><span class="sxs-lookup"><span data-stu-id="42eff-129">See also</span></span>



[<span data-ttu-id="42eff-130">ITnef::Finish</span><span class="sxs-lookup"><span data-stu-id="42eff-130">ITnef::Finish</span></span>](itnef-finish.md)
  
[<span data-ttu-id="42eff-131">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="42eff-131">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="42eff-132">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="42eff-132">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="42eff-133">Каноническое свойство PidTagAttachNumber</span><span class="sxs-lookup"><span data-stu-id="42eff-133">PidTagAttachNumber Canonical Property</span></span>](pidtagattachnumber-canonical-property.md)
  
[<span data-ttu-id="42eff-134">SPropValue</span><span class="sxs-lookup"><span data-stu-id="42eff-134">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="42eff-135">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="42eff-135">ITnef : IUnknown</span></span>](itnefiunknown.md)

