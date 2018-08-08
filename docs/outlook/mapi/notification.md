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
ms.openlocfilehash: 7a8d25dc7cac4226f38baab593b254108210549e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810060"
---
# <a name="notification"></a><span data-ttu-id="f5226-103">NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="f5226-103">NOTIFICATION</span></span>
 
<span data-ttu-id="f5226-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f5226-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f5226-105">Содержит сведения о возникновении события и данные, которые были затронуты события.</span><span class="sxs-lookup"><span data-stu-id="f5226-105">Contains information about an event that has occurred and the data that has been affected by the event.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f5226-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="f5226-106">Header file:</span></span>  <br/> |<span data-ttu-id="f5226-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f5226-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="f5226-108">Members</span><span class="sxs-lookup"><span data-stu-id="f5226-108">Members</span></span>

<span data-ttu-id="f5226-109">**ulEventType**</span><span class="sxs-lookup"><span data-stu-id="f5226-109">**ulEventType**</span></span>
  
> <span data-ttu-id="f5226-110">Тип события уведомления, которое происходит.</span><span class="sxs-lookup"><span data-stu-id="f5226-110">Type of notification event that occurred.</span></span> <span data-ttu-id="f5226-111">Значение элемента **ulEventType** соответствует структуре, включенную в **сведения** объединения.</span><span class="sxs-lookup"><span data-stu-id="f5226-111">The value of the **ulEventType** member corresponds to the structure that is included in the **info** union.</span></span> <span data-ttu-id="f5226-112">Элемент **ulEventType** может быть присвоено одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="f5226-112">The **ulEventType** member can be set to one of the following values:</span></span> 
    
 <span data-ttu-id="f5226-113">_fnevCriticalError_</span><span class="sxs-lookup"><span data-stu-id="f5226-113">_fnevCriticalError_</span></span>
  
