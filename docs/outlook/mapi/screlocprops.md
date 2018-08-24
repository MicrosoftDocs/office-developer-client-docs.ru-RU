---
title: ScRelocProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScRelocProps
api_type:
- COM
ms.assetid: 4aafb254-6074-4a7c-b915-d3d33304ac38
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 241fac608552036e4706956cbe79524aaedacec9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576850"
---
# <a name="screlocprops"></a><span data-ttu-id="c20c1-103">ScRelocProps</span><span class="sxs-lookup"><span data-stu-id="c20c1-103">ScRelocProps</span></span>

  
  
<span data-ttu-id="c20c1-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c20c1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c20c1-105">Регулировка указатели в массиве [SPropValue](spropvalue.md) после массива и его данные были скопированы или перемещены в новое расположение.</span><span class="sxs-lookup"><span data-stu-id="c20c1-105">Adjusts the pointers in an [SPropValue](spropvalue.md) array after the array and its data have been copied or moved to a new location.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c20c1-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="c20c1-106">Header file:</span></span>  <br/> |<span data-ttu-id="c20c1-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c20c1-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="c20c1-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="c20c1-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c20c1-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c20c1-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c20c1-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="c20c1-110">Called by:</span></span>  <br/> |<span data-ttu-id="c20c1-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="c20c1-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScRelocProps(
  int cprop,
  LPSPropValue rgprop,
  LPVOID pvBaseOld,
  LPVOID pvBaseNew,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="c20c1-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="c20c1-112">Parameters</span></span>

 <span data-ttu-id="c20c1-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="c20c1-113">_cprop_</span></span>
  
> <span data-ttu-id="c20c1-114">[in] Число свойств в массиве указывает параметр _rgprop_ .</span><span class="sxs-lookup"><span data-stu-id="c20c1-114">[in] Count of properties in the array pointed to by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="c20c1-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="c20c1-115">_rgprop_</span></span>
  
> <span data-ttu-id="c20c1-116">[in] Указатель на массив структур [SPropValue](spropvalue.md) , для которых должны быть настроены указатели.</span><span class="sxs-lookup"><span data-stu-id="c20c1-116">[in] Pointer to an array of [SPropValue](spropvalue.md) structures for which pointers are to be adjusted.</span></span> 
    
 <span data-ttu-id="c20c1-117">_pvBaseOld_</span><span class="sxs-lookup"><span data-stu-id="c20c1-117">_pvBaseOld_</span></span>
  
> <span data-ttu-id="c20c1-118">[in] Указатель на исходный базовый адрес массива, на который указывает параметр _rgprop_ .</span><span class="sxs-lookup"><span data-stu-id="c20c1-118">[in] Pointer to the original base address of the array pointed to by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="c20c1-119">_pvBaseNew_</span><span class="sxs-lookup"><span data-stu-id="c20c1-119">_pvBaseNew_</span></span>
  
> <span data-ttu-id="c20c1-120">[in] Указатель на новый базовый адрес массива, на который указывает параметр _rgprop_ .</span><span class="sxs-lookup"><span data-stu-id="c20c1-120">[in] Pointer to the new base address of the array pointed to by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="c20c1-121">_печатной_</span><span class="sxs-lookup"><span data-stu-id="c20c1-121">_pcb_</span></span>
  
> <span data-ttu-id="c20c1-122">[in, out] Необязательный указатель на размер, в байтах, массива, указанного в параметре _pvBaseNew_ .</span><span class="sxs-lookup"><span data-stu-id="c20c1-122">[in, out] Optional pointer to the size, in bytes, of the array indicated by the  _pvBaseNew_ parameter.</span></span> <span data-ttu-id="c20c1-123">Если это не имеет значение NULL, параметр _печатной_ число байтов, сохраненных в параметре _pvD_ .</span><span class="sxs-lookup"><span data-stu-id="c20c1-123">If not NULL, the  _pcb_ parameter is set to the number of bytes stored in the  _pvD_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c20c1-124">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="c20c1-124">Return value</span></span>

<span data-ttu-id="c20c1-125">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="c20c1-125">S_OK</span></span>
  
