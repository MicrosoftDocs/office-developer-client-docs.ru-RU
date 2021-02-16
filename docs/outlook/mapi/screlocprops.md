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
# <a name="screlocprops"></a><span data-ttu-id="27463-103">ScRelocProps</span><span class="sxs-lookup"><span data-stu-id="27463-103">ScRelocProps</span></span>

  
  
<span data-ttu-id="27463-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="27463-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="27463-105">Настраивает указатели в [массиве SPropValue](spropvalue.md) после копирования массива и его данных в новое расположение.</span><span class="sxs-lookup"><span data-stu-id="27463-105">Adjusts the pointers in an [SPropValue](spropvalue.md) array after the array and its data have been copied or moved to a new location.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="27463-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="27463-106">Header file:</span></span>  <br/> |<span data-ttu-id="27463-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="27463-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="27463-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="27463-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="27463-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="27463-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="27463-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="27463-110">Called by:</span></span>  <br/> |<span data-ttu-id="27463-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="27463-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScRelocProps(
  int cprop,
  LPSPropValue rgprop,
  LPVOID pvBaseOld,
  LPVOID pvBaseNew,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="27463-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="27463-112">Parameters</span></span>

 <span data-ttu-id="27463-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="27463-113">_cprop_</span></span>
  
> <span data-ttu-id="27463-114">[in] Количество свойств в массиве, на который указывает параметр _rgprop._</span><span class="sxs-lookup"><span data-stu-id="27463-114">[in] Count of properties in the array pointed to by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="27463-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="27463-115">_rgprop_</span></span>
  
> <span data-ttu-id="27463-116">[in] Указатель на массив структур [SPropValue,](spropvalue.md) для которых необходимо скорректировать указатели.</span><span class="sxs-lookup"><span data-stu-id="27463-116">[in] Pointer to an array of [SPropValue](spropvalue.md) structures for which pointers are to be adjusted.</span></span> 
    
 <span data-ttu-id="27463-117">_pvBaseOld_</span><span class="sxs-lookup"><span data-stu-id="27463-117">_pvBaseOld_</span></span>
  
> <span data-ttu-id="27463-118">[in] Указатель на исходный базовый адрес массива, на который указывает параметр _rgprop._</span><span class="sxs-lookup"><span data-stu-id="27463-118">[in] Pointer to the original base address of the array pointed to by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="27463-119">_pvBaseNew_</span><span class="sxs-lookup"><span data-stu-id="27463-119">_pvBaseNew_</span></span>
  
> <span data-ttu-id="27463-120">[in] Указатель на новый базовый адрес массива, на который указывает параметр _rgprop._</span><span class="sxs-lookup"><span data-stu-id="27463-120">[in] Pointer to the new base address of the array pointed to by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="27463-121">_pcb_</span><span class="sxs-lookup"><span data-stu-id="27463-121">_pcb_</span></span>
  
> <span data-ttu-id="27463-122">[in, out] Необязательный указатель на размер массива, указанный параметром  _pvBaseNew_ (в bytes).</span><span class="sxs-lookup"><span data-stu-id="27463-122">[in, out] Optional pointer to the size, in bytes, of the array indicated by the  _pvBaseNew_ parameter.</span></span> <span data-ttu-id="27463-123">Если это не NULL, для параметра _PCB_ устанавливается количество вбайт, хранимых в _параметре pvD._</span><span class="sxs-lookup"><span data-stu-id="27463-123">If not NULL, the  _pcb_ parameter is set to the number of bytes stored in the  _pvD_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="27463-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="27463-124">Return value</span></span>

<span data-ttu-id="27463-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="27463-125">S_OK</span></span>
  
> <span data-ttu-id="27463-126">Указатели были успешно настроены.</span><span class="sxs-lookup"><span data-stu-id="27463-126">Pointers were adjusted successfully.</span></span>
    
<span data-ttu-id="27463-127">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="27463-127">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="27463-128">Один или оба параметра были недопустимы или был задан неизвестный тип свойства.</span><span class="sxs-lookup"><span data-stu-id="27463-128">One or both parameters were invalid, or an unknown property type was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="27463-129">Примечания</span><span class="sxs-lookup"><span data-stu-id="27463-129">Remarks</span></span>

<span data-ttu-id="27463-130">Функция **ScRelocProps** работает при предположении, что массив значений свойств, для которого настраиваются указатели, изначально был выделен в одном вызове, аналогичном вызову функции **ScCopyProps.**</span><span class="sxs-lookup"><span data-stu-id="27463-130">The **ScRelocProps** function operates on the assumption that the property value array for which pointers are adjusted was originally allocated in a single call similar to a call to the **ScCopyProps** function.</span></span> <span data-ttu-id="27463-131">Если клиентские приложения или поставщик службы работают со значением свойства, которое построено из несоединенных блоков памяти, для копирования свойств следует использовать [ScCopyProps.](sccopyprops.md)</span><span class="sxs-lookup"><span data-stu-id="27463-131">If a client application or service provider is working with a property value that is built from disjointed blocks of memory, it should use [ScCopyProps](sccopyprops.md) to copy properties instead.</span></span> 
  
 <span data-ttu-id="27463-132">**ScRelocProps** используется для поддержания срока действия указателей в [массиве SPropValue.](spropvalue.md)</span><span class="sxs-lookup"><span data-stu-id="27463-132">**ScRelocProps** is used to maintain the validity of pointers in an [SPropValue](spropvalue.md) array.</span></span> <span data-ttu-id="27463-133">Для поддержания действительности указателей при записи такого массива в него и его чтении с диска выполните следующие операции:</span><span class="sxs-lookup"><span data-stu-id="27463-133">To maintain pointers' validity when writing such an array to and reading it from a disk, perform the following operations:</span></span> 
  
1. <span data-ttu-id="27463-134">Перед записью массива и данных на диск вызовите **ScRelocProps** в массиве с параметром  _pvBaseNew,_ указывав на некоторое стандартное нулевое значение, например.</span><span class="sxs-lookup"><span data-stu-id="27463-134">Before writing the array and data to a disk, call **ScRelocProps** on the array with the  _pvBaseNew_ parameter pointing to some standard value zero, for instance.</span></span> 
    
2. <span data-ttu-id="27463-135">После чтения массива и данных с диска вызовите **ScRelocProps** в массиве с параметром  _pvBaseOld,_ равным стандартному значению, используемом в шаге 1.</span><span class="sxs-lookup"><span data-stu-id="27463-135">After reading the array and data from a disk, call **ScRelocProps** on the array with the  _pvBaseOld_ parameter equal to the same standard value used in Step 1.</span></span> <span data-ttu-id="27463-136">Массив и данные необходимо считыть в буфер, созданный с одним выделением.</span><span class="sxs-lookup"><span data-stu-id="27463-136">The array and data must be read into a buffer created with a single allocation.</span></span> 
    
3. <span data-ttu-id="27463-137">Параметр  _pcb_ для **ScRelocProps является** необязательным.</span><span class="sxs-lookup"><span data-stu-id="27463-137">The  _pcb_ parameter to **ScRelocProps** is optional.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="27463-138">См. также</span><span class="sxs-lookup"><span data-stu-id="27463-138">See also</span></span>



[<span data-ttu-id="27463-139">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="27463-139">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="27463-140">ScCountProps</span><span class="sxs-lookup"><span data-stu-id="27463-140">ScCountProps</span></span>](sccountprops.md)
  
[<span data-ttu-id="27463-141">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="27463-141">ScDupPropset</span></span>](scduppropset.md)
  
[<span data-ttu-id="27463-142">ScRelocNotifications</span><span class="sxs-lookup"><span data-stu-id="27463-142">ScRelocNotifications</span></span>](screlocnotifications.md)

