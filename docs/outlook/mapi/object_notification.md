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
ms.openlocfilehash: c637b3b03a22f208123397f7277cf8968f2509a0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430170"
---
# <a name="object_notification"></a><span data-ttu-id="3c998-103">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="3c998-103">OBJECT_NOTIFICATION</span></span>

  
  
<span data-ttu-id="3c998-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3c998-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3c998-105">Содержит сведения об объекте, который подвергался изменению, например копированию или изменению.</span><span class="sxs-lookup"><span data-stu-id="3c998-105">Contains information about an object that has undergone a change, such as being copied or modified.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3c998-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="3c998-106">Header file:</span></span>  <br/> |<span data-ttu-id="3c998-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3c998-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="3c998-108">"Участники"</span><span class="sxs-lookup"><span data-stu-id="3c998-108">Members</span></span>

 <span data-ttu-id="3c998-109">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="3c998-109">**cbEntryID**</span></span>
  
> <span data-ttu-id="3c998-110">Количествобайтов в идентификаторе записи, на который указывает **член lpEntryID.**</span><span class="sxs-lookup"><span data-stu-id="3c998-110">Count of bytes in the entry identifier pointed to by the **lpEntryID** member.</span></span> 
    
 <span data-ttu-id="3c998-111">**lpEntryID**</span><span class="sxs-lookup"><span data-stu-id="3c998-111">**lpEntryID**</span></span>
  
> <span data-ttu-id="3c998-112">Указатель на идентификатор записи затронутого объекта.</span><span class="sxs-lookup"><span data-stu-id="3c998-112">Pointer to the entry identifier of the affected object.</span></span>
    
 <span data-ttu-id="3c998-113">**ulObjType**</span><span class="sxs-lookup"><span data-stu-id="3c998-113">**ulObjType**</span></span>
  
> <span data-ttu-id="3c998-114">Тип затронутого объекта.</span><span class="sxs-lookup"><span data-stu-id="3c998-114">Type of object affected.</span></span> <span data-ttu-id="3c998-115">Возможные типы:</span><span class="sxs-lookup"><span data-stu-id="3c998-115">Possible types are as follows:</span></span>
    
<span data-ttu-id="3c998-116">MAPI_STORE</span><span class="sxs-lookup"><span data-stu-id="3c998-116">MAPI_STORE</span></span> 
  
> <span data-ttu-id="3c998-117">Хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="3c998-117">Message store.</span></span> 
    
<span data-ttu-id="3c998-118">MAPI_ADDRBOOK</span><span class="sxs-lookup"><span data-stu-id="3c998-118">MAPI_ADDRBOOK</span></span> 
  
> <span data-ttu-id="3c998-119">Адресная книга.</span><span class="sxs-lookup"><span data-stu-id="3c998-119">Address book.</span></span> 
    
<span data-ttu-id="3c998-120">MAPI_FOLDER</span><span class="sxs-lookup"><span data-stu-id="3c998-120">MAPI_FOLDER</span></span> 
  
> <span data-ttu-id="3c998-121">Папка.</span><span class="sxs-lookup"><span data-stu-id="3c998-121">Folder.</span></span>
    
<span data-ttu-id="3c998-122">MAPI_ABCONT</span><span class="sxs-lookup"><span data-stu-id="3c998-122">MAPI_ABCONT</span></span> 
  
> <span data-ttu-id="3c998-123">Контейнер адресной книги.</span><span class="sxs-lookup"><span data-stu-id="3c998-123">Address book container.</span></span>
    
<span data-ttu-id="3c998-124">MAPI_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="3c998-124">MAPI_MESSAGE</span></span> 
  
> <span data-ttu-id="3c998-125">Сообщение.</span><span class="sxs-lookup"><span data-stu-id="3c998-125">Message.</span></span>
    
<span data-ttu-id="3c998-126">MAPI_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="3c998-126">MAPI_MAILUSER</span></span> 
  
> <span data-ttu-id="3c998-127">Пользователь системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="3c998-127">Messaging user.</span></span>
    
<span data-ttu-id="3c998-128">MAPI_ATTACH</span><span class="sxs-lookup"><span data-stu-id="3c998-128">MAPI_ATTACH</span></span> 
  
> <span data-ttu-id="3c998-129">Вложение.</span><span class="sxs-lookup"><span data-stu-id="3c998-129">Attachment.</span></span>
    
<span data-ttu-id="3c998-130">MAPI_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="3c998-130">MAPI_DISTLIST</span></span> 
  
> <span data-ttu-id="3c998-131">Список рассылки.</span><span class="sxs-lookup"><span data-stu-id="3c998-131">Distribution list.</span></span>
    
<span data-ttu-id="3c998-132">MAPI_PROFSECT</span><span class="sxs-lookup"><span data-stu-id="3c998-132">MAPI_PROFSECT</span></span> 
  
