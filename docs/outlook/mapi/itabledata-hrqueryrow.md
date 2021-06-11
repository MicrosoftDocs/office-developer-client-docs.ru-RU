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
# <a name="itabledatahrqueryrow"></a><span data-ttu-id="532a9-103">ITableData::HrQueryRow</span><span class="sxs-lookup"><span data-stu-id="532a9-103">ITableData::HrQueryRow</span></span>

  
  
<span data-ttu-id="532a9-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="532a9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="532a9-105">Извлекает строку таблицы.</span><span class="sxs-lookup"><span data-stu-id="532a9-105">Retrieves a table row.</span></span>
  
```cpp
HRESULT HrQueryRow(
  LPSPropValue lpSPropValue,
  LPSRow FAR * lppSRow,
  ULONG FAR * lpuliRow
);
```

## <a name="parameters"></a><span data-ttu-id="532a9-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="532a9-106">Parameters</span></span>

 <span data-ttu-id="532a9-107">_lpSPropValue_</span><span class="sxs-lookup"><span data-stu-id="532a9-107">_lpSPropValue_</span></span>
  
> <span data-ttu-id="532a9-108">[in] Указатель на структуру значения свойства, которая описывает столбец индекса для строки, которая должна быть извлечена.</span><span class="sxs-lookup"><span data-stu-id="532a9-108">[in] A pointer to a property value structure that describes the index column for the row to be retrieved.</span></span> <span data-ttu-id="532a9-109">Член структуры значения свойства **ulPropTag** должен содержать тот же тег свойств, что и параметр _ulPropTagIndexColumn_ от вызова к функции [CreateTable,](createtable.md) которая имеет доступ к реализации [ITableData.](itabledataiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="532a9-109">The **ulPropTag** member of the property value structure should contain the same property tag as the  _ulPropTagIndexColumn_ parameter from the call to the [CreateTable](createtable.md) function, which accesses the [ITableData](itabledataiunknown.md) implementation.</span></span> 
    
 <span data-ttu-id="532a9-110">_lppSRow_</span><span class="sxs-lookup"><span data-stu-id="532a9-110">_lppSRow_</span></span>
  
> <span data-ttu-id="532a9-111">[вышел] Указатель на указатель на извлеченную строку.</span><span class="sxs-lookup"><span data-stu-id="532a9-111">[out] A pointer to a pointer to the retrieved row.</span></span> 
    
 <span data-ttu-id="532a9-112">_lpuliRow_</span><span class="sxs-lookup"><span data-stu-id="532a9-112">_lpuliRow_</span></span>
  
> <span data-ttu-id="532a9-113">[in, out] На входе допустимый указатель или NULL, который указывает, что никакой информации не требуется возвращать.</span><span class="sxs-lookup"><span data-stu-id="532a9-113">[in, out] On input, a valid pointer or NULL, which indicates that no information needs to be returned.</span></span> <span data-ttu-id="532a9-114">На выходе допустимый указатель, который указывает на номер строки строки, последовательное число, которое определяет положение строки в таблице.</span><span class="sxs-lookup"><span data-stu-id="532a9-114">On output, a valid pointer that points to the row's row number, a sequential number that identifies the row's position in the table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="532a9-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="532a9-115">Return value</span></span>

<span data-ttu-id="532a9-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="532a9-116">S_OK</span></span> 
  
> <span data-ttu-id="532a9-117">Строка была успешно извлечена.</span><span class="sxs-lookup"><span data-stu-id="532a9-117">The row was successfully retrieved.</span></span>
    
<span data-ttu-id="532a9-118">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="532a9-118">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="532a9-119">Структура [SPropValue,](spropvalue.md) на которую  _указывает lpSPropValue,_ не содержит свойства столбца индекса.</span><span class="sxs-lookup"><span data-stu-id="532a9-119">The [SPropValue](spropvalue.md) structure that  _lpSPropValue_ points to does not contain the index column property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="532a9-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="532a9-120">Remarks</span></span>

<span data-ttu-id="532a9-121">Метод **ITableData::HrQueryRow** извлекает все свойства для строки с столбцом индекса, который соответствует значению столбца индекса, включенного в структуру свойств, на которую указывает _lpSPropValue._</span><span class="sxs-lookup"><span data-stu-id="532a9-121">The **ITableData::HrQueryRow** method retrieves all of the properties for the row that has an index column that matches the value of the index column included in the property structure pointed to by  _lpSPropValue_.</span></span> <span data-ttu-id="532a9-122">**HrQueryRow** также возвращает номер строки, если вызываемая запрашивает его, что определяет положение строки в таблице.</span><span class="sxs-lookup"><span data-stu-id="532a9-122">**HrQueryRow** also returns the row number, if the caller requests it, that identifies the row's position in the table.</span></span> 
  
<span data-ttu-id="532a9-123">Так как **hrQueryRow** не изменит структуру **SPropValue,** на что указывает _lpSPropValue,_ звонители должны освободить структуру при возвращении **HrQueryRow.**</span><span class="sxs-lookup"><span data-stu-id="532a9-123">Because **HrQueryRow** does not modify the **SPropValue** structure pointed to by  _lpSPropValue_, callers must free the structure when **HrQueryRow** returns.</span></span> <span data-ttu-id="532a9-124">Вызыватели также должны освободить **структуру SRow,** которая содержит извлеченную строку.</span><span class="sxs-lookup"><span data-stu-id="532a9-124">Callers must also free the **SRow** structure that contains the retrieved row.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="532a9-125">См. также</span><span class="sxs-lookup"><span data-stu-id="532a9-125">See also</span></span>



[<span data-ttu-id="532a9-126">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="532a9-126">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="532a9-127">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="532a9-127">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="532a9-128">SPropValue</span><span class="sxs-lookup"><span data-stu-id="532a9-128">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="532a9-129">SRow</span><span class="sxs-lookup"><span data-stu-id="532a9-129">SRow</span></span>](srow.md)
  
[<span data-ttu-id="532a9-130">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="532a9-130">ITableData : IUnknown</span></span>](itabledataiunknown.md)

