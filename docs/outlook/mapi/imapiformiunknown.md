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
ms.openlocfilehash: fce8bc45d5cc87c238288653ab989b62076ad451
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808930"
---
# <a name="imapiform--iunknown"></a><span data-ttu-id="550b4-103">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="550b4-103">IMAPIForm : IUnknown</span></span>

  
  
<span data-ttu-id="550b4-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="550b4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="550b4-105">Включение средств просмотра формы для работы с контекстах представления формы и формы уведомлений, для выполнения команд формы и завершение работы форм.</span><span class="sxs-lookup"><span data-stu-id="550b4-105">Enables form viewers to work with form view contexts and form notification, to perform form verbs, and to shut down forms.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="550b4-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="550b4-106">Header file:</span></span>  <br/> |<span data-ttu-id="550b4-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="550b4-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="550b4-108">Предоставляемые:</span><span class="sxs-lookup"><span data-stu-id="550b4-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="550b4-109">Объекты формы</span><span class="sxs-lookup"><span data-stu-id="550b4-109">Form objects</span></span>  <br/> |
|<span data-ttu-id="550b4-110">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="550b4-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="550b4-111">Серверы формы</span><span class="sxs-lookup"><span data-stu-id="550b4-111">Form servers</span></span>  <br/> |
|<span data-ttu-id="550b4-112">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="550b4-112">Called by:</span></span>  <br/> |<span data-ttu-id="550b4-113">Средства просмотра формы</span><span class="sxs-lookup"><span data-stu-id="550b4-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="550b4-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="550b4-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="550b4-115">IID_IMAPIForm</span><span class="sxs-lookup"><span data-stu-id="550b4-115">IID_IMAPIForm</span></span>  <br/> |
|<span data-ttu-id="550b4-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="550b4-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="550b4-117">LPMAPIFORM</span><span class="sxs-lookup"><span data-stu-id="550b4-117">LPMAPIFORM</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="550b4-118">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="550b4-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="550b4-119">SetViewContext</span><span class="sxs-lookup"><span data-stu-id="550b4-119">SetViewContext</span></span>](imapiform-setviewcontext.md) <br/> |<span data-ttu-id="550b4-120">Устанавливает контекст представления для формы.</span><span class="sxs-lookup"><span data-stu-id="550b4-120">Establishes a view context for the form.</span></span>  <br/> |
|[<span data-ttu-id="550b4-121">GetViewContext</span><span class="sxs-lookup"><span data-stu-id="550b4-121">GetViewContext</span></span>](imapiform-getviewcontext.md) <br/> |<span data-ttu-id="550b4-122">Возвращает текущий контекст представления для формы.</span><span class="sxs-lookup"><span data-stu-id="550b4-122">Returns the current view context for the form.</span></span>  <br/> |
|[<span data-ttu-id="550b4-123">ShutdownForm</span><span class="sxs-lookup"><span data-stu-id="550b4-123">ShutdownForm</span></span>](imapiform-shutdownform.md) <br/> |<span data-ttu-id="550b4-124">Закрывает форму.</span><span class="sxs-lookup"><span data-stu-id="550b4-124">Closes the form.</span></span>  <br/> |
|[<span data-ttu-id="550b4-125">DoVerb</span><span class="sxs-lookup"><span data-stu-id="550b4-125">DoVerb</span></span>](imapiform-doverb.md) <br/> |<span data-ttu-id="550b4-126">Запросы, формы выполнить все задачи связывается с определенным команды.</span><span class="sxs-lookup"><span data-stu-id="550b4-126">Requests that the form perform whatever tasks it associates with a specific verb.</span></span>  <br/> |
|[<span data-ttu-id="550b4-127">Уведомить</span><span class="sxs-lookup"><span data-stu-id="550b4-127">Advise</span></span>](imapiform-advise.md) <br/> |<span data-ttu-id="550b4-128">Регистрирует просмотра формы для уведомлений о событиях, которые влияют на форме.</span><span class="sxs-lookup"><span data-stu-id="550b4-128">Registers a form viewer for notifications about events that affect the form.</span></span>  <br/> |
|[<span data-ttu-id="550b4-129">Unadvise</span><span class="sxs-lookup"><span data-stu-id="550b4-129">Unadvise</span></span>](imapiform-unadvise.md) <br/> |<span data-ttu-id="550b4-130">Отменяет регистрацию для уведомлений с помощью средства просмотра формы, ранее установленные путем вызова **уведомлений**.</span><span class="sxs-lookup"><span data-stu-id="550b4-130">Cancels a registration for notifications with a form viewer previously established by calling **Advise**.</span></span>  <br/> |
|[<span data-ttu-id="550b4-131">GetLastError</span><span class="sxs-lookup"><span data-stu-id="550b4-131">GetLastError</span></span>](imapiform-getlasterror.md) <br/> |<span data-ttu-id="550b4-132">Возвращает структуру [MAPIERROR](mapierror.md) , содержащий сведения об ошибке предыдущей появление объекта формы.</span><span class="sxs-lookup"><span data-stu-id="550b4-132">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="550b4-133">См. также</span><span class="sxs-lookup"><span data-stu-id="550b4-133">See also</span></span>



[<span data-ttu-id="550b4-134">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="550b4-134">MAPI Interfaces</span></span>](mapi-interfaces.md)

