---
title: OBJECT_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OBJECT_NOTIFICATION
api_type:
- COM
ms.assetid: de3a2297-e0cc-427b-a978-52bade4d9bce
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 876c8fc3667929e3c2e7403e71e6d392981d34f1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573357"
---
# <a name="objectnotification"></a><span data-ttu-id="be28c-103">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="be28c-103">OBJECT_NOTIFICATION</span></span>

  
  
<span data-ttu-id="be28c-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="be28c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="be28c-105">Содержит сведения об объекте, который внесено изменение, например, копирование или изменены.</span><span class="sxs-lookup"><span data-stu-id="be28c-105">Contains information about an object that has undergone a change, such as being copied or modified.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="be28c-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="be28c-106">Header file:</span></span>  <br/> |<span data-ttu-id="be28c-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="be28c-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _OBJECT_NOTIFICATION
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  ULONG ulObjType;
  ULONG cbParentID;
  LPENTRYID lpParentID;
  ULONG cbOldID;
  LPENTRYID lpOldID;
  ULONG cbOldParentID;
  LPENTRYID lpOldParentID;
  LPSPropTagArray lpPropTagArray;
} OBJECT_NOTIFICATION;

```

## <a name="members"></a><span data-ttu-id="be28c-108">Members</span><span class="sxs-lookup"><span data-stu-id="be28c-108">Members</span></span>

 <span data-ttu-id="be28c-109">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="be28c-109">**cbEntryID**</span></span>
  
> <span data-ttu-id="be28c-110">Число байт в идентификаторе запись, на который указывает член **lpEntryID** .</span><span class="sxs-lookup"><span data-stu-id="be28c-110">Count of bytes in the entry identifier pointed to by the **lpEntryID** member.</span></span> 
    
 <span data-ttu-id="be28c-111">**lpEntryID**</span><span class="sxs-lookup"><span data-stu-id="be28c-111">**lpEntryID**</span></span>
  
> <span data-ttu-id="be28c-112">Указатель на идентификатор записи затронутых объекта.</span><span class="sxs-lookup"><span data-stu-id="be28c-112">Pointer to the entry identifier of the affected object.</span></span>
    
 <span data-ttu-id="be28c-113">**ulObjType**</span><span class="sxs-lookup"><span data-stu-id="be28c-113">**ulObjType**</span></span>
  
> <span data-ttu-id="be28c-114">Тип объекта, связанного.</span><span class="sxs-lookup"><span data-stu-id="be28c-114">Type of object affected.</span></span> <span data-ttu-id="be28c-115">Ниже приведены возможные типы:</span><span class="sxs-lookup"><span data-stu-id="be28c-115">Possible types are as follows:</span></span>
    
<span data-ttu-id="be28c-116">MAPI_STORE</span><span class="sxs-lookup"><span data-stu-id="be28c-116">MAPI_STORE</span></span> 
  
> <span data-ttu-id="be28c-117">Хранение сообщений.</span><span class="sxs-lookup"><span data-stu-id="be28c-117">Message store.</span></span> 
    
<span data-ttu-id="be28c-118">MAPI_ADDRBOOK</span><span class="sxs-lookup"><span data-stu-id="be28c-118">MAPI_ADDRBOOK</span></span> 
  
> <span data-ttu-id="be28c-119">Список адресов.</span><span class="sxs-lookup"><span data-stu-id="be28c-119">Address book.</span></span> 
    
<span data-ttu-id="be28c-120">MAPI_FOLDER</span><span class="sxs-lookup"><span data-stu-id="be28c-120">MAPI_FOLDER</span></span> 
  
> <span data-ttu-id="be28c-121">Папка.</span><span class="sxs-lookup"><span data-stu-id="be28c-121">Folder.</span></span>
    
<span data-ttu-id="be28c-122">MAPI_ABCONT</span><span class="sxs-lookup"><span data-stu-id="be28c-122">MAPI_ABCONT</span></span> 
  
> <span data-ttu-id="be28c-123">Контейнер адресной книги.</span><span class="sxs-lookup"><span data-stu-id="be28c-123">Address book container.</span></span>
    
<span data-ttu-id="be28c-124">MAPI_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="be28c-124">MAPI_MESSAGE</span></span> 
  
> <span data-ttu-id="be28c-125">Сообщение.</span><span class="sxs-lookup"><span data-stu-id="be28c-125">Message.</span></span>
    
<span data-ttu-id="be28c-126">MAPI_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="be28c-126">MAPI_MAILUSER</span></span> 
  
> <span data-ttu-id="be28c-127">Пользователь, обмена мгновенными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="be28c-127">Messaging user.</span></span>
    
<span data-ttu-id="be28c-128">MAPI_ATTACH</span><span class="sxs-lookup"><span data-stu-id="be28c-128">MAPI_ATTACH</span></span> 
  
> <span data-ttu-id="be28c-129">Вложение.</span><span class="sxs-lookup"><span data-stu-id="be28c-129">Attachment.</span></span>
    
<span data-ttu-id="be28c-130">MAPI_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="be28c-130">MAPI_DISTLIST</span></span> 
  
> <span data-ttu-id="be28c-131">Список рассылки.</span><span class="sxs-lookup"><span data-stu-id="be28c-131">Distribution list.</span></span>
    
<span data-ttu-id="be28c-132">MAPI_PROFSECT</span><span class="sxs-lookup"><span data-stu-id="be28c-132">MAPI_PROFSECT</span></span> 
  
> <span data-ttu-id="be28c-133">Раздел профиля.</span><span class="sxs-lookup"><span data-stu-id="be28c-133">Profile section.</span></span>
    
<span data-ttu-id="be28c-134">MAPI_STATUS</span><span class="sxs-lookup"><span data-stu-id="be28c-134">MAPI_STATUS</span></span> 
  
> <span data-ttu-id="be28c-135">Состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="be28c-135">Status object.</span></span>
    
<span data-ttu-id="be28c-136">MAPI_SESSION</span><span class="sxs-lookup"><span data-stu-id="be28c-136">MAPI_SESSION</span></span> 
  
> <span data-ttu-id="be28c-137">Объект сеанса.</span><span class="sxs-lookup"><span data-stu-id="be28c-137">Session object.</span></span>
    
 <span data-ttu-id="be28c-138">**cbParentID**</span><span class="sxs-lookup"><span data-stu-id="be28c-138">**cbParentID**</span></span>
  
> <span data-ttu-id="be28c-139">Число байт в идентификаторе запись, на который указывает член **lpParentID** .</span><span class="sxs-lookup"><span data-stu-id="be28c-139">Count of bytes in the entry identifier pointed to by the **lpParentID** member.</span></span> 
    
 <span data-ttu-id="be28c-140">**lpParentID**</span><span class="sxs-lookup"><span data-stu-id="be28c-140">**lpParentID**</span></span>
  
> <span data-ttu-id="be28c-141">Указатель на идентификатор записи родительского объекта затронутых.</span><span class="sxs-lookup"><span data-stu-id="be28c-141">Pointer to the entry identifier of the parent of the affected object.</span></span>
    
 <span data-ttu-id="be28c-142">**cbOldID**</span><span class="sxs-lookup"><span data-stu-id="be28c-142">**cbOldID**</span></span>
  
> <span data-ttu-id="be28c-143">Число байт в идентификаторе запись, на который указывает член **lpOldID** .</span><span class="sxs-lookup"><span data-stu-id="be28c-143">Count of bytes in the entry identifier pointed to by the **lpOldID** member.</span></span> 
    
 <span data-ttu-id="be28c-144">**lpOldID**</span><span class="sxs-lookup"><span data-stu-id="be28c-144">**lpOldID**</span></span>
  
> <span data-ttu-id="be28c-145">Указатель на идентификатор записи исходного объекта.</span><span class="sxs-lookup"><span data-stu-id="be28c-145">Pointer to the entry identifier of the original object.</span></span> <span data-ttu-id="be28c-146">В этом указатель может быть NULL, если событие не требуется исходный объект.</span><span class="sxs-lookup"><span data-stu-id="be28c-146">This pointer can be NULL if the event does not require an original object.</span></span>
    
 <span data-ttu-id="be28c-147">**cbOldParentID**</span><span class="sxs-lookup"><span data-stu-id="be28c-147">**cbOldParentID**</span></span>
  
> <span data-ttu-id="be28c-148">Число байт в идентификаторе запись, на который указывает член **lpOldParentID** .</span><span class="sxs-lookup"><span data-stu-id="be28c-148">Count of bytes in the entry identifier pointed to by the **lpOldParentID** member.</span></span> 
    
 <span data-ttu-id="be28c-149">**lpOldParentID**</span><span class="sxs-lookup"><span data-stu-id="be28c-149">**lpOldParentID**</span></span>
  
> <span data-ttu-id="be28c-150">Указатель на идентификатор записи родительского исходного объекта.</span><span class="sxs-lookup"><span data-stu-id="be28c-150">Pointer to the entry identifier of the parent of the original object.</span></span> <span data-ttu-id="be28c-151">В этом указатель может быть NULL, если событие не требуется исходный объект.</span><span class="sxs-lookup"><span data-stu-id="be28c-151">This pointer can be NULL if the event does not require an original object.</span></span>
    
 <span data-ttu-id="be28c-152">**lpPropTagArray**</span><span class="sxs-lookup"><span data-stu-id="be28c-152">**lpPropTagArray**</span></span>
  
> <span data-ttu-id="be28c-153">Указатель на структуру [SPropTagArray](sproptagarray.md) , который содержит свойство теги, идентифицирующий свойства, связанного с событием.</span><span class="sxs-lookup"><span data-stu-id="be28c-153">Pointer to an [SPropTagArray](sproptagarray.md) structure that contains the property tags identifying properties affected by the event.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="be28c-154">Замечания</span><span class="sxs-lookup"><span data-stu-id="be28c-154">Remarks</span></span>

<span data-ttu-id="be28c-155">Структура **OBJECT_NOTIFICATION** — это один из участников объединение структуры, включенные в элемент **info** структуры [УВЕДОМЛЕНИЙ](notification.md) .</span><span class="sxs-lookup"><span data-stu-id="be28c-155">The **OBJECT_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="be28c-156">Когда участник **info** структуры **уведомление** содержит структуру **OBJECT_NOTIFICATION** , член **ulEventType** структуры **УВЕДОМЛЕНИЙ** задано значение один из следующих типов событий:</span><span class="sxs-lookup"><span data-stu-id="be28c-156">When the **info** member of a **NOTIFICATION** structure contains an **OBJECT_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to one of the following types of events:</span></span> 
  
- <span data-ttu-id="be28c-157">fnevObjectCreated</span><span class="sxs-lookup"><span data-stu-id="be28c-157">fnevObjectCreated</span></span>
    
- <span data-ttu-id="be28c-158">fnevObjectModified</span><span class="sxs-lookup"><span data-stu-id="be28c-158">fnevObjectModified</span></span>
    
- <span data-ttu-id="be28c-159">fnevObjectDeleted</span><span class="sxs-lookup"><span data-stu-id="be28c-159">fnevObjectDeleted</span></span>
    
- <span data-ttu-id="be28c-160">fnevObjectMoved</span><span class="sxs-lookup"><span data-stu-id="be28c-160">fnevObjectMoved</span></span>
    
- <span data-ttu-id="be28c-161">fnevObjectCopied</span><span class="sxs-lookup"><span data-stu-id="be28c-161">fnevObjectCopied</span></span>
    
- <span data-ttu-id="be28c-162">fnevSearchComplete</span><span class="sxs-lookup"><span data-stu-id="be28c-162">fnevSearchComplete</span></span>
    
<span data-ttu-id="be28c-163">Событие завершения поиска, в тип события fnevSearchComplete указывает, что начального поиска домена для папки поиска завершено.</span><span class="sxs-lookup"><span data-stu-id="be28c-163">The search complete event, represented by the fnevSearchComplete event type, indicates that the initial search of the domain for one search folder has completed.</span></span>
  
<span data-ttu-id="be28c-164">Следующие члены, которые содержат сведения об исходном объекте используются только в перемещение и копирование событий.</span><span class="sxs-lookup"><span data-stu-id="be28c-164">The following members that contain information about the original object are used only in move and copy events.</span></span> 
  
- <span data-ttu-id="be28c-165">**cbOldID**</span><span class="sxs-lookup"><span data-stu-id="be28c-165">**cbOldID**</span></span>
    
- <span data-ttu-id="be28c-166">**lpOldID**</span><span class="sxs-lookup"><span data-stu-id="be28c-166">**lpOldID**</span></span>
    
- <span data-ttu-id="be28c-167">**cbOldParentID**</span><span class="sxs-lookup"><span data-stu-id="be28c-167">**cbOldParentID**</span></span>
    
- <span data-ttu-id="be28c-168">**lpOldParentID**</span><span class="sxs-lookup"><span data-stu-id="be28c-168">**lpOldParentID**</span></span>
    
<span data-ttu-id="be28c-169">Эти элементы не применяются к другим типам событий.</span><span class="sxs-lookup"><span data-stu-id="be28c-169">These members do not apply to the other types of events.</span></span>
  
<span data-ttu-id="be28c-170">Дополнительные сведения о уведомлений видеть темы, описанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="be28c-170">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="be28c-171">**Статья**</span><span class="sxs-lookup"><span data-stu-id="be28c-171">**Topic**</span></span>|<span data-ttu-id="be28c-172">**Описание**</span><span class="sxs-lookup"><span data-stu-id="be28c-172">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="be28c-173">Уведомление о событиях в MAPI</span><span class="sxs-lookup"><span data-stu-id="be28c-173">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="be28c-174">Общий обзор уведомлений и события уведомления.</span><span class="sxs-lookup"><span data-stu-id="be28c-174">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="be28c-175">Обработка уведомлений</span><span class="sxs-lookup"><span data-stu-id="be28c-175">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="be28c-176">Обсуждение как клиенты должны обрабатывать уведомления.</span><span class="sxs-lookup"><span data-stu-id="be28c-176">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="be28c-177">Поддержка уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="be28c-177">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="be28c-178">Обсуждение того, как поставщиков услуг можно использовать метод [IMAPISupport](imapisupportiunknown.md) для создания уведомлений.</span><span class="sxs-lookup"><span data-stu-id="be28c-178">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="be28c-179">См. также</span><span class="sxs-lookup"><span data-stu-id="be28c-179">See also</span></span>



[<span data-ttu-id="be28c-180">�����������</span><span class="sxs-lookup"><span data-stu-id="be28c-180">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="be28c-181">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="be28c-181">SPropTagArray</span></span>](sproptagarray.md)


[<span data-ttu-id="be28c-182">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="be28c-182">MAPI Structures</span></span>](mapi-structures.md)

