---
title: Иаддрбукунадвисе
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
# <a name="iaddrbookunadvise"></a><span data-ttu-id="41d56-103">IAddrBook::Unadvise</span><span class="sxs-lookup"><span data-stu-id="41d56-103">IAddrBook::Unadvise</span></span>

  
  
<span data-ttu-id="41d56-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="41d56-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="41d56-105">ОтМеняет регистрацию уведомления, установленную ранее для записи адресной книги.</span><span class="sxs-lookup"><span data-stu-id="41d56-105">Cancels a notification registration previously established for an address book entry.</span></span>
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="41d56-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="41d56-106">Parameters</span></span>

 <span data-ttu-id="41d56-107">_Улконнектион_</span><span class="sxs-lookup"><span data-stu-id="41d56-107">_ulConnection_</span></span>
  
> <span data-ttu-id="41d56-108">возврата Номер подключения, представляющий отмену регистрации.</span><span class="sxs-lookup"><span data-stu-id="41d56-108">[in] A connection number that represents the registration to be canceled.</span></span> <span data-ttu-id="41d56-109">Параметр _улконнектион_ должен содержать значение, возвращенное при предыдущем вызове метода [IAddrBook:: Advise](iaddrbook-advise.md) .</span><span class="sxs-lookup"><span data-stu-id="41d56-109">The  _ulConnection_ parameter should contain a value returned by a prior call to the [IAddrBook::Advise](iaddrbook-advise.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="41d56-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="41d56-110">Return value</span></span>

<span data-ttu-id="41d56-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="41d56-111">S_OK</span></span> 
  
> <span data-ttu-id="41d56-112">Регистрация успешно отменена.</span><span class="sxs-lookup"><span data-stu-id="41d56-112">The registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="41d56-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="41d56-113">Remarks</span></span>

<span data-ttu-id="41d56-114">Клиенты вызывают метод **unadvise** для прекращения получения уведомлений об изменениях в определенной записи адресной книги.</span><span class="sxs-lookup"><span data-stu-id="41d56-114">Clients call the **Unadvise** method to stop receiving notifications about changes to a particular address book entry.</span></span> <span data-ttu-id="41d56-115">При отмене регистрации уведомления поставщик адресных книг освобождает свой указатель приемника уведомлений вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="41d56-115">When a notification registration is canceled, the address book provider releases its pointer to the caller's advise sink.</span></span> <span data-ttu-id="41d56-116">Тем не менее, при вызове метода **unadvise** может произойти освобождение, если другой поток находится в процессе вызова метода [имапиадвисесинк:: OnNotify](imapiadvisesink-onnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="41d56-116">However, the release can occur during the **Unadvise** call or at some later point, if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="41d56-117">При выполнении уведомления выпуск откладывается до тех пор, пока не \*\*\*\* будет возвращен метод OnNotify.</span><span class="sxs-lookup"><span data-stu-id="41d56-117">When a notification is in progress, the release is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="41d56-118">См. также</span><span class="sxs-lookup"><span data-stu-id="41d56-118">See also</span></span>



[<span data-ttu-id="41d56-119">IAddrBook::Advise</span><span class="sxs-lookup"><span data-stu-id="41d56-119">IAddrBook::Advise</span></span>](iaddrbook-advise.md)
  
[<span data-ttu-id="41d56-120">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="41d56-120">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="41d56-121">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="41d56-121">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

