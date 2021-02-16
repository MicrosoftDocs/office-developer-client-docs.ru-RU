---
title: IMAPIMessageSite IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite
api_type:
- COM
ms.assetid: 883448f5-0d3f-486d-80a3-7b961c209cd0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: bf21ed1d41a61f600cfded777b699cf620c2e00f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433369"
---
# <a name="imapimessagesite--iunknown"></a><span data-ttu-id="961c3-103">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="961c3-103">IMAPIMessageSite : IUnknown</span></span>

  
  
<span data-ttu-id="961c3-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="961c3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="961c3-105">Управляет сообщениями и реализуется кодом средства просмотра форм (обычно клиентского приложения), который реагирует на такие манипуляции.</span><span class="sxs-lookup"><span data-stu-id="961c3-105">Manipulates messages and is implemented by the form viewer code (typically a client application) that responds to such manipulation.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="961c3-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="961c3-106">Header file:</span></span>  <br/> |<span data-ttu-id="961c3-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="961c3-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="961c3-108">Выставим:</span><span class="sxs-lookup"><span data-stu-id="961c3-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="961c3-109">Объекты сайта сообщений</span><span class="sxs-lookup"><span data-stu-id="961c3-109">Message site objects</span></span>  <br/> |
|<span data-ttu-id="961c3-110">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="961c3-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="961c3-111">Просмотр форм</span><span class="sxs-lookup"><span data-stu-id="961c3-111">Form viewers</span></span>  <br/> |
|<span data-ttu-id="961c3-112">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="961c3-112">Called by:</span></span>  <br/> |<span data-ttu-id="961c3-113">Объекты форм</span><span class="sxs-lookup"><span data-stu-id="961c3-113">Form objects</span></span>  <br/> |
|<span data-ttu-id="961c3-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="961c3-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="961c3-115">IID_IMAPIMessageSite</span><span class="sxs-lookup"><span data-stu-id="961c3-115">IID_IMAPIMessageSite</span></span>  <br/> |
|<span data-ttu-id="961c3-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="961c3-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="961c3-117">LPMAPIMESSAGESITE</span><span class="sxs-lookup"><span data-stu-id="961c3-117">LPMAPIMESSAGESITE</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="961c3-118">Порядок ветвей</span><span class="sxs-lookup"><span data-stu-id="961c3-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="961c3-119">GetSession</span><span class="sxs-lookup"><span data-stu-id="961c3-119">GetSession</span></span>](imapimessagesite-getsession.md) <br/> |<span data-ttu-id="961c3-120">Возвращает сеанс MAPI, в котором было создано или открыто текущее сообщение.</span><span class="sxs-lookup"><span data-stu-id="961c3-120">Returns the MAPI session in which the current message was created or opened.</span></span>  <br/> |
|[<span data-ttu-id="961c3-121">GetStore</span><span class="sxs-lookup"><span data-stu-id="961c3-121">GetStore</span></span>](imapimessagesite-getstore.md) <br/> |<span data-ttu-id="961c3-122">Возвращает хранилище сообщений, которое содержит текущее сообщение, если такое хранилище существует.</span><span class="sxs-lookup"><span data-stu-id="961c3-122">Returns the message store that contains the current message, if such a store exists.</span></span>  <br/> |
|[<span data-ttu-id="961c3-123">GetFolder</span><span class="sxs-lookup"><span data-stu-id="961c3-123">GetFolder</span></span>](imapimessagesite-getfolder.md) <br/> |<span data-ttu-id="961c3-124">Возвращает папку, в которой было создано или открыто текущее сообщение, если такая папка существует.</span><span class="sxs-lookup"><span data-stu-id="961c3-124">Returns the folder in which the current message was created or opened, if such a folder exists.</span></span>  <br/> |
|[<span data-ttu-id="961c3-125">GetMessage</span><span class="sxs-lookup"><span data-stu-id="961c3-125">GetMessage</span></span>](imapimessagesite-getmessage.md) <br/> |<span data-ttu-id="961c3-126">Возвращает текущее сообщение.</span><span class="sxs-lookup"><span data-stu-id="961c3-126">Returns the current message.</span></span>  <br/> |
|[<span data-ttu-id="961c3-127">GetFormManager</span><span class="sxs-lookup"><span data-stu-id="961c3-127">GetFormManager</span></span>](imapimessagesite-getformmanager.md) <br/> |<span data-ttu-id="961c3-128">Возвращает интерфейс диспетчера форм, который сервер форм может использовать для открытия другого сервера форм.</span><span class="sxs-lookup"><span data-stu-id="961c3-128">Returns a form manager interface, which a form server can use to open another form server.</span></span>  <br/> |
|[<span data-ttu-id="961c3-129">NewMessage</span><span class="sxs-lookup"><span data-stu-id="961c3-129">NewMessage</span></span>](imapimessagesite-newmessage.md) <br/> |<span data-ttu-id="961c3-130">Создает новое сообщение.</span><span class="sxs-lookup"><span data-stu-id="961c3-130">Creates a new message.</span></span>  <br/> |
|[<span data-ttu-id="961c3-131">CopyMessage</span><span class="sxs-lookup"><span data-stu-id="961c3-131">CopyMessage</span></span>](imapimessagesite-copymessage.md) <br/> |<span data-ttu-id="961c3-132">Копирует текущее сообщение в папку.</span><span class="sxs-lookup"><span data-stu-id="961c3-132">Copies the current message to a folder.</span></span>  <br/> |
|[<span data-ttu-id="961c3-133">MoveMessage</span><span class="sxs-lookup"><span data-stu-id="961c3-133">MoveMessage</span></span>](imapimessagesite-movemessage.md) <br/> |<span data-ttu-id="961c3-134">Перемещает текущее сообщение в папку.</span><span class="sxs-lookup"><span data-stu-id="961c3-134">Moves the current message to a folder.</span></span>  <br/> |
|[<span data-ttu-id="961c3-135">DeleteMessage</span><span class="sxs-lookup"><span data-stu-id="961c3-135">DeleteMessage</span></span>](imapimessagesite-deletemessage.md) <br/> |<span data-ttu-id="961c3-136">Удаляет текущее сообщение.</span><span class="sxs-lookup"><span data-stu-id="961c3-136">Deletes the current message.</span></span>  <br/> |
|[<span data-ttu-id="961c3-137">SaveMessage</span><span class="sxs-lookup"><span data-stu-id="961c3-137">SaveMessage</span></span>](imapimessagesite-savemessage.md) <br/> |<span data-ttu-id="961c3-138">Запрашивает, чтобы текущее сообщение было сохранено.</span><span class="sxs-lookup"><span data-stu-id="961c3-138">Requests that the current message be saved.</span></span>  <br/> |
|[<span data-ttu-id="961c3-139">SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="961c3-139">SubmitMessage</span></span>](imapimessagesite-submitmessage.md) <br/> |<span data-ttu-id="961c3-140">Запрашивает, чтобы текущее сообщение было в очереди для доставки.</span><span class="sxs-lookup"><span data-stu-id="961c3-140">Requests that the current message be queued for delivery.</span></span>  <br/> |
|[<span data-ttu-id="961c3-141">GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="961c3-141">GetSiteStatus</span></span>](imapimessagesite-getsitestatus.md) <br/> |<span data-ttu-id="961c3-142">Возвращает сведения из объекта сайта сообщения о возможностях сайта сообщений для текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="961c3-142">Returns information from a message site object about the message site's capabilities for the current message.</span></span>  <br/> |
|[<span data-ttu-id="961c3-143">GetLastError</span><span class="sxs-lookup"><span data-stu-id="961c3-143">GetLastError</span></span>](imapimessagesite-getlasterror.md) <br/> |<span data-ttu-id="961c3-144">Возвращает структуру [MAPIERROR, которая](mapierror.md) содержит сведения о предыдущей ошибке, которая произошла в объекте сайта сообщения.</span><span class="sxs-lookup"><span data-stu-id="961c3-144">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the message site object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="961c3-145">См. также</span><span class="sxs-lookup"><span data-stu-id="961c3-145">See also</span></span>



[<span data-ttu-id="961c3-146">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="961c3-146">MAPI Interfaces</span></span>](mapi-interfaces.md)

