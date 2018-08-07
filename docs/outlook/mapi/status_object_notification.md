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
ms.openlocfilehash: 71e0a08436c925f0d68d63111722cc01bd73cc5f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812402"
---
# <a name="statusobjectnotification"></a><span data-ttu-id="e4d75-103">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="e4d75-103">STATUS_OBJECT_NOTIFICATION</span></span>

  
  
<span data-ttu-id="e4d75-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e4d75-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e4d75-105">Описывает объект состояния, которые были затронуты изменения.</span><span class="sxs-lookup"><span data-stu-id="e4d75-105">Describes a status object that has been affected by a change.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e4d75-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="e4d75-106">Header file:</span></span>  <br/> |<span data-ttu-id="e4d75-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e4d75-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  ULONG cValues;
  LPSPropValue lpPropVals;
} STATUS_OBJECT_NOTIFICATION;

```

## <a name="members"></a><span data-ttu-id="e4d75-108">Members</span><span class="sxs-lookup"><span data-stu-id="e4d75-108">Members</span></span>

 <span data-ttu-id="e4d75-109">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="e4d75-109">**cbEntryID**</span></span>
  
> <span data-ttu-id="e4d75-110">Число байт в идентификаторе запись, на который указывает член **lpEntryID** .</span><span class="sxs-lookup"><span data-stu-id="e4d75-110">Count of bytes in the entry identifier pointed to by the **lpEntryID** member.</span></span> 
    
 <span data-ttu-id="e4d75-111">**lpEntryID**</span><span class="sxs-lookup"><span data-stu-id="e4d75-111">**lpEntryID**</span></span>
  
> <span data-ttu-id="e4d75-112">Указатель на идентификатор записи измененное состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="e4d75-112">Pointer to the entry identifier of the changed status object.</span></span>
    
 <span data-ttu-id="e4d75-113">**cValues**</span><span class="sxs-lookup"><span data-stu-id="e4d75-113">**cValues**</span></span>
  
> <span data-ttu-id="e4d75-114">Число структур [SPropValue](spropvalue.md) в массиве, на который указывает член **lpPropVals** .</span><span class="sxs-lookup"><span data-stu-id="e4d75-114">Count of [SPropValue](spropvalue.md) structures in the array pointed to by the **lpPropVals** member.</span></span> 
    
 <span data-ttu-id="e4d75-115">**lpPropVals**</span><span class="sxs-lookup"><span data-stu-id="e4d75-115">**lpPropVals**</span></span>
  
> <span data-ttu-id="e4d75-116">Указатель на массив структур **SPropValue** , которые описывают свойства объекта измененное состояние.</span><span class="sxs-lookup"><span data-stu-id="e4d75-116">Pointer to an array of **SPropValue** structures that describe the properties of the changed status object.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e4d75-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="e4d75-117">Remarks</span></span>

<span data-ttu-id="e4d75-118">Структура **STATUS_OBJECT_NOTIFICATION** — это один из участников объединение структуры, включенные в элемент **info** структуры [УВЕДОМЛЕНИЙ](notification.md) .</span><span class="sxs-lookup"><span data-stu-id="e4d75-118">The **STATUS_OBJECT_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="e4d75-119">Структура **STATUS_OBJECT_NOTIFICATION** входит в состав объекта уведомление о состоянии для события из типа _fnevStatusObjectModified_.</span><span class="sxs-lookup"><span data-stu-id="e4d75-119">The **STATUS_OBJECT_NOTIFICATION** structure is included with a status object notification for an event of type  _fnevStatusObjectModified_.</span></span> <span data-ttu-id="e4d75-120">Уведомление о доставке объект является внутренних уведомлений MAPI; для него нельзя зарегистрировать клиентов и поставщиков услуг и поставщиков услуг не удается создать его.</span><span class="sxs-lookup"><span data-stu-id="e4d75-120">Status object notification is an internal MAPI notification; clients and service providers cannot register for it and service providers cannot generate it.</span></span>
  
<span data-ttu-id="e4d75-121">Дополнительные сведения о уведомлений видеть темы, описанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="e4d75-121">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="e4d75-122">**Статья**</span><span class="sxs-lookup"><span data-stu-id="e4d75-122">**Topic**</span></span>|<span data-ttu-id="e4d75-123">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e4d75-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e4d75-124">Уведомление о событиях в MAPI</span><span class="sxs-lookup"><span data-stu-id="e4d75-124">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="e4d75-125">Общий обзор уведомлений и события уведомления.</span><span class="sxs-lookup"><span data-stu-id="e4d75-125">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="e4d75-126">Обработка уведомлений</span><span class="sxs-lookup"><span data-stu-id="e4d75-126">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="e4d75-127">Обсуждение как клиенты должны обрабатывать уведомления.</span><span class="sxs-lookup"><span data-stu-id="e4d75-127">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="e4d75-128">Поддержка уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="e4d75-128">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="e4d75-129">Обсуждение того, как поставщиков услуг можно использовать метод **IMAPISupport** для создания уведомлений.</span><span class="sxs-lookup"><span data-stu-id="e4d75-129">Discussion of how service providers can use the **IMAPISupport** method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e4d75-130">См. также</span><span class="sxs-lookup"><span data-stu-id="e4d75-130">See also</span></span>



[<span data-ttu-id="e4d75-131">�����������</span><span class="sxs-lookup"><span data-stu-id="e4d75-131">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="e4d75-132">SPropValue</span><span class="sxs-lookup"><span data-stu-id="e4d75-132">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="e4d75-133">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="e4d75-133">MAPI Structures</span></span>](mapi-structures.md)

