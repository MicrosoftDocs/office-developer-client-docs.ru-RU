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
ms.openlocfilehash: 6c35220529fb88b470c563a0b004bfcf7e63ef76
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415959"
---
# <a name="table_notification"></a><span data-ttu-id="88082-103">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="88082-103">TABLE_NOTIFICATION</span></span>

<span data-ttu-id="88082-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="88082-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="88082-105">Описывает строку в таблице, на которую повлияло какое-либо событие, например изменение или ошибка.</span><span class="sxs-lookup"><span data-stu-id="88082-105">Describes a row in a table that has been affected by some type of event, such as a change or an error.</span></span> <span data-ttu-id="88082-106">Это приводит к сгенерированию уведомления таблицы.</span><span class="sxs-lookup"><span data-stu-id="88082-106">This causes a table notification to be generated.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="88082-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="88082-107">Header file:</span></span>  <br/> |<span data-ttu-id="88082-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="88082-108">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="88082-109">"Участники"</span><span class="sxs-lookup"><span data-stu-id="88082-109">Members</span></span>

<span data-ttu-id="88082-110">**ulTableEvent**</span><span class="sxs-lookup"><span data-stu-id="88082-110">**ulTableEvent**</span></span>
  
> <span data-ttu-id="88082-111">Bitmask флагов, используемых для представления типа события таблицы.</span><span class="sxs-lookup"><span data-stu-id="88082-111">Bitmask of flags used to represent the table event type.</span></span> <span data-ttu-id="88082-112">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="88082-112">The following flags can be set:</span></span>
    
<span data-ttu-id="88082-113">TABLE_CHANGED</span><span class="sxs-lookup"><span data-stu-id="88082-113">TABLE_CHANGED</span></span> 
  
> <span data-ttu-id="88082-114">Указывает на высоком уровне, что что-то в таблице изменилось.</span><span class="sxs-lookup"><span data-stu-id="88082-114">Indicates at a high level that something about the table has changed.</span></span> <span data-ttu-id="88082-115">Состояние таблицы так же, как и до события.</span><span class="sxs-lookup"><span data-stu-id="88082-115">The table's state is as it was before the event.</span></span> <span data-ttu-id="88082-116">Это означает, **что все свойства PR_INSTANCE_KEY** [(PidTagInstanceKey),](pidtaginstancekey-canonical-property.md)закладки, текущее позиционирование и выбор пользовательского интерфейса по-прежнему действительны.</span><span class="sxs-lookup"><span data-stu-id="88082-116">This means that all **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) properties, bookmarks, current positioning, and user interface selections are still valid.</span></span> <span data-ttu-id="88082-117">Обработать это событие, перечитав таблицу.</span><span class="sxs-lookup"><span data-stu-id="88082-117">Handle this event by rereading the table.</span></span> <span data-ttu-id="88082-118">Поставщики услуг, которые не хотят внедрять уведомления с богатой таблицей, отправляют TABLE_CHANGED события, а не более подробные события, чтобы указать определенный тип изменений.</span><span class="sxs-lookup"><span data-stu-id="88082-118">Service providers that do not want to implement rich table notifications send TABLE_CHANGED events instead of more detailed events to indicate a particular type of change.</span></span> 
    
<span data-ttu-id="88082-119">TABLE_ERROR</span><span class="sxs-lookup"><span data-stu-id="88082-119">TABLE_ERROR</span></span> 
  
