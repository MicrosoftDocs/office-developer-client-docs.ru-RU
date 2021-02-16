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
# <a name="notification"></a><span data-ttu-id="8de5f-103">NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="8de5f-103">NOTIFICATION</span></span>
 
<span data-ttu-id="8de5f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8de5f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8de5f-105">Содержит сведения о событии, которое произошло, и данных, которые были затронуты этим событием.</span><span class="sxs-lookup"><span data-stu-id="8de5f-105">Contains information about an event that has occurred and the data that has been affected by the event.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8de5f-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="8de5f-106">Header file:</span></span>  <br/> |<span data-ttu-id="8de5f-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8de5f-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="8de5f-108">"Участники"</span><span class="sxs-lookup"><span data-stu-id="8de5f-108">Members</span></span>

<span data-ttu-id="8de5f-109">**ulEventType**</span><span class="sxs-lookup"><span data-stu-id="8de5f-109">**ulEventType**</span></span>
  
> <span data-ttu-id="8de5f-110">Тип события уведомления, которое произошло.</span><span class="sxs-lookup"><span data-stu-id="8de5f-110">Type of notification event that occurred.</span></span> <span data-ttu-id="8de5f-111">Значение члена **ulEventType** соответствует структуре, включенной в **объединение данных.**</span><span class="sxs-lookup"><span data-stu-id="8de5f-111">The value of the **ulEventType** member corresponds to the structure that is included in the **info** union.</span></span> <span data-ttu-id="8de5f-112">Для **члена ulEventType** можно установить одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="8de5f-112">The **ulEventType** member can be set to one of the following values:</span></span> 
    
 <span data-ttu-id="8de5f-113">_fnevCriticalError_</span><span class="sxs-lookup"><span data-stu-id="8de5f-113">_fnevCriticalError_</span></span>
  
> <span data-ttu-id="8de5f-114">Произошла глобальная ошибка, например завершение сеанса.</span><span class="sxs-lookup"><span data-stu-id="8de5f-114">A global error has occurred, such as a session shut down in progress.</span></span> <span data-ttu-id="8de5f-115">Член **info** содержит структуру [ERROR_NOTIFICATION](error_notification.md) данных.</span><span class="sxs-lookup"><span data-stu-id="8de5f-115">The **info** member contains an [ERROR_NOTIFICATION](error_notification.md) structure.</span></span> 
    
 <span data-ttu-id="8de5f-116">_fnevExtended_</span><span class="sxs-lookup"><span data-stu-id="8de5f-116">_fnevExtended_</span></span>
  
> <span data-ttu-id="8de5f-117">Произошло внутреннее событие, определенное определенным поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="8de5f-117">An internal event defined by a particular service provider has occurred.</span></span> <span data-ttu-id="8de5f-118">Член **info** содержит структуру [EXTENDED_NOTIFICATION](extended_notification.md) данных.</span><span class="sxs-lookup"><span data-stu-id="8de5f-118">The **info** member contains an [EXTENDED_NOTIFICATION](extended_notification.md) structure.</span></span> 
    
 <span data-ttu-id="8de5f-119">_fnevNewMail_</span><span class="sxs-lookup"><span data-stu-id="8de5f-119">_fnevNewMail_</span></span>
  
> <span data-ttu-id="8de5f-120">Сообщение доставлено в соответствующую папку получения для класса сообщений и ожидает обработки.</span><span class="sxs-lookup"><span data-stu-id="8de5f-120">A message has been delivered to the appropriate receive folder for the message class and is waiting to be processed.</span></span> <span data-ttu-id="8de5f-121">Член **info** содержит структуру [NEWMAIL_NOTIFICATION](newmail_notification.md) данных.</span><span class="sxs-lookup"><span data-stu-id="8de5f-121">The **info** member contains an [NEWMAIL_NOTIFICATION](newmail_notification.md) structure.</span></span> 
    
 <span data-ttu-id="8de5f-122">_fnevObjectCopied_</span><span class="sxs-lookup"><span data-stu-id="8de5f-122">_fnevObjectCopied_</span></span>
  
