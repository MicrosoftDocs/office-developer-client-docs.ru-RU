---
title: имслогонлогофф
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
# <a name="imslogonlogoff"></a><span data-ttu-id="358ef-103">IMSLogon::Logoff</span><span class="sxs-lookup"><span data-stu-id="358ef-103">IMSLogon::Logoff</span></span>

  
  
<span data-ttu-id="358ef-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="358ef-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="358ef-105">Выполняет выход из системы поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="358ef-105">Logs off a message store provider.</span></span> 
  
```cpp
HRESULT Logoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="358ef-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="358ef-106">Parameters</span></span>

 <span data-ttu-id="358ef-107">_лпулфлагс_</span><span class="sxs-lookup"><span data-stu-id="358ef-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="358ef-108">возврата Резервирования должен быть нулевым указателем.</span><span class="sxs-lookup"><span data-stu-id="358ef-108">[in] Reserved; must be a pointer to zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="358ef-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="358ef-109">Return value</span></span>

<span data-ttu-id="358ef-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="358ef-110">S_OK</span></span> 
  
> <span data-ttu-id="358ef-111">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="358ef-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="358ef-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="358ef-112">Remarks</span></span>

<span data-ttu-id="358ef-113">Поставщики хранилища сообщений реализуют метод **имслогон:: logoff** для принудительного завершения работы поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="358ef-113">Message store providers implement the **IMSLogon::Logoff** method to forcibly shut down a message store provider.</span></span> <span data-ttu-id="358ef-114">**Имслогон:: logoff** вызывается в следующих ситуациях:</span><span class="sxs-lookup"><span data-stu-id="358ef-114">**IMSLogon::Logoff** is called in the following situations:</span></span> 
  
- <span data-ttu-id="358ef-115">В то время как MAPI записывает клиент после вызова метода [IMAPISession:: logoff](imapisession-logoff.md) .</span><span class="sxs-lookup"><span data-stu-id="358ef-115">While MAPI is logging off a client after a call to the [IMAPISession::Logoff](imapisession-logoff.md) method.</span></span> 
    
- <span data-ttu-id="358ef-116">В то время как MAPI записывает поставщик хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="358ef-116">While MAPI is logging off a message store provider.</span></span> <span data-ttu-id="358ef-117">В этом случае **имслогон:: logoff** вызывается как часть обработки MAPI метода [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) объекта support, создаваемого поставщиком хранилища сообщений при обработке метода [IMsgStore:: Сторелогофф](imsgstore-storelogoff.md) или **IUnknown:: Release** для объекта хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="358ef-117">In this case, **IMSLogon::Logoff** is called as part of MAPI processing the [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method of the support object that the message store provider creates while it is processing an [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) or **IUnknown::Release** method call on a message store object.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="358ef-118">См. также</span><span class="sxs-lookup"><span data-stu-id="358ef-118">See also</span></span>



[<span data-ttu-id="358ef-119">IMAPISession::Logoff</span><span class="sxs-lookup"><span data-stu-id="358ef-119">IMAPISession::Logoff</span></span>](imapisession-logoff.md)
  
[<span data-ttu-id="358ef-120">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="358ef-120">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)
  
[<span data-ttu-id="358ef-121">IMsgStore::StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="358ef-121">IMsgStore::StoreLogoff</span></span>](imsgstore-storelogoff.md)
  
[<span data-ttu-id="358ef-122">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="358ef-122">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="358ef-123">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="358ef-123">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="358ef-124">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="358ef-124">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

