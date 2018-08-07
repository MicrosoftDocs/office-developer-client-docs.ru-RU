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
ms.openlocfilehash: 979415f1d792f92e593a7073cc84cfd6ba832b6c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812191"
---
# <a name="sccopyprops"></a><span data-ttu-id="d91a6-103">ScCopyProps</span><span class="sxs-lookup"><span data-stu-id="d91a6-103">ScCopyProps</span></span>

  
  
<span data-ttu-id="d91a6-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d91a6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d91a6-105">Копирование свойств, определенных в массив структур [SPropValue](spropvalue.md) в новое место назначения.</span><span class="sxs-lookup"><span data-stu-id="d91a6-105">Copies the properties defined by an array of [SPropValue](spropvalue.md) structures to a new destination.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d91a6-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="d91a6-106">Header file:</span></span>  <br/> |<span data-ttu-id="d91a6-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="d91a6-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="d91a6-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="d91a6-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d91a6-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d91a6-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d91a6-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="d91a6-110">Called by:</span></span>  <br/> |<span data-ttu-id="d91a6-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="d91a6-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCopyProps(
  int cprop,
  LPSPropValue rgprop,
  LPVOID pvDst,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="d91a6-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="d91a6-112">Parameters</span></span>

 <span data-ttu-id="d91a6-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="d91a6-113">_cprop_</span></span>
  
> <span data-ttu-id="d91a6-114">[in] Число свойств для копирования.</span><span class="sxs-lookup"><span data-stu-id="d91a6-114">[in] Count of properties to be copied.</span></span> 
    
 <span data-ttu-id="d91a6-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="d91a6-115">_rgprop_</span></span>
  
> <span data-ttu-id="d91a6-116">[in] Указатель на массив структур [SPropValue](spropvalue.md) , которые определяют свойства, которые нужно скопировать.</span><span class="sxs-lookup"><span data-stu-id="d91a6-116">[in] Pointer to an array of [SPropValue](spropvalue.md) structures that define the properties to be copied.</span></span> <span data-ttu-id="d91a6-117">Параметр _rgprop_ не нужно точки в начало массива, но он должен указывать в начало структур **SPropValue** в массиве.</span><span class="sxs-lookup"><span data-stu-id="d91a6-117">The  _rgprop_ parameter does not have to point to the beginning of the array, but it must point to the beginning of one of the **SPropValue** structures in the array.</span></span> 
    
 <span data-ttu-id="d91a6-118">_pvDst_</span><span class="sxs-lookup"><span data-stu-id="d91a6-118">_pvDst_</span></span>
  
> <span data-ttu-id="d91a6-119">[in] Указатель на начальное положение в памяти, к которому эта функция копирует свойства.</span><span class="sxs-lookup"><span data-stu-id="d91a6-119">[in] Pointer to the initial position in memory to which this function copies the properties.</span></span> 
    
 <span data-ttu-id="d91a6-120">_печатной_</span><span class="sxs-lookup"><span data-stu-id="d91a6-120">_pcb_</span></span>
  
> <span data-ttu-id="d91a6-121">[out] Необязательный указатель на размер, в байтах, блока памяти, на который указывает параметр _pvDst_ .</span><span class="sxs-lookup"><span data-stu-id="d91a6-121">[out] Optional pointer to the size, in bytes, of the block of memory pointed to by the  _pvDst_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d91a6-122">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="d91a6-122">Return value</span></span>

<span data-ttu-id="d91a6-123">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="d91a6-123">S_OK</span></span>
  
> <span data-ttu-id="d91a6-124">Свойства были успешно скопированы.</span><span class="sxs-lookup"><span data-stu-id="d91a6-124">Properties were copied successfully.</span></span>
    
<span data-ttu-id="d91a6-125">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d91a6-125">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="d91a6-126">Обнаружен неизвестный тип свойства.</span><span class="sxs-lookup"><span data-stu-id="d91a6-126">An unknown property type was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d91a6-127">Замечания</span><span class="sxs-lookup"><span data-stu-id="d91a6-127">Remarks</span></span>

<span data-ttu-id="d91a6-128">Новый массив и все данные размещаются в буфера, созданных с помощью одного выделения и функцию [ScRelocProps](screlocprops.md) можно использовать для настройки указателей в отдельных структур [SPropValue](spropvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="d91a6-128">The new array and its data reside in a buffer created with a single allocation, and the [ScRelocProps](screlocprops.md) function can be used to adjust the pointers in the individual [SPropValue](spropvalue.md) structures.</span></span> <span data-ttu-id="d91a6-129">Перед этой настройкой указатели являются допустимыми.</span><span class="sxs-lookup"><span data-stu-id="d91a6-129">Prior to this adjustment, the pointers are valid.</span></span> 
  
 <span data-ttu-id="d91a6-130">**ScCopyProps** сохраняет исходный порядок свойств для массива скопированные свойства.</span><span class="sxs-lookup"><span data-stu-id="d91a6-130">**ScCopyProps** maintains the original property order for the copied property array.</span></span> 
  
<span data-ttu-id="d91a6-131">Параметр _печатной_ является необязательным; Если не равно NULL, перейдут в число байтов, сохраненных в параметре _pvDst_ .</span><span class="sxs-lookup"><span data-stu-id="d91a6-131">The  _pcb_ parameter is optional; if it is not NULL, it is set to the number of bytes stored in the  _pvDst_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d91a6-132">См. также</span><span class="sxs-lookup"><span data-stu-id="d91a6-132">See also</span></span>



[<span data-ttu-id="d91a6-133">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="d91a6-133">ScDupPropset</span></span>](scduppropset.md)

