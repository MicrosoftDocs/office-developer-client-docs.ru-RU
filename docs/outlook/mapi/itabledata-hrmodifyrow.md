---
title: ITableDataHrModifyRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrModifyRow
api_type:
- COM
ms.assetid: 9e255b3e-dd17-4528-ba4e-c3a1aef32b04
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 5ef210aedc884e5c09eca6335199e2ef284b901c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574834"
---
# <a name="itabledatahrmodifyrow"></a><span data-ttu-id="e7590-103">ITableData::HrModifyRow</span><span class="sxs-lookup"><span data-stu-id="e7590-103">ITableData::HrModifyRow</span></span>

  
  
<span data-ttu-id="e7590-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e7590-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e7590-105">Добавление новой строки в таблице, возможно заменить существующую строку.</span><span class="sxs-lookup"><span data-stu-id="e7590-105">Inserts a new table row, possibly replacing an existing row.</span></span>
  
```cpp
HRESULT HrModifyRow(
  LPSRow lpSRow
);
```

## <a name="parameters"></a><span data-ttu-id="e7590-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e7590-106">Parameters</span></span>

 <span data-ttu-id="e7590-107">_lpSRow_</span><span class="sxs-lookup"><span data-stu-id="e7590-107">_lpSRow_</span></span>
  
> <span data-ttu-id="e7590-108">[in] Указатель на структуру [SRow](srow.md) , описывающую строку добавить или заменить существующую строку.</span><span class="sxs-lookup"><span data-stu-id="e7590-108">[in] A pointer to an [SRow](srow.md) structure that describes the row to be added or to replace an existing row.</span></span> <span data-ttu-id="e7590-109">Один структур значение свойства, на который указывает член **lpProps** структуры **SRow** должен содержать столбце индекса такое же значение, которое было указано в параметре _ulPropTagIndexColumn_ в вызове [CreateTable ](createtable.md)функции.</span><span class="sxs-lookup"><span data-stu-id="e7590-109">One of the property value structures pointed to by the **lpProps** member of the **SRow** structure should contain the index column, the same value that was specified in the  _ulPropTagIndexColumn_ parameter in the call to the [CreateTable](createtable.md) function.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e7590-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e7590-110">Return value</span></span>

<span data-ttu-id="e7590-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="e7590-111">S_OK</span></span> 
  
> <span data-ttu-id="e7590-112">Строки были успешно добавлены или изменены.</span><span class="sxs-lookup"><span data-stu-id="e7590-112">The row was successfully inserted or modified.</span></span>
    
<span data-ttu-id="e7590-113">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e7590-113">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="e7590-114">Строка переданное не имеет столбец индекса.</span><span class="sxs-lookup"><span data-stu-id="e7590-114">The passed-in row does not have an index column.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e7590-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="e7590-115">Remarks</span></span>

<span data-ttu-id="e7590-116">Метод **ITableData::HrModifyRow** вставляет строку, описанного в структуре **SRow** указывает параметр _lpSRow_ .</span><span class="sxs-lookup"><span data-stu-id="e7590-116">The **ITableData::HrModifyRow** method inserts the row described by the **SRow** structure pointed to by the  _lpSRow_ parameter.</span></span> <span data-ttu-id="e7590-117">Если строку, в которой имеет такое же значение для его индекс столбца как строку, указывающий _lpSRow_ уже существует в таблице, будет заменен существующей строки.</span><span class="sxs-lookup"><span data-stu-id="e7590-117">If a row that has the same value for its index column as the row that  _lpSRow_ points to already exists in the table, the existing row is replaced.</span></span> <span data-ttu-id="e7590-118">Если нет строки, которая соответствует того, что включено в структуре **SRow** , **HrModifyRow** добавляет строку в конец таблицы.</span><span class="sxs-lookup"><span data-stu-id="e7590-118">If no row exists that matches the one included in the **SRow** structure, **HrModifyRow** adds the row to the end of the table.</span></span> 
  
<span data-ttu-id="e7590-119">Все представления таблицы изменяются, чтобы включить строку, на который указывает _lpSRow_.</span><span class="sxs-lookup"><span data-stu-id="e7590-119">All views of the table are modified to include the row pointed to by  _lpSRow_.</span></span> <span data-ttu-id="e7590-120">Тем не менее если представление имеет ограничение на месте, которое не содержит строку, он может оказаться видимым для пользователя.</span><span class="sxs-lookup"><span data-stu-id="e7590-120">However, if a view has a restriction in place that excludes the row, it may not be visible to the user.</span></span> 
  
<span data-ttu-id="e7590-121">Столбцы в строке, на который указывает _lpSRow_ нет необходимости находиться в том же порядке в виде столбцов в таблице.</span><span class="sxs-lookup"><span data-stu-id="e7590-121">The columns in the row pointed to by  _lpSRow_ do not have to be in the same order as the columns in the table.</span></span> <span data-ttu-id="e7590-122">Звонящий может также содержать как свойства столбцов, которые в настоящее время не в таблице.</span><span class="sxs-lookup"><span data-stu-id="e7590-122">The caller can also include as columns properties that are not currently in the table.</span></span> <span data-ttu-id="e7590-123">Для существующего представления **HrModifyRow** делает доступными этих новых столбцов, но не включать их в текущий набор столбцов.</span><span class="sxs-lookup"><span data-stu-id="e7590-123">For existing views, **HrModifyRow** makes these new columns available but does not include them in the current column set.</span></span> <span data-ttu-id="e7590-124">Для будущего представлений **HrModifyRow** включает в себя новые столбцы в наборе столбцов.</span><span class="sxs-lookup"><span data-stu-id="e7590-124">For future views, **HrModifyRow** includes the new columns in the column set.</span></span> 
  
<span data-ttu-id="e7590-125">После **HrModifyRow** добавляет строку, уведомления отправляются для всех клиентов или поставщиков услуг, у которых представление таблицы и, вызова метода [IMAPITable::Advise](imapitable-advise.md) таблицы для регистрации уведомлений.</span><span class="sxs-lookup"><span data-stu-id="e7590-125">After **HrModifyRow** adds the row, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e7590-126">См. также</span><span class="sxs-lookup"><span data-stu-id="e7590-126">See also</span></span>



[<span data-ttu-id="e7590-127">SRow</span><span class="sxs-lookup"><span data-stu-id="e7590-127">SRow</span></span>](srow.md)
  
[<span data-ttu-id="e7590-128">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="e7590-128">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="e7590-129">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e7590-129">ITableData : IUnknown</span></span>](itabledataiunknown.md)

