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
ms.openlocfilehash: 33287d8ac6b1faeba8b8746a95850f6fd1c37462
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579489"
---
# <a name="imapiformunadvise"></a><span data-ttu-id="7b2b9-103">IMAPIForm::Unadvise</span><span class="sxs-lookup"><span data-stu-id="7b2b9-103">IMAPIForm::Unadvise</span></span>

  
  
<span data-ttu-id="7b2b9-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7b2b9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7b2b9-105">Отменяет регистрацию для уведомлений с помощью средства просмотра формы, ранее установленные путем вызова [IMAPIForm::Advise](imapiform-advise.md).</span><span class="sxs-lookup"><span data-stu-id="7b2b9-105">Cancels a registration for notifications with a form viewer previously established by calling [IMAPIForm::Advise](imapiform-advise.md).</span></span>
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="7b2b9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7b2b9-106">Parameters</span></span>

 <span data-ttu-id="7b2b9-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="7b2b9-107">_ulConnection_</span></span>
  
> <span data-ttu-id="7b2b9-108">[in] Число подключений, определяющее регистрации уведомлений, чтобы отменить.</span><span class="sxs-lookup"><span data-stu-id="7b2b9-108">[in] A connection number that identifies the notification registration to be canceled.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7b2b9-109">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="7b2b9-109">Return value</span></span>

<span data-ttu-id="7b2b9-110">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="7b2b9-110">S_OK</span></span> 
  
> <span data-ttu-id="7b2b9-111">Регистрация отменена.</span><span class="sxs-lookup"><span data-stu-id="7b2b9-111">The registration was canceled.</span></span>
    
<span data-ttu-id="7b2b9-112">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="7b2b9-112">E_INVALIDARG</span></span> 
  
> <span data-ttu-id="7b2b9-113">Номер соединения, переданной в параметре _ulConnection_ не представляет допустимое регистрации.</span><span class="sxs-lookup"><span data-stu-id="7b2b9-113">The connection number passed in the  _ulConnection_ parameter does not represent a valid registration.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="7b2b9-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="7b2b9-114">Remarks</span></span>

<span data-ttu-id="7b2b9-115">Средства просмотра форм вызовите метод **IMAPIForm::Unadvise** для отмены регистрации для уведомлений, сначала установить путем вызова метода **IMAPIForm::Advise** .</span><span class="sxs-lookup"><span data-stu-id="7b2b9-115">Form viewers call the **IMAPIForm::Unadvise** method to cancel a registration for notification that they first established by calling the **IMAPIForm::Advise** method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="7b2b9-116">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="7b2b9-116">Notes to implementers</span></span>

<span data-ttu-id="7b2b9-117">Отменить указатель, содержат представление формы просмотра уведомить приемник путем вызова метода [функции IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="7b2b9-117">Discard the pointer that you are holding to the form viewer's view advise sink by calling its [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="7b2b9-118">Как правило, называется **выпуска** во время вызова **Unadvise** .</span><span class="sxs-lookup"><span data-stu-id="7b2b9-118">Generally, **Release** is called during the **Unadvise** call.</span></span> <span data-ttu-id="7b2b9-119">Тем не менее если другой поток находится в процессе вызова одного из методов [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) для представления уведомить приемник, задержки звонка **выпуска** до возвращения методом **IMAPIViewAdviseSink** .</span><span class="sxs-lookup"><span data-stu-id="7b2b9-119">However, if another thread is in the process of calling one of the [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) methods for the view advise sink, delay the **Release** call until the **IMAPIViewAdviseSink** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7b2b9-120">См. также</span><span class="sxs-lookup"><span data-stu-id="7b2b9-120">See also</span></span>



[<span data-ttu-id="7b2b9-121">IMAPIForm::Advise</span><span class="sxs-lookup"><span data-stu-id="7b2b9-121">IMAPIForm::Advise</span></span>](imapiform-advise.md)
  
[<span data-ttu-id="7b2b9-122">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7b2b9-122">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)
  
[<span data-ttu-id="7b2b9-123">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7b2b9-123">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)

