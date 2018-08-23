---
title: IMAPISessionUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.Unadvise
api_type:
- COM
ms.assetid: 5e608cb0-808d-4418-8521-71dcbce8cdff
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 3b582b48773b9f6f1a6f46f9c0e4c6dcb9782b86
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592068"
---
# <a name="imapisessionunadvise"></a><span data-ttu-id="419e6-103">IMAPISession::Unadvise</span><span class="sxs-lookup"><span data-stu-id="419e6-103">IMAPISession::Unadvise</span></span>

  
  
<span data-ttu-id="419e6-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="419e6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="419e6-105">Показано, как отменить отправку уведомлений, ранее настройка с помощью вызова метода [IMAPISession::Advise](imapisession-advise.md) .</span><span class="sxs-lookup"><span data-stu-id="419e6-105">Cancels the sending of notifications previously set up with a call to the [IMAPISession::Advise](imapisession-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="419e6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="419e6-106">Parameters</span></span>

 <span data-ttu-id="419e6-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="419e6-107">_ulConnection_</span></span>
  
> <span data-ttu-id="419e6-108">[in] Номер подключения, связанный с регистрацию active уведомлений.</span><span class="sxs-lookup"><span data-stu-id="419e6-108">[in] A connection number associated with an active notification registration.</span></span> <span data-ttu-id="419e6-109">Необходимо, с помощью предыдущей вызова **IMAPISession::Advise**были возвращается значение _ulConnection_ .</span><span class="sxs-lookup"><span data-stu-id="419e6-109">The value of  _ulConnection_ must have been returned by a previous call to **IMAPISession::Advise**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="419e6-110">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="419e6-110">Return value</span></span>

<span data-ttu-id="419e6-111">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="419e6-111">S_OK</span></span> 
  
> <span data-ttu-id="419e6-112">Регистрация успешно отменена.</span><span class="sxs-lookup"><span data-stu-id="419e6-112">The registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="419e6-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="419e6-113">Remarks</span></span>

<span data-ttu-id="419e6-114">Метод **IMAPISession::Unadvise** отменяет регистрацию для уведомлений.</span><span class="sxs-lookup"><span data-stu-id="419e6-114">The **IMAPISession::Unadvise** method cancels a registration for notification.</span></span> <span data-ttu-id="419e6-115">Выпуски **Unadvise** указатель вызывающего абонента уведомить приемника, полученных в вызове **уведомлений** , используемые для регистрации.</span><span class="sxs-lookup"><span data-stu-id="419e6-115">**Unadvise** releases its pointer to the caller's advise sink, which it received in the **Advise** call used for registration.</span></span> 
  
<span data-ttu-id="419e6-116">Как правило **Unadvise** вызывает метод [функции IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) приемник уведомлений во время вызова **Unadvise** .</span><span class="sxs-lookup"><span data-stu-id="419e6-116">Generally, **Unadvise** calls the advise sink's [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) method during the **Unadvise** call.</span></span> <span data-ttu-id="419e6-117">Тем не менее если другой поток находится в процессе вызова метода [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) приемник уведомлений, вызов **выпуске** откладывается до возвращения методом **OnNotify** .</span><span class="sxs-lookup"><span data-stu-id="419e6-117">However, if another thread is in the process of calling the advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="419e6-118">См. также</span><span class="sxs-lookup"><span data-stu-id="419e6-118">See also</span></span>



[<span data-ttu-id="419e6-119">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="419e6-119">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="419e6-120">IMAPISession::Advise</span><span class="sxs-lookup"><span data-stu-id="419e6-120">IMAPISession::Advise</span></span>](imapisession-advise.md)
  
[<span data-ttu-id="419e6-121">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="419e6-121">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)

