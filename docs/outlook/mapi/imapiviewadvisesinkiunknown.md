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
ms.openlocfilehash: 157703fc9702bb954b4a5c570fc3d5c045e181cc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567190"
---
# <a name="imapiviewadvisesink--iunknown"></a><span data-ttu-id="61924-103">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="61924-103">IMAPIViewAdviseSink : IUnknown</span></span>

  
  
<span data-ttu-id="61924-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="61924-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="61924-105">Получает уведомления от форм.</span><span class="sxs-lookup"><span data-stu-id="61924-105">Receives notifications from forms.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="61924-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="61924-106">Header file:</span></span>  <br/> |<span data-ttu-id="61924-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="61924-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="61924-108">Предоставляемые:</span><span class="sxs-lookup"><span data-stu-id="61924-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="61924-109">Просмотр рекомендаций объектов приемника</span><span class="sxs-lookup"><span data-stu-id="61924-109">View advise sink objects</span></span>  <br/> |
|<span data-ttu-id="61924-110">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="61924-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="61924-111">Средства просмотра формы</span><span class="sxs-lookup"><span data-stu-id="61924-111">Form viewers</span></span>  <br/> |
|<span data-ttu-id="61924-112">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="61924-112">Called by:</span></span>  <br/> |<span data-ttu-id="61924-113">Объекты формы</span><span class="sxs-lookup"><span data-stu-id="61924-113">Form objects</span></span>  <br/> |
|<span data-ttu-id="61924-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="61924-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="61924-115">IID_IMAPIViewAdviseSink</span><span class="sxs-lookup"><span data-stu-id="61924-115">IID_IMAPIViewAdviseSink</span></span>  <br/> |
|<span data-ttu-id="61924-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="61924-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="61924-117">LPMAPIVIEWADVISESINK</span><span class="sxs-lookup"><span data-stu-id="61924-117">LPMAPIVIEWADVISESINK</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="61924-118">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="61924-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="61924-119">Завершении</span><span class="sxs-lookup"><span data-stu-id="61924-119">OnShutdown</span></span>](imapiviewadvisesink-onshutdown.md) <br/> |<span data-ttu-id="61924-120">Уведомляет средство просмотра формы, что форма закрывается.</span><span class="sxs-lookup"><span data-stu-id="61924-120">Notifies the form viewer that a form is being closed.</span></span>  <br/> |
|[<span data-ttu-id="61924-121">OnNewMessage</span><span class="sxs-lookup"><span data-stu-id="61924-121">OnNewMessage</span></span>](imapiviewadvisesink-onnewmessage.md) <br/> |<span data-ttu-id="61924-122">Уведомляет средство просмотра формы после загрузки, что новое или существующее сообщение в форме.</span><span class="sxs-lookup"><span data-stu-id="61924-122">Notifies the form viewer that either a new or an existing message has been loaded in a form.</span></span>  <br/> |
|[<span data-ttu-id="61924-123">Печать (OnPrint)</span><span class="sxs-lookup"><span data-stu-id="61924-123">OnPrint</span></span>](imapiviewadvisesink-onprint.md) <br/> |<span data-ttu-id="61924-124">Уведомляет средство просмотра формы из состояния печати формы.</span><span class="sxs-lookup"><span data-stu-id="61924-124">Notifies the form viewer of the printing status of a form.</span></span>  <br/> |
|[<span data-ttu-id="61924-125">OnSubmitted</span><span class="sxs-lookup"><span data-stu-id="61924-125">OnSubmitted</span></span>](imapiviewadvisesink-onsubmitted.md) <br/> |<span data-ttu-id="61924-126">Уведомляет средство просмотра формы, что текущего сообщения были отправлены диспетчер очереди MAPI.</span><span class="sxs-lookup"><span data-stu-id="61924-126">Notifies the form viewer that the current message has been submitted to MAPI spooler.</span></span>  <br/> |
|[<span data-ttu-id="61924-127">OnSaved</span><span class="sxs-lookup"><span data-stu-id="61924-127">OnSaved</span></span>](imapiviewadvisesink-onsaved.md) <br/> |<span data-ttu-id="61924-128">Уведомляет средство просмотра формы, который был сохранен текущего сообщения в форме.</span><span class="sxs-lookup"><span data-stu-id="61924-128">Notifies the form viewer that the current message in a form has been saved.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="61924-129">См. также</span><span class="sxs-lookup"><span data-stu-id="61924-129">See also</span></span>



[<span data-ttu-id="61924-130">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="61924-130">MAPI Interfaces</span></span>](mapi-interfaces.md)

