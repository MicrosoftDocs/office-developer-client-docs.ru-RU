---
title: Выбор времени отправки уведомления
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6981a3b0-96eb-44a2-b051-1c5efc70e9e3
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 9ee999841b53f358dcee85d4d92c5056f665dbf1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812483"
---
# <a name="timing-a-notification"></a><span data-ttu-id="8c6ac-103">Выбор времени отправки уведомления</span><span class="sxs-lookup"><span data-stu-id="8c6ac-103">Timing a Notification</span></span>

  
  
<span data-ttu-id="8c6ac-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8c6ac-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8c6ac-105">Так как уведомления о событии представляет собой асинхронный процесс, можно получать уведомления в любое время, не всегда сразу же после возникновения события.</span><span class="sxs-lookup"><span data-stu-id="8c6ac-105">Because event notification is an asynchronous process, you can be notified at any time, not necessarily immediately after the event has occurred.</span></span>
  
 <span data-ttu-id="8c6ac-106">Время между вызовами в метод [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) зависит от поставщика услуг, реализация источник уведомлений.</span><span class="sxs-lookup"><span data-stu-id="8c6ac-106">The timing of calls to your [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method varies depending on the service provider implementing the advise source.</span></span> <span data-ttu-id="8c6ac-107">Поставщиков услуг можно либо сообщите вашего клиента:</span><span class="sxs-lookup"><span data-stu-id="8c6ac-107">Service providers can notify your client either:</span></span> 
  
- <span data-ttu-id="8c6ac-108">Одновременно с событием.</span><span class="sxs-lookup"><span data-stu-id="8c6ac-108">Simultaneously with the event.</span></span>
    
- <span data-ttu-id="8c6ac-109">Непосредственно после события.</span><span class="sxs-lookup"><span data-stu-id="8c6ac-109">Directly after the event.</span></span>
    
- <span data-ttu-id="8c6ac-110">В некоторых более поздней версии точке после событий, возможно **Unadvise** после вызова метода сразу.</span><span class="sxs-lookup"><span data-stu-id="8c6ac-110">At some later point following the event, possibly after an **Unadvise** call.</span></span> 
    
<span data-ttu-id="8c6ac-111">Большинство поставщиков услуг вызов **OnNotify** после возврата в вызывающий метод MAPI, ответственный за событие.</span><span class="sxs-lookup"><span data-stu-id="8c6ac-111">Most service providers call **OnNotify** after the MAPI method responsible for the event has returned to its caller.</span></span> <span data-ttu-id="8c6ac-112">Например при сохранении изменений в сообщение, после вызова [IMAPIProp::SaveChanges](imapiprop-savechanges.md) или после выхода сообщение, после вызова **функции IUnknown::Release** отправляются уведомления для сообщений.</span><span class="sxs-lookup"><span data-stu-id="8c6ac-112">For example, notifications on messages are sent either when changes to the message are saved, after the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) call, or when the message is released, after the **IUnknown::Release** call.</span></span> <span data-ttu-id="8c6ac-113">До отправки уведомления изменения не видны в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="8c6ac-113">Until the notification is sent, no changes are visible in the message store.</span></span> 
  
<span data-ttu-id="8c6ac-114">Вы можете получать уведомления из источника уведомлений после вызова **Unadvise** для отмены регистрации.</span><span class="sxs-lookup"><span data-stu-id="8c6ac-114">You can receive notifications from an advise source after you have called **Unadvise** to cancel a registration.</span></span> <span data-ttu-id="8c6ac-115">Убедитесь, что для освобождения вашей приемник уведомлений только после его счетчика упала на значение равно нулю, не после успешного вызова **Unadvise** .</span><span class="sxs-lookup"><span data-stu-id="8c6ac-115">Be sure to release your advise sink only after its reference count has fallen to zero, not following a successful **Unadvise** call.</span></span> <span data-ttu-id="8c6ac-116">Предполагается, что так как вызова **Unadvise** , приемник уведомлений больше не требуется.</span><span class="sxs-lookup"><span data-stu-id="8c6ac-116">Do not assume that because you have called **Unadvise** that the advise sink is no longer necessary.</span></span> 
  

