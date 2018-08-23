---
title: TABLE_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.TABLE_NOTIFICATION
api_type:
- COM
ms.assetid: 48e478c4-6e9a-40ab-a7bb-e6219b743b08
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7f32145e0947411c48e1e6c3a941c9913a08709c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565846"
---
# <a name="tablenotification"></a><span data-ttu-id="3a983-103">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="3a983-103">TABLE_NOTIFICATION</span></span>

<span data-ttu-id="3a983-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3a983-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3a983-105">Описание строки в таблице, которые были затронуты некоторые тип события, например, изменения или ошибка.</span><span class="sxs-lookup"><span data-stu-id="3a983-105">Describes a row in a table that has been affected by some type of event, such as a change or an error.</span></span> <span data-ttu-id="3a983-106">В этом случае уведомление о таблице был создан.</span><span class="sxs-lookup"><span data-stu-id="3a983-106">This causes a table notification to be generated.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3a983-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="3a983-107">Header file:</span></span>  <br/> |<span data-ttu-id="3a983-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3a983-108">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _TABLE_NOTIFICATION
{
  ULONG ulTableEvent;
  HRESULT hResult;
  SPropValue propIndex;
  SPropValue propPrior;
  SRow row;
} TABLE_NOTIFICATION;

```

## <a name="members"></a><span data-ttu-id="3a983-109">Members</span><span class="sxs-lookup"><span data-stu-id="3a983-109">Members</span></span>

<span data-ttu-id="3a983-110">**ulTableEvent**</span><span class="sxs-lookup"><span data-stu-id="3a983-110">**ulTableEvent**</span></span>
  
> <span data-ttu-id="3a983-111">Битовая маска флаги, используемые для представления типа события по таблице.</span><span class="sxs-lookup"><span data-stu-id="3a983-111">Bitmask of flags used to represent the table event type.</span></span> <span data-ttu-id="3a983-112">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="3a983-112">The following flags can be set:</span></span>
    
<span data-ttu-id="3a983-113">TABLE_CHANGED</span><span class="sxs-lookup"><span data-stu-id="3a983-113">TABLE_CHANGED</span></span> 
  
> <span data-ttu-id="3a983-114">Указывает, что что-то о таблице был изменен на высоком уровне.</span><span class="sxs-lookup"><span data-stu-id="3a983-114">Indicates at a high level that something about the table has changed.</span></span> <span data-ttu-id="3a983-115">В таблице состояния — как до события.</span><span class="sxs-lookup"><span data-stu-id="3a983-115">The table's state is as it was before the event.</span></span> <span data-ttu-id="3a983-116">Это означает, что все свойства **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), закладки, текущее расположение и выбранные элементы интерфейса пользователя еще не истек.</span><span class="sxs-lookup"><span data-stu-id="3a983-116">This means that all **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) properties, bookmarks, current positioning, and user interface selections are still valid.</span></span> <span data-ttu-id="3a983-117">Это событие обрабатывается путем повторного считывания в таблице.</span><span class="sxs-lookup"><span data-stu-id="3a983-117">Handle this event by rereading the table.</span></span> <span data-ttu-id="3a983-118">Поставщики услуг, которые не требуется реализовать расширенный таблице уведомлений отправлять события TABLE_CHANGED, а не более подробные события, чтобы указать определенный тип изменения.</span><span class="sxs-lookup"><span data-stu-id="3a983-118">Service providers that do not want to implement rich table notifications send TABLE_CHANGED events instead of more detailed events to indicate a particular type of change.</span></span> 
    
<span data-ttu-id="3a983-119">TABLE_ERROR</span><span class="sxs-lookup"><span data-stu-id="3a983-119">TABLE_ERROR</span></span> 
  
> <span data-ttu-id="3a983-120">Обычно во время выполнения асинхронной операции произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="3a983-120">An error has occurred, usually during the processing of an asynchronous operation.</span></span> <span data-ttu-id="3a983-121">Ошибки во время обработки из следующих методов можно создать это событие:</span><span class="sxs-lookup"><span data-stu-id="3a983-121">Errors during the processing of the following methods can generate this event:</span></span> 
    
   - [<span data-ttu-id="3a983-122">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="3a983-122">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
    
   - [<span data-ttu-id="3a983-123">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="3a983-123">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
    
   - [<span data-ttu-id="3a983-124">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="3a983-124">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
    
   <span data-ttu-id="3a983-125">После получения события TABLE_ERROR, клиент не может полагаться на точность содержимое таблицы.</span><span class="sxs-lookup"><span data-stu-id="3a983-125">After receiving a TABLE_ERROR event, a client cannot rely on the accuracy of the table contents.</span></span> <span data-ttu-id="3a983-126">Кроме того ожидающие уведомления о другие изменения могут быть потеряны.</span><span class="sxs-lookup"><span data-stu-id="3a983-126">Also, pending notifications about other changes might be lost.</span></span> <span data-ttu-id="3a983-127">Метод [IMAPITable::GetLastError](imapitable-getlasterror.md) не может предоставить любые дополнительные сведения об ошибке, так как он был создан в некоторых предыдущих точке, не обязательно последнего вызова метода.</span><span class="sxs-lookup"><span data-stu-id="3a983-127">The [IMAPITable::GetLastError](imapitable-getlasterror.md) method might not provide any additional information about the error because it was generated at some previous point, not necessarily from the last method call.</span></span> 
    
<span data-ttu-id="3a983-128">TABLE_RELOAD</span><span class="sxs-lookup"><span data-stu-id="3a983-128">TABLE_RELOAD</span></span> 
  
> <span data-ttu-id="3a983-129">Следует перезагрузить данных в таблице.</span><span class="sxs-lookup"><span data-stu-id="3a983-129">The data in the table should be reloaded.</span></span> <span data-ttu-id="3a983-130">Поставщиков услуг отправить TABLE_RELOAD при, например, базовые данные хранятся в базе данных и базы данных будет заменен.</span><span class="sxs-lookup"><span data-stu-id="3a983-130">Service providers send TABLE_RELOAD when, for example, the underlying data is stored in a database and the database is replaced.</span></span> <span data-ttu-id="3a983-131">Обработайте это событие, если предполагается, что ничего о таблице не остаются действительными и повторного чтения в таблице.</span><span class="sxs-lookup"><span data-stu-id="3a983-131">Handle this event by assuming that nothing about the table is still valid and by rereading the table.</span></span> <span data-ttu-id="3a983-132">Все закладки, ключи экземпляра, состояние и данные размещения являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="3a983-132">All bookmarks, instance keys, status and positioning information are invalid.</span></span>
    
<span data-ttu-id="3a983-133">TABLE_RESTRICT_DONE</span><span class="sxs-lookup"><span data-stu-id="3a983-133">TABLE_RESTRICT_DONE</span></span> 
  
> <span data-ttu-id="3a983-134">Ограничение операции, инициированные с для вызова метода **IMAPITable::Restrict** завершена.</span><span class="sxs-lookup"><span data-stu-id="3a983-134">A restriction operation initiated with an **IMAPITable::Restrict** method call has completed.</span></span> 
    
<span data-ttu-id="3a983-135">TABLE_ROW_ADDED</span><span class="sxs-lookup"><span data-stu-id="3a983-135">TABLE_ROW_ADDED</span></span> 
  
> <span data-ttu-id="3a983-136">В таблице и соответствующего объекта сохранен добавлен новую строку.</span><span class="sxs-lookup"><span data-stu-id="3a983-136">A new row has been added to the table and the corresponding object saved.</span></span> <span data-ttu-id="3a983-137">События TABLE_ROW_ADDED создаются после вызова метода [IMAPIProp::SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="3a983-137">TABLE_ROW_ADDED events are generated after a call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
    
<span data-ttu-id="3a983-138">TABLE_ROW_DELETED</span><span class="sxs-lookup"><span data-stu-id="3a983-138">TABLE_ROW_DELETED</span></span> 
  
> <span data-ttu-id="3a983-139">Строка удалена из таблицы.</span><span class="sxs-lookup"><span data-stu-id="3a983-139">A row has been removed from the table.</span></span> <span data-ttu-id="3a983-140">Член **propPrior** имеет значение NULL.</span><span class="sxs-lookup"><span data-stu-id="3a983-140">The **propPrior** member is set to NULL.</span></span> 
    
<span data-ttu-id="3a983-141">TABLE_ROW_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="3a983-141">TABLE_ROW_MODIFIED</span></span> 
  
> <span data-ttu-id="3a983-142">Строка была изменена.</span><span class="sxs-lookup"><span data-stu-id="3a983-142">A row has been changed.</span></span> <span data-ttu-id="3a983-143">Элемент **строки** содержит указанные свойства для строки.</span><span class="sxs-lookup"><span data-stu-id="3a983-143">The **row** member contains the affected properties for the row.</span></span> <span data-ttu-id="3a983-144">Несколько событий TABLE_ROW_MODIFIED, передаются в том порядке, в котором они отображаются в табличном представлении.</span><span class="sxs-lookup"><span data-stu-id="3a983-144">Multiple TABLE_ROW_MODIFIED events are sent in the order that they appear in the table view.</span></span> 
    
  <span data-ttu-id="3a983-145">События TABLE_ROW_MODIFIED отправляются после изменения для соответствующего объекта, выполненные с помощью вызова метода **IMAPIProp::SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="3a983-145">TABLE_ROW_MODIFIED events are sent after changes to the corresponding object have been committed with a call to the **IMAPIProp::SaveChanges** method.</span></span> <span data-ttu-id="3a983-146">Если измененной строки теперь первой строки в таблице, значение свойства тега в элемент **propPrior** — **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3a983-146">If the modified row is now the first row in the table, the value of the property tag in the **propPrior** member is **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).</span></span>
    
<span data-ttu-id="3a983-147">TABLE_SETCOL_DONE</span><span class="sxs-lookup"><span data-stu-id="3a983-147">TABLE_SETCOL_DONE</span></span> 
  
> <span data-ttu-id="3a983-148">Завершения операции параметр столбца, инициированных с для вызова метода **IMAPITable::SetColumns** .</span><span class="sxs-lookup"><span data-stu-id="3a983-148">A column setting operation initiated with an **IMAPITable::SetColumns** method call has completed.</span></span> 
    
<span data-ttu-id="3a983-149">TABLE_SORT_DONE</span><span class="sxs-lookup"><span data-stu-id="3a983-149">TABLE_SORT_DONE</span></span> 
  
> <span data-ttu-id="3a983-150">Таблица сортировки операции, инициированные с для вызова метода **IMAPITable::SortTable** завершена.</span><span class="sxs-lookup"><span data-stu-id="3a983-150">A table sorting operation initiated with an **IMAPITable::SortTable** method call has completed.</span></span> 
    
<span data-ttu-id="3a983-151">**hResult**</span><span class="sxs-lookup"><span data-stu-id="3a983-151">**hResult**</span></span>
  
> <span data-ttu-id="3a983-152">Значение HRESULT для произошедшей ошибки, если член **ulTableEvent** задано значение TABLE_ERROR.</span><span class="sxs-lookup"><span data-stu-id="3a983-152">HRESULT value for the error that has occurred, if the **ulTableEvent** member is set to TABLE_ERROR.</span></span> 
    
<span data-ttu-id="3a983-153">**propIndex**</span><span class="sxs-lookup"><span data-stu-id="3a983-153">**propIndex**</span></span>
  
> <span data-ttu-id="3a983-154">Структура [SPropValue](spropvalue.md) для свойства **PR_INSTANCE_KEY** затронутых строки.</span><span class="sxs-lookup"><span data-stu-id="3a983-154">[SPropValue](spropvalue.md) structure for the **PR_INSTANCE_KEY** property of the affected row.</span></span> 
    
<span data-ttu-id="3a983-155">**propPrior**</span><span class="sxs-lookup"><span data-stu-id="3a983-155">**propPrior**</span></span>
  
> <span data-ttu-id="3a983-156">Структура **SPropValue** для свойства **PR_INSTANCE_KEY** строки перед затронутых проектом.</span><span class="sxs-lookup"><span data-stu-id="3a983-156">**SPropValue** structure for the **PR_INSTANCE_KEY** property of the row before the affected one.</span></span> <span data-ttu-id="3a983-157">При первой строки в таблице, затронутых строку **propPrior** должен иметь значение **PR_NULL** и не нулю.</span><span class="sxs-lookup"><span data-stu-id="3a983-157">If the affected row is the first row in the table, **propPrior** must be set to **PR_NULL** and not zero.</span></span> <span data-ttu-id="3a983-158">Нулевой не является допустимым свойством тегом.</span><span class="sxs-lookup"><span data-stu-id="3a983-158">Zero is not a valid property tag.</span></span> 
    
<span data-ttu-id="3a983-159">**row**</span><span class="sxs-lookup"><span data-stu-id="3a983-159">**row**</span></span>
  
> <span data-ttu-id="3a983-160">Структура [SRow](srow.md) , описывающее затронутых строк.</span><span class="sxs-lookup"><span data-stu-id="3a983-160">[SRow](srow.md) structure describing the affected row.</span></span> <span data-ttu-id="3a983-161">Эта структура заполняется для всех событий уведомлений в таблице.</span><span class="sxs-lookup"><span data-stu-id="3a983-161">This structure is filled for all table notification events.</span></span> <span data-ttu-id="3a983-162">Для события уведомления в таблице, которые не передачи данных строки член **cValues** структуры **SRow** присваивается нулевое значение и член **lpProps** имеет значение NULL.</span><span class="sxs-lookup"><span data-stu-id="3a983-162">For table notification events that do not pass row data, the **cValues** member of the **SRow** structure is set to zero and the **lpProps** member is set to NULL.</span></span> <span data-ttu-id="3a983-163">Поскольку эта структура **SRow** доступен только для чтения; Клиенты необходимо принять его копию, если требуется внести изменения.</span><span class="sxs-lookup"><span data-stu-id="3a983-163">Because this **SRow** structure is read-only; clients must make a copy of it if they want to make modifications.</span></span> <span data-ttu-id="3a983-164">Функция [ScDupPropset](scduppropset.md) можно использовать для создания копии.</span><span class="sxs-lookup"><span data-stu-id="3a983-164">The [ScDupPropset](scduppropset.md) function can be used to make the copy.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="3a983-165">Замечания</span><span class="sxs-lookup"><span data-stu-id="3a983-165">Remarks</span></span>

<span data-ttu-id="3a983-166">**Таблица\_уведомления** структуры — это один из участников объединение структуры, включенные в элемент **info** структуры [УВЕДОМЛЕНИЙ](notification.md) .</span><span class="sxs-lookup"><span data-stu-id="3a983-166">The **TABLE\_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="3a983-167">Член **информация** включает в себя **в ТАБЛИЦЕ\_уведомления** структуры, если член **ulEventType** структуры равен _fnevTableModified_.</span><span class="sxs-lookup"><span data-stu-id="3a983-167">The **info** member includes a **TABLE\_NOTIFICATION** structure when the **ulEventType** member of the structure is set to  _fnevTableModified_.</span></span>
  
<span data-ttu-id="3a983-168">Порядок и типы столбцов в элемент строки отражают порядок и тип, который был фактически во время создания уведомления.</span><span class="sxs-lookup"><span data-stu-id="3a983-168">The order and type of columns in the row member reflect the order and type that was in effect at the time that the notification was generated.</span></span> <span data-ttu-id="3a983-169">Порядок и тип во время создания уведомления не обязательно то же, что при доставке уведомления.</span><span class="sxs-lookup"><span data-stu-id="3a983-169">The order and type at the time that the notification was generated is not necessarily the same as when the notification was delivered.</span></span> 
  
<span data-ttu-id="3a983-170">Дополнительные сведения о уведомлений видеть темы, описанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="3a983-170">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="3a983-171">**Статья**</span><span class="sxs-lookup"><span data-stu-id="3a983-171">**Topic**</span></span>|<span data-ttu-id="3a983-172">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3a983-172">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3a983-173">Уведомление о событиях в MAPI</span><span class="sxs-lookup"><span data-stu-id="3a983-173">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="3a983-174">Общий обзор уведомлений и события уведомления.</span><span class="sxs-lookup"><span data-stu-id="3a983-174">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="3a983-175">Обработка уведомлений</span><span class="sxs-lookup"><span data-stu-id="3a983-175">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="3a983-176">Обсуждение как клиенты должны обрабатывать уведомления.</span><span class="sxs-lookup"><span data-stu-id="3a983-176">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="3a983-177">Поддержка уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="3a983-177">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="3a983-178">Обсуждение того, как поставщиков услуг можно использовать метод **IMAPISupport** для создания уведомлений.</span><span class="sxs-lookup"><span data-stu-id="3a983-178">Discussion of how service providers can use the **IMAPISupport** method to generate notifications.</span></span>  <br/> |
   
<span data-ttu-id="3a983-179">Так как уведомления в таблице является асинхронным, клиенты могут получать уведомления о добавленной строки после обучению работе с добавлением по-другому.</span><span class="sxs-lookup"><span data-stu-id="3a983-179">Because table notifications are asynchronous, clients can receive notification of an added row after learning about the addition through another means.</span></span> <span data-ttu-id="3a983-180">Существует возможность получения TABLE_ERROR события, при наличии ошибки в методе **IMAPITable::Sort**, **IMAPITable::Restrict**или **IMAPITable::SetColumns** или при основной процесс пытается обновить таблицу в организации, например, новый или измененные строки.</span><span class="sxs-lookup"><span data-stu-id="3a983-180">It is possible to receive a TABLE_ERROR event when there is an error in an **IMAPITable::Sort**, **IMAPITable::Restrict**, or **IMAPITable::SetColumns** method or when an underlying process attempts to update a table with, for example, new or modified rows.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3a983-181">См. также</span><span class="sxs-lookup"><span data-stu-id="3a983-181">See also</span></span>

- [<span data-ttu-id="3a983-182">�����������</span><span class="sxs-lookup"><span data-stu-id="3a983-182">NOTIFICATION</span></span>](notification.md) 
- [<span data-ttu-id="3a983-183">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="3a983-183">ScDupPropset</span></span>](scduppropset.md)
- [<span data-ttu-id="3a983-184">SRow</span><span class="sxs-lookup"><span data-stu-id="3a983-184">SRow</span></span>](srow.md)
- [<span data-ttu-id="3a983-185">SPropValue</span><span class="sxs-lookup"><span data-stu-id="3a983-185">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="3a983-186">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="3a983-186">MAPI Structures</span></span>](mapi-structures.md)

