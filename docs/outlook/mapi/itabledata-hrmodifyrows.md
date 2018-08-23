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
ms.openlocfilehash: 06356d60b43d7e5be61d944c07001570bdd5c678
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571110"
---
# <a name="itabledatahrmodifyrows"></a><span data-ttu-id="ee60c-103">ITableData::HrModifyRows</span><span class="sxs-lookup"><span data-stu-id="ee60c-103">ITableData::HrModifyRows</span></span>

  
  
<span data-ttu-id="ee60c-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ee60c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ee60c-105">Вставка нескольких строк таблицы, возможно замена существующих строк.</span><span class="sxs-lookup"><span data-stu-id="ee60c-105">Inserts multiple table rows, possibly replacing existing rows.</span></span>
  
```cpp
HRESULT HrModifyRows(
  ULONG ulFlags,
  LPSRowSet lpSRowSet
);
```

## <a name="parameters"></a><span data-ttu-id="ee60c-106">���������</span><span class="sxs-lookup"><span data-stu-id="ee60c-106">Parameters</span></span>

 <span data-ttu-id="ee60c-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ee60c-107">_ulFlags_</span></span>
  
> <span data-ttu-id="ee60c-108">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="ee60c-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="ee60c-109">_lpSRowSet_</span><span class="sxs-lookup"><span data-stu-id="ee60c-109">_lpSRowSet_</span></span>
  
> <span data-ttu-id="ee60c-110">[in] Указатель на структуру [SRowSet](srowset.md) , которая содержит набор строк, добавлена, замена существующих строк, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="ee60c-110">[in] A pointer to an [SRowSet](srowset.md) structure that contains the set of rows to be added, replacing existing rows if necessary.</span></span> <span data-ttu-id="ee60c-111">Один из структур значение свойства, по **lpProps** членом каждого [SRow](srow.md) структуру в строку, на который указывает должен содержать столбце индекса такое же значение, которое было указано в параметре _ulPropTagIndexColumn_ в вызове [ CreateTable](createtable.md) функции.</span><span class="sxs-lookup"><span data-stu-id="ee60c-111">One of the property value structures pointed to by the **lpProps** member of each [SRow](srow.md) structure in the row set should contain the index column, the same value that was specified in the  _ulPropTagIndexColumn_ parameter in the call to the [CreateTable](createtable.md) function.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ee60c-112">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="ee60c-112">Return value</span></span>

<span data-ttu-id="ee60c-113">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="ee60c-113">S_OK</span></span> 
  
> <span data-ttu-id="ee60c-114">Строки были успешно добавлены или изменены.</span><span class="sxs-lookup"><span data-stu-id="ee60c-114">The rows were successfully inserted or modified.</span></span>
    
<span data-ttu-id="ee60c-115">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ee60c-115">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="ee60c-116">Один или несколько строк, переданное нет столбца индекса.</span><span class="sxs-lookup"><span data-stu-id="ee60c-116">One or more of the passed-in rows does not have an index column.</span></span> <span data-ttu-id="ee60c-117">Если этой ошибки строки не изменяются.</span><span class="sxs-lookup"><span data-stu-id="ee60c-117">If this error is returned, no rows are changed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ee60c-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="ee60c-118">Remarks</span></span>

<span data-ttu-id="ee60c-119">Метод **ITableData::HrModifyRows** вставляет строки, описанные в структуре [SRowSet](srowset.md) указывает параметр _lpSRowSet_ .</span><span class="sxs-lookup"><span data-stu-id="ee60c-119">The **ITableData::HrModifyRows** method inserts the rows described by the [SRowSet](srowset.md) structure pointed to by the  _lpSRowSet_ parameter.</span></span> <span data-ttu-id="ee60c-120">Если значение столбца индекс строки в наборе строк совпадает со значением для существующей строки в таблице, будет заменен существующей строки.</span><span class="sxs-lookup"><span data-stu-id="ee60c-120">If the index column value of a row in the row set matches the value for an existing row in the table, the existing row is replaced.</span></span> <span data-ttu-id="ee60c-121">Если нет строки, которая соответствует того, что включено в структуре **SRowSet** , **HrModifyRows** добавляет строку в конец таблицы.</span><span class="sxs-lookup"><span data-stu-id="ee60c-121">If no row exists that matches the one included in the **SRowSet** structure, **HrModifyRows** adds the row to the end of the table.</span></span> 
  
