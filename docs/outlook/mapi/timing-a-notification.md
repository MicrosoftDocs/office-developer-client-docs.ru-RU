---
title: Синхронизация уведомления
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6981a3b0-96eb-44a2-b051-1c5efc70e9e3
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: fa3b155820c64ff55e324c5611eed7348cb93e2b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411150"
---
# <a name="timing-a-notification"></a><span data-ttu-id="d969f-103">Синхронизация уведомления</span><span class="sxs-lookup"><span data-stu-id="d969f-103">Timing a Notification</span></span>

  
  
<span data-ttu-id="d969f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d969f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d969f-105">Так как уведомление о событии является асинхронным процессом, уведомление можно получать в любое время, а не сразу после события.</span><span class="sxs-lookup"><span data-stu-id="d969f-105">Because event notification is an asynchronous process, you can be notified at any time, not necessarily immediately after the event has occurred.</span></span>
  
 <span data-ttu-id="d969f-106">Время вызовов метода [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) зависит от поставщика услуг, реализующих источник консультаций.</span><span class="sxs-lookup"><span data-stu-id="d969f-106">The timing of calls to your [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method varies depending on the service provider implementing the advise source.</span></span> <span data-ttu-id="d969f-107">Поставщики услуг могут уведомить клиент:</span><span class="sxs-lookup"><span data-stu-id="d969f-107">Service providers can notify your client either:</span></span> 
  
- <span data-ttu-id="d969f-108">Одновременно с событием.</span><span class="sxs-lookup"><span data-stu-id="d969f-108">Simultaneously with the event.</span></span>
    
- <span data-ttu-id="d969f-109">Сразу после события.</span><span class="sxs-lookup"><span data-stu-id="d969f-109">Directly after the event.</span></span>
    
- <span data-ttu-id="d969f-110">Через некоторое время после события, возможно, после вызова **Unadvise.**</span><span class="sxs-lookup"><span data-stu-id="d969f-110">At some later point following the event, possibly after an **Unadvise** call.</span></span> 
    
<span data-ttu-id="d969f-111">Большинство поставщиков услуг **звонят onNotify** после того, как метод MAPI, отвечающий за событие, возвращается вызываемой службе.</span><span class="sxs-lookup"><span data-stu-id="d969f-111">Most service providers call **OnNotify** after the MAPI method responsible for the event has returned to its caller.</span></span> <span data-ttu-id="d969f-112">Например, уведомления о сообщениях отправляются либо при сохранения изменений сообщения, после вызова [IMAPIProp::SaveChanges,](imapiprop-savechanges.md) либо при освобождении сообщения после вызова **IUnknown::Release.**</span><span class="sxs-lookup"><span data-stu-id="d969f-112">For example, notifications on messages are sent either when changes to the message are saved, after the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) call, or when the message is released, after the **IUnknown::Release** call.</span></span> <span data-ttu-id="d969f-113">Пока уведомление не будет отправлено, в хранилище сообщений не будут видны никакие изменения.</span><span class="sxs-lookup"><span data-stu-id="d969f-113">Until the notification is sent, no changes are visible in the message store.</span></span> 
  
<span data-ttu-id="d969f-114">Вы можете получать уведомления от источника консультации после того, как вы вызвали **Unadvise,** чтобы отменить регистрацию.</span><span class="sxs-lookup"><span data-stu-id="d969f-114">You can receive notifications from an advise source after you have called **Unadvise** to cancel a registration.</span></span> <span data-ttu-id="d969f-115">Убедитесь, что выпустите ваш обойдник консультации только после того, как его количество ссылок упадет до нуля, а не после успешного вызова **Unadvise.**</span><span class="sxs-lookup"><span data-stu-id="d969f-115">Be sure to release your advise sink only after its reference count has fallen to zero, not following a successful **Unadvise** call.</span></span> <span data-ttu-id="d969f-116">Не следует предполагать, что так как вы вызвали **Unadvise,** то в этом нет необходимости.</span><span class="sxs-lookup"><span data-stu-id="d969f-116">Do not assume that because you have called **Unadvise** that the advise sink is no longer necessary.</span></span> 
  

