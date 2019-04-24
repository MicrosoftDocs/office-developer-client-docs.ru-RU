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
ms.openlocfilehash: 9ca34fb2cce6e86c42e8e9525cd213f1008997d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348372"
---
# <a name="hraddcolumnsex"></a><span data-ttu-id="3aea0-103">HrAddColumnsEx</span><span class="sxs-lookup"><span data-stu-id="3aea0-103">HrAddColumnsEx</span></span>

  
  
<span data-ttu-id="3aea0-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3aea0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3aea0-105">Добавляет или перемещает столбцы в начало существующей таблицы.</span><span class="sxs-lookup"><span data-stu-id="3aea0-105">Adds or moves columns to the beginning of an existing table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3aea0-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="3aea0-106">Header file:</span></span>  <br/> |<span data-ttu-id="3aea0-107">Мапиутил. h</span><span class="sxs-lookup"><span data-stu-id="3aea0-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="3aea0-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="3aea0-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="3aea0-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="3aea0-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="3aea0-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="3aea0-110">Called by:</span></span>  <br/> |<span data-ttu-id="3aea0-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="3aea0-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="3aea0-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="3aea0-112">Parameters</span></span>

 <span data-ttu-id="3aea0-113">_лптбл_</span><span class="sxs-lookup"><span data-stu-id="3aea0-113">_lptbl_</span></span>
  
> <span data-ttu-id="3aea0-114">возврата Указатель на таблицу MAPI, на которую вы затронули.</span><span class="sxs-lookup"><span data-stu-id="3aea0-114">[in] Pointer to the MAPI table affected.</span></span> 
    
 <span data-ttu-id="3aea0-115">_Лппроптагколумнснев_</span><span class="sxs-lookup"><span data-stu-id="3aea0-115">_lpproptagColumnsNew_</span></span>
  
> <span data-ttu-id="3aea0-116">возврата Указатель на структуру [спроптагаррай](sproptagarray.md) , которая содержит массив тегов свойств для добавления или перемещения свойств в начало таблицы.</span><span class="sxs-lookup"><span data-stu-id="3aea0-116">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags for the properties to be added or moved to the beginning of the table.</span></span> 
    
 <span data-ttu-id="3aea0-117">_Лпаллокатебуффер_</span><span class="sxs-lookup"><span data-stu-id="3aea0-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="3aea0-118">возврата Указатель на функцию [мапиаллокатебуффер](mapiallocatebuffer.md) , которая будет использоваться для выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="3aea0-118">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="3aea0-119">_Лпфрибуффер_</span><span class="sxs-lookup"><span data-stu-id="3aea0-119">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="3aea0-120">возврата Указатель на функцию [мапифрибуффер](mapifreebuffer.md) , который будет использоваться для освобождения памяти.</span><span class="sxs-lookup"><span data-stu-id="3aea0-120">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="3aea0-121">_Лпфнфилтерколумнс_</span><span class="sxs-lookup"><span data-stu-id="3aea0-121">_lpfnFilterColumns_</span></span>
  
> <span data-ttu-id="3aea0-122">возврата Указатель на функцию обратного вызова, предоставляемую вызывающим абонентом.</span><span class="sxs-lookup"><span data-stu-id="3aea0-122">[in] Pointer to a callback function furnished by the caller.</span></span> <span data-ttu-id="3aea0-123">Если для параметра _лпфнфилтерколумнс_ ЗАДАНО значение null, обратный вызов не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3aea0-123">If the  _lpfnFilterColumns_ parameter is set to NULL, no callback is made.</span></span> 
    
 <span data-ttu-id="3aea0-124">_птага_</span><span class="sxs-lookup"><span data-stu-id="3aea0-124">_ptaga_</span></span>
  
> <span data-ttu-id="3aea0-125">возврата Указатель на структуру [спроптагаррай](sproptagarray.md) , которая содержит массив тегов свойств, уже существующих в таблице, перед добавлением или перемещением свойств в начало.</span><span class="sxs-lookup"><span data-stu-id="3aea0-125">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains the array of property tags already existing in the table before properties are added or moved to the beginning.</span></span> <span data-ttu-id="3aea0-126">**Храддколумнсекс** передает этот указатель в качестве параметра функции обратного вызова, на который указывает _лпфнфилтерколумнс_.</span><span class="sxs-lookup"><span data-stu-id="3aea0-126">**HrAddColumnsEx** passes this pointer as the parameter to the callback function pointed to by  _lpfnFilterColumns_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3aea0-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3aea0-127">Return value</span></span>

<span data-ttu-id="3aea0-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="3aea0-128">S_OK</span></span> 
  
> <span data-ttu-id="3aea0-129">Вызов выполнен успешно, и указанные столбцы были перемещены или добавлены.</span><span class="sxs-lookup"><span data-stu-id="3aea0-129">The call succeeded and the specified columns were moved or added.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3aea0-130">Примечания</span><span class="sxs-lookup"><span data-stu-id="3aea0-130">Remarks</span></span>

