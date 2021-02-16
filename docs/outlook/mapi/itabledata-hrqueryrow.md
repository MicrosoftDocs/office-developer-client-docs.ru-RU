---
title: ITableDataHrQueryRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrQueryRow
api_type:
- COM
ms.assetid: 66ce8f36-2b2b-4a8e-b9b2-43782d8357a1
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: da41fadc9a71a410dd115e28ce2cf9c81442b104
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434769"
---
# <a name="itabledatahrqueryrow"></a><span data-ttu-id="ed768-103">ITableData::HrQueryRow</span><span class="sxs-lookup"><span data-stu-id="ed768-103">ITableData::HrQueryRow</span></span>

  
  
<span data-ttu-id="ed768-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ed768-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ed768-105">Извлекает строку таблицы.</span><span class="sxs-lookup"><span data-stu-id="ed768-105">Retrieves a table row.</span></span>
  
```cpp
HRESULT HrQueryRow(
  LPSPropValue lpSPropValue,
  LPSRow FAR * lppSRow,
  ULONG FAR * lpuliRow
);
```

## <a name="parameters"></a><span data-ttu-id="ed768-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ed768-106">Parameters</span></span>

 <span data-ttu-id="ed768-107">_lpSPropValue_</span><span class="sxs-lookup"><span data-stu-id="ed768-107">_lpSPropValue_</span></span>
  
> <span data-ttu-id="ed768-108">[in] Указатель на структуру значения свойства, которая описывает столбец индекса для извлекаемой строки.</span><span class="sxs-lookup"><span data-stu-id="ed768-108">[in] A pointer to a property value structure that describes the index column for the row to be retrieved.</span></span> <span data-ttu-id="ed768-109">Член **ulPropTag** структуры значения свойства должен содержать тот же тег свойства, что и параметр _ulPropTagIndexColumn_ из вызова функции [CreateTable,](createtable.md) которая имеет доступ к реализации [ITableData.](itabledataiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="ed768-109">The **ulPropTag** member of the property value structure should contain the same property tag as the  _ulPropTagIndexColumn_ parameter from the call to the [CreateTable](createtable.md) function, which accesses the [ITableData](itabledataiunknown.md) implementation.</span></span> 
    
 <span data-ttu-id="ed768-110">_lppSRow_</span><span class="sxs-lookup"><span data-stu-id="ed768-110">_lppSRow_</span></span>
  
> <span data-ttu-id="ed768-111">[out] Указатель на указатель на извлеченную строку.</span><span class="sxs-lookup"><span data-stu-id="ed768-111">[out] A pointer to a pointer to the retrieved row.</span></span> 
    
 <span data-ttu-id="ed768-112">_lpuliRow_</span><span class="sxs-lookup"><span data-stu-id="ed768-112">_lpuliRow_</span></span>
  
> <span data-ttu-id="ed768-113">[in, out] При вводе допустимый указатель или NULL, который указывает, что не требуется возвращать сведения.</span><span class="sxs-lookup"><span data-stu-id="ed768-113">[in, out] On input, a valid pointer or NULL, which indicates that no information needs to be returned.</span></span> <span data-ttu-id="ed768-114">При выходе допустимый указатель, который указывает на номер строки строки, последовательное число, определяя положение строки в таблице.</span><span class="sxs-lookup"><span data-stu-id="ed768-114">On output, a valid pointer that points to the row's row number, a sequential number that identifies the row's position in the table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ed768-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ed768-115">Return value</span></span>

<span data-ttu-id="ed768-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="ed768-116">S_OK</span></span> 
  
> <span data-ttu-id="ed768-117">Строка успешно извлечена.</span><span class="sxs-lookup"><span data-stu-id="ed768-117">The row was successfully retrieved.</span></span>
    
<span data-ttu-id="ed768-118">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ed768-118">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="ed768-119">Структура [SPropValue,](spropvalue.md) на которую  _указывает lpSPropValue,_ не содержит свойство столбца индекса.</span><span class="sxs-lookup"><span data-stu-id="ed768-119">The [SPropValue](spropvalue.md) structure that  _lpSPropValue_ points to does not contain the index column property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ed768-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="ed768-120">Remarks</span></span>

<span data-ttu-id="ed768-121">Метод **ITableData::HrQueryRow** извлекает все свойства строки со столбцом индекса, который соответствует значению столбца индекса, включенного в структуру свойств, на которую указывает _lpSPropValue._</span><span class="sxs-lookup"><span data-stu-id="ed768-121">The **ITableData::HrQueryRow** method retrieves all of the properties for the row that has an index column that matches the value of the index column included in the property structure pointed to by  _lpSPropValue_.</span></span> <span data-ttu-id="ed768-122">**HrQueryRow** также возвращает номер строки, если вызываемая строка запрашивает его, что определяет положение строки в таблице.</span><span class="sxs-lookup"><span data-stu-id="ed768-122">**HrQueryRow** also returns the row number, if the caller requests it, that identifies the row's position in the table.</span></span> 
  
<span data-ttu-id="ed768-123">Так **как HrQueryRow** не изменять **структуру SPropValue,** на который указывает  _lpSPropValue,_ при возвращении **HrQueryRow** вызывателям необходимо освободить структуру.</span><span class="sxs-lookup"><span data-stu-id="ed768-123">Because **HrQueryRow** does not modify the **SPropValue** structure pointed to by  _lpSPropValue_, callers must free the structure when **HrQueryRow** returns.</span></span> <span data-ttu-id="ed768-124">Вызыватели также должны освободить **структуру SRow,** которая содержит извлеченную строку.</span><span class="sxs-lookup"><span data-stu-id="ed768-124">Callers must also free the **SRow** structure that contains the retrieved row.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ed768-125">См. также</span><span class="sxs-lookup"><span data-stu-id="ed768-125">See also</span></span>



[<span data-ttu-id="ed768-126">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="ed768-126">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="ed768-127">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="ed768-127">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="ed768-128">SPropValue</span><span class="sxs-lookup"><span data-stu-id="ed768-128">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="ed768-129">SRow</span><span class="sxs-lookup"><span data-stu-id="ed768-129">SRow</span></span>](srow.md)
  
[<span data-ttu-id="ed768-130">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ed768-130">ITableData : IUnknown</span></span>](itabledataiunknown.md)

