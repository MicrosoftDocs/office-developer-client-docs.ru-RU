---
title: Имапиформ IUnknown
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321779"
---
# <a name="imapiform--iunknown"></a><span data-ttu-id="2a9d0-103">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2a9d0-103">IMAPIForm : IUnknown</span></span>

  
  
<span data-ttu-id="2a9d0-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2a9d0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2a9d0-105">Позволяет средствам просмотра форм работать с контекстами представления формы и уведомлениями форм, для выполнения команд форм и для завершения работы форм.</span><span class="sxs-lookup"><span data-stu-id="2a9d0-105">Enables form viewers to work with form view contexts and form notification, to perform form verbs, and to shut down forms.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2a9d0-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="2a9d0-106">Header file:</span></span>  <br/> |<span data-ttu-id="2a9d0-107">Мапиформ. h</span><span class="sxs-lookup"><span data-stu-id="2a9d0-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="2a9d0-108">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="2a9d0-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="2a9d0-109">Объекты форм</span><span class="sxs-lookup"><span data-stu-id="2a9d0-109">Form objects</span></span>  <br/> |
|<span data-ttu-id="2a9d0-110">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="2a9d0-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="2a9d0-111">Серверы форм</span><span class="sxs-lookup"><span data-stu-id="2a9d0-111">Form servers</span></span>  <br/> |
|<span data-ttu-id="2a9d0-112">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="2a9d0-112">Called by:</span></span>  <br/> |<span data-ttu-id="2a9d0-113">Средства просмотра форм</span><span class="sxs-lookup"><span data-stu-id="2a9d0-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="2a9d0-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="2a9d0-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="2a9d0-115">Иид_имапиформ</span><span class="sxs-lookup"><span data-stu-id="2a9d0-115">IID_IMAPIForm</span></span>  <br/> |
|<span data-ttu-id="2a9d0-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="2a9d0-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="2a9d0-117">ЛПМАПИФОРМ</span><span class="sxs-lookup"><span data-stu-id="2a9d0-117">LPMAPIFORM</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="2a9d0-118">Заказ vtable</span><span class="sxs-lookup"><span data-stu-id="2a9d0-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="2a9d0-119">Сетвиевконтекст</span><span class="sxs-lookup"><span data-stu-id="2a9d0-119">SetViewContext</span></span>](imapiform-setviewcontext.md) <br/> |<span data-ttu-id="2a9d0-120">Создает контекст представления для формы.</span><span class="sxs-lookup"><span data-stu-id="2a9d0-120">Establishes a view context for the form.</span></span>  <br/> |
|[<span data-ttu-id="2a9d0-121">Жетвиевконтекст</span><span class="sxs-lookup"><span data-stu-id="2a9d0-121">GetViewContext</span></span>](imapiform-getviewcontext.md) <br/> |<span data-ttu-id="2a9d0-122">Возвращает текущий контекст представления для формы.</span><span class="sxs-lookup"><span data-stu-id="2a9d0-122">Returns the current view context for the form.</span></span>  <br/> |
|[<span data-ttu-id="2a9d0-123">Шутдовнформ</span><span class="sxs-lookup"><span data-stu-id="2a9d0-123">ShutdownForm</span></span>](imapiform-shutdownform.md) <br/> |<span data-ttu-id="2a9d0-124">Закрывает форму.</span><span class="sxs-lookup"><span data-stu-id="2a9d0-124">Closes the form.</span></span>  <br/> |
|[<span data-ttu-id="2a9d0-125">DoVerb</span><span class="sxs-lookup"><span data-stu-id="2a9d0-125">DoVerb</span></span>](imapiform-doverb.md) <br/> |<span data-ttu-id="2a9d0-126">ЗаПрашивает выполнение формой любых задач, которые она связывает с определенной командой.</span><span class="sxs-lookup"><span data-stu-id="2a9d0-126">Requests that the form perform whatever tasks it associates with a specific verb.</span></span>  <br/> |
|[<span data-ttu-id="2a9d0-127">Рекомендуем</span><span class="sxs-lookup"><span data-stu-id="2a9d0-127">Advise</span></span>](imapiform-advise.md) <br/> |<span data-ttu-id="2a9d0-128">Регистрирует средство просмотра форм для уведомлений о событиях, влияющих на форму.</span><span class="sxs-lookup"><span data-stu-id="2a9d0-128">Registers a form viewer for notifications about events that affect the form.</span></span>  <br/> |
|[<span data-ttu-id="2a9d0-129">Unadvise</span><span class="sxs-lookup"><span data-stu-id="2a9d0-129">Unadvise</span></span>](imapiform-unadvise.md) <br/> |<span data-ttu-id="2a9d0-130">ОтМеняет регистрацию для уведомлений с помощью средства просмотра форм, предварительно установленного с помощью метода **advise**.</span><span class="sxs-lookup"><span data-stu-id="2a9d0-130">Cancels a registration for notifications with a form viewer previously established by calling **Advise**.</span></span>  <br/> |
|[<span data-ttu-id="2a9d0-131">GetLastError</span><span class="sxs-lookup"><span data-stu-id="2a9d0-131">GetLastError</span></span>](imapiform-getlasterror.md) <br/> |<span data-ttu-id="2a9d0-132">Возвращает структуру [мапиеррор](mapierror.md) , которая содержит сведения о предыдущей ошибке, возникшей в объекте Form.</span><span class="sxs-lookup"><span data-stu-id="2a9d0-132">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2a9d0-133">См. также</span><span class="sxs-lookup"><span data-stu-id="2a9d0-133">See also</span></span>



[<span data-ttu-id="2a9d0-134">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="2a9d0-134">MAPI Interfaces</span></span>](mapi-interfaces.md)