<span data-ttu-id="3aea0-131">Свойства, переданные в **храддколумнсекс** с помощью параметра _лппроптагколумнснев_ , становятся первыми свойствами, предоставленными при последующих вызовах метода [IMAPITable:: QueryRows](imapitable-queryrows.md) .</span><span class="sxs-lookup"><span data-stu-id="3aea0-131">The properties passed to **HrAddColumnsEx** using the  _lpproptagColumnsNew_ parameter become the first properties exposed on subsequent calls to the [IMAPITable::QueryRows](imapitable-queryrows.md) method.</span></span> <span data-ttu-id="3aea0-132">Все свойства, ранее добавленные в таблицу, которые не были указаны в параметре _лппроптагколумнснев_ , предоставляются после всех добавленных и перемещенных свойств.</span><span class="sxs-lookup"><span data-stu-id="3aea0-132">Any properties previously in the table that were not specified in the  _lpproptagColumnsNew_ parameter are exposed after all the added and moved properties.</span></span> 
  
<span data-ttu-id="3aea0-133">Если какие-либо свойства таблицы не определены при вызове **QueryRows** , они возвращаются с типом свойства пт_нулл и идентификатором свойства проп_ид_нулл.</span><span class="sxs-lookup"><span data-stu-id="3aea0-133">If any table properties are undefined when **QueryRows** is called, they are returned with property type PT_NULL and property identifier PROP_ID_NULL.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="3aea0-134">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="3aea0-134">Notes to callers</span></span>

<span data-ttu-id="3aea0-135">Функция **храддколумнсекс** позволяет вызывающему объекту использовать функцию обратного вызова для фильтрации столбцов, которые уже были в таблице, например для преобразования строк из типа свойства ПТ_УНИКОДЕ в PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="3aea0-135">The **HrAddColumnsEx** function allows the caller to furnish a callback function to filter the columns that were already in the table, for example to convert strings from property type PT_UNICODE to PT_STRING8.</span></span> <span data-ttu-id="3aea0-136">**Храддколумнсекс** передает указатель на ранее существующий набор столбцов в качестве параметра функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="3aea0-136">**HrAddColumnsEx** passes a pointer to the previously existing column set as the parameter to the callback function.</span></span> <span data-ttu-id="3aea0-137">Функция обратного вызова может изменять данные в массиве тегов свойств, но не может добавлять новые теги.</span><span class="sxs-lookup"><span data-stu-id="3aea0-137">The callback function can change data in the property tag array but cannot add new tags.</span></span> 
  
 <span data-ttu-id="3aea0-138">**Храддколумнсекс** сначала вызывает функцию обратного вызова, если она предоставлена, а затем добавляет или перемещает указанные столбцы, а затем вызывает метод [IMAPITable:: метода SetColumns](imapitable-setcolumns.md).</span><span class="sxs-lookup"><span data-stu-id="3aea0-138">**HrAddColumnsEx** first calls the callback function if one is furnished, then adds or moves the specified columns, and finally calls [IMAPITable::SetColumns](imapitable-setcolumns.md).</span></span> 
  
<span data-ttu-id="3aea0-139">Входные параметры _лпаллокатебуффер_ и _лпфрибуффер_ наследует точки для функций [мапиаллокатебуффер](mapiallocatebuffer.md) и [мапифрибуффер](mapifreebuffer.md) соответственно.</span><span class="sxs-lookup"><span data-stu-id="3aea0-139">The  _lpAllocateBuffer_ and  _lpFreeBuffer_ input parameters point to the [MAPIAllocateBuffer](mapiallocatebuffer.md) and [MAPIFreeBuffer](mapifreebuffer.md) functions, respectively.</span></span> <span data-ttu-id="3aea0-140">Точные значения указателей, передаваемых в **храддколумнсекс** , зависят от того, является ли вызывающий абонент клиентским приложением или поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="3aea0-140">The exact values of the pointers passed to **HrAddColumnsEx** depend on whether the caller is a client application or a service provider.</span></span> <span data-ttu-id="3aea0-141">Клиент передает указатели на функции MAPI с указанными именами.</span><span class="sxs-lookup"><span data-stu-id="3aea0-141">A client passes pointers to the MAPI functions with the specified names.</span></span> <span data-ttu-id="3aea0-142">Поставщик услуг передает указатели, полученные в результате инициализации, или извлекаются при вызове метода [имаписуппорт:: жетмемаллокраутинес](imapisupport-getmemallocroutines.md) .</span><span class="sxs-lookup"><span data-stu-id="3aea0-142">A service provider passes the pointers it received in its initialization call or retrieved by calling the [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3aea0-143">См. также</span><span class="sxs-lookup"><span data-stu-id="3aea0-143">See also</span></span>



[<span data-ttu-id="3aea0-144">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="3aea0-144">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)

