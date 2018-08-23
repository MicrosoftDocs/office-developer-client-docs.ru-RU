---
title: Обеспечение потокобезопасности уведомлений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d46ce99a-4d7f-45b0-ba21-154498c15775
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: ad10b2ebd835b21f207fd43ecd8aebc7e1f475f4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585306"
---
# <a name="ensuring-a-thread-safe-notification"></a><span data-ttu-id="3df33-103">Обеспечение потокобезопасности уведомлений</span><span class="sxs-lookup"><span data-stu-id="3df33-103">Ensuring a Thread-Safe Notification</span></span>

  
  
<span data-ttu-id="3df33-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3df33-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3df33-105">Если клиент работает на многопоточные платформы, может потребоваться возникновения вызовы методов [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) в определенном потоке Software assurance.</span><span class="sxs-lookup"><span data-stu-id="3df33-105">If your client runs on a multithreaded platform, you may need assurance that calls to your [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) methods occur on a particular thread.</span></span> <span data-ttu-id="3df33-106">Так как вызовы **OnNotify** обычно могут выполняться в любом потоке, можно получать уведомления на непредвиденные и нежелательного потоки, приводят к ошибкам, которые трудно отладки.</span><span class="sxs-lookup"><span data-stu-id="3df33-106">Because calls to **OnNotify** can typically occur on any thread, it is possible to receive notifications on unexpected and unwanted threads, leading to errors that are difficult to debug.</span></span> 
  
<span data-ttu-id="3df33-107">Чтобы гарантировать, что вызовы **OnNotify** для конкретного уведомления выполняются в том же потоке, который использовался для **уведомлений** звонков, вызвать [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) перед вызовом **уведомлений**.</span><span class="sxs-lookup"><span data-stu-id="3df33-107">To guarantee that calls to **OnNotify** for a particular notification are made on the same thread that was used for the **Advise** call, call [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) before calling **Advise**.</span></span> <span data-ttu-id="3df33-108">\*\* \*\* HrThisThreadAdviseSink \*\*\* создает новый объект приемника уведомлений из объекта приемник уведомлений.</span><span class="sxs-lookup"><span data-stu-id="3df33-108">** **HrThisThreadAdviseSink**** creates a new advise sink object from your advise sink object.</span></span> <span data-ttu-id="3df33-109">Передайте этот новый объект в вызове **уведомлений**.</span><span class="sxs-lookup"><span data-stu-id="3df33-109">Pass this new object in the call to **Advise**.</span></span> <span data-ttu-id="3df33-110">Все клиенты с приемник уведомлений, объекты, которые могут работать вне контекста определенного потока всегда следует регистрировать уведомить приемника объектов, созданных с помощью **HrThisThreadAdviseSink**.</span><span class="sxs-lookup"><span data-stu-id="3df33-110">All clients with advise sink objects that might not work outside the context of a particular thread should always register advise sink objects created with **HrThisThreadAdviseSink**.</span></span>
  

