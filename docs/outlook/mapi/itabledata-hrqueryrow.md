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
ms.openlocfilehash: ef0dc212a6a6f761cd8dd0cae5312c548c02ae50
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583822"
---
# <a name="itabledatahrqueryrow"></a><span data-ttu-id="8df76-103">ITableData::HrQueryRow</span><span class="sxs-lookup"><span data-stu-id="8df76-103">ITableData::HrQueryRow</span></span>

  
  
<span data-ttu-id="8df76-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8df76-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8df76-105">Получает строку таблицы.</span><span class="sxs-lookup"><span data-stu-id="8df76-105">Retrieves a table row.</span></span>
  
```cpp
HRESULT HrQueryRow(
  LPSPropValue lpSPropValue,
  LPSRow FAR * lppSRow,
  ULONG FAR * lpuliRow
);
```

## <a name="parameters"></a><span data-ttu-id="8df76-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8df76-106">Parameters</span></span>

 <span data-ttu-id="8df76-107">_lpSPropValue_</span><span class="sxs-lookup"><span data-stu-id="8df76-107">_lpSPropValue_</span></span>
  
> <span data-ttu-id="8df76-108">[in] Указатель на структуру значение свойства, с описанием столбца индекса для строки нужно вернуть.</span><span class="sxs-lookup"><span data-stu-id="8df76-108">[in] A pointer to a property value structure that describes the index column for the row to be retrieved.</span></span> <span data-ttu-id="8df76-109">Член **ulPropTag** структуры значение свойства должны содержать один и тот же свойство тег параметра- _ulPropTagIndexColumn_ вызов функции [CreateTable](createtable.md) , которая обращается к реализации [ITableData](itabledataiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="8df76-109">The **ulPropTag** member of the property value structure should contain the same property tag as the  _ulPropTagIndexColumn_ parameter from the call to the [CreateTable](createtable.md) function, which accesses the [ITableData](itabledataiunknown.md) implementation.</span></span> 
    
 <span data-ttu-id="8df76-110">_lppSRow_</span><span class="sxs-lookup"><span data-stu-id="8df76-110">_lppSRow_</span></span>
  
> <span data-ttu-id="8df76-111">[out] Указатель на указатель извлеченных строк.</span><span class="sxs-lookup"><span data-stu-id="8df76-111">[out] A pointer to a pointer to the retrieved row.</span></span> 
    
 <span data-ttu-id="8df76-112">_lpuliRow_</span><span class="sxs-lookup"><span data-stu-id="8df76-112">_lpuliRow_</span></span>
  
> <span data-ttu-id="8df76-113">[in, out] На ввод допустимый указатель или значение NULL, который означает необходимость сведения не должно быть возвращено.</span><span class="sxs-lookup"><span data-stu-id="8df76-113">[in, out] On input, a valid pointer or NULL, which indicates that no information needs to be returned.</span></span> <span data-ttu-id="8df76-114">Выходные данные, допустимый указатель, указывающий на номер строки строки, порядковый номер, идентифицирующий положение строки в таблице.</span><span class="sxs-lookup"><span data-stu-id="8df76-114">On output, a valid pointer that points to the row's row number, a sequential number that identifies the row's position in the table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8df76-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8df76-115">Return value</span></span>

<span data-ttu-id="8df76-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="8df76-116">S_OK</span></span> 
  
> <span data-ttu-id="8df76-117">Строка был успешно извлечен.</span><span class="sxs-lookup"><span data-stu-id="8df76-117">The row was successfully retrieved.</span></span>
    
<span data-ttu-id="8df76-118">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8df76-118">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="8df76-119">[SPropValue](spropvalue.md) структуры, указывающего _lpSPropValue_ не содержит свойство column индекса.</span><span class="sxs-lookup"><span data-stu-id="8df76-119">The [SPropValue](spropvalue.md) structure that  _lpSPropValue_ points to does not contain the index column property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="8df76-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="8df76-120">Remarks</span></span>

<span data-ttu-id="8df76-121">Метод **ITableData::HrQueryRow** получает все свойства для строки, которая имеет столбец индекса, который соответствует значению индекса столбца в структуре свойство, которое указывает _lpSPropValue_.</span><span class="sxs-lookup"><span data-stu-id="8df76-121">The **ITableData::HrQueryRow** method retrieves all of the properties for the row that has an index column that matches the value of the index column included in the property structure pointed to by  _lpSPropValue_.</span></span> <span data-ttu-id="8df76-122">**HrQueryRow** также возвращает номер строки, если вызывающий объект запрашивает его, указывающее положение строки в таблице.</span><span class="sxs-lookup"><span data-stu-id="8df76-122">**HrQueryRow** also returns the row number, if the caller requests it, that identifies the row's position in the table.</span></span> 
  
<span data-ttu-id="8df76-123">Так как **HrQueryRow** не изменяет структуру **SPropValue** , на который указывает _lpSPropValue_, вызывающие необходимо освободить структура при возврате **HrQueryRow** .</span><span class="sxs-lookup"><span data-stu-id="8df76-123">Because **HrQueryRow** does not modify the **SPropValue** structure pointed to by  _lpSPropValue_, callers must free the structure when **HrQueryRow** returns.</span></span> <span data-ttu-id="8df76-124">Вызывающие объекты также необходимо освободить **SRow** структуры, содержащей извлеченные строки.</span><span class="sxs-lookup"><span data-stu-id="8df76-124">Callers must also free the **SRow** structure that contains the retrieved row.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8df76-125">См. также</span><span class="sxs-lookup"><span data-stu-id="8df76-125">See also</span></span>



[<span data-ttu-id="8df76-126">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="8df76-126">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="8df76-127">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="8df76-127">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="8df76-128">SPropValue</span><span class="sxs-lookup"><span data-stu-id="8df76-128">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="8df76-129">SRow</span><span class="sxs-lookup"><span data-stu-id="8df76-129">SRow</span></span>](srow.md)
  
[<span data-ttu-id="8df76-130">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8df76-130">ITableData : IUnknown</span></span>](itabledataiunknown.md)