> <span data-ttu-id="8de5f-123">Объект MAPI был скопирован.</span><span class="sxs-lookup"><span data-stu-id="8de5f-123">A MAPI object has been copied.</span></span> <span data-ttu-id="8de5f-124">Член **info** содержит структуру [OBJECT_NOTIFICATION](object_notification.md) данных.</span><span class="sxs-lookup"><span data-stu-id="8de5f-124">The **info** member contains an [OBJECT_NOTIFICATION](object_notification.md) structure.</span></span> 
    
 <span data-ttu-id="8de5f-125">_fnevObjectCreated_</span><span class="sxs-lookup"><span data-stu-id="8de5f-125">_fnevObjectCreated_</span></span>
  
> <span data-ttu-id="8de5f-126">Создан объект MAPI.</span><span class="sxs-lookup"><span data-stu-id="8de5f-126">A MAPI object has been created.</span></span> <span data-ttu-id="8de5f-127">Член **info** содержит структуру **OBJECT_NOTIFICATION** данных.</span><span class="sxs-lookup"><span data-stu-id="8de5f-127">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="8de5f-128">_fnevObjectDeleted_</span><span class="sxs-lookup"><span data-stu-id="8de5f-128">_fnevObjectDeleted_</span></span>
  
> <span data-ttu-id="8de5f-129">Объект MAPI удален.</span><span class="sxs-lookup"><span data-stu-id="8de5f-129">A MAPI object has been deleted.</span></span> <span data-ttu-id="8de5f-130">Член **info** содержит структуру **OBJECT_NOTIFICATION** данных.</span><span class="sxs-lookup"><span data-stu-id="8de5f-130">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="8de5f-131">_fnevObjectModified_</span><span class="sxs-lookup"><span data-stu-id="8de5f-131">_fnevObjectModified_</span></span>
  
> <span data-ttu-id="8de5f-132">Объект MAPI изменился.</span><span class="sxs-lookup"><span data-stu-id="8de5f-132">A MAPI object has changed.</span></span> <span data-ttu-id="8de5f-133">Член **info** содержит структуру **OBJECT_NOTIFICATION** данных.</span><span class="sxs-lookup"><span data-stu-id="8de5f-133">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="8de5f-134">_fnevObjectMoved_</span><span class="sxs-lookup"><span data-stu-id="8de5f-134">_fnevObjectMoved_</span></span>
  
> <span data-ttu-id="8de5f-135">Хранилище сообщений или объект адресной книги перемещены.</span><span class="sxs-lookup"><span data-stu-id="8de5f-135">A message store or address book object has been moved.</span></span> <span data-ttu-id="8de5f-136">Член **info** содержит структуру **OBJECT_NOTIFICATION** данных.</span><span class="sxs-lookup"><span data-stu-id="8de5f-136">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="8de5f-137">_fnevSearchComplete_</span><span class="sxs-lookup"><span data-stu-id="8de5f-137">_fnevSearchComplete_</span></span>
  
> <span data-ttu-id="8de5f-138">Операция поиска завершена, и результаты доступны.</span><span class="sxs-lookup"><span data-stu-id="8de5f-138">A search operation has finished and the results are available.</span></span> <span data-ttu-id="8de5f-139">Член **info** содержит структуру **OBJECT_NOTIFICATION** данных.</span><span class="sxs-lookup"><span data-stu-id="8de5f-139">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="8de5f-140">_fnevTableModified_</span><span class="sxs-lookup"><span data-stu-id="8de5f-140">_fnevTableModified_</span></span>
  
> <span data-ttu-id="8de5f-141">Сведения в таблице изменились.</span><span class="sxs-lookup"><span data-stu-id="8de5f-141">Information in a table has changed.</span></span> <span data-ttu-id="8de5f-142">Член **info** содержит структуру [TABLE_NOTIFICATION](table_notification.md) данных.</span><span class="sxs-lookup"><span data-stu-id="8de5f-142">The **info** member contains an [TABLE_NOTIFICATION](table_notification.md) structure.</span></span> 
    
<span data-ttu-id="8de5f-143">**info**</span><span class="sxs-lookup"><span data-stu-id="8de5f-143">**info**</span></span>
  
> <span data-ttu-id="8de5f-144">Объединение структур уведомлений, описывающих затронутые данные для конкретного типа события.</span><span class="sxs-lookup"><span data-stu-id="8de5f-144">Union of notification structures describing the affected data for a particular type of event.</span></span> <span data-ttu-id="8de5f-145">Структура, включенная в **член данных,** зависит от значения **члена ulEventType.**</span><span class="sxs-lookup"><span data-stu-id="8de5f-145">The structure included in the **info** member depends on the value of the **ulEventType** member.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="8de5f-146">Примечания</span><span class="sxs-lookup"><span data-stu-id="8de5f-146">Remarks</span></span>

