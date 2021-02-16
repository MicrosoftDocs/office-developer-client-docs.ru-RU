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
# <a name="sccountprops"></a><span data-ttu-id="bed7e-103">ScCountProps</span><span class="sxs-lookup"><span data-stu-id="bed7e-103">ScCountProps</span></span>

  
  
<span data-ttu-id="bed7e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bed7e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bed7e-105">Определяет размер массива значений свойств (в bytes) и проверяет память, связанную с массивом.</span><span class="sxs-lookup"><span data-stu-id="bed7e-105">Determines the size, in bytes, of a property value array and validates the memory associated with the array.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bed7e-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="bed7e-106">Header file:</span></span>  <br/> |<span data-ttu-id="bed7e-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="bed7e-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="bed7e-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="bed7e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="bed7e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="bed7e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="bed7e-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="bed7e-110">Called by:</span></span>  <br/> |<span data-ttu-id="bed7e-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="bed7e-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCountProps(
  int cprop,
  LPSPropValue rgprop,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="bed7e-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="bed7e-112">Parameters</span></span>

 <span data-ttu-id="bed7e-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="bed7e-113">_cprop_</span></span>
  
> <span data-ttu-id="bed7e-114">[in] Количество свойств в массиве, указанных _параметром rgprop._</span><span class="sxs-lookup"><span data-stu-id="bed7e-114">[in] Count of properties in the array indicated by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="bed7e-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="bed7e-115">_rgprop_</span></span>
  
> <span data-ttu-id="bed7e-116">[in] Указатель на диапазон в массиве [структур SPropValue,](spropvalue.md) который определяет свойства, размер которых необходимо определить.</span><span class="sxs-lookup"><span data-stu-id="bed7e-116">[in] Pointer to a range in an array of [SPropValue](spropvalue.md) structures that defines the properties whose size is to be determined.</span></span> <span data-ttu-id="bed7e-117">Этот диапазон необязательно начинается с начала массива.</span><span class="sxs-lookup"><span data-stu-id="bed7e-117">This range does not necessarily start at the beginning of the array.</span></span> 
    
 <span data-ttu-id="bed7e-118">_pcb_</span><span class="sxs-lookup"><span data-stu-id="bed7e-118">_pcb_</span></span>
  
> <span data-ttu-id="bed7e-119">[out] Необязательный указатель на размер массива свойств (в bytes).</span><span class="sxs-lookup"><span data-stu-id="bed7e-119">[out] Optional pointer to the size, in bytes, of the property array.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bed7e-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bed7e-120">Return value</span></span>

<span data-ttu-id="bed7e-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="bed7e-121">S_OK</span></span> 
  
> <span data-ttu-id="bed7e-122">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="bed7e-122">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="bed7e-123">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="bed7e-123">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="bed7e-124">По крайней мере одно свойство в массиве значений свойств имеет идентификатор PROP_ID_NULL или PROP_ID_INVALID или массив свойств содержит многоценное свойство без значений свойств.</span><span class="sxs-lookup"><span data-stu-id="bed7e-124">At least one property in the property value array has an identifier of PROP_ID_NULL or PROP_ID_INVALID, or the property array contains a multivalued property with no property values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bed7e-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="bed7e-125">Remarks</span></span>

<span data-ttu-id="bed7e-126">Если в параметре  _PCB_ передается NULL, функция **ScCountProps** проверяет массив уведомлений, но подсчет не делается.</span><span class="sxs-lookup"><span data-stu-id="bed7e-126">If NULL is passed in the  _pcb_ parameter, the **ScCountProps** function validates the array of notifications but no counting is done.</span></span> <span data-ttu-id="bed7e-127">Если в _pcb_ передается ненулевое значение, функция **ScCountNotifications** определяет размер массива и сохраняет ПХБ _причины._</span><span class="sxs-lookup"><span data-stu-id="bed7e-127">If a non-null value is passed in  _pcb_, the **ScCountNotifications** function determines the size of the array and stores the cause  _pcb_.</span></span> <span data-ttu-id="bed7e-128">Параметр  _pcb_ должен быть достаточно большим, чтобы содержать весь массив.</span><span class="sxs-lookup"><span data-stu-id="bed7e-128">The  _pcb_ parameter must be large enough to contain the entire array.</span></span> 
  
<span data-ttu-id="bed7e-129">При подсчете **ScCountProps** проверяет память, связанную с массивом.</span><span class="sxs-lookup"><span data-stu-id="bed7e-129">As it is counting, **ScCountProps** validates the memory associated with the array.</span></span> <span data-ttu-id="bed7e-130">**ScCountProps** работает только со свойствами, сведения о которых есть в MAPI.</span><span class="sxs-lookup"><span data-stu-id="bed7e-130">**ScCountProps** only works with properties about which MAPI has information.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bed7e-131">См. также</span><span class="sxs-lookup"><span data-stu-id="bed7e-131">See also</span></span>



[<span data-ttu-id="bed7e-132">PropCopyMore</span><span class="sxs-lookup"><span data-stu-id="bed7e-132">PropCopyMore</span></span>](propcopymore.md)

