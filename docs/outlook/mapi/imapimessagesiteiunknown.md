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
ms.openlocfilehash: cffa3024b8533f07f8f76fa5bbac219e23d61bdb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589506"
---
# <a name="imapimessagesite--iunknown"></a><span data-ttu-id="e7b50-103">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e7b50-103">IMAPIMessageSite : IUnknown</span></span>

  
  
<span data-ttu-id="e7b50-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e7b50-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e7b50-105">Управляет сообщений и реализуется код средства просмотра формы (обычно клиентское приложение), которая отвечает на такой обработки.</span><span class="sxs-lookup"><span data-stu-id="e7b50-105">Manipulates messages and is implemented by the form viewer code (typically a client application) that responds to such manipulation.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e7b50-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="e7b50-106">Header file:</span></span>  <br/> |<span data-ttu-id="e7b50-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="e7b50-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="e7b50-108">Предоставляемые:</span><span class="sxs-lookup"><span data-stu-id="e7b50-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="e7b50-109">Объекты сайта сообщения</span><span class="sxs-lookup"><span data-stu-id="e7b50-109">Message site objects</span></span>  <br/> |
|<span data-ttu-id="e7b50-110">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="e7b50-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="e7b50-111">Средства просмотра формы</span><span class="sxs-lookup"><span data-stu-id="e7b50-111">Form viewers</span></span>  <br/> |
|<span data-ttu-id="e7b50-112">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="e7b50-112">Called by:</span></span>  <br/> |<span data-ttu-id="e7b50-113">Объекты формы</span><span class="sxs-lookup"><span data-stu-id="e7b50-113">Form objects</span></span>  <br/> |
|<span data-ttu-id="e7b50-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="e7b50-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="e7b50-115">IID_IMAPIMessageSite</span><span class="sxs-lookup"><span data-stu-id="e7b50-115">IID_IMAPIMessageSite</span></span>  <br/> |
|<span data-ttu-id="e7b50-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="e7b50-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="e7b50-117">LPMAPIMESSAGESITE</span><span class="sxs-lookup"><span data-stu-id="e7b50-117">LPMAPIMESSAGESITE</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="e7b50-118">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="e7b50-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="e7b50-119">GetSession</span><span class="sxs-lookup"><span data-stu-id="e7b50-119">GetSession</span></span>](imapimessagesite-getsession.md) <br/> |<span data-ttu-id="e7b50-120">Возвращает сеанса MAPI, в которой была создана или открыта текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="e7b50-120">Returns the MAPI session in which the current message was created or opened.</span></span>  <br/> |
|[<span data-ttu-id="e7b50-121">GetStore</span><span class="sxs-lookup"><span data-stu-id="e7b50-121">GetStore</span></span>](imapimessagesite-getstore.md) <br/> |<span data-ttu-id="e7b50-122">Если такие хранилища возвращает хранилище сообщение, содержащее текущее сообщение.</span><span class="sxs-lookup"><span data-stu-id="e7b50-122">Returns the message store that contains the current message, if such a store exists.</span></span>  <br/> |
|[<span data-ttu-id="e7b50-123">GetFolder</span><span class="sxs-lookup"><span data-stu-id="e7b50-123">GetFolder</span></span>](imapimessagesite-getfolder.md) <br/> |<span data-ttu-id="e7b50-124">Возвращает папку, в которой была создана или открыта, текущего сообщения, если такая папка существует.</span><span class="sxs-lookup"><span data-stu-id="e7b50-124">Returns the folder in which the current message was created or opened, if such a folder exists.</span></span>  <br/> |
|[<span data-ttu-id="e7b50-125">GetMessage</span><span class="sxs-lookup"><span data-stu-id="e7b50-125">GetMessage</span></span>](imapimessagesite-getmessage.md) <br/> |<span data-ttu-id="e7b50-126">Возвращает текущее сообщение.</span><span class="sxs-lookup"><span data-stu-id="e7b50-126">Returns the current message.</span></span>  <br/> |
|[<span data-ttu-id="e7b50-127">GetFormManager</span><span class="sxs-lookup"><span data-stu-id="e7b50-127">GetFormManager</span></span>](imapimessagesite-getformmanager.md) <br/> |<span data-ttu-id="e7b50-128">Возвращает интерфейс диспетчера формы, который сервера форм можно использовать для открытия другой сервер формы.</span><span class="sxs-lookup"><span data-stu-id="e7b50-128">Returns a form manager interface, which a form server can use to open another form server.</span></span>  <br/> |
|[<span data-ttu-id="e7b50-129">NewMessage</span><span class="sxs-lookup"><span data-stu-id="e7b50-129">NewMessage</span></span>](imapimessagesite-newmessage.md) <br/> |<span data-ttu-id="e7b50-130">Создает новое сообщение.</span><span class="sxs-lookup"><span data-stu-id="e7b50-130">Creates a new message.</span></span>  <br/> |
|[<span data-ttu-id="e7b50-131">CopyMessage</span><span class="sxs-lookup"><span data-stu-id="e7b50-131">CopyMessage</span></span>](imapimessagesite-copymessage.md) <br/> |<span data-ttu-id="e7b50-132">Копирует текущего сообщения в папку.</span><span class="sxs-lookup"><span data-stu-id="e7b50-132">Copies the current message to a folder.</span></span>  <br/> |
|[<span data-ttu-id="e7b50-133">MoveMessage</span><span class="sxs-lookup"><span data-stu-id="e7b50-133">MoveMessage</span></span>](imapimessagesite-movemessage.md) <br/> |<span data-ttu-id="e7b50-134">Перемещает текущего сообщения в папку.</span><span class="sxs-lookup"><span data-stu-id="e7b50-134">Moves the current message to a folder.</span></span>  <br/> |
|[<span data-ttu-id="e7b50-135">DeleteMessage</span><span class="sxs-lookup"><span data-stu-id="e7b50-135">DeleteMessage</span></span>](imapimessagesite-deletemessage.md) <br/> |<span data-ttu-id="e7b50-136">Удаление текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="e7b50-136">Deletes the current message.</span></span>  <br/> |
|[<span data-ttu-id="e7b50-137">SaveMessage</span><span class="sxs-lookup"><span data-stu-id="e7b50-137">SaveMessage</span></span>](imapimessagesite-savemessage.md) <br/> |<span data-ttu-id="e7b50-138">Запросы, которые сохранены текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="e7b50-138">Requests that the current message be saved.</span></span>  <br/> |
|[<span data-ttu-id="e7b50-139">SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="e7b50-139">SubmitMessage</span></span>](imapimessagesite-submitmessage.md) <br/> |<span data-ttu-id="e7b50-140">Запросы в текущем сообщении очереди для доставки.</span><span class="sxs-lookup"><span data-stu-id="e7b50-140">Requests that the current message be queued for delivery.</span></span>  <br/> |
|[<span data-ttu-id="e7b50-141">GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="e7b50-141">GetSiteStatus</span></span>](imapimessagesite-getsitestatus.md) <br/> |<span data-ttu-id="e7b50-142">Возвращает сведения из объекта сайта сообщения о сообщении возможности веб-узла для текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="e7b50-142">Returns information from a message site object about the message site's capabilities for the current message.</span></span>  <br/> |
|[<span data-ttu-id="e7b50-143">GetLastError</span><span class="sxs-lookup"><span data-stu-id="e7b50-143">GetLastError</span></span>](imapimessagesite-getlasterror.md) <br/> |<span data-ttu-id="e7b50-144">Возвращает структуру [MAPIERROR](mapierror.md) , которая содержит сведения об ошибке предыдущей появление сообщения объект сайта.</span><span class="sxs-lookup"><span data-stu-id="e7b50-144">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the message site object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e7b50-145">См. также</span><span class="sxs-lookup"><span data-stu-id="e7b50-145">See also</span></span>



[<span data-ttu-id="e7b50-146">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="e7b50-146">MAPI Interfaces</span></span>](mapi-interfaces.md)

