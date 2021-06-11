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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348876"
---
# <a name="imslogonlogoff"></a><span data-ttu-id="5adf1-103">IMSLogon::Logoff</span><span class="sxs-lookup"><span data-stu-id="5adf1-103">IMSLogon::Logoff</span></span>

  
  
<span data-ttu-id="5adf1-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5adf1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5adf1-105">Журналы поставщика магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="5adf1-105">Logs off a message store provider.</span></span> 
  
```cpp
HRESULT Logoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="5adf1-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="5adf1-106">Parameters</span></span>

 <span data-ttu-id="5adf1-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="5adf1-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="5adf1-108">[in] Зарезервировано; должно быть указателем на ноль.</span><span class="sxs-lookup"><span data-stu-id="5adf1-108">[in] Reserved; must be a pointer to zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5adf1-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5adf1-109">Return value</span></span>

<span data-ttu-id="5adf1-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="5adf1-110">S_OK</span></span> 
  
> <span data-ttu-id="5adf1-111">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="5adf1-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5adf1-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="5adf1-112">Remarks</span></span>

<span data-ttu-id="5adf1-113">Поставщики магазинов сообщений реализуют **метод IMSLogon::Logoff** для принудительного отключения поставщика магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="5adf1-113">Message store providers implement the **IMSLogon::Logoff** method to forcibly shut down a message store provider.</span></span> <span data-ttu-id="5adf1-114">**IMSLogon::Logoff** вызван в следующих ситуациях:</span><span class="sxs-lookup"><span data-stu-id="5adf1-114">**IMSLogon::Logoff** is called in the following situations:</span></span> 
  
- <span data-ttu-id="5adf1-115">Хотя MAPI отключает клиента после вызова метода [IMAPISession::Logoff.](imapisession-logoff.md)</span><span class="sxs-lookup"><span data-stu-id="5adf1-115">While MAPI is logging off a client after a call to the [IMAPISession::Logoff](imapisession-logoff.md) method.</span></span> 
    
- <span data-ttu-id="5adf1-116">В то время как MAPI отключается от поставщика магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="5adf1-116">While MAPI is logging off a message store provider.</span></span> <span data-ttu-id="5adf1-117">В этом случае **IMSLogon::Logoff** называется частью обработки [метода MAPI IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) объекта поддержки, создаваемого поставщиком магазина сообщений при обработке [метода IMsgStore::StoreLogoff](imsgstore-storelogoff.md) или **метода IUnknown::Release** на объекте магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="5adf1-117">In this case, **IMSLogon::Logoff** is called as part of MAPI processing the [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method of the support object that the message store provider creates while it is processing an [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) or **IUnknown::Release** method call on a message store object.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="5adf1-118">См. также</span><span class="sxs-lookup"><span data-stu-id="5adf1-118">See also</span></span>



[<span data-ttu-id="5adf1-119">IMAPISession::Logoff</span><span class="sxs-lookup"><span data-stu-id="5adf1-119">IMAPISession::Logoff</span></span>](imapisession-logoff.md)
  
[<span data-ttu-id="5adf1-120">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="5adf1-120">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)
  
[<span data-ttu-id="5adf1-121">IMsgStore::StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="5adf1-121">IMsgStore::StoreLogoff</span></span>](imsgstore-storelogoff.md)
  
[<span data-ttu-id="5adf1-122">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="5adf1-122">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="5adf1-123">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="5adf1-123">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="5adf1-124">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5adf1-124">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

