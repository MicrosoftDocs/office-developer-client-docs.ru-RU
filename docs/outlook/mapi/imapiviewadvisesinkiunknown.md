---
title: IMAPIViewAdviseSink IUnknown
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
ms.openlocfilehash: f16585a96164835784bfa1af3752bd652daf76e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809237"
---
# <a name="imapiviewadvisesink--iunknown"></a><span data-ttu-id="733f4-103">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="733f4-103">IMAPIViewAdviseSink : IUnknown</span></span>

  
  
<span data-ttu-id="733f4-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="733f4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="733f4-105">Получает уведомления от форм.</span><span class="sxs-lookup"><span data-stu-id="733f4-105">Receives notifications from forms.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="733f4-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="733f4-106">Header file:</span></span>  <br/> |<span data-ttu-id="733f4-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="733f4-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="733f4-108">Предоставляемые:</span><span class="sxs-lookup"><span data-stu-id="733f4-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="733f4-109">Просмотр рекомендаций объектов приемника</span><span class="sxs-lookup"><span data-stu-id="733f4-109">View advise sink objects</span></span>  <br/> |
|<span data-ttu-id="733f4-110">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="733f4-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="733f4-111">Средства просмотра формы</span><span class="sxs-lookup"><span data-stu-id="733f4-111">Form viewers</span></span>  <br/> |
|<span data-ttu-id="733f4-112">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="733f4-112">Called by:</span></span>  <br/> |<span data-ttu-id="733f4-113">Объекты формы</span><span class="sxs-lookup"><span data-stu-id="733f4-113">Form objects</span></span>  <br/> |
|<span data-ttu-id="733f4-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="733f4-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="733f4-115">IID_IMAPIViewAdviseSink</span><span class="sxs-lookup"><span data-stu-id="733f4-115">IID_IMAPIViewAdviseSink</span></span>  <br/> |
|<span data-ttu-id="733f4-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="733f4-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="733f4-117">LPMAPIVIEWADVISESINK</span><span class="sxs-lookup"><span data-stu-id="733f4-117">LPMAPIVIEWADVISESINK</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="733f4-118">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="733f4-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="733f4-119">Завершении</span><span class="sxs-lookup"><span data-stu-id="733f4-119">OnShutdown</span></span>](imapiviewadvisesink-onshutdown.md) <br/> |<span data-ttu-id="733f4-120">Уведомляет средство просмотра формы, что форма закрывается.</span><span class="sxs-lookup"><span data-stu-id="733f4-120">Notifies the form viewer that a form is being closed.</span></span>  <br/> |
|[<span data-ttu-id="733f4-121">OnNewMessage</span><span class="sxs-lookup"><span data-stu-id="733f4-121">OnNewMessage</span></span>](imapiviewadvisesink-onnewmessage.md) <br/> |<span data-ttu-id="733f4-122">Уведомляет средство просмотра формы после загрузки, что новое или существующее сообщение в форме.</span><span class="sxs-lookup"><span data-stu-id="733f4-122">Notifies the form viewer that either a new or an existing message has been loaded in a form.</span></span>  <br/> |
|[<span data-ttu-id="733f4-123">Печать (OnPrint)</span><span class="sxs-lookup"><span data-stu-id="733f4-123">OnPrint</span></span>](imapiviewadvisesink-onprint.md) <br/> |<span data-ttu-id="733f4-124">Уведомляет средство просмотра формы из состояния печати формы.</span><span class="sxs-lookup"><span data-stu-id="733f4-124">Notifies the form viewer of the printing status of a form.</span></span>  <br/> |
|[<span data-ttu-id="733f4-125">OnSubmitted</span><span class="sxs-lookup"><span data-stu-id="733f4-125">OnSubmitted</span></span>](imapiviewadvisesink-onsubmitted.md) <br/> |<span data-ttu-id="733f4-126">Уведомляет средство просмотра формы, что текущего сообщения были отправлены диспетчер очереди MAPI.</span><span class="sxs-lookup"><span data-stu-id="733f4-126">Notifies the form viewer that the current message has been submitted to MAPI spooler.</span></span>  <br/> |
|[<span data-ttu-id="733f4-127">OnSaved</span><span class="sxs-lookup"><span data-stu-id="733f4-127">OnSaved</span></span>](imapiviewadvisesink-onsaved.md) <br/> |<span data-ttu-id="733f4-128">Уведомляет средство просмотра формы, который был сохранен текущего сообщения в форме.</span><span class="sxs-lookup"><span data-stu-id="733f4-128">Notifies the form viewer that the current message in a form has been saved.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="733f4-129">См. также</span><span class="sxs-lookup"><span data-stu-id="733f4-129">See also</span></span>



[<span data-ttu-id="733f4-130">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="733f4-130">MAPI Interfaces</span></span>](mapi-interfaces.md)

