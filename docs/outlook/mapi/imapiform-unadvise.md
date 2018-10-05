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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390473"
---
# <a name="imapiformunadvise"></a><span data-ttu-id="ae5bf-103">IMAPIForm::Unadvise</span><span class="sxs-lookup"><span data-stu-id="ae5bf-103">IMAPIForm::Unadvise</span></span>

  
  
<span data-ttu-id="ae5bf-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ae5bf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ae5bf-105">Отменяет регистрацию для уведомлений с помощью средства просмотра формы, ранее установленные путем вызова [IMAPIForm::Advise](imapiform-advise.md).</span><span class="sxs-lookup"><span data-stu-id="ae5bf-105">Cancels a registration for notifications with a form viewer previously established by calling [IMAPIForm::Advise](imapiform-advise.md).</span></span>
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="ae5bf-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ae5bf-106">Parameters</span></span>

 <span data-ttu-id="ae5bf-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="ae5bf-107">_ulConnection_</span></span>
  
> <span data-ttu-id="ae5bf-108">[in] Число подключений, определяющее регистрации уведомлений, чтобы отменить.</span><span class="sxs-lookup"><span data-stu-id="ae5bf-108">[in] A connection number that identifies the notification registration to be canceled.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ae5bf-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ae5bf-109">Return value</span></span>

<span data-ttu-id="ae5bf-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="ae5bf-110">S_OK</span></span> 
  
> <span data-ttu-id="ae5bf-111">Регистрация отменена.</span><span class="sxs-lookup"><span data-stu-id="ae5bf-111">The registration was canceled.</span></span>
    
<span data-ttu-id="ae5bf-112">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="ae5bf-112">E_INVALIDARG</span></span> 
  
> <span data-ttu-id="ae5bf-113">Номер соединения, переданной в параметре _ulConnection_ не представляет допустимое регистрации.</span><span class="sxs-lookup"><span data-stu-id="ae5bf-113">The connection number passed in the  _ulConnection_ parameter does not represent a valid registration.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ae5bf-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="ae5bf-114">Remarks</span></span>

<span data-ttu-id="ae5bf-115">Средства просмотра форм вызовите метод **IMAPIForm::Unadvise** для отмены регистрации для уведомлений, сначала установить путем вызова метода **IMAPIForm::Advise** .</span><span class="sxs-lookup"><span data-stu-id="ae5bf-115">Form viewers call the **IMAPIForm::Unadvise** method to cancel a registration for notification that they first established by calling the **IMAPIForm::Advise** method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="ae5bf-116">Примечания для реализующих</span><span class="sxs-lookup"><span data-stu-id="ae5bf-116">Notes to implementers</span></span>

<span data-ttu-id="ae5bf-117">Отменить указатель, содержат представление формы просмотра уведомить приемник путем вызова метода [функции IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="ae5bf-117">Discard the pointer that you are holding to the form viewer's view advise sink by calling its [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="ae5bf-118">Как правило, называется **выпуска** во время вызова **Unadvise** .</span><span class="sxs-lookup"><span data-stu-id="ae5bf-118">Generally, **Release** is called during the **Unadvise** call.</span></span> <span data-ttu-id="ae5bf-119">Тем не менее если другой поток находится в процессе вызова одного из методов [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) для представления уведомить приемник, задержки звонка **выпуска** до возвращения методом **IMAPIViewAdviseSink** .</span><span class="sxs-lookup"><span data-stu-id="ae5bf-119">However, if another thread is in the process of calling one of the [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) methods for the view advise sink, delay the **Release** call until the **IMAPIViewAdviseSink** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ae5bf-120">См. также</span><span class="sxs-lookup"><span data-stu-id="ae5bf-120">See also</span></span>



[<span data-ttu-id="ae5bf-121">IMAPIForm::Advise</span><span class="sxs-lookup"><span data-stu-id="ae5bf-121">IMAPIForm::Advise</span></span>](imapiform-advise.md)
  
[<span data-ttu-id="ae5bf-122">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ae5bf-122">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)
  
[<span data-ttu-id="ae5bf-123">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ae5bf-123">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)

