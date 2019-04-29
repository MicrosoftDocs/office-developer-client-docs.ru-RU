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
# <a name="canceling-a-notification"></a><span data-ttu-id="86790-103">Отмена уведомления</span><span class="sxs-lookup"><span data-stu-id="86790-103">Canceling a Notification</span></span>

  
  
<span data-ttu-id="86790-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="86790-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="86790-105">Для отмены уведомления клиенты вызывают метод unadvise источника Advise. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="86790-105">To cancel a notification, clients call an advise source's **Unadvise** method.</span></span> <span data-ttu-id="86790-106">Вызов **unadvise** важен, так как он заставляет поставщика услуг освободить ссылку на ваш приемник уведомлений.</span><span class="sxs-lookup"><span data-stu-id="86790-106">Calling **Unadvise** is important because it causes the service provider to release its reference to your advise sink.</span></span> <span data-ttu-id="86790-107">Пока поставщик услуг обслуживает ссылку на приемник уведомлений, приемник уведомлений может продолжать получать [имапиадвисесинк:: OnNotify](imapiadvisesink-onnotify.md) Calls.</span><span class="sxs-lookup"><span data-stu-id="86790-107">As long as a service provider maintains a reference to an advise sink, the advise sink can continue to receive [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) calls.</span></span> <span data-ttu-id="86790-108">На самом деле, из-за асинхронной природы уведомления о событиях клиенты могут получать уведомления даже после успешного \*\*\*\* вызова метода unadvise.</span><span class="sxs-lookup"><span data-stu-id="86790-108">In fact, because of the asynchronous nature of event notification, clients can be notified even after a successful **Unadvise** call.</span></span> <span data-ttu-id="86790-109">Клиенты должны иметь возможность обрабатывать получение уведомлений в любое время.</span><span class="sxs-lookup"><span data-stu-id="86790-109">Clients must be able to handle the receipt of notifications at any time.</span></span> 
  
<span data-ttu-id="86790-110">Так как реализации поставщиков служб различаются, клиенты, которые не могут вызывать метод **unadvise** для отмены уведомления, не могут ничего отказаться от того, когда поставщик будет освобождать ссылку на свой приемник уведомлений.</span><span class="sxs-lookup"><span data-stu-id="86790-110">Because service provider implementations differ, clients that fail to call **Unadvise** to cancel a notification cannot assume anything about when a provider will release its reference to their advise sink.</span></span> <span data-ttu-id="86790-111">Некоторые поставщики услуг освобождают свои ссылки на приемники уведомлений при выпуске их источников рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="86790-111">Some service providers release their references to advise sinks when they release their advise sources.</span></span> <span data-ttu-id="86790-112">Некоторые поставщики услуг не имеют.</span><span class="sxs-lookup"><span data-stu-id="86790-112">Some service providers do not.</span></span> <span data-ttu-id="86790-113">Пока поставщик услуг обслуживает ссылку на приемник уведомлений, этот приемник уведомлений может продолжать получать уведомления.</span><span class="sxs-lookup"><span data-stu-id="86790-113">As long as a service provider maintains a reference to an advise sink, that advise sink can continue to receive notifications.</span></span> 
  

