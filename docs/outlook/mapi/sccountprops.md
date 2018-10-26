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
ms.openlocfilehash: ee004bdfb8d13537fd8823225f155223ebc76ca7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583353"
---
# <a name="sccountprops"></a><span data-ttu-id="269d8-103">ScCountProps</span><span class="sxs-lookup"><span data-stu-id="269d8-103">ScCountProps</span></span>

  
  
<span data-ttu-id="269d8-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="269d8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="269d8-105">Определяет размер в байтах, массива значение свойства и проверяет память, связанную с массивом.</span><span class="sxs-lookup"><span data-stu-id="269d8-105">Determines the size, in bytes, of a property value array and validates the memory associated with the array.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="269d8-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="269d8-106">Header file:</span></span>  <br/> |<span data-ttu-id="269d8-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="269d8-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="269d8-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="269d8-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="269d8-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="269d8-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="269d8-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="269d8-110">Called by:</span></span>  <br/> |<span data-ttu-id="269d8-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="269d8-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCountProps(
  int cprop,
  LPSPropValue rgprop,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="269d8-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="269d8-112">Parameters</span></span>

 <span data-ttu-id="269d8-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="269d8-113">_cprop_</span></span>
  
> <span data-ttu-id="269d8-114">[in] Число свойств в массива, указанного в параметре _rgprop_ .</span><span class="sxs-lookup"><span data-stu-id="269d8-114">[in] Count of properties in the array indicated by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="269d8-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="269d8-115">_rgprop_</span></span>
  
> <span data-ttu-id="269d8-116">[in] Указатель для диапазона ячеек в массив структур [SPropValue](spropvalue.md) , который определяет свойства, размер которого будет определено.</span><span class="sxs-lookup"><span data-stu-id="269d8-116">[in] Pointer to a range in an array of [SPropValue](spropvalue.md) structures that defines the properties whose size is to be determined.</span></span> <span data-ttu-id="269d8-117">Этот диапазон не обязательно запускается в начале массива.</span><span class="sxs-lookup"><span data-stu-id="269d8-117">This range does not necessarily start at the beginning of the array.</span></span> 
    
 <span data-ttu-id="269d8-118">_печатной_</span><span class="sxs-lookup"><span data-stu-id="269d8-118">_pcb_</span></span>
  
> <span data-ttu-id="269d8-119">[out] Необязательный указатель на размер, в байтах, свойство массива.</span><span class="sxs-lookup"><span data-stu-id="269d8-119">[out] Optional pointer to the size, in bytes, of the property array.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="269d8-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="269d8-120">Return value</span></span>

<span data-ttu-id="269d8-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="269d8-121">S_OK</span></span> 
  
> <span data-ttu-id="269d8-122">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="269d8-122">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="269d8-123">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="269d8-123">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="269d8-124">По крайней мере одно свойство в массиве значение свойства имеет идентификатор PROP_ID_NULL или PROP_ID_INVALID или массива свойства содержит многозначного свойства нет значения свойства.</span><span class="sxs-lookup"><span data-stu-id="269d8-124">At least one property in the property value array has an identifier of PROP_ID_NULL or PROP_ID_INVALID, or the property array contains a multivalued property with no property values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="269d8-125">Замечания</span><span class="sxs-lookup"><span data-stu-id="269d8-125">Remarks</span></span>

<span data-ttu-id="269d8-126">Если в параметре _печатной_ передано значение NULL, функция **ScCountProps** проверяет массива уведомления о, но инвентаризации не выполняется.</span><span class="sxs-lookup"><span data-stu-id="269d8-126">If NULL is passed in the  _pcb_ parameter, the **ScCountProps** function validates the array of notifications but no counting is done.</span></span> <span data-ttu-id="269d8-127">Если ненулевое значение передается в _печатной_, функция **ScCountNotifications** определяет размер массива и сохраняет несколько _печатной_.</span><span class="sxs-lookup"><span data-stu-id="269d8-127">If a non-null value is passed in  _pcb_, the **ScCountNotifications** function determines the size of the array and stores the cause  _pcb_.</span></span> <span data-ttu-id="269d8-128">Параметр _печатной_ должен быть достаточно большим для размещения всего массива.</span><span class="sxs-lookup"><span data-stu-id="269d8-128">The  _pcb_ parameter must be large enough to contain the entire array.</span></span> 
  
<span data-ttu-id="269d8-129">Как подсчет, **ScCountProps** проверяет память, связанную с массивом.</span><span class="sxs-lookup"><span data-stu-id="269d8-129">As it is counting, **ScCountProps** validates the memory associated with the array.</span></span> <span data-ttu-id="269d8-130">**ScCountProps** работает только со свойствами, о том, какие заполнению MAPI.</span><span class="sxs-lookup"><span data-stu-id="269d8-130">**ScCountProps** only works with properties about which MAPI has information.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="269d8-131">См. также</span><span class="sxs-lookup"><span data-stu-id="269d8-131">See also</span></span>



[<span data-ttu-id="269d8-132">PropCopyMore</span><span class="sxs-lookup"><span data-stu-id="269d8-132">PropCopyMore</span></span>](propcopymore.md)

