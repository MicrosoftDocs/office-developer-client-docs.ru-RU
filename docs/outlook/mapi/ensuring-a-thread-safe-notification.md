---
title: Обеспечение Thread-Safe уведомлений
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
# <a name="ensuring-a-thread-safe-notification"></a><span data-ttu-id="16df9-103">Обеспечение Thread-Safe уведомлений</span><span class="sxs-lookup"><span data-stu-id="16df9-103">Ensuring a Thread-Safe Notification</span></span>

  
  
<span data-ttu-id="16df9-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="16df9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="16df9-105">Если клиент работает на многопотоковой платформе, может потребоваться подтверждение того, что вызовы ваших методов [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) происходят в определенном потоке.</span><span class="sxs-lookup"><span data-stu-id="16df9-105">If your client runs on a multithreaded platform, you may need assurance that calls to your [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) methods occur on a particular thread.</span></span> <span data-ttu-id="16df9-106">Так как вызовы **OnNotify** обычно могут происходить в любом потоке, можно получать уведомления о непредвиденных и нежелательных потоках, что приводит к ошибкам, которые сложно отлалать.</span><span class="sxs-lookup"><span data-stu-id="16df9-106">Because calls to **OnNotify** can typically occur on any thread, it is possible to receive notifications on unexpected and unwanted threads, leading to errors that are difficult to debug.</span></span> 
  
<span data-ttu-id="16df9-107">Чтобы гарантировать, что **вызовы OnNotify** для определенного уведомления будут  делаться в том же потоке, который использовался для вызова advise, вызовите [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) перед вызовом **advise**.</span><span class="sxs-lookup"><span data-stu-id="16df9-107">To guarantee that calls to **OnNotify** for a particular notification are made on the same thread that was used for the **Advise** call, call [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) before calling **Advise**.</span></span> <span data-ttu-id="16df9-108">\*\* \*\*HrThisThreadAdviseSink\*\*\*\* создает новый объект-замещений из объекта-мятора консультации.</span><span class="sxs-lookup"><span data-stu-id="16df9-108">\*\* \*\*HrThisThreadAdviseSink\*\*\*\* creates a new advise sink object from your advise sink object.</span></span> <span data-ttu-id="16df9-109">Передайте этот новый объект в вызове **"Сообщить".**</span><span class="sxs-lookup"><span data-stu-id="16df9-109">Pass this new object in the call to **Advise**.</span></span> <span data-ttu-id="16df9-110">Все клиенты с рекомендуемые объекты-тонкторы, которые могут не работать вне контекста определенного потока, всегда должны регистрировать объекты-тонкторы, созданные с помощью **HrThisThreadAdviseSink.**</span><span class="sxs-lookup"><span data-stu-id="16df9-110">All clients with advise sink objects that might not work outside the context of a particular thread should always register advise sink objects created with **HrThisThreadAdviseSink**.</span></span>
  

