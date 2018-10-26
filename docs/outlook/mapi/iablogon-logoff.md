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
ms.openlocfilehash: a20fdd45c39cc2147f8fdc7b1998ff6d1b0797bb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586209"
---
# <a name="iablogonlogoff"></a><span data-ttu-id="c6eac-103">IABLogon::Logoff</span><span class="sxs-lookup"><span data-stu-id="c6eac-103">IABLogon::Logoff</span></span>

  
  
<span data-ttu-id="c6eac-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c6eac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c6eac-105">Запускает процесс выхода из системы.</span><span class="sxs-lookup"><span data-stu-id="c6eac-105">Initiates the logoff process.</span></span>
  
```cpp
HRESULT Logoff(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="c6eac-106">���������</span><span class="sxs-lookup"><span data-stu-id="c6eac-106">Parameters</span></span>

 <span data-ttu-id="c6eac-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c6eac-107">_ulFlags_</span></span>
  
> <span data-ttu-id="c6eac-108">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="c6eac-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c6eac-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c6eac-109">Return value</span></span>

<span data-ttu-id="c6eac-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="c6eac-110">S_OK</span></span> 
  
> <span data-ttu-id="c6eac-111">Процесс выхода из системы успешно инициировано.</span><span class="sxs-lookup"><span data-stu-id="c6eac-111">The logoff process was successfully initiated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c6eac-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="c6eac-112">Remarks</span></span>

<span data-ttu-id="c6eac-113">Процесс выхода из системы обычно запускается, когда клиент вызывает метод [IMAPISession::Logoff](imapisession-logoff.md) , чтобы завершить сеанс.</span><span class="sxs-lookup"><span data-stu-id="c6eac-113">The logoff process is typically started when a client calls the [IMAPISession::Logoff](imapisession-logoff.md) method to end a session.</span></span> <span data-ttu-id="c6eac-114">MAPI затем вызывает метод **IABLogon::Logoff** каждой адресной книге для начала процесса выхода из системы.</span><span class="sxs-lookup"><span data-stu-id="c6eac-114">MAPI then calls each address book provider's **IABLogon::Logoff** method to start the logoff process.</span></span> 
  
<span data-ttu-id="c6eac-115">Метод **IABLogon::Logoff** выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="c6eac-115">The **IABLogon::Logoff** method does the following:</span></span> 
  
- <span data-ttu-id="c6eac-116">Освобождает все открытые объекты, такие как вложенными объектами или объекта состояния.</span><span class="sxs-lookup"><span data-stu-id="c6eac-116">Releases all open objects, such as any subobjects or the status object.</span></span>
    
- <span data-ttu-id="c6eac-117">Освобождает объект поддержки поставщика.</span><span class="sxs-lookup"><span data-stu-id="c6eac-117">Releases the provider's support object.</span></span>
    
<span data-ttu-id="c6eac-118">Дополнительные сведения о процессе logoff поставщиками адресных книг видеть [Завершает работу поставщика услуг](shutting-down-a-service-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c6eac-118">For more information about the logoff process of address book providers, see [Shutting Down a Service Provider](shutting-down-a-service-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c6eac-119">См. также</span><span class="sxs-lookup"><span data-stu-id="c6eac-119">See also</span></span>



[<span data-ttu-id="c6eac-120">IABProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="c6eac-120">IABProvider::Logon</span></span>](iabprovider-logon.md)
  
[<span data-ttu-id="c6eac-121">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c6eac-121">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

