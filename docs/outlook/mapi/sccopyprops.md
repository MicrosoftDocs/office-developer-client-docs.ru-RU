---
title: ScCopyProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCopyProps
api_type:
- COM
ms.assetid: 08bc256c-9706-4f3e-9a12-3e9cca5e4caa
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 1afd922459be2ec4bbbd27a61fdf6fcb425548c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411010"
---
# <a name="sccopyprops"></a><span data-ttu-id="87fb9-103">ScCopyProps</span><span class="sxs-lookup"><span data-stu-id="87fb9-103">ScCopyProps</span></span>

  
  
<span data-ttu-id="87fb9-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="87fb9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="87fb9-105">Копирует свойства, определенные массивом [структур SPropValue,](spropvalue.md) в новое назначение.</span><span class="sxs-lookup"><span data-stu-id="87fb9-105">Copies the properties defined by an array of [SPropValue](spropvalue.md) structures to a new destination.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="87fb9-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="87fb9-106">Header file:</span></span>  <br/> |<span data-ttu-id="87fb9-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="87fb9-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="87fb9-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="87fb9-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="87fb9-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="87fb9-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="87fb9-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="87fb9-110">Called by:</span></span>  <br/> |<span data-ttu-id="87fb9-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="87fb9-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCopyProps(
  int cprop,
  LPSPropValue rgprop,
  LPVOID pvDst,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="87fb9-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="87fb9-112">Parameters</span></span>

 <span data-ttu-id="87fb9-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="87fb9-113">_cprop_</span></span>
  
> <span data-ttu-id="87fb9-114">[in] Количество скопированные свойства.</span><span class="sxs-lookup"><span data-stu-id="87fb9-114">[in] Count of properties to be copied.</span></span> 
    
 <span data-ttu-id="87fb9-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="87fb9-115">_rgprop_</span></span>
  
> <span data-ttu-id="87fb9-116">[in] Указатель на массив [структур SPropValue,](spropvalue.md) которые определяют скопированные свойства.</span><span class="sxs-lookup"><span data-stu-id="87fb9-116">[in] Pointer to an array of [SPropValue](spropvalue.md) structures that define the properties to be copied.</span></span> <span data-ttu-id="87fb9-117">Параметр  _rgprop_ не должен указать на начало массива, но он должен указать на начало одной из структур **SPropValue** в массиве.</span><span class="sxs-lookup"><span data-stu-id="87fb9-117">The  _rgprop_ parameter does not have to point to the beginning of the array, but it must point to the beginning of one of the **SPropValue** structures in the array.</span></span> 
    
 <span data-ttu-id="87fb9-118">_pvDst_</span><span class="sxs-lookup"><span data-stu-id="87fb9-118">_pvDst_</span></span>
  
> <span data-ttu-id="87fb9-119">[in] Указатель на исходное положение в памяти, в которое эта функция копирует свойства.</span><span class="sxs-lookup"><span data-stu-id="87fb9-119">[in] Pointer to the initial position in memory to which this function copies the properties.</span></span> 
    
 <span data-ttu-id="87fb9-120">_pcb_</span><span class="sxs-lookup"><span data-stu-id="87fb9-120">_pcb_</span></span>
  
> <span data-ttu-id="87fb9-121">[вышел] Необязательный указатель на размер в bytes блока памяти, указываемого параметром _pvDst._</span><span class="sxs-lookup"><span data-stu-id="87fb9-121">[out] Optional pointer to the size, in bytes, of the block of memory pointed to by the  _pvDst_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="87fb9-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="87fb9-122">Return value</span></span>

<span data-ttu-id="87fb9-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="87fb9-123">S_OK</span></span>
  
> <span data-ttu-id="87fb9-124">Свойства были успешно скопированы.</span><span class="sxs-lookup"><span data-stu-id="87fb9-124">Properties were copied successfully.</span></span>
    
<span data-ttu-id="87fb9-125">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="87fb9-125">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="87fb9-126">Неизвестен тип свойства.</span><span class="sxs-lookup"><span data-stu-id="87fb9-126">An unknown property type was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="87fb9-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="87fb9-127">Remarks</span></span>

<span data-ttu-id="87fb9-128">Новый массив и его данные находятся в буфере, созданном с одним выделением, и для настройки указателей в отдельных структурах [SPropValue](spropvalue.md) можно использовать функцию [ScRelocProps.](screlocprops.md)</span><span class="sxs-lookup"><span data-stu-id="87fb9-128">The new array and its data reside in a buffer created with a single allocation, and the [ScRelocProps](screlocprops.md) function can be used to adjust the pointers in the individual [SPropValue](spropvalue.md) structures.</span></span> <span data-ttu-id="87fb9-129">До этой корректировки указатели действительны.</span><span class="sxs-lookup"><span data-stu-id="87fb9-129">Prior to this adjustment, the pointers are valid.</span></span> 
  
 <span data-ttu-id="87fb9-130">**ScCopyProps** поддерживает исходный порядок свойств для скопированного массива свойств.</span><span class="sxs-lookup"><span data-stu-id="87fb9-130">**ScCopyProps** maintains the original property order for the copied property array.</span></span> 
  
<span data-ttu-id="87fb9-131">Параметр _PCB_ необязателен; если это не NULL, оно задано для количества bytes, хранимого в _параметре pvDst._</span><span class="sxs-lookup"><span data-stu-id="87fb9-131">The  _pcb_ parameter is optional; if it is not NULL, it is set to the number of bytes stored in the  _pvDst_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="87fb9-132">См. также</span><span class="sxs-lookup"><span data-stu-id="87fb9-132">See also</span></span>



[<span data-ttu-id="87fb9-133">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="87fb9-133">ScDupPropset</span></span>](scduppropset.md)

