---
title: IMAPIFormAdviseSink IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormAdviseSink
api_type:
- COM
ms.assetid: 180022af-4c1c-408c-a3fe-ed075cef79ab
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 68c2af0cd8d7ccddf6aa6017cfb830b196ac0771
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392062"
---
# <a name="imapiformadvisesink--iunknown"></a><span data-ttu-id="bc505-103">IMAPIFormAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bc505-103">IMAPIFormAdviseSink : IUnknown</span></span>

  
  
<span data-ttu-id="bc505-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bc505-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bc505-105">Позволяет получать уведомления от средства просмотра формы серверам формы.</span><span class="sxs-lookup"><span data-stu-id="bc505-105">Enables form servers to receive notifications from form viewers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bc505-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="bc505-106">Header file:</span></span>  <br/> |<span data-ttu-id="bc505-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="bc505-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="bc505-108">Предоставляемые:</span><span class="sxs-lookup"><span data-stu-id="bc505-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="bc505-109">Форма уведомить объектов приемника</span><span class="sxs-lookup"><span data-stu-id="bc505-109">Form advise sink objects</span></span>  <br/> |
|<span data-ttu-id="bc505-110">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="bc505-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="bc505-111">Серверы формы</span><span class="sxs-lookup"><span data-stu-id="bc505-111">Form servers</span></span>  <br/> |
|<span data-ttu-id="bc505-112">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="bc505-112">Called by:</span></span>  <br/> |<span data-ttu-id="bc505-113">Средства просмотра формы</span><span class="sxs-lookup"><span data-stu-id="bc505-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="bc505-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="bc505-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="bc505-115">IID_IMAPIFormAdviseSink</span><span class="sxs-lookup"><span data-stu-id="bc505-115">IID_IMAPIFormAdviseSink</span></span>  <br/> |
|<span data-ttu-id="bc505-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="bc505-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="bc505-117">LPMAPIFORMADVISESINK</span><span class="sxs-lookup"><span data-stu-id="bc505-117">LPMAPIFORMADVISESINK</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="bc505-118">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="bc505-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="bc505-119">OnChange</span><span class="sxs-lookup"><span data-stu-id="bc505-119">OnChange</span></span>](imapiformadvisesink-onchange.md) <br/> |<span data-ttu-id="bc505-120">Указывает, было изменено в состояние просмотра формы.</span><span class="sxs-lookup"><span data-stu-id="bc505-120">Indicates that a change has occurred in the status of the form viewer.</span></span>  <br/> |
|[<span data-ttu-id="bc505-121">OnActivateNext</span><span class="sxs-lookup"><span data-stu-id="bc505-121">OnActivateNext</span></span>](imapiformadvisesink-onactivatenext.md) <br/> |<span data-ttu-id="bc505-122">Указывает, является ли форма может обрабатывать класса сообщений для следующего сообщения для отображения.</span><span class="sxs-lookup"><span data-stu-id="bc505-122">Indicates whether the form can handle the message class of the next message to display.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bc505-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="bc505-123">Remarks</span></span>

<span data-ttu-id="bc505-124">Объект приемника для реализации **IMAPIFormAdviseSink** вместо включая с их объекта формы рекомендаций использования серверов формы в форме.</span><span class="sxs-lookup"><span data-stu-id="bc505-124">Form servers use a form advise sink object to implement **IMAPIFormAdviseSink** instead of including it with their form object.</span></span> <span data-ttu-id="bc505-125">Таким образом формы просматривающих отчеты пользователей следует ожидать сбоя вызова метода [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) формы для получения указателя на этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="bc505-125">Therefore, form viewers should expect a failed call to a form's [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) method to obtain a pointer to this interface.</span></span> 
  
<span data-ttu-id="bc505-126">Серверы формы вызов метода [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) средство просмотра для регистрации уведомлений.</span><span class="sxs-lookup"><span data-stu-id="bc505-126">Form servers call a viewer's [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) method to register for notifications.</span></span> <span data-ttu-id="bc505-127">Указатель на их реализации **IMAPIFormAdviseSink** используется в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="bc505-127">A pointer to their **IMAPIFormAdviseSink** implementation is included as a parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bc505-128">См. также</span><span class="sxs-lookup"><span data-stu-id="bc505-128">See also</span></span>



[<span data-ttu-id="bc505-129">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="bc505-129">MAPI Interfaces</span></span>](mapi-interfaces.md)

