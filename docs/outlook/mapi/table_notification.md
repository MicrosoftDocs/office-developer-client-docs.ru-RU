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
# <a name="tablenotification"></a><span data-ttu-id="061b7-103">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="061b7-103">TABLE_NOTIFICATION</span></span>

<span data-ttu-id="061b7-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="061b7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="061b7-105">Описывает строку в таблице, на которую влияют некоторые типы событий, такие как изменение или ошибка.</span><span class="sxs-lookup"><span data-stu-id="061b7-105">Describes a row in a table that has been affected by some type of event, such as a change or an error.</span></span> <span data-ttu-id="061b7-106">Это приводит к созданию уведомления таблицы.</span><span class="sxs-lookup"><span data-stu-id="061b7-106">This causes a table notification to be generated.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="061b7-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="061b7-107">Header file:</span></span>  <br/> |<span data-ttu-id="061b7-108">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="061b7-108">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="061b7-109">Members</span><span class="sxs-lookup"><span data-stu-id="061b7-109">Members</span></span>

<span data-ttu-id="061b7-110">**Ултабливент**</span><span class="sxs-lookup"><span data-stu-id="061b7-110">**ulTableEvent**</span></span>
  
> <span data-ttu-id="061b7-111">Битовая маска флагов, используемых для представления типа табличного события.</span><span class="sxs-lookup"><span data-stu-id="061b7-111">Bitmask of flags used to represent the table event type.</span></span> <span data-ttu-id="061b7-112">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="061b7-112">The following flags can be set:</span></span>
    
<span data-ttu-id="061b7-113">ТАБЛЕ_ЧАНЖЕД</span><span class="sxs-lookup"><span data-stu-id="061b7-113">TABLE_CHANGED</span></span> 
  
> <span data-ttu-id="061b7-114">Указывает на высокий уровень, в котором изменилось какое-либо значение для таблицы.</span><span class="sxs-lookup"><span data-stu-id="061b7-114">Indicates at a high level that something about the table has changed.</span></span> <span data-ttu-id="061b7-115">Состояние таблицы — то, что она была до события.</span><span class="sxs-lookup"><span data-stu-id="061b7-115">The table's state is as it was before the event.</span></span> <span data-ttu-id="061b7-116">Это означает, что все свойства **пр_инстанце_кэй** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), закладки, текущее расположение и параметры пользовательского интерфейса все еще действительны.</span><span class="sxs-lookup"><span data-stu-id="061b7-116">This means that all **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) properties, bookmarks, current positioning, and user interface selections are still valid.</span></span> <span data-ttu-id="061b7-117">ОбРаботайте это событие с помощью пересчитывания таблицы.</span><span class="sxs-lookup"><span data-stu-id="061b7-117">Handle this event by rereading the table.</span></span> <span data-ttu-id="061b7-118">Поставщики услуг, которые не хотят реализовывать Многофункциональные уведомления, отправляют события ТАБЛЕ_ЧАНЖЕД, а не более подробные события, чтобы указать конкретный тип изменения.</span><span class="sxs-lookup"><span data-stu-id="061b7-118">Service providers that do not want to implement rich table notifications send TABLE_CHANGED events instead of more detailed events to indicate a particular type of change.</span></span> 
    
<span data-ttu-id="061b7-119">ТАБЛЕ_ЕРРОР</span><span class="sxs-lookup"><span data-stu-id="061b7-119">TABLE_ERROR</span></span> 
  
