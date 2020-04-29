---
title: Идистлист IMAPIContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IDistList
api_type:
- COM
ms.assetid: bd8e1ddb-3027-428b-8964-81614f80282d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 463d81a6692b6071cada0ad22e7343020563e41c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431549"
---
# <a name="idistlist--imapicontainer"></a><span data-ttu-id="8cc8e-103">IDistList : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="8cc8e-103">IDistList : IMAPIContainer</span></span>

  
  
<span data-ttu-id="8cc8e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8cc8e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8cc8e-105">Предоставляет доступ к спискам рассылки в изменяемых контейнерах адресной книги.</span><span class="sxs-lookup"><span data-stu-id="8cc8e-105">Provides access to distribution lists in modifiable address book containers.</span></span> <span data-ttu-id="8cc8e-106">**Идистлист** позволяет создавать, копировать и удалять списки рассылки, а также выполнять разрешение имен.</span><span class="sxs-lookup"><span data-stu-id="8cc8e-106">**IDistList** can create, copy, and delete distribution lists, in addition to performing name resolution.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8cc8e-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="8cc8e-107">Header file:</span></span>  <br/> |<span data-ttu-id="8cc8e-108">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="8cc8e-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="8cc8e-109">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="8cc8e-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="8cc8e-110">Объекты списка рассылки</span><span class="sxs-lookup"><span data-stu-id="8cc8e-110">Distribution list objects</span></span>  <br/> |
|<span data-ttu-id="8cc8e-111">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="8cc8e-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="8cc8e-112">Поставщики адресных книг</span><span class="sxs-lookup"><span data-stu-id="8cc8e-112">Address book providers</span></span>  <br/> |
|<span data-ttu-id="8cc8e-113">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="8cc8e-113">Called by:</span></span>  <br/> |<span data-ttu-id="8cc8e-114">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="8cc8e-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="8cc8e-115">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="8cc8e-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="8cc8e-116">IID_IDistList</span><span class="sxs-lookup"><span data-stu-id="8cc8e-116">IID_IDistList</span></span>  <br/> |
|<span data-ttu-id="8cc8e-117">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="8cc8e-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="8cc8e-118">лпдистлист</span><span class="sxs-lookup"><span data-stu-id="8cc8e-118">LPDISTLIST</span></span>  <br/> |
|<span data-ttu-id="8cc8e-119">Модель транзакции:</span><span class="sxs-lookup"><span data-stu-id="8cc8e-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="8cc8e-120">Транзакции</span><span class="sxs-lookup"><span data-stu-id="8cc8e-120">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="8cc8e-121">Заказ vtable</span><span class="sxs-lookup"><span data-stu-id="8cc8e-121">Vtable order</span></span>

<span data-ttu-id="8cc8e-122">У этого интерфейса нет уникальных методов.</span><span class="sxs-lookup"><span data-stu-id="8cc8e-122">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="8cc8e-123">**Обязательные свойства**</span><span class="sxs-lookup"><span data-stu-id="8cc8e-123">**Required properties**</span></span>|<span data-ttu-id="8cc8e-124">**Access**</span><span class="sxs-lookup"><span data-stu-id="8cc8e-124">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8cc8e-125">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8cc8e-125">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="8cc8e-126">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8cc8e-126">Read/write</span></span>  <br/> |
|<span data-ttu-id="8cc8e-127">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8cc8e-127">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="8cc8e-128">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8cc8e-128">Read/write</span></span>  <br/> |
|<span data-ttu-id="8cc8e-129">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8cc8e-129">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="8cc8e-130">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="8cc8e-130">Read-only</span></span>  <br/> |
|<span data-ttu-id="8cc8e-131">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8cc8e-131">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="8cc8e-132">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="8cc8e-132">Read-only</span></span>  <br/> |
|<span data-ttu-id="8cc8e-133">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8cc8e-133">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="8cc8e-134">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="8cc8e-134">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8cc8e-135">Примечания</span><span class="sxs-lookup"><span data-stu-id="8cc8e-135">Remarks</span></span>

<span data-ttu-id="8cc8e-136">Интерфейс **идистлист** наследуется от [IMAPIContainer](imapicontainerimapiprop.md) и содержит те же методы, что и контейнеры адресных книг.</span><span class="sxs-lookup"><span data-stu-id="8cc8e-136">The **IDistList** interface inherits from [IMAPIContainer](imapicontainerimapiprop.md) and includes the same methods as address book containers.</span></span> <span data-ttu-id="8cc8e-137">Таким образом, так как методы интерфейса **идистлист** идентичны элементам интерфейса [иабконтаинер](iabcontainerimapicontainer.md) , они не дублируются здесь.</span><span class="sxs-lookup"><span data-stu-id="8cc8e-137">Therefore, because the methods of the **IDistList** interface are identical to those of the [IABContainer](iabcontainerimapicontainer.md) interface, they are not duplicated here.</span></span> 
  
