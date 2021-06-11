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
# <a name="notification"></a><span data-ttu-id="39273-103">NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="39273-103">NOTIFICATION</span></span>
 
<span data-ttu-id="39273-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="39273-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="39273-105">Содержит сведения о произошедшем событии и данных, на которые повлияло событие.</span><span class="sxs-lookup"><span data-stu-id="39273-105">Contains information about an event that has occurred and the data that has been affected by the event.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="39273-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="39273-106">Header file:</span></span>  <br/> |<span data-ttu-id="39273-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="39273-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="39273-108">"Участники"</span><span class="sxs-lookup"><span data-stu-id="39273-108">Members</span></span>

<span data-ttu-id="39273-109">**ulEventType**</span><span class="sxs-lookup"><span data-stu-id="39273-109">**ulEventType**</span></span>
  
> <span data-ttu-id="39273-110">Тип события уведомления, которое произошло.</span><span class="sxs-lookup"><span data-stu-id="39273-110">Type of notification event that occurred.</span></span> <span data-ttu-id="39273-111">Значение члена **ulEventType** соответствует структуре, включенной в **информационное** объединение.</span><span class="sxs-lookup"><span data-stu-id="39273-111">The value of the **ulEventType** member corresponds to the structure that is included in the **info** union.</span></span> <span data-ttu-id="39273-112">Член **ulEventType** может быть назначен одному из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="39273-112">The **ulEventType** member can be set to one of the following values:</span></span> 
    
 <span data-ttu-id="39273-113">_fnevCriticalError_</span><span class="sxs-lookup"><span data-stu-id="39273-113">_fnevCriticalError_</span></span>
  
> <span data-ttu-id="39273-114">Произошла глобальная ошибка, например завершение сеанса.</span><span class="sxs-lookup"><span data-stu-id="39273-114">A global error has occurred, such as a session shut down in progress.</span></span> <span data-ttu-id="39273-115">Член **info** содержит [структуру ERROR_NOTIFICATION.](error_notification.md)</span><span class="sxs-lookup"><span data-stu-id="39273-115">The **info** member contains an [ERROR_NOTIFICATION](error_notification.md) structure.</span></span> 
    
 <span data-ttu-id="39273-116">_fnevExtended_</span><span class="sxs-lookup"><span data-stu-id="39273-116">_fnevExtended_</span></span>
  
> <span data-ttu-id="39273-117">Произошло внутреннее событие, определенное конкретным поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="39273-117">An internal event defined by a particular service provider has occurred.</span></span> <span data-ttu-id="39273-118">Член **info** содержит [структуру EXTENDED_NOTIFICATION.](extended_notification.md)</span><span class="sxs-lookup"><span data-stu-id="39273-118">The **info** member contains an [EXTENDED_NOTIFICATION](extended_notification.md) structure.</span></span> 
    
 <span data-ttu-id="39273-119">_fnevNewMail_</span><span class="sxs-lookup"><span data-stu-id="39273-119">_fnevNewMail_</span></span>
  
> <span data-ttu-id="39273-120">Сообщение доставлено в соответствующую папку получения для класса сообщений и ожидает обработки.</span><span class="sxs-lookup"><span data-stu-id="39273-120">A message has been delivered to the appropriate receive folder for the message class and is waiting to be processed.</span></span> <span data-ttu-id="39273-121">Член **info** содержит [структуру NEWMAIL_NOTIFICATION.](newmail_notification.md)</span><span class="sxs-lookup"><span data-stu-id="39273-121">The **info** member contains an [NEWMAIL_NOTIFICATION](newmail_notification.md) structure.</span></span> 
    
 <span data-ttu-id="39273-122">_fnevObjectCopied_</span><span class="sxs-lookup"><span data-stu-id="39273-122">_fnevObjectCopied_</span></span>
  