> <span data-ttu-id="061b7-120">Произошла ошибка, обычно во время обработки асинхронной операции.</span><span class="sxs-lookup"><span data-stu-id="061b7-120">An error has occurred, usually during the processing of an asynchronous operation.</span></span> <span data-ttu-id="061b7-121">При обработке следующих методов возникли ошибки, которые могут создать это событие:</span><span class="sxs-lookup"><span data-stu-id="061b7-121">Errors during the processing of the following methods can generate this event:</span></span> 
    
   - [<span data-ttu-id="061b7-122">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="061b7-122">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
    
   - [<span data-ttu-id="061b7-123">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="061b7-123">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
    
   - [<span data-ttu-id="061b7-124">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="061b7-124">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
    
   <span data-ttu-id="061b7-125">После получения события ТАБЛЕ_ЕРРОР клиент не может зависеть от точности содержимого таблицы.</span><span class="sxs-lookup"><span data-stu-id="061b7-125">After receiving a TABLE_ERROR event, a client cannot rely on the accuracy of the table contents.</span></span> <span data-ttu-id="061b7-126">Кроме того, ожидающие уведомления о других изменениях могут быть потеряны.</span><span class="sxs-lookup"><span data-stu-id="061b7-126">Also, pending notifications about other changes might be lost.</span></span> <span data-ttu-id="061b7-127">Метод [IMAPITable:: GetLastError](imapitable-getlasterror.md) не может предоставлять дополнительные сведения об ошибке, так как она была создана в какой-либо предыдущей точке, а не обязательно из последнего вызова метода.</span><span class="sxs-lookup"><span data-stu-id="061b7-127">The [IMAPITable::GetLastError](imapitable-getlasterror.md) method might not provide any additional information about the error because it was generated at some previous point, not necessarily from the last method call.</span></span> 
    
<span data-ttu-id="061b7-128">ТАБЛЕ_РЕЛОАД</span><span class="sxs-lookup"><span data-stu-id="061b7-128">TABLE_RELOAD</span></span> 
  
> <span data-ttu-id="061b7-129">Данные в таблице должны быть перезагружены.</span><span class="sxs-lookup"><span data-stu-id="061b7-129">The data in the table should be reloaded.</span></span> <span data-ttu-id="061b7-130">Поставщики услуг отправляют ТАБЛЕ_РЕЛОАД, например, базовые данные хранятся в базе данных, а база данных заменяется.</span><span class="sxs-lookup"><span data-stu-id="061b7-130">Service providers send TABLE_RELOAD when, for example, the underlying data is stored in a database and the database is replaced.</span></span> <span data-ttu-id="061b7-131">ОбРаботайте это событие, предполагая, что ничего для таблицы по-прежнему является допустимым и пересчитывает таблицу.</span><span class="sxs-lookup"><span data-stu-id="061b7-131">Handle this event by assuming that nothing about the table is still valid and by rereading the table.</span></span> <span data-ttu-id="061b7-132">Все закладки, ключи экземпляра, сведения о состоянии и размещении недопустимы.</span><span class="sxs-lookup"><span data-stu-id="061b7-132">All bookmarks, instance keys, status and positioning information are invalid.</span></span>
    
<span data-ttu-id="061b7-133">ТАБЛЕ_РЕСТРИКТ_ДОНЕ</span><span class="sxs-lookup"><span data-stu-id="061b7-133">TABLE_RESTRICT_DONE</span></span> 
  
> <span data-ttu-id="061b7-134">Операция ограничения, инициированная с помощью вызова метода **IMAPITable:: restrict** , завершена.</span><span class="sxs-lookup"><span data-stu-id="061b7-134">A restriction operation initiated with an **IMAPITable::Restrict** method call has completed.</span></span> 
    
<span data-ttu-id="061b7-135">ТАБЛЕ_РОВ_АДДЕД</span><span class="sxs-lookup"><span data-stu-id="061b7-135">TABLE_ROW_ADDED</span></span> 
  
> <span data-ttu-id="061b7-136">В таблицу добавлена новая строка и сохранен соответствующий объект.</span><span class="sxs-lookup"><span data-stu-id="061b7-136">A new row has been added to the table and the corresponding object saved.</span></span> <span data-ttu-id="061b7-137">События ТАБЛЕ_РОВ_АДДЕД создаются после вызова метода [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="061b7-137">TABLE_ROW_ADDED events are generated after a call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
    
<span data-ttu-id="061b7-138">ТАБЛЕ_РОВ_ДЕЛЕТЕД</span><span class="sxs-lookup"><span data-stu-id="061b7-138">TABLE_ROW_DELETED</span></span> 
  
> <span data-ttu-id="061b7-139">Строка была удалена из таблицы.</span><span class="sxs-lookup"><span data-stu-id="061b7-139">A row has been removed from the table.</span></span> <span data-ttu-id="061b7-140">Для члена **пропприор** ЗАДАНО значение null.</span><span class="sxs-lookup"><span data-stu-id="061b7-140">The **propPrior** member is set to NULL.</span></span> 
    
<span data-ttu-id="061b7-141">ТАБЛЕ_РОВ_МОДИФИЕД</span><span class="sxs-lookup"><span data-stu-id="061b7-141">TABLE_ROW_MODIFIED</span></span> 
  
> <span data-ttu-id="061b7-142">Изменена строка.</span><span class="sxs-lookup"><span data-stu-id="061b7-142">A row has been changed.</span></span> <span data-ttu-id="061b7-143">Элемент **Row** содержит затронутые свойства для строки.</span><span class="sxs-lookup"><span data-stu-id="061b7-143">The **row** member contains the affected properties for the row.</span></span> <span data-ttu-id="061b7-144">Несколько событий ТАБЛЕ_РОВ_МОДИФИЕД отправляются в том порядке, в котором они отображаются в представлении таблицы.</span><span class="sxs-lookup"><span data-stu-id="061b7-144">Multiple TABLE_ROW_MODIFIED events are sent in the order that they appear in the table view.</span></span> 
    
  <span data-ttu-id="061b7-145">События ТАБЛЕ_РОВ_МОДИФИЕД отправляются после того, как изменения в соответствующем объекте зафиксированы при вызове метода **IMAPIProp:: SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="061b7-145">TABLE_ROW_MODIFIED events are sent after changes to the corresponding object have been committed with a call to the **IMAPIProp::SaveChanges** method.</span></span> <span data-ttu-id="061b7-146">Если измененная строка теперь является первой строкой в таблице, значение тега свойства в элементе **пропприор** — **пр_нулл** ([PidTagNull](pidtagnull-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="061b7-146">If the modified row is now the first row in the table, the value of the property tag in the **propPrior** member is **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).</span></span>
    
<span data-ttu-id="061b7-147">ТАБЛЕ_СЕТКОЛ_ДОНЕ</span><span class="sxs-lookup"><span data-stu-id="061b7-147">TABLE_SETCOL_DONE</span></span> 
  
> <span data-ttu-id="061b7-148">Операция настройки столбца, инициированная с помощью вызова метода **IMAPITable:: метода SetColumns** , завершена.</span><span class="sxs-lookup"><span data-stu-id="061b7-148">A column setting operation initiated with an **IMAPITable::SetColumns** method call has completed.</span></span> 
    
<span data-ttu-id="061b7-149">ТАБЛЕ_СОРТ_ДОНЕ</span><span class="sxs-lookup"><span data-stu-id="061b7-149">TABLE_SORT_DONE</span></span> 
  
> <span data-ttu-id="061b7-150">Операция сортировки таблицы, инициированная с помощью вызова метода **IMAPITable:: сорттабле** , завершена.</span><span class="sxs-lookup"><span data-stu-id="061b7-150">A table sorting operation initiated with an **IMAPITable::SortTable** method call has completed.</span></span> 
    
<span data-ttu-id="061b7-151">**Состав**</span><span class="sxs-lookup"><span data-stu-id="061b7-151">**hResult**</span></span>
  
> <span data-ttu-id="061b7-152">Значение HRESULT для возникшей ошибки, если для члена **ултабливент** задано значение табле_еррор.</span><span class="sxs-lookup"><span data-stu-id="061b7-152">HRESULT value for the error that has occurred, if the **ulTableEvent** member is set to TABLE_ERROR.</span></span> 
    
<span data-ttu-id="061b7-153">**Пропиндекс**</span><span class="sxs-lookup"><span data-stu-id="061b7-153">**propIndex**</span></span>
  
> <span data-ttu-id="061b7-154">Структура [спропвалуе](spropvalue.md) для свойства **пр_инстанце_кэй** затронутой строки.</span><span class="sxs-lookup"><span data-stu-id="061b7-154">[SPropValue](spropvalue.md) structure for the **PR_INSTANCE_KEY** property of the affected row.</span></span> 
    
<span data-ttu-id="061b7-155">**Пропприор**</span><span class="sxs-lookup"><span data-stu-id="061b7-155">**propPrior**</span></span>
  
> <span data-ttu-id="061b7-156">Структура **спропвалуе** для свойства **пр_инстанце_кэй** строки перед затронутым.</span><span class="sxs-lookup"><span data-stu-id="061b7-156">**SPropValue** structure for the **PR_INSTANCE_KEY** property of the row before the affected one.</span></span> <span data-ttu-id="061b7-157">Если затронутая строка является первой строкой в таблице, для **пропприор** должно быть задано значение **пр_нулл** , а не ноль.</span><span class="sxs-lookup"><span data-stu-id="061b7-157">If the affected row is the first row in the table, **propPrior** must be set to **PR_NULL** and not zero.</span></span> <span data-ttu-id="061b7-158">Ноль не является допустимым тегом свойства.</span><span class="sxs-lookup"><span data-stu-id="061b7-158">Zero is not a valid property tag.</span></span> 
    
<span data-ttu-id="061b7-159">**Строка**</span><span class="sxs-lookup"><span data-stu-id="061b7-159">**row**</span></span>
  
> <span data-ttu-id="061b7-160">Структура [сров](srow.md) , описывающая затронутую строку.</span><span class="sxs-lookup"><span data-stu-id="061b7-160">[SRow](srow.md) structure describing the affected row.</span></span> <span data-ttu-id="061b7-161">Эта структура заполняется для всех событий уведомления таблицы.</span><span class="sxs-lookup"><span data-stu-id="061b7-161">This structure is filled for all table notification events.</span></span> <span data-ttu-id="061b7-162">Для событий уведомления таблицы, которые не передают данные строки, элементу **квалуес** структуры **сров** присваивается нулевое значение, а для элемента **лппропс** задано значение null.</span><span class="sxs-lookup"><span data-stu-id="061b7-162">For table notification events that do not pass row data, the **cValues** member of the **SRow** structure is set to zero and the **lpProps** member is set to NULL.</span></span> <span data-ttu-id="061b7-163">Так как эта структура **сров** доступна только для чтения; Клиенты должны создать копию этого файла, если необходимо внести изменения.</span><span class="sxs-lookup"><span data-stu-id="061b7-163">Because this **SRow** structure is read-only; clients must make a copy of it if they want to make modifications.</span></span> <span data-ttu-id="061b7-164">Для создания копии можно использовать функцию [скдуппропсет](scduppropset.md) .</span><span class="sxs-lookup"><span data-stu-id="061b7-164">The [ScDupPropset](scduppropset.md) function can be used to make the copy.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="061b7-165">Примечания</span><span class="sxs-lookup"><span data-stu-id="061b7-165">Remarks</span></span>

<span data-ttu-id="061b7-166">Структура **уведомления\_таблицы** — это один из элементов объединения структур, включенных в элемент **info** структуры [уведомления](notification.md) .</span><span class="sxs-lookup"><span data-stu-id="061b7-166">The **TABLE\_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="061b7-167">Элемент **info** включает структуру **уведомления таблицы\_** , если элемент **улевенттипе** структуры имеет значение _фневтаблемодифиед_.</span><span class="sxs-lookup"><span data-stu-id="061b7-167">The **info** member includes a **TABLE\_NOTIFICATION** structure when the **ulEventType** member of the structure is set to  _fnevTableModified_.</span></span>
  
<span data-ttu-id="061b7-168">Порядок и тип столбцов в элементе Row отражают порядок и тип, которые действовали на момент создания уведомления.</span><span class="sxs-lookup"><span data-stu-id="061b7-168">The order and type of columns in the row member reflect the order and type that was in effect at the time that the notification was generated.</span></span> <span data-ttu-id="061b7-169">Порядок и тип в момент создания уведомления не обязательно совпадают с моментом доставки уведомления.</span><span class="sxs-lookup"><span data-stu-id="061b7-169">The order and type at the time that the notification was generated is not necessarily the same as when the notification was delivered.</span></span> 
  
<span data-ttu-id="061b7-170">Дополнительные сведения об уведомлении можно найти в разделах, приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="061b7-170">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="061b7-171">**Статья**</span><span class="sxs-lookup"><span data-stu-id="061b7-171">**Topic**</span></span>|<span data-ttu-id="061b7-172">**Описание**</span><span class="sxs-lookup"><span data-stu-id="061b7-172">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="061b7-173">Уведомление о соБытии в MAPI</span><span class="sxs-lookup"><span data-stu-id="061b7-173">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="061b7-174">Общие сведения о событиях уведомлений и уведомлений.</span><span class="sxs-lookup"><span data-stu-id="061b7-174">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="061b7-175">Обработка уведомлений</span><span class="sxs-lookup"><span data-stu-id="061b7-175">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="061b7-176">Обсуждение того, как клиенты должны обрабатывать уведомления.</span><span class="sxs-lookup"><span data-stu-id="061b7-176">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="061b7-177">Поддержка уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="061b7-177">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="061b7-178">Обсуждение того, как поставщики услуг могут использовать метод **имаписуппорт** для создания уведомлений.</span><span class="sxs-lookup"><span data-stu-id="061b7-178">Discussion of how service providers can use the **IMAPISupport** method to generate notifications.</span></span>  <br/> |
   
<span data-ttu-id="061b7-179">Так как уведомления таблиц асинхронны, клиенты могут получать уведомления о добавленной строке после изучения других средств.</span><span class="sxs-lookup"><span data-stu-id="061b7-179">Because table notifications are asynchronous, clients can receive notification of an added row after learning about the addition through another means.</span></span> <span data-ttu-id="061b7-180">Возможно получение события ТАБЛЕ_ЕРРОР при возникновении ошибки в методе **IMAPITable:: Sort**, **IMAPITable:: restrict**или **IMAPITable:: метода SetColumns** , или когда базовый процесс пытается обновить таблицу, например "создать" или " измененные строки.</span><span class="sxs-lookup"><span data-stu-id="061b7-180">It is possible to receive a TABLE_ERROR event when there is an error in an **IMAPITable::Sort**, **IMAPITable::Restrict**, or **IMAPITable::SetColumns** method or when an underlying process attempts to update a table with, for example, new or modified rows.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="061b7-181">См. также</span><span class="sxs-lookup"><span data-stu-id="061b7-181">See also</span></span>

- [<span data-ttu-id="061b7-182">�����������</span><span class="sxs-lookup"><span data-stu-id="061b7-182">NOTIFICATION</span></span>](notification.md) 
- [<span data-ttu-id="061b7-183">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="061b7-183">ScDupPropset</span></span>](scduppropset.md)
- [<span data-ttu-id="061b7-184">SRow</span><span class="sxs-lookup"><span data-stu-id="061b7-184">SRow</span></span>](srow.md)
- [<span data-ttu-id="061b7-185">SPropValue</span><span class="sxs-lookup"><span data-stu-id="061b7-185">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="061b7-186">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="061b7-186">MAPI Structures</span></span>](mapi-structures.md)

