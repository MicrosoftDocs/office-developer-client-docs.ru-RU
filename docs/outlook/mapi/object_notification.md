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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279888"
---
# <a name="objectnotification"></a><span data-ttu-id="f327e-103">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="f327e-103">OBJECT_NOTIFICATION</span></span>

  
  
<span data-ttu-id="f327e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f327e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f327e-105">Содержит сведения об объекте, который был изменен, например копированием или изменением.</span><span class="sxs-lookup"><span data-stu-id="f327e-105">Contains information about an object that has undergone a change, such as being copied or modified.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f327e-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="f327e-106">Header file:</span></span>  <br/> |<span data-ttu-id="f327e-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="f327e-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="f327e-108">Members</span><span class="sxs-lookup"><span data-stu-id="f327e-108">Members</span></span>

 <span data-ttu-id="f327e-109">**Кбентрид**</span><span class="sxs-lookup"><span data-stu-id="f327e-109">**cbEntryID**</span></span>
  
> <span data-ttu-id="f327e-110">Количество байтов в идентификаторе записи, на который указывает элемент **лпентрид** .</span><span class="sxs-lookup"><span data-stu-id="f327e-110">Count of bytes in the entry identifier pointed to by the **lpEntryID** member.</span></span> 
    
 <span data-ttu-id="f327e-111">**Лпентрид**</span><span class="sxs-lookup"><span data-stu-id="f327e-111">**lpEntryID**</span></span>
  
> <span data-ttu-id="f327e-112">Указатель на идентификатор записи затрагиваемого объекта.</span><span class="sxs-lookup"><span data-stu-id="f327e-112">Pointer to the entry identifier of the affected object.</span></span>
    
 <span data-ttu-id="f327e-113">**Улобжтипе**</span><span class="sxs-lookup"><span data-stu-id="f327e-113">**ulObjType**</span></span>
  
> <span data-ttu-id="f327e-114">Тип затрагиваемого объекта.</span><span class="sxs-lookup"><span data-stu-id="f327e-114">Type of object affected.</span></span> <span data-ttu-id="f327e-115">Возможны следующие типы:</span><span class="sxs-lookup"><span data-stu-id="f327e-115">Possible types are as follows:</span></span>
    
<span data-ttu-id="f327e-116">МАПИ_СТОРЕ</span><span class="sxs-lookup"><span data-stu-id="f327e-116">MAPI_STORE</span></span> 
  
> <span data-ttu-id="f327e-117">Хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="f327e-117">Message store.</span></span> 
    
<span data-ttu-id="f327e-118">МАПИ_АДДРБУК</span><span class="sxs-lookup"><span data-stu-id="f327e-118">MAPI_ADDRBOOK</span></span> 
  
> <span data-ttu-id="f327e-119">Адресная книга.</span><span class="sxs-lookup"><span data-stu-id="f327e-119">Address book.</span></span> 
    
<span data-ttu-id="f327e-120">МАПИ_ФОЛДЕР</span><span class="sxs-lookup"><span data-stu-id="f327e-120">MAPI_FOLDER</span></span> 
  
> <span data-ttu-id="f327e-121">Папке.</span><span class="sxs-lookup"><span data-stu-id="f327e-121">Folder.</span></span>
    
<span data-ttu-id="f327e-122">МАПИ_АБКОНТ</span><span class="sxs-lookup"><span data-stu-id="f327e-122">MAPI_ABCONT</span></span> 
  
> <span data-ttu-id="f327e-123">Контейнер адресной книги.</span><span class="sxs-lookup"><span data-stu-id="f327e-123">Address book container.</span></span>
    
<span data-ttu-id="f327e-124">МАПИ_МЕССАЖЕ</span><span class="sxs-lookup"><span data-stu-id="f327e-124">MAPI_MESSAGE</span></span> 
  
> <span data-ttu-id="f327e-125">Сообщение.</span><span class="sxs-lookup"><span data-stu-id="f327e-125">Message.</span></span>
    
<span data-ttu-id="f327e-126">МАПИ_МАИЛУСЕР</span><span class="sxs-lookup"><span data-stu-id="f327e-126">MAPI_MAILUSER</span></span> 
  
> <span data-ttu-id="f327e-127">Пользователь обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="f327e-127">Messaging user.</span></span>
    
<span data-ttu-id="f327e-128">МАПИ_АТТАЧ</span><span class="sxs-lookup"><span data-stu-id="f327e-128">MAPI_ATTACH</span></span> 
  
> <span data-ttu-id="f327e-129">Крепление.</span><span class="sxs-lookup"><span data-stu-id="f327e-129">Attachment.</span></span>
    
<span data-ttu-id="f327e-130">МАПИ_ДИСТЛИСТ</span><span class="sxs-lookup"><span data-stu-id="f327e-130">MAPI_DISTLIST</span></span> 
  
> <span data-ttu-id="f327e-131">Список рассылки.</span><span class="sxs-lookup"><span data-stu-id="f327e-131">Distribution list.</span></span>
    
