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
ms.openlocfilehash: 779585f73a7032ae0259b30ebfc16868c733c7fc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569514"
---
# <a name="newmailnotification"></a><span data-ttu-id="8ac79-103">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="8ac79-103">NEWMAIL_NOTIFICATION</span></span>

  
  
<span data-ttu-id="8ac79-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8ac79-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8ac79-105">Описание сведений, которые относятся к поступления нового сообщения.</span><span class="sxs-lookup"><span data-stu-id="8ac79-105">Describes information that relate to the arrival of a new message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8ac79-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="8ac79-106">Header file:</span></span>  <br/> |<span data-ttu-id="8ac79-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8ac79-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="8ac79-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="8ac79-108">Members</span></span>

 <span data-ttu-id="8ac79-109">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="8ac79-109">**cbEntryID**</span></span>
  
> <span data-ttu-id="8ac79-110">Число байт в идентификаторе запись, на который указывает член **lpEntryID** .</span><span class="sxs-lookup"><span data-stu-id="8ac79-110">Count of bytes in the entry identifier pointed to by the **lpEntryID** member.</span></span> 
    
 <span data-ttu-id="8ac79-111">**lpEntryID**</span><span class="sxs-lookup"><span data-stu-id="8ac79-111">**lpEntryID**</span></span>
  
> <span data-ttu-id="8ac79-112">Указатель на идентификатор записи вновь поступивших сообщения.</span><span class="sxs-lookup"><span data-stu-id="8ac79-112">Pointer to the entry identifier of the newly arrived message.</span></span>
    
 <span data-ttu-id="8ac79-113">**cbParentID**</span><span class="sxs-lookup"><span data-stu-id="8ac79-113">**cbParentID**</span></span>
  
> <span data-ttu-id="8ac79-114">Число байт в идентификаторе запись, на который указывает член **lpParentID** .</span><span class="sxs-lookup"><span data-stu-id="8ac79-114">Count of bytes in the entry identifier pointed to by the **lpParentID** member.</span></span> 
    
 <span data-ttu-id="8ac79-115">**lpParentID**</span><span class="sxs-lookup"><span data-stu-id="8ac79-115">**lpParentID**</span></span>
  
> <span data-ttu-id="8ac79-116">Указатель на идентификатор записи папки получения для недавно полученных сообщений.</span><span class="sxs-lookup"><span data-stu-id="8ac79-116">Pointer to the entry identifier of the receive folder for the newly arrived message.</span></span>
    
 <span data-ttu-id="8ac79-117">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="8ac79-117">**ulFlags**</span></span>
  
> <span data-ttu-id="8ac79-118">Битовая маска флаги, используемые для описания формата строковые свойства, включенные в состав сообщения.</span><span class="sxs-lookup"><span data-stu-id="8ac79-118">Bitmask of flags used to describe the format of the string properties included with the message.</span></span> <span data-ttu-id="8ac79-119">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="8ac79-119">The following flag can be set:</span></span>
    
<span data-ttu-id="8ac79-120">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8ac79-120">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="8ac79-121">Строки переданное хранятся в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="8ac79-121">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="8ac79-122">Если флаг MAPI_UNICODE не установлен, они в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="8ac79-122">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="8ac79-123">**lpszMessageClass**</span><span class="sxs-lookup"><span data-stu-id="8ac79-123">**lpszMessageClass**</span></span>
  
> <span data-ttu-id="8ac79-124">Указатель на класс сообщения вновь поступивших сообщения.</span><span class="sxs-lookup"><span data-stu-id="8ac79-124">Pointer to the message class of the newly arrived message.</span></span> 
    
 <span data-ttu-id="8ac79-125">**ulMessageFlags**</span><span class="sxs-lookup"><span data-stu-id="8ac79-125">**ulMessageFlags**</span></span>
  
> <span data-ttu-id="8ac79-126">Битовая маска флаги, описывающее текущее состояние вновь поступивших сообщений.</span><span class="sxs-lookup"><span data-stu-id="8ac79-126">Bitmask of flags that describes the current state of the newly arrived message.</span></span> <span data-ttu-id="8ac79-127">Член **ulMessageFlags** является копию свойство message **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="8ac79-127">The **ulMessageFlags** member is a copy of the message's **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8ac79-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="8ac79-128">Remarks</span></span>

<span data-ttu-id="8ac79-129">Структура **NEWMAIL_NOTIFICATION** — это один из участников объединение структуры, включенные в элемент **info** структуры [УВЕДОМЛЕНИЙ](notification.md) .</span><span class="sxs-lookup"><span data-stu-id="8ac79-129">The **NEWMAIL_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="8ac79-130">Когда участник **info** структуры **уведомление** содержит структуру **NEWMAIL_NOTIFICATION** , член **ulEventType** структуры **УВЕДОМЛЕНИЙ** задано значение _fnevNewMail._</span><span class="sxs-lookup"><span data-stu-id="8ac79-130">When the **info** member of a **NOTIFICATION** structure contains a **NEWMAIL_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to  _fnevNewMail._</span></span>
  
<span data-ttu-id="8ac79-131">MAPI использует структуру **NEWMAIL_NOTIFICATION** только в качестве члена структуры **УВЕДОМЛЕНИЙ** , который содержит сведения о событии уведомления для приемник уведомлений.</span><span class="sxs-lookup"><span data-stu-id="8ac79-131">MAPI uses the **NEWMAIL_NOTIFICATION** structure only as a member of the **NOTIFICATION** structure, which holds information about a notification event for the advise sink.</span></span> 
  
<span data-ttu-id="8ac79-132">Дополнительные сведения о уведомлений видеть темы, описанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="8ac79-132">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="8ac79-133">**Статья**</span><span class="sxs-lookup"><span data-stu-id="8ac79-133">**Topic**</span></span>|<span data-ttu-id="8ac79-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8ac79-134">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8ac79-135">Уведомление о событии в MAPI</span><span class="sxs-lookup"><span data-stu-id="8ac79-135">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="8ac79-136">Общий обзор уведомлений и события уведомления.</span><span class="sxs-lookup"><span data-stu-id="8ac79-136">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="8ac79-137">Обработка уведомлений</span><span class="sxs-lookup"><span data-stu-id="8ac79-137">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="8ac79-138">Обсуждение как клиенты должны обрабатывать уведомления.</span><span class="sxs-lookup"><span data-stu-id="8ac79-138">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="8ac79-139">Поддержка уведомления о событии</span><span class="sxs-lookup"><span data-stu-id="8ac79-139">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="8ac79-140">Обсуждение того, как поставщиков услуг можно использовать метод [IMAPISupport](imapisupportiunknown.md) для создания уведомлений.</span><span class="sxs-lookup"><span data-stu-id="8ac79-140">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8ac79-141">См. также</span><span class="sxs-lookup"><span data-stu-id="8ac79-141">See also</span></span>



[<span data-ttu-id="8ac79-142">�����������</span><span class="sxs-lookup"><span data-stu-id="8ac79-142">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="8ac79-143">Каноническое свойство PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="8ac79-143">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)


[<span data-ttu-id="8ac79-144">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="8ac79-144">MAPI Structures</span></span>](mapi-structures.md)

