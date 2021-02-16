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
# <a name="table_notification"></a><span data-ttu-id="b64f4-103">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="b64f4-103">TABLE_NOTIFICATION</span></span>

<span data-ttu-id="b64f4-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b64f4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b64f4-105">Описывает строку в таблице, на которую влияет событие определенного типа, например изменение или ошибка.</span><span class="sxs-lookup"><span data-stu-id="b64f4-105">Describes a row in a table that has been affected by some type of event, such as a change or an error.</span></span> <span data-ttu-id="b64f4-106">Это приводит к сгенерированию уведомления таблицы.</span><span class="sxs-lookup"><span data-stu-id="b64f4-106">This causes a table notification to be generated.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b64f4-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="b64f4-107">Header file:</span></span>  <br/> |<span data-ttu-id="b64f4-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b64f4-108">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="b64f4-109">"Участники"</span><span class="sxs-lookup"><span data-stu-id="b64f4-109">Members</span></span>

<span data-ttu-id="b64f4-110">**ulTableEvent**</span><span class="sxs-lookup"><span data-stu-id="b64f4-110">**ulTableEvent**</span></span>
  
> <span data-ttu-id="b64f4-111">Битоваяmas флагов, используемых для представления типа события таблицы.</span><span class="sxs-lookup"><span data-stu-id="b64f4-111">Bitmask of flags used to represent the table event type.</span></span> <span data-ttu-id="b64f4-112">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="b64f4-112">The following flags can be set:</span></span>
    
<span data-ttu-id="b64f4-113">TABLE_CHANGED</span><span class="sxs-lookup"><span data-stu-id="b64f4-113">TABLE_CHANGED</span></span> 
  
> <span data-ttu-id="b64f4-114">На высоком уровне показывает, что что-то в таблице изменилось.</span><span class="sxs-lookup"><span data-stu-id="b64f4-114">Indicates at a high level that something about the table has changed.</span></span> <span data-ttu-id="b64f4-115">Состояние таблицы находится в том же состоянии, что и до события.</span><span class="sxs-lookup"><span data-stu-id="b64f4-115">The table's state is as it was before the event.</span></span> <span data-ttu-id="b64f4-116">Это означает, **что все** PR_INSTANCE_KEY [(PidTagInstanceKey)](pidtaginstancekey-canonical-property.md)свойства, закладки, текущее позиционирование и выбор пользовательского интерфейса остаются действительными.</span><span class="sxs-lookup"><span data-stu-id="b64f4-116">This means that all **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) properties, bookmarks, current positioning, and user interface selections are still valid.</span></span> <span data-ttu-id="b64f4-117">Обработать это событие, перечитав таблицу.</span><span class="sxs-lookup"><span data-stu-id="b64f4-117">Handle this event by rereading the table.</span></span> <span data-ttu-id="b64f4-118">Поставщики услуг, которые не хотят внедрять уведомления с TABLE_CHANGED таблиц, отправляют события TABLE_CHANGED, а не более подробные события, чтобы указать определенный тип изменений.</span><span class="sxs-lookup"><span data-stu-id="b64f4-118">Service providers that do not want to implement rich table notifications send TABLE_CHANGED events instead of more detailed events to indicate a particular type of change.</span></span> 
    
<span data-ttu-id="b64f4-119">TABLE_ERROR</span><span class="sxs-lookup"><span data-stu-id="b64f4-119">TABLE_ERROR</span></span> 
  
