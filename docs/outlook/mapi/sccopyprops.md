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
# <a name="sccopyprops"></a><span data-ttu-id="30381-103">ScCopyProps</span><span class="sxs-lookup"><span data-stu-id="30381-103">ScCopyProps</span></span>

  
  
<span data-ttu-id="30381-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="30381-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="30381-105">Копирует свойства, определенные массивом [структур SPropValue,](spropvalue.md) в новое место назначения.</span><span class="sxs-lookup"><span data-stu-id="30381-105">Copies the properties defined by an array of [SPropValue](spropvalue.md) structures to a new destination.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="30381-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="30381-106">Header file:</span></span>  <br/> |<span data-ttu-id="30381-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="30381-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="30381-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="30381-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="30381-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="30381-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="30381-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="30381-110">Called by:</span></span>  <br/> |<span data-ttu-id="30381-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="30381-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCopyProps(
  int cprop,
  LPSPropValue rgprop,
  LPVOID pvDst,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="30381-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="30381-112">Parameters</span></span>

 <span data-ttu-id="30381-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="30381-113">_cprop_</span></span>
  
> <span data-ttu-id="30381-114">[in] Количество скопированные свойства.</span><span class="sxs-lookup"><span data-stu-id="30381-114">[in] Count of properties to be copied.</span></span> 
    
 <span data-ttu-id="30381-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="30381-115">_rgprop_</span></span>
  
> <span data-ttu-id="30381-116">[in] Указатель на массив структур [SPropValue,](spropvalue.md) которые определяют скопированные свойства.</span><span class="sxs-lookup"><span data-stu-id="30381-116">[in] Pointer to an array of [SPropValue](spropvalue.md) structures that define the properties to be copied.</span></span> <span data-ttu-id="30381-117">Параметр  _rgprop_ не должен указать на начало массива, но он должен указать на начало одной из структур **SPropValue** в массиве.</span><span class="sxs-lookup"><span data-stu-id="30381-117">The  _rgprop_ parameter does not have to point to the beginning of the array, but it must point to the beginning of one of the **SPropValue** structures in the array.</span></span> 
    
 <span data-ttu-id="30381-118">_pvDst_</span><span class="sxs-lookup"><span data-stu-id="30381-118">_pvDst_</span></span>
  
> <span data-ttu-id="30381-119">[in] Указатель на начальное положение в памяти, в которое эта функция копирует свойства.</span><span class="sxs-lookup"><span data-stu-id="30381-119">[in] Pointer to the initial position in memory to which this function copies the properties.</span></span> 
    
 <span data-ttu-id="30381-120">_pcb_</span><span class="sxs-lookup"><span data-stu-id="30381-120">_pcb_</span></span>
  
> <span data-ttu-id="30381-121">[out] Необязательный указатель на размер блока памяти, на который указывает параметр  _pvDst_ (в bytes).</span><span class="sxs-lookup"><span data-stu-id="30381-121">[out] Optional pointer to the size, in bytes, of the block of memory pointed to by the  _pvDst_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="30381-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="30381-122">Return value</span></span>

<span data-ttu-id="30381-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="30381-123">S_OK</span></span>
  
> <span data-ttu-id="30381-124">Свойства были успешно скопированы.</span><span class="sxs-lookup"><span data-stu-id="30381-124">Properties were copied successfully.</span></span>
    
<span data-ttu-id="30381-125">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="30381-125">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="30381-126">Был известен неизвестный тип свойства.</span><span class="sxs-lookup"><span data-stu-id="30381-126">An unknown property type was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="30381-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="30381-127">Remarks</span></span>

<span data-ttu-id="30381-128">Новый массив и его данные находятся в буфере, созданном с одним выделением, и функцию [ScRelocProps](screlocprops.md) можно использовать для настройки указателей в отдельных [структурах SPropValue.](spropvalue.md)</span><span class="sxs-lookup"><span data-stu-id="30381-128">The new array and its data reside in a buffer created with a single allocation, and the [ScRelocProps](screlocprops.md) function can be used to adjust the pointers in the individual [SPropValue](spropvalue.md) structures.</span></span> <span data-ttu-id="30381-129">До этой настройки допустимы указатели.</span><span class="sxs-lookup"><span data-stu-id="30381-129">Prior to this adjustment, the pointers are valid.</span></span> 
  
 <span data-ttu-id="30381-130">**ScCopyProps** поддерживает исходный порядок свойств для скопированного массива свойств.</span><span class="sxs-lookup"><span data-stu-id="30381-130">**ScCopyProps** maintains the original property order for the copied property array.</span></span> 
  
<span data-ttu-id="30381-131">Параметр _pcb_ является необязательным; Если он не NULL, ему задано количество вбайтов, хранимых в _параметре pvDst._</span><span class="sxs-lookup"><span data-stu-id="30381-131">The  _pcb_ parameter is optional; if it is not NULL, it is set to the number of bytes stored in the  _pvDst_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="30381-132">См. также</span><span class="sxs-lookup"><span data-stu-id="30381-132">See also</span></span>



[<span data-ttu-id="30381-133">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="30381-133">ScDupPropset</span></span>](scduppropset.md)