<span data-ttu-id="8de5f-147">Одна или несколько **структур NOTIFICATION** передаются в качестве входных параметров при каждом вызове метода [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) зарегистрированного приемника уведомлений.</span><span class="sxs-lookup"><span data-stu-id="8de5f-147">One or more **NOTIFICATION** structures are passed as input parameters with every call to a registered advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="8de5f-148">Структуры **УВЕДОМЛЕНий** содержат сведения о конкретных событиях, которые произошли, и описывают затронутые объекты.</span><span class="sxs-lookup"><span data-stu-id="8de5f-148">The **NOTIFICATION** structures contain information about the particular events that have occurred and describe the affected objects.</span></span> 
  
<span data-ttu-id="8de5f-149">Прежде чем клиенты или поставщики услуг, получающие уведомление, смогут использовать структуру для обработки события, они должны проверить тип события, как указано в члене **ulEventType.**</span><span class="sxs-lookup"><span data-stu-id="8de5f-149">Before clients or service providers receiving a notification can use the structure to process the event, they must check the event type as indicated in the **ulEventType** member.</span></span> <span data-ttu-id="8de5f-150">Например, показанный здесь пример кода проверяет наличие нового сообщения и при обнаружении события такого типа распечатает класс сообщения.</span><span class="sxs-lookup"><span data-stu-id="8de5f-150">For example, the code sample that is shown here checks for the arrival of a new message and upon detecting an event of this kind, prints out the message class of the message.</span></span> 
  
```cpp
if (pNotif -> ulEventType == fnevNewMail)
{
printf("%s\n", pNotif -> newmail.lpszMessageClass)
}

```

<span data-ttu-id="8de5f-151">Дополнительные сведения об уведомлении см. в темах, описанных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="8de5f-151">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="8de5f-152">**Статья**</span><span class="sxs-lookup"><span data-stu-id="8de5f-152">**Topic**</span></span>|<span data-ttu-id="8de5f-153">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8de5f-153">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8de5f-154">Уведомление о событии в MAPI</span><span class="sxs-lookup"><span data-stu-id="8de5f-154">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="8de5f-155">Общий обзор событий уведомлений и уведомлений.</span><span class="sxs-lookup"><span data-stu-id="8de5f-155">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="8de5f-156">Обработка уведомлений</span><span class="sxs-lookup"><span data-stu-id="8de5f-156">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="8de5f-157">Обсуждение того, как клиенты должны обрабатывать уведомления.</span><span class="sxs-lookup"><span data-stu-id="8de5f-157">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="8de5f-158">Поддержка уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="8de5f-158">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="8de5f-159">Обсуждение того, как поставщики служб могут использовать метод [IMAPISupport](imapisupportiunknown.md) для создания уведомлений.</span><span class="sxs-lookup"><span data-stu-id="8de5f-159">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8de5f-160">См. также</span><span class="sxs-lookup"><span data-stu-id="8de5f-160">See also</span></span>


- [<span data-ttu-id="8de5f-161">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="8de5f-161">ERROR_NOTIFICATION</span></span>](error_notification.md)  
- [<span data-ttu-id="8de5f-162">EXTENDED_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="8de5f-162">EXTENDED_NOTIFICATION</span></span>](extended_notification.md)  
- [<span data-ttu-id="8de5f-163">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="8de5f-163">NEWMAIL_NOTIFICATION</span></span>](newmail_notification.md)  
- [<span data-ttu-id="8de5f-164">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="8de5f-164">OBJECT_NOTIFICATION</span></span>](object_notification.md)  
- [<span data-ttu-id="8de5f-165">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="8de5f-165">STATUS_OBJECT_NOTIFICATION</span></span>](status_object_notification.md)  
- [<span data-ttu-id="8de5f-166">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="8de5f-166">TABLE_NOTIFICATION</span></span>](table_notification.md)
- [<span data-ttu-id="8de5f-167">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="8de5f-167">MAPI Structures</span></span>](mapi-structures.md)

