---
title: Имаилусер IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMailUser
api_type:
- COM
ms.assetid: 74c25870-62d9-484a-9a99-4dc35c52479e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a0e109fe95120483e700bab5b82f6d7cb75e2e28
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436596"
---
# <a name="imailuser--imapiprop"></a><span data-ttu-id="25c1a-103">IMailUser : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="25c1a-103">IMailUser : IMAPIProp</span></span>

  
  
<span data-ttu-id="25c1a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="25c1a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="25c1a-105">Предоставляет доступ ко многим свойствам, связанным с пользователями обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="25c1a-105">Provides access to the many properties that are associated with messaging users.</span></span> <span data-ttu-id="25c1a-106">Интерфейс **имаилусер** реализуется объектами пользователя обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="25c1a-106">The **IMailUser** interface is implemented by messaging user objects.</span></span> <span data-ttu-id="25c1a-107">**Имаилусер** наследуется от интерфейса [IMAPIProp: IUnknown](imapipropiunknown.md) и не обладает уникальными методами.</span><span class="sxs-lookup"><span data-stu-id="25c1a-107">**IMailUser** inherits from the [IMAPIProp : IUnknown](imapipropiunknown.md) interface and has no unique methods of its own.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="25c1a-108">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="25c1a-108">Header file:</span></span>  <br/> |<span data-ttu-id="25c1a-109">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="25c1a-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="25c1a-110">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="25c1a-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="25c1a-111">Объекты пользователя для обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="25c1a-111">Messaging user objects</span></span>  <br/> |
|<span data-ttu-id="25c1a-112">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="25c1a-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="25c1a-113">Поставщики адресных книг</span><span class="sxs-lookup"><span data-stu-id="25c1a-113">Address book providers</span></span>  <br/> |
|<span data-ttu-id="25c1a-114">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="25c1a-114">Called by:</span></span>  <br/> |<span data-ttu-id="25c1a-115">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="25c1a-115">Client applications</span></span>  <br/> |
|<span data-ttu-id="25c1a-116">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="25c1a-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="25c1a-117">IID_IMailUser</span><span class="sxs-lookup"><span data-stu-id="25c1a-117">IID_IMailUser</span></span>  <br/> |
|<span data-ttu-id="25c1a-118">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="25c1a-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="25c1a-119">лпмаилусер</span><span class="sxs-lookup"><span data-stu-id="25c1a-119">LPMAILUSER</span></span>  <br/> |
|<span data-ttu-id="25c1a-120">Модель транзакции:</span><span class="sxs-lookup"><span data-stu-id="25c1a-120">Transaction model:</span></span>  <br/> |<span data-ttu-id="25c1a-121">Транзакции</span><span class="sxs-lookup"><span data-stu-id="25c1a-121">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="25c1a-122">Заказ vtable</span><span class="sxs-lookup"><span data-stu-id="25c1a-122">Vtable order</span></span>

<span data-ttu-id="25c1a-123">У этого интерфейса нет уникальных методов.</span><span class="sxs-lookup"><span data-stu-id="25c1a-123">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="25c1a-124">**Обязательные свойства**</span><span class="sxs-lookup"><span data-stu-id="25c1a-124">**Required properties**</span></span>|<span data-ttu-id="25c1a-125">**Access**</span><span class="sxs-lookup"><span data-stu-id="25c1a-125">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="25c1a-126">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="25c1a-126">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="25c1a-127">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="25c1a-127">Read/write</span></span>  <br/> |
|<span data-ttu-id="25c1a-128">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="25c1a-128">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="25c1a-129">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="25c1a-129">Read/write</span></span>  <br/> |
|<span data-ttu-id="25c1a-130">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="25c1a-130">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="25c1a-131">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="25c1a-131">Read-only</span></span>  <br/> |
|<span data-ttu-id="25c1a-132">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="25c1a-132">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="25c1a-133">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="25c1a-133">Read/write</span></span>  <br/> |
|<span data-ttu-id="25c1a-134">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="25c1a-134">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="25c1a-135">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="25c1a-135">Read-only</span></span>  <br/> |
|<span data-ttu-id="25c1a-136">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="25c1a-136">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="25c1a-137">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="25c1a-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="25c1a-138">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="25c1a-138">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="25c1a-139">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="25c1a-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="25c1a-140">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="25c1a-140">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="25c1a-141">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="25c1a-141">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="25c1a-142">Примечания</span><span class="sxs-lookup"><span data-stu-id="25c1a-142">Remarks</span></span>

<span data-ttu-id="25c1a-143">Пять обязательных свойств называются свойствами базового адреса для получателей:</span><span class="sxs-lookup"><span data-stu-id="25c1a-143">Five of the required properties are known as the base address properties for recipients:</span></span>
  
- <span data-ttu-id="25c1a-144">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="25c1a-144">**PR_ADDRTYPE**</span></span>
    
- <span data-ttu-id="25c1a-145">**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="25c1a-145">**PR_DISPLAY_NAME**</span></span>
    
- <span data-ttu-id="25c1a-146">**PR_EMAIL_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="25c1a-146">**PR_EMAIL_ADDRESS**</span></span>
    
- <span data-ttu-id="25c1a-147">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="25c1a-147">**PR_ENTRYID**</span></span>
    
- <span data-ttu-id="25c1a-148">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="25c1a-148">**PR_SEARCH_KEY**</span></span>
    
