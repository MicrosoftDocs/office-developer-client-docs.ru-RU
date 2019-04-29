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
# <a name="errornotification"></a><span data-ttu-id="d3b65-103">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="d3b65-103">ERROR_NOTIFICATION</span></span>

  
  
<span data-ttu-id="d3b65-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d3b65-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d3b65-105">Описывает сведения, связанные с критической ошибкой.</span><span class="sxs-lookup"><span data-stu-id="d3b65-105">Describes information that relate to a critical error.</span></span> <span data-ttu-id="d3b65-106">Это приводит к созданию уведомления об ошибке.</span><span class="sxs-lookup"><span data-stu-id="d3b65-106">This causes an error notification to be generated.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d3b65-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="d3b65-107">Header file:</span></span>  <br/> |<span data-ttu-id="d3b65-108">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="d3b65-108">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="d3b65-109">Members</span><span class="sxs-lookup"><span data-stu-id="d3b65-109">Members</span></span>

 <span data-ttu-id="d3b65-110">**Кбентрид**</span><span class="sxs-lookup"><span data-stu-id="d3b65-110">**cbEntryID**</span></span>
  
> <span data-ttu-id="d3b65-111">Количество байтов в идентификаторе записи, на который указывает **лпентрид**.</span><span class="sxs-lookup"><span data-stu-id="d3b65-111">Count of bytes in the entry identifier pointed to by **lpEntryID**.</span></span> 
    
 <span data-ttu-id="d3b65-112">**Лпентрид**</span><span class="sxs-lookup"><span data-stu-id="d3b65-112">**lpEntryID**</span></span>
  
> <span data-ttu-id="d3b65-113">Указатель на идентификатор записи объекта, который вызывает ошибку.</span><span class="sxs-lookup"><span data-stu-id="d3b65-113">Pointer to the entry identifier of the object that causes the error.</span></span>
    
 <span data-ttu-id="d3b65-114">**SCODE**</span><span class="sxs-lookup"><span data-stu-id="d3b65-114">**scode**</span></span>
  
> <span data-ttu-id="d3b65-115">Значение ошибки для критической ошибки.</span><span class="sxs-lookup"><span data-stu-id="d3b65-115">Error value for the critical error.</span></span> 
    
 <span data-ttu-id="d3b65-116">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="d3b65-116">**ulFlags**</span></span>
  
> <span data-ttu-id="d3b65-117">Битовая маска флагов, используемая для обозначения формата текста, на который указывает элемент **лпсзеррор** в структуре, на которую указывает **лпмапиеррор**.</span><span class="sxs-lookup"><span data-stu-id="d3b65-117">Bitmask of flags used to designate the format of the text pointed to by the **lpszError** member in the structure pointed to by **lpMAPIError**.</span></span> <span data-ttu-id="d3b65-118">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="d3b65-118">The following flag can be set:</span></span>
    
<span data-ttu-id="d3b65-119">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d3b65-119">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="d3b65-120">Переданные строки имеют формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="d3b65-120">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="d3b65-121">Если флаг МАПИ_УНИКОДЕ не установлен, строки представлены в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="d3b65-121">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="d3b65-122">**Лпмапиеррор**</span><span class="sxs-lookup"><span data-stu-id="d3b65-122">**lpMAPIError**</span></span>
  
> <span data-ttu-id="d3b65-123">Указатель на структуру [мапиеррор](mapierror.md) , описывающую ошибку.</span><span class="sxs-lookup"><span data-stu-id="d3b65-123">Pointer to a [MAPIERROR](mapierror.md) structure describing the error.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d3b65-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="d3b65-124">Remarks</span></span>

<span data-ttu-id="d3b65-125">Структура **еррор_нотификатион** — это один из членов объединения структур, включенных в элемент **info** структуры [уведомления](notification.md) .</span><span class="sxs-lookup"><span data-stu-id="d3b65-125">The **ERROR_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="d3b65-126">Когда элемент **info** структуры **уведомлений** содержит структуру **Еррор_нотификатион** , элемент **улевенттипе** структуры **уведомлений** имеет значение _фневкритикалеррор_.</span><span class="sxs-lookup"><span data-stu-id="d3b65-126">When the **info** member of a **NOTIFICATION** structure contains an **ERROR_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to  _fnevCriticalError_.</span></span>
  
<span data-ttu-id="d3b65-127">Значение члена **кбентрид** и члена **лпентрид** могут иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="d3b65-127">The value of the **cbEntryID** member and the **lpEntryID** member can be NULL.</span></span> 
  
<span data-ttu-id="d3b65-128">Дополнительные сведения об уведомлении можно найти в разделах, приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="d3b65-128">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="d3b65-129">**Статья**</span><span class="sxs-lookup"><span data-stu-id="d3b65-129">**Topic**</span></span>|<span data-ttu-id="d3b65-130">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d3b65-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d3b65-131">Уведомление о соБытии в MAPI</span><span class="sxs-lookup"><span data-stu-id="d3b65-131">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="d3b65-132">Общие сведения о событиях уведомлений и уведомлений.</span><span class="sxs-lookup"><span data-stu-id="d3b65-132">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="d3b65-133">Обработка уведомлений</span><span class="sxs-lookup"><span data-stu-id="d3b65-133">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="d3b65-134">Обсуждение того, как клиенты должны обрабатывать уведомления.</span><span class="sxs-lookup"><span data-stu-id="d3b65-134">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="d3b65-135">Поддержка уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="d3b65-135">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="d3b65-136">Обсуждение того, как поставщики услуг могут использовать метод **имаписуппорт** для создания уведомлений.</span><span class="sxs-lookup"><span data-stu-id="d3b65-136">Discussion of how service providers can use the **IMAPISupport** method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d3b65-137">См. также</span><span class="sxs-lookup"><span data-stu-id="d3b65-137">See also</span></span>



[<span data-ttu-id="d3b65-138">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="d3b65-138">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="d3b65-139">�����������</span><span class="sxs-lookup"><span data-stu-id="d3b65-139">NOTIFICATION</span></span>](notification.md)


[<span data-ttu-id="d3b65-140">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="d3b65-140">MAPI Structures</span></span>](mapi-structures.md)

