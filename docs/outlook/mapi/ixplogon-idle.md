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
ms.openlocfilehash: 75607550f1d6085a670ad997238994400e08f7bd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809630"
---
# <a name="ixplogonidle"></a><span data-ttu-id="0bc11-103">IXPLogon::Idle</span><span class="sxs-lookup"><span data-stu-id="0bc11-103">IXPLogon::Idle</span></span>

  
  
<span data-ttu-id="0bc11-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0bc11-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0bc11-105">Указывает, что система не занята, включив поставщика транспорта для выполнения операций с низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="0bc11-105">Indicates that the system is idle, enabling the transport provider to perform low-priority operations.</span></span>
  
```cpp
HRESULT Idle(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="0bc11-106">���������</span><span class="sxs-lookup"><span data-stu-id="0bc11-106">Parameters</span></span>

 <span data-ttu-id="0bc11-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0bc11-107">_ulFlags_</span></span>
  
> <span data-ttu-id="0bc11-108">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="0bc11-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0bc11-109">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="0bc11-109">Return value</span></span>

<span data-ttu-id="0bc11-110">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="0bc11-110">S_OK</span></span> 
  
> <span data-ttu-id="0bc11-111">Вызов успешно и возвращается ожидаемым значением или значения.</span><span class="sxs-lookup"><span data-stu-id="0bc11-111">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0bc11-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="0bc11-112">Remarks</span></span>

<span data-ttu-id="0bc11-113">Диспетчер очереди MAPI периодически вызывает метод **IXPLogon::Idle** , если запрошен периоды времени, когда система не занята, передав флаг XP_LOGON_SP в вызове метода [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) , которая открыта в текущем сеансе.</span><span class="sxs-lookup"><span data-stu-id="0bc11-113">The MAPI spooler periodically calls the **IXPLogon::Idle** method, if requested, during times when the system is idle by passing the XP_LOGON_SP flag in the call to the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method that opened the current session.</span></span> <span data-ttu-id="0bc11-114">В некоторых случаях, когда система не занята, поставщика транспорта можно выполнить фоновых операций, которые не соответствуют во время других вызовов или, необходимо повторить на регулярной основе.</span><span class="sxs-lookup"><span data-stu-id="0bc11-114">At times when the system is idle, the transport provider can perform background operations that are not appropriate during other calls, or that need to occur on a regular basis.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0bc11-115">См. также</span><span class="sxs-lookup"><span data-stu-id="0bc11-115">See also</span></span>



[<span data-ttu-id="0bc11-116">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="0bc11-116">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="0bc11-117">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0bc11-117">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

