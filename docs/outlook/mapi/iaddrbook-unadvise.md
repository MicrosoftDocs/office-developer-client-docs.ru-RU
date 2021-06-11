---
title: IAddrBookUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.Unadvise
api_type:
- COM
ms.assetid: e0db9e86-9528-43de-b8ba-a5af8b7bda4b
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 2988f1fc149bbfc2d724b62b12bd12ae4f4664a6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436155"
---
# <a name="iaddrbookunadvise"></a><span data-ttu-id="b32c2-103">IAddrBook::Unadvise</span><span class="sxs-lookup"><span data-stu-id="b32c2-103">IAddrBook::Unadvise</span></span>

  
  
<span data-ttu-id="b32c2-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b32c2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b32c2-105">Отменяет регистрацию уведомлений, ранее установленную для записи адресной книги.</span><span class="sxs-lookup"><span data-stu-id="b32c2-105">Cancels a notification registration previously established for an address book entry.</span></span>
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="b32c2-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="b32c2-106">Parameters</span></span>

 <span data-ttu-id="b32c2-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="b32c2-107">_ulConnection_</span></span>
  
> <span data-ttu-id="b32c2-108">[in] Номер подключения, который представляет отменяемую регистрацию.</span><span class="sxs-lookup"><span data-stu-id="b32c2-108">[in] A connection number that represents the registration to be canceled.</span></span> <span data-ttu-id="b32c2-109">Параметр _ulConnection должен_ содержать значение, возвращаемого по предварительному вызову метода [IAddrBook::Advise.](iaddrbook-advise.md)</span><span class="sxs-lookup"><span data-stu-id="b32c2-109">The  _ulConnection_ parameter should contain a value returned by a prior call to the [IAddrBook::Advise](iaddrbook-advise.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b32c2-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b32c2-110">Return value</span></span>

<span data-ttu-id="b32c2-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="b32c2-111">S_OK</span></span> 
  
> <span data-ttu-id="b32c2-112">Регистрация была успешно отменена.</span><span class="sxs-lookup"><span data-stu-id="b32c2-112">The registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b32c2-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="b32c2-113">Remarks</span></span>

<span data-ttu-id="b32c2-114">Клиенты **звонят по методу Unadvise,** чтобы прекратить получать уведомления об изменениях в определенной записи адресной книги.</span><span class="sxs-lookup"><span data-stu-id="b32c2-114">Clients call the **Unadvise** method to stop receiving notifications about changes to a particular address book entry.</span></span> <span data-ttu-id="b32c2-115">Когда регистрация уведомлений отменяется, поставщик адресной книги выпускает указатель на раковину рекомендации вызываемой.</span><span class="sxs-lookup"><span data-stu-id="b32c2-115">When a notification registration is canceled, the address book provider releases its pointer to the caller's advise sink.</span></span> <span data-ttu-id="b32c2-116">Однако выпуск может произойти во время вызова **Unadvise** или в более поздней точке, если другой поток находится в процессе вызова [метода IMAPIAdviseSink::OnNotify.](imapiadvisesink-onnotify.md)</span><span class="sxs-lookup"><span data-stu-id="b32c2-116">However, the release can occur during the **Unadvise** call or at some later point, if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="b32c2-117">Когда уведомление находится в процессе, выпуск откладывается до возвращения метода **OnNotify.**</span><span class="sxs-lookup"><span data-stu-id="b32c2-117">When a notification is in progress, the release is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b32c2-118">См. также</span><span class="sxs-lookup"><span data-stu-id="b32c2-118">See also</span></span>



[<span data-ttu-id="b32c2-119">IAddrBook::Advise</span><span class="sxs-lookup"><span data-stu-id="b32c2-119">IAddrBook::Advise</span></span>](iaddrbook-advise.md)
  
[<span data-ttu-id="b32c2-120">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="b32c2-120">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="b32c2-121">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="b32c2-121">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

