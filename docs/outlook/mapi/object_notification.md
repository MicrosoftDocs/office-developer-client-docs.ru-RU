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
# <a name="objectnotification"></a><span data-ttu-id="a8c0f-103">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="a8c0f-103">OBJECT_NOTIFICATION</span></span>

  
  
<span data-ttu-id="a8c0f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a8c0f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a8c0f-105">Содержит сведения об объекте, который был изменен, например копированием или изменением.</span><span class="sxs-lookup"><span data-stu-id="a8c0f-105">Contains information about an object that has undergone a change, such as being copied or modified.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a8c0f-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="a8c0f-106">Header file:</span></span>  <br/> |<span data-ttu-id="a8c0f-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="a8c0f-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="a8c0f-108">Members</span><span class="sxs-lookup"><span data-stu-id="a8c0f-108">Members</span></span>

 <span data-ttu-id="a8c0f-109">**Кбентрид**</span><span class="sxs-lookup"><span data-stu-id="a8c0f-109">**cbEntryID**</span></span>
  
> <span data-ttu-id="a8c0f-110">Количество байтов в идентификаторе записи, на который указывает элемент **лпентрид** .</span><span class="sxs-lookup"><span data-stu-id="a8c0f-110">Count of bytes in the entry identifier pointed to by the **lpEntryID** member.</span></span> 
    
 <span data-ttu-id="a8c0f-111">**Лпентрид**</span><span class="sxs-lookup"><span data-stu-id="a8c0f-111">**lpEntryID**</span></span>
  
> <span data-ttu-id="a8c0f-112">Указатель на идентификатор записи затрагиваемого объекта.</span><span class="sxs-lookup"><span data-stu-id="a8c0f-112">Pointer to the entry identifier of the affected object.</span></span>
    
 <span data-ttu-id="a8c0f-113">**Улобжтипе**</span><span class="sxs-lookup"><span data-stu-id="a8c0f-113">**ulObjType**</span></span>
  
> <span data-ttu-id="a8c0f-114">Тип затрагиваемого объекта.</span><span class="sxs-lookup"><span data-stu-id="a8c0f-114">Type of object affected.</span></span> <span data-ttu-id="a8c0f-115">Возможны следующие типы:</span><span class="sxs-lookup"><span data-stu-id="a8c0f-115">Possible types are as follows:</span></span>
    
<span data-ttu-id="a8c0f-116">МАПИ_СТОРЕ</span><span class="sxs-lookup"><span data-stu-id="a8c0f-116">MAPI_STORE</span></span> 
  
> <span data-ttu-id="a8c0f-117">Хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="a8c0f-117">Message store.</span></span> 
    
<span data-ttu-id="a8c0f-118">МАПИ_АДДРБУК</span><span class="sxs-lookup"><span data-stu-id="a8c0f-118">MAPI_ADDRBOOK</span></span> 
  
> <span data-ttu-id="a8c0f-119">Адресная книга.</span><span class="sxs-lookup"><span data-stu-id="a8c0f-119">Address book.</span></span> 
    
<span data-ttu-id="a8c0f-120">МАПИ_ФОЛДЕР</span><span class="sxs-lookup"><span data-stu-id="a8c0f-120">MAPI_FOLDER</span></span> 
  
> <span data-ttu-id="a8c0f-121">Папке.</span><span class="sxs-lookup"><span data-stu-id="a8c0f-121">Folder.</span></span>
    
<span data-ttu-id="a8c0f-122">МАПИ_АБКОНТ</span><span class="sxs-lookup"><span data-stu-id="a8c0f-122">MAPI_ABCONT</span></span> 
  
> <span data-ttu-id="a8c0f-123">Контейнер адресной книги.</span><span class="sxs-lookup"><span data-stu-id="a8c0f-123">Address book container.</span></span>
    
<span data-ttu-id="a8c0f-124">МАПИ_МЕССАЖЕ</span><span class="sxs-lookup"><span data-stu-id="a8c0f-124">MAPI_MESSAGE</span></span> 
  
