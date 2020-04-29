---
title: Итабледата IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData
api_type:
- COM
ms.assetid: ac7ae09f-ce19-45cf-8963-fad5bba75452
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3992bea899239ee5975505dec366490d6bbe1698
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430597"
---
# <a name="itabledata--iunknown"></a><span data-ttu-id="ddd93-103">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ddd93-103">ITableData : IUnknown</span></span>

  
  
<span data-ttu-id="ddd93-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ddd93-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ddd93-105">Предоставляет служебные методы для работы с таблицами.</span><span class="sxs-lookup"><span data-stu-id="ddd93-105">Provides utility methods for working with tables.</span></span> <span data-ttu-id="ddd93-106">MAPI предоставляет объекты табличных данных или объекты, которые реализуют **итабледата** , чтобы помочь поставщикам услуг выполнять обслуживание таблиц.</span><span class="sxs-lookup"><span data-stu-id="ddd93-106">MAPI provides table data objects or objects that implement **ITableData** to help service providers perform table maintenance.</span></span> <span data-ttu-id="ddd93-107">Чтобы получить объект данных таблицы, поставщики услуг вызывают функцию [креатетабле](createtable.md) .</span><span class="sxs-lookup"><span data-stu-id="ddd93-107">To obtain a table data object, service providers call the [CreateTable](createtable.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ddd93-108">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="ddd93-108">Header file:</span></span>  <br/> |<span data-ttu-id="ddd93-109">Мапиутил. h</span><span class="sxs-lookup"><span data-stu-id="ddd93-109">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="ddd93-110">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="ddd93-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="ddd93-111">Объекты табличных данных</span><span class="sxs-lookup"><span data-stu-id="ddd93-111">Table data objects</span></span>  <br/> |
|<span data-ttu-id="ddd93-112">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="ddd93-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="ddd93-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="ddd93-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="ddd93-114">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="ddd93-114">Called by:</span></span>  <br/> |<span data-ttu-id="ddd93-115">Поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="ddd93-115">Service providers</span></span>  <br/> |
|<span data-ttu-id="ddd93-116">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="ddd93-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="ddd93-117">IID_IMAPITableData</span><span class="sxs-lookup"><span data-stu-id="ddd93-117">IID_IMAPITableData</span></span>  <br/> |
|<span data-ttu-id="ddd93-118">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="ddd93-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="ddd93-119">лптабледата</span><span class="sxs-lookup"><span data-stu-id="ddd93-119">LPTABLEDATA</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="ddd93-120">Заказ vtable</span><span class="sxs-lookup"><span data-stu-id="ddd93-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="ddd93-121">хржетвиев</span><span class="sxs-lookup"><span data-stu-id="ddd93-121">HrGetView</span></span>](itabledata-hrgetview.md) <br/> |<span data-ttu-id="ddd93-122">Создает табличное представление, возвращая указатель на реализацию [IMAPITable](imapitableiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="ddd93-122">Creates a table view, returning a pointer to an [IMAPITable](imapitableiunknown.md) implementation.</span></span>  <br/> |
|[<span data-ttu-id="ddd93-123">хрмодифиров</span><span class="sxs-lookup"><span data-stu-id="ddd93-123">HrModifyRow</span></span>](itabledata-hrmodifyrow.md) <br/> |<span data-ttu-id="ddd93-124">Вставляет новую строку таблицы, возможно заменив существующую.</span><span class="sxs-lookup"><span data-stu-id="ddd93-124">Inserts a new table row, possibly replacing an existing row.</span></span>  <br/> |
|[<span data-ttu-id="ddd93-125">хрделетеров</span><span class="sxs-lookup"><span data-stu-id="ddd93-125">HrDeleteRow</span></span>](itabledata-hrdeleterow.md) <br/> |<span data-ttu-id="ddd93-126">Удаляет строку таблицы.</span><span class="sxs-lookup"><span data-stu-id="ddd93-126">Deletes a table row.</span></span>  <br/> |
|[<span data-ttu-id="ddd93-127">хркуериров</span><span class="sxs-lookup"><span data-stu-id="ddd93-127">HrQueryRow</span></span>](itabledata-hrqueryrow.md) <br/> |<span data-ttu-id="ddd93-128">Получает строку таблицы.</span><span class="sxs-lookup"><span data-stu-id="ddd93-128">Retrieves a table row.</span></span>  <br/> |
|[<span data-ttu-id="ddd93-129">хренумров</span><span class="sxs-lookup"><span data-stu-id="ddd93-129">HrEnumRow</span></span>](itabledata-hrenumrow.md) <br/> |<span data-ttu-id="ddd93-130">Извлекает строку на основе ее позиции в таблице.</span><span class="sxs-lookup"><span data-stu-id="ddd93-130">Retrieves a row based on its position in the table.</span></span>  <br/> |
|[<span data-ttu-id="ddd93-131">хрнотифи</span><span class="sxs-lookup"><span data-stu-id="ddd93-131">HrNotify</span></span>](itabledata-hrnotify.md) <br/> |<span data-ttu-id="ddd93-132">Отправляет уведомление для строки таблицы.</span><span class="sxs-lookup"><span data-stu-id="ddd93-132">Sends a notification for a table row.</span></span>  <br/> |
|[<span data-ttu-id="ddd93-133">хринсертров</span><span class="sxs-lookup"><span data-stu-id="ddd93-133">HrInsertRow</span></span>](itabledata-hrinsertrow.md) <br/> |<span data-ttu-id="ddd93-134">Вставляет строку таблицы.</span><span class="sxs-lookup"><span data-stu-id="ddd93-134">Inserts a table row.</span></span>  <br/> |
|[<span data-ttu-id="ddd93-135">хрмодифировс</span><span class="sxs-lookup"><span data-stu-id="ddd93-135">HrModifyRows</span></span>](itabledata-hrmodifyrows.md) <br/> |<span data-ttu-id="ddd93-136">Вставляет несколько строк таблицы, что может привести к замене существующих строк.</span><span class="sxs-lookup"><span data-stu-id="ddd93-136">Inserts multiple table rows, possibly replacing existing rows.</span></span>  <br/> |
|[<span data-ttu-id="ddd93-137">хрделетеровс</span><span class="sxs-lookup"><span data-stu-id="ddd93-137">HrDeleteRows</span></span>](itabledata-hrdeleterows.md) <br/> |<span data-ttu-id="ddd93-138">Удаляет несколько строк таблицы.</span><span class="sxs-lookup"><span data-stu-id="ddd93-138">Deletes multiple table rows.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ddd93-139">Примечания</span><span class="sxs-lookup"><span data-stu-id="ddd93-139">Remarks</span></span>

<span data-ttu-id="ddd93-140">Реализация **итабледата** в MAPI работает с таблицами, сохраняя все данные и все связанные с ними ограничения в памяти, делая их неприемлемыми для использования с очень большими таблицами.</span><span class="sxs-lookup"><span data-stu-id="ddd93-140">The MAPI implementation of **ITableData** works with tables by holding all of the data and any associated restrictions in memory, making it unsuitable for use with very large tables.</span></span> <span data-ttu-id="ddd93-141">Большие ограничения и сложные операции, такие как категоризация, не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="ddd93-141">Large restrictions and complex operations such as categorization are not supported.</span></span> 
  
<span data-ttu-id="ddd93-142">Табличные объекты данных идентифицируют строки, используя столбец индекса, свойство, которое гарантированно имеет уникальное значение для каждой строки.</span><span class="sxs-lookup"><span data-stu-id="ddd93-142">Table data objects identify rows by using an index column, a property that is guaranteed to have a unique value for each row.</span></span> <span data-ttu-id="ddd93-143">Большинство поставщиков услуг используют свойство **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) в качестве столбца индекса.</span><span class="sxs-lookup"><span data-stu-id="ddd93-143">Most service providers use the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property as the index column.</span></span> <span data-ttu-id="ddd93-144">Свойства с несколькими значениями не могут использоваться в качестве столбцов индекса.</span><span class="sxs-lookup"><span data-stu-id="ddd93-144">Properties that have multiple values cannot be used as an index column.</span></span>
  
<span data-ttu-id="ddd93-145">Объекты табличных данных создают одно уведомление независимо от количества строк, затронутых изменением или удалением.</span><span class="sxs-lookup"><span data-stu-id="ddd93-145">Table data objects generate a single notification regardless of the number of rows affected by a change or deletion.</span></span> <span data-ttu-id="ddd93-146">Если целевая строка в операции не существует, добавляется строка.</span><span class="sxs-lookup"><span data-stu-id="ddd93-146">If a target row in an operation does not exist, a row is added.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ddd93-147">См. также</span><span class="sxs-lookup"><span data-stu-id="ddd93-147">See also</span></span>



[<span data-ttu-id="ddd93-148">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="ddd93-148">MAPI Interfaces</span></span>](mapi-interfaces.md)