> <span data-ttu-id="39273-123">Скопирован объект MAPI.</span><span class="sxs-lookup"><span data-stu-id="39273-123">A MAPI object has been copied.</span></span> <span data-ttu-id="39273-124">Член **info** содержит [структуру OBJECT_NOTIFICATION.](object_notification.md)</span><span class="sxs-lookup"><span data-stu-id="39273-124">The **info** member contains an [OBJECT_NOTIFICATION](object_notification.md) structure.</span></span> 
    
 <span data-ttu-id="39273-125">_fnevObjectCreated_</span><span class="sxs-lookup"><span data-stu-id="39273-125">_fnevObjectCreated_</span></span>
  
> <span data-ttu-id="39273-126">Создан объект MAPI.</span><span class="sxs-lookup"><span data-stu-id="39273-126">A MAPI object has been created.</span></span> <span data-ttu-id="39273-127">Член **info** содержит **структуру OBJECT_NOTIFICATION.**</span><span class="sxs-lookup"><span data-stu-id="39273-127">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="39273-128">_fnevObjectDeleted_</span><span class="sxs-lookup"><span data-stu-id="39273-128">_fnevObjectDeleted_</span></span>
  
> <span data-ttu-id="39273-129">Объект MAPI удален.</span><span class="sxs-lookup"><span data-stu-id="39273-129">A MAPI object has been deleted.</span></span> <span data-ttu-id="39273-130">Член **info** содержит **структуру OBJECT_NOTIFICATION.**</span><span class="sxs-lookup"><span data-stu-id="39273-130">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="39273-131">_fnevObjectModified_</span><span class="sxs-lookup"><span data-stu-id="39273-131">_fnevObjectModified_</span></span>
  
> <span data-ttu-id="39273-132">Объект MAPI изменился.</span><span class="sxs-lookup"><span data-stu-id="39273-132">A MAPI object has changed.</span></span> <span data-ttu-id="39273-133">Член **info** содержит **структуру OBJECT_NOTIFICATION.**</span><span class="sxs-lookup"><span data-stu-id="39273-133">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="39273-134">_fnevObjectMoved_</span><span class="sxs-lookup"><span data-stu-id="39273-134">_fnevObjectMoved_</span></span>
  
> <span data-ttu-id="39273-135">Перенесено хранилище сообщений или объект адресной книги.</span><span class="sxs-lookup"><span data-stu-id="39273-135">A message store or address book object has been moved.</span></span> <span data-ttu-id="39273-136">Член **info** содержит **структуру OBJECT_NOTIFICATION.**</span><span class="sxs-lookup"><span data-stu-id="39273-136">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="39273-137">_fnevSearchComplete_</span><span class="sxs-lookup"><span data-stu-id="39273-137">_fnevSearchComplete_</span></span>
  
> <span data-ttu-id="39273-138">Операция поиска завершена, и результаты доступны.</span><span class="sxs-lookup"><span data-stu-id="39273-138">A search operation has finished and the results are available.</span></span> <span data-ttu-id="39273-139">Член **info** содержит **структуру OBJECT_NOTIFICATION.**</span><span class="sxs-lookup"><span data-stu-id="39273-139">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="39273-140">_fnevTableModified_</span><span class="sxs-lookup"><span data-stu-id="39273-140">_fnevTableModified_</span></span>
  
> <span data-ttu-id="39273-141">Сведения в таблице изменились.</span><span class="sxs-lookup"><span data-stu-id="39273-141">Information in a table has changed.</span></span> <span data-ttu-id="39273-142">Член **info** содержит [структуру TABLE_NOTIFICATION.](table_notification.md)</span><span class="sxs-lookup"><span data-stu-id="39273-142">The **info** member contains an [TABLE_NOTIFICATION](table_notification.md) structure.</span></span> 
    
<span data-ttu-id="39273-143">**info**</span><span class="sxs-lookup"><span data-stu-id="39273-143">**info**</span></span>
  
> <span data-ttu-id="39273-144">Объединение структур уведомлений, описывающих затронутые данные для определенного типа события.</span><span class="sxs-lookup"><span data-stu-id="39273-144">Union of notification structures describing the affected data for a particular type of event.</span></span> <span data-ttu-id="39273-145">Структура, включенная в **член info,** зависит от значения члена **ulEventType.**</span><span class="sxs-lookup"><span data-stu-id="39273-145">The structure included in the **info** member depends on the value of the **ulEventType** member.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="39273-146">Примечания</span><span class="sxs-lookup"><span data-stu-id="39273-146">Remarks</span></span>

