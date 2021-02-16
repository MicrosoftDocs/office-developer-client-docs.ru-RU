---
title: ITableDataHrModifyRows
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrModifyRows
api_type:
- COM
ms.assetid: d295c896-9882-4d6f-9689-5cf40db208c0
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: d0074dd006fda6d44252011d0b979169e0c3d4cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405361"
---
# <a name="itabledatahrmodifyrows"></a><span data-ttu-id="6f339-103">ITableData::HrModifyRows</span><span class="sxs-lookup"><span data-stu-id="6f339-103">ITableData::HrModifyRows</span></span>

  
  
<span data-ttu-id="6f339-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6f339-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6f339-105">Вставляет несколько строк таблицы, возможно, заменяя существующие строки.</span><span class="sxs-lookup"><span data-stu-id="6f339-105">Inserts multiple table rows, possibly replacing existing rows.</span></span>
  
```cpp
HRESULT HrModifyRows(
  ULONG ulFlags,
  LPSRowSet lpSRowSet
);
```

## <a name="parameters"></a><span data-ttu-id="6f339-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6f339-106">Parameters</span></span>

 <span data-ttu-id="6f339-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6f339-107">_ulFlags_</span></span>
  
> <span data-ttu-id="6f339-108">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="6f339-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="6f339-109">_lpSRowSet_</span><span class="sxs-lookup"><span data-stu-id="6f339-109">_lpSRowSet_</span></span>
  
> <span data-ttu-id="6f339-110">[in] Указатель на структуру [SRowSet,](srowset.md) которая содержит набор добавляемой строки, заменяя при необходимости существующие строки.</span><span class="sxs-lookup"><span data-stu-id="6f339-110">[in] A pointer to an [SRowSet](srowset.md) structure that contains the set of rows to be added, replacing existing rows if necessary.</span></span> <span data-ttu-id="6f339-111">Одна из структур значений свойств, на которые указывает член **lpProps** каждой структуры [SRow](srow.md) в наборе строк, должна содержать столбец индекса, то же значение, которое было указано в параметре _ulPropTagIndexColumn_ при вызове функции [CreateTable.](createtable.md)</span><span class="sxs-lookup"><span data-stu-id="6f339-111">One of the property value structures pointed to by the **lpProps** member of each [SRow](srow.md) structure in the row set should contain the index column, the same value that was specified in the  _ulPropTagIndexColumn_ parameter in the call to the [CreateTable](createtable.md) function.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6f339-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6f339-112">Return value</span></span>

<span data-ttu-id="6f339-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="6f339-113">S_OK</span></span> 
  
> <span data-ttu-id="6f339-114">Строки успешно вставлены или изменены.</span><span class="sxs-lookup"><span data-stu-id="6f339-114">The rows were successfully inserted or modified.</span></span>
    
<span data-ttu-id="6f339-115">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6f339-115">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="6f339-116">Одна или несколько переданных строк не имеют столбца индекса.</span><span class="sxs-lookup"><span data-stu-id="6f339-116">One or more of the passed-in rows does not have an index column.</span></span> <span data-ttu-id="6f339-117">Если возвращается эта ошибка, строки не меняются.</span><span class="sxs-lookup"><span data-stu-id="6f339-117">If this error is returned, no rows are changed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6f339-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="6f339-118">Remarks</span></span>

<span data-ttu-id="6f339-119">Метод **ITableData::HrModifyRows** вставляет строки, описанные в структуре [SRowSet,](srowset.md) на которые указывает параметр _lpSRowSet._</span><span class="sxs-lookup"><span data-stu-id="6f339-119">The **ITableData::HrModifyRows** method inserts the rows described by the [SRowSet](srowset.md) structure pointed to by the  _lpSRowSet_ parameter.</span></span> <span data-ttu-id="6f339-120">Если значение столбца индекса строки в наборе строк соответствует значению существующей строки в таблице, существующая строка заменяется.</span><span class="sxs-lookup"><span data-stu-id="6f339-120">If the index column value of a row in the row set matches the value for an existing row in the table, the existing row is replaced.</span></span> <span data-ttu-id="6f339-121">Если строка, которая соответствует строке, включенной в структуру **SRowSet,** не существует, **HrModifyRows** добавляет строку в конец таблицы.</span><span class="sxs-lookup"><span data-stu-id="6f339-121">If no row exists that matches the one included in the **SRowSet** structure, **HrModifyRows** adds the row to the end of the table.</span></span> 
  
