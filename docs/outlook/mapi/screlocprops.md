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
ms.openlocfilehash: c73fb96c9620a90ab0505b394fcb9853d02dcde5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421090"
---
# <a name="screlocprops"></a><span data-ttu-id="072db-103">ScRelocProps</span><span class="sxs-lookup"><span data-stu-id="072db-103">ScRelocProps</span></span>

  
  
<span data-ttu-id="072db-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="072db-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="072db-105">Корректирует указатели в [массиве SPropValue](spropvalue.md) после копирования массива и его данных в новом расположении.</span><span class="sxs-lookup"><span data-stu-id="072db-105">Adjusts the pointers in an [SPropValue](spropvalue.md) array after the array and its data have been copied or moved to a new location.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="072db-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="072db-106">Header file:</span></span>  <br/> |<span data-ttu-id="072db-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="072db-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="072db-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="072db-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="072db-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="072db-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="072db-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="072db-110">Called by:</span></span>  <br/> |<span data-ttu-id="072db-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="072db-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScRelocProps(
  int cprop,
  LPSPropValue rgprop,
  LPVOID pvBaseOld,
  LPVOID pvBaseNew,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="072db-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="072db-112">Parameters</span></span>

 <span data-ttu-id="072db-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="072db-113">_cprop_</span></span>
  
> <span data-ttu-id="072db-114">[in] Количество свойств в массиве, на который указывает параметр _rgprop._</span><span class="sxs-lookup"><span data-stu-id="072db-114">[in] Count of properties in the array pointed to by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="072db-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="072db-115">_rgprop_</span></span>
  
> <span data-ttu-id="072db-116">[in] Указатель на массив [структур SPropValue,](spropvalue.md) для которых необходимо корректировать указатели.</span><span class="sxs-lookup"><span data-stu-id="072db-116">[in] Pointer to an array of [SPropValue](spropvalue.md) structures for which pointers are to be adjusted.</span></span> 
    
 <span data-ttu-id="072db-117">_pvBaseOld_</span><span class="sxs-lookup"><span data-stu-id="072db-117">_pvBaseOld_</span></span>
  
> <span data-ttu-id="072db-118">[in] Указатель на исходный базовый адрес массива, на который указывает параметр _rgprop._</span><span class="sxs-lookup"><span data-stu-id="072db-118">[in] Pointer to the original base address of the array pointed to by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="072db-119">_pvBaseNew_</span><span class="sxs-lookup"><span data-stu-id="072db-119">_pvBaseNew_</span></span>
  
> <span data-ttu-id="072db-120">[in] Указатель на новый базовый адрес массива, на который указывает параметр _rgprop._</span><span class="sxs-lookup"><span data-stu-id="072db-120">[in] Pointer to the new base address of the array pointed to by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="072db-121">_pcb_</span><span class="sxs-lookup"><span data-stu-id="072db-121">_pcb_</span></span>
  
> <span data-ttu-id="072db-122">[in, out] Необязательный указатель на размер в bytes массива, указанный _параметром pvBaseNew._</span><span class="sxs-lookup"><span data-stu-id="072db-122">[in, out] Optional pointer to the size, in bytes, of the array indicated by the  _pvBaseNew_ parameter.</span></span> <span data-ttu-id="072db-123">Если не NULL, параметр _PCB_ задан для количества bytes, хранимого в _параметре pvD._</span><span class="sxs-lookup"><span data-stu-id="072db-123">If not NULL, the  _pcb_ parameter is set to the number of bytes stored in the  _pvD_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="072db-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="072db-124">Return value</span></span>

<span data-ttu-id="072db-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="072db-125">S_OK</span></span>
  
> <span data-ttu-id="072db-126">Указатели были успешно скорректированы.</span><span class="sxs-lookup"><span data-stu-id="072db-126">Pointers were adjusted successfully.</span></span>
    
<span data-ttu-id="072db-127">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="072db-127">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="072db-128">Один или оба параметра были недействительны, или был встречен неизвестный тип свойства.</span><span class="sxs-lookup"><span data-stu-id="072db-128">One or both parameters were invalid, or an unknown property type was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="072db-129">Примечания</span><span class="sxs-lookup"><span data-stu-id="072db-129">Remarks</span></span>

<span data-ttu-id="072db-130">Функция **ScRelocProps** работает на предположении, что массив значений свойств, для которого корректируются указатели, первоначально был выделен в одном вызове, аналогичном вызову функции **ScCopyProps.**</span><span class="sxs-lookup"><span data-stu-id="072db-130">The **ScRelocProps** function operates on the assumption that the property value array for which pointers are adjusted was originally allocated in a single call similar to a call to the **ScCopyProps** function.</span></span> <span data-ttu-id="072db-131">Если клиентские приложения или поставщик услуг работают со значением свойства, которое построено из разрощенных блоков памяти, для копирования свойств следует использовать [ScCopyProps.](sccopyprops.md)</span><span class="sxs-lookup"><span data-stu-id="072db-131">If a client application or service provider is working with a property value that is built from disjointed blocks of memory, it should use [ScCopyProps](sccopyprops.md) to copy properties instead.</span></span> 
  
 <span data-ttu-id="072db-132">**ScRelocProps** используется для поддержания действительности указателей в [массиве SPropValue.](spropvalue.md)</span><span class="sxs-lookup"><span data-stu-id="072db-132">**ScRelocProps** is used to maintain the validity of pointers in an [SPropValue](spropvalue.md) array.</span></span> <span data-ttu-id="072db-133">Чтобы сохранить достоверность указателей при записи такого массива на диск и его прочтения, выполните следующие операции:</span><span class="sxs-lookup"><span data-stu-id="072db-133">To maintain pointers' validity when writing such an array to and reading it from a disk, perform the following operations:</span></span> 
  
1. <span data-ttu-id="072db-134">Перед записью массива и данных на диск вызываем **scRelocProps** на массиве с параметром  _pvBaseNew,_ указыв, например, на некоторое стандартное значение ноль.</span><span class="sxs-lookup"><span data-stu-id="072db-134">Before writing the array and data to a disk, call **ScRelocProps** on the array with the  _pvBaseNew_ parameter pointing to some standard value zero, for instance.</span></span> 
    
2. <span data-ttu-id="072db-135">После прочтения массива и данных с диска вызываем **ScRelocProps** на массиве с параметром  _pvBaseOld,_ равным стандартному значению, используемом в шаге 1.</span><span class="sxs-lookup"><span data-stu-id="072db-135">After reading the array and data from a disk, call **ScRelocProps** on the array with the  _pvBaseOld_ parameter equal to the same standard value used in Step 1.</span></span> <span data-ttu-id="072db-136">Массив и данные необходимо считыть в буфер, созданный с одним выделением.</span><span class="sxs-lookup"><span data-stu-id="072db-136">The array and data must be read into a buffer created with a single allocation.</span></span> 
    
3. <span data-ttu-id="072db-137">Параметр  _pcb_ для **ScRelocProps** необязателен.</span><span class="sxs-lookup"><span data-stu-id="072db-137">The  _pcb_ parameter to **ScRelocProps** is optional.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="072db-138">См. также</span><span class="sxs-lookup"><span data-stu-id="072db-138">See also</span></span>



[<span data-ttu-id="072db-139">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="072db-139">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="072db-140">ScCountProps</span><span class="sxs-lookup"><span data-stu-id="072db-140">ScCountProps</span></span>](sccountprops.md)
  
[<span data-ttu-id="072db-141">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="072db-141">ScDupPropset</span></span>](scduppropset.md)
  
[<span data-ttu-id="072db-142">ScRelocNotifications</span><span class="sxs-lookup"><span data-stu-id="072db-142">ScRelocNotifications</span></span>](screlocnotifications.md)

