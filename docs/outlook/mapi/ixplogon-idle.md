---
title: IXPLogonIdle
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
ms.openlocfilehash: 12aa8b79e38320d9767a6c333cb0197ea5669862
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578016"
---
# <a name="ixplogonidle"></a><span data-ttu-id="04abb-103">IXPLogon::Idle</span><span class="sxs-lookup"><span data-stu-id="04abb-103">IXPLogon::Idle</span></span>

  
  
<span data-ttu-id="04abb-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="04abb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="04abb-105">Указывает, что система не занята, включив поставщика транспорта для выполнения операций с низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="04abb-105">Indicates that the system is idle, enabling the transport provider to perform low-priority operations.</span></span>
  
```cpp
HRESULT Idle(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="04abb-106">���������</span><span class="sxs-lookup"><span data-stu-id="04abb-106">Parameters</span></span>

 <span data-ttu-id="04abb-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="04abb-107">_ulFlags_</span></span>
  
> <span data-ttu-id="04abb-108">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="04abb-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="04abb-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="04abb-109">Return value</span></span>

<span data-ttu-id="04abb-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="04abb-110">S_OK</span></span> 
  
> <span data-ttu-id="04abb-111">Вызов успешно и возвращается ожидаемым значением или значения.</span><span class="sxs-lookup"><span data-stu-id="04abb-111">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="04abb-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="04abb-112">Remarks</span></span>

<span data-ttu-id="04abb-113">Диспетчер очереди MAPI периодически вызывает метод **IXPLogon::Idle** , если запрошен периоды времени, когда система не занята, передав флаг XP_LOGON_SP в вызове метода [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) , которая открыта в текущем сеансе.</span><span class="sxs-lookup"><span data-stu-id="04abb-113">The MAPI spooler periodically calls the **IXPLogon::Idle** method, if requested, during times when the system is idle by passing the XP_LOGON_SP flag in the call to the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method that opened the current session.</span></span> <span data-ttu-id="04abb-114">В некоторых случаях, когда система не занята, поставщика транспорта можно выполнить фоновых операций, которые не соответствуют во время других вызовов или, необходимо повторить на регулярной основе.</span><span class="sxs-lookup"><span data-stu-id="04abb-114">At times when the system is idle, the transport provider can perform background operations that are not appropriate during other calls, or that need to occur on a regular basis.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="04abb-115">См. также</span><span class="sxs-lookup"><span data-stu-id="04abb-115">See also</span></span>



[<span data-ttu-id="04abb-116">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="04abb-116">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="04abb-117">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="04abb-117">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

