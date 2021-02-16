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
ms.openlocfilehash: c5305ddd20b690f5c2e5807fb7ce2410549f7124
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412865"
---
# <a name="imsprovider--iunknown"></a><span data-ttu-id="1e372-103">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1e372-103">IMSProvider : IUnknown</span></span>

  
  
<span data-ttu-id="1e372-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1e372-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1e372-105">Предоставляет доступ к поставщику хранилище сообщений через объект поставщика.</span><span class="sxs-lookup"><span data-stu-id="1e372-105">Provides access to a message store provider through a message store provider object.</span></span> <span data-ttu-id="1e372-106">Этот объект поставщика для хранения сообщений возвращается при входе поставщика с помощью функции точки входа [MSProviderInit](msproviderinit.md) поставщика.</span><span class="sxs-lookup"><span data-stu-id="1e372-106">This message store provider object is returned at provider logon by the message store provider's [MSProviderInit](msproviderinit.md) entry point function.</span></span> <span data-ttu-id="1e372-107">Объект поставщика хранилища сообщений в основном используется клиентские приложения и пулом MAPI для открытия хранилищ сообщений.</span><span class="sxs-lookup"><span data-stu-id="1e372-107">The message store provider object is primarily used by client applications and the MAPI spooler to open message stores.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1e372-108">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="1e372-108">Header file:</span></span>  <br/> |<span data-ttu-id="1e372-109">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="1e372-109">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="1e372-110">Выставим:</span><span class="sxs-lookup"><span data-stu-id="1e372-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="1e372-111">Объекты поставщиков хранилищ сообщений</span><span class="sxs-lookup"><span data-stu-id="1e372-111">Message store provider objects</span></span>  <br/> |
|<span data-ttu-id="1e372-112">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="1e372-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="1e372-113">Поставщики store сообщений</span><span class="sxs-lookup"><span data-stu-id="1e372-113">Message store providers</span></span>  <br/> |
|<span data-ttu-id="1e372-114">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="1e372-114">Called by:</span></span>  <br/> |<span data-ttu-id="1e372-115">MAPI и пулер MAPI</span><span class="sxs-lookup"><span data-stu-id="1e372-115">MAPI and the MAPI spooler</span></span>  <br/> |
|<span data-ttu-id="1e372-116">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="1e372-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="1e372-117">IID_IMSProvider</span><span class="sxs-lookup"><span data-stu-id="1e372-117">IID_IMSProvider</span></span>  <br/> |
|<span data-ttu-id="1e372-118">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="1e372-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="1e372-119">LPMSPROVIDER</span><span class="sxs-lookup"><span data-stu-id="1e372-119">LPMSPROVIDER</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="1e372-120">Порядок ветвей</span><span class="sxs-lookup"><span data-stu-id="1e372-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="1e372-121">Shutdown</span><span class="sxs-lookup"><span data-stu-id="1e372-121">Shutdown</span></span>](imsprovider-shutdown.md) <br/> |<span data-ttu-id="1e372-122">Закрывает поставщика store сообщений упорядоченным образом.</span><span class="sxs-lookup"><span data-stu-id="1e372-122">Closes a message store provider in an orderly fashion.</span></span>  <br/> |
|[<span data-ttu-id="1e372-123">Logon</span><span class="sxs-lookup"><span data-stu-id="1e372-123">Logon</span></span>](imsprovider-logon.md) <br/> |<span data-ttu-id="1e372-124">Занося mapI в один экземпляр поставщика хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="1e372-124">Logs MAPI on to one instance of a message store provider.</span></span>  <br/> |
|[<span data-ttu-id="1e372-125">SpoolerLogon</span><span class="sxs-lookup"><span data-stu-id="1e372-125">SpoolerLogon</span></span>](imsprovider-spoolerlogon.md) <br/> |<span data-ttu-id="1e372-126">Занося в журнал пул MAPI в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="1e372-126">Logs the MAPI spooler on to a message store.</span></span>  <br/> |
|[<span data-ttu-id="1e372-127">CompareStoreIDs</span><span class="sxs-lookup"><span data-stu-id="1e372-127">CompareStoreIDs</span></span>](imsprovider-comparestoreids.md) <br/> |<span data-ttu-id="1e372-128">Сравнивает два идентификатора записей в хранилище сообщений, чтобы определить, относятся ли они к одному объекту store.</span><span class="sxs-lookup"><span data-stu-id="1e372-128">Compares two message store entry identifiers to determine whether they refer to the same store object.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1e372-129">Примечания</span><span class="sxs-lookup"><span data-stu-id="1e372-129">Remarks</span></span>

<span data-ttu-id="1e372-130">MAPI использует один объект поставщика хранилища сообщений в сеансе независимо от того, сколько хранилищ сообщений открывается поставщиком хранилища.</span><span class="sxs-lookup"><span data-stu-id="1e372-130">MAPI uses one message store provider object per session, no matter how many message stores are opened by the store provider.</span></span> <span data-ttu-id="1e372-131">Если второй сеанс MAPI входит в какие-либо открытые хранилища, MAPI вызывает **MSProviderInit** еще раз, чтобы создать новый объект поставщика хранилища сообщений для этого сеанса.</span><span class="sxs-lookup"><span data-stu-id="1e372-131">If a second MAPI session logs on to any open stores, MAPI calls **MSProviderInit** a second time to create a new message store provider object for that session to use.</span></span> 
  
<span data-ttu-id="1e372-132">Объект поставщика для хранения сообщений должен содержать следующие данные для правильной работы:</span><span class="sxs-lookup"><span data-stu-id="1e372-132">A message store provider object must contain the following to operate correctly:</span></span>
  
- <span data-ttu-id="1e372-133">Указатель  _программы выделения памяти lpMalloc_ для использования всеми хранилищами, открытыми с помощью этого объекта поставщика.</span><span class="sxs-lookup"><span data-stu-id="1e372-133">An  _lpMalloc_ memory-allocation routine pointer for use by all stores opened by using this provider object.</span></span> 
    
- <span data-ttu-id="1e372-134">Подпрограммные указатели _lpfAllocateBuffer_, _ lpfAllocateMore _и _lpfFreeBuffer_ на функции выделения памяти [MAPIAllocateBuffer,](mapiallocatebuffer.md) [MAPIAllocateMore](mapiallocatemore.md)и [MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="1e372-134">The  _lpfAllocateBuffer_,  _ lpfAllocateMore _, and  _lpfFreeBuffer_ routine pointers to the [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) memory allocation functions.</span></span> 
    
- <span data-ttu-id="1e372-135">Связанный список всех хранилищ, открытых с помощью этого объекта поставщика и еще не закрытых.</span><span class="sxs-lookup"><span data-stu-id="1e372-135">A linked list of all the stores opened by using this provider object and not yet closed.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1e372-136">См. также</span><span class="sxs-lookup"><span data-stu-id="1e372-136">See also</span></span>



[<span data-ttu-id="1e372-137">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="1e372-137">MAPI Interfaces</span></span>](mapi-interfaces.md)

