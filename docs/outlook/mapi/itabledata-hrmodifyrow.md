---
title: Итабледатахрмодифиров
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348666"
---
# <a name="itabledatahrmodifyrow"></a><span data-ttu-id="f459e-103">ITableData::HrModifyRow</span><span class="sxs-lookup"><span data-stu-id="f459e-103">ITableData::HrModifyRow</span></span>

  
  
<span data-ttu-id="f459e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f459e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f459e-105">Вставляет новую строку таблицы, возможно заменив существующую.</span><span class="sxs-lookup"><span data-stu-id="f459e-105">Inserts a new table row, possibly replacing an existing row.</span></span>
  
```cpp
HRESULT HrModifyRow(
  LPSRow lpSRow
);
```

## <a name="parameters"></a><span data-ttu-id="f459e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f459e-106">Parameters</span></span>

 <span data-ttu-id="f459e-107">_Лпсров_</span><span class="sxs-lookup"><span data-stu-id="f459e-107">_lpSRow_</span></span>
  
> <span data-ttu-id="f459e-108">возврата Указатель на структуру [сров](srow.md) , описывающую строку, которую необходимо добавить или заменить существующую строку.</span><span class="sxs-lookup"><span data-stu-id="f459e-108">[in] A pointer to an [SRow](srow.md) structure that describes the row to be added or to replace an existing row.</span></span> <span data-ttu-id="f459e-109">Одна из структур значений свойств, на которую ссылается элемент **лппропс** структуры **сров** , должна содержать столбец индекса, то же значение, которое было указано в параметре _улпроптагиндексколумн_ при вызове [креатетабле ](createtable.md)функция.</span><span class="sxs-lookup"><span data-stu-id="f459e-109">One of the property value structures pointed to by the **lpProps** member of the **SRow** structure should contain the index column, the same value that was specified in the  _ulPropTagIndexColumn_ parameter in the call to the [CreateTable](createtable.md) function.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f459e-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f459e-110">Return value</span></span>

<span data-ttu-id="f459e-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="f459e-111">S_OK</span></span> 
  
> <span data-ttu-id="f459e-112">Строка была успешно вставлена или изменена.</span><span class="sxs-lookup"><span data-stu-id="f459e-112">The row was successfully inserted or modified.</span></span>
    
<span data-ttu-id="f459e-113">МАПИ_Е_ИНВАЛИД_ПАРАМЕТЕР</span><span class="sxs-lookup"><span data-stu-id="f459e-113">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="f459e-114">Переданная строка не имеет столбца индекса.</span><span class="sxs-lookup"><span data-stu-id="f459e-114">The passed-in row does not have an index column.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f459e-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="f459e-115">Remarks</span></span>

<span data-ttu-id="f459e-116">Метод **итабледата:: хрмодифиров** вставляет строку, описанную структурой **сров** , на которую указывает параметр _лпсров_ .</span><span class="sxs-lookup"><span data-stu-id="f459e-116">The **ITableData::HrModifyRow** method inserts the row described by the **SRow** structure pointed to by the  _lpSRow_ parameter.</span></span> <span data-ttu-id="f459e-117">Если строка, имеющая то же значение для столбца индекса, в качестве строки, в которой _лпсров_ указывает, уже существует в таблице, то существующая строка заменяется.</span><span class="sxs-lookup"><span data-stu-id="f459e-117">If a row that has the same value for its index column as the row that  _lpSRow_ points to already exists in the table, the existing row is replaced.</span></span> <span data-ttu-id="f459e-118">Если строка, соответствующая одной из структур **сров** , не существует, **хрмодифиров** добавляет строку в конец таблицы.</span><span class="sxs-lookup"><span data-stu-id="f459e-118">If no row exists that matches the one included in the **SRow** structure, **HrModifyRow** adds the row to the end of the table.</span></span> 
  
<span data-ttu-id="f459e-119">Все представления таблицы изменяются, чтобы включить строку, на которую указывает _лпсров_.</span><span class="sxs-lookup"><span data-stu-id="f459e-119">All views of the table are modified to include the row pointed to by  _lpSRow_.</span></span> <span data-ttu-id="f459e-120">Однако если в представлении есть ограничение, которое исключает строку, оно может быть невидимым для пользователя.</span><span class="sxs-lookup"><span data-stu-id="f459e-120">However, if a view has a restriction in place that excludes the row, it may not be visible to the user.</span></span> 
  
<span data-ttu-id="f459e-121">Столбцы в строке, на которые указывает _лпсров_ , не обязательно должны находиться в том же порядке, что и столбцы в таблице.</span><span class="sxs-lookup"><span data-stu-id="f459e-121">The columns in the row pointed to by  _lpSRow_ do not have to be in the same order as the columns in the table.</span></span> <span data-ttu-id="f459e-122">Вызывающий также может включать в себя свойства Columns, которые в настоящее время не находятся в таблице.</span><span class="sxs-lookup"><span data-stu-id="f459e-122">The caller can also include as columns properties that are not currently in the table.</span></span> <span data-ttu-id="f459e-123">Для существующих представлений **хрмодифиров** делает эти новые столбцы доступными, но не включают их в текущий набор столбцов.</span><span class="sxs-lookup"><span data-stu-id="f459e-123">For existing views, **HrModifyRow** makes these new columns available but does not include them in the current column set.</span></span> <span data-ttu-id="f459e-124">Для будущих просмотров **хрмодифиров** включает новые столбцы в наборе столбцов.</span><span class="sxs-lookup"><span data-stu-id="f459e-124">For future views, **HrModifyRow** includes the new columns in the column set.</span></span> 
  
<span data-ttu-id="f459e-125">После того как **хрмодифиров** добавит строку, уведомления отправляются всем клиентам или поставщикам услуг, которые имеют представление таблицы и вызывают метод [IMAPITable:: Advise](imapitable-advise.md) для регистрации уведомлений.</span><span class="sxs-lookup"><span data-stu-id="f459e-125">After **HrModifyRow** adds the row, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f459e-126">См. также</span><span class="sxs-lookup"><span data-stu-id="f459e-126">See also</span></span>



[<span data-ttu-id="f459e-127">SRow</span><span class="sxs-lookup"><span data-stu-id="f459e-127">SRow</span></span>](srow.md)
  
[<span data-ttu-id="f459e-128">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="f459e-128">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="f459e-129">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f459e-129">ITableData : IUnknown</span></span>](itabledataiunknown.md)

