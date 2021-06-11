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
# <a name="timing-a-notification"></a><span data-ttu-id="67ae4-103">Синхронизация уведомления</span><span class="sxs-lookup"><span data-stu-id="67ae4-103">Timing a Notification</span></span>

  
  
<span data-ttu-id="67ae4-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="67ae4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="67ae4-105">Поскольку уведомление о событии является асинхронным процессом, вы можете быть уведомлены в любое время, не обязательно сразу после события.</span><span class="sxs-lookup"><span data-stu-id="67ae4-105">Because event notification is an asynchronous process, you can be notified at any time, not necessarily immediately after the event has occurred.</span></span>
  
 <span data-ttu-id="67ae4-106">Время звонков в [метод IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) зависит от поставщика услуг, реализующих источник консультаций.</span><span class="sxs-lookup"><span data-stu-id="67ae4-106">The timing of calls to your [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method varies depending on the service provider implementing the advise source.</span></span> <span data-ttu-id="67ae4-107">Поставщики услуг могут уведомить клиента:</span><span class="sxs-lookup"><span data-stu-id="67ae4-107">Service providers can notify your client either:</span></span> 
  
- <span data-ttu-id="67ae4-108">Одновременно с событием.</span><span class="sxs-lookup"><span data-stu-id="67ae4-108">Simultaneously with the event.</span></span>
    
- <span data-ttu-id="67ae4-109">Сразу после события.</span><span class="sxs-lookup"><span data-stu-id="67ae4-109">Directly after the event.</span></span>
    
- <span data-ttu-id="67ae4-110">В более поздней точке после события, возможно, после вызова **Unadvise.**</span><span class="sxs-lookup"><span data-stu-id="67ae4-110">At some later point following the event, possibly after an **Unadvise** call.</span></span> 
    
<span data-ttu-id="67ae4-111">Большинство поставщиков услуг звонят **onNotify** после того, как метод MAPI, ответственный за событие, возвращается вызываемой службе.</span><span class="sxs-lookup"><span data-stu-id="67ae4-111">Most service providers call **OnNotify** after the MAPI method responsible for the event has returned to its caller.</span></span> <span data-ttu-id="67ae4-112">Например, уведомления о сообщениях отправляются либо при сохранения изменений в сообщении после вызова [IMAPIProp:::SaveChanges,](imapiprop-savechanges.md) либо при выходе сообщения после вызова **IUnknown::Release.**</span><span class="sxs-lookup"><span data-stu-id="67ae4-112">For example, notifications on messages are sent either when changes to the message are saved, after the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) call, or when the message is released, after the **IUnknown::Release** call.</span></span> <span data-ttu-id="67ae4-113">До тех пор, пока уведомление не будет отправлено, в хранилище сообщений не будут видны изменения.</span><span class="sxs-lookup"><span data-stu-id="67ae4-113">Until the notification is sent, no changes are visible in the message store.</span></span> 
  
<span data-ttu-id="67ae4-114">Вы можете получать уведомления из источника консультаций после того, как вы вызвали **Unadvise,** чтобы отменить регистрацию.</span><span class="sxs-lookup"><span data-stu-id="67ae4-114">You can receive notifications from an advise source after you have called **Unadvise** to cancel a registration.</span></span> <span data-ttu-id="67ae4-115">Не забудьте выпустить раковину рекомендации только после того, как ее количество ссылок опустилось до нуля, а не после успешного вызова **Unadvise.**</span><span class="sxs-lookup"><span data-stu-id="67ae4-115">Be sure to release your advise sink only after its reference count has fallen to zero, not following a successful **Unadvise** call.</span></span> <span data-ttu-id="67ae4-116">Не следует предполагать, что из-за того, что вы вызвали **Unadvise,** необходимость в раковине рекомендации больше не требуется.</span><span class="sxs-lookup"><span data-stu-id="67ae4-116">Do not assume that because you have called **Unadvise** that the advise sink is no longer necessary.</span></span> 
  

