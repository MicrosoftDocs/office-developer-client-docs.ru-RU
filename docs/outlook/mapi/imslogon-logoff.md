---
title: IMSLogonLogoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.Logoff
api_type:
- COM
ms.assetid: 1b0d1b52-6651-4de3-9381-86772d9d52a1
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 66ba27d1d333be3217f2a22ca5d53449372c1f31
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399237"
---
# <a name="imslogonlogoff"></a><span data-ttu-id="57519-103">IMSLogon::Logoff</span><span class="sxs-lookup"><span data-stu-id="57519-103">IMSLogon::Logoff</span></span>

  
  
<span data-ttu-id="57519-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="57519-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="57519-105">Поставщик хранилища, выходит из системы сообщение.</span><span class="sxs-lookup"><span data-stu-id="57519-105">Logs off a message store provider.</span></span> 
  
```cpp
HRESULT Logoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="57519-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="57519-106">Parameters</span></span>

 <span data-ttu-id="57519-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="57519-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="57519-108">[in] Зарезервировано; должен быть указатель нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="57519-108">[in] Reserved; must be a pointer to zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="57519-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="57519-109">Return value</span></span>

<span data-ttu-id="57519-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="57519-110">S_OK</span></span> 
  
> <span data-ttu-id="57519-111">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="57519-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="57519-112">���������</span><span class="sxs-lookup"><span data-stu-id="57519-112">Remarks</span></span>

<span data-ttu-id="57519-113">Поставщики хранилища сообщений реализуйте метод **IMSLogon::Logoff** принудительно завершить работу поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="57519-113">Message store providers implement the **IMSLogon::Logoff** method to forcibly shut down a message store provider.</span></span> <span data-ttu-id="57519-114">**IMSLogon::Logoff** вызывается в следующих ситуациях:</span><span class="sxs-lookup"><span data-stu-id="57519-114">**IMSLogon::Logoff** is called in the following situations:</span></span> 
  
- <span data-ttu-id="57519-115">Во время MAPI выхода клиента после вызова метода [IMAPISession::Logoff](imapisession-logoff.md) .</span><span class="sxs-lookup"><span data-stu-id="57519-115">While MAPI is logging off a client after a call to the [IMAPISession::Logoff](imapisession-logoff.md) method.</span></span> 
    
- <span data-ttu-id="57519-116">Во время выхода поставщика хранилища сообщений MAPI.</span><span class="sxs-lookup"><span data-stu-id="57519-116">While MAPI is logging off a message store provider.</span></span> <span data-ttu-id="57519-117">В этом случае **IMSLogon::Logoff** вызывается в процессе обработки метода [функции IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) объекта поддержки, который создает поставщика хранилища сообщений во время обработки [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) или **IUnknown MAPI:: Выпуск** вызова метода на объект хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="57519-117">In this case, **IMSLogon::Logoff** is called as part of MAPI processing the [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method of the support object that the message store provider creates while it is processing an [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) or **IUnknown::Release** method call on a message store object.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="57519-118">См. также</span><span class="sxs-lookup"><span data-stu-id="57519-118">See also</span></span>



[<span data-ttu-id="57519-119">IMAPISession::Logoff</span><span class="sxs-lookup"><span data-stu-id="57519-119">IMAPISession::Logoff</span></span>](imapisession-logoff.md)
  
[<span data-ttu-id="57519-120">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="57519-120">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)
  
[<span data-ttu-id="57519-121">IMsgStore::StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="57519-121">IMsgStore::StoreLogoff</span></span>](imsgstore-storelogoff.md)
  
[<span data-ttu-id="57519-122">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="57519-122">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="57519-123">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="57519-123">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="57519-124">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="57519-124">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

