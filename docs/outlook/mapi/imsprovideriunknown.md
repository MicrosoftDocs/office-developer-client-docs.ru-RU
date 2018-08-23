---
title: IMSProvider IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSProvider
api_type:
- COM
ms.assetid: 0f17aa44-abcb-4732-b013-d91652847cf6
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 1c00e54d02ba494c94c9826eabe142e1bd3b9a80
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579629"
---
# <a name="imsprovider--iunknown"></a><span data-ttu-id="1430f-103">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1430f-103">IMSProvider : IUnknown</span></span>

  
  
<span data-ttu-id="1430f-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1430f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1430f-105">Предоставляет доступ к поставщику хранилища сообщений через объект поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="1430f-105">Provides access to a message store provider through a message store provider object.</span></span> <span data-ttu-id="1430f-106">Этот объект поставщика хранилища сообщений возвращается при входе в систему поставщика функции точки входа [MSProviderInit](msproviderinit.md) поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="1430f-106">This message store provider object is returned at provider logon by the message store provider's [MSProviderInit](msproviderinit.md) entry point function.</span></span> <span data-ttu-id="1430f-107">Объект поставщика хранилища сообщений в основном используется для открытия хранилищ сообщений с клиентскими приложениями и диспетчер очереди MAPI.</span><span class="sxs-lookup"><span data-stu-id="1430f-107">The message store provider object is primarily used by client applications and the MAPI spooler to open message stores.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1430f-108">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="1430f-108">Header file:</span></span>  <br/> |<span data-ttu-id="1430f-109">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="1430f-109">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="1430f-110">Предоставляемые:</span><span class="sxs-lookup"><span data-stu-id="1430f-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="1430f-111">Объекты поставщика хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="1430f-111">Message store provider objects</span></span>  <br/> |
|<span data-ttu-id="1430f-112">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="1430f-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="1430f-113">Поставщики хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="1430f-113">Message store providers</span></span>  <br/> |
|<span data-ttu-id="1430f-114">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="1430f-114">Called by:</span></span>  <br/> |<span data-ttu-id="1430f-115">MAPI и диспетчер очереди MAPI</span><span class="sxs-lookup"><span data-stu-id="1430f-115">MAPI and the MAPI spooler</span></span>  <br/> |
|<span data-ttu-id="1430f-116">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="1430f-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="1430f-117">IID_IMSProvider</span><span class="sxs-lookup"><span data-stu-id="1430f-117">IID_IMSProvider</span></span>  <br/> |
|<span data-ttu-id="1430f-118">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="1430f-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="1430f-119">LPMSPROVIDER</span><span class="sxs-lookup"><span data-stu-id="1430f-119">LPMSPROVIDER</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="1430f-120">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="1430f-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="1430f-121">Shutdown</span><span class="sxs-lookup"><span data-stu-id="1430f-121">Shutdown</span></span>](imsprovider-shutdown.md) <br/> |<span data-ttu-id="1430f-122">Закрывает поставщика хранилища сообщений определенным образом.</span><span class="sxs-lookup"><span data-stu-id="1430f-122">Closes a message store provider in an orderly fashion.</span></span>  <br/> |
|[<span data-ttu-id="1430f-123">Вход в систему</span><span class="sxs-lookup"><span data-stu-id="1430f-123">Logon</span></span>](imsprovider-logon.md) <br/> |<span data-ttu-id="1430f-124">Журналы MAPI на один экземпляр поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="1430f-124">Logs MAPI on to one instance of a message store provider.</span></span>  <br/> |
|[<span data-ttu-id="1430f-125">SpoolerLogon</span><span class="sxs-lookup"><span data-stu-id="1430f-125">SpoolerLogon</span></span>](imsprovider-spoolerlogon.md) <br/> |<span data-ttu-id="1430f-126">Журналы очереди MAPI вход в систему хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="1430f-126">Logs the MAPI spooler on to a message store.</span></span>  <br/> |
|[<span data-ttu-id="1430f-127">CompareStoreIDs</span><span class="sxs-lookup"><span data-stu-id="1430f-127">CompareStoreIDs</span></span>](imsprovider-comparestoreids.md) <br/> |<span data-ttu-id="1430f-128">Сравнение двух сообщений идентификаторы хранилища записей для определения, является ли они ссылаются на тот же объект хранилища.</span><span class="sxs-lookup"><span data-stu-id="1430f-128">Compares two message store entry identifiers to determine whether they refer to the same store object.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1430f-129">Замечания</span><span class="sxs-lookup"><span data-stu-id="1430f-129">Remarks</span></span>

<span data-ttu-id="1430f-130">MAPI использует один объект поставщика хранилища сообщений на сеанс, независимо от того, сколько сообщений хранилищ открываются поставщиком хранилища.</span><span class="sxs-lookup"><span data-stu-id="1430f-130">MAPI uses one message store provider object per session, no matter how many message stores are opened by the store provider.</span></span> <span data-ttu-id="1430f-131">Если второй журналы сеанса MAPI на любой open хранилищ, MAPI вызывает **MSProviderInit** еще раз для создания нового объекта поставщика хранилища сообщений для данного сеанса для использования.</span><span class="sxs-lookup"><span data-stu-id="1430f-131">If a second MAPI session logs on to any open stores, MAPI calls **MSProviderInit** a second time to create a new message store provider object for that session to use.</span></span> 
  
<span data-ttu-id="1430f-132">Объект поставщика хранилища сообщений, должна содержать следующие действия, чтобы обеспечить правильное функционирование:</span><span class="sxs-lookup"><span data-stu-id="1430f-132">A message store provider object must contain the following to operate correctly:</span></span>
  
- <span data-ttu-id="1430f-133">_LpMalloc_ выделение памяти выполнять рутинные указатель для использования сервером все открыто с помощью этого объекта поставщика хранилища.</span><span class="sxs-lookup"><span data-stu-id="1430f-133">An  _lpMalloc_ memory-allocation routine pointer for use by all stores opened by using this provider object.</span></span> 
    
- <span data-ttu-id="1430f-134">_LpfAllocateBuffer_, _ lpfAllocateMore _ и _lpfFreeBuffer_ процедуры указатели на [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)и [MAPIFreeBuffer](mapifreebuffer.md) функций выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="1430f-134">The  _lpfAllocateBuffer_,  _ lpfAllocateMore _, and  _lpfFreeBuffer_ routine pointers to the [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) memory allocation functions.</span></span> 
    
- <span data-ttu-id="1430f-135">Связанный список всех хранилищ открыто с помощью этого объекта поставщика и еще не закрытый.</span><span class="sxs-lookup"><span data-stu-id="1430f-135">A linked list of all the stores opened by using this provider object and not yet closed.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1430f-136">См. также</span><span class="sxs-lookup"><span data-stu-id="1430f-136">See also</span></span>



[<span data-ttu-id="1430f-137">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="1430f-137">MAPI Interfaces</span></span>](mapi-interfaces.md)

