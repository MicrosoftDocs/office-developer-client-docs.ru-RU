---
title: имапиформадвисе
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
# <a name="imapiformadvise"></a><span data-ttu-id="e0dec-103">IMAPIForm::Advise</span><span class="sxs-lookup"><span data-stu-id="e0dec-103">IMAPIForm::Advise</span></span>

  
  
<span data-ttu-id="e0dec-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e0dec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e0dec-105">Регистрирует средство просмотра форм для уведомлений о событиях, влияющих на форму.</span><span class="sxs-lookup"><span data-stu-id="e0dec-105">Registers a form viewer for notifications about events that affect the form.</span></span>
  
```cpp
HRESULT Advise(
  LPMAPIVIEWADVISESINK pAdvise,
  ULONG FAR * pulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="e0dec-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e0dec-106">Parameters</span></span>

 <span data-ttu-id="e0dec-107">_падвисе_</span><span class="sxs-lookup"><span data-stu-id="e0dec-107">_pAdvise_</span></span>
  
> <span data-ttu-id="e0dec-108">возврата Указатель на объект приемника уведомлений о просмотре для получения последующих уведомлений.</span><span class="sxs-lookup"><span data-stu-id="e0dec-108">[in] A pointer to a view advise sink object to receive the subsequent notifications.</span></span> 
    
 <span data-ttu-id="e0dec-109">_пулконнектион_</span><span class="sxs-lookup"><span data-stu-id="e0dec-109">_pulConnection_</span></span>
  
> <span data-ttu-id="e0dec-110">вышли Указатель на ненулевое значение, представляющее успешную регистрацию уведомлений.</span><span class="sxs-lookup"><span data-stu-id="e0dec-110">[out] A pointer to a nonzero value that represents a successful notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e0dec-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e0dec-111">Return value</span></span>

<span data-ttu-id="e0dec-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="e0dec-112">S_OK</span></span> 
  
> <span data-ttu-id="e0dec-113">Регистрация выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="e0dec-113">The registration was successful.</span></span>
    
<span data-ttu-id="e0dec-114">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="e0dec-114">E_OUTOFMEMORY</span></span> 
  
> <span data-ttu-id="e0dec-115">Не удалось выполнить регистрацию из-за недостатка памяти.</span><span class="sxs-lookup"><span data-stu-id="e0dec-115">The registration was unsuccessful because of insufficient memory.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e0dec-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="e0dec-116">Remarks</span></span>

<span data-ttu-id="e0dec-117">Средства просмотра форм вызывают метод формы **имапиформ:: Advise** для регистрации уведомлений об изменениях формы.</span><span class="sxs-lookup"><span data-stu-id="e0dec-117">Form viewers call a form's **IMAPIForm::Advise** method to register for notification when changes occur to the form.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="e0dec-118">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="e0dec-118">Notes to implementers</span></span>

<span data-ttu-id="e0dec-119">Сохраните копию указателя приемника уведомлений о просмотре, переданной в параметре _падвисе_ , чтобы можно было использовать его для вызова соответствующего метода [имапивиевадвисесинк](imapiviewadvisesinkiunknown.md) при возникновении события.</span><span class="sxs-lookup"><span data-stu-id="e0dec-119">Keep a copy of the view advise sink pointer passed in the  _pAdvise_ parameter so that you can use it to call the appropriate [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) method when an event occurs.</span></span> <span data-ttu-id="e0dec-120">Вызовите метод [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) приемника уведомлений о просмотре, чтобы сохранить указатель до отмены регистрации уведомления.</span><span class="sxs-lookup"><span data-stu-id="e0dec-120">Call the view advise sink's [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) method to retain the pointer until notification registration is canceled.</span></span> <span data-ttu-id="e0dec-121">Задайте для параметра _пулконнектион_ значение ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="e0dec-121">Set the contents of the  _pulConnection_ parameter to a nonzero number.</span></span> 
  
<span data-ttu-id="e0dec-122">Многие формы реализуют вспомогательный объект для обработки регистрации и последующего уведомления о событиях.</span><span class="sxs-lookup"><span data-stu-id="e0dec-122">Many forms implement a helper object to handle the registration and subsequent notification of events.</span></span> 
  
<span data-ttu-id="e0dec-123">Дополнительные сведения о процессе уведомления в разделе Общие сведения об [уведомлении о событиях в MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="e0dec-123">For more information about the notification process in general, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
<span data-ttu-id="e0dec-124">Дополнительные сведения об уведомлении и формах можно найти в статье [Отправка и получение уведомлений формы](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="e0dec-124">For more information about notification and forms, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e0dec-125">См. также</span><span class="sxs-lookup"><span data-stu-id="e0dec-125">See also</span></span>



[<span data-ttu-id="e0dec-126">IMAPIForm::Unadvise</span><span class="sxs-lookup"><span data-stu-id="e0dec-126">IMAPIForm::Unadvise</span></span>](imapiform-unadvise.md)
  
[<span data-ttu-id="e0dec-127">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e0dec-127">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)
  
[<span data-ttu-id="e0dec-128">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e0dec-128">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)


[<span data-ttu-id="e0dec-129">Уведомление о событии в MAPI</span><span class="sxs-lookup"><span data-stu-id="e0dec-129">Event Notification in MAPI</span></span>](event-notification-in-mapi.md)
  
[<span data-ttu-id="e0dec-130">Отправка и получение уведомлений формы</span><span class="sxs-lookup"><span data-stu-id="e0dec-130">Sending and Receiving Form Notifications</span></span>](sending-and-receiving-form-notifications.md)

