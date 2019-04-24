---
title: Имслогонунадвисе
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.Unadvise
api_type:
- COM
ms.assetid: 440d61c4-b69a-4010-a22b-0c9c5c376fbc
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 9172d4956e78ac31cd15d69e70d05c127a474ca5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317278"
---
# <a name="imslogonunadvise"></a><span data-ttu-id="62240-103">IMSLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="62240-103">IMSLogon::Unadvise</span></span>

  
  
<span data-ttu-id="62240-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="62240-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="62240-105">Удаляет регистрацию объекта для уведомления об изменениях хранилища сообщений, ранее установленных с помощью вызова метода [имслогон:: Advise](imslogon-advise.md) .</span><span class="sxs-lookup"><span data-stu-id="62240-105">Removes an object's registration for notification of message store changes previously established by using a call to the [IMSLogon::Advise](imslogon-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="62240-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="62240-106">Parameters</span></span>

 <span data-ttu-id="62240-107">_Улконнектион_</span><span class="sxs-lookup"><span data-stu-id="62240-107">_ulConnection_</span></span>
  
> <span data-ttu-id="62240-108">возврата Номер регистрационного подключения, возвращенного при вызове **имслогон:: Advise**.</span><span class="sxs-lookup"><span data-stu-id="62240-108">[in] The number of the registration connection returned by a call to **IMSLogon::Advise**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="62240-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="62240-109">Return value</span></span>

<span data-ttu-id="62240-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="62240-110">S_OK</span></span> 
  
> <span data-ttu-id="62240-111">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="62240-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="62240-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="62240-112">Remarks</span></span>

<span data-ttu-id="62240-113">Поставщики хранилища сообщений реализуют метод **имслогон::** Unadvise для освобождения указателя на объект приемника уведомлений, переданный в параметре _Лпадвисесинк_ предыдущего вызова **имслогон:: Advise**, отменяя уведомление зарегистрировал.</span><span class="sxs-lookup"><span data-stu-id="62240-113">Message store providers implement the **IMSLogon::Unadvise** method to release the pointer to the advise sink object passed in the  _lpAdviseSink_ parameter in the previous call to **IMSLogon::Advise**, thereby canceling a notification registration.</span></span> <span data-ttu-id="62240-114">При отмене указателя на объект приемника уведомлений вызывается метод " [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) " объекта.</span><span class="sxs-lookup"><span data-stu-id="62240-114">As part of discarding the pointer to the advise sink object, the object's [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method is called.</span></span> <span data-ttu-id="62240-115">Как правило, **выпуск** вызывается во время вызова метода unadvise. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="62240-115">Generally, **Release** is called during the **Unadvise** call.</span></span> <span data-ttu-id="62240-116">Тем не менее, если другой поток находится в процессе вызова метода [имапиадвисесинк:: OnNotify](imapiadvisesink-onnotify.md) для объекта приемника уведомлений, вызов **освобождения** задерживается до возвращения метода **OnNotify** .</span><span class="sxs-lookup"><span data-stu-id="62240-116">However, if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="62240-117">См. также</span><span class="sxs-lookup"><span data-stu-id="62240-117">See also</span></span>



[<span data-ttu-id="62240-118">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="62240-118">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="62240-119">IMSLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="62240-119">IMSLogon::Advise</span></span>](imslogon-advise.md)
  
[<span data-ttu-id="62240-120">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="62240-120">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

