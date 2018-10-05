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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398019"
---
# <a name="imsgstoreunadvise"></a><span data-ttu-id="7861f-103">IMsgStore::Unadvise</span><span class="sxs-lookup"><span data-stu-id="7861f-103">IMsgStore::Unadvise</span></span>

  
  
<span data-ttu-id="7861f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7861f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7861f-105">Показано, как отменить отправку уведомлений, ранее настройка с помощью вызова метода [IMsgStore::Advise](imsgstore-advise.md) .</span><span class="sxs-lookup"><span data-stu-id="7861f-105">Cancels the sending of notifications previously set up with a call to the [IMsgStore::Advise](imsgstore-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="7861f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7861f-106">Parameters</span></span>

 <span data-ttu-id="7861f-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="7861f-107">_ulConnection_</span></span>
  
> <span data-ttu-id="7861f-108">[in] Номер подключения, связанный с регистрацию active уведомлений.</span><span class="sxs-lookup"><span data-stu-id="7861f-108">[in] The connection number associated with an active notification registration.</span></span> <span data-ttu-id="7861f-109">Необходимо, значение _ulConnection_ возвращена предыдущий вызов метода **IMsgStore::Advise** .</span><span class="sxs-lookup"><span data-stu-id="7861f-109">The value of  _ulConnection_ must have been returned by a previous call to the **IMsgStore::Advise** method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7861f-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7861f-110">Return value</span></span>

<span data-ttu-id="7861f-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="7861f-111">S_OK</span></span> 
  
> <span data-ttu-id="7861f-112">Регистрация успешно отменена.</span><span class="sxs-lookup"><span data-stu-id="7861f-112">The registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7861f-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="7861f-113">Remarks</span></span>

<span data-ttu-id="7861f-114">Метод **IMsgStore::Unadvise** отменяет регистрацию для уведомлений.</span><span class="sxs-lookup"><span data-stu-id="7861f-114">The **IMsgStore::Unadvise** method cancels a registration for notification.</span></span> <span data-ttu-id="7861f-115">Выпуски **Unadvise** указатель вызывающего абонента уведомить приемника, полученных в вызове **уведомлений** , используемые для регистрации.</span><span class="sxs-lookup"><span data-stu-id="7861f-115">**Unadvise** releases its pointer to the caller's advise sink, which it received in the **Advise** call used for registration.</span></span> 
  
<span data-ttu-id="7861f-116">Как правило **Unadvise** вызывает метод [функции IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) приемник уведомлений во время вызова **Unadvise** .</span><span class="sxs-lookup"><span data-stu-id="7861f-116">Generally, **Unadvise** calls the advise sink's [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method during the **Unadvise** call.</span></span> <span data-ttu-id="7861f-117">Тем не менее если другой поток находится в процессе вызова метода [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) приемник уведомлений, вызов **выпуске** откладывается до возвращения методом **OnNotify** .</span><span class="sxs-lookup"><span data-stu-id="7861f-117">However, if another thread is in the process of calling the advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7861f-118">См. также</span><span class="sxs-lookup"><span data-stu-id="7861f-118">See also</span></span>



[<span data-ttu-id="7861f-119">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="7861f-119">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="7861f-120">IMsgStore::Advise</span><span class="sxs-lookup"><span data-stu-id="7861f-120">IMsgStore::Advise</span></span>](imsgstore-advise.md)
  
[<span data-ttu-id="7861f-121">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="7861f-121">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