<span data-ttu-id="ee60c-122">Все представления таблицы изменяются, чтобы включить строки, на который указывает _lpSRowSet_.</span><span class="sxs-lookup"><span data-stu-id="ee60c-122">All views of the table are modified to include the rows pointed to by  _lpSRowSet_.</span></span> <span data-ttu-id="ee60c-123">Тем не менее если представление имеет ограничение на месте, которое не содержит строку, он может оказаться видимым для пользователя.</span><span class="sxs-lookup"><span data-stu-id="ee60c-123">However, if a view has a restriction in place that excludes a row, it may not be visible to the user.</span></span> 
  
<span data-ttu-id="ee60c-124">Столбцы в строках, на который указывает _lpSRowSet_ нет необходимости находиться в том же порядке в виде столбцов в таблице.</span><span class="sxs-lookup"><span data-stu-id="ee60c-124">The columns in the rows pointed to by  _lpSRowSet_ do not have to be in the same order as the columns in the table.</span></span> <span data-ttu-id="ee60c-125">Звонящий может также содержать как свойства столбцов, которые в настоящее время не в таблице.</span><span class="sxs-lookup"><span data-stu-id="ee60c-125">The caller can also include as columns properties that are not currently in the table.</span></span> <span data-ttu-id="ee60c-126">Для существующего представления **HrModifyRows** делает доступными этих новых столбцов, но не включать их в текущий набор столбцов.</span><span class="sxs-lookup"><span data-stu-id="ee60c-126">For existing views, **HrModifyRows** makes these new columns available but does not include them in the current column set.</span></span> <span data-ttu-id="ee60c-127">Для будущего представлений **HrModifyRows** включает в себя новые столбцы в наборе столбцов.</span><span class="sxs-lookup"><span data-stu-id="ee60c-127">For future views, **HrModifyRows** includes the new columns in the column set.</span></span> 
  
<span data-ttu-id="ee60c-128">После добавления строки **HrModifyRows** уведомления отправляются для всех клиентов или поставщиков услуг, у которых представление таблицы и, вызова метода [IMAPITable::Advise](imapitable-advise.md) таблицы для регистрации уведомлений.</span><span class="sxs-lookup"><span data-stu-id="ee60c-128">After **HrModifyRows** has added the rows, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> <span data-ttu-id="ee60c-129">MAPI отправляет уведомления TABLE_ROW_ADDED или TABLE_ROW_MODIFIED для каждой строки до восьми строк.</span><span class="sxs-lookup"><span data-stu-id="ee60c-129">MAPI sends TABLE_ROW_ADDED or TABLE_ROW_MODIFIED notifications for each row, up to eight rows.</span></span> <span data-ttu-id="ee60c-130">Если влияет на более восьми строк путем вызова **HrModifyRows** , MAPI отправляет уведомление об одном TABLE_CHANGED, вместо этого.</span><span class="sxs-lookup"><span data-stu-id="ee60c-130">If more than eight rows are affected by the **HrModifyRows** call, MAPI sends a single TABLE_CHANGED notification instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ee60c-131">См. также</span><span class="sxs-lookup"><span data-stu-id="ee60c-131">See also</span></span>



[<span data-ttu-id="ee60c-132">SRowSet</span><span class="sxs-lookup"><span data-stu-id="ee60c-132">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="ee60c-133">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ee60c-133">ITableData : IUnknown</span></span>](itabledataiunknown.md)

