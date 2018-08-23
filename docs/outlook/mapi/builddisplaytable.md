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
ms.openlocfilehash: 3b5268f0b033126083a463f72e47c64957df07eb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577690"
---
# <a name="builddisplaytable"></a><span data-ttu-id="63a3c-103">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="63a3c-103">BuildDisplayTable</span></span>

  
  
<span data-ttu-id="63a3c-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="63a3c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="63a3c-105">Создает таблицу, отображаемое на основе данных страницы свойств, содержащихся в одной или нескольких структур [DTPAGE](dtpage.md) .</span><span class="sxs-lookup"><span data-stu-id="63a3c-105">Creates a display table from the property page data contained in one or more [DTPAGE](dtpage.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="63a3c-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="63a3c-106">Header file:</span></span>  <br/> |<span data-ttu-id="63a3c-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="63a3c-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="63a3c-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="63a3c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="63a3c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="63a3c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="63a3c-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="63a3c-110">Called by:</span></span>  <br/> |<span data-ttu-id="63a3c-111">Поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="63a3c-111">Service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="63a3c-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="63a3c-112">Parameters</span></span>

 <span data-ttu-id="63a3c-113">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="63a3c-113">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="63a3c-114">[in] Указатель на функцию [MAPIAllocateBuffer](mapiallocatebuffer.md) , которые будут использоваться для выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="63a3c-114">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="63a3c-115">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="63a3c-115">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="63a3c-116">[in] Указатель на функцию [MAPIAllocateMore](mapiallocatemore.md) , которые будут использоваться для выделения дополнительной памяти.</span><span class="sxs-lookup"><span data-stu-id="63a3c-116">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="63a3c-117">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="63a3c-117">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="63a3c-118">[in] Указатель на функцию [MAPIFreeBuffer](mapifreebuffer.md) , которые будут использоваться для свободного использования памяти.</span><span class="sxs-lookup"><span data-stu-id="63a3c-118">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="63a3c-119">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="63a3c-119">_lpMalloc_</span></span>
  
> <span data-ttu-id="63a3c-120">Неиспользуемые; должен иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="63a3c-120">Unused; should be set to NULL.</span></span> 
    
 <span data-ttu-id="63a3c-121">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="63a3c-121">_hInstance_</span></span>
  
> <span data-ttu-id="63a3c-122">[in] Экземпляр объекта MAPI, из которого **BuildDisplayTable** извлекает ресурсы.</span><span class="sxs-lookup"><span data-stu-id="63a3c-122">[in] An instance of a MAPI object from which **BuildDisplayTable** retrieves resources.</span></span> 
    
 <span data-ttu-id="63a3c-123">_cPages_</span><span class="sxs-lookup"><span data-stu-id="63a3c-123">_cPages_</span></span>
  
> <span data-ttu-id="63a3c-124">[in] Число структур [DTPAGE](dtpage.md) в массиве указывает параметр _lpPage_ .</span><span class="sxs-lookup"><span data-stu-id="63a3c-124">[in] Count of [DTPAGE](dtpage.md) structures in the array pointed to by the  _lpPage_ parameter.</span></span> 
    
 <span data-ttu-id="63a3c-125">_lpPage_</span><span class="sxs-lookup"><span data-stu-id="63a3c-125">_lpPage_</span></span>
  
> <span data-ttu-id="63a3c-126">[in] Указатель на массив структур **DTPAGE** , которые содержат сведения о страницах в таблице отображения для построения.</span><span class="sxs-lookup"><span data-stu-id="63a3c-126">[in] Pointer to an array of **DTPAGE** structures that contain information about the display table pages to be built.</span></span> 
    
 <span data-ttu-id="63a3c-127">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="63a3c-127">_ulFlags_</span></span>
  
> <span data-ttu-id="63a3c-128">[in] Битовая маска флаги.</span><span class="sxs-lookup"><span data-stu-id="63a3c-128">[in] Bitmask of flags.</span></span> <span data-ttu-id="63a3c-129">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="63a3c-129">The following flag can be set:</span></span>
    
<span data-ttu-id="63a3c-130">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="63a3c-130">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="63a3c-131">Строки переданное хранятся в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="63a3c-131">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="63a3c-132">Если флаг MAPI_UNICODE не установлен, они в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="63a3c-132">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="63a3c-133">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="63a3c-133">_lppTable_</span></span>
  
> <span data-ttu-id="63a3c-134">[out] Указатель на указатель в таблице отображения, который предоставляет интерфейс [IMAPITable](imapitableiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="63a3c-134">[out] Pointer to a pointer to the display table, which exposes the [IMAPITable](imapitableiunknown.md) interface.</span></span> 
    
 <span data-ttu-id="63a3c-135">_lppTblData_</span><span class="sxs-lookup"><span data-stu-id="63a3c-135">_lppTblData_</span></span>
  
> <span data-ttu-id="63a3c-136">[in, out] Указатель на указатель на объект данных в таблице, предоставление интерфейс [ITableData](itabledataiunknown.md) в таблице, возвращаемой в параметре _lppTable_ .</span><span class="sxs-lookup"><span data-stu-id="63a3c-136">[in, out] Pointer to a pointer to a table data object exposing the [ITableData](itabledataiunknown.md) interface on the table returned in the  _lppTable_ parameter.</span></span> <span data-ttu-id="63a3c-137">В случае необходимости объект данных не в таблице _lppTblData_ должно быть присвоено значение NULL вместо значение указателя.</span><span class="sxs-lookup"><span data-stu-id="63a3c-137">If no table data object is desired,  _lppTblData_ should be set to NULL instead of a pointer value.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="63a3c-138">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="63a3c-138">Return value</span></span>

<span data-ttu-id="63a3c-139">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="63a3c-139">None</span></span>
  
## <a name="remarks"></a><span data-ttu-id="63a3c-140">Замечания</span><span class="sxs-lookup"><span data-stu-id="63a3c-140">Remarks</span></span>

<span data-ttu-id="63a3c-141">Функции, на который указывает _lpAllocateBuffer_, _lpAllocateMore_и _lpFreeBuffer_ для большинства выделение и освобождение памяти, в частности для выделения памяти для использования с клиентскими приложениями при вызове интерфейсы объектной использует MAPI Например, [IMAPIProp::GetProps](imapiprop-getprops.md) и [IMAPITable::QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="63a3c-141">MAPI uses the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation, in particular to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="63a3c-142">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="63a3c-142">Notes to callers</span></span>

<span data-ttu-id="63a3c-143">Все возможности считываются из диалогового окна ресурсов, включая:</span><span class="sxs-lookup"><span data-stu-id="63a3c-143">Everything possible is read from the dialog resource, including:</span></span>
  
- <span data-ttu-id="63a3c-144">Заголовок страницы, который является, член _ulbLpszLabel_ структуры [DTBLPAGE](dtblpage.md) чтение из заголовка диалогового окна в ресурсе.</span><span class="sxs-lookup"><span data-stu-id="63a3c-144">The page title that is, the  _ulbLpszLabel_ member of the [DTBLPAGE](dtblpage.md) structure read from the dialog title in the resource.</span></span> 
    
- <span data-ttu-id="63a3c-145">Все заголовки элемента управления, которым будет, _ulbLpszLabel_ члены других структур элементов управления, чтение из текста элемента управления в ресурсе.</span><span class="sxs-lookup"><span data-stu-id="63a3c-145">All control titles that is, the  _ulbLpszLabel_ members of other control structures read from the control text in the resource.</span></span> 
    
 <span data-ttu-id="63a3c-146">**BuildDisplayTable** перезаписывает что-либо переданную структур управления ввода со сведениями из ресурс диалогового окна, что означает, что Звонящий **BuildDisplayTable** нельзя задать динамически заголовков страницы или элемента управления.</span><span class="sxs-lookup"><span data-stu-id="63a3c-146">**BuildDisplayTable** overwrites anything passed in the input control structures with information from the dialog resource, which means the caller of **BuildDisplayTable** cannot dynamically specify page or control titles.</span></span> <span data-ttu-id="63a3c-147">Абоненты, которые необходимо сделать, у которых есть **BuildDisplayTable** возвращает объект данных в таблице в _lppTableData_ и измените строк в нем; или они вместо построения в таблице отображения вручную в объекте таблицы данных.</span><span class="sxs-lookup"><span data-stu-id="63a3c-147">Callers who need to do that can have **BuildDisplayTable** return the table data object in  _lppTableData_ and change rows in it; or they can build the display table by hand in a table data object instead.</span></span> 
  
<span data-ttu-id="63a3c-148">Если _lppTableData_ не задано значение NULL, поставщик несет ответственность за освобождение объект данных в таблице при завершении работы с таблицей отображения.</span><span class="sxs-lookup"><span data-stu-id="63a3c-148">If  _lppTableData_ is not set to NULL, the provider is responsible for freeing the table data object when it is finished with the display table.</span></span> 
  

