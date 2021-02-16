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
# <a name="builddisplaytable"></a><span data-ttu-id="6a835-103">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="6a835-103">BuildDisplayTable</span></span>

  
  
<span data-ttu-id="6a835-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6a835-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6a835-105">Создает таблицу отображения из данных страницы свойств, содержащихся в одной или более [структурах DTPAGE.](dtpage.md)</span><span class="sxs-lookup"><span data-stu-id="6a835-105">Creates a display table from the property page data contained in one or more [DTPAGE](dtpage.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6a835-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="6a835-106">Header file:</span></span>  <br/> |<span data-ttu-id="6a835-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="6a835-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="6a835-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="6a835-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6a835-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="6a835-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="6a835-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="6a835-110">Called by:</span></span>  <br/> |<span data-ttu-id="6a835-111">Поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="6a835-111">Service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="6a835-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="6a835-112">Parameters</span></span>

 <span data-ttu-id="6a835-113">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="6a835-113">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="6a835-114">[in] Указатель на [функцию MAPIAllocateBuffer,](mapiallocatebuffer.md) которая используется для выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="6a835-114">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="6a835-115">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="6a835-115">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="6a835-116">[in] Указатель на [функцию MAPIAllocateMore,](mapiallocatemore.md) которая используется для выделения дополнительной памяти.</span><span class="sxs-lookup"><span data-stu-id="6a835-116">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="6a835-117">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="6a835-117">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="6a835-118">[in] Указатель на [функцию MAPIFreeBuffer,](mapifreebuffer.md) которая используется для освободить память.</span><span class="sxs-lookup"><span data-stu-id="6a835-118">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="6a835-119">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="6a835-119">_lpMalloc_</span></span>
  
> <span data-ttu-id="6a835-120">Неиспользовано; должно быть установлено в NULL.</span><span class="sxs-lookup"><span data-stu-id="6a835-120">Unused; should be set to NULL.</span></span> 
    
 <span data-ttu-id="6a835-121">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="6a835-121">_hInstance_</span></span>
  
> <span data-ttu-id="6a835-122">[in] Экземпляр объекта MAPI, из которого **BuildDisplayTable** извлекает ресурсы.</span><span class="sxs-lookup"><span data-stu-id="6a835-122">[in] An instance of a MAPI object from which **BuildDisplayTable** retrieves resources.</span></span> 
    
 <span data-ttu-id="6a835-123">_cPages_</span><span class="sxs-lookup"><span data-stu-id="6a835-123">_cPages_</span></span>
  
> <span data-ttu-id="6a835-124">[in] Количество структур [DTPAGE](dtpage.md) в массиве, на который указывает параметр _lpPage._</span><span class="sxs-lookup"><span data-stu-id="6a835-124">[in] Count of [DTPAGE](dtpage.md) structures in the array pointed to by the  _lpPage_ parameter.</span></span> 
    
 <span data-ttu-id="6a835-125">_lpPage_</span><span class="sxs-lookup"><span data-stu-id="6a835-125">_lpPage_</span></span>
  
> <span data-ttu-id="6a835-126">[in] Указатель на массив структур **DTPAGE,** содержащих сведения о страницах таблиц отображения, которые необходимо построить.</span><span class="sxs-lookup"><span data-stu-id="6a835-126">[in] Pointer to an array of **DTPAGE** structures that contain information about the display table pages to be built.</span></span> 
    
 <span data-ttu-id="6a835-127">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6a835-127">_ulFlags_</span></span>
  
> <span data-ttu-id="6a835-128">[in] Битоваяmas флагов.</span><span class="sxs-lookup"><span data-stu-id="6a835-128">[in] Bitmask of flags.</span></span> <span data-ttu-id="6a835-129">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="6a835-129">The following flag can be set:</span></span>
    
<span data-ttu-id="6a835-130">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6a835-130">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="6a835-131">Переданные строки имеют формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="6a835-131">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="6a835-132">Если флаг MAPI_UNICODE не установлен, строки будут в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="6a835-132">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="6a835-133">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="6a835-133">_lppTable_</span></span>
  
> <span data-ttu-id="6a835-134">[out] Указатель на указатель на таблицу отображения, которая предоставляет [интерфейс IMAPITable.](imapitableiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="6a835-134">[out] Pointer to a pointer to the display table, which exposes the [IMAPITable](imapitableiunknown.md) interface.</span></span> 
    
 <span data-ttu-id="6a835-135">_lppTblData_</span><span class="sxs-lookup"><span data-stu-id="6a835-135">_lppTblData_</span></span>
  
> <span data-ttu-id="6a835-136">[in, out] Указатель на указатель на объект данных таблицы, который является интерфейсом [ITableData](itabledataiunknown.md) в таблице, возвращаемой в _параметре lppTable._</span><span class="sxs-lookup"><span data-stu-id="6a835-136">[in, out] Pointer to a pointer to a table data object exposing the [ITableData](itabledataiunknown.md) interface on the table returned in the  _lppTable_ parameter.</span></span> <span data-ttu-id="6a835-137">Если объект данных таблицы не требуется, следует установить  _для lppTblData_ значение NULL вместо значения указателя.</span><span class="sxs-lookup"><span data-stu-id="6a835-137">If no table data object is desired,  _lppTblData_ should be set to NULL instead of a pointer value.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6a835-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6a835-138">Return value</span></span>

<span data-ttu-id="6a835-139">Нет</span><span class="sxs-lookup"><span data-stu-id="6a835-139">None</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6a835-140">Примечания</span><span class="sxs-lookup"><span data-stu-id="6a835-140">Remarks</span></span>

<span data-ttu-id="6a835-141">MAPI использует функции, на которые указывают  _lpAllocateBuffer_,  _lpAllocateMore_ и  _lpFreeBuffer_ для выделения большей части памяти и распределения, в частности для выделения памяти для использования клиентских приложений при вызове интерфейсов объектов, таких как [IMAPIProp::GetProps](imapiprop-getprops.md) и [IMAPITable::QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="6a835-141">MAPI uses the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation, in particular to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="6a835-142">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="6a835-142">Notes to callers</span></span>

<span data-ttu-id="6a835-143">В ресурсе диалогового окна считыно все возможное, в том числе:</span><span class="sxs-lookup"><span data-stu-id="6a835-143">Everything possible is read from the dialog resource, including:</span></span>
  
- <span data-ttu-id="6a835-144">Заголовок страницы, т. е. член  _ulbLpszLabel_ структуры [DTBLPAGE,](dtblpage.md) считываемой из заголовка диалоговых окно в ресурсе.</span><span class="sxs-lookup"><span data-stu-id="6a835-144">The page title that is, the  _ulbLpszLabel_ member of the [DTBLPAGE](dtblpage.md) structure read from the dialog title in the resource.</span></span> 
    
- <span data-ttu-id="6a835-145">Все заголовки, то есть  _члены ulbLpszLabel_ других структур управления, считываемого из текста управления в ресурсе.</span><span class="sxs-lookup"><span data-stu-id="6a835-145">All control titles that is, the  _ulbLpszLabel_ members of other control structures read from the control text in the resource.</span></span> 
    
 <span data-ttu-id="6a835-146">**BuildDisplayTable** перезаписает все данные, переданные в структурах управления входными данными, с данными из ресурса диалоговых окной, что означает, что вызывающая стороны **BuildDisplayTable** не может динамически указывать заголовки страниц или управления.</span><span class="sxs-lookup"><span data-stu-id="6a835-146">**BuildDisplayTable** overwrites anything passed in the input control structures with information from the dialog resource, which means the caller of **BuildDisplayTable** cannot dynamically specify page or control titles.</span></span> <span data-ttu-id="6a835-147">Звонявшие, которым необходимо это сделать, могут **получить объект данных таблицы в**  _lppTableData_ и изменить строки в нем; или они могут создать отображаемую таблицу вручную в объекте данных таблицы.</span><span class="sxs-lookup"><span data-stu-id="6a835-147">Callers who need to do that can have **BuildDisplayTable** return the table data object in  _lppTableData_ and change rows in it; or they can build the display table by hand in a table data object instead.</span></span> 
  
<span data-ttu-id="6a835-148">Если  _для lppTableData_ не задано NULL, поставщик отвечает за то, чтобы освободить объект данных таблицы после его завершения с таблицей отображения.</span><span class="sxs-lookup"><span data-stu-id="6a835-148">If  _lppTableData_ is not set to NULL, the provider is responsible for freeing the table data object when it is finished with the display table.</span></span> 
  

