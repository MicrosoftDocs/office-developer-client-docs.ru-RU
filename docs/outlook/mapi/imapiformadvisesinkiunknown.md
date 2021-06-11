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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286606"
---
# <a name="imapiformadvisesink--iunknown"></a><span data-ttu-id="e6506-103">IMAPIFormAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e6506-103">IMAPIFormAdviseSink : IUnknown</span></span>

  
  
<span data-ttu-id="e6506-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e6506-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e6506-105">Позволяет серверам форм получать уведомления от зрителей форм.</span><span class="sxs-lookup"><span data-stu-id="e6506-105">Enables form servers to receive notifications from form viewers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e6506-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="e6506-106">Header file:</span></span>  <br/> |<span data-ttu-id="e6506-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="e6506-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="e6506-108">Подвергается:</span><span class="sxs-lookup"><span data-stu-id="e6506-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="e6506-109">Form advise sink objects</span><span class="sxs-lookup"><span data-stu-id="e6506-109">Form advise sink objects</span></span>  <br/> |
|<span data-ttu-id="e6506-110">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="e6506-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="e6506-111">Серверы форм</span><span class="sxs-lookup"><span data-stu-id="e6506-111">Form servers</span></span>  <br/> |
|<span data-ttu-id="e6506-112">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="e6506-112">Called by:</span></span>  <br/> |<span data-ttu-id="e6506-113">Просмотр форм</span><span class="sxs-lookup"><span data-stu-id="e6506-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="e6506-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="e6506-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="e6506-115">IID_IMAPIFormAdviseSink</span><span class="sxs-lookup"><span data-stu-id="e6506-115">IID_IMAPIFormAdviseSink</span></span>  <br/> |
|<span data-ttu-id="e6506-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="e6506-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="e6506-117">LPMAPIFORMADVISESINK</span><span class="sxs-lookup"><span data-stu-id="e6506-117">LPMAPIFORMADVISESINK</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="e6506-118">Заказ Vtable</span><span class="sxs-lookup"><span data-stu-id="e6506-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="e6506-119">OnChange</span><span class="sxs-lookup"><span data-stu-id="e6506-119">OnChange</span></span>](imapiformadvisesink-onchange.md) <br/> |<span data-ttu-id="e6506-120">Указывает, что в состоянии просмотра формы произошли изменения.</span><span class="sxs-lookup"><span data-stu-id="e6506-120">Indicates that a change has occurred in the status of the form viewer.</span></span>  <br/> |
|[<span data-ttu-id="e6506-121">OnActivateNext</span><span class="sxs-lookup"><span data-stu-id="e6506-121">OnActivateNext</span></span>](imapiformadvisesink-onactivatenext.md) <br/> |<span data-ttu-id="e6506-122">Указывает, может ли форма обрабатывать класс сообщений следующего отображаемого сообщения.</span><span class="sxs-lookup"><span data-stu-id="e6506-122">Indicates whether the form can handle the message class of the next message to display.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e6506-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="e6506-123">Remarks</span></span>

<span data-ttu-id="e6506-124">Серверы форм используют объект раковины формы для реализации **объекта IMAPIFormAdviseSink** вместо того, чтобы включать его в объект формы.</span><span class="sxs-lookup"><span data-stu-id="e6506-124">Form servers use a form advise sink object to implement **IMAPIFormAdviseSink** instead of including it with their form object.</span></span> <span data-ttu-id="e6506-125">Поэтому для просмотра форм следует ожидать неудаваемого вызова метода [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) для получения указателя на этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="e6506-125">Therefore, form viewers should expect a failed call to a form's [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) method to obtain a pointer to this interface.</span></span> 
  
<span data-ttu-id="e6506-126">Серверы форм звонят по методу [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) для регистрации уведомлений.</span><span class="sxs-lookup"><span data-stu-id="e6506-126">Form servers call a viewer's [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) method to register for notifications.</span></span> <span data-ttu-id="e6506-127">В качестве параметра включен указатель на реализацию **IMAPIFormAdviseSink.**</span><span class="sxs-lookup"><span data-stu-id="e6506-127">A pointer to their **IMAPIFormAdviseSink** implementation is included as a parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e6506-128">См. также</span><span class="sxs-lookup"><span data-stu-id="e6506-128">See also</span></span>



[<span data-ttu-id="e6506-129">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="e6506-129">MAPI Interfaces</span></span>](mapi-interfaces.md)

