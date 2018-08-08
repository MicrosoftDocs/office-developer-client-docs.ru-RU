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
ms.openlocfilehash: 1593152786a3345827089e5f6702454896944b1f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810053"
---
# <a name="objectnotification"></a><span data-ttu-id="3d3d3-103">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="3d3d3-103">OBJECT_NOTIFICATION</span></span>

  
  
<span data-ttu-id="3d3d3-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3d3d3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3d3d3-105">Содержит сведения об объекте, который внесено изменение, например, копирование или изменены.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-105">Contains information about an object that has undergone a change, such as being copied or modified.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3d3d3-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="3d3d3-106">Header file:</span></span>  <br/> |<span data-ttu-id="3d3d3-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3d3d3-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="3d3d3-108">Members</span><span class="sxs-lookup"><span data-stu-id="3d3d3-108">Members</span></span>

 <span data-ttu-id="3d3d3-109">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="3d3d3-109">**cbEntryID**</span></span>
  
> <span data-ttu-id="3d3d3-110">Число байт в идентификаторе запись, на который указывает член **lpEntryID** .</span><span class="sxs-lookup"><span data-stu-id="3d3d3-110">Count of bytes in the entry identifier pointed to by the **lpEntryID** member.</span></span> 
    
 <span data-ttu-id="3d3d3-111">**lpEntryID**</span><span class="sxs-lookup"><span data-stu-id="3d3d3-111">**lpEntryID**</span></span>
  
> <span data-ttu-id="3d3d3-112">Указатель на идентификатор записи затронутых объекта.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-112">Pointer to the entry identifier of the affected object.</span></span>
    
 <span data-ttu-id="3d3d3-113">**ulObjType**</span><span class="sxs-lookup"><span data-stu-id="3d3d3-113">**ulObjType**</span></span>
  
> <span data-ttu-id="3d3d3-114">Тип объекта, связанного.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-114">Type of object affected.</span></span> <span data-ttu-id="3d3d3-115">Ниже приведены возможные типы:</span><span class="sxs-lookup"><span data-stu-id="3d3d3-115">Possible types are as follows:</span></span>
    
<span data-ttu-id="3d3d3-116">MAPI_STORE</span><span class="sxs-lookup"><span data-stu-id="3d3d3-116">MAPI_STORE</span></span> 
  
> <span data-ttu-id="3d3d3-117">Хранение сообщений.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-117">Message store.</span></span> 
    
<span data-ttu-id="3d3d3-118">MAPI_ADDRBOOK</span><span class="sxs-lookup"><span data-stu-id="3d3d3-118">MAPI_ADDRBOOK</span></span> 
  
> <span data-ttu-id="3d3d3-119">Список адресов.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-119">Address book.</span></span> 
    
<span data-ttu-id="3d3d3-120">MAPI_FOLDER</span><span class="sxs-lookup"><span data-stu-id="3d3d3-120">MAPI_FOLDER</span></span> 
  
> <span data-ttu-id="3d3d3-121">Папка.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-121">Folder.</span></span>
    
<span data-ttu-id="3d3d3-122">MAPI_ABCONT</span><span class="sxs-lookup"><span data-stu-id="3d3d3-122">MAPI_ABCONT</span></span> 
  
> <span data-ttu-id="3d3d3-123">Контейнер адресной книги.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-123">Address book container.</span></span>
    
<span data-ttu-id="3d3d3-124">MAPI_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="3d3d3-124">MAPI_MESSAGE</span></span> 
  
> <span data-ttu-id="3d3d3-125">Сообщение.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-125">Message.</span></span>
    
<span data-ttu-id="3d3d3-126">MAPI_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="3d3d3-126">MAPI_MAILUSER</span></span> 
  
> <span data-ttu-id="3d3d3-127">Пользователь, обмена мгновенными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-127">Messaging user.</span></span>
    
<span data-ttu-id="3d3d3-128">MAPI_ATTACH</span><span class="sxs-lookup"><span data-stu-id="3d3d3-128">MAPI_ATTACH</span></span> 
  
> <span data-ttu-id="3d3d3-129">Вложение.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-129">Attachment.</span></span>
    
<span data-ttu-id="3d3d3-130">MAPI_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="3d3d3-130">MAPI_DISTLIST</span></span> 
  
> <span data-ttu-id="3d3d3-131">Список рассылки.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-131">Distribution list.</span></span>
    
<span data-ttu-id="3d3d3-132">MAPI_PROFSECT</span><span class="sxs-lookup"><span data-stu-id="3d3d3-132">MAPI_PROFSECT</span></span> 
  
