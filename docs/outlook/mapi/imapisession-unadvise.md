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
ms.openlocfilehash: 98a5faca00f5877eb10110406875b46a69244d94
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335704"
---
# <a name="imapisessionunadvise"></a><span data-ttu-id="e2414-103">IMAPISession::Unadvise</span><span class="sxs-lookup"><span data-stu-id="e2414-103">IMAPISession::Unadvise</span></span>

  
  
<span data-ttu-id="e2414-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e2414-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e2414-105">Отменяет отправку уведомлений, ранее настроенных с помощью вызова метода [IMAPISession::Advise.](imapisession-advise.md)</span><span class="sxs-lookup"><span data-stu-id="e2414-105">Cancels the sending of notifications previously set up with a call to the [IMAPISession::Advise](imapisession-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="e2414-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="e2414-106">Parameters</span></span>

 <span data-ttu-id="e2414-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="e2414-107">_ulConnection_</span></span>
  
> <span data-ttu-id="e2414-108">[in] Номер подключения, связанный с активной регистрацией уведомлений.</span><span class="sxs-lookup"><span data-stu-id="e2414-108">[in] A connection number associated with an active notification registration.</span></span> <span data-ttu-id="e2414-109">Значение  _ulConnection_ должно быть возвращено предыдущим вызовом **в IMAPISession::Advise**.</span><span class="sxs-lookup"><span data-stu-id="e2414-109">The value of  _ulConnection_ must have been returned by a previous call to **IMAPISession::Advise**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e2414-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e2414-110">Return value</span></span>

<span data-ttu-id="e2414-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="e2414-111">S_OK</span></span> 
  
> <span data-ttu-id="e2414-112">Регистрация была успешно отменена.</span><span class="sxs-lookup"><span data-stu-id="e2414-112">The registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e2414-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="e2414-113">Remarks</span></span>

<span data-ttu-id="e2414-114">Метод **IMAPISession::Unadvise** отменяет регистрацию для уведомления.</span><span class="sxs-lookup"><span data-stu-id="e2414-114">The **IMAPISession::Unadvise** method cancels a registration for notification.</span></span> <span data-ttu-id="e2414-115">**Unadvise** выпускает указатель на раковину рекомендации вызываемой, которую он получил в вызове **Advise,** используемом для регистрации.</span><span class="sxs-lookup"><span data-stu-id="e2414-115">**Unadvise** releases its pointer to the caller's advise sink, which it received in the **Advise** call used for registration.</span></span> 
  
<span data-ttu-id="e2414-116">Как правило, **Unadvise** вызывает метод [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) в процессе вызова **Unadvise.**</span><span class="sxs-lookup"><span data-stu-id="e2414-116">Generally, **Unadvise** calls the advise sink's [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method during the **Unadvise** call.</span></span> <span data-ttu-id="e2414-117">Однако если другой поток вызывает метод [IMAPIAdviseSink::OnNotify,](imapiadvisesink-onnotify.md) вызов выпуска откладывается до возвращения метода **OnNotify.** </span><span class="sxs-lookup"><span data-stu-id="e2414-117">However, if another thread is in the process of calling the advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e2414-118">См. также</span><span class="sxs-lookup"><span data-stu-id="e2414-118">See also</span></span>



[<span data-ttu-id="e2414-119">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="e2414-119">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="e2414-120">IMAPISession::Advise</span><span class="sxs-lookup"><span data-stu-id="e2414-120">IMAPISession::Advise</span></span>](imapisession-advise.md)
  
[<span data-ttu-id="e2414-121">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="e2414-121">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)

