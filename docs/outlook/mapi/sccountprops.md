---
title: ScCountProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCountProps
api_type:
- COM
ms.assetid: 76e4cc52-e1a0-4e0b-a2a6-a17644f6b2e7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 49634bda487143ddd8d8806b94f6c451ccf57b75
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404976"
---
# <a name="sccountprops"></a><span data-ttu-id="f94eb-103">ScCountProps</span><span class="sxs-lookup"><span data-stu-id="f94eb-103">ScCountProps</span></span>

  
  
<span data-ttu-id="f94eb-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f94eb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f94eb-105">Определяет размер в bytes массива значений свойств и проверяет память, связанную с массивом.</span><span class="sxs-lookup"><span data-stu-id="f94eb-105">Determines the size, in bytes, of a property value array and validates the memory associated with the array.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f94eb-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="f94eb-106">Header file:</span></span>  <br/> |<span data-ttu-id="f94eb-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="f94eb-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="f94eb-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="f94eb-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f94eb-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f94eb-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f94eb-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="f94eb-110">Called by:</span></span>  <br/> |<span data-ttu-id="f94eb-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="f94eb-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCountProps(
  int cprop,
  LPSPropValue rgprop,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="f94eb-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="f94eb-112">Parameters</span></span>

 <span data-ttu-id="f94eb-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="f94eb-113">_cprop_</span></span>
  
> <span data-ttu-id="f94eb-114">[in] Количество свойств в массиве, указанных параметром _rgprop._</span><span class="sxs-lookup"><span data-stu-id="f94eb-114">[in] Count of properties in the array indicated by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="f94eb-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="f94eb-115">_rgprop_</span></span>
  
> <span data-ttu-id="f94eb-116">[in] Указатель на диапазон в массиве [структур SPropValue,](spropvalue.md) определяя свойства, размер которых должен быть определен.</span><span class="sxs-lookup"><span data-stu-id="f94eb-116">[in] Pointer to a range in an array of [SPropValue](spropvalue.md) structures that defines the properties whose size is to be determined.</span></span> <span data-ttu-id="f94eb-117">Этот диапазон не обязательно начинается в начале массива.</span><span class="sxs-lookup"><span data-stu-id="f94eb-117">This range does not necessarily start at the beginning of the array.</span></span> 
    
 <span data-ttu-id="f94eb-118">_pcb_</span><span class="sxs-lookup"><span data-stu-id="f94eb-118">_pcb_</span></span>
  
> <span data-ttu-id="f94eb-119">[вышел] Необязательный указатель на размер в bytes массива свойств.</span><span class="sxs-lookup"><span data-stu-id="f94eb-119">[out] Optional pointer to the size, in bytes, of the property array.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f94eb-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f94eb-120">Return value</span></span>

<span data-ttu-id="f94eb-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="f94eb-121">S_OK</span></span> 
  
> <span data-ttu-id="f94eb-122">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="f94eb-122">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="f94eb-123">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f94eb-123">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="f94eb-124">По крайней мере одно свойство в массиве значений свойств имеет идентификатор PROP_ID_NULL или PROP_ID_INVALID или массив свойств содержит многоценное свойство без значений свойств.</span><span class="sxs-lookup"><span data-stu-id="f94eb-124">At least one property in the property value array has an identifier of PROP_ID_NULL or PROP_ID_INVALID, or the property array contains a multivalued property with no property values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f94eb-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="f94eb-125">Remarks</span></span>

<span data-ttu-id="f94eb-126">Если NULL передается в  _параметре PCB,_ функция **ScCountProps** проверяет массив уведомлений, но подсчет не делается.</span><span class="sxs-lookup"><span data-stu-id="f94eb-126">If NULL is passed in the  _pcb_ parameter, the **ScCountProps** function validates the array of notifications but no counting is done.</span></span> <span data-ttu-id="f94eb-127">Если значение non-null передается в _pcb,_ функция **ScCountNotifications** определяет размер массива и сохраняет причину _pcb._</span><span class="sxs-lookup"><span data-stu-id="f94eb-127">If a non-null value is passed in  _pcb_, the **ScCountNotifications** function determines the size of the array and stores the cause  _pcb_.</span></span> <span data-ttu-id="f94eb-128">Параметр  _PCB_ должен быть достаточно большим, чтобы содержать весь массив.</span><span class="sxs-lookup"><span data-stu-id="f94eb-128">The  _pcb_ parameter must be large enough to contain the entire array.</span></span> 
  
<span data-ttu-id="f94eb-129">При подсчете **scCountProps** проверяет память, связанную с массивом.</span><span class="sxs-lookup"><span data-stu-id="f94eb-129">As it is counting, **ScCountProps** validates the memory associated with the array.</span></span> <span data-ttu-id="f94eb-130">**ScCountProps** работает только с свойствами, сведения о которых имеются в MAPI.</span><span class="sxs-lookup"><span data-stu-id="f94eb-130">**ScCountProps** only works with properties about which MAPI has information.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f94eb-131">См. также</span><span class="sxs-lookup"><span data-stu-id="f94eb-131">See also</span></span>



[<span data-ttu-id="f94eb-132">PropCopyMore</span><span class="sxs-lookup"><span data-stu-id="f94eb-132">PropCopyMore</span></span>](propcopymore.md)

