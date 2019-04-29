---
title: Итабледатахрмодифировс
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
# <a name="itabledatahrmodifyrows"></a><span data-ttu-id="20543-103">ITableData::HrModifyRows</span><span class="sxs-lookup"><span data-stu-id="20543-103">ITableData::HrModifyRows</span></span>

  
  
<span data-ttu-id="20543-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="20543-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="20543-105">Вставляет несколько строк таблицы, что может привести к замене существующих строк.</span><span class="sxs-lookup"><span data-stu-id="20543-105">Inserts multiple table rows, possibly replacing existing rows.</span></span>
  
```cpp
HRESULT HrModifyRows(
  ULONG ulFlags,
  LPSRowSet lpSRowSet
);
```

## <a name="parameters"></a><span data-ttu-id="20543-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="20543-106">Parameters</span></span>

 <span data-ttu-id="20543-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="20543-107">_ulFlags_</span></span>
  
> <span data-ttu-id="20543-108">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="20543-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="20543-109">_Лпсровсет_</span><span class="sxs-lookup"><span data-stu-id="20543-109">_lpSRowSet_</span></span>
  
> <span data-ttu-id="20543-110">возврата Указатель на структуру [SRowSet](srowset.md) , которая содержит набор добавляемых строк, заменяя существующие строки, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="20543-110">[in] A pointer to an [SRowSet](srowset.md) structure that contains the set of rows to be added, replacing existing rows if necessary.</span></span> <span data-ttu-id="20543-111">Одна из структур значений свойств, на которую ссылается элемент **лппропс** каждой структуры [сров](srow.md) в наборе строк, должна содержать столбец индекса, то есть то же значение, которое было указано в параметре _улпроптагиндексколумн_ в вызове [ Функция Креатетабле](createtable.md) .</span><span class="sxs-lookup"><span data-stu-id="20543-111">One of the property value structures pointed to by the **lpProps** member of each [SRow](srow.md) structure in the row set should contain the index column, the same value that was specified in the  _ulPropTagIndexColumn_ parameter in the call to the [CreateTable](createtable.md) function.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="20543-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="20543-112">Return value</span></span>

<span data-ttu-id="20543-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="20543-113">S_OK</span></span> 
  
> <span data-ttu-id="20543-114">Строки были успешно вставлены или изменены.</span><span class="sxs-lookup"><span data-stu-id="20543-114">The rows were successfully inserted or modified.</span></span>
    
<span data-ttu-id="20543-115">МАПИ_Е_ИНВАЛИД_ПАРАМЕТЕР</span><span class="sxs-lookup"><span data-stu-id="20543-115">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="20543-116">У одной или нескольких переданных строк нет столбца индекса.</span><span class="sxs-lookup"><span data-stu-id="20543-116">One or more of the passed-in rows does not have an index column.</span></span> <span data-ttu-id="20543-117">Если возвращается эта ошибка, строки не изменяются.</span><span class="sxs-lookup"><span data-stu-id="20543-117">If this error is returned, no rows are changed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="20543-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="20543-118">Remarks</span></span>

<span data-ttu-id="20543-119">Метод **итабледата:: хрмодифировс** вставляет строки, описанные в структуре [SRowSet](srowset.md) , на которую указывает параметр _лпсровсет_ .</span><span class="sxs-lookup"><span data-stu-id="20543-119">The **ITableData::HrModifyRows** method inserts the rows described by the [SRowSet](srowset.md) structure pointed to by the  _lpSRowSet_ parameter.</span></span> <span data-ttu-id="20543-120">Если значение столбца индекса строки в наборе строк совпадает со значением существующей строки в таблице, существующая строка заменяется.</span><span class="sxs-lookup"><span data-stu-id="20543-120">If the index column value of a row in the row set matches the value for an existing row in the table, the existing row is replaced.</span></span> <span data-ttu-id="20543-121">Если строка, соответствующая одной из структур **SRowSet** , не существует, **хрмодифировс** добавляет строку в конец таблицы.</span><span class="sxs-lookup"><span data-stu-id="20543-121">If no row exists that matches the one included in the **SRowSet** structure, **HrModifyRows** adds the row to the end of the table.</span></span> 
  
<span data-ttu-id="20543-122">Все представления таблицы изменяются, чтобы включить строки, на которые указывает _лпсровсет_.</span><span class="sxs-lookup"><span data-stu-id="20543-122">All views of the table are modified to include the rows pointed to by  _lpSRowSet_.</span></span> <span data-ttu-id="20543-123">Однако если в представлении есть ограничение, которое исключает строку, оно может быть невидимым для пользователя.</span><span class="sxs-lookup"><span data-stu-id="20543-123">However, if a view has a restriction in place that excludes a row, it may not be visible to the user.</span></span> 
  
<span data-ttu-id="20543-124">Столбцы в строках, на которые указывает _лпсровсет_ , не обязательно должны находиться в том же порядке, что и столбцы в таблице.</span><span class="sxs-lookup"><span data-stu-id="20543-124">The columns in the rows pointed to by  _lpSRowSet_ do not have to be in the same order as the columns in the table.</span></span> <span data-ttu-id="20543-125">Вызывающий также может включать в себя свойства Columns, которые в настоящее время не находятся в таблице.</span><span class="sxs-lookup"><span data-stu-id="20543-125">The caller can also include as columns properties that are not currently in the table.</span></span> <span data-ttu-id="20543-126">Для существующих представлений **хрмодифировс** делает эти новые столбцы доступными, но не включают их в текущий набор столбцов.</span><span class="sxs-lookup"><span data-stu-id="20543-126">For existing views, **HrModifyRows** makes these new columns available but does not include them in the current column set.</span></span> <span data-ttu-id="20543-127">Для будущих просмотров **хрмодифировс** включает новые столбцы в наборе столбцов.</span><span class="sxs-lookup"><span data-stu-id="20543-127">For future views, **HrModifyRows** includes the new columns in the column set.</span></span> 
  
<span data-ttu-id="20543-128">После добавления строк **хрмодифировс** уведомления отправляются всем клиентам или поставщикам услуг, которые имеют представление таблицы и вызывают метод [IMAPITable:: Advise](imapitable-advise.md) для регистрации уведомлений.</span><span class="sxs-lookup"><span data-stu-id="20543-128">After **HrModifyRows** has added the rows, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> <span data-ttu-id="20543-129">MAPI отправляет уведомления ТАБЛЕ_РОВ_АДДЕД или ТАБЛЕ_РОВ_МОДИФИЕД для каждой строки, до восьми строк.</span><span class="sxs-lookup"><span data-stu-id="20543-129">MAPI sends TABLE_ROW_ADDED or TABLE_ROW_MODIFIED notifications for each row, up to eight rows.</span></span> <span data-ttu-id="20543-130">Если вызов **хрмодифировс** влияет на более восьми строк, MAPI отправляет одно уведомление табле_чанжед.</span><span class="sxs-lookup"><span data-stu-id="20543-130">If more than eight rows are affected by the **HrModifyRows** call, MAPI sends a single TABLE_CHANGED notification instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="20543-131">См. также</span><span class="sxs-lookup"><span data-stu-id="20543-131">See also</span></span>



[<span data-ttu-id="20543-132">SRowSet</span><span class="sxs-lookup"><span data-stu-id="20543-132">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="20543-133">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="20543-133">ITableData : IUnknown</span></span>](itabledataiunknown.md)

