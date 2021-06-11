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
# <a name="object_notification"></a><span data-ttu-id="59557-103">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="59557-103">OBJECT_NOTIFICATION</span></span>

  
  
<span data-ttu-id="59557-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="59557-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="59557-105">Содержит сведения об объекте, который подвергся изменениям, например о копировании или изменении.</span><span class="sxs-lookup"><span data-stu-id="59557-105">Contains information about an object that has undergone a change, such as being copied or modified.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="59557-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="59557-106">Header file:</span></span>  <br/> |<span data-ttu-id="59557-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="59557-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="59557-108">"Участники"</span><span class="sxs-lookup"><span data-stu-id="59557-108">Members</span></span>

 <span data-ttu-id="59557-109">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="59557-109">**cbEntryID**</span></span>
  
> <span data-ttu-id="59557-110">Количество bytes в идентификаторе записи, на который указывает член **lpEntryID.**</span><span class="sxs-lookup"><span data-stu-id="59557-110">Count of bytes in the entry identifier pointed to by the **lpEntryID** member.</span></span> 
    
 <span data-ttu-id="59557-111">**lpEntryID**</span><span class="sxs-lookup"><span data-stu-id="59557-111">**lpEntryID**</span></span>
  
> <span data-ttu-id="59557-112">Указатель на идентификатор входа затронутого объекта.</span><span class="sxs-lookup"><span data-stu-id="59557-112">Pointer to the entry identifier of the affected object.</span></span>
    
 <span data-ttu-id="59557-113">**ulObjType**</span><span class="sxs-lookup"><span data-stu-id="59557-113">**ulObjType**</span></span>
  
> <span data-ttu-id="59557-114">Тип затронутого объекта.</span><span class="sxs-lookup"><span data-stu-id="59557-114">Type of object affected.</span></span> <span data-ttu-id="59557-115">Возможные типы:</span><span class="sxs-lookup"><span data-stu-id="59557-115">Possible types are as follows:</span></span>
    
<span data-ttu-id="59557-116">MAPI_STORE</span><span class="sxs-lookup"><span data-stu-id="59557-116">MAPI_STORE</span></span> 
  
> <span data-ttu-id="59557-117">Хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="59557-117">Message store.</span></span> 
    
<span data-ttu-id="59557-118">MAPI_ADDRBOOK</span><span class="sxs-lookup"><span data-stu-id="59557-118">MAPI_ADDRBOOK</span></span> 
  
> <span data-ttu-id="59557-119">Адресная книга.</span><span class="sxs-lookup"><span data-stu-id="59557-119">Address book.</span></span> 
    
<span data-ttu-id="59557-120">MAPI_FOLDER</span><span class="sxs-lookup"><span data-stu-id="59557-120">MAPI_FOLDER</span></span> 
  
> <span data-ttu-id="59557-121">Папка.</span><span class="sxs-lookup"><span data-stu-id="59557-121">Folder.</span></span>
    
<span data-ttu-id="59557-122">MAPI_ABCONT</span><span class="sxs-lookup"><span data-stu-id="59557-122">MAPI_ABCONT</span></span> 
  
> <span data-ttu-id="59557-123">Контейнер адресной книги.</span><span class="sxs-lookup"><span data-stu-id="59557-123">Address book container.</span></span>
    
<span data-ttu-id="59557-124">MAPI_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="59557-124">MAPI_MESSAGE</span></span> 
  
> <span data-ttu-id="59557-125">Сообщение.</span><span class="sxs-lookup"><span data-stu-id="59557-125">Message.</span></span>
    
<span data-ttu-id="59557-126">MAPI_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="59557-126">MAPI_MAILUSER</span></span> 
  
> <span data-ttu-id="59557-127">Пользователь обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="59557-127">Messaging user.</span></span>
    
<span data-ttu-id="59557-128">MAPI_ATTACH</span><span class="sxs-lookup"><span data-stu-id="59557-128">MAPI_ATTACH</span></span> 
  
> <span data-ttu-id="59557-129">Вложение.</span><span class="sxs-lookup"><span data-stu-id="59557-129">Attachment.</span></span>
    
<span data-ttu-id="59557-130">MAPI_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="59557-130">MAPI_DISTLIST</span></span> 
  
> <span data-ttu-id="59557-131">Список рассылки.</span><span class="sxs-lookup"><span data-stu-id="59557-131">Distribution list.</span></span>
    
<span data-ttu-id="59557-132">MAPI_PROFSECT</span><span class="sxs-lookup"><span data-stu-id="59557-132">MAPI_PROFSECT</span></span> 
  
> <span data-ttu-id="59557-133">Раздел Профиль.</span><span class="sxs-lookup"><span data-stu-id="59557-133">Profile section.</span></span>
    
