---
title: иксплогонполл
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
# <a name="ixplogonpoll"></a><span data-ttu-id="0dacb-103">IXPLogon::Poll</span><span class="sxs-lookup"><span data-stu-id="0dacb-103">IXPLogon::Poll</span></span>

  
  
<span data-ttu-id="0dacb-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0dacb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0dacb-105">Указывает, получил ли поставщик транспорта одно или несколько входящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="0dacb-105">Indicates whether the transport provider has received one or more inbound messages.</span></span>
  
```cpp
HRESULT Poll(
  ULONG FAR * lpulIncoming
);
```

## <a name="parameters"></a><span data-ttu-id="0dacb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0dacb-106">Parameters</span></span>

 <span data-ttu-id="0dacb-107">_лпулинкоминг_</span><span class="sxs-lookup"><span data-stu-id="0dacb-107">_lpulIncoming_</span></span>
  
> <span data-ttu-id="0dacb-108">вышли Значение, указывающее на наличие входящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="0dacb-108">[out] A value that indicates the existence of inbound messages.</span></span> <span data-ttu-id="0dacb-109">Ненулевое значение указывает на наличие входящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="0dacb-109">A nonzero value indicates that there are inbound messages.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0dacb-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0dacb-110">Return value</span></span>

<span data-ttu-id="0dacb-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="0dacb-111">S_OK</span></span> 
  
> <span data-ttu-id="0dacb-112">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="0dacb-112">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0dacb-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="0dacb-113">Remarks</span></span>

<span data-ttu-id="0dacb-114">Диспетчер очереди MAPI периодически вызывает метод **иксплогон::P олл** , если поставщик транспорта указывает, что он должен опрашиваться на наличие новых сообщений, которые поставщик выполняет, передав флаг LOGON_SP_POLL в вызов метода [Иксппровидер:: транспортлогон](ixpprovider-transportlogon.md) в начале сеанса.</span><span class="sxs-lookup"><span data-stu-id="0dacb-114">The MAPI spooler periodically calls the **IXPLogon::Poll** method if the transport provider indicates it must be polled for new messages, which the provider does by passing the LOGON_SP_POLL flag to the call to the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method at the beginning of a session.</span></span> <span data-ttu-id="0dacb-115">Если поставщик транспорта указывает в ответ на вызов **опроса** , для обработки которого доступно одно или несколько входящих сообщений, то диспетчер очереди MAPI вызывает метод [Иксплогон:: стартмессаже](ixplogon-startmessage.md) , который позволяет поставщику обработать первое входящее сообщение.</span><span class="sxs-lookup"><span data-stu-id="0dacb-115">If the transport provider indicates in response to the **Poll** call that there are one or more inbound messages available for it to process, the MAPI spooler calls the [IXPLogon::StartMessage](ixplogon-startmessage.md) method to allow the provider to process the first inbound message.</span></span> <span data-ttu-id="0dacb-116">Поставщик транспорта указывает на входящие сообщения, присвоив параметру _лпулинкоминг_ значение ненулевого значения.</span><span class="sxs-lookup"><span data-stu-id="0dacb-116">The transport provider indicates inbound messages by setting the value in the  _lpulIncoming_ parameter to a nonzero value.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0dacb-117">См. также</span><span class="sxs-lookup"><span data-stu-id="0dacb-117">See also</span></span>



[<span data-ttu-id="0dacb-118">IXPLogon::StartMessage</span><span class="sxs-lookup"><span data-stu-id="0dacb-118">IXPLogon::StartMessage</span></span>](ixplogon-startmessage.md)
  
[<span data-ttu-id="0dacb-119">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="0dacb-119">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="0dacb-120">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0dacb-120">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

