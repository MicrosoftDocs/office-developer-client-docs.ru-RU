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
ms.openlocfilehash: 8cd96dd22daeb98646a62672bd17f7de4d2f7dab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808133"
---
# <a name="canceling-a-notification"></a><span data-ttu-id="a9db0-103">Отмена уведомления</span><span class="sxs-lookup"><span data-stu-id="a9db0-103">Canceling a Notification</span></span>

  
  
<span data-ttu-id="a9db0-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a9db0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a9db0-105">Чтобы отменить уведомление, клиенты вызов метода **Unadvise** источник уведомлений.</span><span class="sxs-lookup"><span data-stu-id="a9db0-105">To cancel a notification, clients call an advise source's **Unadvise** method.</span></span> <span data-ttu-id="a9db0-106">Вызов **Unadvise** важна, так как он вызывает поставщика услуг для освобождения ссылку на приемник уведомлений.</span><span class="sxs-lookup"><span data-stu-id="a9db0-106">Calling **Unadvise** is important because it causes the service provider to release its reference to your advise sink.</span></span> <span data-ttu-id="a9db0-107">При условии, что поставщик услуг поддерживает ссылку на приемника уведомления, приемник уведомлений могут предоставляться [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) вызовов.</span><span class="sxs-lookup"><span data-stu-id="a9db0-107">As long as a service provider maintains a reference to an advise sink, the advise sink can continue to receive [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) calls.</span></span> <span data-ttu-id="a9db0-108">На самом деле поскольку асинхронные события уведомлений, можно получать уведомления клиентов, даже после успешного **Unadvise** вызова.</span><span class="sxs-lookup"><span data-stu-id="a9db0-108">In fact, because of the asynchronous nature of event notification, clients can be notified even after a successful **Unadvise** call.</span></span> <span data-ttu-id="a9db0-109">Клиенты должны обладать возможностью для обработки получения уведомлений в любое время.</span><span class="sxs-lookup"><span data-stu-id="a9db0-109">Clients must be able to handle the receipt of notifications at any time.</span></span> 
  
<span data-ttu-id="a9db0-110">Так как отличаются реализации поставщика службы, клиенты, которые не удается вызвать **Unadvise** Отмена уведомление о нельзя предполагают что-либо о при поставщика выпустит ссылка на их приемник уведомлений.</span><span class="sxs-lookup"><span data-stu-id="a9db0-110">Because service provider implementations differ, clients that fail to call **Unadvise** to cancel a notification cannot assume anything about when a provider will release its reference to their advise sink.</span></span> <span data-ttu-id="a9db0-111">Некоторые поставщики услуг освободить их ссылки на приемников уведомлений, когда они освобождать их источников уведомлений.</span><span class="sxs-lookup"><span data-stu-id="a9db0-111">Some service providers release their references to advise sinks when they release their advise sources.</span></span> <span data-ttu-id="a9db0-112">Некоторые поставщики услуг — нет.</span><span class="sxs-lookup"><span data-stu-id="a9db0-112">Some service providers do not.</span></span> <span data-ttu-id="a9db0-113">При условии, что поставщик услуг поддерживает ссылку на приемника уведомления, что приемник уведомлений можно продолжить получать уведомления.</span><span class="sxs-lookup"><span data-stu-id="a9db0-113">As long as a service provider maintains a reference to an advise sink, that advise sink can continue to receive notifications.</span></span> 
  