<span data-ttu-id="25c1a-149">Эти свойства считаются особыми, так как многие другие группы схожих свойств создаются на основе этой базовой группы.</span><span class="sxs-lookup"><span data-stu-id="25c1a-149">These properties are considered special because many other groups of similar properties are built upon this base group.</span></span> <span data-ttu-id="25c1a-150">Другие группы используются для описания получателя в различных ролях, таких как исходный или представительный отправитель сообщения.</span><span class="sxs-lookup"><span data-stu-id="25c1a-150">The other groups are used to describe a recipient in various roles, such as a message's original or delegate sender.</span></span> <span data-ttu-id="25c1a-151">Дополнительные сведения об этих свойствах и способах их использования приведены в разделе [типы адресов MAPI](mapi-address-types.md).</span><span class="sxs-lookup"><span data-stu-id="25c1a-151">For more information about these properties and how to use them, see [MAPI Address Types](mapi-address-types.md).</span></span>
  
<span data-ttu-id="25c1a-152">Пользователи обмена сообщениями могут отображать коллекцию их свойств, поддерживающих свойство **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="25c1a-152">Messaging users can display a collection of their properties by supporting the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property.</span></span> <span data-ttu-id="25c1a-153">**PR_DETAILS_TABLE** — это таблица, описывающая макет диалогового окна сведений или страницы свойств с вкладками, в которой отображаются сведения о свойствах получателя.</span><span class="sxs-lookup"><span data-stu-id="25c1a-153">**PR_DETAILS_TABLE** is a display table that describes the layout of a details dialog box or a tabbed property page that displays recipient property information.</span></span> <span data-ttu-id="25c1a-154">MAPI создает диалоговые окна сведений, когда клиент вызывает метод [IAddrBook::D етаилс](iaddrbook-details.md) .</span><span class="sxs-lookup"><span data-stu-id="25c1a-154">MAPI creates details dialog boxes when a client calls the [IAddrBook::Details](iaddrbook-details.md) method.</span></span> 
  
<span data-ttu-id="25c1a-155">Пользовательские объекты обмена сообщениями могут иметь другие связанные с ними дополнительные свойства.</span><span class="sxs-lookup"><span data-stu-id="25c1a-155">Messaging user objects can have other optional properties associated with them.</span></span> <span data-ttu-id="25c1a-156">MAPI определяет множество свойств, которые предоставляют дополнительные сведения об адресе пользователя для обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="25c1a-156">MAPI defines many properties that provide additional addressing information about a messaging user.</span></span> <span data-ttu-id="25c1a-157">Все эти свойства являются символьными строками.</span><span class="sxs-lookup"><span data-stu-id="25c1a-157">All of these properties are character strings.</span></span> <span data-ttu-id="25c1a-158">В следующем списке приведены наиболее часто используемые свойства:</span><span class="sxs-lookup"><span data-stu-id="25c1a-158">The following list shows the more commonly used properties:</span></span>
  
- <span data-ttu-id="25c1a-159">**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="25c1a-159">**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))</span></span> 
    
- <span data-ttu-id="25c1a-160">**PR_ASSISTANT** ([PidTagAssistant](pidtagassistant-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="25c1a-160">**PR_ASSISTANT** ([PidTagAssistant](pidtagassistant-canonical-property.md))</span></span> 
    
- <span data-ttu-id="25c1a-161">**PR_BUSINESS_TELEPHONE_NUMBER** ([PidTagBusinessTelephoneNumber](pidtagbusinesstelephonenumber-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="25c1a-161">**PR_BUSINESS_TELEPHONE_NUMBER** ([PidTagBusinessTelephoneNumber](pidtagbusinesstelephonenumber-canonical-property.md))</span></span> 
    
- <span data-ttu-id="25c1a-162">**PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="25c1a-162">**PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))</span></span> 
    
- <span data-ttu-id="25c1a-163">**PR_GOVERNMENT_ID_NUMBER** ([PidTagGovernmentIdNumber](pidtaggovernmentidnumber-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="25c1a-163">**PR_GOVERNMENT_ID_NUMBER** ([PidTagGovernmentIdNumber](pidtaggovernmentidnumber-canonical-property.md))</span></span> 
    
- <span data-ttu-id="25c1a-164">**PR_LOCALITY** ([PidTagLocality](pidtaglocality-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="25c1a-164">**PR_LOCALITY** ([PidTagLocality](pidtaglocality-canonical-property.md))</span></span> 
    
- <span data-ttu-id="25c1a-165">**PR_POSTAL_ADDRESS** ([PidTagPostalAddress](pidtagpostaladdress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="25c1a-165">**PR_POSTAL_ADDRESS** ([PidTagPostalAddress](pidtagpostaladdress-canonical-property.md))</span></span> 
    
<span data-ttu-id="25c1a-166">Полный список свойств приведен [в разделе Сопоставление канонических имен свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md).</span><span class="sxs-lookup"><span data-stu-id="25c1a-166">For a complete list of properties, see [Mapping Canonical Property Names to MAPI Names](mapping-canonical-property-names-to-mapi-names.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="25c1a-167">См. также</span><span class="sxs-lookup"><span data-stu-id="25c1a-167">See also</span></span>



[<span data-ttu-id="25c1a-168">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="25c1a-168">MAPI Interfaces</span></span>](mapi-interfaces.md)

