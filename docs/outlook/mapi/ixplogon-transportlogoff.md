---
title: IXPLogonTransportLogoff
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
ms.openlocfilehash: 761228a01e0dc778b962c62436e872ff20d72088
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586314"
---
# <a name="ixplogontransportlogoff"></a><span data-ttu-id="81ab3-103">IXPLogon::TransportLogoff</span><span class="sxs-lookup"><span data-stu-id="81ab3-103">IXPLogon::TransportLogoff</span></span>

  
  
<span data-ttu-id="81ab3-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="81ab3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="81ab3-105">Запускает процесс выхода из системы.</span><span class="sxs-lookup"><span data-stu-id="81ab3-105">Initiates the logoff process.</span></span> 
  
```cpp
HRESULT TransportLogoff(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="81ab3-106">���������</span><span class="sxs-lookup"><span data-stu-id="81ab3-106">Parameters</span></span>

 <span data-ttu-id="81ab3-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="81ab3-107">_ulFlags_</span></span>
  
> <span data-ttu-id="81ab3-108">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="81ab3-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="81ab3-109">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="81ab3-109">Return value</span></span>

<span data-ttu-id="81ab3-110">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="81ab3-110">S_OK</span></span> 
  
> <span data-ttu-id="81ab3-111">Вызов успешно и возвращается ожидаемым значением или значения.</span><span class="sxs-lookup"><span data-stu-id="81ab3-111">The call succeeded and returned the expected value or values.</span></span> <span data-ttu-id="81ab3-112">Если что-либо других значение S_OK возвращается поставщик выход.</span><span class="sxs-lookup"><span data-stu-id="81ab3-112">If anything other than S_OK is returned, the provider is logged off.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="81ab3-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="81ab3-113">Remarks</span></span>

<span data-ttu-id="81ab3-114">Диспетчер очереди MAPI вызывает метод **IXPLogon::TransportLogoff** , чтобы завершить сеанс поставщика транспорта для определенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="81ab3-114">The MAPI spooler calls the **IXPLogon::TransportLogoff** method to terminate a transport provider session for a particular user.</span></span> <span data-ttu-id="81ab3-115">До вызова метода **TransportLogoff**, диспетчер очереди MAPI удаляет все данные о поддерживаемых типов адреса обмена сообщениями для данного сеанса, переданной в метод [IXPLogon::AddressTypes](ixplogon-addresstypes.md) .</span><span class="sxs-lookup"><span data-stu-id="81ab3-115">Before calling **TransportLogoff**, the MAPI spooler discards any data about supported messaging address types for this session passed in the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="81ab3-116">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="81ab3-116">Notes to implementers</span></span>

<span data-ttu-id="81ab3-117">Поставщика транспорта должно быть готово для принятия вызова **TransportLogoff** в любое время.</span><span class="sxs-lookup"><span data-stu-id="81ab3-117">The transport provider should be prepared to accept a call to **TransportLogoff** at any time.</span></span> <span data-ttu-id="81ab3-118">Если сообщение не в процессе, поставщик должен остановить процесс отправки.</span><span class="sxs-lookup"><span data-stu-id="81ab3-118">If a message is in process, the provider should stop the sending process.</span></span> 
  
<span data-ttu-id="81ab3-119">Поставщика транспорта освобождать все ресурсы, выделенные для текущего сеанса.</span><span class="sxs-lookup"><span data-stu-id="81ab3-119">The transport provider should release all resources allocated for its current session.</span></span> <span data-ttu-id="81ab3-120">Если он выделенной памяти для данного сеанса с помощью функции [MAPIAllocateBuffer](mapiallocatebuffer.md) , он должен освободить память с помощью функции [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="81ab3-120">If it has allocated any memory for this session with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, it should free the memory by using the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> <span data-ttu-id="81ab3-121">Памяти, выделенной поставщика транспорта для удовлетворения вызовы метода [IXPLogon::AddressTypes](ixplogon-addresstypes.md) может безопасно снята в данный момент.</span><span class="sxs-lookup"><span data-stu-id="81ab3-121">Any memory allocated by the transport provider to satisfy calls to the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method can be safely released at this time.</span></span> 
  
<span data-ttu-id="81ab3-122">Как правило на завершение вызова **TransportLogoff** поставщика следует сначала объявить недействительным возвращается объект входа путем вызова метода [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) и затем выпуска возвращается объект поддержки.</span><span class="sxs-lookup"><span data-stu-id="81ab3-122">Usually, on completing a **TransportLogoff** call, a provider should first invalidate its logon object by calling the [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) method and then release its support object.</span></span> <span data-ttu-id="81ab3-123">Реализация поставщика из **TransportLogoff** должен освободить объект поддержки и, наконец, так как после выхода объекта поддержки, диспетчер очереди MAPI может быть выпущен сам объект поставщика.</span><span class="sxs-lookup"><span data-stu-id="81ab3-123">The provider's implementation of **TransportLogoff** should release the support object last, because when the support object is released, the MAPI spooler can also release the provider object itself.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="81ab3-124">См. также</span><span class="sxs-lookup"><span data-stu-id="81ab3-124">See also</span></span>



[<span data-ttu-id="81ab3-125">IMAPISupport::MakeInvalid</span><span class="sxs-lookup"><span data-stu-id="81ab3-125">IMAPISupport::MakeInvalid</span></span>](imapisupport-makeinvalid.md)
  
[<span data-ttu-id="81ab3-126">IMAPISupport::SpoolerYield</span><span class="sxs-lookup"><span data-stu-id="81ab3-126">IMAPISupport::SpoolerYield</span></span>](imapisupport-spooleryield.md)
  
[<span data-ttu-id="81ab3-127">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="81ab3-127">IXPLogon::AddressTypes</span></span>](ixplogon-addresstypes.md)
  
[<span data-ttu-id="81ab3-128">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="81ab3-128">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="81ab3-129">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="81ab3-129">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="81ab3-130">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="81ab3-130">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

