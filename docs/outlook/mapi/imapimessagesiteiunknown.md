---
title: Имапимессажесите IUnknown
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
# <a name="imapimessagesite--iunknown"></a><span data-ttu-id="7fcec-103">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7fcec-103">IMAPIMessageSite : IUnknown</span></span>

  
  
<span data-ttu-id="7fcec-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7fcec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7fcec-105">Управляет сообщениями и реализуется с помощью кода средства просмотра форм (как правило, клиентского приложения), который отвечает на такую манипуляцию.</span><span class="sxs-lookup"><span data-stu-id="7fcec-105">Manipulates messages and is implemented by the form viewer code (typically a client application) that responds to such manipulation.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7fcec-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="7fcec-106">Header file:</span></span>  <br/> |<span data-ttu-id="7fcec-107">Мапиформ. h</span><span class="sxs-lookup"><span data-stu-id="7fcec-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="7fcec-108">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="7fcec-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="7fcec-109">Объекты сайта сообщений</span><span class="sxs-lookup"><span data-stu-id="7fcec-109">Message site objects</span></span>  <br/> |
|<span data-ttu-id="7fcec-110">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="7fcec-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="7fcec-111">Средства просмотра форм</span><span class="sxs-lookup"><span data-stu-id="7fcec-111">Form viewers</span></span>  <br/> |
|<span data-ttu-id="7fcec-112">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="7fcec-112">Called by:</span></span>  <br/> |<span data-ttu-id="7fcec-113">Объекты форм</span><span class="sxs-lookup"><span data-stu-id="7fcec-113">Form objects</span></span>  <br/> |
|<span data-ttu-id="7fcec-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="7fcec-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="7fcec-115">IID_IMAPIMessageSite</span><span class="sxs-lookup"><span data-stu-id="7fcec-115">IID_IMAPIMessageSite</span></span>  <br/> |
|<span data-ttu-id="7fcec-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="7fcec-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="7fcec-117">лпмапимессажесите</span><span class="sxs-lookup"><span data-stu-id="7fcec-117">LPMAPIMESSAGESITE</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="7fcec-118">Заказ vtable</span><span class="sxs-lookup"><span data-stu-id="7fcec-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="7fcec-119">Сеансы.</span><span class="sxs-lookup"><span data-stu-id="7fcec-119">GetSession</span></span>](imapimessagesite-getsession.md) <br/> |<span data-ttu-id="7fcec-120">Возвращает сеанс MAPI, в котором было создано или открыто текущее сообщение.</span><span class="sxs-lookup"><span data-stu-id="7fcec-120">Returns the MAPI session in which the current message was created or opened.</span></span>  <br/> |
|[<span data-ttu-id="7fcec-121">DataStore</span><span class="sxs-lookup"><span data-stu-id="7fcec-121">GetStore</span></span>](imapimessagesite-getstore.md) <br/> |<span data-ttu-id="7fcec-122">Возвращает хранилище сообщений, содержащее текущее сообщение, если такое хранилище существует.</span><span class="sxs-lookup"><span data-stu-id="7fcec-122">Returns the message store that contains the current message, if such a store exists.</span></span>  <br/> |
|[<span data-ttu-id="7fcec-123">GetFolder</span><span class="sxs-lookup"><span data-stu-id="7fcec-123">GetFolder</span></span>](imapimessagesite-getfolder.md) <br/> |<span data-ttu-id="7fcec-124">Возвращает папку, в которой было создано или открыто текущее сообщение, если такая папка существует.</span><span class="sxs-lookup"><span data-stu-id="7fcec-124">Returns the folder in which the current message was created or opened, if such a folder exists.</span></span>  <br/> |
|[<span data-ttu-id="7fcec-125">Сообщение о доходе</span><span class="sxs-lookup"><span data-stu-id="7fcec-125">GetMessage</span></span>](imapimessagesite-getmessage.md) <br/> |<span data-ttu-id="7fcec-126">Возвращает текущее сообщение.</span><span class="sxs-lookup"><span data-stu-id="7fcec-126">Returns the current message.</span></span>  <br/> |
|[<span data-ttu-id="7fcec-127">жетформманажер</span><span class="sxs-lookup"><span data-stu-id="7fcec-127">GetFormManager</span></span>](imapimessagesite-getformmanager.md) <br/> |<span data-ttu-id="7fcec-128">Возвращает интерфейс диспетчера форм, который сервер форм может использовать для открытия другого сервера форм.</span><span class="sxs-lookup"><span data-stu-id="7fcec-128">Returns a form manager interface, which a form server can use to open another form server.</span></span>  <br/> |
|[<span data-ttu-id="7fcec-129">NewMessage</span><span class="sxs-lookup"><span data-stu-id="7fcec-129">NewMessage</span></span>](imapimessagesite-newmessage.md) <br/> |<span data-ttu-id="7fcec-130">Создает новое сообщение.</span><span class="sxs-lookup"><span data-stu-id="7fcec-130">Creates a new message.</span></span>  <br/> |
|[<span data-ttu-id="7fcec-131">копимессаже</span><span class="sxs-lookup"><span data-stu-id="7fcec-131">CopyMessage</span></span>](imapimessagesite-copymessage.md) <br/> |<span data-ttu-id="7fcec-132">Копирует текущее сообщение в папку.</span><span class="sxs-lookup"><span data-stu-id="7fcec-132">Copies the current message to a folder.</span></span>  <br/> |
|[<span data-ttu-id="7fcec-133">мовемессаже</span><span class="sxs-lookup"><span data-stu-id="7fcec-133">MoveMessage</span></span>](imapimessagesite-movemessage.md) <br/> |<span data-ttu-id="7fcec-134">Перемещает текущее сообщение в папку.</span><span class="sxs-lookup"><span data-stu-id="7fcec-134">Moves the current message to a folder.</span></span>  <br/> |
|[<span data-ttu-id="7fcec-135">DeleteMessage</span><span class="sxs-lookup"><span data-stu-id="7fcec-135">DeleteMessage</span></span>](imapimessagesite-deletemessage.md) <br/> |<span data-ttu-id="7fcec-136">Удаляет текущее сообщение.</span><span class="sxs-lookup"><span data-stu-id="7fcec-136">Deletes the current message.</span></span>  <br/> |
|[<span data-ttu-id="7fcec-137">савемессаже</span><span class="sxs-lookup"><span data-stu-id="7fcec-137">SaveMessage</span></span>](imapimessagesite-savemessage.md) <br/> |<span data-ttu-id="7fcec-138">Запрашивает сохранение текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="7fcec-138">Requests that the current message be saved.</span></span>  <br/> |
|[<span data-ttu-id="7fcec-139">субмитмессаже</span><span class="sxs-lookup"><span data-stu-id="7fcec-139">SubmitMessage</span></span>](imapimessagesite-submitmessage.md) <br/> |<span data-ttu-id="7fcec-140">Запрашивает доставку текущего сообщения в очередь на доставку.</span><span class="sxs-lookup"><span data-stu-id="7fcec-140">Requests that the current message be queued for delivery.</span></span>  <br/> |
|[<span data-ttu-id="7fcec-141">жетситестатус</span><span class="sxs-lookup"><span data-stu-id="7fcec-141">GetSiteStatus</span></span>](imapimessagesite-getsitestatus.md) <br/> |<span data-ttu-id="7fcec-142">Возвращает сведения из объекта сайта сообщения о возможностях сайта сообщения для текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="7fcec-142">Returns information from a message site object about the message site's capabilities for the current message.</span></span>  <br/> |
|[<span data-ttu-id="7fcec-143">GetLastError</span><span class="sxs-lookup"><span data-stu-id="7fcec-143">GetLastError</span></span>](imapimessagesite-getlasterror.md) <br/> |<span data-ttu-id="7fcec-144">Возвращает структуру [мапиеррор](mapierror.md) , которая содержит сведения о предыдущей ошибке, возникшей в объекте сайта сообщения.</span><span class="sxs-lookup"><span data-stu-id="7fcec-144">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the message site object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7fcec-145">См. также</span><span class="sxs-lookup"><span data-stu-id="7fcec-145">See also</span></span>



[<span data-ttu-id="7fcec-146">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="7fcec-146">MAPI Interfaces</span></span>](mapi-interfaces.md)

