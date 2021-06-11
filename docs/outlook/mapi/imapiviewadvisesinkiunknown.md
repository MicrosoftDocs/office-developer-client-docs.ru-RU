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
ms.openlocfilehash: 70f61fe33baa7870a58c4cbc7d75e0df119b5b1a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429420"
---
# <a name="imapiviewadvisesink--iunknown"></a><span data-ttu-id="322c4-103">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="322c4-103">IMAPIViewAdviseSink : IUnknown</span></span>

  
  
<span data-ttu-id="322c4-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="322c4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="322c4-105">Получает уведомления из форм.</span><span class="sxs-lookup"><span data-stu-id="322c4-105">Receives notifications from forms.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="322c4-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="322c4-106">Header file:</span></span>  <br/> |<span data-ttu-id="322c4-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="322c4-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="322c4-108">Подвергается:</span><span class="sxs-lookup"><span data-stu-id="322c4-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="322c4-109">Просмотр рекомендуемых объектов раковины</span><span class="sxs-lookup"><span data-stu-id="322c4-109">View advise sink objects</span></span>  <br/> |
|<span data-ttu-id="322c4-110">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="322c4-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="322c4-111">Просмотр форм</span><span class="sxs-lookup"><span data-stu-id="322c4-111">Form viewers</span></span>  <br/> |
|<span data-ttu-id="322c4-112">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="322c4-112">Called by:</span></span>  <br/> |<span data-ttu-id="322c4-113">Объекты форм</span><span class="sxs-lookup"><span data-stu-id="322c4-113">Form objects</span></span>  <br/> |
|<span data-ttu-id="322c4-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="322c4-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="322c4-115">IID_IMAPIViewAdviseSink</span><span class="sxs-lookup"><span data-stu-id="322c4-115">IID_IMAPIViewAdviseSink</span></span>  <br/> |
|<span data-ttu-id="322c4-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="322c4-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="322c4-117">LPMAPIVIEWADVISESINK</span><span class="sxs-lookup"><span data-stu-id="322c4-117">LPMAPIVIEWADVISESINK</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="322c4-118">Заказ Vtable</span><span class="sxs-lookup"><span data-stu-id="322c4-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="322c4-119">OnShutdown</span><span class="sxs-lookup"><span data-stu-id="322c4-119">OnShutdown</span></span>](imapiviewadvisesink-onshutdown.md) <br/> |<span data-ttu-id="322c4-120">Заветив зрителю формы, что форма закрывается.</span><span class="sxs-lookup"><span data-stu-id="322c4-120">Notifies the form viewer that a form is being closed.</span></span>  <br/> |
|[<span data-ttu-id="322c4-121">OnNewMessage</span><span class="sxs-lookup"><span data-stu-id="322c4-121">OnNewMessage</span></span>](imapiviewadvisesink-onnewmessage.md) <br/> |<span data-ttu-id="322c4-122">Сообщает зрителю формы, что новое или существующее сообщение загружено в форме.</span><span class="sxs-lookup"><span data-stu-id="322c4-122">Notifies the form viewer that either a new or an existing message has been loaded in a form.</span></span>  <br/> |
|[<span data-ttu-id="322c4-123">OnPrint</span><span class="sxs-lookup"><span data-stu-id="322c4-123">OnPrint</span></span>](imapiviewadvisesink-onprint.md) <br/> |<span data-ttu-id="322c4-124">Заветив зрителю формы состояние печати формы.</span><span class="sxs-lookup"><span data-stu-id="322c4-124">Notifies the form viewer of the printing status of a form.</span></span>  <br/> |
|[<span data-ttu-id="322c4-125">OnSubmitted</span><span class="sxs-lookup"><span data-stu-id="322c4-125">OnSubmitted</span></span>](imapiviewadvisesink-onsubmitted.md) <br/> |<span data-ttu-id="322c4-126">Сообщает зрителю формы, что текущее сообщение было отправлено в пулер MAPI.</span><span class="sxs-lookup"><span data-stu-id="322c4-126">Notifies the form viewer that the current message has been submitted to MAPI spooler.</span></span>  <br/> |
|[<span data-ttu-id="322c4-127">OnSaved</span><span class="sxs-lookup"><span data-stu-id="322c4-127">OnSaved</span></span>](imapiviewadvisesink-onsaved.md) <br/> |<span data-ttu-id="322c4-128">Сообщает зрителю формы, что текущее сообщение в форме сохранено.</span><span class="sxs-lookup"><span data-stu-id="322c4-128">Notifies the form viewer that the current message in a form has been saved.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="322c4-129">См. также</span><span class="sxs-lookup"><span data-stu-id="322c4-129">See also</span></span>



[<span data-ttu-id="322c4-130">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="322c4-130">MAPI Interfaces</span></span>](mapi-interfaces.md)

