---
title: Имапиформунадвисе
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
# <a name="imapiformunadvise"></a><span data-ttu-id="c37c0-103">IMAPIForm::Unadvise</span><span class="sxs-lookup"><span data-stu-id="c37c0-103">IMAPIForm::Unadvise</span></span>

  
  
<span data-ttu-id="c37c0-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c37c0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c37c0-105">ОтМеняет регистрацию для уведомлений с помощью средства просмотра форм, ранее установленного вызовом [имапиформ:: Advise](imapiform-advise.md).</span><span class="sxs-lookup"><span data-stu-id="c37c0-105">Cancels a registration for notifications with a form viewer previously established by calling [IMAPIForm::Advise](imapiform-advise.md).</span></span>
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="c37c0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c37c0-106">Parameters</span></span>

 <span data-ttu-id="c37c0-107">_Улконнектион_</span><span class="sxs-lookup"><span data-stu-id="c37c0-107">_ulConnection_</span></span>
  
> <span data-ttu-id="c37c0-108">возврата Номер подключения, указывающий на отмену регистрации уведомления.</span><span class="sxs-lookup"><span data-stu-id="c37c0-108">[in] A connection number that identifies the notification registration to be canceled.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c37c0-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c37c0-109">Return value</span></span>

<span data-ttu-id="c37c0-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="c37c0-110">S_OK</span></span> 
  
> <span data-ttu-id="c37c0-111">Регистрация отменена.</span><span class="sxs-lookup"><span data-stu-id="c37c0-111">The registration was canceled.</span></span>
    
<span data-ttu-id="c37c0-112">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="c37c0-112">E_INVALIDARG</span></span> 
  
> <span data-ttu-id="c37c0-113">Номер подключения, переданный в параметре _улконнектион_ , не представляет допустимую регистрацию.</span><span class="sxs-lookup"><span data-stu-id="c37c0-113">The connection number passed in the  _ulConnection_ parameter does not represent a valid registration.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c37c0-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c37c0-114">Remarks</span></span>

<span data-ttu-id="c37c0-115">В средствах просмотра форм вызывается метод **имапиформ:: unadvise** для отмены регистрации уведомлений, которые были установлены при вызове метода **Имапиформ:: Advise** .</span><span class="sxs-lookup"><span data-stu-id="c37c0-115">Form viewers call the **IMAPIForm::Unadvise** method to cancel a registration for notification that they first established by calling the **IMAPIForm::Advise** method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="c37c0-116">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="c37c0-116">Notes to implementers</span></span>

<span data-ttu-id="c37c0-117">Отмените указатель, который вы удерживаете, в приемник уведомлений просмотра формы, вызвав его метод [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="c37c0-117">Discard the pointer that you are holding to the form viewer's view advise sink by calling its [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="c37c0-118">Как правило, **выпуск** вызывается во время вызова метода unadvise. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="c37c0-118">Generally, **Release** is called during the **Unadvise** call.</span></span> <span data-ttu-id="c37c0-119">Тем не менее, если другой поток находится в процессе вызова одного из методов [имапивиевадвисесинк](imapiviewadvisesinkiunknown.md) для приемника уведомлений о просмотре, задерживает вызов **освобождения** до возвращения метода **имапивиевадвисесинк** .</span><span class="sxs-lookup"><span data-stu-id="c37c0-119">However, if another thread is in the process of calling one of the [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) methods for the view advise sink, delay the **Release** call until the **IMAPIViewAdviseSink** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c37c0-120">См. также</span><span class="sxs-lookup"><span data-stu-id="c37c0-120">See also</span></span>



[<span data-ttu-id="c37c0-121">IMAPIForm::Advise</span><span class="sxs-lookup"><span data-stu-id="c37c0-121">IMAPIForm::Advise</span></span>](imapiform-advise.md)
  
[<span data-ttu-id="c37c0-122">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c37c0-122">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)
  
[<span data-ttu-id="c37c0-123">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c37c0-123">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)