<span data-ttu-id="8cc8e-138">Список рассылки или объект, реализующий **идистлист** — это коллекция объектов пользователя обмена сообщениями или отдельных получателей.</span><span class="sxs-lookup"><span data-stu-id="8cc8e-138">A distribution list or object that implements **IDistList** is a collection of messaging user objects, or individual recipients.</span></span> <span data-ttu-id="8cc8e-139">Список рассылки может состоять из всех пользовательских объектов обмена сообщениями, а также от некоторых пользователей обмена сообщениями и некоторых списков рассылки.</span><span class="sxs-lookup"><span data-stu-id="8cc8e-139">A distribution list can consist of all messaging user objects, or some messaging user and some distribution lists.</span></span> 
  
<span data-ttu-id="8cc8e-140">Обычно существует два типа списков рассылки:</span><span class="sxs-lookup"><span data-stu-id="8cc8e-140">There are typically two types of distribution lists:</span></span>
  
- <span data-ttu-id="8cc8e-141">Списки рассылки, развернутые базовой системой обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="8cc8e-141">Distribution lists that are expanded by the underlying messaging system.</span></span> <span data-ttu-id="8cc8e-142">Этот тип списка содержит адрес, **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) и обрабатывается так же, как если бы он был отдельным получателем.</span><span class="sxs-lookup"><span data-stu-id="8cc8e-142">This type of list has an address, **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), and is treated the same as if it were an individual recipient.</span></span> 
    
- <span data-ttu-id="8cc8e-143">Списки рассылки, существующие в локальном контейнере и развернутые клиентским приложением.</span><span class="sxs-lookup"><span data-stu-id="8cc8e-143">Distribution lists that exist in a local container and are expanded by the client application.</span></span>
    
<span data-ttu-id="8cc8e-144">К дополнительным свойствам списка рассылки относятся следующие:</span><span class="sxs-lookup"><span data-stu-id="8cc8e-144">Optional distribution list properties include the following:</span></span>
  
- <span data-ttu-id="8cc8e-145">**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8cc8e-145">**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="8cc8e-146">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8cc8e-146">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span> 
    
- <span data-ttu-id="8cc8e-147">**PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8cc8e-147">**PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md))</span></span> 
    
<span data-ttu-id="8cc8e-148">Обратите внимание, что **PR_ADDRTYPE** является обязательным, но **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) нет.</span><span class="sxs-lookup"><span data-stu-id="8cc8e-148">Notice that **PR_ADDRTYPE** is required, but **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) is not.</span></span> <span data-ttu-id="8cc8e-149">Это связано с тем, что список рассылки без адреса электронной почты по-прежнему может получать сообщения, но список его участников должен быть развернут.</span><span class="sxs-lookup"><span data-stu-id="8cc8e-149">That is because a distribution list without an email address can still receive messages, but its member list must be expanded.</span></span> <span data-ttu-id="8cc8e-150">Если для свойства **PR_ADDRTYPE** задано значение МАПИПДЛ, MAPI выполняет расширение.</span><span class="sxs-lookup"><span data-stu-id="8cc8e-150">If the **PR_ADDRTYPE** property is set to MAPIPDL, MAPI performs the expansion.</span></span> <span data-ttu-id="8cc8e-151">Если **PR_ADDRTYPE** имеет значение, отличное от мапипдл, то поставщик транспорта выполняет расширение.</span><span class="sxs-lookup"><span data-stu-id="8cc8e-151">If **PR_ADDRTYPE** is a value other than MAPIPDL, the transport provider performs the expansion.</span></span> 
  
<span data-ttu-id="8cc8e-152">Дополнительные сведения об использовании методов **идистлист** приведены в справочных записях для параллельных методов **иабконтаинер**.</span><span class="sxs-lookup"><span data-stu-id="8cc8e-152">For additional information about how to use the **IDistList** methods, see the reference entries for the parallel methods of **IABContainer**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8cc8e-153">См. также</span><span class="sxs-lookup"><span data-stu-id="8cc8e-153">See also</span></span>



[<span data-ttu-id="8cc8e-154">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="8cc8e-154">MAPI Interfaces</span></span>](mapi-interfaces.md)

