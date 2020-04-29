---
title: STATUS_OBJECT_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.STATUS_OBJECT_NOTIFICATION
api_type:
- COM
ms.assetid: 2872130d-a36b-46ea-bfd1-4700fe3dd41b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 84b44b4b054a2b2617502a6a463a6d4a89546804
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426270"
---
# <a name="status_object_notification"></a><span data-ttu-id="523b6-103">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="523b6-103">STATUS_OBJECT_NOTIFICATION</span></span>

  
  
<span data-ttu-id="523b6-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="523b6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="523b6-105">Описывает объект status, на который влияет изменение.</span><span class="sxs-lookup"><span data-stu-id="523b6-105">Describes a status object that has been affected by a change.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="523b6-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="523b6-106">Header file:</span></span>  <br/> |<span data-ttu-id="523b6-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="523b6-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  ULONG cValues;
  LPSPropValue lpPropVals;
} STATUS_OBJECT_NOTIFICATION;

```

## <a name="members"></a><span data-ttu-id="523b6-108">"Участники"</span><span class="sxs-lookup"><span data-stu-id="523b6-108">Members</span></span>

 <span data-ttu-id="523b6-109">**кбентрид**</span><span class="sxs-lookup"><span data-stu-id="523b6-109">**cbEntryID**</span></span>
  
> <span data-ttu-id="523b6-110">Количество байтов в идентификаторе записи, на который указывает элемент **лпентрид** .</span><span class="sxs-lookup"><span data-stu-id="523b6-110">Count of bytes in the entry identifier pointed to by the **lpEntryID** member.</span></span> 
    
 <span data-ttu-id="523b6-111">**лпентрид**</span><span class="sxs-lookup"><span data-stu-id="523b6-111">**lpEntryID**</span></span>
  
> <span data-ttu-id="523b6-112">Указатель на идентификатор записи измененного объекта Status.</span><span class="sxs-lookup"><span data-stu-id="523b6-112">Pointer to the entry identifier of the changed status object.</span></span>
    
 <span data-ttu-id="523b6-113">**квалуес**</span><span class="sxs-lookup"><span data-stu-id="523b6-113">**cValues**</span></span>
  
> <span data-ttu-id="523b6-114">Количество структур [спропвалуе](spropvalue.md) в массиве, на которое указывает элемент **лппропвалс** .</span><span class="sxs-lookup"><span data-stu-id="523b6-114">Count of [SPropValue](spropvalue.md) structures in the array pointed to by the **lpPropVals** member.</span></span> 
    
 <span data-ttu-id="523b6-115">**лппропвалс**</span><span class="sxs-lookup"><span data-stu-id="523b6-115">**lpPropVals**</span></span>
  
> <span data-ttu-id="523b6-116">Указатель на массив структур **спропвалуе** , описывающих свойства измененного объекта Status.</span><span class="sxs-lookup"><span data-stu-id="523b6-116">Pointer to an array of **SPropValue** structures that describe the properties of the changed status object.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="523b6-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="523b6-117">Remarks</span></span>

<span data-ttu-id="523b6-118">Структура **STATUS_OBJECT_NOTIFICATION** — это один из членов объединения структур, включенных в элемент **info** структуры [уведомления](notification.md) .</span><span class="sxs-lookup"><span data-stu-id="523b6-118">The **STATUS_OBJECT_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="523b6-119">Структура **STATUS_OBJECT_NOTIFICATION** включена в уведомление объекта Status для события типа _фневстатусобжектмодифиед_.</span><span class="sxs-lookup"><span data-stu-id="523b6-119">The **STATUS_OBJECT_NOTIFICATION** structure is included with a status object notification for an event of type  _fnevStatusObjectModified_.</span></span> <span data-ttu-id="523b6-120">Уведомление объекта Status является внутренним уведомлением MAPI; Клиенты и поставщики услуг не могут регистрироваться для ИТ, и поставщики услуг не могут создать ее.</span><span class="sxs-lookup"><span data-stu-id="523b6-120">Status object notification is an internal MAPI notification; clients and service providers cannot register for it and service providers cannot generate it.</span></span>
  
<span data-ttu-id="523b6-121">Дополнительные сведения об уведомлении можно найти в разделах, приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="523b6-121">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="523b6-122">**Статья**</span><span class="sxs-lookup"><span data-stu-id="523b6-122">**Topic**</span></span>|<span data-ttu-id="523b6-123">**Описание**</span><span class="sxs-lookup"><span data-stu-id="523b6-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="523b6-124">Уведомление о событии в MAPI</span><span class="sxs-lookup"><span data-stu-id="523b6-124">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="523b6-125">Общие сведения о событиях уведомлений и уведомлений.</span><span class="sxs-lookup"><span data-stu-id="523b6-125">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="523b6-126">Обработка уведомлений</span><span class="sxs-lookup"><span data-stu-id="523b6-126">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="523b6-127">Обсуждение того, как клиенты должны обрабатывать уведомления.</span><span class="sxs-lookup"><span data-stu-id="523b6-127">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="523b6-128">Поддержка уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="523b6-128">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="523b6-129">Обсуждение того, как поставщики услуг могут использовать метод **имаписуппорт** для создания уведомлений.</span><span class="sxs-lookup"><span data-stu-id="523b6-129">Discussion of how service providers can use the **IMAPISupport** method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="523b6-130">См. также</span><span class="sxs-lookup"><span data-stu-id="523b6-130">See also</span></span>



[<span data-ttu-id="523b6-131">�����������</span><span class="sxs-lookup"><span data-stu-id="523b6-131">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="523b6-132">SPropValue</span><span class="sxs-lookup"><span data-stu-id="523b6-132">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="523b6-133">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="523b6-133">MAPI Structures</span></span>](mapi-structures.md)

