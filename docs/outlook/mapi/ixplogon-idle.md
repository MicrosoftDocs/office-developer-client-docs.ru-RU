---
title: Иксплогонидле
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.Idle
api_type:
- COM
ms.assetid: 8f600db6-f6a6-44f9-aef7-c1309f61eb12
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: ceca6a2dbe5f80f8a3499e509db8d5e6c35d72d0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32298483"
---
# <a name="ixplogonidle"></a><span data-ttu-id="79b9f-103">IXPLogon::Idle</span><span class="sxs-lookup"><span data-stu-id="79b9f-103">IXPLogon::Idle</span></span>

  
  
<span data-ttu-id="79b9f-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="79b9f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="79b9f-105">Указывает на то, что система находится в режиме бездействия, что позволяет поставщику транспорта выполнять операции с низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="79b9f-105">Indicates that the system is idle, enabling the transport provider to perform low-priority operations.</span></span>
  
```cpp
HRESULT Idle(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="79b9f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="79b9f-106">Parameters</span></span>

 <span data-ttu-id="79b9f-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="79b9f-107">_ulFlags_</span></span>
  
> <span data-ttu-id="79b9f-108">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="79b9f-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="79b9f-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="79b9f-109">Return value</span></span>

<span data-ttu-id="79b9f-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="79b9f-110">S_OK</span></span> 
  
> <span data-ttu-id="79b9f-111">Вызов выполнен успешно и вернул ожидаемое значение или значения.</span><span class="sxs-lookup"><span data-stu-id="79b9f-111">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="79b9f-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="79b9f-112">Remarks</span></span>

<span data-ttu-id="79b9f-113">Диспетчер очереди MAPI периодически вызывает метод **иксплогон:: Idle** при запросе, когда система простаивает, ПЕРЕДАВ флаг ксп_логон_сп в вызове метода [Иксппровидер:: транспортлогон](ixpprovider-transportlogon.md) , который открыл текущий сеанс.</span><span class="sxs-lookup"><span data-stu-id="79b9f-113">The MAPI spooler periodically calls the **IXPLogon::Idle** method, if requested, during times when the system is idle by passing the XP_LOGON_SP flag in the call to the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method that opened the current session.</span></span> <span data-ttu-id="79b9f-114">Иногда при простое системы поставщик транспорта может выполнять фоновые операции, которые не подходят для других вызовов, или которые должны выполняться на регулярной основе.</span><span class="sxs-lookup"><span data-stu-id="79b9f-114">At times when the system is idle, the transport provider can perform background operations that are not appropriate during other calls, or that need to occur on a regular basis.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="79b9f-115">См. также</span><span class="sxs-lookup"><span data-stu-id="79b9f-115">See also</span></span>



[<span data-ttu-id="79b9f-116">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="79b9f-116">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="79b9f-117">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="79b9f-117">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