> <span data-ttu-id="a8c0f-125">Сообщение.</span><span class="sxs-lookup"><span data-stu-id="a8c0f-125">Message.</span></span>
    
<span data-ttu-id="a8c0f-126">МАПИ_МАИЛУСЕР</span><span class="sxs-lookup"><span data-stu-id="a8c0f-126">MAPI_MAILUSER</span></span> 
  
> <span data-ttu-id="a8c0f-127">Пользователь обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="a8c0f-127">Messaging user.</span></span>
    
<span data-ttu-id="a8c0f-128">МАПИ_АТТАЧ</span><span class="sxs-lookup"><span data-stu-id="a8c0f-128">MAPI_ATTACH</span></span> 
  
> <span data-ttu-id="a8c0f-129">Крепление.</span><span class="sxs-lookup"><span data-stu-id="a8c0f-129">Attachment.</span></span>
    
<span data-ttu-id="a8c0f-130">МАПИ_ДИСТЛИСТ</span><span class="sxs-lookup"><span data-stu-id="a8c0f-130">MAPI_DISTLIST</span></span> 
  
> <span data-ttu-id="a8c0f-131">Список рассылки.</span><span class="sxs-lookup"><span data-stu-id="a8c0f-131">Distribution list.</span></span>
    
<span data-ttu-id="a8c0f-132">МАПИ_ПРОФСЕКТ</span><span class="sxs-lookup"><span data-stu-id="a8c0f-132">MAPI_PROFSECT</span></span> 
  
> <span data-ttu-id="a8c0f-133">Раздел "профиль".</span><span class="sxs-lookup"><span data-stu-id="a8c0f-133">Profile section.</span></span>
    
<span data-ttu-id="a8c0f-134">МАПИ_СТАТУС</span><span class="sxs-lookup"><span data-stu-id="a8c0f-134">MAPI_STATUS</span></span> 
  
> <span data-ttu-id="a8c0f-135">Объект Status.</span><span class="sxs-lookup"><span data-stu-id="a8c0f-135">Status object.</span></span>
    
<span data-ttu-id="a8c0f-136">МАПИ_СЕССИОН</span><span class="sxs-lookup"><span data-stu-id="a8c0f-136">MAPI_SESSION</span></span> 
  
> <span data-ttu-id="a8c0f-137">Объект Session.</span><span class="sxs-lookup"><span data-stu-id="a8c0f-137">Session object.</span></span>
    
 <span data-ttu-id="a8c0f-138">**Кбпарентид**</span><span class="sxs-lookup"><span data-stu-id="a8c0f-138">**cbParentID**</span></span>
  
> <span data-ttu-id="a8c0f-139">Количество байтов в идентификаторе записи, на который указывает элемент **лппарентид** .</span><span class="sxs-lookup"><span data-stu-id="a8c0f-139">Count of bytes in the entry identifier pointed to by the **lpParentID** member.</span></span> 
    
 <span data-ttu-id="a8c0f-140">**Лппарентид**</span><span class="sxs-lookup"><span data-stu-id="a8c0f-140">**lpParentID**</span></span>
  
> <span data-ttu-id="a8c0f-141">Указатель на идентификатор элемента родительского объекта затрагиваемого объекта.</span><span class="sxs-lookup"><span data-stu-id="a8c0f-141">Pointer to the entry identifier of the parent of the affected object.</span></span>
    
 <span data-ttu-id="a8c0f-142">**Кболдид**</span><span class="sxs-lookup"><span data-stu-id="a8c0f-142">**cbOldID**</span></span>
  
> <span data-ttu-id="a8c0f-143">Количество байтов в идентификаторе записи, на который указывает элемент **лполдид** .</span><span class="sxs-lookup"><span data-stu-id="a8c0f-143">Count of bytes in the entry identifier pointed to by the **lpOldID** member.</span></span> 
    
 <span data-ttu-id="a8c0f-144">**Лполдид**</span><span class="sxs-lookup"><span data-stu-id="a8c0f-144">**lpOldID**</span></span>
  
