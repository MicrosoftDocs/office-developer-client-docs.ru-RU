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
ms.openlocfilehash: eb3b3b3c9c2e9cffb77febf9c96baed40ce3f9e8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566224"
---
# <a name="sccopyprops"></a><span data-ttu-id="cb5c2-103">ScCopyProps</span><span class="sxs-lookup"><span data-stu-id="cb5c2-103">ScCopyProps</span></span>

  
  
<span data-ttu-id="cb5c2-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cb5c2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cb5c2-105">Копирование свойств, определенных в массив структур [SPropValue](spropvalue.md) в новое место назначения.</span><span class="sxs-lookup"><span data-stu-id="cb5c2-105">Copies the properties defined by an array of [SPropValue](spropvalue.md) structures to a new destination.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cb5c2-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="cb5c2-106">Header file:</span></span>  <br/> |<span data-ttu-id="cb5c2-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="cb5c2-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="cb5c2-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="cb5c2-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="cb5c2-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="cb5c2-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="cb5c2-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="cb5c2-110">Called by:</span></span>  <br/> |<span data-ttu-id="cb5c2-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="cb5c2-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCopyProps(
  int cprop,
  LPSPropValue rgprop,
  LPVOID pvDst,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="cb5c2-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="cb5c2-112">Parameters</span></span>

 <span data-ttu-id="cb5c2-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="cb5c2-113">_cprop_</span></span>
  
> <span data-ttu-id="cb5c2-114">[in] Число свойств для копирования.</span><span class="sxs-lookup"><span data-stu-id="cb5c2-114">[in] Count of properties to be copied.</span></span> 
    
 <span data-ttu-id="cb5c2-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="cb5c2-115">_rgprop_</span></span>
  
> <span data-ttu-id="cb5c2-116">[in] Указатель на массив структур [SPropValue](spropvalue.md) , которые определяют свойства, которые нужно скопировать.</span><span class="sxs-lookup"><span data-stu-id="cb5c2-116">[in] Pointer to an array of [SPropValue](spropvalue.md) structures that define the properties to be copied.</span></span> <span data-ttu-id="cb5c2-117">Параметр _rgprop_ не нужно точки в начало массива, но он должен указывать в начало структур **SPropValue** в массиве.</span><span class="sxs-lookup"><span data-stu-id="cb5c2-117">The  _rgprop_ parameter does not have to point to the beginning of the array, but it must point to the beginning of one of the **SPropValue** structures in the array.</span></span> 
    
 <span data-ttu-id="cb5c2-118">_pvDst_</span><span class="sxs-lookup"><span data-stu-id="cb5c2-118">_pvDst_</span></span>
  
> <span data-ttu-id="cb5c2-119">[in] Указатель на начальное положение в памяти, к которому эта функция копирует свойства.</span><span class="sxs-lookup"><span data-stu-id="cb5c2-119">[in] Pointer to the initial position in memory to which this function copies the properties.</span></span> 
    
 <span data-ttu-id="cb5c2-120">_печатной_</span><span class="sxs-lookup"><span data-stu-id="cb5c2-120">_pcb_</span></span>
  
> <span data-ttu-id="cb5c2-121">[out] Необязательный указатель на размер, в байтах, блока памяти, на который указывает параметр _pvDst_ .</span><span class="sxs-lookup"><span data-stu-id="cb5c2-121">[out] Optional pointer to the size, in bytes, of the block of memory pointed to by the  _pvDst_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="cb5c2-122">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="cb5c2-122">Return value</span></span>

<span data-ttu-id="cb5c2-123">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="cb5c2-123">S_OK</span></span>
  
> <span data-ttu-id="cb5c2-124">Свойства были успешно скопированы.</span><span class="sxs-lookup"><span data-stu-id="cb5c2-124">Properties were copied successfully.</span></span>
    
<span data-ttu-id="cb5c2-125">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="cb5c2-125">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="cb5c2-126">Обнаружен неизвестный тип свойства.</span><span class="sxs-lookup"><span data-stu-id="cb5c2-126">An unknown property type was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cb5c2-127">Замечания</span><span class="sxs-lookup"><span data-stu-id="cb5c2-127">Remarks</span></span>

<span data-ttu-id="cb5c2-128">Новый массив и все данные размещаются в буфера, созданных с помощью одного выделения и функцию [ScRelocProps](screlocprops.md) можно использовать для настройки указателей в отдельных структур [SPropValue](spropvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="cb5c2-128">The new array and its data reside in a buffer created with a single allocation, and the [ScRelocProps](screlocprops.md) function can be used to adjust the pointers in the individual [SPropValue](spropvalue.md) structures.</span></span> <span data-ttu-id="cb5c2-129">Перед этой настройкой указатели являются допустимыми.</span><span class="sxs-lookup"><span data-stu-id="cb5c2-129">Prior to this adjustment, the pointers are valid.</span></span> 
  
 <span data-ttu-id="cb5c2-130">**ScCopyProps** сохраняет исходный порядок свойств для массива скопированные свойства.</span><span class="sxs-lookup"><span data-stu-id="cb5c2-130">**ScCopyProps** maintains the original property order for the copied property array.</span></span> 
  
<span data-ttu-id="cb5c2-131">Параметр _печатной_ является необязательным; Если не равно NULL, перейдут в число байтов, сохраненных в параметре _pvDst_ .</span><span class="sxs-lookup"><span data-stu-id="cb5c2-131">The  _pcb_ parameter is optional; if it is not NULL, it is set to the number of bytes stored in the  _pvDst_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cb5c2-132">См. также</span><span class="sxs-lookup"><span data-stu-id="cb5c2-132">See also</span></span>



[<span data-ttu-id="cb5c2-133">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="cb5c2-133">ScDupPropset</span></span>](scduppropset.md)

