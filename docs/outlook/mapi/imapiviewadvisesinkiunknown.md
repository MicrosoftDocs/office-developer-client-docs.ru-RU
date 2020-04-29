---
title: Имапивиевадвисесинк IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink
api_type:
- COM
ms.assetid: 1231391d-803a-4b41-b252-4d986f99361a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 70f61fe33baa7870a58c4cbc7d75e0df119b5b1a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429420"
---
# <a name="imapiviewadvisesink--iunknown"></a><span data-ttu-id="5bee0-103">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5bee0-103">IMAPIViewAdviseSink : IUnknown</span></span>

  
  
<span data-ttu-id="5bee0-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5bee0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5bee0-105">Получает уведомления от форм.</span><span class="sxs-lookup"><span data-stu-id="5bee0-105">Receives notifications from forms.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5bee0-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="5bee0-106">Header file:</span></span>  <br/> |<span data-ttu-id="5bee0-107">Мапиформ. h</span><span class="sxs-lookup"><span data-stu-id="5bee0-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="5bee0-108">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="5bee0-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="5bee0-109">Просмотр объектов приемника уведомлений</span><span class="sxs-lookup"><span data-stu-id="5bee0-109">View advise sink objects</span></span>  <br/> |
|<span data-ttu-id="5bee0-110">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="5bee0-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="5bee0-111">Средства просмотра форм</span><span class="sxs-lookup"><span data-stu-id="5bee0-111">Form viewers</span></span>  <br/> |
|<span data-ttu-id="5bee0-112">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="5bee0-112">Called by:</span></span>  <br/> |<span data-ttu-id="5bee0-113">Объекты форм</span><span class="sxs-lookup"><span data-stu-id="5bee0-113">Form objects</span></span>  <br/> |
|<span data-ttu-id="5bee0-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="5bee0-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="5bee0-115">IID_IMAPIViewAdviseSink</span><span class="sxs-lookup"><span data-stu-id="5bee0-115">IID_IMAPIViewAdviseSink</span></span>  <br/> |
|<span data-ttu-id="5bee0-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="5bee0-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="5bee0-117">лпмапивиевадвисесинк</span><span class="sxs-lookup"><span data-stu-id="5bee0-117">LPMAPIVIEWADVISESINK</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="5bee0-118">Заказ vtable</span><span class="sxs-lookup"><span data-stu-id="5bee0-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="5bee0-119">OnShutdown</span><span class="sxs-lookup"><span data-stu-id="5bee0-119">OnShutdown</span></span>](imapiviewadvisesink-onshutdown.md) <br/> |<span data-ttu-id="5bee0-120">Уведомляет средство просмотра форм о том, что форма закрывается.</span><span class="sxs-lookup"><span data-stu-id="5bee0-120">Notifies the form viewer that a form is being closed.</span></span>  <br/> |
|[<span data-ttu-id="5bee0-121">онневмессаже</span><span class="sxs-lookup"><span data-stu-id="5bee0-121">OnNewMessage</span></span>](imapiviewadvisesink-onnewmessage.md) <br/> |<span data-ttu-id="5bee0-122">Уведомляет средство просмотра форм о том, что в форме загружено новое или существующее сообщение.</span><span class="sxs-lookup"><span data-stu-id="5bee0-122">Notifies the form viewer that either a new or an existing message has been loaded in a form.</span></span>  <br/> |
|[<span data-ttu-id="5bee0-123">OnPrint</span><span class="sxs-lookup"><span data-stu-id="5bee0-123">OnPrint</span></span>](imapiviewadvisesink-onprint.md) <br/> |<span data-ttu-id="5bee0-124">Уведомляет средство просмотра форм о состоянии печати формы.</span><span class="sxs-lookup"><span data-stu-id="5bee0-124">Notifies the form viewer of the printing status of a form.</span></span>  <br/> |
|[<span data-ttu-id="5bee0-125">Onsubmittedо</span><span class="sxs-lookup"><span data-stu-id="5bee0-125">OnSubmitted</span></span>](imapiviewadvisesink-onsubmitted.md) <br/> |<span data-ttu-id="5bee0-126">Уведомляет средство просмотра форм о том, что текущее сообщение было отправлено в Диспетчер очереди MAPI.</span><span class="sxs-lookup"><span data-stu-id="5bee0-126">Notifies the form viewer that the current message has been submitted to MAPI spooler.</span></span>  <br/> |
|[<span data-ttu-id="5bee0-127">Onsaved</span><span class="sxs-lookup"><span data-stu-id="5bee0-127">OnSaved</span></span>](imapiviewadvisesink-onsaved.md) <br/> |<span data-ttu-id="5bee0-128">Уведомляет средство просмотра форм о том, что текущее сообщение сохранено в форме.</span><span class="sxs-lookup"><span data-stu-id="5bee0-128">Notifies the form viewer that the current message in a form has been saved.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5bee0-129">См. также</span><span class="sxs-lookup"><span data-stu-id="5bee0-129">See also</span></span>



[<span data-ttu-id="5bee0-130">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="5bee0-130">MAPI Interfaces</span></span>](mapi-interfaces.md)

