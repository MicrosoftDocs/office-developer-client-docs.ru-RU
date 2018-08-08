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
ms.openlocfilehash: bf72e6f182f67861f909e21f0ec1871d76617974
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/15/2018
ms.locfileid: "19808776"
---
# <a name="iaddrbookunadvise"></a><span data-ttu-id="a79b2-103">IAddrBook::Unadvise</span><span class="sxs-lookup"><span data-stu-id="a79b2-103">IAddrBook::Unadvise</span></span>

  
  
<span data-ttu-id="a79b2-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a79b2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a79b2-105">Отмена регистрации уведомлений, ранее созданные записи адресной книги.</span><span class="sxs-lookup"><span data-stu-id="a79b2-105">Cancels a notification registration previously established for an address book entry.</span></span>
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="a79b2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a79b2-106">Parameters</span></span>

 <span data-ttu-id="a79b2-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="a79b2-107">_ulConnection_</span></span>
  
> <span data-ttu-id="a79b2-108">[in] Номер подключения, который представляет регистрации отменяется.</span><span class="sxs-lookup"><span data-stu-id="a79b2-108">[in] A connection number that represents the registration to be canceled.</span></span> <span data-ttu-id="a79b2-109">Параметр _ulConnection_ должен содержать значение, возвращаемое во время предыдущего вызова метода [IAddrBook::Advise](iaddrbook-advise.md) .</span><span class="sxs-lookup"><span data-stu-id="a79b2-109">The  _ulConnection_ parameter should contain a value returned by a prior call to the [IAddrBook::Advise](iaddrbook-advise.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a79b2-110">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="a79b2-110">Return value</span></span>

<span data-ttu-id="a79b2-111">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="a79b2-111">S_OK</span></span> 
  
> <span data-ttu-id="a79b2-112">Регистрация успешно отменена.</span><span class="sxs-lookup"><span data-stu-id="a79b2-112">The registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a79b2-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="a79b2-113">Remarks</span></span>

<span data-ttu-id="a79b2-114">Клиенты вызовите метод **Unadvise** прекратить получение уведомлений об изменениях в записи определенного адресной книги.</span><span class="sxs-lookup"><span data-stu-id="a79b2-114">Clients call the **Unadvise** method to stop receiving notifications about changes to a particular address book entry.</span></span> <span data-ttu-id="a79b2-115">После отмены регистрации уведомлений адресная книга указатель вызывающего абонента уведомить выпусков поставщика приемника.</span><span class="sxs-lookup"><span data-stu-id="a79b2-115">When a notification registration is canceled, the address book provider releases its pointer to the caller's advise sink.</span></span> <span data-ttu-id="a79b2-116">Тем не менее выпуска могут возникнуть во время вызова **Unadvise** или позже, если другой поток находится в процессе вызова метода [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="a79b2-116">However, the release can occur during the **Unadvise** call or at some later point, if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="a79b2-117">Если уведомление о ходе выполнения, выпуска откладывается до возвращения методом **OnNotify** .</span><span class="sxs-lookup"><span data-stu-id="a79b2-117">When a notification is in progress, the release is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a79b2-118">См. также</span><span class="sxs-lookup"><span data-stu-id="a79b2-118">See also</span></span>



[<span data-ttu-id="a79b2-119">IAddrBook::Advise</span><span class="sxs-lookup"><span data-stu-id="a79b2-119">IAddrBook::Advise</span></span>](iaddrbook-advise.md)
  
[<span data-ttu-id="a79b2-120">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="a79b2-120">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="a79b2-121">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="a79b2-121">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