> <span data-ttu-id="c20c1-126">Указатели были настроены успешно.</span><span class="sxs-lookup"><span data-stu-id="c20c1-126">Pointers were adjusted successfully.</span></span>
    
<span data-ttu-id="c20c1-127">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c20c1-127">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="c20c1-128">Один или оба параметра были недопустимый или обнаружен неизвестный тип свойства.</span><span class="sxs-lookup"><span data-stu-id="c20c1-128">One or both parameters were invalid, or an unknown property type was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c20c1-129">Замечания</span><span class="sxs-lookup"><span data-stu-id="c20c1-129">Remarks</span></span>

<span data-ttu-id="c20c1-130">Функция **ScRelocProps** работает предполагается, что массива значение свойства, для которого настроены указатели сначала выделенная в один вызов следующего вызова функции **ScCopyProps** .</span><span class="sxs-lookup"><span data-stu-id="c20c1-130">The **ScRelocProps** function operates on the assumption that the property value array for which pointers are adjusted was originally allocated in a single call similar to a call to the **ScCopyProps** function.</span></span> <span data-ttu-id="c20c1-131">Если клиентское приложение или поставщик услуг работает со значением свойства, построенного из несвязанное блоки памяти, его следует использовать [ScCopyProps](sccopyprops.md) для копирования вместо этого свойства.</span><span class="sxs-lookup"><span data-stu-id="c20c1-131">If a client application or service provider is working with a property value that is built from disjointed blocks of memory, it should use [ScCopyProps](sccopyprops.md) to copy properties instead.</span></span> 
  
 <span data-ttu-id="c20c1-132">**ScRelocProps** позволяет сохранить целостность указатели в массиве [SPropValue](spropvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="c20c1-132">**ScRelocProps** is used to maintain the validity of pointers in an [SPropValue](spropvalue.md) array.</span></span> <span data-ttu-id="c20c1-133">Для обеспечения допустимости указатели при такой массив для записи и чтения с диска, выполните следующие операции:</span><span class="sxs-lookup"><span data-stu-id="c20c1-133">To maintain pointers' validity when writing such an array to and reading it from a disk, perform the following operations:</span></span> 
  
1. <span data-ttu-id="c20c1-134">Прежде чем записи массива и данных на диск, вызовите **ScRelocProps** массива с параметром _pvBaseNew_ , например с указанием некоторые стандартные нулевые значения.</span><span class="sxs-lookup"><span data-stu-id="c20c1-134">Before writing the array and data to a disk, call **ScRelocProps** on the array with the  _pvBaseNew_ parameter pointing to some standard value zero, for instance.</span></span> 
    
2. <span data-ttu-id="c20c1-135">После прочтения массива и данных с диска, вызовите **ScRelocProps** массива с помощью параметра _pvBaseOld_ равно значению же standard используется в шаге 1.</span><span class="sxs-lookup"><span data-stu-id="c20c1-135">After reading the array and data from a disk, call **ScRelocProps** on the array with the  _pvBaseOld_ parameter equal to the same standard value used in Step 1.</span></span> <span data-ttu-id="c20c1-136">Массив и данных необходимо прочитать в буфер, созданных с помощью за одну операцию.</span><span class="sxs-lookup"><span data-stu-id="c20c1-136">The array and data must be read into a buffer created with a single allocation.</span></span> 
    
3. <span data-ttu-id="c20c1-137">Это необязательный параметр _печатной_ для **ScRelocProps** .</span><span class="sxs-lookup"><span data-stu-id="c20c1-137">The  _pcb_ parameter to **ScRelocProps** is optional.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="c20c1-138">См. также</span><span class="sxs-lookup"><span data-stu-id="c20c1-138">See also</span></span>



[<span data-ttu-id="c20c1-139">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="c20c1-139">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="c20c1-140">ScCountProps</span><span class="sxs-lookup"><span data-stu-id="c20c1-140">ScCountProps</span></span>](sccountprops.md)
  
[<span data-ttu-id="c20c1-141">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="c20c1-141">ScDupPropset</span></span>](scduppropset.md)
  
[<span data-ttu-id="c20c1-142">ScRelocNotifications</span><span class="sxs-lookup"><span data-stu-id="c20c1-142">ScRelocNotifications</span></span>](screlocnotifications.md)

