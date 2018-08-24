---
title: HrThisThreadAdviseSink
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrThisThreadAdviseSink
api_type:
- COM
ms.assetid: 12c07302-472f-4e4f-8087-1bdf0dc09a5a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3df5e012867623d1c5e8fb5c3c93103548ab97be
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588386"
---
# <a name="hrthisthreadadvisesink"></a><span data-ttu-id="dc102-103">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="dc102-103">HrThisThreadAdviseSink</span></span>

  
  
<span data-ttu-id="dc102-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dc102-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dc102-105">Создание приемника уведомления, которое имеет приемника уведомления для потокобезопасность.</span><span class="sxs-lookup"><span data-stu-id="dc102-105">Creates an advise sink that wraps an existing advise sink for thread safety.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dc102-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="dc102-106">Header file:</span></span>  <br/> |<span data-ttu-id="dc102-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="dc102-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="dc102-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="dc102-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="dc102-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="dc102-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="dc102-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="dc102-110">Called by:</span></span>  <br/> |<span data-ttu-id="dc102-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="dc102-111">Client applications</span></span>  <br/> |
   
```cpp
HrThisThreadAdviseSink(
  LPMAPIADVISESINK lpAdviseSink,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a><span data-ttu-id="dc102-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="dc102-112">Parameters</span></span>

 <span data-ttu-id="dc102-113">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="dc102-113">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="dc102-114">[in] Указатель на приемник уведомлений преобразуемый.</span><span class="sxs-lookup"><span data-stu-id="dc102-114">[in] Pointer to the advise sink to be wrapped.</span></span> 
    
 <span data-ttu-id="dc102-115">_lppAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="dc102-115">_lppAdviseSink_</span></span>
  
> <span data-ttu-id="dc102-116">[out] Указатель на указатель на новый приемник уведомлений, который является оболочкой приемник уведомлений, на который указывает параметр _lpAdviseSink_ .</span><span class="sxs-lookup"><span data-stu-id="dc102-116">[out] Pointer to a pointer to a new advise sink that wraps the advise sink pointed to by the  _lpAdviseSink_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="dc102-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dc102-117">Return value</span></span>

<span data-ttu-id="dc102-118">Нет.</span><span class="sxs-lookup"><span data-stu-id="dc102-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dc102-119">Замечания</span><span class="sxs-lookup"><span data-stu-id="dc102-119">Remarks</span></span>

<span data-ttu-id="dc102-120">Программа-оболочка предназначен для убедитесь в том, что уведомления вызывается в том же потоке, который вызывается функция **HrThisThreadAdviseSink** .</span><span class="sxs-lookup"><span data-stu-id="dc102-120">The purpose of the wrapper is to make sure that notification is called on the same thread that called the **HrThisThreadAdviseSink** function.</span></span> <span data-ttu-id="dc102-121">Эта функция используется для защиты уведомлений обратных вызовов, которые необходимо выполнить в определенном потоке.</span><span class="sxs-lookup"><span data-stu-id="dc102-121">This function is used to protect notification callbacks that must run on a particular thread.</span></span> 
  
<span data-ttu-id="dc102-122">Клиентские приложения следует использовать **HrThisThreadAdviseSink** для ограничения при создании уведомлений, то есть, при вызове метода [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) объекта приемник уведомлений, передается клиентом в предыдущем **уведомлений **вызова.</span><span class="sxs-lookup"><span data-stu-id="dc102-122">Client applications should use **HrThisThreadAdviseSink** to restrict when notifications are generated, that is, when calls are made to the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method of the advise sink object passed by the client in a previous **Advise** call.</span></span> <span data-ttu-id="dc102-123">Если уведомления могут создаваться произвольно, уведомления о реализации может принудительно клиента в многопоточные операции при, который может быть неприемлема.</span><span class="sxs-lookup"><span data-stu-id="dc102-123">If notifications are allowed to be generated arbitrarily, a notification implementation might force a client into multithreaded operation when that would not be appropriate.</span></span> <span data-ttu-id="dc102-124">Например клиента использовать библиотеки, например один из библиотеки классов Microsoft Foundation, который не поддерживает многопоточных вызовов.</span><span class="sxs-lookup"><span data-stu-id="dc102-124">For example, a client might use a library, such as one of the Microsoft Foundation Class Libraries, that does not support multithreaded calls.</span></span> <span data-ttu-id="dc102-125">Уведомления в потоке сделает такой клиент неудобен для тестирования и может привести к ошибке.</span><span class="sxs-lookup"><span data-stu-id="dc102-125">Notification on a different thread would make such a client difficult to test and prone to error.</span></span> 
  
 <span data-ttu-id="dc102-126">**HrThisThreadAdviseSink** следит за тем, что **OnNotify** вызовы происходят только при этом соответствующий:</span><span class="sxs-lookup"><span data-stu-id="dc102-126">**HrThisThreadAdviseSink** makes sure that **OnNotify** calls occur only at these appropriate times:</span></span> 
  
- <span data-ttu-id="dc102-127">Во время обработки вызова любого метода MAPI.</span><span class="sxs-lookup"><span data-stu-id="dc102-127">During processing of a call to any MAPI method.</span></span> 
    
- <span data-ttu-id="dc102-128">Во время обработки сообщений Windows.</span><span class="sxs-lookup"><span data-stu-id="dc102-128">During processing of Windows messages.</span></span> 
    
<span data-ttu-id="dc102-129">При реализации **HrThisThreadAdviseSink** все вызовы метода **OnNotify** новый приемник уведомлений в любом потоке вызвать для выполнения в потоке, на котором **HrThisThreadAdviseSink** вызван метод исходного уведомления.</span><span class="sxs-lookup"><span data-stu-id="dc102-129">When **HrThisThreadAdviseSink** is implemented, any calls to the new advise sink's **OnNotify** method on any thread cause the original notification method to be executed on the thread on which **HrThisThreadAdviseSink** was called.</span></span> 
  
<span data-ttu-id="dc102-130">Дополнительные сведения о уведомлений и приемников уведомлений, [Уведомления о событии в MAPI](event-notification-in-mapi.md) и [реализация объекта уведомить приемника](implementing-an-advise-sink-object.md).</span><span class="sxs-lookup"><span data-stu-id="dc102-130">For more information about notification and advise sinks, see [Event Notification in MAPI](event-notification-in-mapi.md) and [Implementing an Advise Sink Object](implementing-an-advise-sink-object.md).</span></span> 
  

