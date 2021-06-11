---
title: IMAPIFormUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.Unadvise
api_type:
- COM
ms.assetid: fdda45e2-631d-404c-8af4-bce68df0968b
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 770ceb7af98f5271baad65043e013feb353d231a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329472"
---
# <a name="imapiformunadvise"></a><span data-ttu-id="4a614-103">IMAPIForm::Unadvise</span><span class="sxs-lookup"><span data-stu-id="4a614-103">IMAPIForm::Unadvise</span></span>

  
  
<span data-ttu-id="4a614-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4a614-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4a614-105">Отменяет регистрацию уведомлений с предварительно установленным средством просмотра форм по вызову [IMAPIForm:::Advise](imapiform-advise.md).</span><span class="sxs-lookup"><span data-stu-id="4a614-105">Cancels a registration for notifications with a form viewer previously established by calling [IMAPIForm::Advise](imapiform-advise.md).</span></span>
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="4a614-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="4a614-106">Parameters</span></span>

 <span data-ttu-id="4a614-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="4a614-107">_ulConnection_</span></span>
  
> <span data-ttu-id="4a614-108">[in] Номер подключения, который определяет отмену регистрации уведомлений.</span><span class="sxs-lookup"><span data-stu-id="4a614-108">[in] A connection number that identifies the notification registration to be canceled.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4a614-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4a614-109">Return value</span></span>

<span data-ttu-id="4a614-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="4a614-110">S_OK</span></span> 
  
> <span data-ttu-id="4a614-111">Регистрация была отменена.</span><span class="sxs-lookup"><span data-stu-id="4a614-111">The registration was canceled.</span></span>
    
<span data-ttu-id="4a614-112">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="4a614-112">E_INVALIDARG</span></span> 
  
> <span data-ttu-id="4a614-113">Номер подключения, переданный в  _параметре ulConnection,_ не является допустимой регистрацией.</span><span class="sxs-lookup"><span data-stu-id="4a614-113">The connection number passed in the  _ulConnection_ parameter does not represent a valid registration.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="4a614-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="4a614-114">Remarks</span></span>

<span data-ttu-id="4a614-115">Зрители формы звонят по методу **IMAPIForm::Unadvise,** чтобы отменить регистрацию для уведомления, которое они впервые установили, позвонив по методу **IMAPIForm::Advise.**</span><span class="sxs-lookup"><span data-stu-id="4a614-115">Form viewers call the **IMAPIForm::Unadvise** method to cancel a registration for notification that they first established by calling the **IMAPIForm::Advise** method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="4a614-116">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="4a614-116">Notes to implementers</span></span>

<span data-ttu-id="4a614-117">Откажитесь от указателя, удерживаемого в представлении просмотра формы, посоветуйте удалить его [метод IUnknown::Release.](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4a614-117">Discard the pointer that you are holding to the form viewer's view advise sink by calling its [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="4a614-118">Как правило, **выпуск** вызываем во время вызова **Unadvise.**</span><span class="sxs-lookup"><span data-stu-id="4a614-118">Generally, **Release** is called during the **Unadvise** call.</span></span> <span data-ttu-id="4a614-119">Однако, если другой поток находится в процессе вызова одного из методов [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) для представления, сообщите об этом, отозвать вызов выпуска до возвращения метода **IMAPIViewAdviseSink.** </span><span class="sxs-lookup"><span data-stu-id="4a614-119">However, if another thread is in the process of calling one of the [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) methods for the view advise sink, delay the **Release** call until the **IMAPIViewAdviseSink** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4a614-120">См. также</span><span class="sxs-lookup"><span data-stu-id="4a614-120">See also</span></span>



[<span data-ttu-id="4a614-121">IMAPIForm::Advise</span><span class="sxs-lookup"><span data-stu-id="4a614-121">IMAPIForm::Advise</span></span>](imapiform-advise.md)
  
[<span data-ttu-id="4a614-122">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4a614-122">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)
  
[<span data-ttu-id="4a614-123">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4a614-123">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)