<span data-ttu-id="39273-147">Одна или несколько **структур УВЕДОМЛЕНий** передаются в качестве параметров ввода с каждым вызовом в зарегистрированный метод [IMAPIAdviseSink::OnNotify.](imapiadvisesink-onnotify.md)</span><span class="sxs-lookup"><span data-stu-id="39273-147">One or more **NOTIFICATION** structures are passed as input parameters with every call to a registered advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="39273-148">Структуры **УВЕДОМЛЕНий** содержат сведения о конкретных событиях, которые произошли, и описывают затронутые объекты.</span><span class="sxs-lookup"><span data-stu-id="39273-148">The **NOTIFICATION** structures contain information about the particular events that have occurred and describe the affected objects.</span></span> 
  
<span data-ttu-id="39273-149">Прежде чем клиенты или поставщики услуг, получающие уведомление, смогут использовать структуру для обработки события, они должны проверить тип события, указанный в члене **ulEventType.**</span><span class="sxs-lookup"><span data-stu-id="39273-149">Before clients or service providers receiving a notification can use the structure to process the event, they must check the event type as indicated in the **ulEventType** member.</span></span> <span data-ttu-id="39273-150">Например, пример кода, показанный здесь, проверяет прибытие нового сообщения и при обнаружении события подобного рода распечатывает класс сообщения сообщения.</span><span class="sxs-lookup"><span data-stu-id="39273-150">For example, the code sample that is shown here checks for the arrival of a new message and upon detecting an event of this kind, prints out the message class of the message.</span></span> 
  
```cpp
if (pNotif -> ulEventType == fnevNewMail)
{
printf("%s\n", pNotif -> newmail.lpszMessageClass)
}

```

<span data-ttu-id="39273-151">Дополнительные сведения об уведомлении см. в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="39273-151">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="39273-152">**Статья**</span><span class="sxs-lookup"><span data-stu-id="39273-152">**Topic**</span></span>|<span data-ttu-id="39273-153">**Описание**</span><span class="sxs-lookup"><span data-stu-id="39273-153">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="39273-154">Уведомление о событиях в MAPI</span><span class="sxs-lookup"><span data-stu-id="39273-154">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="39273-155">Общий обзор событий уведомлений и уведомлений.</span><span class="sxs-lookup"><span data-stu-id="39273-155">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="39273-156">Обработка уведомлений</span><span class="sxs-lookup"><span data-stu-id="39273-156">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="39273-157">Обсуждение того, как клиенты должны обрабатывать уведомления.</span><span class="sxs-lookup"><span data-stu-id="39273-157">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="39273-158">Поддержка уведомления о событиях</span><span class="sxs-lookup"><span data-stu-id="39273-158">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="39273-159">Обсуждение того, как поставщики услуг могут использовать [метод IMAPISupport](imapisupportiunknown.md) для создания уведомлений.</span><span class="sxs-lookup"><span data-stu-id="39273-159">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="39273-160">См. также</span><span class="sxs-lookup"><span data-stu-id="39273-160">See also</span></span>


- [<span data-ttu-id="39273-161">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="39273-161">ERROR_NOTIFICATION</span></span>](error_notification.md)  
- [<span data-ttu-id="39273-162">EXTENDED_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="39273-162">EXTENDED_NOTIFICATION</span></span>](extended_notification.md)  
- [<span data-ttu-id="39273-163">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="39273-163">NEWMAIL_NOTIFICATION</span></span>](newmail_notification.md)  
- [<span data-ttu-id="39273-164">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="39273-164">OBJECT_NOTIFICATION</span></span>](object_notification.md)  
- [<span data-ttu-id="39273-165">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="39273-165">STATUS_OBJECT_NOTIFICATION</span></span>](status_object_notification.md)  
- [<span data-ttu-id="39273-166">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="39273-166">TABLE_NOTIFICATION</span></span>](table_notification.md)
- [<span data-ttu-id="39273-167">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="39273-167">MAPI Structures</span></span>](mapi-structures.md)

