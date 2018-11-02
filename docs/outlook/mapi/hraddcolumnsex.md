---
title: HrAddColumnsEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrAddColumnsEx
api_type:
- COM
ms.assetid: c0a65d2b-a9b8-4477-a1c7-18c8478126f6
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 566a9d23c46ec717eb5eed711fff801b15d49fc1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564236"
---
# <a name="hraddcolumnsex"></a><span data-ttu-id="748e7-103">HrAddColumnsEx</span><span class="sxs-lookup"><span data-stu-id="748e7-103">HrAddColumnsEx</span></span>

  
  
<span data-ttu-id="748e7-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="748e7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="748e7-105">Добавляет или перемещение столбцов в начало существующей таблицы.</span><span class="sxs-lookup"><span data-stu-id="748e7-105">Adds or moves columns to the beginning of an existing table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="748e7-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="748e7-106">Header file:</span></span>  <br/> |<span data-ttu-id="748e7-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="748e7-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="748e7-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="748e7-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="748e7-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="748e7-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="748e7-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="748e7-110">Called by:</span></span>  <br/> |<span data-ttu-id="748e7-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="748e7-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrAddColumnsEx(
  LPMAPITABLE lptbl,
  LPSPropTagArray lpproptagColumnsNew,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer,
  void (FAR * lpfnFilterColumns)(
  LPSPropTagArray ptaga)
);
```

## <a name="parameters"></a><span data-ttu-id="748e7-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="748e7-112">Parameters</span></span>

 <span data-ttu-id="748e7-113">_lptbl_</span><span class="sxs-lookup"><span data-stu-id="748e7-113">_lptbl_</span></span>
  
> <span data-ttu-id="748e7-114">[in] Указатель на влияет на таблицы MAPI.</span><span class="sxs-lookup"><span data-stu-id="748e7-114">[in] Pointer to the MAPI table affected.</span></span> 
    
 <span data-ttu-id="748e7-115">_lpproptagColumnsNew_</span><span class="sxs-lookup"><span data-stu-id="748e7-115">_lpproptagColumnsNew_</span></span>
  
> <span data-ttu-id="748e7-116">[in] Указатель на структуру [SPropTagArray](sproptagarray.md) , который содержит массив теги свойства для свойств для добавления или перемещения в начало таблицы.</span><span class="sxs-lookup"><span data-stu-id="748e7-116">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags for the properties to be added or moved to the beginning of the table.</span></span> 
    
 <span data-ttu-id="748e7-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="748e7-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="748e7-118">[in] Указатель на функцию [MAPIAllocateBuffer](mapiallocatebuffer.md) , которые будут использоваться для выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="748e7-118">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="748e7-119">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="748e7-119">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="748e7-120">[in] Указатель на функцию [MAPIFreeBuffer](mapifreebuffer.md) , которые будут использоваться для свободного использования памяти.</span><span class="sxs-lookup"><span data-stu-id="748e7-120">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="748e7-121">_lpfnFilterColumns_</span><span class="sxs-lookup"><span data-stu-id="748e7-121">_lpfnFilterColumns_</span></span>
  
> <span data-ttu-id="748e7-122">[in] Указатель на функцию обратного вызова, предоставляемого вызывающим абонентом.</span><span class="sxs-lookup"><span data-stu-id="748e7-122">[in] Pointer to a callback function furnished by the caller.</span></span> <span data-ttu-id="748e7-123">Если параметр _lpfnFilterColumns_ имеет значение NULL, обратный вызов не выполняется.</span><span class="sxs-lookup"><span data-stu-id="748e7-123">If the  _lpfnFilterColumns_ parameter is set to NULL, no callback is made.</span></span> 
    
 <span data-ttu-id="748e7-124">_ptaga_</span><span class="sxs-lookup"><span data-stu-id="748e7-124">_ptaga_</span></span>
  
> <span data-ttu-id="748e7-125">[in] Указатель на структуру [SPropTagArray](sproptagarray.md) , содержащий массив тегов свойств, уже существующих в таблице перед свойства при добавлении или перемещено в начале.</span><span class="sxs-lookup"><span data-stu-id="748e7-125">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains the array of property tags already existing in the table before properties are added or moved to the beginning.</span></span> <span data-ttu-id="748e7-126">**HrAddColumnsEx** передается указатель в качестве параметра функции обратного вызова, на который ссылается _lpfnFilterColumns_.</span><span class="sxs-lookup"><span data-stu-id="748e7-126">**HrAddColumnsEx** passes this pointer as the parameter to the callback function pointed to by  _lpfnFilterColumns_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="748e7-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="748e7-127">Return value</span></span>

<span data-ttu-id="748e7-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="748e7-128">S_OK</span></span> 
  
> <span data-ttu-id="748e7-129">Вызов завершился успешно и были перемещены или добавить указанных столбцов.</span><span class="sxs-lookup"><span data-stu-id="748e7-129">The call succeeded and the specified columns were moved or added.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="748e7-130">Примечания</span><span class="sxs-lookup"><span data-stu-id="748e7-130">Remarks</span></span>

<span data-ttu-id="748e7-131">Свойства, переданной в **HrAddColumnsEx** с помощью параметра _lpproptagColumnsNew_ становятся первого свойства, предоставляемые на последующий вызов метода [IMAPITable::QueryRows](imapitable-queryrows.md) .</span><span class="sxs-lookup"><span data-stu-id="748e7-131">The properties passed to **HrAddColumnsEx** using the  _lpproptagColumnsNew_ parameter become the first properties exposed on subsequent calls to the [IMAPITable::QueryRows](imapitable-queryrows.md) method.</span></span> <span data-ttu-id="748e7-132">Любые свойства ранее в таблице, которые не были указаны в параметре _lpproptagColumnsNew_ , предоставляемые после все свойства добавлены и перемещенные.</span><span class="sxs-lookup"><span data-stu-id="748e7-132">Any properties previously in the table that were not specified in the  _lpproptagColumnsNew_ parameter are exposed after all the added and moved properties.</span></span> 
  
<span data-ttu-id="748e7-133">Если при вызове **QueryRows** любого свойства таблицы не определены, они будут возвращены с типом свойства PT_NULL и идентификатор свойства PROP_ID_NULL.</span><span class="sxs-lookup"><span data-stu-id="748e7-133">If any table properties are undefined when **QueryRows** is called, they are returned with property type PT_NULL and property identifier PROP_ID_NULL.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="748e7-134">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="748e7-134">Notes to callers</span></span>

<span data-ttu-id="748e7-135">Функция **HrAddColumnsEx** позволяет вызывающему бесплатной функции обратного вызова для фильтрации столбцов, которые уже были в таблице, например для преобразования строк из тип свойства PT_UNICODE PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="748e7-135">The **HrAddColumnsEx** function allows the caller to furnish a callback function to filter the columns that were already in the table, for example to convert strings from property type PT_UNICODE to PT_STRING8.</span></span> <span data-ttu-id="748e7-136">**HrAddColumnsEx** передает указатель ранее существующего столбца задайте в качестве параметра функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="748e7-136">**HrAddColumnsEx** passes a pointer to the previously existing column set as the parameter to the callback function.</span></span> <span data-ttu-id="748e7-137">Если функция обратного вызова можно изменить данные в массиве тега свойства, но нельзя добавлять новые теги.</span><span class="sxs-lookup"><span data-stu-id="748e7-137">The callback function can change data in the property tag array but cannot add new tags.</span></span> 
  
 <span data-ttu-id="748e7-138">Если один поставляется, а затем добавляет или перемещает указанных столбцов и наконец вызывает [IMAPITable::SetColumns](imapitable-setcolumns.md) **HrAddColumnsEx** сначала вызывается функция обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="748e7-138">**HrAddColumnsEx** first calls the callback function if one is furnished, then adds or moves the specified columns, and finally calls [IMAPITable::SetColumns](imapitable-setcolumns.md).</span></span> 
  
<span data-ttu-id="748e7-139">Входные параметры _lpAllocateBuffer_ и _lpFreeBuffer_ наведите указатель мыши функции [MAPIAllocateBuffer](mapiallocatebuffer.md) и [MAPIFreeBuffer](mapifreebuffer.md) соответственно.</span><span class="sxs-lookup"><span data-stu-id="748e7-139">The  _lpAllocateBuffer_ and  _lpFreeBuffer_ input parameters point to the [MAPIAllocateBuffer](mapiallocatebuffer.md) and [MAPIFreeBuffer](mapifreebuffer.md) functions, respectively.</span></span> <span data-ttu-id="748e7-140">Точные значения указатели, переданной в **HrAddColumnsEx** зависят от того, ли вызывающего клиентского приложения или поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="748e7-140">The exact values of the pointers passed to **HrAddColumnsEx** depend on whether the caller is a client application or a service provider.</span></span> <span data-ttu-id="748e7-141">Клиент передает указатели функции MAPI с указанными именами.</span><span class="sxs-lookup"><span data-stu-id="748e7-141">A client passes pointers to the MAPI functions with the specified names.</span></span> <span data-ttu-id="748e7-142">Поставщик службы передает указатели его полученным в его вызовы инициализации и извлечь путем вызова метода [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) .</span><span class="sxs-lookup"><span data-stu-id="748e7-142">A service provider passes the pointers it received in its initialization call or retrieved by calling the [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="748e7-143">См. также</span><span class="sxs-lookup"><span data-stu-id="748e7-143">See also</span></span>



[<span data-ttu-id="748e7-144">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="748e7-144">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)

