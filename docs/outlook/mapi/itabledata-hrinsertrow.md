---
title: Итабледатахринсертров
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278808"
---
# <a name="itabledatahrinsertrow"></a><span data-ttu-id="1b263-103">ITableData::HrInsertRow</span><span class="sxs-lookup"><span data-stu-id="1b263-103">ITableData::HrInsertRow</span></span>

  
  
<span data-ttu-id="1b263-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1b263-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1b263-105">Вставляет строку таблицы.</span><span class="sxs-lookup"><span data-stu-id="1b263-105">Inserts a table row.</span></span> 
  
```cpp
HRESULT HrInsertRow(
  ULONG uliRow,
  LPSRow lpSRow
);
```

## <a name="parameters"></a><span data-ttu-id="1b263-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1b263-106">Parameters</span></span>

 <span data-ttu-id="1b263-107">_Улиров_</span><span class="sxs-lookup"><span data-stu-id="1b263-107">_uliRow_</span></span>
  
> <span data-ttu-id="1b263-108">возврата Последовательный номер строки, представляющий определенную строку.</span><span class="sxs-lookup"><span data-stu-id="1b263-108">[in] A sequential row number that represents a specific row.</span></span> <span data-ttu-id="1b263-109">Новая строка будет размещаться после строки, которая указывает на число.</span><span class="sxs-lookup"><span data-stu-id="1b263-109">The new row will be placed after the row that the number indicates.</span></span> <span data-ttu-id="1b263-110">Параметр _улиров_ может содержать номера строк от 0 до n, где n — общее количество строк в таблице.</span><span class="sxs-lookup"><span data-stu-id="1b263-110">The  _uliRow_ parameter can contains row numbers from 0 through n, where n is the total number of rows in the table.</span></span> <span data-ttu-id="1b263-111">При передаче n в _улиров_ строка добавляется в конец таблицы.</span><span class="sxs-lookup"><span data-stu-id="1b263-111">Passing n in  _uliRow_ appends the row to the end of the table.</span></span> 
    
 <span data-ttu-id="1b263-112">_Лпсров_</span><span class="sxs-lookup"><span data-stu-id="1b263-112">_lpSRow_</span></span>
  
> <span data-ttu-id="1b263-113">возврата Указатель на структуру [сров](srow.md) , описывающую вставляемую строку.</span><span class="sxs-lookup"><span data-stu-id="1b263-113">[in] A pointer to an [SRow](srow.md) structure that describes the row to be inserted.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1b263-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1b263-114">Return value</span></span>

<span data-ttu-id="1b263-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="1b263-115">S_OK</span></span> 
  
> <span data-ttu-id="1b263-116">Строка была успешно вставлена.</span><span class="sxs-lookup"><span data-stu-id="1b263-116">The row was successfully inserted.</span></span>
    
<span data-ttu-id="1b263-117">МАПИ_Е_ИНВАЛИД_ПАРАМЕТЕР</span><span class="sxs-lookup"><span data-stu-id="1b263-117">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="1b263-118">Строка, имеющая то же значение для столбца индекса, что и вставляемая строка, уже существует в таблице.</span><span class="sxs-lookup"><span data-stu-id="1b263-118">A row that has the same value for its index column as the row to be inserted already exists in the table.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1b263-119">Замечания</span><span class="sxs-lookup"><span data-stu-id="1b263-119">Remarks</span></span>

<span data-ttu-id="1b263-120">Метод **итабледата:: хринсертров** вставляет строку в таблицу в определенном месте.</span><span class="sxs-lookup"><span data-stu-id="1b263-120">The **ITableData::HrInsertRow** method inserts a row into a table at a particular position.</span></span> <span data-ttu-id="1b263-121">Новая строка вставляется после строки, которая находится в позиции, заданной параметром _улиров_ .</span><span class="sxs-lookup"><span data-stu-id="1b263-121">The new row is inserted after the row that is in the position specified by the  _uliRow_ parameter.</span></span> 
  
<span data-ttu-id="1b263-122">Если для _улиров_ задано количество строк в таблице, Новая строка добавляется в конец таблицы.</span><span class="sxs-lookup"><span data-stu-id="1b263-122">If  _uliRow_ is set to the number of rows in the table, the new row is appended to the end of the table.</span></span> 
  
<span data-ttu-id="1b263-123">Свойство, действующее как столбец индекса для таблицы, должно быть включено в элемент **лппропс** структуры [сров](srow.md) , на которую указывает параметр _лпсров_ .</span><span class="sxs-lookup"><span data-stu-id="1b263-123">The property that acts as the index column for the table must be included in the **lpProps** member of the [SRow](srow.md) structure pointed to by the  _lpSRow_ parameter.</span></span> <span data-ttu-id="1b263-124">Это свойство индекса, как правило, **пр_инстанце_кэй** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), используется для уникальной идентификации строки для будущих задач обслуживания.</span><span class="sxs-lookup"><span data-stu-id="1b263-124">This index property, typically **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), is used to uniquely identify the row for future maintenance tasks.</span></span>
  
<span data-ttu-id="1b263-125">Столбцы свойств в структуре **сров** не обязательно должны находиться в том же порядке, что и столбцы свойств в таблице.</span><span class="sxs-lookup"><span data-stu-id="1b263-125">The property columns in the **SRow** structure do not have to be in the same order as the property columns in the table.</span></span> 
  
<span data-ttu-id="1b263-126">После вставки строки уведомления отправляются всем клиентам или поставщикам услуг, которые имеют представление таблицы и вызывают метод [IMAPITable:: Advise](imapitable-advise.md) для регистрации уведомлений.</span><span class="sxs-lookup"><span data-stu-id="1b263-126">After the row is inserted, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> <span data-ttu-id="1b263-127">Если вставленная строка не включена в представление из-за ограничения, уведомления не отправляются.</span><span class="sxs-lookup"><span data-stu-id="1b263-127">No notification is sent if the inserted row is not included in the view due to a restriction.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1b263-128">См. также</span><span class="sxs-lookup"><span data-stu-id="1b263-128">See also</span></span>



[<span data-ttu-id="1b263-129">SRow</span><span class="sxs-lookup"><span data-stu-id="1b263-129">SRow</span></span>](srow.md)
  
[<span data-ttu-id="1b263-130">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="1b263-130">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="1b263-131">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1b263-131">ITableData : IUnknown</span></span>](itabledataiunknown.md)

