---
title: ERROR_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ERROR_NOTIFICATION
api_type:
- COM
ms.assetid: 6c5bb383-f8e2-4d79-bcf2-aa86c130e8b1
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f8d4fb6b8cd7ad0ebf1e7660a0f3c0602274fa10
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425444"
---
# <a name="error_notification"></a><span data-ttu-id="c6da1-103">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="c6da1-103">ERROR_NOTIFICATION</span></span>

  
  
<span data-ttu-id="c6da1-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c6da1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c6da1-105">Описывает сведения, которые относятся к критической ошибке.</span><span class="sxs-lookup"><span data-stu-id="c6da1-105">Describes information that relate to a critical error.</span></span> <span data-ttu-id="c6da1-106">Это приводит к сгенерированию уведомления об ошибке.</span><span class="sxs-lookup"><span data-stu-id="c6da1-106">This causes an error notification to be generated.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c6da1-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="c6da1-107">Header file:</span></span>  <br/> |<span data-ttu-id="c6da1-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c6da1-108">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _ERROR_NOTIFICATION
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  SCODE scode;
  ULONG ulFlags;
  LPMAPIERROR lpMAPIError;
} ERROR_NOTIFICATION;
```

## <a name="members"></a><span data-ttu-id="c6da1-109">"Участники"</span><span class="sxs-lookup"><span data-stu-id="c6da1-109">Members</span></span>

 <span data-ttu-id="c6da1-110">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="c6da1-110">**cbEntryID**</span></span>
  
> <span data-ttu-id="c6da1-111">Количествобайтов в идентификаторе записи, на который указывает **lpEntryID.**</span><span class="sxs-lookup"><span data-stu-id="c6da1-111">Count of bytes in the entry identifier pointed to by **lpEntryID**.</span></span> 
    
 <span data-ttu-id="c6da1-112">**lpEntryID**</span><span class="sxs-lookup"><span data-stu-id="c6da1-112">**lpEntryID**</span></span>
  
> <span data-ttu-id="c6da1-113">Указатель на идентификатор записи объекта, который вызывает ошибку.</span><span class="sxs-lookup"><span data-stu-id="c6da1-113">Pointer to the entry identifier of the object that causes the error.</span></span>
    
 <span data-ttu-id="c6da1-114">**scode**</span><span class="sxs-lookup"><span data-stu-id="c6da1-114">**scode**</span></span>
  
> <span data-ttu-id="c6da1-115">Значение ошибки для критической ошибки.</span><span class="sxs-lookup"><span data-stu-id="c6da1-115">Error value for the critical error.</span></span> 
    
 <span data-ttu-id="c6da1-116">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="c6da1-116">**ulFlags**</span></span>
  
> <span data-ttu-id="c6da1-117">Битоваяmas флагов, используемая для обозначения формата текста, на который указывает элемент **lpszError** в структуре, на который указывает **lpMAPIError.**</span><span class="sxs-lookup"><span data-stu-id="c6da1-117">Bitmask of flags used to designate the format of the text pointed to by the **lpszError** member in the structure pointed to by **lpMAPIError**.</span></span> <span data-ttu-id="c6da1-118">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="c6da1-118">The following flag can be set:</span></span>
    
<span data-ttu-id="c6da1-119">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c6da1-119">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="c6da1-120">Переданные строки имеют формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="c6da1-120">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="c6da1-121">Если флаг MAPI_UNICODE не установлен, строки будут в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="c6da1-121">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="c6da1-122">**lpMAPIError**</span><span class="sxs-lookup"><span data-stu-id="c6da1-122">**lpMAPIError**</span></span>
  
> <span data-ttu-id="c6da1-123">Указатель на [структуру MAPIERROR,](mapierror.md) описывающий ошибку.</span><span class="sxs-lookup"><span data-stu-id="c6da1-123">Pointer to a [MAPIERROR](mapierror.md) structure describing the error.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c6da1-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="c6da1-124">Remarks</span></span>

<span data-ttu-id="c6da1-125">Структура **ERROR_NOTIFICATION** является одним из членов объединения структур, включенных  в состав данных структуры [NOTIFICATION.](notification.md)</span><span class="sxs-lookup"><span data-stu-id="c6da1-125">The **ERROR_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="c6da1-126">Если **информационный** член структуры **NOTIFICATION** содержит структуру ERROR_NOTIFICATION, то для члена **ulEventType** структуры **NOTIFICATION** устанавливается _fnevCriticalError._ </span><span class="sxs-lookup"><span data-stu-id="c6da1-126">When the **info** member of a **NOTIFICATION** structure contains an **ERROR_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to  _fnevCriticalError_.</span></span>
  
<span data-ttu-id="c6da1-127">Значением члена **cbEntryID** и **lpEntryID** может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="c6da1-127">The value of the **cbEntryID** member and the **lpEntryID** member can be NULL.</span></span> 
  
<span data-ttu-id="c6da1-128">Дополнительные сведения об уведомлении см. в темах, описанных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="c6da1-128">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="c6da1-129">**Статья**</span><span class="sxs-lookup"><span data-stu-id="c6da1-129">**Topic**</span></span>|<span data-ttu-id="c6da1-130">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c6da1-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c6da1-131">Уведомление о событии в MAPI</span><span class="sxs-lookup"><span data-stu-id="c6da1-131">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="c6da1-132">Общий обзор событий уведомлений и уведомлений.</span><span class="sxs-lookup"><span data-stu-id="c6da1-132">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="c6da1-133">Обработка уведомлений</span><span class="sxs-lookup"><span data-stu-id="c6da1-133">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="c6da1-134">Обсуждение того, как клиенты должны обрабатывать уведомления.</span><span class="sxs-lookup"><span data-stu-id="c6da1-134">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="c6da1-135">Поддержка уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="c6da1-135">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="c6da1-136">Обсуждение того, как поставщики служб могут использовать метод **IMAPISupport** для создания уведомлений.</span><span class="sxs-lookup"><span data-stu-id="c6da1-136">Discussion of how service providers can use the **IMAPISupport** method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c6da1-137">См. также</span><span class="sxs-lookup"><span data-stu-id="c6da1-137">See also</span></span>



[<span data-ttu-id="c6da1-138">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="c6da1-138">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="c6da1-139">�����������</span><span class="sxs-lookup"><span data-stu-id="c6da1-139">NOTIFICATION</span></span>](notification.md)


[<span data-ttu-id="c6da1-140">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="c6da1-140">MAPI Structures</span></span>](mapi-structures.md)

