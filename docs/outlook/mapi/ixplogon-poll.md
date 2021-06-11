---
title: IXPLogonPoll
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.Poll
api_type:
- COM
ms.assetid: 1524eb06-7492-42de-b455-e0982bda7ece
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 3e68c564357880b623e02081a228e881c084fa94
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425276"
---
# <a name="ixplogonpoll"></a><span data-ttu-id="11710-103">IXPLogon::Poll</span><span class="sxs-lookup"><span data-stu-id="11710-103">IXPLogon::Poll</span></span>

  
  
<span data-ttu-id="11710-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="11710-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="11710-105">Указывает, получил ли поставщик транспорта одно или несколько входящие сообщения.</span><span class="sxs-lookup"><span data-stu-id="11710-105">Indicates whether the transport provider has received one or more inbound messages.</span></span>
  
```cpp
HRESULT Poll(
  ULONG FAR * lpulIncoming
);
```

## <a name="parameters"></a><span data-ttu-id="11710-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="11710-106">Parameters</span></span>

 <span data-ttu-id="11710-107">_lpulIncoming_</span><span class="sxs-lookup"><span data-stu-id="11710-107">_lpulIncoming_</span></span>
  
> <span data-ttu-id="11710-108">[вышел] Значение, которое указывает на наличие входящие сообщения.</span><span class="sxs-lookup"><span data-stu-id="11710-108">[out] A value that indicates the existence of inbound messages.</span></span> <span data-ttu-id="11710-109">Значение nonzero указывает на входящие сообщения.</span><span class="sxs-lookup"><span data-stu-id="11710-109">A nonzero value indicates that there are inbound messages.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="11710-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="11710-110">Return value</span></span>

<span data-ttu-id="11710-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="11710-111">S_OK</span></span> 
  
> <span data-ttu-id="11710-112">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="11710-112">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="11710-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="11710-113">Remarks</span></span>

<span data-ttu-id="11710-114">Шпалер MAPI периодически вызывает метод **IXPLogon::P oll,** если поставщик транспорта указывает, что он должен быть оповещен о новых сообщениях, которые поставщик делает, передав флаг LOGON_SP_POLL вызову [методу IXPProvider::TransportLogon](ixpprovider-transportlogon.md) в начале сеанса.</span><span class="sxs-lookup"><span data-stu-id="11710-114">The MAPI spooler periodically calls the **IXPLogon::Poll** method if the transport provider indicates it must be polled for new messages, which the provider does by passing the LOGON_SP_POLL flag to the call to the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method at the beginning of a session.</span></span> <span data-ttu-id="11710-115">Если поставщик транспорта указывает в ответ на вызов **Poll,** что для обработки доступно одно или несколько входящие сообщения, пуллер MAPI вызывает [метод IXPLogon::StartMessage,](ixplogon-startmessage.md) чтобы разрешить поставщику обрабатывать первое входящий сообщение.</span><span class="sxs-lookup"><span data-stu-id="11710-115">If the transport provider indicates in response to the **Poll** call that there are one or more inbound messages available for it to process, the MAPI spooler calls the [IXPLogon::StartMessage](ixplogon-startmessage.md) method to allow the provider to process the first inbound message.</span></span> <span data-ttu-id="11710-116">Поставщик транспорта указывает входящие сообщения, установив значение параметра  _lpulIncoming_ к значению nonzero.</span><span class="sxs-lookup"><span data-stu-id="11710-116">The transport provider indicates inbound messages by setting the value in the  _lpulIncoming_ parameter to a nonzero value.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="11710-117">См. также</span><span class="sxs-lookup"><span data-stu-id="11710-117">See also</span></span>



[<span data-ttu-id="11710-118">IXPLogon::StartMessage</span><span class="sxs-lookup"><span data-stu-id="11710-118">IXPLogon::StartMessage</span></span>](ixplogon-startmessage.md)
  
[<span data-ttu-id="11710-119">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="11710-119">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="11710-120">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="11710-120">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

