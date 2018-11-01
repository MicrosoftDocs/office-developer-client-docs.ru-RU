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
ms.openlocfilehash: de9b5e377840b1fbfa3b6dd73fd952c0c72efeb7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580644"
---
# <a name="extendednotification"></a><span data-ttu-id="73759-103">EXTENDED_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="73759-103">EXTENDED_NOTIFICATION</span></span>

  
  
<span data-ttu-id="73759-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="73759-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="73759-105">Описывает сведения, относящиеся к событию, зависящие от поставщика службы.</span><span class="sxs-lookup"><span data-stu-id="73759-105">Describes information that relates to an event that is service provider-specific.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="73759-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="73759-106">Header file:</span></span>  <br/> |<span data-ttu-id="73759-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="73759-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _EXTENDED_NOTIFICATION
{
  ULONG ulEvent;
  ULONG cb;
  LPBYTE pbEventParameters;
} EXTENDED_NOTIFICATION;

```

## <a name="members"></a><span data-ttu-id="73759-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="73759-108">Members</span></span>

 <span data-ttu-id="73759-109">**ulEvent**</span><span class="sxs-lookup"><span data-stu-id="73759-109">**ulEvent**</span></span>
  
> <span data-ttu-id="73759-110">Код расширенного событий, определяемый поставщиком.</span><span class="sxs-lookup"><span data-stu-id="73759-110">Extended event code that is defined by the provider.</span></span>
    
 <span data-ttu-id="73759-111">**cb**</span><span class="sxs-lookup"><span data-stu-id="73759-111">**cb**</span></span>
  
> <span data-ttu-id="73759-112">Число байт в параметрах конкретного события, на который указывает **pbEventParameters**.</span><span class="sxs-lookup"><span data-stu-id="73759-112">Count of bytes in the event-specific parameters pointed to by **pbEventParameters**.</span></span> 
    
 <span data-ttu-id="73759-113">**pbEventParameters**</span><span class="sxs-lookup"><span data-stu-id="73759-113">**pbEventParameters**</span></span>
  
> <span data-ttu-id="73759-114">Указатель на параметры, относящиеся к события.</span><span class="sxs-lookup"><span data-stu-id="73759-114">Pointer to event-specific parameters.</span></span> <span data-ttu-id="73759-115">Тип параметров, которые используются зависит от значение элемента **ulEvent** ; Эти параметры описаны поставщиком, выпустивший события.</span><span class="sxs-lookup"><span data-stu-id="73759-115">The type of parameters that are used depends on the value of the **ulEvent** member; these parameters are documented by the provider that issued the event.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="73759-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="73759-116">Remarks</span></span>

<span data-ttu-id="73759-117">Структура **EXTENDED_NOTIFICATION** — это один из участников объединение структуры, включенные в элемент **info** структуры [УВЕДОМЛЕНИЙ](notification.md) .</span><span class="sxs-lookup"><span data-stu-id="73759-117">The **EXTENDED_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="73759-118">Когда участник **info** структуры **уведомление** содержит структуру **EXTENDED_NOTIFICATION** , член **ulEventType** структуры **УВЕДОМЛЕНИЙ** задано значение _fnevExtended_.</span><span class="sxs-lookup"><span data-stu-id="73759-118">When the **info** member of a **NOTIFICATION** structure contains an **EXTENDED_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to  _fnevExtended_.</span></span>
  
<span data-ttu-id="73759-119">Расширенные события определяется поставщиком услуг для представления тип изменения, не могут быть защищены торговыми любой из предварительно определенных событий.</span><span class="sxs-lookup"><span data-stu-id="73759-119">The extended event is defined by a service provider to represent a type of change that cannot be covered by any of the other predefined events.</span></span> <span data-ttu-id="73759-120">Для этого события можно регистрировать только клиентов, которые знать, прежде чем они зарегистрировать, что поставщик услуг поддерживает расширенные события.</span><span class="sxs-lookup"><span data-stu-id="73759-120">Only clients that know before they register that a service provider supports an extended event can register for that event.</span></span> <span data-ttu-id="73759-121">Не поддерживается для клиентов определить без высокий уровень знания, если поставщик услуг поддерживает расширенные события.</span><span class="sxs-lookup"><span data-stu-id="73759-121">It is not possible for clients to determine without advanced knowledge if a service provider supports an extended event.</span></span> <span data-ttu-id="73759-122">Если поставщик услуг поддерживает расширенные события, его показано, как обрабатывать события при получении.</span><span class="sxs-lookup"><span data-stu-id="73759-122">If a service provider supports an extended event, it shows how to handle such an event when it is received.</span></span>
  
<span data-ttu-id="73759-123">Уведомление о расширенных отправляется в сеансе, если это клиент выходит из системы.</span><span class="sxs-lookup"><span data-stu-id="73759-123">An extended notification is sent by the session when a client logs off.</span></span> <span data-ttu-id="73759-124">Регистрация для этого уведомления путем вызова [IMAPISession::Advise](imapisession-advise.md) с параметром _lpEntryID_ значение NULL, а параметр _cbEntryID_ , равным нулю.</span><span class="sxs-lookup"><span data-stu-id="73759-124">Register for this notification by calling [IMAPISession::Advise](imapisession-advise.md) with the  _lpEntryID_ parameter set to NULL and the  _cbEntryID_ parameter set to zero.</span></span> 
  
<span data-ttu-id="73759-125">Дополнительные сведения о уведомлений видеть темы, описанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="73759-125">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="73759-126">**Статья**</span><span class="sxs-lookup"><span data-stu-id="73759-126">**Topic**</span></span>|<span data-ttu-id="73759-127">**Описание**</span><span class="sxs-lookup"><span data-stu-id="73759-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="73759-128">Уведомление о событии в MAPI</span><span class="sxs-lookup"><span data-stu-id="73759-128">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="73759-129">Общий обзор уведомлений и события уведомления.</span><span class="sxs-lookup"><span data-stu-id="73759-129">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="73759-130">Обработка уведомлений</span><span class="sxs-lookup"><span data-stu-id="73759-130">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="73759-131">Обсуждение как клиенты должны обрабатывать уведомления.</span><span class="sxs-lookup"><span data-stu-id="73759-131">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="73759-132">Поддержка уведомления о событии</span><span class="sxs-lookup"><span data-stu-id="73759-132">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="73759-133">Обсуждение того, как поставщиков услуг можно использовать методы [IMAPISupport](imapisupportiunknown.md) для создания уведомлений.</span><span class="sxs-lookup"><span data-stu-id="73759-133">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) methods to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="73759-134">См. также</span><span class="sxs-lookup"><span data-stu-id="73759-134">See also</span></span>



[<span data-ttu-id="73759-135">�����������</span><span class="sxs-lookup"><span data-stu-id="73759-135">NOTIFICATION</span></span>](notification.md)


[<span data-ttu-id="73759-136">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="73759-136">MAPI Structures</span></span>](mapi-structures.md)

