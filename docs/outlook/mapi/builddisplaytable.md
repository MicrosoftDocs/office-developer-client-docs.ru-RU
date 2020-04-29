---
title: BuildDisplayTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- BuildDisplayTable
api_type:
- HeaderDef
ms.assetid: 0846415b-6fe1-4504-8620-108af6719015
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8c5e6078be05ff846b7737ff53e9a6338fcb2141
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431598"
---
# <a name="builddisplaytable"></a><span data-ttu-id="9088d-103">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="9088d-103">BuildDisplayTable</span></span>

  
  
<span data-ttu-id="9088d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9088d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9088d-105">Создает таблицу отображения из данных страницы свойств, которые хранятся в одной или нескольких структурах [дтпаже](dtpage.md) .</span><span class="sxs-lookup"><span data-stu-id="9088d-105">Creates a display table from the property page data contained in one or more [DTPAGE](dtpage.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9088d-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="9088d-106">Header file:</span></span>  <br/> |<span data-ttu-id="9088d-107">Мапиутил. h</span><span class="sxs-lookup"><span data-stu-id="9088d-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="9088d-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="9088d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="9088d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="9088d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="9088d-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="9088d-110">Called by:</span></span>  <br/> |<span data-ttu-id="9088d-111">Поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="9088d-111">Service providers</span></span>  <br/> |
   
```cpp
STDAPI BuildDisplayTable(
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  LPMALLOC lpMalloc,
  HINSTANCE hInstance,
  UINT cPages,
  LPDTPAGE lpPage,
  ULONG ulFlags,
  LPMAPITABLE * lppTable,
  LPTABLEDATA * lppTblData
);
```

## <a name="parameters"></a><span data-ttu-id="9088d-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="9088d-112">Parameters</span></span>

 <span data-ttu-id="9088d-113">_лпаллокатебуффер_</span><span class="sxs-lookup"><span data-stu-id="9088d-113">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="9088d-114">возврата Указатель на функцию [мапиаллокатебуффер](mapiallocatebuffer.md) , которая будет использоваться для выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="9088d-114">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="9088d-115">_лпаллокатеморе_</span><span class="sxs-lookup"><span data-stu-id="9088d-115">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="9088d-116">возврата Указатель на функцию [мапиаллокатеморе](mapiallocatemore.md) , которая будет использоваться для выделения дополнительной памяти.</span><span class="sxs-lookup"><span data-stu-id="9088d-116">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="9088d-117">_лпфрибуффер_</span><span class="sxs-lookup"><span data-stu-id="9088d-117">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="9088d-118">возврата Указатель на функцию [мапифрибуффер](mapifreebuffer.md) , который будет использоваться для освобождения памяти.</span><span class="sxs-lookup"><span data-stu-id="9088d-118">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="9088d-119">_лпмаллок_</span><span class="sxs-lookup"><span data-stu-id="9088d-119">_lpMalloc_</span></span>
  
> <span data-ttu-id="9088d-120">Неиспользуемых должно быть задано значение NULL.</span><span class="sxs-lookup"><span data-stu-id="9088d-120">Unused; should be set to NULL.</span></span> 
    
 <span data-ttu-id="9088d-121">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="9088d-121">_hInstance_</span></span>
  
> <span data-ttu-id="9088d-122">возврата Экземпляр объекта MAPI, из которого **буилддисплайтабле** получает ресурсы.</span><span class="sxs-lookup"><span data-stu-id="9088d-122">[in] An instance of a MAPI object from which **BuildDisplayTable** retrieves resources.</span></span> 
    
 <span data-ttu-id="9088d-123">_кпажес_</span><span class="sxs-lookup"><span data-stu-id="9088d-123">_cPages_</span></span>
  
> <span data-ttu-id="9088d-124">возврата Количество структур [дтпаже](dtpage.md) в массиве, на которые указывает параметр _лппаже_ .</span><span class="sxs-lookup"><span data-stu-id="9088d-124">[in] Count of [DTPAGE](dtpage.md) structures in the array pointed to by the  _lpPage_ parameter.</span></span> 
    
 <span data-ttu-id="9088d-125">_лппаже_</span><span class="sxs-lookup"><span data-stu-id="9088d-125">_lpPage_</span></span>
  
> <span data-ttu-id="9088d-126">возврата Указатель на массив структур **дтпаже** , содержащих сведения о создаваемых страницах таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="9088d-126">[in] Pointer to an array of **DTPAGE** structures that contain information about the display table pages to be built.</span></span> 
    
 <span data-ttu-id="9088d-127">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9088d-127">_ulFlags_</span></span>
  
> <span data-ttu-id="9088d-128">возврата Битовая маска флагов.</span><span class="sxs-lookup"><span data-stu-id="9088d-128">[in] Bitmask of flags.</span></span> <span data-ttu-id="9088d-129">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="9088d-129">The following flag can be set:</span></span>
    
<span data-ttu-id="9088d-130">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9088d-130">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="9088d-131">Переданные строки имеют формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="9088d-131">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="9088d-132">Если флаг MAPI_UNICODE не установлен, строки представлены в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="9088d-132">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="9088d-133">_лпптабле_</span><span class="sxs-lookup"><span data-stu-id="9088d-133">_lppTable_</span></span>
  
> <span data-ttu-id="9088d-134">вышли Указатель на указатель на таблицу отображения, которая предоставляет интерфейс [IMAPITable](imapitableiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="9088d-134">[out] Pointer to a pointer to the display table, which exposes the [IMAPITable](imapitableiunknown.md) interface.</span></span> 
    
 <span data-ttu-id="9088d-135">_лпптблдата_</span><span class="sxs-lookup"><span data-stu-id="9088d-135">_lppTblData_</span></span>
  
> <span data-ttu-id="9088d-136">[вход, выход] Указатель на указатель на табличный объект данных, который предоставляет интерфейс [итабледата](itabledataiunknown.md) для таблицы, возвращаемой параметром _лпптабле_ .</span><span class="sxs-lookup"><span data-stu-id="9088d-136">[in, out] Pointer to a pointer to a table data object exposing the [ITableData](itabledataiunknown.md) interface on the table returned in the  _lppTable_ parameter.</span></span> <span data-ttu-id="9088d-137">Если объект Data Table не нужен, для параметра _лпптблдата_ следует задать значение null, а не значение указателя.</span><span class="sxs-lookup"><span data-stu-id="9088d-137">If no table data object is desired,  _lppTblData_ should be set to NULL instead of a pointer value.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9088d-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9088d-138">Return value</span></span>

<span data-ttu-id="9088d-139">Нет</span><span class="sxs-lookup"><span data-stu-id="9088d-139">None</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9088d-140">Примечания</span><span class="sxs-lookup"><span data-stu-id="9088d-140">Remarks</span></span>

<span data-ttu-id="9088d-141">MAPI использует функции, на которые указывает _лпаллокатебуффер_, _лпаллокатеморе_и _лпфрибуффер_ для большей части памяти и освобождений, в частности, для выделения памяти, используемой клиентскими приложениями при вызове интерфейсов объектов, таких как [IMAPIProp::](imapiprop-getprops.md) и [IMAPITable:: QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="9088d-141">MAPI uses the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation, in particular to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9088d-142">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="9088d-142">Notes to callers</span></span>

<span data-ttu-id="9088d-143">Все возможные варианты считываются из ресурса диалогового окна, в том числе:</span><span class="sxs-lookup"><span data-stu-id="9088d-143">Everything possible is read from the dialog resource, including:</span></span>
  
- <span data-ttu-id="9088d-144">Заголовок страницы, который является элементом _улблпсзлабел_ структуры [дтблпаже](dtblpage.md) , считанным из заголовка диалогового окна ресурса.</span><span class="sxs-lookup"><span data-stu-id="9088d-144">The page title that is, the  _ulbLpszLabel_ member of the [DTBLPAGE](dtblpage.md) structure read from the dialog title in the resource.</span></span> 
    
- <span data-ttu-id="9088d-145">Все заголовки элементов управления, являющиеся элементами _улблпсзлабел_ других структур управления, считанные из текста элемента управления в ресурсе.</span><span class="sxs-lookup"><span data-stu-id="9088d-145">All control titles that is, the  _ulbLpszLabel_ members of other control structures read from the control text in the resource.</span></span> 
    
 <span data-ttu-id="9088d-146">**Буилддисплайтабле** перезаписывает все данные, переданные в структуры элементов управления вводом, сведениями из ресурса диалога, что означает, что вызывающий абонент **буилддисплайтабле** не может динамически указывать заголовки страниц или элементов управления.</span><span class="sxs-lookup"><span data-stu-id="9088d-146">**BuildDisplayTable** overwrites anything passed in the input control structures with information from the dialog resource, which means the caller of **BuildDisplayTable** cannot dynamically specify page or control titles.</span></span> <span data-ttu-id="9088d-147">Звонящие, которым нужно сделать это, могут получить **буилддисплайтабле** , возвращая объект данных таблицы в _лпптабледата_ и изменяя строки в ней. Кроме того, они могут создавать таблицу отображения вручную в объекте данных таблицы.</span><span class="sxs-lookup"><span data-stu-id="9088d-147">Callers who need to do that can have **BuildDisplayTable** return the table data object in  _lppTableData_ and change rows in it; or they can build the display table by hand in a table data object instead.</span></span> 
  
<span data-ttu-id="9088d-148">Если для _лпптабледата_ не ЗАДАНО значение null, поставщик отвечает за освобождение объекта данных таблицы после его завершения с помощью таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="9088d-148">If  _lppTableData_ is not set to NULL, the provider is responsible for freeing the table data object when it is finished with the display table.</span></span> 
  

