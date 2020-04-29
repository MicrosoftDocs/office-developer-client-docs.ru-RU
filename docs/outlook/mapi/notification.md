---
title: NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.NOTIFICATION
api_type:
- COM
ms.assetid: 01b6e695-a649-4efd-a893-7586b476467e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a3235c2305d61318f482943167e5f307e5da0d70
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432879"
---
# <a name="notification"></a><span data-ttu-id="c9e18-103">NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="c9e18-103">NOTIFICATION</span></span>
 
<span data-ttu-id="c9e18-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c9e18-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c9e18-105">Содержит сведения о произошедшем событии и данных, на которые повлияло событие.</span><span class="sxs-lookup"><span data-stu-id="c9e18-105">Contains information about an event that has occurred and the data that has been affected by the event.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c9e18-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="c9e18-106">Header file:</span></span>  <br/> |<span data-ttu-id="c9e18-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="c9e18-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG ulEventType;
  union
  {
    ERROR_NOTIFICATION err;
    NEWMAIL_NOTIFICATION newmail;
    OBJECT_NOTIFICATION obj;
    TABLE_NOTIFICATION tab;
    EXTENDED_NOTIFICATION ext;
    STATUS_OBJECT_NOTIFICATION statobj;
  } info;
} NOTIFICATION, FAR *LPNOTIFICATION;

