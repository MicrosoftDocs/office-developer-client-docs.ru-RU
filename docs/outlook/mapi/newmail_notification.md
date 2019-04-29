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
# <a name="newmailnotification"></a><span data-ttu-id="40808-103">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="40808-103">NEWMAIL_NOTIFICATION</span></span>

  
  
<span data-ttu-id="40808-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="40808-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="40808-105">Сведения, связанные с поступлением нового сообщения.</span><span class="sxs-lookup"><span data-stu-id="40808-105">Describes information that relate to the arrival of a new message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="40808-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="40808-106">Header file:</span></span>  <br/> |<span data-ttu-id="40808-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="40808-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="40808-108">Members</span><span class="sxs-lookup"><span data-stu-id="40808-108">Members</span></span>

 <span data-ttu-id="40808-109">**Кбентрид**</span><span class="sxs-lookup"><span data-stu-id="40808-109">**cbEntryID**</span></span>
  
> <span data-ttu-id="40808-110">Количество байтов в идентификаторе записи, на который указывает элемент **лпентрид** .</span><span class="sxs-lookup"><span data-stu-id="40808-110">Count of bytes in the entry identifier pointed to by the **lpEntryID** member.</span></span> 
    
 <span data-ttu-id="40808-111">**Лпентрид**</span><span class="sxs-lookup"><span data-stu-id="40808-111">**lpEntryID**</span></span>
  
> <span data-ttu-id="40808-112">Указатель на идентификатор вновь полученного сообщения.</span><span class="sxs-lookup"><span data-stu-id="40808-112">Pointer to the entry identifier of the newly arrived message.</span></span>
    
 <span data-ttu-id="40808-113">**Кбпарентид**</span><span class="sxs-lookup"><span data-stu-id="40808-113">**cbParentID**</span></span>
  
> <span data-ttu-id="40808-114">Количество байтов в идентификаторе записи, на который указывает элемент **лппарентид** .</span><span class="sxs-lookup"><span data-stu-id="40808-114">Count of bytes in the entry identifier pointed to by the **lpParentID** member.</span></span> 
    
 <span data-ttu-id="40808-115">**Лппарентид**</span><span class="sxs-lookup"><span data-stu-id="40808-115">**lpParentID**</span></span>
  
> <span data-ttu-id="40808-116">Указатель на идентификатор записи папки получения для вновь полученного сообщения.</span><span class="sxs-lookup"><span data-stu-id="40808-116">Pointer to the entry identifier of the receive folder for the newly arrived message.</span></span>
    
 <span data-ttu-id="40808-117">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="40808-117">**ulFlags**</span></span>
  
> <span data-ttu-id="40808-118">Битовая маска флагов, используемых для описания формата строк свойств, включенных в сообщение.</span><span class="sxs-lookup"><span data-stu-id="40808-118">Bitmask of flags used to describe the format of the string properties included with the message.</span></span> <span data-ttu-id="40808-119">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="40808-119">The following flag can be set:</span></span>
    
<span data-ttu-id="40808-120">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="40808-120">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="40808-121">Переданные строки имеют формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="40808-121">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="40808-122">Если флаг МАПИ_УНИКОДЕ не установлен, строки представлены в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="40808-122">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="40808-123">**Лпсзмессажекласс**</span><span class="sxs-lookup"><span data-stu-id="40808-123">**lpszMessageClass**</span></span>
  
> <span data-ttu-id="40808-124">Указатель на класс сообщения вновь полученного сообщения.</span><span class="sxs-lookup"><span data-stu-id="40808-124">Pointer to the message class of the newly arrived message.</span></span> 
    
 <span data-ttu-id="40808-125">**Улмессажефлагс**</span><span class="sxs-lookup"><span data-stu-id="40808-125">**ulMessageFlags**</span></span>
  
> <span data-ttu-id="40808-126">Битовая маска флагов, описывающих текущее состояние вновь полученного сообщения.</span><span class="sxs-lookup"><span data-stu-id="40808-126">Bitmask of flags that describes the current state of the newly arrived message.</span></span> <span data-ttu-id="40808-127">Элемент **улмессажефлагс** является копией свойства **пр_мессаже_флагс** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) сообщения.</span><span class="sxs-lookup"><span data-stu-id="40808-127">The **ulMessageFlags** member is a copy of the message's **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="40808-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="40808-128">Remarks</span></span>

<span data-ttu-id="40808-129">Структура **невмаил_нотификатион** — это один из членов объединения структур, включенных в элемент **info** структуры [уведомления](notification.md) .</span><span class="sxs-lookup"><span data-stu-id="40808-129">The **NEWMAIL_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="40808-130">Когда элемент **info** структуры **уведомлений** содержит структуру **Невмаил_нотификатион** , элемент **улевенттипе** структуры **уведомлений** имеет значение _фневневмаил._</span><span class="sxs-lookup"><span data-stu-id="40808-130">When the **info** member of a **NOTIFICATION** structure contains a **NEWMAIL_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to  _fnevNewMail._</span></span>
  
<span data-ttu-id="40808-131">MAPI использует структуру **невмаил_нотификатион** только в качестве члена структуры **уведомлений** , в которой хранятся сведения о событии уведомления для приемника уведомлений.</span><span class="sxs-lookup"><span data-stu-id="40808-131">MAPI uses the **NEWMAIL_NOTIFICATION** structure only as a member of the **NOTIFICATION** structure, which holds information about a notification event for the advise sink.</span></span> 
  
<span data-ttu-id="40808-132">Дополнительные сведения об уведомлении можно найти в разделах, приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="40808-132">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="40808-133">**Статья**</span><span class="sxs-lookup"><span data-stu-id="40808-133">**Topic**</span></span>|<span data-ttu-id="40808-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="40808-134">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="40808-135">Уведомление о соБытии в MAPI</span><span class="sxs-lookup"><span data-stu-id="40808-135">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="40808-136">Общие сведения о событиях уведомлений и уведомлений.</span><span class="sxs-lookup"><span data-stu-id="40808-136">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="40808-137">Обработка уведомлений</span><span class="sxs-lookup"><span data-stu-id="40808-137">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="40808-138">Обсуждение того, как клиенты должны обрабатывать уведомления.</span><span class="sxs-lookup"><span data-stu-id="40808-138">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="40808-139">Поддержка уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="40808-139">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="40808-140">Обсуждение того, как поставщики услуг могут использовать метод [имаписуппорт](imapisupportiunknown.md) для создания уведомлений.</span><span class="sxs-lookup"><span data-stu-id="40808-140">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="40808-141">См. также</span><span class="sxs-lookup"><span data-stu-id="40808-141">See also</span></span>



[<span data-ttu-id="40808-142">�����������</span><span class="sxs-lookup"><span data-stu-id="40808-142">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="40808-143">Каноническое свойство PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="40808-143">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)


[<span data-ttu-id="40808-144">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="40808-144">MAPI Structures</span></span>](mapi-structures.md)

