---
title: Функцииimsprovider IUnknown
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317251"
---
# <a name="imsprovider--iunknown"></a><span data-ttu-id="2ca4b-103">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2ca4b-103">IMSProvider : IUnknown</span></span>

  
  
<span data-ttu-id="2ca4b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2ca4b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2ca4b-105">Предоставляет доступ к поставщику хранилища сообщений через объект поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="2ca4b-105">Provides access to a message store provider through a message store provider object.</span></span> <span data-ttu-id="2ca4b-106">Этот объект поставщика хранилища сообщений возвращается при входе поставщика в функцию точки входа [мспровидеринит](msproviderinit.md) поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="2ca4b-106">This message store provider object is returned at provider logon by the message store provider's [MSProviderInit](msproviderinit.md) entry point function.</span></span> <span data-ttu-id="2ca4b-107">Объект поставщика хранилища сообщений в основном используется клиентскими приложениями и диспетчером очереди MAPI для открытия хранилищ сообщений.</span><span class="sxs-lookup"><span data-stu-id="2ca4b-107">The message store provider object is primarily used by client applications and the MAPI spooler to open message stores.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2ca4b-108">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="2ca4b-108">Header file:</span></span>  <br/> |<span data-ttu-id="2ca4b-109">Маписпи. h</span><span class="sxs-lookup"><span data-stu-id="2ca4b-109">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="2ca4b-110">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="2ca4b-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="2ca4b-111">Объекты поставщиков хранилищ сообщений</span><span class="sxs-lookup"><span data-stu-id="2ca4b-111">Message store provider objects</span></span>  <br/> |
|<span data-ttu-id="2ca4b-112">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="2ca4b-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="2ca4b-113">Поставщики хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="2ca4b-113">Message store providers</span></span>  <br/> |
|<span data-ttu-id="2ca4b-114">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="2ca4b-114">Called by:</span></span>  <br/> |<span data-ttu-id="2ca4b-115">MAPI и Диспетчер очереди MAPI</span><span class="sxs-lookup"><span data-stu-id="2ca4b-115">MAPI and the MAPI spooler</span></span>  <br/> |
|<span data-ttu-id="2ca4b-116">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="2ca4b-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="2ca4b-117">Иид_имспровидер</span><span class="sxs-lookup"><span data-stu-id="2ca4b-117">IID_IMSProvider</span></span>  <br/> |
|<span data-ttu-id="2ca4b-118">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="2ca4b-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="2ca4b-119">ЛПМСПРОВИДЕР</span><span class="sxs-lookup"><span data-stu-id="2ca4b-119">LPMSPROVIDER</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="2ca4b-120">Заказ vtable</span><span class="sxs-lookup"><span data-stu-id="2ca4b-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="2ca4b-121">Shutdown</span><span class="sxs-lookup"><span data-stu-id="2ca4b-121">Shutdown</span></span>](imsprovider-shutdown.md) <br/> |<span data-ttu-id="2ca4b-122">ЗаКрывает поставщик хранилища сообщений в определенном порядке.</span><span class="sxs-lookup"><span data-stu-id="2ca4b-122">Closes a message store provider in an orderly fashion.</span></span>  <br/> |
|[<span data-ttu-id="2ca4b-123">Logon</span><span class="sxs-lookup"><span data-stu-id="2ca4b-123">Logon</span></span>](imsprovider-logon.md) <br/> |<span data-ttu-id="2ca4b-124">Регистрирует MAPI на одном экземпляре поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="2ca4b-124">Logs MAPI on to one instance of a message store provider.</span></span>  <br/> |
|[<span data-ttu-id="2ca4b-125">Спулерлогон</span><span class="sxs-lookup"><span data-stu-id="2ca4b-125">SpoolerLogon</span></span>](imsprovider-spoolerlogon.md) <br/> |<span data-ttu-id="2ca4b-126">ЗаНосит в журнал Диспетчер очереди MAPI в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="2ca4b-126">Logs the MAPI spooler on to a message store.</span></span>  <br/> |
|[<span data-ttu-id="2ca4b-127">Компарестореидс</span><span class="sxs-lookup"><span data-stu-id="2ca4b-127">CompareStoreIDs</span></span>](imsprovider-comparestoreids.md) <br/> |<span data-ttu-id="2ca4b-128">Сравнивает два идентификатора записи хранилища сообщений, чтобы определить, ссылаются ли они на один и тот же объект хранилища.</span><span class="sxs-lookup"><span data-stu-id="2ca4b-128">Compares two message store entry identifiers to determine whether they refer to the same store object.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2ca4b-129">Замечания</span><span class="sxs-lookup"><span data-stu-id="2ca4b-129">Remarks</span></span>

<span data-ttu-id="2ca4b-130">MAPI использует один объект поставщика хранилища сообщений для каждого сеанса, независимо от того, сколько хранилищ сообщений открыто поставщиком хранилища.</span><span class="sxs-lookup"><span data-stu-id="2ca4b-130">MAPI uses one message store provider object per session, no matter how many message stores are opened by the store provider.</span></span> <span data-ttu-id="2ca4b-131">Если второй сеанс MAPI выполняет вход в все открытые хранилища, Служба MAPI вызывает **мспровидеринит** во второй раз, чтобы создать новый объект поставщика хранилища сообщений для используемого сеанса.</span><span class="sxs-lookup"><span data-stu-id="2ca4b-131">If a second MAPI session logs on to any open stores, MAPI calls **MSProviderInit** a second time to create a new message store provider object for that session to use.</span></span> 
  
<span data-ttu-id="2ca4b-132">Для правильной работы объект поставщика хранилища сообщений должен содержать следующие объекты:</span><span class="sxs-lookup"><span data-stu-id="2ca4b-132">A message store provider object must contain the following to operate correctly:</span></span>
  
- <span data-ttu-id="2ca4b-133">Указатель процедуры выделения памяти _лпмаллок_ для использования всеми хранилищами, открытыми с помощью этого объекта поставщика.</span><span class="sxs-lookup"><span data-stu-id="2ca4b-133">An  _lpMalloc_ memory-allocation routine pointer for use by all stores opened by using this provider object.</span></span> 
    
- <span data-ttu-id="2ca4b-134">Стандартные указатели _лпфаллокатебуффер_, _ лпфаллокатеморе _ и _лпффрибуффер_ для функций выделения памяти [мапиаллокатебуффер](mapiallocatebuffer.md), [мапиаллокатеморе](mapiallocatemore.md)и [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="2ca4b-134">The  _lpfAllocateBuffer_,  _ lpfAllocateMore _, and  _lpfFreeBuffer_ routine pointers to the [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) memory allocation functions.</span></span> 
    
- <span data-ttu-id="2ca4b-135">Связанный список всех хранилищ, открытых с помощью этого объекта поставщика и еще не закрытых.</span><span class="sxs-lookup"><span data-stu-id="2ca4b-135">A linked list of all the stores opened by using this provider object and not yet closed.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2ca4b-136">См. также</span><span class="sxs-lookup"><span data-stu-id="2ca4b-136">See also</span></span>



[<span data-ttu-id="2ca4b-137">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="2ca4b-137">MAPI Interfaces</span></span>](mapi-interfaces.md)

