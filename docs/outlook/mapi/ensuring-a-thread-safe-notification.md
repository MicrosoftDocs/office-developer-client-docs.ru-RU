---
title: Обеспечение уведомления Thread-Safe
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
# <a name="ensuring-a-thread-safe-notification"></a><span data-ttu-id="90c24-103">Обеспечение уведомления Thread-Safe</span><span class="sxs-lookup"><span data-stu-id="90c24-103">Ensuring a Thread-Safe Notification</span></span>

  
  
<span data-ttu-id="90c24-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="90c24-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="90c24-105">Если клиент работает на многоуровневой платформе, может потребоваться гарантия того, что вызовы в [методы IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) происходят в определенном потоке.</span><span class="sxs-lookup"><span data-stu-id="90c24-105">If your client runs on a multithreaded platform, you may need assurance that calls to your [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) methods occur on a particular thread.</span></span> <span data-ttu-id="90c24-106">Поскольку **вызовы OnNotify** обычно могут возникать в любом потоке, можно получать уведомления о неожиданных и нежелательных потоках, что приводит к ошибкам, которые сложно отлагировать.</span><span class="sxs-lookup"><span data-stu-id="90c24-106">Because calls to **OnNotify** can typically occur on any thread, it is possible to receive notifications on unexpected and unwanted threads, leading to errors that are difficult to debug.</span></span> 
  
<span data-ttu-id="90c24-107">Чтобы гарантировать, что вызовы **в OnNotify** для определенного уведомления  будут сделаны на том же потоке, который использовался для вызова "Советы", перед вызовом сообщите [hrThisThreadAdviseSink](hrthisthreadadvisesink.md) **.**</span><span class="sxs-lookup"><span data-stu-id="90c24-107">To guarantee that calls to **OnNotify** for a particular notification are made on the same thread that was used for the **Advise** call, call [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) before calling **Advise**.</span></span> <span data-ttu-id="90c24-108">\*\* \*\*HrThisThisThreadAdviseSink\*\*\*\* создает новый объект раковины рекомендации из объекта раковины рекомендации.</span><span class="sxs-lookup"><span data-stu-id="90c24-108">\*\* \*\*HrThisThreadAdviseSink\*\*\*\* creates a new advise sink object from your advise sink object.</span></span> <span data-ttu-id="90c24-109">Передай этот новый объект в вызове **Посоветуйте.**</span><span class="sxs-lookup"><span data-stu-id="90c24-109">Pass this new object in the call to **Advise**.</span></span> <span data-ttu-id="90c24-110">Все клиенты, которые могут не работать вне контекста определенного потока, должны всегда регистрировать объекты раковины, созданные **с помощью HrThisThreadAdviseSink.**</span><span class="sxs-lookup"><span data-stu-id="90c24-110">All clients with advise sink objects that might not work outside the context of a particular thread should always register advise sink objects created with **HrThisThreadAdviseSink**.</span></span>
  

