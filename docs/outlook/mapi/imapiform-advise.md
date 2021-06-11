---
title: IMAPIFormAdvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.Advise
api_type:
- COM
ms.assetid: 961318d6-bebe-4f4b-98ff-921cafc68d24
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 2ed8bace97dee3842243ed835769e80e8aaf6b03
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329486"
---
# <a name="imapiformadvise"></a><span data-ttu-id="c12a4-103">IMAPIForm::Advise</span><span class="sxs-lookup"><span data-stu-id="c12a4-103">IMAPIForm::Advise</span></span>

  
  
<span data-ttu-id="c12a4-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c12a4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c12a4-105">Регистрирует просмотра форм для уведомлений о событиях, влияющих на форму.</span><span class="sxs-lookup"><span data-stu-id="c12a4-105">Registers a form viewer for notifications about events that affect the form.</span></span>
  
```cpp
HRESULT Advise(
  LPMAPIVIEWADVISESINK pAdvise,
  ULONG FAR * pulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="c12a4-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="c12a4-106">Parameters</span></span>

 <span data-ttu-id="c12a4-107">_pAdvise_</span><span class="sxs-lookup"><span data-stu-id="c12a4-107">_pAdvise_</span></span>
  
> <span data-ttu-id="c12a4-108">[in] Указатель на представление советует объекту раковины получать последующие уведомления.</span><span class="sxs-lookup"><span data-stu-id="c12a4-108">[in] A pointer to a view advise sink object to receive the subsequent notifications.</span></span> 
    
 <span data-ttu-id="c12a4-109">_pulConnection_</span><span class="sxs-lookup"><span data-stu-id="c12a4-109">_pulConnection_</span></span>
  
> <span data-ttu-id="c12a4-110">[вышел] Указатель на значение nonzero, которое представляет успешную регистрацию уведомлений.</span><span class="sxs-lookup"><span data-stu-id="c12a4-110">[out] A pointer to a nonzero value that represents a successful notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c12a4-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c12a4-111">Return value</span></span>

<span data-ttu-id="c12a4-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="c12a4-112">S_OK</span></span> 
  
> <span data-ttu-id="c12a4-113">Регистрация прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="c12a4-113">The registration was successful.</span></span>
    
<span data-ttu-id="c12a4-114">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="c12a4-114">E_OUTOFMEMORY</span></span> 
  
> <span data-ttu-id="c12a4-115">Регистрация была неудачной из-за недостаточной памяти.</span><span class="sxs-lookup"><span data-stu-id="c12a4-115">The registration was unsuccessful because of insufficient memory.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c12a4-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="c12a4-116">Remarks</span></span>

<span data-ttu-id="c12a4-117">Зрители формы звонят по методу **IMAPIForm:::Advise** формы, чтобы зарегистрироваться для уведомления при внесении изменений в форму.</span><span class="sxs-lookup"><span data-stu-id="c12a4-117">Form viewers call a form's **IMAPIForm::Advise** method to register for notification when changes occur to the form.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="c12a4-118">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="c12a4-118">Notes to implementers</span></span>

<span data-ttu-id="c12a4-119">Храните копию представления, сообщайте указатель раковины, переданный в  _параметре pAdvise,_ чтобы вы могли использовать его для вызова соответствующего метода [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) при событии.</span><span class="sxs-lookup"><span data-stu-id="c12a4-119">Keep a copy of the view advise sink pointer passed in the  _pAdvise_ parameter so that you can use it to call the appropriate [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) method when an event occurs.</span></span> <span data-ttu-id="c12a4-120">Вызов представления советую [методу IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) сохранить указатель до отмены регистрации уведомлений.</span><span class="sxs-lookup"><span data-stu-id="c12a4-120">Call the view advise sink's [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) method to retain the pointer until notification registration is canceled.</span></span> <span data-ttu-id="c12a4-121">Установите содержимое параметра  _pulConnection_ на номер nonzero.</span><span class="sxs-lookup"><span data-stu-id="c12a4-121">Set the contents of the  _pulConnection_ parameter to a nonzero number.</span></span> 
  
<span data-ttu-id="c12a4-122">Во многих формах реализован объект помощника для обработки регистрации и последующего уведомления о событиях.</span><span class="sxs-lookup"><span data-stu-id="c12a4-122">Many forms implement a helper object to handle the registration and subsequent notification of events.</span></span> 
  
<span data-ttu-id="c12a4-123">Дополнительные сведения о процессе уведомления в целом см. в сообщении [о событиях в MAPI.](event-notification-in-mapi.md)</span><span class="sxs-lookup"><span data-stu-id="c12a4-123">For more information about the notification process in general, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
<span data-ttu-id="c12a4-124">Дополнительные сведения об уведомлениях и формах см. в рублях [Отправка и получение уведомлений о форме.](sending-and-receiving-form-notifications.md)</span><span class="sxs-lookup"><span data-stu-id="c12a4-124">For more information about notification and forms, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c12a4-125">См. также</span><span class="sxs-lookup"><span data-stu-id="c12a4-125">See also</span></span>



[<span data-ttu-id="c12a4-126">IMAPIForm::Unadvise</span><span class="sxs-lookup"><span data-stu-id="c12a4-126">IMAPIForm::Unadvise</span></span>](imapiform-unadvise.md)
  
[<span data-ttu-id="c12a4-127">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c12a4-127">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)
  
[<span data-ttu-id="c12a4-128">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c12a4-128">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)


[<span data-ttu-id="c12a4-129">Уведомление о событиях в MAPI</span><span class="sxs-lookup"><span data-stu-id="c12a4-129">Event Notification in MAPI</span></span>](event-notification-in-mapi.md)
  
[<span data-ttu-id="c12a4-130">Отправка и получение уведомлений о форме</span><span class="sxs-lookup"><span data-stu-id="c12a4-130">Sending and Receiving Form Notifications</span></span>](sending-and-receiving-form-notifications.md)

