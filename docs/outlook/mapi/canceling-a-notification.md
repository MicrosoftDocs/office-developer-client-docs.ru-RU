---
title: Отмена уведомления
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: decd5d7d-1f47-47c2-b9c4-be0e652c99dd
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: fb0972638fdd062c99040694222724566281024f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409764"
---
# <a name="canceling-a-notification"></a><span data-ttu-id="bb2ab-103">Отмена уведомления</span><span class="sxs-lookup"><span data-stu-id="bb2ab-103">Canceling a Notification</span></span>

  
  
<span data-ttu-id="bb2ab-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bb2ab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bb2ab-105">Чтобы отменить уведомление, клиенты звонят **методу Unadvise** источника консультации.</span><span class="sxs-lookup"><span data-stu-id="bb2ab-105">To cancel a notification, clients call an advise source's **Unadvise** method.</span></span> <span data-ttu-id="bb2ab-106">Вызов **Unadvise** важен, так как поставщик услуг освобождает ссылку на ваш поставщик услуг.</span><span class="sxs-lookup"><span data-stu-id="bb2ab-106">Calling **Unadvise** is important because it causes the service provider to release its reference to your advise sink.</span></span> <span data-ttu-id="bb2ab-107">Если поставщик услуг поддерживает ссылку на приемник консультации, приемник консультации может продолжать принимать вызовы [IMAPIAdviseSink::OnNotify.](imapiadvisesink-onnotify.md)</span><span class="sxs-lookup"><span data-stu-id="bb2ab-107">As long as a service provider maintains a reference to an advise sink, the advise sink can continue to receive [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) calls.</span></span> <span data-ttu-id="bb2ab-108">В действительности из-за асинхронного характера уведомления о событии клиенты могут получать уведомления даже после успешного вызова **Unadvise.**</span><span class="sxs-lookup"><span data-stu-id="bb2ab-108">In fact, because of the asynchronous nature of event notification, clients can be notified even after a successful **Unadvise** call.</span></span> <span data-ttu-id="bb2ab-109">Клиенты должны иметь возможность обрабатывать получение уведомлений в любое время.</span><span class="sxs-lookup"><span data-stu-id="bb2ab-109">Clients must be able to handle the receipt of notifications at any time.</span></span> 
  
<span data-ttu-id="bb2ab-110">Так как реализации поставщиков служб отличаются, клиенты, которые не могут вызвать **Unadvise** для отмены уведомления, не могут предположить, когда поставщик отпустит ссылку на свой поставщик.</span><span class="sxs-lookup"><span data-stu-id="bb2ab-110">Because service provider implementations differ, clients that fail to call **Unadvise** to cancel a notification cannot assume anything about when a provider will release its reference to their advise sink.</span></span> <span data-ttu-id="bb2ab-111">Некоторые поставщики услуг отпустят свои ссылки, чтобы сообщить операторам, когда они отпустят свои источники рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="bb2ab-111">Some service providers release their references to advise sinks when they release their advise sources.</span></span> <span data-ttu-id="bb2ab-112">Некоторые поставщики услуг этого не делают.</span><span class="sxs-lookup"><span data-stu-id="bb2ab-112">Some service providers do not.</span></span> <span data-ttu-id="bb2ab-113">Если поставщик услуг поддерживает ссылку на приемник консультаций, он может продолжать получать уведомления.</span><span class="sxs-lookup"><span data-stu-id="bb2ab-113">As long as a service provider maintains a reference to an advise sink, that advise sink can continue to receive notifications.</span></span> 
  