<span data-ttu-id="f327e-132">МАПИ_ПРОФСЕКТ</span><span class="sxs-lookup"><span data-stu-id="f327e-132">MAPI_PROFSECT</span></span> 
  
> <span data-ttu-id="f327e-133">Раздел "профиль".</span><span class="sxs-lookup"><span data-stu-id="f327e-133">Profile section.</span></span>
    
<span data-ttu-id="f327e-134">МАПИ_СТАТУС</span><span class="sxs-lookup"><span data-stu-id="f327e-134">MAPI_STATUS</span></span> 
  
> <span data-ttu-id="f327e-135">Объект Status.</span><span class="sxs-lookup"><span data-stu-id="f327e-135">Status object.</span></span>
    
<span data-ttu-id="f327e-136">МАПИ_СЕССИОН</span><span class="sxs-lookup"><span data-stu-id="f327e-136">MAPI_SESSION</span></span> 
  
> <span data-ttu-id="f327e-137">Объект Session.</span><span class="sxs-lookup"><span data-stu-id="f327e-137">Session object.</span></span>
    
 <span data-ttu-id="f327e-138">**Кбпарентид**</span><span class="sxs-lookup"><span data-stu-id="f327e-138">**cbParentID**</span></span>
  
> <span data-ttu-id="f327e-139">Количество байтов в идентификаторе записи, на который указывает элемент **лппарентид** .</span><span class="sxs-lookup"><span data-stu-id="f327e-139">Count of bytes in the entry identifier pointed to by the **lpParentID** member.</span></span> 
    
 <span data-ttu-id="f327e-140">**Лппарентид**</span><span class="sxs-lookup"><span data-stu-id="f327e-140">**lpParentID**</span></span>
  
> <span data-ttu-id="f327e-141">Указатель на идентификатор элемента родительского объекта затрагиваемого объекта.</span><span class="sxs-lookup"><span data-stu-id="f327e-141">Pointer to the entry identifier of the parent of the affected object.</span></span>
    
 <span data-ttu-id="f327e-142">**Кболдид**</span><span class="sxs-lookup"><span data-stu-id="f327e-142">**cbOldID**</span></span>
  
> <span data-ttu-id="f327e-143">Количество байтов в идентификаторе записи, на который указывает элемент **лполдид** .</span><span class="sxs-lookup"><span data-stu-id="f327e-143">Count of bytes in the entry identifier pointed to by the **lpOldID** member.</span></span> 
    
 <span data-ttu-id="f327e-144">**Лполдид**</span><span class="sxs-lookup"><span data-stu-id="f327e-144">**lpOldID**</span></span>
  
> <span data-ttu-id="f327e-145">Указатель на идентификатор элемента исходного объекта.</span><span class="sxs-lookup"><span data-stu-id="f327e-145">Pointer to the entry identifier of the original object.</span></span> <span data-ttu-id="f327e-146">Этот указатель может иметь значение NULL, если для события не требуется исходный объект.</span><span class="sxs-lookup"><span data-stu-id="f327e-146">This pointer can be NULL if the event does not require an original object.</span></span>
    
 <span data-ttu-id="f327e-147">**Кболдпарентид**</span><span class="sxs-lookup"><span data-stu-id="f327e-147">**cbOldParentID**</span></span>
  
> <span data-ttu-id="f327e-148">Количество байтов в идентификаторе записи, на который указывает элемент **лполдпарентид** .</span><span class="sxs-lookup"><span data-stu-id="f327e-148">Count of bytes in the entry identifier pointed to by the **lpOldParentID** member.</span></span> 
    
 <span data-ttu-id="f327e-149">**Лполдпарентид**</span><span class="sxs-lookup"><span data-stu-id="f327e-149">**lpOldParentID**</span></span>
  
> <span data-ttu-id="f327e-150">Указатель на идентификатор элемента родительского объекта исходного объекта.</span><span class="sxs-lookup"><span data-stu-id="f327e-150">Pointer to the entry identifier of the parent of the original object.</span></span> <span data-ttu-id="f327e-151">Этот указатель может иметь значение NULL, если для события не требуется исходный объект.</span><span class="sxs-lookup"><span data-stu-id="f327e-151">This pointer can be NULL if the event does not require an original object.</span></span>
    
 <span data-ttu-id="f327e-152">**Лппроптагаррай**</span><span class="sxs-lookup"><span data-stu-id="f327e-152">**lpPropTagArray**</span></span>
  
> <span data-ttu-id="f327e-153">Указатель на структуру [спроптагаррай](sproptagarray.md) , которая содержит теги свойств, определяющие свойства, затрагиваемые событием.</span><span class="sxs-lookup"><span data-stu-id="f327e-153">Pointer to an [SPropTagArray](sproptagarray.md) structure that contains the property tags identifying properties affected by the event.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="f327e-154">Замечания</span><span class="sxs-lookup"><span data-stu-id="f327e-154">Remarks</span></span>

