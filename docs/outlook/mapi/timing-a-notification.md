---
title: Выбор времени уведомления
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6981a3b0-96eb-44a2-b051-1c5efc70e9e3
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: fa3b155820c64ff55e324c5611eed7348cb93e2b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360398"
---
# <a name="timing-a-notification"></a><span data-ttu-id="101ea-103">Выбор времени уведомления</span><span class="sxs-lookup"><span data-stu-id="101ea-103">Timing a Notification</span></span>

  
  
<span data-ttu-id="101ea-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="101ea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="101ea-105">Так как уведомление о событии является асинхронным процессом, вы можете получать уведомления в любое время, не обязательно сразу после возникновения события.</span><span class="sxs-lookup"><span data-stu-id="101ea-105">Because event notification is an asynchronous process, you can be notified at any time, not necessarily immediately after the event has occurred.</span></span>
  
 <span data-ttu-id="101ea-106">Время вызовов метода [имапиадвисесинк:: OnNotify](imapiadvisesink-onnotify.md) зависит от поставщика услуг, реализующего источник рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="101ea-106">The timing of calls to your [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method varies depending on the service provider implementing the advise source.</span></span> <span data-ttu-id="101ea-107">Поставщики услуг могут уведомлять клиента:</span><span class="sxs-lookup"><span data-stu-id="101ea-107">Service providers can notify your client either:</span></span> 
  
- <span data-ttu-id="101ea-108">Одновременно с событием.</span><span class="sxs-lookup"><span data-stu-id="101ea-108">Simultaneously with the event.</span></span>
    
- <span data-ttu-id="101ea-109">Непосредственно после события.</span><span class="sxs-lookup"><span data-stu-id="101ea-109">Directly after the event.</span></span>
    
- <span data-ttu-id="101ea-110">Позже после события, возможно, после вызова метода unadvise \*\*\*\* .</span><span class="sxs-lookup"><span data-stu-id="101ea-110">At some later point following the event, possibly after an **Unadvise** call.</span></span> 
    
<span data-ttu-id="101ea-111">Большинство поставщиков услуг вызывают \*\*\*\* функцию OnNotify после того, как метод MAPI, отвечающий за событие, возвращается вызывающему абоненту.</span><span class="sxs-lookup"><span data-stu-id="101ea-111">Most service providers call **OnNotify** after the MAPI method responsible for the event has returned to its caller.</span></span> <span data-ttu-id="101ea-112">Например, уведомления о сообщениях отправляются либо при сохранении изменений в сообщении, после вызова [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) , либо при освобождении сообщения после вызова **IUnknown:: Release** .</span><span class="sxs-lookup"><span data-stu-id="101ea-112">For example, notifications on messages are sent either when changes to the message are saved, after the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) call, or when the message is released, after the **IUnknown::Release** call.</span></span> <span data-ttu-id="101ea-113">Пока уведомление не будет отправлено, в хранилище сообщений не будут отображаться никакие изменения.</span><span class="sxs-lookup"><span data-stu-id="101ea-113">Until the notification is sent, no changes are visible in the message store.</span></span> 
  
<span data-ttu-id="101ea-114">Вы можете получать уведомления из источника уведомлений после вызова метода Unadvise для \*\*\*\* отмены регистрации.</span><span class="sxs-lookup"><span data-stu-id="101ea-114">You can receive notifications from an advise source after you have called **Unadvise** to cancel a registration.</span></span> <span data-ttu-id="101ea-115">Не забудьте разблокировать приемник уведомлений только после того, как его значение счетчика ссылок будет равно нулю, а \*\*\*\* не следовать за успешным вызовом метода unadvise.</span><span class="sxs-lookup"><span data-stu-id="101ea-115">Be sure to release your advise sink only after its reference count has fallen to zero, not following a successful **Unadvise** call.</span></span> <span data-ttu-id="101ea-116">Не следует предполагать, что, так как \*\*\*\* вы вызвали метод unadvise, который больше не нужен.</span><span class="sxs-lookup"><span data-stu-id="101ea-116">Do not assume that because you have called **Unadvise** that the advise sink is no longer necessary.</span></span> 
  

