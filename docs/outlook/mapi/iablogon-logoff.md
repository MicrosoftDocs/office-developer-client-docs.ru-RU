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
ms.openlocfilehash: e441e84e0bddff2e5a989849dbcf593320340d2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808727"
---
# <a name="iablogonlogoff"></a><span data-ttu-id="d8b9b-103">IABLogon::Logoff</span><span class="sxs-lookup"><span data-stu-id="d8b9b-103">IABLogon::Logoff</span></span>

  
  
<span data-ttu-id="d8b9b-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d8b9b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d8b9b-105">Запускает процесс выхода из системы.</span><span class="sxs-lookup"><span data-stu-id="d8b9b-105">Initiates the logoff process.</span></span>
  
```cpp
HRESULT Logoff(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="d8b9b-106">���������</span><span class="sxs-lookup"><span data-stu-id="d8b9b-106">Parameters</span></span>

 <span data-ttu-id="d8b9b-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d8b9b-107">_ulFlags_</span></span>
  
> <span data-ttu-id="d8b9b-108">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="d8b9b-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d8b9b-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9">Return value</span></span>

<span data-ttu-id="d8b9b-110">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="d8b9b-110">S_OK</span></span> 
  
> <span data-ttu-id="d8b9b-111">Процесс выхода из системы успешно инициировано.</span><span class="sxs-lookup"><span data-stu-id="d8b9b-111">The logoff process was successfully initiated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d8b9b-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="d8b9b-112">Remarks</span></span>

<span data-ttu-id="d8b9b-113">Процесс выхода из системы обычно запускается, когда клиент вызывает метод [IMAPISession::Logoff](imapisession-logoff.md) , чтобы завершить сеанс.</span><span class="sxs-lookup"><span data-stu-id="d8b9b-113">The logoff process is typically started when a client calls the [IMAPISession::Logoff](imapisession-logoff.md) method to end a session.</span></span> <span data-ttu-id="d8b9b-114">MAPI затем вызывает метод **IABLogon::Logoff** каждой адресной книге для начала процесса выхода из системы.</span><span class="sxs-lookup"><span data-stu-id="d8b9b-114">MAPI then calls each address book provider's **IABLogon::Logoff** method to start the logoff process.</span></span> 
  
<span data-ttu-id="d8b9b-115">Метод **IABLogon::Logoff** выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="d8b9b-115">The **IABLogon::Logoff** method does the following:</span></span> 
  
- <span data-ttu-id="d8b9b-116">Освобождает все открытые объекты, такие как вложенными объектами или объекта состояния.</span><span class="sxs-lookup"><span data-stu-id="d8b9b-116">Releases all open objects, such as any subobjects or the status object.</span></span>
    
- <span data-ttu-id="d8b9b-117">Освобождает объект поддержки поставщика.</span><span class="sxs-lookup"><span data-stu-id="d8b9b-117">Releases the provider's support object.</span></span>
    
<span data-ttu-id="d8b9b-118">Дополнительные сведения о процессе logoff поставщиками адресных книг видеть [Завершает работу поставщика услуг](shutting-down-a-service-provider.md).</span><span class="sxs-lookup"><span data-stu-id="d8b9b-118">For more information about the logoff process of address book providers, see [Shutting Down a Service Provider](shutting-down-a-service-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d8b9b-119">См. также</span><span class="sxs-lookup"><span data-stu-id="d8b9b-119">See also</span></span>



[<span data-ttu-id="d8b9b-120">IABProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="d8b9b-120">IABProvider::Logon</span></span>](iabprovider-logon.md)
  
[<span data-ttu-id="d8b9b-121">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d8b9b-121">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

