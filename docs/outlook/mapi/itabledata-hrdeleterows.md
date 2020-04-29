---
title: итабледатахрделетеровс
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
ms.openlocfilehash: fdd6f40b4d7aa7f65bf1a46d3d9a4f18472b19f7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416456"
---
# <a name="itabledatahrdeleterows"></a><span data-ttu-id="acd21-103">ITableData::HrDeleteRows</span><span class="sxs-lookup"><span data-stu-id="acd21-103">ITableData::HrDeleteRows</span></span>

  
  
<span data-ttu-id="acd21-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="acd21-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="acd21-105">Удаляет несколько строк таблицы.</span><span class="sxs-lookup"><span data-stu-id="acd21-105">Deletes multiple table rows.</span></span>
  
```cpp
HRESULT HrDeleteRows(
  ULONG ulFlags,
  LPSRowSet lprowsetToDelete,
  ULONG FAR * cRowsDeleted
);
```

## <a name="parameters"></a><span data-ttu-id="acd21-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="acd21-106">Parameters</span></span>

 <span data-ttu-id="acd21-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="acd21-107">_ulFlags_</span></span>
  
> <span data-ttu-id="acd21-108">возврата Битовая маска флагов, которые управляют удалением.</span><span class="sxs-lookup"><span data-stu-id="acd21-108">[in] A bitmask of flags that controls the deletion.</span></span> <span data-ttu-id="acd21-109">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="acd21-109">The following flag can be set:</span></span>
    
<span data-ttu-id="acd21-110">TAD_ALL_ROWS</span><span class="sxs-lookup"><span data-stu-id="acd21-110">TAD_ALL_ROWS</span></span> 
  
> <span data-ttu-id="acd21-111">Удаляет все строки из таблицы и всех соответствующих представлений, отправляя одно уведомление TABLE_RELOAD.</span><span class="sxs-lookup"><span data-stu-id="acd21-111">Deletes all rows from the table and all corresponding views, sending a single TABLE_RELOAD notification.</span></span>
    
 <span data-ttu-id="acd21-112">_лпровсеттоделете_</span><span class="sxs-lookup"><span data-stu-id="acd21-112">_lprowsetToDelete_</span></span>
  
> <span data-ttu-id="acd21-113">возврата Указатель на набор строк, который описывает удаляемые строки.</span><span class="sxs-lookup"><span data-stu-id="acd21-113">[in] A pointer to a row set that describes the rows to be deleted.</span></span> <span data-ttu-id="acd21-114">Параметр _лпровсеттоделете_ может иметь значение null, если установлен флаг TAD_ALL_ROWS в параметре _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="acd21-114">The  _lprowsetToDelete_ parameter can be NULL if the TAD_ALL_ROWS flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="acd21-115">_кровсделетед_</span><span class="sxs-lookup"><span data-stu-id="acd21-115">_cRowsDeleted_</span></span>
  
> <span data-ttu-id="acd21-116">вышли Количество удаленных строк.</span><span class="sxs-lookup"><span data-stu-id="acd21-116">[out] The count of the deleted rows.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="acd21-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="acd21-117">Return value</span></span>

<span data-ttu-id="acd21-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="acd21-118">S_OK</span></span> 
  
> <span data-ttu-id="acd21-119">Строки таблицы были успешно удалены.</span><span class="sxs-lookup"><span data-stu-id="acd21-119">The table rows were successfully deleted.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="acd21-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="acd21-120">Remarks</span></span>

<span data-ttu-id="acd21-121">Метод **итабледата:: хрделетеровс** ищет и удаляет строки таблицы, которые содержат столбцы, которые совпадают со свойством, на которое указывает элемент **лппропс** для каждой записи **аров** в наборе строк.</span><span class="sxs-lookup"><span data-stu-id="acd21-121">The **ITableData::HrDeleteRows** method locates and removes the table rows that contain the columns that match the property pointed to by the **lpProps** member of each **aRow** entry in the row set.</span></span> <span data-ttu-id="acd21-122">Столбец индекса используется для идентификации каждой строки; Этот столбец должен иметь тот же тег Property, что и тег свойства, переданный в параметре _улпроптагиндексколумн_ при вызове функции [креатетабле](createtable.md) .</span><span class="sxs-lookup"><span data-stu-id="acd21-122">An index column is used to identify each row; this column must have the same property tag as the property tag passed in the  _ulPropTagIndexColumn_ parameter in the call to the [CreateTable](createtable.md) function.</span></span> 
  
<span data-ttu-id="acd21-123">Количество фактически удаленных строк возвращается в _кровсделетед_.</span><span class="sxs-lookup"><span data-stu-id="acd21-123">The number of rows that were actually deleted is returned in  _cRowsDeleted_.</span></span> <span data-ttu-id="acd21-124">Сообщение об ошибке не возвращается, если не удалось найти одну или несколько строк.</span><span class="sxs-lookup"><span data-stu-id="acd21-124">No error is returned if one or more rows could not be found.</span></span> 
  
<span data-ttu-id="acd21-125">После удаления строк уведомления отправляются всем клиентам или поставщикам услуг, которые имеют представление таблицы и вызывают метод [IMAPITable:: Advise](imapitable-advise.md) для регистрации уведомлений.</span><span class="sxs-lookup"><span data-stu-id="acd21-125">After the rows are deleted, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> 
  
<span data-ttu-id="acd21-126">Удаление строк не приводит к уменьшению числа столбцов, доступных для существующих представлений таблицы или представления таблицы в открытых окнах, даже если удаленные строки являются последними значениями для определенного столбца.</span><span class="sxs-lookup"><span data-stu-id="acd21-126">Deleting rows does not reduce the columns available to existing table views or subsequently opened table views, even if the deleted rows are the last that have values for a specific column.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="acd21-127">См. также</span><span class="sxs-lookup"><span data-stu-id="acd21-127">See also</span></span>



[<span data-ttu-id="acd21-128">CreateTable</span><span class="sxs-lookup"><span data-stu-id="acd21-128">CreateTable</span></span>](createtable.md)
  
[<span data-ttu-id="acd21-129">ITableData::HrDeleteRow</span><span class="sxs-lookup"><span data-stu-id="acd21-129">ITableData::HrDeleteRow</span></span>](itabledata-hrdeleterow.md)
  
[<span data-ttu-id="acd21-130">ITableData::HrModifyRows</span><span class="sxs-lookup"><span data-stu-id="acd21-130">ITableData::HrModifyRows</span></span>](itabledata-hrmodifyrows.md)
  
[<span data-ttu-id="acd21-131">SRowSet</span><span class="sxs-lookup"><span data-stu-id="acd21-131">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="acd21-132">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="acd21-132">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="acd21-133">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="acd21-133">ITableData : IUnknown</span></span>](itabledataiunknown.md)