> <span data-ttu-id="3d3d3-133">Раздел профиля.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-133">Profile section.</span></span>
    
<span data-ttu-id="3d3d3-134">MAPI_STATUS</span><span class="sxs-lookup"><span data-stu-id="3d3d3-134">MAPI_STATUS</span></span> 
  
> <span data-ttu-id="3d3d3-135">Состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-135">Status object.</span></span>
    
<span data-ttu-id="3d3d3-136">MAPI_SESSION</span><span class="sxs-lookup"><span data-stu-id="3d3d3-136">MAPI_SESSION</span></span> 
  
> <span data-ttu-id="3d3d3-137">Объект сеанса.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-137">Session object.</span></span>
    
 <span data-ttu-id="3d3d3-138">**cbParentID**</span><span class="sxs-lookup"><span data-stu-id="3d3d3-138">**cbParentID**</span></span>
  
> <span data-ttu-id="3d3d3-139">Число байт в идентификаторе запись, на который указывает член **lpParentID** .</span><span class="sxs-lookup"><span data-stu-id="3d3d3-139">Count of bytes in the entry identifier pointed to by the **lpParentID** member.</span></span> 
    
 <span data-ttu-id="3d3d3-140">**lpParentID**</span><span class="sxs-lookup"><span data-stu-id="3d3d3-140">**lpParentID**</span></span>
  
> <span data-ttu-id="3d3d3-141">Указатель на идентификатор записи родительского объекта затронутых.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-141">Pointer to the entry identifier of the parent of the affected object.</span></span>
    
 <span data-ttu-id="3d3d3-142">**cbOldID**</span><span class="sxs-lookup"><span data-stu-id="3d3d3-142">**cbOldID**</span></span>
  
> <span data-ttu-id="3d3d3-143">Число байт в идентификаторе запись, на который указывает член **lpOldID** .</span><span class="sxs-lookup"><span data-stu-id="3d3d3-143">Count of bytes in the entry identifier pointed to by the **lpOldID** member.</span></span> 
    
 <span data-ttu-id="3d3d3-144">**lpOldID**</span><span class="sxs-lookup"><span data-stu-id="3d3d3-144">**lpOldID**</span></span>
  
> <span data-ttu-id="3d3d3-145">Указатель на идентификатор записи исходного объекта.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-145">Pointer to the entry identifier of the original object.</span></span> <span data-ttu-id="3d3d3-146">В этом указатель может быть NULL, если событие не требуется исходный объект.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-146">This pointer can be NULL if the event does not require an original object.</span></span>
    
 <span data-ttu-id="3d3d3-147">**cbOldParentID**</span><span class="sxs-lookup"><span data-stu-id="3d3d3-147">**cbOldParentID**</span></span>
  
> <span data-ttu-id="3d3d3-148">Число байт в идентификаторе запись, на который указывает член **lpOldParentID** .</span><span class="sxs-lookup"><span data-stu-id="3d3d3-148">Count of bytes in the entry identifier pointed to by the **lpOldParentID** member.</span></span> 
    
 <span data-ttu-id="3d3d3-149">**lpOldParentID**</span><span class="sxs-lookup"><span data-stu-id="3d3d3-149">**lpOldParentID**</span></span>
  
> <span data-ttu-id="3d3d3-150">Указатель на идентификатор записи родительского исходного объекта.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-150">Pointer to the entry identifier of the parent of the original object.</span></span> <span data-ttu-id="3d3d3-151">В этом указатель может быть NULL, если событие не требуется исходный объект.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-151">This pointer can be NULL if the event does not require an original object.</span></span>
    
 <span data-ttu-id="3d3d3-152">**lpPropTagArray**</span><span class="sxs-lookup"><span data-stu-id="3d3d3-152">**lpPropTagArray**</span></span>
  
> <span data-ttu-id="3d3d3-153">Указатель на структуру [SPropTagArray](sproptagarray.md) , который содержит свойство теги, идентифицирующий свойства, связанного с событием.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-153">Pointer to an [SPropTagArray](sproptagarray.md) structure that contains the property tags identifying properties affected by the event.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="3d3d3-154">Замечания</span><span class="sxs-lookup"><span data-stu-id="3d3d3-154">Remarks</span></span>