> <span data-ttu-id="b64f4-120">Произошла ошибка, обычно во время обработки асинхронной операции.</span><span class="sxs-lookup"><span data-stu-id="b64f4-120">An error has occurred, usually during the processing of an asynchronous operation.</span></span> <span data-ttu-id="b64f4-121">Ошибки во время обработки следующих методов могут привести к этому событию:</span><span class="sxs-lookup"><span data-stu-id="b64f4-121">Errors during the processing of the following methods can generate this event:</span></span> 
    
   - [<span data-ttu-id="b64f4-122">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="b64f4-122">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
    
   - [<span data-ttu-id="b64f4-123">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="b64f4-123">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
    
   - [<span data-ttu-id="b64f4-124">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="b64f4-124">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
    
   <span data-ttu-id="b64f4-125">После получения события TABLE_ERROR клиент не может полагаться на точность содержимого таблицы.</span><span class="sxs-lookup"><span data-stu-id="b64f4-125">After receiving a TABLE_ERROR event, a client cannot rely on the accuracy of the table contents.</span></span> <span data-ttu-id="b64f4-126">Кроме того, могут быть потеряны ожидающих уведомлений о других изменениях.</span><span class="sxs-lookup"><span data-stu-id="b64f4-126">Also, pending notifications about other changes might be lost.</span></span> <span data-ttu-id="b64f4-127">Метод [IMAPITable::GetLastError](imapitable-getlasterror.md) может не предоставлять дополнительные сведения об ошибке, так как она была сгенерирована в какой-либо предыдущей точке, не обязательно из последнего вызова метода.</span><span class="sxs-lookup"><span data-stu-id="b64f4-127">The [IMAPITable::GetLastError](imapitable-getlasterror.md) method might not provide any additional information about the error because it was generated at some previous point, not necessarily from the last method call.</span></span> 
    
<span data-ttu-id="b64f4-128">TABLE_RELOAD</span><span class="sxs-lookup"><span data-stu-id="b64f4-128">TABLE_RELOAD</span></span> 
  
> <span data-ttu-id="b64f4-129">Данные в таблице должны быть перезагружены.</span><span class="sxs-lookup"><span data-stu-id="b64f4-129">The data in the table should be reloaded.</span></span> <span data-ttu-id="b64f4-130">Поставщики услуг отправляют TABLE_RELOAD, например, когда базовая база данных хранится в базе данных и заменяется базой данных.</span><span class="sxs-lookup"><span data-stu-id="b64f4-130">Service providers send TABLE_RELOAD when, for example, the underlying data is stored in a database and the database is replaced.</span></span> <span data-ttu-id="b64f4-131">Обработать это событие, предполагая, что ничего о таблице по-прежнему не является допустимым, и перечитав таблицу.</span><span class="sxs-lookup"><span data-stu-id="b64f4-131">Handle this event by assuming that nothing about the table is still valid and by rereading the table.</span></span> <span data-ttu-id="b64f4-132">Все закладки, ключи экземпляров, сведения о состоянии и положении недопустимы.</span><span class="sxs-lookup"><span data-stu-id="b64f4-132">All bookmarks, instance keys, status and positioning information are invalid.</span></span>
    
<span data-ttu-id="b64f4-133">TABLE_RESTRICT_DONE</span><span class="sxs-lookup"><span data-stu-id="b64f4-133">TABLE_RESTRICT_DONE</span></span> 
  
> <span data-ttu-id="b64f4-134">Операция ограничения, инициированная вызовом метода **IMAPITable::Restrict,** завершена.</span><span class="sxs-lookup"><span data-stu-id="b64f4-134">A restriction operation initiated with an **IMAPITable::Restrict** method call has completed.</span></span> 
    
<span data-ttu-id="b64f4-135">TABLE_ROW_ADDED</span><span class="sxs-lookup"><span data-stu-id="b64f4-135">TABLE_ROW_ADDED</span></span> 
  
> <span data-ttu-id="b64f4-136">В таблицу добавлена новая строка и сохранен соответствующий объект.</span><span class="sxs-lookup"><span data-stu-id="b64f4-136">A new row has been added to the table and the corresponding object saved.</span></span> <span data-ttu-id="b64f4-137">TABLE_ROW_ADDED события создаются после вызова метода [IMAPIProp::SaveChanges.](imapiprop-savechanges.md)</span><span class="sxs-lookup"><span data-stu-id="b64f4-137">TABLE_ROW_ADDED events are generated after a call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
    
<span data-ttu-id="b64f4-138">TABLE_ROW_DELETED</span><span class="sxs-lookup"><span data-stu-id="b64f4-138">TABLE_ROW_DELETED</span></span> 
  
> <span data-ttu-id="b64f4-139">Строка удалена из таблицы.</span><span class="sxs-lookup"><span data-stu-id="b64f4-139">A row has been removed from the table.</span></span> <span data-ttu-id="b64f4-140">Для **члена propPrior** установлено nULL.</span><span class="sxs-lookup"><span data-stu-id="b64f4-140">The **propPrior** member is set to NULL.</span></span> 
    
<span data-ttu-id="b64f4-141">TABLE_ROW_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="b64f4-141">TABLE_ROW_MODIFIED</span></span> 
  
> <span data-ttu-id="b64f4-142">Строка была изменена.</span><span class="sxs-lookup"><span data-stu-id="b64f4-142">A row has been changed.</span></span> <span data-ttu-id="b64f4-143">Член **строки** содержит затронутые свойства для строки.</span><span class="sxs-lookup"><span data-stu-id="b64f4-143">The **row** member contains the affected properties for the row.</span></span> <span data-ttu-id="b64f4-144">Несколько TABLE_ROW_MODIFIED отправляются в том порядке, в который они отображаются в представлении таблицы.</span><span class="sxs-lookup"><span data-stu-id="b64f4-144">Multiple TABLE_ROW_MODIFIED events are sent in the order that they appear in the table view.</span></span> 
    
  <span data-ttu-id="b64f4-145">TABLE_ROW_MODIFIED события отправляются после внесения изменений в соответствующий объект с помощью вызова метода **IMAPIProp::SaveChanges.**</span><span class="sxs-lookup"><span data-stu-id="b64f4-145">TABLE_ROW_MODIFIED events are sent after changes to the corresponding object have been committed with a call to the **IMAPIProp::SaveChanges** method.</span></span> <span data-ttu-id="b64f4-146">Если измененная строка теперь является первой строкой в таблице, значение тега свойства в члене **propPrior** PR_NULL **(** [PidTagNull).](pidtagnull-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="b64f4-146">If the modified row is now the first row in the table, the value of the property tag in the **propPrior** member is **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).</span></span>
    
<span data-ttu-id="b64f4-147">TABLE_SETCOL_DONE</span><span class="sxs-lookup"><span data-stu-id="b64f4-147">TABLE_SETCOL_DONE</span></span> 
  
> <span data-ttu-id="b64f4-148">Операция настройки столбца, инициированная вызовом метода **IMAPITable::SetColumns,** завершена.</span><span class="sxs-lookup"><span data-stu-id="b64f4-148">A column setting operation initiated with an **IMAPITable::SetColumns** method call has completed.</span></span> 
    
<span data-ttu-id="b64f4-149">TABLE_SORT_DONE</span><span class="sxs-lookup"><span data-stu-id="b64f4-149">TABLE_SORT_DONE</span></span> 
  
> <span data-ttu-id="b64f4-150">Операция сортировки таблиц, инициированная вызовом метода **IMAPITable::SortTable,** завершена.</span><span class="sxs-lookup"><span data-stu-id="b64f4-150">A table sorting operation initiated with an **IMAPITable::SortTable** method call has completed.</span></span> 
    
<span data-ttu-id="b64f4-151">**hResult**</span><span class="sxs-lookup"><span data-stu-id="b64f4-151">**hResult**</span></span>
  
> <span data-ttu-id="b64f4-152">Значение HRESULT возникской ошибки, если для члена **ulTableEvent** установлено значение TABLE_ERROR.</span><span class="sxs-lookup"><span data-stu-id="b64f4-152">HRESULT value for the error that has occurred, if the **ulTableEvent** member is set to TABLE_ERROR.</span></span> 
    
<span data-ttu-id="b64f4-153">**propIndex**</span><span class="sxs-lookup"><span data-stu-id="b64f4-153">**propIndex**</span></span>
  
> <span data-ttu-id="b64f4-154">[Структура SPropValue](spropvalue.md) **для** PR_INSTANCE_KEY свойства затронутой строки.</span><span class="sxs-lookup"><span data-stu-id="b64f4-154">[SPropValue](spropvalue.md) structure for the **PR_INSTANCE_KEY** property of the affected row.</span></span> 
    
<span data-ttu-id="b64f4-155">**propPrior**</span><span class="sxs-lookup"><span data-stu-id="b64f4-155">**propPrior**</span></span>
  
> <span data-ttu-id="b64f4-156">**Структура SPropValue** для **PR_INSTANCE_KEY** строки до затронутого.</span><span class="sxs-lookup"><span data-stu-id="b64f4-156">**SPropValue** structure for the **PR_INSTANCE_KEY** property of the row before the affected one.</span></span> <span data-ttu-id="b64f4-157">Если затронутая строка является первой строкой в таблице, **для propPrior** необходимо установить значение **PR_NULL** ноль.</span><span class="sxs-lookup"><span data-stu-id="b64f4-157">If the affected row is the first row in the table, **propPrior** must be set to **PR_NULL** and not zero.</span></span> <span data-ttu-id="b64f4-158">Ноль не является допустимым тегом свойства.</span><span class="sxs-lookup"><span data-stu-id="b64f4-158">Zero is not a valid property tag.</span></span> 
    
<span data-ttu-id="b64f4-159">**row**</span><span class="sxs-lookup"><span data-stu-id="b64f4-159">**row**</span></span>
  
> <span data-ttu-id="b64f4-160">[Структура SRow,](srow.md) описывающие затронутую строку.</span><span class="sxs-lookup"><span data-stu-id="b64f4-160">[SRow](srow.md) structure describing the affected row.</span></span> <span data-ttu-id="b64f4-161">Эта структура заполняется для всех событий уведомлений таблицы.</span><span class="sxs-lookup"><span data-stu-id="b64f4-161">This structure is filled for all table notification events.</span></span> <span data-ttu-id="b64f4-162">Для событий уведомлений таблицы, которые не передают данные строки, для члена **cValues** структуры **SRow** устанавливается нулевое значение, а для члена **lpProps** — значение NULL.</span><span class="sxs-lookup"><span data-stu-id="b64f4-162">For table notification events that do not pass row data, the **cValues** member of the **SRow** structure is set to zero and the **lpProps** member is set to NULL.</span></span> <span data-ttu-id="b64f4-163">Поскольку эта **структура SRow** является только для чтения; клиенты должны сделать ее копию, если они хотят внести изменения.</span><span class="sxs-lookup"><span data-stu-id="b64f4-163">Because this **SRow** structure is read-only; clients must make a copy of it if they want to make modifications.</span></span> <span data-ttu-id="b64f4-164">Для копирования можно использовать функцию [ScDupPropset.](scduppropset.md)</span><span class="sxs-lookup"><span data-stu-id="b64f4-164">The [ScDupPropset](scduppropset.md) function can be used to make the copy.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b64f4-165">Примечания</span><span class="sxs-lookup"><span data-stu-id="b64f4-165">Remarks</span></span>

<span data-ttu-id="b64f4-166">Структура **TABLE \_ NOTIFICATION** — это один из членов объединения структур, включенных в состав данных структуры [NOTIFICATION.](notification.md) </span><span class="sxs-lookup"><span data-stu-id="b64f4-166">The **TABLE\_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="b64f4-167">Член **info** включает структуру **TABLE \_ NOTIFICATION,** когда для члена **ulEventType** структуры установлено в  _fnevTableModified_.</span><span class="sxs-lookup"><span data-stu-id="b64f4-167">The **info** member includes a **TABLE\_NOTIFICATION** structure when the **ulEventType** member of the structure is set to  _fnevTableModified_.</span></span>
  
<span data-ttu-id="b64f4-168">Порядок и тип столбцов в члене строки отражают порядок и тип, которые вступили в силу на момент получения уведомления.</span><span class="sxs-lookup"><span data-stu-id="b64f4-168">The order and type of columns in the row member reflect the order and type that was in effect at the time that the notification was generated.</span></span> <span data-ttu-id="b64f4-169">Порядок и тип уведомления не обязательно совпадают с порядком и типом на момент его доставки.</span><span class="sxs-lookup"><span data-stu-id="b64f4-169">The order and type at the time that the notification was generated is not necessarily the same as when the notification was delivered.</span></span> 
  
<span data-ttu-id="b64f4-170">Дополнительные сведения об уведомлении см. в темах, описанных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="b64f4-170">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="b64f4-171">**Статья**</span><span class="sxs-lookup"><span data-stu-id="b64f4-171">**Topic**</span></span>|<span data-ttu-id="b64f4-172">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b64f4-172">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b64f4-173">Уведомление о событии в MAPI</span><span class="sxs-lookup"><span data-stu-id="b64f4-173">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="b64f4-174">Общий обзор событий уведомлений и уведомлений.</span><span class="sxs-lookup"><span data-stu-id="b64f4-174">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="b64f4-175">Обработка уведомлений</span><span class="sxs-lookup"><span data-stu-id="b64f4-175">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="b64f4-176">Обсуждение того, как клиенты должны обрабатывать уведомления.</span><span class="sxs-lookup"><span data-stu-id="b64f4-176">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="b64f4-177">Поддержка уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="b64f4-177">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="b64f4-178">Обсуждение того, как поставщики служб могут использовать метод **IMAPISupport** для создания уведомлений.</span><span class="sxs-lookup"><span data-stu-id="b64f4-178">Discussion of how service providers can use the **IMAPISupport** method to generate notifications.</span></span>  <br/> |
   
<span data-ttu-id="b64f4-179">Так как уведомления таблиц являются асинхронными, клиенты могут получать уведомления о добавленной строке после изучения добавления другими способами.</span><span class="sxs-lookup"><span data-stu-id="b64f4-179">Because table notifications are asynchronous, clients can receive notification of an added row after learning about the addition through another means.</span></span> <span data-ttu-id="b64f4-180">Можно получить событие TABLE_ERROR при ошибке в методе **IMAPITable::Sort,** **IMAPITable::Restrict** или **IMAPITable::SetColumns** или при попытке обновления таблицы с помощью, например, новых или измененных строк.</span><span class="sxs-lookup"><span data-stu-id="b64f4-180">It is possible to receive a TABLE_ERROR event when there is an error in an **IMAPITable::Sort**, **IMAPITable::Restrict**, or **IMAPITable::SetColumns** method or when an underlying process attempts to update a table with, for example, new or modified rows.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b64f4-181">См. также</span><span class="sxs-lookup"><span data-stu-id="b64f4-181">See also</span></span>

- [<span data-ttu-id="b64f4-182">�����������</span><span class="sxs-lookup"><span data-stu-id="b64f4-182">NOTIFICATION</span></span>](notification.md) 
- [<span data-ttu-id="b64f4-183">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="b64f4-183">ScDupPropset</span></span>](scduppropset.md)
- [<span data-ttu-id="b64f4-184">SRow</span><span class="sxs-lookup"><span data-stu-id="b64f4-184">SRow</span></span>](srow.md)
- [<span data-ttu-id="b64f4-185">SPropValue</span><span class="sxs-lookup"><span data-stu-id="b64f4-185">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="b64f4-186">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="b64f4-186">MAPI Structures</span></span>](mapi-structures.md)

