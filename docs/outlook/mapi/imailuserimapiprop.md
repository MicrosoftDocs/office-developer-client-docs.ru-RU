---
title: IMailUser IMAPIProp
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
ms.openlocfilehash: 0c70d16d294426d30f3ac5f00b6bc46992386a86
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808824"
---
# <a name="imailuser--imapiprop"></a><span data-ttu-id="5beae-103">IMailUser : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="5beae-103">IMailUser : IMAPIProp</span></span>

  
  
<span data-ttu-id="5beae-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5beae-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5beae-105">Предоставляет доступ к много свойств, связанных с системой обмена сообщениями пользователи.</span><span class="sxs-lookup"><span data-stu-id="5beae-105">Provides access to the many properties that are associated with messaging users.</span></span> <span data-ttu-id="5beae-106">Интерфейс **IMailUser** реализуется системы обмена сообщениями объектов-пользователей.</span><span class="sxs-lookup"><span data-stu-id="5beae-106">The **IMailUser** interface is implemented by messaging user objects.</span></span> <span data-ttu-id="5beae-107">**IMailUser** наследует от [IMAPIProp: IUnknown](imapipropiunknown.md) интерфейс и не имеет уникальное методов свои собственные.</span><span class="sxs-lookup"><span data-stu-id="5beae-107">**IMailUser** inherits from the [IMAPIProp : IUnknown](imapipropiunknown.md) interface and has no unique methods of its own.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5beae-108">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="5beae-108">Header file:</span></span>  <br/> |<span data-ttu-id="5beae-109">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5beae-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="5beae-110">Предоставляемые:</span><span class="sxs-lookup"><span data-stu-id="5beae-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="5beae-111">Обмен сообщениями объектов-пользователей</span><span class="sxs-lookup"><span data-stu-id="5beae-111">Messaging user objects</span></span>  <br/> |
|<span data-ttu-id="5beae-112">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="5beae-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="5beae-113">Поставщиками адресных книг</span><span class="sxs-lookup"><span data-stu-id="5beae-113">Address book providers</span></span>  <br/> |
|<span data-ttu-id="5beae-114">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="5beae-114">Called by:</span></span>  <br/> |<span data-ttu-id="5beae-115">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="5beae-115">Client applications</span></span>  <br/> |
|<span data-ttu-id="5beae-116">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="5beae-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="5beae-117">IID_IMailUser</span><span class="sxs-lookup"><span data-stu-id="5beae-117">IID_IMailUser</span></span>  <br/> |
|<span data-ttu-id="5beae-118">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="5beae-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="5beae-119">LPMAILUSER</span><span class="sxs-lookup"><span data-stu-id="5beae-119">LPMAILUSER</span></span>  <br/> |
|<span data-ttu-id="5beae-120">Модель транзакций:</span><span class="sxs-lookup"><span data-stu-id="5beae-120">Transaction model:</span></span>  <br/> |<span data-ttu-id="5beae-121">В транзакции</span><span class="sxs-lookup"><span data-stu-id="5beae-121">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="5beae-122">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="5beae-122">Vtable order</span></span>

<span data-ttu-id="5beae-123">Этот интерфейс не имеет каких-либо уникальных методов.</span><span class="sxs-lookup"><span data-stu-id="5beae-123">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="5beae-124">**Обязательные свойства**</span><span class="sxs-lookup"><span data-stu-id="5beae-124">**Required properties**</span></span>|<span data-ttu-id="5beae-125">**Access**</span><span class="sxs-lookup"><span data-stu-id="5beae-125">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5beae-126">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5beae-126">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5beae-127">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="5beae-127">Read/write</span></span>  <br/> |
|<span data-ttu-id="5beae-128">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5beae-128">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5beae-129">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="5beae-129">Read/write</span></span>  <br/> |
|<span data-ttu-id="5beae-130">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5beae-130">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5beae-131">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="5beae-131">Read-only</span></span>  <br/> |
|<span data-ttu-id="5beae-132">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5beae-132">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5beae-133">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="5beae-133">Read/write</span></span>  <br/> |
|<span data-ttu-id="5beae-134">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5beae-134">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5beae-135">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="5beae-135">Read-only</span></span>  <br/> |
|<span data-ttu-id="5beae-136">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5beae-136">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5beae-137">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="5beae-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="5beae-138">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5beae-138">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5beae-139">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="5beae-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="5beae-140">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5beae-140">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5beae-141">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="5beae-141">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5beae-142">Замечания</span><span class="sxs-lookup"><span data-stu-id="5beae-142">Remarks</span></span>

<span data-ttu-id="5beae-143">Пять необходимые свойства называются свойствами базовый адрес для получателей:</span><span class="sxs-lookup"><span data-stu-id="5beae-143">Five of the required properties are known as the base address properties for recipients:</span></span>
  
- <span data-ttu-id="5beae-144">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="5beae-144">**PR_ADDRTYPE**</span></span>
    
- <span data-ttu-id="5beae-145">**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="5beae-145">**PR_DISPLAY_NAME**</span></span>
    
- <span data-ttu-id="5beae-146">**PR_EMAIL_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="5beae-146">**PR_EMAIL_ADDRESS**</span></span>
    
- <span data-ttu-id="5beae-147">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="5beae-147">**PR_ENTRYID**</span></span>
    
