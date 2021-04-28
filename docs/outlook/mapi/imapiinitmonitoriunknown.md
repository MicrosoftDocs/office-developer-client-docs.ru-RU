---
title: 'IMAPIInitMonitor : IUnknown'
manager: lindalu
26ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIInitMonitor
api_type:
- COM
ms.assetid: ad71ea65-394d-4be2-a9da-cd23099bc2cc
description: IMAPIInitMonitor
Last modified: April 26, 2021
ms.openlocfilehash: dd17d50b04755d9d9c2a10a9b02cd821faf1f7ec
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062048"
---
# <a name="imapiinitmonitor--iunknown"></a><span data-ttu-id="ccfd0-103">IMAPIInitMonitor : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ccfd0-103">IMAPIInitMonitor : IUnknown</span></span>

<span data-ttu-id="ccfd0-104">**Применяется к**: Outlook 2013 | Outlook 2016 | Outlook 2019 г.</span><span class="sxs-lookup"><span data-stu-id="ccfd0-104">**Applies to**: Outlook 2013 | Outlook 2016 | Outlook 2019</span></span>

<span data-ttu-id="ccfd0-105">Иногда приложение, которое потребляет MAPI, может потребовать знать, когда инициализация будет завершена.</span><span class="sxs-lookup"><span data-stu-id="ccfd0-105">There are times when an application which consumes MAPI might want to know when the initialization is completed.</span></span> <span data-ttu-id="ccfd0-106">Например, он имеет несколько потоков, которые могут инициализировать MAPI, или в ответ на инициализацию MAPI приложение хотело бы выполнить некоторую работу, но не хочет всегда вращать стек MAPI.</span><span class="sxs-lookup"><span data-stu-id="ccfd0-106">For example, it has multiple threads which could initialize MAPI, or in response to MAPI being initialized the application would like perform some work, but does not want to always spin up the MAPI stack.</span></span> <span data-ttu-id="ccfd0-107">Монитор инициализации предоставляет эту функцию с помощью [объекта CreateMAPIInitializationMonitor.](createmapiinitializationmonitor.md)</span><span class="sxs-lookup"><span data-stu-id="ccfd0-107">The initialization monitor provides this functionality through a [CreateMAPIInitializationMonitor](createmapiinitializationmonitor.md) object.</span></span>

| <span data-ttu-id="ccfd0-108">быстрая информация</span><span class="sxs-lookup"><span data-stu-id="ccfd0-108">quick info</span></span> | <span data-ttu-id="ccfd0-109">result</span><span class="sxs-lookup"><span data-stu-id="ccfd0-109">result</span></span> |
|:-----|:-----|
|<span data-ttu-id="ccfd0-110">Наследует от:</span><span class="sxs-lookup"><span data-stu-id="ccfd0-110">Inherits from:</span></span>  <br/> |<span data-ttu-id="ccfd0-111">IUnknown</span><span class="sxs-lookup"><span data-stu-id="ccfd0-111">IUnknown</span></span>  <br/> |
|<span data-ttu-id="ccfd0-112">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="ccfd0-112">Implemented by:</span></span>  <br/> | <span data-ttu-id="ccfd0-113">OLMAPI32.DLL</span><span class="sxs-lookup"><span data-stu-id="ccfd0-113">OLMAPI32.DLL</span></span> <br/> |
|<span data-ttu-id="ccfd0-114">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="ccfd0-114">Called by:</span></span>  <br/> |<span data-ttu-id="ccfd0-115">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="ccfd0-115">Client applications</span></span>  <br/> |
|<span data-ttu-id="ccfd0-116">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="ccfd0-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="ccfd0-117">IID_IMAPIInitMonitor</span><span class="sxs-lookup"><span data-stu-id="ccfd0-117">IID_IMAPIInitMonitor</span></span>  <br/> |

## <a name="vtable-order"></a><span data-ttu-id="ccfd0-118">Заказ Vtable</span><span class="sxs-lookup"><span data-stu-id="ccfd0-118">Vtable order</span></span>

| <span data-ttu-id="ccfd0-119">функция</span><span class="sxs-lookup"><span data-stu-id="ccfd0-119">function</span></span> | <span data-ttu-id="ccfd0-120">description</span><span class="sxs-lookup"><span data-stu-id="ccfd0-120">description</span></span> |
|:-----|:-----|
|[<span data-ttu-id="ccfd0-121">IMAPIInitMonitor::IsInitialized</span><span class="sxs-lookup"><span data-stu-id="ccfd0-121">IMAPIInitMonitor::IsInitialized</span></span>](imapiinitmonitor-isinitialized.md) <br/> |<span data-ttu-id="ccfd0-122">Возвращает текущее состояние инициализации MAPI.</span><span class="sxs-lookup"><span data-stu-id="ccfd0-122">Returns the current state of MAPI initialization.</span></span>  <br/> |
|[<span data-ttu-id="ccfd0-123">IMAPIInitMonitor::Wait</span><span class="sxs-lookup"><span data-stu-id="ccfd0-123">IMAPIInitMonitor::Wait</span></span>](imapiinitmonitor-wait.md) <br/> |<span data-ttu-id="ccfd0-124">Инициирует вызов BLOCKING в этом потоке, который возвращается либо после инициализации указанного числа миллисекунд, либо при инициализации MAPI.</span><span class="sxs-lookup"><span data-stu-id="ccfd0-124">Initiates a BLOCKING call on this thread, which will return either when the specified number of milliseconds have elapsed or MAPI has been initialized.</span></span>  <span data-ttu-id="ccfd0-125">INFINITE можно использовать для бесконечного ожидания.</span><span class="sxs-lookup"><span data-stu-id="ccfd0-125">INFINITE can be used to for an infinite wait.</span></span>  <br/> |
|[<span data-ttu-id="ccfd0-126">IMAPIInitMonitor::BeginWait</span><span class="sxs-lookup"><span data-stu-id="ccfd0-126">IMAPIInitMonitor::BeginWait</span></span>](imapiinitmonitor-beginwait.md) <br/> |<span data-ttu-id="ccfd0-127">Начните ожидание инициализации MAPI или указанного числа миллисекунд, которые должны сойти.</span><span class="sxs-lookup"><span data-stu-id="ccfd0-127">Start a wait for MAPI initialization or the specified number of milliseconds to elapse.</span></span> <span data-ttu-id="ccfd0-128">Это возвращает интерфейс IMAPIWaitResult, который должен иметь "End" для того, чтобы начать ожидание.</span><span class="sxs-lookup"><span data-stu-id="ccfd0-128">This return an IMAPIWaitResult interface which should have “End” called in order begin the wait.</span></span>  <span data-ttu-id="ccfd0-129">Это позволяет звонячему управлять тем, какой поток заблокирован во время ожидания.</span><span class="sxs-lookup"><span data-stu-id="ccfd0-129">This allows the caller to control which thread is blocked while we are waiting.</span></span> <br/> |