> <span data-ttu-id="f5226-114">Глобальные ошибка, такие как сеанс, завершите работу в стадии разработки.</span><span class="sxs-lookup"><span data-stu-id="f5226-114">A global error has occurred, such as a session shut down in progress.</span></span> <span data-ttu-id="f5226-115">Член **info** содержит структуру [ERROR_NOTIFICATION](error_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="f5226-115">The **info** member contains an [ERROR_NOTIFICATION](error_notification.md) structure.</span></span> 
    
 <span data-ttu-id="f5226-116">_fnevExtended_</span><span class="sxs-lookup"><span data-stu-id="f5226-116">_fnevExtended_</span></span>
  
> <span data-ttu-id="f5226-117">Внутренний определенные поставщиком услуг конкретного события.</span><span class="sxs-lookup"><span data-stu-id="f5226-117">An internal event defined by a particular service provider has occurred.</span></span> <span data-ttu-id="f5226-118">Член **info** содержит структуру [EXTENDED_NOTIFICATION](extended_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="f5226-118">The **info** member contains an [EXTENDED_NOTIFICATION](extended_notification.md) structure.</span></span> 
    
 <span data-ttu-id="f5226-119">_fnevNewMail_</span><span class="sxs-lookup"><span data-stu-id="f5226-119">_fnevNewMail_</span></span>
  
> <span data-ttu-id="f5226-120">Сообщение было доставлено в соответствующей получать папку для класса сообщений и ожидает обработки.</span><span class="sxs-lookup"><span data-stu-id="f5226-120">A message has been delivered to the appropriate receive folder for the message class and is waiting to be processed.</span></span> <span data-ttu-id="f5226-121">Член **info** содержит структуру [NEWMAIL_NOTIFICATION](newmail_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="f5226-121">The **info** member contains an [NEWMAIL_NOTIFICATION](newmail_notification.md) structure.</span></span> 
    
 <span data-ttu-id="f5226-122">_fnevObjectCopied_</span><span class="sxs-lookup"><span data-stu-id="f5226-122">_fnevObjectCopied_</span></span>
  
> <span data-ttu-id="f5226-123">Объект MAPI был скопирован.</span><span class="sxs-lookup"><span data-stu-id="f5226-123">A MAPI object has been copied.</span></span> <span data-ttu-id="f5226-124">Член **info** содержит структуру [OBJECT_NOTIFICATION](object_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="f5226-124">The **info** member contains an [OBJECT_NOTIFICATION](object_notification.md) structure.</span></span> 
    
 <span data-ttu-id="f5226-125">_fnevObjectCreated_</span><span class="sxs-lookup"><span data-stu-id="f5226-125">_fnevObjectCreated_</span></span>
  
> <span data-ttu-id="f5226-126">Объект MAPI был создан.</span><span class="sxs-lookup"><span data-stu-id="f5226-126">A MAPI object has been created.</span></span> <span data-ttu-id="f5226-127">Член **info** содержит структуру **OBJECT_NOTIFICATION** .</span><span class="sxs-lookup"><span data-stu-id="f5226-127">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="f5226-128">_fnevObjectDeleted_</span><span class="sxs-lookup"><span data-stu-id="f5226-128">_fnevObjectDeleted_</span></span>
  
> <span data-ttu-id="f5226-129">Объект MAPI был удален.</span><span class="sxs-lookup"><span data-stu-id="f5226-129">A MAPI object has been deleted.</span></span> <span data-ttu-id="f5226-130">Член **info** содержит структуру **OBJECT_NOTIFICATION** .</span><span class="sxs-lookup"><span data-stu-id="f5226-130">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="f5226-131">_fnevObjectModified_</span><span class="sxs-lookup"><span data-stu-id="f5226-131">_fnevObjectModified_</span></span>
  
> <span data-ttu-id="f5226-132">Объект MAPI был изменен.</span><span class="sxs-lookup"><span data-stu-id="f5226-132">A MAPI object has changed.</span></span> <span data-ttu-id="f5226-133">Член **info** содержит структуру **OBJECT_NOTIFICATION** .</span><span class="sxs-lookup"><span data-stu-id="f5226-133">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="f5226-134">_fnevObjectMoved_</span><span class="sxs-lookup"><span data-stu-id="f5226-134">_fnevObjectMoved_</span></span>
  
> <span data-ttu-id="f5226-135">Хранение сообщений или адрес был перемещен объект книги.</span><span class="sxs-lookup"><span data-stu-id="f5226-135">A message store or address book object has been moved.</span></span> <span data-ttu-id="f5226-136">Член **info** содержит структуру **OBJECT_NOTIFICATION** .</span><span class="sxs-lookup"><span data-stu-id="f5226-136">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="f5226-137">_fnevSearchComplete_</span><span class="sxs-lookup"><span data-stu-id="f5226-137">_fnevSearchComplete_</span></span>
  
> <span data-ttu-id="f5226-138">Результаты доступны и завершения операции поиска.</span><span class="sxs-lookup"><span data-stu-id="f5226-138">A search operation has finished and the results are available.</span></span> <span data-ttu-id="f5226-139">Член **info** содержит структуру **OBJECT_NOTIFICATION** .</span><span class="sxs-lookup"><span data-stu-id="f5226-139">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="f5226-140">_fnevTableModified_</span><span class="sxs-lookup"><span data-stu-id="f5226-140">_fnevTableModified_</span></span>
  
> <span data-ttu-id="f5226-141">Сведения в таблице, была изменена.</span><span class="sxs-lookup"><span data-stu-id="f5226-141">Information in a table has changed.</span></span> <span data-ttu-id="f5226-142">Член **info** содержит структуру [TABLE_NOTIFICATION](table_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="f5226-142">The **info** member contains an [TABLE_NOTIFICATION](table_notification.md) structure.</span></span> 
    
<span data-ttu-id="f5226-143">**сведения о**</span><span class="sxs-lookup"><span data-stu-id="f5226-143">**info**</span></span>
  
> <span data-ttu-id="f5226-144">Объединение структур уведомлений, описывающих затронутых данных для конкретного типа событий.</span><span class="sxs-lookup"><span data-stu-id="f5226-144">Union of notification structures describing the affected data for a particular type of event.</span></span> <span data-ttu-id="f5226-145">Структура, включенных в член **info** зависит от значение элемента **ulEventType** .</span><span class="sxs-lookup"><span data-stu-id="f5226-145">The structure included in the **info** member depends on the value of the **ulEventType** member.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="f5226-146">Замечания</span><span class="sxs-lookup"><span data-stu-id="f5226-146">Remarks</span></span>

<span data-ttu-id="f5226-147">Один или несколько **УВЕДОМЛЕНИЙ** , структуры, передаются в качестве входных параметров с каждым вызовом метода [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) приемник зарегистрированных уведомлений.</span><span class="sxs-lookup"><span data-stu-id="f5226-147">One or more **NOTIFICATION** structures are passed as input parameters with every call to a registered advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="f5226-148">Структур **УВЕДОМЛЕНИЙ** содержат сведения о конкретных событий, которые происходили и описания затронутые объекты.</span><span class="sxs-lookup"><span data-stu-id="f5226-148">The **NOTIFICATION** structures contain information about the particular events that have occurred and describe the affected objects.</span></span> 
  
<span data-ttu-id="f5226-149">Перед клиентов или поставщиков услуг, получении уведомления можно использовать структуры для обработки событий, их необходимо проверить тип события, указанного в элемент **ulEventType** .</span><span class="sxs-lookup"><span data-stu-id="f5226-149">Before clients or service providers receiving a notification can use the structure to process the event, they must check the event type as indicated in the **ulEventType** member.</span></span> <span data-ttu-id="f5226-150">Например в образце кода, приведенные здесь проверяет наличие поступления нового сообщения и при обнаружении события этого типа выводит данные об класса сообщений для сообщения.</span><span class="sxs-lookup"><span data-stu-id="f5226-150">For example, the code sample that is shown here checks for the arrival of a new message and upon detecting an event of this kind, prints out the message class of the message.</span></span> 
  
```cpp
if (pNotif -> ulEventType == fnevNewMail)
{
printf("%s\n", pNotif -> newmail.lpszMessageClass)
}

```

<span data-ttu-id="f5226-151">Дополнительные сведения о уведомлений видеть темы, описанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="f5226-151">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="f5226-152">**Статья**</span><span class="sxs-lookup"><span data-stu-id="f5226-152">**Topic**</span></span>|<span data-ttu-id="f5226-153">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f5226-153">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f5226-154">Уведомление о событиях в MAPI</span><span class="sxs-lookup"><span data-stu-id="f5226-154">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="f5226-155">Общий обзор уведомлений и события уведомления.</span><span class="sxs-lookup"><span data-stu-id="f5226-155">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="f5226-156">Обработка уведомлений</span><span class="sxs-lookup"><span data-stu-id="f5226-156">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="f5226-157">Обсуждение как клиенты должны обрабатывать уведомления.</span><span class="sxs-lookup"><span data-stu-id="f5226-157">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="f5226-158">Поддержка уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="f5226-158">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="f5226-159">Обсуждение того, как поставщиков услуг можно использовать метод [IMAPISupport](imapisupportiunknown.md) для создания уведомлений.</span><span class="sxs-lookup"><span data-stu-id="f5226-159">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f5226-160">См. также</span><span class="sxs-lookup"><span data-stu-id="f5226-160">See also</span></span>


- [<span data-ttu-id="f5226-161">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="f5226-161">ERROR_NOTIFICATION</span></span>](error_notification.md)  
- [<span data-ttu-id="f5226-162">EXTENDED_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="f5226-162">EXTENDED_NOTIFICATION</span></span>](extended_notification.md)  
- [<span data-ttu-id="f5226-163">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="f5226-163">NEWMAIL_NOTIFICATION</span></span>](newmail_notification.md)  
- [<span data-ttu-id="f5226-164">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="f5226-164">OBJECT_NOTIFICATION</span></span>](object_notification.md)  
- [<span data-ttu-id="f5226-165">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="f5226-165">STATUS_OBJECT_NOTIFICATION</span></span>](status_object_notification.md)  
- [<span data-ttu-id="f5226-166">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="f5226-166">TABLE_NOTIFICATION</span></span>](table_notification.md)
- [<span data-ttu-id="f5226-167">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="f5226-167">MAPI Structures</span></span>](mapi-structures.md)

