---
title: IABLogonLogoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.Logoff
api_type:
- COM
ms.assetid: a36465e2-7be9-4bd6-8091-685f0a045aa9
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: af3c1f5135e90274c0251c5a0addf339c14f36c0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416400"
---
# <a name="iablogonlogoff"></a><span data-ttu-id="ecf0b-103">IABLogon::Logoff</span><span class="sxs-lookup"><span data-stu-id="ecf0b-103">IABLogon::Logoff</span></span>

  
  
<span data-ttu-id="ecf0b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ecf0b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ecf0b-105">Инициирует процесс входа.</span><span class="sxs-lookup"><span data-stu-id="ecf0b-105">Initiates the logoff process.</span></span>
  
```cpp
HRESULT Logoff(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="ecf0b-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="ecf0b-106">Parameters</span></span>

 <span data-ttu-id="ecf0b-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ecf0b-107">_ulFlags_</span></span>
  
> <span data-ttu-id="ecf0b-108">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="ecf0b-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ecf0b-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ecf0b-109">Return value</span></span>

<span data-ttu-id="ecf0b-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="ecf0b-110">S_OK</span></span> 
  
> <span data-ttu-id="ecf0b-111">Успешно начался процесс входа.</span><span class="sxs-lookup"><span data-stu-id="ecf0b-111">The logoff process was successfully initiated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ecf0b-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="ecf0b-112">Remarks</span></span>

<span data-ttu-id="ecf0b-113">Процесс входа обычно начинается, когда клиент вызывает [метод IMAPISession::Logoff](imapisession-logoff.md) для окончания сеанса.</span><span class="sxs-lookup"><span data-stu-id="ecf0b-113">The logoff process is typically started when a client calls the [IMAPISession::Logoff](imapisession-logoff.md) method to end a session.</span></span> <span data-ttu-id="ecf0b-114">Затем MAPI вызывает метод **IABLogon::Logoff** каждого поставщика адресной книги, чтобы запустить процесс входа.</span><span class="sxs-lookup"><span data-stu-id="ecf0b-114">MAPI then calls each address book provider's **IABLogon::Logoff** method to start the logoff process.</span></span> 
  
<span data-ttu-id="ecf0b-115">Метод **IABLogon::Logoff** делает следующее:</span><span class="sxs-lookup"><span data-stu-id="ecf0b-115">The **IABLogon::Logoff** method does the following:</span></span> 
  
- <span data-ttu-id="ecf0b-116">Освобождает все открытые объекты, такие как любые подобекты или объект состояния.</span><span class="sxs-lookup"><span data-stu-id="ecf0b-116">Releases all open objects, such as any subobjects or the status object.</span></span>
    
- <span data-ttu-id="ecf0b-117">Освобождает объект поддержки поставщика.</span><span class="sxs-lookup"><span data-stu-id="ecf0b-117">Releases the provider's support object.</span></span>
    
<span data-ttu-id="ecf0b-118">Дополнительные сведения о процессе входа поставщиков адресных книг см. в книге [Shutting Down a Service Provider.](shutting-down-a-service-provider.md)</span><span class="sxs-lookup"><span data-stu-id="ecf0b-118">For more information about the logoff process of address book providers, see [Shutting Down a Service Provider](shutting-down-a-service-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ecf0b-119">См. также</span><span class="sxs-lookup"><span data-stu-id="ecf0b-119">See also</span></span>



[<span data-ttu-id="ecf0b-120">IABProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="ecf0b-120">IABProvider::Logon</span></span>](iabprovider-logon.md)
  
[<span data-ttu-id="ecf0b-121">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ecf0b-121">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

