---
title: IMsgStoreUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.Unadvise
api_type:
- COM
ms.assetid: 1394039b-d509-49a5-8421-b7362d906879
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: f85b662b7fe710c66a2e69dd3cd3db22e3283ddb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309725"
---
# <a name="imsgstoreunadvise"></a><span data-ttu-id="34000-103">IMsgStore::Unadvise</span><span class="sxs-lookup"><span data-stu-id="34000-103">IMsgStore::Unadvise</span></span>

  
  
<span data-ttu-id="34000-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="34000-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="34000-105">Отменяет отправку уведомлений, ранее установленных с помощью вызова в [метод IMsgStore::Advise.](imsgstore-advise.md)</span><span class="sxs-lookup"><span data-stu-id="34000-105">Cancels the sending of notifications previously set up with a call to the [IMsgStore::Advise](imsgstore-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="34000-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="34000-106">Parameters</span></span>

 <span data-ttu-id="34000-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="34000-107">_ulConnection_</span></span>
  
> <span data-ttu-id="34000-108">[in] Номер подключения, связанный с активной регистрацией уведомлений.</span><span class="sxs-lookup"><span data-stu-id="34000-108">[in] The connection number associated with an active notification registration.</span></span> <span data-ttu-id="34000-109">Значение _ulConnection_ должно быть возвращено предыдущим вызовом в **метод IMsgStore::Advise.**</span><span class="sxs-lookup"><span data-stu-id="34000-109">The value of  _ulConnection_ must have been returned by a previous call to the **IMsgStore::Advise** method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="34000-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="34000-110">Return value</span></span>

<span data-ttu-id="34000-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="34000-111">S_OK</span></span> 
  
> <span data-ttu-id="34000-112">Регистрация была успешно отменена.</span><span class="sxs-lookup"><span data-stu-id="34000-112">The registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="34000-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="34000-113">Remarks</span></span>

<span data-ttu-id="34000-114">Метод **IMsgStore::Unadvise** отменяет регистрацию для уведомления.</span><span class="sxs-lookup"><span data-stu-id="34000-114">The **IMsgStore::Unadvise** method cancels a registration for notification.</span></span> <span data-ttu-id="34000-115">**Unadvise** выпускает указатель на раковину рекомендации вызываемой, которую он получил в вызове **Advise,** используемом для регистрации.</span><span class="sxs-lookup"><span data-stu-id="34000-115">**Unadvise** releases its pointer to the caller's advise sink, which it received in the **Advise** call used for registration.</span></span> 
  
<span data-ttu-id="34000-116">Как правило, **Unadvise** вызывает метод [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) в процессе вызова **Unadvise.**</span><span class="sxs-lookup"><span data-stu-id="34000-116">Generally, **Unadvise** calls the advise sink's [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method during the **Unadvise** call.</span></span> <span data-ttu-id="34000-117">Однако если другой поток вызывает метод [IMAPIAdviseSink::OnNotify,](imapiadvisesink-onnotify.md) вызов выпуска откладывается до возвращения метода **OnNotify.** </span><span class="sxs-lookup"><span data-stu-id="34000-117">However, if another thread is in the process of calling the advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="34000-118">См. также</span><span class="sxs-lookup"><span data-stu-id="34000-118">See also</span></span>



[<span data-ttu-id="34000-119">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="34000-119">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="34000-120">IMsgStore::Advise</span><span class="sxs-lookup"><span data-stu-id="34000-120">IMsgStore::Advise</span></span>](imsgstore-advise.md)
  
[<span data-ttu-id="34000-121">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="34000-121">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

