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
# <a name="screlocprops"></a><span data-ttu-id="2ff8f-103">ScRelocProps</span><span class="sxs-lookup"><span data-stu-id="2ff8f-103">ScRelocProps</span></span>

  
  
<span data-ttu-id="2ff8f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2ff8f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2ff8f-105">НаСтраивает указатели в массиве [спропвалуе](spropvalue.md) после того, как массив и его данные были скопированы или перемещены в новое расположение.</span><span class="sxs-lookup"><span data-stu-id="2ff8f-105">Adjusts the pointers in an [SPropValue](spropvalue.md) array after the array and its data have been copied or moved to a new location.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2ff8f-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="2ff8f-106">Header file:</span></span>  <br/> |<span data-ttu-id="2ff8f-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="2ff8f-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="2ff8f-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="2ff8f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="2ff8f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="2ff8f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="2ff8f-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="2ff8f-110">Called by:</span></span>  <br/> |<span data-ttu-id="2ff8f-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="2ff8f-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScRelocProps(
  int cprop,
  LPSPropValue rgprop,
  LPVOID pvBaseOld,
  LPVOID pvBaseNew,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="2ff8f-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="2ff8f-112">Parameters</span></span>

 <span data-ttu-id="2ff8f-113">_кпроп_</span><span class="sxs-lookup"><span data-stu-id="2ff8f-113">_cprop_</span></span>
  
> <span data-ttu-id="2ff8f-114">возврата Количество свойств в массиве, на которое указывает параметр _ргпроп_ .</span><span class="sxs-lookup"><span data-stu-id="2ff8f-114">[in] Count of properties in the array pointed to by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="2ff8f-115">_ргпроп_</span><span class="sxs-lookup"><span data-stu-id="2ff8f-115">_rgprop_</span></span>
  
> <span data-ttu-id="2ff8f-116">возврата Указатель на массив структур [спропвалуе](spropvalue.md) , для которых необходимо настроить указатели.</span><span class="sxs-lookup"><span data-stu-id="2ff8f-116">[in] Pointer to an array of [SPropValue](spropvalue.md) structures for which pointers are to be adjusted.</span></span> 
    
 <span data-ttu-id="2ff8f-117">_Пвбасеолд_</span><span class="sxs-lookup"><span data-stu-id="2ff8f-117">_pvBaseOld_</span></span>
  
> <span data-ttu-id="2ff8f-118">возврата Указатель на исходный базовый адрес массива, на который указывает параметр _ргпроп_ .</span><span class="sxs-lookup"><span data-stu-id="2ff8f-118">[in] Pointer to the original base address of the array pointed to by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="2ff8f-119">_Пвбасенев_</span><span class="sxs-lookup"><span data-stu-id="2ff8f-119">_pvBaseNew_</span></span>
  
> <span data-ttu-id="2ff8f-120">возврата Указатель на новый базовый адрес массива, на который указывает параметр _ргпроп_ .</span><span class="sxs-lookup"><span data-stu-id="2ff8f-120">[in] Pointer to the new base address of the array pointed to by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="2ff8f-121">_ПКБ_</span><span class="sxs-lookup"><span data-stu-id="2ff8f-121">_pcb_</span></span>
  
> <span data-ttu-id="2ff8f-122">[вход, выход] НеОбязательный указатель размера массива (в байтах), указанного параметром _пвбасенев_ .</span><span class="sxs-lookup"><span data-stu-id="2ff8f-122">[in, out] Optional pointer to the size, in bytes, of the array indicated by the  _pvBaseNew_ parameter.</span></span> <span data-ttu-id="2ff8f-123">Если значение не равно NULL, параметр _ПКБ_ имеет значение, равное числу байтов, хранящихся в параметре _ПВД_ .</span><span class="sxs-lookup"><span data-stu-id="2ff8f-123">If not NULL, the  _pcb_ parameter is set to the number of bytes stored in the  _pvD_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="2ff8f-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2ff8f-124">Return value</span></span>

<span data-ttu-id="2ff8f-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="2ff8f-125">S_OK</span></span>
  
> <span data-ttu-id="2ff8f-126">Указатели были успешно скорректированы.</span><span class="sxs-lookup"><span data-stu-id="2ff8f-126">Pointers were adjusted successfully.</span></span>
    