> <span data-ttu-id="88082-120">Ошибка произошла, как правило, во время обработки асинхронной операции.</span><span class="sxs-lookup"><span data-stu-id="88082-120">An error has occurred, usually during the processing of an asynchronous operation.</span></span> <span data-ttu-id="88082-121">Ошибки при обработке следующих методов могут создавать это событие:</span><span class="sxs-lookup"><span data-stu-id="88082-121">Errors during the processing of the following methods can generate this event:</span></span> 
    
   - [<span data-ttu-id="88082-122">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="88082-122">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
    
   - [<span data-ttu-id="88082-123">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="88082-123">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
    
   - [<span data-ttu-id="88082-124">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="88082-124">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
    
   <span data-ttu-id="88082-125">После получения события TABLE_ERROR клиент не может полагаться на точность содержимого таблицы.</span><span class="sxs-lookup"><span data-stu-id="88082-125">After receiving a TABLE_ERROR event, a client cannot rely on the accuracy of the table contents.</span></span> <span data-ttu-id="88082-126">Кроме того, могут быть потеряны ожидающих уведомлений о других изменениях.</span><span class="sxs-lookup"><span data-stu-id="88082-126">Also, pending notifications about other changes might be lost.</span></span> <span data-ttu-id="88082-127">Метод [IMAPITable::GetLastError](imapitable-getlasterror.md) может не предоставлять дополнительные сведения об ошибке, так как она была сгенерирована в какой-либо предыдущей точке, не обязательно из последнего вызова метода.</span><span class="sxs-lookup"><span data-stu-id="88082-127">The [IMAPITable::GetLastError](imapitable-getlasterror.md) method might not provide any additional information about the error because it was generated at some previous point, not necessarily from the last method call.</span></span> 
    
<span data-ttu-id="88082-128">TABLE_RELOAD</span><span class="sxs-lookup"><span data-stu-id="88082-128">TABLE_RELOAD</span></span> 
  
> <span data-ttu-id="88082-129">Данные в таблице должны быть перезагружены.</span><span class="sxs-lookup"><span data-stu-id="88082-129">The data in the table should be reloaded.</span></span> <span data-ttu-id="88082-130">Поставщики услуг отправляют TABLE_RELOAD, когда, например, в базе данных хранятся данные, а база данных заменяется.</span><span class="sxs-lookup"><span data-stu-id="88082-130">Service providers send TABLE_RELOAD when, for example, the underlying data is stored in a database and the database is replaced.</span></span> <span data-ttu-id="88082-131">Справься с этим событием, если предположить, что ничего не имеется в таблице, и перечитыв таблицу.</span><span class="sxs-lookup"><span data-stu-id="88082-131">Handle this event by assuming that nothing about the table is still valid and by rereading the table.</span></span> <span data-ttu-id="88082-132">Все закладки, ключи экземпляра, сведения о состоянии и позиционировании являются недействительными.</span><span class="sxs-lookup"><span data-stu-id="88082-132">All bookmarks, instance keys, status and positioning information are invalid.</span></span>
    
<span data-ttu-id="88082-133">TABLE_RESTRICT_DONE</span><span class="sxs-lookup"><span data-stu-id="88082-133">TABLE_RESTRICT_DONE</span></span> 
  
> <span data-ttu-id="88082-134">Операция ограничения, начатая с помощью **вызова метода IMAPITable::Restrict,** завершена.</span><span class="sxs-lookup"><span data-stu-id="88082-134">A restriction operation initiated with an **IMAPITable::Restrict** method call has completed.</span></span> 
    
<span data-ttu-id="88082-135">TABLE_ROW_ADDED</span><span class="sxs-lookup"><span data-stu-id="88082-135">TABLE_ROW_ADDED</span></span> 
  
> <span data-ttu-id="88082-136">В таблицу добавлена новая строка и сохранен соответствующий объект.</span><span class="sxs-lookup"><span data-stu-id="88082-136">A new row has been added to the table and the corresponding object saved.</span></span> <span data-ttu-id="88082-137">TABLE_ROW_ADDED события создаются после вызова метода [IMAPIProp::SaveChanges.](imapiprop-savechanges.md)</span><span class="sxs-lookup"><span data-stu-id="88082-137">TABLE_ROW_ADDED events are generated after a call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
    
<span data-ttu-id="88082-138">TABLE_ROW_DELETED</span><span class="sxs-lookup"><span data-stu-id="88082-138">TABLE_ROW_DELETED</span></span> 
  
> <span data-ttu-id="88082-139">Строка удалена из таблицы.</span><span class="sxs-lookup"><span data-stu-id="88082-139">A row has been removed from the table.</span></span> <span data-ttu-id="88082-140">Для **участника propPrior** установлено NULL.</span><span class="sxs-lookup"><span data-stu-id="88082-140">The **propPrior** member is set to NULL.</span></span> 
    
<span data-ttu-id="88082-141">TABLE_ROW_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="88082-141">TABLE_ROW_MODIFIED</span></span> 
  
> <span data-ttu-id="88082-142">Строка изменена.</span><span class="sxs-lookup"><span data-stu-id="88082-142">A row has been changed.</span></span> <span data-ttu-id="88082-143">Член **строки** содержит затронутые свойства строки.</span><span class="sxs-lookup"><span data-stu-id="88082-143">The **row** member contains the affected properties for the row.</span></span> <span data-ttu-id="88082-144">Несколько TABLE_ROW_MODIFIED отправляются в том порядке, в который они отображаются в представлении таблицы.</span><span class="sxs-lookup"><span data-stu-id="88082-144">Multiple TABLE_ROW_MODIFIED events are sent in the order that they appear in the table view.</span></span> 
    
  <span data-ttu-id="88082-145">TABLE_ROW_MODIFIED события отправляются после внесения изменений в соответствующий объект с вызовом метода **IMAPIProp::SaveChanges.**</span><span class="sxs-lookup"><span data-stu-id="88082-145">TABLE_ROW_MODIFIED events are sent after changes to the corresponding object have been committed with a call to the **IMAPIProp::SaveChanges** method.</span></span> <span data-ttu-id="88082-146">Если измененная строка теперь является первой строкой в таблице, значение тега свойства в **члене** **propPrior** PR_NULL [(PidTagNull).](pidtagnull-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="88082-146">If the modified row is now the first row in the table, the value of the property tag in the **propPrior** member is **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).</span></span>
    
<span data-ttu-id="88082-147">TABLE_SETCOL_DONE</span><span class="sxs-lookup"><span data-stu-id="88082-147">TABLE_SETCOL_DONE</span></span> 
  
> <span data-ttu-id="88082-148">Операция настройки столбцов, начатая с помощью **вызова метода IMAPITable::SetColumns,** завершена.</span><span class="sxs-lookup"><span data-stu-id="88082-148">A column setting operation initiated with an **IMAPITable::SetColumns** method call has completed.</span></span> 
    
<span data-ttu-id="88082-149">TABLE_SORT_DONE</span><span class="sxs-lookup"><span data-stu-id="88082-149">TABLE_SORT_DONE</span></span> 
  
> <span data-ttu-id="88082-150">Операция сортировки таблиц, начатая с помощью **вызова метода IMAPITable::SortTable,** завершена.</span><span class="sxs-lookup"><span data-stu-id="88082-150">A table sorting operation initiated with an **IMAPITable::SortTable** method call has completed.</span></span> 
    
<span data-ttu-id="88082-151">**hResult**</span><span class="sxs-lookup"><span data-stu-id="88082-151">**hResult**</span></span>
  
> <span data-ttu-id="88082-152">Значение HRESULT для ошибки, которая произошла, если для члена **ulTableEvent** установлено значение TABLE_ERROR.</span><span class="sxs-lookup"><span data-stu-id="88082-152">HRESULT value for the error that has occurred, if the **ulTableEvent** member is set to TABLE_ERROR.</span></span> 
    
<span data-ttu-id="88082-153">**propIndex**</span><span class="sxs-lookup"><span data-stu-id="88082-153">**propIndex**</span></span>
  
> <span data-ttu-id="88082-154">[Структура SPropValue](spropvalue.md) для **PR_INSTANCE_KEY** свойства затронутой строки.</span><span class="sxs-lookup"><span data-stu-id="88082-154">[SPropValue](spropvalue.md) structure for the **PR_INSTANCE_KEY** property of the affected row.</span></span> 
    
<span data-ttu-id="88082-155">**propPrior**</span><span class="sxs-lookup"><span data-stu-id="88082-155">**propPrior**</span></span>
  
> <span data-ttu-id="88082-156">**Структура SPropValue** для **PR_INSTANCE_KEY** свойства строки перед затрагиваемой.</span><span class="sxs-lookup"><span data-stu-id="88082-156">**SPropValue** structure for the **PR_INSTANCE_KEY** property of the row before the affected one.</span></span> <span data-ttu-id="88082-157">Если затрагиваемая строка является первой строкой в  таблице, **propPrior** должен быть PR_NULL ноль.</span><span class="sxs-lookup"><span data-stu-id="88082-157">If the affected row is the first row in the table, **propPrior** must be set to **PR_NULL** and not zero.</span></span> <span data-ttu-id="88082-158">Zero — это не допустимый тег свойства.</span><span class="sxs-lookup"><span data-stu-id="88082-158">Zero is not a valid property tag.</span></span> 
    
<span data-ttu-id="88082-159">**строка**</span><span class="sxs-lookup"><span data-stu-id="88082-159">**row**</span></span>
  
> <span data-ttu-id="88082-160">[Структура SRow](srow.md) с описанием затронутой строки.</span><span class="sxs-lookup"><span data-stu-id="88082-160">[SRow](srow.md) structure describing the affected row.</span></span> <span data-ttu-id="88082-161">Эта структура заполняется для всех событий уведомлений таблицы.</span><span class="sxs-lookup"><span data-stu-id="88082-161">This structure is filled for all table notification events.</span></span> <span data-ttu-id="88082-162">Для событий уведомлений таблицы, которые не передают данные строки, для **члена cValues** структуры **SRow** установлено значение нуля, а для **участника lpProps** — значение NULL.</span><span class="sxs-lookup"><span data-stu-id="88082-162">For table notification events that do not pass row data, the **cValues** member of the **SRow** structure is set to zero and the **lpProps** member is set to NULL.</span></span> <span data-ttu-id="88082-163">Так как **эта структура SRow** является только для чтения; клиенты должны сделать его копию, если они хотят внести изменения.</span><span class="sxs-lookup"><span data-stu-id="88082-163">Because this **SRow** structure is read-only; clients must make a copy of it if they want to make modifications.</span></span> <span data-ttu-id="88082-164">Для копирования можно использовать функцию [ScDupPropset.](scduppropset.md)</span><span class="sxs-lookup"><span data-stu-id="88082-164">The [ScDupPropset](scduppropset.md) function can be used to make the copy.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="88082-165">Примечания</span><span class="sxs-lookup"><span data-stu-id="88082-165">Remarks</span></span>

<span data-ttu-id="88082-166">Структура **\_ УВЕДОМЛЕНий TABLE** является одним из членов объединения структур, включенных в состав **информационного** члена [структуры NOTIFICATION.](notification.md)</span><span class="sxs-lookup"><span data-stu-id="88082-166">The **TABLE\_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="88082-167">Член **info** включает структуру **УВЕДОМЛЕНий \_ TABLE,** когда член **ulEventType** структуры задан  _для fnevTableModified_.</span><span class="sxs-lookup"><span data-stu-id="88082-167">The **info** member includes a **TABLE\_NOTIFICATION** structure when the **ulEventType** member of the structure is set to  _fnevTableModified_.</span></span>
  
<span data-ttu-id="88082-168">Порядок и тип столбцов в члене строки отражают порядок и тип, которые были в действительности во время получения уведомления.</span><span class="sxs-lookup"><span data-stu-id="88082-168">The order and type of columns in the row member reflect the order and type that was in effect at the time that the notification was generated.</span></span> <span data-ttu-id="88082-169">Порядок и тип на момент получения уведомления необязательно совпадают с моментом доставки уведомления.</span><span class="sxs-lookup"><span data-stu-id="88082-169">The order and type at the time that the notification was generated is not necessarily the same as when the notification was delivered.</span></span> 
  
<span data-ttu-id="88082-170">Дополнительные сведения об уведомлении см. в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="88082-170">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="88082-171">**Статья**</span><span class="sxs-lookup"><span data-stu-id="88082-171">**Topic**</span></span>|<span data-ttu-id="88082-172">**Описание**</span><span class="sxs-lookup"><span data-stu-id="88082-172">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="88082-173">Уведомление о событиях в MAPI</span><span class="sxs-lookup"><span data-stu-id="88082-173">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="88082-174">Общий обзор событий уведомлений и уведомлений.</span><span class="sxs-lookup"><span data-stu-id="88082-174">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="88082-175">Обработка уведомлений</span><span class="sxs-lookup"><span data-stu-id="88082-175">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="88082-176">Обсуждение того, как клиенты должны обрабатывать уведомления.</span><span class="sxs-lookup"><span data-stu-id="88082-176">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="88082-177">Поддержка уведомления о событиях</span><span class="sxs-lookup"><span data-stu-id="88082-177">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="88082-178">Обсуждение того, как поставщики услуг могут использовать **метод IMAPISupport** для создания уведомлений.</span><span class="sxs-lookup"><span data-stu-id="88082-178">Discussion of how service providers can use the **IMAPISupport** method to generate notifications.</span></span>  <br/> |
   
<span data-ttu-id="88082-179">Так как уведомления таблицы асинхронны, клиенты могут получать уведомления о добавленной строке после получения информации о добавлении другими средствами.</span><span class="sxs-lookup"><span data-stu-id="88082-179">Because table notifications are asynchronous, clients can receive notification of an added row after learning about the addition through another means.</span></span> <span data-ttu-id="88082-180">Можно получить событие TABLE_ERROR при ошибке в **IMAPITable::Sort,** **IMAPITable::Restrict** или **методе IMAPITable::SetColumns** или при попытке обновить таблицу с помощью, например, новых или измененных строк.</span><span class="sxs-lookup"><span data-stu-id="88082-180">It is possible to receive a TABLE_ERROR event when there is an error in an **IMAPITable::Sort**, **IMAPITable::Restrict**, or **IMAPITable::SetColumns** method or when an underlying process attempts to update a table with, for example, new or modified rows.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="88082-181">См. также</span><span class="sxs-lookup"><span data-stu-id="88082-181">See also</span></span>

- [<span data-ttu-id="88082-182">�����������</span><span class="sxs-lookup"><span data-stu-id="88082-182">NOTIFICATION</span></span>](notification.md) 
- [<span data-ttu-id="88082-183">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="88082-183">ScDupPropset</span></span>](scduppropset.md)
- [<span data-ttu-id="88082-184">SRow</span><span class="sxs-lookup"><span data-stu-id="88082-184">SRow</span></span>](srow.md)
- [<span data-ttu-id="88082-185">SPropValue</span><span class="sxs-lookup"><span data-stu-id="88082-185">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="88082-186">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="88082-186">MAPI Structures</span></span>](mapi-structures.md)

