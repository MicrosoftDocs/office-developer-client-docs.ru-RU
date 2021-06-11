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
ms.openlocfilehash: 0fb867d662064dfe5ff7759dba4b36a4635a2914
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427731"
---
# <a name="hrthisthreadadvisesink"></a><span data-ttu-id="c18a1-103">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="c18a1-103">HrThisThreadAdviseSink</span></span>

  
  
<span data-ttu-id="c18a1-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c18a1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c18a1-105">Создает раковину рекомендации, которая обертывания существующей раковины рекомендации для безопасности потока.</span><span class="sxs-lookup"><span data-stu-id="c18a1-105">Creates an advise sink that wraps an existing advise sink for thread safety.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c18a1-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="c18a1-106">Header file:</span></span>  <br/> |<span data-ttu-id="c18a1-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="c18a1-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="c18a1-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="c18a1-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c18a1-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c18a1-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c18a1-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="c18a1-110">Called by:</span></span>  <br/> |<span data-ttu-id="c18a1-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="c18a1-111">Client applications</span></span>  <br/> |
   
```cpp
HrThisThreadAdviseSink(
  LPMAPIADVISESINK lpAdviseSink,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a><span data-ttu-id="c18a1-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="c18a1-112">Parameters</span></span>

 <span data-ttu-id="c18a1-113">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="c18a1-113">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="c18a1-114">[in] Указатель на раковину рекомендации, которая должна быть завернута.</span><span class="sxs-lookup"><span data-stu-id="c18a1-114">[in] Pointer to the advise sink to be wrapped.</span></span> 
    
 <span data-ttu-id="c18a1-115">_lppAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="c18a1-115">_lppAdviseSink_</span></span>
  
> <span data-ttu-id="c18a1-116">[вышел] Указатель на указатель на новую раковину рекомендации, которая заворачивает раковину рекомендации, указываемую _параметром lpAdviseSink._</span><span class="sxs-lookup"><span data-stu-id="c18a1-116">[out] Pointer to a pointer to a new advise sink that wraps the advise sink pointed to by the  _lpAdviseSink_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c18a1-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c18a1-117">Return value</span></span>

<span data-ttu-id="c18a1-118">Нет.</span><span class="sxs-lookup"><span data-stu-id="c18a1-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c18a1-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="c18a1-119">Remarks</span></span>

<span data-ttu-id="c18a1-120">Цель оболочки — убедиться, что уведомление вызвано на том же потоке, который называется функцией **HrThisThreadAdviseSink.**</span><span class="sxs-lookup"><span data-stu-id="c18a1-120">The purpose of the wrapper is to make sure that notification is called on the same thread that called the **HrThisThreadAdviseSink** function.</span></span> <span data-ttu-id="c18a1-121">Эта функция используется для защиты от вызовов уведомлений, которые должны работать на определенном потоке.</span><span class="sxs-lookup"><span data-stu-id="c18a1-121">This function is used to protect notification callbacks that must run on a particular thread.</span></span> 
  
<span data-ttu-id="c18a1-122">Клиентские приложения должны использовать **HrThisThreadAdviseSink,** чтобы ограничить время получения уведомлений, то есть при вызове в [метод IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) объекта-раковины, переданного клиентом в предыдущем вызове Посоветуйте. </span><span class="sxs-lookup"><span data-stu-id="c18a1-122">Client applications should use **HrThisThreadAdviseSink** to restrict when notifications are generated, that is, when calls are made to the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method of the advise sink object passed by the client in a previous **Advise** call.</span></span> <span data-ttu-id="c18a1-123">Если уведомления могут быть созданы произвольно, реализация уведомлений может заставить клиента в многоуровневую операцию, если это не будет уместно.</span><span class="sxs-lookup"><span data-stu-id="c18a1-123">If notifications are allowed to be generated arbitrarily, a notification implementation might force a client into multithreaded operation when that would not be appropriate.</span></span> <span data-ttu-id="c18a1-124">Например, клиент может использовать библиотеку, например одну из библиотек классов Microsoft Foundation, которая не поддерживает многоуровневые вызовы.</span><span class="sxs-lookup"><span data-stu-id="c18a1-124">For example, a client might use a library, such as one of the Microsoft Foundation Class Libraries, that does not support multithreaded calls.</span></span> <span data-ttu-id="c18a1-125">Уведомление на другом потоке затруднит тестирование такого клиента и сделает его склонным к ошибке.</span><span class="sxs-lookup"><span data-stu-id="c18a1-125">Notification on a different thread would make such a client difficult to test and prone to error.</span></span> 
  
 <span data-ttu-id="c18a1-126">**HrThisThreadAdviseSink** позволяет убедиться, что **вызовы OnNotify** происходят только в указанные периоды:</span><span class="sxs-lookup"><span data-stu-id="c18a1-126">**HrThisThreadAdviseSink** makes sure that **OnNotify** calls occur only at these appropriate times:</span></span> 
  
- <span data-ttu-id="c18a1-127">Во время обработки вызова к любому методу MAPI.</span><span class="sxs-lookup"><span data-stu-id="c18a1-127">During processing of a call to any MAPI method.</span></span> 
    
- <span data-ttu-id="c18a1-128">Во время обработки Windows сообщений.</span><span class="sxs-lookup"><span data-stu-id="c18a1-128">During processing of Windows messages.</span></span> 
    
<span data-ttu-id="c18a1-129">При **реализации HrThisThreadAdviseSink** любые вызовы в метод **OnNotify** новой раковины рекомендации в любом потоке приводят к выполнению исходного метода уведомления в потоке, на котором был вызван **HrThisThreadAdviseSink.**</span><span class="sxs-lookup"><span data-stu-id="c18a1-129">When **HrThisThreadAdviseSink** is implemented, any calls to the new advise sink's **OnNotify** method on any thread cause the original notification method to be executed on the thread on which **HrThisThreadAdviseSink** was called.</span></span> 
  
<span data-ttu-id="c18a1-130">Дополнительные сведения об уведомлениях и рекомендации по раковинам см. в примере [Event Notification in MAPI](event-notification-in-mapi.md) и [implementing an Advise Sink Object.](implementing-an-advise-sink-object.md)</span><span class="sxs-lookup"><span data-stu-id="c18a1-130">For more information about notification and advise sinks, see [Event Notification in MAPI](event-notification-in-mapi.md) and [Implementing an Advise Sink Object](implementing-an-advise-sink-object.md).</span></span> 
  