> <span data-ttu-id="a8c0f-145">Указатель на идентификатор элемента исходного объекта.</span><span class="sxs-lookup"><span data-stu-id="a8c0f-145">Pointer to the entry identifier of the original object.</span></span> <span data-ttu-id="a8c0f-146">Этот указатель может иметь значение NULL, если для события не требуется исходный объект.</span><span class="sxs-lookup"><span data-stu-id="a8c0f-146">This pointer can be NULL if the event does not require an original object.</span></span>
    
 <span data-ttu-id="a8c0f-147">**Кболдпарентид**</span><span class="sxs-lookup"><span data-stu-id="a8c0f-147">**cbOldParentID**</span></span>
  
> <span data-ttu-id="a8c0f-148">Количество байтов в идентификаторе записи, на который указывает элемент **лполдпарентид** .</span><span class="sxs-lookup"><span data-stu-id="a8c0f-148">Count of bytes in the entry identifier pointed to by the **lpOldParentID** member.</span></span> 
    
 <span data-ttu-id="a8c0f-149">**Лполдпарентид**</span><span class="sxs-lookup"><span data-stu-id="a8c0f-149">**lpOldParentID**</span></span>
  
> <span data-ttu-id="a8c0f-150">Указатель на идентификатор элемента родительского объекта исходного объекта.</span><span class="sxs-lookup"><span data-stu-id="a8c0f-150">Pointer to the entry identifier of the parent of the original object.</span></span> <span data-ttu-id="a8c0f-151">Этот указатель может иметь значение NULL, если для события не требуется исходный объект.</span><span class="sxs-lookup"><span data-stu-id="a8c0f-151">This pointer can be NULL if the event does not require an original object.</span></span>
    
 <span data-ttu-id="a8c0f-152">**Лппроптагаррай**</span><span class="sxs-lookup"><span data-stu-id="a8c0f-152">**lpPropTagArray**</span></span>
  
> <span data-ttu-id="a8c0f-153">Указатель на структуру [спроптагаррай](sproptagarray.md) , которая содержит теги свойств, определяющие свойства, затрагиваемые событием.</span><span class="sxs-lookup"><span data-stu-id="a8c0f-153">Pointer to an [SPropTagArray](sproptagarray.md) structure that contains the property tags identifying properties affected by the event.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a8c0f-154">Примечания</span><span class="sxs-lookup"><span data-stu-id="a8c0f-154">Remarks</span></span>

<span data-ttu-id="a8c0f-155">Структура **обжект_нотификатион** — это один из членов объединения структур, включенных в элемент **info** структуры [уведомления](notification.md) .</span><span class="sxs-lookup"><span data-stu-id="a8c0f-155">The **OBJECT_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="a8c0f-156">Когда элемент **info** структуры **уведомлений** содержит структуру **обжект_нотификатион** , для элемента **улевенттипе** структуры **уведомлений** задается один из следующих типов событий:</span><span class="sxs-lookup"><span data-stu-id="a8c0f-156">When the **info** member of a **NOTIFICATION** structure contains an **OBJECT_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to one of the following types of events:</span></span> 
  
- <span data-ttu-id="a8c0f-157">Фневобжекткреатед</span><span class="sxs-lookup"><span data-stu-id="a8c0f-157">fnevObjectCreated</span></span>
    
- <span data-ttu-id="a8c0f-158">Фневобжектмодифиед</span><span class="sxs-lookup"><span data-stu-id="a8c0f-158">fnevObjectModified</span></span>
    
- <span data-ttu-id="a8c0f-159">Фневобжектделетед</span><span class="sxs-lookup"><span data-stu-id="a8c0f-159">fnevObjectDeleted</span></span>
    