<span data-ttu-id="f327e-155">Структура **обжект_нотификатион** — это один из членов объединения структур, включенных в элемент **info** структуры [уведомления](notification.md) .</span><span class="sxs-lookup"><span data-stu-id="f327e-155">The **OBJECT_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="f327e-156">Когда элемент **info** структуры **уведомлений** содержит структуру **обжект_нотификатион** , для элемента **улевенттипе** структуры **уведомлений** задается один из следующих типов событий:</span><span class="sxs-lookup"><span data-stu-id="f327e-156">When the **info** member of a **NOTIFICATION** structure contains an **OBJECT_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to one of the following types of events:</span></span> 
  
- <span data-ttu-id="f327e-157">Фневобжекткреатед</span><span class="sxs-lookup"><span data-stu-id="f327e-157">fnevObjectCreated</span></span>
    
- <span data-ttu-id="f327e-158">Фневобжектмодифиед</span><span class="sxs-lookup"><span data-stu-id="f327e-158">fnevObjectModified</span></span>
    
- <span data-ttu-id="f327e-159">Фневобжектделетед</span><span class="sxs-lookup"><span data-stu-id="f327e-159">fnevObjectDeleted</span></span>
    
- <span data-ttu-id="f327e-160">Фневобжектмовед</span><span class="sxs-lookup"><span data-stu-id="f327e-160">fnevObjectMoved</span></span>
    
- <span data-ttu-id="f327e-161">Фневобжекткопиед</span><span class="sxs-lookup"><span data-stu-id="f327e-161">fnevObjectCopied</span></span>
    
- <span data-ttu-id="f327e-162">Фневсеарчкомплете</span><span class="sxs-lookup"><span data-stu-id="f327e-162">fnevSearchComplete</span></span>
    
<span data-ttu-id="f327e-163">Событие завершения поиска, представленное типом события Фневсеарчкомплете, указывает на то, что исходный Поиск в домене для одной папки поиска выполнен.</span><span class="sxs-lookup"><span data-stu-id="f327e-163">The search complete event, represented by the fnevSearchComplete event type, indicates that the initial search of the domain for one search folder has completed.</span></span>
  
<span data-ttu-id="f327e-164">Следующие элементы, содержащие сведения об исходном объекте, используются только в событиях перемещения и копирования.</span><span class="sxs-lookup"><span data-stu-id="f327e-164">The following members that contain information about the original object are used only in move and copy events.</span></span> 
  
- <span data-ttu-id="f327e-165">**Кболдид**</span><span class="sxs-lookup"><span data-stu-id="f327e-165">**cbOldID**</span></span>
    
- <span data-ttu-id="f327e-166">**Лполдид**</span><span class="sxs-lookup"><span data-stu-id="f327e-166">**lpOldID**</span></span>
    
- <span data-ttu-id="f327e-167">**Кболдпарентид**</span><span class="sxs-lookup"><span data-stu-id="f327e-167">**cbOldParentID**</span></span>
    
- <span data-ttu-id="f327e-168">**Лполдпарентид**</span><span class="sxs-lookup"><span data-stu-id="f327e-168">**lpOldParentID**</span></span>
    
<span data-ttu-id="f327e-169">Эти элементы не применяются к другим типам событий.</span><span class="sxs-lookup"><span data-stu-id="f327e-169">These members do not apply to the other types of events.</span></span>
  
<span data-ttu-id="f327e-170">Дополнительные сведения об уведомлении можно найти в разделах, приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="f327e-170">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="f327e-171">**Статья**</span><span class="sxs-lookup"><span data-stu-id="f327e-171">**Topic**</span></span>|<span data-ttu-id="f327e-172">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f327e-172">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f327e-173">Уведомление о соБытии в MAPI</span><span class="sxs-lookup"><span data-stu-id="f327e-173">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="f327e-174">Общие сведения о событиях уведомлений и уведомлений.</span><span class="sxs-lookup"><span data-stu-id="f327e-174">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="f327e-175">Обработка уведомлений</span><span class="sxs-lookup"><span data-stu-id="f327e-175">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="f327e-176">Обсуждение того, как клиенты должны обрабатывать уведомления.</span><span class="sxs-lookup"><span data-stu-id="f327e-176">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="f327e-177">Поддержка уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="f327e-177">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="f327e-178">Обсуждение того, как поставщики услуг могут использовать метод [имаписуппорт](imapisupportiunknown.md) для создания уведомлений.</span><span class="sxs-lookup"><span data-stu-id="f327e-178">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f327e-179">См. также</span><span class="sxs-lookup"><span data-stu-id="f327e-179">See also</span></span>



[<span data-ttu-id="f327e-180">�����������</span><span class="sxs-lookup"><span data-stu-id="f327e-180">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="f327e-181">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="f327e-181">SPropTagArray</span></span>](sproptagarray.md)


[<span data-ttu-id="f327e-182">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="f327e-182">MAPI Structures</span></span>](mapi-structures.md)

