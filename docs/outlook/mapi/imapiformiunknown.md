---
title: IMAPIForm IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm
api_type:
- COM
ms.assetid: e9059739-51b4-4574-bd0f-709eb5144ae7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 172cbf9478d3206742df61d211051594e69ab173
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436386"
---
# <a name="imapiform--iunknown"></a><span data-ttu-id="f78a9-103">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f78a9-103">IMAPIForm : IUnknown</span></span>

  
  
<span data-ttu-id="f78a9-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f78a9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f78a9-105">Позволяет зрителям форм работать с контекстами представления форм и уведомлениями форм, выполнять глаголы форм и закрывать формы.</span><span class="sxs-lookup"><span data-stu-id="f78a9-105">Enables form viewers to work with form view contexts and form notification, to perform form verbs, and to shut down forms.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f78a9-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="f78a9-106">Header file:</span></span>  <br/> |<span data-ttu-id="f78a9-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="f78a9-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="f78a9-108">Подвергается:</span><span class="sxs-lookup"><span data-stu-id="f78a9-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="f78a9-109">Объекты форм</span><span class="sxs-lookup"><span data-stu-id="f78a9-109">Form objects</span></span>  <br/> |
|<span data-ttu-id="f78a9-110">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="f78a9-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="f78a9-111">Серверы форм</span><span class="sxs-lookup"><span data-stu-id="f78a9-111">Form servers</span></span>  <br/> |
|<span data-ttu-id="f78a9-112">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="f78a9-112">Called by:</span></span>  <br/> |<span data-ttu-id="f78a9-113">Просмотр форм</span><span class="sxs-lookup"><span data-stu-id="f78a9-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="f78a9-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="f78a9-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="f78a9-115">IID_IMAPIForm</span><span class="sxs-lookup"><span data-stu-id="f78a9-115">IID_IMAPIForm</span></span>  <br/> |
|<span data-ttu-id="f78a9-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="f78a9-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="f78a9-117">LPMAPIFORM</span><span class="sxs-lookup"><span data-stu-id="f78a9-117">LPMAPIFORM</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="f78a9-118">Заказ Vtable</span><span class="sxs-lookup"><span data-stu-id="f78a9-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="f78a9-119">SetViewContext</span><span class="sxs-lookup"><span data-stu-id="f78a9-119">SetViewContext</span></span>](imapiform-setviewcontext.md) <br/> |<span data-ttu-id="f78a9-120">Создает контекст представления для формы.</span><span class="sxs-lookup"><span data-stu-id="f78a9-120">Establishes a view context for the form.</span></span>  <br/> |
|[<span data-ttu-id="f78a9-121">GetViewContext</span><span class="sxs-lookup"><span data-stu-id="f78a9-121">GetViewContext</span></span>](imapiform-getviewcontext.md) <br/> |<span data-ttu-id="f78a9-122">Возвращает текущий контекст представления для формы.</span><span class="sxs-lookup"><span data-stu-id="f78a9-122">Returns the current view context for the form.</span></span>  <br/> |
|[<span data-ttu-id="f78a9-123">ShutdownForm</span><span class="sxs-lookup"><span data-stu-id="f78a9-123">ShutdownForm</span></span>](imapiform-shutdownform.md) <br/> |<span data-ttu-id="f78a9-124">Закрывает форму.</span><span class="sxs-lookup"><span data-stu-id="f78a9-124">Closes the form.</span></span>  <br/> |
|[<span data-ttu-id="f78a9-125">DoVerb</span><span class="sxs-lookup"><span data-stu-id="f78a9-125">DoVerb</span></span>](imapiform-doverb.md) <br/> |<span data-ttu-id="f78a9-126">Запрашивает, чтобы форма выполняла любые задачи, которые она связывает с определенным глаголом.</span><span class="sxs-lookup"><span data-stu-id="f78a9-126">Requests that the form perform whatever tasks it associates with a specific verb.</span></span>  <br/> |
|[<span data-ttu-id="f78a9-127">Консультирование</span><span class="sxs-lookup"><span data-stu-id="f78a9-127">Advise</span></span>](imapiform-advise.md) <br/> |<span data-ttu-id="f78a9-128">Регистрирует просмотра форм для уведомлений о событиях, влияющих на форму.</span><span class="sxs-lookup"><span data-stu-id="f78a9-128">Registers a form viewer for notifications about events that affect the form.</span></span>  <br/> |
|[<span data-ttu-id="f78a9-129">Unadvise</span><span class="sxs-lookup"><span data-stu-id="f78a9-129">Unadvise</span></span>](imapiform-unadvise.md) <br/> |<span data-ttu-id="f78a9-130">Отменяет регистрацию уведомлений со средством просмотра форм, ранее установленным по телефону **Advise**.</span><span class="sxs-lookup"><span data-stu-id="f78a9-130">Cancels a registration for notifications with a form viewer previously established by calling **Advise**.</span></span>  <br/> |
|[<span data-ttu-id="f78a9-131">GetLastError</span><span class="sxs-lookup"><span data-stu-id="f78a9-131">GetLastError</span></span>](imapiform-getlasterror.md) <br/> |<span data-ttu-id="f78a9-132">Возвращает структуру [MAPIERROR, которая](mapierror.md) содержит сведения о предыдущей ошибке, произошедшей в объект формы.</span><span class="sxs-lookup"><span data-stu-id="f78a9-132">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f78a9-133">См. также</span><span class="sxs-lookup"><span data-stu-id="f78a9-133">See also</span></span>



[<span data-ttu-id="f78a9-134">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="f78a9-134">MAPI Interfaces</span></span>](mapi-interfaces.md)