```

## <a name="members"></a><span data-ttu-id="c9e18-108">"Участники"</span><span class="sxs-lookup"><span data-stu-id="c9e18-108">Members</span></span>

<span data-ttu-id="c9e18-109">**улевенттипе**</span><span class="sxs-lookup"><span data-stu-id="c9e18-109">**ulEventType**</span></span>
  
> <span data-ttu-id="c9e18-110">Тип произошедшего события уведомления.</span><span class="sxs-lookup"><span data-stu-id="c9e18-110">Type of notification event that occurred.</span></span> <span data-ttu-id="c9e18-111">Значение элемента **улевенттипе** соответствует структуре, включенной в объединение **сведений** .</span><span class="sxs-lookup"><span data-stu-id="c9e18-111">The value of the **ulEventType** member corresponds to the structure that is included in the **info** union.</span></span> <span data-ttu-id="c9e18-112">Члену **улевенттипе** можно присвоить одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="c9e18-112">The **ulEventType** member can be set to one of the following values:</span></span> 
    
 <span data-ttu-id="c9e18-113">_фневкритикалеррор_</span><span class="sxs-lookup"><span data-stu-id="c9e18-113">_fnevCriticalError_</span></span>
  
> <span data-ttu-id="c9e18-114">Произошла глобальная ошибка, например, выполнение сеанса завершено.</span><span class="sxs-lookup"><span data-stu-id="c9e18-114">A global error has occurred, such as a session shut down in progress.</span></span> <span data-ttu-id="c9e18-115">Элемент **info** содержит структуру [ERROR_NOTIFICATION](error_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="c9e18-115">The **info** member contains an [ERROR_NOTIFICATION](error_notification.md) structure.</span></span> 
    
 <span data-ttu-id="c9e18-116">_фневекстендед_</span><span class="sxs-lookup"><span data-stu-id="c9e18-116">_fnevExtended_</span></span>
  
> <span data-ttu-id="c9e18-117">Произошло внутреннее событие, определенное определенным поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="c9e18-117">An internal event defined by a particular service provider has occurred.</span></span> <span data-ttu-id="c9e18-118">Элемент **info** содержит структуру [EXTENDED_NOTIFICATION](extended_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="c9e18-118">The **info** member contains an [EXTENDED_NOTIFICATION](extended_notification.md) structure.</span></span> 
    
 <span data-ttu-id="c9e18-119">_фневневмаил_</span><span class="sxs-lookup"><span data-stu-id="c9e18-119">_fnevNewMail_</span></span>
  
> <span data-ttu-id="c9e18-120">Сообщение доставлено в соответствующую папку получения для класса сообщений и ожидает обработки.</span><span class="sxs-lookup"><span data-stu-id="c9e18-120">A message has been delivered to the appropriate receive folder for the message class and is waiting to be processed.</span></span> <span data-ttu-id="c9e18-121">Элемент **info** содержит структуру [NEWMAIL_NOTIFICATION](newmail_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="c9e18-121">The **info** member contains an [NEWMAIL_NOTIFICATION](newmail_notification.md) structure.</span></span> 
    
 <span data-ttu-id="c9e18-122">_фневобжекткопиед_</span><span class="sxs-lookup"><span data-stu-id="c9e18-122">_fnevObjectCopied_</span></span>
  
> <span data-ttu-id="c9e18-123">Скопирован объект MAPI.</span><span class="sxs-lookup"><span data-stu-id="c9e18-123">A MAPI object has been copied.</span></span> <span data-ttu-id="c9e18-124">Элемент **info** содержит структуру [OBJECT_NOTIFICATION](object_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="c9e18-124">The **info** member contains an [OBJECT_NOTIFICATION](object_notification.md) structure.</span></span> 
    
 <span data-ttu-id="c9e18-125">_фневобжекткреатед_</span><span class="sxs-lookup"><span data-stu-id="c9e18-125">_fnevObjectCreated_</span></span>
  
> <span data-ttu-id="c9e18-126">Создан объект MAPI.</span><span class="sxs-lookup"><span data-stu-id="c9e18-126">A MAPI object has been created.</span></span> <span data-ttu-id="c9e18-127">Элемент **info** содержит структуру **OBJECT_NOTIFICATION** .</span><span class="sxs-lookup"><span data-stu-id="c9e18-127">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="c9e18-128">_фневобжектделетед_</span><span class="sxs-lookup"><span data-stu-id="c9e18-128">_fnevObjectDeleted_</span></span>
  
> <span data-ttu-id="c9e18-129">Объект MAPI удален.</span><span class="sxs-lookup"><span data-stu-id="c9e18-129">A MAPI object has been deleted.</span></span> <span data-ttu-id="c9e18-130">Элемент **info** содержит структуру **OBJECT_NOTIFICATION** .</span><span class="sxs-lookup"><span data-stu-id="c9e18-130">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="c9e18-131">_фневобжектмодифиед_</span><span class="sxs-lookup"><span data-stu-id="c9e18-131">_fnevObjectModified_</span></span>
  
> <span data-ttu-id="c9e18-132">Объект MAPI изменился.</span><span class="sxs-lookup"><span data-stu-id="c9e18-132">A MAPI object has changed.</span></span> <span data-ttu-id="c9e18-133">Элемент **info** содержит структуру **OBJECT_NOTIFICATION** .</span><span class="sxs-lookup"><span data-stu-id="c9e18-133">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="c9e18-134">_фневобжектмовед_</span><span class="sxs-lookup"><span data-stu-id="c9e18-134">_fnevObjectMoved_</span></span>
  
> <span data-ttu-id="c9e18-135">Было перемещено хранилище сообщений или объект адресной книги.</span><span class="sxs-lookup"><span data-stu-id="c9e18-135">A message store or address book object has been moved.</span></span> <span data-ttu-id="c9e18-136">Элемент **info** содержит структуру **OBJECT_NOTIFICATION** .</span><span class="sxs-lookup"><span data-stu-id="c9e18-136">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="c9e18-137">_фневсеарчкомплете_</span><span class="sxs-lookup"><span data-stu-id="c9e18-137">_fnevSearchComplete_</span></span>
  
> <span data-ttu-id="c9e18-138">Операция поиска завершена, и результаты доступны.</span><span class="sxs-lookup"><span data-stu-id="c9e18-138">A search operation has finished and the results are available.</span></span> <span data-ttu-id="c9e18-139">Элемент **info** содержит структуру **OBJECT_NOTIFICATION** .</span><span class="sxs-lookup"><span data-stu-id="c9e18-139">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="c9e18-140">_фневтаблемодифиед_</span><span class="sxs-lookup"><span data-stu-id="c9e18-140">_fnevTableModified_</span></span>
  
> <span data-ttu-id="c9e18-141">Изменилась информация в таблице.</span><span class="sxs-lookup"><span data-stu-id="c9e18-141">Information in a table has changed.</span></span> <span data-ttu-id="c9e18-142">Элемент **info** содержит структуру [TABLE_NOTIFICATION](table_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="c9e18-142">The **info** member contains an [TABLE_NOTIFICATION](table_notification.md) structure.</span></span> 
    
<span data-ttu-id="c9e18-143">**info**</span><span class="sxs-lookup"><span data-stu-id="c9e18-143">**info**</span></span>
  
> <span data-ttu-id="c9e18-144">Объединение структур уведомлений, описывающих затронутые данные для определенного типа события.</span><span class="sxs-lookup"><span data-stu-id="c9e18-144">Union of notification structures describing the affected data for a particular type of event.</span></span> <span data-ttu-id="c9e18-145">Структура, включенная в элемент **info** , зависит от значения элемента **улевенттипе** .</span><span class="sxs-lookup"><span data-stu-id="c9e18-145">The structure included in the **info** member depends on the value of the **ulEventType** member.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c9e18-146">Примечания</span><span class="sxs-lookup"><span data-stu-id="c9e18-146">Remarks</span></span>

<span data-ttu-id="c9e18-147">Одна или несколько структур **уведомлений** передаются в качестве входных параметров при каждом вызове к зарегистрированному методу [имапиадвисесинк:: OnNotify](imapiadvisesink-onnotify.md) приемника уведомлений.</span><span class="sxs-lookup"><span data-stu-id="c9e18-147">One or more **NOTIFICATION** structures are passed as input parameters with every call to a registered advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="c9e18-148">Структуры **уведомлений** содержат сведения о конкретных событиях, которые произошли, и описывают затронутые объекты.</span><span class="sxs-lookup"><span data-stu-id="c9e18-148">The **NOTIFICATION** structures contain information about the particular events that have occurred and describe the affected objects.</span></span> 
  
<span data-ttu-id="c9e18-149">Прежде чем клиенты или поставщики услуг, получающие уведомление, могут использовать структуру для обработки события, они должны проверить тип события, как указано в элементе **улевенттипе** .</span><span class="sxs-lookup"><span data-stu-id="c9e18-149">Before clients or service providers receiving a notification can use the structure to process the event, they must check the event type as indicated in the **ulEventType** member.</span></span> <span data-ttu-id="c9e18-150">Например, приведенный здесь пример кода проверяет наличие нового сообщения и при обнаружении события такого рода выводит класс сообщения для сообщения.</span><span class="sxs-lookup"><span data-stu-id="c9e18-150">For example, the code sample that is shown here checks for the arrival of a new message and upon detecting an event of this kind, prints out the message class of the message.</span></span> 
  
```cpp
if (pNotif -> ulEventType == fnevNewMail)
{
printf("%s\n", pNotif -> newmail.lpszMessageClass)
}

