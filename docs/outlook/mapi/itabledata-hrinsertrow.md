---
title: ITableDataHrInsertRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrInsertRow
api_type:
- COM
ms.assetid: e5ae37ea-81a5-49c7-9ad0-0bfac518426c
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 2709ac612fc9e2edaa57b280d52c0a5229ee9978
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435441"
---
# <a name="itabledatahrinsertrow"></a><span data-ttu-id="320f5-103">ITableData::HrInsertRow</span><span class="sxs-lookup"><span data-stu-id="320f5-103">ITableData::HrInsertRow</span></span>

  
  
<span data-ttu-id="320f5-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="320f5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="320f5-105">Вставляет строку таблицы.</span><span class="sxs-lookup"><span data-stu-id="320f5-105">Inserts a table row.</span></span> 
  
```cpp
HRESULT HrInsertRow(
  ULONG uliRow,
  LPSRow lpSRow
);
```

## <a name="parameters"></a><span data-ttu-id="320f5-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="320f5-106">Parameters</span></span>

 <span data-ttu-id="320f5-107">_uliRow_</span><span class="sxs-lookup"><span data-stu-id="320f5-107">_uliRow_</span></span>
  
> <span data-ttu-id="320f5-108">[in] Последовательное число строк, представляю которое представляет определенную строку.</span><span class="sxs-lookup"><span data-stu-id="320f5-108">[in] A sequential row number that represents a specific row.</span></span> <span data-ttu-id="320f5-109">Новая строка будет размещена после строки, на которую указывает номер.</span><span class="sxs-lookup"><span data-stu-id="320f5-109">The new row will be placed after the row that the number indicates.</span></span> <span data-ttu-id="320f5-110">Параметр  _uliRow_ может содержит номера строк от 0 до n, где n — это общее число строк в таблице.</span><span class="sxs-lookup"><span data-stu-id="320f5-110">The  _uliRow_ parameter can contains row numbers from 0 through n, where n is the total number of rows in the table.</span></span> <span data-ttu-id="320f5-111">Передача n  _в uliRow_ придает строку в конец таблицы.</span><span class="sxs-lookup"><span data-stu-id="320f5-111">Passing n in  _uliRow_ appends the row to the end of the table.</span></span> 
    
 <span data-ttu-id="320f5-112">_lpSRow_</span><span class="sxs-lookup"><span data-stu-id="320f5-112">_lpSRow_</span></span>
  
> <span data-ttu-id="320f5-113">[in] Указатель на [структуру SRow,](srow.md) которая описывает строку, которую необходимо вставить.</span><span class="sxs-lookup"><span data-stu-id="320f5-113">[in] A pointer to an [SRow](srow.md) structure that describes the row to be inserted.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="320f5-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="320f5-114">Return value</span></span>

<span data-ttu-id="320f5-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="320f5-115">S_OK</span></span> 
  
> <span data-ttu-id="320f5-116">Строка успешно вставлена.</span><span class="sxs-lookup"><span data-stu-id="320f5-116">The row was successfully inserted.</span></span>
    
<span data-ttu-id="320f5-117">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="320f5-117">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="320f5-118">Строка, которая имеет то же значение для столбца индекса, что и строка, которую необходимо вставить, уже существует в таблице.</span><span class="sxs-lookup"><span data-stu-id="320f5-118">A row that has the same value for its index column as the row to be inserted already exists in the table.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="320f5-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="320f5-119">Remarks</span></span>

<span data-ttu-id="320f5-120">Метод **ITableData::HrInsertRow** вставляет строку в таблицу в определенной позиции.</span><span class="sxs-lookup"><span data-stu-id="320f5-120">The **ITableData::HrInsertRow** method inserts a row into a table at a particular position.</span></span> <span data-ttu-id="320f5-121">Новая строка вставляется после строки, которая находится в позиции, указанной параметром _uliRow._</span><span class="sxs-lookup"><span data-stu-id="320f5-121">The new row is inserted after the row that is in the position specified by the  _uliRow_ parameter.</span></span> 
  
<span data-ttu-id="320f5-122">Если  _uliRow_ задан на количество строк в таблице, новая строка примыкает к концу таблицы.</span><span class="sxs-lookup"><span data-stu-id="320f5-122">If  _uliRow_ is set to the number of rows in the table, the new row is appended to the end of the table.</span></span> 
  
<span data-ttu-id="320f5-123">Свойство, которое выступает в качестве столбца индекса для таблицы, должно быть включено в член **lpProps** структуры [SRow,](srow.md) на который указывает параметр _lpSRow._</span><span class="sxs-lookup"><span data-stu-id="320f5-123">The property that acts as the index column for the table must be included in the **lpProps** member of the [SRow](srow.md) structure pointed to by the  _lpSRow_ parameter.</span></span> <span data-ttu-id="320f5-124">Это свойство индекса, **обычно PR_INSTANCE_KEY** [(PidTagInstanceKey),](pidtaginstancekey-canonical-property.md)используется для уникального определения строки для будущих задач обслуживания.</span><span class="sxs-lookup"><span data-stu-id="320f5-124">This index property, typically **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), is used to uniquely identify the row for future maintenance tasks.</span></span>
  
<span data-ttu-id="320f5-125">Столбцы свойств в структуре **SRow** не должны быть в том же порядке, что и столбцы свойств в таблице.</span><span class="sxs-lookup"><span data-stu-id="320f5-125">The property columns in the **SRow** structure do not have to be in the same order as the property columns in the table.</span></span> 
  
<span data-ttu-id="320f5-126">После вставки строки уведомления отправляются всем клиентам или поставщикам услуг, которые имеют представление таблицы и вызвали метод [IMAPITable::Advise](imapitable-advise.md) таблицы для регистрации уведомлений.</span><span class="sxs-lookup"><span data-stu-id="320f5-126">After the row is inserted, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> <span data-ttu-id="320f5-127">Уведомление не отправляется, если вставленная строка не включена в представление из-за ограничения.</span><span class="sxs-lookup"><span data-stu-id="320f5-127">No notification is sent if the inserted row is not included in the view due to a restriction.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="320f5-128">См. также</span><span class="sxs-lookup"><span data-stu-id="320f5-128">See also</span></span>



[<span data-ttu-id="320f5-129">SRow</span><span class="sxs-lookup"><span data-stu-id="320f5-129">SRow</span></span>](srow.md)
  
[<span data-ttu-id="320f5-130">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="320f5-130">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="320f5-131">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="320f5-131">ITableData : IUnknown</span></span>](itabledataiunknown.md)