> <span data-ttu-id="3c998-133">Раздел "Профиль".</span><span class="sxs-lookup"><span data-stu-id="3c998-133">Profile section.</span></span>
    
<span data-ttu-id="3c998-134">MAPI_STATUS</span><span class="sxs-lookup"><span data-stu-id="3c998-134">MAPI_STATUS</span></span> 
  
> <span data-ttu-id="3c998-135">Объект Status.</span><span class="sxs-lookup"><span data-stu-id="3c998-135">Status object.</span></span>
    
<span data-ttu-id="3c998-136">MAPI_SESSION</span><span class="sxs-lookup"><span data-stu-id="3c998-136">MAPI_SESSION</span></span> 
  
> <span data-ttu-id="3c998-137">Объект Session.</span><span class="sxs-lookup"><span data-stu-id="3c998-137">Session object.</span></span>
    
 <span data-ttu-id="3c998-138">**cbParentID**</span><span class="sxs-lookup"><span data-stu-id="3c998-138">**cbParentID**</span></span>
  
> <span data-ttu-id="3c998-139">Количествобайтов в идентификаторе записи, на который указывает **член lpParentID.**</span><span class="sxs-lookup"><span data-stu-id="3c998-139">Count of bytes in the entry identifier pointed to by the **lpParentID** member.</span></span> 
    
 <span data-ttu-id="3c998-140">**lpParentID**</span><span class="sxs-lookup"><span data-stu-id="3c998-140">**lpParentID**</span></span>
  
> <span data-ttu-id="3c998-141">Указатель на идентификатор записи родительского объекта.</span><span class="sxs-lookup"><span data-stu-id="3c998-141">Pointer to the entry identifier of the parent of the affected object.</span></span>
    
 <span data-ttu-id="3c998-142">**cbOldID**</span><span class="sxs-lookup"><span data-stu-id="3c998-142">**cbOldID**</span></span>
  
> <span data-ttu-id="3c998-143">Количествобайтов в идентификаторе записи, на который указывает **член lpOldID.**</span><span class="sxs-lookup"><span data-stu-id="3c998-143">Count of bytes in the entry identifier pointed to by the **lpOldID** member.</span></span> 
    
 <span data-ttu-id="3c998-144">**lpOldID**</span><span class="sxs-lookup"><span data-stu-id="3c998-144">**lpOldID**</span></span>
  
> <span data-ttu-id="3c998-145">Указатель на идентификатор записи исходного объекта.</span><span class="sxs-lookup"><span data-stu-id="3c998-145">Pointer to the entry identifier of the original object.</span></span> <span data-ttu-id="3c998-146">Этот указатель может иметь NULL, если для события не требуется исходный объект.</span><span class="sxs-lookup"><span data-stu-id="3c998-146">This pointer can be NULL if the event does not require an original object.</span></span>
    
 <span data-ttu-id="3c998-147">**cbOldParentID**</span><span class="sxs-lookup"><span data-stu-id="3c998-147">**cbOldParentID**</span></span>
  
> <span data-ttu-id="3c998-148">Количествобайтов в идентификаторе записи, на который указывает **член lpOldParentID.**</span><span class="sxs-lookup"><span data-stu-id="3c998-148">Count of bytes in the entry identifier pointed to by the **lpOldParentID** member.</span></span> 
    
 <span data-ttu-id="3c998-149">**lpOldParentID**</span><span class="sxs-lookup"><span data-stu-id="3c998-149">**lpOldParentID**</span></span>
  
> <span data-ttu-id="3c998-150">Указатель на идентификатор записи родительского объекта.</span><span class="sxs-lookup"><span data-stu-id="3c998-150">Pointer to the entry identifier of the parent of the original object.</span></span> <span data-ttu-id="3c998-151">Этот указатель может иметь NULL, если для события не требуется исходный объект.</span><span class="sxs-lookup"><span data-stu-id="3c998-151">This pointer can be NULL if the event does not require an original object.</span></span>
    
 <span data-ttu-id="3c998-152">**lpPropTagArray**</span><span class="sxs-lookup"><span data-stu-id="3c998-152">**lpPropTagArray**</span></span>
  
> <span data-ttu-id="3c998-153">Указатель на [структуру SPropTagArray,](sproptagarray.md) которая содержит теги свойств, определяющие свойства, затронутые событием.</span><span class="sxs-lookup"><span data-stu-id="3c998-153">Pointer to an [SPropTagArray](sproptagarray.md) structure that contains the property tags identifying properties affected by the event.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="3c998-154">Примечания</span><span class="sxs-lookup"><span data-stu-id="3c998-154">Remarks</span></span>