<span data-ttu-id="2ff8f-127">МАПИ_Е_ИНВАЛИД_ПАРАМЕТЕР</span><span class="sxs-lookup"><span data-stu-id="2ff8f-127">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="2ff8f-128">Один или оба параметра были недопустимы или обнаружен неизвестный тип свойства.</span><span class="sxs-lookup"><span data-stu-id="2ff8f-128">One or both parameters were invalid, or an unknown property type was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2ff8f-129">Примечания</span><span class="sxs-lookup"><span data-stu-id="2ff8f-129">Remarks</span></span>

<span data-ttu-id="2ff8f-130">Функция **скрелокпропс** работает в предположении, что массив значений свойств, для которого корректируются указатели, первоначально выделен в отдельном вызове, аналогичном вызову функции **сккопипропс** .</span><span class="sxs-lookup"><span data-stu-id="2ff8f-130">The **ScRelocProps** function operates on the assumption that the property value array for which pointers are adjusted was originally allocated in a single call similar to a call to the **ScCopyProps** function.</span></span> <span data-ttu-id="2ff8f-131">Если клиентское приложение или поставщик услуг работает со значением свойства, созданным из несвязных блоков памяти, следует использовать [сккопипропс](sccopyprops.md) для копирования свойств.</span><span class="sxs-lookup"><span data-stu-id="2ff8f-131">If a client application or service provider is working with a property value that is built from disjointed blocks of memory, it should use [ScCopyProps](sccopyprops.md) to copy properties instead.</span></span> 
  
 <span data-ttu-id="2ff8f-132">**Скрелокпропс** используется для поддержания допустимости указателей в массиве [спропвалуе](spropvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="2ff8f-132">**ScRelocProps** is used to maintain the validity of pointers in an [SPropValue](spropvalue.md) array.</span></span> <span data-ttu-id="2ff8f-133">Чтобы обеспечить допустимость указателей при записи такого массива на диск и считывание его с диска, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="2ff8f-133">To maintain pointers' validity when writing such an array to and reading it from a disk, perform the following operations:</span></span> 
  
1. <span data-ttu-id="2ff8f-134">Прежде чем записывать массив и данные на диск, вызовите **скрелокпропс** в массиве с параметром _пвбасенев_ , указывающим на некоторое стандартное значение ноль (например,).</span><span class="sxs-lookup"><span data-stu-id="2ff8f-134">Before writing the array and data to a disk, call **ScRelocProps** on the array with the  _pvBaseNew_ parameter pointing to some standard value zero, for instance.</span></span> 
    
2. <span data-ttu-id="2ff8f-135">После считывания массива и данных с диска вызовите **скрелокпропс** в массиве с параметром _пвбасеолд_ , равным тому же стандартному значению, что и на шаге 1.</span><span class="sxs-lookup"><span data-stu-id="2ff8f-135">After reading the array and data from a disk, call **ScRelocProps** on the array with the  _pvBaseOld_ parameter equal to the same standard value used in Step 1.</span></span> <span data-ttu-id="2ff8f-136">Массив и данные должны быть считаны в буфер, созданный с помощью одного выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="2ff8f-136">The array and data must be read into a buffer created with a single allocation.</span></span> 
    
3. <span data-ttu-id="2ff8f-137">Параметр _ПКБ_ для **скрелокпропс** является необязательным.</span><span class="sxs-lookup"><span data-stu-id="2ff8f-137">The  _pcb_ parameter to **ScRelocProps** is optional.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="2ff8f-138">См. также</span><span class="sxs-lookup"><span data-stu-id="2ff8f-138">See also</span></span>



[<span data-ttu-id="2ff8f-139">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="2ff8f-139">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="2ff8f-140">ScCountProps</span><span class="sxs-lookup"><span data-stu-id="2ff8f-140">ScCountProps</span></span>](sccountprops.md)
  
[<span data-ttu-id="2ff8f-141">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="2ff8f-141">ScDupPropset</span></span>](scduppropset.md)
  
[<span data-ttu-id="2ff8f-142">ScRelocNotifications</span><span class="sxs-lookup"><span data-stu-id="2ff8f-142">ScRelocNotifications</span></span>](screlocnotifications.md)

