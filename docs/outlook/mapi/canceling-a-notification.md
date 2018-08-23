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
ms.openlocfilehash: 50d1fb451cbfcd07f97c5b12a9c86c03a435faa6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564775"
---
# <a name="canceling-a-notification"></a><span data-ttu-id="a5f16-103">Отмена уведомления</span><span class="sxs-lookup"><span data-stu-id="a5f16-103">Canceling a Notification</span></span>

  
  
<span data-ttu-id="a5f16-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a5f16-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a5f16-105">Чтобы отменить уведомление, клиенты вызов метода **Unadvise** источник уведомлений.</span><span class="sxs-lookup"><span data-stu-id="a5f16-105">To cancel a notification, clients call an advise source's **Unadvise** method.</span></span> <span data-ttu-id="a5f16-106">Вызов **Unadvise** важна, так как он вызывает поставщика услуг для освобождения ссылку на приемник уведомлений.</span><span class="sxs-lookup"><span data-stu-id="a5f16-106">Calling **Unadvise** is important because it causes the service provider to release its reference to your advise sink.</span></span> <span data-ttu-id="a5f16-107">При условии, что поставщик услуг поддерживает ссылку на приемника уведомления, приемник уведомлений могут предоставляться [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) вызовов.</span><span class="sxs-lookup"><span data-stu-id="a5f16-107">As long as a service provider maintains a reference to an advise sink, the advise sink can continue to receive [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) calls.</span></span> <span data-ttu-id="a5f16-108">На самом деле поскольку асинхронные события уведомлений, можно получать уведомления клиентов, даже после успешного **Unadvise** вызова.</span><span class="sxs-lookup"><span data-stu-id="a5f16-108">In fact, because of the asynchronous nature of event notification, clients can be notified even after a successful **Unadvise** call.</span></span> <span data-ttu-id="a5f16-109">Клиенты должны обладать возможностью для обработки получения уведомлений в любое время.</span><span class="sxs-lookup"><span data-stu-id="a5f16-109">Clients must be able to handle the receipt of notifications at any time.</span></span> 
  
<span data-ttu-id="a5f16-110">Так как отличаются реализации поставщика службы, клиенты, которые не удается вызвать **Unadvise** Отмена уведомление о нельзя предполагают что-либо о при поставщика выпустит ссылка на их приемник уведомлений.</span><span class="sxs-lookup"><span data-stu-id="a5f16-110">Because service provider implementations differ, clients that fail to call **Unadvise** to cancel a notification cannot assume anything about when a provider will release its reference to their advise sink.</span></span> <span data-ttu-id="a5f16-111">Некоторые поставщики услуг освободить их ссылки на приемников уведомлений, когда они освобождать их источников уведомлений.</span><span class="sxs-lookup"><span data-stu-id="a5f16-111">Some service providers release their references to advise sinks when they release their advise sources.</span></span> <span data-ttu-id="a5f16-112">Некоторые поставщики услуг — нет.</span><span class="sxs-lookup"><span data-stu-id="a5f16-112">Some service providers do not.</span></span> <span data-ttu-id="a5f16-113">При условии, что поставщик услуг поддерживает ссылку на приемника уведомления, что приемник уведомлений можно продолжить получать уведомления.</span><span class="sxs-lookup"><span data-stu-id="a5f16-113">As long as a service provider maintains a reference to an advise sink, that advise sink can continue to receive notifications.</span></span> 
  

