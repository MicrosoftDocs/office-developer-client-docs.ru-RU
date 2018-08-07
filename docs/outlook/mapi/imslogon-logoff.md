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
ms.openlocfilehash: 5d9a57cee371675493ba71b2df52b83941d34fc2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809439"
---
# <a name="imslogonlogoff"></a><span data-ttu-id="a7f25-103">IMSLogon::Logoff</span><span class="sxs-lookup"><span data-stu-id="a7f25-103">IMSLogon::Logoff</span></span>

  
  
<span data-ttu-id="a7f25-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a7f25-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a7f25-105">Поставщик хранилища, выходит из системы сообщение.</span><span class="sxs-lookup"><span data-stu-id="a7f25-105">Logs off a message store provider.</span></span> 
  
```cpp
HRESULT Logoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="a7f25-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a7f25-106">Parameters</span></span>

 <span data-ttu-id="a7f25-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="a7f25-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="a7f25-108">[in] Зарезервировано; должен быть указатель нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="a7f25-108">[in] Reserved; must be a pointer to zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a7f25-109">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="a7f25-109">Return value</span></span>

<span data-ttu-id="a7f25-110">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="a7f25-110">S_OK</span></span> 
  
> <span data-ttu-id="a7f25-111">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="a7f25-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a7f25-112">���������</span><span class="sxs-lookup"><span data-stu-id="a7f25-112">Remarks</span></span>

<span data-ttu-id="a7f25-113">Поставщики хранилища сообщений реализуйте метод **IMSLogon::Logoff** принудительно завершить работу поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="a7f25-113">Message store providers implement the **IMSLogon::Logoff** method to forcibly shut down a message store provider.</span></span> <span data-ttu-id="a7f25-114">**IMSLogon::Logoff** вызывается в следующих ситуациях:</span><span class="sxs-lookup"><span data-stu-id="a7f25-114">**IMSLogon::Logoff** is called in the following situations:</span></span> 
  
- <span data-ttu-id="a7f25-115">Во время MAPI выхода клиента после вызова метода [IMAPISession::Logoff](imapisession-logoff.md) .</span><span class="sxs-lookup"><span data-stu-id="a7f25-115">While MAPI is logging off a client after a call to the [IMAPISession::Logoff](imapisession-logoff.md) method.</span></span> 
    
- <span data-ttu-id="a7f25-116">Во время выхода поставщика хранилища сообщений MAPI.</span><span class="sxs-lookup"><span data-stu-id="a7f25-116">While MAPI is logging off a message store provider.</span></span> <span data-ttu-id="a7f25-117">В этом случае **IMSLogon::Logoff** вызывается в процессе обработки метода [функции IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) объекта поддержки, который создает поставщика хранилища сообщений во время обработки [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) или **IUnknown MAPI:: Выпуск** вызова метода на объект хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="a7f25-117">In this case, **IMSLogon::Logoff** is called as part of MAPI processing the [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) method of the support object that the message store provider creates while it is processing an [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) or **IUnknown::Release** method call on a message store object.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="a7f25-118">См. также</span><span class="sxs-lookup"><span data-stu-id="a7f25-118">See also</span></span>



[<span data-ttu-id="a7f25-119">IMAPISession::Logoff</span><span class="sxs-lookup"><span data-stu-id="a7f25-119">IMAPISession::Logoff</span></span>](imapisession-logoff.md)
  
[<span data-ttu-id="a7f25-120">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="a7f25-120">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)
  
[<span data-ttu-id="a7f25-121">IMsgStore::StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="a7f25-121">IMsgStore::StoreLogoff</span></span>](imsgstore-storelogoff.md)
  
[<span data-ttu-id="a7f25-122">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="a7f25-122">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="a7f25-123">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="a7f25-123">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="a7f25-124">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a7f25-124">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

