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
# <a name="object_notification"></a><span data-ttu-id="aa653-103">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="aa653-103">OBJECT_NOTIFICATION</span></span>

  
  
<span data-ttu-id="aa653-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aa653-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aa653-105">Содержит сведения об объекте, который был изменен, например копированием или изменением.</span><span class="sxs-lookup"><span data-stu-id="aa653-105">Contains information about an object that has undergone a change, such as being copied or modified.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="aa653-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="aa653-106">Header file:</span></span>  <br/> |<span data-ttu-id="aa653-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="aa653-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="aa653-108">"Участники"</span><span class="sxs-lookup"><span data-stu-id="aa653-108">Members</span></span>

 <span data-ttu-id="aa653-109">**кбентрид**</span><span class="sxs-lookup"><span data-stu-id="aa653-109">**cbEntryID**</span></span>
  
> <span data-ttu-id="aa653-110">Количество байтов в идентификаторе записи, на который указывает элемент **лпентрид** .</span><span class="sxs-lookup"><span data-stu-id="aa653-110">Count of bytes in the entry identifier pointed to by the **lpEntryID** member.</span></span> 
    
 <span data-ttu-id="aa653-111">**лпентрид**</span><span class="sxs-lookup"><span data-stu-id="aa653-111">**lpEntryID**</span></span>
  
> <span data-ttu-id="aa653-112">Указатель на идентификатор записи затрагиваемого объекта.</span><span class="sxs-lookup"><span data-stu-id="aa653-112">Pointer to the entry identifier of the affected object.</span></span>
    
 <span data-ttu-id="aa653-113">**улобжтипе**</span><span class="sxs-lookup"><span data-stu-id="aa653-113">**ulObjType**</span></span>
  
> <span data-ttu-id="aa653-114">Тип затрагиваемого объекта.</span><span class="sxs-lookup"><span data-stu-id="aa653-114">Type of object affected.</span></span> <span data-ttu-id="aa653-115">Возможны следующие типы:</span><span class="sxs-lookup"><span data-stu-id="aa653-115">Possible types are as follows:</span></span>
    
<span data-ttu-id="aa653-116">MAPI_STORE</span><span class="sxs-lookup"><span data-stu-id="aa653-116">MAPI_STORE</span></span> 
  
> <span data-ttu-id="aa653-117">Хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="aa653-117">Message store.</span></span> 
    
<span data-ttu-id="aa653-118">MAPI_ADDRBOOK</span><span class="sxs-lookup"><span data-stu-id="aa653-118">MAPI_ADDRBOOK</span></span> 
  
> <span data-ttu-id="aa653-119">Адресная книга.</span><span class="sxs-lookup"><span data-stu-id="aa653-119">Address book.</span></span> 
    
<span data-ttu-id="aa653-120">MAPI_FOLDER</span><span class="sxs-lookup"><span data-stu-id="aa653-120">MAPI_FOLDER</span></span> 
  
> <span data-ttu-id="aa653-121">Папке.</span><span class="sxs-lookup"><span data-stu-id="aa653-121">Folder.</span></span>
    
<span data-ttu-id="aa653-122">MAPI_ABCONT</span><span class="sxs-lookup"><span data-stu-id="aa653-122">MAPI_ABCONT</span></span> 
  
> <span data-ttu-id="aa653-123">Контейнер адресной книги.</span><span class="sxs-lookup"><span data-stu-id="aa653-123">Address book container.</span></span>
    
<span data-ttu-id="aa653-124">MAPI_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="aa653-124">MAPI_MESSAGE</span></span> 
  
> <span data-ttu-id="aa653-125">Сообщение.</span><span class="sxs-lookup"><span data-stu-id="aa653-125">Message.</span></span>
    
<span data-ttu-id="aa653-126">MAPI_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="aa653-126">MAPI_MAILUSER</span></span> 
  
> <span data-ttu-id="aa653-127">Пользователь обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="aa653-127">Messaging user.</span></span>
    
<span data-ttu-id="aa653-128">MAPI_ATTACH</span><span class="sxs-lookup"><span data-stu-id="aa653-128">MAPI_ATTACH</span></span> 
  
> <span data-ttu-id="aa653-129">Крепление.</span><span class="sxs-lookup"><span data-stu-id="aa653-129">Attachment.</span></span>
    
<span data-ttu-id="aa653-130">MAPI_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="aa653-130">MAPI_DISTLIST</span></span> 
  
> <span data-ttu-id="aa653-131">Список рассылки.</span><span class="sxs-lookup"><span data-stu-id="aa653-131">Distribution list.</span></span>
    
<span data-ttu-id="aa653-132">MAPI_PROFSECT</span><span class="sxs-lookup"><span data-stu-id="aa653-132">MAPI_PROFSECT</span></span> 
  
