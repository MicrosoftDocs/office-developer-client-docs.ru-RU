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
ms.openlocfilehash: 2405799fa59abf58583553f8e2d3718d68411a19
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574974"
---
# <a name="errornotification"></a><span data-ttu-id="74dac-103">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="74dac-103">ERROR_NOTIFICATION</span></span>

  
  
<span data-ttu-id="74dac-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="74dac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="74dac-105">Описание сведений, которые относятся к критическая ошибка.</span><span class="sxs-lookup"><span data-stu-id="74dac-105">Describes information that relate to a critical error.</span></span> <span data-ttu-id="74dac-106">В этом случае уведомление об ошибке был создан.</span><span class="sxs-lookup"><span data-stu-id="74dac-106">This causes an error notification to be generated.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="74dac-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="74dac-107">Header file:</span></span>  <br/> |<span data-ttu-id="74dac-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="74dac-108">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="74dac-109">Members</span><span class="sxs-lookup"><span data-stu-id="74dac-109">Members</span></span>

 <span data-ttu-id="74dac-110">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="74dac-110">**cbEntryID**</span></span>
  
> <span data-ttu-id="74dac-111">Число байт в идентификаторе запись, на который указывает **lpEntryID**.</span><span class="sxs-lookup"><span data-stu-id="74dac-111">Count of bytes in the entry identifier pointed to by **lpEntryID**.</span></span> 
    
 <span data-ttu-id="74dac-112">**lpEntryID**</span><span class="sxs-lookup"><span data-stu-id="74dac-112">**lpEntryID**</span></span>
  
> <span data-ttu-id="74dac-113">Указатель на идентификатор записи объекта, который вызывает ошибку.</span><span class="sxs-lookup"><span data-stu-id="74dac-113">Pointer to the entry identifier of the object that causes the error.</span></span>
    
 <span data-ttu-id="74dac-114">**SCODE**</span><span class="sxs-lookup"><span data-stu-id="74dac-114">**scode**</span></span>
  
> <span data-ttu-id="74dac-115">Значение ошибки для критическая ошибка.</span><span class="sxs-lookup"><span data-stu-id="74dac-115">Error value for the critical error.</span></span> 
    
 <span data-ttu-id="74dac-116">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="74dac-116">**ulFlags**</span></span>
  
> <span data-ttu-id="74dac-117">Битовая маска флагов используется для назначения формат текста, на который указывает член **lpszError** в структуре, на который указывает **lpMAPIError**.</span><span class="sxs-lookup"><span data-stu-id="74dac-117">Bitmask of flags used to designate the format of the text pointed to by the **lpszError** member in the structure pointed to by **lpMAPIError**.</span></span> <span data-ttu-id="74dac-118">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="74dac-118">The following flag can be set:</span></span>
    
<span data-ttu-id="74dac-119">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="74dac-119">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="74dac-120">Строки переданное хранятся в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="74dac-120">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="74dac-121">Если флаг MAPI_UNICODE не установлен, они в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="74dac-121">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="74dac-122">**lpMAPIError**</span><span class="sxs-lookup"><span data-stu-id="74dac-122">**lpMAPIError**</span></span>
  
> <span data-ttu-id="74dac-123">Указатель на структуру [MAPIERROR](mapierror.md) , описывающее ошибку.</span><span class="sxs-lookup"><span data-stu-id="74dac-123">Pointer to a [MAPIERROR](mapierror.md) structure describing the error.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="74dac-124">Замечания</span><span class="sxs-lookup"><span data-stu-id="74dac-124">Remarks</span></span>

<span data-ttu-id="74dac-125">Структура **ERROR_NOTIFICATION** — это один из участников объединение структуры, включенные в элемент **info** структуры [УВЕДОМЛЕНИЙ](notification.md) .</span><span class="sxs-lookup"><span data-stu-id="74dac-125">The **ERROR_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="74dac-126">Когда участник **info** структуры **уведомление** содержит структуру **ERROR_NOTIFICATION** , член **ulEventType** структуры **УВЕДОМЛЕНИЙ** задано значение _fnevCriticalError_.</span><span class="sxs-lookup"><span data-stu-id="74dac-126">When the **info** member of a **NOTIFICATION** structure contains an **ERROR_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to  _fnevCriticalError_.</span></span>
  
<span data-ttu-id="74dac-127">Значение **cbEntryID** , а **lpEntryID** может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="74dac-127">The value of the **cbEntryID** member and the **lpEntryID** member can be NULL.</span></span> 
  
<span data-ttu-id="74dac-128">Дополнительные сведения о уведомлений видеть темы, описанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="74dac-128">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="74dac-129">**Статья**</span><span class="sxs-lookup"><span data-stu-id="74dac-129">**Topic**</span></span>|<span data-ttu-id="74dac-130">**Описание**</span><span class="sxs-lookup"><span data-stu-id="74dac-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="74dac-131">Уведомление о событиях в MAPI</span><span class="sxs-lookup"><span data-stu-id="74dac-131">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="74dac-132">Общий обзор уведомлений и события уведомления.</span><span class="sxs-lookup"><span data-stu-id="74dac-132">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="74dac-133">Обработка уведомлений</span><span class="sxs-lookup"><span data-stu-id="74dac-133">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="74dac-134">Обсуждение как клиенты должны обрабатывать уведомления.</span><span class="sxs-lookup"><span data-stu-id="74dac-134">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="74dac-135">Поддержка уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="74dac-135">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="74dac-136">Обсуждение того, как поставщиков услуг можно использовать метод **IMAPISupport** для создания уведомлений.</span><span class="sxs-lookup"><span data-stu-id="74dac-136">Discussion of how service providers can use the **IMAPISupport** method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="74dac-137">См. также</span><span class="sxs-lookup"><span data-stu-id="74dac-137">See also</span></span>



[<span data-ttu-id="74dac-138">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="74dac-138">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="74dac-139">�����������</span><span class="sxs-lookup"><span data-stu-id="74dac-139">NOTIFICATION</span></span>](notification.md)


[<span data-ttu-id="74dac-140">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="74dac-140">MAPI Structures</span></span>](mapi-structures.md)

