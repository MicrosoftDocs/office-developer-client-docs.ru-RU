---
title: Иксплогонтранспортлогофф
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.TransportLogoff
api_type:
- COM
ms.assetid: b2b368ce-4486-4f90-985f-59e50ca95229
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 78b4feeca263035b9c90184f10edd294e6cd7b10
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351585"
---
# <a name="ixplogontransportlogoff"></a><span data-ttu-id="b054a-103">IXPLogon::TransportLogoff</span><span class="sxs-lookup"><span data-stu-id="b054a-103">IXPLogon::TransportLogoff</span></span>

  
  
<span data-ttu-id="b054a-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b054a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b054a-105">Инициирует процесс выхода из системы.</span><span class="sxs-lookup"><span data-stu-id="b054a-105">Initiates the logoff process.</span></span> 
  
```cpp
HRESULT TransportLogoff(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="b054a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b054a-106">Parameters</span></span>

 <span data-ttu-id="b054a-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b054a-107">_ulFlags_</span></span>
  
> <span data-ttu-id="b054a-108">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="b054a-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b054a-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b054a-109">Return value</span></span>

<span data-ttu-id="b054a-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="b054a-110">S_OK</span></span> 
  
> <span data-ttu-id="b054a-111">Вызов выполнен успешно и вернул ожидаемое значение или значения.</span><span class="sxs-lookup"><span data-stu-id="b054a-111">The call succeeded and returned the expected value or values.</span></span> <span data-ttu-id="b054a-112">Если возвращено значение, отличное от S_OK, то поставщик вышел из системы.</span><span class="sxs-lookup"><span data-stu-id="b054a-112">If anything other than S_OK is returned, the provider is logged off.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b054a-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="b054a-113">Remarks</span></span>

<span data-ttu-id="b054a-114">Диспетчер очереди MAPI вызывает метод **иксплогон:: транспортлогофф** для завершения сеанса поставщика транспорта для определенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="b054a-114">The MAPI spooler calls the **IXPLogon::TransportLogoff** method to terminate a transport provider session for a particular user.</span></span> <span data-ttu-id="b054a-115">Перед вызовом **транспортлогофф**Диспетчер очереди MAPI отбрасывает все данные о поддерживаемых типах адресов обмена сообщениями для этого сеанса, переданного в методе [Иксплогон:: аддресстипес](ixplogon-addresstypes.md) .</span><span class="sxs-lookup"><span data-stu-id="b054a-115">Before calling **TransportLogoff**, the MAPI spooler discards any data about supported messaging address types for this session passed in the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="b054a-116">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="b054a-116">Notes to implementers</span></span>

<span data-ttu-id="b054a-117">Поставщик транспорта должен быть готов к приему вызова **транспортлогофф** в любое время.</span><span class="sxs-lookup"><span data-stu-id="b054a-117">The transport provider should be prepared to accept a call to **TransportLogoff** at any time.</span></span> <span data-ttu-id="b054a-118">Если сообщение находится в процессе, поставщик должен остановить процесс отправки.</span><span class="sxs-lookup"><span data-stu-id="b054a-118">If a message is in process, the provider should stop the sending process.</span></span> 
  
<span data-ttu-id="b054a-119">Поставщик транспорта должен освободить все ресурсы, выделенные для текущего сеанса.</span><span class="sxs-lookup"><span data-stu-id="b054a-119">The transport provider should release all resources allocated for its current session.</span></span> <span data-ttu-id="b054a-120">Если для этого сеанса выделяется память с помощью функции [мапиаллокатебуффер](mapiallocatebuffer.md) , она должна освободить память с помощью функции [мапифрибуффер](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="b054a-120">If it has allocated any memory for this session with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, it should free the memory by using the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> <span data-ttu-id="b054a-121">Любая память, выделенная поставщиком транспорта для удовлетворения вызовов метода [иксплогон:: аддресстипес](ixplogon-addresstypes.md) , может быть безопасно выпущена в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="b054a-121">Any memory allocated by the transport provider to satisfy calls to the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method can be safely released at this time.</span></span> 
  
<span data-ttu-id="b054a-122">Как правило, при завершении вызова **транспортлогофф** поставщик должен сначала сделать его объектом logon, вызвав метод [Имаписуппорт:: макеинвалид](imapisupport-makeinvalid.md) , а затем отпустить его объект поддержки.</span><span class="sxs-lookup"><span data-stu-id="b054a-122">Usually, on completing a **TransportLogoff** call, a provider should first invalidate its logon object by calling the [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) method and then release its support object.</span></span> <span data-ttu-id="b054a-123">Реализация поставщика **транспортлогофф** должна освобождать объект поддержки последним, так как при отпускании объекта support Диспетчер очереди MAPI также может освободить сам объект поставщика.</span><span class="sxs-lookup"><span data-stu-id="b054a-123">The provider's implementation of **TransportLogoff** should release the support object last, because when the support object is released, the MAPI spooler can also release the provider object itself.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b054a-124">См. также</span><span class="sxs-lookup"><span data-stu-id="b054a-124">See also</span></span>



[<span data-ttu-id="b054a-125">IMAPISupport::MakeInvalid</span><span class="sxs-lookup"><span data-stu-id="b054a-125">IMAPISupport::MakeInvalid</span></span>](imapisupport-makeinvalid.md)
  
[<span data-ttu-id="b054a-126">IMAPISupport::SpoolerYield</span><span class="sxs-lookup"><span data-stu-id="b054a-126">IMAPISupport::SpoolerYield</span></span>](imapisupport-spooleryield.md)
  
[<span data-ttu-id="b054a-127">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="b054a-127">IXPLogon::AddressTypes</span></span>](ixplogon-addresstypes.md)
  
[<span data-ttu-id="b054a-128">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="b054a-128">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="b054a-129">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="b054a-129">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="b054a-130">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b054a-130">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

