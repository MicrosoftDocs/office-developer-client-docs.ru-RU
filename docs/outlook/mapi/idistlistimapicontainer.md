---
title: IDistList IMAPIContainer
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
ms.openlocfilehash: d5b9fb9bf8c84433ee5000cc8832c2f09bfc5fe3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590626"
---
# <a name="idistlist--imapicontainer"></a><span data-ttu-id="efcba-103">IDistList : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="efcba-103">IDistList : IMAPIContainer</span></span>

  
  
<span data-ttu-id="efcba-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="efcba-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="efcba-105">Предоставляет доступ к списки рассылки в поле можно изменить адрес книги контейнеров.</span><span class="sxs-lookup"><span data-stu-id="efcba-105">Provides access to distribution lists in modifiable address book containers.</span></span> <span data-ttu-id="efcba-106">**IDistList** создание, копирование и удаление списков рассылки, кроме разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="efcba-106">**IDistList** can create, copy, and delete distribution lists, in addition to performing name resolution.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="efcba-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="efcba-107">Header file:</span></span>  <br/> |<span data-ttu-id="efcba-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="efcba-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="efcba-109">Предоставляемые:</span><span class="sxs-lookup"><span data-stu-id="efcba-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="efcba-110">Объекты списка рассылки</span><span class="sxs-lookup"><span data-stu-id="efcba-110">Distribution list objects</span></span>  <br/> |
|<span data-ttu-id="efcba-111">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="efcba-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="efcba-112">Поставщиками адресных книг</span><span class="sxs-lookup"><span data-stu-id="efcba-112">Address book providers</span></span>  <br/> |
|<span data-ttu-id="efcba-113">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="efcba-113">Called by:</span></span>  <br/> |<span data-ttu-id="efcba-114">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="efcba-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="efcba-115">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="efcba-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="efcba-116">IID_IDistList</span><span class="sxs-lookup"><span data-stu-id="efcba-116">IID_IDistList</span></span>  <br/> |
|<span data-ttu-id="efcba-117">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="efcba-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="efcba-118">LPDISTLIST</span><span class="sxs-lookup"><span data-stu-id="efcba-118">LPDISTLIST</span></span>  <br/> |
|<span data-ttu-id="efcba-119">Модель транзакций:</span><span class="sxs-lookup"><span data-stu-id="efcba-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="efcba-120">В транзакции</span><span class="sxs-lookup"><span data-stu-id="efcba-120">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="efcba-121">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="efcba-121">Vtable order</span></span>

<span data-ttu-id="efcba-122">Этот интерфейс не имеет каких-либо уникальных методов.</span><span class="sxs-lookup"><span data-stu-id="efcba-122">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="efcba-123">**Обязательные свойства**</span><span class="sxs-lookup"><span data-stu-id="efcba-123">**Required properties**</span></span>|<span data-ttu-id="efcba-124">**Access**</span><span class="sxs-lookup"><span data-stu-id="efcba-124">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="efcba-125">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="efcba-125">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="efcba-126">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="efcba-126">Read/write</span></span>  <br/> |
|<span data-ttu-id="efcba-127">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="efcba-127">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="efcba-128">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="efcba-128">Read/write</span></span>  <br/> |
|<span data-ttu-id="efcba-129">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="efcba-129">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="efcba-130">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="efcba-130">Read-only</span></span>  <br/> |
|<span data-ttu-id="efcba-131">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="efcba-131">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="efcba-132">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="efcba-132">Read-only</span></span>  <br/> |
|<span data-ttu-id="efcba-133">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="efcba-133">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="efcba-134">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="efcba-134">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="efcba-135">Замечания</span><span class="sxs-lookup"><span data-stu-id="efcba-135">Remarks</span></span>

<span data-ttu-id="efcba-136">Интерфейс **IDistList** наследует от [IMAPIContainer](imapicontainerimapiprop.md) и включает в себя идентичные методам как контейнеры адресной книги.</span><span class="sxs-lookup"><span data-stu-id="efcba-136">The **IDistList** interface inherits from [IMAPIContainer](imapicontainerimapiprop.md) and includes the same methods as address book containers.</span></span> <span data-ttu-id="efcba-137">Таким образом так как методы интерфейса **IDistList** , совпадают интерфейса [IABContainer](iabcontainerimapicontainer.md) , они не повторяются здесь.</span><span class="sxs-lookup"><span data-stu-id="efcba-137">Therefore, because the methods of the **IDistList** interface are identical to those of the [IABContainer](iabcontainerimapicontainer.md) interface, they are not duplicated here.</span></span> 
  