<span data-ttu-id="59557-134">MAPI_STATUS</span><span class="sxs-lookup"><span data-stu-id="59557-134">MAPI_STATUS</span></span> 
  
> <span data-ttu-id="59557-135">Объект Status.</span><span class="sxs-lookup"><span data-stu-id="59557-135">Status object.</span></span>
    
<span data-ttu-id="59557-136">MAPI_SESSION</span><span class="sxs-lookup"><span data-stu-id="59557-136">MAPI_SESSION</span></span> 
  
> <span data-ttu-id="59557-137">Объект Session.</span><span class="sxs-lookup"><span data-stu-id="59557-137">Session object.</span></span>
    
 <span data-ttu-id="59557-138">**cbParentID**</span><span class="sxs-lookup"><span data-stu-id="59557-138">**cbParentID**</span></span>
  
> <span data-ttu-id="59557-139">Количество bytes в идентификаторе записи, на который указывает член **lpParentID.**</span><span class="sxs-lookup"><span data-stu-id="59557-139">Count of bytes in the entry identifier pointed to by the **lpParentID** member.</span></span> 
    
 <span data-ttu-id="59557-140">**lpParentID**</span><span class="sxs-lookup"><span data-stu-id="59557-140">**lpParentID**</span></span>
  
> <span data-ttu-id="59557-141">Указатель на идентификатор записи родителя пострадавшего объекта.</span><span class="sxs-lookup"><span data-stu-id="59557-141">Pointer to the entry identifier of the parent of the affected object.</span></span>
    
 <span data-ttu-id="59557-142">**cbOldID**</span><span class="sxs-lookup"><span data-stu-id="59557-142">**cbOldID**</span></span>
  
> <span data-ttu-id="59557-143">Количество bytes в идентификаторе записи, на который указывает член **lpOldID.**</span><span class="sxs-lookup"><span data-stu-id="59557-143">Count of bytes in the entry identifier pointed to by the **lpOldID** member.</span></span> 
    
 <span data-ttu-id="59557-144">**lpOldID**</span><span class="sxs-lookup"><span data-stu-id="59557-144">**lpOldID**</span></span>
  
> <span data-ttu-id="59557-145">Указатель на идентификатор входа исходного объекта.</span><span class="sxs-lookup"><span data-stu-id="59557-145">Pointer to the entry identifier of the original object.</span></span> <span data-ttu-id="59557-146">Этот указатель может быть NULL, если для события не требуется исходный объект.</span><span class="sxs-lookup"><span data-stu-id="59557-146">This pointer can be NULL if the event does not require an original object.</span></span>
    
 <span data-ttu-id="59557-147">**cbOldParentID**</span><span class="sxs-lookup"><span data-stu-id="59557-147">**cbOldParentID**</span></span>
  
> <span data-ttu-id="59557-148">Количество bytes в идентификаторе записи, на который указывает член **lpOldParentID.**</span><span class="sxs-lookup"><span data-stu-id="59557-148">Count of bytes in the entry identifier pointed to by the **lpOldParentID** member.</span></span> 
    
 <span data-ttu-id="59557-149">**lpOldParentID**</span><span class="sxs-lookup"><span data-stu-id="59557-149">**lpOldParentID**</span></span>
  
> <span data-ttu-id="59557-150">Указатель на идентификатор записи родительского исходного объекта.</span><span class="sxs-lookup"><span data-stu-id="59557-150">Pointer to the entry identifier of the parent of the original object.</span></span> <span data-ttu-id="59557-151">Этот указатель может быть NULL, если для события не требуется исходный объект.</span><span class="sxs-lookup"><span data-stu-id="59557-151">This pointer can be NULL if the event does not require an original object.</span></span>
    
 <span data-ttu-id="59557-152">**lpPropTagArray**</span><span class="sxs-lookup"><span data-stu-id="59557-152">**lpPropTagArray**</span></span>
  
> <span data-ttu-id="59557-153">Указатель на [структуру SPropTagArray,](sproptagarray.md) которая содержит теги свойств, определяющие свойства, затронутые событием.</span><span class="sxs-lookup"><span data-stu-id="59557-153">Pointer to an [SPropTagArray](sproptagarray.md) structure that contains the property tags identifying properties affected by the event.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="59557-154">Примечания</span><span class="sxs-lookup"><span data-stu-id="59557-154">Remarks</span></span>