> <span data-ttu-id="aa653-133">Раздел "профиль".</span><span class="sxs-lookup"><span data-stu-id="aa653-133">Profile section.</span></span>
    
<span data-ttu-id="aa653-134">MAPI_STATUS</span><span class="sxs-lookup"><span data-stu-id="aa653-134">MAPI_STATUS</span></span> 
  
> <span data-ttu-id="aa653-135">Объект Status.</span><span class="sxs-lookup"><span data-stu-id="aa653-135">Status object.</span></span>
    
<span data-ttu-id="aa653-136">MAPI_SESSION</span><span class="sxs-lookup"><span data-stu-id="aa653-136">MAPI_SESSION</span></span> 
  
> <span data-ttu-id="aa653-137">Объект Session.</span><span class="sxs-lookup"><span data-stu-id="aa653-137">Session object.</span></span>
    
 <span data-ttu-id="aa653-138">**кбпарентид**</span><span class="sxs-lookup"><span data-stu-id="aa653-138">**cbParentID**</span></span>
  
> <span data-ttu-id="aa653-139">Количество байтов в идентификаторе записи, на который указывает элемент **лппарентид** .</span><span class="sxs-lookup"><span data-stu-id="aa653-139">Count of bytes in the entry identifier pointed to by the **lpParentID** member.</span></span> 
    
 <span data-ttu-id="aa653-140">**лппарентид**</span><span class="sxs-lookup"><span data-stu-id="aa653-140">**lpParentID**</span></span>
  
> <span data-ttu-id="aa653-141">Указатель на идентификатор элемента родительского объекта затрагиваемого объекта.</span><span class="sxs-lookup"><span data-stu-id="aa653-141">Pointer to the entry identifier of the parent of the affected object.</span></span>
    
 <span data-ttu-id="aa653-142">**кболдид**</span><span class="sxs-lookup"><span data-stu-id="aa653-142">**cbOldID**</span></span>
  
> <span data-ttu-id="aa653-143">Количество байтов в идентификаторе записи, на который указывает элемент **лполдид** .</span><span class="sxs-lookup"><span data-stu-id="aa653-143">Count of bytes in the entry identifier pointed to by the **lpOldID** member.</span></span> 
    
 <span data-ttu-id="aa653-144">**лполдид**</span><span class="sxs-lookup"><span data-stu-id="aa653-144">**lpOldID**</span></span>
  
> <span data-ttu-id="aa653-145">Указатель на идентификатор элемента исходного объекта.</span><span class="sxs-lookup"><span data-stu-id="aa653-145">Pointer to the entry identifier of the original object.</span></span> <span data-ttu-id="aa653-146">Этот указатель может иметь значение NULL, если для события не требуется исходный объект.</span><span class="sxs-lookup"><span data-stu-id="aa653-146">This pointer can be NULL if the event does not require an original object.</span></span>
    
 <span data-ttu-id="aa653-147">**кболдпарентид**</span><span class="sxs-lookup"><span data-stu-id="aa653-147">**cbOldParentID**</span></span>
  
> <span data-ttu-id="aa653-148">Количество байтов в идентификаторе записи, на который указывает элемент **лполдпарентид** .</span><span class="sxs-lookup"><span data-stu-id="aa653-148">Count of bytes in the entry identifier pointed to by the **lpOldParentID** member.</span></span> 
    
 <span data-ttu-id="aa653-149">**лполдпарентид**</span><span class="sxs-lookup"><span data-stu-id="aa653-149">**lpOldParentID**</span></span>
  
> <span data-ttu-id="aa653-150">Указатель на идентификатор элемента родительского объекта исходного объекта.</span><span class="sxs-lookup"><span data-stu-id="aa653-150">Pointer to the entry identifier of the parent of the original object.</span></span> <span data-ttu-id="aa653-151">Этот указатель может иметь значение NULL, если для события не требуется исходный объект.</span><span class="sxs-lookup"><span data-stu-id="aa653-151">This pointer can be NULL if the event does not require an original object.</span></span>
    
 <span data-ttu-id="aa653-152">**лппроптагаррай**</span><span class="sxs-lookup"><span data-stu-id="aa653-152">**lpPropTagArray**</span></span>
  
> <span data-ttu-id="aa653-153">Указатель на структуру [спроптагаррай](sproptagarray.md) , которая содержит теги свойств, определяющие свойства, затрагиваемые событием.</span><span class="sxs-lookup"><span data-stu-id="aa653-153">Pointer to an [SPropTagArray](sproptagarray.md) structure that contains the property tags identifying properties affected by the event.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="aa653-154">Примечания</span><span class="sxs-lookup"><span data-stu-id="aa653-154">Remarks</span></span>