<span data-ttu-id="3d3d3-155">Структура **OBJECT_NOTIFICATION** — это один из участников объединение структуры, включенные в элемент **info** структуры [УВЕДОМЛЕНИЙ](notification.md) .</span><span class="sxs-lookup"><span data-stu-id="3d3d3-155">The **OBJECT_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="3d3d3-156">Когда участник **info** структуры **уведомление** содержит структуру **OBJECT_NOTIFICATION** , член **ulEventType** структуры **УВЕДОМЛЕНИЙ** задано значение один из следующих типов событий:</span><span class="sxs-lookup"><span data-stu-id="3d3d3-156">When the **info** member of a **NOTIFICATION** structure contains an **OBJECT_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to one of the following types of events:</span></span> 
  
- <span data-ttu-id="3d3d3-157">fnevObjectCreated</span><span class="sxs-lookup"><span data-stu-id="3d3d3-157">fnevObjectCreated</span></span>
    
- <span data-ttu-id="3d3d3-158">fnevObjectModified</span><span class="sxs-lookup"><span data-stu-id="3d3d3-158">fnevObjectModified</span></span>
    
- <span data-ttu-id="3d3d3-159">fnevObjectDeleted</span><span class="sxs-lookup"><span data-stu-id="3d3d3-159">fnevObjectDeleted</span></span>
    
- <span data-ttu-id="3d3d3-160">fnevObjectMoved</span><span class="sxs-lookup"><span data-stu-id="3d3d3-160">fnevObjectMoved</span></span>
    
- <span data-ttu-id="3d3d3-161">fnevObjectCopied</span><span class="sxs-lookup"><span data-stu-id="3d3d3-161">fnevObjectCopied</span></span>
    
- <span data-ttu-id="3d3d3-162">fnevSearchComplete</span><span class="sxs-lookup"><span data-stu-id="3d3d3-162">fnevSearchComplete</span></span>
    
<span data-ttu-id="3d3d3-163">Событие завершения поиска, в тип события fnevSearchComplete указывает, что начального поиска домена для папки поиска завершено.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-163">The search complete event, represented by the fnevSearchComplete event type, indicates that the initial search of the domain for one search folder has completed.</span></span>
  
<span data-ttu-id="3d3d3-164">Следующие члены, которые содержат сведения об исходном объекте используются только в перемещение и копирование событий.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-164">The following members that contain information about the original object are used only in move and copy events.</span></span> 
  
- <span data-ttu-id="3d3d3-165">**cbOldID**</span><span class="sxs-lookup"><span data-stu-id="3d3d3-165">**cbOldID**</span></span>
    
- <span data-ttu-id="3d3d3-166">**lpOldID**</span><span class="sxs-lookup"><span data-stu-id="3d3d3-166">**lpOldID**</span></span>
    
- <span data-ttu-id="3d3d3-167">**cbOldParentID**</span><span class="sxs-lookup"><span data-stu-id="3d3d3-167">**cbOldParentID**</span></span>
    
- <span data-ttu-id="3d3d3-168">**lpOldParentID**</span><span class="sxs-lookup"><span data-stu-id="3d3d3-168">**lpOldParentID**</span></span>
    
<span data-ttu-id="3d3d3-169">Эти элементы не применяются к другим типам событий.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-169">These members do not apply to the other types of events.</span></span>
  
<span data-ttu-id="3d3d3-170">Дополнительные сведения о уведомлений видеть темы, описанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-170">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="3d3d3-171">**Статья**</span><span class="sxs-lookup"><span data-stu-id="3d3d3-171">**Topic**</span></span>|<span data-ttu-id="3d3d3-172">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3d3d3-172">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3d3d3-173">Уведомление о событиях в MAPI</span><span class="sxs-lookup"><span data-stu-id="3d3d3-173">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="3d3d3-174">Общий обзор уведомлений и события уведомления.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-174">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="3d3d3-175">Обработка уведомлений</span><span class="sxs-lookup"><span data-stu-id="3d3d3-175">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="3d3d3-176">Обсуждение как клиенты должны обрабатывать уведомления.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-176">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="3d3d3-177">Поддержка уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="3d3d3-177">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="3d3d3-178">Обсуждение того, как поставщиков услуг можно использовать метод [IMAPISupport](imapisupportiunknown.md) для создания уведомлений.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-178">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3d3d3-179">См. также</span><span class="sxs-lookup"><span data-stu-id="3d3d3-179">See also</span></span>



[<span data-ttu-id="3d3d3-180">�����������</span><span class="sxs-lookup"><span data-stu-id="3d3d3-180">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="3d3d3-181">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="3d3d3-181">SPropTagArray</span></span>](sproptagarray.md)


[<span data-ttu-id="3d3d3-182">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="3d3d3-182">MAPI Structures</span></span>](mapi-structures.md)

