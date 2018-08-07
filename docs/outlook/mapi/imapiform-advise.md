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
ms.openlocfilehash: b5347205e10b44d62a7e11cbe2f4179970f1bd64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808875"
---
# <a name="imapiformadvise"></a><span data-ttu-id="f99bf-103">IMAPIForm::Advise</span><span class="sxs-lookup"><span data-stu-id="f99bf-103">IMAPIForm::Advise</span></span>

  
  
<span data-ttu-id="f99bf-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f99bf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f99bf-105">Регистрирует просмотра формы для уведомлений о событиях, которые влияют на форме.</span><span class="sxs-lookup"><span data-stu-id="f99bf-105">Registers a form viewer for notifications about events that affect the form.</span></span>
  
```cpp
HRESULT Advise(
  LPMAPIVIEWADVISESINK pAdvise,
  ULONG FAR * pulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="f99bf-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f99bf-106">Parameters</span></span>

 <span data-ttu-id="f99bf-107">_pAdvise_</span><span class="sxs-lookup"><span data-stu-id="f99bf-107">_pAdvise_</span></span>
  
> <span data-ttu-id="f99bf-108">[in] Объект приемника для последующих уведомлений рекомендаций указатель в представление.</span><span class="sxs-lookup"><span data-stu-id="f99bf-108">[in] A pointer to a view advise sink object to receive the subsequent notifications.</span></span> 
    
 <span data-ttu-id="f99bf-109">_pulConnection_</span><span class="sxs-lookup"><span data-stu-id="f99bf-109">_pulConnection_</span></span>
  
> <span data-ttu-id="f99bf-110">[out] Указатель на ненулевое значение, представляющее регистрации успешного уведомлений.</span><span class="sxs-lookup"><span data-stu-id="f99bf-110">[out] A pointer to a nonzero value that represents a successful notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f99bf-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1">Return value</span></span>

<span data-ttu-id="f99bf-112">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="f99bf-112">S_OK</span></span> 
  
> <span data-ttu-id="f99bf-113">Регистрация прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="f99bf-113">The registration was successful.</span></span>
    
<span data-ttu-id="f99bf-114">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="f99bf-114">E_OUTOFMEMORY</span></span> 
  
> <span data-ttu-id="f99bf-115">Регистрация не удалось выполнить из-за нехватки памяти.</span><span class="sxs-lookup"><span data-stu-id="f99bf-115">The registration was unsuccessful because of insufficient memory.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f99bf-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="f99bf-116">Remarks</span></span>

<span data-ttu-id="f99bf-117">Средства просмотра формы вызов метода **IMAPIForm::Advise** формы для регистрации уведомлений при внесении изменений в форме.</span><span class="sxs-lookup"><span data-stu-id="f99bf-117">Form viewers call a form's **IMAPIForm::Advise** method to register for notification when changes occur to the form.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="f99bf-118">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="f99bf-118">Notes to implementers</span></span>

<span data-ttu-id="f99bf-119">Сохранить копию представления уведомить указателя приемника, переданной в параметре _pAdvise_ , которые можно использовать для вызова метода соответствующие [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) при возникновении события.</span><span class="sxs-lookup"><span data-stu-id="f99bf-119">Keep a copy of the view advise sink pointer passed in the  _pAdvise_ parameter so that you can use it to call the appropriate [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) method when an event occurs.</span></span> <span data-ttu-id="f99bf-120">Вызов представление уведомить метода [IUnknown::AddRef's](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx) приемника для сохранения указателя до его отмены регистрации уведомлений.</span><span class="sxs-lookup"><span data-stu-id="f99bf-120">Call the view advise sink's [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx) method to retain the pointer until notification registration is canceled.</span></span> <span data-ttu-id="f99bf-121">Содержимое для параметра _pulConnection_ значение ненулевое число.</span><span class="sxs-lookup"><span data-stu-id="f99bf-121">Set the contents of the  _pulConnection_ parameter to a nonzero number.</span></span> 
  
<span data-ttu-id="f99bf-122">Многие формы реализовать вспомогательный объект для обработки регистрации и последующие уведомления о событиях.</span><span class="sxs-lookup"><span data-stu-id="f99bf-122">Many forms implement a helper object to handle the registration and subsequent notification of events.</span></span> 
  
<span data-ttu-id="f99bf-123">Дополнительные сведения о процессе уведомления в общем случае видеть [Уведомления о событии в MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="f99bf-123">For more information about the notification process in general, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
<span data-ttu-id="f99bf-124">Дополнительные сведения о уведомлений и формах можно [Отправка и получение уведомлений формы](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="f99bf-124">For more information about notification and forms, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f99bf-125">См. также</span><span class="sxs-lookup"><span data-stu-id="f99bf-125">See also</span></span>



[<span data-ttu-id="f99bf-126">IMAPIForm::Unadvise</span><span class="sxs-lookup"><span data-stu-id="f99bf-126">IMAPIForm::Unadvise</span></span>](imapiform-unadvise.md)
  
[<span data-ttu-id="f99bf-127">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f99bf-127">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)
  
[<span data-ttu-id="f99bf-128">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f99bf-128">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)


[<span data-ttu-id="f99bf-129">Уведомление о событиях в MAPI</span><span class="sxs-lookup"><span data-stu-id="f99bf-129">Event Notification in MAPI</span></span>](event-notification-in-mapi.md)
  
[<span data-ttu-id="f99bf-130">Отправка и получение уведомлений о формах</span><span class="sxs-lookup"><span data-stu-id="f99bf-130">Sending and Receiving Form Notifications</span></span>](sending-and-receiving-form-notifications.md)

