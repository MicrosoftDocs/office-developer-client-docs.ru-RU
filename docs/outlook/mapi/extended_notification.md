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
# <a name="extended_notification"></a><span data-ttu-id="e8d1c-103">EXTENDED_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="e8d1c-103">EXTENDED_NOTIFICATION</span></span>

  
  
<span data-ttu-id="e8d1c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e8d1c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e8d1c-105">Описывает сведения, относящиеся к событию, зависящему от поставщика службы.</span><span class="sxs-lookup"><span data-stu-id="e8d1c-105">Describes information that relates to an event that is service provider-specific.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e8d1c-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="e8d1c-106">Header file:</span></span>  <br/> |<span data-ttu-id="e8d1c-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="e8d1c-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _EXTENDED_NOTIFICATION
{
  ULONG ulEvent;
  ULONG cb;
  LPBYTE pbEventParameters;
} EXTENDED_NOTIFICATION;

```

## <a name="members"></a><span data-ttu-id="e8d1c-108">"Участники"</span><span class="sxs-lookup"><span data-stu-id="e8d1c-108">Members</span></span>

 <span data-ttu-id="e8d1c-109">**улевент**</span><span class="sxs-lookup"><span data-stu-id="e8d1c-109">**ulEvent**</span></span>
  
> <span data-ttu-id="e8d1c-110">Код расширенного события, определяемый поставщиком.</span><span class="sxs-lookup"><span data-stu-id="e8d1c-110">Extended event code that is defined by the provider.</span></span>
    
 <span data-ttu-id="e8d1c-111">**cb**</span><span class="sxs-lookup"><span data-stu-id="e8d1c-111">**cb**</span></span>
  
> <span data-ttu-id="e8d1c-112">Количество байтов в параметрах, относящихся к определенному событию, на который указывает **пбевентпараметерс**.</span><span class="sxs-lookup"><span data-stu-id="e8d1c-112">Count of bytes in the event-specific parameters pointed to by **pbEventParameters**.</span></span> 
    
 <span data-ttu-id="e8d1c-113">**пбевентпараметерс**</span><span class="sxs-lookup"><span data-stu-id="e8d1c-113">**pbEventParameters**</span></span>
  
> <span data-ttu-id="e8d1c-114">Указатель на параметры, зависящие от события.</span><span class="sxs-lookup"><span data-stu-id="e8d1c-114">Pointer to event-specific parameters.</span></span> <span data-ttu-id="e8d1c-115">Тип используемых параметров зависит от значения элемента **улевент** ; Эти параметры задокументированы поставщиком, который выдал событие.</span><span class="sxs-lookup"><span data-stu-id="e8d1c-115">The type of parameters that are used depends on the value of the **ulEvent** member; these parameters are documented by the provider that issued the event.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e8d1c-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="e8d1c-116">Remarks</span></span>

<span data-ttu-id="e8d1c-117">Структура **EXTENDED_NOTIFICATION** — это один из членов объединения структур, включенных в элемент **info** структуры [уведомления](notification.md) .</span><span class="sxs-lookup"><span data-stu-id="e8d1c-117">The **EXTENDED_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="e8d1c-118">Когда элемент **info** элемента структуры **уведомлений** содержит структуру **EXTENDED_NOTIFICATION** , элемент **улевенттипе** структуры **уведомлений** имеет значение _фневекстендед_.</span><span class="sxs-lookup"><span data-stu-id="e8d1c-118">When the **info** member of a **NOTIFICATION** structure contains an **EXTENDED_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to  _fnevExtended_.</span></span>
  
<span data-ttu-id="e8d1c-119">Расширенное событие определяется поставщиком услуг для представления типа изменений, которые не могут быть охвачены какими-либо другими предопределенными событиями.</span><span class="sxs-lookup"><span data-stu-id="e8d1c-119">The extended event is defined by a service provider to represent a type of change that cannot be covered by any of the other predefined events.</span></span> <span data-ttu-id="e8d1c-120">Только клиенты, знакомые перед регистрацией того, что поставщик услуг поддерживает расширенное событие, может зарегистрировать это событие.</span><span class="sxs-lookup"><span data-stu-id="e8d1c-120">Only clients that know before they register that a service provider supports an extended event can register for that event.</span></span> <span data-ttu-id="e8d1c-121">Клиенты не могут определить, какие знания не были расширены, если поставщик услуг поддерживает расширенное событие.</span><span class="sxs-lookup"><span data-stu-id="e8d1c-121">It is not possible for clients to determine without advanced knowledge if a service provider supports an extended event.</span></span> <span data-ttu-id="e8d1c-122">Если поставщик услуг поддерживает расширенное событие, он показывает, как обрабатывать такое событие при его получении.</span><span class="sxs-lookup"><span data-stu-id="e8d1c-122">If a service provider supports an extended event, it shows how to handle such an event when it is received.</span></span>
  
<span data-ttu-id="e8d1c-123">Сеанс расширенного уведомления отправляется, когда клиент выходит из системы.</span><span class="sxs-lookup"><span data-stu-id="e8d1c-123">An extended notification is sent by the session when a client logs off.</span></span> <span data-ttu-id="e8d1c-124">Зарегистрируйтесь для получения этого уведомления, вызвав [IMAPISession:: Advise](imapisession-advise.md) с параметром _лпентрид_ , для которого задано значение null, а для параметра _кбентрид_ задано значение 0.</span><span class="sxs-lookup"><span data-stu-id="e8d1c-124">Register for this notification by calling [IMAPISession::Advise](imapisession-advise.md) with the  _lpEntryID_ parameter set to NULL and the  _cbEntryID_ parameter set to zero.</span></span> 
  
<span data-ttu-id="e8d1c-125">Дополнительные сведения об уведомлении можно найти в разделах, приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="e8d1c-125">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="e8d1c-126">**Статья**</span><span class="sxs-lookup"><span data-stu-id="e8d1c-126">**Topic**</span></span>|<span data-ttu-id="e8d1c-127">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e8d1c-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e8d1c-128">Уведомление о событии в MAPI</span><span class="sxs-lookup"><span data-stu-id="e8d1c-128">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="e8d1c-129">Общие сведения о событиях уведомлений и уведомлений.</span><span class="sxs-lookup"><span data-stu-id="e8d1c-129">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="e8d1c-130">Обработка уведомлений</span><span class="sxs-lookup"><span data-stu-id="e8d1c-130">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="e8d1c-131">Обсуждение того, как клиенты должны обрабатывать уведомления.</span><span class="sxs-lookup"><span data-stu-id="e8d1c-131">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="e8d1c-132">Поддержка уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="e8d1c-132">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="e8d1c-133">Обсуждение того, как поставщики услуг могут использовать методы [имаписуппорт](imapisupportiunknown.md) для создания уведомлений.</span><span class="sxs-lookup"><span data-stu-id="e8d1c-133">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) methods to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e8d1c-134">См. также</span><span class="sxs-lookup"><span data-stu-id="e8d1c-134">See also</span></span>



[<span data-ttu-id="e8d1c-135">�����������</span><span class="sxs-lookup"><span data-stu-id="e8d1c-135">NOTIFICATION</span></span>](notification.md)


[<span data-ttu-id="e8d1c-136">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="e8d1c-136">MAPI Structures</span></span>](mapi-structures.md)

