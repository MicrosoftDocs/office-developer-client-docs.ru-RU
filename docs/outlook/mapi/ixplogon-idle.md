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
ms.openlocfilehash: ceca6a2dbe5f80f8a3499e509db8d5e6c35d72d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436050"
---
# <a name="ixplogonidle"></a><span data-ttu-id="bf98e-103">IXPLogon::Idle</span><span class="sxs-lookup"><span data-stu-id="bf98e-103">IXPLogon::Idle</span></span>

  
  
<span data-ttu-id="bf98e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bf98e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bf98e-105">Указывает, что система простаивает, что позволяет поставщику транспорта выполнять операции с низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="bf98e-105">Indicates that the system is idle, enabling the transport provider to perform low-priority operations.</span></span>
  
```cpp
HRESULT Idle(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="bf98e-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="bf98e-106">Parameters</span></span>

 <span data-ttu-id="bf98e-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="bf98e-107">_ulFlags_</span></span>
  
> <span data-ttu-id="bf98e-108">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="bf98e-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bf98e-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bf98e-109">Return value</span></span>

<span data-ttu-id="bf98e-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="bf98e-110">S_OK</span></span> 
  
> <span data-ttu-id="bf98e-111">Вызов удался и возвращает ожидаемое значение или значения.</span><span class="sxs-lookup"><span data-stu-id="bf98e-111">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bf98e-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="bf98e-112">Remarks</span></span>

<span data-ttu-id="bf98e-113">Шпалер MAPI периодически вызывает метод **IXPLogon::Idle,** если это необходимо, в периоды, когда система простаивает, передав флаг XP_LOGON_SP в вызов [методу IXPProvider::TransportLogon,](ixpprovider-transportlogon.md) открывающим текущий сеанс.</span><span class="sxs-lookup"><span data-stu-id="bf98e-113">The MAPI spooler periodically calls the **IXPLogon::Idle** method, if requested, during times when the system is idle by passing the XP_LOGON_SP flag in the call to the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method that opened the current session.</span></span> <span data-ttu-id="bf98e-114">В периоды, когда система простаивает, поставщик транспорта может выполнять фоновые операции, которые не подходят во время других вызовов или которые должны выполняться на регулярной основе.</span><span class="sxs-lookup"><span data-stu-id="bf98e-114">At times when the system is idle, the transport provider can perform background operations that are not appropriate during other calls, or that need to occur on a regular basis.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bf98e-115">См. также</span><span class="sxs-lookup"><span data-stu-id="bf98e-115">See also</span></span>



[<span data-ttu-id="bf98e-116">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="bf98e-116">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="bf98e-117">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bf98e-117">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