- <span data-ttu-id="5beae-148">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="5beae-148">**PR_SEARCH_KEY**</span></span>
    
<span data-ttu-id="5beae-149">Эти свойства рассматриваются особые, поскольку количество групп свойств, аналогичное основаны на это базовая группа.</span><span class="sxs-lookup"><span data-stu-id="5beae-149">These properties are considered special because many other groups of similar properties are built upon this base group.</span></span> <span data-ttu-id="5beae-150">Другие группы используются для описания получателя с разными ролями, такие как исходное сообщение или делегирование отправителя.</span><span class="sxs-lookup"><span data-stu-id="5beae-150">The other groups are used to describe a recipient in various roles, such as a message's original or delegate sender.</span></span> <span data-ttu-id="5beae-151">Дополнительные сведения об этих свойств и как их использовать можно [Типов адресов MAPI](mapi-address-types.md).</span><span class="sxs-lookup"><span data-stu-id="5beae-151">For more information about these properties and how to use them, see [MAPI Address Types](mapi-address-types.md).</span></span>
  
<span data-ttu-id="5beae-152">Пользователи системы обмена сообщениями можно отобразить коллекцию их свойств за счет свойство **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5beae-152">Messaging users can display a collection of their properties by supporting the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property.</span></span> <span data-ttu-id="5beae-153">**PR_DETAILS_TABLE** — это таблица отображения, который описывает макет страницы с вкладками свойство, которое отображает сведения о свойствах получателей или диалоговое окно сведений.</span><span class="sxs-lookup"><span data-stu-id="5beae-153">**PR_DETAILS_TABLE** is a display table that describes the layout of a details dialog box or a tabbed property page that displays recipient property information.</span></span> <span data-ttu-id="5beae-154">MAPI создает сведения о диалоговых окнах, если клиент вызывает метод [IAddrBook::Details](iaddrbook-details.md) .</span><span class="sxs-lookup"><span data-stu-id="5beae-154">MAPI creates details dialog boxes when a client calls the [IAddrBook::Details](iaddrbook-details.md) method.</span></span> 
  
<span data-ttu-id="5beae-155">Обмен сообщениями объектов-пользователей может иметь другие дополнительные свойства, связанные с ними.</span><span class="sxs-lookup"><span data-stu-id="5beae-155">Messaging user objects can have other optional properties associated with them.</span></span> <span data-ttu-id="5beae-156">MAPI определяет множество свойств, которые обеспечивают дополнительные адресации сведений о пользователе обмена мгновенными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="5beae-156">MAPI defines many properties that provide additional addressing information about a messaging user.</span></span> <span data-ttu-id="5beae-157">Все эти свойства, строк символов.</span><span class="sxs-lookup"><span data-stu-id="5beae-157">All of these properties are character strings.</span></span> <span data-ttu-id="5beae-158">В следующем списке приведены наиболее часто используемые свойства:</span><span class="sxs-lookup"><span data-stu-id="5beae-158">The following list shows the more commonly used properties:</span></span>
  
- <span data-ttu-id="5beae-159">**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5beae-159">**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))</span></span> 
    
- <span data-ttu-id="5beae-160">**PR_ASSISTANT** ([PidTagAssistant](pidtagassistant-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5beae-160">**PR_ASSISTANT** ([PidTagAssistant](pidtagassistant-canonical-property.md))</span></span> 
    
- <span data-ttu-id="5beae-161">**PR_BUSINESS_TELEPHONE_NUMBER** ([PidTagBusinessTelephoneNumber](pidtagbusinesstelephonenumber-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5beae-161">**PR_BUSINESS_TELEPHONE_NUMBER** ([PidTagBusinessTelephoneNumber](pidtagbusinesstelephonenumber-canonical-property.md))</span></span> 
    
- <span data-ttu-id="5beae-162">**PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5beae-162">**PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))</span></span> 
    
- <span data-ttu-id="5beae-163">**PR_GOVERNMENT_ID_NUMBER** ([PidTagGovernmentIdNumber](pidtaggovernmentidnumber-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5beae-163">**PR_GOVERNMENT_ID_NUMBER** ([PidTagGovernmentIdNumber](pidtaggovernmentidnumber-canonical-property.md))</span></span> 
    
- <span data-ttu-id="5beae-164">**PR_LOCALITY** ([PidTagLocality](pidtaglocality-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5beae-164">**PR_LOCALITY** ([PidTagLocality](pidtaglocality-canonical-property.md))</span></span> 
    
- <span data-ttu-id="5beae-165">**PR_POSTAL_ADDRESS** ([PidTagPostalAddress](pidtagpostaladdress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5beae-165">**PR_POSTAL_ADDRESS** ([PidTagPostalAddress](pidtagpostaladdress-canonical-property.md))</span></span> 
    
<span data-ttu-id="5beae-166">Полный список свойств в разделе [Сопоставление каноническое имена свойств, чтобы имена MAPI](mapping-canonical-property-names-to-mapi-names.md).</span><span class="sxs-lookup"><span data-stu-id="5beae-166">For a complete list of properties, see [Mapping Canonical Property Names to MAPI Names](mapping-canonical-property-names-to-mapi-names.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5beae-167">См. также</span><span class="sxs-lookup"><span data-stu-id="5beae-167">See also</span></span>



[<span data-ttu-id="5beae-168">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="5beae-168">MAPI Interfaces</span></span>](mapi-interfaces.md)

