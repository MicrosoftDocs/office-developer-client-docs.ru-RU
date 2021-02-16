---
title: NEWMAIL_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.NEWMAIL_NOTIFICATION
api_type:
- COM
ms.assetid: 49913050-900a-4b05-84c4-c596a93ce68b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 25af1c1b05618d4f36a43721e71be6ff5c7c597f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439858"
---
# <a name="newmail_notification"></a><span data-ttu-id="0d252-103">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="0d252-103">NEWMAIL_NOTIFICATION</span></span>

  
  
<span data-ttu-id="0d252-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0d252-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0d252-105">Описывает сведения, которые относятся к поступлению нового сообщения.</span><span class="sxs-lookup"><span data-stu-id="0d252-105">Describes information that relate to the arrival of a new message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0d252-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="0d252-106">Header file:</span></span>  <br/> |<span data-ttu-id="0d252-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0d252-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _NEWMAIL_NOTIFICATION
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  ULONG cbParentID;
  LPENTRYID lpParentID;
  ULONG ulFlags;
  LPSTR lpszMessageClass;
  ULONG ulMessageFlags;
} NEWMAIL_NOTIFICATION;

```

## <a name="members"></a><span data-ttu-id="0d252-108">"Участники"</span><span class="sxs-lookup"><span data-stu-id="0d252-108">Members</span></span>

 <span data-ttu-id="0d252-109">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="0d252-109">**cbEntryID**</span></span>
  
> <span data-ttu-id="0d252-110">Количество вхождений в идентификаторе записи, на который указывает **член lpEntryID.**</span><span class="sxs-lookup"><span data-stu-id="0d252-110">Count of bytes in the entry identifier pointed to by the **lpEntryID** member.</span></span> 
    
 <span data-ttu-id="0d252-111">**lpEntryID**</span><span class="sxs-lookup"><span data-stu-id="0d252-111">**lpEntryID**</span></span>
  
> <span data-ttu-id="0d252-112">Указатель на идентификатор записи нового сообщения.</span><span class="sxs-lookup"><span data-stu-id="0d252-112">Pointer to the entry identifier of the newly arrived message.</span></span>
    
 <span data-ttu-id="0d252-113">**cbParentID**</span><span class="sxs-lookup"><span data-stu-id="0d252-113">**cbParentID**</span></span>
  
> <span data-ttu-id="0d252-114">Количествобайтов в идентификаторе записи, на который указывает **член lpParentID.**</span><span class="sxs-lookup"><span data-stu-id="0d252-114">Count of bytes in the entry identifier pointed to by the **lpParentID** member.</span></span> 
    
 <span data-ttu-id="0d252-115">**lpParentID**</span><span class="sxs-lookup"><span data-stu-id="0d252-115">**lpParentID**</span></span>
  
> <span data-ttu-id="0d252-116">Указатель на идентификатор записи папки получения для нового сообщения.</span><span class="sxs-lookup"><span data-stu-id="0d252-116">Pointer to the entry identifier of the receive folder for the newly arrived message.</span></span>
    
 <span data-ttu-id="0d252-117">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="0d252-117">**ulFlags**</span></span>
  
> <span data-ttu-id="0d252-118">Битовая почта флагов, используемая для описания формата строки свойств, включенных в сообщение.</span><span class="sxs-lookup"><span data-stu-id="0d252-118">Bitmask of flags used to describe the format of the string properties included with the message.</span></span> <span data-ttu-id="0d252-119">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="0d252-119">The following flag can be set:</span></span>
    
<span data-ttu-id="0d252-120">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0d252-120">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="0d252-121">Переданные строки имеют формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="0d252-121">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="0d252-122">Если флаг MAPI_UNICODE не установлен, строки будут в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="0d252-122">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="0d252-123">**lpszMessageClass**</span><span class="sxs-lookup"><span data-stu-id="0d252-123">**lpszMessageClass**</span></span>
  
> <span data-ttu-id="0d252-124">Указатель на класс нового сообщения.</span><span class="sxs-lookup"><span data-stu-id="0d252-124">Pointer to the message class of the newly arrived message.</span></span> 
    
 <span data-ttu-id="0d252-125">**ulMessageFlags**</span><span class="sxs-lookup"><span data-stu-id="0d252-125">**ulMessageFlags**</span></span>
  
> <span data-ttu-id="0d252-126">Битоваяmas флагов, описывающая текущее состояние нового сообщения.</span><span class="sxs-lookup"><span data-stu-id="0d252-126">Bitmask of flags that describes the current state of the newly arrived message.</span></span> <span data-ttu-id="0d252-127">Член **ulMessageFlags** — это копия свойства PR_MESSAGE_FLAGS **сообщения** ([PidTagMessageFlags).](pidtagmessageflags-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="0d252-127">The **ulMessageFlags** member is a copy of the message's **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0d252-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="0d252-128">Remarks</span></span>

<span data-ttu-id="0d252-129">Структура **NEWMAIL_NOTIFICATION** является одним из членов объединения структур, включенных в  состав данных структуры [NOTIFICATION.](notification.md)</span><span class="sxs-lookup"><span data-stu-id="0d252-129">The **NEWMAIL_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="0d252-130">Если **информационный** член структуры **УВЕДОМЛЕНий** содержит NEWMAIL_NOTIFICATION, то для члена **ulEventType** структуры **NOTIFICATION** задается _fnevNewMail._ </span><span class="sxs-lookup"><span data-stu-id="0d252-130">When the **info** member of a **NOTIFICATION** structure contains a **NEWMAIL_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to  _fnevNewMail._</span></span>
  
<span data-ttu-id="0d252-131">MAPI использует **NEWMAIL_NOTIFICATION** только в качестве члена структуры **NOTIFICATION,** в которой хранится информация о событии уведомления для висящего уведомления.</span><span class="sxs-lookup"><span data-stu-id="0d252-131">MAPI uses the **NEWMAIL_NOTIFICATION** structure only as a member of the **NOTIFICATION** structure, which holds information about a notification event for the advise sink.</span></span> 
  
<span data-ttu-id="0d252-132">Дополнительные сведения об уведомлении см. в темах, описанных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="0d252-132">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="0d252-133">**Статья**</span><span class="sxs-lookup"><span data-stu-id="0d252-133">**Topic**</span></span>|<span data-ttu-id="0d252-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0d252-134">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0d252-135">Уведомление о событии в MAPI</span><span class="sxs-lookup"><span data-stu-id="0d252-135">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="0d252-136">Общий обзор событий уведомлений и уведомлений.</span><span class="sxs-lookup"><span data-stu-id="0d252-136">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="0d252-137">Обработка уведомлений</span><span class="sxs-lookup"><span data-stu-id="0d252-137">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="0d252-138">Обсуждение того, как клиенты должны обрабатывать уведомления.</span><span class="sxs-lookup"><span data-stu-id="0d252-138">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="0d252-139">Поддержка уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="0d252-139">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="0d252-140">Обсуждение того, как поставщики служб могут использовать метод [IMAPISupport](imapisupportiunknown.md) для создания уведомлений.</span><span class="sxs-lookup"><span data-stu-id="0d252-140">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0d252-141">См. также</span><span class="sxs-lookup"><span data-stu-id="0d252-141">See also</span></span>



[<span data-ttu-id="0d252-142">�����������</span><span class="sxs-lookup"><span data-stu-id="0d252-142">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="0d252-143">Каноническое свойство PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="0d252-143">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)


[<span data-ttu-id="0d252-144">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="0d252-144">MAPI Structures</span></span>](mapi-structures.md)

