---
title: ITableDataHrEnumRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrEnumRow
api_type:
- COM
ms.assetid: b25d9f2b-9454-4983-98f7-6a051a3b8a04
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 50fd96acd0989459c9887770ec5a3a236f182da5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418374"
---
# <a name="itabledatahrenumrow"></a><span data-ttu-id="6bed8-103">ITableData::HrEnumRow</span><span class="sxs-lookup"><span data-stu-id="6bed8-103">ITableData::HrEnumRow</span></span>

  
  
<span data-ttu-id="6bed8-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6bed8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6bed8-105">Извлекает строку в зависимости от ее положения в таблице.</span><span class="sxs-lookup"><span data-stu-id="6bed8-105">Retrieves a row based on its position in the table.</span></span> 
  
```cpp
HRESULT HrEnumRow(
  ULONG ulRowNumber,
  LPSRow FAR * lppSRow
);
```

## <a name="parameters"></a><span data-ttu-id="6bed8-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="6bed8-106">Parameters</span></span>

 <span data-ttu-id="6bed8-107">_ulRowNumber_</span><span class="sxs-lookup"><span data-stu-id="6bed8-107">_ulRowNumber_</span></span>
  
> <span data-ttu-id="6bed8-108">[in] Число строки, для которой нужно возвращать свойства.</span><span class="sxs-lookup"><span data-stu-id="6bed8-108">[in] The number of the row for which to return properties.</span></span> <span data-ttu-id="6bed8-109">Значение в параметре  _ulRowNumber_ может быть любым значением от 0, которое указывает первую строку в таблице, через n - 1, которое указывает последнюю строку в таблице.</span><span class="sxs-lookup"><span data-stu-id="6bed8-109">The value in the  _ulRowNumber_ parameter can be any value from 0, which indicates the first row in the table, through n - 1, which indicates the last row in the table.</span></span> 
    
 <span data-ttu-id="6bed8-110">_lppSRow_</span><span class="sxs-lookup"><span data-stu-id="6bed8-110">_lppSRow_</span></span>
  
> <span data-ttu-id="6bed8-111">[вышел] Указатель на указатель на структуру [SRow,](srow.md) которая описывает целевую строку.</span><span class="sxs-lookup"><span data-stu-id="6bed8-111">[out] A pointer to a pointer to an [SRow](srow.md) structure that describes the target row.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6bed8-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6bed8-112">Return value</span></span>

<span data-ttu-id="6bed8-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="6bed8-113">S_OK</span></span> 
  
> <span data-ttu-id="6bed8-114">Строка была успешно извлечена или строка для строки, указанной параметром  _ulRowNumber,_ не существует.</span><span class="sxs-lookup"><span data-stu-id="6bed8-114">The row was retrieved successfully, or a row for the row number specified by the  _ulRowNumber_ parameter does not exist.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="6bed8-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="6bed8-115">Remarks</span></span>

<span data-ttu-id="6bed8-116">Метод **ITableData::HrEnumRow** извлекает строку на основе последовательного номера.</span><span class="sxs-lookup"><span data-stu-id="6bed8-116">The **ITableData::HrEnumRow** method retrieves a row based on a sequential number.</span></span> <span data-ttu-id="6bed8-117">Это число представляет порядок вставки (0 указывает первую строку, а число строк минус 1 указывает последнюю строку).</span><span class="sxs-lookup"><span data-stu-id="6bed8-117">This number represents the order of insertion (0 indicates the first row, and the number of rows minus 1 indicates the last row).</span></span> <span data-ttu-id="6bed8-118">MAPI поддерживает этот хронологический порядок вставки строки для срока службы объекта данных таблицы.</span><span class="sxs-lookup"><span data-stu-id="6bed8-118">MAPI maintains this chronological order of row insertion for the lifetime of the table data object.</span></span> 
  
<span data-ttu-id="6bed8-119">Если число, указанное в  _ulRowNumber,_ не соответствует строке в таблице, **HrEnumRow** возвращает S_OK и задает параметр  _lppSRow_ NULL.</span><span class="sxs-lookup"><span data-stu-id="6bed8-119">If the number specified in  _ulRowNumber_ does not correspond to a row in the table, **HrEnumRow** returns S_OK and sets the  _lppSRow_ parameter to NULL.</span></span> 
  
<span data-ttu-id="6bed8-120">MAPI выделяет память для возвращаемой структуры **SRow** с помощью функции [MAPIAllocateBuffer](mapiallocatebuffer.md) при создания объекта данных таблицы.</span><span class="sxs-lookup"><span data-stu-id="6bed8-120">MAPI allocates memory for the returned **SRow** structure by using the [MAPIAllocateBuffer](mapiallocatebuffer.md) function when the table data object is created.</span></span> <span data-ttu-id="6bed8-121">Вызываемая должна освободить эту память, позвонив в [функцию MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="6bed8-121">The caller must release this memory by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="6bed8-122">Чтобы извлечь строки из таблицы в порядке их вставки, пользователи объектов данных таблицы называют **метод HrEnumRow.**</span><span class="sxs-lookup"><span data-stu-id="6bed8-122">To retrieve rows from a table in the order that they were inserted, table data object users call the **HrEnumRow** method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6bed8-123">См. также</span><span class="sxs-lookup"><span data-stu-id="6bed8-123">See also</span></span>



[<span data-ttu-id="6bed8-124">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="6bed8-124">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="6bed8-125">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="6bed8-125">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="6bed8-126">SRow</span><span class="sxs-lookup"><span data-stu-id="6bed8-126">SRow</span></span>](srow.md)
  
[<span data-ttu-id="6bed8-127">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6bed8-127">ITableData : IUnknown</span></span>](itabledataiunknown.md)

