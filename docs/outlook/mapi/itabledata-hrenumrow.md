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
ms.openlocfilehash: 140efe0b2d1b428a94b5bb2919d461779613932a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564684"
---
# <a name="itabledatahrenumrow"></a><span data-ttu-id="00e17-103">ITableData::HrEnumRow</span><span class="sxs-lookup"><span data-stu-id="00e17-103">ITableData::HrEnumRow</span></span>

  
  
<span data-ttu-id="00e17-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="00e17-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="00e17-105">Получает строку на основе его расположения в таблице.</span><span class="sxs-lookup"><span data-stu-id="00e17-105">Retrieves a row based on its position in the table.</span></span> 
  
```cpp
HRESULT HrEnumRow(
  ULONG ulRowNumber,
  LPSRow FAR * lppSRow
);
```

## <a name="parameters"></a><span data-ttu-id="00e17-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="00e17-106">Parameters</span></span>

 <span data-ttu-id="00e17-107">_ulRowNumber_</span><span class="sxs-lookup"><span data-stu-id="00e17-107">_ulRowNumber_</span></span>
  
> <span data-ttu-id="00e17-108">[in] Количество строк, для которого возвращаются свойства.</span><span class="sxs-lookup"><span data-stu-id="00e17-108">[in] The number of the row for which to return properties.</span></span> <span data-ttu-id="00e17-109">Значение параметра _ulRowNumber_ может быть любое значение от 0, что указывает на первую строку в таблице, через n - 1, которое указывает на последнюю строку в таблице.</span><span class="sxs-lookup"><span data-stu-id="00e17-109">The value in the  _ulRowNumber_ parameter can be any value from 0, which indicates the first row in the table, through n - 1, which indicates the last row in the table.</span></span> 
    
 <span data-ttu-id="00e17-110">_lppSRow_</span><span class="sxs-lookup"><span data-stu-id="00e17-110">_lppSRow_</span></span>
  
> <span data-ttu-id="00e17-111">[out] Указатель на указатель на структуру [SRow](srow.md) , описывающий строки целевое значение.</span><span class="sxs-lookup"><span data-stu-id="00e17-111">[out] A pointer to a pointer to an [SRow](srow.md) structure that describes the target row.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="00e17-112">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="00e17-112">Return value</span></span>

<span data-ttu-id="00e17-113">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="00e17-113">S_OK</span></span> 
  
> <span data-ttu-id="00e17-114">Был успешно извлечен строку или строки по максимальному числу строк, указанного с помощью параметра _ulRowNumber_ не существует.</span><span class="sxs-lookup"><span data-stu-id="00e17-114">The row was retrieved successfully, or a row for the row number specified by the  _ulRowNumber_ parameter does not exist.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="00e17-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="00e17-115">Remarks</span></span>

<span data-ttu-id="00e17-116">Метод **ITableData::HrEnumRow** извлекает строки на основании порядковый номер.</span><span class="sxs-lookup"><span data-stu-id="00e17-116">The **ITableData::HrEnumRow** method retrieves a row based on a sequential number.</span></span> <span data-ttu-id="00e17-117">Это значение указывает порядок вставки (0 указывает на первую строку и число строк минус 1 указывает последнюю строку).</span><span class="sxs-lookup"><span data-stu-id="00e17-117">This number represents the order of insertion (0 indicates the first row, and the number of rows minus 1 indicates the last row).</span></span> <span data-ttu-id="00e17-118">MAPI поддерживает этот порядке вставки строки в течение времени жизни объекта данных в таблице.</span><span class="sxs-lookup"><span data-stu-id="00e17-118">MAPI maintains this chronological order of row insertion for the lifetime of the table data object.</span></span> 
  
<span data-ttu-id="00e17-119">Если число указано в _ulRowNumber_ не соответствует строки в таблице, **HrEnumRow** возвращает значение S_OK и параметру _lppSRow_ присваивается значение NULL.</span><span class="sxs-lookup"><span data-stu-id="00e17-119">If the number specified in  _ulRowNumber_ does not correspond to a row in the table, **HrEnumRow** returns S_OK and sets the  _lppSRow_ parameter to NULL.</span></span> 
  
<span data-ttu-id="00e17-120">MAPI выделение памяти для возвращаемых **SRow** структуры с помощью функции [MAPIAllocateBuffer](mapiallocatebuffer.md) при создании объекта данных в таблице.</span><span class="sxs-lookup"><span data-stu-id="00e17-120">MAPI allocates memory for the returned **SRow** structure by using the [MAPIAllocateBuffer](mapiallocatebuffer.md) function when the table data object is created.</span></span> <span data-ttu-id="00e17-121">Вызывающий объект должен освободить память путем вызова функции [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="00e17-121">The caller must release this memory by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="00e17-122">Для извлечения строк из таблицы в том порядке, в том, что они были добавлены, пользователи объектов данных в таблице вызовите метод **HrEnumRow** .</span><span class="sxs-lookup"><span data-stu-id="00e17-122">To retrieve rows from a table in the order that they were inserted, table data object users call the **HrEnumRow** method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="00e17-123">См. также</span><span class="sxs-lookup"><span data-stu-id="00e17-123">See also</span></span>



[<span data-ttu-id="00e17-124">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="00e17-124">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="00e17-125">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="00e17-125">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="00e17-126">SRow</span><span class="sxs-lookup"><span data-stu-id="00e17-126">SRow</span></span>](srow.md)
  
[<span data-ttu-id="00e17-127">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="00e17-127">ITableData : IUnknown</span></span>](itabledataiunknown.md)