<span data-ttu-id="3c998-155">Структура **OBJECT_NOTIFICATION** является одним из членов объединения структур, включенных в  состав данных структуры [NOTIFICATION.](notification.md)</span><span class="sxs-lookup"><span data-stu-id="3c998-155">The **OBJECT_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="3c998-156">Если **информационный** член структуры **NOTIFICATION** содержит структуру OBJECT_NOTIFICATION, то для члена  **ulEventType** структуры **NOTIFICATION** устанавливается один из следующих типов событий:</span><span class="sxs-lookup"><span data-stu-id="3c998-156">When the **info** member of a **NOTIFICATION** structure contains an **OBJECT_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to one of the following types of events:</span></span> 
  
- <span data-ttu-id="3c998-157">fnevObjectCreated</span><span class="sxs-lookup"><span data-stu-id="3c998-157">fnevObjectCreated</span></span>
    
- <span data-ttu-id="3c998-158">fnevObjectModified</span><span class="sxs-lookup"><span data-stu-id="3c998-158">fnevObjectModified</span></span>
    
- <span data-ttu-id="3c998-159">fnevObjectDeleted</span><span class="sxs-lookup"><span data-stu-id="3c998-159">fnevObjectDeleted</span></span>
    
- <span data-ttu-id="3c998-160">fnevObjectMoved</span><span class="sxs-lookup"><span data-stu-id="3c998-160">fnevObjectMoved</span></span>
    
- <span data-ttu-id="3c998-161">fnevObjectCopied</span><span class="sxs-lookup"><span data-stu-id="3c998-161">fnevObjectCopied</span></span>
    
- <span data-ttu-id="3c998-162">fnevSearchComplete</span><span class="sxs-lookup"><span data-stu-id="3c998-162">fnevSearchComplete</span></span>
    
<span data-ttu-id="3c998-163">Событие завершения поиска, представленное типом события fnevSearchComplete, указывает, что первоначальный поиск в домене для одной папки поиска завершен.</span><span class="sxs-lookup"><span data-stu-id="3c998-163">The search complete event, represented by the fnevSearchComplete event type, indicates that the initial search of the domain for one search folder has completed.</span></span>
  
<span data-ttu-id="3c998-164">Следующие члены, содержащие сведения об исходном объекте, используются только в событиях перемещения и копирования.</span><span class="sxs-lookup"><span data-stu-id="3c998-164">The following members that contain information about the original object are used only in move and copy events.</span></span> 
  
- <span data-ttu-id="3c998-165">**cbOldID**</span><span class="sxs-lookup"><span data-stu-id="3c998-165">**cbOldID**</span></span>
    
- <span data-ttu-id="3c998-166">**lpOldID**</span><span class="sxs-lookup"><span data-stu-id="3c998-166">**lpOldID**</span></span>
    
- <span data-ttu-id="3c998-167">**cbOldParentID**</span><span class="sxs-lookup"><span data-stu-id="3c998-167">**cbOldParentID**</span></span>
    
- <span data-ttu-id="3c998-168">**lpOldParentID**</span><span class="sxs-lookup"><span data-stu-id="3c998-168">**lpOldParentID**</span></span>
    
<span data-ttu-id="3c998-169">Эти члены не применяются к другим типам событий.</span><span class="sxs-lookup"><span data-stu-id="3c998-169">These members do not apply to the other types of events.</span></span>
  
<span data-ttu-id="3c998-170">Дополнительные сведения об уведомлении см. в темах, описанных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="3c998-170">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="3c998-171">**Статья**</span><span class="sxs-lookup"><span data-stu-id="3c998-171">**Topic**</span></span>|<span data-ttu-id="3c998-172">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3c998-172">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3c998-173">Уведомление о событии в MAPI</span><span class="sxs-lookup"><span data-stu-id="3c998-173">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="3c998-174">Общий обзор событий уведомлений и уведомлений.</span><span class="sxs-lookup"><span data-stu-id="3c998-174">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="3c998-175">Обработка уведомлений</span><span class="sxs-lookup"><span data-stu-id="3c998-175">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="3c998-176">Обсуждение того, как клиенты должны обрабатывать уведомления.</span><span class="sxs-lookup"><span data-stu-id="3c998-176">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="3c998-177">Поддержка уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="3c998-177">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="3c998-178">Обсуждение того, как поставщики служб могут использовать метод [IMAPISupport](imapisupportiunknown.md) для создания уведомлений.</span><span class="sxs-lookup"><span data-stu-id="3c998-178">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3c998-179">См. также</span><span class="sxs-lookup"><span data-stu-id="3c998-179">See also</span></span>



[<span data-ttu-id="3c998-180">�����������</span><span class="sxs-lookup"><span data-stu-id="3c998-180">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="3c998-181">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="3c998-181">SPropTagArray</span></span>](sproptagarray.md)


[<span data-ttu-id="3c998-182">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="3c998-182">MAPI Structures</span></span>](mapi-structures.md)

