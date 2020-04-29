---
title: Обеспечение безопасного для потоков уведомления
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d46ce99a-4d7f-45b0-ba21-154498c15775
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 88c58d14893f2ac561dc56441eb38b7f4bd0db32
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424849"
---
# <a name="ensuring-a-thread-safe-notification"></a><span data-ttu-id="002fa-103">Обеспечение безопасного для потоков уведомления</span><span class="sxs-lookup"><span data-stu-id="002fa-103">Ensuring a Thread-Safe Notification</span></span>

  
  
<span data-ttu-id="002fa-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="002fa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="002fa-105">Если клиент работает на многопоточной платформе, может потребоваться гарантия того, что вызовы методов [имапиадвисесинк:: OnNotify](imapiadvisesink-onnotify.md) выполняются в определенном потоке.</span><span class="sxs-lookup"><span data-stu-id="002fa-105">If your client runs on a multithreaded platform, you may need assurance that calls to your [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) methods occur on a particular thread.</span></span> <span data-ttu-id="002fa-106">Так как вызовы **OnNotify** могут возникать в любом потоке, можно получать уведомления о непредвиденных и нежелательных потоках, ведущих к ошибкам, которые трудно отладить.</span><span class="sxs-lookup"><span data-stu-id="002fa-106">Because calls to **OnNotify** can typically occur on any thread, it is possible to receive notifications on unexpected and unwanted threads, leading to errors that are difficult to debug.</span></span> 
  
<span data-ttu-id="002fa-107">Чтобы гарантировать, что вызовы **OnNotify** для определенного уведомления выполняются в одном и том же потоке, который использовался для вызова **advise** , вызовите [хрсиссреададвисесинк](hrthisthreadadvisesink.md) перед вызовом **advise**.</span><span class="sxs-lookup"><span data-stu-id="002fa-107">To guarantee that calls to **OnNotify** for a particular notification are made on the same thread that was used for the **Advise** call, call [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) before calling **Advise**.</span></span> <span data-ttu-id="002fa-108">\* \* \* \* Хрсиссреададвисесинк \* \* \* \* создает новый объект приемника уведомлений из объекта приемника уведомлений.</span><span class="sxs-lookup"><span data-stu-id="002fa-108">\*\* \*\*HrThisThreadAdviseSink\*\*\*\* creates a new advise sink object from your advise sink object.</span></span> <span data-ttu-id="002fa-109">Передайте этот новый объект в вызове метода **advise**.</span><span class="sxs-lookup"><span data-stu-id="002fa-109">Pass this new object in the call to **Advise**.</span></span> <span data-ttu-id="002fa-110">Все клиенты с объектами приемника уведомлений, которые могут не работать вне контекста определенного потока, всегда должны регистрировать объекты приемника уведомлений, созданные с помощью **хрсиссреададвисесинк**.</span><span class="sxs-lookup"><span data-stu-id="002fa-110">All clients with advise sink objects that might not work outside the context of a particular thread should always register advise sink objects created with **HrThisThreadAdviseSink**.</span></span>
  

