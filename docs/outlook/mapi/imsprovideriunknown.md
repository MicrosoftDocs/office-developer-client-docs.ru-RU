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
# <a name="imsprovider--iunknown"></a><span data-ttu-id="ef4b4-103">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ef4b4-103">IMSProvider : IUnknown</span></span>

  
  
<span data-ttu-id="ef4b4-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ef4b4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ef4b4-105">Предоставляет доступ к поставщику хранения сообщений через объект поставщика магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="ef4b4-105">Provides access to a message store provider through a message store provider object.</span></span> <span data-ttu-id="ef4b4-106">Этот объект поставщика хранения сообщений возвращается в логотипе поставщика функцией точки входа [поставщика msProviderInit](msproviderinit.md) поставщика сообщений.</span><span class="sxs-lookup"><span data-stu-id="ef4b4-106">This message store provider object is returned at provider logon by the message store provider's [MSProviderInit](msproviderinit.md) entry point function.</span></span> <span data-ttu-id="ef4b4-107">Объект поставщика хранилища сообщений используется в основном клиентские приложения и пульпер MAPI для открытия магазинов сообщений.</span><span class="sxs-lookup"><span data-stu-id="ef4b4-107">The message store provider object is primarily used by client applications and the MAPI spooler to open message stores.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ef4b4-108">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="ef4b4-108">Header file:</span></span>  <br/> |<span data-ttu-id="ef4b4-109">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="ef4b4-109">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="ef4b4-110">Подвергается:</span><span class="sxs-lookup"><span data-stu-id="ef4b4-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="ef4b4-111">Объекты поставщиков хранилищ сообщений</span><span class="sxs-lookup"><span data-stu-id="ef4b4-111">Message store provider objects</span></span>  <br/> |
|<span data-ttu-id="ef4b4-112">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="ef4b4-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="ef4b4-113">Поставщики магазинов сообщений</span><span class="sxs-lookup"><span data-stu-id="ef4b4-113">Message store providers</span></span>  <br/> |
|<span data-ttu-id="ef4b4-114">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="ef4b4-114">Called by:</span></span>  <br/> |<span data-ttu-id="ef4b4-115">MAPI и шпалер MAPI</span><span class="sxs-lookup"><span data-stu-id="ef4b4-115">MAPI and the MAPI spooler</span></span>  <br/> |
|<span data-ttu-id="ef4b4-116">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="ef4b4-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="ef4b4-117">IID_IMSProvider</span><span class="sxs-lookup"><span data-stu-id="ef4b4-117">IID_IMSProvider</span></span>  <br/> |
|<span data-ttu-id="ef4b4-118">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="ef4b4-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="ef4b4-119">LPMSPROVIDER</span><span class="sxs-lookup"><span data-stu-id="ef4b4-119">LPMSPROVIDER</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="ef4b4-120">Заказ Vtable</span><span class="sxs-lookup"><span data-stu-id="ef4b4-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="ef4b4-121">Shutdown</span><span class="sxs-lookup"><span data-stu-id="ef4b4-121">Shutdown</span></span>](imsprovider-shutdown.md) <br/> |<span data-ttu-id="ef4b4-122">Закрывает поставщика магазина сообщений упорядоченным способом.</span><span class="sxs-lookup"><span data-stu-id="ef4b4-122">Closes a message store provider in an orderly fashion.</span></span>  <br/> |
|[<span data-ttu-id="ef4b4-123">Logon</span><span class="sxs-lookup"><span data-stu-id="ef4b4-123">Logon</span></span>](imsprovider-logon.md) <br/> |<span data-ttu-id="ef4b4-124">Журнал MAPI для одного экземпляра поставщика магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="ef4b4-124">Logs MAPI on to one instance of a message store provider.</span></span>  <br/> |
|[<span data-ttu-id="ef4b4-125">SpoolerLogon</span><span class="sxs-lookup"><span data-stu-id="ef4b4-125">SpoolerLogon</span></span>](imsprovider-spoolerlogon.md) <br/> |<span data-ttu-id="ef4b4-126">Регистрирую пульпер MAPI в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="ef4b4-126">Logs the MAPI spooler on to a message store.</span></span>  <br/> |
|[<span data-ttu-id="ef4b4-127">CompareStoreIDs</span><span class="sxs-lookup"><span data-stu-id="ef4b4-127">CompareStoreIDs</span></span>](imsprovider-comparestoreids.md) <br/> |<span data-ttu-id="ef4b4-128">Сравнивает два идентификатора входа в хранилище сообщений, чтобы определить, относятся ли они к одному объекту магазина.</span><span class="sxs-lookup"><span data-stu-id="ef4b4-128">Compares two message store entry identifiers to determine whether they refer to the same store object.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ef4b4-129">Примечания</span><span class="sxs-lookup"><span data-stu-id="ef4b4-129">Remarks</span></span>

<span data-ttu-id="ef4b4-130">MAPI использует один объект поставщика хранилища сообщений в сеансе независимо от того, сколько магазинов сообщений открывается поставщиком.</span><span class="sxs-lookup"><span data-stu-id="ef4b4-130">MAPI uses one message store provider object per session, no matter how many message stores are opened by the store provider.</span></span> <span data-ttu-id="ef4b4-131">Если второй сеанс MAPI входит в открытые магазины, MAPI вызывает **MSProviderInit** во второй раз, чтобы создать новый объект поставщика хранилища сообщений для этого сеанса.</span><span class="sxs-lookup"><span data-stu-id="ef4b4-131">If a second MAPI session logs on to any open stores, MAPI calls **MSProviderInit** a second time to create a new message store provider object for that session to use.</span></span> 
  
<span data-ttu-id="ef4b4-132">Объект поставщика хранения сообщений должен содержать следующие данные, чтобы правильно работать:</span><span class="sxs-lookup"><span data-stu-id="ef4b4-132">A message store provider object must contain the following to operate correctly:</span></span>
  
- <span data-ttu-id="ef4b4-133">Обычный  _указатель памяти lpMalloc_ для использования во всех магазинах, открытых с помощью этого объекта-поставщика.</span><span class="sxs-lookup"><span data-stu-id="ef4b4-133">An  _lpMalloc_ memory-allocation routine pointer for use by all stores opened by using this provider object.</span></span> 
    
- <span data-ttu-id="ef4b4-134">Плановые указатели _lpfAllocateBuffer_, _ lpfAllocateMore _и _lpfFreeBuffer_ на функции распределения памяти [MAPIAllocateBuffer,](mapiallocatebuffer.md) [MAPIAllocateMore](mapiallocatemore.md)и [MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="ef4b4-134">The  _lpfAllocateBuffer_,  _ lpfAllocateMore _, and  _lpfFreeBuffer_ routine pointers to the [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) memory allocation functions.</span></span> 
    
- <span data-ttu-id="ef4b4-135">Связанный список всех магазинов, открытых с помощью этого объекта-поставщика и еще не закрытых.</span><span class="sxs-lookup"><span data-stu-id="ef4b4-135">A linked list of all the stores opened by using this provider object and not yet closed.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ef4b4-136">См. также</span><span class="sxs-lookup"><span data-stu-id="ef4b4-136">See also</span></span>



[<span data-ttu-id="ef4b4-137">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="ef4b4-137">MAPI Interfaces</span></span>](mapi-interfaces.md)

