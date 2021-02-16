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
# <a name="imapisessionunadvise"></a><span data-ttu-id="84c9b-103">IMAPISession::Unadvise</span><span class="sxs-lookup"><span data-stu-id="84c9b-103">IMAPISession::Unadvise</span></span>

  
  
<span data-ttu-id="84c9b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="84c9b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="84c9b-105">Отменяет отправку уведомлений, ранее настроив вызов метода [IMAPISession::Advise.](imapisession-advise.md)</span><span class="sxs-lookup"><span data-stu-id="84c9b-105">Cancels the sending of notifications previously set up with a call to the [IMAPISession::Advise](imapisession-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="84c9b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="84c9b-106">Parameters</span></span>

 <span data-ttu-id="84c9b-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="84c9b-107">_ulConnection_</span></span>
  
> <span data-ttu-id="84c9b-108">[in] Номер подключения, связанный с регистрацией активных уведомлений.</span><span class="sxs-lookup"><span data-stu-id="84c9b-108">[in] A connection number associated with an active notification registration.</span></span> <span data-ttu-id="84c9b-109">Значение _ulConnection_ должно быть возвращено предыдущим вызовом **IMAPISession::Advise.**</span><span class="sxs-lookup"><span data-stu-id="84c9b-109">The value of  _ulConnection_ must have been returned by a previous call to **IMAPISession::Advise**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="84c9b-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="84c9b-110">Return value</span></span>

<span data-ttu-id="84c9b-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="84c9b-111">S_OK</span></span> 
  
> <span data-ttu-id="84c9b-112">Регистрация успешно отменена.</span><span class="sxs-lookup"><span data-stu-id="84c9b-112">The registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="84c9b-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="84c9b-113">Remarks</span></span>

<span data-ttu-id="84c9b-114">Метод **IMAPISession::Unadvise** отменяет регистрацию для уведомления.</span><span class="sxs-lookup"><span data-stu-id="84c9b-114">The **IMAPISession::Unadvise** method cancels a registration for notification.</span></span> <span data-ttu-id="84c9b-115">**Unadvise** отпускает свой указатель на замещетель консультации звонящего, который он получил в вызове **advise,** используемом для регистрации.</span><span class="sxs-lookup"><span data-stu-id="84c9b-115">**Unadvise** releases its pointer to the caller's advise sink, which it received in the **Advise** call used for registration.</span></span> 
  
<span data-ttu-id="84c9b-116">Как правило, **Unadvise** вызывает метод [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) приемника рекомендации во время вызова **Unadvise.**</span><span class="sxs-lookup"><span data-stu-id="84c9b-116">Generally, **Unadvise** calls the advise sink's [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method during the **Unadvise** call.</span></span> <span data-ttu-id="84c9b-117">Однако если в процессе вызова метода [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) приемника рекомендации вызывается другой поток, вызов **release** откладывается до тех пор, пока не будет возвращен метод **OnNotify.**</span><span class="sxs-lookup"><span data-stu-id="84c9b-117">However, if another thread is in the process of calling the advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="84c9b-118">См. также</span><span class="sxs-lookup"><span data-stu-id="84c9b-118">See also</span></span>



[<span data-ttu-id="84c9b-119">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="84c9b-119">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="84c9b-120">IMAPISession::Advise</span><span class="sxs-lookup"><span data-stu-id="84c9b-120">IMAPISession::Advise</span></span>](imapisession-advise.md)
  
[<span data-ttu-id="84c9b-121">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="84c9b-121">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)

