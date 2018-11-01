---
title: ITableDataHrDeleteRows
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrDeleteRows
api_type:
- COM
ms.assetid: 7b351eec-9624-4b38-9978-5d0b67b64687
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 753067c8c0af15a44e0f3b71f6122d8683db4a98
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572111"
---
# <a name="itabledatahrdeleterows"></a><span data-ttu-id="90056-103">ITableData::HrDeleteRows</span><span class="sxs-lookup"><span data-stu-id="90056-103">ITableData::HrDeleteRows</span></span>

  
  
<span data-ttu-id="90056-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="90056-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="90056-105">Удаление нескольких строк таблицы.</span><span class="sxs-lookup"><span data-stu-id="90056-105">Deletes multiple table rows.</span></span>
  
```cpp
HRESULT HrDeleteRows(
  ULONG ulFlags,
  LPSRowSet lprowsetToDelete,
  ULONG FAR * cRowsDeleted
);
```

## <a name="parameters"></a><span data-ttu-id="90056-106">���������</span><span class="sxs-lookup"><span data-stu-id="90056-106">Parameters</span></span>

 <span data-ttu-id="90056-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="90056-107">_ulFlags_</span></span>
  
> <span data-ttu-id="90056-108">[in] Битовая маска флаги, который управляет удаления.</span><span class="sxs-lookup"><span data-stu-id="90056-108">[in] A bitmask of flags that controls the deletion.</span></span> <span data-ttu-id="90056-109">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="90056-109">The following flag can be set:</span></span>
    
<span data-ttu-id="90056-110">TAD_ALL_ROWS</span><span class="sxs-lookup"><span data-stu-id="90056-110">TAD_ALL_ROWS</span></span> 
  
> <span data-ttu-id="90056-111">Удаляет все строки из таблицы и все соответствующие представления, отправки одного TABLE_RELOAD уведомления.</span><span class="sxs-lookup"><span data-stu-id="90056-111">Deletes all rows from the table and all corresponding views, sending a single TABLE_RELOAD notification.</span></span>
    
 <span data-ttu-id="90056-112">_lprowsetToDelete_</span><span class="sxs-lookup"><span data-stu-id="90056-112">_lprowsetToDelete_</span></span>
  
> <span data-ttu-id="90056-113">[in] Указатель на набор строк, с описанием удаляемых строк.</span><span class="sxs-lookup"><span data-stu-id="90056-113">[in] A pointer to a row set that describes the rows to be deleted.</span></span> <span data-ttu-id="90056-114">Параметр _lprowsetToDelete_ может быть NULL, если флаг TAD_ALL_ROWS установлен в параметре _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="90056-114">The  _lprowsetToDelete_ parameter can be NULL if the TAD_ALL_ROWS flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="90056-115">_cRowsDeleted_</span><span class="sxs-lookup"><span data-stu-id="90056-115">_cRowsDeleted_</span></span>
  
> <span data-ttu-id="90056-116">[out] Число удаленных строк.</span><span class="sxs-lookup"><span data-stu-id="90056-116">[out] The count of the deleted rows.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="90056-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="90056-117">Return value</span></span>

<span data-ttu-id="90056-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="90056-118">S_OK</span></span> 
  
> <span data-ttu-id="90056-119">Строки таблицы были успешно удалены.</span><span class="sxs-lookup"><span data-stu-id="90056-119">The table rows were successfully deleted.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="90056-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="90056-120">Remarks</span></span>

<span data-ttu-id="90056-121">Метод **ITableData::HrDeleteRows** обнаруживает и удаляет строки в таблице, содержащие столбцы, которые соответствуют по **lpProps** членом каждой записи **aRow** в строке, на который указывает свойство.</span><span class="sxs-lookup"><span data-stu-id="90056-121">The **ITableData::HrDeleteRows** method locates and removes the table rows that contain the columns that match the property pointed to by the **lpProps** member of each **aRow** entry in the row set.</span></span> <span data-ttu-id="90056-122">Столбец индекса используется для идентификации каждой строки; Этот столбец должен иметь один и тот же тег свойство как свойство tag, переданной в параметре _ulPropTagIndexColumn_ в вызове функции [CreateTable](createtable.md) .</span><span class="sxs-lookup"><span data-stu-id="90056-122">An index column is used to identify each row; this column must have the same property tag as the property tag passed in the  _ulPropTagIndexColumn_ parameter in the call to the [CreateTable](createtable.md) function.</span></span> 
  
<span data-ttu-id="90056-123">Количество строк, которые фактически были удалены, возвращается в _cRowsDeleted_.</span><span class="sxs-lookup"><span data-stu-id="90056-123">The number of rows that were actually deleted is returned in  _cRowsDeleted_.</span></span> <span data-ttu-id="90056-124">Сообщение об ошибке не возвращается, если не удается найти один или несколько строк.</span><span class="sxs-lookup"><span data-stu-id="90056-124">No error is returned if one or more rows could not be found.</span></span> 
  
<span data-ttu-id="90056-125">После удаления строки уведомления отправляются для всех клиентов или поставщиков услуг, у которых представление таблицы и, вызова метода [IMAPITable::Advise](imapitable-advise.md) таблицы для регистрации уведомлений.</span><span class="sxs-lookup"><span data-stu-id="90056-125">After the rows are deleted, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> 
  
<span data-ttu-id="90056-126">Удаление строк не уменьшает столбцов, доступных для существующего представления таблицы или впоследствии открывается представления таблицы, даже если удаленных строк, последний, имеют значения для определенного столбца.</span><span class="sxs-lookup"><span data-stu-id="90056-126">Deleting rows does not reduce the columns available to existing table views or subsequently opened table views, even if the deleted rows are the last that have values for a specific column.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="90056-127">См. также</span><span class="sxs-lookup"><span data-stu-id="90056-127">See also</span></span>



[<span data-ttu-id="90056-128">CreateTable</span><span class="sxs-lookup"><span data-stu-id="90056-128">CreateTable</span></span>](createtable.md)
  
[<span data-ttu-id="90056-129">ITableData::HrDeleteRow</span><span class="sxs-lookup"><span data-stu-id="90056-129">ITableData::HrDeleteRow</span></span>](itabledata-hrdeleterow.md)
  
[<span data-ttu-id="90056-130">ITableData::HrModifyRows</span><span class="sxs-lookup"><span data-stu-id="90056-130">ITableData::HrModifyRows</span></span>](itabledata-hrmodifyrows.md)
  
[<span data-ttu-id="90056-131">SRowSet</span><span class="sxs-lookup"><span data-stu-id="90056-131">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="90056-132">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="90056-132">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="90056-133">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="90056-133">ITableData : IUnknown</span></span>](itabledataiunknown.md)

