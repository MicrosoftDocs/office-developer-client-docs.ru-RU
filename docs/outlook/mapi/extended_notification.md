---
title: EXTENDED_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.EXTENDED_NOTIFICATION
api_type:
- COM
ms.assetid: f01fce7b-a038-4002-8bad-0e6a51ae9d05
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a8b49d0b80102f6295f3f717fb123a6581854d5a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415721"
---
# <a name="extended_notification"></a><span data-ttu-id="5a005-103">EXTENDED_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="5a005-103">EXTENDED_NOTIFICATION</span></span>

  
  
<span data-ttu-id="5a005-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5a005-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5a005-105">Описывает сведения, которые относятся к событию, определенному поставщику услуг.</span><span class="sxs-lookup"><span data-stu-id="5a005-105">Describes information that relates to an event that is service provider-specific.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5a005-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="5a005-106">Header file:</span></span>  <br/> |<span data-ttu-id="5a005-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5a005-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _EXTENDED_NOTIFICATION
{
  ULONG ulEvent;
  ULONG cb;
  LPBYTE pbEventParameters;
} EXTENDED_NOTIFICATION;

```

## <a name="members"></a><span data-ttu-id="5a005-108">"Участники"</span><span class="sxs-lookup"><span data-stu-id="5a005-108">Members</span></span>

 <span data-ttu-id="5a005-109">**ulEvent**</span><span class="sxs-lookup"><span data-stu-id="5a005-109">**ulEvent**</span></span>
  
> <span data-ttu-id="5a005-110">Расширенный код события, определенный поставщиком.</span><span class="sxs-lookup"><span data-stu-id="5a005-110">Extended event code that is defined by the provider.</span></span>
    
 <span data-ttu-id="5a005-111">**cb**</span><span class="sxs-lookup"><span data-stu-id="5a005-111">**cb**</span></span>
  
> <span data-ttu-id="5a005-112">Количество bytes в параметрах, определенных событиями, на которые указывают **pbEventParameters.**</span><span class="sxs-lookup"><span data-stu-id="5a005-112">Count of bytes in the event-specific parameters pointed to by **pbEventParameters**.</span></span> 
    
 <span data-ttu-id="5a005-113">**pbEventParameters**</span><span class="sxs-lookup"><span data-stu-id="5a005-113">**pbEventParameters**</span></span>
  
> <span data-ttu-id="5a005-114">Указатель на параметры, определенные событиям.</span><span class="sxs-lookup"><span data-stu-id="5a005-114">Pointer to event-specific parameters.</span></span> <span data-ttu-id="5a005-115">Тип используемых параметров зависит от значения члена **ulEvent;** эти параметры документируются поставщиком, выдав событие.</span><span class="sxs-lookup"><span data-stu-id="5a005-115">The type of parameters that are used depends on the value of the **ulEvent** member; these parameters are documented by the provider that issued the event.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="5a005-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="5a005-116">Remarks</span></span>

<span data-ttu-id="5a005-117">Структура **EXTENDED_NOTIFICATION** является одним из членов союза структур, включенных в  состав информационного члена [структуры NOTIFICATION.](notification.md)</span><span class="sxs-lookup"><span data-stu-id="5a005-117">The **EXTENDED_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="5a005-118">Если член **структуры**  **УВЕДОМЛЕНий** содержит структуру EXTENDED_NOTIFICATION, то член **ulEventType** структуры **УВЕДОМЛЕНий** задает _fnevExtended_.</span><span class="sxs-lookup"><span data-stu-id="5a005-118">When the **info** member of a **NOTIFICATION** structure contains an **EXTENDED_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to  _fnevExtended_.</span></span>
  
<span data-ttu-id="5a005-119">Расширенное событие определяется поставщиком услуг для представления типа изменений, которые не могут быть охвачены любыми другими предопределяемых событий.</span><span class="sxs-lookup"><span data-stu-id="5a005-119">The extended event is defined by a service provider to represent a type of change that cannot be covered by any of the other predefined events.</span></span> <span data-ttu-id="5a005-120">Только клиенты, которые знают перед регистрацией, что поставщик услуг поддерживает расширенное событие, могут зарегистрироваться для этого события.</span><span class="sxs-lookup"><span data-stu-id="5a005-120">Only clients that know before they register that a service provider supports an extended event can register for that event.</span></span> <span data-ttu-id="5a005-121">Клиенты не могут определить без дополнительных знаний, поддерживает ли поставщик услуг расширенное событие.</span><span class="sxs-lookup"><span data-stu-id="5a005-121">It is not possible for clients to determine without advanced knowledge if a service provider supports an extended event.</span></span> <span data-ttu-id="5a005-122">Если поставщик служб поддерживает расширенное событие, он показывает, как обращаться с таким событием при его получении.</span><span class="sxs-lookup"><span data-stu-id="5a005-122">If a service provider supports an extended event, it shows how to handle such an event when it is received.</span></span>
  
<span data-ttu-id="5a005-123">Расширенное уведомление отправляется сеансом при отключении клиента.</span><span class="sxs-lookup"><span data-stu-id="5a005-123">An extended notification is sent by the session when a client logs off.</span></span> <span data-ttu-id="5a005-124">Зарегистрируйтесь для этого уведомления, позвонив [в IMAPISession:::Advise](imapisession-advise.md) с параметром  _lpEntryID,_ заданным nULL, и  _параметром cbEntryID,_ заданным до нуля.</span><span class="sxs-lookup"><span data-stu-id="5a005-124">Register for this notification by calling [IMAPISession::Advise](imapisession-advise.md) with the  _lpEntryID_ parameter set to NULL and the  _cbEntryID_ parameter set to zero.</span></span> 
  
<span data-ttu-id="5a005-125">Дополнительные сведения об уведомлении см. в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="5a005-125">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="5a005-126">**Статья**</span><span class="sxs-lookup"><span data-stu-id="5a005-126">**Topic**</span></span>|<span data-ttu-id="5a005-127">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5a005-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5a005-128">Уведомление о событиях в MAPI</span><span class="sxs-lookup"><span data-stu-id="5a005-128">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="5a005-129">Общий обзор событий уведомлений и уведомлений.</span><span class="sxs-lookup"><span data-stu-id="5a005-129">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="5a005-130">Обработка уведомлений</span><span class="sxs-lookup"><span data-stu-id="5a005-130">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="5a005-131">Обсуждение того, как клиенты должны обрабатывать уведомления.</span><span class="sxs-lookup"><span data-stu-id="5a005-131">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="5a005-132">Поддержка уведомления о событиях</span><span class="sxs-lookup"><span data-stu-id="5a005-132">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="5a005-133">Обсуждение того, как поставщики услуг могут использовать методы [IMAPISupport](imapisupportiunknown.md) для создания уведомлений.</span><span class="sxs-lookup"><span data-stu-id="5a005-133">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) methods to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5a005-134">См. также</span><span class="sxs-lookup"><span data-stu-id="5a005-134">See also</span></span>



[<span data-ttu-id="5a005-135">�����������</span><span class="sxs-lookup"><span data-stu-id="5a005-135">NOTIFICATION</span></span>](notification.md)


[<span data-ttu-id="5a005-136">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="5a005-136">MAPI Structures</span></span>](mapi-structures.md)

