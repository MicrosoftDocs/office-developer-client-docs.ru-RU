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
ms.openlocfilehash: 826863e30ae39d3c8d523bd2dff84731bcf16971
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808905"
---
# <a name="imapiformunadvise"></a><span data-ttu-id="0e254-103">IMAPIForm::Unadvise</span><span class="sxs-lookup"><span data-stu-id="0e254-103">IMAPIForm::Unadvise</span></span>

  
  
<span data-ttu-id="0e254-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0e254-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0e254-105">Отменяет регистрацию для уведомлений с помощью средства просмотра формы, ранее установленные путем вызова [IMAPIForm::Advise](imapiform-advise.md).</span><span class="sxs-lookup"><span data-stu-id="0e254-105">Cancels a registration for notifications with a form viewer previously established by calling [IMAPIForm::Advise](imapiform-advise.md).</span></span>
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="0e254-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0e254-106">Parameters</span></span>

 <span data-ttu-id="0e254-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="0e254-107">_ulConnection_</span></span>
  
> <span data-ttu-id="0e254-108">[in] Число подключений, определяющее регистрации уведомлений, чтобы отменить.</span><span class="sxs-lookup"><span data-stu-id="0e254-108">[in] A connection number that identifies the notification registration to be canceled.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0e254-109">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="0e254-109">Return value</span></span>

<span data-ttu-id="0e254-110">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="0e254-110">S_OK</span></span> 
  
> <span data-ttu-id="0e254-111">Регистрация отменена.</span><span class="sxs-lookup"><span data-stu-id="0e254-111">The registration was canceled.</span></span>
    
<span data-ttu-id="0e254-112">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="0e254-112">E_INVALIDARG</span></span> 
  
> <span data-ttu-id="0e254-113">Номер соединения, переданной в параметре _ulConnection_ не представляет допустимое регистрации.</span><span class="sxs-lookup"><span data-stu-id="0e254-113">The connection number passed in the  _ulConnection_ parameter does not represent a valid registration.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0e254-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="0e254-114">Remarks</span></span>

<span data-ttu-id="0e254-115">Средства просмотра форм вызовите метод **IMAPIForm::Unadvise** для отмены регистрации для уведомлений, сначала установить путем вызова метода **IMAPIForm::Advise** .</span><span class="sxs-lookup"><span data-stu-id="0e254-115">Form viewers call the **IMAPIForm::Unadvise** method to cancel a registration for notification that they first established by calling the **IMAPIForm::Advise** method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="0e254-116">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="0e254-116">Notes to implementers</span></span>

<span data-ttu-id="0e254-117">Отменить указатель, содержат представление формы просмотра уведомить приемник путем вызова метода [функции IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="0e254-117">Discard the pointer that you are holding to the form viewer's view advise sink by calling its [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="0e254-118">Как правило, называется **выпуска** во время вызова **Unadvise** .</span><span class="sxs-lookup"><span data-stu-id="0e254-118">Generally, **Release** is called during the **Unadvise** call.</span></span> <span data-ttu-id="0e254-119">Тем не менее если другой поток находится в процессе вызова одного из методов [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) для представления уведомить приемник, задержки звонка **выпуска** до возвращения методом **IMAPIViewAdviseSink** .</span><span class="sxs-lookup"><span data-stu-id="0e254-119">However, if another thread is in the process of calling one of the [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) methods for the view advise sink, delay the **Release** call until the **IMAPIViewAdviseSink** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0e254-120">См. также</span><span class="sxs-lookup"><span data-stu-id="0e254-120">See also</span></span>



[<span data-ttu-id="0e254-121">IMAPIForm::Advise</span><span class="sxs-lookup"><span data-stu-id="0e254-121">IMAPIForm::Advise</span></span>](imapiform-advise.md)
  
[<span data-ttu-id="0e254-122">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0e254-122">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)
  
[<span data-ttu-id="0e254-123">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0e254-123">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)