<span data-ttu-id="59557-155">Структура **OBJECT_NOTIFICATION** является одним из членов союза структур, включенных в  состав информационного члена [структуры NOTIFICATION.](notification.md)</span><span class="sxs-lookup"><span data-stu-id="59557-155">The **OBJECT_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="59557-156">Если член **структуры**  уведомлений  содержит структуру OBJECT_NOTIFICATION, то член **ulEventType** структуры **УВЕДОМЛЕНий** устанавливается к одному из следующих типов событий:</span><span class="sxs-lookup"><span data-stu-id="59557-156">When the **info** member of a **NOTIFICATION** structure contains an **OBJECT_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to one of the following types of events:</span></span> 
  
- <span data-ttu-id="59557-157">fnevObjectCreated</span><span class="sxs-lookup"><span data-stu-id="59557-157">fnevObjectCreated</span></span>
    
- <span data-ttu-id="59557-158">fnevObjectModified</span><span class="sxs-lookup"><span data-stu-id="59557-158">fnevObjectModified</span></span>
    
- <span data-ttu-id="59557-159">fnevObjectDeleted</span><span class="sxs-lookup"><span data-stu-id="59557-159">fnevObjectDeleted</span></span>
    
- <span data-ttu-id="59557-160">fnevObjectMoved</span><span class="sxs-lookup"><span data-stu-id="59557-160">fnevObjectMoved</span></span>
    
- <span data-ttu-id="59557-161">fnevObjectCopied</span><span class="sxs-lookup"><span data-stu-id="59557-161">fnevObjectCopied</span></span>
    
- <span data-ttu-id="59557-162">fnevSearchComplete</span><span class="sxs-lookup"><span data-stu-id="59557-162">fnevSearchComplete</span></span>
    
<span data-ttu-id="59557-163">Полное событие поиска, представленное типом события fnevSearchComplete, указывает, что начальный поиск домена для одной папки поиска завершен.</span><span class="sxs-lookup"><span data-stu-id="59557-163">The search complete event, represented by the fnevSearchComplete event type, indicates that the initial search of the domain for one search folder has completed.</span></span>
  
<span data-ttu-id="59557-164">Следующие участники, содержащие сведения о исходном объекте, используются только в событиях перемещения и копирования.</span><span class="sxs-lookup"><span data-stu-id="59557-164">The following members that contain information about the original object are used only in move and copy events.</span></span> 
  
- <span data-ttu-id="59557-165">**cbOldID**</span><span class="sxs-lookup"><span data-stu-id="59557-165">**cbOldID**</span></span>
    
- <span data-ttu-id="59557-166">**lpOldID**</span><span class="sxs-lookup"><span data-stu-id="59557-166">**lpOldID**</span></span>
    
- <span data-ttu-id="59557-167">**cbOldParentID**</span><span class="sxs-lookup"><span data-stu-id="59557-167">**cbOldParentID**</span></span>
    
- <span data-ttu-id="59557-168">**lpOldParentID**</span><span class="sxs-lookup"><span data-stu-id="59557-168">**lpOldParentID**</span></span>
    
<span data-ttu-id="59557-169">Эти участники не применяются к другим типам событий.</span><span class="sxs-lookup"><span data-stu-id="59557-169">These members do not apply to the other types of events.</span></span>
  
<span data-ttu-id="59557-170">Дополнительные сведения об уведомлении см. в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="59557-170">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="59557-171">**Статья**</span><span class="sxs-lookup"><span data-stu-id="59557-171">**Topic**</span></span>|<span data-ttu-id="59557-172">**Описание**</span><span class="sxs-lookup"><span data-stu-id="59557-172">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="59557-173">Уведомление о событиях в MAPI</span><span class="sxs-lookup"><span data-stu-id="59557-173">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="59557-174">Общий обзор событий уведомлений и уведомлений.</span><span class="sxs-lookup"><span data-stu-id="59557-174">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="59557-175">Обработка уведомлений</span><span class="sxs-lookup"><span data-stu-id="59557-175">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="59557-176">Обсуждение того, как клиенты должны обрабатывать уведомления.</span><span class="sxs-lookup"><span data-stu-id="59557-176">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="59557-177">Поддержка уведомления о событиях</span><span class="sxs-lookup"><span data-stu-id="59557-177">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="59557-178">Обсуждение того, как поставщики услуг могут использовать [метод IMAPISupport](imapisupportiunknown.md) для создания уведомлений.</span><span class="sxs-lookup"><span data-stu-id="59557-178">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="59557-179">См. также</span><span class="sxs-lookup"><span data-stu-id="59557-179">See also</span></span>



[<span data-ttu-id="59557-180">�����������</span><span class="sxs-lookup"><span data-stu-id="59557-180">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="59557-181">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="59557-181">SPropTagArray</span></span>](sproptagarray.md)


[<span data-ttu-id="59557-182">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="59557-182">MAPI Structures</span></span>](mapi-structures.md)

