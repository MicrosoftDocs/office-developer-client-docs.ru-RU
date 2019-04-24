---
title: Имапиформадвисесинк IUnknown
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
# <a name="imapiformadvisesink--iunknown"></a><span data-ttu-id="9b528-103">IMAPIFormAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9b528-103">IMAPIFormAdviseSink : IUnknown</span></span>

  
  
<span data-ttu-id="9b528-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9b528-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9b528-105">Позволяет серверам форм получать уведомления от средств просмотра форм.</span><span class="sxs-lookup"><span data-stu-id="9b528-105">Enables form servers to receive notifications from form viewers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9b528-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="9b528-106">Header file:</span></span>  <br/> |<span data-ttu-id="9b528-107">Мапиформ. h</span><span class="sxs-lookup"><span data-stu-id="9b528-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="9b528-108">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="9b528-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="9b528-109">Объекты приемника рекомендаций для форм</span><span class="sxs-lookup"><span data-stu-id="9b528-109">Form advise sink objects</span></span>  <br/> |
|<span data-ttu-id="9b528-110">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="9b528-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="9b528-111">Серверы форм</span><span class="sxs-lookup"><span data-stu-id="9b528-111">Form servers</span></span>  <br/> |
|<span data-ttu-id="9b528-112">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="9b528-112">Called by:</span></span>  <br/> |<span data-ttu-id="9b528-113">Средства просмотра форм</span><span class="sxs-lookup"><span data-stu-id="9b528-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="9b528-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="9b528-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="9b528-115">Иид_имапиформадвисесинк</span><span class="sxs-lookup"><span data-stu-id="9b528-115">IID_IMAPIFormAdviseSink</span></span>  <br/> |
|<span data-ttu-id="9b528-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="9b528-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="9b528-117">ЛПМАПИФОРМАДВИСЕСИНК</span><span class="sxs-lookup"><span data-stu-id="9b528-117">LPMAPIFORMADVISESINK</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="9b528-118">Заказ vtable</span><span class="sxs-lookup"><span data-stu-id="9b528-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="9b528-119">OnChange</span><span class="sxs-lookup"><span data-stu-id="9b528-119">OnChange</span></span>](imapiformadvisesink-onchange.md) <br/> |<span data-ttu-id="9b528-120">Указывает, что в состоянии средства просмотра форм произошло изменение.</span><span class="sxs-lookup"><span data-stu-id="9b528-120">Indicates that a change has occurred in the status of the form viewer.</span></span>  <br/> |
|[<span data-ttu-id="9b528-121">Онактиватенекст</span><span class="sxs-lookup"><span data-stu-id="9b528-121">OnActivateNext</span></span>](imapiformadvisesink-onactivatenext.md) <br/> |<span data-ttu-id="9b528-122">Указывает, может ли форма обрабатывать класс сообщения следующего отображаемого сообщения.</span><span class="sxs-lookup"><span data-stu-id="9b528-122">Indicates whether the form can handle the message class of the next message to display.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9b528-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="9b528-123">Remarks</span></span>

<span data-ttu-id="9b528-124">Серверы форм используют объект приемника уведомлений формы, чтобы реализовать **имапиформадвисесинк** , а не включать его в объект Form.</span><span class="sxs-lookup"><span data-stu-id="9b528-124">Form servers use a form advise sink object to implement **IMAPIFormAdviseSink** instead of including it with their form object.</span></span> <span data-ttu-id="9b528-125">Таким образом, средства просмотра форм должны ожидать неудачный вызов метода [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) формы, чтобы получить указатель на этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="9b528-125">Therefore, form viewers should expect a failed call to a form's [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) method to obtain a pointer to this interface.</span></span> 
  
<span data-ttu-id="9b528-126">Серверы форм вызовите метод средства просмотра [имапивиевконтекст:: сетадвисесинк](imapiviewcontext-setadvisesink.md) для регистрации уведомлений.</span><span class="sxs-lookup"><span data-stu-id="9b528-126">Form servers call a viewer's [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) method to register for notifications.</span></span> <span data-ttu-id="9b528-127">Указатель на свою реализацию **имапиформадвисесинк** включается в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="9b528-127">A pointer to their **IMAPIFormAdviseSink** implementation is included as a parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9b528-128">См. также</span><span class="sxs-lookup"><span data-stu-id="9b528-128">See also</span></span>



[<span data-ttu-id="9b528-129">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="9b528-129">MAPI Interfaces</span></span>](mapi-interfaces.md)

