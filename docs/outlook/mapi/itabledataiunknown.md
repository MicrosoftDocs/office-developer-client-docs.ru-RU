---
title: ITableData IUnknown
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
ms.openlocfilehash: bec68568b30bdc3112493a656de591f222801e46
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586244"
---
# <a name="itabledata--iunknown"></a><span data-ttu-id="a124d-103">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a124d-103">ITableData : IUnknown</span></span>

  
  
<span data-ttu-id="a124d-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a124d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a124d-105">Обеспечивает вспомогательные методы для работы с таблицами.</span><span class="sxs-lookup"><span data-stu-id="a124d-105">Provides utility methods for working with tables.</span></span> <span data-ttu-id="a124d-106">MAPI предоставляет таблицы данных объектов или объектов, которые реализуют **ITableData** для поставщиков услуг проводите обслуживание в таблице.</span><span class="sxs-lookup"><span data-stu-id="a124d-106">MAPI provides table data objects or objects that implement **ITableData** to help service providers perform table maintenance.</span></span> <span data-ttu-id="a124d-107">Чтобы получить объект данных в таблице, поставщиков услуг вызовите функцию [CreateTable](createtable.md) .</span><span class="sxs-lookup"><span data-stu-id="a124d-107">To obtain a table data object, service providers call the [CreateTable](createtable.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a124d-108">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="a124d-108">Header file:</span></span>  <br/> |<span data-ttu-id="a124d-109">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="a124d-109">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="a124d-110">Предоставляемые:</span><span class="sxs-lookup"><span data-stu-id="a124d-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="a124d-111">Объекты данных в таблице</span><span class="sxs-lookup"><span data-stu-id="a124d-111">Table data objects</span></span>  <br/> |
|<span data-ttu-id="a124d-112">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="a124d-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="a124d-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="a124d-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="a124d-114">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="a124d-114">Called by:</span></span>  <br/> |<span data-ttu-id="a124d-115">Поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="a124d-115">Service providers</span></span>  <br/> |
|<span data-ttu-id="a124d-116">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="a124d-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="a124d-117">IID_IMAPITableData</span><span class="sxs-lookup"><span data-stu-id="a124d-117">IID_IMAPITableData</span></span>  <br/> |
|<span data-ttu-id="a124d-118">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="a124d-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="a124d-119">LPTABLEDATA</span><span class="sxs-lookup"><span data-stu-id="a124d-119">LPTABLEDATA</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="a124d-120">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="a124d-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="a124d-121">HrGetView</span><span class="sxs-lookup"><span data-stu-id="a124d-121">HrGetView</span></span>](itabledata-hrgetview.md) <br/> |<span data-ttu-id="a124d-122">Создание нового представления таблицы, возвращает указатель на реализацию [IMAPITable](imapitableiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="a124d-122">Creates a table view, returning a pointer to an [IMAPITable](imapitableiunknown.md) implementation.</span></span>  <br/> |
|[<span data-ttu-id="a124d-123">HrModifyRow</span><span class="sxs-lookup"><span data-stu-id="a124d-123">HrModifyRow</span></span>](itabledata-hrmodifyrow.md) <br/> |<span data-ttu-id="a124d-124">Добавление новой строки в таблице, возможно заменить существующую строку.</span><span class="sxs-lookup"><span data-stu-id="a124d-124">Inserts a new table row, possibly replacing an existing row.</span></span>  <br/> |
|[<span data-ttu-id="a124d-125">HrDeleteRow</span><span class="sxs-lookup"><span data-stu-id="a124d-125">HrDeleteRow</span></span>](itabledata-hrdeleterow.md) <br/> |<span data-ttu-id="a124d-126">Удаляет строку в таблице.</span><span class="sxs-lookup"><span data-stu-id="a124d-126">Deletes a table row.</span></span>  <br/> |
|[<span data-ttu-id="a124d-127">HrQueryRow</span><span class="sxs-lookup"><span data-stu-id="a124d-127">HrQueryRow</span></span>](itabledata-hrqueryrow.md) <br/> |<span data-ttu-id="a124d-128">Получает строку таблицы.</span><span class="sxs-lookup"><span data-stu-id="a124d-128">Retrieves a table row.</span></span>  <br/> |
|[<span data-ttu-id="a124d-129">HrEnumRow</span><span class="sxs-lookup"><span data-stu-id="a124d-129">HrEnumRow</span></span>](itabledata-hrenumrow.md) <br/> |<span data-ttu-id="a124d-130">Получает строку на основе его расположения в таблице.</span><span class="sxs-lookup"><span data-stu-id="a124d-130">Retrieves a row based on its position in the table.</span></span>  <br/> |
|[<span data-ttu-id="a124d-131">HrNotify</span><span class="sxs-lookup"><span data-stu-id="a124d-131">HrNotify</span></span>](itabledata-hrnotify.md) <br/> |<span data-ttu-id="a124d-132">Отправляет уведомления для строки в таблице.</span><span class="sxs-lookup"><span data-stu-id="a124d-132">Sends a notification for a table row.</span></span>  <br/> |
|[<span data-ttu-id="a124d-133">HrInsertRow</span><span class="sxs-lookup"><span data-stu-id="a124d-133">HrInsertRow</span></span>](itabledata-hrinsertrow.md) <br/> |<span data-ttu-id="a124d-134">Вставляет строку в таблице.</span><span class="sxs-lookup"><span data-stu-id="a124d-134">Inserts a table row.</span></span>  <br/> |
|[<span data-ttu-id="a124d-135">HrModifyRows</span><span class="sxs-lookup"><span data-stu-id="a124d-135">HrModifyRows</span></span>](itabledata-hrmodifyrows.md) <br/> |<span data-ttu-id="a124d-136">Вставка нескольких строк таблицы, возможно замена существующих строк.</span><span class="sxs-lookup"><span data-stu-id="a124d-136">Inserts multiple table rows, possibly replacing existing rows.</span></span>  <br/> |
|[<span data-ttu-id="a124d-137">HrDeleteRows</span><span class="sxs-lookup"><span data-stu-id="a124d-137">HrDeleteRows</span></span>](itabledata-hrdeleterows.md) <br/> |<span data-ttu-id="a124d-138">Удаление нескольких строк таблицы.</span><span class="sxs-lookup"><span data-stu-id="a124d-138">Deletes multiple table rows.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a124d-139">Замечания</span><span class="sxs-lookup"><span data-stu-id="a124d-139">Remarks</span></span>

<span data-ttu-id="a124d-140">Реализация интерфейса MAPI **ITableData** работает с таблицами, удерживая любые связанные ограничений и все данные в память, что подходит для использования с очень большой таблицы.</span><span class="sxs-lookup"><span data-stu-id="a124d-140">The MAPI implementation of **ITableData** works with tables by holding all of the data and any associated restrictions in memory, making it unsuitable for use with very large tables.</span></span> <span data-ttu-id="a124d-141">Сложные операции, такие как категоризации и больших ограничения не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a124d-141">Large restrictions and complex operations such as categorization are not supported.</span></span> 
  
<span data-ttu-id="a124d-142">Объекты данных в таблице идентификации строк с помощью столбца индекса, свойство, которое гарантированно имеет уникальное значение для каждой строки.</span><span class="sxs-lookup"><span data-stu-id="a124d-142">Table data objects identify rows by using an index column, a property that is guaranteed to have a unique value for each row.</span></span> <span data-ttu-id="a124d-143">Большинство поставщиков услуг используйте свойство **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) в столбце индекса.</span><span class="sxs-lookup"><span data-stu-id="a124d-143">Most service providers use the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property as the index column.</span></span> <span data-ttu-id="a124d-144">Свойства, которые имеют несколько значений нельзя использовать в качестве столбца индекса.</span><span class="sxs-lookup"><span data-stu-id="a124d-144">Properties that have multiple values cannot be used as an index column.</span></span>
  
<span data-ttu-id="a124d-145">Объекты данных в таблице создания одного уведомления независимо от количества строк, затронутых изменения или удаления.</span><span class="sxs-lookup"><span data-stu-id="a124d-145">Table data objects generate a single notification regardless of the number of rows affected by a change or deletion.</span></span> <span data-ttu-id="a124d-146">Если в целевой строке в рамках одной операции не существует, добавлении строки.</span><span class="sxs-lookup"><span data-stu-id="a124d-146">If a target row in an operation does not exist, a row is added.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a124d-147">См. также</span><span class="sxs-lookup"><span data-stu-id="a124d-147">See also</span></span>



[<span data-ttu-id="a124d-148">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="a124d-148">MAPI Interfaces</span></span>](mapi-interfaces.md)