- <span data-ttu-id="a8c0f-160">Фневобжектмовед</span><span class="sxs-lookup"><span data-stu-id="a8c0f-160">fnevObjectMoved</span></span>
    
- <span data-ttu-id="a8c0f-161">Фневобжекткопиед</span><span class="sxs-lookup"><span data-stu-id="a8c0f-161">fnevObjectCopied</span></span>
    
- <span data-ttu-id="a8c0f-162">Фневсеарчкомплете</span><span class="sxs-lookup"><span data-stu-id="a8c0f-162">fnevSearchComplete</span></span>
    
<span data-ttu-id="a8c0f-163">Событие завершения поиска, представленное типом события Фневсеарчкомплете, указывает на то, что исходный Поиск в домене для одной папки поиска выполнен.</span><span class="sxs-lookup"><span data-stu-id="a8c0f-163">The search complete event, represented by the fnevSearchComplete event type, indicates that the initial search of the domain for one search folder has completed.</span></span>
  
<span data-ttu-id="a8c0f-164">Следующие элементы, содержащие сведения об исходном объекте, используются только в событиях перемещения и копирования.</span><span class="sxs-lookup"><span data-stu-id="a8c0f-164">The following members that contain information about the original object are used only in move and copy events.</span></span> 
  
- <span data-ttu-id="a8c0f-165">**Кболдид**</span><span class="sxs-lookup"><span data-stu-id="a8c0f-165">**cbOldID**</span></span>
    
- <span data-ttu-id="a8c0f-166">**Лполдид**</span><span class="sxs-lookup"><span data-stu-id="a8c0f-166">**lpOldID**</span></span>
    
- <span data-ttu-id="a8c0f-167">**Кболдпарентид**</span><span class="sxs-lookup"><span data-stu-id="a8c0f-167">**cbOldParentID**</span></span>
    
- <span data-ttu-id="a8c0f-168">**Лполдпарентид**</span><span class="sxs-lookup"><span data-stu-id="a8c0f-168">**lpOldParentID**</span></span>
    
<span data-ttu-id="a8c0f-169">Эти элементы не применяются к другим типам событий.</span><span class="sxs-lookup"><span data-stu-id="a8c0f-169">These members do not apply to the other types of events.</span></span>
  
<span data-ttu-id="a8c0f-170">Дополнительные сведения об уведомлении можно найти в разделах, приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="a8c0f-170">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="a8c0f-171">**Статья**</span><span class="sxs-lookup"><span data-stu-id="a8c0f-171">**Topic**</span></span>|<span data-ttu-id="a8c0f-172">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a8c0f-172">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a8c0f-173">Уведомление о соБытии в MAPI</span><span class="sxs-lookup"><span data-stu-id="a8c0f-173">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="a8c0f-174">Общие сведения о событиях уведомлений и уведомлений.</span><span class="sxs-lookup"><span data-stu-id="a8c0f-174">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="a8c0f-175">Обработка уведомлений</span><span class="sxs-lookup"><span data-stu-id="a8c0f-175">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="a8c0f-176">Обсуждение того, как клиенты должны обрабатывать уведомления.</span><span class="sxs-lookup"><span data-stu-id="a8c0f-176">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="a8c0f-177">Поддержка уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="a8c0f-177">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="a8c0f-178">Обсуждение того, как поставщики услуг могут использовать метод [имаписуппорт](imapisupportiunknown.md) для создания уведомлений.</span><span class="sxs-lookup"><span data-stu-id="a8c0f-178">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a8c0f-179">См. также</span><span class="sxs-lookup"><span data-stu-id="a8c0f-179">See also</span></span>



[<span data-ttu-id="a8c0f-180">�����������</span><span class="sxs-lookup"><span data-stu-id="a8c0f-180">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="a8c0f-181">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="a8c0f-181">SPropTagArray</span></span>](sproptagarray.md)


[<span data-ttu-id="a8c0f-182">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="a8c0f-182">MAPI Structures</span></span>](mapi-structures.md)