<span data-ttu-id="efcba-138">Список рассылки или объект, который реализует **IDistList** является коллекция обмена сообщениями объектов-пользователей или отдельных получателей.</span><span class="sxs-lookup"><span data-stu-id="efcba-138">A distribution list or object that implements **IDistList** is a collection of messaging user objects, or individual recipients.</span></span> <span data-ttu-id="efcba-139">Список рассылки может состоять из всех, объектов пользователей обмена мгновенными сообщениями, или некоторые обмена сообщениями пользователя и некоторые списки рассылки.</span><span class="sxs-lookup"><span data-stu-id="efcba-139">A distribution list can consist of all messaging user objects, or some messaging user and some distribution lists.</span></span> 
  
<span data-ttu-id="efcba-140">Как правило, существует два типа списков рассылки:</span><span class="sxs-lookup"><span data-stu-id="efcba-140">There are typically two types of distribution lists:</span></span>
  
- <span data-ttu-id="efcba-141">Списки рассылки, которые развертываются с базовым системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="efcba-141">Distribution lists that are expanded by the underlying messaging system.</span></span> <span data-ttu-id="efcba-142">Этот тип списка с адресом **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) и является обрабатывается так же, как для отдельного получателя.</span><span class="sxs-lookup"><span data-stu-id="efcba-142">This type of list has an address, **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), and is treated the same as if it were an individual recipient.</span></span> 
    
- <span data-ttu-id="efcba-143">Списки рассылки, существующих в локальном контейнере и расширенное клиентским приложением.</span><span class="sxs-lookup"><span data-stu-id="efcba-143">Distribution lists that exist in a local container and are expanded by the client application.</span></span>
    
<span data-ttu-id="efcba-144">Свойства списка рассылки необязательно относятся следующие:</span><span class="sxs-lookup"><span data-stu-id="efcba-144">Optional distribution list properties include the following:</span></span>
  
- <span data-ttu-id="efcba-145">**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="efcba-145">**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="efcba-146">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="efcba-146">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span> 
    
- <span data-ttu-id="efcba-147">**PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="efcba-147">**PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md))</span></span> 
    
<span data-ttu-id="efcba-148">Обратите внимание на то, что **PR_ADDRTYPE** является обязательным, но не является **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="efcba-148">Notice that **PR_ADDRTYPE** is required, but **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) is not.</span></span> <span data-ttu-id="efcba-149">Вот так, как в список рассылки без адрес электронной почты по-прежнему могут получать сообщения, но необходимо развернуть список ее участников.</span><span class="sxs-lookup"><span data-stu-id="efcba-149">That is because a distribution list without an email address can still receive messages, but its member list must be expanded.</span></span> <span data-ttu-id="efcba-150">Если свойство **PR_ADDRTYPE** MAPIPDL, MAPI выполняет развертывание.</span><span class="sxs-lookup"><span data-stu-id="efcba-150">If the **PR_ADDRTYPE** property is set to MAPIPDL, MAPI performs the expansion.</span></span> <span data-ttu-id="efcba-151">Если **PR_ADDRTYPE** значение, отличное от MAPIPDL, поставщика транспорта выполняет развертывание.</span><span class="sxs-lookup"><span data-stu-id="efcba-151">If **PR_ADDRTYPE** is a value other than MAPIPDL, the transport provider performs the expansion.</span></span> 
  
<span data-ttu-id="efcba-152">Для получения дополнительных сведений о том, как использовать методы **IDistList** просмотра операций ссылку для параллельного методы **IABContainer**.</span><span class="sxs-lookup"><span data-stu-id="efcba-152">For additional information about how to use the **IDistList** methods, see the reference entries for the parallel methods of **IABContainer**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="efcba-153">См. также</span><span class="sxs-lookup"><span data-stu-id="efcba-153">See also</span></span>



[<span data-ttu-id="efcba-154">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="efcba-154">MAPI Interfaces</span></span>](mapi-interfaces.md)