<span data-ttu-id="6f339-122">Все представления таблицы изменены, чтобы включить строки, на которые указывает _lpSRowSet._</span><span class="sxs-lookup"><span data-stu-id="6f339-122">All views of the table are modified to include the rows pointed to by  _lpSRowSet_.</span></span> <span data-ttu-id="6f339-123">Однако если представление имеет ограничение, исключа которое исключает строку, оно может быть не видно пользователю.</span><span class="sxs-lookup"><span data-stu-id="6f339-123">However, if a view has a restriction in place that excludes a row, it may not be visible to the user.</span></span> 
  
<span data-ttu-id="6f339-124">Столбцы в строках, на которые указывает  _lpSRowSet,_ не должны быть в том же порядке, что и столбцы в таблице.</span><span class="sxs-lookup"><span data-stu-id="6f339-124">The columns in the rows pointed to by  _lpSRowSet_ do not have to be in the same order as the columns in the table.</span></span> <span data-ttu-id="6f339-125">Вызываемая может также включать в качестве столбцов свойства, которые в настоящее время не находятся в таблице.</span><span class="sxs-lookup"><span data-stu-id="6f339-125">The caller can also include as columns properties that are not currently in the table.</span></span> <span data-ttu-id="6f339-126">Для существующих представлений **HrModifyRows делает** эти новые столбцы доступными, но не включает их в текущий набор столбцов.</span><span class="sxs-lookup"><span data-stu-id="6f339-126">For existing views, **HrModifyRows** makes these new columns available but does not include them in the current column set.</span></span> <span data-ttu-id="6f339-127">Для будущих **представлений HrModifyRows** включает новые столбцы в наборе столбцов.</span><span class="sxs-lookup"><span data-stu-id="6f339-127">For future views, **HrModifyRows** includes the new columns in the column set.</span></span> 
  
<span data-ttu-id="6f339-128">После того как **HrModifyRows** добавил строки, уведомления отправляются всем клиентам или поставщикам услуг, которые имеют представление таблицы и которые вызвали метод [IMAPITable::Advise](imapitable-advise.md) таблицы для регистрации уведомлений.</span><span class="sxs-lookup"><span data-stu-id="6f339-128">After **HrModifyRows** has added the rows, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> <span data-ttu-id="6f339-129">MAPI отправляет TABLE_ROW_ADDED или TABLE_ROW_MODIFIED уведомления для каждой строки до восьми строк.</span><span class="sxs-lookup"><span data-stu-id="6f339-129">MAPI sends TABLE_ROW_ADDED or TABLE_ROW_MODIFIED notifications for each row, up to eight rows.</span></span> <span data-ttu-id="6f339-130">Если вызов **HrModifyRows** затрагивает более восьми строк, MAPI отправляет TABLE_CHANGED уведомления.</span><span class="sxs-lookup"><span data-stu-id="6f339-130">If more than eight rows are affected by the **HrModifyRows** call, MAPI sends a single TABLE_CHANGED notification instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6f339-131">См. также</span><span class="sxs-lookup"><span data-stu-id="6f339-131">See also</span></span>



[<span data-ttu-id="6f339-132">SRowSet</span><span class="sxs-lookup"><span data-stu-id="6f339-132">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="6f339-133">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6f339-133">ITableData : IUnknown</span></span>](itabledataiunknown.md)