<span data-ttu-id="aa653-155">Структура **OBJECT_NOTIFICATION** — это один из членов объединения структур, включенных в элемент **info** структуры [уведомления](notification.md) .</span><span class="sxs-lookup"><span data-stu-id="aa653-155">The **OBJECT_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="aa653-156">Когда элемент **info** элемента структуры **уведомлений** содержит структуру **OBJECT_NOTIFICATION** , элемент **улевенттипе** структуры **уведомлений** задается одним из следующих типов событий:</span><span class="sxs-lookup"><span data-stu-id="aa653-156">When the **info** member of a **NOTIFICATION** structure contains an **OBJECT_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to one of the following types of events:</span></span> 
  
- <span data-ttu-id="aa653-157">фневобжекткреатед</span><span class="sxs-lookup"><span data-stu-id="aa653-157">fnevObjectCreated</span></span>
    
- <span data-ttu-id="aa653-158">фневобжектмодифиед</span><span class="sxs-lookup"><span data-stu-id="aa653-158">fnevObjectModified</span></span>
    
- <span data-ttu-id="aa653-159">фневобжектделетед</span><span class="sxs-lookup"><span data-stu-id="aa653-159">fnevObjectDeleted</span></span>
    
- <span data-ttu-id="aa653-160">фневобжектмовед</span><span class="sxs-lookup"><span data-stu-id="aa653-160">fnevObjectMoved</span></span>
    
- <span data-ttu-id="aa653-161">фневобжекткопиед</span><span class="sxs-lookup"><span data-stu-id="aa653-161">fnevObjectCopied</span></span>
    
- <span data-ttu-id="aa653-162">фневсеарчкомплете</span><span class="sxs-lookup"><span data-stu-id="aa653-162">fnevSearchComplete</span></span>
    
<span data-ttu-id="aa653-163">Событие завершения поиска, представленное типом события Фневсеарчкомплете, указывает на то, что исходный Поиск в домене для одной папки поиска выполнен.</span><span class="sxs-lookup"><span data-stu-id="aa653-163">The search complete event, represented by the fnevSearchComplete event type, indicates that the initial search of the domain for one search folder has completed.</span></span>
  
<span data-ttu-id="aa653-164">Следующие элементы, содержащие сведения об исходном объекте, используются только в событиях перемещения и копирования.</span><span class="sxs-lookup"><span data-stu-id="aa653-164">The following members that contain information about the original object are used only in move and copy events.</span></span> 
  
- <span data-ttu-id="aa653-165">**кболдид**</span><span class="sxs-lookup"><span data-stu-id="aa653-165">**cbOldID**</span></span>
    
- <span data-ttu-id="aa653-166">**лполдид**</span><span class="sxs-lookup"><span data-stu-id="aa653-166">**lpOldID**</span></span>
    
- <span data-ttu-id="aa653-167">**кболдпарентид**</span><span class="sxs-lookup"><span data-stu-id="aa653-167">**cbOldParentID**</span></span>
    
- <span data-ttu-id="aa653-168">**лполдпарентид**</span><span class="sxs-lookup"><span data-stu-id="aa653-168">**lpOldParentID**</span></span>
    
<span data-ttu-id="aa653-169">Эти элементы не применяются к другим типам событий.</span><span class="sxs-lookup"><span data-stu-id="aa653-169">These members do not apply to the other types of events.</span></span>
  
<span data-ttu-id="aa653-170">Дополнительные сведения об уведомлении можно найти в разделах, приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="aa653-170">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="aa653-171">**Статья**</span><span class="sxs-lookup"><span data-stu-id="aa653-171">**Topic**</span></span>|<span data-ttu-id="aa653-172">**Описание**</span><span class="sxs-lookup"><span data-stu-id="aa653-172">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="aa653-173">Уведомление о событии в MAPI</span><span class="sxs-lookup"><span data-stu-id="aa653-173">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="aa653-174">Общие сведения о событиях уведомлений и уведомлений.</span><span class="sxs-lookup"><span data-stu-id="aa653-174">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="aa653-175">Обработка уведомлений</span><span class="sxs-lookup"><span data-stu-id="aa653-175">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="aa653-176">Обсуждение того, как клиенты должны обрабатывать уведомления.</span><span class="sxs-lookup"><span data-stu-id="aa653-176">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="aa653-177">Поддержка уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="aa653-177">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="aa653-178">Обсуждение того, как поставщики услуг могут использовать метод [имаписуппорт](imapisupportiunknown.md) для создания уведомлений.</span><span class="sxs-lookup"><span data-stu-id="aa653-178">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="aa653-179">См. также</span><span class="sxs-lookup"><span data-stu-id="aa653-179">See also</span></span>



[<span data-ttu-id="aa653-180">�����������</span><span class="sxs-lookup"><span data-stu-id="aa653-180">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="aa653-181">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="aa653-181">SPropTagArray</span></span>](sproptagarray.md)


[<span data-ttu-id="aa653-182">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="aa653-182">MAPI Structures</span></span>](mapi-structures.md)

