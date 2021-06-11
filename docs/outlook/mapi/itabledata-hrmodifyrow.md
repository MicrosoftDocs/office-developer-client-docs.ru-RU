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
ms.openlocfilehash: 44ecf095ad24dd266dc5f603ace9c7b9f21c1b41
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409001"
---
# <a name="itabledatahrmodifyrow"></a><span data-ttu-id="b9e9e-103">ITableData::HrModifyRow</span><span class="sxs-lookup"><span data-stu-id="b9e9e-103">ITableData::HrModifyRow</span></span>

  
  
<span data-ttu-id="b9e9e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b9e9e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b9e9e-105">Вставляет новую строку таблицы, возможно, заменив существующую строку.</span><span class="sxs-lookup"><span data-stu-id="b9e9e-105">Inserts a new table row, possibly replacing an existing row.</span></span>
  
```cpp
HRESULT HrModifyRow(
  LPSRow lpSRow
);
```

## <a name="parameters"></a><span data-ttu-id="b9e9e-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="b9e9e-106">Parameters</span></span>

 <span data-ttu-id="b9e9e-107">_lpSRow_</span><span class="sxs-lookup"><span data-stu-id="b9e9e-107">_lpSRow_</span></span>
  
> <span data-ttu-id="b9e9e-108">[in] Указатель на структуру [SRow,](srow.md) описывающую строку, которая должна быть добавлена или заменить существующую строку.</span><span class="sxs-lookup"><span data-stu-id="b9e9e-108">[in] A pointer to an [SRow](srow.md) structure that describes the row to be added or to replace an existing row.</span></span> <span data-ttu-id="b9e9e-109">Одна из структур значений свойств, на которые указывает член **lpProps** структуры **SRow,** должна содержать столбец индекса, то же значение, которое было задано в параметре _ulPropTagIndexColumn_ в вызове к функции [CreateTable.](createtable.md)</span><span class="sxs-lookup"><span data-stu-id="b9e9e-109">One of the property value structures pointed to by the **lpProps** member of the **SRow** structure should contain the index column, the same value that was specified in the  _ulPropTagIndexColumn_ parameter in the call to the [CreateTable](createtable.md) function.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b9e9e-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b9e9e-110">Return value</span></span>

<span data-ttu-id="b9e9e-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="b9e9e-111">S_OK</span></span> 
  
> <span data-ttu-id="b9e9e-112">Строка успешно вставлена или изменена.</span><span class="sxs-lookup"><span data-stu-id="b9e9e-112">The row was successfully inserted or modified.</span></span>
    
<span data-ttu-id="b9e9e-113">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b9e9e-113">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="b9e9e-114">В пройденной строке нет столбца индекса.</span><span class="sxs-lookup"><span data-stu-id="b9e9e-114">The passed-in row does not have an index column.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b9e9e-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="b9e9e-115">Remarks</span></span>

<span data-ttu-id="b9e9e-116">Метод **ITableData::HrModifyRow** вставляет строку, описанную структурой **SRow,** отмеченную параметром _lpSRow._</span><span class="sxs-lookup"><span data-stu-id="b9e9e-116">The **ITableData::HrModifyRow** method inserts the row described by the **SRow** structure pointed to by the  _lpSRow_ parameter.</span></span> <span data-ttu-id="b9e9e-117">Если строка, которая имеет то же значение для столбца индекса, что и строка, на которую  _указывает lpSRow,_ уже существует в таблице, будет заменена существующая строка.</span><span class="sxs-lookup"><span data-stu-id="b9e9e-117">If a row that has the same value for its index column as the row that  _lpSRow_ points to already exists in the table, the existing row is replaced.</span></span> <span data-ttu-id="b9e9e-118">Если строка не соответствует строке, включенной в структуру **SRow,** **HrModifyRow** добавляет строку в конец таблицы.</span><span class="sxs-lookup"><span data-stu-id="b9e9e-118">If no row exists that matches the one included in the **SRow** structure, **HrModifyRow** adds the row to the end of the table.</span></span> 
  
<span data-ttu-id="b9e9e-119">Все представления таблицы изменены, чтобы включить строку, на нее указывает _lpSRow._</span><span class="sxs-lookup"><span data-stu-id="b9e9e-119">All views of the table are modified to include the row pointed to by  _lpSRow_.</span></span> <span data-ttu-id="b9e9e-120">Однако если представление имеет ограничение, исключаее строки, оно может быть не видно пользователю.</span><span class="sxs-lookup"><span data-stu-id="b9e9e-120">However, if a view has a restriction in place that excludes the row, it may not be visible to the user.</span></span> 
  
<span data-ttu-id="b9e9e-121">Столбцы в строке, на которые указывает  _lpSRow,_ не должны быть в том же порядке, что и столбцы в таблице.</span><span class="sxs-lookup"><span data-stu-id="b9e9e-121">The columns in the row pointed to by  _lpSRow_ do not have to be in the same order as the columns in the table.</span></span> <span data-ttu-id="b9e9e-122">Вызываемая может также включать в качестве столбцов свойства, которые в настоящее время не находятся в таблице.</span><span class="sxs-lookup"><span data-stu-id="b9e9e-122">The caller can also include as columns properties that are not currently in the table.</span></span> <span data-ttu-id="b9e9e-123">Для существующих представлений **HrModifyRow** делает эти новые столбцы доступными, но не включает их в текущий набор столбцов.</span><span class="sxs-lookup"><span data-stu-id="b9e9e-123">For existing views, **HrModifyRow** makes these new columns available but does not include them in the current column set.</span></span> <span data-ttu-id="b9e9e-124">Для будущих представлений **HrModifyRow** включает новые столбцы в набор столбцов.</span><span class="sxs-lookup"><span data-stu-id="b9e9e-124">For future views, **HrModifyRow** includes the new columns in the column set.</span></span> 
  
<span data-ttu-id="b9e9e-125">После того, как **HrModifyRow** добавляет строку, уведомления отправляются всем клиентам или поставщикам услуг, которые имеют представление таблицы и которые вызвали метод [IMAPITable::Advise](imapitable-advise.md) таблицы для регистрации уведомлений.</span><span class="sxs-lookup"><span data-stu-id="b9e9e-125">After **HrModifyRow** adds the row, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b9e9e-126">См. также</span><span class="sxs-lookup"><span data-stu-id="b9e9e-126">See also</span></span>



[<span data-ttu-id="b9e9e-127">SRow</span><span class="sxs-lookup"><span data-stu-id="b9e9e-127">SRow</span></span>](srow.md)
  
[<span data-ttu-id="b9e9e-128">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="b9e9e-128">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="b9e9e-129">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b9e9e-129">ITableData : IUnknown</span></span>](itabledataiunknown.md)

