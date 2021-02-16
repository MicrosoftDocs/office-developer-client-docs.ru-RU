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
# <a name="imapiformadvise"></a><span data-ttu-id="72fda-103">IMAPIForm::Advise</span><span class="sxs-lookup"><span data-stu-id="72fda-103">IMAPIForm::Advise</span></span>

  
  
<span data-ttu-id="72fda-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="72fda-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="72fda-105">Регистрирует просмотр формы для уведомлений о событиях, влияющих на форму.</span><span class="sxs-lookup"><span data-stu-id="72fda-105">Registers a form viewer for notifications about events that affect the form.</span></span>
  
```cpp
HRESULT Advise(
  LPMAPIVIEWADVISESINK pAdvise,
  ULONG FAR * pulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="72fda-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="72fda-106">Parameters</span></span>

 <span data-ttu-id="72fda-107">_pAdvise_</span><span class="sxs-lookup"><span data-stu-id="72fda-107">_pAdvise_</span></span>
  
> <span data-ttu-id="72fda-108">[in] Указатель на объект приемника представления рекомендует получать последующие уведомления.</span><span class="sxs-lookup"><span data-stu-id="72fda-108">[in] A pointer to a view advise sink object to receive the subsequent notifications.</span></span> 
    
 <span data-ttu-id="72fda-109">_pulConnection_</span><span class="sxs-lookup"><span data-stu-id="72fda-109">_pulConnection_</span></span>
  
> <span data-ttu-id="72fda-110">[out] Указатель на неимякое значение, которое представляет успешную регистрацию уведомлений.</span><span class="sxs-lookup"><span data-stu-id="72fda-110">[out] A pointer to a nonzero value that represents a successful notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="72fda-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="72fda-111">Return value</span></span>

<span data-ttu-id="72fda-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="72fda-112">S_OK</span></span> 
  
> <span data-ttu-id="72fda-113">Регистрация прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="72fda-113">The registration was successful.</span></span>
    
<span data-ttu-id="72fda-114">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="72fda-114">E_OUTOFMEMORY</span></span> 
  
> <span data-ttu-id="72fda-115">Регистрация не была успешной из-за нехватки памяти.</span><span class="sxs-lookup"><span data-stu-id="72fda-115">The registration was unsuccessful because of insufficient memory.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="72fda-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="72fda-116">Remarks</span></span>

<span data-ttu-id="72fda-117">Посетители форм звонят **методу IMAPIForm::Advise** формы, чтобы зарегистрировать уведомление при внесении изменений в форму.</span><span class="sxs-lookup"><span data-stu-id="72fda-117">Form viewers call a form's **IMAPIForm::Advise** method to register for notification when changes occur to the form.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="72fda-118">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="72fda-118">Notes to implementers</span></span>

<span data-ttu-id="72fda-119">Храните копию указателя приемника рекомендации представления, переданную в  _параметре pAdvise,_ чтобы использовать его для вызова соответствующего метода [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) при событии.</span><span class="sxs-lookup"><span data-stu-id="72fda-119">Keep a copy of the view advise sink pointer passed in the  _pAdvise_ parameter so that you can use it to call the appropriate [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) method when an event occurs.</span></span> <span data-ttu-id="72fda-120">Вызовите метод [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) приемника представлений, чтобы сохранить указатель до отмены регистрации уведомления.</span><span class="sxs-lookup"><span data-stu-id="72fda-120">Call the view advise sink's [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) method to retain the pointer until notification registration is canceled.</span></span> <span data-ttu-id="72fda-121">Установите для содержимого параметра  _pulConnection_ ненулевую нулевую.</span><span class="sxs-lookup"><span data-stu-id="72fda-121">Set the contents of the  _pulConnection_ parameter to a nonzero number.</span></span> 
  
<span data-ttu-id="72fda-122">Многие формы реализуют объект-помощник для обработки регистрации и последующего уведомления о событиях.</span><span class="sxs-lookup"><span data-stu-id="72fda-122">Many forms implement a helper object to handle the registration and subsequent notification of events.</span></span> 
  
<span data-ttu-id="72fda-123">Дополнительные сведения о процессе уведомлений в целом см. в [уведомлении о событии в MAPI.](event-notification-in-mapi.md)</span><span class="sxs-lookup"><span data-stu-id="72fda-123">For more information about the notification process in general, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
<span data-ttu-id="72fda-124">Дополнительные сведения об уведомлениях и формах см. в сведениях об отправке и [получении уведомлений о формах.](sending-and-receiving-form-notifications.md)</span><span class="sxs-lookup"><span data-stu-id="72fda-124">For more information about notification and forms, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="72fda-125">См. также</span><span class="sxs-lookup"><span data-stu-id="72fda-125">See also</span></span>



[<span data-ttu-id="72fda-126">IMAPIForm::Unadvise</span><span class="sxs-lookup"><span data-stu-id="72fda-126">IMAPIForm::Unadvise</span></span>](imapiform-unadvise.md)
  
[<span data-ttu-id="72fda-127">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="72fda-127">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)
  
[<span data-ttu-id="72fda-128">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="72fda-128">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)


[<span data-ttu-id="72fda-129">Уведомление о событии в MAPI</span><span class="sxs-lookup"><span data-stu-id="72fda-129">Event Notification in MAPI</span></span>](event-notification-in-mapi.md)
  
[<span data-ttu-id="72fda-130">Отправка и получение уведомлений формы</span><span class="sxs-lookup"><span data-stu-id="72fda-130">Sending and Receiving Form Notifications</span></span>](sending-and-receiving-form-notifications.md)