```

<span data-ttu-id="c9e18-151">Дополнительные сведения об уведомлении можно найти в разделах, приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="c9e18-151">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="c9e18-152">**Статья**</span><span class="sxs-lookup"><span data-stu-id="c9e18-152">**Topic**</span></span>|<span data-ttu-id="c9e18-153">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c9e18-153">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c9e18-154">Уведомление о событии в MAPI</span><span class="sxs-lookup"><span data-stu-id="c9e18-154">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="c9e18-155">Общие сведения о событиях уведомлений и уведомлений.</span><span class="sxs-lookup"><span data-stu-id="c9e18-155">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="c9e18-156">Обработка уведомлений</span><span class="sxs-lookup"><span data-stu-id="c9e18-156">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="c9e18-157">Обсуждение того, как клиенты должны обрабатывать уведомления.</span><span class="sxs-lookup"><span data-stu-id="c9e18-157">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="c9e18-158">Поддержка уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="c9e18-158">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="c9e18-159">Обсуждение того, как поставщики услуг могут использовать метод [имаписуппорт](imapisupportiunknown.md) для создания уведомлений.</span><span class="sxs-lookup"><span data-stu-id="c9e18-159">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c9e18-160">См. также</span><span class="sxs-lookup"><span data-stu-id="c9e18-160">See also</span></span>


- [<span data-ttu-id="c9e18-161">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="c9e18-161">ERROR_NOTIFICATION</span></span>](error_notification.md)  
- [<span data-ttu-id="c9e18-162">EXTENDED_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="c9e18-162">EXTENDED_NOTIFICATION</span></span>](extended_notification.md)  
- [<span data-ttu-id="c9e18-163">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="c9e18-163">NEWMAIL_NOTIFICATION</span></span>](newmail_notification.md)  
- [<span data-ttu-id="c9e18-164">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="c9e18-164">OBJECT_NOTIFICATION</span></span>](object_notification.md)  
- [<span data-ttu-id="c9e18-165">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="c9e18-165">STATUS_OBJECT_NOTIFICATION</span></span>](status_object_notification.md)  
- [<span data-ttu-id="c9e18-166">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="c9e18-166">TABLE_NOTIFICATION</span></span>](table_notification.md)
- [<span data-ttu-id="c9e18-167">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="c9e18-167">MAPI Structures</span></span>](mapi-structures.md)

