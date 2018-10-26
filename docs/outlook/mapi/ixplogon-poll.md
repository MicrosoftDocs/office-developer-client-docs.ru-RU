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
ms.openlocfilehash: 3426854e727ebce7a2ac2243491994ce0e066ac6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591382"
---
# <a name="ixplogonpoll"></a><span data-ttu-id="c363c-103">IXPLogon::Poll</span><span class="sxs-lookup"><span data-stu-id="c363c-103">IXPLogon::Poll</span></span>

  
  
<span data-ttu-id="c363c-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c363c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c363c-105">Указывает, поставщика транспорта, полученных одного или нескольких входящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="c363c-105">Indicates whether the transport provider has received one or more inbound messages.</span></span>
  
```cpp
HRESULT Poll(
  ULONG FAR * lpulIncoming
);
```

## <a name="parameters"></a><span data-ttu-id="c363c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c363c-106">Parameters</span></span>

 <span data-ttu-id="c363c-107">_lpulIncoming_</span><span class="sxs-lookup"><span data-stu-id="c363c-107">_lpulIncoming_</span></span>
  
> <span data-ttu-id="c363c-108">[out] Значение, указывающее на наличие входящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="c363c-108">[out] A value that indicates the existence of inbound messages.</span></span> <span data-ttu-id="c363c-109">Ненулевое значение указывает на наличие входящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="c363c-109">A nonzero value indicates that there are inbound messages.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c363c-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c363c-110">Return value</span></span>

<span data-ttu-id="c363c-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="c363c-111">S_OK</span></span> 
  
> <span data-ttu-id="c363c-112">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="c363c-112">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c363c-113">���������</span><span class="sxs-lookup"><span data-stu-id="c363c-113">Remarks</span></span>

<span data-ttu-id="c363c-114">Диспетчер очереди MAPI, периодически вызывает метод **IXPLogon::Poll** , если поставщик транспорта указывает, что должно быть запрошено для новых сообщений, которые поставщик, передав LOGON_SP_POLL флаг, вызов [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) метод в начале сеанса.</span><span class="sxs-lookup"><span data-stu-id="c363c-114">The MAPI spooler periodically calls the **IXPLogon::Poll** method if the transport provider indicates it must be polled for new messages, which the provider does by passing the LOGON_SP_POLL flag to the call to the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method at the beginning of a session.</span></span> <span data-ttu-id="c363c-115">Если указывает поставщика транспорта в ответ на звонок **опроса** , что есть один или более входящего сообщения об ошибках для его к процессу, диспетчер очереди MAPI вызывает метод [IXPLogon::StartMessage](ixplogon-startmessage.md) , чтобы разрешить поставщика к процессу первый входящий трафик Сообщение.</span><span class="sxs-lookup"><span data-stu-id="c363c-115">If the transport provider indicates in response to the **Poll** call that there are one or more inbound messages available for it to process, the MAPI spooler calls the [IXPLogon::StartMessage](ixplogon-startmessage.md) method to allow the provider to process the first inbound message.</span></span> <span data-ttu-id="c363c-116">Поставщика транспорта указывает входящих сообщений, указав значение с помощью параметра _lpulIncoming_ ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="c363c-116">The transport provider indicates inbound messages by setting the value in the  _lpulIncoming_ parameter to a nonzero value.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c363c-117">См. также</span><span class="sxs-lookup"><span data-stu-id="c363c-117">See also</span></span>



[<span data-ttu-id="c363c-118">IXPLogon::StartMessage</span><span class="sxs-lookup"><span data-stu-id="c363c-118">IXPLogon::StartMessage</span></span>](ixplogon-startmessage.md)
  
[<span data-ttu-id="c363c-119">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="c363c-119">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="c363c-120">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c363c-120">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

